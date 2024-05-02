---
solution: Journey Optimizer
product: journey optimizer
title: Twilio-Provider konfigurieren
description: Erfahren Sie, wie Sie Ihre Umgebung für den Versand von Textnachrichten mit Journey Optimizer mit Twilio konfigurieren.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 60%

---

# Twilio-Provider konfigurieren {#sms-configuration-twilio}

Um Twilio mit Journey Optimizer zu konfigurieren, müssen Sie neue API-Anmeldeinformationen erstellen, die für Twilio verwendet werden:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

   ![](assets/sms_6.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Konto-SID]** und **[!UICONTROL Authentifizierungs-Token]**: Rufen Sie den Bereich mit den **Kontoinformationen** Ihrer Twilio Console-Dashboard-Seite auf. Dort finden Sie Ihre Anmeldedaten.

   * **[!UICONTROL Nachrichten-SID]**: Geben Sie die eindeutige Kennung ein, die jeder von der Twilio-API erstellten Nachricht zugewiesen ist. Weitere Informationen finden Sie in der [Twilio-Dokumentation](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS- und MMS-Nachrichten erstellen. [Weitere Informationen](sms-configuration-surface.md)

