---
title: Im Experimentbericht verwendete statistische Berechnungen
description: Mehr Informationen über A/B-Tests im Vergleich zum Multi-Armed-Bandit
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
TQID: https://experienceleague.adobe.com/47tFiWTUUsGUMeWhuJVQnakAIrgz1Ax1mO-u8pf27uc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2:
  - id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 658
ht-degree: 95%

---

# A/B-Tests im Vergleich zu Multi-Armed-Bandit-Experimenten {#mab-vs-ab}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Vergleichen Sie A/B- und Multi-Armed-Bandit-Experimente in Adobe Journey Optimizer, einschließlich ihrer Stärken, Einschränkungen und Szenarien, in denen jede Traffic-Zuordnungsmethode am besten funktioniert.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experimenttyp"
>abstract="Der Experimenttyp bestimmt, wie der Traffic während des Tests zwischen den Abwandlungen verteilt wird. Wählen Sie die Methode aus, die am besten zu Ihren Zielen passt:</br><b>A/B-Test</b>: Teilt den Traffic während der Definition zwischen Abwandlungen und misst die Leistung, bis die Ergebnisse statistisch signifikant sind. Am besten geeignet, um in einem kontrollierten Vergleich herauszufinden, welche Abwandlung die bessere Leistung erbringt.</br><b>Mehrarmiger Bandit</b>: Er verlagert den Traffic bei der Datenerfassung zu leistungsstärkeren Abwandlungen und bringt Geschwindigkeit und Optimierung in Einklang. Nützlich, wenn Sie Konversionen während des Experiments maximieren möchten.</br><b>Eigenen mehrarmigen Banditen einbringen</b>: Verwenden Sie Ihren eigenen Algorithmus, um die Traffic-Zuordnung zu bestimmen, sodass Sie bei Vorliegen eines benutzerdefinierten Modells oder einer benutzerdefinierten Strategie flexibel sind."

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
