---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von Kompositions-Workflows
description: Erfahren Sie, wie Sie Workflows für die Komposition erstellen, um bestehende Zielgruppen zu kombinieren und anzuordnen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erstellen von Kompositions-Workflows {#create-compositions}

Mit Komposition-Workflows können Sie bestehende Audiences kombinieren und anordnen, um neue Zielgruppen zu erstellen.

## Erstellen eines Kompositionsarbeitsablaufs {#create}

1. Zugriff auf **[!UICONTROL Segmente]** Menü und wählen Sie **[!UICONTROL Zielgruppe erstellen]**.

1. Auswählen **[!UICONTROL Zielgruppe erstellen]**.

   >[!NOTE]
   >
   >Die **[!UICONTROL Regel erstellen]** Mit der Erstellungsmethode können Sie eine neue Segmentdefinition erstellen, indem Sie die [Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de).

   ![](assets/audiences-create.png)

1. Die Arbeitsfläche der Komposition wird mit zwei Standardaktivitäten angezeigt:

   * **[!UICONTROL Zielgruppe]**: der Ausgangspunkt Ihrer Komposition. Mithilfe dieser Aktivität können Sie eine oder mehrere Zielgruppen als Grundlage für Ihren Workflow auswählen.

   * **[!UICONTROL Speichern]**: der letzte Schritt Ihrer Komposition. Mit dieser Aktivität können Sie das Ergebnis Ihres Workflows in einer neuen Audience speichern.
   Weiterführende Informationen zum Konfigurieren von Aktivitäten auf der Arbeitsfläche des Kompositionsarbeitsablaufs finden Sie im Abschnitt [Arbeiten mit der Arbeitsfläche für Kompositionen](composition-canvas.md).

1. Wählen Sie die **[!UICONTROL Zielgruppe]** -Aktivität und geben Sie dann einen Titel für Ihre Komposition an.

   >[!IMPORTANT]
   >
   >Die **[!UICONTROL Zielgruppe]** Der Titel der Aktivität ist der Titel Ihrer Komposition. Stellen Sie sicher, dass Sie einen aussagekräftigen Namen angeben, um die Komposition einfacher in der Liste abzurufen.

   ![](assets/audiences-new-composition.png)

1. Konfigurieren Sie Ihre Komposition, indem Sie zwischen den **[!UICONTROL Zielgruppe]** und **[!UICONTROL Speichern]** Aktivitäten. [Erfahren Sie, wie Sie mit der Arbeitsfläche für Kompositionen arbeiten.](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Sobald Ihre Komposition fertig ist, klicken Sie auf die **[!UICONTROL Veröffentlichen]** -Schaltfläche, um die Komposition zu veröffentlichen und die resultierenden Zielgruppen in Adobe Experience Platform zu speichern.

   Tritt während der Veröffentlichung ein Fehler auf, werden Warnhinweise mit Informationen zur Behebung des Problems angezeigt.

   ![](assets/audiences-alerts.png)

1. Die Komposition ist veröffentlicht. Die resultierenden Zielgruppen werden in Adobe Experience Platform gespeichert. <!-- and are ready to be targeted in Journey Optimizer campaigns. [Get started with campaigns](../campaigns/get-started-with-campaigns.md)-->

## Auf Kompositionen zugreifen {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Veröffentlichen der Audience"
>abstract="Veröffentlichen Sie Ihre Komposition, um die resultierenden Zielgruppen in Adobe Experience Platform zu speichern."

Alle erstellten Kompositionen können über die **[!UICONTROL Kompositionen]** Registerkarte. Sie können mehrere Status haben:

* **[!UICONTROL Entwurf]**: die Komposition läuft und noch nicht veröffentlicht wurde.
* **[!UICONTROL Veröffentlicht]**: die Komposition veröffentlicht wurde und die resultierenden Zielgruppen gespeichert wurden. <!-- and are available for use.-->
* **[!UICONTROL Archiviert]**: die Komposition archiviert wurde.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Sie können eine vorhandene Komposition jederzeit mit der Schaltfläche mit den Auslassungspunkten in der Liste duplizieren oder löschen.

Weitere Infos:

* [Erste Schritte mit dem Erstellen von Audiences](get-started-audience-orchestration.md)
* [Arbeiten mit der Arbeitsfläche für Kompositionen](composition-canvas.md)
* [Zugreifen auf und Verwalten von Audiences](access-audiences.md)
