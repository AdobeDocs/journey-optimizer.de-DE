---
title: Löschen von Sammlungsqualifizierern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 35%

---

# Löschen eines Sammlungsqualifizierers {#delete-tag}

Gelegentlich kann es erforderlich sein, einen Sammlungsqualifizierer (ehemals als „Tag“ bezeichnet) zu entfernen (DELETE). Dies geschieht durch Ausführung einer DELETE-Anfrage an die [!DNL Offer Library] API mit der ID des Sammlungsqualifizierers, den Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `tag1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 200 und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an den Sammlungsbezeichner senden und sollten einen HTTP-Status 404 (Nicht gefunden) erhalten, da er entfernt wurde.