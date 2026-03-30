---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Live-Aktivitäten
description: Erfahren Sie, wie Sie Live-Aktivitäten in Journey Optimizer senden
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: df4183e15b2907bfb669e7e2e8eb88771627dcf4
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 21%

---

# Erste Schritte mit Live-Aktivitäten {#get-started-mobile-live}


Live-Aktivitäten sind beständige, überprüfbare Benutzeroberflächenelemente, die auf dem Bildschirm „Gerätesperre“ angezeigt werden. Sie ermöglichen es Ihrer Mobile App, aktuelle Informationen in Echtzeit zu präsentieren und halten Benutzer während eines laufenden Ereignisses auf dem Laufenden, ohne dass sie die Mobile App öffnen oder wiederholte Push-Benachrichtigungen erhalten müssen.

>[!AVAILABILITY]
>
>Live-Aktivität in Adobe Journey Optimizer ist nur mit Apple iOS kompatibel.

Im Gegensatz zu herkömmlichen Push-Benachrichtigungen stellen Live-Aktivitäten **statusbasierte Interaktion** dar: Statt einmalige Warnhinweise bereitzustellen, behalten sie eine kontinuierliche, kontextuelle Präsenz bei, die dynamisch aktualisiert wird, wenn sich Ereignisse entwickeln.


![](assets/do-not-localize/live-activity.jpeg){width="30%" align="left"}

Mit Adobe Journey Optimizer können Sie Live **Aktivitäten programmgesteuert über API** ausgelöste Kampagnen remote starten **aktualisieren** und **beenden**. Dabei werden sowohl individuelle als auch zielgruppenbasierte Anwendungsfälle im benötigten Umfang unterstützt.

Live-Aktivitäten können **nur** über **API-ausgelöste** Kampagnen initiiert werden, sodass Sie benutzerdefinierte Payloads bereitstellen und die gesamte Personalisierung über Ihre eigene Payload durchführen können.
Der entsprechende Kampagnentyp **API-ausgelöst** muss auf der Grundlage des vorgesehenen Anwendungsfalls der Live-Aktivität ausgewählt werden:

* Wählen Sie **API-ausgelöstes Marketing** für Broadcast-Anwendungsfälle - zielgruppenbasierte Updates in großem Umfang gesendet:

   * Countdowns von Sportbewertungen und Live-Events
   * Flugstatusaktualisierungen für alle Passagiere einer Strecke
   * Gemeinsame Erlebnisse in einem Benutzersegment

* Wählen Sie **API-ausgelöste Transaktion** für einzelne Anwendungsfälle aus - 1:1 Echtzeit-Updates pro Benutzer:

   * Auftrags-Tracking und Versandfortschritt
   * Statusaktualisierungen zu Mitfahrgelegenheiten oder Diensten
   * Buchungs- und Terminbestätigungen in Echtzeit

## Wichtigste Vorteile

Live-Aktivitäten verlagern die mobile Interaktion von Benachrichtigungssystemen auf Statussysteme, sodass Marken folgende Möglichkeiten haben:

* Aufrechterhaltung **kontinuierlichen Präsenz** auf dem Sperrbildschirm während hochwertiger Ereignisse
* **Informationen dynamisch aktualisieren** ohne Benutzer mit wiederholten Benachrichtigungen zu überfordern
* Bereitstellen **reichhaltigeren, kontextuelleren** mobilen Momenten, die mit realen Ereignissen verknüpft sind
* **Steigerung von Interaktion und Kundenbindung** während aktiver Transaktionen oder Live-Erlebnisse

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um die Live-Aktivität in Ihrer Anwendung zu konfigurieren und zu implementieren:

1. **[Konfigurieren von Adobe Journey Optimizer](mobile-live-configuration.md)**

   Richten Sie Ihre Umgebung ein, indem Sie eine mobile Konfiguration erstellen.

1. **[Integrieren des Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integrieren Sie mit Adobe Experience Platform Mobile SDK, um dynamische Echtzeit-Aktualisierungen auf dem Sperrbildschirm und auf der Dynamic Island zu ermöglichen.

1. **[Live-Aktivität in Journey Optimizer erstellen](create-mobile-live.md)**

   Verwenden Sie API-ausgelöste Kampagnen in Journey Optimizer, um Ihre Live-Aktivität zu starten.

1. **[Nachverfolgen von Kampagnen](../reports/campaign-global-report-cja-activity.md)**

   Beginnen Sie mit der Messung der Wirkung Ihrer Live-Aktivität mit integrierten Berichten.

## Anleitungsvideo

Erfahren Sie, wie Sie iOS Live-Aktivitäten mit Adobe Journey Optimizer konfigurieren, um umfangreiche Echtzeit-Updates auf dem iPhone-Sperrbildschirm und auf Dynamic Island zu liefern.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
