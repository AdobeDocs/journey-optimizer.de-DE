---
title: Erste Schritte mit Datensätzen
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in Adobe Journey Optimizer verwenden.
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 1de18fa479a54c09751324a67793ce50e5657ce3
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 98%

---

# Erste Schritte mit Datensätzen {#datasets-gs}

Alle Daten, die in Adobe Experience Platform aufgenommen werden, bleiben als Datensätze im Data Lake erhalten. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet.

## Zugriff auf Datensätze{#access-datasets}

Der Arbeitsbereich **Datensätze** in der [!DNL Adobe Journey Optimizer]-Benutzeroberfläche ermöglicht es Ihnen, Daten zu durchsuchen und Datensätze zu erstellen.

Wählen Sie **Datensätze** im linken Navigationsbereich aus, um das Dashboard „Datensätze“ zu öffnen.

![](assets/datasets-home.png)

Das Hinzufügen von Daten zu [!DNL Adobe Experience Platform] bildet die Grundlage für die Erstellung eines Profils. Anschließend können Sie Profile in [!DNL Adobe Journey Optimizer] nutzen. Definieren Sie zunächst Schemas, verwenden Sie ETL-Tools, um Ihre Daten vorzubereiten und zu standardisieren, und erstellen Sie dann Datensätze basierend auf Ihren Schemas.

Wählen Sie die Registerkarte **Durchsuchen**, um die Liste aller für Ihr Unternehmen verfügbaren Datensätze anzuzeigen. Zu jedem aufgelisteten Datensatz werden Details angezeigt, einschließlich seines Namens, des Schemas, dem der Datensatz entspricht, und des Status des letzten Aufnahmelaufs.

Standardmäßig werden nur die Datensätze angezeigt, die Sie aufgenommen haben. Wenn Sie die systemgenerierten Datensätze anzeigen möchten, aktivieren Sie im Filter den Umschalter **Systemdatensätze zeigen**.

![](assets/ajo-system-datasets.png)

Wählen Sie den Namen eines Datensatzes aus, um auf seinen Datensatzaktivitäts-Bildschirm zuzugreifen und Details zum ausgewählten Datensatz anzuzeigen. Die Registerkarte „Aktivität“ enthält ein Diagramm, das die Rate der konsumierten Nachrichten sowie eine Liste erfolgreicher und fehlgeschlagener Batches visuell darstellt.

## Vorschau von Datensätzen{#preview-datasets}

Wählen Sie im Datensatzaktivitäts-Bildschirm rechts oben die Option **Vorschau des Datensatzes anzeigen** aus, um eine Vorschau des zuletzt erfolgreichen Batches in diesem Datensatz anzuzeigen. Wenn ein Datensatz leer ist, wird der Vorschau-Link deaktiviert.

![](assets/dataset-preview.png)


## Erstellen von Datensätzen{#create-datasets}

Um einen neuen Datensatz zu erstellen, klicken Sie im Dashboard „Datensätze“ auf die Option **Datensatz erstellen**.

Sie haben folgende Möglichkeiten:

* Datensatz aus Schema erstellen. [Weitere Informationen finden Sie in dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de#schema){target=&quot;_blank&quot;}.
* Datensatz aus CSV-Datei erstellen. [Weitere Informationen finden Sie in dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=de){target=&quot;_blank&quot;}.

In diesem Video erfahren Sie, wie Sie einen Datensatz erstellen, ihn einem Schema zuordnen, ihm Daten hinzufügen und bestätigen, dass die Daten aufgenommen wurden.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Data Governance

Sie können in einem Datensatz die Registerkarte **Data Governance** durchsuchen, um Kennzeichnungen auf Datensatz- und Feldebene zu überprüfen. Mit Data Governance werden Daten entsprechend dem anzuwendenden Richtlinientyp kategorisiert.

Eine der Kernfunktionen von [!DNL Adobe Experience Platform] ist es, Daten aus verschiedenen Unternehmenssystemen zusammenzuführen, damit Marketing-Experten Kunden besser identifizieren, verstehen und ansprechen können. Diese Daten können Nutzungsbeschränkungen unterliegen, die von Ihrem Unternehmen oder durch gesetzliche Bestimmungen festgelegt werden. Daher müssen Sie dafür sorgen, dass Ihre Datenoperationen die entsprechenden Datennutzungsrichtlinien einhalten.

Mit [!DNL Adobe Experience Platform Data Governance] können Sie Kundendaten verwalten und bei der Verwendung von Daten die Einhaltung von relevanten Vorschriften, Einschränkungen und Richtlinien sicherstellen. Die Funktion spielt in Experience Platform auf verschiedenen Ebenen eine wichtige Rolle, wie z. B. bei Katalogisierung, Ermittlung der Datenherkunft, Datennutzungsbezeichnung, Datennutzungsrichtlinien und Steuerung der Nutzung von Daten für Marketing-Aktionen.

Weitere Informationen zu Data Governance und Datennutzungskennzeichnungen finden Sie in der Dokumentation zu [Data Governance](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html?lang=de){target=&quot;&quot;_blank&quot;&quot;}.

## Beispiele und Anwendungsfälle{#uc-datasets}

In diesem [vollständigen Beispiel](../segment/creating-test-profiles.md) erfahren Sie, wie Sie ein Schema und einen Datensatz erstellen und Daten aufnehmen, um Testprofile in Adobe Journey Optimizer hinzuzufügen.

Weitere Informationen zur Erstellung von Datensätzen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target=&quot;_blank&quot;}.

Erfahren Sie in der [Dokumentation zur Datenaufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target=&quot;_blank&quot;}, wie Sie die Benutzeroberfläche für Datensätze verwenden.

Eine Liste der Anwendungsfälle mit Abfragebeispielen ist verfügbar. [here](../start/datasets-query-examples.md).

**Siehe auch**

* [Übersicht über die Streaming-Aufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target=&quot;_blank&quot;}
* [Daten in Adobe Experience Platform aufnehmen](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=de){target=&quot;_blank&quot;}
