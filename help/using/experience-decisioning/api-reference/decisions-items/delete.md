---
title: Entscheidungselement löschen
description: Entscheidungselemente sind Marketing-Angebote, die Sie erstellen und in Sammlungen und Katalogen organisieren können.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 27%

---


# Entscheidungselement löschen {#delete-decision-item}

Gelegentlich kann es erforderlich sein, einen Entscheidungspunkt zu entfernen (DELETE). Dies geschieht, indem Sie mit der ID des Entscheidungselements, das Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API richten.

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
