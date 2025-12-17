---
title: Löschen einer Eignungsregel
description: Mit Eignungsregeln können Sie die geeigneten Kandidatinnen und Kandidaten basierend auf dem definieren, was Sie ansprechen möchten, z. B. Profilattribute und Zielgruppen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: ht
source-wordcount: '127'
ht-degree: 100%

---

# Löschen einer Eignungsregel {#delete-eligibility-rule}

Gelegentlich kann es erforderlich sein, eine Eignungsregel zu entfernen (DELETE). Richten Sie dazu mithilfe der ID der Eignungsregel, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API.

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

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Regel ausführen. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Regel entfernt wurde.
