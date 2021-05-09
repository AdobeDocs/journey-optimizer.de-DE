---
title: Info zu Ereignissen
description: Weitere Informationen zu Ereignissen
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Info zu Ereignissen{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="Info zu Ereignissen"
>abstract="Ein Ereignis ist mit einer Person verbunden. Es bezieht sich auf das Verhalten einer Person (zum Beispiel kaufte eine Person ein Produkt, besuchte einen Laden, verließ eine Website usw.) oder etwas, das mit einer Person verbunden ist (z. B. eine Person erreichte 10 000 Treuepunkte). [!DNL Journey Optimizer] hört in Journey auf, um die besten nächsten Aktionen zu organisieren."

Mit der Ereignis-Konfiguration können Sie festlegen, welche Informationen [!DNL Journey Optimizer] als Ereignis empfangen werden. Sie können mehrere Ereignis (in verschiedenen Schritten einer Journey) verwenden und mehrere Journey können dasselbe Ereignis verwenden.

>[!CAUTION]
>
>Die Konfiguration des Ereignisses ist **mandatory** und muss von einem **technischen Benutzer** durchgeführt werden.

Sie können zwei Typen von Ereignissen konfigurieren:

* **** Unitaryevents: diese Ereignisse sind mit einer Person verbunden. Sie beziehen sich auf das Verhalten einer Person (zum Beispiel kaufte eine Person ein Produkt, besuchte einen Laden, verließ eine Website usw.) oder etwas, das mit einer Person verbunden ist (z. B. eine Person erreichte 10 000 Treuepunkte). [!DNL Journey Optimizer] hört in Journey auf, um die besten nächsten Aktionen zu organisieren. Unäre Ereignis können regelbasiert oder systemseitig erstellt werden. Informationen zum Erstellen eines einheitlichen Ereignisses finden Sie auf dieser [Seite](../event/about-creating.md).

* **** Geschäftsveranstaltungen: ein geschäftliches Ereignis ist ein Ereignis, das im Gegensatz zu einem einheitlichen Ereignis nicht mit einem bestimmten Profil verknüpft ist. So kann es sich beispielsweise um eine News-Warnung, eine Sportaktualisierung, eine Änderung oder Annullierung des Fluges, eine Bestandsaktualisierung, Wetter-Ereignisse usw. handeln. Diese Ereignisse sind zwar nicht für ein Profil spezifisch, können jedoch für eine beliebige Anzahl von Profilen von Interesse sein: Personen, die besondere Nachrichten abonniert haben, Fluggäste, die an einem nicht vorrätigen Produkt interessiert sind, usw. Business-Ereignis sind immer regelbasiert. Wenn Sie ein geschäftliches Ereignis in einer Journey ablegen, wird direkt danach automatisch eine **Read segment**-Aktivität hinzugefügt. Informationen zum Erstellen eines geschäftlichen Ereignisses finden Sie auf dieser [Seite](../event/about-creating-business.md).


>[!NOTE]
>
>Wenn Sie ein Ereignis bearbeiten, das in einem Entwurf oder einer Live-Journey verwendet wird, können Sie nur den Namen, die Beschreibung oder die Nutzdatenfelder ändern. Wir beschränken die Auflage von Entwurf oder Live-Journey, um zu vermeiden, dass Journey.

## Ereignis-ID-Typ{#event-id-type}

Bei geschäftlichen Ereignissen ist der Ereignis-ID-Typ immer regelbasiert.

Bei einheitlichen Ereignissen gibt es zwei Typen von Ereignis-IDs:

* **Regelbasierte** Ereignisse: dieser Ereignis generiert keine eventID. Mit dem einfachen Ausdruck-Editor definieren Sie einfach eine Regel, die vom System verwendet wird, um die relevanten Ereignis zu identifizieren, die Ihre Journey Trigger haben. Diese Regel kann auf allen in der Ereignis-Nutzlast verfügbaren Feldern basieren, z. B. auf der Position des Profils oder der Anzahl der dem Einkaufswagen des Profils hinzugefügten Artikel.

   >[!CAUTION]
   >
   >Für regelbasierte Ereignis wird eine Deckelungsregel definiert. Die Anzahl der qualifizierten Ereignis, die eine Journey für eine bestimmte Organisation (ORG) auf 5000 pro Sekunde verarbeiten kann, wird dadurch begrenzt. Es entspricht den SLAs der Journey Optimizer. Siehe diese [Seite](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **System-** Generatedevents: Für diese Ereignis ist eine eventID erforderlich. Dieses eventID-Feld wird beim Erstellen des Ereignisses automatisch generiert. Das System, das das Ereignis schiebt, sollte keine ID generieren, sondern die in der Payload-Vorschau verfügbare weitergeben.

## Datenzyklus {#section_r1f_xqt_pgb}

Ereignis sind POST-API-Aufrufe. Ereignis werden über Streaming Ingestion APIs an Adobe Experience Platform gesendet. Das URL-Ziel von Ereignissen, die über Transaktionsnachrichten-APIs gesendet werden, wird als &quot;Einlass&quot;bezeichnet. Die Nutzlast von Ereignissen erfolgt nach der XDM-Formatierung.

Die Nutzlast enthält Informationen, die für Streaming-Ingestion-APIs erforderlich sind (in der Kopfzeile), die für die Arbeit mit [!DNL Journey Optimizer] erforderlichen Informationen und die Informationen, die in Journey verwendet werden sollen (z. B. die Menge eines aufgegebenen Einkaufswagens). Es gibt zwei Modi für die Streaming-Erfassung, authentifiziert und nicht authentifiziert. Weitere Informationen zu Streaming Ingestion APIs finden Sie unter [dieser Link](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Nach der Ankunft über Streaming Ingestion APIs fließen Ereignis in einen internen Dienst namens Pipeline und dann in Adobe Experience Platform. Wenn für das Ereignis-Schema das Flag &quot;Kundendienst in Echtzeit&quot;und eine DataSet-ID aktiviert sind, für die auch das Flag &quot;Customer Profil&quot;in Echtzeit aktiviert ist, fließt es in den Echtzeit-Kundendienst (Customer Profil Service).

Bei systemgenerierten Ereignissen werden in der Pipeline-Filter Ereignis mit einer Nutzlast mit [!DNL Journey Optimizer]-eventIDs (siehe den unten stehenden Vorgang zur Erstellung von Ereignissen) angezeigt, die von [!DNL Journey Optimizer] bereitgestellt werden und in der Ereignis-Nutzlast enthalten sind. Bei regelbasierten Ereignissen identifiziert das System das Ereignis mit der eventID-Bedingung. Diese Ereignis werden von [!DNL Journey Optimizer] überwacht und die entsprechende Journey wird ausgelöst.
