---
title: Leitlinien und Einschränkungen für das Entscheidungs-Management
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für das Entscheidungs-Management.
badge: label="Veraltet" type="Informative"
feature: Decisioning
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 99%

---

# Leitlinien und Einschränkungen für das Entscheidungs-Management {#decision-management-guardrails}

Um eine optimale Nutzung des Entscheidungs-Managements sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten.

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

## Rangfolgeformeln

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
