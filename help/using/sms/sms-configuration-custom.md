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
source-git-commit: fc78fcfb0f2ce3616cb8b1df44dda2cfd66262fe
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 34%

---

# Konfigurieren eines benutzerdefinierten SMS-Anbieters {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="Anbieter-URL"
>abstract="Geben Sie die URL des externen APIs an, zu dem eine Verbindung hergestellt werden soll. Diese URL dient als Endpunkt für den Zugriff auf die API-Funktionen."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Header-Parameter"
>abstract="Geben Sie Label, Typ und Wert zusätzlicher Header an, um eine ordnungsgemäße Authentifizierung, Inhaltsformatierung und effektive API-Kommunikation zu ermöglichen. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Anbieter-Payload"
>abstract="Stellen Sie die Anfrage-Payload bereit, damit die korrekten Daten zur Verarbeitung und Antworterstellung gesendet werden."

>[!AVAILABILITY]
>
>Benutzerdefinierte Anbieter sind derzeit nur als Beta-Version für ausgewählte Benutzende verfügbar. Bitte wenden Sie sich an den Adobe-Support, um an der Beta teilzunehmen.
>Beachten Sie, dass diese Beta-Version keine eingehenden Nachrichten für die Verwaltung von Opt-in/Opt-out-Einverständnissen und Versandberichten unterstützt.


Diese Funktion ermöglicht es Ihnen, Ihre eigenen SMS-Provider zu integrieren und zu konfigurieren und bietet Ihnen Flexibilität, die über die Standardanbieter (Sinch, Twilio und Infobip) hinausgeht. Dies ermöglicht nahtlose SMS-Erstellung, -Versand, -Berichterstellung und -Einverständnisverwaltung.

Mit der benutzerdefinierten Provider-Konfiguration für SMS können Sie:

* Konfigurieren von benutzerdefinierten SMS-Anbietern direkt in Journey Optimizer.
* Erweiterte Payload-Anpassung für dynamisches Messaging verwenden.
* Verwalten Sie die Einverständnisvoreinstellungen (Opt-in/Opt-out), um die Einhaltung sicherzustellen.

## API-Anmeldedaten erstellen {#api-credential}

Um Nachrichten in Journey Optimizer mit einem benutzerdefinierten Anbieter zu versenden, der nicht von Adobe bereitgestellt wird (z.B. Sinch, Infobip, Twilio), gehen Sie wie folgt vor:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL API-Anmeldeinformationen]** und klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldeinformationen erstellen]**.

   ![](assets/sms_byo_1.png)

1. Konfigurieren Sie Ihre SMS-API-Anmeldedaten, wie unten beschrieben.

   * **[!UICONTROL SMS-Anbieter]**: Benutzerdefiniert.

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihre API-Anmeldeinformationen ein.

   * **[!UICONTROL Provider-AppId]**: Geben Sie die von Ihrem SMS-Anbieter bereitgestellte Anwendungs-ID ein.

   * **[!UICONTROL Anbietername]**: Geben Sie den Namen Ihres SMS-Anbieters ein.

   * **[!UICONTROL Provider-URL]**: Geben Sie die URL Ihres SMS-Anbieters ein.

   * **[!UICONTROL Authentifizierungstyp&#x200B;]**: Wählen Sie Ihren Autorisierungstyp aus und [ Sie je nach ](#auth-options) Authentifizierungsmethode die entsprechenden Felder aus.

     ![](assets/sms-byop.png)

1. Klicken Sie **[!UICONTROL Abschnitt]** Headers“ auf **[!UICONTROL Neuen Parameter hinzufügen]**, um die HTTP-Header für die Anfragenachricht anzugeben, die an den externen Service gesendet wird.

   Die Header **Felder** Content-Type) und **Charset** sind standardmäßig festgelegt und können nicht gelöscht werden.

   ![](assets/sms_byo_2.png)

1. Fügen Sie Ihre **[!UICONTROL Provider-Payload]** hinzu, um Ihre Anfrage-Payloads zu validieren und anzupassen.

   Sie können Ihre Payload mithilfe von Profilattributen dynamisch personalisieren und mithilfe integrierter Hilfsfunktionen sicherstellen, dass genaue Daten zur Verarbeitung und Antworterstellung gesendet werden.
