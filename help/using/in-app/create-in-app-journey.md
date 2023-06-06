---
title: In-App-Benachrichtigung in einer Journey erstellen
description: Erfahren Sie, wie Sie in Journey Optimizer eine In-App-Nachricht
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informative"
source-git-commit: e91ca6f6210fd883e7a483fe81dda59bdf6ab42a
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 76%

---

# Erstellen einer In-App-Nachricht in einer Journey erstellen. {#create-in-app-journey}

1. Öffnen Sie Ihre Journey und ziehen Sie eine **[!UICONTROL In-App]**-Aktivität per Drag-and-Drop aus dem Bereich **[!UICONTROL Aktionen]** der Palette.

   Wenn ein Profil das Ende seiner Journey erreicht, laufen alle ihm angezeigten In-App-Nachrichten automatisch ab. Aus diesem Grund wird nach Ihrer In-App-Aktivität automatisch eine Warteaktivität hinzugefügt, um einen angemessenen Zeitpunkt zu gewährleisten.

   ![](assets/in_app_journey_1.png)

1. Geben Sie einen **[!UICONTROL Titel]** und eine **[!UICONTROL Beschreibung]** für Ihre Nachricht ein.

1. Wählen Sie die [In-App-Oberfläche](inapp-configuration.md) aus, die verwendet werden soll.

   ![](assets/in_app_journey_2.png)

1. Sie können jetzt über die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** mit der Erstellung Ihrer Inhalte beginnen. [Weitere Informationen](design-in-app.md)

1. Klicken Sie auf **[!UICONTROL Trigger bearbeiten]**, um Ihren Trigger zu konfigurieren.

   ![](assets/in_app_journey_4.png)

1. Aus dem **[!UICONTROL Trigger von In-App-Nachrichten]** auswählen, die Ereignisse und Kriterien, die auf Ihre Nachricht Trigger werden sollen:

   1. Klicken Sie auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]**, wenn Sie möchten, dass der Trigger mehrere Ereignisse oder Kriterien berücksichtigt.
   1. Aus dem **[!UICONTROL Auswählen eines Ereignisses]** wählen Sie in der Dropdown-Liste den Ereignistyp für Ihren Trigger aus.
   1. Wählen Sie die Art der Verknüpfung Ihrer Ereignisse aus, z. B. **[!UICONTROL Und]**, wenn Sie möchten, dass **beide** Auslöser erfüllt sind, damit eine Nachricht angezeigt wird. Wählen Sie stattdessen **[!UICONTROL Oder]**, wenn Sie möchten, dass die Nachricht angezeigt wird, wenn **einer** der Auslöser erfüllt ist.
   1. Klicken Sie auf **[!UICONTROL Gruppe erstellen]**, um Trigger zu gruppieren.

   ![](assets/in_app_journey_3.png)

1. Wählen Sie die Häufigkeit aus, mit der Ihr Trigger aktiv ist:

   * **[!UICONTROL Jedes Mal]**: Zeigt immer die Nachricht an, wenn die Ereignisse im **[!UICONTROL App-Trigger]** angezeigt.
   * **[!UICONTROL Einmal anzeigen]**: Die Nachricht wird nur beim ersten Mal angezeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten.
   * **[!UICONTROL Bis zu Clickthrough]**: Diese Nachricht wird anzeigt, wenn die im Dropdown-Menü **[!UICONTROL Mobile-App-Trigger]** ausgewählten Ereignisse eintreten, bis vom SDK ein Interaktionsereignis mit der Aktion „Angeklickt“ übermittelt wird.
   * **[!UICONTROL X Häufigkeit]**: Zeigen Sie die Nachricht nur eine bestimmte Anzahl an Malen an, bestimmt durch den Wert, der in der Variablen **[!UICONTROL Anzeigezeiten]** -Feld.

1. Wählen Sie den Wochentag und den Zeitpunkt aus, zu dem Ihre In-App-Nachricht ausgelöst werden soll, und klicken Sie auf **[!UICONTROL Speichern]**.

