---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit orchestrierten Kampagnenaktivitäten
description: Erfahren Sie, wie Sie Kampagnenaktivitäten koordinieren
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 66%

---


# Über koordinierte Kampagnenaktivitäten {#orchestrated-campaign-activities}

Aktivitäten orchestrierter Kampagnen sind in drei Kategorien unterteilt. Je nach Kontext können die verfügbaren Aktivitäten unterschiedlich sein.

Alle Aktivitäten werden in den folgenden Abschnitten beschrieben:

* [Targeting-Aktivitäten](#targeting)
* [Kanalaktivitäten](#channel)
* [Aktivitäten zur Flusskontrolle](#flow-control)

![Liste der auf der Arbeitsfläche verfügbaren Aktivitäten](../assets/orchestrated-activities.png){width="80%" align="left"}

## Targeting-Aktivitäten {#targeting}

Diese Aktivitäten sind spezifisch für die Zielgruppenbestimmung. Sie ermöglichen es Ihnen, ein oder mehrere Ziele zu erstellen, indem Sie eine Zielgruppe definieren und diese Zielgruppen mithilfe von Schnittmenge, Vereinigung oder Ausschluss aufteilen oder kombinieren.

![Liste der Targeting-Aktivitäten](../assets/targeting-activities.png){width="40%" align="left"}

* [Zielgruppe erstellen](build-audience.md): Mit dieser Aktivität definieren Sie Ihre Zielpopulation. Sie können entweder eine vorhandene Zielgruppe auswählen oder den Regel-Builder verwenden, um Ihre eigene Abfrage zu definieren.
* [Dimensionsänderung](change-dimension.md): Ändern Sie die Zielgruppendimension beim Erstellen Ihrer orchestrierten Kampagne.
* [Kombinieren](combine.md): Mit dieser Aktivität segmentieren Sie Ihre eingehende Population. Sie können eine Vereinigung, eine Schnittmenge oder einen Ausschluss verwenden.
* [Deduplizierung](deduplication.md): Mit dieser Aktivität löschen Sie Duplikate in Ergebnissen aus eingehenden Aktivitäten.
* [Anreicherung](enrichment.md): Definieren Sie zusätzliche Daten, die in Ihrer orchestrierten Kampagne verarbeitet werden sollen. Mit dieser Aktivität können Sie die eingehende Transition nutzen und die Aktivität so konfigurieren, dass sie die ausgehende Transition mit zusätzlichen Daten ergänzt.
* [Abstimmung](reconciliation.md): Mit dieser Aktivität definieren Sie die Verknüpfung zwischen den Journey Optimizer-Daten und den Daten in einer Arbeitstabelle, z. B. Daten, die aus einer externen Datei geladen wurden.
* [Aufspaltung](split.md): Segmentieren Sie die eingehende Population in mehrere Teilmengen.

## Kanalaktivitäten {#channel}

In Adobe Journey Optimizer können Sie Marketing-Kampagnen automatisieren und über mehrere Kanäle hinweg ausführen. Sie können Kanalaktivitäten in der Arbeitsfläche kombinieren, um eine kanalübergreifende orchestrierte Kampagne zu erstellen, mit der Trigger basierend auf dem Kundenverhalten erstellt werden können. Die folgenden **Kanalaktivitäten** sind verfügbar: E-Mail und SMS. [Erfahren Sie, wie Sie im Kontext einer orchestrierten Kampagne eine Kanalaktion erstellen](channels.md).

## Aktivitäten zur Flusskontrolle {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Endaktivität"
>abstract="Die **Ende**-Aktivität ermöglicht es Ihnen, das Ende einer orchestrierten Kampagne grafisch zu markieren. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional."

![Liste der Aktivitäten zur Flusskontrolle](../assets/flow-control-activities.png){width="30%" align="left"}

Die folgenden Aktivitäten dienen der Organisation und Ausführung orchestrierter Kampagnen. Ihre Hauptaufgabe ist es, die anderen Aktivitäten zu koordinieren:

* [Und-Verknüpfung](and-join.md): Synchronisieren Sie mehrere Ausführungszweige einer orchestrierten Kampagne.
* [Verzweigung](fork.md): Erstellen Sie ausgehende Transitionen, um mehrere Aktivitäten gleichzeitig zu starten.
* [Warten](wait.md): Hält die Ausführung eines Teils einer orchestrierten Kampagne vorübergehend an.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>Die **Ende**-Aktivität markiert grafisch das Ende einer orchestrierten Kampagne. Diese Aktivität hat keine funktionalen Auswirkungen und ist daher optional.