<!--
1. Add your **Inbound settings** to determine how your system handles incoming messages and subscriber preferences: 

    * **[!UICONTROL Inbound Webhook URL]**: Specify the endpoint URL where inbound messages (e.g. replies or new messages from users) are sent.
    * **[!UICONTROL Opt-in Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-In Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-in Message]**: Enter the custom response that is automatically sent as your Opt-In Message.
    * **[!UICONTROL Opt-out Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-Out Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-out Message]**: Enter the custom response that is automatically sent as your Opt-Out Message.
-->

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API-Anmeldedaten]** auf das Papierkorbsymbol, um Ihre API-Anmeldedaten zu löschen.

   ![](assets/sms_byo_3.png)

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

   ![](assets/sms_byo_4.png)

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche für SMS-Nachrichten erstellen.  [Weitere Informationen](sms-configuration-surface.md)

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenbearbeitung, Personalisierung, Linktracking und Berichte nutzen.

### Authentifizierungsoptionen für benutzerdefinierte SMS-Anbieter {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Authentifizierungstyp"
>abstract="Geben Sie die Authentifizierungsmethode an, die für den Zugriff auf die API erforderlich ist. Dadurch wird eine sichere und autorisierte Kommunikation mit dem externen Service sichergestellt."

>[!BEGINTABS]

>[!TAB API-Schlüssel]

Nachdem Sie Ihre API-Anmeldedaten erstellt haben, füllen Sie die Felder aus, die für die API-Schlüsselauthentifizierung erforderlich sind:

* **[!UICONTROL Name]**&#x200B;: Geben Sie einen Namen für Ihre API-Schlüsselkonfiguration ein.
* **[!UICONTROL API-Token]**&#x200B;: Geben Sie das von Ihrem SMS-Anbieter bereitgestellte API-Token ein.

![](assets/sms-byop-api-key.png)

>[!TAB MAC-Authentifizierung]

Nachdem Sie Ihre API-Anmeldedaten erstellt haben, füllen Sie die Felder aus, die für die MAC-Authentifizierung erforderlich sind:

* **[!UICONTROL Name]**&#x200B;: Geben Sie einen Namen für Ihre MAC-Authentifizierungskonfiguration ein.
* **[!UICONTROL API-Token]**&#x200B;: Geben Sie das von Ihrem SMS-Anbieter bereitgestellte API-Token ein.
* **[!UICONTROL API-Geheimschlüssel]**: Geben Sie den von Ihrem SMS-Anbieter bereitgestellten API-Geheimschlüssel ein. Dieser Schlüssel wird verwendet, um den MAC (Nachrichtenauthentifizierungs-Code) für eine sichere Kommunikation zu generieren.
* **[!UICONTROL Hash-Format für Mac-Autorisierung]**: Wählen Sie das Hash-Format für die MAC-Authentifizierung.

![](assets/sms-byop-mac.png)

>[!TAB OAuth-Authentifizierung]

Nachdem Sie Ihre API-Anmeldedaten erstellt haben, füllen Sie die Felder aus, die für die OAuth-Authentifizierung erforderlich sind:

* **[!UICONTROL Name]**&#x200B;: Geben Sie einen Namen für Ihre OAuth-Authentifizierungskonfiguration ein.

* **[!UICONTROL API-Token]**&#x200B;: Geben Sie das von Ihrem SMS-Anbieter bereitgestellte API-Token ein.

* **[!UICONTROL OAuth URL]**&#x200B;: Geben Sie die URL zum Abrufen des OAuth-Tokens ein.

* **[!UICONTROL OAuth-]**&#x200B;: Stellen Sie den OAuth-Anfragetext im JSON-Format bereit, einschließlich Parametern wie `grant_type`, `client_id` und `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB JWT-Authentifizierung]

Nachdem Sie Ihre API-Anmeldedaten erstellt haben, füllen Sie die Felder aus, die für die JWT-Authentifizierung erforderlich sind:

* **[!UICONTROL Name]**&#x200B;: Geben Sie einen Namen für Ihre JWT-Authentifizierungskonfiguration ein.

* **[!UICONTROL API-Token]**&#x200B;: Geben Sie das von Ihrem SMS-Anbieter bereitgestellte API-Token ein.

* **[!UICONTROL JWT-Payload]**&#x200B;: Geben Sie die JSON-Payload ein, die die für das JWT erforderlichen Ansprüche enthält, z. B. Aussteller, Betreff, Zielgruppe und Gültigkeit.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
