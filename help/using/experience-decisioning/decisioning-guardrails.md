---
title: Leitplanken und Einschränkungen bei Entscheidungen
description: Weitere Informationen zu Leitplanken und Einschränkungen bei Entscheidungen.
feature: Decisioning
role: User
level: Intermediate
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 15%

---


# Leitplanken und Einschränkungen bei Entscheidungen {#decisioning-guardrails}

Um eine optimale Nutzung von Decisioning sicherzustellen, sollten Sie die folgenden Leitplanken und Einschränkungen beachten.

Die vollständige Liste der [!DNL Journey Optimizer] und Einschränkungen finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen

| Leitplanke | Limit |
| ------- | ------- |
| Code-basierte Erlebnis-API-Anfrage mit Entscheidungsrichtlinie, die Edge-Segmentierung verwendet | 1500 |
| Code-basierte Erlebnis-API-Anfrage mit Entscheidungsrichtlinie, die keine Edge-Segmentierung verwendet | 5.000 |

## Sammlungen von Elementen

| Leitplanke | Limit |
| ------- | ------- |
| Sammlungen von Elementen | 10 K |
| Gesamte Angebotselemente pro Artikelsammlung | 500 |

## Entscheidungsrichtlinie

| Leitplanke | Limit |
| ------- | ------- |
| Anzahl der Auswahlstrategien und manuellen Elemente pro Entscheidungsrichtlinie | 10 |
| Max. zurückgegebene Angebotselemente pro Entscheidungsrichtlinie | 30 |

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
| Anzahl benutzerdefinierter Attribute pro Angebotskatalogschema | 100 |
| Gesamtzahl der Angebotselemente | 10 K |
| Platzierungen insgesamt | 1K |
| KI-Rangfolgemodell | 5 |
| Häufigkeitsregeln - Maximale Anzahl von Begrenzungsregeln pro Angebot | 10 |
