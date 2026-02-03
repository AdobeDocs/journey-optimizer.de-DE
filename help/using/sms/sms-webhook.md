---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Webhook konfigurieren
description: Erfahren Sie, wie Sie Webhooks konfigurieren, um eingehende Antworten für die Verwaltung des Opt-in- und Opt-out-Einverständnisses zu erfassen
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 73%

---

# Erstellen eines Webhook {#webhook}

>[!BEGINSHADEBOX]

Wenn keine Opt-in- oder Opt-out-Keywords angegeben werden, werden standardmäßige Einverständnisnachrichten verwendet, um den Datenschutz der Benutzenden zu berücksichtigen. Durch das Hinzufügen benutzerdefinierter Keywords werden die Standardwerte automatisch überschrieben.

**Standard-Keywords:**

* **Opt-in**: SUBSCRIBE, YES, UNSTOP, START, CONTINUE, RESUME, BEGIN
* **Opt-out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NO
* **Hilfe**: HELP.

>[!ENDSHADEBOX]

Nachdem Ihre API-Anmeldedaten erfolgreich erstellt wurden, können Sie jetzt Webhooks konfigurieren, um eingehende Antworten für die Verwaltung des Opt-in- und Opt-out-Einverständnisses zu erfassen und Versandberichte einschließlich Lesebestätigungen (sofern verfügbar) zu erhalten.

Beim Einrichten eines Webhooks können Sie seinen Zweck basierend auf dem Typ der Daten definieren, die Sie erfassen möchten:

* **[!UICONTROL Eingehend]**: Verwenden Sie diese Option, wenn Sie Einverständnisantworten wie Opt-ins oder Opt-outs und Benutzereinstellungen erfassen möchten.

* **[!UICONTROL Feedback]**: Wählen Sie diese Option aus, um Versand- und Interaktionsereignisse einschließlich Lesebestätigungen und Benutzerinteraktionen zu verfolgen, um Reporting und Analysen zu unterstützen.

Durchsuchen Sie je nach SMS-Anbieter die folgenden Registerkarten:

>[!BEGINTABS]

>[!TAB Benutzerspezifisch]

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL SMS-Webhooks]** unter **[!UICONTROL SMS-Einstellungen]** aus und klicken Sie auf die Schaltfläche **[!UICONTROL Webhook erstellen]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Konfigurieren Sie Ihre Webhook-Einstellungen wie unten beschrieben:

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihren Webhook ein.

   * **[!UICONTROL SMS-Anbieter auswählen]**: Benutzerdefiniert.

   * **[!UICONTROL Typ]**: Eingehend.

   * **[!UICONTROL API-Anmeldedaten]**: Wählen Sie aus der Dropdown-Liste die [zuvor konfigurierten API-Anmeldedaten](sms-configuration-custom.md#api-credential) aus.

   * **[!UICONTROL Absendertelefonnummer]**: Geben Sie die Telefonnummer der Absenderin bzw. des Absenders ein, die Sie für Ihre Nachrichten verwenden möchten.

     ![](assets/webhook-inbound.png){zoomable="yes"}

1. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg) , um Ihre Keyword-Kategorien hinzuzufügen, und konfigurieren Sie sie dann je nach SMS-Anbieter:

   * **[!UICONTROL Kategorie für eingehende Keywords]**: Wählen Sie für Ihre Keyword-Kategorien entweder **[!UICONTROL Opt-in]**, **[!UICONTROL Opt-out]**, **[!UICONTROL Double-Opt-in]**, **[!UICONTROL Hilfe]** oder **[!UICONTROL Benutzerdefiniert]**.

   * **[!UICONTROL Keyword eingeben]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Nachricht automatisch ausgelöst wird. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg), um mehrere Keywords hinzuzufügen.

     Verwenden Sie für **[!UICONTROL Benutzerdefiniertes Keyword]** nicht einverständnisbezogene Keywords für Batch-basierte Aktionen innerhalb einer Journey.

   * **[!UICONTROL Antwortnachricht]**: Wählen Sie aus der Dropdown-Liste die benutzerdefinierte Antwort aus, die automatisch gesendet wird.

   * **[!UICONTROL Unscharfes Opt-out]**: Aktivieren Sie diese Option, um eine automatische Antwort zu senden, wenn ein Keyword erkannt wird, das nahezu einer Übereinstimmung entspricht.

   ![](assets/sms_byo_6.png){zoomable="yes"}

