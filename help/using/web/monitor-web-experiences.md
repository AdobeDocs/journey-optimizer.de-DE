---
title: Überwachen Ihrer Web-Erlebnisse
description: Informationen zum Überwachen von Web-Erlebnissen in Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c618a0dc-1818-4c6d-9916-0d92e6796f24
  - id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: f8905d41c1ec293d453f3f3992c4f91b94c3357f
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 79%

---

# Überwachen Ihrer Web-Erlebnisse {#monitor-web-experiences}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Ihre Live-Web-Erlebnisse in Adobe Journey Optimizer überwachen können, indem Sie die Web-Berichte überprüfen und das Klick-Tracking für bestimmte Seitenelemente einrichten.

>[!ENDSHADEBOX]

## Überprüfen der Web-Berichte {#check-web-reports}

Sobald Ihr Web-Erlebnis live ist, können Sie auf der Registerkarte **[!UICONTROL Web]** des [Journey-Berichts](../reports/journey-global-report-cja-web.md) und des [Kampagnenberichts](../reports/campaign-global-report-cja-web.md) Elemente wie die Anzahl der Impressionen, die Klickrate und die Anzahl der Zugriffe auf Ihre Web-Seite vergleichen.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Um die Überwachung von Web-Erlebnissen weiter zu verbessern, können Sie auch die Klicks auf ein bestimmtes Element Ihrer Website verfolgen. Auf diese Weise können Sie die Anzahl der Klicks auf dieses Element in den Web-Berichten anzeigen. [Weitere Informationen](#use-click-tracing)

## Verwenden von Klick-Tracking {#use-click-tracking}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_click_tracking"
>title="Verwenden von Klick-Tracking"
>abstract="Klicks auf beliebige Elemente Ihrer Web-Seite verfolgen, um Benutzerinteraktionen zu überwachen. Wählen Sie ein Element aus, wählen **Klick-Tracking** aus dem Kontextmenü und fügen Sie eine aussagekräftige Bezeichnung hinzu. Die verfolgten Daten werden in Ihren Web-Berichten angezeigt, sodass Sie besser verstehen können, wie Benutzer mit Ihren Inhalten interagieren."

Mit dem Web-Designer können Sie ein beliebiges Element Ihrer Website auswählen und die Klicks auf dieses Element verfolgen.

Diese Informationen können zur Verbesserung des Benutzererlebnisses auf Ihrer Web-Site nützlich sein. Wenn beispielsweise die [Web-Berichte](../reports/campaign-global-report-cja-web.md) zeigen, dass häufig auf ein Element geklickt wurde, auf das eigentlich nicht geklickt werden kann, können Sie diesem Element einen Link hinzufügen.

1. Wählen Sie ein Element auf Ihrer Seite und dann **[!UICONTROL Klick-Tracking für Element]** aus dem Kontextmenü aus.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Jedes Element kann ausgewählt werden, unabhängig davon, ob es klickbar ist.

1. Die entsprechende verfolgte Aktion wird automatisch im Bereich **[!UICONTROL Klick-Tracking]** auf der linken Seite angezeigt.

   ![](assets/web-designer-click-track-pane.png)

1. Fügen Sie ein aussagekräftiges Label hinzu, um alle verfolgten Elemente zu verwalten und sie in den Berichten leicht auffindbar zu machen. Das Feld **[!UICONTROL CSS-Auswahl]** zeigt Informationen zum Auffinden des ausgewählten Elements an.

1. Wiederholen Sie die obigen Schritte, um nach Bedarf weitere Elemente für das Klick-Tracking auszuwählen. Die entsprechenden Aktionen werden alle im linken Bereich aufgelistet.

   ![](assets/web-designer-click-tracking-actions.png)

1. Um das Klick-Tracking für ein Element zu entfernen, wählen Sie das entsprechende Löschsymbol aus.

Sobald Ihre Kampagne aktiv ist, können Sie die Anzahl der Klicks für jedes Element im Web-[Live-Bericht](../reports/campaign-live-report.md#web-tab) und im [Customer Journey Analytics-Bericht](../reports/campaign-global-report-cja-web.md) der Kampagne überprüfen.
