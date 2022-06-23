---
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 067453ee3c19c7f269b4b1791ead8b5421adf95b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 75%

---

# Erstellen einer SMS-Nachricht {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS-Erstellung"
>abstract="Fügen Sie Ihre Textnachricht hinzu und beginnen Sie mit ihrer Personalisierung mithilfe des Ausdruckseditors."

>[!NOTE]
>
>Der SMS-Kanal ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer für Adobe.

Nachdem Sie [eine Nachricht erstellt](get-started-content.md) haben, verwenden Sie die Registerkarte **[!UICONTROL SMS]**, um die Einstellungen und den Inhalt für den E-Mail-Kanal zu definieren.

![](assets/sms_1.png)

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS-Nachricht zu beginnen:

1. Klicken Sie auf das Feld **[!UICONTROL Textnachricht hinzufügen]**, um den Ausdruckseditor zu öffnen.

   ![](assets/sms_3.png)

1. Mit dem Ausdruckseditor können Sie Inhalt und Personalisierungsdaten definieren. Weitere Informationen zur Personalisierung im Ausdruckseditor finden Sie in [diesem Abschnitt](../personalization/personalize.md).

   >[!NOTE]
   >
   > SMS-Nachrichten sind auf 160 Zeichen begrenzt.

   ![](assets/sms_2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, wenn Ihre personalisierte Nachricht fertig ist.

1. Klicken Sie auf **[!UICONTROL Vorschau]**, um sich anzeigen zu lassen, wie Ihre SMS-Nachricht auf Smartphones und Tablets angezeigt wird. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../design/preview.md).

1. Sobald Ihre Nachricht fertig ist, können Sie sie über die Schaltfläche **[!UICONTROL Veröffentlichen]** veröffentlichen und sie damit dem Versand zur Verfügung stellen. Mit dieser Aktion wird die neue Version der Nachricht veröffentlicht, die für die nächsten Versandausführungen in Ihren Journeys verwendet wird.

Ihre SMS-Nachricht kann jetzt in einer Journey verwendet werden. [Erfahren Sie, wie Sie Journeys erstellen](../building-journeys/journey-gs.md).

## Opt-in und Opt-out{#sms-opt-in-out}

SMS-Empfänger können mit Opt-in- und Opt-out-Keywords antworten. In Übereinstimmung mit den Branchenstandards und -vorschriften verarbeitet Adobe Journey Optimizer automatisch die folgenden Schlüsselwörter in eingehenden Nachrichten: START, STOP und UNSTOP. Diese Schlüsselwörter Trigger automatische Standardantworten des SMS-Anbieters.

**Verwandte Themen**

* [Konfigurieren des SMS-Kanals](../configuration/sms-configuration.md)
* [SMS-Bericht](../reports/journey-global-report.md#sms-global)
* [Erstellen einer neuen Nachricht](get-started-content.md)
* [Hinzufügen einer Nachricht zu einer Journey](../building-journeys/journeys-message.md)
