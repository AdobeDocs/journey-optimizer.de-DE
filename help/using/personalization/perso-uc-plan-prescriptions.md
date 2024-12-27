---
title: Beispiele für die Personalisierung von Vorlagen
description: Beispiele für die Personalisierung von Journey Optimizer
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: c7ecfdbc9c97c49c77f3c4fb8bcb1656e04819a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 100%

---

# E-Mail mit den Rezepten eines Gesundheitsplans {#plan-prescription}

Ein Profil enthält Gesundheitspläne, und jeder Plan enthält Rezepte. Rezepte haben verschiedene Status, z. B. „Bereit“, „Rückruf“ oder„Abgeholt“.

In diesem Anwendungsfall möchten wir jedem Profil eine einzelne E-Mail senden, einschließlich aller verschriebenen Medikamente, die entweder abgeholt werden können oder zurückgerufen wurden. Klicken Sie auf die einzelnen Registerkarten unten, um weitere Informationen zur Syntax zu erhalten, die für die Implementierung dieses Anwendungsfalls verwendet werden soll.

>[!BEGINTABS]

>[!TAB Gerenderte Nachricht]

<p>Hallo Herr Müller,</p>
<p>Im Folgenden finden Sie die Rezepte, die entweder abgeholt werden können oder zurückgerufen wurden:</p>

**Gesundheitsplan A**

<ul>

<li>
      <strong>Rezept-ID:</strong> pres1<br>
      <strong>Name:</strong> Medikament A<br>
      <strong>Status:</strong> Bereit
   </li>

<li>
      <strong>Rezept-ID:</strong> pres2<br>
      <strong>Name:</strong> Medikament B<br>
      <strong>Status:</strong> Rückruf
   </li>

</ul>

**Gesundheitsplan B**

<ul>

<li>
      <strong>Rezept-ID:</strong> pres4<br>
      <strong>Name:</strong> Medikament D<br>
      <strong>Status:</strong> Breit
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
