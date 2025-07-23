---
solution: Journey Optimizer
product: journey optimizer
title: Reporting für orchestrierte Kampagnen mit Adobe Journey Optimizer
description: Informationen zum Zugriff auf Berichte über orchestrierte Kampagnen mit Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8cb569a2-a4a0-45a5-b7f9-f5a591e44335
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 82%

---

# Berichte über orchestrierte Kampagnen {#report-campaigns}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten Ihrer ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md) | [Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/><b>[Reporting](reporting-campaigns.md)<b> | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

Orchestrierte Kampagnen bieten Ihnen durch ihre zuverlässigen Reporting-Funktionen verwertbare Erkenntnisse. Diese Erkenntnisse helfen Ihnen, das Zielgruppenverhalten besser zu verstehen, die Leistung der einzelnen Schritte in Ihrer Customer Journey zu messen und datengestützte Entscheidungen zur Optimierung zukünftiger Kampagnen zu treffen. Mit detaillierten Metriken und Visualisierungen können Sie die Interaktion verfolgen und Ihre Targeting-Strategien so anpassen, dass sie maximale Wirkung erzielen.

![](assets/report-orchestrated.png)

## Berichtstypen {#reporting-types}

<table style="table-layout:auto; width: 100%; border-collapse: collapse;">
  <tbody>
    <tr>
      <td><a href="../reports/live-report.md"><img alt="Live-Bericht" src="assets/last-24hours.png"></a></td>
      <td>
        Verwenden Sie den <b>Live-Bericht</b>, um die Wirkung und Leistung Ihrer orchestrierten Kampagnen in Echtzeit in einem integrierten Dashboard zu messen und zu visualisieren. Die Daten sind im <b>Live-Bericht</b> verfügbar, sobald Ihre orchestrierte Kampagne im Menü <b>Bericht für letzte 24 Stunden anzeigen</b> ausgeführt wird. Weitere Informationen zu Live-Berichten sind in <a href="../reports/live-report.md">diesem Abschnitt</a> verfügbar.
      </td>
        </br>
    </tr>
    <tr style="background-color: #FFFFFF;">
      <td><a href="../reports/report-gs-cja.md"><img alt="Bericht für gesamte Zeit" src="assets/all-time-report.png"></a></td>
      <td>
        Der <b>Bericht für die gesamte Zeit</b> ist vollständig mit Customer Journey Analytics-Funktionen integriert, wodurch das Reporting plattformübergreifend standardisiert wird und Datenkonsistenz und -zuverlässigkeit verbessert werden. Weitere Informationen zu Berichten für die gesamte Zeit sind <a href="../reports/report-gs-cja.md">in diesem Abschnitt</a> verfügbar.
      </td>
    </tr>
  </tbody>
</table>

## Einblick in Kanalberichte

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../reports/campaign-global-report-cja-email.md"><img alt="email" src="../channels/assets/do-not-localize/email.png"></a><br/><a href="../reports/campaign-global-report-cja-email.md"><strong>E-Mail-Bericht</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-sms.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a><br/><a href="../reports/campaign-global-report-cja-sms.md"><strong>SMS-Bericht</strong></a></td>
<td><a href="../reports/campaign-global-report-cja-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a><a href="../reports/campaign-global-report-cja-push.md"><strong>Push-Bericht</strong></a></td>
</tr></table>

