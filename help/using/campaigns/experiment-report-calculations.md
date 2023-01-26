---
title: Im Experimentationsbericht verwendete statistische Berechnungen
description: Erfahren Sie mehr über statistische Berechnungen, die beim Ausführen von Experimentberichten verwendet werden
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 1%

---

# Statistische Berechnungen im Experimentationsbericht {#experiment-report-calculations}

Auf dieser Seite werden die detaillierten statistischen Berechnungen dokumentiert, die im Experimentationsbericht für Kampagnen in Adobe Journey Optimizer verwendet werden.

Beachten Sie, dass diese Seite für technische Benutzer gedacht ist.

## Konversionsrate

Konversionsrate oder **mean**, μ<sub>ν</sub> für jede Behandlung `ν` in einem Experiment definiert wird als Verhältnis der Summe der Metrik zur Anzahl der dieser Metrik zugewiesenen Profile, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Hier, Y<sub>iν</sub> ist der Wert der Zielmetrik für jedes Profil. `i`, die einer bestimmten Variante zugewiesen wurde *ν*. Wenn es sich bei der objektiven Metrik um eine &quot;eindeutige&quot;Metrik handelt, d. h. um die Anzahl der Profile, die eine bestimmte Aktion durchführen, wird dies als Konversionsrate angezeigt und als Prozentsatz formatiert. Wenn es sich bei der Metrik um eine Metrik vom Typ &quot;Zählung&quot;oder &quot;Gesamtwert&quot;(z. B. E-Mail-Öffnungen, Umsatz) handelt, wird die mittlere Schätzung für die Metrik als &quot;Anzahl pro Profil&quot;oder &quot;Wert pro Profil&quot;angezeigt.

Die Standardabweichung der Stichprobe wird bei Bedarf mit dem Ausdruck verwendet:

![](assets/statistical_2.png){width="225" align="center"}

## Anstieg {#lift}

Die Steigerung zwischen einer Variante  *ν* und der Kontrollvariante  *ν<sub>0</sub>* ist das relative &quot;Delta&quot;in Konversionsraten, definiert als die Berechnung unten, bei der die individuellen Konversionsraten wie oben definiert sind. Dies wird als Prozentsatz angezeigt.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Ungültige Konfidenzintervalle für einzelne Behandlungen

Im Bedienfeld Journey-Experimentierung werden &quot;jederzeit gültige&quot;Konfidenzintervalle (Konfidenzsequenzen) für einzelne Behandlungen in einem Experiment angezeigt.

Die Konfidenzsequenz für eine bestimmte Variante `ν` ist von zentraler Bedeutung für die von der Adobe verwendete statistische Methodik. Die Definition finden Sie unter [diese Seite](https://doi.org/10.48550/arXiv.2103.06476) aus [Waudby-Smith et al.]).

Wenn Sie an der Schätzung eines Zielparameters interessiert sind `ψ` z. B. die Konversionsrate einer Variante in einem Experiment, die Dichotomie zwischen einer Sequenz von &quot;festen&quot;Konfidenzintervallen (CIs) und einer zeiteinheitlichen Konfidenzsequenz (CS) kann wie folgt zusammengefasst werden:

![](assets/statistical_4.png){width="500" align="center"}

Für ein reguläres Konfidenzintervall garantiert die probabilistische Methode, dass der Zielparameter innerhalb des Wertebereichs liegtĊ<sub>n</sub> ist nur bei einem einzelnen festen Wert von `n` , `n` Anzahl der Proben). Im Gegensatz zu einer Konfidenzsequenz wird garantiert, dass jederzeit/alle Werte der Stichprobengröße `t`, liegt der Wert &quot;true&quot;des Zielparameters innerhalb der Grenzen.

Dies hat einige tief greifende Auswirkungen, die für Online-Tests sehr wichtig sind:

* Das CSS kann optional aktualisiert werden, sobald neue Daten verfügbar sind.
* Experimente können kontinuierlich überwacht, adaptiv angehalten oder fortgesetzt werden.
* Der Typ-I-Fehler wird zu allen Stoppzeiten gesteuert, einschließlich datenabhängiger Zeiten.

Adobe verwendet asymptotische Konfidenzsequenzen, die für eine einzelne Variante mit durchschnittlicher Schätzung verwendet werden `μ` hat das Formular:

![](assets/statistical_5.png){width="300" align="center"}

Dabei wird:

* `N` ist die Anzahl der Einheiten für diese Variante.
* `σ` ist eine Stichprobenschätzung der Standardabweichung (siehe oben).
* `α` ist die gewünschte Fehlerrate des Typ-I-Fehlers (oder der Wahrscheinlichkeit einer Fehlabdeckung). Dies ist immer auf 0,05 festgelegt.
* evaluate<sup>2</sup> ist eine Konstante, die die Stichprobengröße anpasst, bei der das CS am härtesten ist. Die Adobe hat sich für einen universellen Wert von<sup>2</sup> = 10<sup>-2,8</sup>, was für die in Online-Experimenten angezeigten Konversionsraten geeignet ist.

