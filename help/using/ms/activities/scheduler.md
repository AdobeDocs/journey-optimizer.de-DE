---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Planung“
description: Erfahren Sie, wie Sie die Planungsaktivität in einer orchestrierten Kampagne verwenden
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 35%

---

# Planung {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planungsaktivität"
>abstract="Die **Planung**-Aktivität ermöglicht die Festlegung des Starts der orchestrierten Kampagne. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der koordinierten Kampagne verwendet werden."


Die Aktivität **Planung** ist eine Aktivität zur **Flusssteuerung**. Sie können den Beginn der orchestrierten Kampagne planen. Diese Aktivität sollte als geplanter Start betrachtet werden. Sie kann nur als erste Aktivität der koordinierten Kampagne verwendet werden.

## Best Practices{#scheduler-best-practices}

* Planen Sie keine orchestrierte Kampagne, die öfter als alle 15 Minuten ausgeführt wird, da die Gesamtleistung des Systems beeinträchtigt werden kann und Blockierungen in der Datenbank entstehen können.
* Wenn Sie einen einmaligen Versand in Ihrer orchestrierten Kampagne durchführen möchten, können Sie eine Planungsaktivität hinzufügen und sie auf „Einmal **&quot;**. Sie können außerdem den **Zeitplan** in den Versandeinstellungen festlegen.
* Wenn Sie einen wiederkehrenden Versand innerhalb Ihrer orchestrierten Kampagne durchführen möchten, müssen Sie eine Aktivität des Typs **Planung** verwenden und die Ausführungsfrequenz festlegen. Die Aktivität „Wiederkehrender Versand“ ermöglicht keine Festlegung eines Zeitplans.

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

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Planung“ hinzu.

1. Konfigurieren Sie die **Ausführungshäufigkeit**:

   * **Einmal**: Die orchestrierte Kampagne wird ein einziges Mal ausgeführt.

   * **Täglich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt einmal täglich ausgeführt.

   * **Mehrmals am Tag:** die orchestrierte Kampagne wird regelmäßig mehrmals am Tag ausgeführt. Sie können Ausführungen zu bestimmten Zeiten oder in regelmäßigen Abständen einrichten.

   * **Wöchentlich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt, ein- oder mehrmals pro Woche ausgeführt.

   * **Monatlich**: Die orchestrierte Kampagne wird zu einem bestimmten Zeitpunkt, ein- oder mehrmals im Monat ausgeführt. Sie können Monate auswählen, in denen die orchestrierte Kampagne ausgeführt werden soll. Sie können für die Ausführung von Workflows auch bestimmte Wochentage des Monats auswählen, z. B. am zweiten Dienstag des Monats.

1. Definieren Sie die Ausführungsdetails. Je nach gewählter Frequenz sind verschiedene Parameter (Uhrzeit, Ausführungsintervall, bestimmte Tage etc.) zu konfigurieren.

1. Klicken Sie **Startzeiten in der Vorschau**, um den Zeitplan der nächsten zehn Ausführungen Ihrer orchestrierten Kampagne zu überprüfen.

1. Definieren des Gültigkeitszeitraums des Zeitplans:

   * **Dauerhaft (läuft nie ab)**: Die orchestrierte Kampagne wird entsprechend der angegebenen Häufigkeit ohne Begrenzung des Zeitrahmens oder der Anzahl der Iterationen ausgeführt.

   * **Gültigkeitszeitraum**: Die orchestrierte Kampagne wird entsprechend der angegebenen Häufigkeit bis zu einem bestimmten Datum ausgeführt. Sie müssen Start- und Enddaten angeben.

>[!NOTE]
>
>Wenn Sie die orchestrierte Kampagne sofort starten möchten, können Sie in der oberen Aktionsleiste der Planung auf **Aufgabe ausführen** klicken. Diese Schaltfläche ist nur verfügbar, wenn Sie die koordinierte Kampagne gestartet haben.

## Beispiel{#scheduler-example}

Im folgenden Beispiel wird die Aktivität so konfiguriert, dass die orchestrierte Kampagne mehrmals täglich um 9 und 12 Uhr am Wochentag zwischen dem 1. Oktober 2025 und dem 1. Januar 2026 ausgeführt wird.

![](../assets/workflow-scheduler2.png)
