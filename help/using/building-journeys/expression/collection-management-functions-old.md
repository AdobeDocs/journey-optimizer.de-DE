---
solution: Journey Optimizer
product: journey optimizer
title: Funktionen zur Verwaltung von Sammlungen
description: Erfahren Sie mehr über die Datentypen in den Funktionen zur Verwaltung von Sammlungen
feature: Journeys
hide: true
hidefromtoc: true
role: Data Engineer, Architect
level: Experienced
keywords: Abfrage, Sammlungen, Funktionen, Payload, Journey
source-git-commit: ff05675fb132becf092dc6b79bbbaa249f01af96
workflow-type: ht
source-wordcount: '739'
ht-degree: 100%

---

# Funktionen zur Verwaltung von Sammlungen

Die Ausdruckssprache bietet auch eine Reihe von Funktionen zum Abfragen von Sammlungen.

Diese Funktionen werden nachfolgend erläutert. Im folgenden Beispiel verwenden wir die Ereignis-Payload, die eine Sammlung enthält:

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

**Die Funktion „all(`<condition>`)“**

Die Funktion **[!UICONTROL all]** ermöglicht mithilfe eines booleschen Ausdrucks die Definition eines Filters für eine bestimmte Sammlung.

```json
<listExpression>.all(<condition>)
```

Beispielsweise können Sie von allen App-Benutzenden diejenigen abfragen, die iOS 13 nutzen (boolescher Ausdruck „app used == iOS 13“). Das Ergebnis dieser Funktion ist die gefilterte Liste mit Elementen, die dem booleschen Ausdruck entsprechen (Beispiel: App-Anwender 1, App-Anwender 34, App-Anwender 432).

In einer Aktivität des Typs „Bedingung der Datenquelle“ können Sie überprüfen, ob das Ergebnis der Funktion **[!UICONTROL all]** null ist. Sie können die Funktion **[!UICONTROL all]** auch mit anderen Funktionen wie **[!UICONTROL count]** kombinieren. Weitere Informationen finden Sie unter [Aktivität „Bedingung der Datenquelle“](../condition-activity.md#data_source_condition).


## Beispiele

>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird unterstützt, aber nicht empfohlen. Wenn für Ihren Anwendungsfall Erlebnisereignisse verwendet werden müssen, sollten Sie alternative Methoden wie [berechnete Attribute](../../audience/computed-attributes.md) in Betracht ziehen oder ein Segment mithilfe der Ereignisse erstellen und dieses Segment in [`inAudience`-Ausdrücke](../../building-journeys/functions/functioninaudience.md) integrieren.

**Beispiel 1:**

Wir möchten überprüfen, ob ein Anwender eine bestimmte Version einer App installiert hat. Zu diesem Zweck rufen wir alle Push-Benachrichtigungs-Token für Mobile Apps mit der Version 1.0 ab. Anschließend führen wir eine Bedingung mit der Funktion **[!UICONTROL Zählen]** aus, um zu überprüfen, ob die zurückgegebene Liste von Tokens mindestens ein Element enthält.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Das Ergebnis ist wahr.

**Beispiel 2:**

Hier verwenden wir die Funktion **[!UICONTROL count]**, um zu überprüfen, ob in der Sammlung Push-Benachrichtigungstoken vorhanden sind.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

Das Ergebnis ist wahr.

<!--Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.-->

>[!NOTE]
>
>Wenn die Filterbedingung in der Funktion **all()** leer ist, gibt der Filter alle Elemente in der Liste zurück. **Um jedoch die Anzahl der Elemente einer Sammlung zu zählen, ist die Funktion „all“ nicht erforderlich.**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Das Ergebnis des Ausdrucks ist **3**.

**Beispiel 3:**

Hier prüfen wir, ob ein Kontakt innerhalb der letzten 24 Stunden keine Mitteilungen erhalten hat. Wir filtern die Sammlung von Erlebnisereignissen, die aus der Experience Platform-Datenquelle abgerufen wurden, mithilfe von zwei Ausdrücken, die auf zwei Elementen der Sammlung basieren. Insbesondere wird der Zeitstempel des Ereignisses mit dem von der Funktion **[!UICONTROL nowWithDelta]** zurückgegebenen Wert „dateTime“ verglichen.

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

Das Ergebnis ist wahr, wenn es kein Erlebnisereignis gibt, das den beiden Bedingungen entspricht.

**Beispiel 4:**

Hier möchten wir überprüfen, ob ein Kontakt in den letzten sieben Tagen mindestens einmal ein Programm gestartet hat, um z. B. eine Push-Benachrichtigung auszulösen, die den Kontakt zum Ansehen eines Tutorials einlädt.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** ist nur bei der Bearbeitung von Ereignissammlungen verfügbar, **[!UICONTROL currentDataPackField]** bei der Bearbeitung von Datenquellensammlungen und **[!UICONTROL currentActionField]** bei der Bearbeitung von benutzerdefinierten Aktionsantwortsammlungen.
>
>Bei der Verarbeitung von Sammlungen mit **[!UICONTROL all]**, **[!UICONTROL first]** und **[!UICONTROL last]** durchlaufen wir eine Schleife über jedes Element der Sammlung, eins nach dem anderen. **[!UICONTROL currentEventField]**, **currentDataPackField** und **[!UICONTROL currentActionField]** entsprechen dem Element, das in einer Schleife läuft.

**Die Funktionen „first(`<condition>`)“ und „last(`<condition>`)“**

Die Funktionen **[!UICONTROL first]** und **[!UICONTROL last]** ermöglichen auch die Definition eines Filters für die Sammlung, wobei das erste/letzte Element der Liste zurückgegeben wird, das dem Filter entspricht.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**Beispiel 1:**

Dieser Ausdruck gibt das erste Push-Benachrichtigungs-Token zurück, das mit Mobile Apps verknüpft ist, deren Version 1.0 ist.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

Das Ergebnis ist „token_1“.

**Beispiel 2:**

Dieser Ausdruck gibt das letzte Push-Benachrichtigungs-Token zurück, das mit Mobile Apps verknüpft ist, deren Version 1.0 ist.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Das Ergebnis ist „token_2“.

>[!NOTE]
>
>Die Erlebnisereignisse werden von Adobe Experience Platform als Sammlung in umgekehrter chronologischer Reihenfolge abgerufen. Entsprechend gilt:
>
>* Die Funktion **[!UICONTROL first]** gibt das neueste Ereignis zurück.
>* Die Funktion **[!UICONTROL last]** gibt das älteste zurück.

**Beispiel 3:**

Wir prüfen, ob das erste (neueste) Adobe Analytics-Ereignis mit einem Wert ungleich null für die DMA-ID den Wert „602“ hat.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**Die Funktion „at(`<index>`)“**

Mit der Funktion **[!UICONTROL at]** können Sie anhand eines Index auf ein bestimmtes Element in einer Sammlung verweisen.
Der Index „0“ ist der erste Index der Sammlung.

_`<listExpression>`.at(`<index>`)_

**Beispiel:**

Dieser Ausdruck gibt das zweite Push-Benachrichtigungstoken der Liste zurück.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Das Ergebnis ist „token_2“.

**Weitere Beispiele**

Dieser Ausdruck gibt die Produktnamen basierend auf dem SKU-Wert zurück. Die Liste dieser Produkte ist in der Ereignisliste enthalten, wobei die Bedingung die Ereignis-ID ist.

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

Dieser Ausdruck ruft den Namen des letzten Produkts in der Produktliste eines Commerce-Ereignisses ab, bei dem der Ereignistyp „productListAdds“ lautet und der Gesamtpreis größer oder gleich 150 ist.

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```
