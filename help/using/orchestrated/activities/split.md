---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Aufspaltung“
description: Erfahren Sie, wie Sie die Aufspaltungsaktivität in einer orchestrierten Kampagne verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 53%

---

# Aufspaltung {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Aktivität „Aufspaltung“"
>abstract="Mit der Aktivität **Aufspaltung** können eingehende Populationen basierend auf unterschiedlichen Auswahlkriterien in mehrere Teilmengen segmentiert werden, z. B. Filterregeln oder Populationsgröße."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Orchestrierte Kampagnenaktivitäten |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Orchestrierte Kampagne erstellen](../create-orchestrated-campaign.md)<br/><br/>[Aktivitäten orchestrieren](../orchestrate-activities.md)<br/><br/>[ Nachrichten mit orchestrierten Kampagnen senden](../send-messages.md)<br/><br/>[Kampagne starten und überwachen](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-rule-builder.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimensionsänderung](change-dimension.md) - [Kombinieren](combine.md) - [Deduplizierung](enrichment.md) - [Verzweigung](fork.md) - [Abstimmung](reconciliation.md) - [Aufspaltung](split.md)[ ](wait.md) Warten](deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

Die **Aufspaltung**-Aktivität ist eine **Targeting**-Aktivität, die die eingehende Population basierend auf definierten Auswahlkriterien wie Filterregeln oder der Populationsgröße in mehrere Teilmengen unterteilt.

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

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >Die **Aufspaltung** verarbeitet Teilmengen in der Reihenfolge, in der sie hinzugefügt werden. Wenn beispielsweise die erste Teilmenge 70 % der Population erfasst, wendet die nächste Teilmenge ihre Kriterien auf die verbleibenden 30 % an.
   >
   >Stellen Sie vor der Ausführung der orchestrierten Kampagne sicher, dass die Teilmengen wie vorgesehen sortiert sind. Verwenden Sie die Pfeiltasten, um ihre Position anzupassen.

1. Sobald die Teilmengen hinzugefügt wurden, zeigt die Aktivität für jede Teilmenge eine ausgehende Transition. Es wird dringend empfohlen, den Titel jeder Teilmenge zu ändern, um sie auf der koordinierten Kampagnen-Arbeitsfläche leicht identifizieren zu können.

1. Konfigurieren Sie Filter für jede Teilmenge:

   1. Klicken Sie auf eine Teilmenge, um deren Einstellungen zu öffnen.

   1. Klicken Sie **[!UICONTROL Filter erstellen]**, um Filterregeln mithilfe des Abfrage-Modellierers zu definieren, z. B. Profile mit einer gültigen E-Mail-Adresse.

      ![](../assets/orchestrated-split-1.png)

   1. Um die Anzahl der ausgewählten Profile zu begrenzen, aktivieren Sie **[!UICONTROL Limit aktivieren]** und geben Sie eine Zahl oder einen Prozentsatz an.

   1. Um eine Transition zu überspringen, wenn die Teilmenge leer ist, aktivieren Sie **[!UICONTROL Leere Transition überspringen].**

1. Um Profile einzuschließen, denen keine Teilmenge zugeordnet ist, aktivieren Sie **[!UICONTROL Komplement erzeugen]**. Dadurch wird eine zusätzliche ausgehende Transition für die verbleibende Population erstellt.

   >[!NOTE]
   >
   >Aktivieren Sie **[!UICONTROL Alle Teilmengen in derselben Tabelle generieren]** um alle Teilmengen in einer Transition zu gruppieren.

1. Verwenden Sie **[!UICONTROL Überlappung der Ausgabepopulationen aktivieren]** damit Profile in mehreren Teilmengen angezeigt werden:

   * **Wenn diese Option** ist, wird jedes Profil nur einer Teilmenge zugewiesen, der ersten, deren Kriterien übereinstimmen, selbst wenn es für andere Teilmengen qualifiziert ist.

   * **Wenn diese Option** ist, können Profile in mehrere Teilmengen aufgenommen werden, wenn sie die jeweiligen Kriterien erfüllen.

Der Aktivität ist jetzt konfiguriert. Bei der orchestrierten Kampagnenausführung wird die Population in der Reihenfolge, in der sie der Aktivität hinzugefügt wurden, in die verschiedenen Untergruppen segmentiert.

## Beispiel{#split-example}

Im folgenden Beispiel wird die Aktivität **[!UICONTROL Aufspaltung]** verwendet, um eine Zielgruppe basierend auf dem Kommunikationskanal, den wir verwenden möchten, in verschiedene Teilmengen zu unterteilen:

* **Untergruppe 1 „E-Mail**: enthält Profile, die eine Telefonnummer angegeben haben.

* **Teilmenge 2 „sms“**: Targeting von Profilen mit einer in der Datenbank gespeicherten Mobiltelefonnummer.

* **Transition ergänzen**: Erfasst alle verbleibenden Profile, die die Kriterien für keine der Teilmengen erfüllen.

![](../assets/orchestrated-split-3.png)
