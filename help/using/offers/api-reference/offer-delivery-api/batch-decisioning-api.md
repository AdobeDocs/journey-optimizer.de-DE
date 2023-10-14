---
title: Batch Decisioning-API
description: Erfahren Sie, wie Sie mit der Batch Decisioning-API innerhalb eines vordefinierten Entscheidungsumfangs die besten Angebote für Zielgruppenprofile auswählen können.
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 100%

---


# Unterbreiten von Angeboten mithilfe der [!DNL Batch Decisioning]-API {#deliver-offers-batch}

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

* **Die Anzahl der ausgeführten Batch-Vorgänge pro Datensatz**: Pro Datensatz können bis zu fünf Batch-Vorgänge gleichzeitig ausgeführt werden. Alle anderen Batch-Anfragen mit demselben Ausgabedatensatz werden der Warteschlange hinzugefügt. Ein in die Warteschlange gestellter Vorgang wird zur Verarbeitung aufgenommen, sobald der vorherige Vorgang abgeschlossen ist.
* **Frequenzlimitierung**: Ein Batch wird auf Basis eines Profil-Snapshots ausgeführt, der einmal täglich erfolgt. Die [!DNL Batch Decisioning]-API begrenzt die Häufigkeit und lädt Profile immer aus dem neuesten Snapshot.

## Erste Schritte {#getting-started}

Bevor Sie diese API verwenden, müssen Sie die folgenden Schritte ausführen.

### Entscheidungsvorbereitung {#prepare-decision}

Um eine oder mehrere Entscheidungen vorzubereiten, stellen Sie sicher, dass Sie einen Datensatz, eine Zielgruppe und eine Entscheidung erstellt haben. Diese Voraussetzungen werden in [diesem Abschnitt](../../batch-delivery.md) näher erläutert.

### API-Anforderungen {#api-requirements}

Alle [!DNL Batch Decisioning]-Anfragen erfordern zusätzlich zu den im [Entwicklerhandbuch zur Entscheidungs-Management-API](../getting-started.md) beschriebenen Kopfzeilen die folgenden Kopfzeilen:

* `Content-Type`: `application/json`
* `x-request-id`: Eine eindeutige Zeichenfolge, mit der die Anfrage identifiziert wird.
* `x-sandbox-name`: Der Sandbox-Name.
* `x-sandbox-id`: Die Sandbox-ID.

## Starten eines Batch-Prozesses {#start-a-batch-process}

Um einen Workload zur Batch-Verarbeitung von Entscheidungen zu starten, stellen Sie eine POST-Anfrage an den Endpunkt `/workloads/decisions`.

>[!NOTE]
>
>Detaillierte Informationen zur Verarbeitungszeit von Batch-Vorgängen finden Sie in [diesem Abschnitt](../../batch-delivery.md).

**API-Format**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
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
| `xdm:segmentIds` | Der Wert ist ein Array, das die eindeutige Kennung der Zielgruppe enthält. Es darf nur einen einzigen Wert enthalten. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | Der Ausgabedatensatz, in den Entscheidungsereignisse geschrieben werden können. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Ein Wrapper, der die `placementId` und die `activityId` enthält |  |
| `xdm:activityId` | Die eindeutige Kennung der Entscheidung. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Die eindeutige Platzierungskennung. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Dies ist ein optionales Feld, das die Anzahl der Elemente anzeigt, wie z. B. die für den Entscheidungsumfang angeforderten Optionen. Standardmäßig gibt die API eine Option pro Umfang zurück. Sie können jedoch durch Spezifizierung dieses Felds explizit zusätzliche Optionen anfordern. Pro Umfang können mindestens 1 und maximal 30 Optionen angefordert werden. | `1` |
| `xdm:includeContent` | Dies ist ein optionales Feld, für das standardmäßig `false` festgelegt ist. Wenn `true` festgelegt wird, wird der Angebotsinhalt in die Entscheidungsereignisse des Datensatzes eingeschlossen. | `false` |

Weitere Informationen zu den wichtigsten Konzepten und Eigenschaften finden Sie in der [Dokumentation zum Entscheidungs-Management](../../get-started/starting-offer-decisioning.md).

**Antwort**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `@id` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Die Organisations-ID. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Die Container-ID. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungs-Workload-Anfrage erstellt wurde. | `1648078924834` |
| `ode:status` | Der Status des Workloads. | `ode:status: "QUEUED"` |

## Abrufen von Informationen zu einer Batch-Entscheidung {#retrieve-information-on-a-batch-decision}

Um Informationen zu einer bestimmten Entscheidung abzurufen, stellen Sie eine GET-Anfrage an den Endpunkt `/workloads/decisions` und geben Sie die entsprechende Workload-ID für Ihre Entscheidung an.

**API-Format**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**Anfrage**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `@id` | Die vom Entscheidungs-Management generierte UUID, die eine einzelne Workload kennzeichnet. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Die Organisations-ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Die Container-ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungs-Workload-Anfrage erstellt wurde. | `1648076994405` |
| `ode:status` | Der Workload-Status ist zu Beginn „IN DIE WARTESCHLANGE GESTELLT“ und ändert sich dann in „VERARBEITUNG LÄUFT“, „AUFNAHME“, „ABGESCHLOSSEN“ oder „FEHLER“. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Wenn der Status „VERARBEITUNG LÄUFT“ oder „AUFNAHME“ lautet, werden weitere Details wie sparkJobId und batchID angezeigt. Wenn der Status „FEHLER“ lautet, werden die Fehlerdetails angezeigt. |  |

## Nächste Schritte {#next-steps}

Jetzt wissen Sie, wie Sie den Workload-Status überprüfen und Angebote über die [!DNL [!DNL Batch Decisioning]]-API bereitstellen können. Weitere Informationen finden Sie unter [Übersicht über das Entscheidungs-Management](../../get-started/starting-offer-decisioning.md).
