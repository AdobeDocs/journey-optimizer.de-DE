---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Live-Aktivitäten
description: Informationen zum Senden von Live-Aktivitäten in Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%

---

# Erste Schritte mit Live-Aktivitäten {#get-started-mobile-live}

>[!AVAILABILITY]
>
>Live-Aktivitäten in Journey Optimizer sind nur mit iOS kompatibel.

Live-Aktivitäten bieten Echtzeit-Aktualisierungen und interaktive Erlebnisse in Apps, sodass Benutzende direkt auf dem Bildschirm ihres Geräts über laufende Ereignisse oder Aufgaben auf dem neuesten Stand bleiben können.

Diese Funktion verbessert die Interaktion, indem Live-Informationen wie Fortschritts-Tracking, Ereignisaktualisierungen oder interaktive Inhalte bereitgestellt werden, ohne dass Benutzende die App öffnen müssen.

Live-Aktivitäten können **nur** über **durch API ausgelöste** Kampagnen initiiert werden, sodass Sie benutzerdefinierte Payloads bereitstellen und die gesamte Personalisierung über Ihre eigene Payload durchführen können.
Der entsprechende Typ einer **durch API ausgelösten** Kampagne muss auf der Grundlage des vorgesehenen Anwendungsfalls der Live-Aktivität ausgewählt werden:

* Wählen Sie **API-ausgelöst (Marketing)** für zielgruppenbasierte Kampagnen aus.

  Konzipiert für auf Zielgruppen oder Segmenten basierte Kommunikation, bei der dieselbe Aktualisierung an mehrere Benutzende gesendet wird, z. B. Sportergebnisse, Ereignisaktualisierungen, gemeinsame Erlebnisse.

* Wählen Sie **API-ausgelöst (Transaktion)** für einzelne Kampagnen aus.

  Vorgesehene einzelne Benutzende, die durch ihr Profil identifiziert werden, z. B. Bestellstatus, Versand-Tracking.

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um Live-Aktivitäten in Ihrer Anwendung zu konfigurieren und zu implementieren:

1. **[Konfigurieren von Adobe Journey Optimizer](mobile-live-configuration.md)**

   Richten Sie Ihre Umgebung ein, indem Sie eine mobile Konfiguration erstellen.

1. **[Integrieren des Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   Integrieren Sie mit Adobe Experience Platform Mobile SDK, um dynamische Echtzeit-Aktualisierungen auf dem Sperrbildschirm und auf der Dynamic Island zu ermöglichen.

1. **[Erstellen von Live-Aktivitäten in Journey Optimizer](create-mobile-live.md)**

   Verwenden Sie durch API ausgelöste Kampagnen in Journey Optimizer, um Ihre Live-Aktivitäten zu starten.

1. **[Nachverfolgen von Kampagnen](../reports/campaign-global-report-cja-activity.md)**

   Messen Sie die Wirkung Ihrer Live-Aktivitäten mit integrierten Berichten. 
