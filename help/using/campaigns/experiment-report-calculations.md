---
title: Im Experimentationsbericht verwendete statistische Berechnungen
description: Erfahren Sie mehr über statistische Berechnungen, die bei der Ausführung von Experimentationsberichten verwendet werden
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 67ba8861-be6f-42ae-b9b8-96168d0dd15c
source-git-commit: c14a9385191cfa4368e0b84ab16a63c4c87e2c69
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 100%

---

# Verstehen der statistischen Berechnungen im Versuchsbericht {#experiment-report-calculations}

Auf dieser Seite werden die detaillierten statistischen Berechnungen dokumentiert, die im Experimentationsbericht für Kampagnen in Adobe Journey Optimizer verwendet werden.

Beachten Sie, dass diese Seite für technische Benutzende gedacht ist.

## Konversionsrate

Die Konversionsrate oder **Mittelwert**, μ<sub>ν</sub> für jede Abwandlung `ν` in einem Experiment ist definiert als Verhältnis der Summe der Metrik zur Anzahl der dieser Metrik zugewiesenen Profile, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Hier ist Y<sub>iν</sub> der Wert der Zielmetrik für jedes Profil `i`, das einer bestimmten Variante *ν* zugewiesen wurde. Wenn es sich bei der Zielmetrik Metrik um eine „eindeutige“ Metrik handelt, d. h. um die Anzahl der Profile, die eine bestimmte Aktion durchführen, wird dies als Konversionsrate angezeigt und als Prozentsatz formatiert. Wenn es sich bei der Metrik um eine Metrik vom Typ „Zählung“ oder „Gesamtwert“ (z. B. E-Mail-Öffnungen bzw. Umsatz) handelt, wird die mittlere Schätzung für die Metrik als „Anzahl pro Profil“ bzw. „Wert pro Profil“ angezeigt.

Die Standardabweichung der Stichprobe wird bei Bedarf mit diesem Ausdruck verwendet:

![](assets/statistical_2.png){width="225" align="center"}

## Anstieg {#lift}

Der Anstieg zwischen einer Variante *ν* und der Kontrollvariante *ν<sub>0</sub>* ist das relative „Delta“ in Konversionsraten, definiert als die folgende Berechnung, bei der die individuellen Konversionsraten wie oben definiert sind. Dies wird als Prozentsatz angezeigt.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Jederzeit gültige Konfidenzintervalle für einzelne Abwandlungen

Im Panel „Experimentieren“ in Journey werden „jederzeit gültige“ Konfidenzintervalle (Konfidenzsequenzen) für einzelne Abwandlungen in einem Experiment angezeigt.

