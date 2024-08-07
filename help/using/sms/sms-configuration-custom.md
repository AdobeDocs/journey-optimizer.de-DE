---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines benutzerdefinierten Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit einem benutzerdefinierten Anbieter konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: ht
source-wordcount: '250'
ht-degree: 100%

---

# Konfigurieren eines benutzerdefinierten Anbieters (Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>Benutzerdefinierte Anbieter sind derzeit nur als Beta-Version für ausgewählte Benutzende verfügbar. Bitte wenden Sie sich an den Adobe-Support, um an der Beta teilzunehmen.
>
>Beachten Sie, dass diese Beta-Version keine eingehenden Nachrichten für die Verwaltung von Opt-in/Opt-out-Einverständnissen und Versandberichten unterstützt.

Um Nachrichten in Journey Optimizer mit einem benutzerdefinierten Anbieter zu versenden, der nicht von Adobe bereitgestellt wird (z.B. Sinch, Infobip, Twilio), gehen Sie wie folgt vor:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** und wählen Sie das Menü **[!UICONTROL API-Anmeldedaten]**.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

   ![](assets/sms_byo_1.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Benutzerdefiniert.

   * **[!UICONTROL Name]**: Wählen Sie einen Namen für Ihre API-Anmeldedaten.

   * **[!UICONTROL Anbieter-App-ID]**: Geben Sie die von Ihrem SMS-Anbieter bereitgestellte Anwendungs-ID ein.

   * **[!UICONTROL Anbietername]**: Geben Sie den Namen Ihres SMS-Anbieters ein.

   * **[!UICONTROL Anbieter-URL]**: Geben Sie die URL Ihres SMS-Anbieters ein.

   * **[!UICONTROL Authentifizierungstyp]**: Wählen Sie Ihren Autorisierungstyp aus. Unterstützte Autorisierungstypen sind **Bearer App** oder **Basic**.

   * **[!UICONTROL API-Token]**: Geben Sie das von Ihrem SMS-Anbieter bereitgestellte API-Token ein.

   * **[!UICONTROL Anbieter-Payload]**: Fügen Sie Ihre Anbieter-Payload hinzu, z. B. `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Stellen Sie sicher, dass die Payload `{{toNumber}}`, `{{fromNumber}}`, `{{message}}` enthält.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenbearbeitung, Personalisierung, Linktracking und Berichte nutzen.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
