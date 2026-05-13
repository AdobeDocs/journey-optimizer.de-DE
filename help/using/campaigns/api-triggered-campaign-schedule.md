---
solution: Journey Optimizer
product: journey optimizer
title: Planen einer von einer API ausgelösten Kampagne
description: Erfahren Sie, wie Sie eine API-ausgelöste Kampagne planen.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
TQID: https://experienceleague.adobe.com/4cCtvRATLk-gNyMcY-jESte82DKpgVbhA75pE4fNKmQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# Planen der API-ausgelösten Kampagne {#api-schedule}

Definieren Sie **[!UICONTROL Kampagnenzeitplan auf]** Registerkarte „Planung“.

## Start- und Enddatum festlegen

Standardmäßig starten API-ausgelöste Kampagnen, sobald sie ausgelöst werden, und enden, sobald die Nachricht einmal gesendet wurde. Wenn Sie Ihre Kampagne nicht direkt nach dem Auslösen ausführen möchten, können Sie das Datum und die Uhrzeit für den Versand der Nachricht mit der Option **[!UICONTROL Kampagnenstart]** angeben.

Mit **[!UICONTROL Option]** Kampagnenende“ können Sie angeben, wann die Ausführung einer Kampagne beendet werden soll. Außerhalb des angegebenen Zeitraums wird die Kampagne nicht ausgeführt.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Stellen Sie bei der Planung von Kampagnen in [!DNL Adobe Journey Optimizer] sicher, dass Ihr Startdatum und Ihre Startzeit mit dem gewünschten ersten Versand übereinstimmen.

## Steuerung der Einstellungsrate

[!DNL Journey Optimizer] ermöglicht es Ihnen, die Ratenkontrolle für ausgehende Aktionen (E-Mail, SMS, Push-Benachrichtigungen) zu aktivieren.

Diese Funktion ist besonders nützlich, um eine Überlastung nachgelagerter Systeme zu verhindern, z. B. Landingpages oder Kundenunterstützungsplattformen. Beispielsweise können Sie eine Ratenbeschränkung von 165 Nachrichten pro Sekunde festlegen, um einen stabilen Versand sicherzustellen, ohne die nachgelagerten Systeme zu überfordern.

Um die Versandrate zu steuern, aktivieren Sie die Option **[!UICONTROL Versand drosseln]** im Abschnitt **[!UICONTROL Versandeinstellungen]** und geben Sie die gewünschte **[!UICONTROL Versandrate]** pro Sekunde an.

* Unterstützte Mindestbereitstellungsrate: 1 pro Sekunde.
* Maximal unterstützte Versandrate: 2.000 pro Sekunde, wenn die Option „Versand drosseln“ aktiviert ist.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Bei der Festlegung einer Versandrate beträgt der maximale Zeitrahmen, für den die Audience einer Kampagne ausgeführt werden kann, 12 Stunden. Wenn die Versandrate auf einen Wert eingestellt ist, der es nicht ermöglicht, dass die gesamte Zielgruppe die Nachricht innerhalb des 12-Stunden-Zeitrahmens gesendet wird, werden die verbleibenden Profile aus der Kampagne ausgeschlossen. Die Anzahl dieser ausgeschlossenen Profile wird im Kampagnenbericht angezeigt.

## Nächste Schritte {#next}

Sobald Ihre Kampagnenkonfiguration und Ihre Inhalte fertig sind, können Sie sie überprüfen und aktivieren. [Weitere Informationen](../campaigns/review-activate-api-triggered-campaign.md)
