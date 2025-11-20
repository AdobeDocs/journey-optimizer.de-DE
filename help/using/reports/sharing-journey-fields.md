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
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 60%

---

# Journey-Felder {#sharing-journey-fields}

Diese Feldergruppe wird im **Journey**-Schema verwendet (in Verbindung mit **journeyStepEvent**).  Sie enthält die unten aufgeführten Felder.


>[!NOTE]
>
>Weitere Informationen über die Attribute von Journey-Eigenschaften finden Sie [in diesem Abschnitt](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

Kennung der Haupt-Journey.

Typ: Zeichenfolge

## journeyVersionID {#journeyversionid-field}

ID der Journey-Version. Diese Kennung stellt die Identität einer Journey dar.

Typ: Zeichenfolge

## name {#name-field}

Name der Journey.

Typ: Zeichenfolge

>[!NOTE]
>
>Der Journey-Name wird verwendet, um Journey-Ausführungsdaten mit Reporting-Datensätzen zu verknüpfen. Wenn Sie eine Journey umbenennen, stellen Sie sicher, dass der neue Name mit dem Namen in Ihrem Reporting-Datensatz übereinstimmt, um ein korrektes Reporting zu gewährleisten. Eine Nichtübereinstimmung kann dazu führen, dass die Berichtsdaten nicht wie erwartet angezeigt werden. Weitere Informationen über [Fehlerbehebung bei fehlenden Berichtsdaten](../building-journeys/report-journey.md#troubleshooting-missing-data).

## description {#description-field}

Beschreibung der Journey.

Typ: Zeichenfolge

## version {#version-field}

Version, dargestellt als `major`.`minor`

Typ: Zeichenfolge
