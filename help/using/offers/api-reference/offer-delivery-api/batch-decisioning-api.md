---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Batch Decisioning-API
description: Erfahren Sie, wie Sie mit der Batch Decisioning-API innerhalb eines vordefinierten Entscheidungsumfangs die besten Angebote für Zielgruppenprofile auswählen können.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/2FrtFGbl169aXj29ltmUKS23eXFns1cG8TPojw3TwCY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 749
ht-degree: 100%

---

# Unterbreiten von Angeboten mithilfe der [!DNL Batch Decisioning]-API {#deliver-offers-batch}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../../experience-decisioning/gs-experience-decisioning.md)

Mit der [!DNL Batch Decisioning]-API können Unternehmen die Entscheidungsfunktion mit einem einzigen Aufruf auf alle Profile in einer bestimmten Zielgruppe anwenden. Der Angebotsinhalt für jedes Profil in der Zielgruppe wird in einen Adobe Experience Platform-Datensatz platziert, über den er für benutzerdefinierte Batch-Workflows zur Verfügung steht.

Mit der [!DNL Batch Decisioning]-API können Sie einen Datensatz mit den besten Angeboten für alle Profile in einer Adobe Experience Platform-Zielgruppe für Entscheidungsumfänge auffüllen. Beispiel: Ein Unternehmen möchte [!DNL Batch Decisioning] ausführen, damit es Angebote an einen Nachrichtenversand-Anbieter senden kann. Diese Angebote werden dann als Inhalt verwendet, der für den Batch-Nachrichtenversand an dieselbe Benutzerzielgruppe gesendet wird.

Dazu muss das Unternehmen folgendermaßen vorgehen:

* Die [!DNL Batch Decisioning]-API ausführen, die zwei Anfragen enthält:

   1. Eine **Batch-POST-Anfrage**, um einen Workload zur Batch-Verarbeitung der Angebotsauswahl zu starten.

   2. Eine **Batch-GET-Anfrage**, um den Status des Batch-Workloads abzurufen.

* Den Datensatz an die Nachrichtenversand-API des Anbieters exportieren

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html) to learn more about exporting audiences.) -->

>[!NOTE]
>
>Batch-Entscheidungen können auch über die Journey Optimizer-Oberfläche getroffen werden. Weitere Informationen finden Sie in [diesem Abschnitt](../../batch-delivery.md), der globale Voraussetzungen und Einschränkungen enthält, die bei der Verwendung der Batch-Entscheidung zu berücksichtigen sind.

* **Die Anzahl der ausgeführten Batch-Aufträge pro Datensatz**: Pro Datensatz können bis zu fünf Batch-Aufträge gleichzeitig ausgeführt werden. Alle anderen Batch-Anfragen mit demselben Ausgabedatensatz werden der Warteschlange hinzugefügt. Ein in die Warteschlange gestellter Auftrag wird zur Verarbeitung aufgenommen, sobald der vorherige Auftrag abgeschlossen ist.
* **Frequenzbegrenzung**: Ein Batch wird auf Basis eines Profil-Snapshots ausgeführt, der einmal täglich erfolgt. Die [!DNL Batch Decisioning]-API begrenzt die Häufigkeit und lädt Profile immer aus dem neuesten Snapshot.

## Erste Schritte {#getting-started}

Bevor Sie diese API verwenden, müssen Sie die folgenden Schritte ausführen.

### Entscheidungsvorbereitung {#prepare-decision}

Um eine oder mehrere Entscheidungen vorzubereiten, stellen Sie sicher, dass Sie einen Datensatz, eine Zielgruppe und eine Entscheidung erstellt haben. Diese Voraussetzungen werden in [diesem Abschnitt](../../batch-delivery.md) näher erläutert.

### API-Anforderungen {#api-requirements}

