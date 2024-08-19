---
title: Löschen einer Elementsammlung
description: Mit Sammlungen können Sie Entscheidungselemente nach Ihren Voreinstellungen kategorisieren und gruppieren.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 27%

---


# Löschen einer Elementsammlung {#delete-decision-item}

Gelegentlich kann es erforderlich sein, eine Artikelsammlung zu entfernen (DELETE). Dies geschieht, indem Sie mit der ID der Elementsammlung, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `itemCollections1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Elementerfassung ausführen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Artikelsammlung entfernt wurde.
