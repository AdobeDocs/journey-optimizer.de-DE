---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Live-Aktivitäten
description: Erfahren Sie, wie Sie Live-Aktivitäten in Journey Optimizer senden
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 60%

---

# Erste Schritte mit Live-Aktivitäten {#get-started-mobile-live}

>[!AVAILABILITY]
>
>Live-Aktivitäten in Journey Optimizer sind nur mit iOS kompatibel.

Live-Aktivitäten bieten Echtzeit-Updates und interaktive Erlebnisse in mobilen Apps, sodass Benutzende direkt auf dem Bildschirm ihres Geräts über laufende Ereignisse oder Aufgaben auf dem Laufenden bleiben können.

Diese Funktion verbessert die Interaktion, indem Live-Informationen wie Fortschritts-Tracking, Ereignisaktualisierungen oder interaktive Inhalte bereitgestellt werden, ohne dass Benutzende die App öffnen müssen.

Live-Aktivitäten können **nur** über **API-ausgelöste** Kampagnen initiiert werden, sodass Sie benutzerdefinierte Payloads bereitstellen und die gesamte Personalisierung über Ihre eigene Payload durchführen können.
Der entsprechende Typ einer **durch API ausgelösten** Kampagne muss auf der Grundlage des vorgesehenen Anwendungsfalls der Live-Aktivität ausgewählt werden:

* Wählen Sie **API-ausgelöst (Marketing)** für zielgruppenbasierte Kampagnen aus.

  Konzipiert für auf Zielgruppen oder Segmenten basierte Kommunikation, bei der dieselbe Aktualisierung an mehrere Benutzende gesendet wird, z. B. Sportergebnisse, Ereignisaktualisierungen, gemeinsame Erlebnisse.

* Wählen Sie **API-ausgelöst (Transaktion)** für einzelne Kampagnen aus.

  Vorgesehene einzelne Benutzende, die durch ihr Profil identifiziert werden, z. B. Bestellstatus, Versand-Tracking.

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
