---
title: Externer Helper zur Datensuche
description: Ausführliche Anleitung zur Verwendung des Externen Daten-Lookup-Helpers für die dynamische Personalisierung in Adobe Journey Optimizer.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 1%

---


# Externer Helper zur Datensuche

Der `externalDataLookup`-Helper im [!DNL Journey Optmizer] Personalisierungseditor kann verwendet werden, um Daten dynamisch von einem externen Endpunkt abzurufen und sie für die Erstellung von Inhalten für eingehende Kanäle wie das Code-basierte Erlebnis, das Web und In-App-Nachrichten-Kanäle zu verwenden.

>[!AVAILABILITY]
>
>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit).

Um den Helper zu verwenden, müssen Sie zunächst eine Aktion im Menü **[!UICONTROL Administration]** > **[!UICONTROL Konfigurationen]** definieren. Bei einer Aktion konfigurieren Sie Details zu einem externen Endpunkt, z. B. URL, GET vs. POST-Methode, Kopfzeilenparameter, Abfrageparameter, POST-Textkörper-JSON-Schema und Antwort-JSON-Schema.

Nachdem die Aktion definiert wurde, kann sie sowohl verwendet werden:

* In Journey werden in einer benutzerdefinierten Aktionsaktivität zum Abrufen von Inhalten
* Verwenden Sie in Journey- und eingehenden Kampagnen einen externalDataLookup-Helper, um Daten in einer eingehenden Aktion abzurufen.

## Leitplanken und Einschränkungen

Siehe auch Benutzerdefinierte Aktionen in [!DNL Journey Optimizer] Kampagnen und Journey für eingehende Kanäle #GuardrailsandGuidelines .

* Standardmäßig verwendet [!DNL Journey Optimizer] beim Aufruf eines externen Endpunkts eine maximale Wartezeit von 300 ms. Wenden Sie sich an [!DNL Journey Optimizer] Engineering, um diese maximale Wartezeit für einen Endpunkt zu erhöhen.
* Im Personalization-Editor können Sie mit [!DNL Journey Optimizer] das Schema der Endpunktantwort beim Einfügen von Ausdrücken nicht durchsuchen und es werden keine Verweise auf JSON-Attribute aus der in Ausdrücken verwendeten Antwort validiert.
* Die unterstützten Datentypen für Payload-Variablenparameter, die über den externalDataLookup-Helper ersetzt werden sollen, sind „String“, „Integer“, „Decimal“, „Boolean“, „listString“, „listInt“, „listInteger“ und „listDecimal“.
* Änderungen an einer Aktionskonfiguration werden nicht in den entsprechenden externalDataLookup-Aufrufen in Live-Kampagnen und Journey-Aufrufen übernommen. Damit eine Änderung übernommen wird, müssen Sie alle Live-Kampagnen oder Journey kopieren oder ändern, die die Aktion in einem externalDataLookup-Helper verwenden.
* Die Verwendung von Variablen wird noch nicht innerhalb der Parameter der externen Datensuche unterstützt.
* Dynamischer URL-Pfad wird derzeit nicht unterstützt.  - Verbesserungen bei eingehenden benutzerdefinierten Aktionen#DynamicPathSegments.
* Multi-Pass-Rendering wird unterstützt.
* Authentifizierungsoptionen in der Aktionskonfiguration werden derzeit nicht vom externalDataLookup-Helper unterstützt. In der Zwischenzeit können Sie bei der API-schlüsselbasierten Authentifizierung oder anderen Nur-Text-Autorisierungsschlüsseln diese als Header-Felder in der Aktionskonfiguration angeben.

## Konfigurieren einer Aktion und Verwenden des Helpers

Gehen Sie wie folgt vor, um eine Aktion zu definieren und den Helper für die Personalisierung zu verwenden:

