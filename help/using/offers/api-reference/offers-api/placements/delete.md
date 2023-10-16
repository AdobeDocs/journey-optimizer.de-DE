---
title: Platzierungen löschen
description: Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 100%

---

# Löschen von Platzierungen {#delete-placement}

Gelegentlich kann es erforderlich sein, eine Platzierung zu entfernen (DELETE). Dies geschieht, indem Sie mit der ID der Platzierung, die Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die Instanz-ID der Platzierung, die Sie aktualisieren möchten. | `offerPlacement1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Platzierung richten. Sie sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Platzierung entfernt wurde.
