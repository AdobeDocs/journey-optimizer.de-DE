---
title: Löschen einer Elementsammlung
description: Erfahren Sie, wie Sie Ihre Gruppenentscheidungen in Sammlungen kategorisieren.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/JpZKEp0CnLg30ExvgHamm6dknBlr9vB1QlAlwMNAZKI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 100%

---

# Löschen einer Elementsammlung {#delete-decision-item}

Gelegentlich kann es erforderlich sein, eine Elementsammlung zu entfernen (DELETE). Führen Sie dazu mithilfe der ID der Elementsammlung, die Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API aus.

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

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Elementsammlung ausführen. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Elementsammlung entfernt wurde.
