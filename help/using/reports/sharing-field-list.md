---
solution: Journey Optimizer
product: journey optimizer
title: Liste der Step-Ereignisfelder
description: Liste der Step-Ereignisfelder
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 97c1d0f2e9f8100f70d5c4e40325abddc5e3dfbd
workflow-type: ht
source-wordcount: '601'
ht-degree: 100%

---

# Liste der Step-Ereignisfelder {#sharing-field-list}

Die Felder der Step-Ereignisse sind nach Kategorie geordnet.

* Informationsfelder debuggen
* Journey-Felder
* Profilfelder
* Service-Ereignisfelder

Für das Attribut „identityMap“ wird die primäre Identität standardmäßig als „primary = true“ definiert.

## debugInfo {#debuginfo-field}

| Feldname | Typ | Beschreibung |
|---|---|------------|
| requestId | Zeichenfolge | Die von Journey Optimizer verwendete Anfrage-ID, um den Fluss einer Anfrage zu verfolgen. |

## journey {#journey-field}

Diese Feldergruppe wird im Journey-Schema verwendet (in Verbindung mit journeyStepEvent). Es enthält die folgenden Felder:

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Kennung für die angegebene Journey |
| VersionID | Zeichenfolge | Kennung der Journey-Version. Diese Kennung stellt die Identität einer Journey dar |
| name | Zeichenfolge | Name der Journey |
| description | Zeichenfolge | Beschreibung der Journey |
| version | Zeichenfolge | Version, dargestellt als `major`.`minor` |

## profile {#profile-field}

Diese Feldergruppe gilt speziell für journeyStepEvent: Das Ereignis bezieht sich auf die Journey und verfügt nicht über identityMap zur Beschreibung der Profilidentität (sofern vorhanden).

Für journeyStepEvent müssen auch Identitätsfelder hinzugefügt werden:

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Die Profilkennung identifiziert das in einer Journey gesendete/verwendete Profil. Beispiel: foo@adobe.com |
| namespace | Zeichenfolge | In diesem Feld wird der Namespace beschrieben, auf den das in der Journey verwendete Profil verweist. Beispiel: E-Mail, ECID |

## serviceEvents {#servicevents-field}

Dieses Mixin enthält alle Felder, die einem Profilexportvorgang entsprechen.

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Die Kennung des ausgelösten Zielgruppenexportvorgangs |
| status | Zeichenfolge | Der Status des Zielgruppenexportvorgangs: in der Warteschlange, gestartet, abgeschlossen |
| exportCountTotal | Ganzzahl | Der maximale Wert des Zielgruppenexportvorgangs |
| exportCountRealized | Ganzzahl | Die tatsächliche Anzahl von Zielgruppen, die über den Vorgang exportiert wurden |
| exportCountFailed | Ganzzahl | Die Anzahl der Zielgruppen, bei denen der Export durch den Vorgang fehlgeschlagen ist |
| exportSegmentID | Zeichenfolge | Die Kennung der exportierten Zielgruppe |
| eventType | Zeichenfolge | Der Ereignistyp, der angibt, ob es sich um ein Fehlerereignis oder ein Informationsereignis handelt: Info, Fehler |
| eventCode | Zeichenfolge | Der Fehler-Code, der den Grund für den entsprechenden eventType angibt |

Weitere Informationen zu eventTypes finden Sie in [diesem Abschnitt](#discarded-events). 

## stepEvents {#stepevents-field}

Diese Kategorie enthält die ursprünglichen Step-Ereignisfelder. Siehe diesen [Abschnitt](../reports/sharing-legacy-fields.md).


## Fehlerbehebung bei verworfenen Ereignistypen in Journey-Schrittereignissen  {#discarded-events}

Beim Abfragen von Journey-Schrittereignissen nach Einträgen mit `eventCode = 'discard'` können verschiedene eventTypes auftreten.

Im Folgenden finden Sie Definitionen, häufige Ursachen und Schritte zur Fehlerbehebung für die häufigsten `eventTypes`, die verworfen werden:

* **EXTERNAL_KEY_COMPUTATION_ERROR**: Das System konnte keine eindeutige Kennung (externen Schlüssel) für die Kundin bzw. den Kunden aus den Ereignisdaten berechnen.
   * Häufige Ursachen: fehlende oder falsch formatierte Kundenkennungen (z. B. E-Mail-Adresse, Kunden-ID) in der Ereignis-Payload.
   * Fehlerbehebung: Überprüfen Sie die Ereigniskonfiguration auf erforderliche Kennungen und stellen Sie sicher, dass Ereignisdaten vollständig und korrekt formatiert sind.
* **NO_INTERESTED_JOURNEYS_FOR_SEGMENTMEMBERSHIP_EVENT**: Es wurde ein Segmentqualifikationsereignis empfangen, aber es sind keine Journeys konfiguriert, die auf dieses Segment reagieren.
   * Häufige Ursachen: Es gibt keine Journeys, die das Segment als Trigger nutzen, Journeys befinden sich im Status „Entwurf“/„Gestoppt“ oder Segment-IDs stimmen nicht überein.
   * Fehlerbehebung: Stellen Sie sicher, dass mindestens eine Journey live und für das Segment konfiguriert ist, und überprüfen Sie Segment-IDs.
* **JOURNEY_INSTANCE_ID_NOT_CREATE**: Das System konnte keine Journey-Instanz für die Kundin oder den Kunden erstellen.
   * Häufige Ursachen: Duplizierte Ereignisse, großes Ereignisvolumen, Einschränkungen der Systemressourcen.
   * Fehlerbehebung: Implementieren Sie Deduplizierung, vermeiden Sie Traffic-Spitzen, optimieren Sie das Journey-Design. Wenden Sie sich an den Support, wenn das Problem fortbesteht.
* **EVENT_WITH_NO_JOURNEY**: Ein Ereignis wurde empfangen, aber es ist keine aktive Journey konfiguriert, um darauf zu reagieren.
   * Häufige Ursachen: Fehlende Übereinstimmung zwischen Ereignisname und ID, Journey nicht veröffentlicht, falsche Sandbox/Organisation, Testmodus/Testprofil stimmen nicht überein.
   * Fehlerbehebung: Überprüfen Sie die Ereignis- und Journey-Konfiguration, prüfen Sie den Journey-Status, verwenden Sie Debugging-Tools.

Für Verwerfungen, die in pausierten Journeys auftreten:

* **PAUSED_JOURNEY_VERSION**: Verwirft Ereignisse am Eintrittspunkt der Journey
* **JOURNEY_IN_PAUSED_STATE**: Verwirft Ereignisse, wenn Profile in einer Journey sind

Weitere Informationen zu diesen Ereignissen sowie zur Fehlerbehebung finden Sie im Abschnitt [Anhalten einer Journey](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys).

## Weitere Ressourcen

* [Beispiele für Datensatzabfragen – Journey-Schrittereignis](../data/datasets-query-examples.md#journey-step-event).
* [Beispiele für Abfragen – Ereignisbasierte Abfragen](query-examples.md#event-based-queries).
* [Wörterbuch für integrierte Schemata](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de)

