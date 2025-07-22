---
solution: Journey Optimizer
product: journey optimizer
title: Personalisieren von Inhalten mit Daten aus einem externen Endpunkt
description: Erfahren Sie, wie Sie Daten dynamisch von einem externen Endpunkt abrufen können, um eingehende Inhalte zu personalisieren.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 1%

---


# Personalisieren von Inhalten mit Daten aus einem externen Endpunkt {#data-endpoint}

>[!AVAILABILITY]
>
>Diese Funktion ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit).

Mit Journey Optimizer können Sie Daten von einem externen Endpunkt nutzen, um Ihre Inhalte in eingehenden Kanälen wie dem Code-basierten Erlebnis-, Web- und In-App-Nachrichtenkanal zu personalisieren.

Dazu steht `externalDataLookup` eine dedizierte Hilfsfunktion im Personalisierungseditor zur Verfügung. Um den Helper zu verwenden, müssen Sie zunächst eine [!DNL Journey Optimizer] (**) definieren** in der Sie Details zum externen Endpunkt konfigurieren.

## Wichtige Informationen

### Laufzeitausführung

Wenn eine eingehende Aktion den Helper externalDataLookup enthält, wird der Endpunkt zum Zeitpunkt des Empfangs und der Verarbeitung der Personalisierungsanfrage durch die [!DNL Adobe Experience Platform] Edge Network dynamisch aufgerufen. Das bedeutet, dass der externe Endpunkt in der Lage sein muss, mindestens so viel gleichzeitiges Laden und Durchsatz zu verarbeiten, wie der Client für die angegebene Oberfläche an die AEP Edge Network sendet.

### Authentifizierung

Authentifizierungsoptionen in der Aktionskonfiguration werden derzeit nicht vom externalDataLookup-Helper unterstützt.
In der Zwischenzeit können Sie bei der API-schlüsselbasierten Authentifizierung oder anderen Nur-Text-Autorisierungsschlüsseln diese als Header-Felder in der Aktionskonfiguration angeben.
NUR für Adobe-interne Endpunkte: Wenden Sie sich an das AJO-Engineering, um die Service-Token-basierte Authentifizierung für einen Endpunkt zu aktivieren.

### Leitplanken und Einschränkungen

Weitere Informationen finden Sie unter Benutzerdefinierte Aktionen in AJO Inbound Channel-Kampagnen #GuardrailsandGuidelines Journey.

Standardmäßig verwendet AJO beim Aufruf eines externen Endpunkts eine maximale Wartezeit von 300 ms. Wenden Sie sich an AJO Engineering, um diese maximale Wartezeit für einen Endpunkt zu erhöhen.
Im Personalization-Editor können Sie mit AJO das Schema der Endpunktantwort beim Einfügen von Ausdrücken nicht durchsuchen und es werden keine Verweise auf JSON-Attribute aus der in Ausdrücken verwendeten Antwort validiert.
Die unterstützten Datentypen für Payload-Variablenparameter, die über den externalDataLookup-Helper ersetzt werden sollen, sind Zeichenfolge, Ganzzahl, Dezimal, Boolesch, listString, listInt, listInteger, listDecimal
Änderungen an einer Aktionskonfiguration werden nicht in den entsprechenden externalDataLookup-Aufrufen in Live-Kampagnen und Journey-Aufrufen übernommen. Damit eine Änderung übernommen wird, müssen Sie alle Live-Kampagnen oder Journey kopieren oder ändern, die die Aktion in einem externalDataLookup-Helper verwenden.
Die Verwendung von Variablen wird noch nicht innerhalb der Parameter der externen Datensuche unterstützt.
Dynamischer URL-Pfad wird derzeit nicht unterstützt.  - Verbesserungen bei eingehenden benutzerdefinierten Aktionen#DynamicPathSegments

## Erstellen einer Aktion

Erstellen Sie eine Aktion zum Konfigurieren des Endpunkts für die Suche. Dies muss nur einmal für jeden Endpunkt durchgeführt werden und sollte von einem technischen Anwender durchgeführt werden. Siehe diese Seite.

Dieselbe Aktion kann sowohl in einer Aktivität vom Typ **[!UICONTROL Benutzerdefinierte Aktion]** zum Abrufen von Inhalten auf einer Journey als auch in einer `externalDataLookup` Hilfsfunktion zum Abrufen von Daten in einer eingehenden Aktion auf einer Journey oder Kampagne verwendet werden.

Navigieren Sie zum Menü **[!UICONTROL Administration]** / **[!UICONTROL Konfigurationen]** .

Notieren Sie sich die Aktions-ID und kopieren Sie sie zur Verwendung in Schritt 6.


## Personalisieren von Inhalten mit abgerufenen Daten

### Fügen Sie die Hilfsfunktion zu Ihrem Inhalt hinzu

1. Erstellen einer eingehenden Kampagne oder Journey-Aktion und Bearbeiten ihres Inhalts.

1. Suchen Sie den Inhalt, in dem Sie die vom externen Endpunkt abgerufenen Daten verwenden möchten, und greifen Sie auf den Personalisierungseditor zu.

1. Wählen Sie das Menü Hilfsfunktionen aus und suchen Sie die Hilfsfunktion `externalDataLookup` .

1. Wählen Sie diese Option aus, um die zugehörige Syntax in Ihren Code einzufügen und die `actionId`- und `result` wie folgt zu ersetzen:

   * `actionId` : Fügen Sie die bei der Erstellung der Aktion kopierte Aktions-ID ein.
   * `result`: Legen Sie diesen Parameter auf den Namen Ihrer Wahl fest. Sie verwenden diese Ergebnisvariable, um auf den abgerufenen Inhalt zuzugreifen.

