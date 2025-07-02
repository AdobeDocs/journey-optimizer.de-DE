---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Kombinieren“
description: Erfahren Sie, wie Sie die Aktivität „Kombinieren“ verwenden.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 01c9b947ce9459944c5c16ef177b55e889eb3634
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 53%

---

# Kombinieren {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Die Aktivität „Kombinieren“"
>abstract="Die Aktivität **Kombinieren** ermöglicht die Segmentierung der eingehenden Population. Sie können also verschiedene Populationen vereinen, einen Teil daraus ausschließen oder nur die in mehreren Zielgruppen enthaltenen Datensätze verwenden."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Orchestrierte Kampagne erstellen](../create-orchestrated-campaign.md)<br/><br/>[Aktivitäten orchestrieren](../orchestrate-activities.md)<br/><br/>[ Nachrichten mit orchestrierten Kampagnen senden](../send-messages.md)<br/><br/>[Kampagne starten und überwachen](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimensionsänderung](change-dimension.md) - [Kombinieren](combine.md) - [Deduplizierung](enrichment.md) - [Verzweigung](fork.md) - [Abstimmung](reconciliation.md) - [Aufspaltung](split.md)[ ](wait.md) Warten](deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

Die **[!UICONTROL Kombinieren]**-Aktivität ist eine Art **[!UICONTROL Targeting]**-Aktivität, mit der Sie Ihre eingehende Population effektiv segmentieren können. Damit können Sie mehrere Populationen zusammenführen, bestimmte Segmente ausschließen oder nur die Daten beibehalten, die für mehrere Ziele freigegeben sind.

Die folgenden Segmentierungsoptionen sind verfügbar:

* **[!UICONTROL Vereinigung]**: führt die Ergebnisse mehrerer Aktivitäten zu einer einzigen einheitlichen Zielgruppe zusammen.

* **[!UICONTROL Schnittmenge]**: Behält nur die Elemente bei, die in allen eingehenden Populationen gleich sind.

* **[!UICONTROL Ausschluss]**: entfernt Elemente aus einer Population anhand festgelegter Kriterien.

## Konfigurieren der Aktivität „Kombinieren“ {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="Optionen für das Zusammenführen von Schnittmengen"
>abstract="Die Schnittmenge dient dazu, nur die Elemente zu behalten, die den verschiedenen eingehenden Populationen in der Aktivität gemeinsam sind. Aktivieren Sie im Abschnitt „Zusammenzuführende Mengen“ alle vorherigen Aktivitäten, die Sie zusammenfügen möchten."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="Optionen für die Zusammenführung von Ausschlüssen"
>abstract="Der Ausschluss dient dazu, gemäß bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen. Aktivieren Sie im Abschnitt „Zusammenzuführende Mengen“ alle vorherigen Aktivitäten, die Sie zusammenfügen möchten."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="Auswählen des Segmentierungstyps"
>abstract="Wählen Sie aus, wie Zielgruppen kombiniert werden. Eine **Vereinigung** dient dazu, das Ergebnis mehrerer Aktivitäten zu einer einzigen Zielgruppe zusammenzufassen. Eine **Schnittmenge** dient dazu, nur die Elemente beizubehalten, die den verschiedenen eingehenden Populationen in der Aktivität gemeinsam sind. Ein **Ausschluss** dient dazu, gemäß bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen. "

Führen Sie die folgenden Schritte aus, um mit der Konfiguration der Aktivität **[!UICONTROL Kombinieren]** zu beginnen:

![](../assets/orchestrated-union.png)

1. Fügen Sie mehrerer Aktivitäten wie **[!UICONTROL Zielgruppe erstellen]** hinzu, um mindestens zwei verschiedene Ausführungsverzweigungen zu bilden.
1. Fügen Sie die Aktivität **[!UICONTROL Kombinieren]** zu einer der vorherigen Verzweigungen hinzu.
1. Wählen Sie einen der Segmentierungstypen aus: [Vereinigung](#union), [Schnittmenge](#intersection) oder [Ausschluss](#exclusion).
1. Klicken Sie auf **[!UICONTROL Fortfahren]**.
1. Aktivieren Sie im Abschnitt **[!UICONTROL Zusammenzuführende Mengen]** alle vorherigen Aktivitäten, die Sie zusammenfügen möchten.

## Union {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Abstimmoptionen"
>abstract="Wählen Sie den **Abstimmtyp** aus, um festzulegen, wie Duplikate behandelt werden. Die Option **Schlüssel** ist standardmäßig aktiviert. Das heißt, die Aktivität behält ein Element nur dann bei, wenn die Elemente der verschiedenen eingehenden Transitionen denselben Schlüssel aufweisen. Verwenden Sie die Option **Auswahl an Spalten**, um die Liste der Spalten zu definieren, auf die die Datenabstimmung angewendet werden soll. "

Innerhalb der Aktivität **[!UICONTROL Kombinieren]** können Sie eine **[!UICONTROL Vereinigung]** konfigurieren, indem Sie einen **[!UICONTROL Abstimmtyp]** auswählen, um zu bestimmen, wie doppelte Datensätze verwaltet werden:

* **[!UICONTROL Nur Schlüssel]** (Standard): Behält einen einzelnen Datensatz bei, wenn mehrere eingehende Transitionen denselben Schlüssel verwenden. Diese Option ist nur anwendbar, wenn die eingehenden Populationen homogen sind.

* **[!UICONTROL Auswahl von Spalten]**: Hier können Sie angeben, welche Spalten für die Datenabstimmung verwendet werden sollen. Wählen Sie **[!UICONTROL Attribut hinzufügen]** aus.

Im folgenden Beispiel wird eine Aktivität **[!UICONTROL Kombinieren]** mit einer **[!UICONTROL Vereinigung]** verwendet, um die Ergebnisse zweier Abfragen, **Mitglieder des Treueprogramms** und **Käufer**, zu einer einzigen, größeren Zielgruppe zusammenzuführen, die alle Profile aus beiden Segmenten enthält.

![](../assets/orchestrated-union-example.png)

## Schnittmenge {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Abstimmoptionen für Schnittmengen"
>abstract="Wählen Sie den **Abstimmtyp** aus, um festzulegen, wie Duplikate behandelt werden. Die Option **Schlüssel** ist standardmäßig aktiviert. Das heißt, die Aktivität behält ein Element nur dann bei, wenn die Elemente der verschiedenen eingehenden Transitionen denselben Schlüssel aufweisen. Verwenden Sie die Option **Auswahl an Spalten**, um die Liste der Spalten zu definieren, auf die die Datenabstimmung angewendet werden soll. "

In der Aktivität **[!UICONTROL Kombinieren]** können Sie eine **[!UICONTROL Schnittmenge]** konfigurieren. Dafür müssen Sie die folgenden zusätzlichen Schritte ausführen:

1. Wählen Sie den **[!UICONTROL Abstimmtyp]**, um festzulegen, wie Duplikate behandelt werden:

   * **[!UICONTROL Nur Schlüssel]** (Standard): Behält einen einzelnen Datensatz bei, wenn mehrere eingehende Transitionen denselben Schlüssel verwenden. Diese Option ist nur anwendbar, wenn die eingehenden Populationen homogen sind.

   * **[!UICONTROL Auswahl von Spalten]**: Hier können Sie angeben, welche Spalten für die Datenabstimmung verwendet werden sollen. Wählen Sie **[!UICONTROL Attribut hinzufügen]** aus.

1. Aktivieren Sie **[!UICONTROL Komplement erzeugen]**, wenn Sie die verbleibende Population verarbeiten möchten. Das Komplement enthält die Vereinigung aller eingehenden Aktivitätsergebnisse, mit Ausnahme der Schnittmenge. Der Aktivität wird eine zusätzliche ausgehende Transition hinzugefügt.

Das folgende Beispiel veranschaulicht die Verwendung der **[!UICONTROL Schnittmenge]** zwischen zwei Abfrageaktivitäten. Sie wird verwendet, um Profile zu identifizieren, die **Mitglieder des Treueprogramms** sind und innerhalb des letzten Monats einen Kauf getätigt haben.

![](../assets/orchestrated-intersection-example.png)


## Ausschluss {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="Ausschlussregeln"
>abstract="Bei Bedarf können Sie die eingehenden Tabellen anpassen. Um eine Zielgruppe aus einer anderen Dimension auszuschließen, muss diese Zielgruppe tatsächlich auf dieselbe Zielgruppendimension wie die Hauptzielgruppe zurückgesetzt werden. Klicken Sie dazu im Abschnitt „Ausschlussregeln“ auf „Regel hinzufügen“ und geben Sie die Bedingungen für die Dimensionsänderung an. Die Datenabstimmung wird entweder über ein Attribut oder über einen Join durchgeführt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="Auswählen von Sets, die kombiniert werden sollen"
>abstract="Wählen Sie im Abschnitt **Zusammenzuführende Mengen** die **Hauptmenge** aus den eingehenden Transitionen. Dies ist die Menge, aus der Elemente ausgeschlossen werden. Die anderen Mengen stimmen mit Elementen überein, bevor sie aus der Primärmenge ausgeschlossen werden."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="Ausschlussregeln"
>abstract="Bei Bedarf können Sie die eingehenden Tabellen anpassen. Um eine Zielgruppe aus einer anderen Dimension auszuschließen, muss diese Zielgruppe tatsächlich auf dieselbe Zielgruppendimension wie die Hauptzielgruppe zurückgesetzt werden. Klicken Sie dazu im Abschnitt „Ausschlussregeln“ auf „Regel hinzufügen“ und geben Sie die Bedingungen für die Dimensionsänderung an. Die Datenabstimmung wird entweder über ein Attribut oder über einen Join durchgeführt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="Kombinieren von „Komplement erzeugen“"
>abstract="Aktivieren Sie die Option „Komplement erzeugen“, um die verbleibende Population in einer zusätzlichen Transition zu verarbeiten."

In der Aktivität **[!UICONTROL Kombinieren]** können Sie einen **[!UICONTROL Ausschluss]** konfigurieren. Dafür müssen Sie die folgenden zusätzlichen Schritte ausführen:

1. Wählen Sie im **[!UICONTROL Zusammenzufügende Sätze]** die **[!UICONTROL Primäre Gruppe]**, die die Hauptpopulation darstellt. Die in den anderen Sätzen gefundenen Datensätze werden aus dieser primären Gruppe ausgeschlossen.

1. Bei Bedarf können Sie eingehende Tabellen anpassen, um Ziele aus verschiedenen Dimensionen auszurichten. Um eine Zielgruppe aus einer anderen Dimension auszuschließen, muss sie zunächst in dieselbe Zielgruppendimension wie die Hauptpopulation aufgenommen werden. Klicken Sie dazu auf **[!UICONTROL Regel hinzufügen]** und definieren Sie die Bedingungen zum Ändern der Dimension. Die Abstimmung erfolgt dann entweder mit einem Attribut oder einem Join.

1. Aktivieren Sie **[!UICONTROL Komplement erzeugen]**, wenn Sie die verbleibende Population verarbeiten möchten. Das Komplement enthält die Vereinigung aller eingehenden Aktivitätsergebnisse, mit Ausnahme der Schnittmenge. Der Aktivität wird eine zusätzliche ausgehende Transition hinzugefügt.

Das folgende **[!UICONTROL Ausschluss]**-Beispiel zeigt zwei Abfragen, die zum Filtern von Profilen konfiguriert wurden, die ein Produkt gekauft haben. Die Profile, die keine Treueprogramm-Mitgliedschaft haben, werden dann aus dem ersten Satz ausgeschlossen.

![](../assets/orchestrated-exclusion-example.png)

