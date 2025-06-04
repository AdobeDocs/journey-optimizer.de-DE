---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Aufspaltung“
description: Erfahren Sie, wie Sie die Aufspaltungsaktivität in einer orchestrierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 83%

---

# Aufspaltung {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Aktivität „Aufspaltung“"
>abstract="Mit der Aktivität **Aufspaltung** können eingehende Populationen basierend auf unterschiedlichen Auswahlkriterien in mehrere Teilmengen segmentiert werden, z. B. Filterregeln oder Populationsgröße."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Orchestrierte Kampagnenaktivitäten |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](gs-campaign-creation.md) | [Orchestrierte Kampagne erstellen](create-orchestrated-campaign.md)<br/><br/>[Aktivitäten orchestrieren](orchestrate-activities.md)<br/><br/>[ Nachrichten mit orchestrierten Kampagnen senden](send-messages.md)<br/><br/>[Kampagne starten und überwachen](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](orchestrated-query-modeler.md)<br/><br/>[Erstellen Sie Ihre ersten ](build-query.md)<br/><br/>[-Bearbeitungsausdrücke](edit-expressions.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimensionsänderung](activities/change-dimension.md) - [Kombinieren](activities/combine.md) - [Deduplizierung](activities/enrichment.md) - [Verzweigung](activities/fork.md) - [Abstimmung](activities/reconciliation.md) - [Aufspaltung](activities/split.md) [&#128279;](activities/wait.md) Warten[&#128279;](activities/deduplication.md)  |

{style="table-layout:fixed"}

+++

<br/><br/>

Die Aktivität **Aufspaltung** ist eine Aktivität zur **Zielgruppenbestimmung**, mit der Sie eingehende Populationen basierend auf unterschiedlichen Auswahlkriterien in mehrere Teilmengen segmentieren können, z. B. Filterregeln oder Populationsgröße.

## Konfigurieren der Aufspaltungsaktivität {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmente für die Aktivität „Aufspaltung“"
>abstract="Es können beliebig viele Teilmengen hinzugefügt werden, um die eingehende Population zu segmentieren.<br/></br>Bei Ausführung der Aktivität **Aufspaltung** wird die Population sukzessive in unterschiedliche Teilmengen segmentiert, und zwar in der Reihenfolge, in der diese zur Aktivität hinzugefügt werden. Vergewissern Sie sich vor dem Start Ihrer orchestrierten Kampagne, dass Sie die Teilmengen mithilfe der Pfeilschaltflächen in der für Sie passenden Reihenfolge angeordnet haben."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filter „Aufspaltungsaktivität“"
>abstract="Auf **[!UICONTROL Filter erstellen]** klicken und die gewünschte Filterregel mithilfe des Abfrage-Modelers konfigurieren, um eine Filterbedingung auf die Teilmenge anzuwenden. Es können beispielsweise Profile aus der eingehenden Population eingeschlossen werden, deren E-Mail-Adresse in der Datenbank vorhanden ist."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Begrenzung der Aufspaltungsaktivität"
>abstract="Um die Anzahl der von der Teilmenge ausgewählten Profile zu begrenzen, muss **[!UICONTROL Grenzwert aktivieren]** aktiviert und die Anzahl oder der Prozentsatz der einzuschließenden Population angegeben werden."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Sortierung der Aufspaltungsaktivität"
>abstract="Beim Festlegen einer Populationsbegrenzung für eine Teilmenge können die ausgewählten Profile anhand eines bestimmten Profilattributs in auf- oder absteigender Reihenfolge sortiert werden. Dazu die Option **Sortierung aktivieren** einschalten. Teilmengen können z. B. so eingeschränkt werden, dass nur die 50 Top-Profile mit dem höchsten Einkaufsbetrag einbezogen werden."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Aufspaltung – Komplement erzeugen"
>abstract="Nachdem Sie alle Teilmengen konfiguriert haben, kann die verbleibende Population ausgewählt werden, die keiner der Teilmengen entspricht, und in eine zusätzliche ausgehende Transition eingeschlossen werden. Schalten Sie dazu die Option **Komplement erzeugen** ein."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Alle Teilmengen in derselben Tabelle erzeugen"
>abstract="Diese Option aktivieren, um alle Teilmengen in einer Ausgabetransition zusammenzufassen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Leere Transition überspringen"
>abstract="Die Option **[!UICONTROL Leere Transition überspringen]** aktivieren, um die ausgehende Transition für diese Teilmenge zu deaktivieren, wenn die Eingangspopulation leer ist."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Überschneidung der Ausgabepopulationen zulassen"
>abstract=" Die Option **[!UICONTROL Überschneidung der Ausgabepopulationen zulassen]** ermöglicht den Umgang mit Profilen, die in mehreren Teilmengen enthalten sind. Wenn das Kästchen nicht aktiviert ist, stellt die Aufspaltungsaktivität sicher, dass eine Empfängerin oder ein Empfänger nicht in mehreren Ausgangstransitionen vorhanden sein kann, selbst wenn sie bzw. er die Kriterien mehrerer Teilmengen erfüllt. Sie bzw. er befindet sich in der Zielgruppe der ersten Registerkarte mit entsprechenden Kriterien. Wenn das Kästchen aktiviert ist, können die Empfangenden in mehreren Teilmengen gefunden werden, falls sie ihren Filterkriterien entsprechen."

Folgen Sie diesen Schritten, um die Aktivität **Aufspaltung** zu konfigurieren:

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Aufspaltung“ hinzu.

1. Der Konfigurationsbereich für die Aktivität wird mit einer standardmäßigen Teilmenge geöffnet. Klicken Sie auf die Schaltfläche **Segment hinzufügen**, um so viele Teilmengen wie gewünscht zum Segmentieren der eingehenden Population hinzuzufügen.

   ![](../assets/workflow-split.png)

   >[!IMPORTANT]
   >
   >Bei Ausführung der Aktivität **Aufspaltung** wird die Population sukzessive in unterschiedliche Teilmengen segmentiert, und zwar in der Reihenfolge, in der diese zur Aktivität hinzugefügt werden. Wenn beispielsweise die erste Teilmenge 70 % der Anfangspopulation abruft, werden die Auswahlkriterien der nächsten hinzugefügten Teilmenge nur auf die restlichen 30 % angewendet usw.
   >
   >Stellen Sie vor Beginn einer orchestrierten Kampagne sicher, dass Sie die Teilmengen in der Ihren Anforderungen entsprechenden Reihenfolge bestellt haben. Verwenden Sie dazu die Pfeilschaltflächen, um die Position einer Teilmenge zu ändern.

1. Sobald die Teilmengen hinzugefügt wurden, zeigt die Aktivität für jede Teilmenge eine ausgehende Transition. Es wird dringend empfohlen, den Titel jeder Teilmenge zu ändern, um sie auf der koordinierten Kampagnen-Arbeitsfläche leicht identifizieren zu können.

1. Konfigurieren Sie, wie jede Teilmenge die eingehende Population filtern soll. Gehen Sie dazu wie folgt vor:

   1. Öffnen Sie die Teilmenge, um ihre Eigenschaften anzuzeigen.

   1. Auf **[!UICONTROL Filter erstellen]** klicken und die gewünschte Filterregel mithilfe des Abfrage-Modelers konfigurieren, um eine Filterbedingung auf die Teilmenge anzuwenden. Es können beispielsweise Profile aus der eingehenden Population eingeschlossen werden, deren E-Mail-Adresse in der Datenbank vorhanden ist.

   1. Um die Anzahl der von der Teilmenge ausgewählten Profile zu begrenzen, muss **[!UICONTROL Grenzwert aktivieren]** aktiviert und die Anzahl oder der Prozentsatz der einzuschließenden Population angegeben werden.

   1. Um eine Transition zu deaktivieren, wenn die Eingangspopulation leer ist, aktivieren Sie die Option **[!UICONTROL Leere Transition überspringen]**. Wenn kein Profil mit der Teilmenge übereinstimmt, wird die orchestrierte Kampagne nicht auf die nächste Aktivität umgestellt.

      ![](../assets/workflow-split-subset.png)

1. Nachdem Sie alle Teilmengen konfiguriert haben, kann die verbleibende Population ausgewählt werden, die keiner der Teilmengen entspricht, und in eine zusätzliche ausgehende Transition eingeschlossen werden. Schalten Sie dazu die Option **[!UICONTROL Komplement erzeugen]** ein.

   ![](../assets/workflow-split-complement.png)

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Alle Teilmengen in derselben Tabelle generieren]** ermöglicht die Gruppierung aller Teilmengen in einer ausgehenden Transition.

