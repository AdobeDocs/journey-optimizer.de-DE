---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren der Kampagnenaktion
description: Informationen zum Konfigurieren der Kampagnenaktion.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: Erstellen, Optimizer, Kampagne, Oberfläche, Nachrichten
exl-id: fed96e48-2e54-4bd4-ae17-77434d1b90eb
source-git-commit: 45c95d5682b35c8afb161b75c88942c010b36d1c
workflow-type: ht
source-wordcount: '528'
ht-degree: 100%

---

# Konfigurieren der Kampagnenaktion {#action-campaign-action}

Verwenden Sie die Registerkarte **[!UICONTROL Aktionen]**, um eine Kanalkonfiguration für Ihre Nachricht auszuwählen und um zusätzliche Einstellungen wie Tracking, Inhaltsexperimente oder mehrsprachige Inhalte zu konfigurieren.

1. **Auswählen des Kanals**

   Navigieren Sie zur Registerkarte **[!UICONTROL Aktionen]**, klicken Sie auf die Schaltfläche **[!UICONTROL Aktion hinzufügen]** und wählen Sie den Kommunikationskanal aus.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >Die verfügbaren Kanäle variieren je nach Ihrem Lizenzierungsmodell und Ihren Add-ons.

1. **Auswählen einer Kanalkonfiguration**

   Eine Konfiguration wird durch [Systemadmins](../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Informationen zum Einrichten von Kanalkonfigurationen](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Erstellen eines Inhaltsexperiments**

   Verwenden Sie den Abschnitt **[!UICONTROL Inhaltsexperiment]** zum Definieren mehrerer Versandabwandlungen, um zu messen, welche für Ihre Zielgruppe am besten geeignet ist. Klicken Sie auf **[!UICONTROL Experiment erstellen]** und führen Sie dann die in diesem Abschnitt beschriebenen Schritte aus: [Erstellen eines Inhaltsexperiments](../content-management/content-experiment.md).

1. **Hinzufügen mehrsprachiger Inhalte**

   Verwenden Sie den Abschnitt **[!UICONTROL Sprachen]**, um in Ihrer Kampagne Inhalte in mehreren Sprachen zu erstellen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die gewünschten **[!UICONTROL Spracheinstellungen]** aus. Detaillierte Informationen zur Einrichtung und Verwendung mehrsprachiger Funktionen finden Sie in diesem Abschnitt: [Erste Schritte mit mehrsprachigen Inhalten](../content-management/multilingual-gs.md)

Je nach ausgewähltem Kommunikationskanal stehen zusätzliche Einstellungen zur Verfügung. Erweitern Sie die folgenden Abschnitte, um weitere Informationen zu erhalten.

+++**Anwenden von Begrenzungsregeln** (E-Mail, Direkt-Mail, Push, SMS)

Wählen Sie in der Dropdown-Liste **[!UICONTROL Geschäftsregeln]** einen Regelsatz aus, um Begrenzungsregeln auf Ihre Kampagne anzuwenden. Mithilfe von Kanalregelsätzen können Sie die Frequenzbegrenzung nach Kommunikationstyp festlegen, um zu verhindern, dass Kundinnen und Kunden mit ähnlichen Nachrichten überlastet werden. [Erfahren Sie, wie Sie mit Regelsätzen arbeiten](../conflict-prioritization/rule-sets.md)

+++

+++**Verfolgen von Interaktionen** (E-Mail, SMS).

Verwenden Sie den Abschnitt **[!UICONTROL Aktions-Tracking]**, um zu verfolgen, wie Ihre Empfängerinnen und Empfänger auf Ihre E-Mail- oder SMS-Sendungen reagieren. Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

+++

+++**Aktivieren des Schnellversandmodus** (Push).

Der Schnellversandmodus ist ein Add-on für [!DNL Journey Optimizer], das den sehr schnellen Versand von Push-Nachrichten in großen Mengen im Rahmen von Kampagnen ermöglicht. Der Schnellversand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch wäre oder wenn Sie eine dringende Push-Benachrichtigung an Mobiltelefone senden möchten, z. B. eine Eilmeldung an Benutzende, die Ihre Nachrichten-App installiert haben. Weitere Informationen zur Performance bei Verwendung des Schnellversand-Modus finden Sie unter [Produktbeschreibung für Adobe Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html).

+++

+++**Zuweisen von Prioritätswerten** (Web, In-App, Code-basiert)

Wenn Sie der Kampagne einen Prioritätswert zuweisen, können Sie eine eingehende Kampagne bei erzwungenen Begrenzungen wie z. B. einer Frequenzbegrenzung priorisieren. Geben Sie einen numerischen Wert ein (0–100). Bitte beachten Sie: Je höher die Zahl, desto höher die Priorität. [Informationen zum Zuweisen von Prioritätswerten zu Journeys und Kampagnen](../conflict-prioritization/priority-scores.md)

+++

+++**Festlegen zusätzlicher Versandregeln** (Inhaltskarten)

Für Inhaltskartenkampagnen können Sie zusätzliche Versandregeln aktivieren, um die Ereignisse und Kriterien auszuwählen, die die Nachricht auslösen sollen. [Informationen zum Erstellen von Inhaltskarten](../content-card/create-content-card.md)

+++

+++**Definieren von Triggern** (In-App)

Für In-App-Nachrichten können Sie über die Schaltfläche **[!UICONTROL Trigger bearbeiten]** die Ereignisse und Kriterien auswählen, die die Nachricht auslösen sollen. [Informationen zum Erstellen einer In-App-Nachricht](../in-app/create-in-app.md)

+++

## Nächste Schritte {#next}

Sobald Ihre Kampagnenaktion fertiggestellt ist, können Sie den Inhalt entwerfen. [Weitere Informationen](campaign-content.md)
