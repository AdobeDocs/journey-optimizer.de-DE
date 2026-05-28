---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Entscheidungen löschen
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/CV9NY9PmXlHXJBjlGAvnk7RN088i1Q6gvzTO5dTCWys
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 100%

---

# Löschen einer Entscheidung {#delete-decision}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Gelegentlich kann es erforderlich sein, eine Entscheidung zu löschen (DELETE). Dies geschieht, indem Sie mit der `id` der Entscheidung, die Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `offerDecision1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Entscheidung richten. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidung entfernt wurde.
