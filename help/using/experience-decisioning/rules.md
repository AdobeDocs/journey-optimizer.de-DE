---
title: Erstellen von Regeln
description: Informationen zum Arbeiten mit Regeln
feature: Decisioning, Campaigns, Journeys, Activities
topic: Integrations, Content Management
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
version: Journey Orchestration
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 100%

---

# Erstellen von Regeln {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Erstellen von Regeln"
>abstract="Sie können zwei Regeltypen erstellen. Zum einen gibt es **Entscheidungsregeln**, die in Entscheidungselementen oder Auswahlstrategien verwendet werden können, um zu steuern, welche Elemente welcher Zielgruppe unterbreitet werden sollen. Zum anderen gibt es **Targeting-Regeln**, um bestimmte Zielgruppensegmente zu bestimmen, die für den Empfang personalisierter Inhalte geeignet sind, oder um einen bestimmten Journey-Pfad einzugeben.<br/><br/>Beim Erstellen einer Entscheidungsregel können Sie **[!UICONTROL Datensatzsuche aktivieren]** auswählen, um Adobe Experience Platform-Daten zu verwenden. Dadurch können Sie Eignungskriterien definieren, die auf dynamischen, externen Attributen basieren, sodass Entscheidungselemente nur angezeigt werden, wenn sie relevant sind."

## Informationen zu Regeln {#about}

In [!DNL Journey Optimizer] können Sie zwei Arten wiederverwendbarer Regeln erstellen:

