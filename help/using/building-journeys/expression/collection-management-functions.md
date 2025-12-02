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
source-git-commit: e7693ba84d8806cf4b0dc10e8fdd18f2511e37ea
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 82%

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

**Konzeptbeispiel:** Unter allen App-Benutzern können Sie die mit IOS 13 abrufen (boolescher Ausdruck &quot;== IOS 13 verwendete App„). Das Ergebnis dieser Funktion ist die gefilterte Liste mit Elementen, die dem booleschen Ausdruck entsprechen (Beispiel: App-Anwender 1, App-Anwender 34, App-Anwender 432).

In einer Aktivität des Typs „Bedingung der Datenquelle“ können Sie überprüfen, ob das Ergebnis der Funktion **[!UICONTROL all]** null ist. Sie können die Funktion **[!UICONTROL all]** auch mit anderen Funktionen wie **[!UICONTROL count]** kombinieren. Weitere Informationen finden Sie unter [Aktivität „Bedingung der Datenquelle“](../condition-activity.md#data_source_condition).

**Code-Beispiele, die die LobbyBeacon-Payload verwenden:**

Die folgenden Beispiele verwenden die Ereignis-Payload, die oben auf dieser Seite angezeigt wird.


>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Wenn Ihr Anwendungsfall die Verwendung von Erlebnisereignissen erfordert, sollten Sie alternative Methoden in Betracht ziehen. [Weitere Informationen](../exp-event-lookup.md)

### Beispiel 1

Wir möchten überprüfen, ob ein Anwender eine bestimmte Version einer App installiert hat. Zu diesem Zweck rufen wir alle Push-Benachrichtigungs-Token für Mobile Apps mit der Version 1.0 ab. Anschließend führen wir eine Bedingung mit der Funktion **[!UICONTROL Zählen]** aus, um zu überprüfen, ob die zurückgegebene Liste von Tokens mindestens ein Element enthält.

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

Mit der Funktion **[!UICONTROL at]** können Sie anhand eines Index auf ein bestimmtes Element in einer Sammlung verweisen.
Der Index „0“ ist der erste Index der Sammlung.

_`<listExpression>`.at(`<index>`)_

### Beispiel

Dieser Ausdruck gibt das zweite Push-Benachrichtigungs-Token der Liste zurück.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Das Ergebnis ist `token_2`.