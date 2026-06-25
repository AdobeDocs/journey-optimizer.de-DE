---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie mit Adobe Experience Platform-Zielgruppen arbeiten.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
TQID: https://experienceleague.adobe.com/OL0VFfxegvbTbSLKeqFaUNTeZllmFtjMW6bmh1XDF00
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 9a0d5b396d569f7375a719229cf5a3779448567e
workflow-type: tm+mt
source-wordcount: 691
ht-degree: 83%

---

# Erste Schritte mit Zielgruppen {#about-segments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Adobe Experience Platform-Zielgruppen durchsuchen, erstellen und verwalten und sie in Ihren Adobe Journey Optimizer-Journey und -Kampagnen ansprechen.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Zielgruppe"
>abstract="Mithilfe von Echtzeit-Kundenprofildaten können Sie mit Adobe Experience Platform auf einfache Weise Segmentdefinitionen für genaue Zielgruppen erstellen, die das einzigartige Verhalten und die Vorlieben Ihrer Kundinnen und Kunden erfassen."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Auswählen der Kampagnenzielgruppe"
>abstract="Diese Liste zeigt alle verfügbaren Adobe Experience Platform-Zielgruppen an. Wählen Sie die Zielgruppe aus, die mit Ihrer Kampagne angesprochen werden soll. Die in der Kampagne konfigurierte Nachricht wird an alle Kontakte gesendet, die zur ausgewählten Zielgruppe gehören. [Weitere Informationen zu Zielgruppen](../audience/about-audiences.md)"

Bei einer Zielgruppe handelt es sich um eine Sammlung von Personen, die ähnliche Verhaltensweisen und/oder Merkmale aufweisen. Sie wird mithilfe des Segmentierungs-Services von Adobe Experience Platform zentral in Adobe Experience Platform konfiguriert und gepflegt und steht in Journey Optimizer zur Verfügung, um in Ihren Journeys und Kampagnen aktiviert zu werden.

Adobe Journey Optimizer bietet zuverlässige Tools zum Erstellen, Verwalten und Anreichern von Zielgruppen, um Ihre Marketing-Maßnahmen zu optimieren. In Kombination mit Adobe Real-Time Customer Data Platform können Sie mit Journey Optimizer Zielgruppen für eine komplexere Segmentierung einlagern und Zielgruppen bidirektional für andere [!DNL Adobe CX Enterprise]-Lösungen freigeben.

Beim Hochladen von Echtzeit-Datenströmen oder Batch-Vorgängen werden Datensätze aktualisiert, und Journey Optimizer verschiebt Personen dynamisch in Echtzeit in Zielgruppen und Journeys und wieder aus diesen heraus.

>[!BEGINSHADEBOX]

Diese Dokumentation enthält Informationen zum Arbeiten mit Zielgruppen in [!DNL Adobe Journey Optimizer]. Detaillierte Informationen zum Zielgruppenportal und zu Zielgruppen finden Sie in der Dokumentation zum Segmentierungs-Service in Adobe Experience Platform. Weitere Informationen finden Sie in diesen Abschnitten:

