---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren der API-ausgelösten Kampagnenaktion
description: Erfahren Sie, wie Sie die API-ausgelöste Kampagnenaktion konfigurieren.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: Kampagnen, API-ausgelöst, REST, Optimizer, Nachrichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 26%

---


# Konfigurieren der API-ausgelösten Kampagnenaktion {#api-action}

Verwenden Sie die Registerkarte **[!UICONTROL Aktionen]**, um eine Kanalkonfiguration für Ihre Nachricht auszuwählen und zusätzliche Einstellungen wie Tracking, Inhaltsexperiment oder mehrsprachige Inhalte zu konfigurieren.

1. **Kanal auswählen**.

   Navigieren Sie zur Registerkarte **[!UICONTROL Aktionen]**, klicken Sie auf die Schaltfläche **[!UICONTROL Aktion hinzufügen]** und wählen Sie den Kommunikationskanal aus.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >Die verfügbaren Kanäle variieren je nach Ihrem Lizenzmodell und Ihren Add-ons.
   >
   >Für API-ausgelöste Kampagnen sind nur die Kanäle E-Mail, SMS und Push-Benachrichtigungen verfügbar.

1. **Wählen Sie eine Kanalkonfiguration**

   Eine Konfiguration wird durch [Systemadmins](../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Erfahren Sie, wie Sie Kanalkonfigurationen einrichten](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Erstellen eines Inhaltsexperiments**

   Im Abschnitt **[!UICONTROL Inhaltsexperiment]** können Sie mehrere Versandmethoden definieren, um zu messen, welche für Ihre Zielgruppe am besten geeignet ist. Klicken Sie auf **[!UICONTROL Experiment erstellen]** und führen Sie dann die in diesem Abschnitt beschriebenen Schritte aus: [Erstellen eines Inhaltsexperiments](../content-management/content-experiment.md).

1. **Mehrsprachige Inhalte hinzufügen**

   Verwenden Sie den **[!UICONTROL Languages]**, um in Ihrer Kampagne Inhalte in mehreren Sprachen zu erstellen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die gewünschten **[!UICONTROL Spracheinstellungen]** aus. Detaillierte Informationen zum Einrichten und Verwenden mehrsprachiger Funktionen finden Sie in diesem Abschnitt: [Erste Schritte mit mehrsprachigen Inhalten](../content-management/multilingual-gs.md)

Je nach ausgewähltem Kommunikationskanal stehen zusätzliche Einstellungen zur Verfügung. Erweitern Sie die folgenden Abschnitte, um weitere Informationen zu erhalten.

+++**Begrenzungsregeln anwenden** (E-Mail, Push, SMS)

Wählen **[!UICONTROL in der Dropdown]** Liste „Geschäftsregeln“ einen Regelsatz aus, um Begrenzungsregeln auf Ihre Kampagne anzuwenden. Mithilfe von Kanalregelsätzen können Sie die Frequenzbegrenzung nach Kommunikationstyp festlegen, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überlastet werden. [Informationen zum Arbeiten mit Regelsätzen](../conflict-prioritization/rule-sets.md)

+++

+++**Interaktion verfolgen** (E-Mail, SMS).

Verwenden Sie den Abschnitt **[!UICONTROL Aktions-Tracking]**, um zu verfolgen, wie Ihre Empfängerinnen und Empfänger auf Ihre E-Mail- oder SMS-Sendungen reagieren. Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

+++

+++**Schnellversandmodus aktivieren** (Push).

Der Schnellversand-Modus ist ein Add-on für [!DNL Journey Optimizer], das den sehr schnellen Versand von Push-Nachrichten in großen Mengen im Rahmen von Kampagnen ermöglicht. Der Schnellversand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch ist oder wenn Sie eine dringende Push-Benachrichtigung auf Mobiltelefone senden möchten, z. B. eine Eilmeldung an Benutzer, die Ihre Nachrichten-App installiert haben. Weitere Informationen zur Performance bei Verwendung des Schnellversand-Modus finden Sie unter [Produktbeschreibung für Adobe Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html).

+++

## Nächste Schritte {#next}

Sobald Ihre Kampagnenkonfiguration und der Inhalt fertig sind, können Sie den Inhalt entwerfen. [Weitere Informationen](api-triggered-campaign-content.md)