* [Entscheidungsregeln](#decision-rules)
* [Targeting-Regeln](#targeting-rules)

### Entscheidungsregeln {#decision-rules}

Entscheidungsregeln ermöglichen es, die Zielgruppe für Entscheidungselemente zu definieren, indem Einschränkungen angewendet werden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch kann genauer gesteuert werden, welche Artikel wem präsentiert werden sollen.

Nehmen wir beispielsweise ein Szenario, in dem Entscheidungselemente mit Yoga-bezogenen Produkten für Frauen vorhanden sind. Mit Entscheidungsregeln kann z. B. festgelegt werden, dass diese Elemente nur für Profile angezeigt werden sollen, deren Geschlecht „weiblich“ ist und die „Yoga“ als einen „Zielpunkt“ angegeben haben.

>[!NOTE]
>
>Zusätzlich zu den Entscheidungsregeln auf Element- und Auswahlstrategieebene können Sie auch Ihre gewünschte Zielgruppe auf Kampagnenebene definieren. [Weitere Informationen](../campaigns/create-campaign.md#audience)

### Targeting-Regeln {#targeting-rules}

>[!AVAILABILITY]
>
>Targeting-Regeln sind derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.
>
>Beachten Sie, dass diese Funktion nur für Organisationen verfügbar ist, die das **Entscheidungsfindungs**-Add-on erworben haben. Sie wird nach und nach für alle Kundinnen und Kunden eingeführt.

Über Targeting-Regeln können bestimmte Qualifizierungen festgelegt werden, die eine Person erfüllen muss, um für den Erhalt personalisierter Inhalte oder den Eintritt in einen bestimmten Journey-Pfad berechtigt zu sein. Diese Regeln basieren auf bestimmten Zielgruppensegmenten, mit denen Sie Teilzielgruppen in Ihren Journeys und Kampagnen ansprechen können.

Häufig handelt es sich dabei um eine Kombination mehrerer Attribute zusätzlich zu Kundenverhaltensereignissen und Kontextdaten. Um Zeit und Aufwand zu sparen, können Sie Targeting-Regeln einmal erstellen und dann in Ihren Journeys und Kampagnen wiederverwenden. Sie können sie auch zum Zeitpunkt der Erstellung schnell inline ändern.

Sie können diese Regeln in folgenden Szenarien verwenden:

* Beim Erstellen von [Targeting zur Inhaltsoptimierung](../content-management/optimization-targeting.md) in Journeys oder Kampagnen.
* Beim Erstellen der [Journey-Pfadoptimierung](../building-journeys/optimize.md#targeting).

➡️ [Funktion im Video kennenlernen](#video)

## Zugriff auf Regeln {#access}

Die Liste der Regeln ist im Menü **[!UICONTROL Entscheidungsfindung]** > **[!UICONTROL Strategie-Setup]** verfügbar.

Folgende Aktionen stehen zur Verfügung:

* Sie können nach der Regelentität filtern (**[!UICONTROL Entscheidungselement]** oder **[!UICONTROL Targeting]** – [Weitere Informationen](#about)).

* Wählen Sie eine Regel aus, indem Sie auf ihren Namen klicken, und bearbeiten Sie sie mit dem Regel-Builder. [Weitere Informationen](#create)

* Über die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben jedem Element können Sie Folgendes ausführen:

   * Wenn Sie die Entität **[!UICONTROL Entscheidungselement]** ausgewählt haben, fügen Sie die Regel einem Paket hinzu, um sie in eine andere Sandbox zu exportieren. Erfahren Sie, wie Sie [Objekte in eine andere Sandbox exportieren](../configuration/copy-objects-to-sandbox.md).
   * Duplizieren Sie eine Regel.
   * Löschen Sie eine Regel.

![](assets/rules-list.png){width=100%}

* Klicken Sie auf das Symbol **[!UICONTROL Weitere Informationen]**, um die Formel anzuzeigen, aus der die Regel besteht.

![](assets/rule-formula.png){width=60%}

## Erstellen einer Regel {#create}

Gehen Sie wie folgt vor, um eine Regel zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Entscheidungsfindung]** > **[!UICONTROL Strategie-Setup]** > **[!UICONTROL Regeln]** und klicken Sie dann auf die Schaltfläche **[!UICONTROL Regel erstellen]**.

1. Wählen Sie die Regelentität aus, um anzugeben, für welchen Objekttyp die Regel erstellt werden soll.

   ![](assets/rules-select-entity.png){width=90%}

   * **[!UICONTROL Entscheidungselement]**: Die Regel kann auf ein [Entscheidungselement](#decision-rules) im Kontext von Entscheidungsfindung angewendet werden.
   * **[!UICONTROL Targeting]**: Die Regel kann beim Erstellen von [Targeting](#targeting-rules)-Regeln verwendet werden, entweder im Rahmen der [Inhaltsoptimierung](../content-management/optimization-targeting.md) in einer Kampagne oder Journey oder in der Aktivität [Journey optimieren](../building-journeys/optimize.md#targeting).

1. Wenn Sie eine Regel für ein **[!UICONTROL Entscheidungselement]** erstellen, können Sie **[!UICONTROL Datensatzsuche aktivieren]** auswählen, um Daten aus Adobe Experience Platform zur Anreicherung Ihrer Entscheidungslogik mit externen Daten zu verwenden. Dies ist besonders nützlich bei Attributen, die sich häufig ändern, beispielsweise die Produktverfügbarkeit oder Echtzeitpreise.

   >[!AVAILABILITY]
   >
   >Diese Funktion steht derzeit allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung. Wenden Sie sich an Ihren Kontakt in der Kundenbetreuung, wenn Sie Zugriff wünschen. [Informationen zum Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung](../experience-decisioning/aep-data-exd.md)

1. Der Bildschirm zur Regelerstellung wird geöffnet. Benennen Sie Ihre Regel und geben Sie eine Beschreibung an.

1. Erstellen Sie die Regel nach Ihren Bedürfnissen mit dem Segment Builder von Adobe Experience Platform. Dazu können verschiedene Datenquellen genutzt werden, z. B.:
   * Profilattribute;
   * Attribute für Entscheidungselemente (nur beim Erstellen einer Regel für ein **[!UICONTROL Entscheidungselement]** verfügbar);
   * Zielgruppen;
   * Kontextdaten von Adobe Experience Platform. [Weitere Informationen zur Nutzung von Kontextdaten](context-data.md)

   ![](assets/decision-rules-build.png){width=85%}

   >[!NOTE]
   >
   >Der zum Erstellen von Regeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Segmentierungs-Service von Adobe Experience Platform auf. Das in der Dokumentation beschriebene globale Verfahren gilt jedoch weiter, um Regeln in [!DNL Journey Optimizer] zu erstellen. [Weitere Informationen zum Erstellen von Segmentdefinitionen](../audience/creating-a-segment-definition.md)

1. Während Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, zeigt der Bereich **[!UICONTROL Zielgruppeneigenschaften]** Informationen zur geschätzten Anzahl der zur Zielgruppe gehörenden Profile an. Klicken Sie auf **[!UICONTROL Schätzung aktualisieren]**, um diese Daten zu aktualisieren.

   ![](assets/decision-rule-audience-properties.png){width=85%}

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn die Regelparameter Daten enthalten, die nicht im Profil gespeichert sind, z. B. Kontextdaten.

1. Sobald Ihre Regel fertig ist, klicken Sie auf **[!UICONTROL Speichern]**. Die erstellte Regel wird in der Liste angezeigt und steht je nach der von Ihnen erstellten Entität zur Verwendung zur Verfügung:

   * in **Entscheidungselementen** und **Auswahlstrategien** für die Präsentation von Entscheidungselementen für Profile;
   * oder beim Erstellen von **Targeting** in der Inhaltsoptimierung oder Pfadoptimierung.

>[!NOTE]
>
>Die Verschachtelungstiefe in einer Regel ist auf 30 Ebenen beschränkt. Dies wird durch Zählen der schließenden Klammern `)` im PQL-String gemessen.
>
>Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 15 KB groß sein. Das entspricht 15.000 ASCII-Zeichen (jeweils 1 Byte) oder 3.750 bis 7.500 Nicht-ASCII-Zeichen (jeweils 2 bis 4 Byte).
>
>[Weitere Informationen zu den Leitlinien und Einschränkungen für Eignungsregeln](decisioning-guardrails.md#eligibility-rules)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie in Adobe Journey Optimizer wiederverwendbare **Targeting-Regeln** erstellen, duplizieren und anwenden, um Kampagnen effizient auf der Grundlage von Kundenattributen wie Region, Sprache und Verhalten zu personalisieren. So sparen Sie Zeit und verbessern die Genauigkeit der Zielgruppe.

>[!VIDEO](https://video.tv.adobe.com/v/3476136/?captions=ger&quality=12)
