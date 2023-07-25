---
solution: Journey Optimizer
product: journey optimizer
title: Liste der Step-Ereignisfelder
description: Liste der Step-Ereignisfelder
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 100%

---

# Liste der Step-Ereignisfelder {#sharing-field-list}

Die Felder der Step-Ereignisse sind nach Kategorie geordnet.

* Informationsfelder debuggen
* Journey-Felder
* Profilfelder
* Service-Ereignisfelder

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

Diese Feldergruppe gilt speziell für „journeyStepEvent“: Das Ereignis bezieht sich auf die Journey und verfügt nicht über „identityMap“ zur Beschreibung der Profilidentität (sofern vorhanden).

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
| eventType | Zeichenfolge | Der Ereignistyp, der angibt, ob es sich um ein Fehlerereignis eines Informationsereignisses handelt: Info, Fehler |
| eventCode | Zeichenfolge | Der Fehler-Code, der den Grund für den entsprechenden eventType angibt |

## stepEvents {#stepevents-field}

Diese Kategorie enthält die ursprünglichen Step-Ereignisfelder. Siehe diesen [Abschnitt](../reports/sharing-legacy-fields.md).
