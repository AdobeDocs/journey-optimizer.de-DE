---
solution: Journey Optimizer
product: journey optimizer
title: Benutzerdefinierten Anbieter konfigurieren
description: Erfahren Sie, wie Sie Ihre Umgebung so konfigurieren, dass mit Journey Optimizer mit einem benutzerdefinierten Provider Textnachrichten gesendet werden.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 24%

---

# Benutzerdefinierten Anbieter konfigurieren (Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>Benutzerdefinierte Anbieter sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar. Wenden Sie sich an den Adobe-Support, um in die Beta-Version aufgenommen zu werden.
>
>Beachten Sie, dass diese Beta eingehende Nachrichten für die Zustimmungsverwaltung und die Versandberichterstellung nicht unterstützt.

Gehen Sie wie folgt vor, um Nachrichten in Journey Optimizer mit einem benutzerdefinierten Provider zu senden, der nicht standardmäßig von Adobe verfügbar ist (z. B. Sinch, Infobip, Twilio):

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie das Menü **[!UICONTROL API-Anmeldeinformationen]** aus.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldedaten erstellen]**.

   ![](assets/sms_byo_1.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Benutzerdefiniert.

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihre API-Berechtigung ein.

   * **[!UICONTROL Provider AppId]**: Geben Sie die von Ihrem SMS-Provider bereitgestellte Anwendungs-ID ein.

   * **[!UICONTROL Provider Name]**: Geben Sie den Namen Ihres SMS-Anbieters ein.

   * **[!UICONTROL Anbieter-URL]**: Geben Sie die URL Ihres SMS-Anbieters ein.

   * **[!UICONTROL Authentifizierungstyp &#x200B;]**: Wählen Sie Ihren Autorisierungstyp aus. Unterstützte Autorisierungstypen sind **Bearer App** oder **Einfach**.

   * **[!UICONTROL API-Token]**: Geben Sie das von Ihrem SMS-Provider bereitgestellte API-Token ein.

   * **[!UICONTROL Provider-Payload]**: Fügen Sie Ihre Provider-Payload hinzu, z. B. `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Stellen Sie sicher, dass die Payload `{{toNumber}}`, `{{fromNumber}}`, `{{message}}` enthält.

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

Nach der Konfiguration können Sie alle nativen Kanalfunktionen wie Nachrichtenbearbeitung, Personalisierung, Linktracking und Reporting nutzen.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
