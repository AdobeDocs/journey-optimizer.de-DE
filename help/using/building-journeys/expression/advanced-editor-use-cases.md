---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden des erweiterten Ausdruckseditors
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: Ausdruck, Bedingung, Anwendungsfälle, Ereignisse
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 51%

---

# Beispiele für erweiterte Ausdrücke{#advanced-expression-examples}

Der erweiterte Ausdruckseditor kann verwendet werden, um Bedingungen zum Filtern von Benutzenden in Ihren Journeys zu erstellen. Mit diesen Bedingungen können Sie Benutzende nach Uhrzeit, Datum, Ort oder Dauer ansprechen, damit diese in der Journey erneut angesprochen werden können.

>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Wenn Ihr Anwendungsfall die Verwendung von Erlebnisereignissen erfordert, sollten Sie alternative Methoden in Betracht ziehen. [Weitere Informationen](../exp-event-lookup.md)


## Erstellen von Bedingungen anhand von Erlebnisereignissen


>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Wenn Ihr Anwendungsfall die Verwendung von Erlebnisereignissen erfordert, sollten Sie alternative Methoden in Betracht ziehen. [Weitere Informationen](../exp-event-lookup.md)
>



Sie benötigen den erweiterten Ausdruckseditor, um Abfragen zu Zeitreihen wie eine Liste der Käufe oder vergangene Klicks auf Nachrichten durchzuführen. Solche Abfragen können nicht mit dem einfachen Editor ausgeführt werden.

>[!NOTE]
>
>Ereignisse beginnen mit @, Datenquellen mit #.

Die Erlebnisereignisse werden von Adobe Experience Platform als Sammlung in umgekehrter chronologischer Reihenfolge abgerufen. Entsprechend gilt:

* Die Funktion „first“ gibt das neueste Ereignis zurück.
* Die Funktion „last“ gibt das älteste zurück.

Angenommen, Sie möchten Kunden mit einem Warenkorbabbruch in den letzten sieben Tagen ansprechen. Dazu möchten Sie diesen Kunden, wenn sie sich in der Nähe eines Geschäfts befinden, eine Nachricht mit einem Angebot für Artikel in diesem Geschäft senden, an denen die Kunden interessiert waren.

**Erstellen Sie dazu die folgenden Bedingungen:**

Sprechen Sie in erster Linie Kunden an, die den Online-Store besucht, aber in den letzten sieben Tagen keine Bestellung abgeschlossen haben.

**Dieser Ausdruck sucht nach einem angegebenen Wert in einem String-Wert:**

`In ("addToCart", #{field reference from experience event})`

**Dieser Ausdruck sucht nach allen Ereignissen für diese Person, die in den letzten sieben Tagen spezifiziert wurden:**

Anschließend werden alle Ereignisse ausgewählt, bei denen etwas dem Warenkorb hinzugefügt wurde, es jedoch nicht zu einem „completePurchase“ kam.

>[!NOTE]
>
>Um Felder schnell in den Ausdruck einzufügen, doppelklicken Sie auf das Feld im linken Panel des Editors.

Der angegebene Zeitstempel dient als der Datums-/Uhrzeitwert, der zweite bezeichnet die Anzahl der Tage.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Dieser Ausdruck gibt einen booleschen Wert zurück.

**Erstellen Sie nun einen Ausdruck, der überprüft, ob das Produkt vorrätig ist**

* Dieser Ausdruck such im Inventar nach dem Mengenfeld eines Produkts mit der Angabe, dass es größer als 0 sein soll.

`#{Inventory.fieldgroup3.quantity} > 0`

* Rechts werden die erforderlichen Werte angegeben. Hier müssen wir den Ort des Geschäfts abrufen, der der Position des Ereignisses „ArriveLumaStudio“ zugeordnet ist:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* Geben Sie die SKU unter Verwendung der `first`-Funktion an, um die jüngste „addToCart“ -Interaktion abzurufen:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

Von dort können Sie einen weiteren Pfad zu Ihrer Journey hinzufügen, wenn das Produkt nicht im Store ist, und eine Benachrichtigung mit einem Interaktionsangebot senden. Konfigurieren Sie die Nachrichten entsprechend und verwenden Sie Personalisierungsdaten, um die Nachricht zu verbessern.

## Zeitstempelfilter in Ausdrücken

Wenn Sie auf mehrere Warenkorb-Aktivitätsereignisse verweisen, geben Sie sowohl ein Start- als auch ein Endzeitstempelfenster an, um die Erfassung historischer Daten zu vermeiden. Beispiel:

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

## Beispiele für Zeichenfolgenmanipulationen mit dem erweiterten Ausdruckseditor

**In Bedingungen**

Diese Bedingung ruft nur die Geofence-Ereignisse ab, die in „Arlington“ ausgelöst wurden:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Erklärung: Dies ist ein strikter Zeichenfolgenvergleich (Groß-/Kleinschreibung beachten), der einer Abfrage im einfachen Modus entspricht, die `equal to` mit der aktivierten Option `Is sensitive` verwendet.

Die gleiche Abfrage mit der deaktivierten Option `Is sensitive` generiert den folgenden Ausdruck im erweiterten Modus:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**In Aktionen**

