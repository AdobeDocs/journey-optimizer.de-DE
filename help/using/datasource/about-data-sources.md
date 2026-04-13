---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Datenquellen
description: Erfahren Sie, wie Sie die ersten Schritte mit Datenquellen machen
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: Daten, Quelle, Journey, Plattform
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 8521e59022c221c0ca4e5b69b5b3aefe6304b417
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 54%

---

# Erste Schritte mit Datenquellen {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informationen zu Datenquellen"
>abstract="Die Konfiguration von Datenquellen wird immer von einem technischen Anwender durchgeführt. Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. Damit können Sie Bedingungen definieren, Parameter- und Personalisierungsdaten in Aktionen verwenden sowie benutzerdefinierte Wartezeiten und die Zeitzone definieren."

>[!TIP]
>Neu bei der Datenverwaltung in Journey Optimizer? Beginnen Sie mit der [Erste Schritte mit dem Daten-Management](../data/gs-data.md) Übersicht , um Schemata, Datensätze, Identitäten und die Art und Weise des Datenflusses zu verstehen, bevor Sie Datenquellen konfigurieren.

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, zum Beispiel für:

* [Definition von Bedingungen](../building-journeys/conditions.md)
* Parameter- und Personalisierungsdaten in [Aktionen](../action/action.md)
* [Definition benutzerdefinierter Wartezeiten](../building-journeys/wait-activity.md#custom)
* [Definition von Zeitzonen](../building-journeys/timezone-management.md)

➡️ [Funktion im Video kennenlernen](#video)

Diese Konfiguration ist nicht erforderlich, wenn Ihre Journeys nur lokale Daten von einer Ereignis-Payload nutzen. Wenn Ihre Journey beispielsweise aus einem Ereignis besteht, gefolgt von einer Kanalaktionsaktivität, die nur Daten aus dem Ereignis verwendet, müssen Sie keine Datenquelle konfigurieren.

Es gibt zwei Arten von Datenquellen:

* Die **vorkonfigurierte** Datenquelle von Adobe Experience Platform, die die Verbindung zum Echtzeit-Kundenprofildienst definiert. Dies ist eine integrierte Datenquelle. Weitere Informationen finden Sie auf [dieser Seite](../datasource/adobe-experience-platform-data-source.md).
* Die **externen** Datenquellen, mit denen Sie eine Verbindung zu externen Systemen definieren können. Diese können Sie erstellen. Weitere Informationen finden Sie auf [dieser Seite](../datasource/external-data-sources.md).

>[!NOTE]
>
>Da die Antworten jetzt unterstützt werden, sollten Sie für Anwendungsfälle mit externen Datenquellen benutzerdefinierte Aktionen anstelle von Datenquellen verwenden.  Weitere Informationen zu Antworten finden Sie in [diesem Abschnitt](../action/action-response.md).

Für jede Datenquelle definieren Sie die Informationen, die mit Feldergruppen abgerufen werden sollen. Feldergruppen sind Gruppen von Feldern, die aus einer Datenquelle abgerufen werden können. Weitere Informationen finden Sie auf [dieser Seite](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Datenquellen unterstützen keine Schemabeziehungen.

## Wählen Ihrer Datenzugriffsstrategie {#data-access-strategy}

Bevor Sie eine Datenquelle konfigurieren, überlegen Sie, welcher Ansatz Ihrem Anwendungsfall am besten entspricht. Es stehen drei Optionen zur Verfügung, die jeweils unterschiedliche Kompromisse hinsichtlich Persistenz, Profilanreicherung und Wiederverwendbarkeit aufweisen. Eine ausführliche Erläuterung dieser Optionen finden Sie unter [Best Practices für erweiterte Journey in Journey Optimizer](https://experienceleague.adobe.com/de/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Option 1 - Zugriff auf externe Daten über benutzerdefinierte Aktionen (kein Data Lake)**

Stellen Sie zur Journey-Laufzeit eine direkte Verbindung zu einer externen API her, ohne Daten im Data Lake von Experience Platform beizubehalten. Am besten geeignet, wenn:

* Die Daten sind nur innerhalb des Journey-Kontexts nützlich und anderswo nicht benötigt.
* Auf das externe System kann über einen API-Endpunkt zugegriffen werden, der die erforderlichen Attribute zurückgibt.

Erfahren Sie mehr über [benutzerdefinierte Aktionen](../action/action.md) und [benutzerdefinierte &#x200B;](../action/action-response.md).

**Option 2 — Datensatz im Data Lake, nicht für Profil aktiviert**

Nehmen Sie Daten in einen Datensatz auf, um Journey auf der Grundlage kontextueller Ereignisdaten Trigger zu erstellen und zu personalisieren, ohne zum Echtzeit-Kundenprofil beizutragen. Am besten geeignet, wenn:

* Datensätze enthalten ein Identitätsfeld, das für den Zugriff auf Profile verwendet werden kann, die bereits in Experience Platform gespeichert sind.
* Die Daten werden nicht für die Erstellung von Zielgruppen oder die Identitätszuordnung außerhalb von Journey Optimizer benötigt.

**Option 3 - Profil-aktivierter Datensatz im Data Lake**

Nehmen Sie Daten in einen [profilaktivierten Datensatz](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} auf, um Zielgruppen zu erstellen, Identitätsdiagramme anzureichern und Daten über mehrere Journey- und RT-CDP-Ziele hinweg zu nutzen. Am besten geeignet, wenn:

* Die Daten sind für Zielgruppendefinitionen nützlich, die in Kanälen außerhalb von Journey Optimizer verwendet werden.
* Die Daten enthalten mehrere Identitäten, die zu umfangreicheren, zusammengefügten Profilfragmenten beitragen.

| | Im Data Lake persistierte Daten | Datensatz für Profil aktiviert |
| --- | --- | --- |
| **Option 1** — Externe Daten über benutzerdefinierte Aktionen | Nein | Nein |
| **Option 2** — Datensatz nicht für Profil aktiviert | Ja | Nein |
| **Option 3** — Profil-aktivierter Datensatz | Ja | Ja |

Weitere Informationen zum Konfigurieren einer Adobe Experience Platform-Datenquelle und einer externen Datenquelle sowie zum Suchen und Verwenden von Daten in einer Journey finden Sie in diesem [Tutorial-Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=de){target="_blank"}.

## Anleitungsvideo {#video}

Erfahren Sie, was eine Datenquelle ist, und lernen Sie, wie Sie Experience Platform- und externe Datenquellen konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

