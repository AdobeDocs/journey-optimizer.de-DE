---
title: Wichtige Schritte zum Erstellen eines Angebots
description: Machen Sie sich mit den wichtigsten Schritten für die Erstellung eines Angebots vertraut
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 100%

---

# Wichtigste Schritte bei der Angebotserstellung und -verwaltung {#key-steps-to-manage-offers}

Nachfolgend werden die wichtigsten Schritte zum Erstellen, Konfigurieren und Verwalten von Angeboten sowie deren Verwendung in einer Entscheidung beschrieben.

![](../assets/offer-create-manage-process.png)

Ein vollständiges Beispiel zur Konfiguration von Angeboten, zur Verwendung in einer Entscheidung und zur Nutzung dieser Entscheidung in einer E-Mail finden Sie auf [dieser Seite](../offers-e2e.md).

## Erstellen von Komponenten {#create-components}

Bevor Sie mit dem Erstellen von Angeboten beginnen, müssen Sie mehrere Komponenten definieren, die Sie in Ihren Angeboten verwenden wollen.

1. **Erstellen Sie Platzierungen**, die Container sind, mit denen Ihre Angebote präsentiert werden. Sie können z. B. eine Platzierung erstellen, die ausschließlich Angeboten im Bildformat gewidmet ist und sich oben in Ihren Nachrichten befindet.

1. **Erstellen Sie Entscheidungsregeln**, die die Bedingungen für die Präsentation der Angebote festlegen.

1. **Erstellen Sie Sammlungsqualifizierer** (ehemals als „Tags“ bezeichnet), die Sie mit den Angeboten verknüpfen, damit Sie Angebote einfach organisieren und in der Bibliothek suchen können.

1. Wenn Sie Regeln definieren möchten, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst unterbreitet werden soll (anstatt die Prioritätswerte der Angebote zu berücksichtigen), können Sie **eine Ranglisteformel erstellen**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Platzierungen erstellen</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Entscheidungsregeln erstellen</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Tags erstellen</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Ranglisteformeln erstellen</a>
</div>
<p>
</td>
</tr>
</table>

## Angebote erstellen und verwalten {#create-and-manage-offers}

1. **Erstellen Sie Angebote** und konfigurieren Sie deren Inhalt und Eigenschaften.

1. **Erstellen Sie Fallback-Angebote**, die angezeigt werden, wenn Kunden für keines der ausgewählten Angebote geeignet sind.

1. **Erstellen Sie eine Sammlung**, um die von Ihnen erstellten personalisierten Angebote zusammenzufassen und in einer Entscheidung zu verwenden.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Erstellen von Angeboten</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Erstellen von Fallback-Angeboten</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Erstellen von Sammlungen</a>
</div>
<p>
</td>
</tr>
</table>

## Entscheidungen erstellen und konfigurieren {#create-and-configure-decisions}

1. **Erstellen Sie eine Entscheidung**, die Platzierungen mit den personalisierten Angeboten und den Fallback-Angeboten kombiniert. Diese Kombination wird von der Offer Decisioning-Engine verwendet, um das beste Angebot für ein bestimmtes Profil zu finden.

1. **Konfigurieren Sie die Entscheidung**. Wählen Sie dazu die Platzierungen aus und wählen Sie für jede Platzierung eine Sammlung und ein Fallback-Angebot aus.

1. Bei Bedarf können Sie einer Platzierung eine **Rangfolgenformel zuweisen**, wenn Sie eine Entscheidung konfigurieren.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Erstellen von Entscheidungen</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Konfigurieren von Entscheidungen</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Zuweisen einer Rangfolge</a>
</div>
<p>
</td>
</tr>
</table>
