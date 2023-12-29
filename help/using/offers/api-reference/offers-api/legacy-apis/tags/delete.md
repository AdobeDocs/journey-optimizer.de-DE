---
title: Löschen von Sammlungsqualifizierern
description: Mit Sammlungsqualifizierern können Sie Ihre Angebote besser organisieren und sortieren.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: cc67519e-7a80-49c7-8c8b-c777be633026
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 100%

---

# Löschen eines Sammlungsqualifizierers {#delete-tag}

Gelegentlich kann es erforderlich sein, einen Sammlungsqualifizierer (ehemals als „Tag“ bezeichnet) zu entfernen (DELETE). Es können nur Sammlungskennzeichner gelöscht werden, die Sie im Mandanten-Container erstellt haben. Dies geschieht, indem Sie eine DELETE-Anfrage an die [!DNL Offer Library]-API mit der $ID des Sammlungsqualifizierers durchführen, den Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Sammlungsqualifizierer befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID des Sammlungsqualifizierers, den Sie aktualisieren möchten. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

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

Sie können die Löschung bestätigen, indem Sie eine Nachschlageanfrage (GET) an den Sammlungsqualifizierer versuchen. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da der Sammlungsqualifizierer aus dem Container entfernt wurde.
