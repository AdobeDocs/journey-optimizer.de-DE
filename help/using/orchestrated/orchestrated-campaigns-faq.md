---
solution: Journey Optimizer
product: journey optimizer
title: Häufig gestellte Fragen zu orchestrierten Kampagnen
description: Häufig gestellte Fragen zu mit Journey Optimizer orchestrierten Kampagnen
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: e63fd5dc50100000a810e2dfcb8c8e8827628b0c
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 4%

---

# Häufig gestellte Fragen {#faq-oc}

Im Folgenden finden Sie häufig gestellte Fragen zu mit Adobe Journey Optimizer orchestrierten Kampagnen.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen.

## Was sind orchestrierte Kampagnen? {#what-are-oc}

Orchestrierte Kampagnen in Adobe Journey Optimizer helfen Marken dabei, skaliert komplexe, direkte Marketing-Kampagnen durchzuführen. Sie sind für markeninitiierte Interaktionen konzipiert, z. B. für Werbeaktionen, saisonale Kampagnen oder Account-basierte Kommunikation.

Verglichen mit Einzelversand-Kampagnen ermöglichen sie **Orchestrierung und Sequenzierung** ausgehendes Marketing: Zielgruppen durchlaufen einen mehrstufigen Workflow gemeinsam, anstatt einen einmaligen Schlag zu erhalten.

## Was kann ich mit orchestrierten Kampagnen tun? {#what-can-i-do}

Die wichtigsten Funktionen ermöglichen Folgendes:

* **On-Demand-Zielgruppen**: Zielgruppen mithilfe von relationalen Abfragen sofort erstellen und verfeinern.
* **Segmentierung mehrerer Entitäten**: Erstellen Sie präzise Zielgruppen, indem Sie Kundendaten mit verwandten Entitäten (z. B. Konten, Käufen, Buchungen) verbinden.
* **Sichtbarkeit vor dem Versand**: Zur Optimierung der Zielgruppenbestimmung ist die genaue Anzahl der Zielgruppen vor dem Start anzuzeigen.
* **Mehrstufige Workflows**: Führen Sie sequenzielle Kampagnen wie saisonale Werbeaktionen, Produkteinführungen oder Treueangebote aus.

>[!BEGINSHADEBOX]

**Best Practices**

* Definieren Sie ein **klares Kampagnenziel** bevor Sie Workflows entwerfen.
* Beginnen Sie mit einer **Pilotzielgruppe**, um Zählungen und Logik vor der Skalierung zu überprüfen.
* Halten Sie die Segmentierungsregeln **so einfach wie möglich**, um die Leistung und Transparenz zu optimieren.
* Verwenden Sie **konsistente Benennungskonventionen** für Zielgruppen und Kampagnen, um die Verwaltung zu vereinfachen.

>[!ENDSHADEBOX]


## Welche Kanäle werden unterstützt? {#channels}

Orchestrierte Kampagnen unterstützen **E-Mail, SMS und Push-Benachrichtigungen**.


>[!BEGINSHADEBOX]

**Recommendations**

* Passen Sie den Kanal an die **Art Ihrer Nachricht** an (z. B. Dringend = SMS, personalisierte Angebote = E-Mail, Kontextuell = Push).
* Überprüfen Sie immer die Einverständnis- und Abonnementvoreinstellungen, bevor Sie einen Kanal aktivieren.
* Testen Sie das Rendern von Nachrichten auf mehreren Geräten und Clients, um ein konsistentes Erlebnis zu gewährleisten.

>[!ENDSHADEBOX]


## Wie unterscheiden sich orchestrierte Kampagnen von Journey? {#oc-vs-journeys}

* **Orchestrierte Kampagnen**: Optimiert für **Batch-, Eins-zu-Viele-**-Kampagnen. Ganze Zielgruppen durchlaufen die Kampagnen-Arbeitsfläche gemeinsam.
* **Journey**: Am besten geeignet für **Echtzeit-, Eins-zu-eins-**-Interaktion. Jeder Kunde bewegt sich in seinem eigenen Tempo durch die Journey, ausgelöst durch Verhalten oder Ereignisse.

>[!BEGINSHADEBOX]

**Tipp** - Viele Unternehmen verwenden **beides zusammen** Journey für ausgelöste, reaktive Erlebnisse und koordinierte Kampagnen für geplante, kalenderbasierte Initiativen.

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

## Kann ich Nachrichten mit diesen Daten personalisieren? {#personalization}

Ja. In Campaign Orchestration kann ein als „Personenentität“ bekanntes Empfängerprofil aktualisiert werden und diese Daten können für die Personalisierung verwendet werden. Darüber hinaus können angereicherte Daten aus verknüpften Entitäten in der relationalen Datenbank auch für die Personalisierung verwendet werden. Sie können Kundenprofile zusammen mit verknüpften Daten (wie Käufen oder Abonnements) verwenden, um Inhalte über alle unterstützten Kanäle hinweg zu personalisieren.

>[!BEGINSHADEBOX]

**Recommendations**

