---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Journey-Ereignissen
description: Erfahren Sie, wie Sie mit Ereignissen in Ihren Journeys arbeiten.
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: Ereignisse, Ereignis, Journey, Definition, Starten
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
TQID: https://experienceleague.adobe.com/xvLSBd-rwKKNqwQNDa4D8GfFzc-ND1FkC3EdstufkIY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 6657a77a27455643fa0fb3d94a4d7e3ab83e6843
workflow-type: tm+mt
source-wordcount: 2407
ht-degree: 29%

---

# Arbeiten mit Journey-Ereignissen {#about-events}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Hier erfahren Sie mehr über die drei Ereignistypen, ihre Schemaanforderungen und die wichtigsten Einschränkungen und darüber, wie Sie den richtigen für Ihren Anwendungsfall auswählen.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Journey-Ereignisse"
>abstract="Journey Optimizer unterstützt in Journeys drei Ereignistypen: unitäre Ereignisse, die mit dem Verhalten einer bestimmten Person verknüpft sind (z. B. ein Kauf oder ein Treuemeilenstein), Geschäftsereignisse, die durch ein globales Ereignis ausgelöst werden (z. B. eine Flugstornierung oder ein Aktien-Update), und Zielgruppen-Qualifizierungsereignisse, die ausgelöst werden, wenn ein Profil in eine Zielgruppe aufgenommen wird oder aus einer Zielgruppe aussteigt. Verwenden Sie Ereignisse, um Journeys auszulösen und die richtigen Aktionen für Ihre Profile zu orchestrieren."

