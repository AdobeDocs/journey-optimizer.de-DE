---
title: Löschen einer Rangfolgenformel
description: Mithilfe von Rangfolgeformeln können Sie die Funktionen für die Bewertung definieren, die zum Sortieren von Elementen verwendet werden.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 19%

---

# Löschen einer Rangfolgenformel {#delete-selection-strategy}

Gelegentlich kann es erforderlich sein, (DELETE) eine Rangfolgenformel zu entfernen. Dies geschieht, indem eine DELETE-Anfrage an die Angebotsbibliotheks-API unter Verwendung der ID der Rangfolgenformel durchgeführt wird, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `rankingFormula1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Suchanfrage (GET) an die Rangfolgenformel stellen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Rangfolgenformel entfernt wurde.

