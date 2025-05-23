---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren eines benutzerdefinierten Anbieters
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von Textnachrichten mit Journey Optimizer mit einem benutzerdefinierten Anbieter konfigurieren
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 37313ca8a9527c934d8aeaf265e9674219726636
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 21%

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

Diese Funktion ermöglicht es Ihnen, Ihre eigenen SMS-Provider zu integrieren und zu konfigurieren und bietet Ihnen Flexibilität, die über die Standardanbieter (Sinch, Twilio und Infobip) hinausgeht. Dies ermöglicht nahtlose SMS-Erstellung, -Versand, -Berichterstellung und -Einverständnisverwaltung.

Mit der benutzerdefinierten Anbieterkonfiguration für SMS können Sie benutzerdefinierte SMS-Anbieter direkt in Journey Optimizer konfigurieren, die erweiterte Payload-Anpassung für dynamisches Messaging verwenden und Einverständnisvoreinstellungen (Opt-in/Opt-out) verwalten, um die Einhaltung der Vorgaben sicherzustellen.

Gehen Sie wie folgt vor, um Ihren benutzerdefinierten SMS-Anbieter zu konfigurieren:

1. [API-Anmeldedaten erstellen](#api-credential)
1. [Webhook erstellen](#webhook)
1. [Erstellen einer Kanalkonfiguration](sms-configuration-surface.md)
1. [Erstellen von Journey oder Campaign mit SMS-Kanalaktion](create-sms.md)

## API-Anmeldedaten erstellen {#api-credential}

Um Nachrichten in Journey Optimizer mit einem benutzerdefinierten Anbieter zu versenden, der nicht von Adobe bereitgestellt wird (z.B. Sinch, Infobip, Twilio), gehen Sie wie folgt vor:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL API-Anmeldeinformationen]** unter **[!UICONTROL SMS-Einstellungen]** und klicken Sie auf die Schaltfläche **[!UICONTROL Neue API-Anmeldeinformationen erstellen]**.

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

1. Wenn Sie die Konfiguration Ihrer API-Anmeldedaten abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL API]** Anmeldedaten auf das ![bin-Symbol](assets/do-not-localize/Smock_Delete_18_N.svg), um Ihre API-Anmeldedaten zu löschen.

   ![](assets/sms_byo_3.png)

1. Um vorhandene Anmeldedaten zu ändern, suchen Sie die gewünschten API-Anmeldedaten und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

   ![](assets/sms_byo_4.png)

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt [die Einstellungen für den Webhook) für SMS-](#webhook) einrichten.

### Authentifizierungsoptionen für benutzerdefinierte SMS-Anbieter {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Authentifizierungstyp"
>abstract="Geben Sie die Authentifizierungsmethode an, die für den Zugriff auf das API erforderlich ist. Dadurch wird eine sichere und autorisierte Kommunikation mit dem externen Dienst sichergestellt."

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

## Webhook erstellen {#webhook}

>[!BEGINSHADEBOX]

Wenn keine Opt-in- oder Opt-out-Keywords angegeben werden, werden standardmäßige Einverständnisnachrichten verwendet, um den Datenschutz der Benutzenden zu berücksichtigen. Durch das Hinzufügen benutzerdefinierter Keywords werden die Standardwerte automatisch überschrieben.

**Standard-Schlüsselwörter:**

* **Opt-in**: ABONNIEREN, JA, UNSTOP, START, FORTSETZEN, FORTSETZEN, BEGINNEN
* **Opt-out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NEIN
* **Hilfe**: HILFE

>[!ENDSHADEBOX]

Nachdem Ihre API-Anmeldeinformationen erfolgreich erstellt wurden, besteht der nächste Schritt darin, einen Webhook zu erstellen und Ihre eingehenden Einstellungen zu konfigurieren. Diese Konfiguration stellt sicher, dass Ihr System eingehende Daten oder Nachrichten ordnungsgemäß empfangen und verarbeiten kann.

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL SMS-Webhooks]** unter **[!UICONTROL SMS-Einstellungen]** und klicken Sie auf die Schaltfläche **[!UICONTROL Webhook erstellen]**.

   ![](assets/sms_byo_5.png)

1. Konfigurieren Sie Ihre Webhook-Einstellungen, wie unten beschrieben:

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihren Webhook ein.

   * **[!UICONTROL SMS-Anbieter auswählen]**: Benutzerdefiniert.

   * **[!UICONTROL API-Anmeldeinformationen auswählen]**: Wählen Sie aus der Dropdown-Liste, die Sie [zuvor konfigurierte API-Anmeldeinformationen](#api-credential).

   * **[!UICONTROL Opt-in-Schlüsselwörter]**: Geben Sie die standardmäßigen oder benutzerdefinierten Schlüsselwörter ein, durch die Ihre Opt-in-Nachricht automatisch in einen Trigger umgewandelt wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-in-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-in-Nachricht gesendet wird.

   * **[!UICONTROL Opt-out-Keywords]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, mit denen Ihre Opt-out-Nachricht automatisch in Trigger gesetzt wird. Verwenden Sie für mehrere Keywords kommagetrennte Werte.

   * **[!UICONTROL Opt-out-Nachricht]**: Geben Sie die benutzerdefinierte Antwort ein, die automatisch als Opt-out-Nachricht gesendet wird.

   ![](assets/sms_byo_6.png)

1. Klicken Sie **[!UICONTROL Payload-Editor anzeigen]**, um Ihre Anfrage-Payloads zu validieren und anzupassen.

   Sie können Ihre Payload mithilfe von Profilattributen dynamisch personalisieren und mithilfe integrierter Hilfsfunktionen sicherstellen, dass genaue Daten zur Verarbeitung und Antworterstellung gesendet werden.

1. Klicken Sie **[!UICONTROL Senden]** wenn Sie die Konfiguration Ihres Webhooks abgeschlossen haben.

1. Klicken Sie im **[!UICONTROL Webhooks]** auf das ![bin-Symbol](assets/do-not-localize/Smock_Delete_18_N.svg), um Ihren Webhook zu löschen.

1. Um die vorhandene Konfiguration zu ändern, suchen Sie den gewünschten Webhook und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

1. Greifen Sie auf Ihre neue (Webhook **[!UICONTROL URL zu und kopieren Sie]** von Ihrem zuvor gesendeten **[!UICONTROL Webhook]**.

   ![](assets/sms_byo_7.png)

Nachdem Sie die Einstellungen für den eingehenden Webhook erstellt und konfiguriert haben, müssen Sie jetzt eine [Kanalkonfiguration](sms-configuration-surface.md) für SMS-Nachrichten erstellen.

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenbearbeitung, Personalisierung, Linktracking und Berichte nutzen.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

