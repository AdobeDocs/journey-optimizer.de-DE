---
title: Löschen von Entscheidungsregeln
description: Entscheidungsregeln sind Beschränkungen, die zu einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um die Berechtigung zu bestimmen.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Eine Entscheidungsregel löschen

Gelegentlich kann es erforderlich sein, eine Entscheidungsregel (DELETE) zu entfernen. Es können nur die Entscheidungsregeln gelöscht werden, die Sie im Container des Mieters erstellen. Dies geschieht, indem eine DELETE-Anforderung an die [!DNL Offer Library]-API mit der Instanzkennung der Entscheidungsregel ausgeführt wird, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungsregeln befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Entscheidungsregel, die Sie aktualisieren möchten. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Anforderung**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Eine erfolgreiche Antwort gibt HTTP-Status 202 (Kein Inhalt) und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Entscheidungsregel senden. Sie müssen einen Accept-Header in die Anforderung einbeziehen, sollten jedoch einen HTTP-Status 404 (nicht gefunden) erhalten, da die Entscheidungsregel aus dem Container entfernt wurde.
