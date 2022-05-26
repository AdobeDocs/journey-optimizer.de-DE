---
title: Bibliothek mit Zeichenfolgen-Funktionen
description: Bibliothek mit Zeichenfolgen-Funktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: b9ebacf410f268e19bbaf1d43ee98f5376d0913f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 97%

---

# Zeichenfolgen-Funktionen {#string}

Erfahren Sie, wie Sie im Ausdruckseditor Zeichenfolgen-Funktionen verwenden.

## Binnenmajuskel {#camelCase}

Mit der Funktion `camelCase` wird der erste Buchstabe eines jeden Wortes einer Zeichenfolge großgeschrieben.

**Format**

```sql
{%= camelCase(string)%}
```

**Beispiel**

Mit der folgenden Funktion wird der erste Buchstabe der Straßenadresse des Profils großgeschrieben.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Verknüpfen {#concate}

Die Funktion `concat` kombiniert zwei Zeichenfolgen zu einer.

**Format**

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

**Format**

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

**Format**

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

**Format**

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

**Format**

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

**Format**

```sql
{%= encode64(string) %}
```

## Endet mit{#endsWith}

Mit der Funktion `endsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.

**Format**

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

**Format**

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

**Format**

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

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Beispiel**

Mit der folgenden Abfrage wird die E-Mail-Domain der persönlichen E-Mail-Adresse extrahiert.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Ist leer {#isEmpty}

Mit der Funktion `isEmpty` wird bestimmt, ob eine Zeichenfolge leer ist.

**Format**

```sql
{%= isEmpty(string) %}
```

**Beispiel**

Die folgende Funktion gibt „true“ zurück, wenn die Mobiltelefonnummer des Profils leer ist. Andernfalls wird „false“ zurückgegeben.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Links kürzen {#leftTrim}

Die Funktion `leftTrim` wird verwendet, um Leerzeichen vom Anfang einer Zeichenfolge zu entfernen.

**Format**

```sql
{%= leftTrim(string) %}
```

## Länge {#length}

Die Funktion `length` wird verwendet, um die Anzahl der Zeichen in einer Zeichenfolge oder einem Ausdruck abzurufen.

**Format**

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

**Format**

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

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Beispiel**

Die folgende Abfrage bestimmt, ob der Name der Person ohne Unterscheidung der Groß-/Kleinschreibung mit „John“ beginnt.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Maske (#mask)

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

## Ungleich{#notEqualTo}

Mit der Funktion `notEqualTo` wird bestimmt, ob eine Zeichenfolge nicht gleich der angegebenen Zeichenfolge ist.

**Format**

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

## Gruppe regelmäßiger Ausdrücke{#regexGroup}

Die Funktion `Group` wird verwendet, um spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck zu extrahieren.

**Format**

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
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Ersetzen {#replace}

Die Funktion `replace` wird verwendet, um eine bestimmte Unterzeichenfolge in einer Zeichenfolge durch eine andere Unterzeichenfolge zu ersetzen.

**Format**

```sql
{%= replace(string,string,string) %}
```

**Beispiel**

Die folgende Funktion

```sql

```


## Alle ersetzen{#replaceAll}

Die Funktion `replaceAll` wird verwendet, um alle Unterzeichenfolgen eines Textes mit übereinstimmender „Ziel“-Zeichenfolge mit der angegebenen literalen „Ersetzungs“-Zeichenfolge zu ersetzen. Die Ersetzung erfolgt vom Anfang der Zeichenfolge zum Ende, z. B. führt ein Ersetzen von „aa“ in der Zeichenfolge „aaa“ durch „b“ zu „ba“ und nicht zu „ab“.

**Format**

```sql
{%= replaceAll(string,string,string) %}
```


## Rechts kürzen {#rightTrim}

Mit der Funktion `rightTrim` werden Leerzeichen vom Ende einer Zeichenfolge entfernt.


**Format**

```sql
{%= rightTrim(string) %}
```

## Teilen {#split}

Die Funktion `split` wird verwendet, um eine Zeichenfolge durch ein bestimmtes Zeichen zu teilen.

**Format**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Beginnt mit{#startsWith}

Mit der Funktion `startsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge beginnt.

**Format**

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

## Kürzen{#trim}

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
