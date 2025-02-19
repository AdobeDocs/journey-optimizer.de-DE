---
title: Leitplanken und Einschränkungen beim Entscheidungs-Management
description: Erfahren Sie mehr über Leitplanken und Einschränkungen beim Entscheidungs-Management.
feature: Decisioning
role: User
level: Intermediate
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 16%

---


# Leitplanken und Einschränkungen beim Entscheidungs-Management {#decision-management-guardrails}

Beachten Sie die folgenden Leitplanken und Einschränkungen, um eine optimale Nutzung des Entscheidungs-Managements sicherzustellen.

Die vollständige Liste der [!DNL Journey Optimizer] und Einschränkungen finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen

Der Versanddurchsatz entspricht der Anzahl der Entscheidungsantworten, die vom Entscheidungs-Management-App-Service in einer bestimmten Zeit bereitgestellt werden können.

| Leitplanke | Limit |
| ------- | ------- |
| Decisioning-API-Anfragen pro Sekunde | 500 |
| Edge Decisioning-API-Anfragen pro Sekunde mit Edge-Segmentierung | 1500 |
| Edge Decisioning-API-Anfragen pro Sekunde ohne Edge-Segmentierung | 5.000 |
| Pro Antwort zurückgegebene Angebote | Bis zu 30 pro Entscheidungsumfang oder insgesamt 100 |
| Maximale Anzahl an beteiligten Angebotsregeln pro Anfrage | 100 |

## Entscheidungen

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungen insgesamt | 10 K |
| Live-Entscheidungen | 1K |
| Platzierungen pro Entscheidung | 30 |

## Sammlungen

| Leitplanke | Limit |
| ------- | ------- |
| Angebote pro Sammlung | 500 |
| Sammlungen | 10 K |
| Sammlungen pro Entscheidung | 30 |

## Sammlungsqualifizierer

| Leitplanke | Limit |
| ------- | ------- |
| Sammlungskennzeichner pro Angebot oder Sammlung | 20 |
| Gesamtzahl der Sammlungskennzeichner | 1000 |

## Angebote

| Leitplanke | Limit |
| ------- | ------- |
| Angebote insgesamt | 10 K |
| Maximale Anzahl von **aktiven** Angeboten pro Sandbox | 10 K |
| Maximale Größe von Angeboten einschließlich Attributen (1 KB), maximal 30 Attribute | 1KB |
| Max. Größe der Angebotsdarstellung (insgesamt für alle Platzierungen) | 1KB |

## Eignungsregeln

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungsregeln und Rangfolgeformeln insgesamt | 10 K kombiniert |
| Maximale Anzahl von Profilattributen pro Regel | 25 |
| Maximale Anzahl von Kontextdatenattributen pro Regel | 30 |
| Maximale Größe der PQL-Regel | 15K (UTF-8) |
| Maximale Anzahl von Verschachtelungsebenen | 30 |

## Rangfolgeformeln

| Leitplanke | Limit |
| ------- | ------- |
| Maximale Größe der Rangfolgenformel PQL | 8 KB (UTF-8) |
| Maximale Anzahl an Profilattributen | 25 |
| Maximale Anzahl von Kontextdatenattributen | 30 |
| Maximale Anzahl von Verschachtelungsebenen | 30 |

## Sonstige

| Leitplanke | Limit |
| ------- | ------- |
| Platzierungen | 1000 |
| KI-Rangfolgemodell | 5 |
| Frequenzlimitierung : Maximale Anzahl von Begrenzungsregeln pro Angebot | 10 |
