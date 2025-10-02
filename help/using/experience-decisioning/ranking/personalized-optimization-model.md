---
product: experience platform
solution: Experience Platform
title: Modell zur personalisierten Optimierung
description: Erfahren Sie mehr über Modelle zur personalisierten Optimierung
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: 1c7bcffe-5a25-444f-8a95-057b7a07f252
source-git-commit: 0e9d8335bed8d8157a0f2302a5ff2b0a74257218
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 100%

---

# Modell zur personalisierten Optimierung {#personalized-optimization-model}

## Überblick {#overview}

Durch Nutzung modernster Technologien beim überwachten maschinellen Lernen und beim Deep Learning ermöglicht es die personalisierte Optimierung Business-Anwendenden (Marketing-Fachleuten), Geschäftsziele zu definieren und mithilfe ihrer Kundendaten geschäftsorientierte Modelle zu trainieren und so personalisierte Angebote unterbreiten und KPIs maximieren zu können.

<!--![](../../rn/assets/do-not-localize/ai-ranking.gif)-->

## Datensatzanforderungen

Zum Trainieren eines Modells für personalisierte Optimierung muss der Datensatz die folgenden Mindestanforderungen erfüllen:

* Mindestens 2 Angebote im Datensatz müssen innerhalb der letzten 30 Tage mindestens 250 Anzeigeereignisse und 25 Erfolgsereignisse (z. B. Klicks oder Konversionen) aufweisen.
* Angebote mit weniger als 250 Anzeigen und/oder 25 Erfolgsereignissen innerhalb der letzten 30 Tage können in personalisierten Traffic aufgenommen werden, werden jedoch vom Personalisierungsmodell so behandelt, als würden sie auf der Ebene des Angebots mit der schlechtesten Bewertung * abschneiden, bis sie diesen Schwellenwert überschreiten.
* Angebote mit weniger als 250 Anzeigen und/oder 25 Erfolgsereignissen innerhalb der letzten 30 Tage bleiben für die Aufnahme in den Exploration-Traffic geeignet.

Bis ein Modell für personalisierte Optimierung zum ersten Mal trainiert wird, werden Angebote im Rahmen einer Auswahlstrategie mit einem personalisierten Optimierungsmodell nach dem Zufallsprinzip bereitgestellt.

## Grundlegende Modellannahmen und -beschränkungen {#key}

Um die Vorteile der personalisierten Optimierung zu maximieren, müssen einige wichtige Voraussetzungen und Beschränkungen beachtet werden.

* **Die Angebote sind so unterschiedlich, dass auch die Präferenzen der Benutzenden bezüglich der in Frage kommenden Angebote unterschiedlich sind**. Wenn die Angebote zu ähnlich sind, hat das resultierende Modell weniger Wirkung, da die Reaktionen scheinbar zufällig sind.
Wenn eine Bank beispielsweise zwei Kreditkarten anbietet, deren einziger Unterschied die Farbe ist, hat die Empfehlung einer Karte weniger Auswirkung. Wenn aber an jede Karte unterschiedliche Bedingungen geknüpft sind, haben Kunden und Kundinnen einen bestimmten Grund, warum sie sich für eine der Karten entscheiden. Dies bietet deshalb einen ausreichenden Unterschied zwischen den Angeboten, sodass ein wirkungsvolleres Modell erstellt werden kann.
* **Die Zusammensetzung des Traffics von Benutzenden ist stabil**. Wenn sich die Zusammensetzung des Benutzenden-Traffics während des Trainings der Modelle und der Vorhersagephase drastisch ändert, kann sich die Modell-Performance verschlechtern. Angenommen, in der Trainings-Phase des Modells sind nur Daten für Benutzende in Zielgruppe A verfügbar, aber das trainierte Modell wird verwendet, um Prognosen für Benutzende in Zielgruppe B zu generieren. In diesem Fall kann die Modell-Performance beeinträchtigt werden.
* **Die Performance der Angebote ändert sich innerhalb eines kurzen Zeitraums nicht dramatisch**, da dieses Modell wöchentlich aktualisiert wird und die Performance-Änderungen mit der Aktualisierung des Modells übermittelt werden. Ein Beispiel: Ein Produkt war früher sehr beliebt, aber in einem öffentlichen Bericht wird festgestellt, dass das Produkt gesundheitsschädlich ist, und das Produkt wird sehr schnell unpopulär. In diesem Szenario könnte das Modell dieses Produkt so lange empfehlen, bis das Modell aufgrund von Verhaltensänderungen der Benutzenden aktualisiert wird.

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
* In der Phase der **Online-Schlussfolgerung** werden die Angebote auf der Grundlage der vom Modell in Echtzeit generierten Punktzahlen eingestuft. Im Gegensatz zu herkömmlichen kollaborativen Filtertechniken, bei denen es schwierig ist, Merkmale für Benutzende und Angebote einzubeziehen, ist die personalisierte Optimierung eine auf Deep Learning basierende Empfehlungsmethode, die in der Lage ist, komplexe und nicht-lineare Interaktionsmuster von Merkmalen einzubeziehen und zu lernen.

