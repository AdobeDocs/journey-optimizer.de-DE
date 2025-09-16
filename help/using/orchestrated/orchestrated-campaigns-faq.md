---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu orchestrierten Kampagnen
description: Häufig gestellte Fragen zu mit Journey Optimizer orchestrierten Kampagnen
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 028f5d506d5fdbd2ed19ad7ded8c1fcd0a391702
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 21%

---

# Häufig gestellte Fragen {#faq-oc}

Im Folgenden finden Sie häufig gestellte Fragen zu mit Adobe Journey Optimizer orchestrierten Kampagnen.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder verbinden Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

## Was ist eine Kampagnenorchestrierung? {#what-are-oc}

Die Kampagnenorchestrierung ist eine Funktion von Journey Optimizer, die ein- oder mehrstufige Workflows unterstützt, welche den relationalen Datenspeicher nutzen, um Zielgruppen für die Batch-Interaktion zu erstellen und zu segmentieren.

Damit steht Journey Optimizer ein neuer Kampagnentyp zur Verfügung: **Orchestrierte Kampagnen**. Mit orchestrierten Kampagnen können Marken komplexe, direkte Marketing-Kampagnen im benötigten Umfang durchführen. Sie sind für markenbezogene Interaktionen konzipiert, z. B. für Werbeaktionen, saisonale Kampagnen oder kontobasierte Kommunikation.

Verglichen mit Einzelversand-/Aktionskampagnen ermöglichen sie **Orchestrierung und Sequenzierung** ausgehendem Marketing: Zielgruppen durchlaufen einen mehrstufigen Workflow gemeinsam, anstatt einen einmaligen Schuss zu erhalten.

## Was kann ich mit einer orchestrierten Kampagne tun? {#what-can-i-do}

Die wichtigsten Funktionen ermöglichen Folgendes:

* **On-Demand-Zielgruppen**: Sofortiges Erstellen und Verfeinern von Zielgruppen mithilfe von relationalen Abfragen.
* **Segmentierung für mehrere Entitäten**: Erstellen präziser Zielgruppen durch die Verknüpfung von Kundendaten mit zugehörigen Entitäten (z. B. Konten, Käufe, Buchungen).
* **Sichtbarkeit vor dem Versand**: Anzeigen der genauen Zielgruppenzahlen vor dem Start, um das Targeting zu optimieren.
* **Mehrstufige Workflows**: Durchführung von sequenziellen Kampagnen wie saisonalen Werbeaktionen, Produkteinführungen oder Treueangeboten.

>[!BEGINSHADEBOX]

**Best Practices**

* Definieren Sie ein **klares Kampagnenziel** bevor Sie Workflows entwerfen.
* Beginnen Sie mit einer **Pilotzielgruppe**, um Zählungen und Logik vor der Skalierung zu überprüfen.
* Halten Sie die Segmentierungsregeln **so einfach wie möglich**, um die Leistung und Transparenz zu optimieren.
* Verwenden Sie **konsistente Benennungskonventionen** für Zielgruppen und Kampagnen, um die Verwaltung zu vereinfachen.

>[!ENDSHADEBOX]

## Wie greife ich auf die Kampagnenorchestrierung zu? {#access-oc}

Für einen Zugriff auf die Kampagnenorchestrierung muss die Lizenz entweder das Paket **Journey Optimizer – Kampagnen und Journeys** oder das Paket **Journey Optimizer – Kampagnen** enthalten. Wenden Sie sich an den Adobe-Support, um Ihre Lizenz zu bestätigen und bei Bedarf zu aktualisieren.