1. Geben Sie eine **[!UICONTROL Standardantwortnachricht]** ein, die automatisch gesendet wird, wenn eine eingehende Nachricht keinem konfigurierten Schlüsselwort oder keiner konfigurierten Kategorie entspricht.

1. Klicken Sie auf **[!UICONTROL Payload-Editor anzeigen]**, um Ihre Anfrage-Payloads zu validieren und anzupassen.

   Sie können Ihre Payload mithilfe von Profilattributen dynamisch personalisieren und mithilfe integrierter Hilfsfunktionen sicherstellen, dass genaue Daten zur Verarbeitung und Antworterstellung gesendet werden.

1. Wenn Sie die Konfiguration Ihres Webhook abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Um einen **[!UICONTROL Feedback]**-Webhook zu erstellen, gehen Sie wie oben beschrieben vor, indem Sie **[!UICONTROL Feedback]** als Webhook auswählen **[!UICONTROL Typ]**.

1. Über das **[!UICONTROL Webhooks]**-Menü können Sie vorhandene Webhooks bearbeiten oder löschen oder auf die **[!UICONTROL Webhook-URL]** zugreifen und diese kopieren, um sie in Ihren SMS-Anbieter zu integrieren.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Nachdem Sie die Einstellungen für den Webhook erstellt und konfiguriert haben, müssen Sie jetzt eine [Kanalkonfiguration](sms-configuration-surface.md) für SMS-Nachrichten erstellen.

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenerstellung, Personalisierung, Linktracking und Reporting nutzen.

>[!TAB Infobip]

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL SMS-Webhooks]** unter **[!UICONTROL SMS-Einstellungen]** aus und klicken Sie auf die Schaltfläche **[!UICONTROL Webhook erstellen]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Konfigurieren Sie Ihre Webhook-Einstellungen wie unten beschrieben:

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihren Webhook ein.

   * **[!UICONTROL SMS-Anbieter auswählen]**: Infobip.

   * **[!UICONTROL Typ]**: Eingehend.

   * **[!UICONTROL API-Anmeldedaten]**: Wählen Sie aus der Dropdown-Liste die [zuvor konfigurierten API-Anmeldedaten](sms-configuration-infobip.md#api-credential) aus.

   * **[!UICONTROL Absendertelefonnummer]**: Geben Sie die Telefonnummer der Absenderin bzw. des Absenders ein, die Sie für Ihre Nachrichten verwenden möchten.

     ![](assets/webhook-infobip-1.png){zoomable="yes"}

1. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg) , um Ihre Keyword-Kategorien hinzuzufügen, und konfigurieren Sie sie dann je nach SMS-Anbieter:

   * **[!UICONTROL Kategorie für eingehende Keywords]**: Wählen Sie für Ihre Keyword-Kategorien entweder **[!UICONTROL Opt-in]**, **[!UICONTROL Opt-out]**, **[!UICONTROL Double-Opt-in]**, **[!UICONTROL Hilfe]** oder **[!UICONTROL Benutzerdefiniert]**.

   * **[!UICONTROL Keyword eingeben]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Nachricht automatisch ausgelöst wird. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg), um mehrere Keywords hinzuzufügen.

     Verwenden Sie für **[!UICONTROL Benutzerdefiniertes Keyword]** nicht einverständnisbezogene Keywords für Batch-basierte Aktionen innerhalb einer Journey.

   * **[!UICONTROL Antwortnachricht]**: Wählen Sie aus der Dropdown-Liste die benutzerdefinierte Antwort aus, die automatisch gesendet wird.

   * **[!UICONTROL Unscharfes Opt-out]**: Aktivieren Sie diese Option, um eine automatische Antwort zu senden, wenn ein Keyword erkannt wird, das nahezu einer Übereinstimmung entspricht.

   ![](assets/webhook-infobip-2.png){zoomable="yes"}

1. Geben Sie eine **[!UICONTROL Standardantwortnachricht]** ein, die automatisch gesendet wird, wenn eine eingehende Nachricht keinem konfigurierten Schlüsselwort oder keiner konfigurierten Kategorie entspricht.

