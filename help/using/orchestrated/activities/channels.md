---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer Kanalaktivität in einer mehrstufigen Kampagne
description: Erfahren Sie, wie Sie eine Kanalaktivität in einer mehrstufigen Kampagne hinzufügen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 7842bd150b6c15f21a30b778d42520cc42237d82
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 21%

---

# Kanalaktivitäten {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="E-Mail-Aktivität"
>abstract="Die Aktivität E-Mail ermöglicht den Versand von E-Mails innerhalb einer orchestrierten Kampagne, sowohl für einmalige als auch für wiederkehrende Nachrichten. Dies dient zur Automatisierung des E-Mail-Versands an eine Zielgruppe, die innerhalb derselben orchestrierten Kampagne berechnet wird. Kanalaktivitäten können in einer mehrstufigen Kampagnenarbeitsfläche kombiniert werden, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf Kundenverhalten und Daten Aktionen ausgelöst werden können."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="SMS-Aktivität"
>abstract="Die SMS-Aktivität ermöglicht den Versand von SMS innerhalb einer orchestrierten Kampagne, sowohl für einmalige als auch für wiederkehrende Nachrichten. Dies dient zur Automatisierung des SMS-Versands an eine Zielgruppe, die innerhalb derselben orchestrierten Kampagne berechnet wird. Kanalaktivitäten können in der mehrstufigen Kampagnenarbeitsfläche kombiniert werden, um kanalübergreifende Kampagnen zu erstellen, mit denen basierend auf Kundenverhalten und Daten Aktionen ausgelöst werden können."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Push-Aktivität"
>abstract="Mit der Aktivität Push können Sie Push-Benachrichtigungen als Teil Ihrer orchestrierten Kampagne senden. Sie ermöglicht den Versand sowohl einmaliger als auch wiederkehrender orchestrierter Kampagnen und automatisiert so den Versand von Push-Benachrichtigungen an eine vordefinierte Zielgruppe innerhalb derselben orchestrierten Kampagne. Sie können Kanalaktivitäten in der Kampagnenarbeitsfläche kombinieren, um kanalübergreifende Kampagnen zu erstellen, mit denen anhand des Kundenverhaltens und der Daten Trigger erstellt werden können."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Aktivität „Direkt-Mail“"
>abstract="Die Aktivität Briefpost erleichtert den Briefpostversand innerhalb Ihrer orchestrierten Kampagne, sowohl für einmalige als auch für wiederkehrende Nachrichten. Sie dient dazu, das Generieren der von Direkt-Mail-Dienstleistern benötigten Extraktionsdatei zu automatisieren. Sie können Kanalaktivitäten in der orchestrierten Kampagnen-Arbeitsfläche kombinieren, um Cross-Channel-Kampagnen zu erstellen, mit denen anhand des Kundenverhaltens und der Daten Trigger erstellt werden können."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Erstellen einer orchestrierten Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - **[Kanalaktivitäten](channels.md)** - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Verzweigung](enrichment.md) - [Abstimmung](fork.md) [ ](reconciliation.md) [ ](split.md) - Aufspaltung[Warten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer] ermöglicht die Automatisierung und Ausführung von Marketing-Kampagnen über verschiedene Kanäle hinweg. Sie können Kanalaktivitäten in der orchestrierten Kampagnen-Arbeitsfläche kombinieren, um kanalübergreifend orchestrierte Kampagnen zu erstellen, mit denen anhand des Kundenverhaltens und der Daten Trigger erstellt werden können.

Sie können beispielsweise eine Begrüßungs-E-Mail-Kampagne erstellen, die eine Reihe von Nachrichten über verschiedene Kanäle wie E-Mail, SMS und Push-Benachrichtigungen enthält. Sie können auch eine Folge-E-Mail senden, nachdem eine Kundin oder ein Kunde einen Kauf getätigt hat, oder eine personalisierte Geburtstagsnachricht per SMS an eine Kundin bzw. einen Kunden senden.

Mithilfe von Kanalaktivitäten können Sie umfassende und personalisierte Kampagnen erstellen, die Kundinnen und Kunden über mehrere Touchpoints hinweg ansprechen und Konversionen fördern. Unterstützte Kanäle sind E-Mail, SMS und Push.

>[!PREREQUISITES]
>
>Bevor Sie eine Kanalaktivität hinzufügen, müssen Sie die Audience definieren. Die Zielgruppe ist das hauptsächliche Ziel Ihres Versands: die Profile, die die Nachrichten erhalten. [Erfahren Sie, wie Sie die Aktivität „Zielgruppe aufbauen“ verwenden](build-audience.md)

Gehen Sie wie folgt vor, um einen Versand im Kontext einer orchestrierten Kampagne einzurichten.

## Kanalaktivität hinzufügen und ihre Eigenschaften definieren {#add}

1. Fügen Sie der Arbeitsfläche eine Kanalaktivität hinzu. Verfügbare Kanalaktivitäten sind **[!UICONTROL E-Mail]**, **[!UICONTROL SMS]** und **[!UICONTROL Push]**.

   ![Bild, das die Arbeitsfläche mit verfügbaren Aktivitäten zeigt](../assets/channel-add.png)

