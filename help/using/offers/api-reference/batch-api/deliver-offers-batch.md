---
title: Batch Decisioning-API
description: Erfahren Sie, wie Sie mit der Batch Decisioning-API die besten Angebote für segmentierte Profile innerhalb eines vordefinierten Entscheidungsbereichs auswählen können.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 3c40f3b6f76272db32b929a886a0cd63f797a842
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 8%

---


# Angebote mithilfe der [!DNL Batch Decisioning] API {#deliver-offers-batch}

Die [!DNL Batch Decisioning] Mit der API können Unternehmen die offer decisioning-Funktionalität für alle Profile in einem Segment in einem einzigen Aufruf verwenden. Der Angebotsinhalt für jedes Profil im Segment wird in einem Adobe Experience Platform-Datensatz platziert, wo er für benutzerdefinierte Batch-Workflows verfügbar ist.

Mit dem [!DNL Batch Decisioning] API können Sie einen Datensatz mit den besten Angeboten für alle Profile in einem Adobe Experience Platform-Segment für Entscheidungsbereiche ausfüllen. Eine Organisation kann beispielsweise [!DNL Batch Decisioning] , damit sie Angebote an einen Anbieter senden können. Diese Angebote werden dann als Inhalt verwendet, der für die Batch-Nachrichtenübermittlung an dasselbe Benutzersegment gesendet wird.

Dazu würde die Organisation:

* Führen Sie die [!DNL Batch Decisioning] API, die zwei Anfragen enthält:

   1. A **Batch-POST-Anfrage** , um eine Arbeitslast für die Stapelverarbeitung der Angebotsauswahl zu starten.

   2. A **Batch-GET-Anfrage** , um den Status der Batch-Arbeitslast zu erhalten.

* Exportieren Sie den Datensatz in die Nachrichtenbereitstellungs-API.

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

## Erste Schritte {#getting-started}

Bevor Sie diese API verwenden, stellen Sie sicher, dass Sie die folgenden erforderlichen Schritte ausführen.

### Entscheidungsvorbereitung {#prepare-decision}

Gehen Sie wie folgt vor, um eine oder mehrere Entscheidungen vorzubereiten:

* Um das Entscheidungsergebnis zu exportieren, erstellen Sie einen Datensatz mit dem Schema &quot;ODE DecisionEvents&quot;.

