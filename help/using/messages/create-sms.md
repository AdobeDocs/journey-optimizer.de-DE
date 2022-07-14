---
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: ht
source-wordcount: '427'
ht-degree: 100%

---

# Erstellen einer SMS-Nachricht {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-Erstellung"
>abstract="Fügen Sie Ihre Textnachricht hinzu und beginnen Sie mit ihrer Personalisierung mithilfe des Ausdruckseditors."

Nachdem Sie [eine Nachricht erstellt haben](get-started-content.md), verwenden Sie die Registerkarte **[!UICONTROL SMS]**, um die Einstellungen und den Inhalt der SMS-Nachricht festzulegen.


>[!AVAILABILITY]
>
>Der SMS-Kanal ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter.

![](assets/sms_1.png)

Wenn Sie zum ersten Mal eine SMS erstellen, stellen Sie sicher, dass der SMS-Kanal konfiguriert wurde. [Weitere Informationen](../configuration/sms-configuration.md).

## Definieren Ihres SMS-Inhalts{#sms-content}

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS-Nachricht zu beginnen:

1. Klicken Sie auf das Feld **[!UICONTROL Textnachricht hinzufügen]**, um den Ausdruckseditor zu öffnen.

   ![](assets/sms_3.png)

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren. Sie können jedes Attribut verwenden, um Inhalte zu personalisieren, z. B. den Profilnamen oder die Stadt. Weitere Informationen zur Personalisierung im Ausdruckseditor finden Sie in [diesem Abschnitt](../personalization/personalize.md).

   >[!NOTE]
   >
   > Eine SMS-Nachricht kann bis zu 160 Zeichen lang sein, einschließlich Leerzeichen und Zeilenumbrüchen.

   ![](assets/sms_2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Ihre Nachricht fertig ist.

## Validieren Ihrer SMS{#sms-preview}

Sobald der Inhalt der Nachricht festgelegt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie [personalisierte Inhalte](../personalization/personalize.md) eingefügt haben, können Sie überprüfen, wie diese Inhalte in der Nachricht angezeigt werden, indem Sie Testprofildaten verwenden.

Um zu visualisieren, wie Ihre SMS-Nachricht auf Mobilgeräten angezeigt wird, navigieren Sie zur Registerkarte **[!UICONTROL Vorschau]**.

Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../design/preview.md).

## Veröffentlichen Ihrer SMS {#sms-publish}

Sobald Ihre Nachricht fertig ist, können Sie sie über die Schaltfläche **[!UICONTROL Veröffentlichen]** veröffentlichen und sie damit dem Versand zur Verfügung stellen. Mit dieser Aktion wird die neue Version der Nachricht veröffentlicht, die für die nächsten Versandausführungen in Ihren Journeys verwendet wird.

Ihre SMS-Nachricht kann jetzt in einer Journey verwendet werden. [Erfahren Sie, wie Sie Journeys erstellen](../building-journeys/journey-gs.md).

## Opt-in und Opt-out{#sms-opt-in-out}

Bei allen Marketing-Nachrichten muss die SMS eine Möglichkeit enthalten, mit der sich die Empfangenden leicht abmelden können. Nach der Abmeldung werden die Profile automatisch aus der Zielgruppe künftiger Marketing-Nachrichten entfernt. Für Transaktionsnachrichten ist das Hinzufügen eines Links zum Abmelden nicht erforderlich.

Menschen, die SMS erhalten, können mit Keywords zum Opt-in oder Opt-out antworten. In Übereinstimmung mit den Branchenstandards und -vorschriften verarbeitet Adobe Journey Optimizer automatisch die folgenden Schlüsselwörter in eingehenden Nachrichten: START, STOP und UNSTOP. Diese Keywords lösen automatische Standardantworten des SMS-Anbieters aus.

Weiterführende Informationen zur Unterstützung von nativen eingehenden Keywords (Start, Stopp und Unstop) für SMS finden Sie im folgenden Video.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

## Anleitungsvideo

Erfahren Sie, wie Sie SMS-Nachrichten konfigurieren, erstellen und in Ihre Journey integrieren können.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](../configuration/sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer neuen Nachricht](get-started-content.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
