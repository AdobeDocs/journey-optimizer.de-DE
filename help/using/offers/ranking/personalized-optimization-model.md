---
product: experience platform
solution: Experience Platform
title: Modell zur personalisierten Optimierung
description: Erfahren Sie mehr über Modelle zur personalisierten Optimierung
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: f2174848c70610fc543ea9ddf766f0f7e579053a
workflow-type: ht
source-wordcount: '781'
ht-degree: 100%

---

# Modell zur personalisierten Optimierung {#personalized-optimization-model}

## Übersicht {#overview}

Durch die Nutzung modernster Technologien im Bereich des überwachten maschinellen Lernens und des Deep Learning ermöglicht es die automatische Personalisierung einem Business-Anwendenden (Marketer), Geschäftsziele zu definieren und seine Kundendaten zu nutzen, um geschäftsorientierte Modelle zu trainieren, um personalisierte Angebote zu unterbreiten und KPI zu optimieren.

## Grundlegende Modellannahmen und -beschränkungen {#key}

Um die Vorteile der automatischen Personalisierung optimal nutzen zu können, müssen einige wichtige Voraussetzungen und Beschränkungen beachtet werden.

* **Die Angebote sind so unterschiedlich, dass auch die Präferenzen der Benutzenden bezüglich der in Frage kommenden Angebote unterschiedlich sind**. Wenn die Angebote zu ähnlich sind, hat das resultierende Modell weniger Wirkung, da die Reaktionen scheinbar zufällig sind.
Wenn eine Bank beispielsweise zwei Kreditkarten anbietet, deren einziger Unterschied die Farbe ist, hat die Empfehlung einer Karte weniger Auswirkung. Wenn aber an jede Karte unterschiedliche Bedingungen geknüpft sind, haben Kunden und Kundinnen einen bestimmten Grund, warum sie sich für eine der Karten entscheiden. Dies bietet deshalb einen ausreichenden Unterschied zwischen den Angeboten, sodass ein wirkungsvolleres Modell erstellt werden kann.
* **Die Zusammensetzung des Traffics von Benutzenden ist stabil**. Wenn sich die Zusammensetzung des Benutzenden-Traffics während des Trainings der Modelle und der Vorhersagephase drastisch ändert, kann sich die Modellleistung verschlechtern. Angenommen, in der Trainings-Phase des Modells sind nur Daten für Benutzende in Zielgruppe A verfügbar, aber das trainierte Modell wird verwendet, um Prognosen für Benutzende in Zielgruppe B zu generieren. In diesem Fall kann die Modellleistung beeinträchtigt werden.
* **Die Leistungen der Angebote ändern sich innerhalb eines kurzen Zeitraums nicht dramatisch**, da dieses Modell wöchentlich aktualisiert wird und die Leistungsänderungen mit der Aktualisierung des Modells übermittelt werden. Ein Beispiel: Ein Produkt war früher sehr beliebt, aber in einem öffentlichen Bericht wird festgestellt, dass das Produkt gesundheitsschädlich ist, und das Produkt wird sehr schnell unpopulär. In diesem Szenario könnte das Modell dieses Produkt so lange empfehlen, bis das Modell aufgrund von Verhaltensänderungen der Benutzenden aktualisiert wird.

## Funktionsweise {#how}

Das Modell lernt komplexe Wechselwirkungen zwischen Angeboten, Informationen über Benutzende und kontextuelle Informationen, um Endbenutzenden personalisierte Angebote zu empfehlen. Funktionen werden durch Eingaben in das Modell verfügbar.

Es gibt drei Arten von Funktionen:

| Funktionstypen | Hinzufügen von Funktionen zu Modellen |
|--------------|----------------------------|
| Entscheidungs-Objekte (placementID, activityID, decisionScopeID) | Teil der Feedback-Erlebnisereignisse aus dem Entscheidungs-Management, die an AEP gesendet werden |
| Zielgruppen | Bis zu 50 Zielgruppen können beim Erstellen des KI-Rangfolgenmodells als Funktionen hinzugefügt werden |
| Kontextdaten | Teil der Feedback-Erlebnisereignisse aus dem Decisioning, die an AEP gesendet werden. Verfügbare Kontextdaten zum Hinzufügen zum Schema: Details zu Commerce, Kanal, Anwendung, Web, Umgebung und Gerät sowie placeContext |

