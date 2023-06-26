---
solution: Journey Optimizer
product: journey optimizer
title: Informationen zu Datenquellen
description: Erfahren Sie, wie Sie eine Datenquelle konfigurieren
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: Daten, Quelle, Journey, Plattform
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Informationen zu Datenquellen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informationen zu Datenquellen"
>abstract="Die Konfiguration von Datenquellen wird immer von einem technischen Anwender durchgeführt. Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. Damit können Sie Bedingungen definieren, Parameter- und Personalisierungsdaten in Aktionen verwenden sowie benutzerdefinierte Wartezeiten und die Zeitzone definieren."

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, zum Beispiel für:

* [Definition von Bedingungen](../building-journeys/condition-activity.md)
* Parameter- und Personalisierungsdaten in [Aktionen](../action/action.md)
* [Definition benutzerdefinierter Wartezeiten](../building-journeys/wait-activity.md#custom)
* [Definition von Zeitzonen](../building-journeys/timezone-management.md)

➡️ [Entdecken Sie diese Funktion im Video](#video)

Diese Konfiguration ist nicht erforderlich, wenn Ihre Journeys nur lokale Daten von einer Ereignis-Payload nutzen. Wenn Ihre Journey beispielsweise aus einem Ereignis besteht, gefolgt von einer Kanalaktionsaktivität, die nur Daten aus dem Ereignis verwendet, müssen Sie keine Datenquelle konfigurieren.

Es gibt zwei Arten von Datenquellen:

* Die vorkonfigurierte Datenquelle von Adobe Experience Platform, die die Verbindung zum Echtzeit-Kundenprofildienst definiert. Dies ist eine integrierte Datenquelle. Weitere Informationen finden Sie auf [dieser Seite](../datasource/adobe-experience-platform-data-source.md).
* Die externen Datenquellen, mit denen Sie eine Verbindung zu externen Systemen definieren können. Diese können Sie erstellen. Weitere Informationen finden Sie auf [dieser Seite](../datasource/external-data-sources.md).

Für jede Datenquelle definieren Sie die Informationen, die mit Feldergruppen abgerufen werden sollen. Feldergruppen sind Gruppen von Feldern, die aus einer Datenquelle abgerufen werden können. Weitere Informationen finden Sie auf [dieser Seite](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Datenquellen unterstützen keine Schemabeziehungen.

Weitere Informationen zum Konfigurieren einer Adobe Experience Platform-Datenquelle und einer externen Datenquelle sowie zum Suchen und Verwenden von Daten in einer Journey finden Sie in diesem [Tutorial-Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=de){target="_blank"}.

## Anleitungsvideo {#video}

Erfahren Sie, was eine Datenquelle ist, und lernen Sie, wie Sie Experience Platform- und externe Datenquellen konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

