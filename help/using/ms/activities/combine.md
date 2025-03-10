---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Kombinieren“
description: Erfahren Sie, wie Sie die Aktivität „Kombinieren“ verwenden.
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 100%

---

# Kombinieren {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Die Aktivität „Kombinieren“"
>abstract="Die Aktivität **Kombinieren** ermöglicht die Segmentierung der eingehenden Population. Sie können also verschiedene Populationen vereinen, einen Teil daraus ausschließen oder nur die in mehreren Zielgruppen enthaltenen Datensätze verwenden."

Die Aktivität **Kombinieren** ist eine Aktivität zur **Zielgruppenbestimmung**. Diese Aktivität ermöglicht die Segmentierung Ihrer eingehenden Population. Sie können also verschiedene Populationen vereinen, einen Teil daraus ausschließen oder nur die in mehreren Zielgruppen enthaltenen Datensätze verwenden. Im Folgenden finden Sie die verfügbaren Segmentierungstypen:

<!--
The **Combine** activity can be placed after any other activity, but not at the beginning of the workflow. Any activity can be placed after the **Combine**.
-->

* Eine **Vereinigung** dient dazu, das Ergebnis mehrerer Aktivitäten zu einer einzigen Zielgruppe zusammenzufassen.
* Eine **Schnittmenge** dient dazu, nur die Elemente zu behalten, die den verschiedenen eingehenden Populationen in der Aktivität gemeinsam sind.
* Ein **Ausschluss** dient dazu, gemäß bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen.

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

Führen Sie die folgenden Schritte aus, um mit der Konfiguration der Aktivität **Kombinieren** zu beginnen:

![](../assets/workflow-combine.png)

1. Fügen Sie mehrerer Aktivitäten wie **Zielgruppe erstellen** hinzu, um mindestens zwei verschiedene Ausführungsverzweigungen zu bilden.
1. Fügen Sie die Aktivität **Kombinieren** zu einer der vorherigen Verzweigungen hinzu.
1. Wählen Sie einen der Segmentierungstypen aus: [Vereinigung](#union), [Schnittmenge](#intersection) oder [Ausschluss](#exclusion).
1. Klicken Sie auf **Weiter**.
1. Aktivieren Sie im Abschnitt **Zusammenzuführende Mengen** alle vorherigen Aktivitäten, die Sie zusammenfügen möchten.

## Union {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Abstimmoptionen"
>abstract="Wählen Sie den **Abstimmtyp** aus, um festzulegen, wie Duplikate behandelt werden. Die Option **Schlüssel** ist standardmäßig aktiviert. Das heißt, die Aktivität behält ein Element nur dann bei, wenn die Elemente der verschiedenen eingehenden Transitionen denselben Schlüssel aufweisen. Verwenden Sie die Option **Auswahl an Spalten**, um die Liste der Spalten zu definieren, auf die die Datenabstimmung angewendet werden soll. "

In der Aktivität **Kombinieren** können Sie eine **Vereinigung** konfigurieren. Für die Vereinigung müssen Sie den **Abstimmtyp** auswählen, um festzulegen, wie Dubletten behandelt werden:

* **Nur die Schlüssel** – Standardmodus; die Aktivität behält nur eines der Elemente bei, wenn mehrere aus verschiedenen eingehenden Transitionen stammende Elemente denselben Schlüssel aufweisen. Diese Option kann nur verwendet werden, wenn die eingehenden Populationen homogen sind.
* **Auswahl an Spalten** – Wählen Sie diese Option, um die Liste der Spalten zu definieren, auf die die Datenabstimmung angewendet werden soll. Wählen Sie zunächst die die Quelldaten enthaltende Hauptmenge aus und dann die für die Herstellung der Verknüpfung zu verwendenden Spalten.

## Schnittmenge {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Abstimmoptionen für Schnittmengen"
>abstract="Wählen Sie den **Abstimmtyp** aus, um festzulegen, wie Duplikate behandelt werden. Die Option **Schlüssel** ist standardmäßig aktiviert. Das heißt, die Aktivität behält ein Element nur dann bei, wenn die Elemente der verschiedenen eingehenden Transitionen denselben Schlüssel aufweisen. Verwenden Sie die Option **Auswahl an Spalten**, um die Liste der Spalten zu definieren, auf die die Datenabstimmung angewendet werden soll. "

In der Aktivität **Kombinieren** können Sie eine **Schnittmenge** konfigurieren. Dafür müssen Sie die folgenden zusätzlichen Schritte ausführen:

1. Wählen Sie den **Abstimmtyp**, um festzulegen, wie Duplikate behandelt werden. Siehe den Abschnitt [Vereinigung](#union).
1. Sie können die Option **Komplement erzeugen** aktivieren, wenn Sie die verbleibende Population verarbeiten möchten. Das Komplement enthält die Vereinigung der Ergebnisse aller eingehenden Aktivitäten abzüglich der Schnittmenge. Der Aktivität wird daraufhin eine zusätzliche ausgehende Transition hinzugefügt.

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

In der Aktivität **Kombinieren** können Sie einen **Ausschluss** konfigurieren. Dafür müssen Sie die folgenden zusätzlichen Schritte ausführen:

1. Wählen Sie im Abschnitt **Zusammenzuführende Mengen** die **Hauptmenge** aus den eingehenden Transitionen. Dies ist die Menge, aus der Elemente ausgeschlossen werden. Die anderen Mengen stimmen mit Elementen überein, bevor sie aus der Primärmenge ausgeschlossen werden.
1. Bei Bedarf können Sie die eingehenden Tabellen anpassen. Um eine Zielgruppe aus einer anderen Dimension auszuschließen, muss diese Zielgruppe tatsächlich auf dieselbe Zielgruppendimension wie die Hauptzielgruppe zurückgesetzt werden. Klicken Sie dazu im Abschnitt **Ausschlussregeln** auf **Regel hinzufügen** und geben Sie die Bedingungen für die Dimensionsänderung an. Die Datenabstimmung wird entweder über ein Attribut oder über einen Join durchgeführt.
1. Sie können die Option **Komplement erzeugen** aktivieren, wenn Sie die verbleibende Population verarbeiten möchten. Siehe den Abschnitt [Schnittmenge](#intersection).

## Beispiele{#combine-examples}

Im folgenden Beispiel verwenden wir die Aktivität **Kombinieren**, und wir fügen die Aktivität **Vereinigung** hinzu, um alle Profile der beiden Abfragen abzurufen: Personen zwischen 18 und 27 Jahren und Personen zwischen 34 und 40 Jahren.

![](../assets/workflow-union-example.png)

Das folgende Beispiel zeigt die **Schnittmenge** zwischen zwei Abfrageaktivitäten. Sie wird hier zum Abrufen von Profilen verwendet, die zwischen 18 und 27 Jahre alt sind und deren E-Mail-Adresse angegeben wurde.

![](../assets/workflow-intersection-example.png)

Folgendes **Ausschluss**-Beispiel zeigt zwei Abfragen, die zum Filtern von Profilen konfiguriert wurden, die zwischen 18 und 27 Jahre alt sind und die eine Adobe-E-Mail-Domain haben. Die Profile mit einer Adobe-E-Mail-Domain werden dann aus der ersten Menge ausgeschlossen.

![](../assets/workflow-exclusion-example.png)
