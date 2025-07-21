---
solution: Journey Optimizer
product: journey optimizer
title: Planen der Aktionskampagne
description: Erfahren Sie, wie Sie die Aktionskampagne planen.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 32%

---


# Planen der Aktionskampagne {#action-campaign-schedule}

Definieren Sie **[!UICONTROL Kampagnenzeitplan auf]** Registerkarte „Planung“.

Standardmäßig starten Aktionskampagnen, sobald sie manuell aktiviert werden, und enden, sobald die Nachricht einmal gesendet wurde. Wenn Sie Ihre Kampagne nicht direkt nach der Aktivierung ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben.

Mit **[!UICONTROL Option]** Kampagnenende“ können Sie angeben, wann die Ausführung einer Kampagne beendet werden soll. Außerhalb des angegebenen Zeitraums wird die Kampagne nicht ausgeführt.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Stellen Sie bei der Planung von Kampagnen in [!DNL Adobe Journey Optimizer] sicher, dass Ihr Startdatum und Ihre Startzeit mit dem gewünschten ersten Versand übereinstimmen. Wenn bei wiederkehrenden Kampagnen die anfängliche geplante Zeit bereits überschritten ist, werden die Kampagnen gemäß ihren Intervallregeln auf das nächste verfügbare Zeitfenster verschoben.

Je nach Kampagnenkanal stehen zusätzliche Planungsoptionen zur Verfügung:

* **Häufigkeit** (E-Mail, SMS, Push-Aktion)

  Sie können aber auch festlegen, mit welcher Häufigkeit die Nachricht der Kampagne gesendet werden soll. Verwenden Sie dazu die Option **[!UICONTROL Aktions-Trigger]** im Bildschirm zur Kampagnenerstellung, um festzulegen, ob die Kampagne täglich, wöchentlich oder monatlich ausgeführt werden soll.

* **Aktivierung des IP-Aufwärmplans** (E-Mail)

  Für E-Mail-Kampagnen können Sie spezifische IP-Aufwärmplan-Aktivierungskampagnen erstellen. Der Kampagnenzeitplan wird durch den IP-Aufwärmplan gesteuert, mit dem er verknüpft wird. Der Zeitplan wird also nicht mehr in der Kampagne selbst definiert. [Erfahren Sie, wie Sie IP-Aufwärmkampagnen erstellen](../configuration/ip-warmup-campaign.md).

## Nächste Schritte {#next}

Sobald Ihr Kampagnenkalender fertig ist, können Sie die Kampagne überprüfen und aktivieren. [Weitere Informationen](review-activate-campaign.md)
