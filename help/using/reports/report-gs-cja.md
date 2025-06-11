---
solution: Journey Optimizer
product: journey optimizer
title: Neues Reporting-Erlebnis
description: Erste Schritte mit dem Bericht für die gesamte Zeit
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 66%

---

# Erste Schritte mit dem Bericht für die gesamte Zeit {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Aktivieren von Customer Journey Analytics"
>abstract="Um diesen Bericht in Customer Journey Analytics zu analysieren, wenden Sie sich an Ihre oder Ihren Admin, um sicherzustellen, dass Ihre Organisation Customer Journey Analytics erworben hat und die Integration ordnungsgemäß konfiguriert ist."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

Journey Optimizer Reporting verfügt über eine verbesserte Kompatibilität mit Customer Journey Analytics-Funktionen, wodurch die Berichterstellung plattformübergreifend standardisiert und die Datenkonsistenz und -zuverlässigkeit verbessert wird. Diese nahtlose Integration zwischen Journey Optimizer und Customer Journey Analytics bietet einen klareren Überblick über Leistungsmetriken und ermöglicht es Benutzenden, fundiertere Entscheidungen zu treffen.

Der Zugriff auf diese Reporting-Funktionen hängt vom Kontext und den Produktbereichen ab:

* **Journey** - Wenn Sie eine Journey oder Sendungen im Kontext einer Journey auswählen möchten, rufen Sie über das Menü **[!UICONTROL Journey]** Ihre Journey auf und klicken Sie auf die Schaltfläche **[!UICONTROL Bericht anzeigen]**.

  In der Liste der vorhandenen Journeys können Sie auch **[!UICONTROL Bericht]** über das erweiterte Menü Ihrer ausgewählten Journey auswählen. [Weitere Informationen zum Journey-Bericht](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Kampagnen** - Wenn Sie eine Kampagne als Ziel wählen möchten, rufen Sie im Menü **[!UICONTROL Kampagnen]** Ihre Kampagne auf und klicken Sie auf die Schaltfläche **[!UICONTROL Berichte]** und dann auf **[!UICONTROL Alle Zeitberichte anzeigen]**.

  In der Liste der vorhandenen Kampagnen können Sie auch **[!UICONTROL Bericht]** über das erweiterte Menü Ihrer ausgewählten Kampagne auswählen. [Weitere Informationen zum Kampagnen-Bericht](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Global** - Wenn Sie Metriken für alle Kampagnen und Journey in Ihrer Umgebung auswählen möchten, greifen Sie auf den Bericht **Übersicht** zu, indem Sie im Abschnitt **[!UICONTROL Journey-Management]** zum Menü **[!UICONTROL Berichte]**. [Weitere Informationen zum Übersichtsbericht](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>Das Reporting in Adobe Journey Optimizer ist derzeit standardmäßig auf UTC eingestellt. Die Möglichkeit, die Zeitzone für das Reporting anzupassen, wird in einer zukünftigen Version eingeführt.

## Voraussetzungen {#prerequisites}

* Wenn Sie **nicht** im Besitz von Customer Journey Analytics sind oder wenn Sie es besitzen, aber **keinen** Zugriff auf Customer Journey Analytics-Produktprofile haben, werden die Berechtigungen in Journey Optimizer verwaltet. In diesem Fall benötigen Sie die Berechtigung **[!UICONTROL Kanalberichte anzeigen]** oder zugehörige Rollen. [Weitere Informationen](../administration/permissions.md)

* Customer Journey Analytics Wenn Sie **besitzen** und Zugriff auf ein Customer Journey Analytics-Produktprofil haben, benötigen Sie Folgendes:

   * Die Berechtigungen **[!UICONTROL Zielgruppen erstellen]** und **[!UICONTROL Zielgruppe anzeigen]** für Customer Journey Analytics. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * Die Berechtigung **[!UICONTROL Profile verwalten]** für Adobe Journey Optimizer. [Weitere Informationen](../administration/permissions.md)

* Ihre Datenansichten in Customer Journey Analytics müssen mit der folgenden Einstellung konfiguriert werden: **Als Standard-Datenansicht in Adobe Journey Optimizer festlegen**. [Weitere Informationen zu Datenansichten](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Alle Zeitberichte pro Kanal

Globale Zeitberichte stehen für alle Kanäle zur Verfügung. Wählen Sie den Bericht für den Kanal aus, für den Sie weitere Details benötigen.

### Ausgehende Kanäle

Wählen Sie einen ausgehenden Kanal aus, um zugehörige **globale Echtzeitberichte** zu ermitteln.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="E-Mail" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>E-Mail-Kanal</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>SMS-Kanal</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="Push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>Push-Kanal</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="Direkt-Mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>Direkt-Mail-Kanal</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>Journey-Bericht</strong></a></p></div></td>
</tr></table>

### Eingehende Erlebnisse

Wählen Sie ein eingehendes Erlebnis aus, um zugehörige **globale Echtzeitberichte“ zu**.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="In-App" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>In-App-Kanal</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><p><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>Web-Kanal</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><img alt="Code-basiertes Erlebnis" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>Code-basierte Erlebnisse</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>Kampagnenbericht</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>Journey-Bericht</strong></a></p></div></td>
<td><img alt="Inhaltskarten" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>Inhaltskarten</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>Kampagnenbericht</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>Journey-Bericht</strong></a></p></div></td>
</tr></table>

## Anleitungsvideo{#video}

Das folgende Video zeigt Ihnen, wie Sie das erweiterte Reporting in Journey Optimizer mit Customer Journey Analytics verwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3443160?captions=ger)