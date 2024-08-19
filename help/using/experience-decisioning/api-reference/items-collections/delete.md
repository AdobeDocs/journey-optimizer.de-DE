---
title: Löschen einer Elementsammlung
description: Erfahren Sie, wie Sie Ihre Gruppenentscheidungen in Sammlungen kategorisieren.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 28%

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
