---
title: Entscheidungsregeln
description: Weitere Informationen zur Arbeit mit Entscheidungsregeln
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 100%

---

# Entscheidungsregeln {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Erstellen von Entscheidungsregeln"
>abstract="Entscheidungsregeln ermöglichen es, die Zielgruppe für Entscheidungselemente zu definieren, indem Einschränkungen angewendet werden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch kann genauer gesteuert werden, welche Artikel wem präsentiert werden sollen."

## Über Entscheidungsregeln {#about}

Entscheidungsregeln ermöglichen es, die Zielgruppe für Entscheidungselemente zu definieren, indem Einschränkungen angewendet werden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch kann genauer gesteuert werden, welche Artikel wem präsentiert werden sollen.

Nehmen wir beispielsweise ein Szenario, in dem Entscheidungselemente mit Yoga-bezogenen Produkten für Frauen vorhanden sind. Mit Entscheidungsregeln kann z. B. festgelegt werden, dass diese Elemente nur für Profile angezeigt werden sollen, deren Geschlecht „weiblich“ ist und die „Yoga“ als einen „Zielpunkt“ angegeben haben.

>[!NOTE]
>
>Zusätzlich zu den Entscheidungsregeln auf Element- und Auswahlstrategieebene können Sie auch Ihre gewünschte Zielgruppe auf Kampagnenebene definieren. [Weitere Informationen](../campaigns/create-campaign.md#audience)

Die Liste der Entscheidungsregeln ist im Menü **[!UICONTROL Strategie-Setup]** verfügbar.

![](assets/decision-rules-list.png)

## Erstellen einer Entscheidungsregel {#create}

Gehen Sie wie folgt vor, um eine Entscheidungsregel zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Strategie-Setup]** > **[!UICONTROL Entscheidungsregeln]** und klicken Sie auf die Schaltfläche **[!UICONTROL Regel erstellen]**.

1. Der Bildschirm zur Erstellung von Entscheidungsregeln wird geöffnet. Benennen Sie Ihre Regel und geben Sie eine Beschreibung an.

1. Erstellen Sie die Entscheidungsregel nach Ihren Bedürfnissen mit dem Adobe Experience Platform Segment Builder. Zu diesem Zweck können Sie verschiedene Datenquellen wie Profilattribute, Zielgruppen oder Kontextdaten aus Adobe Experience Platform nutzen. [Erfahren Sie, wie Sie Kontextdaten nutzen](#context-data).

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >Der zum Erstellen von Entscheidungsregeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Experience Platform-Segmentierungs-Service auf. Das in der Dokumentation beschriebene globale Verfahren gilt jedoch weiter, um Entscheidungsregeln zu erstellen. [Weitere Informationen zum Erstellen von Segmentdefinitionen](../audience/creating-a-segment-definition.md)

1. Während Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, zeigt der Bereich **[!UICONTROL Zielgruppeneigenschaften]** Informationen zur geschätzten Anzahl der zur Zielgruppe gehörenden Profile an. Klicken Sie auf **[!UICONTROL Schätzung aktualisieren]**, um diese Daten zu aktualisieren.

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten.

1. Sobald Ihre Entscheidungsregel fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Die erstellte Regel erscheint in der Liste und kann in Entscheidungselementen und Auswahlstrategien verwendet werden, um die Präsentation von Entscheidungselementen in Profilen zu steuern.

   >[!NOTE]
   >
   >Die Verschachtelungstiefe in einer Eignungsregel ist auf 30 Ebenen beschränkt. Diese wird durch Zählen der schließenden Klammern `)` in der PQL-Zeichenfolge gemessen. Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 15 KB groß sein. Das entspricht 15.000 ASCII-Zeichen (jeweils 1 Byte) oder 3.750 bis 7.500 Nicht-ASCII-Zeichen (jeweils 2 bis 4 Byte). [Weitere Informationen zu den Schutzmechanismen und Einschränkungen bei der Entscheidungsfindung](gs-experience-decisioning.md#guardrails)
