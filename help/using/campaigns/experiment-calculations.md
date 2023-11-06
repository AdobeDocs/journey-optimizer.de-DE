---
solution: Journey Optimizer
product: journey optimizer
title: Von Adobe Journey Optimizer Experimentation verwendete statistische Berechnungen
description: Erfahren Sie mehr über statistische Berechnungen, die bei der Durchführung von Experimenten verwendet werden
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: Inhalt, Experiment, statistisch, Berechnung
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 1490ac2efd39c6bf9b6ca97e682750463e9f054d
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 100%

---

# Verstehen von statistischen Berechnungen {#experiment-calculations}

Dieser Artikel beschreibt die statistischen Berechnungen, die bei der Durchführung von Experimenten in Adobe Journey Optimizer verwendet werden.

Experimente verwenden [fortschrittliche statistische Methoden](../campaigns/assets/confidence_sequence_technical_details.pdf) zur Berechnung von **Konfidenzsequenzen** und **Konfidenz**, die es Ihnen ermöglichen, Ihre Experimente so lange wie nötig durchzuführen und Ihre Ergebnisse kontinuierlich zu überwachen.

Dieser Artikel beschreibt die Funktionsweise von Experimenten und bietet eine intuitive Einführung in die **jederzeit gültigen Konfidenzsequenzen** von Adobe.

Für erfahrene Benutzende sind die technischen Details und Referenzen auf [dieser Seite](../campaigns/assets/confidence_sequence_technical_details.pdf) aufgeführt.

## Statistische Tests und Fehlerkontrolle {#statistical-testing}

Mit einem Experiment möchten Sie ermitteln, ob ein Unterschied zwischen zwei Populationen besteht, und die Wahrscheinlichkeit bestimmen, dass ein Unterschied auf einen Zufall zurückzuführen ist.

Im Allgemeinen gibt es zwei Hypothesen:

* Die **Nullhypothese** bedeutet, dass es durch die Abwandlung keine Auswirkung gibt.
* Die **Alternativhypothese** bedeutet, dass es durch die Abwandlung eine Auswirkung gibt.

Bei der statistischen Signifikanz geht es darum zu bewerten, wie stark die Beweise sind, um die Nullhypothese zu verwerfen. Ein wichtiger Punkt, den es zu beachten gilt: Mithilfe der statistischen Signifikanz wird beurteilt, wie wahrscheinlich Unterschiede durch die Abwandlungen sind, nicht jedoch die Wahrscheinlichkeit ihres Erfolgs. Daher wird die statistische Signifikanz in Verbindung mit der **Steigerung** verwendet.

Für wirksame Experimente müssen verschiedene Fehlertypen berücksichtigt werden, die zu falschen Rückschlüssen führen können.

![](assets/technote_1.png)

Die obige Tabelle zeigt die verschiedenen Fehlertypen:

* **Falsch-Positiv (Fehler vom Typ I)**: ist eine falsche Zurückweisung der Nullhypothese, obwohl sie in Wirklichkeit wahr ist. Im Kontext von Online-Experimenten bedeutet dies, dass wir fälschlicherweise zu dem Schluss kommen, dass die Ergebniskennzahl zwischen den einzelnen Abwandlungen unterschiedlich ist, obwohl sie identisch war.
  </br>Bevor wir das Experiment durchführen, wählen wir normalerweise einen Schwellenwert `\alpha`. Nachdem das Experiment ausgeführt wurde, wird der `p-value` berechnet, und wenn er über dem Schwellenwert liegt, weisen wir die Nullhypothese zurück (nicht `null if p < \alpha`). Die Wahl von `/alpha` basiert auf den Konsequenzen einer falschen Antwort, so könnte man sich z. B. in einer klinischen Studie, in der das Leben eines Menschen betroffen sein könnte, für ein `\alpha = 0.005` entscheiden. Ein häufig verwendeter Schwellenwert bei Online-Experimenten ist `\alpha = 0.05`, was bedeutet, dass auf lange Sicht 5 von 100 Experimenten als falsch-positiv eingestuft werden.

* **Falsch-Negativ (Fehler vom Typ II)**: bedeutet, dass wir die Nullhypothese nicht zurückweisen, obwohl sie falsch ist. Bei Experimenten bedeutet dies, dass wir die Nullhypothese nicht ablehnen, obwohl sie in Wirklichkeit anders ist. Um diesen Fehlertyp zu kontrollieren, müssen wir im Allgemeinen genügend Teilnehmende in unserem Experiment haben, um eine bestimmte Aussagekraft (Power) zu gewährleisten, die als `1 - \beta` (d. h. 1 minus die Wahrscheinlichkeit eines Fehlers vom Typ II) definiert ist.

Bei den meisten statistischen Inferenzverfahren müssen Sie Ihre Stichprobengröße im Voraus festlegen, und zwar auf der Grundlage der Effektgröße, die Sie bestimmen möchten, sowie Ihrer Fehlertoleranz (`\alpha` und `\beta`). Die Methodik von Adobe Journey Optimizer ist jedoch so konzipiert, dass Sie Ihre Ergebnisse kontinuierlich und für jede Stichprobengröße überprüfen können.

