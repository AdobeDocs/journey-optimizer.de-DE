---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen finden Sie in  [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0433e312db84ee16a076c183a82345de372c6ae7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# Erste Schritte mit Kampagnen {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Kampagnen"
>abstract="Erstellen Sie Kampagnen, um einmalige Inhalte für ein bestimmtes Segment über verschiedene Kanäle hinweg bereitzustellen. Bevor Sie eine neue Kampagne erstellen, stellen Sie sicher, dass Sie über eine Kanaloberfläche (d. h. Nachrichtenvoreinstellung) und ein Adobe Experience Platform-Segment verfügen, die einsatzbereit sind."

Verwenden Sie Journey Optimizer-Kampagnen, um mithilfe verschiedener Kanäle einmalige Inhalte für ein bestimmtes Segment bereitzustellen. Bei Verwendung von Journeys werden die Aktionen nacheinander ausgeführt. Bei Kampagnen werden die Aktionen gleichzeitig ausgeführt, entweder sofort oder nach einem bestimmten Zeitplan.

Sie können zwei Arten von Kampagnen erstellen:

* **Geplante Kampagnen** ermöglichen einfache, im Batch versendete Ad-hoc-Nachrichten für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen.
* **API-ausgelöste Kampagnen** ermöglichen über REST-APIs einfache Transaktions- und operative Nachrichten (Kennwortzurücksetzung, Kartenkündigung usw.), bei denen die Notwendigkeit einer Personalisierung mit Profilattributen und Kontextdaten aus der Payload bestehen kann.

Die wichtigsten Schritte zum Erstellen einer Kampagne sind wie folgt:

![](assets/create-campaign-process.png)

➡️ [Entdecken Sie diese Funktion im Video](#video)

## Vor Beginn {#campaign-prerequisites}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie mit der Erstellung Ihrer ersten Kampagne in Journey Optimizer beginnen:

1. **Sie benötigen entsprechende Berechtigungen**. Diese Funktion steht nur Benutzenden mit Zugriff auf ein kampagnenbezogenes **[!UICONTROL Produktprofil]** zur Verfügung, beispielsweise Kampagnen-Admins, Kampagnen-Genehmigende, Kampagnen-Manager und/oder Kampagnen-Betrachtende.

   Wenn Sie nicht auf Kampagnen zugreifen können, müssen Ihre Berechtigungen erweitert werden. Wenn Sie für Ihre Organisation Zugriff auf die [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} haben, führen Sie die folgenden Schritte aus. Wenden Sie sich andernfalls an Ihren Journey Optimizer-Admin.

   +++Erfahren Sie, wie Sie Kampagnenberechtigungen zuweisen

   So weisen Sie Ihren Benutzenden die entsprechenden **[!UICONTROL Produktprofile]** zu:

   1. Wählen Sie in der [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} das [!DNL Adobe Experience Platform]-Produkt aus.

   1. Wechseln Sie zur Registerkarte **[!UICONTROL Produktprofil]** und wählen Sie eines der integrierten kampagnenbezogenen **[!UICONTROL Produktprofile]**: Kampagnen-Admin, Kampagnen-Genehmigende, Kampagnen-Manager oder Kampagnen-Betrachtende.

      Weitere Informationen zu kampagnenbezogenen **[!UICONTROL Produktprofilen]** und **[!UICONTROL Berechtigungen]** in Journey Optimizer [finden Sie auf dieser Seite](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Klicken Sie auf **[!UICONTROL Benutzer hinzufügen]**, um Ihrem Benutzenden das ausgewählte **[!UICONTROL Produktprofil]** zuzuweisen.

      ![](assets/do-not-localize/admin_2.png)

   1. Geben Sie den Namen, die Gruppe oder die E-Mail-Adresse der Benutzenden ein und klicken Sie auf **[!UICONTROL Speichern]**.
   Ihre Benutzenden können jetzt auf **[!UICONTROL Kampagnen]** zugreifen.

+++

1. **Sie benötigen eine Audience**. Audience-Segmente müssen vor der Erstellung der Kampagne verfügbar sein. Weitere Informationen zum Erstellen von Audience finden Sie [auf dieser Seite](../segment/about-segments.md).
1. **Sie benötigen eine Kanaloberfläche**. Um einen Kanal auswählen zu können, muss die entsprechende Kanaloberfläche (d. h. Voreinstellung) erstellt und verfügbar sein. Weitere Informationen zu Kanaloberflächen finden Sie [auf dieser Seite](../configuration/channel-surfaces.md).

## Zugriff auf Kampagnen {#access}

Auf Kampagnen kann über das Menü **[!UICONTROL Kampagnen]** zugegriffen werden.

Standardmäßig werden in der Liste alle Kampagnen mit dem Status **[!UICONTROL Entwurf]**, **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** angezeigt.

Um gestoppte, abgeschlossene und archivierte Kampagnen anzuzeigen, müssen Sie den Filter löschen.

![](assets/create-campaign-list.png)

## Kampagnenstatus {#statuses}

Kampagnen können mehrere Status aufweisen:

* **[!UICONTROL Entwurf]**: Die Kampagne wird noch bearbeitet, sie wurde nicht aktiviert.
* **[!UICONTROL Wird aktiviert]**: Die Kampagne wird aktiviert.
* **[!UICONTROL Live]**: Die Kampagne wurde aktiviert.
* **[!UICONTROL Geplant]**: Die Kampagne wurde so konfiguriert, dass sie an einem bestimmten Startdatum aktiviert wird.
* **[!UICONTROL Gestoppt]**: Die Kampagne wurde manuell gestoppt. Sie können sie nicht mehr aktivieren oder wiederverwenden. [Informationen zum Stoppen einer Kampagne](modify-stop-campaign.md#stop)
* **[!UICONTROL Abgeschlossen]**: Die Kampagne ist abgeschlossen. Dieser Status wird automatisch 3 Tage nach der Aktivierung einer Kampagne zugewiesen oder am Enddatum der Kampagne, wenn sie eine wiederkehrende Ausführung aufweist.
* **[!UICONTROL Archiviert]**: Die Kampagne wurde archiviert. [Informationen zum Archivieren von Kampagnen](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Das Symbol „Entwurfsversion öffnen“ neben einem Status **[!UICONTROL Live]** oder **[!UICONTROL Geplant]** zeigt an, dass eine neue Version der Kampagne erstellt wurde und noch nicht aktiviert wurde. [Weitere Informationen](modify-stop-campaign.md#modify).

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Ihre erste Kampagne erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
