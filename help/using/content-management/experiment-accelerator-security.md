---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Experimentation Accelerator
description: Datennutzung in KI mit Journey Optimizer Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: Inhalt, Experiment, mehrere, Zielgruppe, Abwandlung
exl-id: b7c00cdc-430c-40a2-90c9-6dd891d2563b
source-git-commit: 61ae9196f699c3b6aa1d9a5bb2259d36aaebc0e3
workflow-type: ht
source-wordcount: '439'
ht-degree: 100%

---

# Datennutzung in KI mit Journey Optimizer Experimentation Accelerator{#experiment-accelerator-security}

Mit **Adobe Journey Optimizer Experimentation Accelerator** können Sie automatisch Erkenntnisse gewinnen und Möglichkeiten zur Verbesserung Ihrer Experimente und Experimentprogramme empfehlen. Zur Bereitstellung dieser Empfehlungen nutzt die Lösung KI und maschinelles Lernen. Diese Anweisung verdeutlicht, wie die Daten Ihrer Kundinnen und Kunden in **Journey Optimizer Experimentation Accelerator** verwendet werden.

## Welche Daten verwendet Journey Optimizer Experimentation Accelerator?

Derzeit gibt es drei Datentypen, die von **Journey Optimizer Experimentation Accelerator** verwendet werden:

* **Metadaten zu Experimenten**: Experimentname, die Definition der im Experiment verwendeten Zielgruppe und die Abwandlungen im Experiment, z. B. Name, Aufspaltungsprozentsätze, Ort oder Oberfläche, in der das Experiment bereitgestellt wird.

* **Leistung der Abwandlungen**: Anzahl der Personen, Durchschnitt der Erfolgsmetrik und Standardabweichung für die einzelnen Abwandlungen.

* **Inhalt der Abwandlung**: Die gerenderte HTML und der Screenshot der Abwandlung, wie sie für Benutzende auf Ihrer Website erscheinen würde.

## Was macht Journey Optimizer Experimentation Accelerator mit diesen Daten?

**Journey Optimizer Experimentation Accelerator** nimmt die Inhalte für die einzelnen Abwandlungen und erstellt eine Einbettung (d. h. eine mathematische Darstellung des Inhalts) und korreliert diese Einbettungen dann mit der Leistung der Abwandlungen. Dieser Prozess ermöglicht die Extraktion der Inhaltsattribute, die am besten abgeschnitten haben, für eine zukünftige Verwendung. Diese Attribute werden dann in ein von Adobe gehostetes Large Language Model (LLM) aufgenommen, das sie in für Menschen lesbare Anweisungen umwandelt, die dazu dienen, Erkenntnisse zu generieren und Opportunities vorzuschlagen.

## Welche Einschränkungen weist Journey Optimizer Experimentation Accelerator in Bezug auf die verwendeten Daten auf?

Jede Kundin bzw. jeder Kunde wird einer bestimmten Organisation und Sandbox zugewiesen. Für jede Sandbox wird ein eigenes Modell trainiert. Wenn eine Sandbox gelöscht wird, werden alle zugehörigen Daten, Signale und Modelle dauerhaft entfernt.

* Wir verwenden Kundendaten nur, um das kundenspezifische Modell zu trainieren oder zu optimieren.

* Wir mischen niemals Kundschaft, um ein Modell zu trainieren oder zu optimieren.

## Ändern Adobe-Modelle oder KI das Anwendererlebnis einer Marke automatisch?

Nein. **Journey Optimizer Experimentation Accelerator** empfiehlt nur, was geändert werden könnte und wie dies geändert werden könnte. Nur Benutzende, die berechtigt sind, das Erlebnis mithilfe von Journey Optimizer oder Target zu ändern, können diese Empfehlungen umsetzen. Alle Empfehlungen können überprüft und bearbeitet werden, bevor sie bereitgestellt werden.

## Besteht ein Risiko für die Daten- oder Systemstabilität?

**Journey Optimizer Experimentation Accelerator** nimmt nur Daten auf und analysiert sie, wodurch Erkenntnisse und Empfehlungen für zukünftige Tests entstehen. Das Tool hat keine Zugriffsberechtigung zum Ändern von Testeinstellungen. Alle im Tool generierten Vorschläge werden zur Implementierung an Target und Journey Optimizer gesendet. So wird sichergestellt, dass sie keine Auswirkungen auf die aktuellen Aktivitäten von Kundschaft haben.
