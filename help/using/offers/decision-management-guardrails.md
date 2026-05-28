---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Leitlinien und Einschränkungen für das Entscheidungs-Management
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für das Entscheidungs-Management.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/teZQ3GKXJoj05ZD7bCCzKSzwLdUbgF8DXp8csDostOw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 83%

---

# Leitlinien und Einschränkungen für das Entscheidungs-Management {#decision-management-guardrails}

>[!IMPORTANT]
>
>Auf dieser Seite werden Leitplanken für die alte Funktion **Entscheidungs-Management** behandelt. Wenn Sie **Decisioning** verwenden - [!DNL Adobe Journey Optimizer] aktuelle Entscheidungsfunktion, die über Code-basierte Erlebnis- und E-Mail-Kanäle verfügbar ist -, lesen Sie stattdessen [Entscheidungs-Leitplanken und -](../experience-decisioning/decisioning-guardrails.md) .
>
>Sie sind sich nicht sicher, welche Funktion Sie verwenden? [Erfahren Sie mehr über &#x200B;](../experience-decisioning/gs-experience-decisioning.md).

Diese Seite gilt für Benutzer, die noch mit dem alten Entscheidungs-Management-System arbeiten. Beachten Sie für eine optimale Nutzung die folgenden Leitplanken und Einschränkungen.

Die vollständige Liste der Leitlinien und Einschränkungen für [!DNL Journey Optimizer] finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen

Der Versanddurchsatz entspricht der Anzahl der Entscheidungsantworten, die vom Entscheidungs-Management-App-Dienst innerhalb einer bestimmten Zeit bereitgestellt werden können.

| Leitplanke | Limit |
| ------- | ------- |
| Decisioning-API-Anfragen pro Sekunde | 500 pro Organisation |
| Edge Decisioning-API-Anfragen pro Sekunde mit Edge-Segmentierung | 1.500 pro Organisation |
| Edge Decisioning-API-Anfragen pro Sekunde ohne Edge-Segmentierung | 5.000 pro Organisation |
| Pro Antwort zurückgegebene Angebote | Bis zu 30 pro Entscheidungsumfang oder insgesamt 100 |
| Maximale Anzahl der pro Anfrage beteiligten Angebotsregeln | 100 |

## Entscheidungen

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungen insgesamt | 10.000 |
| Live-Entscheidungen | 1.000 |
| Platzierungen pro Entscheidung | 30 |

## Sammlungen

| Leitplanke | Limit |
| ------- | ------- |
| Angebote pro Sammlung | 500 |
| Sammlungen | 10.000 |
| Sammlungen pro Entscheidung | 30 |

## Sammlungsqualifizierer

| Leitplanke | Limit |
| ------- | ------- |
| Sammlungsqualifizierer pro Angebot oder Sammlung | 20 |
| Sammlungsqualifizierer insgesamt | 1.000 |

## Angebote

| Leitplanke | Limit |
| ------- | ------- |
| Angebote insgesamt | 10.000 |
| Maximale Anzahl der **aktiven** Angebote pro Sandbox | 10.000 |
| Maximale Größe der Angebote einschließlich Attributen (1 KB), maximal 30 Attribute | 1 KB |
| Maximale Größe der Angebotsdarstellung (insgesamt für alle Platzierungen) | 1 KB |

## Eignungsregeln

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungsregeln und Rangfolgeformeln insgesamt | 10.000 (zusammen) |
| Maximale Anzahl an Profilattributen pro Regel | 25 |
| Maximale Anzahl an Kontextdatenattributen pro Regel | 30 |
| Maximale Größe der PQL-Regel | 15.000 (UTF-8) |
| Maximale Anzahl an Verschachtelungsebenen | 30 |

## Rangfolgenformeln

| Leitplanke | Limit |
| ------- | ------- |
| Maximale Größe der Rangfolgeformel-PQL | 8.000 (UTF-8) |
| Maximale Anzahl an Profilattributen | 25 |
| Maximale Anzahl an Kontextdatenattributen | 30 |
| Maximale Anzahl an Verschachtelungsebenen | 30 |

## Sonstige

| Leitplanke | Limit |
| ------- | ------- |
| Platzierungen | 1.000 |
| KI-Rangfolgemodell | 5 |
| Frequenzbegrenzung: Maximale Anzahl an Begrenzungsregeln pro Angebot | 10 |

## Konfigurationen {#configurations}

Die Gesamtzahl der Konfigurationen, die vom Entscheidungs-Management unterstützt werden, darf 20.000 nicht überschreiten.

Die Gesamtzahl der Konfigurationen entspricht der Gesamtzahl der [Begrenzungsregeln](offer-library/add-constraints.md#capping) die in Ihrer Sandbox vorhanden sind. Für jede Begrenzungsregel, die auf alle [Platzierungen](offer-library/creating-placements.md) angewendet wird, muss die Regel auf alle Platzierungen multipliziert werden, die mit dem angegebenen Angebot verknüpft sind.
