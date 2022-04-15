---
title: Erste Schritte mit Datensätzen
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in Adobe Journey Optimizer verwenden.
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 55%

---

# Erste Schritte mit Datensätzen {#datasets-gs}

Alle Daten, die in Adobe Experience Platform aufgenommen werden, bleiben als Datensätze im Data Lake erhalten. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet.

## Auf Datensätze zugreifen{#access-datasets}

Die **Datensätze** Arbeitsbereich in [!DNL Adobe Journey Optimizer] Mithilfe der Benutzeroberfläche können Sie Daten untersuchen und Datensätze erstellen.

Auswählen **Datensätze** im linken Navigationsbereich, um das Dashboard &quot;Datensätze&quot;zu öffnen.

![](assets/datasets-home.png)

Das Hinzufügen von Daten zu Adobe Experience Platform bildet die Grundlage für die Erstellung eines Profils. Anschließend können Sie Profile in [!DNL Adobe Journey Optimizer] nutzen. Definieren Sie zunächst Schemas, verwenden Sie ETL-Tools, um Ihre Daten vorzubereiten und zu standardisieren, und erstellen Sie dann Datensätze basierend auf Ihren Schemas.

Wählen Sie die **Durchsuchen** um die Liste aller für Ihre Organisation verfügbaren Datensätze anzuzeigen. Zu jedem aufgelisteten Datensatz werden Details angezeigt, einschließlich seines Namens, des Schemas, dem der Datensatz entspricht, und des Status des letzten Erfassungslaufs.

Standardmäßig werden nur die Datensätze angezeigt, die Sie in aufgenommen haben. Wenn Sie die systemgenerierten Datensätze anzeigen möchten, aktivieren Sie die **Anzeigen von Systemdatensätzen** Aus dem Filter ein-/ausblenden.

![](assets/ajo-system-datasets.png)

Wählen Sie den Namen eines Datensatzes aus, um auf den Bildschirm Datensatzaktivität zuzugreifen und Details zum ausgewählten Datensatz anzuzeigen. Der Tab „Aktivität“ enthält ein Diagramm, das die Rate der konsumierten Nachrichten sowie eine Liste erfolgreicher und fehlgeschlagener Batches visuell darstellt.

## Erstellen von Datensätzen{#create-datasets}

Um einen neuen Datensatz zu erstellen, wählen Sie zunächst **Datensatz erstellen** im Dashboard &quot;Datensätze&quot;ein.

Sie haben folgende Möglichkeiten:

* Datensatz aus Schema erstellen. [Weitere Informationen finden Sie in dieser Dokumentation .](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Datensatz aus CSV-Datei erstellen. [Weitere Informationen finden Sie in dieser Dokumentation .](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=de){target=&quot;_blank&quot;}


In diesem Video erfahren Sie, wie Sie einen Datensatz erstellen, ihn einem Schema zuordnen, ihm Daten hinzufügen und bestätigen, dass die Daten erfasst wurden.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


Erfahren Sie, wie Sie ein Schema, einen Datensatz und Daten erstellen, um Testprofile in Adobe Journey Optimizer hinzuzufügen [Dieses End-to-End-Beispiel](../segment/creating-test-profiles.md)

Erfahren Sie mehr über die Erstellung von Datensätzen in [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target=&quot;_blank&quot;}.

Erfahren Sie in der [Dokumentation zur Datenaufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target=&quot;_blank&quot;}, wie Sie die Benutzeroberfläche für Datensätze verwenden.


**Siehe auch**

* [Erstellen eines Schemas und eines Datensatzes und Aufnehmen von Daten zum Hinzufügen von Testprofilen in Journey Optimizer](../segment/creating-test-profiles.md)
* [Übersicht über die Streaming-Aufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=de){target=&quot;_blank&quot;}
* [Daten in Adobe Experience Platform aufnehmen](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=de){target=&quot;_blank&quot;}
