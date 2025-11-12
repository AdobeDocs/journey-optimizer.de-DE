---
solution: Journey Optimizer
product: journey optimizer
title: Kampagnenbericht
description: Erfahren Sie, wie Sie Live-Aktivitätsdaten aus dem Kampagnenbericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 4%

---

# Live-Kampagnenbericht {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Sie können auf den Bericht Ihrer Live-Aktivitätskampagne zugreifen, indem Sie in Ihrer Kampagne auf **[!UICONTROL Berichte]** und dann auf **[!UICONTROL Alle Zeitberichte anzeigen]** klicken. [Weitere Informationen](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Versandstatistiken {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

Die Tabelle **[!UICONTROL Versandstatistiken]** bietet einen detaillierten Überblick über Schlüsselmetriken im Zusammenhang mit Ihren Live-Aktivitätskampagnen. Es werden wichtige Informationen wie die Größe der Zielgruppe und die Anzahl der erfolgreich zugestellten Push-Benachrichtigungen angezeigt, anhand derer Sie die Reichweite und Leistung Ihrer Live-Push-Benachrichtigungen insgesamt bewerten können.

+++ Weitere Informationen zu den Metriken „Versandstatistiken“

* **[!UICONTROL Ausgewählt]**: Gesamtzahl der während der Live-Aktivität ausgewählten Profile.

* **[!UICONTROL Sendet]**: Gesamtzahl der Push-Benachrichtigungen, die an Zielgruppenprofile gesendet wurden.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich an Geräte gesendeten Push-Benachrichtigungen im Verhältnis zur Gesamtzahl der Sendeversuche.

* **[!UICONTROL Fehler senden]**: Gesamtzahl der Push-Benachrichtigungen, die aufgrund von Fehlern (z. B. ungültige Token oder Verbindungsprobleme) nicht gesendet werden konnten.

* **[!UICONTROL Ausschlüsse senden]**: Anzahl der Profile, die von Adobe Journey Optimizer vom Versand ausgeschlossen wurden (z. B. aufgrund des Opt-out-Status oder von Eignungsregeln).

+++

## Lebenszyklus der Live-Aktivität {#lifecycle}

![](assets/activity-lifecycle.png)

Die **[!UICONTROL Live-Aktivitäts]** Lebenszyklus-Tabelle bietet einen umfassenden Überblick über den Fortschritt Ihrer Live-Aktivitäten im Zeitverlauf. Sie bietet Einblicke in wichtige Ereignisse, z. B. wann Aktivitäten gestartet, aktualisiert oder beendet werden, sodass Sie die Benutzerinteraktion und den gesamten Lebenszyklus Ihrer Live-Aktivitätskampagnen besser verstehen können.

+++ Weitere Informationen zu Lebenszyklusmetriken von Live-Aktivitäten

* **[!UICONTROL Remote-Starts]**: Anzahl der Live-Aktivitäten, die remote initiiert und normalerweise vom Server- oder Backend-System ausgelöst werden.

* **[!UICONTROL Lokale Starts]**: Anzahl der Live-Aktivitäten, die lokal auf dem Gerät eines Benutzers gestartet wurden und häufig auf Benutzerinteraktionen oder Client-seitige Trigger zurückzuführen sind.

**[!UICONTROL Updates]**: Gesamtzahl der an Geräte gesendeten Live-Aktivitätsaktualisierungen. Zu den Aktualisierungen gehören Statusänderungen, neue Inhalte oder Fortschrittsbenachrichtigungen.

**[!UICONTROL Endet]**: Anzahl der Live-Aktivitäten, die entweder automatisch nach Abschluss oder manuell über einen definierten Trigger oder eine Zeitüberschreitung beendet wurden.

**[!UICONTROL Gesamtanzahl]**: Gesamtsumme aller Live-Aktivitäts-Lebenszyklus-Ereignisse, einschließlich Starts, Aktualisierungen und Enden, die eine vollständige Messung des Live-Aktivitätsvolumens liefern.

+++

## Fehlergründe {#error-reasons}

![](assets/error-reasons-activity.png)

Die **[!UICONTROL Fehlergründe]**-Tabelle ermöglicht es Ihnen, die spezifischen Fehler zu identifizieren, die während des Sendevorgangs Ihrer Live-Aktivitäten aufgetreten sind, was eine gründliche Analyse aller aufgetretenen Probleme erleichtert.

## Gründe für Ausschluss {#excluded-reasons}

![](assets/excluded-activity.png)

Die **[!UICONTROL Ausschlussgründe]** zeigt visuell die verschiedenen Faktoren an, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass sie Ihre Live-Aktivität nicht erhalten können.
