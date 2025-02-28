---
product: journey optimizer
title: inAudience
description: Erfahren Sie mehr über die Funktion „inAudience“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 85a8d0713f87a8b3505a2294402156ba6598c8bb
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 74%

---

# inAudience {#inAudience}

Überprüft, ob eine Person zu einer bestimmten Zielgruppe gehört.

>[!NOTE]
>
>Sie können bis zu 100 Zielgruppen abrufen.

Der Zielgruppenname muss eine Zeichenfolgenkonstante sein. Er darf weder ein Feldverweis noch ein Ausdruck sein.

Zielgruppen werden in [Adobe Experience Platform](https://platform.adobe.com/audience/overview) definiert. Der Ausdruckseditor bietet eine automatisch ausgefüllte Zielgruppenliste.

Zielgruppen können zwei Status aufweisen:

* realisiert: Entität qualifiziert sich für die Segmentdefinition.
* beendet: Entität beendet die Segmentdefinition.

Nur Einzelpersonen mit dem **Realisiert**-Zielgruppenbeteiligungsstatus werden als Mitglieder der Zielgruppe betrachtet. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=de#interpret-segment-results).

`inAudience('audienceName') == true` bedeutet, dass Sie eine segmentMembership mit dem eingegebenen Status haben.

`inAudience('audienceName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.

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
