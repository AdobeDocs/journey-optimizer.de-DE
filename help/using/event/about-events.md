---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Ereignissen
description: Erfahren Sie mehr über Ereignisse.
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: Ereignisse, Ereignis, Journey, Definition, Starten
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 100%

---

# Informationen zu Ereignissen{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Informationen zu Ereignissen"
>abstract="Ein Ereignis ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von Journey Optimizer in Journeys überwacht, um die nächsten besten Aktionen zu orchestrieren."

Mit der Ereigniskonfiguration können Sie festlegen, welche Informationen [!DNL Journey Optimizer] als Ereignisse erhält. Sie können mehrere Ereignisse (in verschiedenen Schritten der Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

>[!CAUTION]
>
>Die Ereigniskonfiguration ist **obligatorisch** und muss von einem **Datentechniker** durchgeführt werden.

Sie können zwei Ereignistypen definieren:

* **Unitäre** Ereignisse: Diese Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unitäre Ereignisse können regelbasiert oder systemgeneriert sein. Informationen zum Erstellen eines unitären Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

* **Geschäftsereignisse**: Ein Geschäftsereignis ist ein Ereignis, das im Gegensatz zu einem unitären Ereignis nicht mit einem bestimmten Profil verknüpft ist. Dabei kann es sich beispielsweise um eine Nachrichtenmeldung, Sportaktualisierung, eine Änderung oder Annullierung eines Fluges, eine Bestandsaktualisierung oder um Wetterereignisse handeln. Obwohl diese Ereignisse nicht profilspezifisch sind, können sie für eine beliebige Zahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichten abonniert haben, Passagiere eines bestimmten Fluges oder Kunden, die an einem nicht vorrätigen Produkt interessiert sind. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis in eine Journey einfügen, wird danach automatisch eine Aktivität vom Typ **Zielgruppe lesen** hinzugefügt. Informationen zum Erstellen eines Geschäftsereignisses finden Sie auf dieser [Seite](../event/about-creating-business.md).


>[!NOTE]
>
>Wenn Sie ein Ereignis bearbeiten, das in einer Entwurfs- oder Live-Journey verwendet wird, können Sie nur den Namen oder die Beschreibung ändern oder Payload-Felder hinzufügen. Die Bearbeitungsmöglichkeiten von Entwurfs- oder Live-Journeys sind stark beschränkt, damit Unterbrechungen von Journeys vermieden werden.

Unitäre Journeys (beginnend mit einem Ereignis oder einer Zielgruppen-Qualifizierung) enthalten einen Schutzmechanismus, der verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.

➡️ [Entdecken Sie diese Funktion im Video](#video).

## Ereignis-ID-Typ{#event-id-type}

Bei Geschäftsereignissen ist der Ereignis-ID-Typ immer regelbasiert.

Bei unitären Ereignissen sind zwei Typen von Ereignis-IDs möglich:

* **Regelbasierte** Ereignisse: dieser Ereignistyp generiert keine eventID. Mit dem einfachen Ausdruckseditor definieren Sie einfach eine Regel, anhand derer das System die relevanten Ereignisse identifiziert, die Ihre Journeys auslösen. Diese Regel kann auf einem beliebigen Feld basieren, das in der Ereignis-Payload verfügbar ist, z. B. dem Standort des Profils oder der Anzahl der Artikel, die dem Warenkorb des Profils hinzugefügt wurden.

  >[!CAUTION]
  >
  >Für regelbasierte Ereignisse wird eine Begrenzungsregel definiert. Die Anzahl der qualifizierten Ereignisse, die eine Journey für eine bestimmte Organisation verarbeiten kann, wird durch die Regel auf 5.000 pro Sekunde begrenzt. Dies entspricht den Journey Optimizer-SLAs. Weitere Informationen finden Sie in Ihrer Journey Optimizer-Lizenz und in der [Journey Optimizer-Produktbeschreibung.](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html).

* **Systemgenerierte** Ereignisse: für diese Ereignisse ist eine eventID erforderlich. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis per Push sendet, sollte keine ID generieren, sondern die ID übergeben, die in der Payload-Vorschau verfügbar ist.

>[!NOTE]
>
>Journey Optimizer erfordert, dass Ereignisse an den Data Collection Core Service (DCCS) gestreamt werden, damit eine Journey ausgelöst werden kann. Ereignisse, die in Batches aufgenommen werden, oder Ereignissen aus internen Journey Optimizer-Datensätzen (Nachrichten-Feedback, E-Mail-Tracking usw.) können nicht zum Auslösen einer Journey verwendet werden. Für Anwendungsfälle, bei denen Sie keine Streaming-Ereignisse empfangen können, erstellen Sie stattdessen eine auf diesen Ereignissen basierende Zielgruppe und verwenden Sie die Aktivität **Zielgruppe lesen**. Die Zielgruppen-Qualifizierung kann zwar theoretisch verwendet werden, kann aber im späteren Verlauf abhängig von den verwendeten Aktionen zu Problemen führen. Diese Daten müssen nicht unbedingt an das Echtzeit-Profil gesendet werden. Wenn Sie die Ereignisse zur Segmentierung oder Suche in einer separaten Journey verwenden möchten, empfehlen wir, den Datensatz für das Profil zu aktivieren.

## Datenzyklus {#data-cycle}

Ereignisse sind POST-API-Aufrufe. Ereignisse werden über Streaming-Aufnahme-APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als „Inlet“ bezeichnet. Die Payload der Ereignisse verwendet die XDM-Formatierung.

Die Payload enthält Informationen, die von Streaming-Aufnahme-APIs benötigt werden, um zu funktionieren (im Header), Informationen, die [!DNL Journey Optimizer] benötigt, um zu funktionieren, und Informationen, die in Journeys verwendet werden (im Hauptteil z. B. der Betrag eines Transaktionsabbruchs). Es gibt zwei Modi für die Streaming-Aufnahme: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [diesem Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de).

Nach dem Eingang über Streaming-Aufnahme-APIs fließen Ereignisse in einen internen Service, die sogenannte Pipeline, und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung „Echtzeit-Kundenprofildienst“ aktiviert ist und es über eine Datensatz-ID verfügt, die ebenfalls die Markierung „Echtzeit-Kundenprofil“ hat, fließt das Ereignis in den Echtzeit-Kundenprofildienst.

Systemgenerierte Ereignisse: Die Pipeline filtert Ereignisse mit einer Payload, die eventIDs von [!DNL Journey Optimizer] enthalten (siehe den Ereigniserstellungsprozess unten), die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Payload enthalten sind. Regelbasierte Ereignisse: Das System identifiziert das Ereignis mit der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie ein Ereignis konfigurieren und den Streaming-Endpunkt und die Payload für ein Ereignis angeben.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Machen Sie sich mit den entsprechenden Anwendungsfällen für Geschäftsereignisse vertraut. Erfahren Sie, wie Sie mithilfe eines Geschäftsereignisses eine Journey erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
