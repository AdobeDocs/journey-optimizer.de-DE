---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des LINE-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von LINE-Nachrichten mit Journey Optimizer konfigurieren.
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
source-git-commit: bc734ed1249b1ec186eb5f479d605bafee8a1d06
workflow-type: ht
source-wordcount: '351'
ht-degree: 100%

---

# Konfigurieren eines LINE-Kanals in Journey Optimizer {#line-configuration}

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** auf und klicken Sie dann auf **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/line-config-1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration ein und wählen Sie dann den zu konfigurierenden Kanal aus.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Um der Konfiguration benutzerdefinierte oder grundlegende Datennutzungs-Labels zuzuweisen, können Sie **[!UICONTROL Zugriff verwalten]** auswählen. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen Sie den Kanal **LINE** aus.

   ![](assets/line-config-2.png)

1. Wählen Sie eine **[!UICONTROL Marketing-Aktion]** aus, um Einverständnisrichtlinien mit den Nachrichten zu verknüpfen, die diese Konfiguration verwenden. Es werden alle mit der Marketing-Aktion verknüpften Einverständnisrichtlinien genutzt, um die Präferenzen Ihrer Kundinnen und Kunden zu respektieren. [Weitere Informationen](../action/consent.md#surface-marketing-actions)

1. Wählen Sie den Nachrichtentyp für die Konfiguration aus:

   * **Marketing**: Für Werbenachrichten, z. B. für wöchentliche Werbeaktionen eines Einzelhandelsgeschäfts. Diese Nachrichten erfordern das Einverständnis der Benutzerin bzw. des Benutzers und sollten den LINE-Richtlinien zu Benutzer-Opt-ins entsprechen.
   * **Transaktion**: Für nicht kommerzielle Nachrichten, z. B. Bestellbestätigungen, Benachrichtigungen bei Passwortrücksetzungen oder Versand-Updates. Diese Nachrichten können auch an Benutzende gesendet werden, die sich von Marketing-Kommunikation abgemeldet haben, sind jedoch streng auf bestimmte Transaktionskontexte beschränkt.

1. Wählen Sie Ihre **[!UICONTROL Kanaleinstellungen]** aus.

   Wenden Sie sich an den Adobe-Support, um Ihre **[!UICONTROL Kanaleinstellungen]** einzurichten.

   ![](assets/line-config-2.png)

1. Wählen Sie Ihre **[!UICONTROL LINE-Benutzer-ID]** aus, die zugeordnet werden soll. Dies ist die Kennung, über die Nachrichten mit einzelnen Benutzenden in Ihrem LINE-Kanal verknüpft werden.

1. Geben Sie Ihren **[!UICONTROL Absendernamen]** ein, z. B. den Namen Ihrer Marke.

1. Senden Sie Ihre Änderungen ab.

Sie können Ihre Konfiguration nun beim Erstellen Ihrer LINE-Nachricht auswählen.

## Konfigurieren der LINE-Kanal-Einstellungs-API {#line-api}

Diese API richtet Kanaleinstellungen ein, die die erforderlichen Autorisierungs- und Konfigurationsdetails für die Verbindung mit der LINE-Messaging-API speichern. Diese Einstellungen ermöglichen es Adobe Journey Optimizer, sich zu authentifizieren und Nachrichten über LINE mit den bereitgestellten Anmeldeinformationen zu senden.

**Endpunkt**

```
POST https://platform.adobe.io/journey/imp/config/channel-settings
```

| Header-Name | Beschreibung |
|-|-|
| Autorisierung | Benutzer-Token Ihres technischen Kontos |
| x-api-key | Client-ID aus der Adobe Developer Console |
| x-gw-ims-org-id | Die ID Ihrer IMS-Organisation |
| x-sandbox-name | Sandbox-Name, z. B. prod |
| Content-Type | Muss „application“/„json“ sein |


**Anfrageinhalt**

```json
{
    "name": "your_defined_name",
    "channelRegistryId": "line",
    "channel": "line",
    "channelSettings": {
        "channelId": "your_line_channel_id",
        "channelSecret": "your_line_channel_secret"
    }
}
```

**Antwort auf Kanaleinstellungen**

```json
{
"id": "3603ed66-ae86-42b8-8a90-d4b4e54e7c3b",
"name": "your_defined_name",
"channelRegistryId": "line",
"channel": "line",
"channelSettings": {
    "channelId": "your_line_channel_id",
    "channelSecret": "your_line_channel_secret"
    },
    "channelPublicationId": "v1_line",
    "createdAt": "2025-07-30T12:00:00.000Z",
    "modifiedAt": "2025-07-30T12:00:00.000Z",
    "isFromLatestVersion": true,
    "_etag": "\"eab98d24-18af-48ae-90f9-e59d4f8cfb2b\""
}
```
