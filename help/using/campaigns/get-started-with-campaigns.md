---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen finden Sie in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Erste Schritte mit Kampagnen {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Kampagnen"
>abstract="Erstellen Sie Kampagnen, um einmalige Inhalte für ein bestimmtes Segment über verschiedene Kanäle hinweg bereitzustellen. Bevor Sie Ihre Kampagne erstellen, stellen Sie sicher, dass Sie über eine Kanaloberfläche (d. h. eine Nachrichtenvorgabe) und ein Adobe Experience Platform-Segment verfügen, die einsatzbereit sind."

Verwenden Sie Journey Optimizer-Kampagnen, um einmalige Inhalte mithilfe verschiedener Kanäle für ein bestimmtes Segment bereitzustellen. Bei der Verwendung von Journeys werden Aktionen nacheinander ausgeführt. Bei Kampagnen werden Aktionen gleichzeitig, entweder sofort oder basierend auf einem festgelegten Zeitplan ausgeführt.

Sie können zwei Kampagnentypen erstellen:

* **Geplante Kampagnen** ermöglichen einfache Ad-hoc-Batch-Nachrichten für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen.
* **API-ausgelöste Kampagnen** ermöglichen einfache Transaktions-/Betriebsnachrichten mit REST-APIs (Kennwortzurücksetzung, Kartenabbruch usw.), bei denen die Notwendigkeit einer Personalisierung mit Profilattributen und Kontextdaten aus der Payload bestehen kann.

Die wichtigsten Schritte zum Erstellen einer Kampagne sind:

![](assets/create-campaign-process.png)

➡️ [Funktion im Video kennenlernen](#video)

## Vorbereitung {#campaign-prerequisites}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie mit der Erstellung Ihrer ersten Kampagne in Journey Optimizer beginnen:

1. **Sie benötigen entsprechende Berechtigungen**. Kampagnen stehen nur Benutzern mit Zugriff auf kampagnenbezogene **[!UICONTROL Product profile]** z. B. Campaign-Administrator, Campaign Genehmiger, Campaign Manager und/oder Campaign-Viewer.

   Wenn Sie nicht auf Kampagnen zugreifen können, müssen Ihre Berechtigungen erweitert werden. Wenn Sie Zugriff auf [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} für Ihre Organisation verwenden, führen Sie die folgenden Schritte aus. Wenn nicht, wenden Sie sich an Ihren Journey Optimizer-Administrator.

   +++Erfahren Sie, wie Sie Kampagnenberechtigungen zuweisen

   Zuweisen der entsprechenden **[!UICONTROL Product profile]** an Ihre Benutzer:

   1. Von [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, wählen Sie die [!DNL Adobe Experience Platform] Produkt.

   1. Navigieren Sie zum **[!UICONTROL Product profile]** -Tab eine der nativen Kampagnenkomponenten auswählen **[!UICONTROL Product profile]**: Kampagnenadministrator, Kampagnenvalidierer, Kampagnenmanager oder Kampagnen-Viewer.

      Weitere Informationen zur Journey Optimizer-Kampagne **[!UICONTROL Product profiles]** und **[!UICONTROL Permissions]**, [auf diese Seite verweisen](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Klicken **[!UICONTROL Add user]** , um Ihrem Benutzer die ausgewählte **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Geben Sie den Namen, die Gruppe oder die E-Mail-Adresse Ihres Benutzers ein und klicken Sie auf **[!UICONTROL Save]**.
   Ihr Benutzer kann jetzt auf **[!UICONTROL Campaigns]**.

+++

1. **Sie benötigen eine Zielgruppe**. Zielgruppensegmente müssen vor der Erstellung der Kampagne verfügbar sein. Erfahren Sie mehr über die Erstellung von Zielgruppen [auf dieser Seite](../segment/about-segments.md).
1. **Sie benötigen eine Kanaloberfläche**. Um einen Kanal auswählen zu können, muss die entsprechende Kanaloberfläche (d. h. Vorgabe) erstellt und verfügbar sein. Weitere Informationen zu Kanaloberflächen [auf dieser Seite](../configuration/channel-surfaces.md).

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Ihre erste Kampagne erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
