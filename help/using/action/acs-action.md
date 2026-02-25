---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren mit Adobe Campaign Standard
description: Durchführen der Integration von Journey Optimizer mit Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: Kampagne, Standard, Integration, Begrenzung, Aktion
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 100%

---

# Integrieren mit Adobe Campaign Standard {#using_adobe_campaign_standard}

Wenn Sie über Adobe Campaign Standard verfügen, haben Sie Zugriff auf eine integrierte Aktion, die die Verbindung zu Adobe Campaign Standard ermöglicht. Mit der Transaktionsnachrichten-Funktion von Adobe Campaign Standard können Sie E-Mails, Push-Benachrichtigungen und SMS senden.

Die Transaktionsnachricht in Campaign Standard und das zugehörige Ereignis müssen veröffentlicht werden, damit sie in Journey Optimizer verwendet werden können. Wenn das Ereignis veröffentlicht wird, die Nachricht jedoch nicht, wird sie nicht in der Benutzeroberfläche von Journey Optimizer angezeigt. Wenn die Nachricht veröffentlicht wird, das zugehörige Ereignis jedoch nicht, wird sie in der Benutzeroberfläche von Journey Optimizer angezeigt, sie kann jedoch nicht verwendet werden.

## Leitlinien und Einschränkungen {#important-notes}

* Für Adobe Campaign Standard-Aktionen ist automatisch eine Begrenzungsregel von 4.000 Aufrufen pro 5 Minuten definiert. Lesen Sie mehr über Service-Level-Vereinbarungen für Transaktionsnachrichten in der [Produktbeschreibung von Adobe Campaign Standard](https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html){target="_blank"}.

* Die Adobe Campaign Standard-Integration wird über eine dedizierte integrierte Aktion in der Aktionsliste eingerichtet. Dies muss für jede Sandbox konfiguriert werden.

* Sie können eine Campaign Standard-Aktion nicht mit den Aktivitäten „Zielgruppen-Qualifizierung“ oder „Zielgruppe lesen“ verwenden.

* Eine Journey kann nicht sowohl [integrierte Kanalaktionen](../building-journeys/journey-action.md) als auch [Campaign Standard-Aktionen](../building-journeys/using-adobe-campaign-standard.md) verwenden.

## Konfigurieren der Aktion {#configure-action}

In Journey Optimizer muss eine Aktion pro Transaktionsnachricht konfiguriert werden.

Gehen Sie wie folgt vor, um Campaign Standard-Aktion zu konfigurieren:

1. Wählen SIe **[!UICONTROL Konfigurationen]** im Menüabschnitt ADMINISTRATION aus. 

1. Klicken Sie im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Verwalten]**. Die Liste der Aktionen wird angezeigt.

1. Wählen Sie die integrierte **[!UICONTROL AdobeCampaignStandard]**-Aktion aus. Der Bereich für die Aktionskonfiguration wird auf der rechten Seite des Bildschirms geöffnet.

   ![](assets/actioncampaign.png)

1. Kopieren Sie die URL der Adobe Campaign Standard-Instanz und fügen Sie sie in das Feld **[!UICONTROL URL]** ein.

1. Klicken Sie auf **[!UICONTROL Instanz-URL testen]**, um die Gültigkeit der Instanz zu testen.

   >[!NOTE]
   >
   >Dieser Test bestätigt Folgendes:
   >
   >* Der Host ist „.campaign.adobe.com“, „.campaign-sandbox.adobe.com“, „.campaign-demo.adobe.com“, „.ats.adobe.com“ oder „.adls.adobe.com“.
   >
   >* Die URL beginnt mit „https“
   >
   >* Die mit dieser Adobe Campaign Standard-Instanz verknüpfte Organisation ist identisch mit der Journey Optimizer-Organisation

Sobald diese Konfiguration abgeschlossen ist, stehen in der Kategorie **[!UICONTROL Aktion]** beim Erstellen einer Journey drei Aktionen zur Verfügung: **[!UICONTROL E-Mail]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]**. [Erfahren Sie mehr über die Verwendung](../building-journeys/using-adobe-campaign-standard.md).

![](assets/journey58.png)

Das Ereignis **Reaktionen** wird verwendet, um auf Tracking-Daten zu reagieren, die sich auf eine Campaign Standard-Nachricht beziehen, die innerhalb derselben Journey gesendet wurde:

* Bei Push-Benachrichtigungen können Journeys auf angeklickte, gesendete oder fehlgeschlagene Nachrichten reagieren. 

* Bei SMS-Nachrichten können Journeys auf gesendete oder fehlgeschlagene Nachrichten reagieren. 

* Bei E-Mails können Journeys auf angeklickte, gesendete, geöffnete oder fehlgeschlagene Nachrichten reagieren. [Erfahren Sie mehr zu Reaktionsereignissen](../building-journeys/reaction-events.md).

Wenn zum Senden von Nachrichten ein Drittanbietersystem verwendet wird, muss eine benutzerdefinierte Aktion hinzugefügt und konfiguriert werden. [Erfahren Sie mehr zur Konfiguration benutzerdefinierter Aktionen](../action/about-custom-action-configuration.md).