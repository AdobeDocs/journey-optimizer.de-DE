---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen einer Kanalaktivität in einer mehrstufigen Kampagne
description: Erfahren Sie, wie Sie eine Kanalaktivität in einer mehrstufigen Kampagne hinzufügen
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: d8128190a51cac665c9f25b5077185a496ad7849
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 36%

---

# Kanalaktivitäten {#channel}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Orchestrierte Kampagne erstellen](../create-orchestrated-campaign.md)<br/><br/>[Aktivitäten orchestrieren](../orchestrate-activities.md)<br/><br/>[ Nachrichten mit orchestrierten Kampagnen senden](../send-messages.md)<br/><br/>[Kampagne starten und überwachen](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimensionsänderung](change-dimension.md) - [Kombinieren](combine.md) - [Deduplizierung](enrichment.md) - [Verzweigung](fork.md) - [Abstimmung](reconciliation.md) - [Aufspaltung](split.md)[ ](wait.md) Warten](deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

Adobe Journey Optimizer ermöglicht die Automatisierung und Ausführung von Marketing-Kampagnen über eingehende und ausgehende Kanäle hinweg. Sie können Kanalaktivitäten in der orchestrierten Kampagnen-Arbeitsfläche kombinieren, um kanalübergreifend orchestrierte Kampagnen zu erstellen, mit denen anhand des Kundenverhaltens und der Daten Trigger erstellt werden können. Die unterstützten Kanäle sind auf [dieser Seite](../../channels/gs-channels.md) aufgeführt.

Sie können beispielsweise eine Begrüßungs-E-Mail-Kampagne erstellen, die eine Reihe von Nachrichten über verschiedene Kanäle wie E-Mail, SMS, Push-Benachrichtigungen und Briefpost enthält. Sie können auch eine Folge-E-Mail senden, nachdem eine Kundin oder ein Kunde einen Kauf getätigt hat, oder eine personalisierte Geburtstagsnachricht per SMS an eine Kundin bzw. einen Kunden senden.

Mithilfe von Kanalaktivitäten können Sie umfassende und personalisierte Kampagnen erstellen, die Kundinnen und Kunden über mehrere Touchpoints hinweg ansprechen, und Konversionen fördern.

## Voraussetzungen {#channel-activity-prereq}

Beginnen Sie mit der Erstellung Ihrer orchestrierten Kampagne mit den relevanten Aktivitäten:

* Bevor Sie eine Kanalaktivität einfügen, müssen Sie die Zielgruppe definieren. Die Audience ist die Hauptzielgruppe Ihres Versands: die Profile, die die Nachrichten erhalten.

* Um einen wiederkehrenden Versand durchzuführen, starten Sie Ihre orchestrierte Kampagne mit einer **[!UICONTROL Planung]**-Aktivität. Sie können die Aktivität **[!UICONTROL Planung]** auch für einmalige Einzelsendungen verwenden, um für diese Sendungen das Kontaktdatum festzulegen. Dieses Kontaktdatum kann auch in den Versandeinstellungen festgelegt werden.

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

Gehen Sie wie folgt vor, um einen Versand im Kontext einer orchestrierten Kampagne einzurichten:

1. Kanalaktivität hinzufügen. Unterstützte Kanäle sind **[!UICONTROL E-Mail]**, **[!UICONTROL SMS]** oder **[!UICONTROL Push-Benachrichtigung]**

1. Wählen Sie den **Versandtyp** aus: einmalig oder wiederkehrend.

   * Ein **Einzelversand** ist ein einmaliger Versand, der nur einmal verschickt wird, z. B. eine E-Mail zum „Black Friday“.
   * Ein **wiederkehrender Versand** wird basierend auf seiner Ausführungshäufigkeit mehrmals gesendet. Bei jeder Ausführung der orchestrierten Kampagne wird die Audience neu berechnet und der Versand mit den aktualisierten Inhalten an die aktualisierte Audience gesendet. Dabei kann es sich um einen wöchentlichen Newsletter oder eine wiederkehrende Geburtstags-E-Mail handeln.

1. Wählen Sie eine **[!UICONTROL Versandvorlage]** aus. Vorlagen sind vorkonfigurierte, kanalspezifische Versandeinstellungen. Für jeden Kanal ist eine integrierte Vorlage verfügbar, die standardmäßig vorausgefüllt ist.

   ![](../assets/delivery-activity-in-wf.png)

   Sie können die Vorlage im linken Bereich zur Konfiguration der Kanalaktivität auswählen. Wenn die zuvor ausgewählte Zielgruppe nicht mit dem Kanal kompatibel ist, können Sie keine Vorlage auswählen. Um dies zu beheben, aktualisieren Sie die Aktivität **[!UICONTROL Zielgruppe aufbauen]**, um eine Zielgruppe mit dem richtigen Zielgruppen-Mapping auszuwählen.

1. Klicken Sie auf **[!UICONTROL Versand erstellen]**. Sie können dann Ihre Nachrichteneinstellungen und den Inhalt so wie einen eigenständigen Versand definieren. Sie können den Inhalt auch testen und simulieren.

1. Navigieren Sie zurück zu Ihrer orchestrierten Kampagne. Wenn Sie mit der orchestrierten Kampagne fortfahren möchten, aktivieren Sie die Option **[!UICONTROL Ausgehende Transition erzeugen]**, um nach der Kanalaktivität eine Transition hinzuzufügen.

1. Klicken Sie **[!UICONTROL Starten]** um Ihre orchestrierte Kampagne zu starten.

   Standardmäßig erfolgt der Trigger einer orchestrierten Kampagne in der Vorbereitungsphase der Nachricht, ohne dass die Nachricht sofort gesendet werden muss.

1. Öffnen Sie die Kanalaktivität, um den Versand über die Schaltfläche **[!UICONTROL Überprüfen und senden]** zu bestätigen.

1. Klicken Sie im Versand-Dashboard auf **[!UICONTROL Senden]**.

## Beispiele {#cross-channel-workflow-sample}

Im Folgenden finden Sie ein Beispiel einer kanalübergreifenden orchestrierten Kampagne mit einer Segmentierung und zwei Sendungen. Die organisierte Kampagne richtet sich an alle Kunden, die in Paris leben und sich für Kaffeemaschinen interessieren. Innerhalb dieser Population wird eine E-Mail an die regulären Kundinnen und Kunden und eine SMS an diejenigen mit VIP-Status gesendet.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

Sie können auch eine wiederkehrende orchestrierte Kampagne erstellen, um eine personalisierte SMS an jeden ersten Tag des Monats um 20 Uhr an alle in Paris lebenden Kunden zu senden.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
