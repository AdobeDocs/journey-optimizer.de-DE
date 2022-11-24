---
title: In-App-Bericht
description: Erfahren Sie, wie Sie Daten aus dem In-App-Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3d496efc-1bf9-4895-906c-3757f92c6fe3
source-git-commit: 3f43cfac56e4665dc16ce24e9736bcfcd3c544bf
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 53%

---

# In-App-Bericht {#inapp-report}

Der In-App-Bericht ist im Kampagnenbericht verfügbar.

Die Seite „Kampagnenbericht“ wird mit den folgenden Registerkarten angezeigt:

* [Campaign](../reports/campaign-global-report.md#campaign-live)
* [E-Mail](../reports/campaign-global-report.md#email-live)
* [Push-Benachrichtigung](../reports/campaign-global-report.md#push-live)
* [SMS](../reports/campaign-global-report.md#sms-live)
* [In-App](#in-app-global)

Der **[!UICONTROL Globale Bericht]** in Campaign ist in verschiedene Widgets unterteilt, die Erfolge und Fehler bei Ihrer Kampagne detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](../reports/global-report.md#modify-dashboard).

Eine detaillierte Liste aller in Adobe Journey Optimizer verfügbaren Metriken finden Sie auf [dieser Seite](../reports/global-report.md#list-of-components-global.md)

## Registerkarte „In-App“ {#inapp-global}

Im **[!UICONTROL globalen Bericht]** Ihrer Kampagne finden Sie auf der Registerkarte **[!UICONTROL In-App]** die wichtigsten Informationen zu den In-App-Sendungen, die in Ihrer Kampagne versendet wurden.

![](assets/campaign_report_global_6.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL In-App-Leistung]** geben die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucher mit Ihren In-App-Nachrichten an, z. B.:

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Nutzer, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.

* **[!UICONTROL Abweisungsrate]**: Prozentsatz der In-App-Nachrichten, die von Empfängern abgewiesen wurden.

Das Diagramm **[!UICONTROL In-App-Zusammenfassung]** zeigt die Entwicklung Ihrer In-App-Impressions für den betroffenen Zeitraum an.

Das Diagramm und die Tabelle **[!UICONTROL Klicks nach Schaltfläche]** enthalten die verfügbaren Daten für das Empfängerverhalten je nach Schaltfläche:

* **[!UICONTROL Klicks]**: Gesamtzahl der Empfänger, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.
+++

**Verwandte Themen:**

* [Erstellen einer In-App-Nachricht](../in-app/create-in-app.md)
* [Entwerfen der In-App-Nachricht](../in-app/design-in-app.md)
* [In-App-Konfiguration](../in-app/inapp-configuration.md)


>[!BEGINTABS]

>[!TAB Hinzufügen eines Push zu einer Journey]

1. Öffnen Sie die Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

>[!TAB Hinzufügen einer Push-Benachrichtigung zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Push-Benachrichtigung]** als Aktion und wählen Sie die **[!UICONTROL Anwendungsoberfläche]** verwendet werden.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Zeitplan]** Ihrer Kampagne.

1. Aus dem **[!UICONTROL Action Triggers]** Menü, wählen Sie die **[!UICONTROL Häufigkeit]** Ihrer Push-Benachrichtigung:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monatlich

>[!ENDTABS]

Test 2:

1. Dies ist ein Test

>[!BEGINTABS]

    >[!TAB Push zu einer Journey hinzufügen]
    
    1. Öffnen Sie die Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.
    
    1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.
    
    >[!TAB Eine Push-Benachrichtigung zu einer Kampagne hinzufügen]
    
    1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie ** aus.[!UICONTROL Push-Benachrichtigung]** als Aktion und wählen Sie **[!UICONTROL Anwendungsoberfläche]** zu verwenden.
    
    1. Klicken Sie auf **[!UICONTROL Erstellen]**.
    
    1. Von **[!UICONTROL Eigenschaften]** Abschnitt, bearbeiten Sie die ** Ihrer Kampagne[!UICONTROL Titel]** und **[!UICONTROL Beschreibung]**.
    
    1. Klicken Sie auf **[!UICONTROL Zielgruppe auswählen]**-Schaltfläche, um die Zielgruppe aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.
    
    1. Im **[!UICONTROL Identitäts-Namespace]** verwenden, wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren.
    
    1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie das ** konfigurieren[!UICONTROL Zeitplan]** Ihrer Kampagne.
    
    1. Von **[!UICONTROL Action Triggers]** Menü, wählen Sie **[!UICONTROL Häufigkeit]** Ihrer Push-Benachrichtigung:
    
    * Einmal
    * Täglich
    * Wöchentlich
    * Monatlich

>[!ENDTABS]

1. Dies ist Teil des Tests

Test 3:

1. Dies ist ein Test

   >[!BEGINTABS]

   >[!TAB Hinzufügen eines Push zu einer Journey]

   1. Öffnen Sie die Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

   1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.
   >[!TAB Hinzufügen einer Push-Benachrichtigung zu einer Kampagne]

   1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Push-Benachrichtigung]** als Aktion und wählen Sie die **[!UICONTROL Anwendungsoberfläche]** verwendet werden.

   1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.

   1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll.

   1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Zeitplan]** Ihrer Kampagne.

   1. Aus dem **[!UICONTROL Action Triggers]** Menü, wählen Sie die **[!UICONTROL Häufigkeit]** Ihrer Push-Benachrichtigung:

      * Einmal
      * Täglich
      * Wöchentlich
      * Monatlich

   >[!ENDTABS]

1. Dies ist Teil des Tests

Test 3:

1. Dies ist ein Test

>[!BEGINTABS]

>[!TAB Hinzufügen eines Push zu einer Journey]

1. Öffnen Sie die Journey und ziehen Sie eine Push-Aktivität per Drag-and-Drop aus dem Bereich Aktionen der Palette.

1. Geben Sie grundlegende Informationen zu Ihrer Nachricht ein (Titel, Beschreibung, Kategorie) und wählen Sie dann die zu verwendende Nachrichtenoberfläche aus.

>[!TAB Hinzufügen einer Push-Benachrichtigung zu einer Kampagne]

1. Erstellen Sie eine neue geplante oder API-gesteuerte Kampagne und wählen Sie **[!UICONTROL Push-Benachrichtigung]** als Aktion und wählen Sie die **[!UICONTROL Anwendungsoberfläche]** verwendet werden.

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

1. Bearbeiten Sie im Bereich **[!UICONTROL Eigenschaften]** den **[!UICONTROL Titel]** und die **[!UICONTROL Beschreibung]** Ihrer Kampagne.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Audience auswählen]**, um die Audience aus der Liste der verfügbaren Adobe Experience Platform-Segmente zu definieren.

1. Wählen Sie im Feld **[!UICONTROL Identity-Namespace]** den Namespace aus, der zur Identifizierung der Personen im ausgewählten Segment verwendet werden soll.

1. Kampagnen sind so konzipiert, dass sie an einem bestimmten Datum oder in regelmäßigen Abständen ausgeführt werden. Erfahren Sie, wie Sie die **[!UICONTROL Zeitplan]** Ihrer Kampagne.

1. Aus dem **[!UICONTROL Action Triggers]** Menü, wählen Sie die **[!UICONTROL Häufigkeit]** Ihrer Push-Benachrichtigung:

   * Einmal
   * Täglich
   * Wöchentlich
   * Monatlich

>[!ENDTABS]

1. Dies ist Teil des Tests
