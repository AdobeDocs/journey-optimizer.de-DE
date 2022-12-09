---
product: experience platform
solution: Experience Platform
title: Personalisiertes Optimierungsmodell
description: Erfahren Sie mehr über personalisierte Optimierungsmodelle
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Personalisiertes Optimierungsmodell {#personalized-optimization-model}

>[!CAUTION]
>
>Die Verwendung personalisierter Optimierungsmodelle ist derzeit nur für ausgewählte Benutzer in einem frühen Zugriff verfügbar.

## Übersicht {#overview}

Durch die Nutzung der modernsten Technologien im beaufsichtigten maschinellen Lernen und tiefen Lernens ermöglicht die automatische Personalisierung einem Business-Anwender (Marketingexperten), Geschäftsziele zu definieren und seine Kundendaten zu nutzen, um geschäftsorientierte Modelle für personalisierte Angebote zu trainieren und KPIs zu maximieren.

## Grundlegende Modellannahmen und -beschränkungen {#key}

Um den Vorteil der automatischen Personalisierung zu maximieren, sollten Sie einige wichtige Annahmen und Einschränkungen beachten.

* **Angebote sind so unterschiedlich, dass Benutzer unterschiedliche Voreinstellungen unter den betreffenden Angeboten haben.**. Wenn Angebote zu ähnlich sind, hat ein resultierendes Modell weniger Auswirkungen, da die Antworten scheinbar zufällig sind.
Wenn beispielsweise eine Bank über zwei Kreditkartenangebote verfügt, bei denen der einzige Unterschied die Farbe ist, ist es möglicherweise nicht wichtig, welche Karte empfohlen wird, aber wenn jede Karte unterschiedliche Bedingungen hat, bietet dies eine Begründung dafür, warum bestimmte Kunden eine wählen würden, und ausreichend Unterschiede zwischen Angeboten bereitstellen, um ein wirkungsvolleres Modell zu erstellen.
* **Die Traffic-Zusammensetzung des Benutzers ist stabil**. Wenn sich die Traffic-Zusammensetzung der Benutzer während des Trainings und der Vorhersage der Modelle drastisch ändert, kann sich die Modellleistung verschlechtern. Angenommen, in der Modellschulungsphase sind nur Daten für Benutzer in Segment A verfügbar, aber das trainierte Modell wird verwendet, um Prognosen für Benutzer in Segment B zu generieren. Anschließend kann die Modellleistung beeinträchtigt werden.
* **Die Angebotsleistung ändert sich in einem kurzen Zeitraum nicht wesentlich** da dieses Modell wöchentlich aktualisiert wird und Leistungsänderungen als Modellaktualisierungen übermittelt werden. Ein Produkt war beispielsweise schon einmal sehr beliebt, aber in einem öffentlichen Bericht wird festgestellt, dass das Produkt für unsere Gesundheit schädlich ist, und dieses Produkt wird extrem schnell unbeliebt. In diesem Szenario kann das Modell dieses Produkt weiter vorhersagen, bis das Modell mit Änderungen im Benutzerverhalten aktualisiert wird.

## Funktionsweise {#how}

Die automatische Personalisierung erfährt komplexe Funktionsinteraktionen zwischen Angeboten, Benutzerinformationen und Kontextinformationen, um Endbenutzern personalisierte Angebote zu empfehlen. Funktionen sind Eingaben in das Modell.

Es gibt drei Arten von Funktionen:

| Funktionstypen | Hinzufügen von Funktionen zu Modellen |
|--------------|----------------------------|
| Entscheidungsobjekte (placementID, activityID, decisionScopeID) | Teil des Feedbacks zur Entscheidungsverwaltung an AEP gesendete Erlebnisereignisse |
| Segmente | 0-50 Segmente können bei der Erstellung des Ranking AI-Modells als Funktionen hinzugefügt werden |
| Kontextdaten | Teil des Entscheidungs-Feedbacks Erlebnisereignisse, die an AEP gesendet werden. Verfügbare Kontextdaten zum Hinzufügen zum Schema: Commerce-Details, Kanaldetails, Anwendungsdetails, Web-Details, Umgebungsdetails, Gerätedetails, placeContext |

Das Modell umfasst zwei Phasen:

* Im **Offline-Modellschulung** -Phase, wird ein Modell durch Lernen und Einprägen von Funktionsinteraktionen in historischen Daten trainiert.
* Im **Online-Einsicht** -Phase, werden die Kandidatenangebote basierend auf den vom Modell generierten Echtzeit-Ergebnissen nach Rang geordnet. Im Gegensatz zu herkömmlichen kollaborativen Filtertechniken, die sich nur schwer mit Funktionen für Benutzer und Angebote integrieren lassen, ist die automatische Personalisierung eine lernbasierte Empfehlungsmethode, die komplexe und nicht lineare Interaktionsmuster von Funktionen einschließen und erlernen kann.

Im Folgenden finden Sie ein vereinfachtes Beispiel zur Veranschaulichung der Grundidee der automatischen Personalisierung. Angenommen, wir verfügen über einen Datensatz, der historische Interaktionen zwischen Benutzern und Angeboten speichert, wie in Abbildung 1 dargestellt. Es gibt:
* Zwei Angebote, offer_1 und offer_2,
* Zwei Funktionen, Feature_1 und Feature_2,
* Eine Antwortspalte.

Der Wert von feature_1, feature_2 und response ist entweder 0 oder 1. Wenn wir uns die blauen Kästchen und orangefarbenen Kästchen in Abbildung 1 ansehen, können wir feststellen, dass die Antworten für offer_1 mit höherer Wahrscheinlichkeit 1 sind, wenn feature_1 und feature_2 dieselben Werte aufweisen, während für offer_2 die Beschriftungen eher 1 lauten, wenn feature_1 0 und feature_2 1 ist. Wir können auch sehen, dass im roten Feld offer_1 bereitgestellt wird, wenn feature_1 den Wert 0 und feature_2 den Wert 1 hat und die Antwort den Wert 0 hat. Basierend auf dem Muster, das wir in orangefarbenen Feldern sehen, ist offer_2 wahrscheinlich eine bessere Empfehlung, wenn feature_1 den Wert 0 und feature_2 den Wert 1 hat.

Im Grunde ist dies die Idee, historische Funktionsinteraktionen zu lernen und zu merken und sie anzuwenden, um personalisierte Prognosen zu generieren.

![](../assets/perso-ranking-schema.png)

## Cold-Start-Problem {#cold-start}

Ein Cold-Start-Problem tritt auf, wenn nicht genügend Daten für eine Empfehlung vorhanden sind. Bei der automatischen Personalisierung gibt es zwei Arten von Kaltstart-Problemen.

* **Erstellen einer neuen Rangstrategie ohne historische Daten**, werden Angebote für einen Zeitraum zufällig zur Datenerfassung bereitgestellt und die Daten werden zur Schulung des ersten Modells verwendet.
* A **Nachdem das erste Modell veröffentlicht wurde**, werden 10 % des gesamten Traffics für zufällige Dienste zugewiesen, während 90 % des Traffics für Modellempfehlungen verwendet werden. Wenn also neue Angebote zur Rangstrategie hinzugefügt würden, würden sie als Teil des 10 %-Traffics bereitgestellt. Die für diese Angebote erfassten Daten würden bestimmen, wie oft sie unter den 90 % des Traffics ausgewählt werden, da das Modell weiter aktualisiert wird.

## Umschulung {#re-training}

Modelle werden neu trainiert, um die neuesten Funktionsinteraktionen kennenzulernen und die Leistungsbeeinträchtigung des Modells wöchentlich zu reduzieren.