1. Die Option **[!UICONTROL Überlappung der Ausgabepopulationen zulassen]** ermöglicht den Umgang mit Profilen, die in mehreren Teilmengen enthalten sind:

   * Wenn das Kästchen nicht aktiviert ist, stellt die Aufspaltungsaktivität sicher, dass eine Empfängerin oder ein Empfänger nicht in mehreren Ausgangstransitionen vorhanden sein kann, selbst wenn sie bzw. er die Kriterien mehrerer Teilmengen erfüllt. Sie befinden sich in der Zielgruppe der ersten Registerkarte mit passenden Kriterien.
   * Wenn das Kästchen aktiviert ist, können die Empfangenden in mehreren Teilmengen gefunden werden, falls sie ihren Filterkriterien entsprechen. Best Practice ist die Verwendung exklusiver Kriterien.

Der Aktivität ist jetzt konfiguriert. Bei der orchestrierten Kampagnenausführung wird die Population in der Reihenfolge, in der sie der Aktivität hinzugefügt wurden, in die verschiedenen Untergruppen segmentiert.

## Beispiel{#split-example}

Im folgenden Beispiel wird die Aktivität **[!UICONTROL Aufspaltung]** verwendet, um eine Zielgruppe basierend auf dem Kommunikationskanal, den wir verwenden möchten, in verschiedene Teilmengen zu unterteilen:

* **Teilmenge 1 „Push“**: Diese Teilmenge umfasst alle Profile, die unsere Mobile App installiert haben.
* **Teilmenge 2 „SMS“**: Benutzende von Mobiltelefonen: Für die verbleibende Population, die nicht in Teilmenge 1 fiel, wendet Teilmenge 2 eine Filterregel an, um Profile mit Mobiltelefonen in der Datenbank auszuwählen.
* **Komplement-Transition**: Diese Transition erfasst alle verbleibenden Profile, die weder Teilmenge 1 noch Teilmenge 2 entsprachen. Insbesondere enthält sie Profile, die weder die Mobile App installiert haben noch über ein Mobiltelefon verfügen, z. B. Benutzende, die die Mobile App nicht installiert haben oder keine registrierte Mobiltelefonnummer haben.

![](../assets/workflow-split-example.png)
