---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen des Workflows für die erste Komposition
description: Erfahren Sie, wie Sie Kompositions-Workflows erstellen, um bestehende Audiences zu kombinieren und anzuordnen.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informative"
source-git-commit: 8b1bf0b0469c1efc5194dae56ddddd9f05dbf722
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 86%

---

# Erstellen des Workflows für die erste Komposition {#create-compositions}

<table style="table-layout:fixed"><tr style="border: 0;"><tr><td>Was Sie in dieser Dokumentation finden werden:<br/><ul>
<li><a href="get-started-audience-orchestration.md">Erste Schritte mit der Audience-Komposition</a></li>
<li><b><a href="create-compositions.md">Erstellen des Workflows für die erste Komposition</a></b></li>
<li><a href="composition-canvas.md">Arbeiten mit der Arbeitsfläche für Kompositionen</a></li>
<li><a href="access-audiences.md">Zugreifen auf und Verwalten von Audiences</a></li></ul></td></tr></table>

## Erstellen eines Kompositions-Workflows {#create}

Gehen Sie wie folgt vor, um einen Kompositionsarbeitsablauf zu erstellen:

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

1. Bitte die Eigenschaften der Komposition öffnen, um einen Titel und eine Beschreibung anzugeben.

   Wenn in den Eigenschaften kein Titel definiert ist, wird der Titel der Komposition auf &quot;Komposition&quot;gesetzt, gefolgt von Erstellungsdatum und -zeit.

   ![](assets/audiences-properties.png)

1. Konfigurieren Sie Ihre Komposition, indem Sie so viele Aktivitäten für **[!UICONTROL Audience]** und **[!UICONTROL Speichern]** hinzufügen, wie Sie benötigen. [Erfahren Sie, wie Sie mit der Arbeitsfläche für Kompositionen arbeiten](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Sobald Ihre Komposition fertig ist, klicken Sie auf die Schaltfläche **[!UICONTROL Veröffentlichen]**, um die Komposition zu veröffentlichen und die resultierenden Audiences in Adobe Experience Platform zu speichern.

   Tritt während der Veröffentlichung ein Fehler auf, werden Warnhinweise mit Informationen zur Behebung des Problems angezeigt.

   ![](assets/audiences-alerts.png)

1. Die Komposition wird veröffentlicht. Die resultierenden Zielgruppen werden in Adobe Experience Platform gespeichert und können für Journey Optimizer-Kampagnen verwendet werden. [Mit Kampagnen arbeiten](../campaigns/get-started-with-campaigns.md)

## Zugriff auf Kompositionen {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Veröffentlichen Ihrer Audience"
>abstract="Veröffentlichen Sie Ihre Komposition, um die resultierende(n) Audience(s) in Adobe Experience Platform zu speichern."

Alle erstellten Kompositionen sind über die Registerkarte **[!UICONTROL Kompositionen]** verfügbar. Sie können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Komposition ist in Arbeit und wurde noch nicht veröffentlicht.
* **[!UICONTROL Veröffentlicht]**: Die Komposition wurde veröffentlicht, die resultierenden Zielgruppen wurden gespeichert und sind zur Verwendung verfügbar.
* **[!UICONTROL Archiviert]**: Die Komposition wurde archiviert.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Sie können eine bestehende Komposition jederzeit duplizieren oder löschen, indem Sie die Schaltfläche mit den Auslassungspunkten in der Liste verwenden.
