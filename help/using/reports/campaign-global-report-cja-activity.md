---
solution: Journey Optimizer
product: journey optimizer
title: Kampagnenbericht
description: Informationen zum Verwenden von Daten zu Live-Aktivitäten aus dem Kampagnenbericht
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 58%

---

# Live-Kampagnenbericht {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Sie können auf Ihren Bericht zu Kampagnen mit Live-Aktivitäten zugreifen, indem Sie in Ihrer Kampagne auf die Schaltfläche **[!UICONTROL Berichte]** klicken und dann **[!UICONTROL Bericht für gesamte Zeit anzeigen]** auswählen. [Weitere Informationen](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Versandstatistiken {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

Die Tabelle **[!UICONTROL Versandstatistiken]** bietet einen detaillierten Überblick über Schlüsselmetriken im Zusammenhang mit Ihren Kampagnen mit Live-Aktivitäten. Es werden wichtige Informationen wie die Größe der Zielgruppe und die Anzahl der erfolgreich zugestellten Push-Benachrichtigungen angezeigt. So können Sie die Reichweite und Leistung Ihrer Live-Push-Benachrichtigungen insgesamt einschätzen.

+++ Weitere Informationen zu den Metriken „Versandstatistiken“

* **[!UICONTROL Zielgruppe]**: Anzahl der Profile, die sich für die Zielgruppe qualifiziert haben, bevor Ausschlüsse, Unterdrückungen oder Einverständnisentnahmen angewendet wurden.

* **[!UICONTROL Sendungen]**: Gesamtzahl der Push-Benachrichtigungen, bei denen versucht wurde, sie an Zielgruppenprofile zu senden.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich an Geräte gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der Sendeversuche.

* **[!UICONTROL Sendefehler]**: Gesamtzahl der Push-Benachrichtigungen, die aufgrund von Fehlern (z. B. ungültige Token oder Verbindungsprobleme) nicht gesendet werden konnten.

* **[!UICONTROL Sendeausschlüsse]**: Anzahl der Profile, die von Adobe Journey Optimizer vom Versand ausgeschlossen wurden (z. B. wegen Opt-out-Status oder Eignungsregeln).

+++

## Lebenszyklus der Live-Aktivität {#lifecycle}

Die Tabelle **[!UICONTROL Lebenszyklus der Live-Aktivität]** bietet einen umfassenden Überblick über den Fortschritt Ihrer Live-Aktivitäten im zeitlichen Verlauf. Sie liefert Einblicke in wichtige Ereignisse (z. B. wann Aktivitäten gestartet, aktualisiert oder beendet werden), sodass Sie die Benutzerinteraktion und den gesamten Lebenszyklus Ihrer Kampagnen mit Live-Aktivitäten besser verstehen können.

Das Reporting unterscheidet sich je nachdem, ob Sie Transaktions- oder Marketing-Kampagnen verwenden.

### Transaktions-Live-Aktivitäten

![](assets/activity-lifecycle.png)

Für eine Transaktionskampagne zeigt der Bericht Live-Kampagnenaktivitäten alle Lebenszyklus-Ereignisse an, einschließlich Remote-Starts, lokaler Starts, Aktualisierungen und Enden.

+++ Weitere Informationen zu Lebenszyklusmetriken von Live-Aktivitäten mit Transaktionskampagnen

* **[!UICONTROL Remote-Starts]**: Gesamtzahl der remote initiierten Live-Aktivitäten-Startereignisse, die normalerweise vom Server oder Back-End-Systemen ausgelöst werden.

* **[!UICONTROL Lokale Starts]**: Gesamtzahl der Startereignisse von Live-Aktivitäten, die lokal auf dem Gerät eines Benutzers initiiert wurden und häufig auf Benutzerinteraktion oder Client-seitige Trigger zurückzuführen sind.

* **[!UICONTROL Aktualisierungen]**: Gesamtzahl der an Geräte gesendeten Aktualisierungen von Live-Aktivitäten. Zu Aktualisierungen gehören Statusänderungen, neue Inhalte oder Fortschrittsbenachrichtigungen.

* **[!UICONTROL Ends]**: Gesamtzahl der an Geräte gesendeten Live-Aktivitäten-Endereignisse.

* **[!UICONTROL Gesamtanzahl]**: Gesamtzahl aller Lebenszyklusereignisse bei Live-Aktivitäten, einschließlich Starts, Aktualisierungen und Enden, die eine vollständige Messung des Live-Aktivitätsvolumens liefern.

+++

### Marketing-Live-Aktivitäten

![](assets/activity-lifecycle-broadcast.png)

Marketing-Kampagnen verwenden Live-Aktivitäten für Broadcast-Anwendungsfälle, bei denen Updates an mehrere Geräte gleichzeitig gesendet werden.

Bei iOS Live-Aktivitäten in Marketing-Kampagnen zeigt der Bericht nur **[!UICONTROL Fernstartereignisse]** und **[!UICONTROL Fernstartereignisse]** beim Start an. **[!UICONTROL Updates]** und **[!UICONTROL Ends]**-Ereignisse werden nicht verfolgt, da APNs Aktualisierungen an alle Geräte verteilen, ohne Feedback zu geben. Um **[!UICONTROL Updates]** und **[!UICONTROL Ends]**-Ereignisse anzuzeigen, verwenden Sie die Push-Benachrichtigungskonsole von [Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Weitere Informationen zu Lebenszyklusmetriken von Live-Aktivitäten mit Marketing-Kampagnen

* **[!UICONTROL Remote-Starts]**: Gesamtzahl der remote initiierten Live-Aktivitäten-Startereignisse, die normalerweise vom Server oder Back-End-Systemen ausgelöst werden.

* **[!UICONTROL Fehler beim Remotestart]**: Gesamtzahl der Fehler, die beim Versuch aufgetreten sind, Live-Aktivitäten remote zu starten (z. B. ungültige Token oder Verbindungsprobleme).

+++

## Fehlergründe {#error-reasons}

![](assets/error-reasons-activity.png)

Anhand der Tabelle **[!UICONTROL Fehlergründe]** können Sie die spezifischen Fehler identifizieren, die während des Sendevorgangs Ihrer Live-Aktivitäten aufgetreten sind. Dies ermöglicht eine gründliche Analyse aller aufgetretenen Probleme.

## Gründe für Ausschluss {#excluded-reasons}

![](assets/excluded-activity.png)

Die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigt visuell die verschiedenen Faktoren auf, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine Live-Aktivitäten von Ihnen erhalten konnten.
