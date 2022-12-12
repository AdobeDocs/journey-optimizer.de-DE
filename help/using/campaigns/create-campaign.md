---
solution: Journey Optimizer
product: journey optimizer
title: Kampagne erstellen
description: Erfahren Sie, wie Sie Kampagnen in erstellen [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# Kampagne erstellen {#create-campaign}

>[!NOTE]
>
>Bevor Sie eine neue Kampagne erstellen, stellen Sie sicher, dass Sie über einen Oberflächenkanal (d. h. eine Nachrichtenvorgabe) und ein Adobe Experience Platform-Segment verfügen, die einsatzbereit sind. Weitere Informationen finden Sie in den folgenden Abschnitten:
>
>* [Erstellen von Kanaloberflächen](../configuration/channel-surfaces.md)
>* [Erste Schritte mit Segmenten](../segment/about-segments.md)


## Erste Kampagne erstellen {#create}

1. Zugriff auf **[!UICONTROL Campaigns]** Menü und klicken Sie auf **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >Sie können auch eine vorhandene Live-Kampagne duplizieren, um eine neue zu erstellen. [Weitere Infos](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. Im **[!UICONTROL Properties]** Geben Sie an, wie die Kampagne ausgeführt werden soll:

   * **[!UICONTROL Scheduled]**
   * **[!UICONTROL API-triggered]**

   Weiterführende Informationen zum Kampagnentyp und zu den damit verbundenen Aktivitäten finden Sie in diesem Abschnitt [Abschnitt](#campaigntype).

1. Im **[!UICONTROL Actions]** wählen Sie den Kanal und die Kanaloberfläche aus, die zum Senden der Nachricht verwendet werden sollen, und klicken Sie dann auf **[!UICONTROL Create]**.

   Eine Oberfläche ist eine Konfiguration, die durch eine [Systemadministrator](../start/path/administrator.md). Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomäne, Mobile Apps usw. [Weitere Infos](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >In der Dropdown-Liste werden nur mit dem Marketingkampagnentyp kompatible Kanaloberflächen aufgelistet.

1. Geben Sie einen Titel und eine Beschreibung für die Kampagne an.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Um der Kampagne benutzerdefinierte oder Kerndatennutzungsbezeichnungen zuzuweisen, klicken Sie auf die Schaltfläche **[!UICONTROL Manage access]** Schaltfläche. [Weitere Informationen zur Zugriffskontrolle auf Objektebene (OLA)](../administration/object-based-access.md)

## Nachricht erstellen {#content}

Im **[!UICONTROL Actions]** erstellen Sie die Nachricht, die mit der Kampagne gesendet werden soll.

1. Klicken Sie auf **[!UICONTROL Edit content]** und erstellen Sie dann den Nachrichteninhalt.

   Hier erfahren Sie, wie Sie Ihren Nachrichteninhalt in den folgenden Seiten erstellen:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Lead" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>E-Mails erstellen</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Gelegentlich" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Push-Benachrichtigungen erstellen</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validierung" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>SMS-Nachrichten erstellen</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Sobald Ihr Inhalt definiert ist, verwenden Sie die **[!UICONTROL Simulate content]** -Schaltfläche, um Ihren Inhalt mit Testprofilen in der Vorschau anzuzeigen und zu testen. [Weitere Infos](../email/preview.md).

1. Klicken Sie auf den Pfeil, um zum Bildschirm zur Kampagnenerstellung zurückzukehren.

   ![](assets/create-campaign-design.png)

1. Im **[!UICONTROL Actions tracking]** Geben Sie an, ob Sie verfolgen möchten, wie Ihre Empfänger auf Ihren Versand reagieren: Sie können Klicks und/oder Öffnungen verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne über den Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report.md)

## Audience definieren {#audience}

1. Definieren Sie die Zielgruppe. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Select audience]** -Schaltfläche, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   >[!NOTE]
   >
   >Für API-gesteuerte Kampagnen muss die Zielgruppe über API-Aufruf festgelegt werden. [Weitere Infos](api-triggered-campaigns.md)

   Im **[!UICONTROL Identity namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Einzelpersonen, die zu einem Segment gehören, das nicht die ausgewählte Identität (den ausgewählten Namespace) unter ihren verschiedenen Identitäten hat, werden von der Kampagne nicht als Ziel ausgewählt.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Kampagnen planen {#schedule}

1. Um Ihre Kampagne an einem bestimmten Datum oder in regelmäßigen Abständen auszuführen, konfigurieren Sie die **[!UICONTROL Schedule]** Abschnitt. [Erfahren Sie, wie Sie Kampagnen planen](#schedule)

1. Um der Kampagne benutzerdefinierte oder Kerndatennutzungsbezeichnungen zuzuweisen, klicken Sie auf die Schaltfläche **[!UICONTROL Manage access]** Schaltfläche. [Weitere Informationen zur Zugriffskontrolle auf Objektebene (OLA)](../administration/object-based-access.md)

Sobald Ihre Kampagne fertig ist, können Sie sie überprüfen und veröffentlichen. [Weitere Infos](#review-activate)

## Kampagnentyp {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Kampagnentyp"
>abstract="Bei einer Marketing-Nachricht durch Angabe eines Versanddatums wird die **Geplant** type ist am besten geeignet. Wenn Sie jedoch Transaktionsnachrichten wie das Zurücksetzen des Kennworts oder den Abbruch der Karte senden möchten, wird die Variable **API-ausgelöst** type ist die beste Wahl."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Kampagnenkategorie"
>abstract="Der Kategoriewert ist direkt mit dem Kampagnentyp-Wert verknüpft. Kampagnentyp für die **Marketing** Kategorie und API-gesteuerter Typ für die Kategorie **Transactional**"

Es stehen zwei Kampagnentypen zur Verfügung:

* **[!UICONTROL Scheduled]**: die Kampagne sofort oder an einem bestimmten Datum ausführen. Geplante Kampagnen zielen auf den Versand ab **Marketing** Geben Sie Meldungen ein.

* **[!UICONTROL API-triggered]**: die Kampagne mithilfe eines API-Aufrufs ausführen. API-gesteuerte Kampagnen zielen auf das Senden von **transactional** Nachrichten, d. h. Nachrichten, die aufgrund einer von einer Person durchgeführten Aktion gesendet werden: Zurücksetzen des Kennworts, Abbruch der Karte usw. [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen.](api-triggered-campaigns.md)
