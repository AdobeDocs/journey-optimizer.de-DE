---
title: Löschen eines Entscheidungselements
description: Entscheidungselemente sind Marketing-Angebote, die Sie erstellen und in Sammlungen und Katalogen organisieren können.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 100%

---

# Löschen eines Entscheidungselements {#delete-decision-item}

Um ein Entscheidungselement zu entfernen, führen Sie eine DELETE-Anfrage an die Angebotsbibliothek-API mit der ID des Entscheidungselements aus, das Sie löschen möchten.

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

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an das Entscheidungselement richten. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da das Entscheidungselement entfernt wurde.
