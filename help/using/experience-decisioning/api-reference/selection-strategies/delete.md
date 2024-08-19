---
title: Löschen einer Auswahlstrategie
description: Auswahlstrategien bestehen aus Kollektionen, die mit Begrenzungen und Rangmethoden zur Bestimmung von Angeboten verknüpft sind.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 27%

---


# Löschen einer Auswahlstrategie {#delete-selection-strategy}

Gelegentlich kann es erforderlich sein, eine Auswahlstrategie zu entfernen (DELETE). Dies geschieht, indem Sie mithilfe der ID der Auswahlstrategie, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API richten.

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
