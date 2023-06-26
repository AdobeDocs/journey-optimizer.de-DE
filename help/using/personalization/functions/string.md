---
title: Bibliothek mit Zeichenfolgen-Funktionen
description: Bibliothek mit Zeichenfolgen-Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 118eddf540d1dfb3a30edb0b877189ca908944b1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Zeichenfolgen-Funktionen {#string}

Erfahren Sie, wie Sie im Ausdruckseditor Zeichenfolgenfunktionen verwenden können.

## Binnenmajuskel {#camelCase}

Mit der Funktion `camelCase` wird der erste Buchstabe eines jeden Wortes einer Zeichenfolge großgeschrieben.

**Syntax**

```sql
{%= camelCase(string)%}
```

**Beispiel**

Mit der folgenden Funktion wird der erste Buchstabe der Straßenadresse des Profils großgeschrieben.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Char-Code bei {#char-code-at}

Die Funktion `charCodeAt` gibt den ASCII-Wert eines Zeichens zurück, z. B. die Funktion charCodeAt in JavaScript. Als Eingabeargumente werden eine Zeichenfolge und eine Ganzzahl (die die Position des Zeichens definiert) benötigt und es wird der entsprechende ASCII-Wert zurückgegeben.

**Syntax**

```sql
{%= charCodeAt(string,int) %}: int
```

**Beispiel**

Die folgende Funktion gibt den ASCII-Wert von o zurück, also 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Verknüpfen {#concate}

Die Funktion `concat` kombiniert zwei Zeichenfolgen zu einer.

**Syntax**

```sql
{%= concat(string,string) %}
```

**Beispiel**

Mit der folgenden Funktion wird die Stadt und das Land eines Profils in einer einzigen Zeichenfolge kombiniert.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Enthält {#contains}

Mit der Funktion `contains` wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält.

**Syntax**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die überprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiele**

* Mit der folgenden Funktion wird geprüft, ob der Vorname des Profils den Buchstaben A enthält (in Groß- oder Kleinschreibung). Ist dies der Fall, wird „true“ zurückgegeben, andernfalls wird „false“ zurückgegeben.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* Die folgende Abfrage bestimmt unter Berücksichtigung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge „2010@gm“ enthält.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## Enthält nicht{#doesNotContain}

Mit der Funktion `doesNotContain` wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge nicht enthält.

**Syntax**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die überprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt unter Berücksichtigung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge „2010@gm“ nicht enthält.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Endet nicht mit{#doesNotEndWith}

Mit der Funktion `doesNotEndWith` wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet.

**Syntax**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person nicht mit „.com“ endet.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Beginnt nicht mit{#doesNotStartWith}

Mit der Funktion `doesNotStartWith` wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge beginnt.

**Syntax**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Personenname nicht mit „Joe“ beginnt.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codieren 64{#encode64}

Die Funktion `encode64` wird zum Codieren einer Zeichenfolge verwendet, um personenbezogene Daten (PI) beizubehalten, wenn diese z. B. in eine URL aufgenommen werden sollen.

**Syntax**

```sql
{%= encode64(string) %}
```

## Endet mit{#endsWith}

Mit der Funktion `endsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.

**Syntax**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard)/false. |

**Beispiel**

In der folgenden Abfrage wird unter Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob die E-Mail-Adresse des Benutzers mit „.com“ endet.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Gleich{#equals}

Mit der Funktion `equals` wird bestimmt, ob eine Zeichenfolge gleich der angegebenen Zeichenfolge ist, wobei zwischen Groß- und Kleinschreibung unterschieden wird.

**Syntax**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Mit der folgenden Abfrage wird unter Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob der Name der Person „John“ lautet.

```sql
{%=equals(profile.person.name,"John") %}
```

## Gleich ohne Groß-/Kleinschreibung{#equalsIgnoreCase}

Mit der Funktion `equalsIgnoreCase` wird bestimmt, ob eine Zeichenfolge gleich der angegebenen Zeichenfolge ist, wobei nicht zwischen Groß- und Kleinschreibung unterschieden wird.

**Syntax**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Mit der folgenden Abfrage wird ohne Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob der Name der Person „John“ lautet.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## E-Mail-Domain extrahieren {#extractEmailDomain}

Die Funktion `extractEmailDomain` wird verwendet, um die Domain einer E-Mail-Adresse zu extrahieren.

**Syntax**

```sql
{%= extractEmailDomain(string) %}
```

**Beispiel**

Mit der folgenden Abfrage wird die E-Mail-Domain der persönlichen E-Mail-Adresse extrahiert.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Währung formatieren {#format-currency}

Die Funktion `formatCurrency` wird verwendet, um eine beliebige Zahl in die entsprechende sprachabhängige Währungsdarstellung zu konvertieren, je nachdem, welches Gebietsschema als Zeichenfolge im zweiten Argument übergeben wurde.

**Syntax**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Beispiel**

Diese Abfrage gibt 56,00 £ zurück.

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## URL-Host abrufen {#get-url-host}

Die Funktion `getUrlHost` dient zum Abrufen des Host-Namens einer URL.

**Syntax**

```sql
{%= getUrlHost(string) %}: string
```

**Beispiel**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Gibt „www.myurl.com“ zurück

## URL-Pfad abrufen {#get-url-path}

Die Funktion `getUrlPath` wird verwendet, um den Pfad nach dem Domain-Namen einer URL abzurufen.

**Syntax**

```sql
{%= getUrlPath(string) %}: string
```

**Beispiel**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Gibt „/contact.html“ zurück

## URL-Protokoll abrufen {#get-url-protocol}

Die Funktion `getUrlProtocol` dient zum Abrufen des Protokolls einer URL.

**Syntax**

```sql
{%= getUrlProtocol(string) %}: string
```

**Beispiel**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Gibt „http“ zurück

## Index von {#index-of}

Die Funktion `indexOf` wird verwendet, um die Position (im ersten Argument) des ersten Auftretens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

**Syntax**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der im ersten Parameter gesucht werden soll. |

**Beispiel**

```sql
{%= indexOf("hello world","world" ) %}
```

Gibt 6 zurück.

## Ist leer {#isEmpty}

Mit der Funktion `isEmpty` wird ermittelt, ob eine Zeichenfolge leer ist.

**Syntax**

```sql
{%= isEmpty(string) %}
```

**Beispiel**

Die folgende Funktion gibt „true“ zurück, wenn die Mobiltelefonnummer des Profils leer ist. Andernfalls wird „false“ zurückgegeben.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Ist nicht leer {#is-not-empty}

Die Funktion `isNotEmpty` wird verwendet, um zu bestimmen, ob eine Zeichenfolge nicht leer ist.

**Syntax**

```sql
{= isNotEmpty(string) %}: boolean
```

**Beispiel**

Die folgende Funktion gibt „true“ zurück, wenn die Mobiltelefonnummer des Profils nicht leer ist. Andernfalls wird „false“ zurückgegeben.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Letzter Index von {#last-index-of}

Die Funktion `lastIndexOf` wird verwendet, um die Position (im ersten Argument) des letzten Auftretens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

**Syntax**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der im ersten Parameter gesucht werden soll. |

**Beispiel**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Gibt 7 zurück.

## Links kürzen {#leftTrim}

Die Funktion `leftTrim` wird verwendet, um Leerzeichen vom Anfang einer Zeichenfolge zu entfernen.

**Syntax**

```sql
{%= leftTrim(string) %}
```

## Länge {#length}

Die Funktion `length` wird verwendet, um die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck abzurufen.

**Syntax**

```sql
{%= length(string) %}
```

**Beispiel**

Die folgende Funktion gibt die Länge des Stadtnamens des Profils zurück.

```sql
{%= length(profile.homeAddress.city) %}
```

## Ist wie{#like}

Mit der Funktion `like` wird bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht.

**Syntax**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Der Ausdruck, der mit der ersten Zeichenfolge übereinstimmen soll. Es werden zwei Sonderzeichen zum Erstellen eines Ausdrucks unterstützt: `%` und `_`. <ul><li>`%` wird verwendet, um 0 oder mehr Zeichen zu repräsentieren.</li><li>`_` wird verwendet, um genau ein Zeichen zu repräsentieren.</li></ul> |

**Beispiel**

In der folgenden Abfrage werden alle Städte abgerufen, in denen Profile leben und die das Muster „es“ enthalten.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Kleinbuchstaben{#lower}

Mit der Funktion `lowerCase` wird eine Zeichenfolge in Kleinbuchstaben umgewandelt.

**Syntax**

```sql
{%= lowerCase(string) %}
```

**Beispiel**

Mit dieser Funktion wird der Vorname des Profils in Kleinbuchstaben umgewandelt.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Stimmt überein mit{#matches}

Mit der Funktion `matches` wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt. Weitere Informationen zu Übereinstimmungsmustern bei regulären Ausdrücken finden Sie in [diesem Dokument](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

**Syntax**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Beispiel**

Die folgende Abfrage bestimmt, ob der Name der Person ohne Unterscheidung der Groß-/Kleinschreibung mit „John“ beginnt.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Maskieren {#mask}

Die Funktion `Mask` wird verwendet, um einen Teil einer Zeichenfolge durch „X“-Zeichen zu ersetzen.

**Syntax**

```sql
{%= mask(string,integer,integer) %}
```

**Beispiel**

Die folgende Abfrage ersetzt die Zeichenfolge „123456789“ durch „X“, mit Ausnahme des ersten und der letzten beiden Zeichen.

```sql
{%= mask("123456789",1,2) %}
```

Die Abfrage gibt `1XXXXXX89` zurück.

## MD5 {#md5}

Die Funktion `md5` wird verwendet, um den MD5-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

**Syntax**

```sql
{%= md5(string) %}: string
```

**Beispiel**

```sql
{%= md5("hello world") %}
```

Gibt „5eb63bbbe01eeed093cb22bb8f5acdc3“ zurück

## Ungleich{#notEqualTo}

Mit der Funktion `notEqualTo` wird bestimmt, ob eine Zeichenfolge nicht gleich der angegebenen Zeichenfolge ist.

**Syntax**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person nicht „John“ lautet.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Entspricht nicht (Groß-/Kleinschreibung ignorieren) {#not-equal-with-ignore-case}

Die Funktion `notEqualWithIgnoreCase` wird verwendet, um zwei Zeichenfolgen zu vergleichen, wobei Groß-/Kleinschreibung ignoriert wird.

**Syntax**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage ermittelt, ob der Name der Person nicht „john“ lautet (ohne Berücksichtigung von Groß-/Kleinschreibung).

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Gruppe regelmäßiger Ausdrücke{#regexGroup}

Die Funktion `Group` wird verwendet, um spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck zu extrahieren.

**Syntax**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING}` | Die Zeichenfolge, die überprüft werden soll. |
| `{EXPRESSION}` | Der reguläre Ausdruck, der mit der ersten Zeichenfolge übereinstimmen soll. |
| `{GROUP}` | Ausdrucksgruppe, mit der eine Übereinstimmung gefunden werden soll. |

**Beispiel**

Die folgende Abfrage wird verwendet, um den Domain-Namen aus einer E-Mail-Adresse zu extrahieren.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Ersetzen {#replace}

Die Funktion `replace` wird verwendet, um eine bestimmte Unterzeichenfolge in einer Zeichenfolge durch eine andere Unterzeichenfolge zu ersetzen.

**Syntax**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, in der die Teilzeichenfolge ersetzt werden muss. |
| `{STRING_2}` | Die zu ersetzende Teilzeichenfolge. |
| `{STRING_3}` | Die als Ersatz dienende Teilzeichenfolge. |

**Beispiel**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Gibt „Hallo Mark, hier ist dein monatlicher Newsletter!“ zurück.

## Alle ersetzen{#replaceAll}

Die Funktion `replaceAll` wird verwendet, um alle Unterzeichenfolgen eines Textes, die mit dem „Regex“-Ausdruck übereinstimmen, durch die angegebene literale „Ersatz“-Zeichenfolge zu ersetzen. Regex hat eine besondere Handhabung für „\“ und „+“, und alle Regex-Ausdrücke folgen der PQL-Escaping-Strategie. Die Ersetzung erfolgt vom Anfang der Zeichenfolge zum Ende, z. B. führt ein Ersetzen von „aa“ in der Zeichenfolge „aaa“ durch „b“ zu „ba“ und nicht zu „ab“.

**Syntax**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Wenn der als zweites Argument verwendete Ausdruck ein spezielles Regex-Zeichen ist, verwenden Sie einen doppelten umgekehrten Schrägstrich (`//`).  Spezielle Regex-Zeichen sind: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Weitere Informationen finden Sie in der [Oracle-Dokumentation](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Rechts kürzen {#rightTrim}

Mit der Funktion `rightTrim` werden Leerzeichen vom Ende einer Zeichenfolge entfernt.

**Syntax**

```sql
{%= rightTrim(string) %}
```

## Teilen {#split}

Die Funktion `split` wird verwendet, um eine Zeichenfolge durch ein bestimmtes Zeichen zu teilen.

**Syntax**

```sql
{%= split(string,string) %}
```

## Beginnt mit{#startsWith}

Mit der Funktion `startsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt.

**Syntax**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf „true“ gesetzt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person mit „Joe“ beginnt.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Zeichenfolge zu Datum {#string-to-date}

Die Funktion `stringToDate` konvertiert einen Zeichenfolgenwert in einen Datums-/Uhrzeitwert. Es gibt zwei Argumente: Zeichenfolgendarstellung eines Datums/Uhrzeit und Zeichenfolgendarstellung des Formatierers.

**Syntax**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Beispiel**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Zeichenfolge zu Ganzzahl {#string-to-integer}

Die Funktion `string_to_integer` wird verwendet, um einen Zeichenfolgenwert in einen ganzzahligen Wert zu konvertieren.

**Syntax**

```sql
{= string_to_integer(string) %}: int
```

## Zeichenfolge zu Zahl {#string-to-number}

Die Funktion `stringToNumber` wird verwendet, um eine Zeichenfolge in eine Zahl zu konvertieren. Bei einer ungültigen Eingabe wird dieselbe Zeichenfolge als Ausgabe zurückgegeben.

**Syntax**

```sql
{%= stringToNumber(string) %}: double
```

## Teilzeichenfolge {#sub-string}

Die Funktion `Count string` wird verwendet, um die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurückzugeben.
**Syntax**

```sql
{= substr(string, integer, integer) %}: string
```

## Titelschreibweise{#titleCase}

Die Funktion **titleCase** wird verwendet, um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben.

**Syntax**

```sql
{%= titleCase(string) %}
```

**Beispiel**

Wenn die Person in der Washington High Street lebt, gibt diese Funktion „Washington High Street“ zurück.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Zu booleschem Wert {#to-bool}

Die Funktion `toBool` wird verwendet, um einen Argumentwert je nach Typ in einen booleschen Wert zu konvertieren.

**Syntax**

```sql
{= toBool(string) %}: boolean
```

## Zu Uhrzeit-/Datumsangabe {#to-date-time}

Die Funktion `toDateTime` wird verwendet, um die Zeichenfolge in ein Datum zu konvertieren. Bei einer ungültigen Eingabe wird als Ausgabe das Epoch-Datum zurückgegeben.

**Syntax**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Nur zu Datums-/Uhrzeitangabe {#to-date-time-only}

Die Funktion `toDateTimeOnly` wird verwendet, um einen Argumentwert in einen Datums-/Uhrzeitwert zu konvertieren. Bei einer ungültigen Eingabe wird als Ausgabe das Epoch-Datum zurückgegeben. Diese Funktion akzeptiert die Feldtypen string, date, long und int.

**Syntax**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Kürzen {#trim}

Die Funktion **trim** entfernt alle Leerzeichen vom Anfang und Ende einer Zeichenfolge.

**Syntax**

```sql
{%= trim(string) %}
```

## Großbuchstaben{#upper}

Mit der Funktion **upperCase** wird eine Zeichenfolge in Großbuchstaben umgewandelt.

**Syntax**

```sql
{%= upperCase(string) %}
```

**Beispiel**

Mit dieser Funktion wird der Nachname des Profils in Großbuchstaben umgewandelt.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## URL-Decodierung {#url-decode}

Die Funktion `urlDecode` wird zum Decodieren einer URL-codierten Zeichenfolge verwendet.

**Syntax**

```sql
{%= urlDecode(string) %}: string
```

## URL-Codierung {#url-encode}

Die Funktion `Count only null` wird verwendet, um eine Zeichenfolge mit einer URL zu codieren.

**Syntax**

```sql
{%= urlEncode(string) %}: string
```
