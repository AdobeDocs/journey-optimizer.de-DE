---
title: Von Adobe Journey Optimizer Experimentation verwendete statistische Berechnungen
description: Erfahren Sie mehr über statistische Berechnungen, die bei der Durchführung von Experimenten verwendet werden
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: f0e2f80a815aebb7574582fbf33770aa5da0abab
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 93%

---

# Verstehen von statistischen Berechnungen {#experiment-calculations}

>[!AVAILABILITY]
>
>Die **Inhaltstest** ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie beim Adobe-Support.

Dieser Artikel beschreibt die statistischen Berechnungen, die bei der Durchführung von Experimenten in Adobe Journey Optimizer verwendet werden.

Experimente verwenden fortschrittliche statistische Methoden zur Berechnung von **Konfidenzsequenzen** und **Konfidenz**, die es Ihnen ermöglichen, Ihre Experimente so lange wie nötig durchzuführen und Ihre Ergebnisse kontinuierlich zu überwachen.

Dieser Artikel beschreibt die Funktionsweise von Experimenten und bietet eine intuitive Einführung in die **jederzeit gültigen Konfidenzsequenzen** von Adobe.

Für erfahrene Benutzende sind die technischen Details und Referenzen auf [dieser Seite](../campaigns/assets/confidence_sequence_technical_details.pdf) aufgeführt.

## Statistische Tests und Fehlerkontrolle {#statistical-testing}

![](assets/technote_1.png)

Wie in der obigen Tabelle dargestellt, sind viele statistische Herleitungsmethoden darauf ausgelegt, zwei Arten von Fehlern zu kontrollieren:

* **Falsch-Positiv (Fehler vom Typ I)**: ist eine falsche Zurückweisung der Nullhypothese, obwohl sie in Wirklichkeit wahr ist. Im Kontext von Online-Experimenten bedeutet dies, dass wir fälschlicherweise zu dem Schluss kommen, dass die Ergebniskennzahl zwischen den einzelnen Behandlungen unterschiedlich ist, obwohl sie identisch war.
   </br>Bevor wir das Experiment durchführen, wählen wir normalerweise einen Schwellenwert `\alpha`. Nach der Durchführung des Experiments wird der `p-value` berechnet, und `null if p < \alpha` wird verworfen. Ein häufig verwendeter Schwellenwert ist `\alpha = 0.05`, was bedeutet, dass auf lange Sicht 5 von 100 Experimenten als falsch positiv eingestuft werden.

* **Falsch-Negativ (Fehler vom Typ II)**: bedeutet, dass wir die Nullhypothese nicht zurückweisen, obwohl sie falsch ist. Bei Experimenten bedeutet dies, dass wir die Nullhypothese nicht ablehnen, obwohl sie in Wirklichkeit anders ist. Um diesen Fehlertyp zu kontrollieren, müssen wir im Allgemeinen genügend Teilnehmende in unserem Experiment haben, um eine bestimmte Aussagekraft (Power) zu gewährleisten, die als `1 - \beta` (d. h. 1 minus die Wahrscheinlichkeit eines Fehlers vom Typ II) definiert ist.

Bei den meisten statistischen Inferenzverfahren müssen Sie Ihre Stichprobengröße im Voraus festlegen, und zwar auf der Grundlage der Effektgröße, die Sie bestimmen möchten, sowie Ihrer Fehlertoleranz (`\alpha` und `\beta`). Die Methodik von Adobe Journey Optimizer ist jedoch so konzipiert, dass Sie Ihre Ergebnisse kontinuierlich und für jede Stichprobengröße überprüfen können.

## Die statistische Methodik von Adobe: Jederzeit gültige Konfidenzsequenzen

Eine **Konfidenzsequenz** ist ein sequenzielles Analogon eines **Konfidenzintervalls**, z. B. wenn Sie Ihre Experimente hundertmal wiederholen und eine Schätzung der mittleren Metrik und die zugehörige 95%ige Konfidenzsequenz für jede neue Person berechnen, die an dem Experiment teilnimmt. Eine 95%ige Konfidenzsequenz beinhaltet den wahren Wert der Metrik in 95 von 100 Experimenten, die Sie durchgeführt haben. Ein 95%-Konfidenzintervall kann nur einmal pro Experiment berechnet werden, um denselben Abdeckungsgrad von 95 % zu gewährleisten, und nicht bei jeder einzelnen neuen Person. Konfidenzsequenzen ermöglichen daher eine kontinuierliche Überwachung der Experimente, ohne die Falsch-Positiv-Fehlerrate zu erhöhen.

