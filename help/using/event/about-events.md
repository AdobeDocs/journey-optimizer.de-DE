---
title: Informationen zu Ereignissen
description: Erfahren Sie mehr über Ereignisse.
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 57%

---

# Informationen zu Ereignissen{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Informationen zu Ereignissen"
>abstract="Ein Ereignis ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (z. B. eine Person hat ein Produkt gekauft, einen Shop besucht, eine Website verlassen usw.) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren."

Mit der Ereigniskonfiguration können Sie festlegen, welche Informationen [!DNL Journey Optimizer] als Ereignisse erhält. Sie können mehrere Ereignis (in verschiedenen Schritten einer Journey) verwenden und mehrere Journey können dasselbe Ereignis verwenden.

>[!CAUTION]
>
>Die Konfiguration des Ereignisses ist **mandatory** und muss von einem **technischen Benutzer** durchgeführt werden.

Sie können zwei Typen von Ereignissen konfigurieren:

* **** Unitaryevents: diese Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (zum Beispiel kaufte eine Person ein Produkt, besuchte einen Laden, verließ eine Website usw.) oder auf etwas, das mit einer Person in Verbindung steht (z. B. eine Person hat 10.000 Treuepunkte erreicht). Diese Ereignisse werden von [!DNL Journey Optimizer] in Journeys überwacht, um die besten nächsten Aktionen zu orchestrieren. Unäre Ereignis können regelbasiert oder systemseitig erstellt werden. Informationen zum Erstellen eines einheitlichen Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

* **** Geschäftsveranstaltungen: ein geschäftliches Ereignis ist ein Ereignis, das im Gegensatz zu einem einheitlichen Ereignis nicht mit einem bestimmten Profil verknüpft ist. So kann es sich beispielsweise um eine News-Warnung, eine Sportaktualisierung, eine Änderung oder Annullierung des Fluges, eine Bestandsaktualisierung, Wetter-Ereignisse usw. handeln. Diese Ereignisse sind zwar nicht für ein Profil spezifisch, können jedoch für eine beliebige Anzahl von Profilen von Interesse sein: Personen, die besondere Nachrichten abonniert haben, Fluggäste, die an einem nicht vorrätigen Produkt interessiert sind, usw. Business-Ereignis sind immer regelbasiert. Wenn Sie ein geschäftliches Ereignis in einer Journey ablegen, wird direkt danach automatisch eine **Read segment**-Aktivität hinzugefügt. Informationen zum Erstellen eines geschäftlichen Ereignisses finden Sie auf dieser [Seite](../event/about-creating-business.md).


>[!NOTE]
>
>Wenn Sie ein Ereignis bearbeiten, das in einer Entwurfs- oder Live-Journey verwendet wird, können Sie nur den Namen oder die Beschreibung ändern oder Payload-Felder hinzufügen. Die Bearbeitungsmöglichkeiten von Entwurfs- oder Live-Journeys sind stark beschränkt, damit Unterbrechungen von Journeys vermieden werden.

## Ereignis-ID-Typ{#event-id-type}

Bei geschäftlichen Ereignissen ist der Ereignis-ID-Typ immer regelbasiert.

Bei einheitlichen Ereignissen gibt es zwei Typen von Ereignis-IDs:

* **Regelbasierte** Ereignisse: dieser Ereignistyp generiert keine eventID. Mit dem einfachen Ausdruckseditor definieren Sie einfach eine Regel, anhand derer das System die relevanten Ereignisse identifiziert, die Ihre Journeys auslösen. Diese Regel kann auf einem beliebigen Feld basieren, das in der Ereignis-Payload verfügbar ist, z. B. dem Standort des Profils oder der Anzahl der Artikel, die dem Warenkorb des Profils hinzugefügt wurden.

   >[!CAUTION]
   >
   >Für regelbasierte Ereignisse wird eine Begrenzungsregel definiert. Die Anzahl der qualifizierten Ereignisse, die eine Journey für eine bestimmte Organisation (ORG) verarbeiten kann, wird auf 5000 pro Sekunde begrenzt. Es entspricht den SLAs der Journey Optimizer. Weitere Informationen finden Sie auf dieser [Seite](https://helpx.adobe.com/de/legal/product-descriptions/journey-orchestration.html).

* **Systemgenerierte** Ereignisse: für diese Ereignisse ist eine eventID erforderlich. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis per Push sendet, sollte keine ID generieren, sondern die ID übergeben, die in der Payload-Vorschau verfügbar ist.

## Datenzyklus {#section_r1f_xqt_pgb}

Ereignisse sind POST-API-Aufrufe. Ereignis werden über Streaming Ingestion APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als „Inlet“ bezeichnet. Die Payload der Ereignisse verwendet die XDM-Formatierung.

Die Nutzlast enthält Informationen, die für Streaming-Ingestion-APIs erforderlich sind (in der Kopfzeile), die für die Arbeit mit [!DNL Journey Optimizer] erforderlichen Informationen und die Informationen, die in Journey verwendet werden sollen (z. B. die Menge eines aufgegebenen Einkaufswagens). Es gibt zwei Modi für die Streaming-Aufnahme: authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming-Aufnahme-APIs finden Sie unter [diesem Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Nach der Ankunft über Streaming Ingestion APIs fließen Ereignis in einen internen Dienst namens Pipeline und dann in Adobe Experience Platform. Wenn für das Ereignisschema die Markierung „Echtzeit-Kundenprofildienst“ aktiviert ist und es über eine Datensatz-ID verfügt, die ebenfalls die Markierung „Echtzeit-Kundenprofil“ hat, fließt das Ereignis in den Echtzeit-Kundenprofildienst.

Systemgenerierte Ereignisse: Die Pipeline filtert Ereignisse mit einer Payload, die eventIDs von [!DNL Journey Optimizer] enthalten (siehe den Ereigniserstellungsprozess unten), die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Payload enthalten sind. Regelbasierte Ereignisse: Das System identifiziert das Ereignis mit der eventID-Bedingung. Diese Ereignisse werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.
