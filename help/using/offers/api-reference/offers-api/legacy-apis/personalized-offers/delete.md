---
title: Personalisierte Angebote löschen
description: Ein personalisiertes Angebot ist eine anpassbare Marketing-Nachricht, die auf Eignungsregeln und Einschränkungen basiert.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6ae37843-2679-48a3-96ef-bb93a5d4a333
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '144'
ht-degree: 100%

---

# Personalisiertes Angebot löschen {#delete-personalized-offer}

Gelegentlich kann es erforderlich sein, ein personalisiertes Angebot zu entfernen (DELETE). Es können nur personalisierte Angebote gelöscht werden, die Sie im Mandanten-Container erstellen. Dies geschieht, indem Sie mit der $id des personalisierten Angebots, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die personalisierten Angebote befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (kein Inhalt) und leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für das personalisierte Angebot ausführen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da das personalisierte Angebot aus dem Container entfernt wurde.
