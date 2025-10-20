---
title: Löschen einer Auswahlstrategie
description: Auswahlstrategien bestehen aus Sammlungen, die mit Begrenzungen und Rangfolgenmethoden zur Bestimmung von Angeboten verknüpft sind.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 100%

---

# Löschen einer Auswahlstrategie {#delete-selection-strategy}

Gelegentlich kann es erforderlich sein, eine Auswahlstrategie zu entfernen (DELETE). Führen Sie dazu mithilfe der ID der Auswahlstrategie, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliotheks-API aus.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
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

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Auswahlstrategie ausführen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Auswahlstrategie entfernt wurde.
