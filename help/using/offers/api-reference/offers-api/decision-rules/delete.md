---
title: Entscheidungsregeln löschen
description: Entscheidungsregeln sind Begrenzungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um dessen Eignung zu bestimmen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 35%

---

# Entscheidungsregel löschen {#delete-decision-rule}

Gelegentlich kann es erforderlich sein, eine Entscheidungsregel zu entfernen (DELETE). Dies geschieht durch Ausführung einer DELETE-Anfrage an die [!DNL Offer Library] API mit der `id` der Entscheidungsregel, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
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

Eine erfolgreiche Antwort gibt den HTTP-Status 200 und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Entscheidungsregel senden und sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidungsregel entfernt wurde.