* [Handbuch zur Benutzeroberfläche des Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [Segmentierungs-Service - häufig gestellte Fragen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## Durchsuchen von Zielgruppen {#browse}

Sie können auf Zielgruppen über das Menü **[!UICONTROL Kunde]** > **[!UICONTROL Zielgruppen]** zugreifen.

Ein Dashboard zeigt Überschneidungen zwischen wichtigen Zielgruppen visuell an und unterstützt das Untersuchen wertvoller Zielgruppen-Trends. Änderungen der Zielgruppengröße über einen bestimmten Zeitraum oder plötzliche Spitzen bei Zielgruppen können beispielsweise Ereignisse oder Aktionen hervorheben, die zum Schrumpfen einer Zielgruppe geführt haben, aber auch solche, die ein Zielgruppenwachstum nach sich gezogen haben, etwa ein erfolgreiches Angebot.

![](assets/audiences-overview.png)

Im Zielgruppenportal können Sie Zielgruppen mit standardisierten Labels, Governance-Steuerelementen, durchsuchbaren Ordnern und Tags einfach verwalten, suchen und erkunden.

Weitere Informationen zum Arbeiten mit Zielgruppen im Zielgruppenportal sind in der [Dokumentation zum Segmentierungs-Service in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"} verfügbar.

## Zielgruppentypen {#types}

Zielgruppen können auf unterschiedliche Weise erstellt werden:

* **Segmentdefinitionen**: Erstellen Sie mithilfe des Adobe Experience Platform Segmentierungsdienstes eine neue Zielgruppendefinition. Zielgruppen werden aus Segmentdefinitionen generiert und je nach Auswertungstyp zu unterschiedlichen Zeiten aktualisiert:

   * Streaming-Segmentierung: Zielgruppen werden in Echtzeit aktualisiert, während neue Daten einfließen, wodurch eine kontinuierliche Relevanz basierend auf der Benutzeraktivität sichergestellt wird.
   * Batch-Segmentierung: Zielgruppen werden alle 24 Stunden aktualisiert und es wird eine Momentaufnahme der Profile in einem festen Intervall erfasst. Bei Verwendung in Journey werden neu qualifizierte Segmentmitglieder möglicherweise erst beim nächsten Schnappschuss angezeigt. [Weitere Informationen zum Timing](../building-journeys/audience-qualification-events.md#timing-segment-membership).
   * Edge-Segmentierung: Zielgruppen werden sofort am Edge ausgewertet, was die Personalisierung in Echtzeit ermöglicht.

  [Weitere Informationen zum Erstellen von Segmentdefinitionen](creating-a-segment-definition.md)

* **Benutzerdefinierter Upload**: Importieren einer Zielgruppe mithilfe einer CSV-Datei. [Weitere Informationen zum Erstellen von Zielgruppen aus benutzerdefinierten Uploads](custom-upload.md)

* **Zielgruppenkomposition**: Erstellen Sie einen Kompositions-Workflow, um vorhandene Zielgruppen in einer visuellen Arbeitsfläche zu kombinieren und Aktionen wie Rang, Aufspaltung oder Zusammenführen anzuwenden, um neue Zielgruppen zu erstellen. [Weitere Informationen zum Arbeiten mit Zielgruppenkomposition](get-started-audience-orchestration.md)

* **Komposition föderierter Zielgruppen**: Führen Sie Datensätze direkt aus Ihrem bestehenden Data Warehouse zusammen, um in Adobe Experience Platform Zielgruppen und Attribute in einem System aufzubauen und anzureichern. [Weitere Informationen zum Arbeiten mit der Komposition föderierter Zielgruppen](federated-audience-composition.md).

## Ansprechen von Zielgruppen in Journeys und Kampagnen {#target-audiences}

Sobald Ihre Zielgruppen bereit sind, können Sie sie beim Erstellen von Journeys oder Kampagnen auswählen, sodass Sie die richtigen Personen zur richtigen Zeit mit relevanten Nachrichten erreichen. [Weitere Informationen zur Zielgruppenaktivierung in Journey Optimizer](target-audiences.md).

>[!NOTE]
>
>Profile, die über eine Zielgruppenaktivierung eingebunden wurden - unabhängig davon, ob es sich um eine Journey-, Kampagnen- oder Entscheidungsaktivität handelt - werden bei der Lizenzmetrik **Engageable Profiles** Ihres Unternehmens mitgezählt. Jedes Profil wird einmal pro Sandbox in einem rollierenden 12-Monats-Fenster gezählt. [Überwachen Sie die Anzahl der aktivierbaren Profile](license-usage.md)

## Anleitungsvideo {#video}

Informationen über einheitliche Kundenprofile und Zielgruppen in Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
