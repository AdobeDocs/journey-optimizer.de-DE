---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen zur Verwaltung von Sammlungen
description: Erfahren Sie mehr über die Datentypen in den Funktionen zur Verwaltung von Sammlungen
feature: Journeys
role: Developer
level: Experienced
keywords: Abfrage, Sammlungen, Funktionen, Payload, Journey
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sNFI7l-UMGmRV2wRcvYa56tILLoWFxXeG3N5txgrUiw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 51%

---

# Funktionen zur Verwaltung von Sammlungen {#collection-management-functions}


## Informationen zu Funktionen zum Abfragen von Sammlungen

Die Ausdruckssprache bietet auch eine Reihe von Funktionen zum Abfragen von Sammlungen. Diese Funktionen werden nachfolgend erläutert.

In den folgenden Beispielen verwenden wir ein Ereignis mit dem Namen „LobbyBeacon“, das eine Sammlung von Push-Benachrichtigungs-Token enthält. Die Beispiele auf dieser Seite verwenden die unten dargestellte Payload-Struktur für Ereignisse:

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

>[!NOTE]
>
>In den folgenden Beispielen wird diese Payload mit `@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}` referenziert, wobei „LobbyBeacon“ der Ereignisname ist und der Rest des Pfads der oben gezeigten Struktur entspricht.

## Die Funktion „all(`<condition>`)“

Die Funktion **[!UICONTROL all]** ermöglicht mithilfe eines booleschen Ausdrucks die Definition eines Filters für eine bestimmte Sammlung.

```json
<listExpression>.all(<condition>)
```

**Kontextbeispiel:** Sie können alle App-Benutzenden abrufen, die iOS 13 verwenden (boolescher Ausdruck „app used == iOS 13“). Das Ergebnis dieser Funktion ist die gefilterte Liste mit Elementen, die dem booleschen Ausdruck entsprechen (Beispiel: App-Anwender 1, App-Anwender 34, App-Anwender 432).

In einer Aktivität des Typs „Bedingung der Datenquelle“ können Sie überprüfen, ob das Ergebnis der Funktion **[!UICONTROL all]** null ist. Sie können die Funktion **[!UICONTROL all]** auch mit anderen Funktionen wie **[!UICONTROL count]** kombinieren. Weitere Informationen finden Sie unter [Aktivität „Bedingung der Datenquelle“](../conditions.md#data_source_condition).

**Code-Beispiele, die die LobbyBeacon-Payload verwenden:**

Die folgenden Beispiele verwenden die Ereignis-Payload, die oben auf dieser Seite angezeigt wird.


>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Wenn Ihr Anwendungsfall die Verwendung von Erlebnisereignissen erfordert, sollten Sie alternative Methoden in Betracht ziehen. [Weitere Informationen](../exp-event-lookup.md)

### Beispiel 1

Wir möchten überprüfen, ob ein Anwender eine bestimmte Version einer App installiert hat. Zu diesem Zweck rufen wir alle Push-Benachrichtigungs-Token für Apps mit der Version 1.0 ab. Anschließend führen wir eine Bedingung mit der Funktion **[!UICONTROL count]** aus, um zu überprüfen, ob die zurückgegebene Liste von Token mindestens ein Element enthält.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Das Ergebnis ist wahr.

### Beispiel 2

Hier verwenden wir die Funktion **[!UICONTROL count]**, um zu überprüfen, ob in der Sammlung Push-Benachrichtigungs-Token vorhanden sind.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


Das Ergebnis ist wahr.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Das Ergebnis des Ausdrucks ist **3**.


>[!NOTE]
>
>* Wenn die Filterbedingung in der Funktion **all()** leer ist, gibt der Filter alle Elemente in der Liste zurück. **Um jedoch die Anzahl der Elemente einer Sammlung zu zählen, ist die Funktion „all“ nicht erforderlich.**
>
>* `currentEventField` ist nur bei der Bearbeitung von Ereignissammlungen verfügbar, `currentDataPackField` bei der Bearbeitung von Datenquellensammlungen und `currentActionField` bei der Bearbeitung von benutzerdefinierten Aktionsantwortsammlungen.
>
>  Bei der Verarbeitung von Sammlungen mit `all`, `first` und `last` wird nacheinander eine Schleife um jedes Element der Sammlung gebildet. `currentEventField`, `currentDataPackField` und `currentActionField` entsprechen dem Element, um das die Schleife gebildet wird.


## Die Funktionen „first(`<condition>`)“ und „last(`<condition>`)“

Die Funktionen **[!UICONTROL first]** und **[!UICONTROL last]** ermöglichen auch die Definition eines Filters für die Sammlung, wobei das erste/letzte Element der Liste zurückgegeben wird, das dem Filter entspricht.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Beispiel 1

Dieser Ausdruck gibt das erste Push-Benachrichtigungs-Token zurück, das mit Apps verknüpft ist, deren Version 1.0 ist.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

Das Ergebnis ist `token_1`.

### Beispiel 2

Dieser Ausdruck gibt das letzte Push-Benachrichtigungs-Token zurück, das mit Apps verknüpft ist, deren Version 1.0 ist.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Das Ergebnis ist `token_2`.

## Die Funktion „at(`<index>`)“

Mit der Funktion **[!UICONTROL at]** können Sie anhand eines Index auf ein bestimmtes Element in einer Auflistung verweisen.
Index 0 ist der erste Index der Sammlung.

_`<listExpression>`.at(`<index>`)_

### Beispiel

Dieser Ausdruck gibt das zweite Push-Benachrichtigungs-Token der Liste zurück.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Das Ergebnis ist `token_2`.

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die im erweiterten Ausdruckseditor von Journey verwendeten Funktionen zur Sammlungsverwaltung für `all()`, `first()`, `last()` und `at()` dokumentiert, die anhand von Payload-Beispielen für Push-Benachrichtigungs-Token veranschaulicht werden.

**intents:**

* Filtern Sie eine Sammlung von Ereignis- oder Datenquellenfeldern mithilfe einer booleschen Bedingung mit `all(<condition>)`
* Zählen gefilterter oder ungefilterter Sammlungselemente mithilfe von `count()` in Kombination mit Sammlungsfunktionen
* Abrufen des ersten oder letzten übereinstimmenden Elements einer Sammlung mit `first()` oder `last()`
* Zugreifen auf ein Sammlungselement an einem bestimmten nullbasierten Index mithilfe von `at(<index>)`
* Verstehen, welche Schleifenvariable (`currentEventField`, `currentDataPackField`, `currentActionField`) für jeden Sammlungskontext gilt

**Glossar:**

* **all(condition)**: Filtert eine Sammlung und gibt alle Elemente zurück, die mit dem gegebenen booleschen Ausdruck übereinstimmen *(produktspezifisch)*
* **first(condition)**: Gibt das erste Element (das letzte für Erlebnisereignisse) in einer Sammlung zurück, das der Bedingung entspricht *(product-specific)*
* **last(condition)**: Gibt das letzte (älteste für Erlebnisereignisse) Element in einer Sammlung zurück, das der Bedingung entspricht *(produktspezifisch)*
* **at(index)**: Gibt das Element im angegebenen nullbasierten Index einer Sammlung zurück *produktspezifisch)*
* **currentEventField**: Schleifenvariable nur bei der Iteration über Ereignisauflistungen verfügbar *(produktspezifisch)*
* **currentDataPackField**: Schleifenvariable nur bei der Iteration über Datenquellensammlungen verfügbar *(produktspezifisch)*
* **currentActionField**: Schleifenvariable nur bei der Iteration über Sammlungen von benutzerdefinierten Aktionsantworten verfügbar *(produktspezifisch)*

