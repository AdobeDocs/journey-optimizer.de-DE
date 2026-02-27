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
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 22%

---

# Live-Kampagnenbericht {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Sie können auf Ihren Bericht zu Kampagnen mit Live-Aktivitäten zugreifen, indem Sie in Ihrer Kampagne auf die Schaltfläche **[!UICONTROL Berichte]** klicken und dann **[!UICONTROL Bericht für gesamte Zeit anzeigen]** auswählen. [Weitere Informationen](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Versandstatistiken {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

Die Tabelle **[!UICONTROL Versandstatistiken]** bietet einen detaillierten Überblick über Schlüsselmetriken im Zusammenhang mit Ihrer Live-Aktivitätskampagne. Darin werden wichtige Informationen wie die Größe der Zielgruppe und die Anzahl der erfolgreich bereitgestellten Live-Aktivitäten angezeigt, anhand derer Sie die Reichweite und Leistung Ihrer Live-Aktivität insgesamt bewerten können.

+++ Weitere Informationen zu den Metriken „Versandstatistiken“

* **[!UICONTROL Zielgruppe]**: Anzahl der Profile, die sich für die Zielgruppe qualifiziert haben, bevor Ausschlüsse, Unterdrückungen oder Einverständnisentnahmen angewendet wurden.

* **[!UICONTROL Sendungen]**: Gesamtzahl der Live-Aktivitäten, die an Zielgruppenprofile gesendet wurden.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich an Geräte zugestellten Live-Aktivitäten im Verhältnis zur Gesamtzahl der Sendeversuche.

* **[!UICONTROL Fehler senden]**: Gesamtzahl der Live-Aktivitäten, die aufgrund von Fehlern (z. B. ungültige Token oder Verbindungsprobleme) nicht gesendet werden konnten.

* **[!UICONTROL Sendeausschlüsse]**: Anzahl der Profile, die von Adobe Journey Optimizer vom Versand ausgeschlossen wurden (z. B. wegen Opt-out-Status oder Eignungsregeln).

+++

## Lebenszyklus der Live-Aktivität {#lifecycle}

Die **[!UICONTROL Live-Aktivitäts]** Lebenszyklus-Tabelle bietet einen umfassenden Überblick über den Fortschritt Ihrer Live-Aktivität im Zeitverlauf. Sie bietet Einblicke in wichtige Ereignisse, z. B. wann eine Aktivität gestartet, aktualisiert oder beendet wird, sodass Sie die Benutzerinteraktion und den gesamten Lebenszyklus Ihrer Live-Aktivitätskampagne besser verstehen können.

Das Reporting unterscheidet sich je nachdem, ob Sie Transaktions- oder Marketing-Kampagnen verwenden.

### Transaktions-Live-Aktivität

![](assets/activity-lifecycle.png)

Für eine Transaktionskampagne zeigt der Bericht Live-Aktivitätskampagne alle Lebenszyklusereignisse an, einschließlich Remote-Starts, lokaler Starts, Aktualisierungen und Enden.

+++ Weitere Informationen zu Lebenszyklusmetriken von Live-Aktivitäten mit Transaktionskampagnen

* **[!UICONTROL Remote-Starts]**: Gesamtzahl der remote initiierten Live-Aktivitäts-Startereignisse, die normalerweise vom Server oder Back-End-Systemen ausgelöst werden.

* **[!UICONTROL Lokale Starts]**: Gesamtzahl der Live-Aktivitäts-Startereignisse, die lokal auf dem Gerät eines Benutzers initiiert wurden und häufig auf Benutzerinteraktion oder Client-seitige Trigger zurückzuführen sind.

* **[!UICONTROL Aktualisierungen]**: Gesamtzahl der an Geräte gesendeten Aktualisierungen von Live-Aktivitäten. Zu Aktualisierungen gehören Statusänderungen, neue Inhalte oder Fortschrittsbenachrichtigungen.

