---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Planung“
description: Erfahren Sie, wie Sie die Planungsaktivität in einer mehrstufigen Kampagne verwenden
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 42%

---

# Planung {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planungsaktivität"
>abstract="Mit der Aktivität **Planung** können Sie planen, wann die mehrstufige Kampagne gestartet werden soll. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der mehrstufigen Kampagne verwendet werden."


Die Aktivität **Planung** ist eine Aktivität zur **Flusssteuerung**. Damit können Sie den Beginn der mehrstufigen Kampagne planen. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der mehrstufigen Kampagne verwendet werden.

## Best Practices{#scheduler-best-practices}

* Planen Sie keine mehrstufige Kampagne, die öfter als alle 15 Minuten ausgeführt wird, da dies die Gesamtleistung des Systems beeinträchtigen und Blöcke in der Datenbank erstellen kann.
* Wenn Sie einen einmaligen Versand in Ihrer mehrstufigen Kampagne durchführen möchten, können Sie eine Planungsaktivität hinzufügen und sie auf „Einmal **&quot;**. Sie können außerdem den **Zeitplan** in den Versandeinstellungen festlegen.
* Wenn Sie einen wiederkehrenden Versand in Ihrer mehrstufigen Kampagne durchführen möchten, müssen Sie eine **Planung“** und die Ausführungsfrequenz festlegen. Die Aktivität „Wiederkehrender Versand“ ermöglicht keine Festlegung eines Zeitplans.

## Konfigurieren der Aktivität „Planung“ {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Gültigkeit der Planung"
>abstract="Sie können einen Gültigkeitszeitraum für die Planung definieren. Er kann dauerhaft sein (Standard) oder bis zu einem bestimmten Datum gültig sein."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Planungsoptionen"
>abstract="Definieren Sie die Häufigkeit der Planung. Er kann zu einem bestimmten Zeitpunkt, einmal oder mehrmals pro Tag, Woche oder Monat, ausgeführt werden."

Gehen Sie folgendermaßen vor, um die Aktivität **Planung** zu konfigurieren:

![](../assets/workflow-scheduler.png)

1. Fügen Sie **mehrstufigen Kampagne** Aktivität „Planung“ hinzu.

1. Konfigurieren Sie die **Ausführungshäufigkeit**:

   * **Einmal**: Die mehrstufige Kampagne wird ein einziges Mal ausgeführt.

   * **Täglich**: Die mehrstufige Kampagne wird zu einem bestimmten Zeitpunkt einmal täglich ausgeführt.

   * **Mehrmals am Tag:** Die mehrstufige Kampagne wird regelmäßig mehrmals am Tag ausgeführt. Sie können Ausführungen zu bestimmten Zeiten oder in regelmäßigen Abständen einrichten.

   * **Wöchentlich**: Die mehrstufige Kampagne wird zu einem bestimmten Zeitpunkt einmal oder mehrmals pro Woche ausgeführt.

   * **Monatlich**: Die mehrstufige Kampagne wird zu einem bestimmten Zeitpunkt ausgeführt, ein- oder mehrmals im Monat. Sie können Monate auswählen, in denen die mehrstufige Kampagne ausgeführt werden soll. Sie können für die Ausführung von Workflows auch bestimmte Wochentage des Monats auswählen, z. B. am zweiten Dienstag des Monats.

1. Definieren Sie die Ausführungsdetails. Je nach gewählter Frequenz sind verschiedene Parameter (Uhrzeit, Ausführungsintervall, bestimmte Tage etc.) zu konfigurieren.

1. Klicken Sie **Startzeiten in der Vorschau**, um den Zeitplan der nächsten zehn Ausführungen Ihrer mehrstufigen Kampagne zu überprüfen.

1. Definieren des Gültigkeitszeitraums des Zeitplans:

   * **Dauerhaft (läuft nie ab)**: Die mehrstufige Kampagne wird entsprechend der angegebenen Häufigkeit ohne Begrenzung des Zeitrahmens oder der Anzahl der Iterationen ausgeführt.

   * **Gültigkeitszeitraum**: Die mehrstufige Kampagne wird entsprechend der angegebenen Häufigkeit bis zu einem bestimmten Datum ausgeführt. Sie müssen Start- und Enddaten angeben.

>[!NOTE]
>
>Wenn Sie die mehrstufige Kampagne sofort starten möchten, können Sie in der oberen Aktionsleiste der Planung auf **Aufgabe ausführen** klicken. Diese Schaltfläche ist nur verfügbar, wenn Sie die mehrstufige Kampagne gestartet haben.

## Beispiel{#scheduler-example}

Im folgenden Beispiel wird die Aktivität so konfiguriert, dass die mehrstufige Kampagne mehrmals täglich um 9 und 12 Uhr an jedem Wochentag vom 1. Oktober 2025 bis zum 1. Januar 2026 ausgeführt wird.

![](../assets/workflow-scheduler2.png)