1. Wählen Sie die hinzugefügte Aktivität aus und klicken Sie je nach **[!UICONTROL Kanal auf]** E-Mail bearbeiten **[!UICONTROL „SMS bearbeiten]** oder **[!UICONTROL Push bearbeiten]**.

   ![Bild, das die Arbeitsfläche mit einer E-Mail -Aktivität zeigt](../assets/channel-edit.png)

1. Geben Sie auf **[!UICONTROL Registerkarte]** eine Beschreibung für Ihre Kampagne ein und wechseln Sie dann zur Registerkarte **[!UICONTROL Aktionen]**, um die Aktivität zu konfigurieren.

## Einrichten der Kanalkonfiguration und -einstellungen {#configuration}

Verwenden Sie die Registerkarte **[!UICONTROL Aktionen]**, um eine Kanalkonfiguration für Ihre Nachricht auszuwählen und zusätzliche Einstellungen wie Tracking, Inhaltsexperiment oder mehrsprachige Inhalte zu konfigurieren.

1. Wählen Sie die Kanalkonfiguration für Ihre Nachricht aus.

   Eine Konfiguration wird durch [Systemadmins](../../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Erfahren Sie, wie Sie Kanalkonfigurationen einrichten](../../configuration/channel-surfaces.md).

   ![Bild mit dem Abschnitt Aktionen](../assets/channel-actions.png)

1. Verwenden Sie für E-Mail und SMS die Optionen im Abschnitt **[!UICONTROL Aktions-Tracking]**, um zu verfolgen, wie Ihre Empfängerinnen und Empfänger auf Ihre E-Mail- oder SMS-Sendungen reagieren. Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../../reports/campaign-global-report-cja.md)

1. Verwenden Sie für Push-Benachrichtigungen die Option **[!UICONTROL Schnellversandmodus]**, um einen Nachrichtenversand mit hoher Geschwindigkeit über den Push-Kanal an eine Audience von weniger als 30 Millionen durchzuführen.

   Der Schnellversand-Modus ist ein Add-on für [!DNL Journey Optimizer], das den sehr schnellen Versand von Push-Nachrichten in großen Mengen im Rahmen von Kampagnen ermöglicht. Der Schnellversand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch ist oder wenn Sie eine dringende Push-Benachrichtigung auf Mobiltelefone senden möchten, z. B. eine Eilmeldung an Benutzer, die Ihre Nachrichten-App installiert haben. Weitere Informationen zur Performance bei Verwendung des Schnellversand-Modus finden Sie unter [Produktbeschreibung für Adobe Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html).

1. Im Abschnitt **[!UICONTROL Inhaltsexperiment]** können Sie mehrere Versandmethoden definieren, um zu messen, welche für Ihre Zielgruppe am besten geeignet ist. Klicken Sie auf **[!UICONTROL Experiment erstellen]** und führen Sie dann die in diesem Abschnitt beschriebenen Schritte aus: [Erstellen eines Inhaltsexperiments](../../content-management/content-experiment.md).

   ![Bild mit dem Abschnitt „Inhaltsexperiment“](../assets/channel-experiment.png)

1. Verwenden Sie den **[!UICONTROL Languages]**, um in Ihrer Kampagne Inhalte in mehreren Sprachen zu erstellen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die gewünschten **[!UICONTROL Spracheinstellungen]** aus. Detaillierte Informationen zum Einrichten und Verwenden mehrsprachiger Funktionen finden Sie in diesem Abschnitt: [Erste Schritte mit mehrsprachigen Inhalten](../../content-management/multilingual-gs.md)

Wenn Ihre Kanalaktivität konfiguriert wurde, wählen Sie die Registerkarte **[!UICONTROL Inhalt]** aus, um ihren Inhalt zu definieren.

## Definieren des Inhalts {#content}

Verwenden Sie die **[!UICONTROL Inhalt]**, um den Inhalt der Nachricht zu definieren. Der Prozess der Inhaltserstellung hängt vom ausgewählten Kanal ab. Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="E-Mail" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>E-Mail</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="Push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Push-Benachrichtigung</strong></a></td>
</tr></table>

Wenn Ihr Inhalt definiert wurde, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und Ihren Inhalt mit Testprofilen oder Beispieleingabedaten zu testen, die aus einer CSV-/JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Weitere Informationen](../../content-management/preview-test.md)

## Nächste Schritte {#next}

Wenn der Nachrichteninhalt fertig ist, navigieren Sie mit dem Pfeil „Zurück **[!UICONTROL zurück zu Ihrer]**.

Sie können jetzt die Orchestrierung der Aktivitäten auf der Arbeitsfläche abschließen und die Kampagne veröffentlichen, um den Nachrichtenversand zu starten. [Erfahren Sie, wie Sie orchestrierte Kampagnen starten und überwachen](../start-monitor-campaigns.md)

![Bild mit der Schaltfläche „Zurück“](../assets/channel-back.png)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
