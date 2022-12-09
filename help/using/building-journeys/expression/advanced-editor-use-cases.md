---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden des erweiterten Ausdruckseditors
description: Erfahren Sie, wie Sie erweiterte Ausdrücke erstellen
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Beispiele für erweiterte Ausdrücke{#advanced-expression-examples}

Der erweiterte Ausdruckseditor kann verwendet werden, um Bedingungen zu erstellen, mit denen Sie Benutzer in Ihren Journeys filtern können. Mit diesen Bedingungen können Sie Benutzer auf Zeit, Datum, Ort, Dauer oder Aktionen wie Kauf oder Abbruch von Warenkörben ausrichten, damit sie in der Journey erneut angesprochen werden können.

>[!NOTE]
>
>Ereignisse beginnen mit @, Datenquellen mit #.

## Erstellen von Bedingungen für Erlebnisereignisse

Der erweiterte Ausdruckseditor ist für Abfragen zu Zeitreihen wie einer Liste von Käufen oder früheren Klicks auf Nachrichten obligatorisch. Solche Abfragen können nicht mit dem einfachen Editor durchgeführt werden.

Die Erlebnisereignisse werden von Adobe Experience Platform als Sammlung in umgekehrter chronologischer Reihenfolge abgerufen. Entsprechend gilt:

* Die Funktion first gibt das neueste Ereignis zurück
* Die Funktion last gibt die älteste zurück.

Angenommen, Sie möchten Kunden mit einem Warenkorbabbruch in den letzten sieben Tagen ansprechen, um eine Nachricht zu senden, wenn sich der Kunde in der Nähe eines Stores befindet, mit einem Angebot zu Artikeln, die er wünschte und die im Geschäft sind.

**Sie müssen die folgenden Bedingungen erstellen:**

Wählen Sie zunächst Kunden aus, die den Online-Store besucht, aber in den letzten sieben Tagen keine Bestellung abgeschlossen haben.

<!--**This expression looks for a specified value in a string value:**

`In (“addToCart”, #{field reference from experience event})`-->

**Dieser Ausdruck sucht nach allen Ereignissen für diesen Benutzer, die in den letzten sieben Tagen angegeben wurden:**

Anschließend werden alle addtocart-Ereignisse ausgewählt, die nicht in completePurchase umgewandelt wurden.

>[!NOTE]
>
>Um Felder schnell in den Ausdruck einzufügen, doppelklicken Sie auf das Feld im linken Bereich des Editors.

Der angegebene Zeitstempel dient als Datums- und Uhrzeitwert, der zweite als Anzahl von Tagen.

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

**Erstellen wir nun einen Ausdruck, der überprüft, ob das Produkt vorrätig ist.**

* Im Bestand sucht dieser Ausdruck nach dem Mengenfeld eines Produkts und gibt an, dass es größer als 0 sein soll.

`#{Inventory.fieldgroup3.quantity} > 0`

* Rechts werden die erforderlichen Werte angegeben. Hier müssen wir den Speicherort des Stores abrufen, der vom Speicherort des Ereignisses &quot;ArriveLumaStudio&quot;zugeordnet ist:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* Geben Sie die SKU mithilfe der Funktion an. `first` , um die neueste &quot;addToCart&quot;-Interaktion abzurufen:

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

Von dort können Sie einen weiteren Pfad in Ihrer Journey hinzufügen, wenn das Produkt nicht im Speicher ist, und eine Benachrichtigung mit einem Interaktionsangebot senden. Konfigurieren Sie die Nachrichten entsprechend und verwenden Sie Personalisierungsdaten, um die Nachrichtenzielgruppe zu verbessern.

## Beispiele für Zeichenfolgenmanipulationen mit dem erweiterten Ausdruckseditor

**In Bedingungen**

Diese Bedingung ruft nur die Geofence-Ereignisse ab, die in &quot;Arlington&quot;ausgelöst wurden:

```json
        @{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Erklärung: Dies ist ein strikter Zeichenfolgenvergleich (Groß-/Kleinschreibung beachten), der einer Abfrage im einfachen Modus entspricht, die `equal to` mit `Is sensitive` aktiviert.

Dieselbe Abfrage mit `Is sensitive` deaktiviert wird den folgenden Ausdruck im erweiterten Modus generieren:

```json
        equalIgnoreCase(@{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**In Aktionen**

Mit dem folgenden Ausdruck können Sie die CRM-ID in einem Feld für die Aktionspersonalisierung definieren:

```json
substr(
   @{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Erklärung: Dieses Beispiel verwendet `substr` und `lastIndexOf` Funktionen zum Entfernen von geschweiften Klammern, die die mit einem App-Startereignis übergebene CRM-ID umschließen.

Weitere Informationen zur Verwendung des erweiterten Ausdruckseditors finden Sie unter [dieses Video](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html).