Hier ist ein vereinfachtes Beispiel, um die Grundidee der personalisierten Optimierung zu veranschaulichen. Nehmen wir an, wir haben einen Datensatz, in dem historische Interaktionen zwischen Benutzenden und Angeboten gespeichert sind, wie in Abbildung 1 dargestellt. Es gibt:

* Zwei Angebote, offer_1 und offer_2,
* Zwei Funktionen, Feature_1 und Feature_2,
* Eine Spalte mit der Reaktion.

Der Wert von feature_1, feature_2 und der Reaktion ist entweder 0 oder 1. Wenn wir uns die blauen und orangefarbenen Kästchen in Abbildung 1 ansehen, können wir feststellen, dass bei offer_1 die Reaktionen mit größerer Wahrscheinlichkeit 1 sind, wenn feature_1 und feature_2 die gleichen Werte haben, während bei offer_2 die Werte mit größerer Wahrscheinlichkeit 1 sind, wenn feature_1 0 ist und feature_2 1 ist. Wir können auch sehen, dass im roten Kästchen offer_1 bereitgestellt wird, wenn feature_1 gleich 0 und feature_2 gleich 1 ist, und die Reaktion gleich 0 ist. Ausgehend von dem Muster in den orangefarbenen Kästchen, wo feature_1 gleich 0 und feature_2 gleich 1 ist, ist offer_2 wahrscheinlich eine bessere Empfehlung.

Im Grunde werden hierbei frühere Merkmalsinteraktionen erlernt und gespeichert und danach angewendet, um personalisierte Vorhersagen zu generieren.

![](../assets/perso-ranking-schema.png)

## „Kaltstart“-Problem {#cold-start}

Das „Kaltstart“-Problem tritt auf, wenn es nicht genügend Daten gibt, um eine Empfehlung bereitzustellen. Bei der personalisierten Optimierung gibt es zwei Arten von „Kaltstart“-Problemen.

* **Nachdem ein neues KI-Modell ohne historische Daten erstellt wurde**, werden die Angebote über einen bestimmten Zeitraum nach dem Zufallsprinzip bereitgestellt, um Daten zu sammeln, die dann zum Trainieren des ersten Modells verwendet werden.
* **Nach der Freigabe des ersten Modells** werden 10 % des gesamten Traffics für die zufällige Bereitstellung von Angeboten verwendet, während 90 % des Traffics für Modellempfehlungen verwendet werden. Wenn also neue Angebote in das KI-Modell aufgenommen werden, würden sie als Teil der 10 % des Traffics bereitgestellt werden. Die zu diesen Angeboten gesammelten Daten würden dann im Zuge der weiteren Aktualisierung des Modells bestimmen, wie oft diese Angebote unter den 90 % des Traffics ausgewählt werden.

## Erneutes Training {#re-training}

Die Modelle werden wöchentlich neu trainiert, um die neuesten Interaktionen zwischen den Merkmalen zu erlernen und der Verschlechterung der Modell-Performance entgegenzuwirken.
