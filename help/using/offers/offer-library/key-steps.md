---
title: Wichtige Schritte zum Erstellen eines Angebots
description: Machen Sie sich mit den wichtigsten Schritten für die Erstellung eines Angebots vertraut.
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 100%

---

# Wichtigste Schritte bei der Angebotserstellung und -verwaltung {#key-steps}

Nachfolgend werden die wichtigsten Schritte zum Erstellen, Konfigurieren und Verwalten von Angeboten sowie deren Verwendung in einer Entscheidung beschrieben.

![](../../assets/offer-create-manage-process.png)

Ein vollständiges Beispiel zur Konfiguration von Angeboten, zur Verwendung in einer Entscheidung und zur Nutzung dieser Entscheidung in einer E-Mail finden Sie auf [dieser Seite](../offers-e2e.md).

## Erstellen von Komponenten

Bevor Sie mit dem Erstellen von Angeboten beginnen, müssen Sie mehrere Komponenten definieren, die Sie in Ihren Angeboten verwenden wollen.

1. **Erstellen Sie Platzierungen**, die Container sind, mit denen Ihre Angebote präsentiert werden. Sie können z. B. eine Platzierung erstellen, die ausschließlich Angeboten im Bildformat gewidmet ist und sich oben in Ihren Nachrichten befindet.

1. **Erstellen Sie Entscheidungsregeln**, die die Bedingungen für die Präsentation der Angebote festlegen.

1. **Erstellen Sie Tags**, die Sie mit den Angeboten verknüpfen, damit Sie Angebote einfach organisieren und in der Bibliothek suchen können.

1. Wenn Sie Regeln definieren möchten, die bestimmen, welches Angebot für eine bestimmte Platzierung zuerst unterbreitet werden soll (anstatt die Prioritätswerte der Angebote zu berücksichtigen), können Sie **eine Rangfolgenformel** erstellen.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Platzierungen erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Entscheidungsregeln erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Tags erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">Rangfolgeformeln erstellen</a></p></td>
</table>

## Angebote erstellen und verwalten

1. **Erstellen Sie Angebote** und konfigurieren Sie deren Inhalt und Eigenschaften.

1. **Erstellen Sie Fallback-Angebote**, die angezeigt werden, wenn Kunden für keines der ausgewählten Angebote geeignet sind.

1. **Erstellen Sie eine Kollektion**, um die von Ihnen erstellten personalisierten Angebote zusammenzufassen und in einer Entscheidung zu verwenden.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Angebote erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Fallback-Angebote erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Kollektionen erstellen</a></p></td></tr>
</table>

## Entscheidungen erstellen und konfigurieren

1. **Erstellen Sie eine Entscheidung**, die Platzierungen mit den personalisierten Angeboten und den Fallback-Angeboten kombiniert. Diese Kombination wird vom Offer Decisioning-Modul verwendet, um das beste Angebot für ein bestimmtes Profil zu finden.

1. **Konfigurieren Sie die Entscheidung**. Wählen Sie dazu die Platzierungen aus und wählen Sie für jede Platzierung eine Sammlung und ein Fallback-Angebot aus.

1. Bei Bedarf können Sie einer Platzierung eine **Rangfolgenformel zuweisen**, wenn Sie eine Entscheidung konfigurieren.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Entscheidungen erstellen</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Entscheidungen konfigurieren</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Rangfolge zuweisen</a></p></td>
</tr>
</table>
