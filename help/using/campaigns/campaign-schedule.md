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
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 4417643cbf206b9ad112bae5c270cdfc746a9c5d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 64%

---

# Planen der Aktionskampagne {#action-campaign-schedule}

Definieren Sie auf der Registerkarte **[!UICONTROL Zeitplan]** den Zeitplan der Kampagne.

## Start- und Enddatum festlegen

Standardmäßig starten Aktionskampagnen, sobald sie manuell aktiviert werden, und enden, sobald die Nachricht einmal gesendet wurde. Wenn Sie Ihre Kampagne nicht direkt nach der Aktivierung ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben.

Über die Option **[!UICONTROL Kampagnenende]** können Sie angeben, wann die Ausführung einer Kampagne gestoppt werden soll. Außerhalb der angegebenen Daten wird die Kampagne nicht ausgeführt.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Stellen Sie bei der Planung von Kampagnen in [!DNL Adobe Journey Optimizer] sicher, dass Ihr Startdatum und Ihre Startzeit mit dem gewünschten ersten Versand übereinstimmen. Wenn bei wiederkehrenden Kampagnen die anfängliche geplante Zeit bereits überschritten ist, werden die Kampagnen gemäß ihren Intervallregeln auf das nächste verfügbare Zeitfenster verschoben.

## Steuerung der Einstellungsrate

[!DNL Journey Optimizer] ermöglicht es Ihnen, die Ratenkontrolle für ausgehende Aktionen (E-Mail, SMS, Push-Benachrichtigungen) zu aktivieren.

Diese Funktion ist besonders nützlich, um eine Überlastung nachgelagerter Systeme zu verhindern, z. B. Landingpages oder Kundenunterstützungsplattformen. Beispielsweise können Sie eine Ratenbeschränkung von 165 Nachrichten pro Sekunde festlegen, um einen stabilen Versand sicherzustellen, ohne die nachgelagerten Systeme zu überfordern.

Um die Versandrate zu steuern, aktivieren Sie die Option **[!UICONTROL Versand drosseln]** im Abschnitt **[!UICONTROL Versandeinstellungen]** und geben Sie die gewünschte **[!UICONTROL Versandrate]** pro Sekunde an.

![](assets/throttling-rate-control.png)

## Ausführungshäufigkeit festlegen

Für E-Mail-, SMS- und Push-Benachrichtigungsaktionen können Sie eine Häufigkeit festlegen, mit der die Nachricht der Kampagne gesendet werden soll. Verwenden Sie dazu die Option **[!UICONTROL Aktions-Trigger]** im Bildschirm zur Kampagnenerstellung, um festzulegen, ob die Kampagne täglich, wöchentlich oder monatlich ausgeführt werden soll.

![](assets/action-triggers.png)

## IP-Aufwärmpläne einrichten

Für E-Mail-Aktionen können Sie spezifische IP-Aufwärmplan-Aktivierungskampagnen erstellen. Der Zeitplan der Kampagne wird von dem IP-Aufwärmplan bestimmt, mit dem er verknüpft ist. Dies bedeutet, dass der Zeitplan nicht mehr in der Kampagne selbst definiert ist. [Informationen zum Erstellen von IP-Aufwärmkampagnen](../configuration/ip-warmup-campaign.md).

## Nächste Schritte {#next}

Sobald Ihr Kampagnenzeitplan fertiggestellt ist, können Sie die Kampagne überprüfen und aktivieren. [Weitere Informationen](review-activate-campaign.md)
