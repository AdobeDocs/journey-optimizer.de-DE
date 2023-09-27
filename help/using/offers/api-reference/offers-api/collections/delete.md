---
title: Löschen von Sammlungen
description: Sammlungen sind Untergruppen von Angeboten, die auf von einem Marketing-Experten vordefinierten Bedingungen basieren, z. B. der Kategorie des Angebots.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 48%

---

# Löschen von Sammlungen {#delete-collection}

Gelegentlich kann es erforderlich sein, eine Sammlung zu entfernen (DELETE). Dies geschieht durch Ausführung einer DELETE-Anfrage an die [!DNL Offer Library] API mit der `id` der Kollektion, die Sie löschen möchten.

**API-Format**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Persistenz-APIs. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | Die ID der Entität, die Sie löschen möchten. | `offerCollection1234` |

**Anfrage**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Antwort**

Eine erfolgreiche Antwort gibt den HTTP-Status 200 und einen leeren Text zurück.

Sie können den Löschvorgang bestätigen, indem Sie eine Nachschlageanfrage (GET) für die Sammlung ausführen. Sie sollten den HTTP-Status 404 (Nicht gefunden) erhalten, da die Sammlung entfernt wurde.
