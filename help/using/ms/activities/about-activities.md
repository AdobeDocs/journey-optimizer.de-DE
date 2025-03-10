---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit mehrstufigen Kampagnenaktivitäten
description: Erfahren Sie, wie Sie mehrstufige Kampagnenaktivitäten erstellen
hide: true
hidefromtoc: true
source-git-commit: 658d82820d3f307481c44a142c38727f777fd879
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 55%

---


# Über mehrstufige Kampagnenaktivitäten {#ms-campaign-activities}

Mehrstufige Kampagnenaktivitäten werden in drei Kategorien unterteilt. Je nach Kontext können die verfügbaren Aktivitäten unterschiedlich sein.

Alle Aktivitäten werden in den folgenden Abschnitten beschrieben:

* [Zielgruppenbestimmungs- und Daten-Management-Aktivitäten](#targeting)
* [Kanalaktivitäten](#channel)
* [Aktivitäten zur Flusssteuerung](#flow-control)

![](../assets/workflow-activities.png)

## Aktivitäten zur Zielgruppenbestimmung {#targeting}

Diese Aktivitäten sind spezifisch für die Zielgruppenbestimmung. Sie ermöglichen es Ihnen, ein oder mehrere Ziele zu erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Schnittmenge, Vereinigung oder Ausschluss aufteilen oder kombinieren.

* [Zielgruppe erstellen](build-audience.md): Mit dieser Aktivität definieren Sie Ihre Zielpopulation. Sie können entweder eine bestehende Zielgruppe auswählen oder den Abfrage-Modeler verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie die Zielgruppendimension beim Erstellen Ihrer mehrstufigen Kampagne.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Dubletten in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten zur Verarbeitung in Ihrer mehrstufigen Kampagne. Mit dieser Aktivität können Sie die eingehende Transition nutzen und die Aktivität so konfigurieren, dass sie die ausgehende Transition mit zusätzlichen Daten ergänzt.
* [Abstimmung](reconciliation.md) Definieren Sie die Relation zwischen den Daten in Journey Optimizer und den Daten in einer Arbeitstabelle, z. B. Daten aus einer externen Datei.
* [Audience speichern](save-audience.md): Aktualisieren Sie eine vorhandene Audience oder erstellen Sie eine neue Audience aus der Population, die in einer mehrstufigen Kampagne im Upstream berechnet wird.
* [Aufspaltung](split.md): Segmentieren Sie die eingehende Population in mehrere Teilmengen.

## Daten-Management-Aktivitäten {#data}

Diese Aktivitäten dienen der Manipulation und Anreicherung von Populationsdaten.

* [Datei laden](load-file.md): Mit dieser Aktivität können Sie mit Profilen und Daten arbeiten, die in einer externen Datei gespeichert sind.
* [Daten aktualisieren](update-data.md): Mit dieser Aktivität führen Sie eine gebündelte Aktualisierung von Datenbankfeldern durch. Die Art der Datenbankaktualisierung kann über verschiedene Optionen definiert werden.

## Kanalaktivitäten {#channel}

Mit Adobe Journey Optimizer können Sie Marketing-Kampagnen über mehrere Kanäle hinweg automatisieren und ausführen. Sie können Kanalaktivitäten in der Arbeitsfläche kombinieren, um eine kanalübergreifende mehrstufige Kampagne zu erstellen, mit der basierend auf dem Kundenverhalten Trigger erstellt werden können. Es sind folgende **Kanalaktivitäten** verfügbar: E-Mail-, SMS-, Android- und iOS-Push-Benachrichtigungen. [Erfahren Sie, wie Sie einen Versand im Kontext einer mehrstufigen Kampagne einrichten](channels.md).

## Aktivitäten zur Flusssteuerung {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Endaktivität"
>abstract="Die **Ende**-Aktivität ermöglicht es Ihnen, das Ende einer mehrstufigen Kampagne grafisch zu markieren. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional."

Die folgenden Aktivitäten dienen der Organisation und Ausführung mehrstufiger Kampagnen. Ihre Hauptaufgabe ist es, die anderen Aktivitäten zu koordinieren:

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer mehrstufigen Kampagne.
* **Ende**: Markieren Sie das Ende einer mehrstufigen Kampagne grafisch. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
* [Verzweigung](fork.md): Erstellen Sie ausgehende Transitionen, um mehrere Aktivitäten gleichzeitig zu starten.
* [Planung](scheduler.md): Zeitplan für den Start der mehrstufigen Kampagne.
* [Test](test.md): Mit dieser Aktivität aktivieren Sie Transitionen auf Grundlage der angegebenen Bedingungen.
* [Warten](wait.md): Hält die Ausführung eines Teils einer mehrstufigen Kampagne vorübergehend an.
