---
solution: Journey Optimizer
product: journey optimizer
title: Schrittereignisfeldliste
description: Schrittereignisfeldliste
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e96efa67-ee47-40b9-b680-f5119d8c3481
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Schrittereignisfeldliste {#sharing-field-list}

Die Felder der Schrittereignisse sind nach Kategorie geordnet.

* Informationsfelder debuggen
* Journey-Felder
* Profilfelder
* Dienstereignisfelder

## debugInfo {#debuginfo-field}

| Feldname | Typ | Beschreibung |
|---|---|------------|
| requestId | Zeichenfolge | Die von Journey Optimizer verwendete Anfrage-ID zum Verfolgen des Anfrageflusses. |

## Journey {#journey-field}

Diese Feldergruppe wird im Journey-Schema verwendet (im Zusammenhang mit journeyStepEvent). Sie enthält die folgenden Felder:

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Kennung für die jeweilige Journey |
| VersionID | Zeichenfolge | Kennung der Journey-Version. Diese ID stellt die Identität einer Journey dar. |
| name | Zeichenfolge | Name der Journey |
| description | Zeichenfolge | Beschreibung der Journey |
| version | Zeichenfolge | Version, dargestellt als `major`.`minor` |

## profile {#profile-field}

Diese Feldergruppe ist spezifisch für journeyStepEvent: Dieses Ereignis steht im Zusammenhang mit der Journey und verfügt nicht über die identityMap, die die Profilidentität beschreibt (sofern vorhanden).

Für journeyStepEvent müssen auch Identitätsfelder hinzugefügt werden:

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Die Profilkennung identifiziert das Profil, das in einer Journey gesendet/verwendet wird. Beispiel: foo@adobe.com |
| namespace | Zeichenfolge | In diesem Feld wird der Namespace beschrieben, auf den das in der Journey verwendete Profil verweist. Beispiel: E-Mail, ECID |

## serviceEvents {#servicevents-field}

Dieses Mixin enthält alle Felder, die einem Profilexport-Auftrag entsprechen.

| Feldname | Typ | Beschreibung |
|---|---|------------|
| ID | Zeichenfolge | Die Kennung des vom Segmentexport ausgelösten Auftrags |
| status | Zeichenfolge | Der Status des Segmentexportauftrags: in die Warteschlange gestellt, gestartet, fertig gestellt |
| exportCountTotal | Ganzzahl | Der maximale Wert des Segmentexportauftrags |
| exportCountRealized | Ganzzahl | Die tatsächliche Anzahl von Segmenten, die über den Auftrag exportiert wurden |
| exportCountFailed | Ganzzahl | Die Anzahl der Segmente, die beim Exportieren durch den Auftrag fehlgeschlagen sind |
| exportSegmentID | Zeichenfolge | Die Kennung des zu exportierenden Segments |
| eventType | Zeichenfolge | Der Ereignistyp, der angibt, ob es sich um ein Fehlerereignis von info -Ereignis handelt: Info, Fehler |
| eventCode | Zeichenfolge | Der Fehlercode, der den Grund für den entsprechenden eventType angibt |

## stepEvents {#stepevents-field}

Diese Kategorie enthält die Felder für das ursprüngliche Schrittereignis. Siehe hierzu [Abschnitt](../reports/sharing-legacy-fields.md).
