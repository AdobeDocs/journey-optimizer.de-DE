---
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: ad09f4ec728e95da23f862e0e59fe827c71f0024
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 93%

---

# Erstellen einer SMS-Nachricht {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-Erstellung"
>abstract="Fügen Sie eine Textnachricht hinzu und beginnen Sie mit ihrer Personalisierung mithilfe des Ausdruckseditors."

Verwenden Sie [!DNL Journey Optimizer], um Textnachrichten an die mobilen Geräte Ihrer Kunden zu senden. Mit dem SMS-Editor können Sie Nachrichten im Textformat erstellen, personalisieren und in der Vorschau anzeigen.

Nachdem Sie [eine SMS-Aktivität zu Ihrer Journey hinzugefügt](get-started-content.md) und die Grundeinstellungen festgelegt haben, verwenden Sie den rechten Fensterbereich **[!UICONTROL Aktionen: SMS]**, um den Inhalt für die SMS-Nachricht zu erstellen.

![](assets/sms-edit-content.png)

Wenn Sie zum ersten Mal eine SMS erstellen, stellen Sie sicher, dass der SMS-Kanal konfiguriert wurde. [Weitere Informationen](../configuration/sms-configuration.md).

## Definieren Ihres SMS-Inhalts{#sms-content}

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS-Nachricht zu beginnen:

1. Klicken Sie auf das Feld **[!UICONTROL Nachricht]**, um den Ausdruckseditor zu öffnen.

   ![](assets/sms-content.png)

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren. Sie können jedes Attribut verwenden, um Inhalte zu personalisieren, z. B. den Profilnamen oder die Stadt. Weitere Informationen zur Personalisierung im Ausdruckseditor finden Sie in [diesem Abschnitt](../personalization/personalize.md).

1. Klicken Sie auf **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau.

   ![](assets/sms-content-preview.png)

## Validieren Ihrer SMS{#sms-preview}

>[!NOTE]
>
> Für eine bessere Zustellbarkeit sollten Sie stets die Telefonnummern in den vom Provider unterstützten Formaten verwenden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sobald der Inhalt der Nachricht festgelegt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie [personalisierte Inhalte](../personalization/personalize.md) eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

Um zu sehen, wie Ihre SMS-Nachricht auf mobilen Geräten angezeigt wird, klicken Sie auf die Registerkarte **[!UICONTROL Inhalt simulieren]**. Weiterführende Informationen zum Simulieren von Inhalten finden Sie in [diesem Abschnitt](../design/preview.md).

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. Weiterführende Informationen finden Sie in [diesem Abschnitt](alerts.md).

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
