---
title: Datensatz für Platzierungen
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Platzierungen verwendet werden.
source-git-commit: 958bf03f3d3c2dd1606daba9dfef1284e2ed5cdd
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 92%

---

# Datensatz für Platzierungen {#placements-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für Platzierungen aktualisiert.

![](../../assets/dataset-placements.png)

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebotsbibliothek zugreifen.

Hier finden Sie die Liste aller Felder, die im Datasatz **[!UICONTROL Entscheidungsobjekt-Repository – Platzierungen]** verwendet werden können.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## ID

**Feld:** _id
**Titel:** Kennung 
**Beschreibung:** Eine eindeutige Kennung für den Eintrag.
**Typ:** Zeichenfolge

## _Erlebnis

**Feld:** _Erlebnis 
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
**Titel:** Typ der Inhaltskomponente
**Beschreibung:** Eine Aufzählung von URIs, bei der jeder Wert einem Typ zugeordnet ist, der der Inhaltskomponente gegeben wurde. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der Wert „@type“ ein Verweis auf das Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.
**Typ:** Zeichenfolge

#### _experience > decisioning > contentTypes

**Feld:** contentTypes 
**Typ:** Array

* **MIME-Medientyp**

   **Titel:** MIME-Medientyp
   **Beschreibung:** Eine Begrenzung für den Medientyp der Komponenten, der an dieser Platzierung erwartet wird. Für eine Komponente kann es mehr als einen Medientyp geben, z. B. verschiedene Bildformate.
   **Typ:** Zeichenfolge

#### _experience > decisioning > Placement Description

**Feld:** Beschreibung 
**Titel:** Beschreibung der Platzierung 
**Beschreibung:** Es wird verwendet, um für den Menschen lesbare Absichten darüber zu vermitteln, wie dynamischer Inhalt im gesamten Versand der Nachricht verwendet wird. Dass ein bestimmter Bereich ein \&quot;Banner\&quot; in einer Web-Seite ist, wird oft über die Beschreibung und nicht durch eine formale Methode übertragen.
**Typ:** Zeichenfolge

#### _experience > decisioning > Placement Name

**Feld:** Name 
**Title:** Name der Platzierung 
**Beschreibung:** Ein zugewiesener Name für die Platzierung, der in menschlichen Interaktionen darauf verweist.
**Typ:** Zeichenfolge

## _repo

**Feld:** _repo
**Typ:** Objekt

### _repo > Placement ETag

**Feld:** ETag
**Titel:** ETag der Platzierung
**Beschreibung:** Die Revision, in der sich das Objekt der Entscheidungsoption befand, als der Schnappschuss erstellt wurde.
**Typ:** Zeichenfolge
