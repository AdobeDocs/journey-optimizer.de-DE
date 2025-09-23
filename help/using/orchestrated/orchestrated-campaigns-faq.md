---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu orchestrierten Kampagnen
description: Häufig gestellte Fragen zu mit Journey Optimizer orchestrierten Kampagnen
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 15%

---

# Häufig gestellte Fragen {#faq-oc}

Im Folgenden finden Sie häufig gestellte Fragen zu mit Adobe Journey Optimizer orchestrierten Kampagnen.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder verbinden Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}.

+++ Was ist eine Kampagnenorchestrierung?

Die Kampagnenorchestrierung ist eine Funktion von Journey Optimizer, die ein- oder mehrstufige Workflows unterstützt, welche den relationalen Datenspeicher nutzen, um Zielgruppen für die Batch-Interaktion zu erstellen und zu segmentieren.

Damit steht Journey Optimizer ein neuer Kampagnentyp zur Verfügung: **Orchestrierte Kampagnen**. Mit orchestrierten Kampagnen können Marken komplexe, direkte Marketing-Kampagnen im benötigten Umfang durchführen. Sie sind für markenbezogene Interaktionen konzipiert, z. B. für Werbeaktionen, saisonale Kampagnen oder kontobasierte Kommunikation.

Verglichen mit Einzelversand-/Aktionskampagnen ermöglichen sie **Orchestrierung und Sequenzierung** ausgehendem Marketing: Zielgruppen durchlaufen einen mehrstufigen Workflow gemeinsam, anstatt einen einmaligen Schuss zu erhalten.

+++

+++ Was kann ich mit einer orchestrierten Kampagne tun?

Die wichtigsten Funktionen ermöglichen Folgendes:

* **On-Demand-Zielgruppen**: Sofortiges Erstellen und Verfeinern von Zielgruppen mithilfe von relationalen Abfragen.
* **Segmentierung für mehrere Entitäten**: Erstellen präziser Zielgruppen durch die Verknüpfung von Kundendaten mit zugehörigen Entitäten (z. B. Konten, Käufe, Buchungen).
* **Sichtbarkeit vor dem Versand**: Anzeigen der genauen Zielgruppenzahlen vor dem Start, um das Targeting zu optimieren.
* **Mehrstufige Workflows**: Durchführung von sequenziellen Kampagnen wie saisonalen Werbeaktionen, Produkteinführungen oder Treueangeboten.

**Best Practices**

* Definieren Sie ein **klares Kampagnenziel** bevor Sie Workflows entwerfen.
* Beginnen Sie mit einer **Pilotzielgruppe**, um Zählungen und Logik vor der Skalierung zu überprüfen.
* Halten Sie die Segmentierungsregeln **so einfach wie möglich**, um die Leistung und Transparenz zu optimieren.
* Verwenden Sie **konsistente Benennungskonventionen** für Zielgruppen und Kampagnen, um die Verwaltung zu vereinfachen.

+++

+++ Wie greife ich auf die Kampagnenorchestrierung zu?

Für einen Zugriff auf die Kampagnenorchestrierung muss die Lizenz entweder das Paket **Journey Optimizer – Kampagnen und Journeys** oder das Paket **Journey Optimizer – Kampagnen** enthalten. Wenden Sie sich an den Adobe-Support, um Ihre Lizenz zu bestätigen und bei Bedarf zu aktualisieren.

