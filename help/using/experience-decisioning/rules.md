---
title: Regeln erstellen
description: Erfahren Sie, wie Sie mit Regeln arbeiten
feature: Decisioning, Campaigns, Journeys, Activities
topic: Integrations, Content Management
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/yfeFpaNi0rYVeyXdzaZ7SfoZnu-BkyivCMDzED7dpsM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1106
ht-degree: 0%

---

# Regeln erstellen {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Regeln erstellen"
>abstract="Sie können zwei Regeltypen erstellen: **Entscheidungsregeln** die in Entscheidungselementen oder Auswahlstrategien verwendet werden können, um zu steuern, welche Elemente welcher Zielgruppe unterbreitet werden sollen, oder **Targeting-Regeln** um bestimmte Zielgruppensegmente zu bestimmen, die für den Empfang personalisierter Inhalte geeignet sind, oder um einen bestimmten Journey-Pfad einzugeben.<br/><br/>Beim Erstellen einer Entscheidungsregel können Sie „Datensatzsuche aktivieren **[!UICONTROL auswählen,]** Adobe Experience Platform-Daten zu verwenden. Auf diese Weise können Sie Eignungskriterien basierend auf dynamischen, externen Attributen definieren, sodass Entscheidungselemente nur angezeigt werden, wenn sie relevant sind."

## Über Regeln {#about}

In [!DNL Journey Optimizer] können Sie zwei Arten wiederverwendbarer Regeln erstellen:

