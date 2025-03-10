---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Erfahren Sie, wie Sie die Aktivität Verzweigung in einer mehrstufigen Kampagne verwenden
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 67%

---

# Zielgruppe speichern {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Verwenden Sie diese Aktivität, um eine vorhandene Audience zu aktualisieren oder eine neue Audience aus der Population zu erstellen, die im Vorfeld in der mehrstufigen Kampagne berechnet wurde. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Ausgehende Transition generieren"
>abstract="Verwenden Sie diese Option, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten."

Die Aktivität **Zielgruppe speichern** ist eine Aktivität zur **Zielgruppenbestimmung**. Mit dieser Aktivität können Sie eine vorhandene Audience aktualisieren oder eine neue Audience aus der Population erstellen, die im Vorfeld in einer mehrstufigen Kampagne berechnet wurde. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste in Adobe Campaign hinzugefügt und sind über das Menü **Zielgruppen** zugänglich.

Diese Aktivität wird im Wesentlichen verwendet, um innerhalb einer mehrstufigen Kampagne berechnete Populationen in wiederverwendbare Audiences umzuwandeln. Verbinden Sie sie mit anderen Zielgruppenbestimmungsaktivitäten, wie etwa den Aktivitäten **Zielgruppe aufbauen** oder **Kombinieren**.

## Konfigurieren der Aktivität „Zielgruppe speichern“{#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

![](../assets/workflow-save-audience.png)

1. Fügen Sie **mehrstufigen Kampagne** Aktivität „Zielgruppe speichern“ hinzu.

1. Wählen Sie im Dropdown-Menü **Modus** die Aktion aus, die Sie ausführen möchten:

   * **Erstellen oder Aktualisieren einer vorhandenen Zielgruppe**: Definieren Sie eine **Zielgruppenbezeichnung**. Wenn die Zielgruppe bereits existiert, wird sie aktualisiert, andernfalls wird eine neue Zielgruppe erstellt.

   * **Vorhandene Zielgruppe aktualisieren**: Wählen Sie die **Zielgruppe**, die Sie aktualisieren möchten, in der Liste der vorhandenen Zielgruppen aus.

1. Wählen Sie den **Aktualisierungsmodus** aus, der für vorhandene Zielgruppen gelten soll:

   * **Zielgruppeninhalt durch neue Daten ersetzen**: Der gesamte Inhalt der Zielgruppe wird ersetzt. Die zuvor enthaltenen Daten gehen dabei verloren. Nur die in der eingehenden Transition der Aktivität „Zielgruppe speichern“ übermittelten Daten werden beibehalten. Bei dieser Option werden Zielgruppendimension und -typ der aktualisierten Zielgruppe gelöscht.

   * **Zielgruppeninhalt mit den neuen Daten ergänzen**: Der alte Zielgruppeninhalt wird beibehalten und die Daten der eingehenden Transition der Aktivität „Zielgruppe speichern“ wird hinzugefügt.

1. Markieren Sie die Option **Ausgehende Transition erzeugen**, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten.

Der Inhalt der gespeicherten Zielgruppe ist anschließend in der Detailansicht der Zielgruppe verfügbar, auf die Sie im Menü **Zielgruppen** zugreifen können. Die in dieser Ansicht verfügbaren Spalten entsprechen den Spalten der eingehenden Transition der mehrstufigen Kampagne der Aktivität **Zielgruppe speichern**.


## Beispiel{#save-audience-example}

Im folgenden Beispiel wird eine einfache Zielgruppenaktualisierung von der Zielgruppenbestimmung aus gezeigt. Es wird ein Planer hinzugefügt, um die mehrstufige Kampagne einmal monatlich auszuführen. Eine Abfrage ruft alle Profile ab, die für die verschiedenen verfügbaren Anwendungen angemeldet sind. Die Aktivität **Zielgruppe speichern** aktualisiert die Zielgruppe, indem sie Profile löscht, die sich seit der letzten mehrstufigen Kampagnenausführung vom Service abgemeldet haben, und indem sie die neu abonnierten Profile hinzufügt.
