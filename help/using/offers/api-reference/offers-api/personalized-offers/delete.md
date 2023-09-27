---
title: Personalisierte Angebote löschen
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 34%

---

# Personalisiertes Angebot löschen {#delete-personalized-offer}

Gelegentlich kann es erforderlich sein, ein personalisiertes Angebot zu entfernen (DELETE). Dies geschieht durch Ausführung einer DELETE-Anfrage an die [!DNL Offer Library] API mit der ID des personalisierten Angebots, das Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |
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

Eine erfolgreiche Antwort gibt den HTTP-Status 200 und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an das personalisierte Angebot senden und den HTTP-Status 404 (Nicht gefunden) erhalten, da das personalisierte Angebot entfernt wurde.
