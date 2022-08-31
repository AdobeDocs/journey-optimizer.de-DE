---
title: Durch Experimentierung verwendete statistische Berechnungen
description: Erfahren Sie mehr über statistische Berechnungen, die beim Ausführen von Experimenten verwendet werden
feature: Overview
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 2%

---

# Verstehen von statistische Berechnungen {#experiment-calculations}

>[!AVAILABILITY]
>
>Die Funktion für Inhaltsexperimente ist derzeit nur für eine Reihe von ausgewählten Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie bei Ihrer Adobe-Support-Person.

In diesem Artikel werden die statistischen Berechnungen beschrieben, die beim Ausführen von Experimenten in Adobe Journey Optimizer verwendet werden. Experimente verwenden erweiterte statistische Methoden zur Berechnung **Konfidenzsequenzen** und **Konfidenz**, mit denen Sie Ihre Experimente so lange wie nötig ausführen und Ihre Ergebnisse kontinuierlich überwachen können.

In diesem Artikel wird beschrieben, wie die Experimentierung funktioniert, und es wird eine intuitive Einführung in die Adobe bereitgestellt. **Beliebige zeitgültige Konfidenzsequenzen**.

Für erfahrene Benutzer werden die technischen Details und Referenzen im Abschnitt [diese Seite](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Statistische Tests und Fehlerkontrolle {#statistical-testing}

![](assets/technote_1.png)

Wie in der obigen Tabelle dargestellt, dienen viele statistische Aufschlussmethoden dazu, zwei Arten von Fehlern zu beheben:

* **Falsch positive Werte (Fehler vom Typ I)**: ist eine falsche Zurückweisung der Nullhypothese, obwohl sie tatsächlich wahr ist. Im Kontext von Online-Experimenten bedeutet dies, dass wir fälschlicherweise zu dem Schluss kommen, dass die Ergebnismetrik zwischen den einzelnen Behandlungen unterschiedlich ist, obwohl sie identisch war.
   </br>Bevor wir das Experiment durchführen, wählen wir normalerweise einen Schwellenwert aus `\alpha`. Nachdem das Experiment ausgeführt wurde, wird die `p-value` berechnet wird und wir lehnen die `null if p < \alpha`. Ein häufig verwendeter Schwellenwert ist `\alpha = 0.05`, was bedeutet, dass wir auf lange Sicht erwarten, dass 5 von 100 Experimenten falsch-positive Ergebnisse sind.

* **False Negative (Fehler vom Typ II)**: bedeutet, dass wir die Null-Hypothese nicht zurückweisen, obwohl sie falsch ist. Für Experimente bedeutet dies, dass wir die Null-Hypothese nicht ablehnen, obwohl sie tatsächlich anders ist. Um diesen Fehlertyp zu steuern, müssen wir im Allgemeinen genügend Benutzer in unserem Experiment haben, um eine bestimmte Leistung zu garantieren, die wie folgt definiert ist: `1 - \beta`(d. h. eins abzüglich der Wahrscheinlichkeit eines Fehlers vom Typ II).

Die meisten statistischen Erkennungsverfahren erfordern, dass Sie Ihre Stichprobengröße vorzeitig anhand der zu bestimmenden Effektgröße sowie Ihrer Fehlertoleranz (`\alpha` und `\beta`). Die Adobe Journey Optimizer-Methode ist jedoch so konzipiert, dass Sie Ihre Ergebnisse kontinuierlich für jede Stichprobengröße betrachten können.

## Statistische Methode der Adobe: Beliebige zeitgültige Konfidenzsequenzen

A **Konfidenzsequenz** ist ein sequenzielles Analogon eines **Konfidenzintervall**, z. B. wenn Sie Ihre Experimente hundertmal wiederholen und eine Schätzung der durchschnittlichen Metrik und der zugehörigen 95-%-Konfidenzsequenz für jeden neuen Benutzer berechnen, der in das Experiment eintritt. Eine Konfidenzsequenz von 95 % enthält den wahren Wert der Metrik in 95 der 100 Experimente, die Sie ausgeführt haben. Ein Konfidenzintervall von 95 % konnte nur einmal pro Versuch berechnet werden, um die gleiche 95-%-Garantie zu erhalten. nicht bei jedem neuen Benutzer. Konfidenzsequenzen ermöglichen es Ihnen daher, Experimente kontinuierlich zu überwachen, ohne die Falsch-Positiv-Fehlerrate zu erhöhen.

Der Unterschied zwischen Konfidenzsequenzen und Konfidenzintervallen für ein einzelnes Experiment ist in der nachstehenden Animation dargestellt:

![](assets/technote_2.gif)

**Konfidenzsequenzen** den Schwerpunkt von Experimenten auf Schätzungen statt auf Hypothesentests zu verlagern, d. h. auf eine genaue Schätzung des Unterschieds der Mittel zwischen den Behandlungen, anstatt darauf zu achten, ob eine Null-Hypothese basierend auf einem Schwellenwert für statistische Bedeutung zurückgewiesen wird oder nicht.

In ähnlicher Weise wie die Beziehung zwischen `p-values`oder **Konfidenz** und **Konfidenzintervalle**, gibt es auch eine Beziehung zwischen **Konfidenzsequenzen** und jeder beliebigen Zeit `p-values`oder jedes beliebige gültige Vertrauen. Angesichts der Vertrautheit von Mengen wie der Konfidenz bietet die Adobe sowohl die **Konfidenzsequenzen** und jedes Mal gültige Vertrauen in die Berichte.

Die theoretischen Grundlagen von **Konfidenzsequenzen** Sie stammen aus der Untersuchung von Sequenzen von zufälligen Variablen, die als Martingales bezeichnet werden. Im Folgenden werden einige wichtige Ergebnisse für erfahrene Leser vorgestellt, aber die Handlungsmöglichkeiten der Praktiker sind klar:

>[!NOTE]
>
>Konfidenzsequenzen können als sichere sequenzielle Analoga von Konfidenzintervallen interpretiert werden. Sie können Daten in Ihren Experimenten jederzeit ansehen und interpretieren sowie sicher stoppen oder Experimente fortsetzen. die entsprechende &quot;Beliebige Zeit gültige Konfidenz&quot;oder `p-value`, ist auch sicher zu interpretieren.

Da Konfidenzsequenzen &quot;jederzeit gültig&quot;sind, müssen sie konservativer sein als eine feste Horizontmethodik, die bei derselben Stichprobengröße verwendet wird. Die Begrenzungen der Konfidenzsequenz sind im Allgemeinen größer als die eines Konfidenzintervalls, während das jedes Mal gültige Konfidenzintervall kleiner ist als eine feste Horizont-Konfidenzberechnung. Der Vorteil dieses Konservatismus besteht darin, dass Sie Ihre Ergebnisse jederzeit sicher interpretieren können.

## Definieren eines Experiments als abgeschlossen

![](assets/experimentation_report_2.png)

Jedes Mal, wenn Sie den Experimentbericht ansehen, analysiert Adobe die Daten, die bis zu diesem Zeitpunkt im Experiment gesammelt wurden, und deklariert einen Versuch als &quot;Fazit&quot;, wenn die jederzeit gültige Konfidenz für mindestens eine der Behandlungen einen Schwellenwert von 95 % überschreitet.

Zu diesem Zeitpunkt wird die Behandlung, die die beste Leistung erzielt (basierend auf der Konversionsrate oder dem profilnormalisierten Metrikwert), oben im Berichtbildschirm hervorgehoben und mit einem Stern im Tabellenbericht angegeben. Bei dieser Bestimmung werden nur Behandlungen mit einer Konfidenz von mehr als 95 % zusammen mit der Grundlinie berücksichtigt.

Wenn es mehr als zwei Behandlungen gibt, wird der Bonferroni-Korrekturlink verwendet, um mehrere Vergleichsprobleme zu beheben, und die familiäre Fehlerrate wird gesteuert. In diesem Szenario ist es auch möglich, dass es mehrere Behandlungen gibt, deren Konfidenzintervall größer als 95 % ist und deren Konfidenzintervalle sich überschneiden. In diesem Fall erklärt Adobe die mit der höchsten Konversionsrate (oder dem profilnormalisierten Metrikwert) als die leistungsstärkste.
