---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit dem Inhaltsexperiment
description: Weitere Informationen zum Experimentieren mit Inhalten finden Sie unter [!DNL Journey Optimizer]
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 0%

---

# Erste Schritte mit Inhaltsexperimenten {#get-started-experiment}

>[!AVAILABILITY]
>
>Die Funktion &quot;Inhaltserfahrung&quot;ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.

## Was ist ein Inhaltsexperiment?

Mit Inhaltsexperimenten können Sie Inhalte für die Aktionen in Ihren Kampagnen optimieren.

Bei Experimenten handelt es sich um eine Reihe von randomisierten Prüfungen, was im Rahmen von Online-Tests bedeutet, dass einige zufällig ausgewählte Benutzer einer bestimmten Variante einer Nachricht ausgesetzt sind und eine andere zufällig ausgewählte Gruppe von Benutzern einer anderen Behandlung unterzogen wird. Nach dem Versand der Nachricht können Sie dann die Ergebnismetriken messen, die Sie interessieren, z. B. Öffnungen von E-Mails oder Klicks.

## Warum sollten Experimente ausgeführt werden?

![](assets/content_experiment_schema.png)

Mit Experimenten können Sie die Änderungen isolieren, die zu Verbesserungen in Ihren Metriken führen. Wie in der Abbildung oben dargestellt: Einige zufällig ausgewählte Benutzer sind jeder Behandlungsgruppe ausgesetzt, was bedeutet, dass die Gruppen im Durchschnitt dieselben Merkmale aufweisen. So kann jeder Unterschied in den Ergebnissen so interpretiert werden, dass er auf die Unterschiede in den Behandlungen zurückzuführen ist, d.h. Sie können einen kausalen Zusammenhang zwischen den vorgenommenen Änderungen und den Ergebnissen, die Sie interessiert sind, herstellen.

Auf diese Weise können Sie datenbasierte Entscheidungen zur Optimierung Ihrer Geschäftsziele treffen.

Für Inhaltstests in Adobe Journey Optimizer können Sie Ideen testen, z. B.:

* **Betreff**: Wie könnte sich eine Änderung des Tons oder des Personalisierungsgrads einer Betreffzeile auswirken?
* **Nachrichteninhalt**: Führt eine Änderung des visuellen Layouts einer E-Mail zu mehr Klicks auf die E-Mail?

## Wie funktioniert das Inhaltsexperiment? {#content-experiment-work}

### Zufällige Zuweisung

Inhaltsexperimentierung in Adobe Journey Optimizer verwendet einen pseudo-zufälligen Hash der Besucheridentität, um eine zufällige Zuweisung von Benutzern in Ihrer Zielgruppe zu einer der von Ihnen definierten Behandlungen durchzuführen. Der Hash-Mechanismus stellt sicher, dass in Szenarien, in denen der Besucher mehrmals an einer Kampagne teilnimmt, er deterministisch dieselbe Behandlung erhält.

Im Detail wird der 32-Bit-Algorithmus MumurHash3 verwendet, um die Benutzeridentitätszeichenfolge in einen von 10.000 Buckets zu hashen. In einem Inhaltsexperiment mit 50 % des Traffics, der jeder Behandlung zugeordnet wird, erhalten Benutzer, die in Behälter 1 bis 5.000 fallen, die erste Behandlung, während Benutzer in den Buckets 5.001 bis 10.000 die zweite Behandlung erhalten. Da Pseudozufall-Hashing verwendet wird, ist der Besucher, wie Sie feststellen, möglicherweise nicht genau 50-50. Die Aufteilung entspricht dennoch statistisch Ihrem Zielaufteilungsprozentsatz.

Beachten Sie, dass Sie bei der Konfiguration jeder Kampagne mit einem Inhaltsexperiment einen Identitäts-Namespace auswählen müssen, aus dem die userId für den Randomisierungsalgorithmus ausgewählt wird. Dies ist unabhängig von der [Ausführungsadressen](../configuration/primary-email-addresses.md).

### Datenerfassung und Analyse

Zum Zeitpunkt der Zuweisung, d. h. wenn die Nachricht in ausgehenden Kanälen gesendet wird oder wenn der Benutzer die Kampagne in eingehenden Kanälen betritt, wird ein &quot;Zuweisungsdatensatz&quot;im entsprechenden Systemdatensatz protokolliert. Dadurch wird aufgezeichnet, welcher Behandlung der Benutzer zugewiesen wurde, sowie Experiment- und Kampagnen-IDs.

Zielmetriken können in zwei Hauptklassen gruppiert werden:

