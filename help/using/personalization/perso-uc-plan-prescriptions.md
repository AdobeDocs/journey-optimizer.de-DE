---
title: Beispiele für die Personalisierung von Vorlagen
description: Beispiele für die Personalisierung von Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 21%

---

# E-Mail mit den Rezepten eines Gesundheitsplans {#plan-prescription}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Führen Sie ein Personalisierungs-Anwendungsbeispiel durch, das verschachtelte Profil-Arrays mit bedingten Regeln durchläuft, um einen Gesundheitsplan für E-Mail-Rezepte zu erstellen, die abholbereit sind oder zurückgerufen werden.

>[!ENDSHADEBOX]

Ein Profil enthält Gesundheitspläne, und jeder Plan enthält Rezepte. Rezepte haben verschiedene Status, z. B. „Bereit“, „Rückruf“ oder„Abgeholt“.

In diesem Anwendungsfall möchten wir jedem Profil eine einzelne E-Mail senden, einschließlich aller verschriebenen Medikamente, die entweder abgeholt werden können oder zurückgerufen wurden. Klicken Sie auf die einzelnen Registerkarten unten, um weitere Informationen zur Syntax zu erhalten, die für die Implementierung dieses Anwendungsfalls verwendet werden soll.

>[!BEGINTABS]

>[!TAB Gerenderte Nachricht]

<p>Hallo Herr Müller,</p>
<p>Im Folgenden finden Sie die Rezepte, die entweder abgeholt werden können oder zurückgerufen wurden:</p>

**Gesundheitsplan A**

<ul>

<li>
      <strong>Verschreibungs-ID:</strong> press1<br>
      <strong>name:</strong> Medikament A<br>
      <strong>state:</strong> ready
   </li>

<li>
      <strong>Verschreibungs-ID:</strong> press2<br>
      <strong>Name:</strong> Medizin B<br>
      <strong>state:</strong> recall
   </li>

</ul>

**Gesundheitsplan B**

<ul>

<li>
      <strong>Rezept-ID:</strong> press4<br>
      <strong>Name:</strong> Medizin-ID<br>
      <strong>state:</strong> ready
   </li>

</ul>

>[!TAB HTML-Vorlage]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Profildaten]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]

## Kurzübersicht {#quick-reference}

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

>[!BEGINTABS]

>[!TAB Übersicht]

**TL;DR**

Auf dieser Seite wird ein vollständiger Anwendungsfall für die Personalisierung veranschaulicht: Durch die Iteration werden verschachtelte Profil-Arrays (Gesundheitspläne mit Verschreibungen) mit bedingter Filterung durchlaufen, sodass in einer E-Mail nur Verschreibungen im Status „bereit“ oder „zurückgerufen“ angezeigt werden.

**Intents**

* Hier finden Sie ein Beispiel für eine gerenderte Ausgabe einer personalisierten E-Mail mit einem Gesundheitsplan
* Grundlegendes zur HTML-Vorlage unter Verwendung verschachtelter `{{#each}}` und `{%#if%}` für die Iteration bedingter Arrays
* Machen Sie sich mit der erforderlichen Profildatenstruktur vertraut: einem `plans`-Array, in dem jeder Plan ein `prescriptions`-Array mit `state` Feldern enthält

>[!TAB Glossar]

* **Verschachtelte Iteration**: Verwenden von `{{#each}}`-Schleifen innerhalb anderer `{{#each}}`-Schleifen zum Durchlaufen von Array-Strukturen mit mehreren Ebenen in Profildaten (z. B. Plänen → Vorschriften).
* **Rezeptstatus**: Ein Feld auf jedem Rezeptobjekt, das in diesem Anwendungsfall seinen Lebenszyklusstatus angibt - die verwendeten Werte sind „bereit“, „zurückrufen“ und „aufgenommen“. *(Anwendungsfall-spezifisch)*
* **`{%#if%}`/`{%/if%}`**: Bedingte Blocksyntax, die in Nachrichtenvorlagen zum Filtern von Array-Elementen während der Iteration verwendet wird (nicht identisch mit der doppelt geschweiften `{{#if}}` Handlebars-Syntax).

>[!TAB Terminologie]

* **Kanonischer Name:** verschachtelte Array-Iteration — Varianten: verschachtelte Schleifen, jede, mehrstufige Iteration
* **Verwechseln Sie nicht:** `{{#each}}` / `{{/each}}` (Handlebars-Iterationssyntax, doppelte geschweifte Klammern) ≠ `{%#if%}` / `{%/if%}` (bedingte Syntax, Prozent-geschweifte Klammern) - beide werden in dieser Vorlage zusammen verwendet
* **Verwechseln Sie nicht:** „bereit“ (Rezept für Abholung verfügbar) ≠ „zurückrufen“ (Rezept wurde zurückgerufen) ≠ „abgeholt“ (Rezept bereits abgeholt - durch den bedingten Filter von der Ausgabe ausgeschlossen)

>[!TAB FAQs]

**F: Welche Rezeptstatus sind in der E-Mail-Ausgabe enthalten?**

Es werden nur Rezepte mit dem Status „bereit“ oder „zurückgerufen“ angezeigt. Rezepte mit Status „aufgenommen“ werden vom `{%#if prescription.state = "ready" or prescription.state = "recall"%}` bedingten Filter ausgeschlossen.

**F: Welche Profildatenstruktur ist für diesen Anwendungsfall erforderlich?**

Ein Profil mit einem `plans` Array, wobei jedes Planobjekt ein `prescriptions` Array enthält. Jedes Rezeptobjekt muss über `prescription_id`-, `name`- und `state` verfügen.

**F: Wie werden Pläne und Rezepte in der Vorlage iteriert?**

Die äußere `{{#each profile.plans as |plan|}}` durchläuft jeden Gesundheitsplan. Darin durchläuft `{{#each plan.prescriptions as |prescription|}}` die Rezepte jedes Plans, und ein bedingter Block filtert nur in den Status „bereit“ oder „zurückzurufen“.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
