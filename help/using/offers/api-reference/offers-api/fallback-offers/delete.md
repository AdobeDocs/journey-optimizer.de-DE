---
title: Ausweichmanöver-Angebot löschen
description: Ein Ausweich-Angebot wird an Kunden gesendet, wenn sie nicht für andere Angebot zugelassen sind
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Ausweichmanöver-Angebot löschen

Gelegentlich kann es erforderlich sein, ein Fallback-Angebot (DELETE) zu entfernen. Es können nur Fallback-Angebot gelöscht werden, die Sie im Container des Mieters erstellen. Dies geschieht, indem Sie eine DELETE-Anforderung an die [!DNL Offer Library]-API mit der $id des Ausweichmanagers ausführen, das Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Fallback-Angebot befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Fallback-Angebots. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Anforderung**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Eine erfolgreiche Antwort gibt HTTP-Status 202 (Kein Inhalt) und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an das Ausweichmanöver-Angebot senden. Sie müssen einen Accept-Header in die Anforderung einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da das Fallback-Angebot aus dem Container entfernt wurde.
