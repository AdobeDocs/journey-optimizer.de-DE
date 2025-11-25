---
product: journey optimizer
title: Zeichenfolgenfunktionen
description: Erfahren Sie mehr über Zeichenfolgefunktionen
feature: Journeys
role: Developer
level: Experienced
keywords: Zeichenfolge, Funktionen, Ausdruck, Journey, Text, Manipulation
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: ht
source-wordcount: '1127'
ht-degree: 100%

---

# Zeichenfolgenfunktionen {#string-functions}

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
| string | Zeichenfolge |

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

* Zeichenfolge

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
| string | string |
| string searched | Zeichenfolge |

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

* Zeichenfolge

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

Gibt die Position (im ersten Argument) des ersten Auftretens des zweiten Parameters zurück. Gibt „–1“ zurück, wenn keine Übereinstimmung vorliegt.

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

* Zeichenfolge

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

+++

## isNotEmpty {#isNotEmpty}

Gibt „true“ zurück, wenn die Zeichenfolge im Parameter nicht leer ist.

+++Syntax

`isNotEmpty(<parameters>)`

+++

+++Parameter

* Zeichenfolge

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

Gibt die Position (im ersten Argument) des letzten Auftretens des zweiten Parameters zurück. Gibt „–1“ zurück, wenn keine Übereinstimmung vorliegt.

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

Gibt „11“ zurück.

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

* Zeichenfolge

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
| string | string |
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
| string | Zeichenfolge |

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

