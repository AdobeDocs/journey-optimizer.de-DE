---
title: Konfiguration des Posteingangs
description: Konfiguration des Posteingangskanals
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 41%

---

# Konfigurieren des Posteingangs {#inbox-configuration}

Bevor Sie Inhaltskarten-Erlebnisse über den Posteingang bereitstellen können, müssen Sie eine **Posteingang**-Kanalkonfiguration in **[!UICONTROL Kanalkonfigurationen]** definieren. Diese Konfiguration verknüpft die Oberfläche mit dem Einverständnis, optionalen Zugriffsbeschriftungen und dem Ort, an dem das Erlebnis im Web oder in Ihrer iOS- oder Android-App angezeigt wird. Gehen Sie wie folgt vor, um eine Konfiguration zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** auf und klicken Sie dann auf **[!UICONTROL Kanalkonfiguration erstellen]**.

   ![](assets/inbox-configuration-1.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration an.

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Um der Konfiguration benutzerdefinierte oder grundlegende Datennutzungs-Labels zuzuweisen, können Sie **[!UICONTROL Zugriff verwalten]** auswählen. [Erfahren Sie mehr über die Zugriffssteuerung auf Objektebene (Object Level Access Control, OLAC)](../administration/object-based-access.md).

1. Wählen Sie **[!UICONTROL Posteingang]** Kanal aus.

   ![](assets/inbox-configuration-2.png)

1. Wählen Sie eine **[!UICONTROL Marketing-Aktion]** aus, um Einverständnisrichtlinien mit den Nachrichten zu verknüpfen, die diese Konfiguration verwenden. Es werden alle mit der Marketing-Aktion verknüpften Einverständnisrichtlinien genutzt, um die Präferenzen Ihrer Kundinnen und Kunden zu respektieren. [Weitere Informationen](../action/consent.md#surface-marketing-actions)

1. Wählen Sie die Plattform aus, auf die das Posteingangserlebnis angewendet werden soll.

   ![](assets/inbox-configuration-3.png)

1. Beim Web:

   * Geben **[!UICONTROL Seiten-URL]** die URL der Seite ein, auf der der Posteingang angezeigt werden soll, oder wählen Sie sie aus. Verwenden Sie diese Option, wenn das Erlebnis auf eine Seite beschränkt ist.

   * Definieren **[!UICONTROL unter „Standort auf]**&quot; die seiteninterne Platzierung, z. B. die Region oder Kennung, die Ihre Site für die Oberfläche des Posteingangs verwendet. [Weitere Informationen](../web/web-configuration.md)

     ![](assets/inbox-configuration-4.png)

1. Für iOS und Android:

   * Geben **[!UICONTROL unter „App]** ID“ die Kennung für Ihre App ein, damit die Konfiguration für den richtigen iOS- oder Android-Build gilt.

   * Geben **[!UICONTROL unter „Speicherort oder Pfad in der App]** den Bildschirm, die Route oder den Container an, in dem Benutzer den Posteingang öffnen sollen.

1. Senden Sie Ihre Änderungen ab.

Sie können jetzt beim Erstellen Ihres Posteingangs Ihre Konfiguration auswählen.

➡️ [Befolgen Sie die auf dieser Seite beschriebenen Schritte](inbox-create.md)
