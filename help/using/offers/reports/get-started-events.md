---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Arbeiten mit Entscheidungs-Management-Ereignissen
description: Erfahren Sie, wie Sie Entscheidungs-Management-Berichte in Adobe Experience Platform erstellen.
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# Erste Schritte mit Entscheidungs-Management-Ereignissen {#monitor-offer-events}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Jedes Mal, wenn das Entscheidungs-Management eine Entscheidung für ein bestimmtes Profil trifft, werden Informationen zu diesen Ereignissen automatisch an Adobe Experience Platform gesendet.

Auf diese Weise erhalten Sie Einblicke in Ihre Entscheidungen, z. B. in das Angebot, das einem bestimmten Profil unterbreitet wurde. Sie können diese Daten exportieren, um sie in Ihrem eigenen Berichtssystem zu analysieren, oder nutzen Sie Adobe Experience Platform [Abfrage-Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=de) in Kombination mit anderen Tools für erweiterte Analyse- und Berichtszwecke.

## Wichtige Informationen in Datensätzen {#key-information}

Jedes Ereignis, das gesendet wird, wenn eine Entscheidung getroffen wird, enthält vier wichtige Datenpunkte, die Sie für Analyse- und Reporting-Zwecke nutzen können:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Name und ID des Fallback-Angebots, wenn kein personalisiertes Angebot ausgewählt wurde,
* **[!UICONTROL Placement]**: Name, ID und Kanal der Platzierung, über die das Angebot gesendet wird,
* **[!UICONTROL Selections]**: Name und ID des für das Profil ausgewählten Angebots,
* **[!UICONTROL Aktivität]**: Name und ID der Entscheidung.

Zusätzlich können Sie auch die Felder **[!UICONTROL identityMap]** und **[!UICONTROL Timestamp]** nutzen, um Informationen über das Profil und den Zeitpunkt, zu dem das Angebot zugestellt wurde, abzurufen.

Weitere Informationen zu allen XDM-Feldern, die mit jeder Entscheidung gesendet werden, finden Sie in [diesem Abschnitt](xdm-fields.md).

## Zugriff auf Datensätze {#access-datasets}

Die Datensätze, die Entscheidungs-Management-Ereignisse enthalten, sind über das Menü **[!UICONTROL Datensätze]** in Adobe Experience Platform zugänglich. Für jede Ihrer Instanzen wird bei der Bereitstellung automatisch ein Datensatz erstellt.

![](../assets/events-datasets-list.png)

Diese Datensätze basieren auf dem **[!UICONTROL ODE DecisionEvents]**-Schema, das alle XDM-Felder enthält, die erforderlich sind, um Informationen des Entscheidungs-Managements an Adobe Experience Platform zu senden.

>[!NOTE]
>
>Beachten Sie, dass es sich bei ODE DecisionEvents-Datensätzen um **Nicht-Profil-Datensätze** handelt, d. h. sie können nicht in Experience Platform aufgenommen werden, um vom Echtzeit-Kundenprofil verwendet zu werden.
