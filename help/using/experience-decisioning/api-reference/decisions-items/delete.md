---
title: Entscheidungselement löschen
description: Entscheidungselemente sind Marketing-Angebote, die Sie erstellen und in Sammlungen und Katalogen organisieren können.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 29%

---


# Entscheidungselement löschen {#delete-decision-item}

Um ein Entscheidungselement zu entfernen, senden Sie eine DELETE-Anfrage an die Angebotsbibliothek-API mit der Kennung des Entscheidungselements, das Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `offerItem1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für das Entscheidungselement ausführen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da das Entscheidungselement entfernt wurde.
