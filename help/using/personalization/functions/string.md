---
title: Funktionsbibliothek
description: Funktionsbibliothek
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 7%

---

# Zeichenfolgen-Funktionen {#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM-Zeichenfolgen-Funktionen

## Ist wie{#like}

Mit der Funktion `like` wird bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht.

**Format**

```sql
like ({STRING_1},{STRING_2})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Der Ausdruck, der mit der ersten Zeichenfolge übereinstimmen soll. Es werden zwei Sonderzeichen zum Erstellen eines Ausdrucks unterstützt: `%` und `_`. <ul><li>`%` wird verwendet, um 0 oder mehr Zeichen zu repräsentieren.</li><li>`_` wird verwendet, um genau ein Zeichen zu repräsentieren.</li></ul> |

**Beispiel**

In der folgenden Abfrage werden alle Städte mit dem Muster &quot;es&quot;abgerufen.

```sql
like (city ,"%es%")
```

## Beginnt mit{#startsWith}

Mit der Funktion `startsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge Beginn.

**Format**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person mit &quot;Joe&quot;Beginn.

```sql
startsWith(person.name,"Joe")
```

## Beginnt nicht mit{#doesNotStartWith}

Mit der Funktion `doesNotStartWith` wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge Beginn.

**Format**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Personenname nicht mit &quot;Joe&quot;Beginn.

```sql
doesNotStartWith(person.name,"Joe")
```

## Endet mit{#endsWith}

Mit der Funktion `endsWith` wird bestimmt, ob eine Zeichenfolge mit einer angegebenen Unterzeichenfolge endet.

**Format**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

In der folgenden Abfrage wird unter Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob die E-Mail-Adresse des Benutzers mit &quot;.com&quot;endet.

```sql
endsWith(person.emailAddress,".com")
```

## Endet nicht mit{#doesNotEndWith}

Mit der Funktion `doesNotEndWith` wird bestimmt, ob eine Zeichenfolge nicht mit einer angegebenen Unterzeichenfolge endet.

**Format**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person nicht mit &quot;.com&quot;endet.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Enthält{#contains}

Mit der Funktion `contains` wird bestimmt, ob eine Zeichenfolge eine angegebene Unterzeichenfolge enthält.

**Format**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt unter Berücksichtigung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge &quot;2010@gm&quot;enthält.

```sql
contains(person.emailAddress,"2010@gm")
```

## Enthält nicht{#doesNotContain}

Mit der Funktion `doesNotContain` wird bestimmt, ob eine Zeichenfolge keine angegebene Unterzeichenfolge enthält.

**Format**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die Zeichenfolge, nach der in der ersten Zeichenfolge gesucht werden soll. |
| `{BOOLEAN}` | Ein optionaler Parameter, mit dem bestimmt wird, ob bei der Prüfung die Groß-/Kleinschreibung beachtet wird. Standardmäßig ist dies auf true festgelegt. |

**Beispiel**

Die folgende Abfrage bestimmt unter Berücksichtigung der Groß-/Kleinschreibung, ob die E-Mail-Adresse der Person die Zeichenfolge &quot;2010@gm&quot;nicht enthält.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Gleich{#equals}

Mit der Funktion `equals` wird bestimmt, ob eine Zeichenfolge mit der angegebenen Zeichenfolge übereinstimmt.

**Format**

```sql
equals({STRING_1},{STRING_2})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Mit der folgenden Abfrage wird unter Berücksichtigung der Groß-/Kleinschreibung bestimmt, ob der Name der Person &quot;John&quot;lautet.

```sql
equals(person.name,"John")
```

## Ungleich{#notEqualTo}

Mit der Funktion `notEqualTo` wird bestimmt, ob eine Zeichenfolge nicht mit der angegebenen Zeichenfolge übereinstimmt.

**Format**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argument | Beschreibung |
| --------- | ----------- |
| `{STRING_1}` | Die Zeichenfolge, die überprüft werden soll. |
| `{STRING_2}` | Die mit der ersten Zeichenfolge zu vergleichende Zeichenfolge. |

**Beispiel**

Die folgende Abfrage bestimmt bei Beachtung der Groß-/Kleinschreibung, ob der Name der Person nicht &quot;John&quot;lautet.

```sql
notEqualTo(person.name,"John")
```

## Übereinstimmungen{#matches}

Mit der Funktion `matches` wird bestimmt, ob eine Zeichenfolge mit einem bestimmten regulären Ausdruck übereinstimmt. Weitere Informationen zu Übereinstimmungsmustern in regulären Ausdrücken finden Sie in [diesem Dokument](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

**Format**

```sql
matches({STRING_1},STRING_2})
```

**Beispiel**

Die folgende Abfrage bestimmt, ob der Name der Person ohne Unterscheidung der Groß-/Kleinschreibung mit &quot;John&quot;Beginn.

```sql
matches(person.name.,"(?i)^John")
```

## Gruppe regulärer Ausdruck{#regexGroup}

Die Funktion `regexGroup` wird verwendet, um spezifische Informationen basierend auf dem bereitgestellten regulären Ausdruck zu extrahieren.

**Format**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Beispiel**

Die folgende Abfrage wird verwendet, um den Domänennamen aus einer E-Mail-Adresse zu extrahieren.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
