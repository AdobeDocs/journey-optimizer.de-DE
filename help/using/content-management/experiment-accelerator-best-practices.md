---
solution: Journey Optimizer
product: journey optimizer
title: Best Practices für Journey Optimizer Experimentation Accelerator
description: Verbessern Ihrer Fähigkeit, Experimente effektiv durchzuführen und Erkenntnisse zu gewinnen
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Zielgruppe, Abwandlung
exl-id: 001e05db-e343-4a95-9694-274a8c50d08c
source-git-commit: 61ae9196f699c3b6aa1d9a5bb2259d36aaebc0e3
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 98%

---

# Best Practices für Journey Optimizer Experimentation Accelerator {#content-experiment-best-practices}

## Was sind A/B-Tests?

Bei A/B-Tests werden zwei oder mehr Varianten eines Objekts verglichen, um zu ermitteln, welche Variante bezüglich eines definierten Ziels besser abschneidet.

Teilnehmerinnen und Teilnehmer werden nach dem Zufallsprinzip einer Version zugewiesen, die als Variante bezeichnet wird. Anschließend wird ihr Verhalten verfolgt. Die Ergebnisse zeigen, ob eine Variante die anderen statistisch übertrifft.

## Wichtige Terminologie

| Begriff | Definition |
|-|-|
| Kontrollvariante | Die Originalversion, die als Baseline für den Vergleich verwendet wird. |
| Variante oder Abwandlung | Eine neue Version, die für Tests mit der Kontrollvariante erstellt wird. |
| Hypothese | Eine Vorhersage, welche Veränderung bessere Ergebnisse hervorbringen wird und warum. |
| Stichprobengröße | Die Anzahl der Einzelpersonen oder Sitzungen, die in den Test eingeschlossen werden. |
| Statistische Signifikanz | Ein Maß für die Konfidenz, dass die Ergebnisse nicht auf Zufallsfehler zurückzuführen sind. |
| Anstieg | Die prozentuale Verbesserung oder Verschlechterung einer Variante im Vergleich zur Kontrollvariante. |
| Primäre Metrik | Das wichtigste Maß, mit dem der Erfolg des Tests bestimmt wird. |
| Sekundäre Metriken | Unterstützende Metriken, die zusätzliche Erkenntnisse liefern oder bei der Überwachung unbeabsichtigter Effekte helfen. |
| Konfidenzintervall | Der geschätzte Bereich, in den der wahre Effekt wahrscheinlich fallen wird. |
| Segment | Eine bestimmte Teilmenge der Zielgruppe, die unabhängig analysiert wird (z. B. neue Benutzende, Besuchende mit Mobilgeräten). |

## Best Practices für die Durchführung von Experimenten

* **Mit einer klaren Hypothese beginnen**

  Eine starke Hypothese beinhaltet das, was Sie ändern, was Ihren Erwartungen nach passieren soll und warum.
Beispiel: _Wir glauben, dass eine Änderung von X den Wert Y wegen Z erhöhen wird._

* **Aussagekräftige Erfolgsmetrik definieren**

  Wählen Sie eine Metrik, die zu Ihren übergeordneten Zielen passt. Vermeiden Sie „leere“ Metriken, die gut aussehen, aber keine echten Auswirkungen widerspiegeln.

* **Jeweils eine Änderung testen (sofern möglich)**

  Durch eine Isolierung von Variablen lassen sich Ergebnisse einfacher genau interpretieren. Wenn Sie mehrere Änderungen auf einmal testen, wissen Sie möglicherweise nicht, was den Effekt verursacht hat.

* **Test ausreichend lang ausführen**

  Vorzeitige Schlussfolgerungen können irreführend sein. Warten Sie auf eine statistisch signifikante Stichprobengröße, bevor Sie aktiv werden.

* **Auf externe Faktoren achten**

  Saisonabhängigkeit, Feiertage und andere Änderungen in Ihrer Umgebung können Ergebnisse verfälschen. Dokumentieren Sie alles, was das Verhalten während des Tests beeinflussen könnte.

