---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Kampagnen
description: Weitere Informationen zu Kampagnen in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: Kampagne, Vorgehensweise, Starten, Optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 84%

---

# Erste Schritte mit Kampagnen {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Kampagnen"
>abstract="Erstellen Sie Kampagnen, um einmalige Inhalte für eine bestimmte Zielgruppe über verschiedene Kanäle hinweg bereitzustellen. Bevor Sie Ihre Kampagne erstellen, stellen Sie sicher, dass Sie über eine Kanaloberfläche (d. h. eine Nachrichtenvorgabe) und eine Adobe Experience Platform-Zielgruppe verfügen."

Verwenden Sie Journey Optimizer-Kampagnen, um mithilfe verschiedener Kanäle einmalige Inhalte für eine bestimmte Zielgruppe bereitzustellen. Bei Verwendung von Journeys werden die Aktionen nacheinander ausgeführt. Bei Kampagnen werden die Aktionen gleichzeitig ausgeführt, entweder sofort oder nach einem bestimmten Zeitplan.

Sie können zwei Arten von Kampagnen erstellen:

* **Geplante Kampagnen** ermöglichen einfache, im Batch versendete Ad-hoc-Nachrichten für Marketing-Anwendungsfälle wie Werbeangebote, Interaktionskampagnen, Ankündigungen, rechtliche Hinweise oder Richtlinienaktualisierungen.
* **API-ausgelöste Kampagnen** ermöglichen es, dass Marketing-Nachrichten eine Zielgruppe zum richtigen Zeitpunkt ansprechen oder dass Transaktions-/Betriebsnachrichten an einen Kontakt gerichtet werden, z. B. zum Zurücksetzen des Kennworts. Dabei kann eine Personalisierung erforderlich sein, indem nicht nur das Profilattribut, sondern auch die Echtzeit-Kontextdaten im Trigger verwendet werden, der eine REST-API-Payload ist.

Die wichtigsten Schritte zum Erstellen einer Kampagne sind wie folgt:

![](assets/create-campaign-process.png)

➡️ [Entdecken Sie diese Funktion im Video](#video)

## Vor Beginn {#campaign-prerequisites}

Überprüfen Sie die folgenden Voraussetzungen, bevor Sie mit der Erstellung Ihrer ersten Kampagne in Journey Optimizer beginnen:

1. **Sie benötigen entsprechende Berechtigungen**. Diese Funktion steht nur Benutzenden mit Zugriff auf ein kampagnenbezogenes **[!UICONTROL Produktprofil]** zur Verfügung, beispielsweise Kampagnen-Admins, Kampagnen-Genehmigende, Kampagnen-Manager und/oder Kampagnen-Betrachtende.

   Wenn Sie nicht auf Kampagnen zugreifen können, müssen Ihre Berechtigungen erweitert werden. Wenn Sie für Ihre Organisation Zugriff auf die [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} haben, führen Sie die folgenden Schritte aus. Wenden Sie sich andernfalls an Ihren Journey Optimizer-Admin.

   +++Erfahren Sie, wie Sie Kampagnenberechtigungen zuweisen

   So weisen Sie Ihren Benutzenden die entsprechenden **[!UICONTROL Produktprofile]** zu:

   1. Wählen Sie in der [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} das [!DNL Adobe Experience Platform]-Produkt aus.

   1. Wechseln Sie zur Registerkarte **[!UICONTROL Produktprofil]** und wählen Sie eines der integrierten kampagnenbezogenen **[!UICONTROL Produktprofile]**: Kampagnen-Admin, Kampagnen-Genehmigende, Kampagnen-Manager oder Kampagnen-Betrachtende.

      Weitere Informationen zu kampagnenbezogenen **[!UICONTROL Produktprofilen]** und **[!UICONTROL Berechtigungen]** in Journey Optimizer [finden Sie auf dieser Seite](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Klicken Sie auf **[!UICONTROL Benutzer hinzufügen]**, um Ihrem Benutzenden das ausgewählte **[!UICONTROL Produktprofil]** zuzuweisen.

      ![](assets/do-not-localize/admin_2.png)

   1. Geben Sie den Namen, die Gruppe oder die E-Mail-Adresse der Benutzenden ein und klicken Sie auf **[!UICONTROL Speichern]**.

   Ihre Benutzenden können jetzt auf **[!UICONTROL Kampagnen]** zugreifen.

+++

1. **Sie benötigen eine Audience**. Zielgruppen müssen vor der Erstellung der Kampagne verfügbar sein. Weitere Informationen zu Zielgruppen [auf dieser Seite](../audience/about-audiences.md).
1. **Sie benötigen eine Kanaloberfläche**. Um einen Kanal auswählen zu können, muss die entsprechende Kanaloberfläche (d. h. Voreinstellung) erstellt und verfügbar sein. Weitere Informationen zu Kanaloberflächen finden Sie [auf dieser Seite](../configuration/channel-surfaces.md).

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie Ihre erste Kampagne erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
