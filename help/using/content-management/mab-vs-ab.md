---
title: Im Experimentationsbericht verwendete statistische Berechnungen
description: Erfahren Sie mehr über A/B-Tests vs. mehrarmige Bandit
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
source-git-commit: a659f596c0d37f4b91ec41e52c02c8385f6ae16b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 3%

---

# A/B-Experimente vs. Experimente mit mehrarmigen Banditen {#mab-vs-ab}

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experimenttyp"
>abstract="Der Experimenttyp bestimmt, wie der Traffic während des Tests zwischen den Behandlungen verteilt wird. Wählen Sie die Methode aus, die am besten zu Ihren Zielen passt:</br><b>A/B-Experiment</b>: Teilt den Traffic, während Sie zwischen Abwandlungen definieren und die Leistung messen, bis die Ergebnisse statistisch signifikant sind. Am besten können Sie lernen, welche Behandlung in einem kontrollierten Vergleich besser abschneidet.</br><b>Multi-Armed Bandit</b>: Verlagert den Traffic hin zu leistungsfähigeren Abwandlungen, wenn Daten gesammelt werden, wodurch Geschwindigkeit und Optimierung miteinander in Einklang gebracht werden. Dies ist nützlich, wenn Sie die Konversionen während des Experiments maximieren möchten.</br><b>Bring your own Multi-Armed Bandit</b>: Verwenden Sie Ihren eigenen Algorithmus, um die Traffic-Zuordnung zu bestimmen, sodass Sie flexibel sind, wenn Sie ein benutzerdefiniertes Modell oder eine benutzerdefinierte Strategie haben."

Auf dieser Seite finden Sie einen detaillierten Vergleich von **A/B**- und **Multi-Armed Bandit**-Experimenten, wobei die jeweiligen Stärken, Einschränkungen und Szenarien erläutert werden, in denen jeder Ansatz am effektivsten ist.


## A/B {#ab-test}

Beim herkömmlichen A/B-Experiment wird der Traffic gleichmäßig auf die Abwandlungen aufgeteilt und diese Zuordnung beibehalten, bis das Experiment abgeschlossen ist. Sobald die statistische Signifikanz erreicht ist, wird die erfolgreichste Behandlung identifiziert und anschließend skaliert.

### Vorteile

Die wichtigsten Stärken herkömmlicher A/B-Experimente sind:

* **Strenge der Statistiken**

  Das feste Design bietet klar definierte Fehlerquoten und Konfidenzintervalle.

  Frameworks für Hypothesentests, z. B. eine Konfidenz von 95 %, sind einfacher anzuwenden und zu interpretieren.

  Richtig durchdachte Experimente reduzieren die Wahrscheinlichkeit falsch positiver Ergebnisse.

* **Einfachheit**

  Die Methodik ist einfach zu entwerfen und auszuführen.

  Die Ergebnisse können den nicht-technischen Stakeholdern klar vermittelt werden.

* **Umfassende Datenerfassung**

  Jede Behandlung wird angemessen belichtet, sodass nicht nur die erfolgreichste Variante, sondern auch die leistungsschwachen Alternativen analysiert werden können.

  Diese zusätzlichen Informationen können als Grundlage für langfristige strategische Entscheidungen dienen.

* **Bias-Steuerung**

  Feste Zuordnung reduziert die Anfälligkeit für Verzerrungen wie den „Fluch des Siegers“ oder eine Regression zum Mittelwert.

### Einschränkungen

Die wichtigsten Einschränkungen herkömmlicher A/B-Experimente sind:

* **Opportunity-Kosten**

  Ein erheblicher Teil des Traffics wird auf minderwertige Behandlungen gelenkt, was während des Tests Konversionen oder Umsätze verringern kann.

  Die erfolgreichste Behandlung kann erst nach Abschluss des Experiments implementiert werden.

* **Anforderung für feste Dauer**

  Tests müssen in der Regel über den vorgegebenen Zeithorizont laufen, auch wenn sich externe Bedingungen, z. B. Saisonabhängigkeit, Marktveränderungen, mittendrin ändern.

  Die Anpassung während des Experiments ist begrenzt.

## Mehrarmiger Bandit {#mab-experiment}

Mehrarmige Bandit-Algorithmen nutzen die adaptive Allokation: Mit zunehmendem Beweismaterial fließt mehr Traffic in Behandlungen mit besserer Leistung. Ziel ist es, die kumulative Belohnung während des Experiments zu maximieren, anstatt sich ausschließlich auf das Endergebnis zu konzentrieren.

### Vorteile

Die wichtigsten Stärken der Multi-Armed-Bandit-Methoden sind:

* **Schnellere Optimierung**

  Viel versprechende Behandlungen werden früher priorisiert, was die Gesamtleistung während des Tests verbessert.

* **Adaptivität**

  Die Zuteilungen werden bei der Datenerfassung kontinuierlich aktualisiert, sodass Multi-Armed Bandit für dynamische Umgebungen geeignet ist.

* **Geringere Opportunity-Kosten**

  Schlechte Behandlungsmethoden werden schnell abgeschafft, wodurch verschwendetes Traffic minimiert wird.

* **Eignung für kontinuierliche Tests**

  Effektiv für laufende Experimente oder Kontexte, in denen Traffic teuer ist.

### Einschränkungen

Die wichtigsten Einschränkungen von Multi-Armed-Bandit-Methoden sind:

* **Schwächere statistische Garantien**

  Herkömmliche Hypothesentests sind schwieriger anzuwenden, und Regeln zum Stoppen sind weniger klar.

* **Weniger Transparenz**

  Die adaptive Zuordnung kann für Stakeholder schwierig zu erklären sein.

* **Eingeschränkte Informationen zu Behandlungen mit unzureichender Leistung**

  Schwache Behandlungen erhalten wenig Exposition, was die diagnostische insight einschränkt.

* **Komplexität der Implementierung**

  Erfordert erweiterte Algorithmen und Infrastruktur mit einem größeren Potenzial für Fehlkonfigurationen.

## Verwendung von A/B vs. Multi-Armed Bandit

| Szenario | Empfohlene Methode |
|-|-|
| Sie führen explorative oder forschungsgesteuerte Tests durch | A/B |
| Sie führen ständig aktive Kampagnen durch, z. B. Anzeigen, Empfehlungen | mehrarmiger Bandit |
| Konversionen während des Tests maximieren | mehrarmiger Bandit |
| Sie wollen klare, selbstbewusste Einblicke | A/B |
| Sie müssen sich schnell anpassen, z.B. Saisonverschiebungen | mehrarmiger Bandit |
| Sie verfügen über eingeschränktes Traffic und möchten den ROI schnell optimieren. | mehrarmiger Bandit |
| Sie haben hohen Traffic und können sich langsameres Lernen leisten | A/B |
| Stakeholder benötigen klare Entscheidungspunkte | A/B |