## Konfidenz {#confidence}

Die von der Adobe verwendete Konfidenz ist eine &quot;jederzeit gültige&quot;Konfidenz, die durch Umkehrung der Konfidenzsequenz für den durchschnittlichen Behandlungseffekt erzielt wird.

Präzise in zwei Proben *t* Test auf den Unterschied zwischen den Mittelwerten zweier Varianten. Es gibt eine 1:1-Zuordnung zwischen der *p*-Wert für diesen Test und das Konfidenzintervall für die Differenz der Mittelwerte. Eine jederzeit gültige *p*-Wert kann durch Invertieren der (jederzeit gültigen) Konfidenzsequenz für die Schätzung des durchschnittlichen Behandlungseffekts abgerufen werden:

![](assets/statistical_6.png){width="200" align="center"}

Hier, *E* ist eine Erwartung. Die verwendete Schätzung ist ein umgekehrter Tendenzgewichteter (IPW) Schätzer. Betrachtung N = N<sub>0</sub> +N<sub>1</sub> Einheiten, Variantenzuweisungen für jede Einheit `i` durch A gekennzeichnet<sub>i</sub>=0,1, wenn die Einheit der Variante zugewiesen ist `ν`=0,1. Wenn die Benutzer mit einer festen Wahrscheinlichkeit (Tendenz) zugewiesen werden<sub>0</sub>, (1-H<sub>0</sub>) und ihre Ergebnismetrik ist Y<sub>i</sub>, ist die IPW-Schätzung für den durchschnittlichen Behandlungseffekt:

![](assets/statistical_12.png){width="400" align="center"}

feststellen, dass *f* ist die Einflussfunktion Waudby-Smith et al. zeigte, dass die Konfidenzsequenz für diesen Schätzer:

![](assets/statistical_7.png){width="500" align="center"}

Ersetzen der Zuweiswahrscheinlichkeit durch ihre empirischen Schätzungen: BS<sub>0</sub> = N<sub>0</sub>/N, kann der Varianzbegriff in Form von individuellen Stichprobenmittelschätzungen μ ausgedrückt werden.<sub>0,1</sub> und Standardabweichungsschätzungen, σ<sub>0,1</sub> as:

![](assets/statistical_8.png){width="500" align="center"}

Beachten Sie als Nächstes, dass für einen regelmäßigen Hypothesentest mit Teststatistik z = (μ)<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>) gibt es eine Korrespondenz zwischen `p`-Werte und Konfidenzintervalle:

![](assets/statistical_9.png){width="500" align="center"}

where `Φ` ist die kumulative Verteilung der normalen Normalwerte. Für jeden Zeitraum gültig `p`-Werte, in Anbetracht der Konfidenzsequenz für den oben definierten durchschnittlichen Behandlungseffekt, können wir diese Beziehung umkehren:

![](assets/statistical_10.png){width="600" align="center"}

Schließlich wird die **jederzeit gültige Konfidenz** ist:

![](assets/statistical_11.png){width="200" align="center"}

## Ein Experiment für schlüssig erklären

Für ein Experiment mit zwei Armen zeigt das Bedienfeld &quot;Journey Optimizer-Experimentierung&quot;eine Meldung an, dass ein Experiment **schlüssig** wenn die jederzeit gültige Konfidenz 95 % überschreitet (d. h. die jederzeit gültige Gültigkeit `p`-Wert unter 5%).

Wenn mehr als zwei Varianten vorhanden sind, wird die Bonferonni-Korrektur angewendet, um die familiäre Fehlerrate zu steuern. Für ein Experiment mit `K` und eine einzige Ausgangsbehandlung (Kontrolle), gibt es `K-1` unabhängige Hypothesentests. Die Bonferonni-Korrektur bedeutet, dass wir die Null-Hypothese ablehnen, dass die Kontrolle und eine bestimmte Variante über die gleichen Mittel verfügen, wenn die jederzeit gültige `p`-value (definiert oben) liegt unterhalb eines Schwellenwerts von `α/(K-1)`.

## Beste Leistung

Wenn ein Experiment als abgeschlossen erklärt wird, wird der Arm mit der besten Leistung angezeigt. Dies ist der Arm mit der besten Leistung (höchste Mittelwert- oder Konversionsrate), der zu dem Satz gehört, der die Kontrolle enthält, und allen Armen mit einer `p`-Wert unterhalb des Bonferonni-Schwellenwerts.
