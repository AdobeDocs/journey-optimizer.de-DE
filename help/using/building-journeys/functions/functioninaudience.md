---
product: journey optimizer
title: inAudience
description: Erfahren Sie mehr über die Funktion „inAudience“.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, Funktion, Ausdruck, Journey
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 385e27fd4ea34f6a10b8da6b99a2c888edf9d57e
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 68%

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

`inAudience('audienceName') == false` bedeutet, dass Sie über eine segmentMitgliedschaft mit dem Status „beendet“ haben.


>[!IMPORTANT]
>
>Wenn Sie den Namen einer bestehenden Zielgruppe ändern, werden in Ihren Journey-Ausdrücken nicht automatisch alle Verweise auf diese Zielgruppe aktualisiert. Wenn Ihr Bedingungsknoten `inAudience('oldAudienceName')` verwendet, müssen Sie den Ausdruck manuell bearbeiten, um den neuen Namen zu verwenden. Andernfalls wird der Journey-Zustand beschädigt.

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

Die Funktion gibt &quot;**[!UICONTROL &quot; zurück]** wenn die Person in der Journey-Instanz Teil der Adobe Experience Platform-Zielgruppe „Männer über 50“ ist, **[!UICONTROL false]** andernfalls.

