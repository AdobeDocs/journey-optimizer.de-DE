---
solution: Journey Optimizer
product: journey optimizer
title: Über Ereignisse
description: Erfahren Sie mehr über Ereignisse
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Über Ereignisse{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Über Ereignisse"
>abstract="Eine Veranstaltung ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Dies wird von Journey Optimizer in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren."

Mit der Ereigniskonfiguration können Sie die Informationen definieren [!DNL Journey Optimizer] wird als Ereignisse empfangen. Sie können mehrere Ereignisse (in verschiedenen Schritten einer Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

>[!CAUTION]
>
>Ereigniskonfiguration ist **mandatory** und muss von einer **Data Engineer**.

Sie können zwei Ereignistypen konfigurieren:

* **Einzelfall** events: Diese Veranstaltung ist mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Laden besucht, eine Website verlassen usw.) oder etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Das ist es [!DNL Journey Optimizer] überwacht in Journeys, um die besten nächsten Aktionen zu orchestrieren. Einzelereignisse können regelbasiert oder systemgeneriert sein. Informationen zum Erstellen eines einheitlichen Ereignisses finden Sie in diesem Abschnitt [page](../event/about-creating.md).

* **Unternehmen** events: Ein Geschäftsereignis ist ein Ereignis, das im Gegensatz zu einem Einzelereignis nicht mit einem bestimmten Profil verknüpft ist. Es kann sich beispielsweise um eine Nachrichtenwarnung, eine Sportaktualisierung, eine Flugänderung oder Absage, eine Bestandsaktualisierung, Wetterereignisse usw. handeln. Diese Ereignisse sind zwar nicht profilspezifisch, können aber für eine beliebige Anzahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichtenthemen abonniert haben, Fluggäste, die an einem nicht vorrätigen Produkt interessiert sind, usw. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis in einer Journey ablegen, wird automatisch ein **Segment lesen** -Aktivität direkt nach. Informationen zum Erstellen eines Geschäftsereignisses finden Sie in diesem [page](../event/about-creating-business.md).


>[!NOTE]
>
>Wenn Sie ein Ereignis bearbeiten, das in einer Entwurfs- oder Live-Journey verwendet wird, können Sie nur den Namen und die Beschreibung ändern oder Payload-Felder hinzufügen. Wir beschränken die Bearbeitung von Entwurfs- oder Live-Journeys strikt, um zu verhindern, dass Journeys unterbrochen werden.

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzmaßnahme, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Eintritt in das Profil wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis eine Journey um 12:01 Uhr für ein bestimmtes Profil auslöst und ein anderes um 12:03 Uhr eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), startet die Journey für dieses Profil nicht erneut.

➡️ [Funktion im Video kennenlernen](#video)

## Ereignis-ID-Typ{#event-id-type}

Bei Geschäftsereignissen ist der Ereignis-ID-Typ immer regelbasiert.

Bei Einzelereignissen gibt es zwei Arten von Ereignis-IDs:

* **Regelbasiert** events: dieser Ereignistyp generiert keine eventID. Mit dem einfachen Ausdruckseditor definieren Sie einfach eine Regel, die vom System verwendet wird, um die relevanten Ereignisse zu identifizieren, die Ihre Journeys auslösen werden. Diese Regel kann auf jedem Feld basieren, das in der Ereignis-Payload verfügbar ist, z. B. dem Speicherort des Profils oder der Anzahl der Artikel, die zum Warenkorb des Profils hinzugefügt werden.

   >[!CAUTION]
   >
   >Eine Begrenzungsregel ist für regelbasierte Ereignisse definiert. Die Anzahl der qualifizierten Ereignisse, die eine Journey für eine bestimmte Organisation verarbeiten kann, wird auf 5000 pro Sekunde begrenzt. Dies entspricht den Journey Optimizer-SLAs. Weitere Informationen finden Sie in Ihrer Journey Optimizer-Lizenzierung und [Produktbeschreibung für Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Systemgeneriert** events: für diese Ereignisse eine eventID erforderlich ist. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis per Push sendet, sollte keine ID generieren, sondern die ID übergeben, die in der Payload-Vorschau verfügbar ist.

Für Journey Optimizer müssen Ereignisse gestreamt oder in Batches an Adobe Experience Platform übertragen werden. Diese Daten müssen nicht unbedingt an das Echtzeit-Profil gesendet werden. Wenn Sie die Ereignisse für die Segmentierung oder Suche in einer separaten Journey verwenden möchten, empfehlen wir, den Datensatz für Profil zu aktivieren.

## Datenzyklus {#data-cycle}

Ereignisse sind POST-API-Aufrufe. Ereignisse werden über Streaming-Aufnahme-APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als &quot;Inlet&quot;bezeichnet. Die Payload der Ereignisse folgt der XDM-Formatierung.

Die Payload enthält Informationen, die von Streaming-Aufnahme-APIs benötigt werden, um zu funktionieren (in der Kopfzeile), sowie die Informationen, die für [!DNL Journey Optimizer] , um zu arbeiten und Informationen zu erhalten, die in Journeys verwendet werden (im Hauptteil, z. B. die Menge eines Transaktionsabbruchs). Es gibt zwei Modi für die Streaming-Erfassung: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [dieser Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Nach dem Eingang über Streaming-Aufnahme-APIs fließen Ereignisse in einen internen Dienst namens Pipeline und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung &quot;Echtzeit-Kundenprofildienst&quot;aktiviert ist und eine Datensatz-ID, die auch die Markierung &quot;Echtzeit-Kundenprofil&quot;aufweist, fließt sie in den Echtzeit-Kundenprofildienst.

Bei systemgenerierten Ereignissen filtert die Pipeline Ereignisse mit einer Payload, die [!DNL Journey Optimizer] eventIDs (siehe den Ereigniserstellungsprozess unten) bereitgestellt von [!DNL Journey Optimizer] und in der Ereignis-Payload enthalten sind. Bei regelbasierten Ereignissen identifiziert das System das Ereignis mithilfe der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] und die entsprechende Journey ausgelöst wird.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie ein Ereignis konfigurieren, den Streaming-Endpunkt und die Payload für ein Ereignis angeben.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Machen Sie sich mit den anwendbaren Anwendungsfällen für Geschäftsereignisse vertraut. Erfahren Sie, wie Sie mithilfe eines Geschäftsereignisses eine Journey erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
