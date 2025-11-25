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
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '1555'
ht-degree: 100%

---

# Arbeiten mit Journey-Ereignissen {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Journey-Ereignisse"
>abstract="Ein Ereignis ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person verknüpft ist (z. B. eine Person hat 10.000 Treuepunkte erreicht). Journey Optimizer überwacht unitäre Ereignisse in Journeys, um die nächsten besten Aktionen zu orchestrieren."

Ereignisse ermöglichen es, Journeys einzeln auszulösen und allen Benutzenden beim Eintritt in die Journey Nachrichten in Echtzeit zu senden.

In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Sie können mehrere Ereignisse (in verschiedenen Schritten der Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

Die Ereigniskonfiguration ist **obligatorisch** und muss vom Daten-Engineering durchgeführt werden.

Sie können zwei Arten von Ereignissen konfigurieren: **unitäre Ereignisse** und **Geschäftsereignisse**.

➡️ [Funktion im Video kennenlernen](#video)

## Unitäre Ereignisse {#unitary-events}

**Unitäre** Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unitäre Ereignisse können regelbasiert oder systemgeneriert sein. Informationen zum Erstellen eines unitären Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profileintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn also beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres Ereignis verzeichnet wird (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

## Geschäftsereignisse {#business-events}

**Geschäftsereignisse** sind nicht mit einem bestimmten Profil verknüpft. Dabei kann es sich beispielsweise um eine Nachrichtenmeldung, Sportaktualisierung, eine Änderung oder Annullierung eines Fluges, eine Bestandsaktualisierung oder um Wetterereignisse handeln. Obwohl diese Ereignisse nicht profilspezifisch sind, können sie für eine beliebige Zahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichten abonniert haben, Passagiere eines bestimmten Fluges oder Kunden, die an einem nicht vorrätigen Produkt interessiert sind. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis in einer Journey ablegen, wird direkt danach eine Aktivität **Zielgruppe lesen** automatisch hinzugefügt. Informationen zum Erstellen eines Geschäftsereignisses finden Sie auf [dieser Seite](../event/about-creating-business.md).


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
>Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. Über Ereignisse, die in Batches aufgenommen werden, oder Ereignisse aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) kann eine Journey nicht ausgelöst werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, erstellen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe und verwenden Sie die Aktivität **Zielgruppe lesen**. Die Zielgruppen-Qualifizierung kann zwar theoretisch verwendet werden, kann aber im späteren Verlauf abhängig von den verwendeten Aktionen zu Problemen führen. Diese Daten müssen nicht unbedingt an das Echtzeitprofil gesendet werden. Wenn Sie die Ereignisse zur Segmentierung verwenden möchten, empfehlen wir, den Datensatz für das Profil zu aktivieren.

## Datenzyklus {#data-cycle}

Ereignisse sind POST-API-Aufrufe. Ereignisse werden über Streaming-Aufnahme-APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als „Inlet“ bezeichnet. Die Payload der Ereignisse verwendet die XDM-Formatierung.

Die Payload enthält Informationen, die von Streaming-Aufnahme-APIs benötigt werden, um zu funktionieren (im Header), Informationen, die [!DNL Journey Optimizer] benötigt, um zu funktionieren, und Informationen, die in Journeys verwendet werden (im Hauptteil z. B. der Betrag eines Transaktionsabbruchs). Es gibt zwei Modi für die Streaming-Aufnahme: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [diesem Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de){target="_blank"}.

Nach dem Eingang über Streaming-Aufnahme-APIs fließen Ereignisse in einen internen Service, die sogenannte Pipeline, und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung „Echtzeit-Kundenprofildienst“ aktiviert ist und es über eine Datensatz-ID verfügt, die ebenfalls die Markierung „Echtzeit-Kundenprofil“ hat, fließt das Ereignis in den Echtzeit-Kundenprofildienst.

Systemgenerierte Ereignisse: Die Pipeline filtert Ereignisse mit einer Payload, die eventIDs von [!DNL Journey Optimizer] enthalten (siehe den Ereigniserstellungsprozess unten), die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Payload enthalten sind. Regelbasierte Ereignisse: Das System identifiziert das Ereignis mit der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.


## Über den Journey-Ereignisdurchsatz {#event-thoughput}

Adobe Journey Optimizer unterstützt auf Organisationsebene ein Spitzenvolumen von 5.000 Journey-Ereignissen pro Sekunde über alle Sandboxes hinweg. Dieses Kontingent gilt für alle Ereignisse, die in aktiven Journeys genutzt werden, darunter in Journeys vom Typ **Live**, **Probelauf**, **Geschlossen** und **Angehalten**. Sobald dieses Kontingent erreicht wird, werden neue Ereignisse mit einer Verarbeitungsrate von 5.000 pro Sekunde in die Warteschlange gestellt. Die maximale Zeit, die ein Ereignis in der Warteschlange verbringen kann, beträgt ** 24Stunden**.

Weitere Informationen zu Journey-Verarbeitungsraten und dazu, wie sich verschiedene Journey-Typen auf den Durchsatz auswirken, finden Sie [diesem Abschnitt](../building-journeys/entry-management.md#journey-processing-rate).

Die folgenden Ereignistypen werden auf das Kontingent von 5.000 TPS angerechnet:

* **Externe unitäre Ereignisse**: Umfasst sowohl regelbasierte als auch systemgenerierte Ereignisse. Wenn sich ein Raw-Ereignis für verschiedene Regeldefinitionen qualifiziert, zählt jede qualifizierte Regel als ein separates Ereignis. Weitere Informationen finden Sie unten.

* **Zielgruppen-Qualifizierungsereignisse**: Wenn dieselbe Streaming-Zielgruppe in verschiedenen Journeys zum Einsatz kommt, wird jede Verwendung separat gezählt. Wird dieselbe Zielgruppe beispielsweise in einer Zielgruppen-Qualifizierungsaktivität in zwei Journeys verwendet, werden zwei Ereignisse gezählt.

* **Reaktionsereignisse**: Ereignisse, die durch Profilreaktionen (geöffnete E-Mails, angeklickte E-Mails usw.) in einer Journey ausgelöst werden.

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

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Machen Sie sich mit den entsprechenden Anwendungsfällen für Geschäftsereignisse vertraut. Erfahren Sie, wie Sie mithilfe eines Geschäftsereignisses eine Journey erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