1. Schließen Sie bei Bedarf Ihren Journey-Fluss ab, indem Sie zusätzliche Aktionen oder Ereignisse per Drag-and-Drop verschieben. [Weitere Informationen](../building-journeys/about-journey-activities.md)

1. Sobald Ihre In-App-Nachricht fertig ist, schließen Sie die Konfiguration ab und veröffentlichen Sie Ihre Journey, um sie zu aktivieren.

Weitere Informationen zur Konfiguration einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

## Einschränkungen bei In-App-Aktivitäten {#in-app-activity-limitations}

* Diese Funktion ist derzeit nicht für Kundinnen und Kunden im Gesundheitswesen verfügbar.

* Personalisierung kann nur Profilattribute enthalten.

* Die In-App-Anzeige ist an die Journey-Lebensdauer gebunden, d. h. wenn die Journey für ein Profil endet, werden alle In-App-Nachrichten innerhalb dieser Journey nicht mehr für dieses Profil angezeigt.  Daher ist es nicht möglich, eine In-App-Nachricht direkt von einer Journey-Aktivität aus zu stoppen. Stattdessen müssen Sie die gesamte Journey beenden, um zu verhindern, dass die In-App-Nachrichten dem Profil angezeigt werden.

* Im Testmodus hängt die Anzeige der App von der Journey-Lebensdauer ab. Um zu verhindern, dass die Journey während des Tests zu früh endet, passen Sie den **[!UICONTROL Wartezeit]**-Wert für Ihre **[!UICONTROL Warten]**-Aktivitäten an.

* **[!UICONTROL Reaktion]**-Aktivitäten können nicht verwendet werden, um auf ein Öffnen oder Klicken in der App zu reagieren.

* Eine Aktivierungsverzögerung kann zwischen dem Zeitpunkt, zu dem ein Benutzerprofil eine In-App-Aktivität auf der Arbeitsfläche erreicht, und dem Zeitpunkt auftreten, zu dem es diese In-App-Nachricht zu sehen beginnt.

## In-App-Bericht {#inapp-report}

Von Ihrer Journey **[!UICONTROL Gesamtbericht]**, die **[!UICONTROL In-App]** im Tab werden die wichtigsten Informationen zu den in Ihren Journey gesendeten In-App-Sendungen aufgeführt.

Weitere Informationen [Journey globaler Bericht](../reports/journey-global-report.md).

![](assets/in-app-journey-report.png)

+++Erfahren Sie mehr über die verschiedenen Metriken und Widgets, die für den In-App-Bericht verfügbar sind.

Die KPIs der **[!UICONTROL In-App-Leistung]** geben die wichtigsten Informationen bezüglich der Interaktion Ihrer Besucher mit Ihren In-App-Nachrichten an, z. B.:

* **[!UICONTROL Eindeutige Impressions]**: Anzahl der eindeutigen Nutzer, an die die In-App-Nachricht gesendet wurde.

* **[!UICONTROL Impressions]**: Gesamtzahl der an alle Benutzer gesendeten In-App-Nachrichten.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.

* **[!UICONTROL Abweisungsrate]**: Prozentsatz der In-App-Nachrichten, die von Empfängern abgewiesen wurden.

Das Diagramm **[!UICONTROL In-App-Zusammenfassung]** zeigt die Entwicklung Ihrer In-App-Impressions für den betroffenen Zeitraum an.

Die **[!UICONTROL Klicks nach Schaltfläche]** Diagramme und Tabellen enthalten die verfügbaren Daten für das Empfängerverhalten pro Schaltfläche:

* **[!UICONTROL Klicks]**: Gesamtzahl der Empfänger, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben.

* **[!UICONTROL Klickrate]**: Prozentualer Anteil der Benutzer, die mit den in der In-App-Nachricht enthaltenen Schaltflächen interagiert haben, im Verhältnis zur Zahl der Benutzer, die die Nachricht gesehen haben.
+++

**Verwandte Themen:**

* [Entwerfen der In-App-Nachricht](design-in-app.md)
* [Testen und Senden der In-App-Nachricht](send-in-app.md)
* [In-App-Bericht](../reports/campaign-global-report.md#inapp-report)
* [In-App-Konfiguration](inapp-configuration.md)
