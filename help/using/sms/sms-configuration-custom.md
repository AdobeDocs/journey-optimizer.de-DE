---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines benutzerdefinierten Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit einem benutzerdefinierten Anbieter konfigurieren
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 100%

---

# Konfigurieren eines benutzerdefinierten Anbieters {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="Provider-URL"
>abstract="Geben Sie die URL des externen API an, mit dem Sie eine Verbindung herstellen möchten. Diese URL dient als Endpunkt für den Zugriff auf die Funktionen und Möglichkeiten des API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Authentifizierungstyp"
>abstract="Geben Sie die Authentifizierungsmethode an, die für den Zugriff auf das API erforderlich ist, z. B. OAuth- oder Bearer-Token. Dies gewährleistet eine sichere und autorisierte Kommunikation mit dem externen Service."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Header-Parameter"
>abstract="Geben Sie Label, Typ und Wert zusätzlicher Kopfzeilen an, um eine ordnungsgemäße Authentifizierung, Inhaltsformatierung und effektive API-Kommunikation zu ermöglichen. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Provider-Payload"
>abstract="Geben Sie die Anfrage-Payload an, um sicherzustellen, dass die richtigen Daten zur Verarbeitung und Antworterstellung gesendet werden."

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

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenbearbeitung, Personalisierung, Linktracking und Berichte nutzen.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
