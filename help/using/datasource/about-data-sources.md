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
TQID: https://experienceleague.adobe.com/eG1QcfpHtxpabUt5e7RZiMIpSAJD6Z6bjO-4wtZEUOg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: dd51b532-b93f-4bcf-8dbf-0d007f593acaid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e366af78935405cd5acb15269194875098b20914
workflow-type: tm+mt
source-wordcount: 948
ht-degree: 42%

---

# Erste Schritte mit Datenquellen {#about-data-sources}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, was Datenquellen sind und wie Sie die richtige Datenzugriffsstrategie auswählen, damit Sie zusätzliche Daten zu Bedingungen, Personalisierung und Timing in Ihre Journey importieren können.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="Informationen zu Datenquellen"
>abstract="Die Konfiguration von Datenquellen wird immer von einem technischen Anwender durchgeführt. Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. Damit können Sie Bedingungen definieren, Parameter- und Personalisierungsdaten in Aktionen verwenden sowie benutzerdefinierte Wartezeiten und die Zeitzone definieren."

>[!TIP]
>Sie haben noch keine Erfahrungen mit dem Daten-Management in Journey Optimizer? Beginnen Sie mit der [Erste Schritte mit dem Daten-Management](../data/gs-data.md) Übersicht , um Schemata, Datensätze, Identitäten und die Art und Weise des Datenflusses zu verstehen, bevor Sie Datenquellen konfigurieren.

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
>Da die Antworten jetzt unterstützt werden, sollten Sie für Anwendungsfälle mit externen Datenquellen benutzerdefinierte Aktionen anstelle von Datenquellen verwenden. Weitere Informationen zu Antworten finden Sie in [diesem Abschnitt](../action/action-response.md).

Für jede Datenquelle definieren Sie die Informationen, die mit Feldergruppen abgerufen werden sollen. Feldergruppen sind Gruppen von Feldern, die aus einer Datenquelle abgerufen werden können. Weitere Informationen finden Sie auf [dieser Seite](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Datenquellen unterstützen keine Schemabeziehungen.

## Wählen Ihrer Datenzugriffsstrategie {#data-access-strategy}

Bevor Sie eine Datenquelle konfigurieren, überlegen Sie, welcher Ansatz Ihrem Anwendungsfall am besten entspricht. Es stehen drei Optionen zur Verfügung, die jeweils unterschiedliche Kompromisse hinsichtlich Persistenz, Profilanreicherung und Wiederverwendbarkeit aufweisen. Eine ausführliche Erläuterung dieser Optionen finden Sie unter [Best Practices für erweiterte Journey in Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Option 1 - Zugriff auf externe Daten über benutzerdefinierte Aktionen (kein Data Lake)**

Stellen Sie zur Journey-Laufzeit eine direkte Verbindung zu einer externen API her, ohne Daten im Data Lake von Experience Platform beizubehalten. Am besten geeignet, wenn:

* Die Daten sind nur innerhalb des Journey-Kontexts nützlich und anderswo nicht benötigt.
* Auf das externe System kann über einen API-Endpunkt zugegriffen werden, der die erforderlichen Attribute zurückgibt.

Erfahren Sie mehr über [benutzerdefinierte Aktionen](../action/action.md) und [benutzerdefinierte ](../action/action-response.md).

>[!TIP]
>
>Diese Option eignet sich gut, wenn Sie **beiden Fragen** ja“ beantworten:
>* Sind die Daten nur innerhalb des Journey-Kontexts nützlich und werden sie an anderer Stelle nicht benötigt? Wenn die Daten auch für Zielgruppen oder andere Kanäle benötigt werden, ziehen Sie die Optionen 2 oder 3 in Betracht.
>* Ist der Zugriff auf das externe System über einen API-Endpunkt möglich, der die erforderlichen Attribute zurückgibt? Andernfalls müssen Sie die Daten zuerst in den Data Lake aufnehmen.

**Option 2 — Datensatz im Data Lake, nicht für Profil aktiviert**

Nehmen Sie Daten in einen Datensatz auf, um Journey auf der Grundlage kontextueller Ereignisdaten Trigger zu erstellen und zu personalisieren, ohne zum Echtzeit-Kundenprofil beizutragen. Am besten geeignet, wenn:

* Datensätze enthalten ein Identitätsfeld, das für den Zugriff auf Profile verwendet werden kann, die bereits in Experience Platform gespeichert sind.
* Die Daten werden nicht für die Erstellung von Zielgruppen oder die Identitätszuordnung außerhalb von Journey Optimizer benötigt.

>[!TIP]
>
>Diese Option eignet sich gut, wenn Sie **beiden Fragen** ja“ beantworten:
>* Enthalten Datensätze ein Identitätsfeld, das für den Zugriff auf Profile verwendet werden kann, die bereits in Experience Platform gespeichert sind? Andernfalls können Journey nicht auf Profile zugreifen und sie nicht an sie senden.
>* Werden die Daten NICHT für die Erstellung [ Zielgruppe oder ](../audience/about-audiences.md) Identitätszuordnung außerhalb von Journey Optimizer benötigt? Ist dies der Fall, verwenden Sie stattdessen Option 3.

**Option 3 - Profil-aktivierter Datensatz im Data Lake**

Nehmen Sie Daten in einen [profilaktivierten Datensatz](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} auf, um Zielgruppen zu erstellen, Identitätsdiagramme anzureichern und Daten über mehrere Journey- und RT-CDP-Ziele hinweg zu nutzen. Am besten geeignet, wenn:

* Die Daten sind für Zielgruppendefinitionen nützlich, die in Kanälen außerhalb von Journey Optimizer verwendet werden.
* Die Daten enthalten mehrere Identitäten, die zu umfangreicheren, zusammengefügten Profilfragmenten beitragen.

>[!CAUTION]
>
>**Bevor Sie einen Datensatz für Profil aktivieren** sollten Sie die folgenden Bereiche bewerten:
>* **Datensynchronisation** - Externe Datenbanken müssen mit Warnhinweisen synchronisiert werden, um Aufnahmefehler zu identifizieren.
>* **[Profil-](https://experienceleague.adobe.com/de/docs/experience-platform/profile/guardrails){target="_blank"}**: Profilspezifische Leitplanken gelten zusätzlich zu den &quot;[ Leitplanken für die Datenaufnahme](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/guardrails){target="_blank"} für Experience Platform.
>* **Identitätsintegrität** - Identitätsdaten in Ihren Quellsystemen müssen sorgfältig geplant werden, um gesunde Identitätsdiagramme zu erhalten.
>* **Data Lake-Nutzung** - Der gesamte Speicherverbrauch, Tabellenbeziehungen und adressierbare Profile müssen vor der Aufnahme bewertet werden.

| | Im Data Lake persistierte Daten | Datensatz für Profil aktiviert |
| --- | --- | --- |
| **Option 1** — Externe Daten über benutzerdefinierte Aktionen | Nein | Nein |
| **Option 2** — Datensatz nicht für Profil aktiviert | Ja | Nein |
| **Option 3** — Profil-aktivierter Datensatz | Ja | Ja |

Weitere Informationen zum Konfigurieren einer Adobe Experience Platform-Datenquelle und einer externen Datenquelle sowie zum Suchen und Verwenden von Daten in einer Journey finden Sie in diesem [Tutorial-Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=de){target="_blank"}.

## Anleitungsvideo {#video}

Erfahren Sie, was eine Datenquelle ist, und lernen Sie, wie Sie Experience Platform- und externe Datenquellen konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