* **Segmentierung durchdacht verwenden**

  Wenn Sie Ergebnisse nach Zielgruppensegmenten aufschlüsseln, können verborgene Muster sichtbar werden. Sie sollten jedoch kleine Stichprobengrößen nicht überinterpretieren.

* **Erkenntnisse dokumentieren und teilen**

  Halten Sie klar fest, was getestet wurde, warum und was Sie gelernt haben. Das schafft institutionelles Wissen und verhindert Wiederholungsfehler.

## Allgemeine Metriken

| Metrik | Was sie misst | Verwendung |
|-|-|-|
| Konversionsrate | Der Prozentsatz der Benutzenden, die eine gewünschte Aktion abgeschlossen haben | Nützlich zum Tracking des Erfolgs bei einem zielgesteuerten Erlebnis |
| Klickrate (CTR) | Der Prozentsatz der Benutzenden, die auf ein bestimmtes Element klicken | Gibt an, wie überzeugend das Erlebnis ist |
| Interaktionsrate | Der Grad der Interaktion der Benutzenden mit dem Erlebnis | Gut zum Messen von Interesse oder Aufmerksamkeit |
| Bounce-Rate | Der Prozentsatz der Benutzenden, die schnell wieder gehen, ohne Aktivitäten auszuführen | Kann auf ein unpassendes oder verwirrendes Erlebnis hindeuten |
| Zeit auf Seite | Die Zeit, die Benutzende mit einem bestimmten Teil des Erlebnisses verbringen | Kann die Tiefe des Interesses oder Komplexität widerspiegeln |
| Umsatz pro Besucherin bzw. Besucher (RPV) | Durchschnittlicher Umsatz pro Benutzerin bzw. Benutzer | Wird häufig in Commerce-fokussierten Experimenten verwendet |
| Bindungsrate | Der Prozentsatz der Benutzenden, die im Laufe der Zeit zurückkehren oder aktiv bleiben | Nützlich für langfristige Wertermittlungen |

## Was macht ein gutes Experiment aus?

Ein gutes Experiment führt nicht nur zu einem Erfolg, sondern auch zu einem klaren, verwertbaren Lernen.
Achten Sie auf Folgendes:

&check; **Statistische Konfidenz**: Der Unterschied zwischen den Varianten ist wahrscheinlich nicht zufällig.
&check; **Ausrichtung an Zielen**: Die primäre Metrik spiegelt bedeutenden Fortschritt bei der Erreichung eines Geschäftsziels wider.
&check; **Sekundäre Auswirkung**: Keine signifikanten negativen Auswirkungen auf zugehörige Metriken.
&check; **Skalierbarkeit**: Das Ergebnis kann für zukünftige Entscheidungen genutzt oder auf andere Bereiche verallgemeinert werden.
&check; **Klarheit**: Die Ursache des Ergebnisses ist relativ gut isoliert und bekannt.

Beim Experimentieren geht es nicht nur darum, die „beste“ Variante zu finden, sondern auch darum, durch Tests und Iterationen Wissen aufzubauen. Gut durchgeführte Experimente liefern Erkenntnisse, die zu intelligenteren Entscheidungen, besseren Anwendererlebnissen und optimierten Ergebnissen führen.

>[!BEGINSHADEBOX]

**Beispiel:**

* **Unternehmen**: Hotelkette
* **Hypothese**: Wenn wir auf der Homepage Formulierungen mit größerer Dringlichkeit verwenden, führt dies zu mehr Buchungen.
   * **Kontrollvariante**: Originalversion
   * **Variante**: Neue Version mit mehr Dringlichkeit
   * **Primäre Metrik**: Buchungsrate
   * **Sekundäre Metriken**: Bounce-Rate, Besuchszeit pro Site
* **Ergebnis**: Die Variante führte zu einer Steigerung der Buchungsrate um 14 %, ohne dass sich andere Metriken negativ änderten.
* **Aktion**: Erwägen Sie, die Variante einzuführen und Folgeexperimente durchzuführen, um ähnliche Ansätze in anderen Bereichen zu testen.

>[!ENDSHADEBOX]
