---
title: Platzierungs-Datensatz
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Platzierungen verwendet werden
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Platzierungs-Datensatz {#placements-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für Platzierungen aktualisiert.

![](../assets/dataset-placements.png)

Der zuletzt erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>Erfahren Sie, wie Sie für jedes Objekt Ihrer Angebotsbibliothek in auf die exportierten Datensätze zugreifen können. [diesem Abschnitt](../export-catalog/access-dataset.md).

Im Folgenden finden Sie eine Liste aller Felder, die im **[!UICONTROL Decision Object Repository - Placements]** Datensatz.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Kennung {#identifier}

**Feld:** _id
**Titel:** Kennung
**Beschreibung:** Eine eindeutige Kennung für den Datensatz.
**Typ:** Zeichenfolge

## _experience {#experience}

**Feld:** _experience
**Typ:** Objekt

### _experience > decisioning

**Feld:** Entscheidungsfindung
**Typ:** Objekt

#### _experience > decisioning > Platzierungs-Kanalkennung

**Feld:** channelID
**Titel:** Kanalkennung der Platzierung
**Beschreibung:** Der Kanal, in dem der Vorschlag gemacht wurde. Der Wert ist ein gültiger Kanal-URI. Siehe https://ns.adobe.com/xdm/channels/channel.
**Typ:** Zeichenfolge

#### _experience > decisioning > Content Component Type

**Feld:** componentType
**Titel:** Content Component Type
**Beschreibung:** Ein Auflistungssatz von URIs, bei dem jeder Wert einem Typ zugeordnet ist, der der Inhaltskomponente angegeben ist. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der @type-Wert ein Verweis auf ein Schema ist, das zusätzliche Eigenschaften der Inhaltskomponente beschreibt.
**Typ:** Zeichenfolge

#### _experience > decisioning > contentTypes

**Feld:** contentTypes
**Typ:** array

**_experience > decisioning > contentTypes > MIME Media Type**

**Titel:** MIME-Medientyp
**Beschreibung:** Eine Einschränkung für den Medientyp der Komponenten, die in dieser Platzierung erwartet werden. Für eine Komponente kann es mehrere Medientypen geben, z. B. unterschiedliche Bildformate.
**Typ:** Zeichenfolge

#### _experience > decisioning > Placement Description

**Feld:** description
**Titel:** Platzierungsbeschreibung
**Beschreibung:** Sie wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie dynamischer Inhalt im übergeordneten Nachrichtenversand verwendet wird. Dass ein bestimmter Bereich ein \&quot;Banner\&quot; in einer Webseite ist, wird oft über die Beschreibung und nicht über eine formale Methode vermittelt.
**Typ:** Zeichenfolge

#### _experience > decisioning > Placement Name

**Feld:** name
**Titel:** Platzierungsname
**Beschreibung:** Ein zugewiesener Name für die Platzierung, auf den in menschlichen Interaktionen verwiesen wird.
**Typ:** Zeichenfolge

## _repo {#repo}

**Feld:** _repo
**Typ:** Objekt

### _repo > Placement ETag

**Feld:** etag
**Titel:** Platzierung ETag
**Beschreibung:** Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt der Momentaufnahme befand.
**Typ:** Zeichenfolge
