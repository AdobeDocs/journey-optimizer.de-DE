---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten-Management in Journey Optimizer
description: Erfahren Sie, wie Daten in und aus Adobe Journey Optimizer fließen, einschließlich Schlüsselkonzepte, Einrichtungsschritte und Leitplanken.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 89d575834871a5c55bfce75511083b4b651301b8
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 2%

---


# Erste Schritte mit Daten-Management {#about-data}

Daten sind die Grundlage für jede Journey, Entscheidung und Nachricht, die Sie mit [!DNL Adobe Journey Optimizer] versenden.

Auf dieser Seite erhalten Sie einen praktischen Ausgangspunkt zum Verständnis:

* Die von Journey Optimizer verwendeten grundlegenden Datenbausteine (Schemata, Datensätze, Identitäten, Profile)
* Verwendung von Adobe Experience Platform-Daten durch Journey Optimizer
* Welche Dateneinstellungsschritte Ihr Team durchlaufen muss, bevor Journey und Kampagnen erstellt werden können
* Wie Sie als Nächstes vorgehen, um detaillierte Konfigurationen und Best Practices anzuzeigen

Verwenden Sie dieses Handbuch zusammen mit Ihren Dateningenieuren, Administratoren und Marketern, damit jeder Benutzer ein gemeinsames Bild davon hat, wie Daten in Journey Optimizer ein- und ausfließen.

