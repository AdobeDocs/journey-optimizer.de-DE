---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Datennutzung in KI mit Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Zielgruppe, Abwandlung
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Datennutzung in KI mit Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Erste Schritte mit Experimentation Accelerator](experiment-accelerator.md)
* [Datennutzung in KI mit Experimentation Accelerator](experiment-accelerator-security.md)
* [Best Practices für Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Experimente überwachen](experiment-accelerator-monitor.md)
* [Experimentier-Metriken](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

Mit **Adobe Journey Optimizer Experimentation Accelerator** können Sie automatisch Einblicke gewinnen und Möglichkeiten zur Verbesserung Ihrer Experimente und Experimentierprogramme empfehlen. Die Lösung nutzt KI und maschinelles Lernen, um diese Empfehlungen bereitzustellen. Diese Anweisung verdeutlicht, wie die Daten Ihrer Kunden in **Experimentation Accelerator verwendet**.

## Welche Daten verwendet Experimentationsbeschleuniger?

Derzeit gibt es drei Datentypen, die von **Experimentationsbeschleuniger** verwendet werden:

* **Experimentmetadaten**: Experimentname, die Definition der im Experiment verwendeten Zielgruppe und die Abwandlungen im Experiment, z. B. Name, Aufspaltungsprozentsätze, Ort oder Oberfläche, für die das Experiment bereitgestellt wird.

* **Leistung der Behandlungen**: Anzahl der Personen, Durchschnitt der Erfolgsmetrik und Standardabweichung für jede Behandlung.

* **Inhalt der Abwandlung**: Die gerenderte HTML und der Screenshot der Abwandlung, wie sie für Benutzende auf Ihrer Website erscheinen würde.

## Was macht der Experimentationsbeschleuniger mit diesen Daten?

**Experimentationsbeschleuniger** nimmt den Inhalt für jede Behandlung und erstellt eine Einbettung, d. h. eine mathematische Darstellung des Inhalts, und korreliert diese Einbettungen dann mit der Leistung der Behandlungen. Dieser Prozess ermöglicht die Extraktion der Inhaltsattribute, die für die zukünftige Verwendung die beste Leistung erzielt haben. Diese Attribute werden dann in ein von Adobe gehostetes großes Sprachmodell eingespeist, das sie in für Menschen lesbare Aussagen umwandelt, die verwendet werden, um Erkenntnisse zu generieren und Chancen vorzuschlagen.

## Welche Einschränkungen hat Experimentation Accelerator in Bezug auf die verwendeten Daten?

Jeder Kunde wird einer bestimmten Organisation und Sandbox zugewiesen. Für jede Sandbox wird ein dediziertes Modell trainiert. Wenn eine Sandbox gelöscht wird, werden alle zugehörigen Daten, Signale und Modelle dauerhaft entfernt.

* Wir verwenden Kundendaten nur, um das Modell dieses Kunden zu trainieren oder zu optimieren.

* Wir mischen nie Kunden, um ein Modell zu trainieren oder zu optimieren.

## Ändern Adobe-Modelle oder KI das Benutzererlebnis einer Marke automatisch?

Nein. **Experimentation Accelerator** empfiehlt nur, was geändert werden könnte und wie dies geändert werden könnte. Nur Benutzer, die berechtigt sind, das Erlebnis mithilfe von Journey Optimizer oder Target zu ändern, können diese Empfehlungen umsetzen. Alle Empfehlungen können überprüft und bearbeitet werden, bevor sie verworfen werden.

## Besteht ein Risiko für die Daten- oder Systemstabilität?

**Experimentation Accelerator** nimmt nur Daten auf und analysiert sie, was Erkenntnisse und Empfehlungen für zukünftige Tests liefert. Er hat keine Zugriffsberechtigung zum Ändern von Testeinstellungen. Alle im Tool generierten Vorschläge werden zur Implementierung an Target und Journey Optimizer gesendet. So wird sichergestellt, dass sie keine Auswirkungen auf die aktuellen Aktivitäten eines Kunden haben.
