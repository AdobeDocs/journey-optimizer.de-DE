---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren mit Marketo Engage
description: Erfahren Sie, wie Sie die Aktion „Marketo Engage“ verwenden
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: Marketo, Integration von Marketo Engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 100%

---

# Integrieren mit Marketo Engage {#integrating-with-marketo-engage}

Begeben Sie sich auf eine Reise der nahtlosen Datenintegration mit Marketo Engage. Diese spezifische benutzerdefinierte Aktion in Journey Optimizer unterstützt die Aufnahme von zwei wesentlichen Datentypen:

* Personen (Profile): Marketo wandelt Profile in verwertbare Erkenntnisse um.
* Benutzerdefinierte Objekte: Passen Sie Ihre Daten mit benutzerdefinierten Objekten (z. B. Produkten) für einen personalisierten Marketing-Ansatz an.

## Voraussetzungen {#prerequisites}

* Die Kundeninstanz von Marketo Engage muss IMS-fähig sein.
* Die Marketo Engage-Instanz und AEP-/AJO-Instanz müssen sich in derselben IMS-Organisation befinden.
* Der Kundin bzw. dem Kunden muss Zugriff auf den **MktoSync: Ingestion Service** bereitgestellt werden.

## Konfigurieren der Aktion {#configure-marketo-action}

* Navigieren Sie zu „Administration“ > „Konfigurationen“ > „Aktionen“ und klicken Sie auf „Verwalten“.
* Klicken Sie in der Liste „Aktionen“ auf die Aktion „Erstellen“. Weitere Informationen zu benutzerdefinierten Aktionen finden Sie [hier](../building-journeys/using-custom-actions.md){target="_blank"}.
* Geben Sie den Namen und die Beschreibung ein und wählen Sie „Adobe Marketo Engage“ als Aktionstyp aus.

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Klicken Sie für Ihre Payloads **Anfrage** und **Antwort** auf „Payload bearbeiten“.
* Erstellen Sie für beide Ihren Payload und fügen Sie ihn in das entsprechende Popup ein.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Überprüfen und Konfigurieren von Payload-Werten
Hinweis: Um Werte dynamisch zu übergeben, ändern Sie für jedes Feld **Konstante** zu **Variable**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* Klicken Sie im Fenster „Feldkonfiguration“ auf **Speichern** und dann für Ihre benutzerdefinierte Aktion auf **Speichern**.

Sie können Ihre benutzerdefinierte Aktion jetzt auf Ihrer eigenen Arbeitsfläche verwenden.


## Payload-Syntax {#payload-syntax}

### Person

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Payload-Beispiel für Person**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Payload-Beispiel für benutzerdefiniertes Objekt**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## Verwenden der Aktion {#engage-using}

* Ziehen Sie die benutzerdefinierte Aktion auf die Journey-Arbeitsfläche.
* Klicken Sie unter **Anfrageparameter** für jeden Parameter mit dynamischen Werten, die Sie in der Payload konfiguriert haben, auf „Bearbeiten“.

![](assets/engage-use-canvas.png){width="70%" align="left"}
