---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten-Management in Journey Optimizer
description: Erfahren Sie, wie Daten in und aus Adobe Journey Optimizer fließen, einschließlich Schlüsselkonzepte, Einrichtungsschritte und Leitlinien.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
subfeature_v2:
  - id: a1cdc218-59b7-4eef-b5cf-2a7ad74b3371
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf3fbcd7-c075-4ae4-8de5-96e736ab2ea3
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4cb75d06f45f9d15cdbeda5afa06acf8e27d13de
workflow-type: tm+mt
source-wordcount: 2652
ht-degree: 98%

---

# Erste Schritte mit Daten-Management {#about-data}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Verschaffen Sie sich einen praktischen Überblick darüber, wie Daten in und aus Adobe Journey Optimizer fließen und Schemata, Datensätze, Identitäten, Profile und Datenquellen abdecken. So kann Ihr Team die Schritte zur Datenbereitschaft abschließen, bevor Sie Journey und Kampagnen erstellen.

>[!ENDSHADEBOX]

Daten sind die Grundlage für jede Journey, Entscheidung und Nachricht, die Sie mit [!DNL Adobe Journey Optimizer] versenden.

Auf dieser Seite erhalten Sie einen praktischen Ausgangspunkt, um mehr zu folgenden Themen zu erfahren:

* Die von Journey Optimizer verwendeten grundlegenden Datenbausteine (Schemata, Datensätze, Identitäten, Profile)
* Wie Journey Optimizer Adobe Experience Platform-Daten verwendet
* Welche Dateneinrichtungsschritte Ihr Team durchlaufen muss, bevor Journeys und Kampagnen erstellt werden können
* Wo Sie weitere Informationen zu detaillierter Konfiguration und Best Practices finden

Verwenden Sie dieses Handbuch zusammen mit Ihren Datentechnik-, Administrations- und Marketing-Teams, damit alle ein gemeinsames Verständnis davon haben, wie Daten in Journey Optimizer ein- und ausfließen.

>[!TIP]
>Sie haben noch keine Erfahrungen mit dem Daten-Management in Journey Optimizer? Sehen Sie sich das [Überblick-Tutorial zum Einrichten von Daten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} an, um eine praktische, anfängerfreundliche Anleitung zu Schemata, Datensätzen und Quellen zu erhalten.

## Wie Journey Optimizer Adobe Experience Platform-Daten verwendet {#aep-data}

[!DNL Adobe Journey Optimizer] basiert auf [!DNL Adobe Experience Platform]. Es verfügt über keinen separaten, isolierten Datenspeicher. Stattdessen wird dieselbe Datengrundlage wie bei anderen Experience Cloud-Anwendungen verwendet.

Schemata und Datensätze werden in Adobe Experience Platform gespeichert. Identitäten und das [Echtzeit-Kundenprofil](../audience/get-started-profiles.md) werden von Identity Service und Profil-Service verwaltet. Journey Optimizer liest Profil- und Ereignisdaten aus Adobe Experience Platform, um Journey-Bedingungen auszuwerten, Nachrichten zu personalisieren und Angebote auszuwählen. Interaktionsdaten wie Versand-, Öffnungs-, Klick- und Bounce-Ereignisse sowie Journey-Schrittereignisse werden zurück in Experience Platform-Datensätze geschrieben. Es können auch zusätzliche Datensätze zur Laufzeit nachgeschlagen werden, ohne diese Daten in das Profil zu kopieren.

>[!TIP]
>Stellen Sie sich Adobe Experience Platform als zentrale Datenschicht und Journey Optimizer als eine Anwendung vor, die Journeys und Nachrichten mithilfe dieser gemeinsamen Datengrundlage orchestriert.