1. Erstellen Sie eine Aktion zum Konfigurieren des Endpunkts für die Suche. Dies muss nur einmal für jeden Endpunkt durchgeführt werden und sollte von einem technischen Anwender durchgeführt werden. [Erfahren Sie, wie Sie eine benutzerdefinierte Aktion konfigurieren](../action/about-custom-action-configuration.md)

   Notieren Sie sich die Aktions-ID und kopieren Sie sie.

   ![](assets/external-data-action.png)

1. Erstellen Sie eine eingehende Kampagne oder Journey-Aktion. In diesem Beispiel zeigen wir, wie der externalDataLookup-Helper in einer Code-basierten Experience JSON-Aktion verwendet wird, aber er kann in einem Personalisierungsfeld in jedem eingehenden Kanal verwendet werden.

1. Bearbeiten Sie den Inhalt der Aktion, navigieren Sie zu Hilfsfunktionen im Personalisierungseditor und dann zu **[!UICONTROL Hilfsfunktionen]** > **[!UICONTROL Helper]**.

1. Klicken Sie auf die Schaltfläche `+` , um den Helper externalDataLookup einzufügen. Der Hilfsausdruck wird mit Platzhalterwerten für die `actionId` und die `result` in den Editor eingefügt.

   ![](assets/external-data-personalization.png)

   Ersetzen Sie die Platzhalterwerte wie folgt:

   * `actionId`: Fügen Sie die zuvor kopierte Aktions-ID ein.
   * `result`: Legen Sie den Namen Ihrer Wahl fest. Sie verwenden diese Ergebnisvariable, um auf den abgerufenen Inhalt zuzugreifen.

1. Fügen Sie alle Variablenparameterwerte hinzu, die als Teil des Endpunkt-Aufrufs übergeben werden sollen. So können Sie beispielsweise einen Parameter für die Sprache und einen Parameter für die maximale Anzahl von Elementen übergeben.

   ![](assets/external-data-personalization-example.png)

1. Verwenden Sie die Ergebnisvariable, um auf die abgerufenen Daten zuzugreifen und sie in den Inhalt für die eingehende Aktion einzufügen. So können Sie beispielsweise ein JSON-Array von Elementen zurückgeben, die vom Endpunkt abgerufen wurden.

   ![](assets/external-data-personalization-result.png)

## Funktionsweise

### Laufzeitausführung

Wenn eine eingehende Aktion den Helper externalDataLookup enthält, wird der Endpunkt zum Zeitpunkt des Empfangs und der Verarbeitung der [!DNL Journey Optimizer] Personalisierungsanfrage durch die AEP Edge Network dynamisch aufgerufen.

Das bedeutet, dass der externe Endpunkt in der Lage sein muss, mindestens so viel gleichzeitiges Laden und Durchsatz zu verarbeiten, wie der Client für die angegebene Oberfläche an die AEP Edge Network sendet.

### Syntax

`{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}`

### Übergeben von Parametern

Wenn der externe Endpunkt aufgerufen wird, werden alle in der Aktion definierten konstanten Kopfzeilenwerte, Abfrageparameter und Wert der Anfrage-Payload mit den in der Aktionskonfiguration angegebenen Werten gesendet.

Für beliebige Variablenkopfwerte, Abfrage-/Pfadparameter oder Anfrage-Payload-Werte können Sie Werte mithilfe von Parametern dynamisch an den externalDataLookup-Helper übergeben.

Parameternamen:

* Kopfzeilenparameter: Kopfzeile.<parameter-name>
* Abfrageparameter: Abfrage.<parameter-name>
* Payload-Parameter: Payload.<parameter-name>
* Pfadparameter: dynamic_path.<parameter-name>

Beispiel:

`{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}`