* Direkte Metriken, bei denen der Benutzer direkt auf die Behandlung reagiert, z. B. beim Öffnen einer E-Mail oder Klicken auf einen Link.
* Indirekte oder &quot;untere Trichtermetriken&quot;, die auftreten, nachdem der Benutzer der Behandlung ausgesetzt wurde.

Bei direkten objektiven Metriken, bei denen Adobe Journey Optimizer Ihre Nachrichten verfolgt, werden die Antwortereignisse der Endbenutzer automatisch mit den Kampagnen- und Behandlungs-IDs getaggt, was eine direkte Verknüpfung der Antwortmetrik mit einer Behandlung ermöglicht. [Erfahren Sie mehr über Tracking](../email/message-tracking.md).

![](assets/technote_2.png)

Bei indirekten oder &quot;untergeordneten&quot;Zielen wie Käufen werden die Antwortereignisse der Endbenutzer nicht mit Kampagnen- und Behandlungs-IDs versehen, d. h., ein Kaufereignis tritt nach der Exposition gegenüber einer Behandlung auf. Dieser Kauf ist nicht direkt mit einer Vorbehandlungszuweisung verbunden. Für diese Metriken ordnet Adobe die Behandlung dem untersten Trichterkonversionsereignis zu, wenn:

* Die Benutzeridentität ist zum Zeitpunkt der Zuweisung und Konversionsereignisse identisch.
* Die Konversion erfolgt innerhalb von sieben Tagen nach der Behandlungszuweisung.

![](assets/technote_3.png)

Adobe Journey Optimizer verwendet dann erweiterte statistische Methoden, die jederzeit gültig sind, um diese Rohdaten für die Berichterstellung zu interpretieren, mit denen Sie Ihre Experimentationsberichte interpretieren können. Weitere Informationen hierzu finden Sie unter [diese Seite](../campaigns/experiment-calculations.md).

## Tipps zum Ausführen von Experimenten

Beim Ausführen von Experimenten ist es wichtig, bestimmte Best Practices zu befolgen. Im Folgenden finden Sie einige Tipps zum Ausführen dieser Experimente:

+++Isolieren der Variablen, die Sie testen möchten

Formulieren Sie einige Hypothesen, die Sie testen möchten, und beschränken Sie diese Hypothese auf möglichst wenige Änderungen, um festzustellen, welche Auswirkungen auf Ihren Versand erzielt wurden.

Eine gute Hypothese kann beispielsweise sein, ob eine Personalisierung in E-Mail-Betreffzeilen zu besseren Öffnungsraten führt. Das Hinzufügen einer Änderung des Nachrichteninhalts oder von Bildern kann jedoch zu einer verwirrenden Schlussfolgerung führen.
+++

+++ Stellen Sie sicher, dass Sie die richtige Metrik verwenden

Bestimmen Sie die Metrik, die Sie als Ziel auswählen möchten, und ob die von Ihnen vorgenommenen Änderungen direkte Auswirkungen auf diese Metrik haben können.

So ist es beispielsweise unwahrscheinlich, dass sich eine Änderung des Inhalts des Nachrichtentextes auf die Öffnungsraten der E-Mail auswirkt.
+++

+++ Führen Sie Ihren Test für die richtige Zielgruppengröße oder lange genug aus.

