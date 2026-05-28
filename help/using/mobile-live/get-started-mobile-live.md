---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Live-Aktivitäten
description: Informationen zum Senden von Live-Aktivitäten in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 100%

---

# Erste Schritte mit Live-Aktivitäten {#get-started-mobile-live}


Live-Aktivitäten sind andauernde, übersichtliche Benutzeroberflächenelemente, die auf dem Sperrbildschirm des Geräts angezeigt werden. Sie ermöglichen es Ihrer App, aktuelle Informationen in Echtzeit zu liefern, und halten Benutzenden während eines stattfindenden Ereignisses auf dem Laufenden, ohne dass sie die App öffnen oder wiederholte Push-Benachrichtigungen erhalten müssen.

>[!AVAILABILITY]
>
>Live-Aktivitäten in Adobe Journey Optimizer sind nur mit Apple iOS kompatibel.

Im Gegensatz zu herkömmlichen Push-Benachrichtigungen stellen Live-Aktivitäten eine **statusbasierte Interaktion** dar: Statt einmalige Benachrichtigungen zu senden, werden sie kontinuierlich und kontextuell angezeigt sowie dynamisch aktualisiert, während Ereignisse stattfinden.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="iOS-Live-Aktivitäten auf Sperrbildschirm und Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Wichtigste Vorteile</strong></p>
<p>Live-Aktivitäten verlagern die mobile Interaktion von Benachrichtigungssystemen auf Statussysteme, sodass Marken folgende Möglichkeiten haben:</p>
<ul>
<li>Aufrechterhalten einer <strong>kontinuierlichen Anzeige</strong> auf dem Sperrbildschirm während hochwertiger Ereignisse</li>
<li><strong>Dynamisches Aktualisieren von Informationen</strong>, ohne Benutzende mit wiederholten Benachrichtigungen zu überfordern</li>
<li>Bereitstellen von <strong>umfassenderen, kontextuelleren</strong> mobilen Momenten, die mit realen Ereignissen verknüpft sind</li>
<li><strong>Steigern von Interaktion und Kundenbindung</strong> während aktiver Transaktionen oder Live-Erlebnisse</li>
</ul>
</td>
</tr>
</table>

Mit Adobe Journey Optimizer können Sie Live-Aktivitäten programmgesteuert über durch API ausgelöste Kampagnen aus der Ferne **starten**, **aktualisieren** und **beenden**. Dabei werden sowohl individuelle als auch zielgruppenbasierte Anwendungsfälle im benötigten Umfang unterstützt.

Live-Aktivitäten können **nur** über **durch API ausgelöste** Kampagnen initiiert werden, sodass Sie benutzerdefinierte Payloads bereitstellen und die gesamte Personalisierung über Ihre eigene Payload durchführen können.
Der entsprechende Typ einer **durch API ausgelösten** Kampagne muss auf der Grundlage des vorgesehenen Anwendungsfalls der Live-Aktivität ausgewählt werden:

* Wählen Sie **API-ausgelöst (Marketing)** für Broadcast-Anwendungsfälle aus – zielgruppenbasierte Updates werden im benötigten Umfang gesendet:

   * Sportergebnisse und Countdowns für Live-Veranstaltungen
   * Updates des Flugstatus für alle Passagierinnen und Passagiere einer Strecke
   * Gemeinsame Erlebnisse in einem Benutzersegment

* Wählen Sie **API-ausgelöst (Transaktion)** für individuelle Anwendungsfälle aus – 1:1-Echtzeit-Updates pro Person:

   * Auftrags-Tracking und Versandfortschritt
   * Status-Updates zu Mitfahrgelegenheiten oder Diensten
   * Buchungs- und Terminbestätigungen in Echtzeit

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um Live-Aktivitäten in Ihrer Anwendung zu konfigurieren und zu implementieren:

1. **[Konfigurieren von Adobe Journey Optimizer](mobile-live-configuration.md)**

   Richten Sie Ihre Umgebung ein, indem Sie eine mobile Konfiguration erstellen.

1. **[Integrieren des Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integrieren Sie mit Adobe Experience Platform Mobile SDK, um dynamische Echtzeit-Aktualisierungen auf dem Sperrbildschirm und auf der Dynamic Island zu ermöglichen.

1. **[Erstellen einer Live-Aktivität in Journey Optimizer](create-mobile-live.md)**

   Verwenden Sie durch API ausgelöste Kampagnen in Journey Optimizer, um Ihre Live-Aktivität zu starten.

1. **[Nachverfolgen von Kampagnen](../reports/campaign-global-report-cja-activity.md)**

   Messen Sie die Wirkung Ihrer Live-Aktivität mit integrierten Berichten.

## Anleitungsvideo

Erfahren Sie, wie Sie iOS-Live-Aktivitäten mit Adobe Journey Optimizer konfigurieren, um umfangreiche Echtzeit-Updates auf dem iPhone-Sperrbildschirm und auf Dynamic Island bereitzustellen.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