Weitere Informationen zum Lizenzierungsmodell für Campaign Orchestration finden Sie in der [Adobe Journey Optimizer-](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

## Welche Kanäle werden unterstützt? {#channels}

Sie können orchestrierte Kampagnen erstellen, um (E **Mails**, **SMS** und **Push-Benachrichtigungen** zu senden.


>[!BEGINSHADEBOX]

**Recommendations**

* Passen Sie den Kanal an die **Art Ihrer Nachricht** an (z. B. Dringend = SMS, personalisierte Angebote = E-Mail, Kontextuell = Push).
* Überprüfen Sie immer die Einverständnis- und Abonnementvoreinstellungen, bevor Sie einen Kanal aktivieren.
* Testen Sie das Rendern von Nachrichten auf mehreren Geräten und Clients, um ein konsistentes Erlebnis zu gewährleisten.

>[!ENDSHADEBOX]


## Wie unterscheiden sich orchestrierte Kampagnen von Journey? {#oc-vs-journeys}

* **Orchestrierte Kampagnen**: Optimiert für **Batch-, Eins-zu-Viele-**-Kampagnen. Zielgruppen werden in großen Mengen nach einem Zeitplan ausgeführt.
* **Journeys**: Am besten geeignet für **Echtzeit-1:1-Interaktion**. Jede Person durchläuft die Customer Journey in ihrem eigenen Tempo, ausgelöst durch ihr Verhalten oder bestimmte Ereignisse.

>[!BEGINSHADEBOX]

**Best Practice**: Verwenden Sie sie zusammen - Journey für ausgelöste, reaktive Erlebnisse und koordinierte Kampagnen für geplante, kalenderbasierte Initiativen.

>[!ENDSHADEBOX]

## Was ist Segmentierung mehrerer Entitäten? {#multi-entity}

Die Kampagnenorchestrierung in Adobe Journey Optimizer verwendet eine relationale Datenbank. Dieser Typ von Datenmodell verfügt über separate Datenschemata, die über 1- :1 1:many-Beziehungen verbunden sind. Dadurch können Benutzer eine Abfrage für ein beliebiges Schema starten - nicht nur auf Empfängerebene - und dann hin und her zu anderen zugehörigen Schemas wechseln, z. B. Käufe, Produkte, Buchungen oder Empfängerdetails, was eine große Flexibilität bei der Erstellung von Segmenten und Audiences bietet.
Verfeinert.

>[!BEGINSHADEBOX]

**Beispiel** - Targeting aller Empfänger, deren Abonnements in den nächsten 30 Tagen ablaufen. In der Kampagnenorchestrierung kann die Abfrage mit dem Abonnementschema beginnen, nur die Spalte mit dem Ablaufdatum dieses Schemas durchsuchen und alle abgelaufenen Abonnements zurückgeben. Anschließend kann ein Rollup zu den Empfängerdaten durchgeführt werden, die mit diesen spezifischen Abonnement-IDs verknüpft sind und schneller und effizienter Ergebnisse zurückgeben als Datenmodelle, die jede Abfrage auf Empfängerebene starten.

>[!ENDSHADEBOX]


## Wie funktioniert das Datenmodell? {#data-model}

Kampagnen verwenden eine **relationale Datenbank**. Auf diese Weise können Sie Abfragen über verschiedene Datensätze hinweg durchführen (z. B. Kunden, Produkte, Abonnements) und sie für eine erweiterte Segmentierung flexibel verbinden.

>[!BEGINSHADEBOX]

**Best Practices**

* Organisieren Sie Datensätze so, dass **Beziehungen (Joins** Geschäftslogik widerspiegeln.
* Vermeiden Sie unnötige Joins, um die Leistung von Abfragen zu erhalten.
* Validieren Sie die Beispielergebnisse, bevor Sie groß angelegte Extraktionen durchführen.

>[!ENDSHADEBOX]

## Kann ich Nachrichten mit relationalen Daten personalisieren? {#personalization}

Ja. In Campaign Orchestration kann ein als „Personenentität“ bekanntes Empfängerprofil aktualisiert werden und diese Daten können für die Personalisierung verwendet werden. Darüber hinaus können angereicherte Daten aus verknüpften Entitäten in der relationalen Datenbank auch für die Personalisierung verwendet werden. Sie können Kundenprofile zusammen mit verknüpften Daten (wie etwa Käufen oder Abonnements) verwenden, um Inhalte über alle unterstützten Kanäle hinweg zu personalisieren.

>[!BEGINSHADEBOX]

**Recommendations**

* Verwenden Sie **Transaktions- und Verhaltensdaten** um Angebote relevant zu machen.
* Kombinieren Sie **statische Attribute** (z. B. Treuestufe) mit **dynamischen** (z. B. Datum des letzten Kaufs).
* Personalisierung kurz halten - das Überladen von Nachrichten mit Daten kann die Lesbarkeit beeinträchtigen.

>[!ENDSHADEBOX]


## Integrieren sich orchestrierte Kampagnen mit anderen Adobe-Lösungen? {#integrations}

Ja. Die Kampagnenorchestrierung ist nativ mit integriert:

* **Customer Journey Analytics**: Berichte zur Kampagnenorchestrierung sind verfügbar.
* **Real-Time CDP**: In Campaign integrierte Audiences können in Real-Time CDP gelesen werden.
* **Komposition föderierter Zielgruppen (FAC)**: als Add-on verfügbar.

## Was ist mit Berechtigungen und Einverständnis? {#permissions}

Berechtigungen und Einverständnis für orchestrierte Kampagnen und Journey werden in Adobe Experience Platform zentral verwaltet. Diese Einstellungen werden vor dem Versand für beide Lösungen auf jede Empfängerin und jeden Empfänger angewendet.

>[!BEGINSHADEBOX]

**Best Practices**

* Wenden Sie **zentralisierte Governance** an und vermeiden Sie die separate Einverständnisverwaltung auf Kampagnenebene.
* Prüfen Sie die Einverständnisdaten regelmäßig, um Inkonsistenzen zu erkennen.
* Respekt **kanalspezifische Opt-outs** — gehen Sie nicht davon aus, dass die globale Zustimmung alle Kanäle abdeckt.

>[!ENDSHADEBOX]

## Kann ich Ad-hoc-Segmentierung in orchestrierten Kampagnen durchführen? {#ad-hoc}

In der Kampagnenorchestrierung wird die Ad-hoc-Segmentierung als „Live-Segmentierung“ bezeichnet, bei der Sie in Echtzeit auf alle im relationalen Speicher verfügbaren Daten zugreifen, eine komplexe Abfrage darauf erstellen und das Ergebnis für eine sofortige Aktivierung über ausgehende Kanäle erhalten können (z. B. E-Mail + SMS).

>[!BEGINSHADEBOX]

**Tipps**

* Ad-hoc-Segmentierung für **zeitkritische Anforderungen** (z. B. Flash-Werbeaktionen) verwenden.
* Speichern und dokumentieren Sie nützliche Abfragen, damit sie in zukünftigen Kampagnen wiederverwendet werden können.
* Überprüfen Sie vor der Aktivierung die Anzahl der Zielgruppen, um zu verhindern, dass der Versand zu hoch oder zu hoch ausfällt.

>[!ENDSHADEBOX]



## Unterstützen orchestrierte Kampagnen die Entscheidungsfindung? {#decisioning}

Ja. Entscheidungsfindung kann relationale Daten aus orchestrierten Kampagnen verwenden. Sobald ein relationales Schema mit XDM-Schemata verbunden ist, können XDM-Daten bei der Entscheidungsfindung verwendet werden.

## Wie funktioniert die Bereitstellung in allen Umgebungen? {#deployment}

Objekte, die in orchestrierten Kampagnen erstellt werden (z. B. Zielgruppen, Workflows), sind an die Sandbox gebunden, in der sie erstellt werden. Standardmäßige Verpackungs- und Bereitstellungs-Workflows in Umgebungen (Entwicklung, Staging, Produktion) sind derzeit nicht für koordinierte Kampagnen verfügbar.

>[!BEGINSHADEBOX]

**Best Practices**

* **separate Sandboxes** für Experimente, Qualitätssicherung und Produktion verwalten.
* Dokumentenkonfigurationen sollten sorgfältig konfiguriert werden, um bei Bedarf eine manuelle Replikation zu ermöglichen.
* Abstimmung mit Governance-Teams, um Konfigurationsabweichungen zwischen Umgebungen zu reduzieren

>[!ENDSHADEBOX]

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->


>[!MORELIKETHIS]
>
>* [Leitplanken und Einschränkungen für koordinierte Kampagnen](../orchestrated/guardrails.md)
>* [Erste Schritte mit Schemata und Datensätzen in orchestrierten Kampagnen](../orchestrated/gs-schemas.md)
>* [Erstellen Sie Ihre erste orchestrierte Kampagne](../orchestrated/gs-campaign-creation.md)
>* [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
