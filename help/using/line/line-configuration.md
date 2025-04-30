---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren des LINE-Kanals
description: Erfahren Sie, wie Sie Ihre Umgebung für das Senden von LINE-Nachrichten mit Journey Optimizer konfigurieren
feature: Line, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 8714ac6b2fd76ec859c358535fa322f0ac333a82
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 42%

---

# Konfigurieren des LINE-Kanals in Journey Optimizer {#line-configuration}

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** auf und klicken Sie dann auf **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/line-config-1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration ein und wählen Sie dann den zu konfigurierenden Kanal aus.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Um der Konfiguration benutzerdefinierte oder grundlegende Datennutzungskennzeichnungen zuzuweisen, können Sie **[!UICONTROL Zugriff verwalten]** auswählen. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLAC)](../administration/object-based-access.md).

1. Wählen Sie **LINE**-Kanal aus.

   ![](assets/line-config-2.png)

1. Wählen Sie eine **[!UICONTROL Marketing-Aktion]** aus, um Einverständnisrichtlinien mit den Nachrichten zu verknüpfen, die diese Konfiguration verwenden. Es werden alle mit dieser Marketing-Aktion verknüpften Einverständnisrichtlinien genutzt, um die Voreinstellungen Ihrer Kundinnen und Kunden zu respektieren. [Weitere Informationen](../action/consent.md#surface-marketing-actions)

1. Wählen Sie den Nachrichtentyp für die Konfiguration aus:

   * **Marketing**: Für Werbenachrichten, z. B. für wöchentliche Werbeaktionen eines Einzelhandelsgeschäfts. Diese Nachrichten erfordern das Einverständnis des Benutzers und sollten den Richtlinien von LINE bezüglich Benutzer-Opt-ins entsprechen.
   * **Transaktion**: Für nicht-kommerzielle Nachrichten, wie Bestellbestätigungen, Benachrichtigungen beim Zurücksetzen des Kennworts oder Versandaktualisierungen. Diese Nachrichten können auch an Benutzer gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben, sind jedoch streng auf bestimmte Transaktionskontexte beschränkt.

1. Wählen Sie Ihre **[!UICONTROL Kanaleinstellungen]** aus.

   Wenden Sie sich an den Adobe-Support, um Ihre **[!UICONTROL Kanaleinstellungen]** einzurichten.

   ![](assets/line-config-2.png)

1. Wählen Sie Ihre **[!UICONTROL LINE-Benutzer]** ID aus, die Sie zuordnen möchten. Dies ist die Kennung, die verwendet wird, um Nachrichten mit einzelnen Benutzern in Ihrem LINE-Kanal zu verknüpfen.

1. Geben Sie Ihren **[!UICONTROL Absendernamen]** ein, z. B. den Namen Ihrer Marke.

1. Senden Sie Ihre Änderungen ab.

Jetzt können Sie beim Erstellen Ihrer LINE-Nachricht Ihre Konfiguration auswählen.