* [Entscheidungsregeln](#decision-rules)
* [Zielgruppenbestimmungsregeln](#targeting-rules)

### Entscheidungsregeln {#decision-rules}

Entscheidungsregeln ermöglichen es Ihnen, die Audience für Entscheidungselemente zu definieren, indem Sie Einschränkungen anwenden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Auf diese Weise können Sie genau steuern, welche Elemente wem präsentiert werden sollen.

Betrachten wir beispielsweise ein Szenario, in dem Sie Entscheidungselemente mit Yoga-bezogenen Produkten für Frauen haben. Mit Entscheidungsregeln können Sie festlegen, dass diese Elemente nur Profilen angezeigt werden sollen, deren Geschlecht „Weiblich“ ist und die einen „Point of Interest“ in „Yoga“ angegeben haben.

>[!NOTE]
>
>Zusätzlich zu den Entscheidungsregeln auf Element- und Auswahlstrategieebene können Sie auch Ihre vorgesehene Audience auf Kampagnenebene definieren. [Weitere Informationen](../campaigns/create-campaign.md#audience)

### Zielgruppenbestimmungsregeln {#targeting-rules}

>[!AVAILABILITY]
>
>Zielgruppenbestimmungsregeln sind derzeit nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.
>
>Beachten Sie, dass diese Funktion nur für Organisationen verfügbar ist, die das Add-on **Decisioning** erworben haben. Er wird nach und nach für alle Kunden eingeführt.

Mit Zielgruppenbestimmungsregeln können spezifische Qualifikationen festgelegt werden, die eine Kundin oder ein Kunde erfüllen muss, um für den Erhalt personalisierter Inhalte oder die Eingabe eines bestimmten Journey-Pfads berechtigt zu sein. Diese Regeln basieren auf bestimmten Zielgruppensegmenten, mit denen Sie Unterzielgruppen in Ihren Journey und Kampagnen ansprechen können.

Häufig handelt es sich dabei um eine Kombination mehrerer Attribute zusätzlich zu Kundenverhaltensereignissen und Kontextdaten. Um Zeit und Aufwand zu sparen, können Sie Targeting-Regeln einmal erstellen und dann in Ihren Journey und Kampagnen wiederverwenden, sodass Sie sie zum Zeitpunkt der Erstellung schnell inline ändern können.

Sie können die folgenden Regeln verwenden:

* Beim Erstellen [Zielgruppenbestimmung zur Inhaltsoptimierung](../building-journeys/path-targeting.md) in Journey oder Kampagnen;
* Beim Erstellen der [Journey-Pfadoptimierung](../building-journeys/path-targeting.md).

➡️ [Entdecken Sie diese Funktion im Video](#video)

## Zugriffsregeln {#access}

Die Liste der Regeln ist im Menü **[!UICONTROL Entscheidungsfindung]** > **[!UICONTROL Strategie einrichten]** verfügbar.

Die folgenden Aktionen sind verfügbar:

* Sie können nach der Regelentität filtern **[!UICONTROL Entscheidungselement]** oder **[!UICONTROL Targeting]** - [Weitere Informationen](#about).

* Wählen Sie eine Regel aus, indem Sie auf ihren Namen klicken, und bearbeiten Sie sie mit dem Regel-Builder. [Weitere Informationen](#create)

* Über die Schaltfläche **[!UICONTROL Mehr Aktionen]** neben jedem Element haben Sie folgende Möglichkeiten:

   * Wenn Sie die Entität **[!UICONTROL Entscheidungselement]** ausgewählt haben, fügen Sie die Regel einem Paket hinzu, um sie in eine andere Sandbox zu exportieren. Erfahren Sie, wie [&#x200B; Objekte in eine andere Sandbox exportieren &#x200B;](../configuration/copy-objects-to-sandbox.md).
   * Duplizieren Sie eine Regel.
   * Löschen einer Regel.

![](assets/rules-list.png){width=100%}

* Klicken Sie auf das Symbol **[!UICONTROL Weitere Informationen]**, um die Formel anzuzeigen, aus der die Regel besteht.

![](assets/rule-formula.png){width=60%}

## Erstellen einer Regel {#create}

Gehen Sie wie folgt vor, um eine Regel zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Decisioning]** > **[!UICONTROL Strategie einrichten]** > **[!UICONTROL Regeln]** und klicken Sie dann auf die Schaltfläche **[!UICONTROL Regel erstellen]**.

1. Wählen Sie die Regelentität aus, um anzugeben, für welchen Objekttyp die Regel erstellt werden soll.

   ![](assets/rules-select-entity.png){width=90%}

   * **[!UICONTROL Entscheidungselement]** - Die Regel kann auf ein [Entscheidungselement](#decision-rules) im Kontext von Entscheidungsfindung angewendet werden;
   * **[!UICONTROL Targeting]** - Die Regel kann beim Erstellen von [Targeting](#targeting-rules)-Regeln verwendet werden, entweder im Rahmen der [Inhaltsoptimierung](../building-journeys/path-targeting.md) in einer Kampagne oder einer Journey, entweder in der [Journey optimieren](../building-journeys/path-targeting.md).

1. Wenn Sie eine Regel **[!UICONTROL Entscheidungselement]** erstellen, können Sie **[!UICONTROL Datensatzsuche aktivieren]** auswählen, um Daten aus Adobe Experience Platform zur Anreicherung Ihrer Entscheidungslogik mit externen Daten zu verwenden. Dies ist besonders nützlich bei Attributen, die sich häufig ändern, z. B. Produktverfügbarkeit oder Echtzeit-Preisen. [Erfahren Sie, wie Sie Adobe Experience Platform-Daten für die Entscheidungsfindung verwenden](../experience-decisioning/aep-data-exd.md)

1. Der Bildschirm zur Regelerstellung wird geöffnet. Benennen Sie Ihre Regel und geben Sie eine Beschreibung ein.

1. Erstellen Sie mit dem Segment Builder von Adobe Experience Platform die Regel entsprechend Ihren Anforderungen. Dazu können Sie verschiedene Datenquellen nutzen, z. B.:
   * Profilattribute;
   * Entscheidungselement-Attribute - nur beim Erstellen einer Regel **[!UICONTROL Entscheidungselement]** verfügbar;
   * Zielgruppen;
   * Kontextdaten aus Adobe Experience Platform. [Erfahren Sie, wie Sie Kontextdaten nutzen](context-data.md)

   ![](assets/decision-rules-build.png){width=85%}

   >[!NOTE]
   >
   >Der zum Erstellen von Regeln bereitgestellte Segment Builder weist einige Besonderheiten im Vergleich zum Segmentierungs-Service von Adobe Experience Platform auf. Der in der Dokumentation beschriebene globale Prozess gilt jedoch für das Erstellen von Regeln in [!DNL Journey Optimizer]. [Erfahren Sie, wie Sie Segmentdefinitionen erstellen](../audience/creating-a-segment-definition.md)

1. Während Sie neue Felder im Arbeitsbereich hinzufügen und konfigurieren, zeigt der Bereich **[!UICONTROL Zielgruppeneigenschaften]** Informationen zur geschätzten Anzahl der Profile an, die zur Zielgruppe gehören. Klicken Sie **[!UICONTROL Schätzung aktualisieren]**, um die Daten zu aktualisieren.

   ![](assets/decision-rule-audience-properties.png){width=85%}

   >[!NOTE]
   >
   >Profilschätzungen sind nicht verfügbar, wenn die Regelparameter Daten enthalten, die nicht im Profil gespeichert sind, z. B. Kontextdaten.

1. Sobald Ihre Regel fertig ist, klicken Sie auf **[!UICONTROL Erstellen]**. Die erstellte Regel wird in der Liste angezeigt und steht je nach der von Ihnen erstellten Entität zur Verwendung zur Verfügung:

   * in **Entscheidungspunkten** und **Auswahlstrategien** für die Präsentation von Entscheidungselementen für Profile;
   * Oder beim Erstellen von **Targeting** in der Inhaltsoptimierung oder Pfadoptimierung.

>[!NOTE]
>
>Die Verschachtelungstiefe in einer Regel ist auf 30 Ebenen begrenzt. Dies wird durch die Zählung der schließenden Klammern gemessen, die in der PQL-Zeichenfolge `)` sind.
>
>Eine Regelzeichenfolge kann für UTF-8-codierte Zeichen eine Größe von bis zu 15 KB haben. Dies entspricht 15.000 ASCII-Zeichen (je 1 Byte) oder 3.750-7.500 Nicht-ASCII-Zeichen (jeweils 2-4 Byte).
>
>[Erfahren Sie mehr über Eignungsregeln, Leitplanken und Einschränkungen](decisioning-guardrails.md#eligibility-rules)

## KI-gestützte Regeloptimierung {#optimize}

[!DNL Journey Optimizer] können automatisch Regeln analysieren und Vereinfachungen vorschlagen, die die ursprüngliche Logik beibehalten. Nur Regeln, deren PQL-Ausdruck größer als **2 KB** (UTF-8-kodiert) ist, sind zulässig. Kleinere Ausdrücke werden nicht analysiert. Wenn eine Vereinfachung gefunden wird, wird neben **[!UICONTROL Regel im Inventar ein roter]** Optimieren“ angezeigt.

>[!NOTE]
>
>Die KI-gestützte Regeloptimierung stützt sich auf dieselben generativen KI-Funktionen wie **KI-Assistent** und verwendet dieselben Zugriffssteuerungen. Benutzern muss für die Ressource **[!UICONTROL KI-Assistent]** die Berechtigung **[!UICONTROL Inhalt generieren]** gewährt werden. Weitere Informationen finden Sie unter [Zugriff auf KI-Assistent](../content-management/gs-generative.md#generative-access).

![](assets/decision-rules-ai.png)

So optimieren Sie eine Regel:

1. Klicken Sie im Regelinventar auf das rote Symbol neben dem Regelnamen.

1. Das Fenster **[!UICONTROL Optimieren]** wird geöffnet, in dem der ursprüngliche PQL-Ausdruck zusammen mit der von KI vorgeschlagenen Version angezeigt wird.

   ![](assets/decision-rules-ai-details.png)

1. Um zu überprüfen, ob sich beide Ausdrücke identisch verhalten, klicken Sie auf **[!UICONTROL Optimierungsanalyse herunterladen (TSV)]**, um eine Datei herunterzuladen, die zeigt, wie simulierte Profile für jede Version ausgewertet werden.

1. Wenn Sie zufrieden sind, klicken **[!UICONTROL auf]**, um den ursprünglichen Ausdruck durch den optimierten Ausdruck zu ersetzen.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie wiederverwendbare **Targeting-Regeln** in Adobe Journey Optimizer erstellen, duplizieren und anwenden, um Kampagnen effizient auf der Grundlage von Kundenattributen wie Region, Sprache und Verhalten zu personalisieren und so Zeit zu sparen und gleichzeitig die Genauigkeit der Zielgruppe zu verbessern.

>[!VIDEO](https://video.tv.adobe.com/v/3476136/?captions=ger&quality=12)
