---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Datensätzen
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in Adobe Journey Optimizer verwenden.
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 7e27f5502d64d0c91de2c67e4011e650e77c6a92
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Erste Schritte mit Datensätzen {#datasets-gs}

Alle Daten, die in Adobe Experience Platform erfasst werden, werden im Data Lake als Datensätze persistiert. Ein Datensatz ist ein Speicher- und Verwaltungskonstrukt für eine Sammlung von Daten, normalerweise eine Tabelle, die ein Schema (Spalten) und Felder (Zeilen) enthält.

## Auf Datensätze zugreifen{#access-datasets}

Die **Datensätze** Arbeitsbereich in [!DNL Adobe Journey Optimizer] Mithilfe der Benutzeroberfläche können Sie Daten untersuchen und Datensätze erstellen.

Auswählen **Datensätze** im linken Navigationsbereich, um das Dashboard &quot;Datensätze&quot;zu öffnen.

![](assets/datasets-home.png)

Daten hinzufügen zu [!DNL Adobe Experience Platform] ist die Grundlage für den Aufbau eines Profils. Anschließend können Sie Profile in [!DNL Adobe Journey Optimizer]. Definieren Sie zunächst Schemata, verwenden Sie ETL-Tools, um Ihre Daten vorzubereiten und zu standardisieren, und erstellen Sie dann Datensätze basierend auf Ihren Schemas.

Wählen Sie die **Durchsuchen** um die Liste aller für Ihre Organisation verfügbaren Datensätze anzuzeigen. Details werden für jeden aufgelisteten Datensatz angezeigt, einschließlich seines Namens, des Schemas, dem der Datensatz entspricht, und des Status des letzten Erfassungslaufs.

Standardmäßig werden nur die Datensätze angezeigt, die Sie in aufgenommen haben. Wenn Sie die systemgenerierten Datensätze anzeigen möchten, aktivieren Sie die **Anzeigen von Systemdatensätzen** Aus dem Filter ein-/ausblenden.

![](assets/ajo-system-datasets.png)

Wählen Sie den Namen eines Datensatzes aus, um auf den Bildschirm Datensatzaktivität zuzugreifen und Details zum ausgewählten Datensatz anzuzeigen. Der Tab Aktivität enthält ein Diagramm, das die Rate der konsumierten Nachrichten sowie eine Liste erfolgreicher und fehlgeschlagener Batches visualisiert.

Im Folgenden finden Sie die verschiedenen verfügbaren Datensätze:

**Berichterstellung**

* _Reporting - Datensatz mit Nachrichten-Feedback-Ereignissen_: Versandlogs der Nachrichten. Informationen zum gesamten Nachrichtenversand von Journey Optimizer für Berichterstellungs- und Segmenterstellungszwecke. In diesem Datensatz wird auch das Feedback von E-Mail-ISPs zu Bounces aufgezeichnet.
* _Reporting - E-Mail-Tracking-Erlebnisdatensatz_: Interaktionsprotokolle für den E-Mail-Kanal, der zur Berichterstellung und Segmenterstellung verwendet wird. Informationen, die gespeichert werden und Informationen zu Aktionen enthalten, die der Endbenutzer in E-Mails (Öffnungen, Klicks usw.) durchführt.
* _Berichterstellung - Ereignis-Datensatz für Push-Tracking_: Interaktionsprotokolle für den Push-Kanal, der für Berichte- und Segmenterstellungszwecke verwendet wird. Gespeicherte Informationen zu Aktionen, die vom Endbenutzer bei Push-Benachrichtigungen ausgeführt werden.
* _Reporting - Journey Step-Ereignis_: Erfasst alle Journey Step-Erlebnisereignisse, die von Journey Optimizer generiert wurden, und kann von Diensten wie Reporting genutzt werden. Auch für die Erstellung von Berichten in Customer Journey Analytics für YoY-Analysen wichtig. An Journey-Metadaten gebunden.
* _Reporting - Journeys_: Metadaten-Datensatz mit Informationen zu jedem Schritt in einer Journey.
* _Berichterstellung - BCC_: Feedback-Ereignis-Datensatz, in dem die Versandlogs für BCC-E-Mails gespeichert werden. Für Berichtszwecke.

**Einverständnis**

* _Datensatz des Zustimmungsdienstes_: speichert Einverständnisinformationen eines Profils.

**Intelligent Services**

* _Sendezeit-Optimierungsbewertungen/Interaktionswerte_: Ausgabe von Bewertungen von Journey AI.

## Vorschau von Datensätzen anzeigen{#preview-datasets}

Wählen Sie im Bildschirm Datensatzaktivität die Option **Vorschau des Datensatzes anzeigen** in der oberen rechten Ecke des Bildschirms, um eine Vorschau des zuletzt erfolgreichen Batches in diesem Datensatz anzuzeigen. Wenn ein Datensatz leer ist, wird der Vorschau-Link deaktiviert.

![](assets/dataset-preview.png)

## Erstellen von Datensätzen{#create-datasets}

Um einen neuen Datensatz zu erstellen, wählen Sie zunächst **Datensatz erstellen** im Dashboard &quot;Datensätze&quot;ein.

Sie können:

* Erstellen Sie einen Datensatz aus einem Schema. [Weitere Informationen finden Sie in dieser Dokumentation .](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Erstellen Sie einen Datensatz aus einer CSV-Datei. [Weitere Informationen finden Sie in dieser Dokumentation .](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html){target=&quot;_blank&quot;}

In diesem Video erfahren Sie, wie Sie einen Datensatz erstellen, ihn einem Schema zuordnen, ihm Daten hinzufügen und bestätigen, dass die Daten erfasst wurden.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Data Governance

Durchsuchen Sie in einem Datensatz die **Data Governance** -Registerkarte, um Beschriftungen auf Datensatz- und Feldebene zu überprüfen. Data Governance kategorisiert Daten nach dem anzuwendenden Richtlinientyp.

Eine der Kernfunktionen von [!DNL Adobe Experience Platform] ist es, Daten aus verschiedenen Unternehmenssystemen zusammenzuführen, damit Marketing-Experten Kunden besser identifizieren, verstehen und ansprechen können. Diese Daten können Nutzungsbeschränkungen unterliegen, die von Ihrer Organisation oder durch gesetzliche Bestimmungen festgelegt werden. Daher müssen Sie sicherstellen, dass Ihre Datenvorgänge mit Datennutzungsrichtlinien konform sind.

[!DNL Adobe Experience Platform Data Governance] ermöglicht Ihnen, Kundendaten zu verwalten und die Einhaltung von Vorschriften, Einschränkungen und Richtlinien für die Datennutzung sicherzustellen. Sie spielt in Experience Platform auf verschiedenen Ebenen eine Schlüsselrolle, einschließlich Katalogisierung, Datenherkunft, Datennutzungsbezeichnung, Datennutzungsrichtlinien und Steuerung der Nutzung von Daten für Marketing-Aktionen.

Weitere Informationen zu Data Governance und Datennutzungsbezeichnungen finden Sie im Abschnitt [Data Governance-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;}

## Beispiele und Anwendungsbeispiele{#uc-datasets}

Erfahren Sie, wie Sie ein Schema, einen Datensatz und Daten erfassen, um Testprofile in Adobe Journey Optimizer hinzuzufügen in [Dieses End-to-End-Beispiel](../segment/creating-test-profiles.md)

Erfahren Sie mehr über die Erstellung von Datensätzen in [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

Erfahren Sie, wie Sie die Benutzeroberfläche &quot;Datensätze&quot;im [Dokumentation zur Datenerfassung - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}.

Eine Liste der Anwendungsfälle mit Abfragebeispielen ist verfügbar. [here](../data/datasets-query-examples.md).

**Siehe auch**

* [Streaming-Erfassung - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}
* [Daten in Adobe Experience Platform erfassen](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
