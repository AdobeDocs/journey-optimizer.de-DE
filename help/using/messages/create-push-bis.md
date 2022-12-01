---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren einer Push-Benachrichtigung
description: Erfahren Sie, wie Sie in Journey Optimizer eine Push-Benachrichtigung erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 50%

---

# Erstellen einer Push-Benachrichtigung {#create-push-notification-bis}

## Push-Benachrichtigung in einer Journey oder Kampagne erstellen

Gehen Sie wie folgt vor, um eine Push-Benachrichtigung zu erstellen:

>[!BEGINTABS]

>[!TAB Hinzufügen eines Push zu einer Journey]

1. Öffnen Sie die Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

   Weitere Informationen zum Konfigurieren einer Journey finden Sie unter

1. Klicken Sie im Journey-Konfigurationsbildschirm auf das **[!UICONTROL Inhalt bearbeiten]** Schaltfläche zum Konfigurieren des Push-Inhalts.

1. Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen.

1. Wenn Ihre Push-Benachrichtigung fertig ist, schließen Sie die Konfiguration Ihres aus, um sie zu senden.

   Um das Verhalten Ihrer Empfänger über Push-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die dedizierten Optionen im Tracking-Abschnitt im aktiviert sind.

>[!TAB Hinzufügen einer Push-Benachrichtigung zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Push-Benachrichtigung]** als Aktion und wählen Sie die **[!UICONTROL Anwendungsoberfläche]** verwendet werden.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Zeitplan]** der Kampagne in anzeigen.

1. Aus dem **[!UICONTROL Action Triggers]** Menü, wählen Sie die **[!UICONTROL Häufigkeit]** Ihrer Push-Benachrichtigung:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monatlich

1. Klicken Sie im Konfigurationsbildschirm der Kampagne auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** Schaltfläche zum Konfigurieren des Push-Inhalts.

1. Sobald der Inhalt der Nachricht erstellt wurde, können Sie mithilfe von Testprofilen eine Vorschau erstellen und einen Testversand durchführen.

1. Wenn Ihre Push-Benachrichtigung fertig ist, schließen Sie die Konfiguration Ihres aus, um sie zu senden.

   Um das Verhalten Ihrer Empfänger über Push-Öffnungen und/oder Interaktionen zu verfolgen, stellen Sie sicher, dass die dedizierten Optionen im Tracking-Abschnitt in der aktiviert sind.

>[!ENDTABS]

## Schnellversand-Modus

Schnellversand-Modus, in Journey zuvor als Burst-Modus bezeichnet, ist ein [!DNL Journey Optimizer] -Add-on, das den sehr schnellen Versand von Push-Nachrichten in großen Mengen durch Kampagnen ermöglicht.

Der Schnellversand wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch wäre oder wenn Sie eine dringende Push-Benachrichtigung an Mobiltelefone senden möchten, z. B. eine Eilmeldung an Benutzende, die Ihre Nachrichten-App installiert haben.

Weiterführende Informationen zur Leistung bei Verwendung des Rapid Delivery-Modus finden Sie im Abschnitt .

### Voraussetzungen

Für Nachrichten mit Schnellversand gelten folgende Anforderungen:

* Der Schnellversand ist nur für **[!UICONTROL geplante]** Kampagnen verfügbar und nicht für Kampagnen, die über eine API ausgelöst werden.
* In der Push-Benachrichtigung ist keine Personalisierung zulässig,
* Die Audience muss weniger als 30 Millionen Profile enthalten.
* Im Modus Schneller Versand können Sie bis zu fünf Kampagnen gleichzeitig ausführen.

### Aktivieren des Schnellversand-Modus

1. Erstellen Sie eine Push-Benachrichtigungskampagne und aktivieren Sie die Option **[!UICONTROL Schnellversand]**.

1. Konfigurieren Sie den Inhalt der Nachricht und wählen Sie die Audience aus.

   >[!IMPORTANT]
   >
   >Stellen Sie sicher, dass der Inhalt der Nachricht keine Personalisierung enthält und dass die Audience weniger als 30 Millionen Profile umfasst.

1. Überprüfen und aktivieren Sie Ihre Kampagne wie gewohnt. Beachten Sie, dass im Testmodus Nachrichten nicht über den Schnellversand-Modus gesendet werden.