Das Modell umfasst zwei Phasen:

* In der Phase des **Offline-Modelltrainings** wird ein Modell durch Erlernen und Speichern von in historischen Daten ersichtlichen Merkmalsinteraktionen trainiert.
* In der Phase der **Online-Schlussfolgerung** werden die Angebote auf der Grundlage der vom Modell in Echtzeit generierten Punktzahlen eingestuft. Im Gegensatz zu herkömmlichen kollaborativen Filtertechniken, bei denen es schwierig ist, Merkmale für Benutzende und Angebote einzubeziehen, ist die automatische Personalisierung eine auf Deep Learning basierende Empfehlungsmethode, die in der Lage ist, komplexe und nichtlineare Interaktionsmuster von Merkmalen einzubeziehen und zu lernen.

Hier ist ein vereinfachtes Beispiel, um die Grundidee der automatischen Personalisierung zu veranschaulichen. Nehmen wir an, wir haben einen Datensatz, in dem historische Interaktionen zwischen Benutzenden und Angeboten gespeichert sind, wie in Abbildung 1 dargestellt. Es gibt:
* Zwei Angebote, offer_1 und offer_2,
* Zwei Funktionen, Feature_1 und Feature_2,
* Eine Spalte mit der Reaktion.

Der Wert von feature_1, feature_2 und der Reaktion ist entweder 0 oder 1. Wenn wir uns die blauen und orangefarbenen Kästchen in Abbildung 1 ansehen, können wir feststellen, dass bei offer_1 die Reaktionen mit größerer Wahrscheinlichkeit 1 sind, wenn feature_1 und feature_2 die gleichen Werte haben, während bei offer_2 die Werte mit größerer Wahrscheinlichkeit 1 sind, wenn feature_1 0 ist und feature_2 1 ist. Wir können auch sehen, dass im roten Kästchen offer_1 bereitgestellt wird, wenn feature_1 gleich 0 und feature_2 gleich 1 ist, und die Reaktion gleich 0 ist. Ausgehend von dem Muster in den orangefarbenen Kästchen, wo feature_1 gleich 0 und feature_2 gleich 1 ist, ist offer_2 wahrscheinlich eine bessere Empfehlung.

Im Grunde werden hierbei frühere Merkmalsinteraktionen erlernt und gespeichert und danach angewendet, um personalisierte Vorhersagen zu generieren.

![](../assets/perso-ranking-schema.png)

## „Kaltstart“-Problem {#cold-start}

Das „Kaltstart“-Problem tritt auf, wenn es nicht genügend Daten gibt, um eine Empfehlung bereitzustellen. Bei der automatischen Personalisierung gibt es zwei Arten von „Kaltstart“-Problemen.

* **Nachdem ein neues KI-Modell ohne historische Daten erstellt wurde**, werden die Angebote über einen bestimmten Zeitraum nach dem Zufallsprinzip bereitgestellt, um Daten zu sammeln, die dann zum Trainieren des ersten Modells verwendet werden.
* **Nach der Freigabe des ersten Modells** werden 10 % des gesamten Traffics für die zufällige Bereitstellung von Angeboten verwendet, während 90 % des Traffics für Modellempfehlungen verwendet werden. Wenn also neue Angebote in das KI-Modell aufgenommen werden, würden sie als Teil der 10 % des Traffics bereitgestellt werden. Die zu diesen Angeboten gesammelten Daten würden dann im Zuge der weiteren Aktualisierung des Modells bestimmen, wie oft diese Angebote unter den 90 % des Traffics ausgewählt werden.

## Erneutes Training {#re-training}

Die Modelle werden wöchentlich neu trainiert, um die neuesten Interaktionen zwischen den Merkmalen zu erlernen und der Verschlechterung der Modellleistung entgegenzuwirken.
