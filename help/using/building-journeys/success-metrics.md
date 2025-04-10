---
solution: Journey Optimizer
product: journey optimizer
title: Veröffentlichen der Journey
description: Erfahren Sie, wie Sie über Ihre gewählte Journey-Metrik berichten können.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: d28341dd39ec3ab838a5fbb3ae49539b8776c60b
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 96%

---

# Konfigurieren und Verfolgen der Journey-Metrik {#success-metrics}

Mit Journey-Metriken können Sie die Wirkung Ihrer Aktivitäten effektiv messen, indem Sie deren Leistung anhand vordefinierter Metriken verfolgen.
Durch Tracking dieser Metriken können Sie sehen, wie gut Ihre Journey funktioniert, Bereiche identifizieren, in denen Verbesserungen möglich sind, und fundierte Entscheidungen treffen, um die Kundeninteraktion zu optimieren.

## Voraussetzungen {#prerequisites}

Bevor Sie Ihre Journey-Metrik verwenden können, müssen Sie einen Datensatz mit den [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} `Commerce Details`, `Web` und `Mobile` hinzufügen.

## Verfügbare Metriken {#metrics}

Die Liste der Metriken variiert abhängig von den [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} in Ihrem Datensatz.

Wenn Ihr Datensatz nicht konfiguriert ist, sind nur die folgenden Metriken verfügbar: **[!UICONTROL Klick]**, **[!UICONTROL Einzelklick]**, **[!UICONTROL Klickrate]** und **[!UICONTROL Öffnungsrate]**.

Beachten Sie, dass Sie mit einer Customer Journey Analytics-Lizenz benutzerdefinierte Erfolgsmetriken erstellen können. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Metriken | Verwandte Feldergruppe |
|-|-|
| Klicks | Keine Feldergruppe erforderlich |
| Einzelklicks | Keine Feldergruppe erforderlich |
| Clickthrough-Rate (CTR) | Keine Feldergruppe erforderlich |
| Klick-Öffnungsrate (CTOR) | Keine Feldergruppe erforderlich |
| Seitenansichten | Web-Feldergruppe |
| Mobile-App-Starts | Mobile-Feldergruppe |
| Erste Mobile-App-Starts | Mobile-Feldergruppe |
| Mobile-App-Installationen | Mobile-Feldergruppe |
| App-Upgrades | Mobile-Feldergruppe |
| Käufe | Commerce-Details-Feldergruppe |
| Checkouts | Commerce-Details-Feldergruppe |
| Hinzufügungen zum Warenkorb | Commerce-Details-Feldergruppe |
| Öffnungen des Warenkorbs | Commerce-Details-Feldergruppe |
| Warenkorbansichten | Commerce-Details-Feldergruppe |
| Entnahmen aus Warenkorb | Commerce-Details-Feldergruppe |
| Produktansichten | Commerce-Details-Feldergruppe |
| Für später speichern | Commerce-Details-Feldergruppe |

## Attribution {#attribution}

Jede Metrik enthält eine festgelegte Attribution, die bestimmt, welche Touchpoints oder Interaktionen zu einem bestimmten Ergebnis beigetragen haben.

* **Metrikattribution mit Journey Optimizer-Lizenz**:

  Mit der Journey Optimizer-Lizenz allein ist das maximal verfügbare Lookback-Fenster für eine ausgewählte Metrik auf 7 Tage festgelegt. Für diese Metriken ist das Attributionsmodell standardmäßig auf **Letztkontakt** festgelegt, d. h. auf die letzte Interaktion vor der Konversion.

  Sie können beispielsweise verfolgen, ob ein Kauf getätigt wurde, nachdem eine Kundin oder ein Kunde innerhalb der letzten 7 Tage mit Ihrer Journey interagiert hat.

* **Metrikattribution mit Customer Journey Analytics-Lizenz**:

  Mit Journey Optimizer- und Customer Journey Analytics-Lizenz können Sie benutzerdefinierte Metriken mit bestimmten Attributionseinstellungen erstellen oder die Attributionen der integrierten Metriken ändern.

  Weitere Informationen zu [Attributionsmodellen](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Zuweisen der Journey-Metrik {#assign}

Gehen Sie wie unten beschrieben vor, um mit dem Tracking Ihrer Journey-Metrik zu beginnen:

1. Klicken Sie im Menü **[!UICONTROL Journeys]** auf **[!UICONTROL Journey erstellen]**.

1. Bearbeiten Sie den Konfigurationsbereich der Journey, um den Namen der Journey zu definieren und ihre Eigenschaften festzulegen. Erfahren Sie auf dieser Seite , wie Sie die Eigenschaften [ Journey festlegen](../building-journeys/journey-properties.md).

1. Wählen Sie die **[!UICONTROL Journey-Metriken]** zur Messung der Effektivität Ihrer Journey.

   Beachten Sie, dass die Metriken für die Journey selbst und für alle Elemente der Journey gelten.

   ![](assets/success_metric.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

1. Entwerfen Sie Ihre Journey mit den erforderlichen **[!UICONTROL Aktivitäten]**.

1. Testen und veröffentlichen Sie Ihre Journey.

1. Öffnen Sie den Journey-Bericht, um die Leistung der zugewiesenen Erfolgsmetrik zu verfolgen.

   Die gewählte Metrik wird in der Tabelle mit den KPIs und Journey-Statistiken des Berichts angezeigt.

   ![](assets/success_metric_2.png)
