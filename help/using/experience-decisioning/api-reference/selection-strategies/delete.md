---
title: Auswahlstrategie löschen
description: Auswahlstrategien bestehen aus Sammlungen, die mit Einschränkungen und Ranking-Methoden verknüpft sind, um Angebote zu bestimmen.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/KnyhVoNWfjSIIMw2q7OZkBG--wgaBU4JXn7A9i41Vf8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 0%

---

# Auswahlstrategie löschen {#delete-selection-strategy}

Gelegentlich kann es erforderlich sein, (DELETE) eine Auswahlstrategie zu entfernen. Dies geschieht, indem Sie eine DELETE-Anfrage an die Angebotsbibliotheks-API mit der ID der Auswahlstrategie durchführen, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `selectionStrategy1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status-Code 200 und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Suchanfrage (GET) an die Auswahlstrategie stellen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Auswahlstrategie entfernt wurde.
