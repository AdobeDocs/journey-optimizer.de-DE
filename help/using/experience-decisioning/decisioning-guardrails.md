---
title: Leitlinien und Einschränkungen für die Entscheidungsfindung
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für die Entscheidungsfindung.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 100%

---

# Leitlinien und Einschränkungen für die Entscheidungsfindung {#decisioning-guardrails}

Um eine optimale Nutzung der Entscheidungsfindung sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten.

Die vollständige Liste der Leitlinien und Einschränkungen für [!DNL Journey Optimizer] finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen {#decision-requests}

| Leitplanke | Limit |
| ------- | ------- |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die Edge-Segmentierung verwendet | 1.500 |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die keine Edge-Segmentierung verwendet | 5.000 |

## Elementsammlung {#item-collections}

| Leitplanke | Limit |
| ------- | ------- |
| Elementsammlungen | 10.000 |
| Angebotselemente insgesamt pro Elementsammlung | 500 |

## Entscheidungsrichtlinie {#decision-policy}

| Leitplanke | Limit |
| ------- | ------- |
| Anzahl der Auswahlstrategien und manuellen Elemente pro Entscheidungsrichtlinie | 10 |
| Maximale Anzahl der zurückgegebenen Angebotselemente pro Entscheidungsrichtlinie | 30 |

## Eignungsregeln {#eligibility-rules}

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungsregeln und Rangfolgeformeln insgesamt | 10.000 (zusammen) |
| Maximale Anzahl an Profilattributen pro Regel | 25 |
| Maximale Anzahl an Kontextdatenattributen pro Regel | 30 |
| Maximale Größe der PQL-Regel | 15.000 (UTF-8) |
| Maximale Anzahl an Verschachtelungsebenen | 30 |

## Rangfolgenformeln {#ranking-formulas}

| Leitplanke | Limit |
| ------- | ------- |
| Maximale Größe der Rangfolgeformel-PQL | 8.000 (UTF-8) |
| Maximale Anzahl an Profilattributen | 25 |
| Maximale Anzahl an Kontextdatenattributen | 30 |
| Maximale Anzahl an Verschachtelungsebenen | 30 |

## Sonstige {#others}

| Leitplanke | Limit |
| ------- | ------- |
| Anzahl der benutzerdefinierte Attribute pro Angebotskatalogschema | 100 |
| Angebotselemente insgesamt | 10.000 |
| Platzierungen insgesamt | 1.000 |
| KI-Rangfolgemodell | 5 |
| Häufigkeitsregeln: Maximale Anzahl der Begrenzungsregeln pro Angebot | 10 |
