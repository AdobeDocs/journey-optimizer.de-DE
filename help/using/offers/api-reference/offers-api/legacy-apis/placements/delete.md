---
title: Platzierungen löschen
description: Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 100%

---

# Platzierung löschen {#delete-placement}

Gelegentlich kann es erforderlich sein, eine Platzierung zu entfernen (DELETE). Es können nur Platzierungen gelöscht werden, die Sie im Mandanten-Container erstellen. Dies geschieht, indem Sie mit der Instanz-ID der Platzierung, die Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Platzierungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Platzierung, die Sie aktualisieren möchten. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Anfrage**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (kein Inhalt) und leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Platzierung ausführen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Platzierung aus dem Container entfernt wurde.
