---
title: Leitlinien und Einschränkungen für die Entscheidungsfindung
description: Erfahren Sie mehr über die Leitlinien und Einschränkungen für die Entscheidungsfindung.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: bb672c8eb917a29aaebc7134cc833c423c0ecc5c
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 19%

---

# Leitlinien und Einschränkungen für die Entscheidungsfindung {#decisioning-guardrails}

Um eine optimale Nutzung der Entscheidungsfindung sicherzustellen, sollten Sie die folgenden Leitlinien und Einschränkungen beachten.

Die vollständige Liste der Leitlinien und Einschränkungen für [!DNL Journey Optimizer] finden Sie in [diesem Abschnitt](../start/guardrails.md).

## Entscheidungsanfragen {#decision-requests}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Code-basierte Erlebnis-API-Anfrage mit Entscheidungsrichtlinie unter Verwendung der Edge-Segmentierung | 1 500 |
|| Code-basierte Erlebnis-API-Anfrage mit Entscheidungsrichtlinie, die keine Edge-Segmentierung verwendet | 5 000 |
|| Maximale Anzahl von Oberflächen-URIs pro Edge-Entscheidungsanfrage | 30 |

## Elementsammlung {#item-collections}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Sammlungen von Elementen | 10 K |
|| Gesamte Angebotselemente pro Artikelsammlung | 500 |

## Entscheidungsrichtlinie {#decision-policy}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Anzahl der Auswahlstrategien und manuellen Elemente pro Entscheidungsrichtlinie | 10 |
|| Max. zurückgegebene Angebotselemente pro Entscheidungsrichtlinie | 30 |

## Eignungsregeln {#eligibility-rules}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Entscheidungsregeln und Rangfolgeformeln insgesamt | 10 K kombiniert |
|| Maximale Anzahl von Profilattributen pro Regel | 25 |
|| Maximale Anzahl von Kontextdatenattributen pro Regel | 30 |
|| Maximale Größe der PQL-Regel | 15K (UTF-8) |
|| Maximale Anzahl von Verschachtelungsebenen | 30 |

## Rangfolgenformeln {#ranking-formulas}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Maximale Größe der Rangfolgenformel PQL | 8 KB (UTF-8) |
|| Maximale Anzahl an Profilattributen |25 |
|| Maximale Anzahl von Kontextdatenattributen | 30 |
|| Maximale Anzahl von Verschachtelungsebenen | 30 |

## Sonstige {#others}

|| Leitplanke | Grenze |
|| ------- | ------- |
|| Anzahl benutzerdefinierter Attribute pro Angebotskatalogschema | 100 |
|| Gesamtzahl der Angebotselemente | 10 K |
|| Platzierungen insgesamt | 1K |
|| KI-Rangfolgemodell | 5 |
|| Häufigkeitsregeln - Maximale Anzahl von Begrenzungsregeln pro Angebot | 10 |

## Konfigurationen  {#configurations}

Die Gesamtzahl der von Decisioning unterstützten Konfigurationen darf 20.000 nicht überschreiten.

Die Gesamtzahl der Konfigurationen entspricht der Gesamtzahl der [Begrenzungsregeln](items.md#capping) die in Ihrer Sandbox vorhanden sind.
