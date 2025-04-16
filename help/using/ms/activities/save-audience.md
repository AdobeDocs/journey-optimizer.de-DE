---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe speichern“
description: Erfahren Sie, wie Sie die Aktivität Verzweigung in einer koordinierten Kampagne verwenden
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 67%

---

# Zielgruppe speichern {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Speichern einer Zielgruppe"
>abstract="Use this activity to update an existing audience or create a new audience from the population computed upstream in the orchestrated campaign. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste hinzugefügt und sind über das Menü **Zielgruppen** zugänglich."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Ausgehende Transition generieren"
>abstract="Verwenden Sie diese Option, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten."

Die Aktivität **Zielgruppe speichern** ist eine Aktivität zur **Zielgruppenbestimmung**. This activity allows you to update an existing audience or create a new audience from the population computed upstream in an orchestrated campaign. Die Zielgruppen werden zur bereits bestehenden Zielgruppenliste in Adobe Campaign hinzugefügt und sind über das Menü **Zielgruppen** zugänglich.

This activity is essentially used to keep population groups computed in the same orchestrated campaign, by converting them into reusable audiences. Verbinden Sie sie mit anderen Zielgruppenbestimmungsaktivitäten, wie etwa den Aktivitäten **Zielgruppe aufbauen** oder **Kombinieren**.

## Konfigurieren der Aktivität „Zielgruppe speichern“{#save-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Zielgruppe aufbauen** zu konfigurieren:

![](../assets/workflow-save-audience.png)

1. Add a **Save audience** activity to your orchestrated campaign.

1. Wählen Sie im Dropdown-Menü **Modus** die Aktion aus, die Sie ausführen möchten:

   * **Erstellen oder Aktualisieren einer vorhandenen Zielgruppe**: Definieren Sie eine **Zielgruppenbezeichnung**. Wenn die Zielgruppe bereits existiert, wird sie aktualisiert, andernfalls wird eine neue Zielgruppe erstellt.

   * **Vorhandene Zielgruppe aktualisieren**: Wählen Sie die **Zielgruppe**, die Sie aktualisieren möchten, in der Liste der vorhandenen Zielgruppen aus.

1. Wählen Sie den **Aktualisierungsmodus** aus, der für vorhandene Zielgruppen gelten soll:

   * **Zielgruppeninhalt durch neue Daten ersetzen**: Der gesamte Inhalt der Zielgruppe wird ersetzt. Die zuvor enthaltenen Daten gehen dabei verloren. Nur die in der eingehenden Transition der Aktivität „Zielgruppe speichern“ übermittelten Daten werden beibehalten. Bei dieser Option werden Zielgruppendimension und -typ der aktualisierten Zielgruppe gelöscht.

   * **Zielgruppeninhalt mit den neuen Daten ergänzen**: Der alte Zielgruppeninhalt wird beibehalten und die Daten der eingehenden Transition der Aktivität „Zielgruppe speichern“ wird hinzugefügt.

1. Markieren Sie die Option **Ausgehende Transition erzeugen**, wenn Sie eine Transition nach der Aktivität **Zielgruppe speichern** hinzufügen möchten.

Der Inhalt der gespeicherten Zielgruppe ist anschließend in der Detailansicht der Zielgruppe verfügbar, auf die Sie im Menü **Zielgruppen** zugreifen können. The columns available from this view correspond to the columns of the inbound transition of the orchestrated campaign&#39;s **Save audience** activity.


## Beispiel{#save-audience-example}

Im folgenden Beispiel wird eine einfache Zielgruppenaktualisierung von der Zielgruppenbestimmung aus gezeigt. A scheduler is added to run the orchestrated campaign once a month. Eine Abfrage ruft alle Profile ab, die für die verschiedenen verfügbaren Anwendungen angemeldet sind. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last orchestrated campaign execution and by adding the newly subscribed profiles.