**Leitplanken:**

* Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Erwägen Sie alternative Methoden wie berechnete Attribute
* `currentEventField`, `currentDataPackField` und `currentActionField` sind nur innerhalb des jeweiligen Sammlungskontexts verfügbar
* Die Funktion `all` ist nicht erforderlich, um Sammlungselemente zu zählen - `count()` kann direkt auf den Feldpfad angewendet werden
* Wenn `all()` mit einer leeren Bedingung aufgerufen wird, werden alle Elemente in der Auflistung zurückgegeben

**Terminologie:**

* Kanonischer Name: Sammlungsverwaltungsfunktionen — Akronym: none — Varianten: Sammlungsfunktionen, Abfragen-Sammlungsfunktionen
* Synonyme: „all()“ = „Sammlungsfilterfunktion“; „at()“ = „Index-Accessor“
* Nicht verwechseln: `first()` (aktuelles Erlebnisereignis) ≠ erstes eingefügtes Element in allgemeinen Listen

**FAQ:**

* **F: Was ist der Unterschied zwischen `all()` mit einer leeren Bedingung und `all()` mit einer Bedingung?** — Eine leere `all()` gibt jedes Element zurück; eine bedingungsbasierte `all()` gibt nur Elemente zurück, die mit diesem booleschen Ausdruck übereinstimmen.
* **F: Wie zähle ich Push-Benachrichtigungs-Token, ohne `all()` zu verwenden?** — `count()` direkt über den Token-Feldpfad aufrufen, z. B. `count(@event{LobbyBeacon...pushNotificationTokens.token})`.
* **F: Welche Variable verwende ich, um auf das aktuelle Element zu verweisen, wenn ich eine Datenquellensammlung durchlaufe?** - Verwenden Sie `currentDataPackField` in `all()`, `first()` oder `last()` von Datenquellensammlungen.
* **F: Wie erhalte ich das zweite Element in einer Sammlung?** — Verwenden Sie `at(1)`, da Index 0 das erste Element ist.
* **F: Warum gibt `last()` das älteste Erlebnisereignis zurück?** — Erlebnisereignisse werden in umgekehrter chronologischer Reihenfolge gespeichert, sodass die letzte Position in der Sammlung dem ältesten Ereignis entspricht.

+++
