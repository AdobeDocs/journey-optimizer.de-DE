---
solution: Journey Optimizer
product: journey optimizer
title: Planen einer Kampagne, die durch API ausgelöst wird
description: Informationen zum Planen einer Kampagne, die durch API ausgelöst wird.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 64%

---

# Planen der Kampagne, die durch API ausgelöst wird {#api-schedule}

Definieren Sie auf der Registerkarte **[!UICONTROL Zeitplan]** den Zeitplan der Kampagne.

## Start- und Enddatum festlegen

Standardmäßig starten durch API ausgelöste Kampagnen, wenn sie ausgelöst werden, und enden, sobald die Nachricht einmal gesendet wurde. Wenn Sie Ihre Kampagne nicht direkt nach der Auslösung ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben.

Über die Option **[!UICONTROL Kampagnenende]** können Sie angeben, wann die Ausführung einer Kampagne gestoppt werden soll. Außerhalb der angegebenen Daten wird die Kampagne nicht ausgeführt.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Stellen Sie bei der Planung von Kampagnen in [!DNL Adobe Journey Optimizer] sicher, dass Ihr Startdatum und Ihre Startzeit mit dem gewünschten ersten Versand übereinstimmen.

## Steuerung der Einstellungsrate

[!DNL Journey Optimizer] ermöglicht es Ihnen, die Ratenkontrolle für ausgehende Aktionen (E-Mail, SMS, Push-Benachrichtigungen) zu aktivieren.

Diese Funktion ist besonders nützlich, um eine Überlastung nachgelagerter Systeme zu verhindern, z. B. Landingpages oder Kundenunterstützungsplattformen. Beispielsweise können Sie eine Ratenbeschränkung von 165 Nachrichten pro Sekunde festlegen, um einen stabilen Versand sicherzustellen, ohne die nachgelagerten Systeme zu überfordern.

Um die Versandrate zu steuern, aktivieren Sie die Option **[!UICONTROL Versand drosseln]** im Abschnitt **[!UICONTROL Versandeinstellungen]** und geben Sie die gewünschte **[!UICONTROL Versandrate]** an.

![](assets/throttling-rate-control.png)

## Nächste Schritte {#next}

Nachdem die Kampagnenkonfiguration und der Inhalt fertig sind, können Sie sie überprüfen und aktivieren. [Weitere Informationen](review-activate-campaign.md)