Mit dem folgenden Ausdruck können Sie die CRM-ID in einem Feld zur Aktionspersonalisierung definieren:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Erläuterung: In diesem Beispiel werden die `substr`- und `lastIndexOf`-Funktionen verwendet, um geschweifte Klammern zu entfernen, die die CRM-ID einschließen, die bei einem App-Startereignis übergeben wurde.


Weitere Informationen zur Verwendung des erweiterten Ausdruckseditors finden Sie in [diesem Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=de).

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite finden Sie praktische Beispiele für die Verwendung des erweiterten Ausdruckseditors zum Erstellen von Journey-Bedingungen, die Benutzer nach Warenkorbaktivität, Inventarstatus, Geofence-Ereignissen, Zeichenfolgenmanipulationen und Zeitstempelfenstern filtern.

**intents:**

* Erstellen Sie mit `in()` und `inLastDays()` eine Warenkorbabbruchsbedingung, um Benutzende anzusprechen, die Artikel hinzugefügt, den Kauf jedoch nicht innerhalb von 7 Tagen abgeschlossen haben
* Filtern von Erlebnisereignissammlungen nach Zeitstempelfenster, um die Erfassung historischer Daten zu vermeiden
* Anwenden von Zeichenfolgenvergleichen, bei denen zwischen Groß- und Kleinschreibung unterschieden wird, auf Geofence-Ereignisfelder
* Extrahieren und Bearbeiten von CRM-IDs aus Startereignissen von Mobile Apps mithilfe von `substr` und `lastIndexOf`
* Überprüfen der Verfügbarkeit des Produktbestands durch Vergleich eines Mengenfelds mit einem Schwellenwert
* Kombinieren mehrerer boolescher Ausdrücke mithilfe der `and`/`not`-Logik in Journey-Bedingungen

**Glossar:**

* **Erweiterter Ausdruckseditor**: Die Journey Optimizer-Oberfläche zum Schreiben komplexer Ausdrücke auf Code-Ebene mithilfe von Funktionen, Operatoren und Feldverweisen *(produktspezifisch)*
* **currentDataPackField**: Eine Schleifenvariable, die bei der Iteration über Datenquellensammlungen in `all()`-, `first()`- oder `last()`-Funktionen verwendet wird *(produktspezifisch)*
* **inLastDays(timestamp, N)**: Eine Datumsfunktion, die „true“ zurückgibt, wenn der angegebene Zeitstempel innerhalb der letzten N Tage fällt *(produktspezifisch)*
* **Erlebnisereignisse**: In Adobe Experience Platform gespeicherte Zeitreihen-Verhaltensdatensätze, die in umgekehrter chronologischer Reihenfolge abgerufen werden *(produktspezifisch)*

**Leitplanken:**

* Die direkte Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Stattdessen sollten alternative Methoden wie berechnete Attribute oder Zielgruppensegmente verwendet werden
* Der erweiterte Ausdruckseditor muss (nicht der einfache Editor) für Abfragen von Zeitreihendaten wie Sammlungen von Käufen oder Klicks verwendet werden
* Durch Doppelklicken auf ein Feld im linken Bereich wird es schnell in den Ausdruck eingefügt. Vermeiden Sie die manuelle Eingabe von Feldpfaden, um Fehler zu reduzieren
* Ausdrücke, die Erlebnisereignisse abfragen, geben einen booleschen Wert zurück. Stellen Sie sicher, dass die nachgelagerte Logik einen booleschen Typ erwartet.

**Terminologie:**

* Kanonischer Name: Erweiterter Ausdruckseditor — Akronym: none — Varianten: Ausdruckseditor, Erweiterter Editor
* Synonyme: „addToCart“ = „Zum Warenkorb hinzufügen Interaktion“; „completePurchase“ = „Kaufabschluss-Ereignis“
* Verwechseln Sie nicht: Ereignisse (mit dem Präfix `@`) ≠ Datenquellen (mit dem Präfix `#`)

**FAQ:**

* **F: Warum muss ich den erweiterten Editor anstelle des einfachen Editors für Abfragen zum Warenkorbabbruch verwenden?** - Der einfache Editor kann keine Abfragen für Zeitreihensammlungen durchführen. Der erweiterte Editor ist für `all()`-, `first()`- und `last()` erforderlich.
* **F: Wie verweise ich in einem Ausdruck auf das letzte „addToCart“-Ereignis?** - Verwenden Sie die `first()` Funktion für die Erlebnisereignissammlung, die nach `productInteraction == "addToCart"` gefiltert wird, da Ereignisse in umgekehrter chronologischer Reihenfolge zurückgegeben werden.
* **F: Wie beachte ich im erweiterten Editor die Groß-/Kleinschreibung bei einem Zeichenfolgenvergleich?** — Verwenden Sie die `equalIgnoreCase()` Funktion anstelle des `==` Operators.
* **F: Welchen Zweck hat das Hinzufügen eines Zeitstempelfensters bei der Abfrage von Warenkorbereignissen?** — Wenn Sie sowohl einen Start- als auch einen Endzeitstempel angeben, wird verhindert, dass historische Daten aufgenommen werden, die außerhalb des vorgesehenen Aktivitätsfensters liegen.
* **F: Wie entferne ich geschweifte Klammern aus einer CRM-ID-Zeichenfolge, die in einem Ereignis übergeben wird?** - Verwenden Sie `substr()` in Kombination mit `lastIndexOf()`, um den Inhalt zwischen den geschweiften Klammern zu extrahieren.

+++
