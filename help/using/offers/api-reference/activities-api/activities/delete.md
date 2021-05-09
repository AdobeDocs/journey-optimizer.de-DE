---
title: Entscheidungen löschen
description: Eine Entscheidung enthält die Logik, die die Auswahl eines Angebots informiert.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Eine Entscheidung löschen

Gelegentlich kann es erforderlich sein, eine Entscheidung (DELETE) zu entfernen (früher als Angebot-Aktivität bekannt). Es können nur Entscheidungen gelöscht werden, die Sie im Pächter-Container erstellen. Dies geschieht, indem Sie eine DELETE-Anforderung an die [!DNL Offer Library]-API mit der $id des Ausweichmanagers ausführen, das Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem die Entscheidungen getroffen werden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Entscheidung. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Anforderung**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Eine erfolgreiche Antwort gibt HTTP-Status 202 (Kein Inhalt) und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Entscheidung senden. Sie müssen einen Accept-Header in die Anforderung einbeziehen, sollten jedoch den HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidung aus dem Container entfernt wurde.
