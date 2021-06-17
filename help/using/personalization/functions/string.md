---
title: Zeichenfunktionen-Bibliothek
description: Zeichenfunktionen-Bibliothek
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 58%

---

# Zeichenfolgen-Funktionen {#string}

Erfahren Sie, wie Sie im Ausdruckseditor Zeichenfolgen-Funktionen verwenden.

## Camel Case {#camelCase}

Die Funktion `camelCase` großgeschrieben den ersten Buchstaben jedes Wortes einer Zeichenfolge.

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

Die Funktion `concat` kombiniert zwei Zeichenfolgen zu einer.

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

Mit der Funktion `contains` wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält.

**Format**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `STRING_1` | Die Zeichenfolge, die überprüft werden soll. |
| `STRING_2` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiele**

* Die folgende Funktion prüft, ob der Vorname des Profils den Buchstaben A enthält (in Groß- oder Kleinschreibung). Ist dies der Fall, wird &quot;true&quot;zurückgegeben, andernfalls wird &quot;false&quot;zurückgegeben.

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
| `CASE_SENSITIVE` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

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
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

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
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Personenname nicht mit „Joe“ beginnt.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Kodierung 64{#encode64}

Die Funktion `encode64` wird zum Kodieren einer Zeichenfolge verwendet, um personenbezogene Daten (PI) beizubehalten, wenn diese z. B. in eine URL aufgenommen werden sollen.

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
| `{CASE_SENSITIVE}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Mögliche Werte: true (Standard) / false. |

**Beispiel**

In der folgenden Abfrage wird unter Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob die E-Mail-Adresse des Benutzers mit „.com“ endet.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Gleich{#equals}

Mit der Funktion `equals` wird bestimmt, ob eine Zeichenfolge mit Groß-/Kleinschreibung der angegebenen Zeichenfolge entspricht.

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

## Entspricht Groß-/Kleinschreibung ignorieren{#equalsIgnoreCase}

Mit der Funktion `equalsIgnoreCase` wird bestimmt, ob eine Zeichenfolge ohne Groß-/Kleinschreibung mit der angegebenen Zeichenfolge übereinstimmt.

**Format**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage ermittelt ohne Groß-/Kleinschreibung, ob der Name der Person &quot;John&quot; lautet.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## E-Mail-Domäne extrahieren {#extractEmailDomain}

Die Funktion `extractEmailDomain` wird verwendet, um die Domain einer E-Mail-Adresse zu extrahieren.

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Beispiel**

Die folgende Abfrage extrahiert die E-Mail-Domain der persönlichen E-Mail-Adresse.

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

Die folgende Funktion gibt &quot;true&quot;zurück, wenn die Mobiltelefonnummer des Profils leer ist. Andernfalls wird &quot;false&quot;zurückgegeben.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Linker Schnitt {#leftTrim}

Die Funktion `leftTrim` wird verwendet, um Leerzeichen vom Anfang einer Zeichenfolge zu entfernen.

**Format**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

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

Die folgende Abfrage ruft alle Städte ab, in denen Profile leben, die das Muster &quot;es&quot;enthalten.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Kleinbuchstabe{#lower}

Die Funktion `lowerCase` konvertiert eine Zeichenfolge in Kleinbuchstaben.

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

Mit der Funktion `matches` wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt. Weitere Informationen zu Übereinstimmungsmustern bei regulären Ausdrücken finden Sie in [diesem Dokument](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Beispiel**

Die folgende Abfrage bestimmt ohne Groß-/Kleinschreibung, ob der Name der Person mit &quot;John&quot; beginnt.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

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
| `{EXPRESSION}` | Der reguläre Ausdruck, der mit der ersten Zeichenfolge abgeglichen werden soll. |
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

Die folgende Funktion .

```sql

```


## Alle ersetzen{#replaceAll}

Die Funktion `replaceAll` wird verwendet, um alle Unterzeichenfolgen eines Textes zu ersetzen, der mit der &quot;target&quot;-Zeichenfolge mit der angegebenen literalen &quot;replacement&quot;-Zeichenfolge übereinstimmt. Die Ersetzung erfolgt vom Anfang der Zeichenfolge zum Ende, z. B. führt ein Ersetzen von „aa“ in der Zeichenfolge „aaa“ durch „b“ zu „ba“ und nicht zu „ab“.

**Format**

```sql
{%= replaceAll(string,string,string) %}
```


## Rechter Schnitt {#rightTrim}

Die Funktion `rightTrim` entfernt Leerzeichen vom Ende einer Zeichenfolge.


**Format**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

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

Wenn die Person in der Washington High Street lebt, wird diese Funktion die Washington High Street zurückbringen.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Zuschneiden{#trim}

Die Funktion **trim** entfernt alle Leerzeichen vom Anfang und am Ende einer Zeichenfolge.

**Syntax**

```sql
{%= trim(string) %}
```

## Großbuchstaben{#upper}

Die Funktion **upperCase** konvertiert eine Zeichenfolge in Großbuchstaben.

**Syntax**

```sql
{%= upperCase(string) %}
```

**Beispiel**

Diese Funktion konvertiert den Nachnamen des Profils in Großbuchstaben.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
