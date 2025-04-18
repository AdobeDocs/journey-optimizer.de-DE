---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit orchestrierten Kampagnenaktivitäten
description: Erfahren Sie, wie Sie Kampagnenaktivitäten koordinieren
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 960c7ab18cdca6e34c06f2dc6672aefdb5340ef0
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 56%

---

# Über orchestrierte Kampagnenaktivitäten {#ms-campaign-activities}

Orchestrierte Kampagnenaktivitäten werden in drei Kategorien unterteilt. Je nach Kontext können die verfügbaren Aktivitäten unterschiedlich sein.

Alle Aktivitäten werden in den folgenden Abschnitten beschrieben:

* [Zielgruppenbestimmungs- und Daten-Management-Aktivitäten](#targeting)
* [Kanalaktivitäten](#channel)
* [Aktivitäten zur Flusssteuerung](#flow-control)

![](../assets/workflow-activities.png)

## Aktivitäten zur Zielgruppenbestimmung {#targeting}

Diese Aktivitäten sind spezifisch für die Zielgruppenbestimmung. Sie ermöglichen es Ihnen, ein oder mehrere Ziele zu erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Schnittmenge, Vereinigung oder Ausschluss aufteilen oder kombinieren.

* [Zielgruppe erstellen](build-audience.md): Mit dieser Aktivität definieren Sie Ihre Zielpopulation. Sie können entweder eine bestehende Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie die Zielgruppendimension beim Erstellen Ihrer orchestrierten Kampagne.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten, die in Ihrer orchestrierten Kampagne verarbeitet werden sollen. Mit dieser Aktivität können Sie die eingehende Transition nutzen und die Aktivität so konfigurieren, dass sie die ausgehende Transition mit zusätzlichen Daten ergänzt.
* [Abstimmung](reconciliation.md) Definieren Sie die Relation zwischen den Daten in Journey Optimizer und den Daten in einer Arbeitstabelle, z. B. Daten aus einer externen Datei.
* [Audience speichern](save-audience.md): Aktualisieren Sie eine vorhandene Audience oder erstellen Sie eine neue Audience aus der Population, die in einer orchestrierten Kampagne im Upstream berechnet wird.
* [Aufspaltung](split.md): Segmentieren Sie die eingehende Population in mehrere Teilmengen.

## Daten-Management-Aktivitäten {#data}

Diese Aktivitäten dienen der Manipulation und Anreicherung von Populationsdaten.

* [Datei laden](load-file.md): Mit dieser Aktivität können Sie mit Profilen und Daten arbeiten, die in einer externen Datei gespeichert sind.
* [Daten aktualisieren](update-data.md): Mit dieser Aktivität führen Sie eine gebündelte Aktualisierung von Datenbankfeldern durch. Die Art der Datenbankaktualisierung kann über verschiedene Optionen definiert werden.

## Kanalaktivitäten {#channel}

Mit Adobe Journey Optimizer können Sie Marketing-Kampagnen über mehrere Kanäle hinweg automatisieren und ausführen. Sie können Kanalaktivitäten in der Arbeitsfläche kombinieren, um eine kanalübergreifende orchestrierte Kampagne zu erstellen, mit der Trigger-Aktionen basierend auf dem Kundenverhalten erstellt werden können. Es sind folgende **Kanalaktivitäten** verfügbar: E-Mail-, SMS-, Android- und iOS-Push-Benachrichtigungen. [Erfahren Sie, wie Sie einen Versand im Kontext einer orchestrierten Kampagne einrichten](channels.md).

## Aktivitäten zur Flusssteuerung {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Endaktivität"
>abstract="Die **Ende**-Aktivität ermöglicht es Ihnen, das Ende einer orchestrierten Kampagne grafisch zu markieren. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional."

Die folgenden Aktivitäten sind spezifisch für die Organisation und Ausführung orchestrierter Kampagnen. Ihre Hauptaufgabe ist es, die anderen Aktivitäten zu koordinieren:

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer orchestrierten Kampagne.
* **Ende**: Markieren Sie grafisch das Ende einer orchestrierten Kampagne. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
* [Verzweigung](fork.md): Erstellen Sie ausgehende Transitionen, um mehrere Aktivitäten gleichzeitig zu starten.
* [Test](test.md): Mit dieser Aktivität aktivieren Sie Transitionen auf Grundlage der angegebenen Bedingungen.
* [Warten](wait.md): Hält die Ausführung eines Teils einer orchestrierten Kampagne vorübergehend an.
