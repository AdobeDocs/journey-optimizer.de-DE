---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Wichtige Schritte zum Erstellen eines Angebots
description: Machen Sie sich mit den wichtigsten Schritten für die Erstellung eines Angebots vertraut
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/26dKfdb1fhdF0bGpilYam-2bzuJZPjFYGeKy3ni0dzE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 95%

---

# Wichtigste Schritte bei der Angebotserstellung und -verwaltung {#key-steps-to-manage-offers}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Nachfolgend werden die wichtigsten Schritte zum Erstellen, Konfigurieren und Verwalten von Angeboten sowie deren Verwendung in einer Entscheidung beschrieben.

![](../assets/offer-create-manage-process.png)

Ein vollständiges Beispiel zur Konfiguration von Angeboten, zur Verwendung in einer Entscheidung und zur Nutzung dieser Entscheidung in einer E-Mail finden Sie auf [dieser Seite](../offers-e2e.md).

## Erstellen von Komponenten {#create-components}

Bevor Sie mit dem Erstellen von Angeboten beginnen, müssen Sie mehrere Komponenten definieren, die Sie in Ihren Angeboten verwenden wollen.

1. [Erstellen Sie Platzierungen](creating-placements.md), die Container sind, mit denen Ihre Angebote präsentiert werden. Sie können z. B. eine Platzierung erstellen, die ausschließlich Angeboten im Bildformat gewidmet ist und sich oben in Ihren Nachrichten befindet.

1. [Erstellen Sie Entscheidungsregeln](creating-decision-rules.md), die die Bedingungen für die Präsentation der Angebote festlegen.

1. [Erstellen Sie Sammlungsqualifizierer](creating-tags.md) (ehemals als „Tags“ bezeichnet), die Sie mit den Angeboten verknüpfen, damit Sie Angebote einfach organisieren und in der Bibliothek suchen können.

1. Wenn Sie Regeln definieren möchten, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst unterbreitet werden soll (anstatt die Prioritätswerte der Angebote zu berücksichtigen), können Sie [eine Ranglisteformel erstellen](../ranking/create-ranking-formulas.md).

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Angebote erstellen und verwalten {#create-and-manage-offers}

1. [Erstellen Sie Angebote](creating-personalized-offers.md) und konfigurieren Sie deren Inhalt und Eigenschaften. Beim Personalisieren von Angebotsinhalten (Darstellungen) werden nur bestimmte Funktionen unterstützt - siehe [Unterstützte Funktionen im Personalisierungseditor](personalization-editor-supported-functions.md).

1. [Erstellen Sie Fallback-Angebote](creating-fallback-offers.md), die angezeigt werden, wenn Kunden für keines der ausgewählten Angebote geeignet sind.

1. [Erstellen Sie eine Sammlung](creating-collections.md), um die von Ihnen erstellten personalisierten Angebote zusammenzufassen und in einer Entscheidung zu verwenden.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Entscheidungen erstellen und konfigurieren {#create-and-configure-decisions}

1. [Erstellen Sie eine Entscheidung](../offer-activities/create-offer-activities.md), die Platzierungen mit den personalisierten Angeboten und den Fallback-Angeboten kombiniert. Diese Kombination wird von der Offer Decisioning-Engine verwendet, um das beste Angebot für ein bestimmtes Profil zu finden.

1. [Konfigurieren Sie die Entscheidung](../offer-activities/create-offer-activities.md#add-decision-scopes). Wählen Sie dazu die Platzierungen aus und wählen Sie für jede Platzierung eine Sammlung und ein Fallback-Angebot aus.

1. Bei Bedarf können Sie einer Platzierung eine [Rangfolgenformel](../offer-activities/configure-offer-selection.md#assign-ranking-formula) oder eine [KI-Rangfolge](../offer-activities/configure-offer-selection.md#use-ranking-strategy) zuweisen, wenn Sie eine Entscheidung konfigurieren.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->