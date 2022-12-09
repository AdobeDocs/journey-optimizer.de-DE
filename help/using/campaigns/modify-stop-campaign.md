---
solution: Journey Optimizer
product: journey optimizer
title: Ändern oder Anhalten einer Kampagne
description: Erfahren Sie, wie Sie Live-Kampagnen in ändern, stoppen oder duplizieren [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Verwalten von Kampagnen {#modify-stop-campaign}

Nach Aktivierung einer Kampagne können Sie diese jederzeit ändern oder stoppen. Diese Vorgänge stehen nur bei Kampagnen mit wiederkehrender Ausführung zur Verfügung.

Darüber hinaus können Sie Live-Kampagnen (einmal oder mit wiederkehrender Ausführung) duplizieren, um neue zu erstellen und abgeschlossene oder gestoppte Kampagnen zu archivieren.

## Auf Kampagnen zugreifen {#access}

Auf Kampagnen kann über die **[!UICONTROL Campaigns]** Menü.

Standardmäßig werden in der Liste alle Kampagnen mit dem **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** und **[!UICONTROL Live]** Status.

Um angehaltene, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

## Kampagnenstatus {#statuses}

Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Draft]**: Die Kampagne wird bearbeitet, sie wurde nicht aktiviert.
* **[!UICONTROL Activating]**: Die Kampagne wird aktiviert.
* **[!UICONTROL Live]**: Die Kampagne wurde aktiviert.
* **[!UICONTROL Scheduled]**: Die Kampagne ist so konfiguriert, dass sie an einem bestimmten Startdatum aktiviert wird.
* **[!UICONTROL Stopped]**: Die Kampagne wurde manuell gestoppt. Sie können sie nicht mehr aktivieren oder wiederverwenden. [Erfahren Sie, wie Sie eine Kampagne stoppen](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**: Die Kampagne ist abgeschlossen. Dieser Status wird automatisch 3 Tage nach der Aktivierung einer Kampagne zugewiesen oder am Enddatum der Kampagne, wenn sie eine wiederkehrende Ausführung aufweist.
* **[!UICONTROL Archived]**: Die Kampagne wurde archiviert. [Erfahren Sie, wie Sie Kampagnen archivieren](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Das Symbol &quot;Entwurfsversion öffnen&quot;neben einem **[!UICONTROL Live]** oder **[!UICONTROL Scheduled]** Der Status zeigt an, dass eine neue Version der Kampagne erstellt wurde und noch nicht aktiviert wurde. [Weitere Infos](modify-stop-campaign.md#modify).

## Ändern einer wiederkehrenden Kampagne {#modify}

Gehen Sie wie folgt vor, um eine neue Version einer wiederkehrenden Kampagne zu ändern und zu erstellen:

1. Öffnen Sie die Kampagne und klicken Sie auf die Schaltfläche **[!UICONTROL Modify campaign]** Schaltfläche.

1. Eine neue Version der Kampagne wird erstellt. Sie können die Live-Version überprüfen, indem Sie auf **[!UICONTROL Open live version]**.

   ![](assets/create-campaign-draft.png)

   In der Kampagnenliste werden aktivierte Kampagnen mit dem Entwurf der aktuellen Version mit einem bestimmten Symbol im **[!UICONTROL Status]** Spalte. Klicken Sie auf dieses Symbol, um den Entwurf der Kampagne zu öffnen.

   ![](assets/create-campaign-edit-list.png)

1. Sobald Ihre Änderungen fertig sind, können Sie die neue Version der Kampagne aktivieren (siehe [Kampagne überprüfen und aktivieren](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >Durch die Aktivierung des Entwurfs wird die Live-Version der Kampagne ersetzt.

## Wiederkehrende Kampagne stoppen {#stop}

Um eine wiederkehrende Kampagne anzuhalten, öffnen Sie sie und klicken Sie auf die Schaltfläche **[!UICONTROL Stop campaign]** Schaltfläche.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>Durch das Anhalten einer Kampagne wird der laufende Versand nicht gestoppt, aber der geplante Versand wird gestoppt oder das nächste Vorkommen, wenn der Versand bereits durchgeführt wird.

<!-- inbound campaign (inapp): can stop and resume -->

## Kampagne duplizieren {#duplicate}

Sie können eine Live-Kampagne duplizieren, um eine neue zu erstellen. Öffnen Sie dazu die Kampagne und klicken Sie auf **[!UICONTROL Duplicate]**.

![](assets/create-campaign-duplicate.png)

## Kampagne archivieren {#archive}

Mit der Zeit wächst die Liste der Kampagnen und erschwert es schließlich, abgeschlossene und gestoppte Kampagnen zu durchsuchen.

Um dies zu verhindern, können Sie abgeschlossene und gestoppte Kampagnen archivieren, die Sie nicht mehr benötigen. Klicken Sie dazu auf die Schaltfläche mit den Auslassungspunkten und wählen Sie **[!UICONTROL Archive]**.

![](assets/create-campaign-archive.png)

Archivierte Kampagnen können dann mithilfe des dedizierten Filters in der Liste abgerufen werden. [Erfahren Sie, wie Sie auf Kampagnen zugreifen können](get-started-with-campaigns.md#access)
