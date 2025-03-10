---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität Daten-Update in mehrstufigen Kampagnen
description: Erfahren Sie, wie Sie die Aktivität „Daten-Update“ verwenden
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 85%

---

# Daten-Update {#update-data}

Die Aktivität **Daten-Update** ist eine **Daten-Management**-Aktivität. Sie ermöglicht eine gebündelte Aktualisierung der Datenbankfelder. Die Art der Datenbankaktualisierung kann über verschiedene Optionen definiert werden.

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## Konfigurieren der Aktivität „Daten-Update“{#update-data-configuration}

Um die Aktivität **Daten aktualisieren** zu konfigurieren, fügen Sie zunächst die Aktivität zu Ihrer mehrstufigen Kampagne hinzu und definieren Sie einen Titel.

![](../assets/workflow-update-data.png)

### Aktionstyp

Geben Sie im Feld **Aktionstyp** an, auf welche Weise die Daten aktualisiert werden sollen:

* **Einfügen oder aktualisieren**: Fügt neue Daten ein oder aktualisiert in der Datenbank existierende Einträge.
* **Einfügen**: Fügt lediglich neue Daten ein, existierende Datensätze werden nicht verändert. Wenn Abstimmkriterien definiert wurden, werden nur nicht abgestimmte Datensätze hinzugefügt.
* **Aktualisieren** – aktualisiert Daten existierender Datensätze, fügt keine neuen Datensätze hinzu.
* **Löschen** – löscht in der Datenbank existierende Daten.

Im Feld **Aktualisierungsgröße** wird bestimmt, wie viele Elemente der eingehenden Transition aktualisiert werden. Bei Angabe von 500 beispielsweise werden die 500 ersten Datensätze aktualisiert.

### Datensatz-Identifizierung

In diesem Abschnitt können Sie angeben, auf welche Weise die Einträge der Datenbank erkannt werden:

* Wenn die eingehenden Daten einer existierenden Zielgruppendimension entsprechen, wählen Sie die Option **Über die Zielgruppendimension** und dann die Zielgruppendimension im Feld **Zu aktualisierende Zielgruppendimension** aus.
* Sie können auch die Option **Verwendung von benutzerdefinierten Links** auswählen und einen oder mehrere Links angeben, was die Identifizierung der Daten in der Datenbank ermöglicht.
* Wenn eine Aktualisierung durchgeführt werden soll, ist die Verwendung der Option **Verwendung von Abstimmregeln** zwingend erforderlich.

### Zu aktualisierende Felder

Fügen Sie im Abschnitt **Zu aktualisierende Felder** die Felder hinzu, auf die die Aktualisierung angewendet werden soll, und geben Sie bei Bedarf Bedingungen für diese Aktualisierung an. Dies ist über das Feld **Berücksichtigt wenn** möglich. Die Bedingungen werden nacheinander, in Reihenfolge der Liste geprüft. Die Reihenfolge kann mithilfe der Pfeile rechts der Tabelle angepasst werden. Es ist möglich, mehrmals dasselbe Zielfeld zu verwenden.

Mithilfe der Schaltfläche **Automatische Zuordnung** können Sie die Felder automatisch zuordnen. Die Funktion des automatischen Verbindens erkennt Felder gleichen Namens.

Wenn Sie den Vorgang **Einfügen oder aktualisieren** ausgewählt haben, können Sie im Feld **Typ des Vorgangs** für jedes Feld individuell entscheiden, welche der möglichen Aktionen ausgeführt werden soll.

### Erweiterte Optionen

Über die **erweiterten Optionen** können weitere Optionen zur Aktualisierung von Daten und zum Umgang mit Dubletten definiert werden:

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

Mit diesen beiden letzten Optionen können Sie bestimmte Aktionen ausführen:

* **Ausgehende Transition erzeugen**: Erstellt eine ausgehende Transition, die am Ende der Ausführung aktiviert wird. Eine Aktualisierung signalisiert in der Regel das Ende einer mehrstufigen Targeting-Kampagne, weshalb die Option nicht standardmäßig aktiviert ist.

* **Ausgehende Transition für die Zurückweisungen erzeugen**: Erstellt eine ausgehende Transition mit Einträgen, die nach der Aktualisierung nicht korrekt verarbeitet wurden (z. B. wenn es eine Dublette gibt). Die Aktualisierung markiert im Allgemeinen das Ende einer mehrstufigen Targeting-Kampagne, weshalb die Option standardmäßig nicht aktiviert ist.
