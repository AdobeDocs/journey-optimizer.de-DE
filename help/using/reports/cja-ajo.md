---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Customer Journey Analytics
description: Erste Schritte mit Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 7523ee45581c9b84cd006d563d3cc04dc4214f3f
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 92%

---

# Manuelles Konfigurieren von [!DNL Customer Journey Analytics] {#cja-ajo}

Die [!DNL Journey Optimizer]-Integration mit [!DNL Customer Journey Analytics] bietet eine ganzheitliche Ansicht all Ihrer Journeys mit automatisierter Berichtverteilung und benutzerdefinierten Visualisierungen der Daten.

Im folgenden Abschnitt wird beschrieben, wie Sie mit Journey Optimizer generierte Daten manuell für eine eingehende Analyse in Customer Journey Analytics nutzen können. Diese Integration kann automatisch eingerichtet werden. [Weitere Informationen](report-gs-cja.md)

![](assets/cja.png)

Nachdem Sie Ihre Journey in [!DNL Journey Optimizer] erstellt haben, können Sie Ihre Kundendaten nach [!DNL Customer Journey Analytics] importieren, um Berichte zu starten und die Auswirkungen jeder Interaktion eines Kunden oder einer Kundin mit Ihren Journeys zu verstehen.

➡️ [Customer Journey Analytics entdecken](https://experienceleague.adobe.com/de/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>Zusätzlich zu dieser Integration können Sie auch den Inhalt von Adobe Journey Optimizer-Datensätzen an Cloud-Speicherorte exportieren und diese Informationen zu Berichts- oder Analysezwecken verwenden. [Erfahren Sie, wie Datensätze an Cloud-Speicherorte exportiert werden](../data/export-datasets.md)
>

Bevor Sie [!DNL Customer Journey Analytics] für Ihre Journeys verwenden können, müssen Sie zunächst die folgende Integration konfigurieren:

1. [Erstellen Sie eine Verbindung](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=de){target="_blank"} in [!DNL Customer Journey Analytics] mit dem **[!UICONTROL Datensatz]**, den Sie an Adobe Experience Platform senden möchten.

   Die folgenden [!DNL Journey Optimizer] können konfiguriert werden:
   * [Journey-Schritt-Ereignis](../data/datasets-query-examples.md#journey-step-event): Ermöglicht Ihnen zu sehen, wer in Ihre Journeys eintritt und wie weit sie kommen.
   * [Nachrichten-Feedback/Tracking von Datensätzen](../data/datasets-query-examples.md#message-feedback-event-dataset): Ermöglicht Ihnen, Versandinformationen bezüglich Ihrer Nachrichten, die über [!DNL Journey Optimizer] gesendet worden sind, anzuzeigen.
   * [Entitäts- und Journey-Datensätze](../data/datasets-query-examples.md#entity-dataset): Ermöglicht Ihnen, Anzeigenamen zu suchen und diese in Ihrem Reporting zu verwenden.

1. [Erstellen Sie eine Datenansicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de){target="_blank"} für die Konfiguration von Abmessungen und Metriken, die Sie für Ihren Bericht verwenden möchten.

   Sie können Journey Optimizer-spezifische Metriken erstellen, um die Daten Ihrer Journeys besser wiederzugeben. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=de#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics){target="_blank"}

>[!NOTE]
>
>Wenn für Ihre Sandbox mehrere Verbindungen vorhanden sind, überprüfen Sie, ob die [Datenansicht](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de){target="_blank"} auf die [Verbindung](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-connections/manage-connections){target="_blank"} mit dem Flag **[!UICONTROL In CJA verwenden]** verweist. Andernfalls kann die Schaltfläche [**Analysieren in CJA** &#x200B;](report-cja-manage.md#analyze) in [!DNL Journey Optimizer] deaktiviert sein.

Wenn Sie [!DNL Journey Optimizer] zusammen mit [!DNL Customer Journey Analytics] verwenden, kann das zu Abweichungen in den Reporting-Daten führen, die durch Folgendes verursacht werden:

* **Sowohl [!DNL Journey Optimizer] als auch [!DNL Customer Journey Analytics] synchronisieren Daten aus Azure Data Lake Storage (ADLS) für das Reporting.**

  Die Verarbeitungszeit für eingehende Daten kann von Produkt zu Produkt leicht unterschiedlich sein. Aus diesem Grund kann es vorkommen, dass die Daten nicht übereinstimmen, wenn Berichte von einem bestimmten Datum bis zum aktuellen Tag angezeigt werden. Um Abweichungen zu vermeiden, verwenden Sie Datumsbereiche, die den aktuellen Tag ausschließen.

* **In [!DNL Journey Optimizer]-Berichten schließt die Metrik „Gesendet“ auch die Metrik „Erneut versuchen“ ein.**

  **[!UICONTROL Erneute Zustellversuche]** werden in die Metrik **[!UICONTROL Gesendet]** in [!DNL Customer Journey Analytics] nicht aufgenommen. Dies führt dazu, dass die Metriken **[!UICONTROL Gesendet]** von [!DNL Customer Journey Analytics] niedrigere Werte anzeigen als in [!DNL Journey Optimizer]. Jedoch werden Daten zu erneuten Zustellversuchen in die Metrik **[!UICONTROL Nachrichten erfolgreich gesendet]** oder die **[!UICONTROL Bounces]**-Metrik einbezogen.
Um Abweichungen zu vermeiden, verwenden Sie Datumsbereiche, die vor einer Woche oder sogar noch früher liegen.

* **Berichte werden aus einer unterschiedlichen Datenquelle bereitgestellt.**

  Dies kann zu Datenabweichungen von 1-2 % zwischen den Produkten führen.
