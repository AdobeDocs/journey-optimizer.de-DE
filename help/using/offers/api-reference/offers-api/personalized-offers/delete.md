---
title: Personalisierte Angebote löschen
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '114'
ht-degree: 100%

---

# Personalisiertes Angebot löschen {#delete-personalized-offer}

Gelegentlich kann es erforderlich sein, ein personalisiertes Angebot zu entfernen (DELETE). Dies geschieht, indem Sie mit der ID des personalisierten Angebots, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `personalizedOffer1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an das personalisierte Angebot richten. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da das personalisierte Angebot entfernt wurde.
