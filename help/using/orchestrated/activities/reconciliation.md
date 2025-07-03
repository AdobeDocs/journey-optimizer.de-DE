---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Abstimmung“
description: Erfahren Sie, wie Sie die Aktivität Abstimmung in einer orchestrierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 34%

---

# Abstimmung {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Aktivität „Abstimmung“"
>abstract="Die Aktivität **Abstimmung** ist eine Aktivität zur **Zielgruppenbestimmung**, mit der Sie die Verknüpfung zwischen den Daten in der Adobe Campaign-Datenbank und den Daten in einer Arbeitstabelle definieren können."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Abstimmung – Feld auswählen"
>abstract="Abstimmung – Feld auswählen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Abstimmung – Bedingung erstellen"
>abstract="Abstimmung – Bedingung erstellen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Abstimmung – Komplement erzeugen"
>abstract="Abstimmung – Komplement erzeugen"


+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Zugreifen auf und Verwalten von orchestrierten Kampagnen](../access-manage-orchestrated-campaigns.md) | [Wichtige Schritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md)<br/><br/>[Erstellen und Planen der Kampagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](../orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](../orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](../build-query.md)<br/><br/>[Ausdrücke bearbeiten](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimension ändern](change-dimension.md) - [Kanalaktivitäten](channels.md) - [Kombinieren](combine.md) - [Anreicherung](deduplication.md) - [Formulare](enrichment.md) - [Abstimmung](fork.md) <b>[ ](reconciliation.md)</b> [ ](save-audience.md) [ ](split.md) ->Zielgruppe speichern[ -AufspaltungWarten](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Die Aktivität **[!UICONTROL Abstimmung]** ist eine **[!UICONTROL Targeting]**-Aktivität, mit der Sie die Relation zwischen den Daten in Adobe Journey Optimizer und den Daten in einer Arbeitstabelle definieren können, z. B. Daten, die aus einer externen Datei geladen wurden.

Die Aktivität **[!UICONTROL Anreicherung]** ermöglicht das Hinzufügen zusätzlicher Daten zu einer orchestrierten Kampagne, z. B. durch Kombination von Daten aus mehreren Quellen oder durch Verknüpfung mit einer temporären Ressource. Dagegen werden mit der Aktivität **[!UICONTROL Abstimmung]** nicht identifizierte oder externe Daten mit vorhandenen Ressourcen in der Datenbank abgeglichen.

**[!UICONTROL Abstimmung]** erfordert, dass die entsprechenden Datensätze bereits im System vorhanden sind. Wenn Sie beispielsweise eine Kaufdatei importieren, in der Produkte, Zeitstempel und Kundeninformationen aufgelistet sind, müssen sowohl die Produkte als auch die Kunden bereits in der Datenbank vorhanden sein, um den Link herzustellen.

## Konfigurieren der Abstimmungsaktivität {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Zielgruppendimension"
>abstract="Wählen Sie die neue Zielgruppendimension aus. Mit einer Dimension können Sie die Zielpopulation definieren: Empfängerinnen und Empfänger, Abonnentinnen und Abonnenten der App, Benutzerinnen und Benutzer, Abonnentinnen und Abonnenten usw. Standardmäßig ist die aktuelle Zielgruppendimension ausgewählt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Abstimmregeln"
>abstract="Wählen Sie die für die Deduplizierung zu verwendenden Abstimmungsregeln aus. Um Attribute zu verwenden, wählen Sie die Option **Einfache Attribute** und dann die Quell- und Zielfelder aus. Um mithilfe des Abfrage-Modelers eine eigene Abstimmbedingung zu erstellen, wählen Sie die Option **Erweiterte Abstimmbedingungen** aus."
>additional-url="https://experienceleague.adobe.com/de/docs/campaign-web/v8/query-database/query-modeler-overview" text="Arbeiten mit dem Abfrage-Modeler"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Auswählen der Zielgruppendimension"
>abstract="Wählen Sie die Zielgruppendimension für Ihre eingehenden Daten zum Abstimmen aus."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=de#targeting-dimensions" text="Zielgruppendimensionen"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Beibehalten nicht abgestimmter Daten"
>abstract="Standardmäßig werden nicht abgestimmte Daten in der ausgehenden Transition beibehalten und stehen in der Arbeitstabelle zur späteren Verwendung zur Verfügung. Um nicht abgestimmte Daten zu entfernen, deaktivieren Sie die Option **Nicht abgestimmte Daten beibehalten**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Abstimmattribut"
>abstract="Wählen Sie das Attribut aus, das zur Abstimmung der Daten verwendet werden soll, und klicken Sie auf „Bestätigen“."

Gehen Sie wie folgt vor, um die Aktivität **[!UICONTROL Abstimmung]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL Workflow]** Aktivität Abstimmung hinzu.

1. Wählen Sie eine neue Zielgruppendimension aus, um zu definieren, auf wen Sie abzielen, z. B. Empfänger oder Abonnenten.

1. Legen Sie die Felder fest, die für den Abgleich Ihrer eingehenden Daten mit vorhandenen Profilen verwendet werden sollen.

1. Um Daten mithilfe einfacher Felder abzugleichen, wählen Sie **[!UICONTROL Einfache Attribute]** aus.

1. Legen Sie die passenden Felder fest:

   * **[!UICONTROL Source]**: Listet die eingehenden Datenfelder auf.

   * **[!UICONTROL Ziel]** bezieht sich auf Felder in der ausgewählten Zielgruppendimension.

   Eine Übereinstimmung tritt auf, wenn beide Werte gleich sind, z. B. durch **[!UICONTROL E-Mail]**, um Profile zu identifizieren.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Um weitere übereinstimmende Regeln hinzuzufügen, klicken Sie auf **[!UICONTROL Regel hinzufügen]**. Alle Bedingungen müssen erfüllt sein, damit eine Übereinstimmung eintritt.

1. Für komplexere Bedingungen wählen Sie **[!UICONTROL Erweiterte Abstimmbedingungen]**. Verwenden Sie den [Abfrage-Modellierer](../orchestrated-rule-builder.md), um benutzerdefinierte Logik zu definieren.

1. Um zu filtern, welche Daten abgeglichen werden sollen, klicken Sie auf **[!UICONTROL Filter erstellen]** und definieren Sie Ihre Bedingung im Abfrage-Modellierer.

1. Standardmäßig werden nicht übereinstimmende Datensätze in der ausgehenden Transition beibehalten und in der Arbeitstabelle gespeichert. Um diese zu entfernen, aktivieren Sie die Option **[!UICONTROL Nicht abgestimmte Daten beibehalten]**.

## Beispiel {#example-reconciliation}

In diesem Beispiel wird die Aktivität **[!UICONTROL Abstimmung]** in Adobe Journey Optimizer verwendet, um sicherzustellen, dass E-Mails nur an erkannte Kunden gesendet werden. Die Daten fließen über eine Aktivität vom Typ **[!UICONTROL Zielgruppe lesen]** ein, die auf Benutzende mit früheren Bestellungen abzielt. Die Aktivität **[!UICONTROL Abstimmung]** gleicht diese eingehenden Daten dann mithilfe des E-Mail-Felds mit vorhandenen Profilen in der Datenbank ab.

![](../assets/workflow-reconciliation-sample-1.0.png)
