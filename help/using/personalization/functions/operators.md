---
title: Funktionsbibliothek "Operatoren"
description: Funktionsbibliothek "Operatoren"
feature: Personalisierung
topic: Personalisierung
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 59%

---

# Operatoren {#operators}

## Boolesche Funktionen

Boolesche Funktionen werden verwendet, um eine boolesche Logik für verschiedene Elemente durchzuführen.

### Und{#and}

Die Funktion `and` wird zur Erstellung einer logischen Verknüpfung verwendet.

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

Die Funktion `or` wird verwendet, um eine logische Trennung zu erstellen.

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





## Vergleichsfunktionen

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und &quot;true&quot;oder &quot;false&quot;entsprechend zurückzugeben.

### Gleich{#equals}

Die Funktion `=` (gleich) prüft, ob ein Wert oder Ausdruck gleich einem anderen Wert oder Ausdruck ist.

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

Die Funktion `!=` (ungleich) prüft, ob ein Wert oder Ausdruck **ungleich** einem anderen Wert oder Ausdruck ist.

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

Mit der Funktion `>` (größer als) wird überprüft, ob der erste Wert größer als der zweite ist.

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

Mit der Funktion `>=` (größer oder gleich) wird überprüft, ob der erste Wert größer oder gleich dem zweiten Wert ist.

**Format**

```sql
{%= expression1 >= expression2 %}
```

**Beispiel**

Die folgende Operation definiert Personen, die im Jahr 1970 oder danach geboren wurden.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Kleiner als{#lessthan}

Mit der Vergleichsfunktion `<` (kleiner als) wird geprüft, ob der erste Wert kleiner als der zweite ist.

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

Mit der Vergleichsfunktion `<=` (kleiner oder gleich) wird geprüft, ob der erste Wert kleiner oder gleich dem zweiten Wert ist.

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

