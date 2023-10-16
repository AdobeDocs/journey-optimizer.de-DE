---
title: Entscheidungsregeln löschen
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 100%

---

# Entscheidungsregel löschen {#delete-decision-rule}

Gelegentlich kann es erforderlich sein, eine Entscheidungsregel zu entfernen (DELETE). Dies geschieht, indem Sie mit der `id` der Entscheidungsregel, die Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `offerRule1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Entscheidungsregel richten. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidungsregel entfernt wurde.
