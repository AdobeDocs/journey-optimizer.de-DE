---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden benutzerdefinierter Aktionen zum Schreiben von Journey-Ereignissen in AEP
description: Verwenden benutzerdefinierter Aktionen zum Schreiben von Journey-Ereignissen in AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---


# Anwendungsbeispiel: Verwenden benutzerdefinierter Aktionen zum Schreiben von Journey-Ereignissen in Experience Platform{#custom-action-aep}

In diesem Anwendungsbeispiel wird beschrieben, wie Sie benutzerdefinierte Ereignisse mithilfe von benutzerdefinierten Aktionen und authentifizierten Aufrufen aus Journey in Adobe Experience Platform schreiben.

## Konfigurieren eines IO-Projekts

1. Klicken Sie in der Adobe Developer Console auf **Projekt** und öffnen Sie Ihr IO-Projekt.

1. Im **Anmeldeinformationen** Abschnitt, klicken Sie auf **OAuth Server-zu-Server**.

   ![](assets/custom-action-aep-1.png)

1. Klicks **cURL anzeigen, Befehl**.

   ![](assets/custom-action-aep-2.png)

1. Kopieren Sie den cURL-Befehl und speichern Sie client_id, client_secret, grant_type und scope.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

## Konfigurieren der Quelle mithilfe des HTTP-API-Inlets

1. Erstellen Sie einen Endpunkt in Adobe Experience Platform, um die Daten aus Journey zu schreiben.

1. Klicken Sie in Adobe Experience Platform auf **Quellen**, unter **Verbindungen** im linken Menü. under **HTTP-API** klicken **Daten hinzufügen**.

   ![](assets/custom-action-aep-3.png)

1. Auswählen **Neues Konto** und aktivieren Sie die Authentifizierung. Klicken Sie auf **Verbindung mit Quelle herstellen**.

   ![](assets/custom-action-aep-4.png)

1. Klicken Sie auf **Nächste** und wählen Sie den Datensatz aus, in den Sie die Daten schreiben möchten. Klicks **Nächste** und **Beenden**.

   ![](assets/custom-action-aep-5.png)

1. Öffnen Sie den neu erstellten Datenfluss. Kopieren Sie die Schema-Payload und speichern Sie sie in Ihrem Notebook.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Benutzerdefinierte Aktion konfigurieren

1. Öffnen Sie Adobe Journey Optimizer und klicken Sie auf **Konfigurationen**, unter **Administration** im linken Menü. under **Aktionen** klicken **Verwalten** und klicken **Aktion erstellen**.

1. Legen Sie die URL fest und wählen Sie die Methode Post aus.

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Stellen Sie sicher, dass die Kopfzeilen (Inhaltstyp, Zeichensatz, Sandbox-Name) konfiguriert sind.

   ![](assets/custom-action-aep-7bis.png)

### Einrichten der Authentifizierung

1. Wählen Sie die **Typ** as **Benutzerdefiniert** mit der folgenden Payload.

1. Fügen Sie client_secret, client_id, scope und grant_type (aus der zuvor verwendeten IO-Projekt-Payload) ein.

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Verwenden Sie die **Klicken Sie auf , um die Authentifizierung zu testen** Schaltfläche zum Testen der Verbindung.

   ![](assets/custom-action-aep-8.png)

### Einrichten der Payload

1. Im **Anfrage** und **Reaktion** -Felder die Payload aus der zuvor verwendeten Quellverbindung einfügen.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. Ändern Sie die Feldkonfiguration unter **Konstante** nach **Variable** für Felder, die dynamisch ausgefüllt werden. Speichern Sie die benutzerdefinierte Aktion.

## Journey

1. Verwenden Sie abschließend diese benutzerdefinierte Aktion in einer Journey, um die benutzerdefinierten Journey-Ereignisse zu schreiben.

1. Füllen Sie die Journey-Version-ID, Knoten-ID, Knotenname und andere Attribute gemäß Ihrem Anwendungsfall aus.

   ![](assets/custom-action-aep-9.png)