Alle [!DNL Batch Decisioning]-Anfragen erfordern zusätzlich zu den im [Entwicklerhandbuch zur Entscheidungs-Management-API](../getting-started.md) beschriebenen Kopfzeilen die folgenden Kopfzeilen:

* `Content-Type`: `application/json`
* `x-request-id`: Eine eindeutige Zeichenfolge, mit der die Anfrage identifiziert wird.
* `x-sandbox-name`: Der Sandbox-Name.

## Starten eines Batch-Prozesses {#start-a-batch-process}

Um einen Workload zur Batch-Verarbeitung von Entscheidungen zu starten, stellen Sie eine POST-Anfrage an den Endpunkt `/workloads/decisions`.

>[!NOTE]
>
>Detaillierte Informationen zur Verarbeitungszeit von Batch-Aufträgen finden Sie in [diesem Abschnitt](../../batch-delivery.md).

**API-Format**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/dwm` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `xdm:activityId` | Die eindeutige Kennung der Entscheidung. |  |
| `xdm:dataSetId` | Der Ausgabedatensatz, in den Entscheidungsereignisse geschrieben werden können. | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | Dies ist ein optionales Feld, für das standardmäßig `false` festgelegt ist. Wenn `true` festgelegt wird, wird der Angebotsinhalt in die Entscheidungsereignisse des Datensatzes eingeschlossen. | `false` |
| `xdm:itemCount` | Dies ist ein optionales Feld, das die Anzahl der Elemente anzeigt, wie z. B. die für den Entscheidungsumfang angeforderten Optionen. Standardmäßig gibt die API eine Option pro Umfang zurück. Sie können jedoch durch Spezifizierung dieses Felds explizit zusätzliche Optionen anfordern. Pro Umfang können mindestens 1 und maximal 30 Optionen angefordert werden. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Die eindeutige Platzierungskennung. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | Ein Wrapper, der die `placementId` und die `activityId` enthält |  |
| `xdm:segmentIds` | Der Wert ist ein Array, das die eindeutige Kennung der Zielgruppe enthält. Es darf nur einen einzigen Wert enthalten. | `609028e4-e66c-4776-b0d9-c782887e2273` |

Weitere Informationen zu den wichtigsten Konzepten und Eigenschaften finden Sie in der [Dokumentation zum Entscheidungs-Management](../../get-started/starting-offer-decisioning.md).

**Antwort**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `@id` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Die Organisations-ID. | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungs-Workload-Anfrage erstellt wurde. | `1648078924834` |
| `ode:status` | Der Status des Workloads. | `ode:status: "QUEUED"` |

## Abrufen von Informationen zu einer Batch-Entscheidung {#retrieve-information-on-a-batch-decision}

Um Informationen zu einer bestimmten Entscheidung abzurufen, stellen Sie eine GET-Anfrage an den Endpunkt `/workloads/decisions` und geben Sie die entsprechende Workload-ID für Ihre Entscheidung an.

**API-Format**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Antwort**

```json
{
   "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `@id` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Die Organisations-ID | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungs-Workload-Anfrage erstellt wurde. | `1648076994405` |
| `ode:status` | Der Workload-Status ist zu Beginn „IN DIE WARTESCHLANGE GESTELLT“ und ändert sich dann in „VERARBEITUNG LÄUFT“, „AUFNAHME“, „ABGESCHLOSSEN“ oder „FEHLER“. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Wenn der Status „VERARBEITUNG LÄUFT“ oder „AUFNAHME“ lautet, werden weitere Details wie sparkJobId und batchID angezeigt. Wenn der Status „FEHLER“ lautet, werden die Fehlerdetails angezeigt. |  |

## Nächste Schritte {#next-steps}

Jetzt wissen Sie, wie Sie den Workload-Status überprüfen und Angebote über die [!DNL [!DNL Batch Decisioning]]-API bereitstellen können. Weitere Informationen finden Sie unter [Übersicht über das Entscheidungs-Management](../../get-started/starting-offer-decisioning.md).
