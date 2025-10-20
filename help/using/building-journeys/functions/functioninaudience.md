---
product: journey optimizer
title: inAudience
description: Erfahren Sie mehr über die Funktion „inAudience“.
feature: Journeys
role: Engineer
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 100%

---

# inAudience {#inAudience}

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

`inAudience('audienceName') == true` bedeutet, dass Sie eine segmentMembership mit dem Status „eingetreten“ haben. 

`inAudience('audienceName') == false` bedeutet, dass Sie über eine segmentMembership mit dem Status „beendet“ verfügen.


>[!IMPORTANT]
>
>Wenn Sie den Namen einer bestehenden Zielgruppe ändern, werden die Verweise auf diese Zielgruppe in Ihren Journey-Ausdrücken nicht automatisch aktualisiert. Wenn Ihr Bedingungsknoten `inAudience('oldAudienceName')` verwendet, müssen Sie den Ausdruck manuell bearbeiten, damit der neue Name verwendet wird. Andernfalls wird die Journey-Bedingung aufgehoben.

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

Die Funktion gibt **[!UICONTROL wahr]** zurück, wenn der Kontakt in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „Herren über 50“ ist. Andernfalls wird **[!UICONTROL falsch]** zurückgegeben.

