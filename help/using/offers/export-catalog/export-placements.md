---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Platzierungsdatensatz
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Platzierungen verwendet werden
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UFE7I-hQM4jKPpclDl3avrcE-q-vwRq-c91WOLdPBgo
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 87%

---

# Platzierungsdatensatz {#placements-dataset}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch erstellte Datensatz für Platzierungen aktualisiert.

![](../assets/dataset-placements.png)

Der zuletzt erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt](../export-catalog/access-dataset.md) erfahren Sie, wie Sie für die einzelnen Objekte Ihrer Angebotsbibliothek auf die exportierten Datensätze zugreifen können.

Im Folgenden finden Sie eine Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – Platzierungen]** verwendet werden können.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ Kennung

**Feld:** _id
**title:** Kennung
**Beschreibung:** Eine eindeutige Kennung für den Datensatz.
**Type:** String

+++

+++ _experience

**Feld:** _experience
**Typ:** Objekt

+++

+++ _experience > decisioning

**Feld:** decisioning
**Typ:** Objekt

+++

+++ _experience > decisioning > Placement&#39;s Channel Identifier

**Feld:** channelID
**title:** Kanalkennung der Platzierung
**Beschreibung:** Der Kanal, in dem der Vorschlag gemacht wurde. Der Wert ist ein gültiger Kanal-URI. Siehe https://ns.adobe.com/xdm/channels/channel.
**Type:** String

+++

+++ _experience > decisioning > Content Component Type

**Feld:** componentType
**Titel:** Inhalts-Komponententyp
**Beschreibung:** Eine Auflistung von URIs, bei der jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente zugewiesen wurde. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der @type ein Verweis auf ein Schema ist, das zusätzliche Eigenschaften der Inhaltskomponente beschreibt.
**Type:** String

+++

+++ _experience > decisioning > contentTypes

**Feld:** contentTypes
**Typ:** Array

+++

+++_experience > decisioning > contentTypes > MIME Media Type

**title:** MIME-Medientyp
**Beschreibung:** Eine Begrenzung für den Medientyp der Komponenten, der an dieser Platzierung erwartet wird. Für eine Komponente kann es mehr als einen Medientyp geben, z. B. verschiedene Bildformate.
**Type:** String

+++

+++ _experience > decisioning > Placement Description

**Feld:** description
**title:** Platzierungsbeschreibung
**Beschreibung:** Wird verwendet, um für den Menschen lesbare Absichten darüber zu vermitteln, wie dynamischer Inhalt im gesamten Nachrichtenversand verwendet wird. Dass ein bestimmter Bereich ein \„Banner\&quot; auf einer Web-Seite ist, wird oft über die Beschreibung und nicht durch eine formale Methode übermittelt.
**Type:** String

+++

+++ _experience > decisioning > Placement Name

**Feld:** name
**title:** Platzierungsname
**Beschreibung:** Ein zugewiesener Name für die Platzierung, auf den in menschlichen Interaktionen verwiesen werden kann.
**Type:** String

+++

+++ _repo

**Feld:** _repo
**Typ:** Objekt

+++

+++ _repo > Placement ETag

**Feld:** eTag
**Titel:** ETag für Platzierung
**Beschreibung:** Die Überprüfung, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Speicherauszugs befand.
**Type:** String

+++
