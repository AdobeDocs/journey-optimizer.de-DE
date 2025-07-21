---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren der Kampagnenaktion
description: Erfahren Sie, wie Sie die Kampagnenaktion konfigurieren.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 33%

---


# Konfigurieren der Kampagnenaktion {#action-campaign-action}

Verwenden Sie die Registerkarte **[!UICONTROL Aktionen]**, um eine Kanalkonfiguration für Ihre Nachricht auszuwählen und zusätzliche Einstellungen wie Tracking, Inhaltsexperiment oder mehrsprachige Inhalte zu konfigurieren.

1. **Kanal auswählen**

   Navigieren Sie zur Registerkarte **[!UICONTROL Aktionen]**, klicken Sie auf die Schaltfläche **[!UICONTROL Aktion hinzufügen]** und wählen Sie den Kommunikationskanal aus.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >Die verfügbaren Kanäle variieren je nach Ihrem Lizenzmodell und Ihren Add-ons.

1. **Wählen Sie eine Kanalkonfiguration**

   Eine Konfiguration wird durch [Systemadmins](../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Erfahren Sie, wie Sie Kanalkonfigurationen einrichten](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Erstellen eines Inhaltsexperiments**

   Im Abschnitt **[!UICONTROL Inhaltsexperiment]** können Sie mehrere Versandmethoden definieren, um zu messen, welche für Ihre Zielgruppe am besten geeignet ist. Klicken Sie auf **[!UICONTROL Experiment erstellen]** und führen Sie dann die in diesem Abschnitt beschriebenen Schritte aus: [Erstellen eines Inhaltsexperiments](../content-management/content-experiment.md).

1. **Mehrsprachige Inhalte hinzufügen**

   Verwenden Sie den **[!UICONTROL Languages]**, um in Ihrer Kampagne Inhalte in mehreren Sprachen zu erstellen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die gewünschten **[!UICONTROL Spracheinstellungen]** aus. Detaillierte Informationen zum Einrichten und Verwenden mehrsprachiger Funktionen finden Sie in diesem Abschnitt: [Erste Schritte mit mehrsprachigen Inhalten](../content-management/multilingual-gs.md)

Je nach ausgewähltem Kommunikationskanal stehen zusätzliche Einstellungen zur Verfügung. Erweitern Sie die folgenden Abschnitte, um weitere Informationen zu erhalten.

+++**Begrenzungsregeln anwenden** (E-Mail, Briefpost, Push, SMS)

Wählen **[!UICONTROL in der Dropdown]** Liste „Geschäftsregeln“ einen Regelsatz aus, um Begrenzungsregeln auf Ihre Kampagne anzuwenden. Mithilfe von Kanalregelsätzen können Sie die Frequenzbegrenzung nach Kommunikationstyp festlegen, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überlastet werden. [Informationen zum Arbeiten mit Regelsätzen](../conflict-prioritization/rule-sets.md)

+++

+++**Interaktion verfolgen** (E-Mail, SMS).

Verwenden Sie den Abschnitt **[!UICONTROL Aktions-Tracking]**, um zu verfolgen, wie Ihre Empfängerinnen und Empfänger auf Ihre E-Mail- oder SMS-Sendungen reagieren. Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

+++

+++**Schnellversandmodus aktivieren** (Push).

Der Schnellversand-Modus ist ein Add-on für [!DNL Journey Optimizer], das den sehr schnellen Versand von Push-Nachrichten in großen Mengen im Rahmen von Kampagnen ermöglicht. Der Schnellversand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch ist oder wenn Sie eine dringende Push-Benachrichtigung auf Mobiltelefone senden möchten, z. B. eine Eilmeldung an Benutzer, die Ihre Nachrichten-App installiert haben. Weitere Informationen zur Performance bei Verwendung des Schnellversand-Modus finden Sie unter [Produktbeschreibung für Adobe Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html).

+++

+++**Prioritätswerte zuweisen** (Web, In-App, Code-basiert)

Durch Zuweisung eines Prioritätswerts zur Kampagne können Sie bei einer auferlegten Einschränkung wie einer Häufigkeitsbegrenzung eine eingehende Kampagne priorisieren. Geben Sie einen numerischen Wert ein (0–100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. [Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](../conflict-prioritization/priority-scores.md)

+++

+++**Festlegen zusätzlicher Versandregeln** (Inhaltskarten)

Für Inhaltskartenkampagnen können Sie zusätzliche Versandregeln aktivieren, um die Ereignisse und Kriterien auszuwählen, die die Nachricht auslösen sollen. [Erfahren Sie, wie Sie Inhaltskarten erstellen](../content-card/create-content-card.md)

+++

+++**Trigger definieren** (In-App)

Für In-App-Nachrichten können Sie über die Schaltfläche **[!UICONTROL Trigger bearbeiten]** die Ereignisse und Kriterien auswählen, die die Nachricht auslösen sollen. [Erfahren Sie, wie Sie eine In-App-Nachricht erstellen](../in-app/create-in-app.md)

+++

## Nächste Schritte {#next}

Sobald Ihre Kampagnenaktion fertig ist, können Sie ihren Inhalt entwerfen. [Weitere Informationen](campaign-content.md)
