---
title: Kontextdaten in Experience Decisioning nutzen
description: Erfahren Sie, wie Sie Kontextdaten in Experience Decisioning nutzen können.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 50%

---

# Kontextdaten in Experience Decisioning nutzen {#context}

Mit Experience Decisioning können Sie alle in Adobe Experience Platform verfügbaren Informationen nutzen, um verschiedene Aktionen auszuführen, z. B. die Erstellung von [Entscheidungsregeln](rules.md) oder [Ranking-Formeln](ranking.md). Sie können beispielsweise eine Entscheidungsregel entwerfen, für die das aktuelle Wetter zum Zeitpunkt der Entscheidungsanforderung 80 Grad Celsius beträgt.

>[!NOTE]
>
>Kontextdaten werden in Adobe Experience Platform definiert und zum Zeitpunkt einer Entscheidungsanfrage gesendet. Sie enthält keine historischen Daten.

Um Kontextdaten zu verwenden, müssen Sie zunächst die Daten definieren, die Sie in Experience Decisioning zur Verfügung stellen möchten. Danach werden diese Daten nahtlos in Experience Decisioning in der **[!UICONTROL Kontextdaten]** beim Erstellen einer Entscheidungsregel verfügbar. Sie können die Daten auch bei der Bearbeitung einer Rangformel nutzen.

![](assets/decision-rules-context.png)

Hier erfahren Sie, wie Sie die Erlebnis-Entscheidung mit Daten aus Adobe Experience Platform versorgen können:

1. Erstellen Sie ein **Erlebnisereignis-Schema** in Adobe Experience Platform und den dazugehörigen **Datensatz**. [Lernen Sie, wie man Schemata erstellt](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. So erstellen Sie einen neuen Adobe Experience Platform-Datenstrom:

   1. Navigieren Sie zum Menü **[!UICONTROL Datenströme]** und wählen Sie **[!UICONTROL Neuer Datenstrom]**.

   1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Ereignisschema]** das zuvor erstellte Erlebnis-Ereignisschema aus und klicken Sie auf **[!UICONTROL Speichern]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Klicken Sie auf **[!UICONTROL Dienst hinzufügen]** und wählen Sie „Adobe Experience Platform“ als Dienst. Wählen Sie in der Dropdown-Liste **[!UICONTROL Ereignisdatensatz]** den zuvor erstellten Ereignisdatensatz und aktivieren Sie die Option **[!UICONTROL Adobe Journey Optimizer]**.

      ![](assets/decision-rules-context-datastream-service.png)

Sobald der Datenstrom gespeichert ist, werden die Informationen des ausgewählten Datensatzes automatisch abgerufen und in die Erlebnis-Entscheidung integriert. In der Regel sind sie innerhalb von etwa 24 Stunden verfügbar.

Weitere Anleitungen für die Arbeit mit Adobe Experience Platform finden Sie in den folgenden Ressourcen:

* [Schemata für das Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Datensätze](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Datenströme](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/overview){target="_blank"}
