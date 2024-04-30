---
title: Entscheidungsregeln
description: Weitere Informationen zur Arbeit mit Entscheidungsregeln
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 29228a17176421ccf29598d6ebba815b800db7a2
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 36%

---

# Entscheidungsregeln {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Erstellen von Entscheidungsregeln"
>abstract="Entscheidungsregeln ermöglichen es, die Zielgruppe für Entscheidungselemente zu definieren, indem Einschränkungen angewendet werden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch kann genauer gesteuert werden, welche Artikel wem präsentiert werden sollen."

>[!BEGINSHADEBOX „Was Sie in diesem Dokumentationshandbuch finden“]

* [Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)
* Verwalten Ihrer Entscheidungselemente: [Konfigurieren des Elementkatalogs](catalogs.md) – [Erstellen von Entscheidungselementen](items.md) – [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: **[Erstellen von Entscheidungsregeln](rules.md)** – [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

Entscheidungsregeln ermöglichen es, die Zielgruppe für Entscheidungselemente zu definieren, indem Einschränkungen angewendet werden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch kann genauer gesteuert werden, welche Artikel wem präsentiert werden sollen.

Nehmen wir beispielsweise ein Szenario, in dem Entscheidungselemente mit Yoga-bezogenen Produkten für Frauen vorhanden sind. Mit Entscheidungsregeln können Sie festlegen, dass diese Elemente nur für Profile angezeigt werden sollen, deren Geschlecht &quot;weiblich&quot;ist und die in &quot;Yoga&quot;einen &quot;Zielpunkt&quot;angegeben haben.

>[!NOTE]
>
>Zusätzlich zu den Entscheidungsregeln auf Element- und Auswahlstrategieebene können Sie auch Ihre gewünschte Zielgruppe auf Kampagnenebene definieren. [Weitere Informationen](../campaigns/create-campaign.md#audience)

Die Liste der Entscheidungsregeln ist unter **[!UICONTROL Konfiguration]** im Menü **[!UICONTROL Entscheidungsregeln]** verfügbar.

![](assets/decision-rules-list.png)

## Erstellen von Entscheidungsregeln {#create}

Gehen Sie wie folgt vor, um eine Entscheidungsregel zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Konfiguration]** / **[!UICONTROL Entscheidungsregeln]** Klicken Sie dann auf **[!UICONTROL Regel erstellen]** Schaltfläche.

1. Der Bildschirm zur Erstellung von Entscheidungsregeln wird geöffnet. Benennen Sie Ihre Regel und geben Sie eine Beschreibung ein.

1. Erstellen Sie die Entscheidungsregel entsprechend Ihren Anforderungen mit dem Adobe Experience Platform Segment Builder. Dazu können Sie verschiedene Datenquellen nutzen, wie Profilattribute, Zielgruppen oder Kontextdaten aus Adobe Experience Platform. [Erfahren Sie, wie Sie Kontextdaten in Entscheidungsregeln nutzen](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >Der zum Erstellen von Entscheidungsregeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Adobe Experience Platform-Segmentierungsdienst auf.  Der in der Dokumentation beschriebene globale Prozess ist jedoch weiterhin gültig, um Entscheidungsregeln zu erstellen. [Weitere Informationen zum Erstellen von Segmentdefinitionen](../audience/creating-a-segment-definition.md)

1. Während Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, zeigt der Bereich **[!UICONTROL Zielgruppeneigenschaften]** Informationen zur geschätzten Anzahl der zur Zielgruppe gehörenden Profile an. Klicken Sie auf **[!UICONTROL Schätzung aktualisieren]**, um diese Daten zu aktualisieren.

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten.

1. Sobald Ihre Entscheidungsregel fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Die erstellte Regel wird in der Liste angezeigt und steht zur Verwendung in Entscheidungselementen und Auswahlstrategien zur Verfügung, um die Präsentation von Entscheidungselementen zu Profilen zu steuern.

## Nutzung von Kontextdaten in Entscheidungsregeln {#context-data}

Im Bildschirm zur Erstellung von Experience Decisioning-Regeln können Sie alle in Adobe Experience Platform verfügbaren Informationen nutzen, um Entscheidungsregeln zu erstellen. Sie können beispielsweise eine Entscheidungsregel entwerfen, für die das aktuelle Wetter ≥ 80 Grad sein muss.

Dazu müssen Sie zunächst die Daten definieren, die Sie in Experience Decisioning zur Verfügung stellen möchten. Danach werden diese Daten nahtlos in Experience Decisioning in der **[!UICONTROL Kontextdaten]** beim Erstellen einer Entscheidungsregel verfügbar.

![](assets/decision-rules-context.png)

Gehen Sie wie folgt vor, um Experience Decisioning mit Adobe Experience Platform-Daten zu versehen:

1. Erstellen Sie eine **Erlebnisereignisschema**  in Adobe Experience Platform und den zugehörigen **Datensatz**. [Erfahren Sie, wie Sie Schemas erstellen](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Erstellen Sie einen neuen Adobe Experience Platform-Datenspeicher:

   1. Navigieren Sie zum **[!UICONTROL Datenspeicher]** Menü und wählen Sie **[!UICONTROL Neuer Datenspeicher]**.

   1. Im **[!UICONTROL Ereignisschema]** in der Dropdown-Liste das zuvor erstellte Erlebnisereignis-Schema auswählen und auf **[!UICONTROL Speichern]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Klicks **[!UICONTROL Dienst hinzufügen]** und wählen Sie &quot;Adobe Experience Platform&quot;als Dienst aus. Im **[!UICONTROL Ereignis-Datensatz]** in der Dropdown-Liste auswählen, den zuvor erstellten Ereignis-Datensatz auswählen und die **[!UICONTROL Adobe Journey Optimizer]** -Option.

      ![](assets/decision-rules-context-datastream-service.png)

Sobald der Datastream gespeichert wurde, werden die Informationen des ausgewählten Datensatzes automatisch abgerufen und in Experience Decisioning integriert, sodass sie in der Regel innerhalb von ca. 24 Stunden verfügbar sind.

Weitere Anleitungen zum Arbeiten mit Adobe Experience Platform finden Sie in den folgenden Ressourcen:

* [Experience-Datenmodell (XDM)-Schemas](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Datensätze](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Datenspeicher](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
