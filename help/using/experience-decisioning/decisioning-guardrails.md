---
title: Leitlinien und Einschränkungen für die Entscheidungsfindung
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für die Entscheidungsfindung.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
source-git-commit: 5be6ecd85b0b45e01f7a27e0ffc55a2c6a22bcea
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 83%

---

# Leitlinien und Einschränkungen für die Entscheidungsfindung {#decisioning-guardrails}

Um eine optimale Nutzung der Entscheidungsfindung sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten.

Die vollständige Liste der Leitlinien und Einschränkungen für [!DNL Journey Optimizer] finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen {#decision-requests}

| Leitplanke | Limit |
| ------- | ------- |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die Edge-Segmentierung verwendet | 1.500 |
| API-Anfrage „Code-basiertes Erlebnis“ mit Entscheidungsrichtlinie, die keine Edge-Segmentierung verwendet | 5.000 |
| Maximale Anzahl von Oberflächen-URIs pro Edge-Entscheidungsanfrage | 30 |

## Entscheidungselemente {#decision-items}

| Leitplanke | Limit |
| ------- | ------- |
| Entscheidungselemente insgesamt | 10.000 |
| Maximale Größe von Elementen, einschließlich Attributen (1 KB), max. 30 Attribute | 1 KB |
| Häufigkeitsregeln - Maximale Anzahl von Begrenzungsregeln pro Entscheidungselement | 10 |

## Elementsammlung {#item-collections}

| Leitplanke | Limit |
| ------- | ------- |
| Elementsammlungen | 10.000 |
| Gesamtzahl der Entscheidungselemente pro Sammlung | 500 |

## Entscheidungsrichtlinie {#decision-policy}

| Leitplanke | Limit |
| ------- | ------- |
| Anzahl der Auswahlstrategien und manuellen Elemente pro Entscheidungsrichtlinie | 10 |
| Max. zurückgegebene Entscheidungselemente pro Entscheidungsrichtlinie | 30 |

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
| Anzahl benutzerdefinierter Attribute pro Elementkatalogschema | 100 |
| Platzierungen insgesamt | 1.000 |
| KI-Rangfolgemodell | 5 |

## Konfigurationen  {#configurations}

Die Gesamtzahl der von der Entscheidungsfindung unterstützten Konfigurationen darf 20.000 nicht überschreiten.

Die Gesamtzahl der Konfigurationen entspricht der Gesamtzahl der [Begrenzungsregeln](items.md#capping), die in Ihrer Sandbox vorhanden sind.
