---
title: Eine Sammlung löschen
description: Sammlungen sind Untergruppen von Angeboten, die auf vordefinierten, von einem Marketingexperten definierten Bedingungen basieren, z. B. der Kategorie des Angebots.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Eine Sammlung löschen

Es kann gelegentlich erforderlich sein, eine Sammlung zu entfernen (DELETE). Es können nur Sammlungen gelöscht werden, die Sie im Pächter-Container erstellen. Dies geschieht, indem eine DELETE-Anforderung an die [!DNL Offer Library]-API mit der $id der Sammlung ausgeführt wird, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Sammlungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Sammlung, die Sie aktualisieren möchten. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Anforderung**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Reaktion**

Eine erfolgreiche Antwort gibt HTTP-Status 202 (Kein Inhalt) und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an die Sammlung senden. Sie müssen einen Accept-Header in die Anforderung einbeziehen, erhalten jedoch den HTTP-Status 404 (Nicht gefunden), da die Sammlung aus dem Container entfernt wurde.
