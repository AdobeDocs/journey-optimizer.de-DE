---
title: Helper
description: Helper
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: b495462aed9a67ff25c2563288bb2ca57e9b7db7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 100%

---

# Helper {#gs-helpers}

## Standardwert für Fallback{#default-value}

Der Helper `Default Fallback Value` wird verwendet, um einen standardmäßigen Fallback-Wert zurückzugeben, wenn ein Attribut leer oder null ist. Dieser Mechanismus funktioniert für Profilattribute und Journey-Ereignisse.

**Syntax**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In diesem Beispiel wird der Wert `there` angezeigt, wenn das Attribut `firstName` dieses Profils leer oder null ist.

## Bedingungen{#if-function}

Der Helper `if` wird zum Definieren eines bedingten Blocks verwendet.
Wenn die Auswertung des Ausdrucks „true“ zurückgibt, wird der Block dargestellt, andernfalls wird er übersprungen.

**Syntax**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Nach dem Helper `if` können Sie eine `else`-Anweisung einfügen, um einen Code-Block auszuführen, wenn die Auswertung „false“ zurückgibt.
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
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
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

   Der folgende Vorgang fügt einen Link zur Website „www.adobe.com/academia“ für Profile mit „.edu“-E-Mail-Adressen hinzu, zur Website „www.adobe.com/org“ für Profile mit „.org“-E-Mail-Adressen und zur Standard-URL „www.adobe.com/users“ für alle anderen Profile:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Bedingte Inhalte basierend auf Zielgruppenzugehörigkeit**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Weitere Informationen zu Zielgruppen und zum Segmentierungs-Service finden Sie in diesem [Abschnitt](../../audience/about-audiences.md).


## Außer{#unless}

Der Helper `unless` wird zum Definieren eines bedingten Blocks verwendet. Im Gegensatz zur Hilfsfunktion `if` wird der Block gerendert, wenn die Auswertung des Ausdrucks „falsch“ zurückgibt.

**Syntax**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Beispiel**

Darstellung von Inhalt je nach E-Mail-Adressenerweiterung:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

## Jeweils{#each}

Der Helper `each` wird verwendet, um die Elemente eines Arrays zu verarbeiten.
Die Syntax des Helpers ist ```{{#each ArrayName}}``` YourContent `{{/each}}`
Die einzelnen Array-Elemente werden durch die Verwendung des Keywords **this** innerhalb des Blocks referenziert. Der Index des Array-Elements kann mithilfe von `{{@index}}` gerendert werden.

**Syntax**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
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
{{/each}}
```

>[!NOTE]
>
>Sie können auch den `each`-Helper verwenden, um die von benutzerdefinierten Aktionsantworten zurückgegebenen Arrays zu durchlaufen. Ein Beispiel für die Iteration über verschachtelte Arrays aus einer benutzerdefinierten Aktionsantwort finden Sie unter [Verwenden von benutzerdefinierten Aktionsantworten in nativen Kanälen](../../action/action-response.md#response-in-channels).

## Mit{#with}

Der Helper `with` wird verwendet, um das Auswertungs-Token des Vorlagenteils zu ändern.

**Syntax**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Der Helper `with` ist auch nützlich, um die Kurzform einer Variable zu definieren.

**Beispiel**

Verwenden Sie „with“ zur Definition eines kurzen Aliasnamens für einen langen Variablennamen:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Zulassen{#let}

Die `let`-Funktion ermöglicht das Speichern eines Ausdrucks als Variable, die später in einer Abfrage verwendet werden kann.

**Syntax**

```sql
{% let variable = expression %} {{variable}}
```

**Beispiel**

Im folgenden Beispiel können Sie die Gesamtsumme der Preise für Produkte im Warenkorb mit Preisen zwischen 100 und 1000 berechnen.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## Ausführungsmetadaten {#execution-metadata}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Die Hilfsfunktion `executionMetadata` ermöglicht die dynamische Erfassung und Speicherung benutzerdefinierter Schlüssel-Wert-Paare im Ausführungskontext der Nachricht.

**Syntax**

```
{{executionMetadata key="your_key" value="your_value"}}
```

In dieser Syntax bezieht sich `key` auf den Metadatennamen und `value` sind die beizubehaltenden Metadaten.

**Anwendungsfall**

Mit dieser Funktion können Sie kontextuelle Informationen an beliebige native Aktionen Ihrer Kampagnen oder Journeys anhängen. Dadurch können Sie kontextuelle Versanddaten in Echtzeit für verschiedene Zwecke wie Tracking, Analyse, Personalisierung und nachgelagerte Verarbeitung in externe Systeme exportieren.

>[!NOTE]
>
>Die Funktion „Ausführungsmetadaten“ wird von [benutzerdefinierten Aktionen](../../action/action.md) nicht unterstützt.

Sie können beispielsweise die Hilfsfunktion „Ausführungsmetadaten“ verwenden, um eine bestimmte ID an jeden Versand anzuhängen, der an jedes Profil gesendet wird. Diese Informationen werden zur Laufzeit generiert und die angereicherten Ausführungsmetadaten können dann zur nachgelagerten Abstimmung mit einer externen Reporting-Plattform exportiert werden.

**Funktionsweise**

Wählen Sie in einer Kampagne oder Journey ein beliebiges Element aus Ihrem Kanalinhalt aus und fügen Sie mithilfe des Personalisierungseditors diesem Element die Hilfsfunktion `executionMetadata` hinzu.

>[!NOTE]
>
>Die Funktion „Ausführungsmetadaten“ ist nicht sichtbar, wenn der Inhalt selbst angezeigt wird.


Zur Laufzeit wird der Metadatenwert dem vorhandenen **[!UICONTROL Nachrichten-Feedback-Ereignisdatensatz]** hinzugefügt, wobei das folgende Schema hinzugefügt wird:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>In [diesem Abschnitt](../../data/get-started-datasets.md) erfahren Sie mehr über Datensätze.

**Einschränkung**

Die Obergrenze für Schlüssel-Wert-Paare pro Aktion ist 2 KB.

Wenn die Grenze von 2 KB überschritten wird, wird die Nachricht weiterhin zugestellt, aber jedes der Schlüssel-Wert-Paare kann abgeschnitten werden.

**Beispiel**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In diesem Beispiel ist unter der Annahme `profile.person.name.firstName` = „Alex“ die resultierende Entität:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

