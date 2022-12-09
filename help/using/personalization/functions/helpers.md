---
title: Helfer
description: Helfer
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 44e87553b5a001414f28a972ec5c61947decdf55
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Helfer {#gs-helpers}

## Standardwert für Fallback{#default-value}

Die `Default Fallback Value` Helper wird verwendet, um einen standardmäßigen Fallback-Wert zurückzugeben, wenn ein Attribut leer oder null ist. Dieser Mechanismus funktioniert für Profilattribute und Journey-Ereignisse.

**Syntax**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In diesem Beispiel wird der Wert `there` angezeigt wird, wenn die `firstName` -Attribut dieses Profils leer oder null ist.

## Bedingungen{#if-function}

Die `if` dient zur Definition eines bedingten Blocks.
Wenn die Ausdrucksauswertung &quot;true&quot;zurückgibt, wird der Block gerendert, andernfalls wird er übersprungen.

**Syntax**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Im Folgenden `if` Helper, können Sie eine `else` -Anweisung, um einen Codeblock anzugeben, der ausgeführt werden soll, wenn dieselbe Bedingung falsch ist.
Die `elseif` -Anweisung gibt eine neue Bedingung an, um zu testen, ob die erste Anweisung &quot;false&quot;zurückgibt.


**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Beispiele**

1. **Verschiedene Store-Links basierend auf bedingten Ausdrücken rendern**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **E-Mail-Adresserweiterung bestimmen**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Bedingten Link hinzufügen**

   Der folgende Vorgang fügt einen Link zur &quot;www.adobe.com/academia&#39;&quot;-Website für Profile mit &quot;.edu&quot;-E-Mail-Adressen hinzu, zur &quot;www.adobe.com/org&#39;&quot;-Website für Profile mit &quot;.org&quot;-E-Mail-Adressen und zur Standard-URL &quot;www.adobe.com/users&#39;&quot;für alle anderen Profile:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Bedingter Inhalt basierend auf Segmentmitgliedschaft**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Bestimmen, ob ein Profil bereits Mitglied ist**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Weiterführende Informationen zum Segmentierungs- und Segmentierungsdienst finden Sie in diesem Abschnitt [Abschnitt](../../segment/about-segments.md).


## Sofern{#unless}

Die `unless` dient zur Definition eines bedingten Blocks. Durch den Widerstand gegen die `if`  Wenn die Ausdrucksauswertung &quot;false&quot;zurückgibt, wird der Block gerendert.

**Syntax**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Beispiel**

Wiedergabe von Inhalten basierend auf der E-Mail-Adresserweiterung:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Jeder{#each}

Die `each` wird verwendet, um über ein Array zu iterieren.
Die Syntax des Helfers lautet ```{{#each ArrayName}}``` YourContent {{/each}}
Mithilfe des Suchbegriffs können wir auf die einzelnen Array-Elemente verweisen **this** innerhalb des Blocks. Der Index des Elements des Arrays kann mithilfe von {{@index}}.

**Syntax**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Beispiel**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Beispiel**

Rendering a list of products that this user in the cart:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Mit{#with}

Die `with` wird verwendet, um das Bewertungstoken des Vorlagenteils zu ändern.

**Syntax**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Die `with` Helper ist auch bei der Definition einer Verknüpfungsvariablen hilfreich.

**Beispiel**

Verwenden Sie mit , um lange Variablennamen auf kürzere Namen auszurichten:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Lasst{#let}

Die `let` -Funktion kann ein Ausdruck als Variable gespeichert und später in einer Abfrage verwendet werden.

**Syntax**

```sql
{% let variable = expression %} {{variable}}
```

**Beispiel**

Im folgenden Beispiel werden alle Summen der Produktsummen mit der Transaktion in USD angezeigt, wobei die Summe 100 USD und weniger 1000 USD übersteigt.

```sql
{% let variable = expression %} {{variable}}
```
