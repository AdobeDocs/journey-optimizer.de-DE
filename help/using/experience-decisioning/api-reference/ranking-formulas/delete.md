---
title: Löschen einer Rangfolgeformel
description: Mithilfe von Rangfolgenformeln können Sie die Funktionen für die Bewertung definieren, die zum Ordnen von Elementen verwendet werden.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ea50481-b1b9-4e0c-ad4e-c4139891bfdf
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 100%

---

# Löschen einer Rangfolgeformel {#delete-selection-strategy}

Gelegentlich kann es erforderlich sein, eine Rangfolgenformel zu entfernen (DELETE). Richten Sie dazu mithilfe der ID der Rangfolgenformel, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API.

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

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Rangfolgenformel richten. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Rangfolgenformel entfernt wurde.