Parameterwerte können feste Werte sein oder durch Verweise auf Profilfelder oder andere kontextuelle Attribute personalisiert werden, z. B.:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}`

Payload-Parameter können mit Punktnotation bereitgestellt werden, um auf verschachtelte JSON-Attribute zu verweisen, z. B.:

`{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}`

### Zugriff auf das Ergebnis

Um auf die Daten zuzugreifen, die von einem externen Endpunkt-Suchaufruf abgerufen wurden, können Sie mithilfe von Personalisierungsausdrücken und Hilfsfunktionen auf Felder verweisen, die in der Antwort-Payload in der Aktionsdefinition definiert sind.

Wenn die Antwort-Payload in der Aktion beispielsweise wie folgt aussieht:

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Dann können Sie beispielsweise die Beschreibung des ersten Videos in einer Code-basierten Experience HTML-Aktion wie der folgenden abrufen und darauf zugreifen:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Sie können die Elemente auch abrufen und in einer Schleife durchlaufen, um ein Element-Array in einer Code-basierten Experience JSON-Aktion wie der folgenden zurückzugeben:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Fehlerbehebung

### Zeitüberschreitungen und Fehlerbehandlung

[!DNL Journey Optimizer] verwendet beim Aufruf des externen Endpunkts eine strikte Zeitüberschreitung, um die Leistungsmerkmale von AEP Edge Network mit niedriger Latenz und hohem Durchsatz beizubehalten.

Wenn beim Erreichen des Endpunkts eine Zeitüberschreitung auftritt oder ein anderer Fehler auftritt, ist die Ergebnisvariable leer. Alle Verweise auf Attribute innerhalb der Ergebnisvariablen sind in diesem Fall ebenfalls leer. Wenn Sie das Attribut einfach im Inhalt anzeigen, wird es als leer angezeigt. Wenn Sie versuchen, ein Array-Attribut im Ergebnis zu durchlaufen, werden keine Elemente zurückgegeben.

Wenn Sie Zeitüberschreitungen oder Fehler eleganter handhaben möchten, indem Sie Fallback-Inhalte anzeigen, können Sie überprüfen, ob das Ergebnis der Suche leer ist, und in diesem Fall Fallback-Inhalte anzeigen.

Sie können beispielsweise einen Fallback-Wert für ein einzelnes Attribut wie das folgende anzeigen:

`First video description: {%=result.videos[0].description ?: "none found" %}`

Oder Sie können einen gesamten Inhaltsblock bedingt wie folgt rendern:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
{%#if result%}
   ... do something with result ...
{%else%}
    ... return fallback content ...
{%/if%}
```

### Debugging

Um Sie beim Debuggen zu unterstützen, werden Zeitüberschreitungs- und Fehlerdetails für die externe Datensuche in die Edge Delivery-Ansicht in AEP Assurance aufgenommen. Wenn bei einer eingehenden Aktion keine erwarteten Ergebnisse für einen externalDataLookup-Helper angezeigt werden, können Sie eine Assurance-Sitzung starten, einen [!DNL Journey Optimizer]-Aufruf aus einer Web- oder mobilen Implementierung initiieren und die Edge Delivery-Ansicht verwenden, um Details zur Zeitüberschreitung oder zu Fehlern zu ermitteln.

Beispiel:

Im Abschnitt Edge Delivery des Assurance-Trace wurde im Rahmen der Ausführungsdetails ein neuer CustomActions-Block mit ähnlichen Anfrage- und Antwortdetails wie dem folgenden hinzugefügt. Der Abschnitt Fehler sollte beim Debuggen helfen, wenn beim Ausführen benutzerdefinierter Aktionen Probleme aufgetreten sind

![](assets/external-data-troubleshoot.png)

## Häufig gestellte Fragen

* Wie wird ein kontextuelles Attribut aus der Anfrage als Parameter an eine externe Datensuche übergeben?

  Verwenden Sie das Menü Kontextuelle Attribute > Datenstrom > Ereignis , um das von Ihnen verwendete Erlebnisereignisschema zu durchsuchen und das entsprechende Attribut als Parameterwert wie den folgenden einzufügen:

  `{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

* Macht [!DNL Journey Optimizer] eine Zwischenspeicherung von externen Endpunktantworten?

  Derzeit nicht verfügbar. Diese Funktion wird in Zukunft unterstützt.