1. Wenn Sie die Konfiguration Ihres Webhook abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Um einen **[!UICONTROL Feedback]**-Webhook zu erstellen, gehen Sie wie oben beschrieben vor, indem Sie **[!UICONTROL Feedback]** als Webhook auswählen **[!UICONTROL Typ]**.

1. Über das **[!UICONTROL Webhooks]**-Menü können Sie vorhandene Webhooks bearbeiten oder löschen oder auf die **[!UICONTROL Webhook-URL]** zugreifen und diese kopieren, um sie in Ihren SMS-Anbieter zu integrieren.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Nachdem Sie die Einstellungen für „eingehend“ für den Webhook erstellt und konfiguriert haben, müssen Sie jetzt eine [Kanalkonfiguration](sms-configuration-surface.md) für SMS-Nachrichten erstellen. 

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenerstellung, Personalisierung, Linktracking und Reporting nutzen.

>[!TAB Sinch]

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL SMS-Webhooks]** unter **[!UICONTROL SMS-Einstellungen]** aus und klicken Sie auf die Schaltfläche **[!UICONTROL Webhook erstellen]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Konfigurieren Sie Ihre Webhook-Einstellungen wie unten beschrieben:

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihren Webhook ein.

   * **[!UICONTROL SMS-Anbieter auswählen]**: Sinch.

   * **[!UICONTROL Typ]**: Eingehend.

   * **[!UICONTROL API-Anmeldedaten]**: Wählen Sie aus der Dropdown-Liste die [zuvor konfigurierten API-Anmeldedaten](sms-configuration-sinch.md#create-api) aus.

   * **[!UICONTROL Absendertelefonnummer]**: Geben Sie die Telefonnummer der Absenderin bzw. des Absenders ein, die Sie für Ihre Nachrichten verwenden möchten.

     ![](assets/webhook-sinch-1.png){zoomable="yes"}

1. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg) , um Ihre Keyword-Kategorien hinzuzufügen, und konfigurieren Sie sie dann je nach SMS-Anbieter:

   * **[!UICONTROL Kategorie für eingehende Keywords]**: Wählen Sie für Ihre Keyword-Kategorien entweder **[!UICONTROL Opt-in]**, **[!UICONTROL Opt-out]**, **[!UICONTROL Double-Opt-in]**, **[!UICONTROL Hilfe]** oder **[!UICONTROL Benutzerdefiniert]**.

   * **[!UICONTROL Keyword eingeben]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Nachricht automatisch ausgelöst wird. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg), um mehrere Keywords hinzuzufügen.

     Verwenden Sie für **[!UICONTROL Benutzerdefiniertes Keyword]** nicht einverständnisbezogene Keywords für Batch-basierte Aktionen innerhalb einer Journey.

   * **[!UICONTROL Antwortnachricht]**: Wählen Sie aus der Dropdown-Liste die benutzerdefinierte Antwort aus, die automatisch gesendet wird.

   * **[!UICONTROL Unscharfes Opt-out]**: Aktivieren Sie diese Option, um eine automatische Antwort zu senden, wenn ein Keyword erkannt wird, das nahezu einer Übereinstimmung entspricht.

   ![](assets/webhook-sinch-2.png){zoomable="yes"}

1. Geben Sie eine **[!UICONTROL Standardantwortnachricht]** ein, die automatisch gesendet wird, wenn eine eingehende Nachricht keinem konfigurierten Schlüsselwort oder keiner konfigurierten Kategorie entspricht.

1. Wenn Sie die Konfiguration Ihres Webhook abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL Webhooks]** auf ![Papierkorbsymbol](assets/do-not-localize/Smock_Delete_18_N.svg), um Ihren Webhook zu löschen.

1. Um vorhandene Konfigurationen zu ändern, suchen Sie den gewünschten Webhook und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

1. Greifen Sie über Ihren zuvor gesendeten **[!UICONTROL Webhook]** auf Ihre neue **[!UICONTROL Webhook-URL]** zu und kopieren Sie sie.

   ![](assets/sms_byo_7.png){zoomable="yes"}

