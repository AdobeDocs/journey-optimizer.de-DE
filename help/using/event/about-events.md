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
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 2152
ht-degree: 68%

---

# Arbeiten mit Journey-Ereignissen {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Journey-Ereignisse"
>abstract="Journey Optimizer unterstützt in Journeys drei Ereignistypen: unitäre Ereignisse, die mit dem Verhalten einer bestimmten Person verknüpft sind (z. B. ein Kauf oder ein Treuemeilenstein), Geschäftsereignisse, die durch ein globales Ereignis ausgelöst werden (z. B. eine Flugstornierung oder ein Aktien-Update), und Zielgruppen-Qualifizierungsereignisse, die ausgelöst werden, wenn ein Profil in eine Zielgruppe aufgenommen wird oder aus einer Zielgruppe aussteigt. Verwenden Sie Ereignisse, um Journeys auszulösen und die richtigen Aktionen für Ihre Profile zu orchestrieren."

Ereignisse ermöglichen es, Journeys einzeln auszulösen und allen Benutzenden beim Eintritt in die Journey Nachrichten in Echtzeit zu senden.

>[!IMPORTANT]
>
>Ereignisanforderungen und -beschränkungen (Streaming, Abfrage-Service, Batch-Aufnahme) finden Sie unter [Journey-Leitplanken - Ereignisse](../start/guardrails.md#events-g).

In der Ereigniskonfiguration konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Sie können mehrere Ereignisse (in verschiedenen Schritten der Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

Die Ereigniskonfiguration ist **obligatorisch** und muss vom Daten-Engineering durchgeführt werden.

Sie können drei Ereignistypen konfigurieren: **Unitäre Ereignisse**, **Geschäftsereignisse** und **Zielgruppen-Qualifizierungsereignisse**.

➡️ [Funktion im Video kennenlernen](#video)

## Unitäre Ereignisse {#unitary-events}

**Unitäre** Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person verknüpft ist (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unitäre Ereignisse können regelbasiert oder systemgeneriert sein. Informationen zum Erstellen eines unitären Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profileintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn also beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres Ereignis verzeichnet wird (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

## Geschäftsereignisse {#business-events}

**Geschäftsereignisse** sind nicht mit einem bestimmten Profil verknüpft. Dabei kann es sich beispielsweise um eine Nachrichtenmeldung, Sportaktualisierung, eine Änderung oder Annullierung eines Fluges, eine Bestandsaktualisierung oder um Wetterereignisse handeln. Diese Ereignisse sind zwar nicht profilspezifisch, können aber für eine beliebige Anzahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichtenthemen abonniert haben, Passagiere eines Fluges oder Kunden, die an einem nicht vorrätigen Produkt interessiert sind. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis auf einer Journey ablegen, wird automatisch eine Aktivität **Zielgruppe lesen** unmittelbar danach hinzugefügt. Erfahren Sie (auf [&#x200B; Seite), wie Sie ein Geschäftsereignis &#x200B;](../event/about-creating-business.md).

## Zielgruppen-Qualifizierungsereignisse {#audience-qualification-events}

Ein **Zielgruppen-Qualifizierungsereignis** wird ausgelöst, wenn ein Profil in eine Zielgruppe eintritt oder diese verlässt. Beispiel: Kunden, die einen Schwellenwert für Treueausgaben überschreiten, werden in die Zielgruppe der Gold-Stufe aufgenommen, d. h., bei der Qualifizierung wird die Journey für dieses Profil in Echtzeit (für Streaming-Zielgruppen) oder bei der nächsten Batch-Auswertung Trigger. Im Gegensatz zu unitären Ereignissen können Sie mit der Zielgruppen-Qualifizierung eine komplexe Trigger-Logik erstellen, indem Sie die volle Leistungsfähigkeit von Zielgruppendefinitionen nutzen, ohne dass Implementierungsänderungen erforderlich sind, um ein neues Ereignis zu senden. Weitere Informationen zu [Zielgruppen-Qualifizierungsereignissen](../building-journeys/audience-qualification-events.md).

>[!NOTE]
>
>Zielgruppen-Qualifizierungsereignisse werden nicht in **Administration > Ereignisse** konfiguriert, sondern direkt auf der Journey-Arbeitsfläche als erster Schritt einer Journey ausgewählt.

## Unitäre vs. geschäftliche Ereignisse auf einen Blick {#event-comparison}

| | Unitäres Ereignis | Geschäftsereignis |
|---|---|---|
| **Mit einem Profil verknüpft?** | Ja - ausgelöst durch die Aktion einer bestimmten Person. | Nein — ausgelöst durch ein externes Ereignis, das nicht an eine Person gebunden ist. |
| **Eintrittsverhalten** | Ein Profil gelangt in Echtzeit auf die Journey. | Mehrere Profile treten über einen automatischen Schritt „Zielgruppe lesen“ ein. |
| **Typische Anwendungsfälle** | Kaufbestätigung, Formularübermittlung, App-Anmeldung, Treuemeilenstein. | Flugstornierung, Warnhinweis bezüglich der Bestandsauffüllung, aktuelle Nachrichten, Wetterereignis. |
| **Wie startet man die Journey** | Ereignisbasierter Eintrag - keine Zielgruppe erforderlich. | Geschäftsereignis + automatische Zielgruppe lesen (von Journey Optimizer hinzugefügt). |
| **Mehrere pro Journey?** | Ja, Sie können mehrere unitäre Ereignisse über Journey-Schritte hinweg überwachen. | Nein - nur ein Geschäftsereignis pro Journey, platziert am Anfang. |
| **Ereignis-ID-Typ** | Regelbasiert oder systemgeneriert. | Immer regelbasiert. |

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
>Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. In Batches aufgenommene Ereignisse, über den **Abfrage-Service** eingefügte Ereignisse oder Ereignisse aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) können nicht zum Auslösen einer Journey verwendet werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, erstellen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe und verwenden Sie die Aktivität **Zielgruppe lesen**. Die Zielgruppen-Qualifizierung kann zwar theoretisch verwendet werden, kann aber im späteren Verlauf abhängig von den verwendeten Aktionen zu Problemen führen. Diese Daten müssen nicht unbedingt an das Echtzeitprofil gesendet werden. Wenn Sie die Ereignisse zur Segmentierung verwenden möchten, empfehlen wir, den Datensatz für das Profil zu aktivieren.

## Auswahlmöglichkeiten {#choose-event-type}

Verwenden Sie die folgenden Kriterien, um den richtigen Ereignistyp für Ihren Journey auszuwählen - die Schlüsselfrage ist: **Lösen Sie eine Aktion für eine bestimmte Person aus oder senden Sie sie an viele Profile?** [Weitere Informationen zu Journey-Typen](../building-journeys/journey.md#journey-types).

* **Wählen Sie ein unitäres** aus, wenn der Trigger an eine bestimmte Person gebunden ist, z. B. an einen Kauf, eine Formularübermittlung oder einen Treuemeilenstein. Unitäre Ereignisse erfordern eine personenbasierte primäre Identität im Schema und starten die Journey sofort für dieses Profil. [Erfahren Sie, wie Sie ein unitäres Ereignis konfigurieren](../event/about-creating.md).

* **Wählen Sie ein Geschäftsereignis aus** wenn der Trigger ein globales Ereignis ist - z. B. eine Wiederverfügbarkeit eines Produkts, ein Preisverfall oder eine Flugannullierung - und Sie an eine Reihe von Profilen senden möchten, die mit diesem Signal in Verbindung stehen. Geschäftsereignisse müssen der erste Schritt auf dem Journey sein und Profile automatisch über die Aktivität „Zielgruppe lesen **ansprechen**. Sie erfordern ein Zeitreihenschema mit einer primären Identität für Nicht-Personen und den `_id`- und `timestamp`. Planen Sie eine Verzögerung des Zielgruppenexports von 15 Minuten bis zu einer Stunde ein. [Erfahren Sie, wie Sie ein Geschäftsereignis konfigurieren](../event/about-creating-business.md).

* **Wählen Sie ein Zielgruppen-Qualifizierungsereignis** wenn es sich bei dem Trigger um ein Profil handelt, das in eine Zielgruppe eintritt oder diese verlässt, und Sie eine komplexere Segmentierungslogik benötigen, als ein einzelnes Ereignis bereitstellen kann. So können Sie beispielsweise abgelaufene Kundinnen und Kunden, die gerade einen Ausgabenschwellenwert erreicht haben, erneut ansprechen oder einen Offboarding-Fluss auslösen, wenn ein VIP-Mitglied die Treuestufe verlässt. [Weitere Informationen zu Zielgruppen-Qualifizierungsereignissen](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Geschäftsereignisse können nicht auf derselben Journey wie unitäre Ereignisse oder Zielgruppen-Qualifizierungsaktivitäten verwendet werden.

## Datenzyklus {#data-cycle}

Ereignisse sind POST-API-Aufrufe. Ereignisse werden über Streaming-Aufnahme-APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als „Inlet“ bezeichnet. Die Payload der Ereignisse verwendet die XDM-Formatierung.

Die Payload enthält Informationen, die von Streaming-Aufnahme-APIs benötigt werden, um zu funktionieren (im Header), Informationen, die [!DNL Journey Optimizer] benötigt, um zu funktionieren, und Informationen, die in Journeys verwendet werden (im Hauptteil z. B. der Betrag eines Transaktionsabbruchs). Es gibt zwei Modi für die Streaming-Aufnahme: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [diesem Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de){target="_blank"}.

Nach dem Eingang über Streaming-Aufnahme-APIs fließen Ereignisse in einen internen Service, die sogenannte Pipeline, und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung „Echtzeit-Kundenprofildienst“ aktiviert ist und es über eine Datensatz-ID verfügt, die ebenfalls die Markierung „Echtzeit-Kundenprofil“ hat, fließt das Ereignis in den Echtzeit-Kundenprofildienst.

Systemgenerierte Ereignisse: Die Pipeline filtert Ereignisse mit einer Payload, die eventIDs von [!DNL Journey Optimizer] enthalten (siehe den Ereigniserstellungsprozess unten), die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Payload enthalten sind. Regelbasierte Ereignisse: Das System identifiziert das Ereignis mit der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.


## Über den Journey-Ereignisdurchsatz {#event-thoughput}

Adobe Journey Optimizer unterstützt auf Organisationsebene ein Spitzenvolumen von 5.000 Journey-Ereignissen pro Sekunde über alle Sandboxes hinweg. Dieses Kontingent gilt für alle Ereignisse, die in aktiven Journeys genutzt werden, darunter in Journeys vom Typ **Live**, **Probelauf**, **Geschlossen** und **Angehalten**. Sobald dieses Kontingent erreicht wird, werden neue Ereignisse mit einer Verarbeitungsrate von 5.000 pro Sekunde in die Warteschlange gestellt. Die maximale Zeit, die ein Ereignis in der Warteschlange verbringen kann, beträgt **&#x200B; 24Stunden**.

Weitere Informationen zu Journey-Verarbeitungsraten und dazu, wie sich verschiedene Journey-Typen auf den Durchsatz auswirken, finden Sie [diesem Abschnitt](../building-journeys/entry-management.md#journey-processing-rate).

Die folgenden Ereignistypen werden auf das Kontingent von 5.000 TPS angerechnet:

* **Externe unitäre Ereignisse**: Umfasst sowohl regelbasierte als auch systemgenerierte Ereignisse. Wenn sich ein Raw-Ereignis für verschiedene Regeldefinitionen qualifiziert, zählt jede qualifizierte Regel als ein separates Ereignis. Weitere Informationen finden Sie unten.

* **Zielgruppen-Qualifizierungsereignisse**: Wenn dieselbe Streaming-Zielgruppe in verschiedenen Journeys zum Einsatz kommt, wird jede Verwendung separat gezählt. Wird dieselbe Zielgruppe beispielsweise in einer Zielgruppen-Qualifizierungsaktivität in zwei Journeys verwendet, werden zwei Ereignisse gezählt.

* **Reaktionsereignisse**: Ereignisse, die durch Profilreaktionen ausgelöst werden (geöffnete E-Mail, angeklickte E-Mail usw.) innerhalb einer Journey.

* **Geschäftsereignisse**: Ereignisse, die nicht an ein bestimmtes Profil gebunden sind, sondern an ein geschäftsbezogenes Ereignis.

* **Analytics-Ereignisse**: Wenn die [Integration mit Adobe Analytics zum Auslösen von Journeys](about-analytics.md) aktiviert wurde, sind diese Ereignisse ebenfalls Teil des Umfangs.

* **Fortsetzungsereignisse**: Technisches Ereignis, das ausgelöst wird, wenn ein Profil von einer angehaltenen Journey aus fortgesetzt wird. Erfahren Sie mehr über das [Fortsetzen angehaltener Journeys](../building-journeys/journey-pause.md#journey-resume-steps).

* **Abschlussereignisse von Warteknoten**: Wenn ein Profil einen Warteknoten verlässt, wird ein technisches Ereignis generiert, um die Journey fortzusetzen.

>[!NOTE]
>
>Mit Ausnahme von Warte- und Fortsetzungsereignissen werden alle anderen Ereignistypen ebenfalls auf das Kontingent angerechnet, wenn sie in Journeys auf Grundlage von „Zielgruppen lesen“ verwendet werden.

### Informationen zu Raw-Ereignissen, die sich für verschiedene Regeldefinitionen qualifizieren

Ein und dasselbe Raw-Ereignis kann sich in Journeys für verschiedene Regeldefinitionen qualifizieren. Wenn ein Ereignis im Abschnitt **Administration** für dasselbe Ereignisschema konfiguriert wird, können verschiedene Ereignisregeln definiert werden. Angenommen, es ist ein Kaufereignis mit den Feldern „city“ und „purchaseValue“ vorhanden. Betrachten wir die folgenden Szenarien:

1. Ein Ereignis **E1** mit dem Namen `newYorkPurchases` wird mit einer Regeldefinition erstellt, die `city=='New York'` lautet. Dieses Ereignis kann in 10 Journeys verwendet werden, wird aber dennoch nur als ein Ereignis gezählt, wenn es auftritt.

1. Nehmen wir nun an, dass darüber hinaus ein Ereignis **E2** mit dem Namen `highValuePurchases` mit `purchaseValue > 1000` als Regeldefinition erstellt wird, und zwar im selben Ereignisschema wie **E1**. In dem Fall wird dasselbe eingehende Ereignis anhand von zwei Regeln bewertet: `newYorkPurchases` und `highValuePurchases`. Nun kann es vorkommen, dass ein Kauf in New York auch ein hochwertiger Kauf ist.

   In dem Fall erstellt Journey Optimizer aus demselben eingehenden Ereignis zwei Ereignisse (**E1** und **E2**), wodurch das einzelne eingehende Ereignis als zwei Ereignisse gezählt wird.

   Beachten Sie, dass solche Ereignisse gezählt werden, sobald sie in einer aktiven Journey verwendet werden, darunter in Journeys vom Typ **Live**, **Probelauf**, **Abgeschlossen** und **Angehalten**.

## Aktualisieren und Löschen eines Ereignisses {#update-event}


Um Unterbrechungen vorhandener Journeys zu vermeiden, wenn Sie ein Ereignis bearbeiten, das in einer **Entwurfs**-, **Live**- oder **geschlossenen** Journey verwendet wird, können Sie nur den Namen bzw. die Beschreibung ändern oder Payload-Felder hinzufügen.

Jedes Ereignis, das in **Live**-, **Entwurfs**- oder **geschlossenen** Journeys verwendet wird, kann nicht gelöscht werden. Um ein verwendetes Ereignis zu löschen, müssen Sie seine Verwendung durch Journeys unterbinden und/oder es aus den Entwurfs-Journeys entfernen, in denen es verwendet wird. Sie können das Feld **[!UICONTROL Verwendet in]** überprüfen. Es zeigt die Anzahl der Journeys an, die dieses bestimmte Ereignis verwenden. Sie können auf die Schaltfläche **[!UICONTROL Customer Journeys anzeigen]** klicken, um die Liste der entsprechenden Journeys zu öffnen.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie ein Ereignis konfigurieren und den Streaming-Endpunkt und die Payload für ein Ereignis angeben.

>[!VIDEO](https://video.tv.adobe.com/v/3431515?captions=ger&quality=12)

Machen Sie sich mit den entsprechenden Anwendungsfällen für Geschäftsereignisse vertraut. Erfahren Sie, wie Sie mithilfe eines Geschäftsereignisses eine Journey erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
