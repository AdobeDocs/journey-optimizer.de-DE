---
title: Leitlinien und Einschränkungen für die Entscheidungsfindung
description: Erfahren Sie mehr über Leitplanken und Einschränkungen bei Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 97%

---

# Leitlinien und Einschränkungen für die Entscheidungsfindung {#decisioning-guardrails}

Um eine optimale Nutzung der Entscheidungsfindung sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten.

Die vollständige Liste der Leitlinien und Einschränkungen für [!DNL Journey Optimizer] finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen

| Leitplanke | Limit |
| ------- | ------- |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die Edge-Segmentierung verwendet | 1.500 |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die keine Edge-Segmentierung verwendet | 5.000 |

## Elementsammlung

| Leitplanke | Limit |
| ------- | ------- |
| Elementsammlungen | 10.000 |
| Angebotselemente insgesamt pro Elementsammlung | 500 |

## Entscheidungsrichtlinie

| Leitplanke | Limit |
| ------- | ------- |
| Anzahl der Auswahlstrategien und manuellen Elemente pro Entscheidungsrichtlinie | 10 |
| Maximale Anzahl der zurückgegebenen Angebotselemente pro Entscheidungsrichtlinie | 30 |

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
| Anzahl der benutzerdefinierte Attribute pro Angebotskatalogschema | 100 |
| Angebotselemente insgesamt | 10.000 |
| Platzierungen insgesamt | 1.000 |
| KI-Rangfolgemodell | 5 |
| Häufigkeitsregeln: Maximale Anzahl der Begrenzungsregeln pro Angebot | 10 |
