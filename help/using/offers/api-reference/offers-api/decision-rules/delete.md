---
title: Entscheidungsregeln löschen
description: Entscheidungsregeln sind Einschränkungen, die einem personalisierten Angebot hinzugefügt und auf ein Profil angewendet werden, um die Eignung zu bestimmen.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Entscheidungsregel löschen {#delete-decision-rule}

Gelegentlich kann es erforderlich sein, eine Entscheidungsregel zu entfernen (DELETE). Es können nur Entscheidungsregeln gelöscht werden, die Sie im Mandanten-Container erstellen. Dies geschieht durch Ausführung einer DELETE-Anfrage an die [!DNL Offer Library] API mit der Instanz-ID der Entscheidungsregel, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungsregeln befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Entscheidungsregel, die Sie aktualisieren möchten. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Anfrage**

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

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (Kein Inhalt) und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Entscheidungsregel ausführen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidungsregel aus dem Container entfernt wurde.
