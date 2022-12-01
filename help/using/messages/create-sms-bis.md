---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer SMS-Nachricht
description: Erfahren Sie, wie Sie in Journey Optimizer eine SMS-Nachricht erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 55%

---

# Erstellen einer SMS-Nachricht {#create-sms-bis}

>[!NOTE]
>
>In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketing-Nachrichten eine Möglichkeit für die Empfänger enthalten, ihr Abo einfach zu kündigen. Zu diesem Zweck können SMS-Empfänger mit Keywords zum Opt-in oder Opt-out antworten.

## SMS-Nachrichten in einer Journey oder Kampagne erstellen

Gehen Sie wie folgt vor, um mit der Personalisierung Ihrer SMS-Nachricht zu beginnen:

>[!BEGINTABS]

>[!TAB Eine SMS-Nachricht zu einer Journey hinzufügen]

1. Öffnen Sie die Journey und ziehen Sie eine SMS-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

   Weiterführende Informationen zur Konfiguration einer Journey finden Sie im Abschnitt .

Sie können jetzt mit der Erstellung des Inhalts Ihrer SMS-Nachricht beginnen, indem Sie **[!UICONTROL Inhalt bearbeiten]** Schaltfläche.

>[!TAB Eine SMS zu einer Kampagne hinzufügen]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL SMS]** als Aktion und wählen Sie die **[!UICONTROL Anwendungsoberfläche]** verwendet werden.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Im **[!UICONTROL Aktionsverfolgung]** angeben, ob Sie Klicks auf Links in Ihrer SMS-Nachricht verfolgen möchten.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Zeitplan]** der Kampagne in anzeigen.

1. Aus dem **[!UICONTROL Action Triggers]** Menü, wählen Sie die **[!UICONTROL Häufigkeit]** Ihrer SMS-Nachricht:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monat

Sie können jetzt mit der Erstellung des Inhalts Ihrer SMS-Nachricht beginnen, indem Sie **[!UICONTROL Inhalt bearbeiten]** Schaltfläche.

>[!ENDTABS]

## Definieren Ihres SMS-Inhalts

1. Klicken Sie auf dem Journey- oder Kampagnenkonfigurationsbildschirm auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** Schaltfläche zum Konfigurieren des SMS-Inhalts.

1. Klicken Sie auf das Feld **[!UICONTROL Nachricht]**, um den Ausdruckseditor zu öffnen.

1. Verwenden Sie den Ausdruckseditor, um Inhalte zu definieren und dynamische Inhalte hinzuzufügen. Sie können jedes Attribut verwenden, sowie z. B. Profilnamen oder Stadt.

1. Klicken Sie auf **[!UICONTROL Speichern]** und überprüfen Sie Ihre Nachricht in der Vorschau.

1. Wenn Ihre SMS-Nachricht fertig ist, konfigurieren Sie Ihre , um sie zu senden.

## Validieren Ihrer SMS

>[!NOTE]
>
> Zur besseren Zustellbarkeit sollte stets die Telefonnummern in den vom Provider unterstützten Formaten verwendet werden. Beispielsweise unterstützen Twilio und Sinch nur Telefonnummern im E.164-Format.

Sobald der Inhalt der Nachricht festgelegt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen. Wenn Sie die Nachricht eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie dieser Inhalt in der Nachricht angezeigt wird.

Um zu sehen, wie Ihre SMS-Nachricht auf mobilen Geräten angezeigt wird, klicken Sie auf die Registerkarte **[!UICONTROL Inhalt simulieren]**. Erfahren Sie mehr über die Inhaltsimulation in .

Sie müssen auch Warnhinweise im oberen Bereich des Editors überprüfen.  Einige davon sind einfache Warnhinweise, andere können die Verwendung der Nachricht verhindern. Weitere Informationen finden Sie in .
