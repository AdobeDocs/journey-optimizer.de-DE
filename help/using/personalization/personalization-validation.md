---
solution: Journey Optimizer
product: journey optimizer
title: Personalisierungsvalidierung
description: Erfahren Sie mehr über die Validierung der Personalisierung und die Fehlerbehebung.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Personalisierungsvalidierung {#personalization-validation}

## Validierungsmechanismen {#validation-mechanisms}

Im **Ausdruckseditor** -Bildschirm verwenden, verwenden Sie die **Bestätigen** -Schaltfläche, um die Syntax Ihrer Personalisierung zu überprüfen.

>[!NOTE]
> Die Validierung wird automatisch ausgeführt, wenn Sie auf die **Hinzufügen** -Schaltfläche, um das Editor-Fenster zu schließen.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Wenn die Personalisierungssyntax ungültig ist, können Sie das Ausdruckseditor-Fenster nicht schließen.

## Häufige Fehler {#common-errors}

* **Pfad &quot;XYZ&quot;nicht gefunden**

Beim Versuch, auf ein Feld zu verweisen, das nicht im Schema definiert ist.

In diesem Fall **firstName1** nicht als Attribut im Profilschema definiert ist:

```
{{profile.person.name.firstName1}}
```

* **Geben Sie für die Variable &quot;XYZ&quot;einen Fehler ein. Erwartetes Array. Zeichenfolge gefunden.**

Beim Versuch, über eine Zeichenfolge anstelle eines Arrays zu iterieren:

In diesem Fall **product** ist kein Array:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Ungültige Handlebars-Syntax. Found`‘[XYZ}}’`**

Wenn eine ungültige Handlebars-Syntax verwendet wird.

Handlebars-Ausdrücke sind von **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Ungültige Segmentdefinition**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Spezifische Fehler bei Angeboten {#specific-errors}

Die Fehler im Zusammenhang mit der Angebotsintegration in einer E-Mail- oder Push-Nachricht haben das folgende Muster:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

Die Validierung erfolgt während der Validierung des Personalisierungsinhalts im Ausdruckseditor.

<table> 
 <thead> 
  <tr> 
   <th> Fehler-Titel<br /> </th> 
   <th> Validierung/Auflösung <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Ressource mit id placementID und Typ OfferPlacement nicht gefunden <br/>
Ressource mit ID activityID und Typ OfferActivity nicht gefunden<br/></td> 
   <td>Überprüfen, ob ActivityID und/oder PlacementID verfügbar sind</td> 
  </tr> 
   <tr> 
   <td>Die Ressource konnte nicht validiert werden.</td> 
   <td>Der Komponententyp in der Platzierung sollte mit dem Angebot offerType übereinstimmen</td> 
  </tr> 
   <tr> 
   <td>Die öffentliche URL ist in offerId nicht vorhanden.</td> 
   <td>Für Bildangebote (alle personalisierten Angebote und Fallback, die mit dem Entscheidungs- und Platzierungspaar verknüpft sind) sollte eine öffentliche URL eingetragen sein (deliveryURL sollte nicht leer sein).</td> 
  </tr> 
  <tr> 
   <td>Die Entscheidung enthält Nicht-Profil-Attribute.</td> 
   <td>Die Angebotsmodellnutzung sollte nur die Profilattribute enthalten.</td> 
  </tr> 
  <tr> 
   <td>Beim Abrufen der Entscheidungsverwendung ist ein Fehler aufgetreten.</td> 
   <td>Dieser Fehler kann auftreten, wenn die API versucht, das Angebotsmodell abzurufen.</td> 
  </tr>
  <tr> 
   <td>Angebotsattribut offer-attribute ist ungültig.</td> 
   <td>Überprüfen Sie, ob das in der Angebots-Dropdown-Liste referenzierte Angebotsattribut gültig ist. Im Folgenden finden Sie die gültigen Attribute: <br/>
Bild: deliveryURL, linkURL<br/>
Text: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>
