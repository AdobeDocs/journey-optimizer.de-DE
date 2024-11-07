---
title: Nutzung von Kontextdaten in Decisioning
description: Erfahren Sie, wie Sie Kontextdaten in Decisioning nutzen können.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: 22eae783ec2a7db2209b2a12b78b286e4f97ee1b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 59%

---

# Nutzung von Kontextdaten in Decisioning {#context}

Mit Decisioning können Sie alle in Adobe Experience Platform verfügbaren Informationen nutzen, um verschiedene Aktionen durchzuführen, z. B. das Erstellen von [Entscheidungsregeln](rules.md) oder [Ranking-Formeln](ranking.md). Sie können zum Beispiel eine Entscheidungsregel entwerfen, die verlangt, dass das aktuelle Wetter zum Zeitpunkt der Entscheidungsanfrage  wärmer als 25 °C sein muss.

>[!NOTE]
>
>Kontextdaten werden in Adobe Experience Platform definiert und zum Zeitpunkt einer Entscheidungsanfrage gesendet. Historische Daten werden nicht berücksichtigt.

Um Kontextdaten zu verwenden, müssen Sie zunächst die Daten definieren, die Sie in der Entscheidungsfindung zur Verfügung stellen möchten. Anschließend werden diese Daten nahtlos in die Entscheidungsfindung auf der Registerkarte **[!UICONTROL Kontextdaten]** integriert, die beim Erstellen einer Entscheidungsregel verfügbar ist. Sie können die Daten auch bei der Bearbeitung einer Rangfolgeformel nutzen.

![](assets/decision-rules-context.png)

Gehen Sie wie folgt vor, um Decisioning mit Adobe Experience Platform-Daten zu versehen:

1. Erstellen Sie ein **Erlebnisereignis-Schema** in Adobe Experience Platform und den dazugehörigen **Datensatz**. [Lernen Sie, wie man Schemata erstellt](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. So erstellen Sie einen neuen Adobe Experience Platform-Datenstrom:

   1. Navigieren Sie zum Menü **[!UICONTROL Datenströme]** und wählen Sie **[!UICONTROL Neuer Datenstrom]**.

   1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Ereignisschema]** das zuvor erstellte Erlebnis-Ereignisschema aus und klicken Sie auf **[!UICONTROL Speichern]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Klicken Sie auf **[!UICONTROL Dienst hinzufügen]** und wählen Sie „Adobe Experience Platform“ als Dienst. Wählen Sie in der Dropdown-Liste **[!UICONTROL Ereignisdatensatz]** den zuvor erstellten Ereignisdatensatz und aktivieren Sie die Option **[!UICONTROL Adobe Journey Optimizer]**.

      ![](assets/decision-rules-context-datastream-service.png)

Sobald der Datastream gespeichert wurde, werden die Informationen des ausgewählten Datensatzes automatisch abgerufen und in Decisioning integriert, sodass sie in der Regel innerhalb von ca. 24 Stunden verfügbar sind.

Weitere Anleitungen für die Arbeit mit Adobe Experience Platform finden Sie in den folgenden Ressourcen:

* [Schemata für das Experience-Datenmodell (XDM)](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Datensätze](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Datenströme](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/overview){target="_blank"}