* Erstellen Sie ein Platform-Segment, das ausgewertet und dann aktualisiert werden soll. Siehe Abschnitt [Segmentierungsdokumentation](http://www.adobe.com/go/segmentation-overview-en) , um mehr darüber zu erfahren, wie Sie die Bewertung der Segmentmitgliedschaft aktualisieren.

* Erstellen Sie in Adobe Journey Optimizer eine Entscheidung (die einen Entscheidungsbereich umfasst, der aus einer Entscheidungs-ID und einer Platzierungs-ID besteht). Siehe Abschnitt [Abschnitt zur Definition von Entscheidungsbereichen](../../offer-activities/create-offer-activities.md) des Leitfadens zum Erstellen von Entscheidungen , um mehr zu erfahren.

### API-Anforderungen {#api-requirements}

Alle [!DNL Batch Decisioning] -Anfragen erfordern zusätzlich zu den in der Variablen [Entwicklerhandbuch zur Entscheidungs-API](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`: Eine eindeutige Zeichenfolge, die die Anforderung angibt.
* `x-sandbox-name`: Der Sandbox-Name.
* `x-sandbox-id`: Die Sandbox-ID.

## Batch-Prozess starten {#start-a-batch-process}

Um eine Arbeitslast für Batch-Prozessentscheidungen zu starten, stellen Sie eine POST-Anfrage an die `/workloads/decisions` -Endpunkt.

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
| `xdm:segmentIds` | Der Wert ist ein Array, das die eindeutige Kennung des Segments enthält. Sie darf nur einen Wert enthalten. | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | Der Ausgabedatensatz, in den Entscheidungsereignisse geschrieben werden können. | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | Ein Wrapper, der die `placementId` und `activityId` |  |
| `xdm:activityId` | Die eindeutige Kennung der Entscheidung. | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | Die eindeutige Platzierungskennung. | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | Dies ist ein optionales Feld, das die Anzahl der Elemente anzeigt, wie z. B. die für den Entscheidungsbereich angeforderten Optionen. Standardmäßig gibt die API eine Option pro Perimeter zurück. Sie können jedoch durch Angabe dieses Felds explizit nach weiteren Optionen fragen. Pro Bereich können mindestens 1 und maximal 30 Optionen angefordert werden. | `1` |
| `xdm:includeContent` | Dies ist ein optionales Feld und ist `false` Standardmäßig. Wenn `true`, wird der Angebotsinhalt in die Entscheidungsereignisse des Datensatzes aufgenommen. | `false` |

Siehe Abschnitt [Dokumentation zur Entscheidungsverwaltung](../../get-started/starting-offer-decisioning.md) für einen Überblick über die wichtigsten Konzepte und Eigenschaften.

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
| `@id` | Die von Offer Decisioning generierte UUID, die eine einzelne Arbeitslast identifiziert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Die ID für Ihre IMS-Organisation. | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Ihre Container-ID. | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidung-Workload-Anfrage erstellt wurde. | `1648078924834` |
| `ode:status` | Der Status der Arbeitslast. | `ode:status: "QUEUED"` |

## Abrufen von Informationen zu einer Batch-Entscheidung {#retrieve-information-on-a-batch-decision}

Um Informationen zu einer bestimmten Entscheidung abzurufen, stellen Sie eine GET-Anfrage an die `/workloads/decisions` -Endpunkt hinzugefügt, während Sie den entsprechenden Arbeitslast-ID-Wert für Ihre Entscheidung angeben.

**API-Format**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | Die von Offer Decisioning generierte UUID, die eine einzelne Arbeitslast identifiziert. | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

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
| `@id` | Die von Offer Decisioning generierte UUID, die eine einzelne Arbeitslast identifiziert. | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | Kennung der IMS-Organisation | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | Die Container-ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungsarbeitslastanforderung erstellt wurde. | `1648076994405` |
| `ode:status` | Der Status der Arbeitslast beginnt mit &quot;QUEUED&quot; und ändert sich in &quot;PROCESSING&quot;, &quot;INGESTING&quot;, &quot;COMPLETED&quot; oder &quot;ERROR&quot;. | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | Hier werden weitere Details wie sparkJobId und batchID angezeigt, wenn der Status &quot;PROCESSING&quot;oder &quot;INGESTING&quot;lautet. Er zeigt die Fehlerdetails an, wenn der Status &quot;FEHLER&quot;lautet. |  |

## Dienstebenen {#service-levels}

Die End-to-End-Zeit für jede Batch-Entscheidung ist die Dauer von dem Zeitpunkt, zu dem die Arbeitslast erstellt wird, bis zu dem Zeitpunkt, zu dem das Entscheidungsergebnis im Ausgabedatensatz verfügbar ist. Die Segmentgröße in der Payload der POST-Anfrage ist der Hauptfaktor, der sich auf die End-to-End-Batch-Entscheidungszeit auswirkt.  Im Folgenden finden Sie einige Beobachtungen zu verschiedenen Segmentgrößen:

| Segmentgröße | End-to-End-Verarbeitungszeit |
|--------------|----------------------------|
| 10.000 Profile oder weniger | 6 Minuten |
| 1 Million Profile oder weniger | 10 Minuten |
| 15 Millionen Profile oder weniger | 75 Minuten |

## Einschränkungen {#limitations}

Bei Verwendung von [!DNL Batch Decisioning] Beachten Sie die folgenden Einschränkungen:

* **Einzelner Batch-Auftrag pro Datensatz**: Derzeit kann pro Datensatz immer nur ein einzelner Batch-Auftrag ausgeführt werden. Alle anderen Anfragen mit demselben Ausgabedatensatz antworten mit HTTP 429 (Zu viele Anforderungen), bevor die vorherige Anfrage abgeschlossen wird.
* **Frequenzlimitierung**: Ein Batch wird aus dem Profil-Snapshot ausgeführt, der einmal täglich erfolgt. Die [!DNL Batch Decisioning] Die API begrenzt die Häufigkeit und lädt Profile immer aus der neuesten Momentaufnahme.

## Nächste Schritte {#next-steps}

In diesem API-Handbuch haben Sie nach dem Arbeitsbelastungsstatus gesucht und Angebote mithilfe des [!DNL] bereitgestellt. [!DNL Batch Decisioning]] -API. Weitere Informationen finden Sie unter [Übersicht über das Entscheidungs-Management](../../get-started/starting-offer-decisioning.md).
