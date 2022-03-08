---
title: SMS-Konfiguration
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von SMS-Nachrichten mit Journey Optimizer konfigurieren
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 100%

---

# Konfigurieren des SMS-Kanals {#sms-configuration}

>[!CAUTION]
>
> Die Verwendung des SMS-Kanals ist derzeit nur für ausgewählte Benutzer verfügbar. Wenn Sie diese Funktion nutzen möchten, wenden Sie sich an Ihren Adobe-Kundenbetreuer.

[!DNL Journey Optimizer] ermöglicht es Ihnen, Journeys zu erstellen und Nachrichten an eine ausgewählte Audience zu senden.

## Erstellen neuer API-Anmeldeinformationen {#create-api}

Gehen Sie wie folgt vor, um Ihren SMS-Anbieter in Journey Optimizer zu konfigurieren:

1. Gehen Sie in das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL API-Anmeldeinformationen]** und klicken Sie auf **[!UICONTROL API-Anmeldeinformationen erstellen]**.

   ![](../assets/sms_4.png)

1. Wählen Sie Sinch als **[!UICONTROL SMS-Anbieter]** aus.

1. Geben Sie einen **[!UICONTROL Namen]** für Ihre API-Anmeldeinformationen ein.

1. Geben Sie Ihre **[!UICONTROL Service-ID]** und Ihr **[!UICONTROL API-Token]** ein.

   >[!NOTE]
   >
   > Für Sinch sind spezielle API-Anmeldeinformationen erforderlich. Greifen Sie über Ihren Sinch-Account auf das Menü „SMS“ > „APIs“ zu, um Ihre **[!UICONTROL Service-ID]** und Ihr **[!UICONTROL API-Token]** zu finden.

   ![](../assets/sms_5.png)

1. Wenn Sie die Konfiguration Ihrer API-Anmeldeinformationen abgeschlossen haben, klicken Sie auf **[!UICONTROL Senden]**.

Nachdem Sie Ihre API-Anmeldeinformationen erstellt und konfiguriert haben, müssen Sie jetzt eine Nachrichtenvoreinstellung für SMS-Nachrichten erstellen.

## Erstellen einer Nachrichtenvoreinstellung für SMS-Nachrichten {#message-preset-sms}

Nachdem Ihr SMS-Kanal konfiguriert wurde, müssen Sie eine Nachrichtenvoreinstellung erstellen, um über **[!DNL Journey Optimizer]** SMS-Nachrichten senden zu können.

Gehen Sie wie folgt vor, um eine Nachrichtenvoreinstellung zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Branding]** > **[!UICONTROL Nachrichtenvoreinstellungen]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvoreinstellung erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Voreinstellung ein und wählen Sie dann den SMS-Kanal aus.

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren Sie die **SMS**-Einstellungen.

   ![](../assets/preset-sms.png)

   * Wählen Sie den **[!UICONTROL SMS-Typ]** aus, der mit der Voreinstellung gesendet werden soll: **[!UICONTROL Transaktionsnachricht]** oder **[!UICONTROL Marketing]**.

   * Wählen Sie die **[!UICONTROL SMS-Konfiguration]** aus, um sie mit der Voreinstellung zu verknüpfen.

      Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von SMS-Nachrichten finden Sie in [diesem Abschnitt](sms-configuration.md).

   * Geben Sie die **[!UICONTROL Absendernummer]** ein, die Sie für Ihre Sendungen verwenden möchten.

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Nachrichtenvoreinstellung auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/sms_preset_2.png)

1. Nachdem die Nachrichtenvoreinstellung erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   >[!NOTE]
   >
   >In [diesem Abschnitt](#monitor-message-presets) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   ![](../assets/preset-active.png)

Sie können jetzt mit Journey Optimizer SMS-Nachrichten senden.

**Verwandte Themen**

* [Erstellen einer SMS-Nachricht](../messages/create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