Wenn Sie Ihre Tests länger ausführen, können Sie kleinere Unterschiede in der Zielmetrik zwischen den Behandlungen erkennen. Wenn der Ausgangswert Ihrer Zielmetrik jedoch klein ist, benötigen Sie größere Stichprobengrößen.
Die Anzahl der Benutzer, die in Ihr Experiment aufgenommen werden müssen, hängt von der zu erkennenden Effektgröße, der Varianz oder Verbreitung Ihrer Zielmetrik sowie von Ihrer Toleranz für falsch-positive und falsch-negative Fehler ab. In klassischen Experimenten können Sie eine [Stichprobengrößenrechner](https://experienceleague.adobe.com/tools/calculator/testcalculator.html){_blank}, um zu bestimmen, wie lange Sie Ihren Test ausführen müssen.
+++

+++Statistische Unsicherheit verstehen

Wenn Sie ein Experiment durchführen, bei dem 1000 Benutzer eine Behandlung gesehen haben und die Konversionsrate auf 5 % eingestellt ist. Wäre dies die tatsächliche Konversionsrate, wenn alle Ihre Benutzer einbezogen würden? Wie lautet die wahre Konversionsrate?
Statistische Methoden geben uns eine Möglichkeit, diese Unsicherheit zu formalisieren. Eines der wichtigsten Konzepte, das bei der Durchführung von Online-Experimenten zu verstehen ist, ist, dass die beobachteten Konversionsraten mit einer Reihe zugrunde liegender realer Konversionsraten übereinstimmen. Daher müssen Sie warten, bis diese Schätzungen präzise genug sind, bevor Sie versuchen, eine Schlussfolgerung zu ziehen. Konfidenzintervalle und Konfidenz helfen uns, diese Unsicherheit zu quantifizieren.
+++

+++ Erstellen Sie neue Hypothesen und testen Sie sie kontinuierlich.

Um echte geschäftliche Einblicke zu gewinnen, sollten Sie nur an einem Experiment festhalten. Führen Sie stattdessen Experimente durch, indem Sie neue Hypothesen formulieren und neue Tests mit unterschiedlichen Änderungen durchführen, verschiedene Segmente betrachten und die Auswirkungen auf die verschiedenen Metriken untersuchen.
+++

## Interpretieren der Ergebnisse Ihrer Experimente {#interpret-results}

![](assets/experimentation_report_3.png)

In diesem Abschnitt werden die Experimentberichte beschrieben und wie Sie die verschiedenen statistischen Mengen verstehen, die angezeigt werden.

Im Folgenden finden Sie einige Richtlinien für die Interpretation der Ergebnisse Ihres Inhaltserlebnisses.

Beachten Sie, dass bei einer vollständigen Beschreibung der Ergebnisse alle verfügbaren Nachweise berücksichtigt werden sollten (d. h. Stichprobengrößen, Konversionsraten, Konfidenzintervalle usw.) und nicht nur die endgültige Erklärung. Selbst wenn ein Ergebnis noch nicht schlüssig ist, kann es dennoch überzeugende Beweise dafür geben, dass eine Behandlung anders ist als eine andere.

Statistische Berechnungen werden in diesem Abschnitt erläutert [page](../campaigns/experiment-calculations.md).

### 1. Vergleich normalisierter Metriken {#normalized-metrics}

Wenn Sie die Leistung von zwei Behandlungen vergleichen, sollten Sie immer die normalisierten Metriken vergleichen, um Unterschiede in der Anzahl der Profile zu berücksichtigen, die jeder Behandlung ausgesetzt sind.

Wenn das Experimentziel beispielsweise auf **[!UICONTROL Unique Opens]** und eine bestimmte Behandlung 10.000 Profile mit 200 aufgezeichneten Einzelöffnungen angezeigt wurde, stellt dies einen **[!UICONTROL Conversion Rate]** von 2 %. Bei nicht eindeutigen Metriken, z. B. der Öffnungs-Metrik, wird die normalisierte Metrik als **[!UICONTROL Count per Profile]**, während bei kontinuierlichen Metriken wie &quot;Preissumme&quot;die normalisierte Metrik als **[!UICONTROL Total per Profile]**.

### 2. Konfidenzintervalle {#confidence-intervals}

Wenn Sie Experimente mit Beispielen Ihrer Profile durchführen, stellt die für eine bestimmte Behandlung beobachtete Konversionsrate eine Schätzung der zugrunde liegenden tatsächlichen Konversionsrate dar.

Wenn beispielsweise die Behandlung A eine **[!UICONTROL Conversion Rate]** 3%, während die Behandlung B beobachtet wurde **[!UICONTROL Conversion Rate]** von 2%, ist die Behandlung A besser als die Behandlung B? Um dies zu beantworten, müssen wir zunächst die Unsicherheit bei diesen beobachteten Konversionsraten quantifizieren.

Konfidenzintervalle helfen bei der Quantifizierung der Unsicherheit in den geschätzten Konversionsraten, aber größere Konfidenzintervalle bedeuten mehr Unsicherheit. Je mehr Profile zum Experiment hinzugefügt werden, desto kleiner werden die Intervalle, die eine präzisere Schätzung darstellen. Das Konfidenzintervall stellt einen Bereich von Konversionsraten dar, die mit den beobachteten Daten kompatibel sind.

Wenn sich die Konfidenzintervalle für zwei Behandlungen kaum überschneiden, bedeutet dies, dass die beiden Behandlungen unterschiedliche Konversionsraten aufweisen. Wenn es jedoch eine große Überschneidung zwischen den Konfidenzintervallen für zwei Behandlungen gibt, ist es wahrscheinlicher, dass die beiden Behandlungen dieselbe Konversionsrate aufweisen.

Adobe verwendet 95 % beliebige gültige Konfidenzintervalle oder Konfidenzsequenzen, was bedeutet, dass die Ergebnisse jederzeit während des Experiments sicher angezeigt werden können.

### 3. Steigerungen verstehen {#understand-lift}

Die Zusammenfassung des Experimentberichts zeigt die **[!UICONTROL Lift over Baseline]**, das einen Messwert für die prozentuale Verbesserung der Konversionsrate einer bestimmten Behandlung im Vergleich zum Ausgangswert darstellt. Es ist genau definiert, der Leistungsunterschied zwischen einer bestimmten Behandlung und der Grundlinie, geteilt durch die Leistung der Grundlinie, ausgedrückt als Prozentsatz.

### 3. Vertrauen verstehen {#understand-confidence}

Während Sie sich in erster Linie auf die **[!UICONTROL Confidence interval]** für die Leistung jeder Behandlung zeigt Adobe auch die Konfidenz an, die ein probabilistischer Messwert dafür ist, wie viele Beweise dafür vorliegen, dass eine bestimmte Behandlung mit der Basisbehandlung identisch ist. Ein höheres Konfidenzniveau deutet auf weniger Anzeichen für die Annahme hin, dass die Basistherapie und die Behandlung außerhalb des Ausgangswerts die gleiche Leistung aufweisen. Genauer gesagt ist das angezeigte Vertrauen eine Wahrscheinlichkeit (ausgedrückt als Prozentsatz), dass wir einen kleineren Unterschied in den Konversionsraten zwischen einer bestimmten Behandlung und der Grundlinie beobachtet hätten, wenn in Wirklichkeit kein Unterschied in den zugrunde liegenden tatsächlichen Konversionsraten besteht. In Bezug auf p-Werte ist die angezeigte Konfidenz 1 - p-Wert.

Adobe verwendet &quot;Anytime Valid&quot;-Konfidenz und &quot;Anytime Valid&quot;-p-Werte, die mit den oben beschriebenen Konfidenzsequenzen konsistent sind.

### 4. Statistische Bedeutung

Beim Ausführen von Experimenten wird ein Ergebnis als statistisch signifikant betrachtet, wenn sehr unwahrscheinlich war, dass es mit einer Nullhypothese beobachtet wurde, dass eine bestimmte Behandlung und die Grundlinie identische zugrunde liegende Konversionsraten/Leistungen aufweisen.

Adobe erklärt ein Experiment als abgeschlossen, wenn die Konfidenz über 95 % liegt.

## Vorgehensweise nach dem Ausführen eines Experiments

Nach dem Ausführen Ihres Experiments gibt es mehrere mögliche Folgeaktionen:

* **Gewinnerideen bereitstellen**

   Mit einem eindeutigen Ergebnis können Sie diese Gewinneridee bereitstellen, indem Sie entweder all Ihren Kunden die beste Behandlung zukommen lassen oder indem Sie neue Kampagnen erstellen, in denen die Struktur der Behandlung mit der besten Leistung repliziert wird.
   </br>Beachten Sie, dass in einer dynamischen Umgebung das, was gleichzeitig gut funktioniert, später möglicherweise nicht mehr gut funktioniert.

* **Ausführen von Folgetests**

   Manchmal sind die Ergebnisse Ihrer Experimente nicht eindeutig, entweder weil nicht genügend Profile vorhanden waren, um einen Unterschied bei den Behandlungen zu erkennen, oder weil die von Ihnen definierten Behandlungen nicht ausreichend unterschiedlich waren.

   Wenn die Hypothese, die Sie getestet haben, weiterhin relevant ist, führen Sie einen Follow-up-Test für eine größere oder andere Zielgruppe durch oder ändern Sie Ihre Behandlungen so, dass klarere Unterschiede vorliegen, um die beste Folgeaktion zu sein.

* **Detailliertere Tauchanalysen durchführen**

   Die Behandlung, die für eine Zielgruppe gut funktioniert, kann manchmal nicht die beste Behandlung für eine andere Zielgruppe sein. Durch tiefere Analysen darüber, wie sich Behandlungen für verschiedene Segmente verhalten, können Ideen für neue Tests generiert werden.

   Ebenso kann die Untersuchung der Leistung jeder Behandlung mit verschiedenen Metriken auch einen umfassenderen Überblick über Ihre Experimente geben.

   >[!CAUTION]
   >
   >Mehr Analysen bedeuten eine höhere Wahrscheinlichkeit, einen falschen oder falsch positiven Effekt zu erkennen.
