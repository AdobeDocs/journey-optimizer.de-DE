---
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 62%

---

# Erstellen einer SMS-Nachricht {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-Erstellung"
>abstract="Fügen Sie Ihre Textnachricht hinzu und beginnen Sie mit der Personalisierung mit dem Ausdruckseditor."

Verwendung [!DNL Journey Optimizer] , um Ihren Kunden auf ihren Mobilgeräten Textnachrichten zu senden. Sie können Nachrichten im Textformat im SMS-Editor erstellen, personalisieren und in der Vorschau anzeigen.

Einmal [SMS hinzugefügt](get-started-content.md) -Aktivität in Ihrer Journey und den definierten Grundeinstellungen verwenden Sie die **[!UICONTROL Aktionen: SMS]** den Inhalt der SMS-Nachricht erstellen.

>[!AVAILABILITY]
>
>Der SMS-Kanal ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter.

![](assets/sms-edit-content.png)

Wenn Sie zum ersten Mal eine SMS erstellen, stellen Sie sicher, dass der SMS-Kanal konfiguriert wurde. [Weitere Informationen](../configuration/sms-configuration.md).

## Definieren Ihres SMS-Inhalts{#sms-content}

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS-Nachricht zu beginnen:

1. Klicken Sie auf **[!UICONTROL Nachricht]** -Feld, um den Ausdruckseditor zu öffnen.

   ![](assets/sms-content.png)

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren. Sie können jedes Attribut verwenden, um Inhalte zu personalisieren, z. B. den Profilnamen oder die Stadt. Weitere Informationen zur Personalisierung finden Sie im Ausdruckseditor unter [diesem Abschnitt](../personalization/personalize.md).

1. Klicken **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau.

   ![](assets/sms-content-preview.png)


## Validieren Ihrer SMS{#sms-preview}

Sobald der Inhalt der Nachricht festgelegt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie [personalisierte Inhalte](../personalization/personalize.md) eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** Registerkarte. Weitere Informationen zur Inhaltsimulation finden Sie unter [diesem Abschnitt](../design/preview.md).

Sie müssen Warnhinweise auch im oberen Bereich des Editors überprüfen.  Bei einigen handelt es sich um einfache Warnungen, andere können Sie jedoch daran hindern, die Nachricht zu verwenden. Weiterführende Informationen finden Sie in [diesem Abschnitt](alerts.md).

![](assets/sms-alert-button.png)


## Opt-in und Opt-out{#sms-opt-in-out}

Bei allen Marketing-Nachrichten muss die SMS eine Möglichkeit enthalten, mit der sich die Empfangenden leicht abmelden können. Nach der Abmeldung werden die Profile automatisch aus der Zielgruppe künftiger Marketing-Nachrichten entfernt. Für Transaktionsnachrichten ist das Hinzufügen eines Links zum Abmelden nicht erforderlich.

Menschen, die SMS erhalten, können mit Keywords zum Opt-in oder Opt-out antworten. In Übereinstimmung mit den Branchenstandards und -vorschriften verarbeitet Adobe Journey Optimizer automatisch die folgenden Schlüsselwörter in eingehenden Nachrichten: START, STOP und UNSTOP. Diese Keywords lösen automatische Standardantworten des SMS-Anbieters aus.

Weiterführende Informationen zur Unterstützung von nativen eingehenden Keywords (Start, Stopp und Unstop) für SMS finden Sie im folgenden Video.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](../configuration/sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer neuen Nachricht](get-started-content.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
