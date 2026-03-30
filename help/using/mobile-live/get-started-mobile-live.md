---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Live-Aktivitäten
description: Informationen zum Senden von Live-Aktivitäten in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: c6b36f31af29d21053cc455fd5dbba68ed5af63b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 20%

---

# Erste Schritte mit Live-Aktivitäten {#get-started-mobile-live}


Live-Aktivitäten sind beständige, überprüfbare Benutzeroberflächenelemente, die auf dem Bildschirm „Gerätesperre“ angezeigt werden. Sie ermöglichen es Ihrer Mobile App, aktuelle Informationen in Echtzeit zu präsentieren und halten Benutzer während eines laufenden Ereignisses auf dem Laufenden, ohne dass sie die Mobile App öffnen oder wiederholte Push-Benachrichtigungen erhalten müssen.

>[!AVAILABILITY]
>
>Live-Aktivitäten in Adobe Journey Optimizer sind nur mit Apple iOS kompatibel.

Im Gegensatz zu herkömmlichen Push-Benachrichtigungen stellen Live-Aktivitäten **statusbasierte Interaktion** dar: Statt einmalige Warnhinweise bereitzustellen, behalten sie eine kontinuierliche, kontextuelle Präsenz bei, die dynamisch aktualisiert wird, wenn sich Ereignisse entwickeln.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="iOS Live-Aktivitäten auf Lock Screen und Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Wichtigste Vorteile</strong></p>
<p>Live-Aktivitäten verlagern die mobile Interaktion von Benachrichtigungssystemen auf Statussysteme, sodass Marken folgende Möglichkeiten haben:</p>
<ul>
<li>Aufrechterhaltung <strong>kontinuierlichen Präsenz</strong> auf dem Sperrbildschirm während hochwertiger Ereignisse</li>
<li><strong>Informationen dynamisch aktualisieren</strong> ohne Benutzer mit wiederholten Benachrichtigungen zu überfordern</li>
<li>Bereitstellen <strong>reichhaltigeren, kontextuelleren</strong> mobilen Momenten, die mit realen Ereignissen verknüpft sind</li>
<li><strong>Steigerung von Interaktion und Kundenbindung</strong> während aktiver Transaktionen oder Live-Erlebnisse</li>
</ul>
</td>
</tr>
</table>

Mit Adobe Journey Optimizer können Sie Live **Aktivitäten programmgesteuert über API** ausgelöste Kampagnen remote starten **aktualisieren** und **beenden**. Dabei werden sowohl individuelle als auch zielgruppenbasierte Anwendungsfälle im benötigten Umfang unterstützt.

Live-Aktivitäten können **nur** über **API-ausgelöste**-Kampagnen initiiert werden, sodass Sie benutzerdefinierte Payloads bereitstellen und die gesamte Personalisierung über Ihre eigene Payload durchführen können.
Der entsprechende Kampagnentyp **API-ausgelöst** muss auf der Grundlage des vorgesehenen Anwendungsfalls der Live-Aktivität ausgewählt werden:

* Wählen Sie **API-ausgelöstes Marketing** für Broadcast-Anwendungsfälle - zielgruppenbasierte Updates in großem Umfang gesendet:

   * Countdowns von Sportbewertungen und Live-Events
   * Flugstatusaktualisierungen für alle Passagiere einer Strecke
   * Gemeinsame Erlebnisse in einem Benutzersegment

* Wählen Sie **API-ausgelöste Transaktion** für einzelne Anwendungsfälle aus - 1:1 Echtzeit-Updates pro Benutzer:

   * Auftrags-Tracking und Versandfortschritt
   * Statusaktualisierungen zu Mitfahrgelegenheiten oder Diensten
   * Buchungs- und Terminbestätigungen in Echtzeit

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um Live-Aktivitäten in Ihrer Anwendung zu konfigurieren und zu implementieren:

1. **[Konfigurieren von Adobe Journey Optimizer](mobile-live-configuration.md)**

   Richten Sie Ihre Umgebung ein, indem Sie eine mobile Konfiguration erstellen.

1. **[Integrieren des Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integrieren Sie mit Adobe Experience Platform Mobile SDK, um dynamische Echtzeit-Aktualisierungen auf dem Sperrbildschirm und auf der Dynamic Island zu ermöglichen.

1. **[Erstellen einer Live-Aktivität in Journey Optimizer](create-mobile-live.md)**

   Verwenden Sie API-ausgelöste Kampagnen in Journey Optimizer, um Ihre Live-Aktivität zu starten.

1. **[Nachverfolgen von Kampagnen](../reports/campaign-global-report-cja-activity.md)**

   Beginnen Sie mit der Messung der Wirkung Ihrer Live-Aktivität mit integrierten Berichten.

## Anleitungsvideo

Erfahren Sie, wie Sie iOS Live-Aktivitäten mit Adobe Journey Optimizer konfigurieren, um umfangreiche Echtzeit-Updates auf dem iPhone-Sperrbildschirm und auf Dynamic Island zu liefern.

>[!VIDEO](https://video.tv.adobe.com/v/3479873/?captions=ger&learn=on)
