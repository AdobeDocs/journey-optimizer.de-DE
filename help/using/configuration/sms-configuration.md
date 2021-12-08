---
title: SMS-Konfiguration
description: Erfahren Sie, wie Sie Ihre Umgebung so konfigurieren, dass SMS-Nachrichten mit Journey Optimizer gesendet werden
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: c86c9121e601f0c208626f578e923e7d30adc9c4
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 35%

---

# SMS-Kanal konfigurieren {#sms-configuration}

>[!CAUTION]
>
> Die Verwendung des SMS-Kanals ist derzeit nur für ausgewählte Benutzer verfügbar. Wenn Sie diese Funktion nutzen möchten, wenden Sie sich an Ihren Kundenbetreuer bei der Adobe.

[!DNL Journey Optimizer] ermöglicht es Ihnen, Journeys zu erstellen und Nachrichten an eine ausgewählte Audience zu senden.

## Erstellen neuer API-Anmeldedaten {#create-api}

Gehen Sie wie folgt vor, um Ihren SMS-Anbieter mit Journey Optimizer zu konfigurieren:

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL API-Anmeldeinformationen]** Menü und klicken Sie auf **[!UICONTROL API-Anmeldeinformationen erstellen]**.

   ![](../assets/sms_4.png)

1. Wählen Sie Sinken als **[!UICONTROL SMS-Anbieter]**.

1. Geben Sie einen **[!UICONTROL Name]** für Ihre API-Anmeldedaten.

1. Geben Sie Ihre **[!UICONTROL Dienst-ID]** und **[!UICONTROL API-Token]**.

   >[!NOTE]
   >
   > Für Sinch sind spezielle API-Anmeldeinformationen erforderlich. Suchen Sie nach **[!UICONTROL Dienst-ID]** und **[!UICONTROL API-Token]**, greifen Sie über Ihr Einzelkonto auf das Menü SMS > APIs zu,

   ![](../assets/sms_5.png)

1. Klicken **[!UICONTROL Einsenden]** als Sie die Konfiguration Ihrer API-Anmeldeinformationen abgeschlossen haben.

Nachdem Sie Ihre API-Anmeldedaten erstellt und konfiguriert haben, müssen Sie jetzt eine Nachrichtenvorgabe für SMS-Nachrichten erstellen.

## Nachrichtenvorgabe für SMS-Nachrichten erstellen {#message-preset-sms}

Nachdem Ihr SMS-Kanal konfiguriert wurde, müssen Sie eine Nachrichtenvorgabe erstellen, über die Sie SMS-Nachrichten senden können **[!DNL Journey Optimizer]**.

Gehen Sie wie folgt vor, um eine Nachrichtenvoreinstellung zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Branding]** > **[!UICONTROL Nachrichtenvoreinstellungen]** auf und klicken Sie dann auf **[!UICONTROL Nachrichtenvoreinstellung erstellen]**.

   ![](../assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Vorgabe ein und wählen Sie dann den SMS-Kanal aus.

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Konfigurieren Sie die **SMS** -Einstellungen.

   ![](../assets/preset-sms.png)

   * Wählen Sie die **[!UICONTROL SMS-Typ]** wird mit der Vorgabe gesendet: **[!UICONTROL Transactional]** oder **[!UICONTROL Marketing]**.

   * Wählen Sie die **[!UICONTROL SMS-Konfiguration]** , um sie mit der Vorgabe zu verknüpfen.

      Weiterführende Informationen zur Konfiguration der Umgebung für den Versand von SMS-Nachrichten finden Sie im Abschnitt [diesem Abschnitt](sms-configuration.md).

   * Geben Sie die **[!UICONTROL Absendernummer]** &#x200B; Sie für Ihre Kommunikation verwenden möchten.

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Nachrichtenvoreinstellung auch als Entwurf speichern und ihre Konfiguration später fortsetzen.

   ![](../assets/sms_preset_2.png)

1. Nachdem die Nachrichtenvoreinstellung erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   >[!NOTE]
   >
   >In [diesem Abschnitt](#monitor-message-presets) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich abgeschlossen sind, erhält die Nachrichtenvoreinstellung den Status **[!UICONTROL Aktiv]**. Sie kann nun zum Versand von Nachrichten verwendet werden.

   ![](../assets/preset-active.png)

Informationen zum Konfigurieren einer Nachrichtenvorgabe für Push-Benachrichtigungen und E-Mails finden Sie unter [diesem Abschnitt](message-presets.md).

Jetzt können Sie mit Journey Optimizer SMS-Nachrichten senden.

**Verwandte Themen**

* [SMS erstellen](../create-sms.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
