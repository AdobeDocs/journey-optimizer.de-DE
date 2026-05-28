---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des LINE-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von LINE-Nachrichten mit Journey Optimizer konfigurieren.
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
TQID: https://experienceleague.adobe.com/yDRCVzfdPGXisgxJ59UT8HYsdXI82H07Ol--YP7wmE0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e09fc1e6-407c-418f-adc5-e2ffe8b8986eid: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 365
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
| Inhaltstyp | Muss „application“/„json“ sein |


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