* Verwenden Sie **Transaktions- und Verhaltensdaten** um Angebote relevant zu machen.
* Kombinieren Sie **statische Attribute** (z. B. Treuestufe) mit **dynamischen** (z. B. Datum des letzten Kaufs).
* Personalisierung kurz halten - das Überladen von Nachrichten mit Daten kann die Lesbarkeit beeinträchtigen.

>[!ENDSHADEBOX]


## Kann diese Lösung mit anderen Adobe-Lösungen integriert werden? {#integrations}

Ja. Die Kampagnenorchestrierung ist nativ mit integriert:

* **Customer Journey Analytics**: Berichte zur Kampagnenorchestrierung sind verfügbar.
* **Real-Time CDP**: In Campaign integrierte Audiences können in Real-Time CDP gelesen werden.
* **Federated Audience Composition (FAC)**: als Add-on verfügbar.

## Was ist mit Berechtigungen und Einverständnis? {#permissions}

Berechtigungen und Einverständnis für orchestrierte Kampagnen und Journey werden in Adobe Experience Platform zentral verwaltet. Diese Einstellungen werden vor dem Versand für beide Lösungen auf jede Empfängerin und jeden Empfänger angewendet.

>[!BEGINSHADEBOX]

**Best Practices**

* Wenden Sie **zentralisierte Governance** an und vermeiden Sie die separate Einverständnisverwaltung auf Kampagnenebene.
* Prüfen Sie die Einverständnisdaten regelmäßig, um Inkonsistenzen zu erkennen.
* Respekt **kanalspezifische Opt-outs** — gehen Sie nicht davon aus, dass die globale Zustimmung alle Kanäle abdeckt.

>[!ENDSHADEBOX]

## Kann ich eine Ad-hoc-Segmentierung vornehmen? {#ad-hoc}

In der Kampagnenorchestrierung wird die Ad-hoc-Segmentierung als „Live-Segmentierung“ bezeichnet, bei der Sie in Echtzeit auf alle im relationalen Speicher verfügbaren Daten zugreifen, eine komplexe Abfrage darauf erstellen und das Ergebnis für eine sofortige Aktivierung über ausgehende Kanäle erhalten können (z. B. E-Mail + SMS).

>[!BEGINSHADEBOX]

**Tipps**

* Ad-hoc-Segmentierung für **zeitkritische Anforderungen** (z. B. Flash-Werbeaktionen) verwenden.
* Speichern und dokumentieren Sie nützliche Abfragen, damit sie in zukünftigen Kampagnen wiederverwendet werden können.
* Überprüfen Sie vor der Aktivierung die Anzahl der Zielgruppen, um zu verhindern, dass der Versand zu hoch oder zu hoch ausfällt.

>[!ENDSHADEBOX]


## Unterstützt dies die Entscheidungsfindung? {#decisioning}

Derzeit verwendet Decisioning keine relationalen Daten aus orchestrierten Kampagnen.

## Wie funktioniert die Bereitstellung in allen Umgebungen? {#deployment}

Objekte, die in orchestrierten Kampagnen erstellt werden (z. B. Zielgruppen, Workflows), sind an die Sandbox gebunden, in der sie erstellt werden. Standardmäßige Verpackungs- und Bereitstellungs-Workflows in Umgebungen (Entwicklung, Staging, Produktion) sind derzeit nicht für koordinierte Kampagnen verfügbar.

>[!BEGINSHADEBOX]

**Best Practices**

* **separate Sandboxes** für Experimente, Qualitätssicherung und Produktion verwalten.
* Dokumentenkonfigurationen sollten sorgfältig konfiguriert werden, um bei Bedarf eine manuelle Replikation zu ermöglichen.
* Abstimmung mit Governance-Teams, um Konfigurationsabweichungen zwischen Umgebungen zu reduzieren

>[!ENDSHADEBOX]

## Gibt es empfohlene Vorgehensweisen zum Ausführen von Kampagnen in großem Umfang? {#scale}

Ja, befolgen Sie die folgenden Best Practices:

* **Planen Sie Kampagnen rund um Geschäftskalender** (Produkteinführungen, saisonale Spitzen), um Volumen und Ressourcen aufeinander abzustimmen.
* Verwenden Sie **Zielgruppenvorschauen** vor dem Versand, um die erwartete Größe zu bestätigen und Überraschungen zu vermeiden.
* Staffeln Sie **Sendezeiten** um zu vermeiden, dass nachgelagerte Systeme (z. B. Callcenter, Websites) überlastet werden.
* Richten Sie eine **Überwachungsroutine** ein - verfolgen Sie Versandlogs, Fehlerquoten und Opt-outs nach jedem Versand.
* Führen Sie **Analyse nach der Kampagne** in Customer Journey Analytics aus, um das Targeting und die Orchestrierung für den nächsten Zyklus zu verfeinern.



>[!MORELIKETHIS]
>
>* [Leitplanken und Einschränkungen für koordinierte Kampagnen](../orchestrated/guardrails.md)
>* [Erste Schritte mit Schemata und Datensätzen in orchestrierten Kampagnen](../orchestrated/gs-schemas.md)
>* [Erstellen Sie Ihre erste orchestrierte Kampagne](../orchestrated/gs-campaign-creation.md)
>* [Journey Optimizer-Produktbeschreibung](https://helpx.adobe.com/de/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