Nachdem Sie die Einstellungen für „eingehend“ für den Webhook erstellt und konfiguriert haben, müssen Sie jetzt eine [Kanalkonfiguration](sms-configuration-surface.md) für SMS-Nachrichten erstellen. 

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenerstellung, Personalisierung, Linktracking und Reporting nutzen.

>[!TAB Twilio]

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** `>` **[!UICONTROL Kanäle]**, wählen Sie das Menü **[!UICONTROL SMS-Webhooks]** unter **[!UICONTROL SMS-Einstellungen]** aus und klicken Sie auf die Schaltfläche **[!UICONTROL Webhook erstellen]**.

   ![](assets/sms_byo_5.png){zoomable="yes"}

1. Konfigurieren Sie Ihre Webhook-Einstellungen wie unten beschrieben:

   * **[!UICONTROL Name]**: Geben Sie einen Namen für Ihren Webhook ein.

   * **[!UICONTROL Wählen Sie SMS-Anbieter]**: Twilio.

   * **[!UICONTROL Typ]**: Eingehend.

   * **[!UICONTROL API-Anmeldedaten]**: Wählen Sie aus der Dropdown-Liste die [zuvor konfigurierten API-Anmeldedaten](sms-configuration-twilio.md#create-api) aus.

   * **[!UICONTROL Absendertelefonnummer]**: Geben Sie die Telefonnummer der Absenderin bzw. des Absenders ein, die Sie für Ihre Nachrichten verwenden möchten.

1. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg) , um Ihre Keyword-Kategorien hinzuzufügen, und konfigurieren Sie sie dann je nach SMS-Anbieter:

   * **[!UICONTROL Kategorie für eingehende Keywords]**: Wählen Sie für Ihre Keyword-Kategorien entweder **[!UICONTROL Opt-in]**, **[!UICONTROL Opt-out]**, **[!UICONTROL Double-Opt-in]**, **[!UICONTROL Hilfe]** oder **[!UICONTROL Benutzerdefiniert]**.

   * **[!UICONTROL Keyword eingeben]**: Geben Sie die standardmäßigen oder benutzerdefinierten Keywords ein, durch die Ihre Nachricht automatisch ausgelöst wird. Klicken Sie auf ![](assets/do-not-localize/Smock_Add_18_N.svg), um mehrere Keywords hinzuzufügen.

     Verwenden Sie für **[!UICONTROL Benutzerdefiniertes Keyword]** nicht einverständnisbezogene Keywords für Batch-basierte Aktionen innerhalb einer Journey.

   * **[!UICONTROL Antwortnachricht]**: Wählen Sie aus der Dropdown-Liste die benutzerdefinierte Antwort aus, die automatisch gesendet wird.

   * **[!UICONTROL Unscharfes Opt-out]**: Aktivieren Sie diese Option, um eine automatische Antwort zu senden, wenn ein Keyword erkannt wird, das nahezu einer Übereinstimmung entspricht.

1. Geben Sie eine **[!UICONTROL Standardantwortnachricht]** ein, die automatisch gesendet wird, wenn eine eingehende Nachricht keinem konfigurierten Schlüsselwort oder keiner konfigurierten Kategorie entspricht.

1. Wenn Sie die Konfiguration Ihres Webhook abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

1. Klicken Sie im Menü **[!UICONTROL Webhooks]** auf ![Papierkorbsymbol](assets/do-not-localize/Smock_Delete_18_N.svg), um Ihren Webhook zu löschen.

1. Um vorhandene Konfigurationen zu ändern, suchen Sie den gewünschten Webhook und klicken Sie auf die Option **[!UICONTROL Bearbeiten]**, um die erforderlichen Änderungen vorzunehmen.

1. Greifen Sie über Ihren zuvor gesendeten **[!UICONTROL Webhook]** auf Ihre neue **[!UICONTROL Webhook-URL]** zu und kopieren Sie sie.

Nachdem Sie die Einstellungen für „eingehend“ für den Webhook erstellt und konfiguriert haben, müssen Sie jetzt eine [Kanalkonfiguration](sms-configuration-surface.md) für SMS-Nachrichten erstellen. 

Nach der Konfiguration können Sie alle betriebsbereiten Kanalfunktionen wie Nachrichtenerstellung, Personalisierung, Linktracking und Reporting nutzen.


>[!ENDTABS]


## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)