Ereignisse ermöglichen es, Journeys einzeln auszulösen und allen Benutzenden beim Eintritt in die Journey Nachrichten in Echtzeit zu senden. In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Sie können mehrere Ereignisse (in verschiedenen Schritten der Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

Die Ereigniskonfiguration ist **obligatorisch** und muss vom Daten-Engineering durchgeführt werden.

>[!IMPORTANT]
>
>* Stellen Sie vor dem Konfigurieren von Ereignissen Folgendes sicher: die Rolle **Journey Optimizer-** oder **Datentechniker**, ein XDM-Schema mit aktiviertem **Echtzeit-**, einen aktiven Streaming-Endpunkt und Zugriff auf die richtige Sandbox.
>
>* Ereignisanforderungen und -beschränkungen (Streaming, Abfrage-Service, Batch-Aufnahme) finden Sie unter [Journey-Leitplanken - Ereignisse](../start/guardrails.md#events-g).

**Wer macht was:**

| Aufgabe | Rolle |
| --- | --- |
| Entwerfen und Erstellen des XDM-Schemas | Datentechniker |
| Einrichten des Streaming-Endpunkts | Datentechniker |
| Konfigurieren von unitären und Geschäftsereignissen (**Administration > Ereignisse**) | Datentechniker oder Administrator |
| Verwenden von Ereignissen in einem Journey | Journey Practitioner |
| Zielgruppen-Qualifizierungsereignisse konfigurieren (auf der Arbeitsfläche ausgewählt) | Journey Practitioner |

Sie können drei Ereignistypen konfigurieren: **Unitäre Ereignisse**, **Geschäftsereignisse** und **Zielgruppen-Qualifizierungsereignisse**.

➡️ [Funktion im Video kennenlernen](#video)

➡️ [Funktion im Video kennenlernen](#video)

## Unitäre Ereignisse {#unitary-events}

**Unitäre** Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person verknüpft ist (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unitäre Ereignisse können regelbasiert oder systemgeneriert sein. [Erfahren Sie, wie Sie ein unitäres Ereignis erstellen](../event/about-creating.md).

**Schemaanforderung:** Ein XDM ExperienceEvent-Schema mit einer personenbasierten primären Identität und aktiviertem **Echtzeit** Kundenprofil.

**Beispiel:** Ein Kunde fügt Artikel zu seinem Warenkorb hinzu und schließt den Browser. Wenn ein Warenkorbabbruch ausgelöst wird, gelangt das Profil in Echtzeit auf die Journey und erhält eine Stunde später eine Wiederherstellungs-E-Mail.

>[!NOTE]
>
>Die Journey beinhalten eine Leitplanke für den erneuten Eintritt: Der erneute Profileintritt ist nach dem Journey-Trigger standardmäßig 5 Minuten lang blockiert. Wenn beispielsweise ein Ereignis den Trigger einer Journey bei 12% für ein :01 und ein weiteres bei 12:03 eintrifft, wird die Journey für dieses Profil nicht neu gestartet.

## Geschäftsereignisse {#business-events}

**Geschäftsereignisse** sind nicht mit einem bestimmten Profil verknüpft. Dabei kann es sich beispielsweise um eine Nachrichtenmeldung, Sportaktualisierung, eine Änderung oder Annullierung eines Fluges, eine Bestandsaktualisierung oder um Wetterereignisse handeln. Diese Ereignisse sind zwar nicht profilspezifisch, können aber für eine beliebige Anzahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichtenthemen abonniert haben, Passagiere eines Fluges oder Kunden, die an einem nicht vorrätigen Produkt interessiert sind. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis auf einer Journey ablegen, wird automatisch eine Aktivität **Zielgruppe lesen** unmittelbar danach hinzugefügt. [Erfahren Sie, wie Sie ein Geschäftsereignis erstellen](../event/about-creating-business.md).

**Schemaanforderung:** Ein XDM-Schema für eine Zeitreihe mit einer primären Identität für Nicht-Personen, und die `_id`- und `timestamp` werden ausgefüllt. Planen Sie eine Verzögerung des Zielgruppenexports von 15 Minuten bis zu einer Stunde ein.

**Beispiel** Eine Fluggesellschaft annulliert einen Flug. Ein Geschäftsereignis wird ausgelöst, [!DNL Journey Optimizer] liest die Zielgruppe der betroffenen Passagiere und sendet ihnen jeweils eine Umbuchungsbenachrichtigung.

## Zielgruppen-Qualifizierungsereignisse {#audience-qualification-events}

Ein **Zielgruppen-Qualifizierungsereignis** wird ausgelöst, wenn ein Profil in eine Zielgruppe eintritt oder diese verlässt. Beispiel: Kunden, die einen Schwellenwert für Treueausgaben überschreiten, werden in die Zielgruppe der Gold-Stufe aufgenommen, d. h., bei der Qualifizierung wird die Journey für dieses Profil in Echtzeit (für Streaming-Zielgruppen) oder bei der nächsten Batch-Auswertung Trigger. Im Gegensatz zu unitären Ereignissen können Sie mit der Zielgruppen-Qualifizierung eine komplexe Trigger-Logik erstellen, indem Sie die volle Leistungsfähigkeit von Zielgruppendefinitionen nutzen, ohne dass Implementierungsänderungen erforderlich sind, um ein neues Ereignis zu senden. Weitere Informationen zu [Zielgruppen-Qualifizierungsereignissen](../building-journeys/audience-qualification-events.md).

**Schemaanforderung:** zusätzliches Schema erforderlich — das Ereignis beruht auf bestehenden Zielgruppendefinitionen, die bereits in Adobe Experience Platform erstellt wurden.

**Beispiel** Die Treueausgaben eines Kunden überschreiten den Gold-Stufen-Schwellenwert. Ihr Profil qualifiziert sich für das Gold-Publikum, die Journey-Trigger automatisch und sendet eine Willkommensbelohnung.

>[!NOTE]
>
>Zielgruppen-Qualifizierungsereignisse werden nicht in **Administration > Ereignisse** konfiguriert, sondern direkt auf der Journey-Arbeitsfläche als erster Schritt einer Journey ausgewählt.

## Ereignistypen auf einen Blick {#event-comparison}

| | Unitäres Ereignis | Geschäftsereignis | Zielgruppen-Qualifizierungsereignis |
| --- | --- | --- | --- |
| **Mit einem Profil verknüpft?** | Ja - ausgelöst durch die Aktion einer bestimmten Person. | Nein — ausgelöst durch ein externes Ereignis, das nicht an eine Person gebunden ist. | Ja - Wird ausgelöst, wenn ein Profil eine Zielgruppe betritt oder verlässt. |
| **Eintrittsverhalten** | Ein Profil gelangt in Echtzeit auf die Journey. | Mehrere Profile treten über einen automatischen Schritt „Zielgruppe lesen“ ein. | Ein Profil tritt ein, wenn sich die Zielgruppenzugehörigkeit ändert. |
| **Typische Anwendungsfälle** | Warenkorbabbruch, Wiederherstellung, Formularübermittlung, App-Anmeldung, Treuemeilenstein. | Flugstornierung, Warnhinweis bezüglich der Bestandsauffüllung, aktuelle Nachrichten, Wetterereignis. | Erneute Interaktion abgelaufener Kundinnen und Kunden, Änderungen der Treuestufe, VIP-Offboarding-Abläufe. |
| **Wie startet man die Journey** | Ereignisbasierter Eintrag - keine Zielgruppe erforderlich. | Geschäftsereignis + automatische Zielgruppe lesen (von Journey Optimizer hinzugefügt). | Profil tritt in eine definierte Zielgruppe ein oder verlässt diese. |
| **Mehrere pro Journey?** | Ja, Sie können mehrere unitäre Ereignisse über Journey-Schritte hinweg überwachen. | Nein - nur ein Geschäftsereignis pro Journey, platziert am Anfang. | Ja - kann mit anderen Aktivitäten kombiniert werden. |
| **Ereignis-ID-Typ** | Regelbasiert oder systemgeneriert. | Immer regelbasiert. | Keine Ereignis-ID — basierend auf der Auswertung der Zielgruppenzugehörigkeit. |
| **In Administration konfiguriert?** | Ja | Ja | Nein — direkt auf der Journey-Arbeitsfläche ausgewählt. |

>[!NOTE]
>
>Eine Journey kann nur **ein** Geschäftsereignis enthalten, bei dem es sich um die erste Aktivität handeln muss. Journey Optimizer fügt nach der Aktivität automatisch die Aktivität **Zielgruppe lesen** hinzu, um zu definieren, welche Profile die von diesem Ereignis ausgelöste Journey erhalten.

## Ereignis-ID-Typ {#event-id-type}

Bei **Geschäftsereignissen** ist der Ereignis-ID-Typ immer regelbasiert.

Bei **unitären** Ereignissen sind zwei Typen von Ereignis-IDs möglich:

* **Regelbasierte** Ereignisse: Dieser Ereignistyp generiert keine eventID. Mit dem einfachen Ausdruckseditor definieren Sie einfach eine Regel, anhand derer das System die relevanten Ereignisse identifiziert, die Ihre Journeys auslösen. Diese Regel kann auf einem beliebigen Feld basieren, das in der Ereignis-Payload verfügbar ist, z. B. dem Standort des Profils oder der Anzahl der Artikel, die dem Warenkorb des Profils hinzugefügt wurden.

  >[!CAUTION]
  >
  >Für regelbasierte Ereignisse wird eine Begrenzungsregel definiert. Die Anzahl der qualifizierten Ereignisse, die eine Journey für eine bestimmte Organisation verarbeiten kann, wird durch die Regel auf 5.000 pro Sekunde begrenzt. Dies entspricht den Journey Optimizer-SLAs. Weitere Informationen finden Sie in Ihrer Journey Optimizer-Lizenz und in der [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* **Systemgenerierte** Ereignisse: für diese Ereignisse ist eine eventID erforderlich. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis per Push sendet, sollte keine ID generieren, sondern die ID übergeben, die in der Payload-Vorschau verfügbar ist.

>[!NOTE]
>
>Nur Streaming-Ereignisse können Journey-Trigger auslösen. Folgende(**)** zum Trigger einer Journey verwendet werden:
>
>* In Batch aufgenommene Ereignisse
>* Ereignisse eingefügt über **Abfrage-Service**
>* Ereignisse aus internen [!DNL Journey Optimizer] (Nachrichten-Feedback, E-Mail-Tracking und Ähnliches)
>
>Wenn Sie keine Streaming-Ereignisse empfangen können, erstellen Sie eine auf diesen Ereignissen basierende Zielgruppe und verwenden Sie stattdessen die Aktivität **Zielgruppe lesen** . Um Ereignisse nur für die Segmentierung zu verwenden, aktivieren Sie den Datensatz für **Echtzeit-Kundenprofil**.

## Auswahlmöglichkeiten {#choose-event-type}

Verwenden Sie die folgenden Kriterien, um den richtigen Ereignistyp für Ihren Journey auszuwählen - die Schlüsselfrage ist: **Lösen Sie eine Aktion für eine bestimmte Person aus oder senden Sie sie an viele Profile?** [Weitere Informationen zu Journey-Typen](../building-journeys/journey.md#journey-types).

Jeder Ereignistyp wird einem bestimmten Journey-Muster zugeordnet:

| Ereignistyp | Journey-Muster |
| --- | --- |
| Unitäres Ereignis | Echtzeit-Journey mit einem Profil - Trigger sofort, wenn eine Person handelt |
| Geschäftsereignis | Versand-Journey - Targeting vieler Profile über einen automatischen Schritt „Zielgruppe lesen“ |
| Zielgruppen-Qualifizierungsereignis | Segmentausgelöstes Journey - Wird ausgelöst, wenn ein Profil eine Zielgruppe betritt oder verlässt |

* **Wählen Sie ein unitäres** aus, wenn der Trigger an eine bestimmte Person gebunden ist, z. B. an einen Kauf, eine Formularübermittlung oder einen Treuemeilenstein. Unitäre Ereignisse erfordern eine personenbasierte primäre Identität im Schema und starten die Journey sofort für dieses Profil. [Erfahren Sie, wie Sie ein unitäres Ereignis konfigurieren](../event/about-creating.md).

* **Wählen Sie ein Geschäftsereignis aus** wenn der Trigger ein globales Ereignis ist - z. B. eine Wiederverfügbarkeit eines Produkts, ein Preisverfall oder eine Flugannullierung - und Sie an eine Reihe von Profilen senden möchten, die mit diesem Signal in Verbindung stehen. Geschäftsereignisse müssen der erste Schritt auf dem Journey sein und Profile automatisch über die Aktivität „Zielgruppe lesen **ansprechen**. Sie erfordern ein Zeitreihenschema mit einer primären Identität für Nicht-Personen und den `_id`- und `timestamp`. Planen Sie eine Verzögerung des Zielgruppenexports von 15 Minuten bis zu einer Stunde ein. [Erfahren Sie, wie Sie ein Geschäftsereignis konfigurieren](../event/about-creating-business.md).

* **Wählen Sie ein Zielgruppen-Qualifizierungsereignis** wenn es sich bei dem Trigger um ein Profil handelt, das in eine Zielgruppe eintritt oder diese verlässt, und Sie eine komplexere Segmentierungslogik benötigen, als ein einzelnes Ereignis bereitstellen kann. So können Sie beispielsweise abgelaufene Kundinnen und Kunden, die gerade einen Ausgabenschwellenwert erreicht haben, erneut ansprechen oder einen Offboarding-Fluss auslösen, wenn ein VIP-Mitglied die Treuestufe verlässt. [Weitere Informationen zu Zielgruppen-Qualifizierungsereignissen](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Geschäftsereignisse können nicht auf derselben Journey wie unitäre Ereignisse oder Zielgruppen-Qualifizierungsaktivitäten verwendet werden.

## Wichtige Einschränkungen {#key-constraints}

Verwenden Sie diese Zusammenfassung, um Ihre Implementierung zu planen, bevor Sie Ereignisse konfigurieren.

| Beschränkung | Details |
| --- | --- |
| Durchsatzgrenze | 5.000 Ereignisse pro Sekunde und Organisation in allen Sandboxes (unitär und Journey mit gelesener Zielgruppe) |
| Wiedereintrittsblock | Erneuter Profileintritt für 5 Minuten nach einem unitären Journey-Trigger blockiert |
| Geschäftsereignisse pro Journey | Maximal 1, muss der erste Schritt sein |
| Business + Unitäres in einer Journey kombinieren | Nicht unterstützt |
| Batch-Ereignisse | Journey können nicht Trigger werden - Verwenden Sie stattdessen **Aktivität „Zielgruppe lesen** . |
| Zielgruppen-Qualifizierung - Administration | Nicht konfiguriert in **Administration > Ereignisse** — direkt auf der Journey-Arbeitsfläche ausgewählt |
| Live-Ereignis bearbeiten | Nur der Name und die Beschreibung können geändert oder Payload-Felder hinzugefügt werden |

## So erreichen Ereignisse Journey Optimizer {#data-cycle}

Ereignisse müssen als POST-Aufrufe über [Adobe Experience Platform-Streaming-Aufnahme-APIs an [!DNL Journey Optimizer] gesendet &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de){target="_blank"}. Die Payload muss der XDM-Formatierung entsprechen und für das Ereignisschema muss **Echtzeit-Kundenprofil** aktiviert sein.

Es werden sowohl authentifizierte als auch nicht authentifizierte Streaming-Modi unterstützt. Batch-aufgenommene Ereignisse und Ereignisse aus internen [!DNL Journey Optimizer]-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking und Ähnliches) können nicht zum Trigger von Journey verwendet werden. Verwenden Sie stattdessen eine Aktivität **Zielgruppe lesen** für diese Anwendungsfälle.


## Grenzwerte für Ereignisdurchsatz {#event-throughput}

Adobe Journey Optimizer erzwingt für alle Sandboxes separate Durchsatzbeschränkungen pro Ereignistyp auf Unternehmensebene:

* **Unitäre Ereignisse**: 5.000 Ereignisse pro Sekunde
* **Zielgruppenbasierte Journey-Ereignisse lesen**: 5.000 Ereignisse pro Sekunde

Diese Beschränkungen gelten für alle Ereignisse, die in aktiven Journey verwendet werden, einschließlich **Live**, **Dry Run**, **Closed** und **Paused** Journey. Wenn ein Limit erreicht wird, werden neue Ereignisse mit 5.000 pro Sekunde in die Warteschlange gestellt und verarbeitet, bis die Warteschlange abgelaufen ist.

Weitere Informationen zu Journey-Verarbeitungsraten und wie sich verschiedene Journey-Typen auf den Durchsatz auswirken, finden [&#x200B; unterWeitere Informationen zu Journey-Verarbeitungsraten](../building-journeys/entry-management.md#journey-processing-rate).

Die folgenden Ereignistypen werden für diese Kontingente gezählt:

* **Externe unitäre Ereignisse**: Umfasst sowohl regelbasierte als auch systemgenerierte Ereignisse. Wenn dasselbe Rohereignis für mehrere Regeldefinitionen qualifiziert ist, zählt jede übereinstimmende Regel als separates Ereignis für das Kontingent.

* **Zielgruppen-Qualifizierungsereignisse**: Wenn dieselbe Streaming-Zielgruppe in verschiedenen Journeys zum Einsatz kommt, wird jede Verwendung separat gezählt. Wird dieselbe Zielgruppe beispielsweise in einer Zielgruppen-Qualifizierungsaktivität in zwei Journeys verwendet, werden zwei Ereignisse gezählt.

* **Reaktionsereignisse**: Ereignisse, die durch Profilreaktionen ausgelöst werden (geöffnete E-Mail, angeklickte E-Mail usw.) innerhalb einer Journey.

* **Geschäftsereignisse**: Ereignisse, die nicht an ein bestimmtes Profil gebunden sind, sondern an ein geschäftsbezogenes Ereignis.

* **Analytics-Ereignisse**: Wenn die [Integration mit Adobe Analytics zum Auslösen von Journeys](about-analytics.md) aktiviert wurde, sind diese Ereignisse ebenfalls Teil des Umfangs.

* **Fortsetzungsereignisse**: Technisches Ereignis, das ausgelöst wird, wenn ein Profil von einer angehaltenen Journey aus fortgesetzt wird. Erfahren Sie mehr über das [Fortsetzen angehaltener Journeys](../building-journeys/journey-pause.md#journey-resume-steps).

* **Abschlussereignisse von Warteknoten**: Wenn ein Profil einen Warteknoten verlässt, wird ein technisches Ereignis generiert, um die Journey fortzusetzen.

>[!NOTE]
>
>Mit Ausnahme von Warte- und Fortsetzungsereignissen werden alle anderen Ereignistypen ebenfalls auf das Kontingent angerechnet, wenn sie in Journeys auf Grundlage von „Zielgruppen lesen“ verwendet werden.

## Aktualisieren und Löschen eines Ereignisses {#update-event}


Um Unterbrechungen vorhandener Journeys zu vermeiden, wenn Sie ein Ereignis bearbeiten, das in einer **Entwurfs**-, **Live**- oder **geschlossenen** Journey verwendet wird, können Sie nur den Namen bzw. die Beschreibung ändern oder Payload-Felder hinzufügen.

Jedes Ereignis, das in **Live**-, **Entwurfs**- oder **geschlossenen** Journeys verwendet wird, kann nicht gelöscht werden. Um ein verwendetes Ereignis zu löschen, müssen Sie dessen Verwendung durch die Journey unterbrechen und/oder es aus den Journey des Entwurfs entfernen, in dem es verwendet wird. Sie können das Feld **[!UICONTROL Verwendet in]** überprüfen. Es zeigt die Anzahl der Journeys an, die dieses bestimmte Ereignis verwenden. Sie können auf die Schaltfläche **[!UICONTROL Customer Journeys anzeigen]** klicken, um die Liste der entsprechenden Journeys zu öffnen.

## Häufig gestellte Fragen {#faq}

**Kann ich dasselbe Ereignis in mehreren Journey verwenden?**
Ja. Mehrere Journey können gleichzeitig dasselbe Ereignis hören.

**Kann ich ein Geschäftsereignis und ein unitäres Ereignis auf derselben Journey kombinieren?**
Nein - Geschäftsereignisse können nicht auf derselben Journey wie unitäre Ereignisse oder Zielgruppen-Qualifizierungsaktivitäten verwendet werden.

**Muss ich etwas für Zielgruppen-Qualifizierungsereignisse konfigurieren?**
Nein - Zielgruppen-Qualifizierungsereignisse werden nicht in **Administration > Ereignisse** konfiguriert. Wählen Sie als ersten Schritt die Audience direkt auf der Journey-Arbeitsfläche aus.

**Kann ich Batch-aufgenommene Daten für den Trigger einer Journey verwenden?**
Nein - Journey können nur durch gestreamte Ereignisse Trigger werden. Erstellen Sie für Batch-Daten eine Zielgruppe und verwenden Sie stattdessen **Aktivität „Zielgruppe lesen** .

**Mein Journey wird nicht ausgelöst - was soll ich überprüfen?**

* Stellen Sie sicher, dass für Ihr Ereignisschema **Echtzeit-Kundenprofil** aktiviert ist.
* Vergewissern Sie sich, dass Ereignisse gestreamt werden - Batch-aufgenommene Ereignisse können keine Trigger-Journey auslösen.
* Überprüfen Sie bei regelbasierten Ereignissen, ob die Regelbedingung mit den eingehenden Payload-Feldern übereinstimmt.
* Vergewissern Sie sich, dass sich die Journey im **Live**-Status befindet und dass das Profil alle Einstiegsbedingungen erfüllt.

## Nächste Schritte {#next-steps}

* [Konfigurieren eines unitären Ereignisses](../event/about-creating.md)
* [Konfigurieren eines Geschäftsereignisses](../event/about-creating-business.md)
* [Weitere Informationen zu Zielgruppen-Qualifizierungsereignissen](../building-journeys/audience-qualification-events.md)
* [Verwalten des Eintritts und erneuten Eintritts von Journey](../building-journeys/entry-management.md)

>[!TIP]
>
>Wenn Ihr Journey nicht ausgelöst wird, stellen Sie sicher, dass für Ihr Ereignisschema **Echtzeit-Kundenprofil** aktiviert ist und dass Ereignisse gestreamt werden - Batch-aufgenommene Ereignisse können keine Trigger-Journey auslösen.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie ein Ereignis konfigurieren und den Streaming-Endpunkt und die Payload für ein Ereignis angeben.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Machen Sie sich mit den entsprechenden Anwendungsfällen für Geschäftsereignisse vertraut. Erfahren Sie, wie Sie mithilfe eines Geschäftsereignisses eine Journey erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
