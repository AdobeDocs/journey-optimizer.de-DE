---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Konfiguration
description: Erfahren Sie, wie Sie Ihre Umgebung so konfigurieren, dass SMS mit Journey Optimizer gesendet werden
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a7c9cbcc23e4a2ef8a3acd887c0f51e51c5befc0
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# SMS-Kanal konfigurieren {#sms-configuration}

[!DNL Journey Optimizer] ermöglicht Ihnen das Erstellen Ihrer Journeys und das Senden von Nachrichten an eine bestimmte Zielgruppe.

Konfigurieren Sie vor dem SMS-Versand Ihre Instanz. Sie müssen [Provider-Einstellungen integrieren](#create-api) mit Journey Optimizer und [SMS-Oberfläche erstellen](#message-preset-sms) (d. h. SMS-Vorgabe). Diese Schritte müssen von einem [Adobe Journey Optimizer-Systemadministrator](../start/path/administrator.md).

>[!IMPORTANT]
>
>Adobe Journey Optimizer lässt sich derzeit mit Drittanbietern wie Sinch und Twilio integrieren, die SMS-Dienste unabhängig von Adobe Journey Optimizer anbieten.  Vor der SMS-Konfiguration müssen Sie bei einem dieser SMS-Provider ein Konto erstellen, um das API-Token und die Service-ID zu erhalten, über das Sie die Verbindung zwischen Adobe Journey Optimizer und dem entsprechenden SMS-Provider herstellen können. Ihre Nutzung von SMS-Diensten unterliegt zusätzlichen Bedingungen des jeweiligen SMS-Anbieters. Da Sinch und Twilio Drittanbieterprodukte sind, die Adobe Journey Optimizer-Benutzern über eine Integration zur Verfügung stehen, müssen sich Benutzer von Sinch oder Twilio bei allen Fragen oder Anfragen im Zusammenhang mit SMS-Diensten an den jeweiligen SMS-Provider wenden, um Unterstützung zu erhalten. Adobe hat keine Kontrolle und ist nicht für Produkte von Drittanbietern verantwortlich.

## Erstellen neuer API-Anmeldedaten {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Konfigurieren Ihres SMS-Anbieters mit Journey Optimizer"
>abstract="Wählen Sie Ihren Anbieter aus und geben Sie Ihre SMS-API-Anmeldeinformationen ein."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Konfigurieren Ihres SMS-Anbieters mit Journey Optimizer"
>abstract="Vor dem SMS-Versand müssen Sie die Provider-Einstellungen in Journey Optimizer integrieren. Danach müssen Sie eine SMS-Oberfläche erstellen. Diese Schritte müssen von einem Adobe Journey Optimizer-Systemadministrator durchgeführt werden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=en#message-preset-sms" text="SMS-Kanaloberfläche erstellen"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Wählen Sie die Konfiguration des SMS-Anbieters aus."
>abstract="Wählen Sie die für Ihren SMS-Anbieter konfigurierten API-Anmeldeinformationen aus."

Gehen Sie wie folgt vor, um Ihren SMS-Anbieter mit Journey Optimizer zu konfigurieren:

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** Menü und klicken Sie auf **[!UICONTROL Create API credential]**.

   ![](assets/sms_6.png)

1. Wählen Sie Ihre **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]. Suchen Sie nach **[!UICONTROL Service ID]** und **[!UICONTROL API Token]**, greifen Sie über Ihr Einzelkonto auf das Menü SMS > APIs zu.
   * [!DNL Twilio]. Suchen Sie nach **[!UICONTROL Service ID]** und **[!UICONTROL API Token]**, greifen Sie auf den Bereich Kontoinformationen der Konsole-Dashboard -Seite zu.

1. Geben Sie einen **[!UICONTROL Name]** für Ihre API-Anmeldedaten.

1. Geben Sie Ihre **[!UICONTROL Service ID]** und **[!UICONTROL API Token]**.

   ![](assets/sms_7.png)

1. Klicken **[!UICONTROL Submit]** als Sie die Konfiguration Ihrer API-Anmeldeinformationen abgeschlossen haben.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Kanaloberfläche (d. h. eine Nachrichtenvorgabe) für SMS-Nachrichten erstellen.

## Erstellen einer Kanaloberfläche für SMS-Nachrichten {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="SMS-Kategorie definieren"
>abstract="Wählen Sie unter Verwendung dieser Oberfläche den Typ der zu sendenden SMS-Nachrichten aus: Marketing für Werbe-SMS-Nachrichten, für die die Zustimmung des Benutzers erforderlich ist, oder Transaktionen für nicht kommerzielle SMS-Nachrichten, die in bestimmten Kontexten auch an abgemeldete Profile gesendet werden können."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="Abmeldung in Marketing-SMS-Nachrichten"

Nachdem Ihr SMS-Kanal konfiguriert wurde, müssen Sie eine Kanaloberfläche erstellen, über die Sie SMS-Nachrichten senden können. **[!DNL Journey Optimizer]**.

Gehen Sie wie folgt vor, um eine Kanaloberfläche zu erstellen:

1. Zugriff auf **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** Menü und klicken Sie auf **[!UICONTROL Create channel surface]**.

   ![](assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Oberfläche ein und wählen Sie dann den SMS-Kanal aus.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A-Z) beginnen. Sie darf nur alphanumerische Zeichen enthalten. Sie können auch Unterstriche verwenden `_`, Punkt`.` und Bindestrich `-` Zeichen.

1. Konfigurieren Sie die **SMS** -Einstellungen.

   ![](assets/preset-sms.png)

   * Wählen Sie die **[!UICONTROL SMS Type]** wird mit der Oberfläche gesendet: **[!UICONTROL Transactional]** oder **[!UICONTROL Marketing]**.

   * Wählen Sie die **[!UICONTROL SMS configuration]** mit der Oberfläche zu verknüpfen.

      Weiterführende Informationen zur Konfiguration der Umgebung für den Versand von SMS-Nachrichten finden Sie im Abschnitt [diesem Abschnitt](#create-api).

   * Geben Sie die **[!UICONTROL Sender number]** &#x200B; Sie für Ihre Kommunikation verwenden möchten.

   * Wählen Sie Ihre **[!UICONTROL SMS Execution Field]** zur Auswahl der **[!UICONTROL Profile attribute]** mit den Telefonnummern der Profile verknüpft sind.

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie auf **[!UICONTROL Submit]** zur Bestätigung. Sie können die Kanaloberfläche auch als Entwurf speichern und die Konfiguration später fortsetzen.

   ![](assets/sms_preset_2.png)

1. Nachdem die Kanaloberfläche erstellt wurde, wird sie in der Liste mit der **[!UICONTROL Processing]** Status.

   >[!NOTE]
   >
   >Wenn die Prüfungen nicht erfolgreich sind, erfahren Sie mehr über die möglichen Fehlerursachen in [diesem Abschnitt](#monitor-channel-surfaces).

1. Sobald die Prüfungen erfolgreich sind, erhält die Kanaloberfläche die **[!UICONTROL Active]** Status. Es kann zum Versand von Nachrichten verwendet werden.

   ![](assets/preset-active.png)

Jetzt können Sie mit Journey Optimizer SMS-Nachrichten senden.

**Verwandte Themen**

* [SMS erstellen](create-sms.md)
* [Hinzufügen einer Nachricht in einer Journey](../building-journeys/journeys-message.md)
