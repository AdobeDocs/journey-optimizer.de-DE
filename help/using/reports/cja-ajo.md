---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Customer Journey Analytics
description: Erste Schritte mit Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 928ad6822efbe95c0ddf5456531d92be8b4bed75
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Arbeiten mit [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] Integration mit [!DNL Customer Journey Analytics] bietet eine ganzheitliche Sicht auf all Ihre Journeys mit automatisierter Berichtverteilung und benutzerdefinierten Visualisierungen der Daten.

![](assets/cja.png)

Nachdem Sie Ihre Journey in erstellt haben [!DNL Journey Optimizer], können Sie Ihre Kundendaten in [!DNL Customer Journey Analytics] , um Berichte zu erstellen und die Auswirkungen jeder Interaktion zu verstehen, die ein Kunde mit Ihren Journeys hat.

➡️ [Entdecken Sie Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

Vor der Verwendung [!DNL Customer Journey Analytics] für Ihre Journeys müssen Sie diese Integration zunächst konfigurieren:

1. [Verbindung erstellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] mit dem **[!UICONTROL Dataset]** Sie möchten an Adobe Experience Platform senden.

   Folgendes [!DNL Journey Optimizer] kann konfiguriert werden:
   * [Journey-Schrittereignis](../data/datasets-query-examples.md#journey-step-event): können Sie sehen, wer Ihre Journeys betritt und wie weit sie kommen.
   * [Nachrichten-Feedback/Tracking-Datensätze](../data/datasets-query-examples.md#message-feedback-event-dataset): ermöglicht Ihnen, Versandinformationen über Ihre Nachrichten anzuzeigen, die über [!DNL Journey Optimizer].
   * [Entitäts- und Journey-Datensätze](../data/datasets-query-examples.md#entity-dataset): ermöglicht Ihnen, Anzeigenamen zu suchen und in Ihren Berichten zu verwenden.

1. [Datenansicht erstellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) um die Dimensionen und Metriken zu konfigurieren, die Sie für Ihren Bericht verwenden möchten.

   Sie können Journey Optimizer-spezifische Metriken erstellen, um die Daten Ihrer Journeys besser widerzuspiegeln. [Weitere Infos](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Verwenden [!DNL Journey Optimizer] mit [!DNL Customer Journey Analytics] kann zu Abweichungen bei den Berichtsdaten führen, die durch Folgendes verursacht werden:

* **Beide [!DNL Journey Optimizer] und [!DNL Customer Journey Analytics] Synchronisieren von Daten aus Azure Data Lake Storage (ADLS) für die Berichterstellung.**

   Die Verarbeitungszeit für eingehende Daten kann sich von Produkt zu Produkt etwas unterscheiden. Aus diesem Grund stimmen die Daten bei der Anzeige von Berichten von einem bestimmten Datum bis zum aktuellen Tag möglicherweise nicht überein. Um Diskrepanzen zu vermeiden, verwenden Sie Datumsbereiche, die den aktuellen Tag ausschließen.

* **In [!DNL Journey Optimizer] Berichte enthält die Metrik Gesendet auch die Metrik Wiederholen .**

   **[!UICONTROL Retries]** wird nicht in **[!UICONTROL Sent]** Metrik in [!DNL Customer Journey Analytics]. Dies führt zu [!DNL Customer Journey Analytics] **[!UICONTROL Sent]** Metriken, die niedrigere Werte als [!DNL Journey Optimizer]. Wiederholungsdaten werden jedoch in die **[!UICONTROL Messages successfully sent]** oder **[!UICONTROL Bounces]** Metrik.
Um Diskrepanzen zu vermeiden, verwenden Sie Datumsbereiche, die vor einer Woche oder später liegen.

* **Berichte werden aus einer anderen Datenquelle bereitgestellt.**

   Dies könnte zu Datendiskrepanzen zwischen 1 und 2 % zwischen den Produkten führen.
