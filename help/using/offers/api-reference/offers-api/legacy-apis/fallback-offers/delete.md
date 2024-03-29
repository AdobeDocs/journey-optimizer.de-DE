---
title: Löschen von Fallback-Angeboten
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn keine anderen Angebote für sie geeignet sind.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5e97a1fd-7542-4c9a-8234-21c1fa419671
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 100%

---

# Löschen von Fallback-Angeboten {#delete-fallback-offer}

Gelegentlich kann es erforderlich sein, ein Fallback-Angebot zu entfernen (DELETE). Es können nur Fallback-Angebote gelöscht werden, die Sie im Mandanten-Container erstellen. Dies geschieht, indem Sie mit der $id des Fallback-Angebots, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Fallback-Angebote befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Fallback-Angebots. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Anfrage**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (kein Inhalt) und leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für das Fallback-Angebot ausführen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da das Fallback-Angebot aus dem Container entfernt wurde.
