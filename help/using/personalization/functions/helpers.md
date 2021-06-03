---
title: Helpers
description: Funktionsbibliothek
source-git-commit: 7e20bef085d0fa6983f9ebd84f8cbc3bee2f4542
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 66%

---


# Helpers {#gs-helpers}

![](../../assets/do-not-localize/badge.png)


## Bedingungen{#if-function}

Der Helper `if` wird zum Definieren eines bedingten Blocks verwendet.
Wenn die Auswertung des Ausdrucks „true“ zurückgibt, wird der Block dargestellt, andernfalls wird er übersprungen.

**Syntax**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Nach dem Helper `if` können Sie eine `else`-Anweisung einfügen, um einen Code-Block auszuführen, wenn die Auswertung  „false“ zurückgibt.
Die `elseif`-Anweisung gibt eine weitere Bedingung an, die geprüft wird, wenn die erste Anweisung „false“ zurückgibt.


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

1. **Rendern verschiedener Produkt-Links basierend auf bedingten Ausdrücken**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Bestimmen einer E-Mail-Adressenerweiterung**

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

1. **Prüfen Sie, ob ein Profil bereits Mitglied ist**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Weitere Informationen zur Segmentierung und und zum Segmentierungsdienst finden Sie in diesem [Abschnitt](../../segment/about-segments.md).


## Unless{#unless}

Der Helper `unless` wird zum Definieren eines bedingten Blocks verwendet. Im Gegensatz zum Helper `if` wird der Block gerendert, wenn die Ausdrucksauswertung &quot;false&quot;zurückgibt.

**Syntax**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Beispiel**

Darstellung von Content je nach E-Mail-Adressenerweiterung:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Each{#each}

Der Helfer `each` wird verwendet, um die Elemente eines Arrays zu verarbeiten.
Die Syntax des Helfers ist ```{{#each ArrayName}}``` IhrContent {{/each}}
Die einzelnen Array-Elemente werden durch die Verwendung des Keywords **this** innerhalb des Blocks referenziert. Der Index des jeweiligen Array-Elements kann mithilfe von {{@index}} abgerufen werden.

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

So wird eine Liste von Produkten dargestellt, die dieser Benutzer in den Warenkorb gelegt hat:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## With{#with}

Der `with`-Helfer wird verwendet, um das Bewertungstoken des Vorlagenteils zu ändern.

**Syntax**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Der `with`-Helfer ist nützlich, um auch eine Kurzbefehl-Variable zu definieren.

**Beispiel**

Verwenden Sie with zur Definition eines kurzen Aliasnamens für einen langen Variablennamen:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

Die `let`-Funktion ermöglicht das Speichern eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann.

**Syntax**

```sql
{% let variable = expression %} {{variable}}
```

**Beispiel**

Im folgenden Beispiel werden alle Summen der Produktsummen mit der Transaktion in USD angezeigt, wobei die Summe 100 USD und weniger 1000 USD übersteigt.

```sql
{% let variable = expression %} {{variable}}
```