>[!TIP]
>Neu bei der Datenverwaltung in Journey Optimizer? Sehen Sie sich [&#x200B; Tutorial zum Einrichten &#x200B;](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} Datenübersicht an, um eine praktische, anfängerfreundliche Anleitung für Schemata, Datensätze und Quellen zu erhalten.

## Verwendung von Adobe Experience Platform-Daten durch Journey Optimizer {#aep-data}

[!DNL Adobe Journey Optimizer] basiert auf [!DNL Adobe Experience Platform]. Es unterhält keinen separaten, isolierten Datenspeicher. Stattdessen wird dieselbe Datengrundlage wie bei anderen Experience Cloud-Programmen verwendet.

Schemata und Datensätze sind in Adobe Experience Platform verfügbar. Identitäten und das [Echtzeit-Kundenprofil](../audience/get-started-profiles.md) werden von Identity Service und Profil-Service verwaltet. Journey Optimizer liest Profil- und Ereignisdaten aus Adobe Experience Platform, um Journey-Bedingungen auszuwerten, Nachrichten zu personalisieren und Angebote auszuwählen. Es schreibt Interaktionsdaten wie Sende-, Öffnungs-, Klick- und Bounce-Ereignisse und Journey-Schrittereignisse zurück in Experience Platform-Datensätze. Es können auch zusätzliche Datensätze zur Laufzeit nachgeschlagen werden, ohne diese Daten in das Profil zu kopieren.

>[!TIP]
>Stellen Sie sich Adobe Experience Platform als zentrale Datenschicht und Journey Optimizer als eine Anwendung vor, die Journey und Nachrichten mithilfe dieser gemeinsamen Datengrundlage orchestriert.

➡️ [Erfahren Sie mehr über die Architektur von Journey Optimizer](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Wichtige Datenkonzepte in Journey Optimizer {#key-concepts}

Beim Arbeiten mit Daten in Journey Optimizer werden Sie auf verschiedene verwandte Konzepte stoßen. Die nachstehende Tabelle bietet einen schnellen Überblick; in den folgenden Abschnitten werden die einzelnen Konzepte detaillierter erläutert.

| Konzept | Was es ist | Primäre Verwendung in Journey Optimizer |
|---|---|---|
| XDM-Schema | Regeln, die Ihre Daten darstellen, validieren und formatieren (basierend auf einer Klasse und Feldergruppen) | Modellprofilattribute und Verhaltensereignisse |
| Datensatz | Speichertabelle für schemakonforme Daten | Profil-, Ereignis- und systemgenerierte Daten speichern |
| Source-Connector | Streamt Daten oder Batches aus externen Systemen nach AEP | Aufnehmen von CRM-, Analyse- und Web-Daten |
| Datenquelle | Zeigt AEP oder externe Felder in Journey an | Power Journey-Bedingungen und Nachrichtenpersonalisierung |
| Identität | Kennung, die einen einzelnen Kunden eindeutig repräsentiert | Profile kanalübergreifend zusammenfügen |
| Datensatz nachschlagen | Laufzeitreferenz zu AEP-Daten ohne Profilspeicher | Nachrichten mit Live-Referenzdaten anreichern |

### Schema (XDM-Schema) {#schema}

Ein Schema ist ein Regelsatz, der Ihre Daten repräsentiert, validiert und formatiert. Sie besteht aus einer **Klasse** (die das Basisverhalten definiert: Datensatz oder Zeitreihen) und optionalen **Feldergruppen** (die bestimmte Felder hinzufügen). Schemata werden mithilfe von Experience-Datenmodell(XDM)-Standards definiert und sind in Adobe Experience Platform live.

XDM dient der Lösung eines echten Problems: Dasselbe Konzept - ein Kunde, ein Kauf, ein Produkt - wird in den Quellsystemen unterschiedlich benannt und strukturiert. XDM bietet eine gemeinsame Sprache, die diese Konzepte unabhängig vom Ursprung der Daten unter einer einzigen Definition zusammenfasst. Dadurch kann Journey Optimizer konsistent mit Daten aus Ihrem CRM, Ihrer Website, Ihrer Mobile App und Ihrem Data Warehouse gleichzeitig arbeiten.

In Journey Optimizer arbeiten Sie normalerweise mit **XDM Individual Profile**-Schemata für Kundenattribute (Name, Voreinstellungen, Einverständnis) und **XDM ExperienceEvent**-Schemata für Verhaltensereignisse (Käufe, Seitenansichten, Anmeldungen).

➡️ [Weitere Informationen zu Schemata](get-started-schemas.md)

### Datensatz {#dataset}

Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, das einem Schema entspricht - stellen Sie sich ihn als Tabelle mit einem definierten Satz von Spalten und Zeilen vor. Alle von Journey Optimizer verwendeten Daten werden in Adobe Experience Platform-Datensätzen gespeichert. Dabei kann es sich um Profildatensätze (die zum Echtzeit-Kundenprofil beitragen), Ereignisdatensätze (die Verhaltensdaten für Journey und Analysen speichern) oder Systemdatensätze handeln, die von Journey Optimizer automatisch für Tracking-, Feedback- und Journey-Schrittereignisse erstellt werden.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

### Source-Connector {#source-connector}

Ein Quell-Connector (auch als **source** bezeichnet) hilft Ihnen dabei, Daten aus mehreren Systemen - z. B. Adobe Analytics, Adobe Experience Platform Web SDK, Cloud-Speicher (S3, Azure Blob) oder CRM-Datenbanken - in Adobe Experience Platform aufzunehmen. Über die Rohaufnahme hinaus ermöglichen Connectoren die Strukturierung, Beschriftung und Verbesserung von Daten mithilfe von Experience Platform-Services, einschließlich der Feldzuordnung zu Ihren XDM-Schemata und der Data Governance-Beschriftung.

➡️ [Weitere Informationen zu Quell-Connectoren](../start/get-started-sources.md)

### Datenquelle (Journey Optimizer) {#data-source}

Eine Datenquelle in Journey Optimizer definiert, welche Felder aus Adobe Experience Platform (oder externen APIs) in Journey und Nachrichten verfügbar gemacht werden. Datenquellen, die in der Journey Optimizer-Benutzeroberfläche konfiguriert sind, umfassen normalerweise die integrierte Adobe Experience Platform-Datenquelle (Bereitstellung von Echtzeit-Kundenprofilattributen und -ereignissen) und optional externe oder benutzerdefinierte Datenquellen, die zur Journey-Laufzeit zur zusätzlichen Anreicherung aufgerufen werden. Sie werden für Journey-Bedingungen, benutzerdefinierte Aktionen und die Nachrichtenpersonalisierung verwendet.

➡️ [Erfahren Sie mehr über Datenquellen](../datasource/about-data-sources.md)

>[!NOTE]
>Das [Adobe Experience Platform-Glossar](https://experienceleague.adobe.com/de/docs/experience-platform/landing/glossary){target="_blank"} definiert „Datenquelle“ allgemein als Ursprung von Daten (CRM, Mobile App usw.). In Journey Optimizer hat **Datenquelle** eine bestimmte Bedeutung: eine Benutzeroberflächenkonfiguration, die steuert, welche Felder in Journey und Nachrichten verfügbar gemacht werden.

### Identität und Echtzeit-Kundenprofil {#identity}

Eine Identität ist eine Kennung, die einen einzelnen Kunden eindeutig repräsentiert, z. B. eine Cookie-ID, Geräte-ID, E-Mail-Adresse oder CRM-ID. Identitäten sind in Namespaces (E-Mail, ECID, CRMID) organisiert, und mehrere Identitäten für dieselbe Person werden in einem einheitlichen Identitätsdiagramm zusammengefasst. Das Echtzeit-Kundenprofil verwendet dieses Diagramm, um eine ganzheitliche Sicht auf jeden einzelnen Kunden zu erhalten, indem es Daten aus verschiedenen Kanälen kombiniert - einschließlich Online-, Offline-, CRM- und Drittanbieter-Quellen.

Ein Schlüsselkonzept für Anfänger ist das **Profilfragment**-Modell. Jedes Mal, wenn ein Kunde mit Ihrer Marke auf einem bestimmten Gerät oder Kanal interagiert - Ihrer Website, Ihrer Mobile App, einem Store - wird diese Interaktion als Profilfragment aufgezeichnet: eine Teilansicht dieses Kunden basierend auf diesem bestimmten Touchpoint. Das Echtzeit-Kundenprofil ordnet diese Fragmente kontinuierlich auf der Grundlage gemeinsamer Identitätswerte zusammen und erstellt so ein vollständiges, aktuelles Profil. Journey Optimizer liest aus diesem zusammengestellten Profil, um Bedingungen auszuwerten, Angebote auszuwählen und Nachrichten in Echtzeit zu personalisieren.

➡️ [Erfahren Sie mehr über Identitäten in Journey Optimizer](../audience/get-started-identity.md)

### Datensatz nachschlagen {#lookup-dataset}

Mit einem Lookup-Datensatz kann Journey Optimizer Referenz- oder Transaktionsdaten zur Laufzeit aus einem Adobe Experience Platform-Datensatz abrufen, ohne diese Daten im Echtzeit-Kundenprofil zu speichern. Dies ist nützlich für sich häufig ändernde Referenzdaten (Preise, Lager, Geschäftszeiten) oder Transaktionsdaten, die zum Zeitpunkt der Nachricht benötigt werden, aber nicht zum Profil gehören. Journey Optimizer führt die Suche während der Journey- oder Nachrichtenausführung anhand eines Schlüssels, z. B. einer Produkt-ID, durch.

➡️ [Weitere Informationen zu Lookup-Datensätzen](lookup-aep-data.md)

## Checkliste zur Datenbereitschaft {#checklist}

Bevor Marketing-Fachleute mit der Erstellung von Journey und Kampagnen beginnen, sollte Ihr Unternehmen eine Reihe von Schritten zur Datenbereitschaft durchführen. Dadurch wird sichergestellt, dass Journey Optimizer die richtigen Daten zur richtigen Zeit und konform verwenden kann.

>[!NOTE]
>Die folgenden Schritte umfassen mehrere Rollen: Dateningenieure, Administratoren und Marketing-Experten. Verwenden Sie diese Checkliste als gemeinsamen Plan, um Ihre Umgebung vorzubereiten. Die Schritte 1-4 werden in Adobe Experience Platform ausgeführt. Die Schritte 5-6 werden in Journey Optimizer konfiguriert.

Die folgenden sechs Schritte führen Sie durch den vollständigen Prozess der Dateneinrichtung, von der Identitätskonfiguration bis zur Überprüfung, ob Daten korrekt in Journey Optimizer fließen:

1. Definieren der Identitätsstrategie
1. Entwerfen von Schemata für Profil- und Ereignisdaten
1. Profilaktivierte Datensätze erstellen
1. Aufnehmen von Daten aus Quellen
1. Konfigurieren von Datenquellen in Journey Optimizer
1. Tracking, Feedback und Journey von Datensätzen überprüfen

+++ Definieren der Identitätsstrategie

Wählen Sie eine primäre Identität für Ihre Kunden aus (z. B. ECID, E-Mail oder CRMID) und konfigurieren Sie die entsprechenden Namespaces im Adobe Experience Platform Identity Service. Stellen Sie sicher, dass Identitätsfelder in Ihren profilaktivierten Schemata vorhanden sind, und überprüfen Sie, ob die Profile korrekt in das Identitätsdiagramm eingeordnet sind.

➡️ [Erfahren Sie mehr über Identitäten in Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Entwerfen von Schemata für Profil- und Ereignisdaten

Erstellen Sie **XDM-Individualprofil**-Schemas zur Erfassung von Kundenattributen wie Name und Kontaktinformationen, Voreinstellungen und Interessen sowie Lebenszyklus-Stadium oder Einverständnisstatus. Erstellen Sie **XDM ExperienceEvent**-Schemas zur Erfassung von Verhaltens- und Transaktionsdaten wie Web- und App-Ereignisse, Käufe und Offline-Interaktionen. Markieren Sie die richtigen Felder gegebenenfalls als Identitäten und Profilattribute.

➡️ [Weitere Informationen zu Schemata](get-started-schemas.md)

+++

+++ Profilaktivierte Datensätze erstellen

Erstellen Sie in Adobe Experience Platform Datensätze basierend auf Ihren XDM-Schemata und aktivieren Sie das Profil für jeden Datensatz, der zum Echtzeit-Kundenprofil beitragen soll. Überprüfen Sie, ob die von Journey Optimizer erstellten systemgenerierten Datensätze im Arbeitsbereich Datensätze angezeigt werden.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

+++

+++ Aufnehmen von Daten aus Quellen

Konfigurieren Sie Quell-Connectoren für Ihre Unternehmenssysteme, z. B. Adobe Analytics, Adobe Experience Platform Web SDK oder Ihre CRM- und POS-Plattformen, und ordnen Sie eingehende Felder Ihren XDM-Schemata zu. Überprüfen Sie, ob Daten in den richtigen Datensätzen landen und wie erwartet im Echtzeit-Kundenprofil angezeigt werden.

➡️ [Weitere Informationen zu Quell-Connectoren](../start/get-started-sources.md)

➡️ [Tutorial: Erstellen Sie Datensätze und nehmen Sie Daten auf](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Konfigurieren von Datenquellen in Journey Optimizer

Datenquellen sind ein Journey Optimizer-spezifisches Konzept: Sie sind nicht der Ort, an dem Ihre Daten leben, sondern wo Sie deklarieren, welche Felder Journey Optimizer beim Journey und bei der Nachrichtenausführung lesen darf. Bevor eine Journey eine Bedingung wie „Ist der Kunde Mitglied des Treueprogramms?“ Um eine Nachricht mit einem Vornamen zu personalisieren, müssen die entsprechenden Profilfelder über eine Datenquellenkonfiguration verfügbar gemacht werden.

Journey Optimizer enthält eine integrierte [Adobe Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) die direkten Zugriff auf Echtzeit-Kundenprofilattribute bietet. Dies deckt den Großteil der Anwendungsfälle ab: das Lesen von Profilattributen zur Personalisierung oder das Überprüfen von Einverständnis- und Präferenzfeldern. Sie können [externe Datenquellen](../datasource/external-data-sources.md) auch so konfigurieren, dass Drittanbieter-APIs zur Journey-Laufzeit aufgerufen werden, um beispielsweise einen Echtzeit-Treueprogramm-Score, eine Produktempfehlung oder eine Store-Inventarebene abzurufen, die nicht in Adobe Experience Platform gespeichert ist.

>[!NOTE]
>Der direkte Zugriff auf Erlebnisereignisdaten über die integrierte Adobe Experience Platform-Datenquelle wird nicht mehr unterstützt und schrittweise deaktiviert. [Weitere Informationen](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

Das Konfigurieren von Datenquellen ist eine Verwaltungsaufgabe, die die vollständige Datenschicht für Journey-Autoren und Marketing-Experten freischaltet. Sobald ein Feld über eine Datenquelle verfügbar gemacht wurde, wird es im Journey-Bedingungsgenerator, in den Nachrichtenpersonalisierungseditoren und in Offer Decisioning-Regeln verfügbar, ohne dass zum Zeitpunkt der Journey-Erstellung zusätzliche technische Arbeiten erforderlich sind.

➡️ [Erfahren Sie mehr über die Konfiguration von Datenquellen](../datasource/about-data-sources.md)

+++

+++ Tracking, Feedback und Journey von Datensätzen überprüfen

Überprüfen Sie, ob im Arbeitsbereich Datensätze von Journey Optimizer systemgenerierte Datensätze verfügbar sind. Führen Sie Test-Journey und -Kampagnen aus und verwenden Sie dann den Abfrage-Editor, um zu überprüfen, ob Sende-, Öffnen-, Klick- und Bounce-Ereignisse aufgezeichnet werden und ob Journey-Schrittereignisse und -Status korrekt erfasst werden. Verwenden Sie diese Datensätze für die fortlaufende Überwachung, Fehlerbehebung und Journey-Optimierung.

➡️ [Erfahren Sie mehr über Abfragen in Journey Optimizer](get-started-queries.md)

+++

## Leitplanken und Überlegungen zum Datendesign {#guardrails}

Einige Produkt-Leitplanken und Einschränkungen können sich auf die Gestaltung Ihres Datenmodells und Ihrer Journey auswirken. Überprüfen Sie diese frühzeitig, um eine spätere Überarbeitung zu vermeiden.

>[!IMPORTANT]
>Die neuesten Informationen finden Sie immer auf der Seite [Leitplanken und Einschränkungen &#x200B;](../start/guardrails.md) Journey Optimizer . In den nachstehenden Zusammenfassungen werden die wichtigsten Punkte hervorgehoben, sie können sich jedoch im Laufe der Zeit weiterentwickeln.

### Journey Optimizer-Systemdatensätze und TTL {#datasets-ttl}

Journey Optimizer erstellt mehrere systemgenerierte Datensätze zum Tracking, Feedback und Journey von Schrittereignissen. Ab Februar 2025 wird für einige dieser Datensätze eine TTL-Schutzmaßnahme (Time-to-Live) eingeführt, die sich auf die Aufbewahrungsdauer von Daten für Analysen und Fehlerbehebungen auswirken kann.

➡️ [Weitere Informationen zu den Leitplanken für Datensatz-TTL](datasets-ttl.md)

### Streaming-Segmentierung und Journey Optimizer-Ereignisse {#streaming-segmentation}

Seit dem 1. November 2024 unterstützt die Streaming-Segmentierung nicht mehr das Senden und Öffnen von Ereignissen aus Journey Optimizer-Tracking- und -Feedback-Datensätzen. Verwenden Sie für Anwendungsfälle wie Frequenzlimitierung und Ermüdungsverwaltung [Geschäftsregeln](../conflict-prioritization/rule-sets.md) anstelle von Streaming-Segmenten basierend auf Sende-/Open-Ereignissen.

➡️ [Weitere Informationen zu Datensätzen](get-started-datasets.md)

### Datensatzsuche und -entscheidung {#lookup-guardrails}

Die Datensatzsuche eignet sich ideal für häufig wechselnde Attribute (Inventar, Preise, Wetter) oder Daten, die nicht im Echtzeit-Kundenprofil gespeichert werden müssen. Überprüfen Sie produktspezifische Leitplanken wie Größenbeschränkungen für Datensätze und Abfrageobergrenzen in der entsprechenden Dokumentation, bevor Sie Ihre Suchstrategie entwerfen.

➡️ [Weitere Informationen zu Lookup-Datensätzen](lookup-aep-data.md)

## Beispiel: Daten für eine Begrüßungs-Journey vorbereiten {#example}

Das folgende Beispiel zeigt, wie die Konzepte auf dieser Seite in einem einfachen Szenario zusammenarbeiten.

1. Dateningenieure erstellen ein Schema [XDM Individual Profile](get-started-schemas.md) für Kundenattribute (Name, E-Mail, Treuestufe, Einverständnis) und ein XDM ExperienceEvent-Schema für Web-Anmeldungsereignisse.
1. [Profil-Datensätze](get-started-datasets.md) werden für jedes Schema erstellt: einen für CRM-Attribute und einen für Anmeldungsereignisse.
1. Web- und Mobile-Teams streamen Registrierungsereignisse über Adobe Experience Platform Web SDK. CRM-Daten werden über einen [Quell-Connector](../start/get-started-sources.md) aufgenommen.
1. Ein Administrator konfiguriert die [Adobe Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) in Journey Optimizer und macht Felder wie `profile.person.name.firstName`, `profile.personalEmail.address` und `profile.loyaltyTier` verfügbar.
1. Ein Marketing[Experte erstellt eine Begrüßungs-Journey](../building-journeys/journey-gs.md), die auf ein Registrierungsereignis wartet und diese Profilattribute verwendet, um [&#x200B; Begrüßungs-E-Mail zu personalisieren](../personalization/personalize.md). Journey Optimizer schreibt Ereignisse zum Senden und Öffnen in Tracking-Datensätze und protokolliert den Journey-Fortschritt in Journey-Schritt-Ereignisdatensätzen.
1. Entwicklerinnen und Entwickler verwenden [Abfrage-Editor](get-started-queries.md), um zu überprüfen, ob Ereignisse ordnungsgemäß fließen, und die Leistung (Öffnungen, Klicks, Versandzeit) zu analysieren. Basierend auf diesen Erkenntnissen passt das Team die Journey und den Inhalt an.

Dieser Fluss veranschaulicht, wie Schemas, Datensätze, Quellen, Datenquellen und Abfragen in einem vollständigen, anfängerfreundlichen Anwendungsfall zusammenarbeiten.

## Verwandte Ressourcen {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

**Erste Schritte mit Schemata**

Erfahren Sie, wie Sie XDM-Schemata in Adobe Experience Platform erstellen, die richtigen Klassen- und Feldergruppen auswählen und Ihre Profilattribute und Verhaltensereignisse modellieren.

[Weitere Informationen](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=de)

**Arbeiten mit Datensätzen**

Erfahren Sie, wie Sie profilaktivierte und Ereignis-Datensätze erstellen, die Datenaufnahme überwachen und die systemgenerierten Datensätze erkunden, die Journey Optimizer automatisch für Tracking-, Feedback- und Journey-Schrittereignisse erstellt.

[Weitere Informationen](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=de)

**Konfigurieren von Datenquellen**

Schrittweise Anleitungen zum Einrichten der integrierten Adobe Experience Platform-Datenquelle und optionalen externen Datenquellen, um Profilfelder und externe API-Antworten innerhalb Ihrer Journey bereitzustellen.

[Weitere Informationen](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=de)

**Verwenden von Adobe Experience Platform-Daten (Suche)**

Erfahren Sie, wie Sie Nachrichten zur Laufzeit mit Referenz- oder Transaktionsdaten aus AEP-Datensätzen anreichern können, ohne diese Daten im Echtzeit-Kundenprofil zu speichern.

[Weitere Informationen](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

**Erste Schritte mit Abfragen**

Verwenden Sie den Abfrage-Service, um Journey Optimizer-Datensätze zu analysieren, sicherzustellen, dass Ereignisse korrekt verlaufen, und Berichtsabfragen für die Daten „Senden“, „Öffnen“, „Klicken“ und „Bounce“ zu erstellen.

[Weitere Informationen](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=de)

**Erste Schritte mit Profilen**

Erfahren Sie, wie das Echtzeit-Kundenprofil in Journey Optimizer funktioniert und wie Sie einzelne Kundenprofile in der Platform-Benutzeroberfläche durchsuchen, überprüfen und validieren können.

[Weitere Informationen](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

**Tutorial zur Datenübersicht einrichten**

Eine Videoeinführung für Anfänger zum Einrichten von Daten in Journey Optimizer, die Schemata, Datensätze und Quellen von Anfang bis Ende behandelt.

[Tutorial ansehen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=de)

**Tutorial zum Erstellen von Datensätzen und Aufnehmen von Daten**

Ein praktisches Tutorial, das zeigt, wie Datensätze in Adobe Experience Platform erstellt und Daten mithilfe von Quell-Connectoren aufgenommen werden, mit schrittweisen Anweisungen, die Sie in Ihrer eigenen Sandbox befolgen können.

[Tutorial ansehen](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
