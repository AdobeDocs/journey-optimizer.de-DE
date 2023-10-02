---
title: Entscheidungsregeln
description: Erfahren Sie, wie Sie mit Entscheidungsregeln arbeiten.
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 7437268e87cc2c71bec394fbef1b512b31946cf5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 8%

---

# Entscheidungsregeln {#rules}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)
* Verwalten von Entscheidungselementen
   * [Konfigurieren des Elementkatalogs](catalogs.md)
   * [Erstellen von Entscheidungselementen](items.md)
   * [Verwalten von Elementsammlungen](collections.md)
* Elementauswahl konfigurieren
   * **[Entscheidungsregeln erstellen](rules.md)**
   * [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Entscheidungsrichtlinien erstellen](create-decision.md)

>[!ENDSHADEBOX]

Entscheidungsregeln ermöglichen es Ihnen, die Zielgruppe für Entscheidungselemente zu definieren, indem Sie Einschränkungen anwenden, entweder direkt auf der Entscheidungselementebene oder innerhalb einer bestimmten Auswahlstrategie. Dadurch können Sie genau steuern, welche Artikel wem präsentiert werden sollen.

Nehmen wir beispielsweise ein Szenario, in dem Sie Entscheidungselemente mit Yoga-bezogenen Produkten für Frauen haben. Mit Entscheidungsregeln können Sie festlegen, dass diese Elemente nur für Profile angezeigt werden sollen, deren Geschlecht &quot;weiblich&quot;ist und die in &quot;Yoga&quot;einen &quot;Zielpunkt&quot;angegeben haben.

Zusätzlich zu den Entscheidungsregeln auf Element- und Auswahlstrategieebene können Sie auch zusätzliche Parameter für Ihre gewünschte Zielgruppe auf Kampagnenebene erstellen. [Weitere Informationen](../campaigns/create-campaign.md)

Die Liste der Entscheidungsregeln ist im **[!UICONTROL Konfiguration]** / **[!UICONTROL Entscheidungsregeln]** Menü.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Vorerst werden Entscheidungsregeln mithilfe von Journey Optimizer verwaltet. **Entscheidungsmanagement** Menü. Daher wird die Variable **[!UICONTROL Entscheidungsregeln]** Liste in Experience Decisioning umfasst Regeln, die aus beiden Journey Optimizer erstellt wurden **[!UICONTROL Entscheidungsverwaltung]** oder **[!UICONTROL Erlebnisentscheidungen]** Menüs.

Gehen Sie wie folgt vor, um eine Sammlung zu erstellen:

1. Navigieren Sie zu **[!UICONTROL Konfiguration]** / **[!UICONTROL Entscheidungsregeln]**.
1. Die Benutzeroberfläche für die Entscheidungsverwaltung von Journey Optimizer wird im zentralen Bereich angezeigt. Führen Sie die im Abschnitt [Dokumentation zur Entscheidungsverwaltung](../offers/offer-library/creating-decision-rules.md) um Ihre Regel auf Grundlage Ihrer Anforderungen zu erstellen.

1. Nachdem die Regel erstellt wurde, wird sie in der Liste angezeigt und steht zur Verwendung in Entscheidungselementen und Auswahlstrategien zur Verfügung, um die Präsentation von Entscheidungselementen zu Profilen zu steuern.
