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
ht-degree: 35%

---

# inSegment {#inSegment}

Überprüft, ob eine Person zu einer bestimmten Zielgruppe gehört.

>[!NOTE]
>
>Sie können bis zu 100 Zielgruppen abrufen.

Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Zielgruppen werden im Abschnitt [Adobe Experience Platform](https://platform.adobe.com/audience/overview). Der Ausdruckseditor bietet eine automatisch ausgefüllte Liste von Zielgruppen.

Zielgruppen können drei Status haben:

* vorhanden: -Entität befindet sich weiterhin in der Zielgruppe.
* realisiert: -Entität in die Audience eingeben.
* beendet: -Entität die Audience beendet.

Nur Personen mit der **Realisiert** und **Bestehend** Der Beteiligungsstatus von Zielgruppen wird als Mitglieder der Zielgruppe betrachtet. Weiterführende Informationen zur Audience-Evaluierung finden Sie im Abschnitt [Dokumentation zum Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

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

Die Funktion gibt **[!UICONTROL true]** wenn die Person innerhalb der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe mit dem Namen &quot;Herren über 50&quot;ist, **[!UICONTROL false]** andernfalls.
