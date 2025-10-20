---
product: journey optimizer
title: inSegment
description: Erfahren Sie mehr über die Funktion „inSegment“
feature: Journeys
role: Engineer
level: Experienced
keywords: inSegment, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 100%

---

# inSegment {#inSegment}

Überprüft, ob eine Person zu einer bestimmten Zielgruppe gehört.

>[!NOTE]
>
>Sie können bis zu 100 Zielgruppen abrufen.

Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview) definiert. Der Ausdruckseditor bietet eine automatisch ausgefüllte Zielgruppenliste.

Zielgruppen können zwei Status aufweisen:

* Realisiert: Entität qualifiziert sich für die Segmentdefinition.
* Ausgestiegen: Die Entität verlässt die Segmentdefinition.

Nur Personen mit dem Zielgruppenzugehörigkeitsstatus **Realisiert** werden als Mitglieder der Zielgruppe angesehen. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

`inSegment('segmentName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten/vorhanden“ haben. 

`inSegment('segmentName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.

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
