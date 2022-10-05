---
title: Arbeiten mit Customer Journey Analytics
description: Erste Schritte mit Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: ce0906afb8561c586cb080c4a49c58fb5bfac6a9
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 7%

---

# Arbeiten mit [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)
[!DNL Journey Optimizer] Integration mit [!DNL Customer Journey Analytics] bietet eine ganzheitliche Sicht auf all Ihre Journey mit automatisierter Berichtverteilung und benutzerdefinierten Visualisierungen der Daten.

Nachdem Sie die Journey in [!DNL Journey Optimizer], können Sie Ihre Kundendaten in [!DNL Customer Journey Analytics] , um Berichte zu erstellen und die Auswirkungen jeder Interaktion eines Kunden mit seinen Journey zu verstehen.

➡️ [Discover-Customer Journey Analytics](https://docs.adobe.com/content/help/de-DE/experience-cloud/user-guides/home.translate.html){target=&quot;_blank&quot;}

Vor der Verwendung [!DNL Customer Journey Analytics] für Ihre Journey müssen Sie zunächst diese Integration konfigurieren:

1. [Verbindung erstellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=de) in [!DNL Customer Journey Analytics] mit dem **[!UICONTROL Datensatz]** Sie an Platform senden möchten.

   Folgendes [!DNL Journey Optimizer] kann konfiguriert werden:
   * [Journey-Schrittereignis](../start/datasets-query-examples.md#journey-step-event): können Sie sehen, wer in die Journey eintritt und wie weit sie kommen.
   * [Nachrichten-Feedback/Tracking-Datensätze](../start/datasets-query-examples.md#message-feedback-event-dataset): ermöglicht Ihnen, Versandinformationen über Ihre Nachrichten anzuzeigen, die über [!DNL Journey Optimizer].
   * [Entitäts- und Journey-Datensätze](../start/datasets-query-examples.md#entity-dataset): ermöglicht Ihnen, Anzeigenamen zu suchen und in Ihren Berichten zu verwenden.

1. [Datenansicht erstellen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=de) um die Dimensionen und Metriken zu konfigurieren, die Sie für Ihren Bericht verwenden möchten.

   Sie können Journey Optimizer-spezifische Metriken erstellen, um Ihre Journey besser widerzuspiegeln. [Weitere Informationen](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


Verwenden [!DNL Journey Optimizer] mit [!DNL Customer Journey Analytics] kann zu Abweichungen bei den Berichtsdaten führen, die durch Folgendes verursacht werden:

* **Beide [!DNL Journey Optimizer] und [!DNL Customer Journey Analytics] Synchronisieren von Daten aus Azure Data Lake Storage (ADLS) für die Berichterstellung.**

   Die Verarbeitungszeit für eingehende Daten kann sich von Produkt zu Produkt etwas unterscheiden. Aus diesem Grund stimmen die Daten bei der Anzeige von Berichten von einem bestimmten Datum bis zum aktuellen Tag möglicherweise nicht überein. Um Diskrepanzen zu vermeiden, verwenden Sie Datumsbereiche, die den aktuellen Tag ausschließen.

* **In [!DNL Journey Optimizer] Berichte enthält die Metrik Gesendet auch die Metrik Wiederholen .**

   **[!UICONTROL Weitere Zustellversuche]** wird nicht in **[!UICONTROL Gesendet]** Metrik in [!DNL Customer Journey Analytics]. Dies führt zu [!DNL Customer Journey Analytics] **[!UICONTROL Gesendet]** Metriken, die niedrigere Werte als [!DNL Journey Optimizer]. Wiederholungsdaten werden jedoch in die **[!UICONTROL Nachrichten wurden erfolgreich gesendet]** oder **[!UICONTROL Bounces]** Metrik.
Um Diskrepanzen zu vermeiden, verwenden Sie Datumsbereiche, die vor einer Woche oder später liegen.

* **Berichte werden aus einer anderen Datenquelle bereitgestellt.**

   Dies könnte zu Datendiskrepanzen zwischen 1 und 2 % zwischen den Produkten führen.
