---
product: experience platform
solution: Experience Platform
title: Modelle zur automatischen Optimierung
description: Erfahren Sie mehr über Modelle zur automatischen Optimierung
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 0%

---

# Modelle zur automatischen Optimierung {#auto-optimization-model}

Ein Automatisierte Optimierung-Modell dient der Bereitstellung von Angeboten, die die von Geschäftskunden festgelegten Renditen (KPIs) maximieren. Diese KPIs können in Form von Konversionsraten, Umsatz usw. vorliegen. Zu diesem Zeitpunkt konzentriert sich die automatisierte Optimierung auf die Optimierung von Angebotsklicks mit Angebotskonversion als Ziel. Die automatische Optimierung ist nicht personalisiert und wird auf der Grundlage der &quot;globalen&quot;Leistung der Angebote optimiert.

## Einschränkungen {#limitations}

Die Verwendung von Modellen zur automatischen Optimierung der Entscheidungsfindung unterliegt den folgenden Beschränkungen:

* Modelle zur automatischen Optimierung funktionieren nicht mit der Batch Decisioning-API.
* Das zum Erstellen des Modells benötigte Feedback muss als Erlebnisereignis gesendet werden. Sie sollte nicht automatisch in [!DNL Journey Optimizer] Kanäle.

## Terminologie {#terminology}

Die folgenden Begriffe sind nützlich, wenn es um die automatische Optimierung geht:

* **Multi-Armed Bandit**: A [Multi-Armed Bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=&quot;_blank&quot;} Ansatz zur Optimierung gleicht forschendes Lernen und die Nutzung dieses Lernens aus.

