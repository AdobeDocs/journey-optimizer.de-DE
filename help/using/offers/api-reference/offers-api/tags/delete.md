---
title: Löschen von Sammlungsqualifizierern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 67%

---


# Löschen eines Sammlungsqualifizierers {#delete-tag}

Gelegentlich kann es erforderlich sein, einen Sammlungsqualifizierer (ehemals als „Tag“ bezeichnet) zu entfernen (DELETE). Dies geschieht, indem Sie mit der ID des Kollektionqualifikators, den Sie löschen möchten, eine DELETE-Anfrage an die Angebotsbibliothek-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
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

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können die Löschung bestätigen, indem Sie eine Nachschlageanfrage (GET) an den Sammlungsqualifizierer versuchen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da der Sammlungsbezeichner entfernt wurde.