---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Entscheidungen löschen
description: Eine Entscheidung enthält die Logik, die über die Auswahl eines Angebots bestimmt.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 36a87d98-fd61-416e-83a1-e267a7b4d455
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-NdP9Eia9rQR-PKVEESckF-pk8XA8-Zyy-2trkJLHhc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 100%

---

# Löschen einer Entscheidung {#delete-decision}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../../experience-decisioning/gs-experience-decisioning.md)


Gelegentlich kann es erforderlich sein, eine Entscheidung zu löschen (DELETE). Es können nur Entscheidungen gelöscht werden, die Sie im Mandanten-Container erstellt haben. Dies geschieht, indem Sie mit der $id des Fallback-Angebots, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Die Instanz-ID der Entscheidung. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Anfrage**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 202 (Kein Inhalt) und leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine GET-Anfrage (Nachschlagen) an die Entscheidung senden. Sie müssen einen Accept-Header in die Anfrage einbeziehen, sollten jedoch einen HTTP-Status 404 (Nicht gefunden) erhalten, da die Entscheidung aus dem Container entfernt wurde.
