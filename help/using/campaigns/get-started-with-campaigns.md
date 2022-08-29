---
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen finden Sie in  [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: bbcafe364ca13501972b3d8e1150aa2f51ba88a0
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 19%

---

# Erste Schritte mit Kampagnen {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Kampagnen"
>abstract="Erstellen Sie Kampagnen, um einmalige Inhalte für ein bestimmtes Segment über verschiedene Kanäle hinweg bereitzustellen. Stellen Sie vor der Erstellung Ihrer Kampagne sicher, dass Sie über eine Kanaloberfläche (d. h. eine Nachrichtenvorgabe) und ein Adobe Experience Platform-Segment verfügen, die einsatzbereit sind."

Verwenden Sie Journey Optimizer-Kampagnen, um mithilfe verschiedener Kanäle einmalige Inhalte für ein bestimmtes Segment bereitzustellen. Bei Verwendung von Journey werden die Aktionen nacheinander ausgeführt. Bei Kampagnen werden Aktionen gleichzeitig, entweder sofort oder basierend auf einem festgelegten Zeitplan ausgeführt.

Erstellen Sie Kampagnen, um einfache Ad-hoc-Batch-Nachrichten für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen zu senden.

➡️ [Entdecken Sie diese Funktion im Video](#video).

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Vor Beginn {#campaign-prerequisites}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie mit der Erstellung Ihrer ersten Kampagne in Journey Optimizer beginnen:

1. **Sie benötigen entsprechende Berechtigungen**. Kampagnen stehen nur Benutzern mit Zugriff auf kampagnenbezogene **[!UICONTROL Produktprofil]** z. B. Campaign-Administrator, Campaign Genehmiger, Campaign Manager und/oder Campaign-Viewer.

   Wenn Sie nicht auf Kampagnen zugreifen können, müssen Ihre Berechtigungen erweitert werden. Wenn Sie Zugriff auf [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} für Ihre Organisation verwenden, führen Sie die folgenden Schritte aus. Wenden Sie sich andernfalls an Ihren Journey Optimizer-Administrator.

   +++Erfahren Sie, wie Sie Kampagnenberechtigungen zuweisen

   Zuweisen der entsprechenden **[!UICONTROL Produktprofil]** an Ihre Benutzer:

   1. Von [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, wählen Sie die [!DNL Adobe Experience Platform] Produkt.

   1. Navigieren Sie zum **[!UICONTROL Produktprofil]** -Tab eine der nativen Kampagnenkomponenten auswählen **[!UICONTROL Produktprofil]**: Kampagnenadministrator, Kampagnenvalidierer, Kampagnenmanager oder Kampagnen-Viewer.

      Weitere Informationen zur Journey Optimizer-Kampagne **[!UICONTROL Produktprofile]** und **[!UICONTROL Berechtigungen]**, [auf diese Seite verweisen](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Klicken **[!UICONTROL Benutzer hinzufügen]** , um Ihrem Benutzer die ausgewählte **[!UICONTROL Produktprofil]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Geben Sie den Namen, die Gruppe oder die E-Mail-Adresse Ihres Benutzers ein und klicken Sie auf **[!UICONTROL Speichern]**.
   Ihr Benutzer kann jetzt auf **[!UICONTROL Kampagnen]**.

+++

1. **Sie benötigen eine Zielgruppe**. Zielgruppensegmente müssen vor der Erstellung der Kampagne verfügbar sein. Erfahren Sie mehr über die Erstellung von Zielgruppen [auf dieser Seite](../segment/about-segments.md).
1. **Sie benötigen eine Kanaloberfläche**. Um einen Kanal auswählen zu können, muss die entsprechende Kanaloberfläche (d. h. Vorgabe) erstellt und verfügbar sein. Weitere Informationen zu Kanaloberflächen [auf dieser Seite](../configuration/channel-surfaces.md).

## Zugriff auf Kampagnen {#access}

Auf Kampagnen kann über das Menü **[!UICONTROL Kampagnen]** zugegriffen werden.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt. Um angehaltene, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

## Kampagnenstatus {#statuses}

Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Kampagne wird noch bearbeitet, sie wurde nicht aktiviert.
* **[!UICONTROL Wird aktiviert]**: Die Kampagne wird aktiviert.
* **[!UICONTROL Live]**: Die Kampagne wurde aktiviert.
* **[!UICONTROL Geplant]**: Die Kampagne ist so konfiguriert, dass sie an einem bestimmten Startdatum aktiviert wird.
* **[!UICONTROL Angehalten]**: Die Kampagne wurde manuell gestoppt. Sie können sie nicht mehr aktivieren oder wiederverwenden. [Weitere Informationen](modify-stop-campaign.md#stop)
* **[!UICONTROL Abgeschlossen]**: Die Kampagne ist abgeschlossen. Dieser Status wird automatisch 3 Tage nach der Aktivierung einer Kampagne zugewiesen oder am Enddatum der Kampagne, wenn sie eine wiederkehrende Ausführung aufweist.
* **[!UICONTROL Archiviert:]** Die Kampagne wurde archiviert.

>[!NOTE]
>
>Das Symbol &quot;Entwurfsversion öffnen&quot;neben einem **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** Der Status zeigt an, dass eine neue Version der Kampagne erstellt wurde und noch nicht aktiviert wurde. [Weitere Informationen](modify-stop-campaign.md#modify).

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Ihre erste Kampagne erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