## Die statistische Methodik von Adobe: Jederzeit gültige Konfidenzsequenzen

Eine **Konfidenzsequenz** ist ein sequenzielles Analogon eines **Konfidenzintervalls**, z. B. wenn Sie Ihre Experimente hundertmal wiederholen und eine Schätzung der mittleren Metrik und die zugehörige 95%ige Konfidenzsequenz für jede neue Person berechnen, die an dem Experiment teilnimmt. Eine 95%ige Konfidenzsequenz beinhaltet den wahren Wert der Metrik in 95 von 100 Experimenten, die Sie durchgeführt haben. Ein 95%-Konfidenzintervall kann nur einmal pro Experiment berechnet werden, um denselben Abdeckungsgrad von 95 % zu gewährleisten, und nicht bei jeder einzelnen neuen Person. Konfidenzsequenzen ermöglichen daher eine kontinuierliche Überwachung der Experimente, ohne die Falsch-Positiv-Fehlerrate zu erhöhen.

Der Unterschied zwischen Konfidenzsequenzen und Konfidenzintervallen für ein einzelnes Experiment ist in der nachstehenden Animation dargestellt:

![](assets/technote_2.gif)

**Konfidenzsequenzen** verlagern den Schwerpunkt der Experimente auf die Schätzung und nicht auf die Hypothesenprüfung, d. h. sie konzentrieren sich auf die genaue Schätzung des Unterschieds der Mittelwerte zwischen den Abwandlungen und nicht auf die Frage, ob eine Nullhypothese auf der Grundlage eines Schwellenwerts für die statistische Signifikanz verworfen werden soll oder nicht.

Ähnlich wie bei der Beziehung zwischen `p-values`, oder **Konfidenz**, und **Konfidenzintervallen** gibt es jedoch auch eine Beziehung zwischen **Konfidenzsequenzen** und jederzeit gültigen `p-values` bzw. jederzeit gültiger Konfidenz. Angesichts der Bekanntheit von Größen wie der Konfidenz gibt Adobe in seinen Berichten sowohl die **Konfidenzsequenzen** als auch die jederzeit gültige Konfidenz an.

Die theoretischen Grundlagen der **Konfidenzsequenzen** stammen aus der Untersuchung von Sequenzen von Zufallsvariablen, die als Martingale bekannt sind. Einige wichtige Ergebnisse werden im Folgenden für Fortgeschrittene aufgeführt, aber die Schlussfolgerungen für Fachleute sind offensichtlich:

>[!NOTE]
>
>Konfidenzsequenzen können als sichere sequenzielle Analoga von Konfidenzintervallen interpretiert werden. Mit Konfidenzintervallen können Sie das Experiment erst interpretieren, wenn die vordefinierte Stichprobengröße erreicht wurde. Mit Konfidenzsequenzen können Sie Daten jedoch jederzeit in Ihren Experimenten betrachten und interpretieren sowie Experimente sicher stoppen oder fortsetzen. Der entsprechende jederzeit gültige Konfidenzwert, auch `p-value` genannt, kann ebenfalls immer sicher interpretiert werden.

Es ist wichtig zu beachten, dass Konfidenzsequenzen, da sie „jederzeit gültig“ sind, konservativer sind als eine Methodik mit festem Zeithorizont, die bei gleichem Stichprobenumfang verwendet wird. Die Grenzen der Konfidenzsequenzen sind im Allgemeinen breiter als die einer Konfidenzintervallberechnung, während die jederzeit gültige Konfidenz kleiner ist als eine Konfidenzberechnung mit festem Horizont. Der Vorteil dieses Konservatismus besteht darin, dass Sie Ihre Ergebnisse jederzeit sicher interpretieren können.

## Ein Experiment für schlüssig erklären

![](assets/experimentation_report_2.png)

Jedes Mal, wenn Sie sich den Experimentbericht anzeigen lassen, analysiert Adobe die Daten, die sich bis zu diesem Zeitpunkt im Experiment angesammelt haben, und erklärt ein Experiment als „schlüssig“, wenn die jederzeit gültige Konfidenz einen Schwellenwert von 95 % für mindestens eine der Abwandlungen überschreitet.

Zu diesem Zeitpunkt wird die Abwandlung, die die beste Leistung aufweist (basierend auf der Konversionsrate oder dem profilnormierten Metrikwert), am oberen Rand des Berichtsbildschirms hervorgehoben und im tabellarischen Bericht mit einem Stern gekennzeichnet. Nur Abwandlungen, die eine Konfidenz von mehr als 95 % aufweisen, sowie die Baseline werden bei dieser Bestimmung berücksichtigt.

Wenn es mehr als zwei Abwandlungen gibt, wird die Verknüpfung mit der Bonferroni-Korrektur verwendet, um Probleme mit Mehrfachvergleichen zu korrigieren und die familienspezifische Fehlerquote zu kontrollieren. In diesem Szenario ist es auch möglich, dass es mehrere Abwandlungen gibt, deren Konfidenz größer als 95 % ist und deren Konfidenzintervalle sich überschneiden. In diesem Fall erklärt Adobe Journey Optimizer die Behandlung mit der höchsten Konversionsrate (oder dem höchsten profilnormierten Metrikwert) zum besten Ergebnis.
