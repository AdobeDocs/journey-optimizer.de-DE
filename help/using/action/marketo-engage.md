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
source-git-commit: a5ee7c668b51a761266b50216047caf48496f678
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 36%

---

# Integrieren mit Marketo Engage {#integrating-with-marketo-engage}

Begeben Sie sich auf eine Reise der nahtlosen Datenintegration mit Marketo Engage. In Ihren Journey ist eine spezifische benutzerdefinierte Aktion verfügbar, um Adobe Journey Optimizer und Marketo Engage zu integrieren. Diese benutzerdefinierte Aktion unterstützt die Aufnahme von zwei wichtigen Datentypen:

* **Personen** (Profile): Marketo transformiert Profile in umsetzbare Einblicke.
* **Benutzerdefinierte Objekte**: Passen Sie Ihre Daten mit benutzerdefinierten Objekten wie Produkten für einen personalisierten Marketing-Ansatz an.

## Voraussetzungen {#prerequisites}

Für diese Integration gelten die folgenden Voraussetzungen:

* Die Kundeninstanz von Marketo Engage muss IMS-fähig sein.
* Die Marketo Engage-Instanz und Adobe Experience Platform/Journey Optimizer-Instanz müssen sich in derselben IMS-Organisation befinden.
* Der Kundin bzw. dem Kunden muss Zugriff auf den **MktoSync: Ingestion Service** bereitgestellt werden.

## Konfigurieren der Aktion {#configure-marketo-action}


In Journey Optimizer müssen Sie eine benutzerdefinierte Aktion für Marketo Engage konfigurieren. Führen Sie folgende Schritte aus:

1. Wählen **[!UICONTROL Konfigurationen]** im Menüabschnitt ADMINISTRATION aus.
1. Klicken **[!UICONTROL Abschnitt „Aktionen]** auf **[!UICONTROL Aktion erstellen]**. Der Bereich für die Aktionskonfiguration wird auf der rechten Seite des Bildschirms geöffnet.
1. Geben Sie Namen und Beschreibung ein und wählen Sie **Adobe Marketo Engage** als **Aktionstyp**

![](assets/engage-customaction-creation.png){width="40%" align="left"}

1. Klicken Sie auf das **Payload bearbeiten**-Symbol für Ihre **Anfrage** und **Antwort**-Payloads.
1. Erstellen Sie für beide Ihre Payload und fügen Sie sie in das entsprechende Popup ein.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

1. Überprüfen und Konfigurieren von Payload-Werten
Hinweis: Um Werte dynamisch zu übergeben, ändern Sie für jedes Feld **Konstante** zu **Variable**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Klicken Sie **Konfigurationsbildschirm Feld auf** Speichern“ und dann **benutzerdefinierte Aktion** Speichern“.

Sie können jetzt Ihre benutzerdefinierte Aktion auf der Journey-Arbeitsfläche verwenden.

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


## Aktion verwenden {#engage-using}

Für jede konfigurierte Aktion ist eine Marketo Engage-Aktionsaktivität in der Journey-Designer-Palette verfügbar.

Gehen Sie wie folgt vor, um sie zu verwenden:

1. Ziehen Sie die benutzerdefinierte Aktion auf die Journey-Arbeitsfläche.

1. Geben Sie den Titel und die Beschreibung dieser Aktion ein.

1. Klicken Sie **Abschnitt** auf das Symbol **Bearbeiten** für jeden Parameter und wählen Sie die dynamischen Werte aus, die Sie in der Payload konfiguriert haben.

![](assets/engage-use-canvas.png){width="70%" align="left"}
