---
title: Löschen einer Eignungsregel
description: Mit Eignungsregeln können Sie die geeigneten Kandidaten basierend auf dem definieren, was Sie ansprechen möchten, z. B. Profilattribute und Audiences.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 25%

---

# Löschen einer Eignungsregel {#delete-eligibility-rule}

Gelegentlich kann es erforderlich sein, eine Eignungsregel zu entfernen (DELETE). Dies geschieht, indem Sie eine DELETE-Anfrage an die Angebotsbibliotheks-API mit der ID der Eignungsregel ausführen, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `rule1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Suchanfrage (GET) an die Regel stellen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Regel entfernt wurde.
