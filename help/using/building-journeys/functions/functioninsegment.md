---
product: journey optimizer
title: inSegment
description: Erfahren Sie mehr über die Funktion „inSegment“
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# inSegment {#inSegment}

Überprüft, ob eine Person zu einer bestimmten Zielgruppe gehört.

>[!NOTE]
>
>Sie können bis zu 100 Zielgruppen abrufen.

Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview) definiert. Der Ausdruckseditor bietet eine automatisch ausgefüllte Zielgruppenliste.

Zielgruppen können drei Status aufweisen:

* Vorhanden: Die Entität befindet sich weiterhin in der Zielgruppe.
* Realisiert: Die Entität tritt in die Zielgruppe ein.
* Ausgestiegen: Die Entität verlässt die Zielgruppe.

Nur Personen mit den Zielgruppenteilnahmestatus **Realisiert** und **Vorhanden** werden als Mitglieder der Zielgruppe angesehen. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

`IF inSegment('segmentName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten/vorhanden“ haben. 

`ELSE inSegment('segmentName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.

## Kategorie

Adobe Experience Platform

## Funktionssyntax

`inSegment(<parameter>)`

## Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Segment | Zielgruppenname | `<string>` |

## Signatur und zurückgegebener Typ

`inSegment(<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`inSegment("men over 50")`

Erklärung:

Die Funktion gibt **[!UICONTROL true]** zurück, wenn die Person in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „men over 50“ (Herren über 50) ist. Andernfalls wird **[!UICONTROL false]** zurückgegeben.
