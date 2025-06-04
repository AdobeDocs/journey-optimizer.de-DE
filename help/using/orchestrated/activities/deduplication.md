---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Deduplizierung“
description: Erfahren Sie, wie Sie die Aktivität „Deduplizierung“ verwenden.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 01fbf78d15e620fa7b540e3a1a6972949a0c4795
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 48%

---

# Deduplizierung {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Felder zum Identifizieren von Dubletten"
>abstract="Klicken Sie im Abschnitt **Felder zum Identifizieren von Dubletten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Dubletten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Aktivität „Deduplizierung“"
>abstract="Mithilfe der Aktivität **Deduplizierung** lassen sich Dubletten in Ergebnissen aus eingehenden Aktivitäten löschen. Sie wird hauptsächlich im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendaten zulassen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Erzeugen eines Komplements"
>abstract="Sie können eine zusätzliche ausgehende Transition mit der verbleibenden Population generieren, die als Duplikat ausgeschlossen wurde. Schalten Sie dazu die Option **Komplement erzeugen** ein"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Deduplizierungseinstellungen"
>abstract="Um Dubletten in den eingehenden Daten zu löschen, definieren Sie die Deduplizierungsmethode in den folgenden Feldern. Standardmäßig wird nur ein Eintrag beibehalten. Sie sollten außerdem die Deduplizierungsmethode anhand eines Ausdrucks oder Attributs auswählen. Standardmäßig wird der Eintrag, der von den Duplikaten ausgenommen sein soll, zufällig ausgewählt."

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Orchestrierte Kampagnenaktivitäten |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](../gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](../configuration-steps.md)<br/><br/>[Schlüsselschritte für die orchestrierte Kampagnenerstellung](../gs-campaign-creation.md) | [Orchestrierte Kampagne erstellen](../create-orchestrated-campaign.md)<br/><br/>[Aktivitäten orchestrieren](../orchestrate-activities.md)<br/><br/>[ Nachrichten mit orchestrierten Kampagnen senden](../send-messages.md)<br/><br/>[Kampagne starten und überwachen](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Arbeiten mit der Abfrage Modeler](../orchestrated-query-modeler.md)<br/><br/>[Erstellen Sie Ihre ersten ](../build-query.md)<br/><br/>[-Bearbeitungsausdrücke](../edit-expressions.md) | [Erste Schritte mit Aktivitäten](about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](and-join.md) - [Zielgruppe aufbauen](build-audience.md) - [Dimensionsänderung](change-dimension.md) - [Kombinieren](combine.md) - [Deduplizierung](enrichment.md) - [Verzweigung](fork.md) - [Abstimmung](reconciliation.md) - [Aufspaltung](split.md)[ ](wait.md) Warten](deduplication.md) [ |

{style="table-layout:fixed"}

+++

<br/>

Die **Deduplizierungsaktivität** ist eine **Zielgruppenbestimmungsaktivität**. Mithilfe dieser Aktivität lassen sich Dubletten in Ergebnissen aus eingehenden Aktivitäten löschen, z. B. duplizierte Profile aus der Empfängerliste. Die **Deduplizierungsaktivität** wird im Allgemeinen im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendatum zulassen.

## Konfigurieren der Deduplizierungsaktivität{#deduplication-configuration}

Gehen Sie folgendermaßen vor, um die **Deduplizierungsaktivität** zu konfigurieren:


1. Fügen Sie **orchestrierten Kampagne** Aktivität „Deduplizierung“ hinzu.

1. Klicken Sie im Abschnitt **Felder zum Identifizieren von Dubletten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Dubletten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen.

![](../assets/deduplication-1.png)

1. Wählen Sie **Abschnitt** Deduplizierungseinstellungen“ aus, wie viele eindeutige Datensätze beibehalten werden sollen, indem Sie das Feld Beizubehaltende Duplikate verwenden. Der Standardwert ist 1, wobei ein Datensatz pro doppelter Gruppe beibehalten wird. Legen Sie ihn auf 0 fest, um alle Duplikate zu behalten.

   Wenn beispielsweise Datensatz A und B Duplikate von Y sind und Datensatz C ein Duplikat von Z ist:

   * **Wenn der Wert des Felds 1 ist** werden nur die Y- und Z-Datensätze beibehalten.
   * **Wenn der Wert des Felds 0 ist**: Alle Datensätze (A, B, C, Y, Z) werden beibehalten.
   * **Wenn der Wert des Felds 2 ist**: C und Z werden beibehalten, plus zwei Werte von A, B und Y, zufällig oder basierend auf Ihrer Deduplizierungsmethode.

1. Wählen Sie eine **Deduplizierungsmethode**, die definiert, wie das System entscheidet, welche Datensätze aus jeder Gruppe von Duplikaten beibehalten werden sollen:

   * **Zufällige Auswahl**: Wählt nach dem Zufallsprinzip unter den Dubletten den Eintrag aus, der beibehalten werden soll.
   * **Ausdruck verwenden**: Behält Datensätze mit dem höchsten oder niedrigsten Wert basierend auf einem von Ihnen definierten Ausdruck bei.
   * **Nicht leere Werte**: Speichert Datensätze, bei denen das ausgewählte Feld nicht leer ist, z. B. nur Profile mit einer Telefonnummer.
   * **Nach einer Werteliste**: Ermöglicht die Priorisierung bestimmter Werte für ein oder mehrere Felder, z. B. kann Datensätzen mit „Land“ Priorität eingeräumt werden, für die Frankreich festgelegt ist. Klicken Sie auf **Attribut**, um ein Feld auszuwählen oder einen benutzerdefinierten Ausdruck zu erstellen. Verwenden Sie die **Hinzufügen**, um bevorzugte Werte in der Prioritätsreihenfolge einzugeben.

   ![](../assets/deduplication-2.png)

1. Aktivieren Sie die Option **Komplement erzeugen**, wenn Sie die verbleibende Population verwenden möchten. Das Komplement besteht aus allen Duplikaten. Der Aktivität wird dann eine zusätzliche Transition hinzugefügt.

## Beispiel{#deduplication-example}

Im folgenden Beispiel wird eine Aktivität **Deduplizierung** verwendet, um doppelte Datensätze aus der Zielgruppe zu entfernen, bevor ein Versand durchgeführt wird. Die Zielgruppe wird zunächst so gefiltert, dass nur Profile mit einem nicht leeren E-Mail-Feld einbezogen werden. Anschließend verwendet die Aktivität **Deduplizierung** die E-Mail-Adresse, um Duplikate zu identifizieren und auszuschließen.

![](../assets/deduplication-3.png)
