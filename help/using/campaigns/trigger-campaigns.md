---
solution: Journey Optimizer
product: journey optimizer
title: Überprüfen und Aktivieren einer Kampagne
description: Überprüfen und Aktivieren von Kampagnen in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: Kampagne, Überprüfung, Validierung, Aktivierung, Aktivieren, Optimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 1d3638499a9e8261a5f1b09744b82642198a5d5d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 100%

---


# Ausführen einer Kampagne, die durch API ausgelöst wird {#execute}

Nachdem Ihre Kampagne aktiviert wurde, müssen Sie die generierte Beispiel-cURL-Anfrage abrufen und im API verwenden, um Ihre Payload zu erstellen und die Kampagne auszulösen.

## Wichtige Informationen {#must-read}

* **Start- und Enddatum einer Kampagne** – Wenn Sie bei der Erstellung der Kampagne ein bestimmtes Start- und/oder Enddatum konfiguriert haben, wird die Kampagne außerhalb dieses Zeitraums nicht ausgeführt und API-Aufrufe schlagen fehl.

* **Aufrufzeitüberschreitung** – Der Aufruf der REST-API zur Ausführung interaktiver Nachrichten hat einen Zeitüberschreitungswert von 60 Sekunden. Im Falle unerwarteter Zeitüberschreitungen gibt es jedoch interne erneute Zustellversuche, um den Versand zu gewährleisten.

## Auslösen der Kampagne {#trigger}

1. Öffnen Sie die Kampagne, kopieren Sie dann die Payload-Anfrage aus dem Abschnitt **[!UICONTROL cURL-Anfrage]** und fügen Sie diese ein. Diese Payload enthält nun alle Personalisierungsvariablen (Profil und Kontext), die in der Nachricht verwendet werden. Sie ist verfügbar, sobald die Kampagne aktiv ist.

   ![](assets/api-triggered-curl.png)

1. Verwenden Sie diese cURL-Anfrage in den APIs, um Ihre Payload zu erstellen und die Kampagne auszulösen. Weitere Informationen finden Sie in der [Dokumentation zur API für die Ausführung interaktiver Nachrichten](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   Beispiele für API-Aufrufe finden Sie auch auf [dieser Seite](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
