---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer Kanalaktivität in einer mehrstufigen Kampagne
description: Erfahren Sie, wie Sie eine Kanalaktivität in einer mehrstufigen Kampagne hinzufügen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 1a4cd7df44cb54aaf4d18409574f5ceb9537935c
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 30%

---

# Kanalaktivitäten {#channel}

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

## Voraussetzungen {#channel-activity-prereq}

Beginnen Sie mit der Erstellung Ihrer orchestrierten Kampagne mit den relevanten Aktivitäten:

* Bevor Sie eine Kanalaktivität einfügen, müssen Sie die Zielgruppe definieren. Die Zielgruppe ist das hauptsächliche Ziel Ihres Versands: die Profile, die die Nachrichten erhalten. [Erfahren Sie, wie Sie die Aktivität „Zielgruppe aufbauen“ verwenden](build-audience.md)

* Um einen wiederkehrenden Versand durchzuführen, starten Sie Ihre orchestrierte Kampagne mit einer **[!UICONTROL Planung]**-Aktivität. Sie können die Aktivität **[!UICONTROL Planung]** auch für einmalige Einzelsendungen verwenden, um für diese Sendungen das Kontaktdatum festzulegen. Dieses Kontaktdatum kann auch in den Versandeinstellungen festgelegt werden. [Erfahren Sie, wie Sie eine orchestrierte Kampagne planen](../create-orchestrated-campaign.md#schedule)

## Konfigurieren einer Kanalaktivität {#create-a-delivery-in-a-workflow}

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

Gehen Sie wie folgt vor, um einen Versand im Kontext einer orchestrierten Kampagne einzurichten.

### Kanalaktivität hinzufügen und ihre Eigenschaften definieren {#add}

1. Fügen Sie der Arbeitsfläche eine Kanalaktivität hinzu. Verfügbare Kanalaktivitäten sind **[!UICONTROL E-Mail]**, **[!UICONTROL SMS]** und **[!UICONTROL Push]**.

   ![Bild, das die Arbeitsfläche mit verfügbaren Aktivitäten zeigt](../assets/channel-add.png)

1. Wählen Sie die hinzugefügte Aktivität aus und klicken Sie je nach **[!UICONTROL Kanal auf]** E-Mail bearbeiten **[!UICONTROL „SMS]**&quot; oder **[!UICONTROL Push bearbeiten]**.

   ![Bild, das die Arbeitsfläche mit einer E-Mail -Aktivität zeigt](../assets/channel-edit.png)

1. Geben **[!UICONTROL auf der]** „Eigenschaften“ eine Beschreibung für Ihre Kampagne ein.

### Einrichten der Kanalkonfiguration und -einstellungen {#configuration}

1. Wählen Sie die Registerkarte **[!UICONTROL Aktionen]** und wählen Sie die Kanalkonfiguration aus, die für Ihre Nachricht verwendet werden soll.

   Eine Konfiguration wird durch [Systemadmins](../../start/path/administrator.md) definiert. Sie enthält alle technischen Parameter zum Senden der Nachricht, wie z. B. Kopfzeilenparameter, Subdomain, Mobile Apps usw. [Erfahren Sie, wie Sie Kanalkonfigurationen einrichten](../../configuration/channel-surfaces.md).

1. Je nach Kanal stehen mehrere Optionen zur Verfügung. Durchsuchen Sie die folgenden Registerkarten, um weitere Informationen zu erhalten:

   >[!BEGINTABS]

   >[!TAB E-Mail]

   Verwenden Sie die Optionen **[!UICONTROL Öffnungen von E]** Mails verfolgen und **[!UICONTROL Klicks auf Links und Schaltflächen in E-Mails]**, um zu verfolgen, wie Ihre Empfänger auf Ihren Versand reagieren.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

   >[!TAB SMS]

   Verwenden Sie die Option **[!UICONTROL Klicks auf Links in SMS verfolgen]**, um Klicks auf Links in Ihrer SMS zu verfolgen.

   Die Tracking-Ergebnisse sind nach Ausführung der Kampagne im Kampagnenbericht verfügbar. [Weitere Informationen zu Kampagnenberichten](../reports/campaign-global-report-cja.md)

   >[!TAB Push-Benachrichtigung]

   Der Schnellversand-Modus ist ein Add-on für **[!DNL Journey Optimizer]**, das den sehr schnellen Versand großer Mengen von Push-Nachrichten ermöglicht.

   Aktivieren Sie die Option **[!UICONTROL Schnellversandmodus]**, um einen Nachrichtenversand mit hoher Geschwindigkeit über den Push-Kanal an eine Audience von weniger als 30 Millionen durchzuführen. [Weitere Informationen](../push/create-push.md#rapid-delivery)

   >[!ENDTABS]

1. Im **[!UICONTROL Inhaltsexperiment]** können Sie mehrere Versandbehandlungen definieren, um zu messen, welche für Ihre Zielgruppe am besten geeignet ist.

   Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Experiment erstellen]** und führen Sie dann die in diesem Abschnitt beschriebenen Schritte aus: [Erstellen eines Inhaltsexperiments](../../content-management/content-experiment.md).

1. Im **[!UICONTROL Languages]** können Sie innerhalb Ihrer Kampagne Inhalte in mehreren Sprachen erstellen.

   Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Sprachen hinzufügen]** und wählen Sie die gewünschten **[!UICONTROL Spracheinstellungen]** aus. Detaillierte Informationen zum Einrichten und Verwenden mehrsprachiger Funktionen finden Sie in diesem Abschnitt: [Erste Schritte mit mehrsprachigen Inhalten](../../content-management/multilingual-gs.md)

### Definieren des Inhalts {#content}

Wählen Sie die **[!UICONTROL Inhalt]**, um den Inhalt der Nachricht zu definieren. Der Prozess der Inhaltserstellung hängt vom ausgewählten Kanal ab.

Auf den folgenden Seiten erfahren Sie, wie Sie Ihren Nachrichteninhalt erstellen:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="E-Mail" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>E-Mail</strong></a></div></td>
<td><a href="../sms/../create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="Push" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>Push-Benachrichtigung</strong></a></div></td>
</tr></table>

Nachdem der Inhalt definiert ist, verwenden Sie die Schaltfläche **[!UICONTROL Inhalt simulieren]**, um eine Vorschau anzuzeigen und den Inhalt mit Testprofilen oder Beispieleingabedaten zu testen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Weitere Informationen](../content-management/preview-test.md).

## Nächste Schritte {#next}

Navigieren Sie mithilfe des Pfeils **[!UICONTROL Zurück]** zurück zu Ihrer orchestrierten Kampagne.

![Bild mit der Schaltfläche „Zurück“](../assets/channel-back.png)

Sie können jetzt die Orchestrierung der Aktivitäten auf der Arbeitsfläche abschließen und die Kampagne veröffentlichen, um den Nachrichtenversand zu starten. [Erfahren Sie, wie Sie orchestrierte Kampagnen starten und überwachen](../start-monitor-campaigns.md)

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
