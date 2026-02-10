---
title: Vorteile der Migration zu Decisioning
description: Erfahren Sie mehr über die Vorteile der Migration vom Entscheidungs-Management zum Entscheidungs-Management
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: aedd7845-3d8d-457a-a7f3-03897846b241
source-git-commit: 741b39a7588ae4e1161891226d95609508b00031
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 3%

---

# Vorteile der Migration zu Decisioning {#migrate-to-decisioning}

## Was ist Decisioning? {#what-is-decisioning}

Journey Optimizer Decisioning ist eine Erweiterung der Entscheidungsfunktion, die die Grundlage für zukünftige Entscheidungen über andere Objekte (wie Journey) legt. Diese neue Funktion vereinheitlicht wichtige Workflow-Konzepte für optimiertes Authoring und Management, führt Experimente in die Entscheidungsfindung ein und verlagert Entscheidungselemente in einen schemabasierten Ansatz für das dynamische Element-Rendering.

Mit dem Entscheidungs-Framework der nächsten Generation und den in Adobe Journey Optimizer verfügbaren Funktionen können Marken verfügbare Daten, Informationen und den Kontext eines Kunden nutzen, um das beste Erlebnis für jeden Kunden zu ermitteln und so den Geschäftswert zu optimieren. [Weitere Informationen](gs-experience-decisioning.md)

## Warum zu Decisioning migrieren? {#why-migrate}

Decisioning bietet gegenüber dem alten Entscheidungs-Management-Framework erhebliche Funktionen und Vorteile:

### KI- und maschinelle Lernfunktionen

* **Benutzerdefinierte Metriken**: Möglichkeit, benutzerdefinierte Optimierungsmetriken für KI-Modelle zu verwenden. Dies bietet Berichterstellungsinteroperabilität mit [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-overview){target="_blank"}, standardisiert das Reporting auf beiden Plattformen und verbessert die Datenkonsistenz und -zuverlässigkeit. Die nahtlose Integration bietet eine klarere Ansicht der Leistungsmetriken und fügt neue Funktionen hinzu, wie z. B. das Erstellen einfacher Metriken, das Veröffentlichen von Zielgruppen, das Stellen von Ad-hoc-Fragen mit Insight Builder und das Planen von Berichten.

