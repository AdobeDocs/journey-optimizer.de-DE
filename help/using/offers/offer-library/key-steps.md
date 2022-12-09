---
title: Wichtige Schritte zum Erstellen eines Angebots
description: Wichtige Schritte zum Erstellen eines Angebots
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Wichtige Schritte zum Erstellen und Verwalten von Angeboten {#key-steps-to-manage-offers}

Die wichtigsten Schritte zum Erstellen, Konfigurieren und Verwalten von Angeboten sowie deren Verwendung in einer Entscheidung werden nachfolgend beschrieben.

![](../assets/offer-create-manage-process.png)

Ein vollständiges Beispiel, das die Konfiguration von Angeboten veranschaulicht, sie in einer Entscheidung verwendet und diese Entscheidung in einer E-Mail nutzt, finden Sie unter [diese Seite](../offers-e2e.md).

## Erstellen von Komponenten {#create-components}

Bevor Sie mit der Erstellung von Angeboten beginnen, müssen Sie mehrere Komponenten definieren, die Sie in Ihren Angeboten verwenden werden.

1. **Platzierungen erstellen**: Container, die zur Präsentation Ihrer Angebote verwendet werden. Sie können beispielsweise eine Platzierung erstellen, die ausschließlich Angeboten im Bildformat gewidmet ist und sich oben in Ihren Nachrichten befindet.

1. **Entscheidungsregeln erstellen** , der die Bedingungen für die Unterbreitung der Angebote festlegt.

1. **Tags erstellen** die Sie mit den Angeboten verknüpfen, sodass Sie sie einfach organisieren und in der Bibliothek durchsuchen können.

1. Wenn Sie Regeln definieren möchten, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst unterbreitet werden soll (anstatt die Prioritätswerte der Angebote zu berücksichtigen), können Sie **eine Rangformel erstellen**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Platzierungen erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Entscheidungsregeln erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Tags erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">Erstellen von Ranking-Formeln</a></p></td>
</table>

## Angebote erstellen und verwalten {#create-and-manage-offers}

1. **Angebote erstellen** und konfigurieren Sie ihren Inhalt und ihre Eigenschaften.

1. **Fallback-Angebote erstellen**: Angebote, die nur als letztes Mittel angezeigt werden, wenn Kunden für keines der ausgewählten Angebote geeignet sind.

1. **Kollektion erstellen** , um die von Ihnen erstellten personalisierten Angebote einzubeziehen und sie bei einer Entscheidung zu verwenden.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Angebote erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Fallback-Angebote erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Kollektionen erstellen</a></p></td></tr>
</table>

## Entscheidungen erstellen und konfigurieren {#create-and-configure-decisions}

1. **Entscheidung erstellen** , das Platzierungen mit den personalisierten Angeboten und den Fallback-Angeboten kombiniert. Diese Kombination wird von der Decisioning-Engine verwendet, um das beste Angebot für ein bestimmtes Profil zu finden.

1. **Entscheidung konfigurieren**. Wählen Sie dazu die Platzierungen aus und wählen Sie für jede Platzierung eine Sammlung und einen Fallback aus.

1. Bei Bedarf können Sie **eine Rangformel zuweisen** an eine Platzierung beim Konfigurieren der Entscheidung.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Entscheidungen erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Entscheidungen konfigurieren</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Rangzuweisung</a></p></td>
</tr>
</table>
