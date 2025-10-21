---
title: Im Experimentbericht verwendete statistische Berechnungen
description: Mehr Informationen über A/B-Tests im Vergleich zum Multi-Armed-Bandit
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
source-git-commit: a659f596c0d37f4b91ec41e52c02c8385f6ae16b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 100%

---

# A/B-Tests im Vergleich zu Multi-Armed-Bandit-Experimenten {#mab-vs-ab}

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experimenttyp"
>abstract="Der Experimenttyp bestimmt, wie der Traffic während des Tests zwischen den Abwandlungen verteilt wird. Wählen Sie die Methode aus, die am besten zu Ihren Zielen passt:</br><b>A/B-Test</b>: Teilt den Traffic während der Definition zwischen Abwandlungen und misst die Leistung, bis die Ergebnisse statistisch signifikant sind. Ideal, um zu erfahren, welche Abwandlung in einem kontrollierten Vergleich besser funktioniert.</br><b>Mehrarmiger Bandit</b>: Verlagert den Traffic hin zu leistungsfähigeren Abwandlungen, wenn Daten gesammelt werden, wodurch Geschwindigkeit und Optimierung miteinander in Einklang gebracht werden. Nützlich, wenn Sie Konversionen während des Experiments maximieren möchten.</br><b>Eigenen mehrarmigen Banditen einbringen</b>: Verwenden Sie Ihren eigenen Algorithmus, um die Traffic-Zuordnung zu bestimmen, sodass Sie bei Vorliegen eines benutzerdefinierten Modells oder einer benutzerdefinierten Strategie flexibel sind."

Auf dieser Seite finden Sie einen detaillierten Vergleich von **A/B**-Tests und **Multi-Armed-Bandit**-Experimenten. Es werden die jeweiligen Stärken, Einschränkungen und Szenarien erläutert, in denen die beiden Ansätze am effektivsten sind.


## A/B {#ab-test}

Bei herkömmlichen A/B-Tests wird Traffic gleichmäßig auf Abwandlungen aufgeteilt und diese Zuordnung beibehalten, bis das Experiment abgeschlossen ist. Sobald statistische Signifikanz erreicht ist, wird die erfolgreichste Abwandlung identifiziert und anschließend skaliert.

### Vorteile

Die wichtigsten Stärken herkömmlicher A/B-Tests sind:

* **Statistische Strenge**

  Das feste Design sorgt für klar definierte Fehlerquoten und Konfidenzintervalle.

  Frameworks für Hypothesentests (z. B. Konfidenz von 95 %) sind einfacher anzuwenden und zu interpretieren.

  Gut durchdachte Experimente reduzieren die Wahrscheinlichkeit falsch positiver Ergebnisse.

* **Einfachheit**

  Die Methodik ist einfach zu entwerfen und auszuführen.

  Ergebnisse können nicht-technischen Stakeholdern klar vermittelt werden.

* **Umfangreiche Datenerfassung**

  Jede Abwandlung wird ausreichend bereitgestellt, sodass nicht nur die erfolgreichste Variante, sondern auch die leistungsschwachen Alternativen analysiert werden können.

  Diese zusätzlichen Informationen können als Grundlage für langfristige strategische Entscheidungen dienen.

* **Verzerrungkontrolle**

  Feste Zuordnung reduziert die Anfälligkeit für Verzerrungen wie den „Fluch des Gewinners“ oder eine Regression zur Mitte.

### Einschränkungen

Die wichtigsten Einschränkungen bei herkömmlichen A/B-Tests sind:

* **Opportunity-Kosten**

  Ein erheblicher Teil des Traffics wird zu minderwertigen Abwandlungen gelenkt, was während des Testens Konversionen oder Umsätze verringern kann.

  Die erfolgreichste Abwandlung kann erst nach Abschluss des Experiments implementiert werden.

* **Anforderung an feste Dauer**

  Tests müssen in der Regel über den vorgegebenen Zeitraum laufen, auch wenn sich externe Bedingungen (z. B. Jahreszeit, Markt) unterdessen ändern.

  Anpassungsmöglichkeiten während des Experiments sind begrenzt.

## Multi-Armed Bandit {#mab-experiment}

Multi-Armed-Bandit-Algorithmen nutzen adaptive Zuordnung: Mit zunehmenden Erkenntnissen wird mehr Traffic zu Abwandlungen mit besserer Leistung geleitet. Ziel ist es, die kumulative Belohnung während des Experiments zu maximieren, anstatt sich ausschließlich auf das Endergebnis zu konzentrieren.

### Vorteile

Die wichtigsten Stärken von Multi-Armed-Bandit-Methoden sind:

* **Schnellere Optimierung**

  Vielversprechende Abwandlungen werden früher priorisiert, was die Gesamtleistung beim Testen verbessert.

* **Adaptivität**

  Zuordnungen werden bei der Datenerfassung kontinuierlich aktualisiert, sodass Multi-Armed Bandit für dynamische Umgebungen geeignet ist.

* **Geringere Opportunity-Kosten**

  Mangelhafte Abwandlungen werden schnell beseitigt, wodurch die Verschwendung von Traffic minimiert wird.

* **Eignung für kontinuierliche Tests**

  Effektiv für laufende Experimente oder Kontexte, in denen Traffic teuer ist.

### Einschränkungen

Die wichtigsten Einschränkungen von Multi-Armed-Bandit-Methoden sind:

* **Schwächere statistische Garantien**

  Herkömmliche Hypothesentests sind schwieriger anzuwenden und Regeln zum Stoppen sind weniger klar.

* **Weniger Transparenz**

  Adaptive Zuordnung kann für Stakeholder schwer zu erklären sein.

* **Eingeschränkte Informationen zu leistungsschwachen Abwandlungen**

  Leistungsschwache Abwandlungen erhalten wenig Exposition, was die diagnostischen Erkenntnisse einschränkt.

* **Komplexität der Implementierung**

  Erfordert fortgeschrittene Algorithmen und Infrastruktur, wobei es ein größeres Potenzial für Fehlkonfigurationen gibt.

## Verwendung von A/B vs. Multi-Armed Bandit

| Szenario | Empfohlene Methode |
|-|-|
| Sie führen explorative oder forschungsorientierte Tests durch | A/B |
| Sie führen kontinuierlich aktive Kampagnen durch, z. B. Anzeigen, Empfehlungen | Multi-Armed Bandit |
| Sie wollen Konversionen während des Testens maximieren | Multi-Armed Bandit |
| Sie wollen klare, zuverlässige Erkenntnisse | A/B |
| Sie müssen schnell Anpassungen vornehmen (z. B. jahreszeitliche Verschiebungen) | Multi-Armed Bandit |
| Sie verfügen über eingeschränkten Traffic und möchten die Rentabilität schnell optimieren | Multi-Armed Bandit |
| Sie haben viel Traffic und können sich langsameres Lernen leisten | A/B |
| Stakeholder benötigen klare Entscheidungspunkte | A/B |
