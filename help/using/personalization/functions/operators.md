---
title: Bibliothek mit Operatorfunktionen
description: Bibliothek mit Operatorfunktionen
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 100%

---

# Operatoren {#operators}

## Boolesche Funktionen {#boolean-functions}

Boolesche Funktionen werden verwendet, um eine boolesche Logik auf verschiedene Elemente anzuwenden.

### Und{#and}

Die Funktion `and` wird zur Erstellung einer logischen Verknüpfung verwendet.

**Format**

```sql
{%= query1 and query2 %}
```

**Beispiel**

Durch den folgenden Vorgang werden alle Personen mit Wohnsitz in Frankreich und dem Geburtsjahr 1985 zurückgegeben.

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

Durch den folgenden Vorgang werden alle Personen mit Wohnsitz in Frankreich oder dem Geburtsjahr 1985 zurückgegeben.

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

Vergleichsfunktionen werden verwendet, um zwischen verschiedenen Ausdrücken und Werten zu vergleichen und entsprechend „true“ oder „false“ zurückzugeben.

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

Mit dem folgenden Vorgang wird geprüft, ob das Land der Wohnadresse nicht Frankreich ist.

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

Mit dem folgenden Vorgang werden Personen definiert, die nach 1970 geboren wurden.

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

Mit dem folgenden Vorgang werden Personen definiert, die im Jahr 1970 oder danach geboren wurden.

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

Mit dem folgenden Vorgang werden Personen definiert, die vor 2000 geboren wurden.

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

Mit dem folgenden Vorgang werden Personen definiert, die im Jahr 2000 oder früher geboren wurden.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Vorgänge mit Zahlen**
