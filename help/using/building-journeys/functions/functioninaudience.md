---
product: journey optimizer
title: inAudience
description: Erfahren Sie mehr über die Funktion „inAudience“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# inAudience {#inAudience}

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

`inAudience('audienceName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten/vorhanden“ haben. 

`inAudience('audienceName') == false` bedeutet, dass Sie eine segmentMembership mit dem Status „ausgestiegen“ haben.

## Kategorie

Adobe Experience Platform

## Funktionssyntax

`inAudience(<parameter>)`

## Parameter

| Parameter | Beschreibung | Typ |
|--- |--- |--- |
| Zielgruppe | Zielgruppenname | `<string>` |

## Signatur und zurückgegebener Typ

`inAudience(<string>)`

Gibt einen booleschen Wert zurück.

## Beispiel

`inAudience("men over 50")`

Erklärung:

Die Funktion gibt **[!UICONTROL true]** zurück, wenn die Person in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „men over 50“ (Herren über 50) ist. Andernfalls wird **[!UICONTROL false]** zurückgegeben.
