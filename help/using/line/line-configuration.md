---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des LINE-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von LINE-Nachrichten mit Journey Optimizer konfigurieren.
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
source-git-commit: d11d389259057b20c3803643ca40266b9cb4302c
workflow-type: ht
source-wordcount: '269'
ht-degree: 100%

---

# Konfigurieren eines LINE-Kanals in Journey Optimizer {#line-configuration}

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** auf und klicken Sie dann auf **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/line-config-1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration ein und wählen Sie dann den zu konfigurierenden Kanal aus.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Um der Konfiguration benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, können Sie **[!UICONTROL Zugriff verwalten]** auswählen. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

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
