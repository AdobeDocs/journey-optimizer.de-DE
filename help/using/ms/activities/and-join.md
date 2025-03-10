---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Und-Verknüpfung“
description: Erfahren Sie, wie Sie die Aktivität „Und-Verknüpfung“ in einer mehrstufigen Kampagne verwenden
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 66%

---

# Und-Verknüpfung {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Aktivität &quot;Und-Verknüpfung&quot;"
>abstract="Die Aktivität **Und-Verknüpfung** ermöglicht es, die Ausführung verschiedener Zweige einer mehrstufigen Kampagne zu synchronisieren. Sie wird ausgelöst, sobald alle vorangehenden Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der mehrstufigen Kampagne fortfahren."

Die Aktivität **Und-Verknüpfung** ist eine Aktivität zur **Flusskontrolle**. Dies ermöglicht es, die Ausführung verschiedener mehrstufiger Kampagnen zu synchronisieren.

Diese Aktivität löst ihre ausgehende Transition erst aus, wenn alle eingehenden Transitionen aktiviert sind, d. h. wenn alle vorangegangenen Aktivitäten beendet sind. Auf diese Weise können Sie sicherstellen, dass bestimmte Aktivitäten abgeschlossen sind, bevor Sie mit der Ausführung der mehrstufigen Kampagne fortfahren.

## Konfigurieren der Aktivität „Und-Verknüpfung“{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Zusammenführungssoptionen"
>abstract="Wählen Sie die Aktivitäten aus, die Sie verknüpfen möchten. Wählen Sie in der Dropdown-Liste **Hauptmenge** die Population der eingehenden Transition aus, die Sie beibehalten möchten."

Führen Sie die folgenden Schritte aus, um die Aktivität **Und-Verknüpfung** zu konfigurieren:

![](../assets/workflow-andjoin.png)

1. Fügen Sie mehrere Aktivitäten wie z. B. Kanalaktivitäten hinzu, um mindestens zwei verschiedene Ausführungsverzweigungen zu bilden.
1. Fügen Sie die Aktivität **Und-Verknüpfung** zu einer der Verzweigungen hinzu.
1. Aktivieren Sie im Abschnitt **Zusammenführungsoptionen** alle vorherigen Aktivitäten, denen Sie beitreten möchten.
1. Wählen Sie in der Dropdown-Liste **Hauptmenge** die Population der eingehenden Transition aus, die Sie beibehalten möchten. Die ausgehende Transition darf nur eine der Populationen der eingehenden Transition enthalten.

## Beispiel{#and-join-example}

Das folgende Beispiel zeigt zwei mehrstufige Kampagnenzweige mit einem E-Mail- und SMS-Versand. Die Und-Verknüpfung wird ausgelöst, wenn beide eingehenden Transitionen aktiviert sind. Die Push-Benachrichtigungen werden erst dann gesendet, wenn beide Sendungen abgeschlossen sind.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
