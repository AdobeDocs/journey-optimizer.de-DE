---
title: Personalisierungsüberprüfung
description: Weitere Informationen zur Validierung der Personalisierung und zur Fehlerbehebung
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Personalisierungsüberprüfung {#personalization-validation}

![](../assets/do-not-localize/badge.png)

## Überprüfungsmechanismen

Im Anzeigebereich &quot;Ausdruck-Editor&quot;können Sie mit der Schaltfläche **Bestätigen** Ihre Personalisierungssyntax überprüfen.

>[!NOTE]
> Die Überprüfung wird automatisch durchgeführt, wenn Sie auf **Hinzufügen** klicken, um das Editor-Fenster zu schließen.


![](assets/perso_validation1.png)

>[!IMPORTANT]
> Wenn die Personalisierungssyntax ungültig ist, können Sie das Fenster des Ausdruck-Editors nicht schließen.


## Häufige Fehler

* **Pfad &quot;XYZ&quot;nicht gefunden**

Beim Versuch, auf ein Feld zu verweisen, das nicht im Schema definiert ist.

In diesem Fall ist **firstName1** nicht als Attribut im Profil-Schema definiert:

```
{{profile.person.name.firstName1}}
```

* **Type mismatch for variable &quot;XYZ&quot;. Erwartetes Array. Zeichenfolge gefunden.**

Beim Versuch, eine Zeichenfolge anstelle eines Arrays zu iterieren, gilt Folgendes:

In diesem Fall ist **product** kein Array:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Ungültige Handlebars-Syntax.`‘[XYZ}}’`** gefunden

Wenn eine ungültige Handlebars-Syntax verwendet wird.

Handlebars-Ausdruck sind von **{{Ausdruck}}** umgeben

```
   {{[profile.person.name.firstName}}
```

* **Ungültige Segmentdefinition**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### Spezifische Fehler bei Angeboten

Die Fehler bei der Integration von Angeboten in eine E-Mail- oder Push-Nachricht haben das folgende Muster:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

Die Überprüfung wird während der Nachrichtenveröffentlichung oder während der Überprüfung des Personalisierungsinhalts im Ausdruck-Editor durchgeführt.

<table> 
 <thead> 
  <tr> 
   <th> Fehlertitel<br /> </th> 
   <th> Validierung/Auflösung <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Ressource mit id placementID und Typ OfferPlacement nicht gefunden <br/>
Ressource mit id activityID und Typ OfferActivity nicht gefunden<br/></td> 
   <td>Überprüfen, ob ActivityID und/oder Platzierungs-ID verfügbar sind</td> 
  </tr> 
   <tr> 
   <td>Ressource konnte nicht validiert werden.</td> 
   <td>Der componentType in der Platzierung sollte mit dem offerType-Angebot übereinstimmen.</td> 
  </tr> 
   <tr> 
   <td>Die öffentliche URL ist in Angebot offerId nicht vorhanden.</td> 
   <td>Für die Image-Angebot (alle personalisierten und Fallback, die mit dem Decision- und Placement-Paar verknüpft sind) sollte eine öffentliche URL gefüllt sein (deliveryURL sollte nicht leer sein).</td> 
  </tr> 
  <tr> 
   <td>Die Entscheidung (früher als Angebot-Aktivität bezeichnet) enthält Nicht-Profil-Attribute.</td> 
   <td>Angebote Die Modellverwendung sollte nur die Profil-Attribute enthalten.</td> 
  </tr> 
  <tr> 
   <td>Beim Abrufen der Entscheidungsverwendung ist ein Fehler aufgetreten.</td> 
   <td>Dieser Fehler kann auftreten, wenn die API versucht, das Angebot-Modell abzurufen.</td> 
  </tr>
  <tr> 
   <td>Angebot Attribute Angebot-Attribut ist ungültig.</td> 
   <td>Überprüfen Sie, ob das Angebot-Attribut, auf das in der Angebot-Dropdown-Liste verwiesen wird, gültig ist. Folgende Attribute sind gültig: <br/>
Bild: deliveryURL, linkURL<br/>
Text: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>

