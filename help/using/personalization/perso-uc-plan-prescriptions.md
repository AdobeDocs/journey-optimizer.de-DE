---
title: Beispiele für Vorlagen-Personalization
description: Beispiele für Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: f1d6c293fb8b22085911ab45c18f944a63b9655b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# E-Mail zur Verschreibungen von Gesundheitsplänen {#plan-prescription}

Ein Profil enthält Gesundheitspläne, und jeder Plan enthält Verschreibungen. Verschreibungen haben verschiedene Status, z. B. &quot;bereit&quot;, &quot;Rückruf&quot;oder &quot;aufgenommen&quot;.

In diesem Anwendungsfall möchten wir jedem Profil eine einzelne E-Mail senden, einschließlich aller Rezepte, die entweder abgeholt oder zurückgerufen werden können. Klicken Sie auf die einzelnen Registerkarten unten, um weitere Informationen zur Syntax zu erhalten, die für die Implementierung dieses Anwendungsfalls verwendet werden soll.

>[!BEGINTABS]

>[!TAB Rendered Message]

<p>Hallo John Doe,</p>
<p>Im Folgenden finden Sie die Verschreibungen, die entweder abgeholt werden können oder zurückgerufen wurden:</p>

**Health Plan A**

<ul>

<li>
      <strong>Rezept-ID:</strong> pres1<br>
      <strong>Name:</strong> Mediation A<br>
      <strong>Status:</strong> ready
   </li>

<li>
      <strong>Rezept-ID:</strong> pres2<br>
      <strong>Name:</strong> Mediation B<br>
      <strong>state:</strong> recall
   </li>

</ul>

**Health Plan B**

<ul>

<li>
      <strong>Rezept-ID:</strong> pres4<br>
      <strong>Name:</strong> medication d<br>
      <strong>Status:</strong> ready
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