* **Steigerungsmessung**: Möglichkeit, Traffic in KI-Modellen zu visualisieren, zu erkunden oder zu nutzen. Dadurch können Marketing-Experten und Datenwissenschaftler quantifizieren, wie die KI-Exploration die langfristige Modellleistung und die Auffindbarkeit neuer erfolgreicher Angebote verbessert. Transparenz bei der Traffic-Zuordnung schafft Vertrauen in KI-Entscheidungen und ermöglicht es Teams, im Laufe der Zeit sowohl für das Lernen als auch für die Leistung zu optimieren. [Weitere Informationen](ranking/auto-optimization-model.md#lift)

* **AI Formula Builder**: Möglichkeit, KI-Modell-Score-Ausgaben auf vorhandene Formelfunktionen anzuwenden. Dadurch können Marketing-Experten KI-Ausgaben nahtlos mit deterministischen Regeln und Gewichtungen für differenziertere Optimierungsstrategien kombinieren, die Kontrolle und Flexibilität verbessern und gleichzeitig die Intelligenz des maschinellen Lernens nutzen. [Weitere Informationen](ranking/ranking-formulas.md)

### Experimentieren

Möglichkeit zum Experimentieren mit Angeboten, Aspekten eines bestimmten Angebots und/oder Ranking-Methoden. Dadurch können Marketing-Fachleute kontrollierte Experimente zur Kreativ-, Eignungs- und Ranking-Logik durchführen, um leistungsstarke Varianten zu identifizieren, Lernzyklen zu beschleunigen und die kontinuierliche Optimierung des Entscheidungssystems zu fördern.

### Verbessertes Reporting

Dashboard, das die Leistung von Entscheidungselementen und Auswahlstrategien gegenüber Schlüsselelementen der Interaktions-funnel dokumentiert. Ein intuitives Dashboard für vorkonfigurierte Entscheidungen zeigt schnell den Wert der Kampagnen- und Journey-Performance für wichtige KPIs in der Angebots- und Inhaltsbereitstellung, Display- und Klick-Interaktion, Fallback-Nutzungsraten und der Abkehr von KI- und maschinellen Lernranking-Modellen. [Weitere Informationen](cja-reporting.md)

### Betriebseffizienz

* **Sandbox-Kopie**: Möglichkeit zum Kopieren über Objekte zwischen Sandboxes (z. B. „Von Entwicklung nach Produktion„). Dies vereinfacht Bereitstellungs- und Test-Workflows durch die nahtlose Migration von Entscheidungslogik, Angeboten und Konfigurationsobjekten zwischen Umgebungen, wodurch die Einrichtungszeit verkürzt und menschliche Fehler minimiert werden. [Weitere Informationen](../configuration/copy-objects-to-sandbox.md)

* **Schemabasiertes Elementkatalogmanagement**: Möglichkeit zur direkten Definition und Verwaltung von Entscheidungselementen für schemabezogene Datensätze, was dynamische Aktualisierungen und vereinfachte Governance ermöglicht. Dies optimiert die Katalogverwaltung, indem Entscheidungselemente mit zugrunde liegenden Datenquellen synchronisiert werden, die Inhaltsgenauigkeit sichergestellt wird, schnellere Aktualisierungen ermöglicht werden und Governance im großen Maßstab unterstützt wird. [Weitere Informationen](items.md)

* **Standortunabhängige Entscheidungsfindung**: Möglichkeit, Entscheidungslogik über Platzierungen/Standorte hinweg wiederverwendbar zu machen, indem Entscheidungsauswahl und Versand entkoppelt werden. Dies fördert die Wiederverwendbarkeit und Effizienz, da ein einzelnes Entscheidungsmodell für mehrere Platzierungen oder Oberflächen (z. B. Web, App, E-Mail) genutzt werden kann, wodurch die Logik zentralisiert und die Cross-Channel-Personalisierung beschleunigt wird. [Weitere Informationen](placements.md)

* **Wiederverwendbare Inhaltsfragmente**: Möglichkeit, JSON- oder HTML-Inhaltsblöcke (z. B. Titel, Kopfzeilen, Fußzeilen, CTAs) einmal zu definieren und in mehreren Angebotsobjekten darauf zu verweisen. Dies optimiert die Inhaltserstellung und die Governance, indem freigegebene Komponenten zentral verwaltet und in allen Angeboten automatisch aktualisiert werden können. [Weitere Informationen](../content-management/fragments.md)

### Kommende Funktionen

* **Kanalentscheidung** Möglichkeit, mithilfe der Entscheidungslogik den besten Kanal für die Interaktion zu ermitteln (z. B. E-Mail vs. Push vs. Web) und nicht nur das beste Angebot innerhalb eines einzelnen Kanals. Dies verbessert das Kundenerlebnis, indem optimiert wird, wo eine Nachricht zugestellt wird, nicht nur, was zugestellt wird.

* **Nachrichtenoptimierung**: Möglichkeit zur Verwendung von KI oder regelbasierten Ansätzen zur Optimierung des Nachrichteninhalts für jedes Profil, wodurch die Interaktion und Konversionsergebnisse verbessert werden. Dadurch können Marketing-Fachleute Ton, Bilder und Layout dynamisch auf der Grundlage von Zielgruppenattributen und Leistungsdaten anpassen.

* **Journey-Pfadoptimierung**: Möglichkeit, anhand von Experimentergebnissen, Echtzeitkontext, Regeln und/oder Konversionsneigung zu bestimmen, welchem Journey-Pfad ein Profil folgen soll. Auf diese Weise können Teams Profile intelligent durch die optimale Journey-Verzweigung leiten, um für jeden Benutzer die richtige Kadenz und den richtigen Inhalt sicherzustellen.

* **Journey-Entscheidung**: Schlichtung zwischen mehreren Journeys, wenn ein Profil für mehr als ein Profil geeignet ist, um sicherzustellen, dass das wertvollste oder relevanteste Journey ausgewählt wird. Dadurch werden Nachrichtenkonflikte und Übernachrichten vermieden, indem für jedes Profil die höchste Priorität für die Journey ausgewählt wird.

### Zusätzliche Funktionen

* **Richtliniendurchsetzung**: Befähigung von Business-Anwendern zur Verwendung von Funktionen [Datennutzungskennzeichnung und -durchsetzung (DULE)](https://experienceleague.adobe.com/de/docs/experience-platform/data-governance/labels/overview){target="_blank"} und [Einverständnis](../action/consent.md) innerhalb von Decisioning, wodurch der Datenschutz im gesamten Entscheidungs-Workflow gewährleistet wird. Dadurch wird sichergestellt, dass Entscheidungen automatisch die Datennutzungsrichtlinien und die Voreinstellungen für das Kundeneinverständnis berücksichtigen.

* **Native Messaging-Kanal-**: Integriertes Messaging und Entscheidungsfindung innerhalb eines einzigen Frameworks über mehrere Kanäle hinweg: [Code-basiertes Erlebnis](../code-based/get-started-code-based.md), [E-Mail](../email/get-started-email.md) (eingeschränkte Verfügbarkeit), [SMS](../sms/get-started-sms.md) und [Push-Benachrichtigungen](../push/get-started-push.md). Dank der intuitiven Unterstützung der Benutzeroberfläche können Benutzer Entscheidungskomponenten direkt in Workflows zur Nachrichtenerstellung einfügen.

* **Experience Platform-Datensatzsuche**: Möglichkeit zum Hochladen und Referenzieren von [Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/catalog/datasets/overview){target="_blank"}Datensätzen direkt innerhalb der Angebotsauswahlregeln, der Rangfolge und des personalisierten Angebotsinhalts. Dies erhöht die Flexibilität bei Personalisierung und Targeting, da die Entscheidungslogik dynamische externe Datenquellen verwenden kann. [Weitere Informationen](../data/lookup-aep-data.md)

* **Skalierbarkeit und Leistung**: Eine Verbesserung der Architektur, die die Entscheidungsberechnung vom Hub an den Edge verschiebt, wodurch die Latenz erheblich reduziert und der Durchsatz für Anwendungsfälle mit hohem Traffic verbessert wird.

## Beispielhafte Anwendungsfälle {#use-cases}

| Anwendungsfall | Entscheidungs-Management | Entscheidungsfindung |
|----------|---------------------|-------------|
| **Multi-Placement-Strategie** | Entscheidungslogik, die an eine bestimmte Platzierung gebunden ist (z. B. Web- oder E-Mail-Speicherort) | Eine einzige Strategie unterstützt sowohl die Homepage als auch die Mobile App |
| **Konsistente Angebotsattribute** | Jedes Angebot verwaltet seine eigenen Attribute manuell. Keine Konsistenz auf Schemaebene | Marketing-Experten definieren „discountType“ und „offerValue“ einmal; jedes Angebot übernimmt diese Felder automatisch |
| **Dynamische KI-Rangfolge** | Rankings basieren ausschließlich auf Modellausgabe oder statischen Regeln | Ein Marketer kann die Gewichtung anpassen (z. B. 60 % KI-Konversionswert + 40 % Gewinnspanne), um Umsatz- und Interaktionsziele auszugleichen |
| **A/B-Teststrategien** | Keine Unterstützung für integrierte Experimente | Ein Team kann A/B-Tests durchführen, ob „KI + Geschäftsregeln“ die „prioritätsbasierte Rangfolge“ übertreffen |
| **Benutzerdefinierte KI-Metriken** | Wird nur für die Klickneigung optimiert, keine Einblicke in die Modellexploration oder die Steigerung. | Retailer trainiert ein „Likelihood-Kaufmodell“ und überwacht die Steigerung bei neuen und bekannten Produkten |
| **Wiederverwendbarkeit von Inhalten** | Jedes Angebot speichert den gesamten Inhalt unabhängig voneinander | Die Aktualisierung einer Kopfzeile oder CTA wird automatisch an Hunderte von Angeboten weitergegeben |
| **Integriertes Authoring** | Entscheidungsfindung und Messaging sind in separaten Frameworks mit eingeschränkter Integration verfügbar | Ein Marketer fügt personalisierte Angebote in eine E-Mail ein, ohne den Nachrichteneditor verlassen zu müssen |
| **Einhaltung von Datenschutzbestimmungen** | Erfordert manuelle Koordination mit Engineering- und Daten-Teams zur Durchsetzung | Ein Marketer erstellt eine Angebotsregel in dem Wissen, dass Einverständnisvoreinstellungen automatisch bestimmte Profile ausschließen |
| **Echtzeit-Inventar** | Statische Daten; begrenzte Flexibilität bei der Verwendung externer oder kontextueller Datensätze | Verwenden Sie einen Produktinventar-Datensatz, um Angebote für nicht vorrätige Artikel in Echtzeit zu unterdrücken |
| **Skalieren der Leistung** | Entscheidungen, die im Hub mit höherer Latenz getroffen werden | Echtzeit-Personalisierung für Millionen eingehender Anfragen mit einer Reaktionszeit von weniger als 100 ms |

## Migrations-Tools {#migration-tooling}

Ein umfangreicher Satz von **Migrations-Tool-APIs** steht zur Verfügung, um Entscheidungs-Management-Entitäten in das Decisioning zu migrieren. Diese APIs ermöglichen eine nahtlose Migration zwischen Sandboxes mit Funktionen zur automatischen Auflösung von Abhängigkeiten und zum Rollback.

Mit den Migrations-Tool-APIs können Sie:

* **Analysieren von** zwischen Quell- und Ziel-Sandboxes
* **Migration in verschiedenen Bereichen** - Sandbox-, Angebots- oder Entscheidungsebene
* **Rollback-Migrationen** wenn Probleme erkannt werden

Die vollständige API-Dokumentation, einschließlich Authentifizierung, Endpunkte, Anfrage-/Antwortbeispiele und schrittweise Workflows, finden Sie auf [dieser Seite](decisioning-migration-api.md).

## Verwandte Themen {#related-topics}

* [Erste Schritte mit der Entscheidungsfindung](gs-experience-decisioning.md)
* [Leitplanken und Einschränkungen bei Entscheidungen](decisioning-guardrails.md)
* [Häufig gestellte Fragen zu Decisioning](decisioning-faq.md)