Der Unterschied zwischen Konfidenzsequenzen und Konfidenzintervallen für ein einzelnes Experiment ist in der nachstehenden Animation dargestellt:

![](assets/technote_2.gif)

**Konfidenzsequenzen** verlagern den Schwerpunkt der Experimente auf die Schätzung und nicht auf die Hypothesenprüfung, d. h. sie konzentrieren sich auf die genaue Schätzung des Unterschieds der Mittelwerte zwischen den Behandlungen und nicht auf die Frage, ob eine Nullhypothese auf der Grundlage eines Schwellenwerts für die statistische Signifikanz verworfen werden soll oder nicht.

Ähnlich wie bei der Beziehung zwischen `p-values`, oder **Konfidenz**, und **Konfidenzintervallen** gibt es jedoch auch eine Beziehung zwischen **Konfidenzsequenzen** und jederzeit gültigen `p-values` bzw. jederzeit gültiger Konfidenz. Angesichts der Bekanntheit von Größen wie der Konfidenz gibt Adobe in seinen Berichten sowohl die **Konfidenzsequenzen** als auch die jederzeit gültige Konfidenz an.

Die theoretischen Grundlagen der **Konfidenzsequenzen** stammen aus der Untersuchung von Sequenzen von Zufallsvariablen, die als Martingale bekannt sind. Einige wichtige Ergebnisse werden im Folgenden für Fortgeschrittene aufgeführt, aber die Schlussfolgerungen für Fachleute sind offensichtlich:

>[!NOTE]
>
>Konfidenzsequenzen können als sichere sequentielle Analoga von Konfidenzintervallen interpretiert werden. Mit ihnen können Sie die Daten in Ihren Experimenten jederzeit betrachten und interpretieren und Experimente sicher stoppen oder fortsetzen. die entsprechende &quot;Beliebige Zeit gültige Konfidenz&quot;oder `p-value`, ist auch sicher zu interpretieren.

Es ist wichtig zu beachten, dass Konfidenzsequenzen, da sie „jederzeit gültig“ sind, konservativer sind als eine Methodik mit festem Zeithorizont, die bei gleichem Stichprobenumfang verwendet wird. Die Grenzen der Konfidenzsequenzen sind im Allgemeinen breiter als die einer Konfidenzintervallberechnung, während die jederzeit gültige Konfidenz kleiner ist als eine Konfidenzberechnung mit festem Horizont. Der Vorteil dieses Konservatismus besteht darin, dass Sie Ihre Ergebnisse jederzeit sicher interpretieren können.

## Ein Experiment für schlüssig erklären

![](assets/experimentation_report_2.png)

Jedes Mal, wenn Sie sich den Experimentbericht anzeigen lassen, analysiert Adobe die Daten, die sich bis zu diesem Zeitpunkt im Experiment angesammelt haben, und erklärt ein Experiment als „schlüssig“, wenn die jederzeit gültige Konfidenz einen Schwellenwert von 95 % für mindestens eine der Behandlungen überschreitet.

Zu diesem Zeitpunkt wird die Behandlung, die die beste Leistung aufweist (basierend auf der Konversionsrate oder dem profilnormierten Metrikwert), am oberen Rand des Berichtsbildschirms hervorgehoben und im tabellarischen Bericht mit einem Stern gekennzeichnet. Nur Behandlungen, die eine Konfidenz von mehr als 95 % aufweisen, sowie die Grundlinie werden bei dieser Bestimmung berücksichtigt.

Wenn es mehr als zwei Behandlungen gibt, wird die Verknüpfung mit der Bonferroni-Korrektur verwendet, um Probleme mit Mehrfachvergleichen zu korrigieren und die familienspezifische Fehlerquote zu kontrollieren. In diesem Szenario ist es auch möglich, dass es mehrere Behandlungen gibt, deren Konfidenz größer als 95 % ist und deren Konfidenzintervalle sich überschneiden. In diesem Fall deklariert Adobe Journey Optimizer die mit der höchsten Konversionsrate (oder dem profilnormalisierten Metrikwert) als die leistungsstärkste.