Die Konfidenzsequenz für eine bestimmte Variante `ν` ist von zentraler Bedeutung für die von Adobe verwendete statistische Methodik. Die Definition finden Sie auf [dieser Seite](https://doi.org/10.48550/arXiv.2103.06476) (reproduziert aus [Waudby-Smith et al.]).

Wenn Sie an der Schätzung eines Zielgruppen-Parameters `ψ` interessiert sind, z. B. der Konversionsrate einer Variante in einem Experiment, kann die Dichotomie zwischen einer Sequenz von „zeitlich festen“ Konfidenzintervallen (CIs) und einer zeiteinheitlichen Konfidenzsequenz (CS) wie folgt zusammengefasst werden:

![](assets/statistical_4.png){width="500" align="center"}

Bei einem regulären Konfidenzintervall ist die Garantie der probabilistischen Methode, dass der Zielgruppen-Parameter innerhalb des Wertebereichs Ċ<sub>n</sub> liegt, nur bei einem einzelnen festen Wert von `n` gültig (wobei `n` die Anzahl der Stichproben ist). Dagegen wird bei einer Konfidenzsequenz garantiert, dass jederzeit und bei allen Werten der Stichprobengröße `t` der „wahre“ Wert des Parameters von Interesse innerhalb der Grenzen liegt.

Dies hat einige tiefgreifende Auswirkungen, die für Online-Tests sehr wichtig sind:

* Die CS kann optional aktualisiert werden, wenn neue Daten verfügbar sind.
* Experimente können kontinuierlich überwacht, adaptiv angehalten oder fortgesetzt werden.
* Der Fehler vom Typ I wird bei allen Stoppzeiten kontrolliert, einschließlich datenabhängiger Zeiten.

Adobe verwendet asymptotische Konfidenzsequenzen, die für eine einzelne Variante mit dem geschätzten Durchschnittswert `μ` diese Form haben:

![](assets/statistical_5.png){width="300" align="center"}

Dabei gilt:

* `N` ist die Anzahl der Einheiten für diese Variante.
* `σ` ist eine Stichprobenschätzung der Standardabweichung (wie oben definiert).
* `α` ist die gewünschte Fehlerrate des Fehlers vom Typ I (oder der Wahrscheinlichkeit einer Fehlabdeckung). Diese ist immer auf 0,05 festgelegt.
* p<sup>2</sup> ist eine Konstante, die die Stichprobengröße so anpasst, dass die CS möglichst dicht anliegt. Adobe hat den universellen Wert p<sup>2</sup> = 10<sup>-2,8</sup> gewählt, was für Konversationsraten geeignet ist, die in Online-Experimenten vorkommen.

## Konfidenz {#confidence}

Die von Adobe verwendete Konfidenz ist eine „jederzeit gültige“ Konfidenz, die durch Umkehrung der Konfidenzsequenz für den durchschnittlichen Abwandlungseffekt erzielt wird.

Genauer gesagt, gibt es in einem Test mit zwei Stichproben von *t*, bei dem auf den Unterschied zwischen den Mittelwerten zweier Varianten getestet wird, eine 1:1-Zuordnung zwischen dem *p*-Wert für diesen Test und das Konfidenzintervall für die Differenz der Mittelwerte. In Analogie dazu kann ein jederzeit gültiger *p*-Wert erlangt werden, indem die (jederzeit gültige) Konfidenzsequenz für die Schätzung des durchschnittlichen Abwandlungseffekts invertiert wird:

![](assets/statistical_6.png){width="200" align="center"}

Hierbei ist *E* eine Erwartung. Die verwendete Schätzung ist eine Schätzung mit umgekehrter Tendenzgewichtung (inverse propensity weighted, IPW). Angenommen, es gibt N = N<sub>0</sub> +N<sub>1</sub> Einheiten, mit Variantenzuweisungen für jede Einheit `i`, die durch A<sub>i</sub>=0,1 gekennzeichnet sind, wenn die Einheit der Variante `ν`=0,1 zugewiesen ist. Wenn den Benutzenden eine feste Wahrscheinlichkeit (Tendenz) π<sub>0</sub>, (1-π<sub>0</sub>) zugewiesen wird und ihre Ergebnismetrik Y<sub>i</sub> ist, dann ist die IPW-Schätzung für den durchschnittlichen Abwandlungseffekt:

![](assets/statistical_12.png){width="400" align="center"}

Mit der Feststellung, dass *f* die Einflussfunktion ist, zeigten Waudby-Smith et al., dass die Konfidenzsequenz für diese Schätzung wie folgt ist:

![](assets/statistical_7.png){width="500" align="center"}

Wenn die Zuweisungswahrscheinlichkeit durch ihre empirischen Schätzungen: π<sub>0</sub> = N<sub>0</sub>/N ersetzt wird, kann der Varianzbegriff als Funktion der Mittelwertschätzungen μ<sub>0,1</sub> einzelner Stichproben und der Standardabweichungsschätzungen σ<sub>0,1</sub> ausgedrückt werden als:

![](assets/statistical_8.png){width="500" align="center"}

Beachten Sie als Nächstes, dass für einen regelmäßigen Hypothesentest mit Teststatistik z = (μ<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>) eine Korrespondenz zwischen `p`-Werten und Konfidenzintervallen beseht:

![](assets/statistical_9.png){width="500" align="center"}

wobei `Φ` die kumulative Standard-Normalverteilung ist. Bei jederzeit gültigen `p`-Werten, können wir in Anbetracht der Konfidenzsequenz für den oben definierten durchschnittlichen Abwandlungseffekt diese Beziehung umkehren:

![](assets/statistical_10.png){width="600" align="center"}

Und schließlich ist die **jederzeit gültige Konfidenz**:

![](assets/statistical_11.png){width="200" align="center"}

## Ein Experiment für schlüssig erklären

Bei einem Experiment mit zwei Testverzweigungen zeigt das Panel „Experimentieren“ in Journey Optimizer eine Nachricht an, dass ein Experiment **schlüssig** ist, wenn die jederzeit gültige Konfidenz 95 % überschreitet (d. h. der jederzeit gültige `p`-Wert unter 5 % liegt).

Wenn mehr als zwei Varianten vorhanden sind, wird die Bonferonni-Korrektur angewendet, um die familienspezifische Fehlerquote zu kontrollieren. Bei einem Experiment mit `K` Abwandlungen und einer einzigen Baseline-Abwandlung (Kontrolle) gibt es `K-1` unabhängige Hypothesentests. Die Bonferonni-Korrektur bedeutet, dass wir die Null-Hypothese ablehnen, dass die Kontrolle und eine bestimmte Variante über die gleichen Mittelwerte verfügen, wenn der jederzeit gültige `p`-Wert (wie oben definiert) unterhalb des Schwellenwerts von `α/(K-1)` liegt.

## Testverzweigung mit dem besten Ergebnis

Wenn ein Experiment als schlüssig erklärt wird, wird die Testverzweigung mit dem besten Ergebnis angezeigt. Dies ist die Testverzweigung mit dem besten Ergebnis (höchster Mittelwert oder höchste Konversionsrate) aus dem Satz, der die Kontrolle enthält, und aus allen Testverzweigungen mit einem `p`-Wert unterhalb des Bonferroni-Schwellenwerts.
