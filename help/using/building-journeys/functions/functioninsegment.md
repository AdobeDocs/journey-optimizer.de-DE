---
product: journey optimizer
title: inSegment
description: Erfahren Sie mehr über die Funktion inSegment
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# inSegment {#inSegment}

Überprüft, ob eine Person zu einem bestimmten Segment gehört.

>[!NOTE]
>
>Sie können bis zu 100 Segmente abrufen.

Der Segmentname muss eine Zeichenfolgenkonstante sein. Es darf sich weder um einen Feldverweis noch um einen Ausdruck handeln.

Segmente werden im Abschnitt [Adobe Experience Platform](https://platform.adobe.com/segment/overview). Der Ausdruckseditor bietet eine automatisch ausgefüllte Segmentliste.

Segmente können drei Status aufweisen:

* vorhanden: -Entität befindet sich weiterhin im Segment.
* realisiert: -Entität in das Segment ein.
* beendet: -Entität das Segment verlässt.

Nur Personen mit der **Realisiert** und **Bestehend** Segmentteilsstatus werden als Mitglieder des Segments betrachtet. Weiterführende Informationen zur Auswertung eines Segments finden Sie im Abschnitt [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` bedeutet, dass Sie über eine segmentMembership mit dem eingegebenen/vorhandenen Status verfügen.

`ELSE inSegment('segmentName') == false` bedeutet, dass Sie über eine segmentMembership des Status &quot;Exited&quot;verfügen.

## Kategorie

Adobe Experience Platform

## Funktionssyntax

`inSegment(<parameter>)`

## Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Segment | Der Segmentname | `<string>` |

## Signatur und zurückgegebener Typ

`inSegment(<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`inSegment("men over 50")`

Erklärung:

Die Funktion gibt **[!UICONTROL true]** wenn der Kontakt in der Journey-Instanz Teil des Adobe Experience Platform-Segments namens &quot;Herren über 50&quot;ist, **[!UICONTROL false]** andernfalls.
