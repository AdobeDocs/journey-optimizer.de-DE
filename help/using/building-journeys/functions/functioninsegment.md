---
product: journey optimizer
title: inSegment
description: Erfahren Sie mehr über die Funktion „inSegment“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 100%

---

# inSegment {#inSegment}

Überprüft, ob ein Kontakt zu einem bestimmten Segment gehört.

>[!NOTE]
>
>Sie können bis zu 100 Segmente abrufen.

Der Segmentname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Segmente werden in [Adobe Experience Platform](https://platform.adobe.com/segment/overview) definiert. Der Ausdruckseditor bietet eine automatisch ausgefüllte Segmentliste.

Segmente können drei Status haben:

* vorhanden: Entität befindet sich weiterhin im Segment.
* realisiert: Entität tritt in das Segment ein.
* beendet: Entität verlässt das Segment.

Nur Personen mit den Segmentteilnahmestatus **Realisiert** und **Vorhanden** werden als Mitglieder des Segments betrachtet. Weitere Informationen zum Auswerten eines Segments finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

`IF inSegment('segmentName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten/vorhanden“ haben. 

`ELSE inSegment('segmentName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.

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

Die Funktion gibt **[!UICONTROL true]** zurück, wenn der Kontakt in der Journey-Instanz Teil des Adobe Experience Platform-Segments namens „Herren über 50“ ist, andernfalls wird **[!UICONTROL false]** zurückgegeben.