* **[!UICONTROL Ends]**: Gesamtzahl der an Geräte gesendeten Live-Aktivitätsendereignisse.

* **[!UICONTROL Gesamtanzahl]**: Gesamtzahl aller Lebenszyklusereignisse bei Live-Aktivitäten, einschließlich Starts, Aktualisierungen und Enden, die eine vollständige Messung des Live-Aktivitätsvolumens liefern.

+++

### Marketing-Live-Aktivität

![](assets/activity-lifecycle-broadcast.png)

Marketing-Kampagnen verwenden Live-Aktivitäten für Broadcast-Anwendungsfälle, bei denen Updates an mehrere Geräte gleichzeitig gesendet werden.

Bei iOS-Live-Aktivitäten in Marketing-Kampagnen zeigt der Bericht nur **[!UICONTROL Fernstartereignisse]** und **[!UICONTROL Fehler bei Fernstartereignissen]** am Start an. **[!UICONTROL Updates]** und **[!UICONTROL Ends]**-Ereignisse werden nicht verfolgt, da APNs Aktualisierungen an alle Geräte verteilen, ohne Feedback zu geben. Um **[!UICONTROL Updates]** und **[!UICONTROL Ends]**-Ereignisse anzuzeigen, verwenden Sie die Push-Benachrichtigungskonsole von [Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Weitere Informationen zu Lebenszyklusmetriken von Live-Aktivitäten mit Marketing-Kampagnen

* **[!UICONTROL Remote-Starts]**: Gesamtzahl der remote initiierten Live-Aktivitäts-Startereignisse, die normalerweise vom Server oder Back-End-Systemen ausgelöst werden.

* **[!UICONTROL Fehler beim Remotestart]**: Gesamtzahl der Fehler, die beim Versuch aufgetreten sind, die Live-Aktivität remote zu starten (z. B. ungültige Token oder Verbindungsprobleme).

+++

#### Abrufen von Aktualisierungen und Endzahlen über API {#retrieving-updates-end-api}

Als Alternative zur Verwendung der Push-Benachrichtigungskonsole von Apple können Aktualisierungen und Endzahlen über Headless-API-Aufrufe abgerufen werden.

Beim Ausführen von Aktualisierungs- oder End-API-Aufrufen für Broadcast-Anwendungsfälle enthält die Antwort einen `controlBreakdown`-Abschnitt, der Zähler bereitstellt, die angeben, wie viele Aktualisierungs- und End-Aufrufe für die Ausführung der Live-Aktivität ausgeführt wurden. Dieser Block fehlt bei älteren Ausführungen ohne Lebenszyklusdaten. Der Ausführungsstatus kann bei Bedarf auch explizit mithilfe des GET-Endpunkts abgerufen werden.

**UPDATE/END-Antwort (200 OK)**

```json
{
  "executionId": "HA-exec-abc",
  "campaignId": "campaign-abc-123",
  "campaignVersionId": "v1",
  "audienceId": "audience-segment-id",
  "status": "processing",
  "targetedProfileCount": 150000,
  "createdAt": "2026-02-27T10:00:00Z",
  "executionLifecycle": {
    "lastControlAt": "2026-02-27T10:45:00Z",
    "controlBreakdown": {
      "update": 5,
      "end": 1
    }
  }
}
```

**Ausführungsstatus (GET)**

```
GET /im/executions/audience/{executionId}
```

## Fehlergründe {#error-reasons}

![](assets/error-reasons-activity.png)

Die **[!UICONTROL Fehlergründe]**-Tabelle ermöglicht es Ihnen, die spezifischen Fehler zu identifizieren, die während des Sendevorgangs Ihrer Live-Aktivität aufgetreten sind, was eine gründliche Analyse aller aufgetretenen Probleme erleichtert.

## Gründe für Ausschluss {#excluded-reasons}

![](assets/excluded-activity.png)

Die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigt visuell die verschiedenen Faktoren auf, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine Live-Aktivitäten von Ihnen erhalten konnten.
