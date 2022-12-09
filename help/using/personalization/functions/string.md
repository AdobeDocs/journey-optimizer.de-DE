---
title: Zeichenfunktionen-Bibliothek
description: Zeichenfunktionen-Bibliothek
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1d9fc184bb67362aac608e9816fe3afe64eb055c
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 0%

---

# Zeichenfolgen-Funktionen {#string}

Erfahren Sie, wie Sie im Ausdruckseditor Zeichenfolgen-Funktionen verwenden.

## Camel Case {#camelCase}

Die `camelCase` -Funktion Großschreibung des ersten Buchstabens eines jeden Worts einer Zeichenfolge.

**Format**

```sql
{%= camelCase(string)%}
```

**Beispiel**

Mit der folgenden Funktion wird der erste Buchstabe in der Straßenadresse des Profils großgeschrieben.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

Die `concat` -Funktion kombiniert zwei Zeichenfolgen zu einer.

**Format**

```sql
{%= concat(string,string) %}
```

**Beispiel**

Die folgende Funktion kombiniert Profilstadt und -land in einer einzigen Zeichenfolge.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Enthält {#contains}

Die `contains` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält.

**Format**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die geprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiele**

* Die folgende Funktion prüft, ob der Vorname des Profils den Buchstaben A enthält (in Groß- oder Kleinschreibung). Ist dies der Fall, wird &quot;true&quot;zurückgegeben, andernfalls wird &quot;false&quot;zurückgegeben.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge &quot;2010@gm&quot;enthält.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## Enthält nicht{#doesNotContain}

Die `doesNotContain` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge keine angegebene Teilzeichenfolge enthält.

**Format**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die geprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge &quot;2010@gm&quot;nicht enthält.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## endet nicht mit{#doesNotEndWith}

Die `doesNotEndWith` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge nicht mit einer angegebenen Teilzeichenfolge endet.

**Format**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person nicht mit &quot;.com&quot;endet.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Beginnt nicht mit{#doesNotStartWith}

Die `doesNotStartWith` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge nicht mit einer angegebenen Teilzeichenfolge beginnt.

**Format**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob der Name der Person nicht mit &quot;Joe&quot;beginnt.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Kodierung 64{#encode64}

Die `encode64` -Funktion wird zum Kodieren einer Zeichenfolge verwendet, um personenbezogene Daten (PI) beizubehalten, wenn diese z. B. in eine URL aufgenommen werden sollen.

**Format**

```sql
{%= encode64(string) %}
```

## Endet in{#endsWith}

Die `endsWith` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.

**Format**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person mit &quot;.com&quot; endet.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Gleich{#equals}

Die `equals` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge mit der angegebenen Zeichenfolge übereinstimmt, wobei Groß-/Kleinschreibung berücksichtigt wird.

**Format**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die mit der ersten Zeichenfolge verglichen werden soll. |

**Beispiel**

Die folgende Abfrage ermittelt mit Groß-/Kleinschreibung, ob der Name der Person &quot;John&quot; lautet.

```sql
{%=equals(profile.person.name,"John") %}
```

## Entspricht Groß-/Kleinschreibung ignorieren{#equalsIgnoreCase}

Die `equalsIgnoreCase` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge ohne Groß-/Kleinschreibung mit der angegebenen Zeichenfolge übereinstimmt.

**Format**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die mit der ersten Zeichenfolge verglichen werden soll. |

**Beispiel**

Die folgende Abfrage ermittelt ohne Groß-/Kleinschreibung, ob der Name der Person &quot;John&quot; lautet.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## E-Mail-Domäne extrahieren {#extractEmailDomain}

Die `extractEmailDomain` -Funktion wird verwendet, um die Domäne einer E-Mail-Adresse zu extrahieren.

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Beispiel**

Die folgende Abfrage extrahiert die E-Mail-Domain der persönlichen E-Mail-Adresse.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Abrufen des URL-Hosts {#get-url-host}

Die `getUrlHost` -Funktion zum Abrufen des Hostnamens einer URL verwendet.

**Format**

```sql
{%= getUrlHost(string) %}: string
```

**Beispiel**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

Gibt &quot;www.myurl.com&quot;zurück

## URL-Pfad abrufen {#get-url-path}

Die `getUrlPath` -Funktion wird verwendet, um den Pfad nach dem Domänennamen einer URL abzurufen.

**Format**

```sql
{%= getUrlPath(string) %}: string
```

**Beispiel**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

Gibt &quot;/contact.html&quot;zurück

## Abrufen des URL-Protokolls {#get-url-protocol}

Die `getUrlProtocol` -Funktion wird zum Abrufen des Protokolls einer URL verwendet.

**Format**

```sql
{%= getUrlProtocol(string) %}: string
```

**Beispiel**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

Gibt &quot;http&quot;zurück

## Index von {#index-of}

Die `indexOf` -Funktion wird verwendet, um die Position (im ersten Argument) des ersten Vorkommens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

**Format**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die im ersten Parameter durchsucht werden soll |

**Beispiel**

```sql
{%= indexOf("hello world","world" ) %}
```

Gibt 6 zurück.

## Ist leer {#isEmpty}

Die `isEmpty` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge leer ist.

**Format**

```sql
{%= isEmpty(string) %}
```

**Beispiel**

Die folgende Funktion gibt &quot;true&quot;zurück, wenn die Mobiltelefonnummer des Profils leer ist. Andernfalls wird &quot;false&quot;zurückgegeben.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Ist nicht leer {#is-not-empty}

Die `isNotEmpty` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge nicht leer ist.

**Format**

```sql
{= isNotEmpty(string) %}: boolean
```

**Beispiel**

Die folgende Funktion gibt &quot;true&quot;zurück, wenn die Mobiltelefonnummer des Profils nicht leer ist. Andernfalls wird &quot;false&quot;zurückgegeben.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Letzter Index von {#last-index-of}

Die `lastIndexOf` -Funktion wird verwendet, um die Position (im ersten Argument) des letzten Vorkommens des zweiten Parameters zurückzugeben. Gibt -1 zurück, wenn keine Übereinstimmung vorliegt.

**Format**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die im ersten Parameter durchsucht werden soll |

**Beispiel**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Gibt 7 zurück.

## Linker Schnitt {#leftTrim}

Die `leftTrim` -Funktion verwendet wird, um Leerzeichen vom Anfang einer Zeichenfolge zu entfernen.

**Format**

```sql
{%= leftTrim(string) %}
```

## Länge {#length}

Die `length` -Funktion wird verwendet, um die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck abzurufen.

**Format**

```sql
{%= length(string) %}
```

**Beispiel**

Die folgende Funktion gibt die Länge des Stadtnamens des Profils zurück.

```sql
{%= length(profile.homeAddress.city) %}
```

## liken{#like}

Die `like` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt.

**Format**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Der Ausdruck, der mit der ersten Zeichenfolge abgeglichen werden soll. Es werden zwei Sonderzeichen zum Erstellen eines Ausdrucks unterstützt: `%` und `_`. <ul><li>`%` wird verwendet, um null oder mehr Zeichen darzustellen.</li><li>`_` wird verwendet, um genau ein Zeichen darzustellen.</li></ul> |

**Beispiel**

Die folgende Abfrage ruft alle Städte ab, in denen Profile leben, die das Muster &quot;es&quot;enthalten.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Kleinbuchstabe{#lower}

Die `lowerCase` -Funktion konvertiert eine Zeichenfolge in Kleinbuchstaben.

**Syntax**

```sql
{%= lowerCase(string) %}
```

**Beispiel**

Diese Funktion konvertiert den Vornamen des Profils in Kleinbuchstaben.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Stimmt überein mit{#matches}

Die `matches` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt. Siehe [dieses Dokuments](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) für weitere Informationen zum Abgleichen von Mustern in regulären Ausdrücken.

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Beispiel**

Die folgende Abfrage bestimmt ohne Groß-/Kleinschreibung, ob der Name der Person mit &quot;John&quot; beginnt.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Maskieren {#mask}

Die `Mask` -Funktion wird verwendet, um einen Teil einer Zeichenfolge durch &quot;X&quot;-Zeichen zu ersetzen.

**Format**

```sql
{%= mask(string,integer,integer) %}
```

**Beispiel**

Die folgende Abfrage ersetzt die Zeichenfolge &quot;123456789&quot;durch &quot;X&quot;, mit Ausnahme der ersten und der letzten beiden Zeichen.

```sql
{%= mask("123456789",1,2) %}
```

Die Abfrage gibt `1XXXXXX89`.

## MD5 {#md5}

Die `md5` -Funktion wird verwendet, um den md5-Hash einer Zeichenfolge zu berechnen und zurückzugeben.

**Format**

```sql
{%= md5(string) %}: string
```

**Beispiel**

```sql
{%= md5("hello world") %}
```

Gibt &quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;zurück

## Ungleich{#notEqualTo}

Die `notEqualTo` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge nicht mit der angegebenen Zeichenfolge übereinstimmt.

**Format**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die mit der ersten Zeichenfolge verglichen werden soll. |

**Beispiel**

Die folgende Abfrage bestimmt unter Berücksichtigung der Groß-/Kleinschreibung, ob der Name der Person nicht &quot;John&quot; lautet.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Nicht gleich Groß-/Kleinschreibung ignorieren {#not-equal-with-ignore-case}

Die `notEqualWithIgnoreCase` -Funktion verwendet, um zwei Zeichenfolgen zu vergleichen, wobei Groß-/Kleinschreibung ignoriert wird.

**Format**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, die mit der ersten Zeichenfolge verglichen werden soll. |

**Beispiel**

Die folgende Abfrage ermittelt, ob der Name der Person nicht &quot;john&quot;lautet, ohne Groß-/Kleinschreibung.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Gruppe Regulärer Ausdruck{#regexGroup}

Die `Group` -Funktion wird verwendet, um spezifische Informationen basierend auf dem angegebenen regulären Ausdruck zu extrahieren.

**Format**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING}` | Die Zeichenfolge, die geprüft werden soll. |
| `{EXPRESSION}` | Der reguläre Ausdruck, der mit der ersten Zeichenfolge abgeglichen werden soll. |
| `{GROUP}` | Ausdrucksgruppe, mit der eine Übereinstimmung gefunden werden soll. |

**Beispiel**

Mithilfe der folgenden Abfrage wird der Domain-Name aus einer E-Mail-Adresse extrahiert.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Ersetzen {#replace}

Die `replace` -Funktion wird verwendet, um eine angegebene Teilzeichenfolge in einer Zeichenfolge durch eine andere Teilzeichenfolge zu ersetzen.

**Format**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, in der die Teilzeichenfolge ersetzt werden muss. |
| `{STRING_2}` | Die zu ersetzende Unterzeichenfolge. |
| `{STRING_3}` | Die Ersatz-Teilzeichenfolge. |

**Beispiel**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Gibt &quot;Hallo Mark, hier ist Ihr monatlicher Newsletter!&quot; zurück.

## Alle ersetzen{#replaceAll}

Die `replaceAll` -Funktion wird verwendet, um alle Teilzeichenfolgen eines Textes zu ersetzen, der mit der &quot;Ziel&quot;-Zeichenfolge mit der angegebenen literalen &quot;Ersatz&quot;-Zeichenfolge übereinstimmt. Die Ersetzung erfolgt vom Anfang der Zeichenfolge bis zum Ende, z. B. führt das Ersetzen von &quot;aa&quot;durch &quot;b&quot;in der Zeichenfolge &quot;aaa&quot;zu &quot;ba&quot;anstelle von &quot;ab&quot;.

**Format**

```sql
{%= replaceAll(string,string,string) %}
```

## Rechter Schnitt {#rightTrim}

Die `rightTrim` -Funktion verwendet wird, entfernt Leerzeichen vom Ende einer Zeichenfolge.

**Format**

```sql
{%= rightTrim(string) %}
```

## Aufspaltung {#split}

Die `split` -Funktion verwendet wird, um eine Zeichenfolge durch ein bestimmtes Zeichen zu teilen.

**Format**

```sql
{%= split(string,string) %}
```

## Beginnt mit{#startsWith}

Die `startsWith` -Funktion wird verwendet, um zu bestimmen, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt.

**Format**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die geprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, der bestimmt, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf &quot;true&quot;gesetzt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Berücksichtigung der Groß-/Kleinschreibung, ob der Name der Person mit &quot;Joe&quot;beginnt.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Zeichenfolge in Ganzzahl {#string-to-integer}

Die `string_to_integer` -Funktion wird verwendet, um einen Zeichenfolgenwert in einen ganzzahligen Wert zu konvertieren.

**Format**

```sql
{= string_to_integer(string) %}: int
```

## Zeichenfolge zu Zahl {#string-to-number}

Die `stringToNumber` -Funktion verwendet wird, um eine Zeichenfolge in eine Zahl zu konvertieren. Es wird dieselbe Zeichenfolge wie für eine ungültige Eingabe zurückgegeben.

**Format**

```sql
{%= stringToNumber(string) %}: double
```

## Unterzeichenfolge {#sub-string}

Die `Count string` -Funktion wird verwendet, um die Unterzeichenfolge des Zeichenfolgenausdrucks zwischen dem Anfangsindex und dem Endindex zurückzugeben.
**Format**

```sql
{= substr(string, integer, integer) %}: string
```

## Titelschreibweise{#titleCase}

Die **titleCase** -Funktion wird verwendet, um die ersten Buchstaben jedes Wortes einer Zeichenfolge großzuschreiben.

**Syntax**

```sql
{%= titleCase(string) %}
```

**Beispiel**

Wenn die Person in der Washington High Street lebt, wird diese Funktion die Washington High Street zurückbringen.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Nach Bool {#to-bool}

Die `toBool` -Funktion wird verwendet, um einen Argumentwert je nach Typ in einen booleschen Wert zu konvertieren.

**Format**

```sql
{= toBool(string) %}: boolean
```

## To Date Time {#to-date-time}

Die `toDateTime` -Funktion verwendet wird, um die Zeichenfolge in das Datum zu konvertieren. Es wird das Epochendatum als Ausgabe für ungültige Eingabe zurückgegeben.

**Format**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Nur für Datum/Uhrzeit {#to-date-time-only}

Die `toDateTimeOnly` -Funktion wird verwendet, um einen Argumentwert in einen Datum/Uhrzeit-Wert zu konvertieren. Es wird das Epochendatum als Ausgabe für ungültige Eingabe zurückgegeben.

**Format**

```sql
{%= toDateTimeOnly(string) %}: date-time
```

## Zuschneiden{#trim}

Die **trim** entfernt alle Leerzeichen am Anfang und am Ende einer Zeichenfolge.

**Syntax**

```sql
{%= trim(string) %}
```

## Großbuchstaben{#upper}

Die **upperCase** -Funktion konvertiert einen String in Großbuchstaben.

**Syntax**

```sql
{%= upperCase(string) %}
```

**Beispiel**

Diese Funktion konvertiert den Nachnamen des Profils in Großbuchstaben.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## url decode {#url-decode}

Die `urlDecode` -Funktion wird zum Dekodieren einer URL-codierten Zeichenfolge verwendet.

**Format**

```sql
{%= urlDecode(string) %}: string
```

## URL-Kodierung {#url-encode}

Die `Count only null` -Funktion verwendet wird, um eine Zeichenfolge mit einer URL zu kodieren.

**Format**

```sql
{%= urlEncode(string) %}: string
```
