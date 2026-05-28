---
title: Leitlinien und Einschränkungen für die Entscheidungsfindung
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für die Entscheidungsfindung.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/oTljriepwffzR-LIAc2kWjTQx9Oj0QMgJpbghkSEsmY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: d4ea4f32486c74b97e4a8d6ddd29e98c75fba060
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 79%

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
| Maximale Anzahl von AEM-Inhaltsfragmenten pro Entscheidungselement | 5 |

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
| Max. Entscheidungsrichtlinien pro E-Mail | 10 |

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

## Konfigurationen {#configurations}

Die Gesamtzahl der von der Entscheidungsfindung unterstützten Konfigurationen darf 20.000 nicht überschreiten.

Die Gesamtzahl der Konfigurationen entspricht der Gesamtzahl der [Begrenzungsregeln](items.md#capping), die in Ihrer Sandbox vorhanden sind.