1. Fügen Sie alle Variablenparameterwerte hinzu, die als Teil des Endpunkt-Aufrufs übergeben werden sollen. So können Sie beispielsweise einen Parameter für die Sprache und einen Parameter für die maximale Anzahl von Elementen übergeben.

### Personalisieren mit abgerufenen Daten

Um auf die Daten zuzugreifen, die von einem externen Endpunkt-Suchaufruf abgerufen wurden, können Sie mithilfe von Personalisierungsausdrücken und Hilfsfunktionen auf Felder verweisen, die in der Antwort-Payload in der Aktionsdefinition definiert sind.

Verwenden Sie die Variable `result` , um auf die abgerufenen Daten zuzugreifen und sie in den Inhalt für die eingehende Aktion einzufügen. So können Sie beispielsweise ein JSON-Array von Elementen zurückgeben, die vom Endpunkt abgerufen wurden.

Nehmen wir das folgende Beispiel, bei dem die Antwort-Payload in der Aktion wie folgt konfiguriert wurde:

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

Personalization-Beispiel 1: Anzeigen der Beschreibung des ersten Videos in einer Code-basierten Experience HTML-Aktion:

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization-Beispiel 2: Zurückgeben eines Element-Arrays in einer Code-basierten Experience JSON-Aktion:

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

## Zeitüberschreitungen und Fehlerbehandlung

AJO verwendet beim Aufruf des externen Endpunkts eine strikte Zeitüberschreitung, um die Leistungsmerkmale von AEP Edge Network mit niedriger Latenz und hohem Durchsatz beizubehalten.

Wenn beim Erreichen des Endpunkts eine Zeitüberschreitung auftritt oder ein anderer Fehler auftritt, ist die Ergebnisvariable leer. Alle Verweise auf Attribute innerhalb der Ergebnisvariablen sind in diesem Fall ebenfalls leer. Wenn Sie das Attribut einfach im Inhalt anzeigen, wird es als leer angezeigt. Wenn Sie versuchen, ein Array-Attribut im Ergebnis zu durchlaufen, werden keine Elemente zurückgegeben.

Wenn Sie Zeitüberschreitungen oder Fehler eleganter handhaben möchten, indem Sie Fallback-Inhalte anzeigen, können Sie überprüfen, ob das Ergebnis der Suche leer ist, und in diesem Fall Fallback-Inhalte anzeigen.

Sie können beispielsweise einen Fallback-Wert für ein einzelnes Attribut wie das folgende anzeigen:

Erste Videobeschreibung: {%=result.videos[0].description ?: „none found“ %}


Oder Sie können einen gesamten Inhaltsblock bedingt wie folgt rendern:

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if Ergebnis%}
… etwas mit dem Ergebnis machen …
{%else%}
… Fallback-Inhalt zurückgeben …
{%/if%}
Debugging
Um Sie beim Debuggen zu unterstützen, werden Zeitüberschreitungs- und Fehlerdetails für die externe Datensuche in die Edge Delivery-Ansicht in AEP Assurance aufgenommen. Wenn bei einer eingehenden Aktion keine erwarteten Ergebnisse für einen externalDataLookup-Helper angezeigt werden, können Sie eine Assurance-Sitzung starten, einen AJO-Aufruf über eine Web- oder Mobile-Implementierung initiieren und die Edge Delivery-Ansicht verwenden, um Details zur Zeitüberschreitung oder zu Fehlern zu ermitteln.

Beispiel:

Im Edge Delivery-Abschnitt des Assurance-Trace wurde im Rahmen der Ausführungsdetails ein neuer CustomActions-Block hinzugefügt mit

Anfrage- und Antwortdetails ähnlich denen unten. Der Abschnitt Fehler sollte beim Debuggen helfen, wenn beim Ausführen benutzerdefinierter Aktionen Probleme aufgetreten sind

## Häufig gestellte Fragen

+++Wie übergebe ich ein kontextuelles Attribut aus der Anfrage als Parameter an eine externe Datensuche?

Verwenden Sie das Menü Kontextuelle Attribute > Datenstrom > Ereignis , um das von Ihnen verwendete Erlebnisereignisschema zu durchsuchen und das entsprechende Attribut als Parameterwert wie den folgenden einzufügen:

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++Ermöglicht AJO das Zwischenspeichern externer Endpunktantworten?

Derzeit nicht verfügbar. Diese Funktion wird in Zukunft unterstützt.

+++









Syntax
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Übergeben von Parametern
Wenn der externe Endpunkt aufgerufen wird, werden alle in der Aktion definierten konstanten Kopfzeilenwerte, Abfrageparameter und Wert der Anfrage-Payload mit den in der Aktionskonfiguration angegebenen Werten gesendet.

Für beliebige Variablenkopfwerte, Abfrage-/Pfadparameter oder Anfrage-Payload-Werte können Sie Werte mithilfe von Parametern dynamisch an den externalDataLookup-Helper übergeben.

Parameternamen:

Kopfzeilenparameter: Kopfzeile.<parameter-name>
Abfrageparameter: Abfrage.<parameter-name>
Payload-Parameter: Payload.<parameter-name>
Pfadparameter: dynamic_path.<parameter-name>
Beispiel:

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
Parameterwerte können feste Werte sein oder durch Verweise auf Profilfelder oder andere kontextuelle Attribute personalisiert werden, z. B.:

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
Payload-Parameter können mit Punktnotation bereitgestellt werden, um auf verschachtelte JSON-Attribute zu verweisen, z. B.:

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}