➡️ [Weitere Informationen zur Architektur von Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Wichtige Datenkonzepte in Journey Optimizer {#key-concepts}

Beim Arbeiten mit Daten in Journey Optimizer werden Sie auf verschiedene verwandte Konzepte stoßen. Die nachstehende Tabelle bietet einen schnellen Überblick. In den folgenden Abschnitten werden die einzelnen Konzepte detaillierter erläutert.

| Konzept | Was es ist | Primäre Verwendung in Journey Optimizer |
|---|---|---|
| XDM-Schema | Regeln, die Ihre Daten darstellen, validieren und formatieren (basierend auf einer Klasse und Feldergruppen) | Profilattribute und Verhaltensereignisse modellieren |
| Datensatz | Speichertabelle für schemakonforme Daten | Profil-, ereignis- und systemgenerierte Daten speichern |
| Quell-Connector | Streamt oder vereinigt Daten zu Batches aus externen Systemen nach AEP | Aufnehmen von CRM-, Analyse- und Web-Daten |
| Datenquelle | Macht AEP- oder externe Felder in Journey verfügbar | Journey-Bedingungen und Nachrichtenpersonalisierung ermöglichen |
| Identität | Kennung, die eine einzelne Person eindeutig repräsentiert | Profile kanalübergreifend zuordnen |
| Lookup-Datensatz | Laufzeitreferenz zu AEP-Daten ohne Profilspeicher | Nachrichten mit Live-Referenzdaten anreichern |

### Schema (XDM-Schema) {#schema}

Ein Schema ist ein Regelsatz, der Ihre Daten darstellt, validiert und formatiert. Es besteht aus einer **Klasse** (die das Basisverhalten definiert: Eintrag oder Zeitreihen) und optionalen **Feldergruppen** (die bestimmte Felder hinzufügen). Schemata werden mithilfe von Experience-Datenmodell-Standards (XDM) definiert und werden in Adobe Experience Platform gespeichert.

XDM dient der Lösung eines echten Problems: Dasselbe Konzept – eine Person, ein Kauf, ein Produkt – wird in den Quellsystemen unterschiedlich benannt und strukturiert. XDM bietet eine gemeinsame Sprache, die diese Konzepte unabhängig vom Ursprung der Daten unter einer einzigen Definition zusammenfasst. Dadurch kann Journey Optimizer konsistent mit Daten aus Ihrem CRM, Ihrer Website, Ihrer App und Ihrem Data Warehouse gleichzeitig arbeiten.

In Journey Optimizer arbeiten Sie normalerweise mit Schemata des Typs **XDM-Profil für Einzelpersonen** für Kundenattribute (Name, Voreinstellungen, Einverständnis) und Schemata des Typs **XDM-ExperienceEvent** für Verhaltensereignisse (Käufe, Seitenansichten, Anmeldungen).

➡️ [Weitere Informationen über Schemata](get-started-schemas.md)

### Datensatz {#dataset}

Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, das einem Schema entspricht. Stellen Sie sich ihn als Tabelle mit einem definierten Satz von Spalten und Zeilen vor. Alle von Journey Optimizer verwendeten Daten werden in Adobe Experience Platform-Datensätzen gespeichert. Dabei kann es sich um Profildatensätze (die zum Echtzeit-Kundenprofil beitragen), Ereignisdatensätze (die Verhaltensdaten für Journeys und Analysen speichern) oder Systemdatensätze handeln, die von Journey Optimizer automatisch für Tracking-, Feedback- und Journey-Schrittereignisse erstellt werden.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

### Quell-Connector {#source-connector}

Ein Quell-Connector (auch als **Quelle** bezeichnet) hilft Ihnen dabei, Daten aus mehreren Systemen, z. B. Adobe Analytics, Adobe Experience Platform Web SDK, Cloud-Speicher (S3, Azure Blob) oder CRM-Datenbanken, in Adobe Experience Platform aufzunehmen. Über die Rohaufnahme hinaus ermöglichen Connectoren die Strukturierung, das Labeling und die Verbesserung von Daten mithilfe von Experience Platform-Services, einschließlich der Feldzuordnung zu Ihren XDM-Schemata und des Data-Governance-Labelings.

➡️ [Weitere Informationen zu Quell-Connectoren](../start/get-started-sources.md)

### Datenquelle (Journey Optimizer) {#data-source}

Eine Datenquelle in Journey Optimizer definiert, welche Felder aus Adobe Experience Platform (oder externen APIs) in Journeys und Nachrichten verfügbar gemacht werden. Datenquellen, die in der Journey Optimizer-Benutzeroberfläche konfiguriert sind, umfassen normalerweise die integrierte Adobe Experience Platform-Datenquelle (Bereitstellung von Echtzeit-Kundenprofilattributen) und optionale externe oder benutzerdefinierte Datenquellen, die zur Journey-Laufzeit zur zusätzlichen Anreicherung aufgerufen werden. Sie werden für Journey-Bedingungen, benutzerdefinierte Aktionen und die Nachrichtenpersonalisierung verwendet.

➡️ [Weitere Informationen zu Datenquellen](../datasource/about-data-sources.md)

>[!NOTE]
>Das [Adobe Experience Platform-Glossar](https://experienceleague.adobe.com/de/docs/experience-platform/landing/glossary){target="_blank"} definiert „Datenquelle“ allgemein als Ursprung von Daten (CRM, App usw.). In Journey Optimizer hat **Datenquelle** eine bestimmte Bedeutung: eine Benutzeroberflächenkonfiguration, die steuert, welche Felder in Journeys und Nachrichten verfügbar gemacht werden.

### Identität und Echtzeit-Kundenprofil {#identity}

Eine Identität ist eine Kennung, die eine einzelne Person eindeutig repräsentiert, z. B. eine Cookie-ID, Geräte-ID, E-Mail-Adresse oder CRM-ID. Identitäten sind in Namespaces (E-Mail, ECID, CRMID) organisiert und mehrere Identitäten für dieselbe Person werden in einem einheitlichen Identitätsdiagramm zusammengefasst. Das Echtzeit-Kundenprofil nutzt dieses Diagramm, um eine ganzheitliche Sicht auf jede einzelne Person zu erhalten, indem Daten aus verschiedenen Kanälen miteinander kombiniert werden, einschließlich Online-, Offline-, CRM- und Drittanbieter-Daten.

Ein wichtiges Konzept für Einsteigende ist das **Profilfragment**-Modell. Jedes Mal, wenn eine Person mit Ihrer Marke auf einem bestimmten Gerät oder Kanal interagiert (Ihrer Website, Ihrer App, einem Store) wird diese Interaktion als Profilfragment aufgezeichnet: eine Teilansicht dieser Person basierend auf diesem bestimmten Touchpoint. Das Echtzeit-Kundenprofil ordnet diese Fragmente kontinuierlich auf der Grundlage gemeinsamer Identitätswerte zu und erstellt so ein vollständiges, aktuelles Profil. Journey Optimizer liest dieses zusammengestellte Profil, um Bedingungen auszuwerten, Angebote auszuwählen und Nachrichten in Echtzeit zu personalisieren.

➡️ [Weitere Informationen zu Identitäten in Journey Optimizer](../audience/get-started-identity.md)

### Lookup-Datensatz {#lookup-dataset}

Mit einem Lookup-Datensatz kann Journey Optimizer Referenz- oder Transaktionsdaten zur Laufzeit aus einem Adobe Experience Platform-Datensatz abrufen, ohne diese Daten im Echtzeit-Kundenprofil zu speichern. Dies ist nützlich für sich häufig ändernde Referenzdaten (Preise, Lager, Geschäftszeiten) oder Transaktionsdaten, die zum Zeitpunkt der Nachricht benötigt werden, aber nicht zum Profil gehören. Journey Optimizer führt die Suche während der Journey- oder Nachrichtenausführung anhand eines Schlüssels durch, z. B. einer Produkt-ID.

➡️ [Weitere Informationen zu Lookup-Datensätzen](lookup-aep-data.md)

## Checkliste zur Datenbereitschaft {#checklist}

Bevor Marketing-Fachleute mit der Erstellung von Journeys und Kampagnen beginnen, sollte Ihr Unternehmen eine Reihe von Schritten zur Datenbereitschaft durchführen. Dadurch wird sichergestellt, dass Journey Optimizer die richtigen Daten zur richtigen Zeit und konform verwenden kann.

>[!NOTE]
>Die folgenden Schritte umfassen mehrere Rollen: Datentechnik, Administration und Marketing. Verwenden Sie diese Checkliste als gemeinsamen Plan, um Ihre Umgebung vorzubereiten. Die Schritte 1–4 werden in Adobe Experience Platform ausgeführt. Die Schritte 5–-6 werden in Journey Optimizer konfiguriert.

Die folgenden sechs Schritte führen Sie durch den vollständigen Dateneinrichtungsprozess, von der Identitätskonfiguration bis zur Überprüfung, ob Daten korrekt in Journey Optimizer fließen:

1. Definieren der Identitätsstrategie
1. Entwerfen von Schemata für Profil- und Ereignisdaten
1. Erstellen von profilaktivierten Datensätzen
1. Aufnehmen von Daten aus Ihren Quellen
1. Konfigurieren von Datenquellen in Journey Optimizer
1. Überprüfen von Tracking-, Feedback- und Journey-Datensätzen

+++ Definieren der Identitätsstrategie

Wählen Sie eine primäre Identität für Ihre Kundschaft aus (z. B. ECID, E-Mail oder CRMID) und konfigurieren Sie die entsprechenden Namespaces im Adobe Experience Platform Identity Service. Stellen Sie sicher, dass Identitätsfelder in Ihren profilaktivierten Schemata vorhanden sind, und überprüfen Sie, ob die Profile im Identitätsdiagramm korrekt zugeordnet sind.

➡️ [Weitere Informationen zu Identitäten in Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Entwerfen von Schemata für Profil- und Ereignisdaten

Erstellen Sie Schemata des Typs **XDM-Profil für Einzelpersonen** zur Erfassung von Kundenattributen wie Name und Kontaktinformationen, Voreinstellungen und Interessen sowie Lebenszyklusphase oder Einverständnisstatus. Erstellen Sie Schemata des Typs **XDM-ExperienceEvent** zur Erfassung von Verhaltens- und Transaktionsdaten wie Web- und App-Ereignisse, Käufe und Offline-Interaktionen. Markieren Sie die richtigen Felder gegebenenfalls als Identitäten und Profilattribute.

➡️ [Weitere Informationen über Schemata](get-started-schemas.md)

+++

+++ Erstellen von profilaktivierten Datensätzen

Erstellen Sie in Adobe Experience Platform Datensätze basierend auf Ihren XDM-Schemata und aktivieren Sie das Profil für jeden Datensatz, der zum Echtzeit-Kundenprofil beitragen soll. Überprüfen Sie, ob die von Journey Optimizer erstellten systemgenerierten Datensätze im Arbeitsbereich „Datensätze“ angezeigt werden.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

+++

+++ Aufnehmen von Daten aus Ihren Quellen

Konfigurieren Sie Quell-Connectoren für Ihre Unternehmenssysteme, z. B. Adobe Analytics, Adobe Experience Platform Web SDK oder Ihre CRM- und POS-Plattformen, und ordnen Sie eingehende Felder Ihren XDM-Schemata zu. Überprüfen Sie, ob Daten in den richtigen Datensätzen landen und wie erwartet im Echtzeit-Kundenprofil angezeigt werden.

➡️ [Weitere Informationen zu Quell-Connectoren](../start/get-started-sources.md)

➡️ [Tutorial: Erstellen von Datensätzen und Aufnehmen von Daten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Konfigurieren von Datenquellen in Journey Optimizer

Datenquellen sind ein Journey Optimizer-spezifisches Konzept: Sie sind nicht der Ort, an dem Ihre Daten gespeichert werden, sondern der Ort, an dem Sie deklarieren, welche Felder Journey Optimizer bei der Journey- und Nachrichtenausführung lesen darf. Bevor eine Journey eine Bedingung wie „Ist die Person Mitglied des Treueprogramms?“ überprüfen oder eine Nachricht mit einem Vornamen personalisieren kann, müssen die entsprechenden Profilfelder über eine Datenquellenkonfiguration verfügbar gemacht werden.

Journey Optimizer enthält eine integrierte [Adobe Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md), die direkten Zugriff auf Echtzeit-Kundenprofilattribute bietet. Dies deckt den Großteil der Anwendungsfälle ab: das Lesen von Profilattributen zur Personalisierung oder das Überprüfen von Einverständnis- und Voreinstellungsfeldern. Sie können [externe Datenquellen](../datasource/external-data-sources.md) auch so konfigurieren, dass Drittanbieter-APIs zur Journey-Laufzeit aufgerufen werden, um beispielsweise einen Echtzeit-Treueprogrammwert, eine Produktempfehlung oder eine Store-Inventarebene abzurufen, die nicht in Adobe Experience Platform gespeichert ist.

>[!NOTE]
>Der direkte Zugriff auf Erlebnisereignisdaten über die integrierte Adobe Experience Platform-Datenquelle wird nicht mehr unterstützt und schrittweise deaktiviert. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

Das Konfigurieren von Datenquellen ist eine Verwaltungsaufgabe, die die vollständige Datenschicht für Journey-Erstellende und Marketing-Experten freischaltet. Sobald ein Feld über eine Datenquelle verfügbar gemacht wurde, kann es im Journey-Bedingungs-Builder, in den Nachrichtenpersonalisierungseditoren und in Angebotsentscheidungsregeln verwendet werden, ohne dass zum Zeitpunkt der Journey-Erstellung zusätzliche technische Arbeiten erforderlich sind.

➡️ [Weitere Informationen zur Konfiguration von Datenquellen](../datasource/about-data-sources.md)

+++

+++ Überprüfen von Tracking-, Feedback- und Journey-Datensätzen

Überprüfen Sie, ob im Arbeitsbereich „Datensätze“ von Journey Optimizer systemgenerierte Datensätze verfügbar sind. Führen Sie Test-Journeys und -Kampagnen aus und verwenden Sie dann den Abfrage-Editor, um zu überprüfen, ob Versand-, Öffnungs-, Klick- und Bounce-Ereignisse aufgezeichnet werden und ob Journey-Schrittereignisse und -Status korrekt erfasst werden. Verwenden Sie diese Datensätze für fortlaufendes Monitoring sowie fortlaufende Fehlerbehebung und Journey-Optimierung.

➡️ [Weitere Informationen zu Abfragen in Journey Optimizer](get-started-queries.md)

+++

## Leitlinien und Überlegungen zum Daten-Design {#guardrails}

Einige Produktleitlinien und -einschränkungen können sich auf das Design Ihres Datenmodells und Ihrer Journeys auswirken. Überprüfen Sie diese frühzeitig, um die Notwendigkeit einer späteren Überarbeitung zu vermeiden.

>[!IMPORTANT]
>Die neuesten Informationen finden Sie immer auf der Seite [Leitlinien und Einschränkungen für Journey Optimizer](../start/guardrails.md). In den nachstehenden Zusammenfassungen werden die wichtigsten Punkte hervorgehoben, sie können sich jedoch im Laufe der Zeit verändern.

### Journey Optimizer-Systemdatensätze und TTL {#datasets-ttl}

Journey Optimizer erstellt mehrere systemgenerierte Datensätze für Tracking, Feedback und Journey-Schrittereignisse. Seit Februar 2025 gibt es für einige dieser Datensätze eine TTL-Leitlinie (Time-to-Live), die sich auf die Aufbewahrungsdauer von Daten für Analysen und Fehlerbehebungen auswirken kann.

➡️ [Weitere Informationen zu den Datensatz-TTL-Leitlinien](datasets-ttl.md)

### Streaming-Segmentierung und Journey Optimizer-Ereignisse {#streaming-segmentation}

Seit 1. November 2024 unterstützt die Streaming-Segmentierung keine Versand- und Öffnungsereignisse aus Tracking- und Feedback-Datensätzen von Journey Optimizer mehr. Verwenden Sie für Anwendungsfälle wie Frequenzbegrenzung und Ermüdungsverwaltung [Geschäftsregeln](../conflict-prioritization/rule-sets.md) anstelle von Streaming-Segmenten basierend auf Versand-/Öffnungsereignissen.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

### Datensatzsuche und Entscheidungsfindung {#lookup-guardrails}

Die Datensatzsuche eignet sich ideal für sich häufig ändernde Attribute (Inventar, Preise, Wetter) oder Daten, die nicht im Echtzeit-Kundenprofil gespeichert werden müssen. Überprüfen Sie produktspezifische Leitlinien wie Größenbeschränkungen für Datensätze und Abfragebegrenzungen in der entsprechenden Dokumentation, bevor Sie Ihre Suchstrategie entwerfen.

➡️ [Weitere Informationen zu Lookup-Datensätzen](lookup-aep-data.md)

## Beispiel: Vorbereiten von Daten für eine Begrüßungs-Journey {#example}

Das folgende Beispiel zeigt, wie die Konzepte auf dieser Seite in einem einfachen Szenario zusammenarbeiten.

1. Eine Dateningenieurin bzw. ein Dateningenieur erstellt ein Schema des Typs [XDM-Profil für Einzelpersonen](get-started-schemas.md) für Kundenattribute (Name, E-Mail, Treuestufe, Einverständnis) und ein Schema des Typs XDM-ExperienceEvent für Web-Anmeldungsereignisse.
1. [Profilaktivierte Datensätze](get-started-datasets.md) werden für jedes Schema erstellt: einer für CRM-Attribute und einer für Anmeldungsereignisse.
1. Web- und Mobile-Teams streamen Anmeldungsereignisse über Adobe Experience Platform Web SDK. CRM-Daten werden über einen [Quell-Connector](../start/get-started-sources.md) aufgenommen.
1. Eine bzw. ein Admin konfiguriert die [Adobe Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) in Journey Optimizer und macht Felder wie `profile.person.name.firstName`, `profile.personalEmail.address` und `profile.loyaltyTier` verfügbar.
1. Eine Marketing-Fachkraft [erstellt eine Begrüßungs-Journey](../building-journeys/journey-gs.md), die auf ein Anmeldungsereignis wartet und diese Profilattribute verwendet, um [&#x200B; Begrüßungs-E-Mails zu personalisieren](../personalization/personalize.md). Journey Optimizer schreibt Versand- und Öffnungsereignisse in Tracking-Datensätze und protokolliert den Journey-Fortschritt in Journey-Schrittereignisdatensätzen.
1. Eine Entwicklerin bzw. ein Entwickler verwendet den [Abfrage-Editor](get-started-queries.md), um zu überprüfen, ob Ereignisse ordnungsgemäß funktionieren, und analysieren die Leistung (Öffnungen, Klicks, Versandzeit). Basierend auf diesen Erkenntnissen passt das Team die Journey und den Inhalt an.

Dieser Fluss veranschaulicht, wie Schemata, Datensätze, Quellen, Datenquellen und Abfragen in einem vollständigen, anfängerfreundlichen Anwendungsfall zusammenarbeiten.

## Verwandte Ressourcen {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Erste Schritte mit Schemata**

Erfahren Sie, wie Sie XDM-Schemata in Adobe Experience Platform erstellen, die richtigen Klassen- und Feldergruppen auswählen und Ihre Profilattribute und Verhaltensereignisse modellieren.

[Weitere Informationen](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Arbeiten mit Datensätzen**

Erfahren Sie, wie Sie profilaktivierte Datensätze und Ereignisdatensätze erstellen, die Datenaufnahme überwachen und die systemgenerierten Datensätze erkunden, die Journey Optimizer automatisch für Tracking-, Feedback- und Journey-Schrittereignisse erstellt.

[Weitere Informationen](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Konfigurieren von Datenquellen**

Detaillierte Anleitungen zum Einrichten der integrierten Adobe Experience Platform-Datenquelle und der optionalen externen Datenquellen, um Profilfelder und Antworten externer APIs innerhalb Ihrer Journey verfügbar zu machen.

[Weitere Informationen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Verwenden von Adobe Experience Platform-Daten (Suche)**

Erfahren Sie, wie Sie Nachrichten zur Laufzeit mit Referenz- oder Transaktionsdaten aus AEP-Datensätzen anreichern können, ohne diese Daten im Echtzeit-Kundenprofil zu speichern.

[Weitere Informationen](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Erste Schritte mit Abfragen**

Verwenden Sie den Abfrage-Service, um Journey Optimizer-Datensätze zu analysieren, sicherzustellen, dass Ereignisse korrekt funktionieren, und Reporting-Abrfagen zu Versand-, Öffnungs-, Klick- und Bounce-Daten zu erstellen.

[Weitere Informationen](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Erste Schritte mit Profilen**

Erfahren Sie, wie das Echtzeit-Kundenprofil in Journey Optimizer funktioniert und wie Sie einzelne Kundenprofile in der Platform-Benutzeroberfläche durchsuchen, überprüfen und validieren können.

[Weitere Informationen](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Überblick-Tutorial zum Einrichten von Daten**

Eine anfängerfreundliche Videoeinführung zum Einrichten von Daten in Journey Optimizer, die Schemata, Datensätze und Quellen von Anfang bis Ende behandelt.

[Tutorial ansehen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial zum Erstellen von Datensätzen und Aufnehmen von Daten**

Ein praktisches Tutorial, das zeigt, wie Datensätze in Adobe Experience Platform erstellt und Daten mithilfe von Quell-Connectoren aufgenommen werden, mit detaillierten Anweisungen, die Sie in Ihrer eigenen Sandbox befolgen können.

[Tutorial ansehen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
