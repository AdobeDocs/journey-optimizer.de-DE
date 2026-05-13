---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Löschen eines Fallback-Angebots
description: Ein Fallback-Angebot wird an Kunden gesendet, wenn keine anderen Angebote für sie geeignet sind.
feature: Decision Management, API
badge: label="Vorgängerversion" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/3SJmNX6JrEY07R4pePNPzdokJrK7Ye6e9gV5i1LlDJA
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
source-wordcount: 138
ht-degree: 100%

---

# Löschen eines Fallback-Angebots {#delete-fallback-offer}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../../experience-decisioning/gs-experience-decisioning.md)


Gelegentlich kann es erforderlich sein, ein Fallback-Angebot zu löschen (DELETE). Dies geschieht, indem Sie mit der ID des Fallback-Angebots, das Sie löschen möchten, eine DELETE-Anfrage an die [!DNL Offer Library]-API richten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für persistente APIs. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `fallbackOffer1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Bei einer erfolgreichen Antwort wird der HTTP-Status 200 und leerer Text zurückgegeben.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) an das Angebot richten. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da das Fallback-Angebot entfernt wurde.
