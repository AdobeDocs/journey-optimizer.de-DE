---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität Warten in mehrstufigen Kampagnen
description: Erfahren Sie, wie Sie die Aktivität Warten in mehrstufigen Kampagnen verwenden
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 85%

---

# Warten {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Aktivität „Warten“"
>abstract="Die Aktivität **Warten** wird verwendet, um die Transition von einer Aktivität zu einer anderen zu verzögern."

Die Aktivität **Warten** ist eine Aktivität zur **Flusskontrolle**. Sie wird verwendet, um einen bestimmten Zeitraum zwischen der Ausführung zweier Aktivitäten zu definieren. Beispielsweise kann man mehrere Tage nach einer E-Mail-Versandaktivität warten, dann die während dieses Zeitraums erfolgten Öffnungen und Klicks analysieren, bevor man weitere Verarbeitungsschritte (Erinnerungs-E-Mail, Zielgruppenerstellung etc.) unternimmt.

## Konfiguration{#wait-configuration}

Gehen Sie folgendermaßen vor, um die Aktivität **Warten** zu konfigurieren:

1. Fügen Sie **mehrstufige Kampagne** Aktivität „Warten“ hinzu.

1. Geben Sie die **Dauer** der Wartezeit zwischen den eingehenden und ausgehenden Transitionen an.

1. Wählen Sie die Zeiteinheit im Feld **Zeiträume** aus: Sekunden, Minuten, Stunden, Tage.

## Beispiel{#wait-example}

Das folgende Beispiel erläutert die Aktivität **Warten** anhand eines typischen Fallbeispiels. Darin wird eine E-Mail mit einer Einladung zu einem Event verschickt. 24 Stunden nach dem Versand wird ein SMS-Versand an dieselbe Population gesendet.

![](../assets/workflow-wait-example.png)
