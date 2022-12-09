---
title: Funktionsbibliothek "Operatoren"
description: Funktionsbibliothek "Operatoren"
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Benutzer {#operators}

## Boolesche Funktionen {#boolean-functions}

Boolesche Funktionen werden verwendet, um eine boolesche Logik für verschiedene Elemente durchzuführen.

### und{#and}

Die `and` -Funktion verwendet wird, um ein logisches Bindewort zu erstellen.

**Format**

```sql
{%= query1 and query2 %}
```

**Beispiel**

Mit der folgenden Operation werden alle Personen zurückgeführt, deren Heimatland Frankreich und Geburtsjahr 1985 sind.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### Oder{#or}

Die `or` -Funktion verwendet wird, um eine logische Trennung zu erstellen.

**Format**

```sql
{%= query1 or query2 %}
```

**Beispiel**

Mit der folgenden Operation werden alle Personen zurückgeführt, deren Heimatland Frankreich oder Geburtsjahr 1985 ist.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## Vergleichsfunktionen {#comparison-functions}

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und &quot;true&quot;oder &quot;false&quot;entsprechend zurückzugeben.

### Gleich{#equals}

Die `=` (gleich) überprüft, ob ein Wert oder Ausdruck mit einem anderen Wert oder Ausdruck übereinstimmt.

**Format**

```sql
{%= expression = value %}
```

**Beispiel**

Mit dem folgenden Vorgang wird geprüft, ob das Land der Wohnadresse Frankreich ist.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Ungleich{#notequal}

Die `!=` Funktion (nicht gleich) überprüft, ob ein Wert oder Ausdruck **not** entspricht einem anderen Wert oder Ausdruck.

**Format**

```sql
{%= expression != value %}
```

**Beispiel**

Der folgende Vorgang prüft, ob das Land der Wohnadresse nicht Frankreich ist.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Größer als{#greaterthan}

Die `>` (greater than) dient zur Überprüfung, ob der erste Wert größer als der zweite Wert ist.

**Format**

```sql
{%= expression1 > expression2 %}
```

**Beispiel**

Die folgende Operation definiert Personen, die nach 1970 geboren wurden.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Größer oder gleich{#greaterthanorequal}

Die `>=` -Funktion (größer oder gleich) wird verwendet, um zu überprüfen, ob der erste Wert größer oder gleich dem zweiten Wert ist.

**Format**

```sql
{%= expression1 >= expression2 %}
```

**Beispiel**

Die folgende Operation definiert Personen, die in oder nach 1970 geboren sind.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Kleiner als{#lessthan}

Die `<` (less than) Mithilfe der Vergleichsfunktion wird geprüft, ob der erste Wert kleiner als der zweite Wert ist.

**Format**

```sql
{%= expression1 < expression2 %}
```

**Beispiel**

Die folgende Operation definiert Personen, die vor 2000 geboren wurden.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Kleiner oder gleich{#lessthanorequal}

Die `<=` (kleiner oder gleich) Mithilfe der Vergleichsfunktion wird geprüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist.

**Format**

```sql
{%= expression1 <= expression2 %}
```

**Beispiel**

Die folgende Operation definiert Personen, die im Jahr 2000 oder früher geboren wurden.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Vorgänge mit Zahlen**
