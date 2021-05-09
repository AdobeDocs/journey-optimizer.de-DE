---
title: Platzierungsdataset
description: In diesem Abschnitt werden alle im exportierten Datensatz verwendeten Felder für Platzierungen Liste.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Platzierungsdataset {#placements-dataset}

Bei jeder Änderung eines Angebots wird der automatisch generierte Datensatz für Platzierungen aktualisiert.

![](../assets/dataset-placements.png)

Der letzte erfolgreiche Stapel im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebot-Bibliothek zugreifen.

Eine Platzierung beschreibt einen Ort oder Ort in einer personalisierten Nachricht. Es wird verwendet, um technische Einschränkungen für Inhalte festzulegen, die durch die Personalisierungsentscheidung bereitgestellt werden. Die Platzierung stellt auch eine Anforderung dar, bestimmte Metriktypen zu erstellen, wenn ein Erlebnis-Ereignis erzeugt wird, an dem diese Platzierung beteiligt ist. Beispielsweise erleichtert die Platzierung ein personalisiertes klickbares Bild in einer E-Mail, das einem Endbenutzer angezeigt wird. Die Platzierung kann z. B. vom zusammengestellten Erlebnis angefordert werden, dass der Klick auf das Bild in einem Erlebnis-Ereignis mit der Metrik https://ns.adobe.com/xdm/data/metrics/web/linkclicks und einem Verweis auf diese Platzierung gemeldet wird.

Hier finden Sie die Liste aller Felder, die im Dataset **[!UICONTROL Decision Object Repository - Placements]** verwendet werden können.

## Bezeichner

Eine eindeutige ID für den Datensatz.

Typ: string

## _experience

### Entscheidungsfindung

#### Kanal-ID der Platzierung

Der Kanal, in dem der Vorschlag gemacht wurde. Der Wert ist ein gültiger Kanal-URI. Siehe https://ns.adobe.com/xdm/channels/channel.

Typ: string

#### Content Component Type

Ein aufgezählter Satz von URIs, bei dem jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente angegeben wurde. Einige Benutzer der Inhaltsdarstellungen erwarten, dass der Wert &quot;@type&quot;ein Verweis auf Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.

Typ: string

#### MIME-Medientyp

Eine Beschränkung für den Medientyp der Komponenten, die an dieser Platzierung erwartet werden. Es kann mehr als einen Medientyp für eine Komponente wie z. B. ein anderes Bildformat geben.

Typ: string

#### Platzierungsbeschreibung

Es wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie dynamische Inhalte im gesamten Versand der Nachricht verwendet werden. Dass ein bestimmter Bereich ein \&quot;Banner\&quot; in einer Webseite ist, wird oft über die Beschreibung und nicht durch eine formale Methode übertragen.

Typ: string

#### Platzierungsname

Ein zugewiesener Name für die Platzierung, auf die in menschlichen Interaktionen Bezug genommen wird.

Typ: string

## _repo

### Platzierung ETag

Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Snapshots befand.

Typ: string
