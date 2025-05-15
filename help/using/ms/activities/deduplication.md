---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Deduplizierung“
description: Erfahren Sie, wie Sie die Aktivität „Deduplizierung“ verwenden.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 98%

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

Die **Deduplizierungsaktivität** ist eine **Zielgruppenbestimmungsaktivität**. Mithilfe dieser Aktivität lassen sich Dubletten in Ergebnissen aus eingehenden Aktivitäten löschen, z. B. duplizierte Profile aus der Empfängerliste. Die **Deduplizierungsaktivität** wird im Allgemeinen im Anschluss an Zielgruppenbestimmungsaktivitäten und vor Aktivitäten verwendet, die die Verwendung von Zielgruppendatum zulassen.

## Konfigurieren der Deduplizierungsaktivität{#deduplication-configuration}

Gehen Sie folgendermaßen vor, um die **Deduplizierungsaktivität** zu konfigurieren:

![](../assets/workflow-deduplication.png)

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Deduplizierung“ hinzu.

1. Klicken Sie im Abschnitt **Felder zum Identifizieren von Dubletten** auf die Schaltfläche **Attribut hinzufügen**, um die Felder anzugeben, für die die Identifizierung von Dubletten aufgrund identischer Werte möglich ist, wie z. B. E-Mail-Adresse, Vorname, Nachname usw. Durch die Reihenfolge der Felder können Sie angeben, welche Felder zuerst verarbeitet werden sollen.

1. Wählen Sie im Abschnitt **Deduplizierungseinstellungen** die Anzahl der eindeutigen **beizubehaltenden Dubletten** aus. Der Standardwert dieses Felds ist 1. Mittels des Werts 0 lassen sich alle Dubletten beibehalten.

   Nehmen wir z. B. den Fall, dass die Datensätze A und B wie Duplikate des Datensatzes Y und ein Datensatz C wie ein Duplikat des Datensatzes Z angesehen werden:

   * Wenn der Wert des Felds 1 ist: nur die Datensätze Y und Z werden beibehalten.
   * Wenn der Wert des Felds 0 ist: alle Datensätze werden beibehalten.
   * Wenn der Wert des Felds 2 ist: Die Datensätze C und Z werden beibehalten und von den Datensätzen A, B und Y werden zwei entweder nach dem Zufallsprinzip oder in Abhängigkeit von der im Anschluss ausgewählten Deduplizierungsmethode beibehalten.

1. Wählen Sie die **Deduplizierungsmethode** aus, die verwendet werden soll:

   * **Zufällige Auswahl**: Wählt nach dem Zufallsprinzip unter den Dubletten den Eintrag aus, der beibehalten werden soll.
   * **Von einem Ausdruck ausgehend**: Behält Einträge bei, für die der angegebene Ausdruck den kleinsten oder größten Wert aufweist.
   * **Wert nicht leer**: Behält Einträge bei, für die der Ausdruck nicht leer ist.
   * **Gemäß einer Werteliste**: Definiert eine Priorität nach Wert für ein oder mehrere Felder. Klicken Sie zur Bestimmung dieser Werte auf **Attribute**, um ein Feld auszuwählen, oder erstellen Sie einen Ausdruck und fügen Sie dann den oder die Werte der entsprechenden Tabelle hinzu. Verwenden Sie zum Definieren eines neues Felds die Schaltfläche **Hinzufügen** oberhalb der Werteliste.

1. Aktivieren Sie die Option **Komplement erzeugen**, wenn Sie die verbleibende Population verwenden möchten. Das Komplement besteht aus allen Duplikaten. Der Aktivität wird dann eine zusätzliche Transition hinzugefügt.

## Beispiel{#deduplication-example}

Verwenden Sie im folgenden Beispiel eine Deduplizierungsaktivität, um vor dem Versand Dubletten aus der Zielgruppe auszuschließen. Die identifizierten duplizierten Profile werden einer dedizierten Zielgruppe hinzugefügt, die bei Bedarf wiederverwendet werden kann. Wählen Sie die **E-Mail-Adresse** zur Identifizierung der Dubletten. Behalten Sie einen Eintrag bei und wählen Sie die Deduplizierungsmethode **Zufällig** aus.

![](../assets/workflow-deduplication-example.png)
