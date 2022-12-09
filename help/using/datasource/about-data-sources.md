---
solution: Journey Optimizer
product: journey optimizer
title: Über Datenquellen
description: Erfahren Sie, wie Sie eine Datenquelle konfigurieren
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Über Datenquellen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Über Datenquellen"
>abstract="Die Konfiguration der Datenquelle wird immer von einem technischen Anwender durchgeführt. Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, zum Beispiel: Bedingungsdefinition, Parameter- und Personalisierungsdaten in Aktionen, benutzerdefinierte Wartedefinition, Zeitzonendefinition."

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, zum Beispiel:

* [Definition von Bedingungen](../building-journeys/condition-activity.md)
* Parameter- und Personalisierungsdaten in [Aktionen](../action/action.md)
* [benutzerdefinierte Wartedefinition](../building-journeys/wait-activity.md#custom)
* [Zeitzonendefinition](../building-journeys/timezone-management.md)

➡️ [Funktion im Video kennenlernen](#video)

Diese Konfiguration ist nicht erforderlich, wenn Ihre Journeys nur lokale Daten aus einer Ereignis-Payload nutzen. Wenn Ihre Journey beispielsweise aus einem Ereignis gefolgt von einer Kanalaktionsaktivität besteht, die nur Daten aus dem Ereignis verwendet, müssen Sie keine Datenquelle konfigurieren.

Es gibt zwei Arten von Datenquellen:

* Die vorkonfigurierte Adobe Experience Platform-Datenquelle, die die Verbindung zum Echtzeit-Kundenprofildienst definiert. Dies ist eine integrierte Datenquelle. Siehe [diese Seite](../datasource/adobe-experience-platform-data-source.md).
* Die externen Datenquellen, mit denen Sie eine Verbindung zu externen Systemen definieren können. Diese können Sie erstellen. Siehe [diese Seite](../datasource/external-data-sources.md).

Für jede Datenquelle definieren Sie die Informationen, die mithilfe von Feldergruppen abgerufen werden sollen. Feldergruppen sind Gruppen von Feldern, die aus einer Datenquelle abgerufen werden können. Siehe [diese Seite](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Schemabeziehungen werden für Datenquellen nicht unterstützt.

Weitere Informationen zum Konfigurieren einer Adobe Experience Platform-Datenquelle und einer externen Datenquelle sowie zum Suchen und Verwenden von Daten in einer Journey finden Sie in diesem Abschnitt [Tutorial-Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target=&quot;_blank&quot;}.

## Anleitungsvideo {#video}

Erfahren Sie, was eine Datenquelle ist, und lernen Sie, wie Sie Experience Platform und externe Datenquellen konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

