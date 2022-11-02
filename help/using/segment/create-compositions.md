---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen von Kompositions-Workflows
description: Erfahren Sie, wie Sie Kompositions-Workflows erstellen, um bestehende Audiences zu kombinieren und anzuordnen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: af59c7ed83f18932fe13791b50713eabfba3b549
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 75%

---

# Erstellen von Kompositions-Workflows {#create-compositions}

Mit Kompositions-Workflows können Sie bestehende Audiences kombinieren und anordnen, um neue Audiences zu erstellen.

## Erstellen eines Kompositions-Workflows {#create}

1. Gehen Sie zum **[!UICONTROL Segmente]**-Menü und wählen Sie **[!UICONTROL Audience erstellen]** aus.

1. Wählen Sie **[!UICONTROL Audience erstellen]** aus.

   >[!NOTE]
   >
   >Mit der Erstellungsmethode **[!UICONTROL Regel erstellen]** können Sie die Definition eines neuen Segments erstellen, indem Sie den [Segmentierungs-Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=de) verwenden.

   ![](assets/audiences-create.png)

1. Die Arbeitsfläche der Komposition wird mit zwei Standardaktivitäten angezeigt:

   * **[!UICONTROL Audience]**: der Ausgangspunkt Ihrer Komposition. Mithilfe dieser Aktivität können Sie eine oder mehrere Audiences als Grundlage für Ihren Workflow auswählen.

   * **[!UICONTROL Speichern]**: der letzte Schritt Ihrer Komposition. Mit dieser Aktivität können Sie das Ergebnis Ihres Workflows in einer neuen Audience speichern.
   Weiterführende Informationen zum Konfigurieren von Aktivitäten auf der Arbeitsfläche des Kompositions-Workflows finden Sie im Abschnitt [Arbeiten mit der Arbeitsfläche für Kompositionen](composition-canvas.md).

1. Öffnen Sie die Eigenschaften der Komposition, um einen Titel und eine Beschreibung anzugeben.

   Wenn in den Eigenschaften kein Titel definiert ist, wird die Kompositionsbezeichnung der Anfang sein. **[!UICONTROL Zielgruppe]** Aktivität.

   ![](assets/audiences-properties.png)

1. Konfigurieren Sie Ihre Komposition, indem Sie so viele Aktivitäten für **[!UICONTROL Audience]** und **[!UICONTROL Speichern]** hinzufügen, wie Sie benötigen. [Erfahren Sie, wie Sie mit der Arbeitsfläche für Kompositionen arbeiten](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Sobald Ihre Komposition fertig ist, klicken Sie auf die **[!UICONTROL Veröffentlichen]** -Schaltfläche, um die Komposition zu veröffentlichen und die resultierenden Zielgruppen in Adobe Experience Platform zu speichern.

   Tritt während der Veröffentlichung ein Fehler auf, werden Warnhinweise mit Informationen zur Behebung des Problems angezeigt.

   ![](assets/audiences-alerts.png)

1. Die Komposition wird veröffentlicht. Die resultierenden Zielgruppen werden in Adobe Experience Platform gespeichert und können für Journey Optimizer-Kampagnen verwendet werden. [Erste Schritte mit Kampagnen](../campaigns/get-started-with-campaigns.md)

## Zugriff auf Kompositionen {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Veröffentlichen Ihrer Audience"
>abstract="Veröffentlichen Sie Ihre Komposition, um die resultierende(n) Audience(s) in Adobe Experience Platform zu speichern."

Alle erstellten Kompositionen sind über die Registerkarte **[!UICONTROL Kompositionen]** verfügbar. Sie können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Komposition ist in Arbeit und wurde noch nicht veröffentlicht.
* **[!UICONTROL Veröffentlicht]**: die Komposition veröffentlicht wurde, die resultierenden Zielgruppen gespeichert wurden und zur Verwendung verfügbar sind.
* **[!UICONTROL Archiviert]**: Die Komposition wurde archiviert.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Sie können eine vorhandene Komposition jederzeit mithilfe der Schaltfläche mit den Auslassungspunkten in der Liste duplizieren oder löschen.

Weitere Informationen:

* [Erste Schritte mit der Audience-Komposition](get-started-audience-orchestration.md)
* [Arbeiten mit der Arbeitsfläche für Kompositionen](composition-canvas.md)
* [Zugreifen auf und Verwalten von Audiences](access-audiences.md)
