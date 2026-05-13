---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Felder
description: Journey-Felder
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 100%

---

# Journey-Felder {#sharing-journey-fields}

Diese Feldergruppe wird im **Journey**-Schema verwendet (in Verbindung mit **journeyStepEvent**). Sie enthält die unten aufgeführten Felder.


>[!NOTE]
>
>Weitere Informationen über die Attribute von Journey-Eigenschaften finden Sie [in diesem Abschnitt](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

Kennung der Haupt-Journey.

Typ: Zeichenfolge

## journeyVersionID {#journeyversionid-field}

Kennung der Journey-Version. Diese Kennung stellt die Identität einer Journey dar.

Typ: Zeichenfolge

## name {#name-field}

Name der Journey.

Typ: Zeichenfolge

>[!NOTE]
>
>Der Journey-Name wird verwendet, um Journey-Ausführungsdaten mit Berichtsdatensätzen zu verknüpfen. Wenn Sie eine Journey umbenennen, stellen Sie sicher, dass der neue Name mit dem Namen in Ihrem Berichtsdatensatz übereinstimmt, um korrekte Berichte zu gewährleisten. Bei Nichtübereinstimmung werden die Berichtsdaten möglicherweise nicht wie erwartet angezeigt. Erfahren Sie mehr zur [Fehlerbehebung bei fehlenden Berichtsdaten](../building-journeys/report-journey.md#troubleshooting-missing-data).

## description {#description-field}

Beschreibung der Journey.

Typ: Zeichenfolge

## version {#version-field}

Version, dargestellt als `major`.`minor`

Typ: Zeichenfolge