Weitere Informationen zum Lizenzierungsmodell für Campaign Orchestration finden Sie in der [Adobe Journey Optimizer-](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++ Wie unterscheiden sich orchestrierte Kampagnen von Journey?

* **Orchestrierte Kampagnen**: Optimiert für **Batch-, Eins-zu-Viele-**-Kampagnen. Zielgruppen werden in großen Mengen nach einem Zeitplan ausgeführt.
* **Journeys**: Am besten geeignet für **Echtzeit-1:1-Interaktion**. Jede Person durchläuft die Customer Journey in ihrem eigenen Tempo, ausgelöst durch ihr Verhalten oder bestimmte Ereignisse.

**Best Practice**: Verwenden Sie sie zusammen - Journey für ausgelöste, reaktive Erlebnisse und koordinierte Kampagnen für geplante, kalenderbasierte Initiativen.


+++

+++ Was ist Segmentierung mehrerer Entitäten?

Die Kampagnenorchestrierung in Adobe Journey Optimizer verwendet eine relationale Datenbank. Dieser Typ von Datenmodell verfügt über separate Datenschemata, die über 1- :1 1:many-Beziehungen verbunden sind. Dadurch können Benutzer eine Abfrage für ein beliebiges Schema starten - nicht nur auf Empfängerebene - und dann hin und her zu anderen zugehörigen Schemas wechseln, z. B. Käufe, Produkte, Buchungen oder Empfängerdetails, was eine große Flexibilität bei der Erstellung von Segmenten und Audiences bietet.
Verfeinert.


**Beispiel** - Targeting aller Empfänger, deren Abonnements in den nächsten 30 Tagen ablaufen. In der Kampagnenorchestrierung kann die Abfrage mit dem Abonnementschema beginnen, nur die Spalte mit dem Ablaufdatum dieses Schemas durchsuchen und alle abgelaufenen Abonnements zurückgeben. Anschließend kann ein Rollup zu den Empfängerdaten durchgeführt werden, die mit diesen spezifischen Abonnement-IDs verknüpft sind und schneller und effizienter Ergebnisse zurückgeben als Datenmodelle, die jede Abfrage auf Empfängerebene starten.

+++

+++ Wie funktioniert das Datenmodell?

Kampagnen verwenden eine **relationale Datenbank**. Auf diese Weise können Sie Abfragen über verschiedene Datensätze hinweg durchführen (z. B. Kunden, Produkte, Abonnements) und sie für eine erweiterte Segmentierung flexibel verbinden.

**Best Practices**

* Organisieren Sie Datensätze so, dass **Beziehungen (Joins** Geschäftslogik widerspiegeln.
* Vermeiden Sie unnötige Joins, um die Leistung von Abfragen zu erhalten.
* Validieren Sie die Beispielergebnisse, bevor Sie groß angelegte Extraktionen durchführen.


+++

+++ Kann ich Nachrichten mit relationalen Daten personalisieren?

Ja. In Campaign Orchestration kann ein als „Personenentität“ bekanntes Empfängerprofil aktualisiert werden und diese Daten können für die Personalisierung verwendet werden. Darüber hinaus können angereicherte Daten aus verknüpften Entitäten in der relationalen Datenbank auch für die Personalisierung verwendet werden. Sie können Kundenprofile zusammen mit verknüpften Daten (wie etwa Käufen oder Abonnements) verwenden, um Inhalte über alle unterstützten Kanäle hinweg zu personalisieren.


**Recommendations**

* Verwenden Sie **Transaktions- und Verhaltensdaten** um Angebote relevant zu machen.
* Kombinieren Sie **statische Attribute** (z. B. Treuestufe) mit **dynamischen** (z. B. Datum des letzten Kaufs).
* Personalisierung kurz halten - das Überladen von Nachrichten mit Daten kann die Lesbarkeit beeinträchtigen.


+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Welche Kanäle werden unterstützt?

Sie können orchestrierte Kampagnen erstellen, um (E **Mails**, **SMS** und **Push-Benachrichtigungen** zu senden.

+++

+++ Können mehrere Kommunikationen und verschiedene Kanäle innerhalb derselben orchestrierten Kampagne gestartet werden?

Ja, orchestrierte Kampagnen unterstützen eine kanalübergreifende Orchestrierung.

+++

+++ Sind orchestrierte Kampagnenvorlagen verfügbar?

Nein, Sie können keine Kampagnenvorlagen definieren oder verwenden. Sie können jedoch Inhaltsvorlagen für Ihre Kommunikation verwenden.

+++

+++ Ist der Content Designer für Nachrichten spezifisch für orchestrierte Kampagnen?

Nein, Content Designer einschließlich E-Mail-Designer ist in allen Funktionen von Journey Optimizer gleich.

+++

+++ Wie sind die verschiedenen Kanäle in orchestrierten Kampagnen verbunden?

Die Kanalkomponente und die Laufzeitumgebung sind in allen Journey Optimizer-Kampagnen vorhanden. Die unterstützten Kanäle unterscheiden sich jedoch.

+++


+++ Können sich orchestrierte Kampagnen mit ausgehenden Kanälen (Web, InApp) verbinden?

Nein, ausgehende Kanäle werden in koordinierten Kampagnen nicht unterstützt.

+++

+++ Was ist mit Berechtigungen und Einverständnis?

Berechtigungen und Einverständnis für orchestrierte Kampagnen und Journey werden in Adobe Experience Platform zentral verwaltet. Diese Einstellungen werden vor dem Versand für beide Lösungen auf jede Empfängerin und jeden Empfänger angewendet.


**Best Practices**

* Wenden Sie **zentralisierte Governance** an und vermeiden Sie die separate Einverständnisverwaltung auf Kampagnenebene.
* Prüfen Sie die Einverständnisdaten regelmäßig, um Inkonsistenzen zu erkennen.
* Respekt **kanalspezifische Opt-outs** — gehen Sie nicht davon aus, dass die globale Zustimmung alle Kanäle abdeckt.

+++


+++ Kann ich Ad-hoc-Segmentierung in orchestrierten Kampagnen durchführen?

In der Kampagnenorchestrierung wird die Ad-hoc-Segmentierung als „Live-Segmentierung“ bezeichnet, bei der Sie in Echtzeit auf alle im relationalen Speicher verfügbaren Daten zugreifen, eine komplexe Abfrage darauf erstellen und das Ergebnis für eine sofortige Aktivierung über ausgehende Kanäle erhalten können (z. B. E-Mail + SMS).


**Tipps**

* Ad-hoc-Segmentierung für **zeitkritische Anforderungen** (z. B. Flash-Werbeaktionen) verwenden.
* Speichern und dokumentieren Sie nützliche Abfragen, damit sie in zukünftigen Kampagnen wiederverwendet werden können.
* Überprüfen Sie vor der Aktivierung die Anzahl der Zielgruppen, um zu verhindern, dass der Versand zu hoch oder zu hoch ausfällt.

+++


+++ Greift Campaign Orchestration nur auf Daten zu, die über Batch geladen werden, oder kann es auch aktualisierte Echtzeit-Tabellen (wie Analytics-Daten) abfragen?

Journey Optimizer Campaign Orchestration kann zunächst eine Ad-hoc-Abfrage auf Basis modellbasierter Schemata erstellen. Modellbasierte Schemata unterstützen derzeit nur Batch-Quellen. Darüber hinaus unterstützt sie „Zielgruppe lesen“ aus jeder Art von Adobe Experience Platform-Zielgruppe.

+++

+++ Unterstützen orchestrierte Kampagnen die Entscheidungsfindung?

Ja. Entscheidungsfindung kann relationale Daten aus orchestrierten Kampagnen verwenden. Sobald modellbasierte Schemata mit XDM-Schemata verbunden sind, können XDM-Daten bei der Entscheidungsfindung verwendet werden.

+++


+++ Wie funktioniert die Bereitstellung in allen Umgebungen?

Objekte, die in orchestrierten Kampagnen erstellt werden (z. B. Zielgruppen, Workflows), sind an die Sandbox gebunden, in der sie erstellt werden. Standardmäßige Verpackungs- und Bereitstellungs-Workflows in Umgebungen (Entwicklung, Staging, Produktion) sind derzeit nicht für koordinierte Kampagnen verfügbar.

**Best Practices**

* **separate Sandboxes** für Experimente, Qualitätssicherung und Produktion verwalten.
* Dokumentenkonfigurationen sollten sorgfältig konfiguriert werden, um bei Bedarf eine manuelle Replikation zu ermöglichen.
* Abstimmung mit Governance-Teams, um Konfigurationsabweichungen zwischen Umgebungen zu reduzieren

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Welche Beziehung besteht zwischen Empfänger- und Profilentitäten?

Die Segmentierung wird für Empfängerinnen und Empfänger beim Versand über das Adobe Experience Platform-Profil durchgeführt. Die Zielgruppendimension „Empfänger“ erweitert das einheitliche Profil um zusätzliche Daten, die für die Segmentierung in orchestrierten Kampagnen verwendet werden, während „Empfänger“ zur Laufzeit mit dem Profil abgeglichen wird, um Nachrichten zu senden und die Einverständnisrichtlinie und die Geschäftsregeln zu überprüfen. Diese Abstimmung ist nützlich, um Geschäftsregeln und Einverständnisanträge auf Profilebene zu vereinheitlichen

![](assets/recipients-and-profiles.png)

+++

+++ In welchen Fällen wird die Verwendung von Empfänger- und Profilentitäten empfohlen?

Wenn Sie mit „Ja“ antworten, wird der beste Datenspeicher vorgeschlagen. Bestätigen Sie jedoch immer den besten Ansatz basierend auf Ihrem Anwendungsfall und den Einschränkungen mit Ihrem Adobe-Support-Mitarbeiter.

| relationaler Speicher | Echtzeit-Kundenprofil |
|---------|----------|
| Ist die Quelle der Daten bereits relational? | Ist die Quelle des Daten-Streaming? |
| Beabsichtigen Sie, Daten direkt für Marketing-Anwendungsfälle zu erfassen? | Ist die Datenfrische eine wichtige Anforderung? |
| Gibt es eine große Menge an historischen Daten (`>` 2 Monate), die für Anwendungsfälle der Marketing-Aktivierung benötigt werden? | Gibt es Szenarien, in denen aktuelle Aktionen oder Entscheidungen Daten erfordern? |
| Gibt es Ad-hoc-Anforderungen für die Erstellung, Auswertung und Aktivierung von Zielgruppen? | Können die Verhaltensdaten mithilfe vorberechneter Aggregate auf `<` 90 Tage beschränkt werden? |
|  | Sind Daten erforderlich, um Nachrichten in Echtzeit zu personalisieren? |

+++

+++ Wie viele Aktivitäten sind pro orchestrierter Kampagne maximal zulässig?

Die Anzahl der Aktivitäten in einer orchestrierten Kampagne ist auf 500 begrenzt.

+++

+++ Ist es möglich, Anreicherungen durchzuführen, um zusätzliche Daten hinzuzufügen?

Ja, Sie können Daten aus dem relationalen Speicher und aus Adobe Experience Platform-Zielgruppen anreichern.

+++

+++ Müssen alle Filter über Zielgruppen definiert werden, oder kann ein bestimmter Filtertyp konfiguriert werden?

Orchestrierte Kampagnen unterstützen vordefinierte Filter: Sie können eine Abfrage definieren und als Filter speichern und zu Ihren Favoriten hinzufügen, um sie für weitere Segmentierungsaufgaben wiederzuverwenden.

+++


## Weitere Ressourcen

Weitere Informationen und Aktualisierungen finden Sie in den folgenden Ressourcen:

* [Leitplanken und Einschränkungen für koordinierte Kampagnen](../orchestrated/guardrails.md)
* [Erste Schritte mit Schemata und Datensätzen in orchestrierten Kampagnen](../orchestrated/gs-schemas.md)
* [Erstellen der ersten orchestrierten Kampagne](../orchestrated/gs-campaign-creation.md)
* [Produktbeschreibung zu Journey Optimizer](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
