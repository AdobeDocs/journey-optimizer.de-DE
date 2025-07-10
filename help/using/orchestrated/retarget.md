---
solution: Journey Optimizer
product: journey optimizer
title: Starten und Überwachen orchestrierter Kampagnen mit Adobe Journey Optimizer
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer orchestrierte Kampagnen starten und überwachen.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# Erstellen von Retargeting-Abfragen {#retarget}

+++ Inhaltsverzeichnis

| Willkommen bei koordinierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>[Konfigurationsschritte](configuration-steps.md)<br/><br/>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Wichtige Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[ Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Ausdrücke bearbeiten](edit-expressions.md)<br/><br/><b>[Retargeting](retarget.md)</b> | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) - [Zielgruppe aufbauen](activities/build-audience.md) - [Dimension ändern](activities/change-dimension.md) - [Kanalaktivitäten](activities/channels.md) - [Kombinieren](activities/combine.md) - [Anreicherung](activities/deduplication.md) - [Formulare](activities/enrichment.md) - [Abstimmung](activities/fork.md) [&#128279;](activities/reconciliation.md) [&#128279;](activities/save-audience.md) [&#128279;](activities/split.md) ->Zielgruppe speichern[ -AufspaltungWarten](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Dokumentation in Bearbeitung

>[!ENDSHADEBOX]

Beim Retargeting können Sie die Empfängerinnen und Empfänger darauf ansprechen, wie sie auf eine frühere orchestrierte Kampagne reagiert haben. Sie können beispielsweise eine zweite E-Mail an Profile senden, die die erste erhalten, aber nicht darauf geklickt haben.

Eine orchestrierte Kampagne bietet hierfür zwei Hauptdatenquellen:

- **Nachrichten-Feedback**: Erfasst Ereignisse im Zusammenhang mit dem Versand, z. B. gesendete, geöffnete, zurückgesendete Nachricht usw.

- **E-Mail-Tracking**: Erfasst Benutzeraktionen wie Klicks und Öffnungen.

## Erstellen einer Feedback-basierten Retargeting-Regel

Feedback-basierte Retargeting-Regel ermöglicht die erneute Zielgruppenbestimmung von Empfängern auf der Grundlage von Nachrichtenversand-Ereignissen, die im Datensatz **Nachrichten-Feedback** erfasst wurden. Zu diesen Ereignissen gehören Ergebnisse wie Nachrichten, die gesendet, geöffnet, zurückgewiesen oder als Spam gekennzeichnet werden.

Mithilfe dieser Daten können Sie Regeln definieren, um Empfänger zu identifizieren, die eine frühere Nachricht erhalten, aber nicht damit interagiert haben, was eine Folgekommunikation basierend auf bestimmten Versandstatus ermöglicht.

1. Erstellen Sie eine neue **Orchestrierte Kampagne**.

2. Fügen Sie die Aktivität **Zielgruppe aufbauen** hinzu und legen Sie für die Zielgruppendimension **Empfänger (caas)** fest.

3. Klicken Sie **Regel-Builder** auf **Bedingung hinzufügen** und wählen Sie **Nachrichten-Feedback** aus der Attributauswahl aus. Klicken Sie auf **Bestätigen**.

4. Fügen Sie eine Bedingung für **Feedback-Status** hinzu und setzen Sie den Wert auf **Nachricht gesendet**.

5. So wählen Sie eine bestimmte orchestrierte Kampagne aus:

   - Fügen Sie eine weitere Bedingung hinzu, suchen Sie nach `entity` und navigieren Sie zu:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Wählen Sie **Orchestrierter Kampagnenname** und geben Sie den Kampagnennamen an.

6. So wählen Sie eine bestimmte Nachricht oder Aktivität innerhalb dieser orchestrierten Kampagne aus:

   - Fügen Sie eine weitere Bedingung hinzu, suchen Sie nach `entity` und navigieren Sie zu:\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Wählen Sie **Orchestrierte Kampagnenaktion - Name** und geben Sie den Namen der Kampagnenaktion an.

     Aktionsnamen finden Sie, indem Sie auf das ![Informationssymbol](assets/do-not-localize/info-icon.svg) neben einer Aktivität auf der Arbeitsfläche klicken.

   >[!TIP]
   >
   >Anstatt Namen zu verwenden, können Sie auch nach der **Kampagnen-ID** (UUID) filtern, die Sie in Ihren Kampagneneigenschaften finden.

## Erstellen einer Tracking-basierten Retargeting-Regel

Die Tracking-basierte Retargeting-Regel richtet sich anhand der Daten aus dem Datensatz **E-Mail-Tracking** an Empfänger auf der Grundlage ihrer Interaktionen mit einer Nachricht. Es werden Benutzeraktionen wie E-Mail-Öffnungen und Link-Klicks erfasst.

Um Empfängerinnen und Empfänger auf der Grundlage von Nachrichteninteraktionen (z. B. Öffnen oder Klicken) erneut anzusprechen, verwenden Sie die Entität **E-Mail-Tracking** wie folgt:

1. Erstellen Sie eine neue **orchestrierte Kampagne** und fügen Sie dann eine Aktivität **Zielgruppe aufbauen** mit **Empfänger (caas)** als Zielgruppendimension hinzu, um sich auf die zuvor orchestrierten Kampagnenempfängerinnen und -empfänger zu konzentrieren.

1. Fügen Sie eine neue Bedingung für **E-Mail-Tracking** hinzu. Klicken Sie **Bestätigen**, um eine Bedingung wie „E-Mail-Tracking existiert“ zu erstellen.

1. Fügen Sie innerhalb dieser Bedingung eine Bedingung hinzu und suchen Sie nach **Interaktionstyp**-Attribut.

1. Verwenden Sie in den benutzerdefinierten Bedingungsoptionen **Enthalten in** als Operator und wählen Sie einen oder mehrere Werte je nach Anwendungsfall aus. Beispiel:
   - **Nachricht geöffnet**
   - **Link der Nachricht angeklickt**

1. So verknüpfen Sie die Tracking-Daten mit einer bestimmten Kampagne:

   - Fügen Sie eine Bedingung innerhalb des E-Mail-Tracking-Blocks hinzu.

   - Navigieren Sie zu `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Fügen Sie Bedingungen für sowohl **Name der koordinierten Kampagne** als auch bei Bedarf **Aktionsname der koordinierten Kampagne** hinzu.

     Aktionsnamen finden Sie, indem Sie auf das ![Informationssymbol](assets/do-not-localize/info-icon.svg) neben einer Aktivität auf der Arbeitsfläche klicken.

   >[!TIP]
   >
   >Anstatt Namen zu verwenden, können Sie auch nach der **Kampagnen-ID** (UUID) filtern, die Sie in Ihren Kampagneneigenschaften finden.
