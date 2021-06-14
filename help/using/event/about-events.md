---
title: Informationen zu Ereignissen
description: Erfahren Sie mehr über Ereignisse.
feature: Ereignisse
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 100%

---

# Informationen zu Ereignissen{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Informationen zu Ereignissen"
>abstract="Ein Ereignis ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren."

Mit der Ereigniskonfiguration können Sie festlegen, welche Informationen [!DNL Journey Optimizer] als Ereignisse erhält. Sie können mehrere Ereignisse (in verschiedenen Schritten der Journey) verwenden und mehrere Journeys können dasselbe Ereignis verwenden.

>[!CAUTION]
>
>Die Ereigniskonfiguration ist **obligatorisch** und muss von einem **technischen Benutzer** durchgeführt werden.

Sie können zwei Ereignistypen definieren:

* **Unitäre** Ereignisse: Diese Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unitäre Ereignisse können regelbasiert oder systemgeneriert sein. Informationen zum Erstellen eines unitären Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

* **Geschäftsereignisse**: Ein Geschäftsereignis ist ein Ereignis, das im Gegensatz zu einem unitären Ereignis nicht mit einem bestimmten Profil verknüpft ist. Dabei kann es sich beispielsweise um eine Nachrichtenmeldung, Sportaktualisierung, eine Änderung oder Annullierung eines Fluges, eine Bestandsaktualisierung oder um Wetterereignisse handeln. Obwohl diese Ereignisse nicht profilspezifisch sind, können sie für eine beliebige Zahl von Profilen von Interesse sein: Personen, die bestimmte Nachrichten abonniert haben, Passagiere eines bestimmten Fluges oder Kunden, die an einem nicht vorrätigen Produkt interessiert sind. Geschäftsereignisse sind immer regelbasiert. Wenn Sie ein Geschäftsereignis in eine Journey einfügen, wird automatisch eine Aktivität des Typs **Segment lesen** hinzugefügt. Informationen zum Erstellen eines Geschäftsereignisses finden Sie auf dieser [Seite](../event/about-creating-business.md).


>[!NOTE]
>
>Wenn Sie ein Ereignis bearbeiten, das in einer Entwurfs- oder Live-Journey verwendet wird, können Sie nur den Namen oder die Beschreibung ändern oder Payload-Felder hinzufügen. Die Bearbeitungsmöglichkeiten von Entwurfs- oder Live-Journeys sind stark beschränkt, damit Unterbrechungen von Journeys vermieden werden.

## Ereignis-ID-Typ{#event-id-type}

Bei Geschäftsereignissen ist der Ereignis-ID-Typ immer regelbasiert.

Bei unitären Ereignissen sind zwei Typen von Ereignis-IDs möglich:

* **Regelbasierte** Ereignisse: dieser Ereignistyp generiert keine eventID. Mit dem einfachen Ausdruckseditor definieren Sie einfach eine Regel, anhand derer das System die relevanten Ereignisse identifiziert, die Ihre Journeys auslösen. Diese Regel kann auf einem beliebigen Feld basieren, das in der Ereignis-Payload verfügbar ist, z. B. dem Standort des Profils oder der Anzahl der Artikel, die dem Warenkorb des Profils hinzugefügt wurden.

   >[!CAUTION]
   >
   >Für regelbasierte Ereignisse wird eine Begrenzungsregel definiert. Die Anzahl der qualifizierten Ereignisse, die eine Journey für eine bestimmte Organisation (ORG) verarbeiten kann, wird auf 5000 pro Sekunde begrenzt. Dies entspricht den Journey Optimizer-SLAs. Weitere Informationen finden Sie auf dieser [Seite](https://helpx.adobe.com/de/legal/product-descriptions/journey-orchestration.html).

* **Systemgenerierte** Ereignisse: für diese Ereignisse ist eine eventID erforderlich. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis per Push sendet, sollte keine ID generieren, sondern die ID übergeben, die in der Payload-Vorschau verfügbar ist.

## Datenzyklus {#section_r1f_xqt_pgb}

Ereignisse sind POST-API-Aufrufe. Ereignisse werden über Streaming-Aufnahme-APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als „Inlet“ bezeichnet. Die Payload der Ereignisse verwendet die XDM-Formatierung.

Die Payload enthält Informationen, die von Streaming-Aufnahme-APIs benötigt werden, um zu funktionieren (im Header), Informationen, die [!DNL Journey Optimizer] benötigt, um zu funktionieren, und Informationen, die in Journeys verwendet werden (im Hauptteil z. B. der Betrag eines Transaktionsabbruchs). Es gibt zwei Modi für die Streaming-Aufnahme: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [diesem Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=de).

Nach dem Eingang über Streaming-Aufnahme-APIs fließen Ereignisse in einen internen Dienst, die sogenannte Pipeline, und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung „Echtzeit-Kundenprofildienst“ aktiviert ist und es über eine Datensatz-ID verfügt, die ebenfalls die Markierung „Echtzeit-Kundenprofil“ hat, fließt das Ereignis in den Echtzeit-Kundenprofildienst.

Systemgenerierte Ereignisse: Die Pipeline filtert Ereignisse mit einer Payload, die eventIDs von [!DNL Journey Optimizer] enthalten (siehe den Ereigniserstellungsprozess unten), die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Payload enthalten sind. Regelbasierte Ereignisse: Das System identifiziert das Ereignis mit der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.
