---
title: Personalization-Rezepte
description: Gängige Personalisierungsmuster und Beispiele aus der Praxis für Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 378c98d4dc9552de3eed68eda59d9917c2b56347
workflow-type: tm+mt
source-wordcount: 845
ht-degree: 0%

---

# Personalization-Rezepte {#personalization-recipes}

>[!BEGINSHADEBOX]

**Auf dieser Seite** finden Sie einsatzbereite Personalisierungsrezepte für Datumsangaben, Arrays, Zeichenfolgen, bedingte Logik und PQL-Edge-Fälle, die Sie direkt in Ihren Adobe Journey Optimizer-Inhalt kopieren können.

>[!ENDSHADEBOX]

Auf dieser Seite finden Sie einsatzbereite Personalisierungsmuster für die häufigsten Anwendungsfälle in Adobe Journey Optimizer. Alle Beispiele verwenden die Syntax des Personalisierungseditors und können direkt in E-Mail-, SMS- oder Push-Inhalte kopiert werden.

Eine vollständige Übersicht der verfügbaren Funktionen finden Sie unter [Hilfsfunktionen](functions/helpers.md), [Datums-/](functions/dates.md), [Zeichenfolgenfunktionen](functions/string.md) und [Array-Funktionen](functions/arrays-list.md).

