---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen der Zielgruppendimension
description: Erfahren Sie, wie Sie dem Kundenprofil ein relationales Schema zuordnen.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 9%

---

# Konfigurieren einer Zielgruppendimension {#configuration}

+++ Inhaltsverzeichnis

| Willkommen bei orchestrierten Kampagnen | Starten der ersten orchestrierten Kampagne | Abfragen der Datenbank | Aktivitäten für orchestrierte Kampagnen |
|---|---|---|---|
| [Erste Schritte mit orchestrierten Kampagnen](gs-orchestrated-campaigns.md)<br/><br/>Erstellen und Verwalten von relationalen Schemata und Datensätzen:</br> <ul><li>[Erste Schritte mit Schemata und Datensätzen](gs-schemas.md)</li><li>[Manuelles Schema](manual-schema.md)</li><li>[Datei-Upload-Schema](file-upload-schema.md)</li><li>[Daten aufnehmen](ingest-data.md)</li></ul>[Zugriff und Verwaltung orchestrierter Kampagnen](access-manage-orchestrated-campaigns.md)<br/><br/>[Die wichtigsten Schritte zum Erstellen einer orchestrierten Kampagne](gs-campaign-creation.md)<br/><br/>[Konfigurieren einer Zielgruppendimension](target-dimension.md) | <b>[Erstellen und Planen der Kampagne](create-orchestrated-campaign.md)</b><br/><br/>[Orchestrieren von Aktivitäten](orchestrate-activities.md)<br/><br/>[Starten und Überwachen der Kampagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Arbeiten mit dem Regel-Builder](orchestrated-rule-builder.md)<br/><br/>[Erstellen der ersten Abfrage](build-query.md)<br/><br/>[Bearbeiten von Ausdrücken](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Erste Schritte mit Aktivitäten](activities/about-activities.md)<br/><br/>Aktivitäten:<br/>[Und-Verknüpfung](activities/and-join.md) – [Zielgruppe erstellen](activities/build-audience.md) – [Dimensionsänderung](activities/change-dimension.md) – [Kanalaktivitäten](activities/channels.md) – [Kombinieren](activities/combine.md) – [Deduplizierung](activities/deduplication.md) – [Anreicherung](activities/enrichment.md) – [Verzweigung](activities/fork.md) – [Abstimmung](activities/reconciliation.md) – [Zielgruppe speichern](activities/save-audience.md) – [Aufspaltung](activities/split.md) – [Warten](activities/wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

Der Inhalt dieser Seite ist nicht endgültig und kann geändert werden.

>[!ENDSHADEBOX]

In vielen Fällen kann ein einzelnes Kundenprofil mit mehreren verwandten Entitäten verknüpft werden, z. B. Abonnements, Service-Verträgen oder Geräten, die jeweils eine eigene eindeutige Kennung und Kommunikationsanforderungen aufweisen.

Mit **Orchestrierten Kampagnen** können Sie jetzt mithilfe der relationalen Schemafunktionen von **Adobe Experience Platform zielgerichtete Kommunikationen auf Entitätsebene entwerfen und**. Auf diese Weise können Sie Segmente segmentieren, personalisieren und Berichte für jede Entität und nicht für jeden Empfänger erstellen.

## Erstellen der Zielgruppendimension {#targeting-dimension}

Ein einzelnes Kundenprofil kann mit mehreren verwandten Entitäten verknüpft werden, z. B. Verträgen, Geräten oder Abonnements, wobei jede eine eigene eindeutige Kennung hat. Diese Einrichtung ermöglicht es, jede Entität einzeln anzusprechen, zu segmentieren und Berichte dazu zu erstellen.

Richten Sie zunächst die Kampagnenorchestrierung ein, indem Sie dem Kundenprofil ein relationales Schema zuordnen.

1. Rufen Sie **[!UICONTROL Administration]** das Menü **[!UICONTROL Konfigurationen]** auf und wählen Sie **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Klicken Sie **[!UICONTROL Erstellen]**, um mit der Erstellung Ihrer **[!UICONTROL Zielgruppendimension]** zu beginnen.

1. Wählen Sie Ihr [zuvor konfiguriertes Schema](gs-schemas.md) aus &#x200B; Dropdown-Liste aus.

1. Wählen Sie den **[!UICONTROL Identitätswert]** für die Entität aus, die Sie ansprechen möchten.

   In diesem Beispiel ist das Kundenprofil mit mehreren Abonnements verknüpft, die jeweils durch eine eindeutige `crmID` im `Recipient` dargestellt werden. Wenn Sie die **[!UICONTROL Target Dimension]** auf die Verwendung des `Recipient` Schemas und dessen `crmID` festlegen, können Sie Nachrichten auf Abonnementebene und nicht an das Hauptkundenprofil senden, um sicherzustellen, dass jeder Vertrag oder jede Zeile eine eigene personalisierte Nachricht erhält.

   [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Klicken Sie **[!UICONTROL Speichern]**, um die Einrichtung abzuschließen.

Fahren Sie nach der Konfiguration **[!UICONTROL Target-Dimension]** mit der Erstellung und Einrichtung Ihrer **[!UICONTROL Kanalkonfiguration]** fort und definieren Sie die entsprechenden **[!UICONTROL Ausführungsdetails]**.

## Konfigurieren der Kanalkonfiguration {#channel-configuration}

Nach der Einrichtung Ihrer **[!UICONTROL Target Dimension]** müssen Sie Ihre E-Mail- oder SMS-**[!UICONTROL Kanalkonfiguration]** konfigurieren und die entsprechenden **[!UICONTROL Ausführungsdetails]** definieren. Dadurch wird sichergestellt, dass Nachrichten mit der richtigen Identitäts- und Zielgruppenbestimmungslogik gesendet werden.

1. Erstellen und konfigurieren Sie zunächst Ihre **[!UICONTROL Kanalkonfiguration]**.

   Sie können auch eine vorhandene **[!UICONTROL Kanalkonfiguration“]**.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus](../email/surface-personalization.md)

1. Rufen Sie im **[!UICONTROL Ausführungsdetails]** Ihrer **[!UICONTROL Kanalkonfiguration]** die Registerkarte **[!UICONTROL Orchestrierte Kampagnen]** auf.

   ![](assets/target-dimension-3.png)

1. Klicken Sie auf **[!UICONTROL Aktiviert]**, um sie mit orchestrierten Kampagnen kompatibel zu machen.

1. Wählen Sie Ihre Versandmethode:

   * **[!UICONTROL Target Dimension]**: An die primäre Entität, z. B. den Empfänger, senden.

   * **[!UICONTROL Target + Sekundäre Dimension]**: Senden Sie Daten sowohl über primäre als auch sekundäre Entitäten, z. B. Empfänger + Vertrag.

1. Wählen Sie aus der Dropdown-Liste Ihre [zuvor erstellte Target-Dimension](#targeting-dimension) aus.

   ![](assets/target-dimension-4.png)

1. Wählen Sie **[!UICONTROL Abschnitt]** Ausführungsadresse) aus, welche **[!UICONTROL Source]** zum Abrufen der Versandadresse verwendet werden soll, z. B. die E-Mail-Adresse oder Telefonnummer:

   * **[!UICONTROL Profil]**: Wählen Sie diese Option aus, wenn die Versandadresse, z. B. die E-Mail, direkt im Hauptkundenprofil gespeichert wird.

     Nützlich beim Senden von Nachrichten an den Hauptkunden, nicht an eine bestimmte zugehörige Entität.

   * **[!UICONTROL Target Dimension]**: Wählen Sie diese Option, wenn die Versandadresse in der entsprechenden Entität (z. B. einem Empfänger oder einem Abonnement) gespeichert ist.

     Dies ist nützlich, wenn jeder Empfänger eine eigene Versandadresse hat, z. B. eine andere E-Mail-Adresse oder Telefonnummer.

1. Klicken Sie im Feld **[!UICONTROL Versandadresse]** auf ![Bearbeiten](assets/do-not-localize/edit.svg), um das spezifische Feld auszuwählen, das für Ihren Nachrichtenversand verwendet werden soll.

   ![](assets/target-dimension-4.png)

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Senden]**.

Ihr Kanal kann jetzt mit &quot;**Kampagnen“ verwendet** und Nachrichten werden entsprechend der ausgewählten Zielgruppendimension zugestellt.
