---
title: Informationen zu Datenquellen
description: Erfahren Sie, wie Sie eine Datenquelle konfigurieren
feature: Datenquellen
topic: Administration.
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 87%

---

# Informationen zu Datenquellen {#concept_s1s_dqt_52b}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="Informationen zu Datenquellen"
>abstract="Die Konfiguration von Datenquellen wird immer von einem technischen Anwender durchgeführt. Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. Damit können Sie Bedingungen definieren, Parameter- und Personalisierungsdaten in Aktionen verwenden sowie benutzerdefinierte Wartezeiten und die Zeitzone definieren."

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, zum Beispiel für:

* [Definition von Bedingungen](../building-journeys/condition-activity.md)
* Parameter- und Personalisierungsdaten in [Aktionen](../action/action.md)
* [Definition benutzerdefinierter Wartezeiten](../building-journeys/wait-activity.md#custom)
* [Definition von Zeitzonen](../building-journeys/timezone-management.md)

Diese Konfiguration ist nicht erforderlich, wenn Ihre Journeys nur lokale Daten aus einer Ereignis-Payload nutzen. Wenn Ihre Journey beispielsweise aus einem Ereignis und einer E-Mail-Aktivität besteht, die nur Daten aus dem Ereignis verwendet, müssen Sie keine Datenquelle konfigurieren.

Es gibt zwei Arten von Datenquellen:

* Die vorkonfigurierte Datenquelle von Adobe Experience Platform, die die Verbindung zum Echtzeit-Kundenprofildienst definiert. Dies ist eine integrierte Datenquelle. Weitere Informationen finden Sie auf [dieser Seite](../datasource/adobe-experience-platform-data-source.md).
* Die externen Datenquellen, mit denen Sie eine Verbindung zu externen Systemen definieren können. Diese können Sie erstellen. Weitere Informationen finden Sie auf [dieser Seite](../datasource/external-data-sources.md).

Für jede Datenquelle definieren Sie die Informationen, die mit Feldergruppen abgerufen werden sollen. Feldergruppen sind Gruppen von Feldern, die aus einer Datenquelle abgerufen werden können. Weitere Informationen finden Sie auf [dieser Seite](../datasource/configure-data-sources.md#define-field-groups).

Weitere Informationen zum Konfigurieren einer Adobe Experience Platform-Datenquelle und einer externen Datenquelle sowie zum Suchen und Verwenden von Daten in einer Journey finden Sie in diesem [Tutorial-Video](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html?lang=de){target=&quot;_blank&quot;}.
