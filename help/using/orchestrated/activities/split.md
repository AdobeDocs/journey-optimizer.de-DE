---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Aufspaltung“
description: Informationen zur Verwendung der Aktivität „Aufspaltung“ in einer orchestrierten Kampagne
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '801'
ht-degree: 100%

---


# Aufspaltung {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Aktivität „Aufspaltung“"
>abstract="Mit der Aktivität **Aufspaltung** können eingehende Populationen basierend auf unterschiedlichen Auswahlkriterien in mehrere Teilmengen segmentiert werden, z. B. Filterregeln oder Populationsgröße."

Die Aktivität **[!UICONTROL Aufspaltung]** ist eine **[!UICONTROL Targeting]**-Aktivität, mit der Sie die eingehende Population basierend auf definierten Auswahlkriterien in mehrere Teilmengen segmentieren können, z. B. basierend auf Filterregeln oder Populationsgröße.

## Konfigurieren der Aufspaltungsaktivität {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmente für die Aktivität „Aufspaltung“"
>abstract="Es können beliebig viele Teilmengen hinzugefügt werden, um die eingehende Population zu segmentieren.<br/></br>Bei Ausführung der Aktivität **Aufspaltung** wird die Population sukzessive in unterschiedliche Teilmengen segmentiert, und zwar in der Reihenfolge, in der diese zur Aktivität hinzugefügt werden. Vergewissern Sie sich vor dem Start Ihrer orchestrierten Kampagne, dass Sie die Teilmengen mithilfe der Pfeilschaltflächen in der für Sie passenden Reihenfolge angeordnet haben."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filter für die Aufspaltungsaktivität"
>abstract="Um eine Filterbedingung auf die Teilmenge anzuwenden, klicken Sie auf **[!UICONTROL Filter erstellen]** und konfigurieren Sie die gewünschte Filterregel mithilfe des Regel-Builders. Es können beispielsweise alle Profile aus der eingehenden Population eingeschlossen werden, deren E-Mail-Adresse in der Datenbank vorhanden ist."

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

Folgen Sie diesen Schritten, um die Aktivität **[!UICONTROL Aufspaltung]** zu konfigurieren:

1. Fügen Sie Ihrer orchestrierten Kampagne eine Aktivität des Typs **[!UICONTROL Aufspaltung]** hinzu.

1. Der Konfigurationsbereich für die Aktivität wird mit einer standardmäßigen Teilmenge geöffnet. Klicken Sie auf die Schaltfläche **[!UICONTROL Segment hinzufügen]**, um so viele Teilmengen wie gewünscht zum Segmentieren der eingehenden Population hinzuzufügen.

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >Die Aktivität **Aufspaltung** verarbeitet Teilmengen in der Reihenfolge, in der sie hinzugefügt werden. Wenn beispielsweise die erste Teilmenge 70 % der Population erfasst, wendet die nächste Teilmenge ihre Kriterien auf die verbleibenden 30 % an.
   >
   >Stellen Sie vor der Ausführung der orchestrierten Kampagne sicher, dass die Teilmengen wie vorgesehen sortiert sind. Verwenden Sie die Pfeiltasten, um ihre Position anzupassen.

1. Sobald die Teilmengen hinzugefügt wurden, zeigt die Aktivität für jede Teilmenge eine ausgehende Transition. Es wird dringend empfohlen, die Labels jeder Teilmenge zu ändern, um sie in der Arbeitsfläche der orchestrierten Kampagne leicht identifizieren zu können.

1. Konfigurieren Sie Filter für jede Teilmenge:

   1. Klicken Sie auf eine Teilmenge, um deren Einstellungen zu öffnen.

   1. Klicken Sie auf **[!UICONTROL Filter erstellen]**, um Filterregeln mithilfe des Abfrage-Modelers zu definieren, beispielsweise die Auswahl von Profilen mit einer gültigen E-Mail-Adresse.

      ![](../assets/orchestrated-split-1.png)

   1. Um die Anzahl der ausgewählten Profile zu begrenzen, aktivieren Sie **[!UICONTROL Grenzwert aktivieren]** und geben Sie eine Zahl oder einen Prozentsatz an.

   1. Um eine Transition zu überspringen, wenn die Teilmenge leer ist, aktivieren Sie **[!UICONTROL Leere Transition überspringen].**

1. Um Profile einzuschließen, die keiner Teilmenge entsprechen, aktivieren Sie **[!UICONTROL Komplement erzeugen]**. Dadurch wird eine zusätzliche ausgehende Transition für die verbleibende Population erstellt.

   >[!NOTE]
   >
   >Aktivieren Sie **[!UICONTROL Alle Teilmengen in derselben Tabelle erzeugen]**, um alle Teilmengen in einer einzelnen Transition zu gruppieren.

1. Verwenden Sie **[!UICONTROL Überschneidung der Ausgabepopulationen zulassen]** damit Profile in mehreren Teilmengen angezeigt werden können:

   * **Wenn diese Option deaktiviert ist**, wird jedes Profil nur der ersten Teilmenge zugewiesen, deren Kriterien es entspricht, selbst wenn es für andere Teilmengen qualifiziert ist.

   * **Wenn diese Option aktiviert ist**, können Profile in mehrere Teilmengen eingeschlossen werden, wenn sie die jeweiligen Kriterien erfüllen.

Der Aktivität ist jetzt konfiguriert. Bei der Ausführung orchestrierter Kampagnen wird die Population in die verschiedenen Teilmengen segmentiert, und zwar in der Reihenfolge, in der diese der Aktivität hinzugefügt wurden.

## Beispiel{#split-example}

Im folgenden Beispiel wird die Aktivität **[!UICONTROL Aufspaltung]** verwendet, um eine Zielgruppe basierend auf dem Kommunikationskanal, den wir verwenden möchten, in verschiedene Teilmengen zu unterteilen:

* **Teilmenge 1 „email“**: Schließt Profile ein, die eine Telefonnummer angegeben haben.

* **Teilmenge 2 „sms“**: Spricht Profile mit einer in der Datenbank gespeicherten Mobiltelefonnummer an.

* **Komplementtransition**: Erfasst alle verbleibenden Profile, die die Kriterien für keine der Teilmengen erfüllen.

![](../assets/orchestrated-split-3.png)
