---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Verbessern Sie Ihre Fähigkeit, Experimente effektiv durchzuführen und Erkenntnisse zu gewinnen
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Zielgruppe, Abwandlung
hide: true
hidefromtoc: true
source-git-commit: e4d5631701c5c270af7aec931f6b98a567b4ed29
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 3%

---

# Erste Schritte mit Experimentation Accelerator {#content-experiment}

>[!BEGINSHADEBOX]

* **[Erste Schritte mit der Experimentation Accelerator](experiment-accelerator.md)**
* [Registerkarte „Experimente“](experiment-accelerator-monitor.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
> Die Experimentation Accelerator befindet sich derzeit in der Beta-Phase, wobei die Funktionen nach und nach eingeführt werden.

**Experimentation Accelerator** ist ein leistungsstarkes Tool zur Optimierung und Verbesserung des Experimentierprozesses. Durch die Integration mit Adobe Target und Adobe Journey Optimizer bietet sie eine zentralisierte Plattform für die Verwaltung, Analyse und Optimierung von Experimenten. Durch die Nutzung KI-gesteuerter Erkenntnisse und adaptiver Tests ermöglicht Ihnen der Experimentation Accelerator datengesteuerte Entscheidungen, verbessert Marketing-Strategien und steigert messbare Ergebnisse.

Zu den wichtigsten Vorteilen gehören:

* **Schnelleres Experimentieren** Führen Sie adaptive, immer aktive Tests mit Modellen durch, die sich im Laufe der Zeit anpassen.

* **Unified Platform**: Verwalten Sie alle Experimente aus Adobe Target und Journey Optimizer an einem Ort.

* **KI-gesteuerte Insights**: Automatisches Aufdecken wichtiger Ergebnisse, Leistungstreiber und neuer Chancen.

* **Intelligenteres Targeting**: Verwenden Sie Verhaltens- und Inhaltsdaten, um Experimente mit hoher Wirkung zu priorisieren.

* **KPI-Überwachung**: Verfolgen Sie Metriken wie Steigerung, Umsatz und Konfidenz in allen Experimenten.

* **Nahtlose Collaboration**: Ergebnisse einfach freigeben und Teamrollen mit Echtzeit-Warnhinweisen verwalten.

Nachdem Sie [Experiment erstellt und konfiguriert ](content-experiment.md) und Ihre Kampagnen oder Journey an Ihre Profile gesendet haben, können Sie auf die **[!UICONTROL Experimentation Accelerator]** zugreifen, um sich eingehender mit der Leistung Ihres Experiments zu befassen.

So greifen Sie auf die **[!UICONTROL Experimentation Accelerator]**:

* Wählen Sie im Menü links **[!UICONTROL Experimentation Accelerator]** in der Dropdown-Liste **[!UICONTROL Experimentieren]** aus.

* Wählen Sie alternativ **[!UICONTROL Experimentation Accelerator]** über den Apps Switcher aus.

Beachten Sie, dass Benutzer mit nur einer Target-Lizenz nur über den Apps Switcher darauf zugreifen können.

<!--
<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="Overview" href="experiment-accelerator-overview.md" src="assets/do-not-localize/experiments-2.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-overview.md">Overview</a></strong></p></div></td>
<td><img alt="Experiments" href="experiment-accelerator-monitor.md" src="assets/do-not-localize/experiment-overview.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-monitor.md">Experiments</a></strong></p></div></td>
<td><img alt="Metrics" href="experiment-accelerator-metrics.md" src="assets/do-not-localize/experiment-metrics.png">
<div align="center"><p><strong><a href="experiment-accelerator-metrics.md">Metrics</a></strong></p></div></td>
</tr></table>
-->

## Was sind A/B-Tests?

Bei A/B-Tests werden zwei oder mehr Versionen eines Objekts verglichen, um festzustellen, welche Version gegenüber einem definierten Ziel eine bessere Leistung erbringt.

Die Teilnehmer werden nach dem Zufallsprinzip einer Version zugewiesen, die als Variante bezeichnet wird, und ihr Verhalten wird verfolgt. Die Ergebnisse zeigen, ob eine Version die anderen statistisch übertrifft.

## Wichtige Terminologie

| Begriff | Definition |
|-|-|
| Kontrollvariante | Die Originalversion, die als Grundlage für den Vergleich verwendet wurde. |
| Variante oder Abwandlung | Eine neue Version, die für Tests mit dem Steuerelement erstellt wurde. |
| Hypothese | Eine Vorhersage, welche Veränderungen bessere Ergebnisse hervorbringen werden und warum. |
| Stichprobengröße | Die Anzahl der Einzelpersonen oder Sitzungen, die in den Test eingeschlossen sind. |
| statistische Signifikanz | Ein Maß für die Zuversicht, dass die Ergebnisse nicht auf einen Zufallsfehler zurückzuführen sind. |
| Anstieg | Die prozentuale Verbesserung oder Abnahme einer Variante im Vergleich zur Kontrolle. |
| Primäre Metrik | Das wichtigste Maß, mit dem der Erfolg des Tests bestimmt wird. |
| Sekundäre Metriken | Unterstützende Metriken, die zusätzliche insight bieten oder bei der Überwachung unbeabsichtigter Auswirkungen helfen. |
| Konfidenzintervall | Der geschätzte Bereich, in dem der tatsächliche Effekt wahrscheinlich fallen wird. |
| Segment | Eine bestimmte Untergruppe der Zielgruppe wird unabhängig analysiert (z. B. neue Benutzende, mobile Besucher). |

## Best Practices für die Durchführung von Experimenten

* **Beginnen Sie mit einer klaren Hypothese**

  Eine starke Hypothese beinhaltet, was Sie ändern, was Sie erwarten zu passieren und warum.
Beispiel: _Wir glauben, dass die Änderung von X Y aufgrund von Z erhöht._

* **Definieren Sie eine aussagekräftige Erfolgsmetrik**

  Wählen Sie eine Metrik aus, die Ihren umfassenderen Zielen entspricht. Vermeiden Sie „Vanity“-Metriken, die gut aussehen, aber keine echten Auswirkungen widerspiegeln.

* **Jeweils eine Änderung testen (sofern möglich)**

  Durch die Isolierung von Variablen können Ergebnisse einfacher genau interpretiert werden. Wenn Sie mehrere Änderungen gleichzeitig testen, wissen Sie möglicherweise nicht, was den Effekt verursacht hat.

* **Lassen Sie den Test lange genug laufen**

  Vorzeitige Schlussfolgerungen können irreführend sein. Warten Sie vor der Aktion auf eine statistisch signifikante Stichprobengröße.

* **Achten Sie auf externe Faktoren**

  Saisonabhängigkeit, Feiertage und andere Änderungen in Ihrer Umgebung können die Ergebnisse verfälschen. Dokumentieren Sie alles, was das Verhalten während des Tests beeinflussen könnte.

* **Verwenden Sie die Segmentierung sorgfältig**

  Wenn Sie die Ergebnisse nach Zielgruppensegmenten aufschlüsseln, können verborgene Muster sichtbar werden. Sie sollten jedoch kleine Stichprobengrößen nicht überinterpretieren.

* **Dokumentieren und Freigeben von Erkenntnissen**

  Halten Sie klar fest, was getestet wurde, warum und was Sie gelernt haben. Das baut institutionelle Kenntnisse auf und verhindert Wiederholungsfehler.

## Allgemeine Metriken

| Metrik | Was IT misst | Verwendung |
|-|-|-|
| Konversionsrate | Der Prozentsatz der Benutzenden, die eine gewünschte Aktion abgeschlossen haben | Nützlich zum Nachverfolgen des Erfolgs eines zielgesteuerten Erlebnisses |
| Clickthrough-Rate (CTR) | Der Prozentsatz der Benutzer, die auf ein bestimmtes Element klicken | Gibt an, wie überzeugend das Erlebnis ist |
| Interaktionsrate | Der Grad der Interaktion der Benutzer mit dem Erlebnis | Gut zum Messen von Interesse oder Aufmerksamkeit |
| Bounce-Rate | Der Prozentsatz der Benutzenden, die schnell gehen, ohne Maßnahmen zu ergreifen | Kann ein schlechtes oder verwirrendes Erlebnis signalisieren |
| Zeit auf Seite | Die Zeit, die Benutzende mit einem bestimmten Teil des Erlebnisses verbringen | Kann die Tiefe des Interesses oder der Komplexität widerspiegeln |
| Umsatz pro Besucher (RPV) | Durchschnittlicher Umsatz pro Benutzer | Wird häufig in Commerce-fokussierten Experimenten verwendet |
| Bindungsrate | Der Prozentsatz der Benutzenden, die im Laufe der Zeit zurückkehren oder aktiv bleiben | Nützlich für langfristige Wertermittlungen |

## Was macht ein gutes Experiment aus?

Ein gutes Experiment führt nicht nur zu einem Sieg, sondern auch zu einem klaren, umsetzbaren Lernen.
Suchen Sie nach Folgendem:

&check; **Statistische Konfidenz**: Der Unterschied zwischen den Varianten ist wahrscheinlich nicht zufällig bedingt.
&check; **Ausrichtung an Zielen**: Die primäre Metrik spiegelt einen bedeutenden Fortschritt bei der Erreichung eines Geschäftsziels wider.
&check; **Sekundäre Auswirkung**: Keine signifikanten negativen Auswirkungen auf zugehörige Metriken.
&check; **Skalierbarkeit**: Das Ergebnis kann für zukünftige Entscheidungen genutzt oder auf andere Bereiche verallgemeinert werden.
&check; **Clarity**: Die Ursache des Ergebnisses ist relativ isoliert und bekannt.

Beim Experimentieren geht es nicht nur darum, die „beste“ Version zu finden, sondern auch darum, Wissen durch Tests und Iterationen aufzubauen. Gut durchgeführte Experimente liefern Einblicke, die zu intelligenteren Entscheidungen, besseren Anwendererlebnissen und verbesserten Ergebnissen führen.

>[!BEGINSHADEBOX]

**Beispiel:**

* **Unternehmen**: Hotelkette
* **Hypothese**: Wenn wir dringendere Sprache auf der Startseite verwenden, führt dies zu mehr Buchungen.
   * **Kontrolle**: Originalversion
   * **Variante**: Neue Version mit Dringlichkeit hinzugefügt
   * **Primäre Metrik**: Buchungsrate
   * **Sekundäre Metriken**: Absprungrate, Zeit vor Ort
* **Ergebnis**: Die Variante führte zu einer Steigerung der Buchungsrate um 14 %, ohne dass sich andere Metriken negativ änderten.
* **Aktion**: Erwägen Sie, die Variante einzuführen und Folgeexperimente durchzuführen, um ähnliche Ansätze in anderen Bereichen zu testen.

>[!ENDSHADEBOX]
