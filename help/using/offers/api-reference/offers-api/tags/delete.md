---
title: Tags löschen
description: Mit Tags können Sie Ihre Angebote besser organisieren und sortieren.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 100%

---

# Tag löschen

Gelegentlich kann es erforderlich sein, ein Tag zu entfernen (DELETE). Es können nur Tags gelöscht werden, die Sie im Mandanten-Container erstellen. Dies geschieht, indem Sie mit der $id des Tags, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Tags befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Tags, das Sie aktualisieren möchten. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Anfrage**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (kein Inhalt) und leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für das Tag ausführen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da das Tag aus dem Container entfernt wurde.
