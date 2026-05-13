---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Fallback-Angebot aktualisieren
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn sie für andere Angebote nicht infrage kommen
feature: Decision Management, API
badge: label="Veraltet" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: f153c2ee-e789-4d8e-a03b-e914690ff354
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/LS2tnWXKdj2cFf-VFEJd-tygvnE48dyi2JAKSejsxZ8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# Fallback-Angebot aktualisieren {#update-fallback-offer}

>[!TIP]
>
>Decisioning, [!DNL Adobe Journey Optimizer] neue Entscheidungsfunktion, ist jetzt über die Code-basierten Erlebnis- und E-Mail-Kanäle verfügbar! [Weitere Informationen](../../../../../experience-decisioning/gs-experience-decisioning.md)


Sie können ein Fallback-Angebot in Ihrem Container ändern oder aktualisieren, indem Sie eine PATCH-Anfrage an die [!DNL Offer Library]-API richten.

Weitere Informationen zu JSON-Patch-Vorgängen, einschließlich verfügbarer Vorgänge, finden Sie in der offiziellen [JSON-Patch-Dokumentation](https://jsonpatch.com/).

## Accept- und Content-Type-Kopfzeilen {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte der Felder *Content-Type* und *Accept* im Anfrage-Header:

| Header-Name | Wert |
| ----------- | ----- |
| content-type | `application/json` |

**API-Format**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Fallback-Angebote befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Fallback-Angebots. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Anfrage**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| Parameter | Beschreibung |
| --------- | ----------- |
| `op` | Der Operationsaufruf, der verwendet wird, um die Aktion zu definieren, die zum Aktualisieren der Verbindung erforderlich ist. Operationen umfassen: `add`, `replace` und `remove`. |
| `path` | Der Pfad des zu aktualisierenden Parameters. |
| `value` | Der neue Wert, mit dem Sie Ihren Parameter aktualisieren möchten. |

**Antwort**

Eine erfolgreiche Antwort gibt die aktualisierten Details des Fallback-Angebots zurück, einschließlich der eindeutigen `id`.

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