* **Thomson-Probenahme**: Thompson Sampling ist ein Algorithmus für Online-Entscheidungsprobleme, bei dem sequenziell Maßnahmen getroffen werden, die einen Ausgleich zwischen der Nutzung dessen, was bekannt ist, um die sofortige Leistung zu maximieren, und Investitionen zur Sammlung neuer Informationen, die die zukünftige Leistung verbessern können, herstellen müssen. [Weitere Infos](#thompson-sampling)

* [**Beta-Distribution**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}: Satz von fortlaufenden [Wahrscheinlichkeitsverteilung](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} definiert im Intervall [0, 1] [parametrisiert](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} durch zwei positive Werte [Formparameter](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

## Thompson Sampling {#thompson-sampling}

Der Algorithmus, der der automatischen Optimierung zugrunde liegt, lautet **Thompson-Sampling**. In diesem Abschnitt besprechen wir die Intuition hinter Thompson Sampling.

[Thompson-Sampling](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, oder Bayes-Bandits, ist ein Bayes-Ansatz für das Multi-Armed Bandit-Problem.  Die Grundidee ist, die durchschnittliche Belohnung zu behandeln? aus jedem Angebot als **Zufallsvariable** und nutzen Sie die bisher gesammelten Daten, um unseren &quot;Glauben&quot; über die durchschnittliche Belohnung zu aktualisieren. Dieser &quot;Glaube&quot;wird mathematisch durch eine **posteriale Wahrscheinlichkeitsverteilung** - im Wesentlichen ein Wertebereich für die durchschnittliche Belohnung sowie die Plausibilität (oder Wahrscheinlichkeit), dass die Belohnung diesen Wert für jedes Angebot hat. Dann werden wir für jede Entscheidung **Beispiel eines Punkts aus jeder dieser nachträglichen Rewards-Verteilungen** und wählen Sie das Angebot aus, dessen jeweilige Belohnung den höchsten Wert aufweist.

Dieser Vorgang wird in der folgenden Abbildung veranschaulicht, in der wir drei verschiedene Angebote haben. Anfänglich haben wir keine Beweise aus den Daten und wir gehen davon aus, dass alle Angebote eine gleichmäßige Verteilung der Belohnung nach dem Posterior aufweisen. Wir zeichnen ein Beispiel aus der Verteilung der posterioralen Belohnung jedes Angebots. Das aus der Verteilung von Angebot 2 ausgewählte Beispiel hat den höchsten Wert. Dies ist ein Beispiel für **Exploration**. Nach der Anzeige von Angebot 2 erfassen wir jede potenzielle Belohnung (z. B. Konversion/Keine Konversion) und aktualisieren die nachgelagerte Verteilung von Angebot 2 mit Bayes Theorem, wie unten beschrieben.  Wir setzen diesen Prozess fort und aktualisieren die posterioren Distributionen jedes Mal, wenn ein Angebot angezeigt und die Prämie eingesammelt wird. In der zweiten Abbildung wird Angebot 3 ausgewählt - trotz Angebot 1 mit der höchsten durchschnittlichen Belohnung (die Verteilung der Belohnung nach der Nachher ist am weitesten rechts), hat der Prozess der Probenahme von jeder Verteilung dazu geführt, dass wir ein scheinbar suboptimales Angebot 3 ausgewählt haben. Damit geben wir uns die Möglichkeit, mehr über die wahre Belohnungsverteilung von Angebot 3 zu erfahren.

Je mehr Proben gesammelt werden, desto größer wird das Konfidenzniveau, und es wird eine genauere Schätzung der möglichen Belohnung erzielt (entsprechend einer geringeren Verteilung der Belohnungen). Dieser Prozess der Aktualisierung unserer Überzeugungen, sobald mehr Beweise verfügbar werden, wird als **Bayesian Inference**.

Wenn ein Angebot (z. B. Angebot 1) ein eindeutiger Gewinner ist, wird die Verteilung der nachgelagerten Belohnung von anderen getrennt. Zu diesem Zeitpunkt wird die von Angebot 1 in die Stichprobe einbezogene Belohnung für jede Entscheidung wahrscheinlich die höchste sein, und wir werden sie mit einer höheren Wahrscheinlichkeit auswählen. Dies ist **Nutzung** - wir sind der festen Überzeugung, dass Angebot 1 das beste ist, und daher wird es ausgewählt, um die Belohnungen zu maximieren.

![](../assets/ai-ranking-thompson-sampling.png)

**Abbildung 1**: *Für jede Entscheidung wird ein Punkt aus den posterioren Rewards-Distributionen entnommen. Es wird das Angebot mit dem höchsten Stichprobenwert (Konversionsrate) ausgewählt. In der Anfangsphase haben alle Angebote eine einheitliche Verteilung, da wir keine Beweise für die Konversionsraten der Angebote aus den Daten haben. Da wir mehr Proben sammeln, werden die posterioren Distributionen enger und genauer. Letztlich wird jedes Mal das Angebot mit der höchsten Konversionsrate ausgewählt.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Technische Details**

Zur Berechnung/Aktualisierung von Verteilungen verwenden wir **Bayes Theorem**. Für jedes Angebot ***i***, möchten wir ihre ***P(??i berechnen | data)**, d. h. für jedes Angebot ***i***, wie wahrscheinlich ein Belohnungswert ist **??i** ist, in Anbetracht der Daten, die wir bisher für dieses Angebot gesammelt haben.

Von Bayes Theorem:

***Posterior = Wahrscheinlichkeit * Vorherige***

Die **vorherige Wahrscheinlichkeit** ist die anfängliche Schätzung der Wahrscheinlichkeit, eine Ausgabe zu erzeugen. Die Wahrscheinlichkeit, nachdem einige Beweise gesammelt wurden, wird als **posteriale Wahrscheinlichkeit**. 

Die automatische Optimierung ist so konzipiert, dass binäre Belohnungen (Klick/Klick) berücksichtigt werden. In diesem Fall stellt die Wahrscheinlichkeit die Anzahl der Erfolge aus N Versuchen dar und wird nach dem Modell eines **Binomialische Verteilung**. Bei einigen Wahrscheinlichkeitsfunktionen befindet sich der Posterior, wenn Sie ein bestimmtes Vorfeld wählen, in derselben Verteilung wie zuvor. Eine solche Vorgeschichte nennt man **vorher konjugieren**. Diese Art von Vorkenntnissen macht die Berechnung der Posterior-Verteilung sehr einfach. Die **Beta-Distribution** ist ein Konjugat vor der binomialen Wahrscheinlichkeit (binäre Belohnungen) und daher eine praktische und sinnvolle Wahl für die vorherigen und nachgelagerten Wahrscheinlichkeitsverteilungen. Die Beta-Verteilung akzeptiert zwei Parameter. ***α*** und ***β***. Diese Parameter können als Anzahl von Erfolgen und Fehlschlägen und als Mittelwert betrachtet werden, der angegeben wird durch:

![](../assets/ai-ranking-beta-distribution.png)

Die oben erläuterte Funktion &quot;Wahrscheinlichkeit&quot;wird von einer Binomial-Distribution modelliert, deren Erfolge (Konversionen) und Fehler (keine Konversionen) vorliegen und q eine [Zufallsvariable](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} mit einer [Beta-Distribution](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

Die vorherige Version wird von der Beta-Distribution modelliert und die nachgelagerte Verteilung hat die folgende Form:

![](../assets/ai-ranking-posterior-distribution.svg)

Die Berechnung des Posteriors erfolgt einfach durch Hinzufügen der Anzahl an Erfolgen und Fehlern zu den vorhandenen Parametern ***α***, ***β***.

Zur automatischen Optimierung beginnen wir, wie im Beispiel oben gezeigt, mit einer vorherigen Verteilung. ***Beta(1, 1)*** (einheitliche Verteilung) für alle Angebote und nach Erzielen von Erfolgen und Fehlschlägen für ein bestimmtes Angebot wird der Posterior zu einer Beta-Distribution mit Parametern ***(s+α, f+β)*** für dieses Angebot.
+++

**Verwandte Themen**:

Für einen tieferen Einblick in die Thompson-Probenahme lesen Sie die folgenden Forschungsarbeiten:
* [Eine empirische Bewertung des Thompson-Stichprobenverfahrens](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Analyse der Thompson-Probenahme für das Multi-Armed Bandit-Problem](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

## Cold-Start-Problem {#cold-start}

Das Problem &quot;Kaltstart&quot;tritt auf, wenn ein neues Angebot zu einer Kampagne hinzugefügt wird und keine Daten zur Konversionsrate des neuen Angebots verfügbar sind. Während dieses Zeitraums müssen wir eine Strategie dafür entwickeln, wie oft dieses neue Angebot ausgewählt wird, damit der Leistungsabfall minimiert wird, während wir Informationen über die Konversionsrate dieses neuen Angebots sammeln. Es gibt mehrere Lösungen, um dieses Problem anzugehen. Der Schlüssel ist, ein Gleichgewicht zwischen der Erforschung dieses neuen Angebots zu finden, während wir die Ausbeutung nicht viel opfern. Derzeit verwenden wir &quot;einheitliche Verteilung&quot;, um die Konversionsrate des neuen Angebots (vorherige Verteilung) zu schätzen. Grundsätzlich geben wir allen Konversionsratenwerten die gleiche Wahrscheinlichkeit des Auftretens.


![](../assets/ai-ranking-cold-start-strategies.png)

**Abbildung 2**: *Betrachten Sie eine Kampagne mit drei Angeboten. Während der Kampagne wird Angebot 4 zur Kampagne hinzugefügt. Zunächst liegen keine Daten über die Konversionsrate des Angebots 4 vor und wir müssen uns mit dem Kaltstart-Problem befassen. Wir verwenden eine gleichmäßige Verteilung als ersten Schätzwert zur Konversionsrate von Angebot 4, während wir Daten für dieses neue Angebot sammeln. Wie im Abschnitt [Thompson-Sampling](#thompson-sampling) um auszuwählen, welches Angebot einem Benutzer angezeigt werden soll, wählen wir die Punkte aus den posterioren Verteilung der Angebote aus und wählen das Angebot mit dem höchsten Beispielwert aus. Im obigen Beispiel wird Angebot 4 ausgewählt und später anhand der erfassten Belohnung aktualisiert. Die nachgelagerte Verteilung dieses Angebots wird wie im Abschnitt [Thompson-Sampling](#thompson-sampling) Abschnitt.*

## Steigerungsmessung {#lift}

&quot;Steigerung&quot;ist die Metrik, die verwendet wird, um die Leistung einer beliebigen Strategie zu messen, die im Rang-Service bereitgestellt wird, im Vergleich zur Basisstrategie (Bereitstellung von Angeboten einfach zufällig).

Wenn wir z. B. die Performance einer Thompson Sampling (TS)-Strategie im Ranking Service messen möchten und der KPI die Konversionsrate (CVR) ist, wird die &quot;Steigerung&quot;der TS-Strategie gegenüber der Basisstrategie folgendermaßen definiert:

![](../assets/ai-ranking-lift.png)
