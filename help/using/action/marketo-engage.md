---
solution: Journey Optimizer
product: journey optimizer
title: Integrieren mit Marketo Engage
description: Erfahren Sie, wie Sie die Aktion „Marketo Engage“ verwenden
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: Marketo, Integration von Marketo Engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '325'
ht-degree: 100%

---

# Integrieren mit Marketo Engage {#integrating-with-marketo-engage}

Begeben Sie sich auf eine Reise der nahtlosen Datenintegration mit Marketo Engage. In den Journeys ist eine spezifische benutzerdefinierte Aktion zum Integrieren von Adobe Journey Optimizer und Marketo Engage verfügbar. Diese benutzerdefinierte Aktion unterstützt die Aufnahme von zwei wesentlichen Datentypen:

* **Personen** (Profile): Marketo wandelt Profile in verwertbare Erkenntnisse um.
* **Benutzerdefinierte Objekte**: Daten werden mit benutzerdefinierten Objekten (z. B. Produkten) für einen personalisierten Marketing-Ansatz angepasst.

## Voraussetzungen {#prerequisites}

Für diese Integration gelten die folgenden Voraussetzungen:

* Die Kundeninstanz von Marketo Engage muss IMS-fähig sein
* Die Marketo Engage-Instanz und die Adobe Experience Platform/Journey Optimizer-Instanz müssen sich in derselben Organisation befinden
* Der Kundin bzw. dem Kunden muss Zugriff auf den **MktoSync: Ingestion Service** bereitgestellt werden

## Konfigurieren der Aktion {#configure-marketo-action}


In Journey Optimizer muss eine benutzerdefinierte Aktion für Marketo Engage konfiguriert werden. Führen Sie folgende Schritte aus:

1. Wählen SIe **[!UICONTROL Konfigurationen]** im Menüabschnitt ADMINISTRATION aus. 
1. Klicken Sie im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Aktion erstellen]**. Der Bereich für die Aktionskonfiguration wird auf der rechten Seite des Bildschirms geöffnet.
1. Geben Sie Name und Beschreibung ein und wählen Sie **Adobe Marketo Engage** als **Aktionstyp** aus.
   ![](assets/engage-customaction-creation.png){width="40%" align="left"}
1. Klicken Sie für die Payloads **Anfrage** und **Antwort** auf **Payload bearbeiten**.
1. Erstellen Sie Ihre Payload für beide und fügen Sie sie in das entsprechende Popup ein.
   ![](assets/engage-customaction-payload.png){width="70%" align="left"}
1. Überprüfen und Konfigurieren von Payload-Werten

   Hinweis: Um Werte dynamisch zu übergeben, ändern Sie für jedes Feld **Konstante** in **Variable**.

   ![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Klicken Sie im Bildschirm „Feldkonfiguration“ auf **Speichern** und **speichern** Sie dann die benutzerdefinierte Aktion.

Die benutzerdefinierte Aktion kann jetzt auf der eigenen Journey-Arbeitsfläche verwendet werden.

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

Für jede konfigurierte Aktion ist eine Marketo Engage-Aktionsaktivität in der Journey-Designer-Palette verfügbar.

Gehen Sie wie folgt vor, um diese zu verwenden:

1. Ziehen Sie die benutzerdefinierte Aktion auf die Journey-Arbeitsfläche.

1. Geben Sie Label und Beschreibung dieser Aktion ein.

1. Klicken Sie im Abschnitt **Anfrageparameter** für jeden Parameter auf das Symbol **Bearbeiten** und wählen Sie die dynamischen Werte aus, die in der Payload konfiguriert wurden.

![](assets/engage-use-canvas.png){width="70%" align="left"}
