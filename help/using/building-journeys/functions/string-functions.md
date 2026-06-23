---
product: journey optimizer
title: Zeichenfolgen-Funktionen
description: Erfahren Sie mehr über Zeichenfolgefunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Zeichenfolge, Funktionen, Ausdruck, Journey, Text, Manipulation
version: Journey Orchestration
exl-id: 8186c564-56fa-417a-afd3-8e479e5b23b9
TQID: https://experienceleague.adobe.com/wrP3c7l3uHzN6w3l-fXBQOSb5Tx2NuW-6iyogKpDPc8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1668
ht-degree: 68%

---

# Zeichenfolgen-Funktionen {#string-functions}

Mit Zeichenfolgenfunktionen können Sie Textwerte in Ihren Journey-Ausdrücken bearbeiten und mit ihnen arbeiten. Diese Funktionen sind für die Textverarbeitung, Validierung, Umwandlung und Analyse in Ihren Customer Journeys unerlässlich.

Verwenden Sie Zeichenfolgenfunktionen für Folgendes:

* Verketten und Kombinieren mehrerer Textwerte ([contact](#concat))
* Suchen nach bestimmten Textmustern oder Unterzeichenfolgen ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* Vergleichen von Zeichenfolgen mit Übereinstimmungen, bei denen die Groß-/Kleinschreibung beachtet oder nicht beachtet wird ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* Überprüfen von Anfang und Ende von Zeichenfolgen ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase))
* Extrahieren von Textteilen mithilfe von Vorgängen in Unterzeichenfolgen ([substr](#substr))
* Umwandeln von Text in Groß- oder Kleinbuchstaben ([upper](#upper), [lower](#lower), [trim](#trim))
* Überprüfen, ob Zeichenfolgen leer sind oder bestimmte Werte enthalten ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))
* Ersetzen von Textmustern durch neue Werte ([replace](#replace), [replaceAll](#replaceAll))
* Aufspalten von Zeichenfolgen zur weiteren Verarbeitung in Arrays ([split](#split))
* Abrufen der Zeichenfolgenlänge ([length](#length)) oder Generieren von eindeutige Kennungen ([uuid](#uuid))

Zeichenfolgenfunktionen bieten umfangreiche Textbearbeitungsfunktionen, die eine ausgefeilte Datenverarbeitung und eine bedingte Logik ermöglichen, die auf Textinhalten in Ihren Journey-Ausdrücken basiert.

## concat {#concat}

Verkettet zwei Zeichenfolgenparameter oder eine Liste von Zeichenfolgen.

+++Syntax

`concat(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Liste | listString |
| string | string |

+++

+++Signatur und zurückgegebener Typ

`concat(<string>,<string>)`

`concat(<listString>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`concat("Hello","World")`

Gibt „HelloWorld“ zurück.

`concat(["Hello"," ","World"])`

Gibt „Hello World“ zurück.

+++

## contain {#contain}

Überprüft, ob die zweite Argumentzeichenfolge in der ersten Argumentzeichenfolge enthalten ist.

+++Syntax

`contain(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`contain(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`contain("rowing is great", "great")`

Gibt „true“ zurück.

+++

## containIgnoreCase {#containIgnoreCase}

Überprüft, ob die zweite Argumentzeichenfolge in der ersten Argumentzeichenfolge enthalten ist, ohne Groß-/Kleinschreibung zu berücksichtigen.

+++Syntax

`containIgnoreCase(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | Zeichenfolge |
| string searched | string |

+++

+++Signatur und zurückgegebener Typ

`containIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`containIgnoreCase("rowing is great", "GREAT")`

Gibt „true“ zurück.

+++

## endWith {#endWith}

Gibt „true“ zurück, wenn der zweite Parameter ein Suffix des ersten Parameters ist.

+++Syntax

`endWith(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | string |
| suffix | string |

+++

+++Signatur und zurückgegebener Typ

`endWith(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`endWith("Hello World", "World")`

Gibt „true“ zurück.

`endWith("Hello World", "Hello")`

Gibt „false“ zurück.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Überprüft, ob die erste Argumentzeichenfolge mit einer bestimmten Zeichenfolge endet (zweite Argumentzeichenfolge), wobei Groß-/Kleinschreibung nicht berücksichtigt wird.

+++Syntax

`endWithIgnoreCase(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | string |
| suffix | string |

+++

+++Signatur und zurückgegebener Typ

`endWithIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`endWithIgnoreCase("rowing is great", "AT")`

Gibt „true“ zurück.

+++

## equalIgnoreCase {#equalIgnoreCase}

Vergleicht die erste Argumentzeichenfolge mit der zweiten Argumentzeichenfolge und ignoriert dabei die Groß-/Kleinschreibung.

+++Syntax

`equalIgnoreCase(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`equalIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Gibt „true“ zurück.

+++

## indexOf {#indexOf}

Gibt die Position (im ersten Argument) des ersten Auftretens des zweiten Parameters zurück. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

+++Syntax

`indexOf(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | Zeichenfolge |
| angegebener Wert | Zeichenfolge |

+++

+++Signatur und zurückgegebener Typ

`indexOf(<string>,<string>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`indexOf("Hello", "l")`

Gibt 2 zurück.

Erklärung:

In „Hello“ befindet sich das erste Auftreten von „l“ an Position 2.

+++

## isEmpty {#isEmpty}

Gibt „true“ zurück, wenn die Zeichenfolge im Parameter keine Zeichen enthält.

+++Syntax

`isEmpty(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`isEmpty(<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`isEmpty("")`

Gibt „true“ zurück.

`isEmpty("Hello World")`

Gibt „false“ zurück.

`isEmpty(<null>)`

Gibt „false“ zurück.

+++

## isNotEmpty {#isNotEmpty}

Gibt „true“ zurück, wenn die Zeichenfolge im Parameter nicht leer ist.

+++Syntax

`isNotEmpty(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`isNotEmpty(<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`isNotEmpty("")`

Gibt „false“ zurück.

`isNotEmpty("hello")`

Gibt „true“ zurück.

+++

## lastIndexOf {#lastIndexOf}

Gibt die Position (im ersten Argument) des letzten Auftretens des zweiten Parameters zurück. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

+++Syntax

`lastIndexOf(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | Zeichenfolge |
| angegebener Wert | Zeichenfolge |

+++

+++Signatur und zurückgegebener Typ

`lastIndexOf(<string>,<string>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`lastIndexOf("Hello", "l")`

Gibt 3 zurück.

Erklärung:

In „Hello“ befindet sich das letzte Auftreten von „l“ an Position 3.

+++

## length {#length}

Gibt die Anzahl der Zeichen des Zeichenfolgenausdrucks im Parameter zurück.

+++Syntax

`length(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`length(<string>)`

Gibt eine Ganzzahl zurück.

+++

+++Beispiele

`length("Hello World")`

Gibt 11 zurück.

+++

## lower {#lower}

Gibt eine Version des Parameters in Kleinbuchstaben zurück.

+++Syntax

`lower(<parameter>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`lower(<string>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`lower("A")`

Gibt „a“ zurück.

+++

## matchRegExp {#matchRegExp}

Gibt „true“ zurück, wenn die Zeichenfolge im ersten Parameter mit dem regulären Ausdruck im zweiten Parameter übereinstimmt. Weitere Informationen finden Sie auf [dieser Seite](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Syntax

`matchRegExp(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|--- |--- |
| string | string |
| regexp | string |

+++

+++Signatur und zurückgegebener Typ

`matchRegExp(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`matchRegExp("12345", "\\d+")`

Gibt „true“ zurück.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Überprüft, ob sich die erste Argumentzeichenfolge von der zweiten Argumentzeichenfolge unterscheidet, wobei Groß-/Kleinschreibung ignoriert wird.

+++Syntax

`notEqualIgnoreCase(<parameters>)`

+++

+++Parameter

* string

+++

+++Signatur und zurückgegebener Typ

`notEqualIgnoreCase(<string>,<string>)`

Gibt einen booleschen Wert zurück.

+++

+++Beispiele

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Ersetzt das erste Auftreten, das mit der Zielzeichenfolge übereinstimmt, in der Basiszeichenfolge durch die Ersatzzeichenfolge.

Die Ersetzung verläuft vom Anfang der Zeichenfolge zum Ende. Wenn Sie z. B. in der Zeichenfolge „aaa“ „aa“ durch „b“ ersetzen, erhalten Sie „ba“ und nicht „ab“.

+++Syntax

`replace(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|--------------|
| base | string |
| target | string (RegExp) |
| replacement | string |

+++

+++Signatur und zurückgegebener Typ

`replace(<base>,<target>,<replacement>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`replace("Hello World", "l", "x")`

Gibt „Hexlo World“ zurück.

**Beispiel mit RegExp:**

Da der Zielparameter ein regulärer Ausdruck ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen auslassen. Siehe folgendes Beispiel:

* auszuwertende Zeichenfolge: `|OFFER_A|OFFER_B`
* bereitgestellt von einem Profilattribut `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Zeichenfolge, die ersetzt werden soll: `|OFFER_A`
* Zeichenfolge ersetzt durch: `''`
* Sie müssen `\\` vor dem Zeichen `|` hinzufügen.

Der Ausdruck lautet:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

Die zurückgegebene Zeichenfolge lautet: `|OFFER_B`

Sie können auch die Zeichenfolge erstellen, die mit einem bestimmten Attribut ersetzt werden soll:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Ersetzt jedes Auftreten, das mit der Zielzeichenfolge übereinstimmt, in der Basiszeichenfolge durch die Ersatzzeichenfolge.

Die Ersetzung verläuft vom Anfang der Zeichenfolge zum Ende. Wenn Sie z. B. in der Zeichenfolge „aaa“ „aa“ durch „b“ ersetzen, erhalten Sie „ba“ und nicht „ab“.

+++Syntax

`replaceAll(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|--------------|
| base | string |
| target | string (RegExp) |
| replacement | string |

+++

+++Signatur und zurückgegebener Typ

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`replaceAll("Hello World", "l", "x")`

Gibt „Hexxo Worxd“ zurück.

Da der Zielparameter ein regulärer Ausdruck ist, müssen Sie je nach der Zeichenfolge, die Sie ersetzen möchten, möglicherweise einige Zeichen auslassen. Siehe das Beispiel in der Funktion [replace](#replace).

+++

## split {#split}

Spaltet die erste Argumentzeichenfolge mit einer Trennzeichenfolge (zweite Argumentzeichenfolge, die ein regulärer Ausdruck sein kann) auf, um eine Liste von Zeichenfolgen (Token) zu erzeugen.

+++Syntax

`split(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| Eingabezeichenfolge | Zeichenfolge |
| Trennzeichenfolge | Zeichenfolge |

+++

+++Signaturen und zurückgegebener Typ

`split(<input string>, <separator string>)`

Gibt eine listString zurück.

+++

+++Beispiele

`split("A_B_C", "_")`

Gibt `["A","B","C"]` zurück

Beispiel mit dem Ereignisfeld „event.appVersion“ mit dem Wert: 20.45.2.3434

`split(@event{event.appVersion}, "\\.")`

Gibt `["20", "45", "2", "3434"]` zurück

+++

## startWith {#startWith}

Gibt „true“ zurück, wenn der zweite Parameter ein Präfix des ersten Parameters ist.

+++Syntax

`startWith(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-------------|--------|
| string | string |
| prefix | string |

+++

+++Signatur und zurückgegebener Typ

`startWith(<string>,<string>)`

Geben einen booleschen Wert zurück.

+++

+++Beispiele

`startWith("Hello World", "Hello")`

Gibt „true“ zurück.

`startWith("Hello World", "World")`

Gibt „false“ zurück.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Gibt „true“ zurück, wenn der zweite Parameter ein Präfix des ersten Parameters ist, ohne die Groß-/Kleinschreibung zu berücksichtigen.

+++Syntax

`startWithIgnoreCase(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-------------|--------|
| string | string |
| prefix | string |

+++

+++Signatur und zurückgegebener Typ

`startWithIgnoreCase(<string>,<string>)`

Geben einen booleschen Wert zurück.

+++

+++Beispiele

`startWithIgnoreCase("rowing is great", "RO")`

Gibt „true“ zurück.

+++

## substr {#substr}

Gibt die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurück. Wenn der Endindex nicht definiert ist, wird die Zeichenfolge zwischen dem Anfangsindex und dem Ende zurückgegeben.

+++Syntax

`substr(<parameters>)`

+++

+++Parameter

| Parameter | type |
|-------------|----------|
| string | Zeichenfolge |
| beginIndex | integer |
| endIndex | integer |

+++

+++Signatur und zurückgegebener Typ

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`substr("Hello World",6)`

Gibt „World“ zurück.

`substr("Hello World", 0, 5)`

Gibt „Hello“ zurück.

+++

## trim {#trim}

Entfernt Leerzeichen am Anfang und Ende.

+++Syntax

`trim(<parameters>)`

+++

+++Parameter

| Parameter | Typ |
|-----------|------------------|
| string | string |

+++

+++Signatur und zurückgegebener Typ

`trim(<string>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`trim(" Hello ")`

Gibt „Hello“ zurück.

+++

## upper {#upper}

Gibt eine Version des Parameters in Großbuchstaben zurück.

+++Syntax

`upper(<parameters>)`

+++

+++Signatur und zurückgegebener Typ

`upper(<string>)`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`upper("b")`

Gibt „B“ zurück.

+++

## uuid {#uuid}

Generiert einen zufälligen UUID (Universal Unique IDentifier).

+++Syntax

`uuid()`

+++

+++Parameter 

Für diese Funktion sind keine Parameter erforderlich.

+++

+++Signatur und zurückgegebener Typ

`uuid()`

Gibt eine Zeichenfolge zurück.

+++

+++Beispiele

`uuid()`

Gibt „79e70b7f-8a85-400b-97a1-9f9826121553“ zurück.

+++

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden alle Zeichenfolgenfunktionen dokumentiert, die in AJO-Journey-Ausdrücken verfügbar sind und die Textsuche, den Vergleich, die Transformation, die Extraktion, die Validierung, das Ersetzen, die Aufspaltung und die Erstellung eindeutiger Bezeichner abdecken.

**intents:**
* Verketten von zwei oder mehr Zeichenfolgen mithilfe von `concat`
* Suchen Sie mithilfe von `contain` oder `containIgnoreCase` nach einer Teilzeichenfolge in einer Zeichenfolge (Groß-/Kleinschreibung wird nicht beachtet)
* Vergleichen Sie zwei Zeichenfolgen, ohne die Groß-/Kleinschreibung zu berücksichtigen, indem Sie `equalIgnoreCase` oder `notEqualIgnoreCase` verwenden
* Überprüfen Sie, ob eine Zeichenfolge mit einem bestimmten Präfix oder Suffix beginnt oder endet, indem Sie `startWith`, `endWith` und die Varianten ohne Unterscheidung der Groß-/Kleinschreibung verwenden
* Extrahieren einer Teilzeichenfolge nach Indexpositionen mithilfe von `substr`
* Ersetzt das erste oder alle Vorkommen eines Musters in einer Zeichenfolge mit `replace` oder `replaceAll`
* Aufspalten einer Zeichenfolge in eine Liste von Token durch ein Trennzeichen mithilfe von `split`
* Generieren einer zufälligen UUID für eindeutige Kennungsanforderungen mithilfe von `uuid`
* Mit `isEmpty` oder `isNotEmpty` überprüfen, ob eine Zeichenfolge leer oder nicht leer ist

**Glossar:**
* **RegExp**: Ein Muster regulärer Ausdrücke, das als Zielparameter in `replace`, `replaceAll` und `matchRegExp` verwendet wird - Sonderzeichen müssen mit `\\` maskiert werden
* **UUID**: Universeller eindeutiger Bezeichner - eine zufällig generierte Zeichenfolgenkennung, die von `uuid()` zurückgegeben wird
* **substr**: Extrahiert einen Teil einer Zeichenfolge durch Angabe eines Startindex und eines optionalen Endindex (nullbasiert)

**Leitplanken:**
* Der `target` Parameter in `replace` und `replaceAll` wird als RegExp behandelt. Sonderzeichen (z. B. `|`, `.`) müssen mit `\\` maskiert werden
* `replace` ersetzt nur das erste übereinstimmende Vorkommen. Ersetzen Sie jedes Vorkommen mit `replaceAll`
* `isEmpty` gibt für Nullwerte „false“ zurück (nicht „true„); null wird nicht als leere Zeichenfolge betrachtet
* `indexOf` und `lastIndexOf` geben -1 zurück, wenn keine Übereinstimmung gefunden wird
* Zeichenfolgen-Indexpositionen sind nullbasiert (das erste Zeichen befindet sich an Position 0)

**Terminologie:**
* Kanonischer Name: Zeichenfolgen-Funktionen — Akronym: none — Varianten: Textfunktionen, Zeichenfolgen-Manipulationsfunktionen
* Synonyme: „contain“ = „Teilzeichenfolge überprüfen“; „split“ = „Tokenize string“; „trim“ = „strip whitespace“
* Verwechseln Sie nicht: „replace“ (nur erstes Vorkommen) ≠ „replaceAll“ (alle Vorkommen)
* Verwechseln Sie nicht: „indexOf“ (Position des ersten Vorkommens) ≠ „lastIndexOf“ (Position des letzten Vorkommens)
* Verwechseln Sie nicht: „isEmpty“ (wahr nur für Zeichenfolge mit Nulllänge) ≠ null check (isEmpty gibt „false“ für null zurück)
* Verwechseln Sie nicht: „equalIgnoreCase“ (gibt „true“ zurück, wenn „case ignoriert„) ≠ „notEqualIgnoreCase“ (gibt „true“ zurück, wenn ein anderer Groß-/Kleinschreibung ignoriert wird)

**FAQ:**
* **F: Wie kann ich überprüfen, ob eine Zeichenfolge eine Teilzeichenfolge enthält, unabhängig von der Groß-/Kleinschreibung?** — Verwenden Sie `containIgnoreCase("myString", "searchTerm")`, das „true“ zurückgibt, wenn der Suchbegriff in einem beliebigen Fall gefunden wird.
* **F: Was ist der Unterschied zwischen `replace` und `replaceAll`?** — `replace` ersetzt nur das erste übereinstimmende Vorkommen; `replaceAll` ersetzt jedes Vorkommen in der Zeichenfolge.
* **F: Warum muss ich das `|` Zeichen in `replace` auslassen?** — Der Zielparameter wird als regulärer Ausdruck behandelt. `|` ist ein spezielles RegExp-Zeichen und muss als `\\|` maskiert werden, damit er als Pipe behandelt wird.
* **Q: Gibt `isEmpty` „true“ für null zurück?** — Nein, `isEmpty` gibt „false“ für null zurück; es gibt nur „true“ für eine `""` mit null Länge zurück.
* **F: Wie extrahiere ich die Hauptversionsnummer aus einer Versionszeichenfolge wie „20.45.2.3434“?** - Verwenden Sie `getListItem(split(@event{event.appVersion}, "\\."), 0)`, um nach Punkt zu teilen und das erste Element abzurufen.
* **F: Wie generiere ich eine eindeutige Kennung in einem Journey-Ausdruck?** — Verwenden Sie `uuid()`, das eine zufällig generierte UUID-Zeichenfolge ohne erforderliche Parameter zurückgibt.

+++
