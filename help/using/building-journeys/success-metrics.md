---
solution: Journey Optimizer
product: journey optimizer
title: Veröffentlichen der Journey
description: Erfahren Sie, wie Sie Berichte zu Ihrer ausgewählten Journey-Metrik erstellen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
hide: true
hidefromtoc: true
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: 48ef8d42057ffe51c27221c2176192d4e637fb96
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 12%

---

# Konfigurieren und Verfolgen der Journey-Metrik {#success-metrics}

Mit Journey-Metriken können Sie die Wirkung Ihrer Aktivitäten effektiv messen, indem Sie deren Performance anhand vordefinierter Metriken verfolgen.
Durch die Verfolgung dieser Metriken können Sie sehen, wie gut Ihr Journey funktioniert, Bereiche identifizieren, in denen Verbesserungen möglich sind, und fundierte Entscheidungen treffen, um die Kundeninteraktion zu verbessern.

## Voraussetzungen {#prerequisites}

Bevor Sie Ihre Journey-Metrik verwenden können, müssen Sie einen Datensatz hinzufügen, der die `Commerce Details`-, `Web`- und `Mobile`[Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} enthält.

## Verfügbare Metriken {#metrics}

Die Liste der Metriken variiert je nach den [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} die in Ihrem Datensatz enthalten sind.

Wenn Ihr Datensatz nicht konfiguriert ist, sind nur die folgenden Metriken verfügbar: **[!UICONTROL Click]**, **[!UICONTROL Unique Click]**, **[!UICONTROL Clickthrough Rate]** und **[!UICONTROL Open Rate]**.

Beachten Sie, dass Sie mit einer Customer Journey Analytics-Lizenz benutzerdefinierte Erfolgsmetriken erstellen können. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Metriken | Verwandte Feldergruppe |
|-|-|
| Klicks | Keine Feldergruppe erforderlich |
| Einzelklicks | Keine Feldergruppe erforderlich |
| Clickthrough-Rate (CTR) | Keine Feldergruppe erforderlich |
| Clickthrough-Öffnungsrate (CTOR) | Keine Feldergruppe erforderlich |
| Seitenansichten | Web-Feldergruppe |
| Mobile-App-Starts | Mobile-Feldergruppe |
| Erste Mobile-App-Starts | Mobile-Feldergruppe |
| Mobile-App-Installationen | Mobile-Feldergruppe |
| App-Upgrades | Mobile-Feldergruppe |
| Käufe | Commerce Details-Feldergruppe |
| Checkouts | Commerce Details-Feldergruppe |
| Hinzufügen zum Warenkorb | Commerce Details-Feldergruppe |
| Öffnung des Einkaufswagens | Commerce Details-Feldergruppe |
| Warenkorbansichten | Commerce Details-Feldergruppe |
| Entnahmen aus dem Einkaufswagen | Commerce Details-Feldergruppe |
| Produktansichten | Commerce Details-Feldergruppe |
| Für später speichern | Commerce Details-Feldergruppe |

## Attribution {#attribution}

Jede Metrik enthält einen Attributionssatz, der bestimmt, welche Touchpoints oder Interaktionen zu einem bestimmten Ergebnis beigetragen haben.

* **Metrikattribution mit Journey Optimizer-Lizenz**:

  Nur mit der Journey Optimizer-Lizenz ist das maximal verfügbare Lookback-Fenster für eine ausgewählte Metrik auf 7 Tage festgelegt. Für diese Metriken ist das Attributionsmodell standardmäßig auf &quot;**&quot; festgelegt** d. h. auf die letzte Interaktion vor der Konversion.

  Sie können beispielsweise verfolgen, ob ein Kauf getätigt wurde, nachdem ein Kunde innerhalb der letzten sieben Tage mit Ihrem Journey interagiert hat.

* **Metrikattribution mit Customer Journey Analytics-Lizenz**:

  Mit sowohl Journey Optimizer- als auch Customer Journey Analytics-Lizenzen können Sie benutzerdefinierte Metriken mit bestimmten Attributionseinstellungen erstellen oder die Zuordnungen der integrierten Metriken ändern.

  Weitere Informationen zu [Attributionsmodellen](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Zuweisen der Journey-Metrik {#assign}

Gehen Sie wie folgt vor, um mit dem Tracking Ihrer Journey-Metrik zu beginnen:

1. Klicken Sie im Menü **[!UICONTROL Journey]** auf **[!UICONTROL Journey erstellen]**.

1. Bearbeiten Sie den Konfigurationsbereich der Journey, um den Namen der Journey zu definieren und ihre Eigenschaften festzulegen. Informationen zum Festlegen der Eigenschaften Ihrer Journey finden Sie auf [dieser Seite](../building-journeys/journey-properties.md).

1. Wählen Sie Ihre **[!UICONTROL Journey-Metriken]** die zur Messung der Effektivität Ihres Journey verwendet werden.

   Beachten Sie, dass die Metriken für die Journey selbst gelten und für alle Elemente der Journey gelten.

   ![](assets/success_metric.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Entwerfen Sie Ihren Journey mit den erforderlichen **[!UICONTROL Aktivitäten]**.

1. Testen und Veröffentlichen des Journey.

1. Öffnen Sie den Journey-Bericht, um die Leistung der zugewiesenen Erfolgsmetrik zu verfolgen.

   Die ausgewählte Metrik wird in der Tabelle KPIs des Berichts und Journey-Statistiken angezeigt.

   ![](assets/success_metric_2.png)