>[!TIP]
>
>Bevor Sie Beispiele kopieren, lesen Sie die Best Practices für [Personalization](personalization-syntax.md#best-practices) um die häufigsten Syntaxfehler zu vermeiden.

## Rezepte für Datum und Uhrzeit {#date-time-recipes}

### Rezept 1 - Zeigt das aktuelle Datum in einem lesbaren Format an {#recipe-current-date}

Verwenden Sie `formatDate` mit `getCurrentZonedDateTime()`, um das heutige Datum in einem beliebigen Format wiederzugeben:

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

Ausgabe (Beispiel): `April 11, 2026`

**Allgemeine Formatmuster:**

| Muster | Ausgabebeispiel |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>Verwenden Sie `y` in Kleinbuchstaben (Kalenderjahr) anstelle von `Y` (wöchentliches Jahr), um unerwartete Ergebnisse an den Jahresgrenzen zu vermeiden. Siehe [Musterzeichen](functions/dates.md#pattern-characters) für die vollständige Referenz.

### Rezept 2 — Countdown bis zu einem Ablauf- oder Ereignisdatum {#recipe-countdown}

Verwenden Sie `dateDiff`, um die Anzahl der verbleibenden Tage bis zu einem Profildatumsattribut zu berechnen und es dann dynamisch zu rendern:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

Ausgabe (Beispiel): `Your reward points expire in 7 days. Use them before they're gone!`

### Rezept 3 - X Tage vor einem dynamischen Enddatum {#recipe-days-before}

Um ein Datum zu berechnen, das X Tage vor einem Profilattribut liegt (z. B. um in Inhalt oder Betreffzeilen zu referenzieren), verwenden Sie `addDays` mit einem negativen Offset:

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

Ausgabe (Beispiel): `April 04, 2026` *(7 Tage vor dem 11. April)*

Um auch eine feste Tageszeit festzulegen (z. B. 9 Uhr), kombinieren Sie mit `setHours`:

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### Rezept 4 — Aktuelle Zeit nur als HH:MM anzeigen {#recipe-time-only}

Verwenden Sie `extractHours` und `extractMinutes`, um nur den Zeitanteil anzuzeigen, mit einem Schutzmechanismus mit führender Null für Minuten:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Ausgabe (Beispiel): `Your appointment is at 14:05.`

### Rezept 5 - Wochenende vs. Wochentag erkennen {#recipe-weekend}

Verwenden Sie `dayOfWeek` , um Inhalte auf der Grundlage des Tages anzupassen. Die Funktion gibt 1 (Montag) bis 7 (Sonntag) zurück. Verwenden Sie den `=` Operator (PQL-Syntax, nicht `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()` dient der **(**) je nach Tag. Wenn Sie Profile je nach Wochentag auf einer Journey unterschiedlich weiterleiten möchten, verwenden Sie die integrierte Option **Zeitbedingung → Wochentag** in der Aktivität Journey-Bedingung . [Weitere Informationen](../building-journeys/condition-activity.md#date_condition)

## Array- und Schleifenrezepte {#array-recipes}

### Rezept 6 - Listet alle Elemente aus einem Profil-Array auf {#recipe-list-items}

Verwenden Sie `{{#each}}` , um über ein Profil-Array zu iterieren und jedes Element zu rendern. Dies ist nur im Personalisierungseditor (E-Mail, SMS, Push) verfügbar:

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

Ausgabe (Beispiel):

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>`{{#each}}` wird in der Aktivität Journey-Bedingung nicht unterstützt. Verwenden Sie zum Filtern von Arrays in Bedingungen [Sammlungs-Management-Funktionen](../building-journeys/expression/collection-management-functions.md).

### Rezept 7 - Zeigt die Top N Elemente aus einem Array nach Preis {#recipe-first-n}

Verwenden Sie `topN` , um die Top-N-Elemente nach einem numerischen Feld zu sortieren und abzurufen. Da `topN` eine PQL-Funktion ist, weisen Sie sie zuerst mit `{% let %}` einer Variablen zu und dann mit `{{#each}}`:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)` sortiert Bestellungen nach `price` in absteigender Reihenfolge und gibt die drei wichtigsten zurück. Es werden nicht einfach die ersten drei Elemente in der ursprünglichen Array-Reihenfolge zurückgegeben.

Oder verwenden Sie `head`, um nur das oberste Element abzurufen:

```sql
{%= head(profile.purchases.recentItems).name %}
```

### Rezept 8 - Inhalt bedingt pro Array-Element rendern {#recipe-conditional-loop}

Verwenden Sie `{%#if%}` in `{{#each}}`, um die Ausgabe nur für übereinstimmende Elemente zu rendern. Definieren Sie einen Schleifenalias mit `as |order|`, damit der PQL-Auswerter den Attributverweis in der Bedingung auflösen kann:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status` funktioniert in Handlebars-Ausdrücken, wird aber vom PQL-Auswerter in `{%#if%}` nicht aufgelöst. Durch die Verwendung eines benannten Schleifenalias (z. B. `order`) wird das -Attribut sowohl für den Handlebars- als auch für den PQL-Kontext verfügbar.

## Zeichenfolgen- und Formatierungsrezepte {#string-recipes}

### Rezept 9 - Eine Zeichenfolge mit replaceAll reinigen und wiederverwenden {#recipe-replaceall-reuse}

`replaceAll` gibt einen neuen Wert zurück - das Original wird nicht geändert. Verwenden Sie `{% let %}`, um das Ergebnis zu speichern und mehrmals darauf zu verweisen, ohne den Funktionsaufruf zu wiederholen:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

Ausgabe (Beispiel):

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### Rezept 10 - Einen Wert in der JSON-Ausgabe doppelt angeben {#recipe-json-quotes}

Um ein literales doppeltes Anführungszeichen in eine Zeichenfolge einzuschließen (z. B. um JSON für eine benutzerdefinierte Payload zu generieren), Escape-Zeichen mit einem umgekehrten Schrägstrich (`\"`):

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

Ausgabe: `{ "greeting": "Hello \"John\"" }`

### Rezept 11 - Formatieren einer Datumskomponente in Großbuchstaben {#recipe-uppercase-date}

Kombinieren Sie `formatDate` mit `upperCase`, um Monats- oder Tagesnamen in Großbuchstaben zu ändern:

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

Ausgabe (Beispiel): `APRIL`

Für eine vollständige Datumszeichenfolge in Großbuchstaben:

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

Ausgabe (Beispiel): `WEDNESDAY JANUARY 01 2020`

## Bedingte Logik - Rezepte {#conditional-recipes}

### Rezept 12 — IF/ELSEIF/ELSE in personalisierten Inhalten {#recipe-if-elseif}

Verwenden Sie `{%#if%}`, `{%else if%}` und `{%else%}` für eine bedingte Logik mit mehreren Verzweigungen. Dieses Muster funktioniert in E-Mail-Inhalten und -Fragmenten:

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### Rezept 13 — Null-Safe-Attributanzeige {#recipe-null-safe}

Verwenden Sie ein bedingtes Fallback, um zu vermeiden, dass leere Werte gerendert werden, wenn ein Profilattribut null sein kann oder fehlt:

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

Oder inline mit einem Muster im ternären Stil unter Verwendung von `isEmpty`:

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## PQL Edge Case-Rezepte {#pql-edge-cases}

### Rezept 14 - Referenzieren eines mit Bindestrichen versehenen Attributschlüssels {#recipe-hyphenated-key}

Wenn der XDM-Schemafeldname Bindestriche enthält (z. B. `order-total`, `event-type`), schließen Sie ihn in einen PQL-Ausdruck mit Backticks ein, um zu verhindern, dass der Bindestrich als Subtraktionsoperator interpretiert wird:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>Backticks werden nur innerhalb von PQL-Ausdrücken (`{%= ... %}`) unterstützt. Sie werden in der reinen Handlebars-Interpolation (`{{...}}`) nicht akzeptiert. Wenn Sie einen Feldwert mit Bindestrich direkt rendern müssen, werten Sie ihn über einen PQL-Ausdruck aus oder speichern Sie ihn zuerst mit `{% let %}` in einer Variablen.

### Rezept 15 - Referenzieren einer numerischen Ereignis-ID in einem Kontextattribut {#recipe-numeric-event-id}

Wenn Sie ein Journey-Kontextereignis verwenden, dessen ID eine numerische Zeichenfolge ist (z. B. `1697323153`), schließen Sie die ID in Backticks ein und verwenden Sie `{% let %}` mit `toDateTime()` und `formatDate()`:

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

Ausgabe (Beispiel): `Your appointment: 18/03/2026 14:30`

### Rezept 16 - Zwang eingeben: Zeichenfolgenfeld mit einer Zahl vergleichen {#recipe-type-coercion}

PQL ist stark typisiert. Wenn ein Profilfeld als Zeichenfolge gespeichert wird, Sie es jedoch numerisch vergleichen müssen, konvertieren Sie es zuerst mit `stringToNumber()`:

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

Für boolesche Felder, die als Zeichenfolgen gespeichert werden:

```sql
{%= toBool(profile.consents.email.val) = true %}
```

