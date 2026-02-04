---
title: Decisioning-Migrations-API
description: Erfahren Sie, wie Sie mit der Decisioning Migration Service-API Entscheidungs-Management-Objekte zwischen Sandboxes mit automatisierter Unterstützung der Abhängigkeitsauflösung und Rollback migrieren können.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 5%

---


# Decisioning-Migrations-API {#decisioning-migration-api}

Mit der Decisioning Migration Service-API können Sie Entscheidungs-Management-Objekte von einer Sandbox in eine andere migrieren. Der Migrationsprozess wird als asynchrone Workflows ausgeführt, die Funktionen zur Abhängigkeitsanalyse, Ausführung und optionales Rollback enthalten.

Mit dieser API können Sie Ihre Entscheidungs-Inhalte nahtlos zwischen Umgebungen (z. B. von der Entwicklung zum Staging oder von der Staging- zur Produktionsumgebung) wechseln, während die Datenintegrität und -beziehungen erhalten bleiben.

Weitere Informationen zu den Vorteilen und Funktionen von Decisioning im Vergleich zum Entscheidungs-Management finden Sie unter [Vorteile der Migration zu Decisioning](migrate-to-decisioning.md).

## Funktionen {#capabilities}

Die Decisioning Migration Service-API bietet die folgenden Funktionen:

* **Abhängigkeitsanalyse** - Identifizieren Sie alle erforderlichen Abhängigkeiten zwischen Quell- und Ziel-Sandboxes, einschließlich Attributen, Segmenten und Datensatzanforderungen.
* **Flexibler Migrationsbereich** - Führen Sie Migrationen je nach Bedarf auf Sandbox-, Angebots- oder Entscheidungsebene aus.
* **Rollback-Unterstützung**: Setzt eine abgeschlossene Migration zurück, wenn bei der Validierung Probleme auftreten.

## Voraussetzungen {#prerequisites}

### Erforderliche Berechtigungen {#permissions}

Um die Migrations-API verwenden zu können, benötigen Sie entsprechende Berechtigungen in der Quell- und Ziel-Sandbox:

**Source Sandbox** - Lesezugriff auf Entscheidungs-Management-Objekte

**Target-Sandbox** - Zugriff auf Decisioning-Objekte erstellen und bearbeiten

Zu den typischen Berechtigungen gehören:

* Entscheidungen verwalten/anzeigen
* Entscheidungen verwalten/anzeigen
* Verwalten von Angeboten
* Rangfolgestrategien verwalten
* Verwalten von Kampagnen (bei Migration von kampagnenbezogenen Artefakten)
* Datenströme verwalten/anzeigen (beim Erstellen eines Datenstroms)
* Verwalten/Anzeigen von Schemata

>[!NOTE]
>
>Erfahren Sie in ([&#x200B; Abschnitt), wie Sie &#x200B;](gs-experience-decisioning.md#steps) zuweisen. Eine vollständige Liste der Berechtigungen finden Sie auf der Seite [Integrierte Berechtigungen](../administration/ootb-permissions.md#ootb-permissions) .

### Vorbereiten der Ziel-Sandbox {#target-sandbox-preparation}

Bevor Sie eine Migration ausführen, stellen Sie sicher, dass Ihre Ziel-Sandbox ordnungsgemäß konfiguriert ist:

* **Attribute** - Überprüfen Sie, ob die erforderlichen Profilattribute und Kontextattribute in der Ziel-Sandbox vorhanden sind, oder bereiten Sie Zuordnungen für sie vor.
* **Segmente** - Stellen Sie sicher, dass die erforderlichen Segmente in der Ziel-Sandbox vorhanden sind, oder planen Sie ihre Zuordnung mithilfe des Namespace und der ID.
* **Datensatz** - Identifizieren Sie einen Datensatznamen, der für die Migration verwendet werden soll (`dependency.datasetName`).
* **Datenstrom** - Festlegen, ob bei der Migration ein Datenstrom erstellt werden soll (`createDataStream`).

Weitere Informationen zur Sandbox-Verwaltung finden Sie unter [&#x200B; und Zuweisen von Sandboxes](../administration/sandboxes.md).

## API-Grundlagen {#api-basics}

### Basis-URLs {#base-urls}

Verwenden Sie je nach Umgebung die folgenden Basis-URLs:

* **Produktion**: `https://platform.adobe.io`
* **STAGING**: `https://platform-stage.adobe.io`

### Authentifizierung {#authentication}

Alle API-Anfragen erfordern die folgenden Kopfzeilen:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

Detaillierte Anweisungen zum Einrichten der Authentifizierung finden Sie im [Authentifizierungshandbuch für Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Workflow-Modell {#workflow-model}

Jeder API-Aufruf erstellt oder ruft eine Workflow-Ressource ab. Workflows sind asynchrone Vorgänge, die den Fortschritt und die Ergebnisse von Migrationsaufgaben verfolgen.

Ein Workflow verfügt über die folgenden Eigenschaften:

* `id` - Eindeutige Workflow-Kennung (UUID)
* `status` - Aktueller Workflow-Status: `New`, `Running`, `Completed`, `Failed` oder `Cancelled`
* `result` - Workflow-Ausgabe nach Abschluss (einschließlich Migrationsergebnissen und Warnungen)
* `errors` - Details zu strukturierten Fehlern bei Fehlschlägen
* `_etag` - Versionskennung, die für Löschvorgänge verwendet wird (nur Service-Benutzer)
* `_links.self` - Workflow-URL zum Abrufen des Status

## Migrations-Workflow {#migration-workflow}

Der Migrationsprozess besteht aus zwei Hauptschritten: Analysieren von Abhängigkeiten und Ausführen der Migration. Führen Sie diese Schritte aus, um eine erfolgreiche Migration sicherzustellen.

### Schritt 1: Abhängigkeiten analysieren {#analyze-dependencies}

Verwenden Sie vor der Migration den Abhängigkeits-Workflow, um zu ermitteln, was in Ihrer Ziel-Sandbox vom Entscheidungs-Management zum Entscheidungs-Management zugeordnet werden muss. Diese Analyse hilft Ihnen, die Beziehungen zwischen Objekten zu verstehen und die erforderlichen Zuordnungen vorzubereiten.

#### Erstellen eines Abhängigkeits-Workflows {#create-dependency-workflow}

Verwenden Sie den folgenden API-Aufruf, um einen Workflow zur Abhängigkeitsanalyse zu erstellen.

**API-Format**

```http
POST /migration/service/dependency
```

**Abhängigkeit auf Sandbox-Ebene (zuerst empfohlen)**

Beginnen Sie mit einer Analyse auf Sandbox-Ebene, um einen vollständigen Überblick über alle Abhängigkeiten zu erhalten:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Abhängigkeit auf Angebotsebene**

Um die Abhängigkeiten nur für bestimmte Angebote zu analysieren, legen Sie `requestLevel: "offer"` fest und stellen Sie ein `offersList`-Array mit den Angebots-IDs bereit, die Sie analysieren möchten.

**Abhängigkeit auf Entscheidungsebene**

Um die Abhängigkeiten nur für bestimmte Entscheidungen zu analysieren, legen Sie `requestLevel: "decision"` fest und stellen Sie ein `decisionsList`-Array mit den Entscheidungs-IDs bereit, die Sie analysieren möchten.

#### Überprüfen des Workflow-Status der Abhängigkeit {#poll-dependency-status}

Fragen Sie den Abhängigkeits-Workflow ab, um zu überprüfen, wann die Analyse abgeschlossen ist.

**API-Format**

```http
GET /migration/service/dependency/{id}
```

**Anfrage**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

Wenn das `status` Feld `Completed` anzeigt, ist die Abhängigkeitsanalyse bereit. Verwenden Sie die Workflow-Ausgabe, um Ihre Zuordnungen von Migrationsabhängigkeiten zu erstellen:

* **profileAttributeDependency** - Ordnet Quellprofilattribute Zielprofilattributen zu
* **contextAttributeDependency** - Ordnet Quellkontextattribute Zielkontextattributen zu
* **segmentsDependency** - Ordnet Quellsegmentschlüssel Zielsegmentkennungen (`{segmentNamespace, segmentId}`) zu
* **datasetName** - Gibt den Zieldatensatznamen für die Migration an

### Schritt 2: Migration ausführen {#execute-migration}

Nachdem Sie die Abhängigkeiten analysiert und die Zuordnungen vorbereitet haben, können Sie die Migration ausführen.

#### Migrationsprozess erstellen {#create-migration-workflow}

Verwenden Sie die Abhängigkeitszuordnungen aus Schritt 1, um Ihre Migration zu konfigurieren und auszuführen.

**API-Format**

```http
POST /migration/service/migrations
```

**Migration auf Sandbox-Ebene**

So migrieren Sie alle Decisioning-Objekte von einer Sandbox in eine andere:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**Migration auf Angebotsebene**

Um nur bestimmte Angebote zu migrieren, verwenden Sie `requestLevel: "offer"` und fügen Sie ein `offersList`-Array hinzu:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migration auf Entscheidungsebene**

Um nur bestimmte Entscheidungen zu migrieren, verwenden Sie `requestLevel: "decision"` und fügen Sie ein `decisionsList`-Array hinzu:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Überwachen des Migrationsstatus {#poll-migration-status}

Abfrage des Migrations-Workflows zur Verfolgung des Fortschritts.

**API-Format**

```http
GET /migration/service/migrations/{id}
```

**Anfrage**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**Migrationsergebnisse**

Wenn im Feld `status` `Completed` angezeigt wird, war die Migration erfolgreich. Die Workflow-`result` umfasst:
* Zuordnungen von migrierten Objekten
* Etwaige Warnungen während der Migration

Wenn das `status` Feld `Failed` anzeigt, überprüfen Sie das `errors[]` Array und `result.error` Feld für Details zu den Problemen.

## Validieren der Migration {#validate-migration}

Überprüfen Sie nach erfolgreichem Abschluss der Migration, ob alle Objekte korrekt migriert wurden.

### Validierungs-Checkliste {#validation-checklist}

1. **Segmente** - Überprüfen Sie, ob alle referenzierten Segmente in der Ziel-Sandbox entsprechend Ihren Zuordnungen korrekt aufgelöst werden.
2. **Attribute** - Vergewissern Sie sich, dass alle Profilattribute und Kontextattribute in der Ziel-Sandbox vorhanden sind und korrekt zugeordnet werden.
3. **Entscheidungsobjekte** - Überprüfen Sie migrierte Objekte in der Benutzeroberfläche von Journey Optimizer:
   * Angebote (Entscheidungselemente)
   * Eignungsregeln
   * Rangfolgenformeln
   * Auswahlstrategien
   * Entscheidungsrichtlinien
4. **Datenstromtests** - Wenn ein Datenstrom erstellt wurde, testen Sie die Laufzeitbereitstellung mithilfe der Edge Interact-API.

### Beispiel {#test-runtime-delivery}

Wenn bei der Migration ein Datenstrom erstellt wurde, können Sie die Angebotsbereitstellung anhand des folgenden Beispiels testen:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Rollback für eine Migration {#rollback}

Wenn Sie während der Validierung Probleme feststellen, können Sie eine abgeschlossene Migration zurücksetzen, um den vorherigen Status der Ziel-Sandbox wiederherzustellen.

### Erstellen eines Rollback-Workflows {#create-rollback-workflow}

Starten Sie ein Rollback, indem Sie einen Rollback-Workflow erstellen, der auf die Migration verweist, die Sie zurücksetzen möchten.

**API-Format**

```http
POST /migration/service/rollbacks/{migrationWorkflowId}
```

Ersetzen Sie `{migrationWorkflowId}` durch die ID des Migrations-Workflows, den Sie zurücksetzen möchten.

**Anfrage**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### Überwachen des Rollback-Status {#poll-rollback-status}

Abruf des Rollback-Workflows zur Verfolgung des Fortschritts.

**API-Format**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**Anfrage**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## Gleichzeitige Workflows handhaben {#handle-concurrency}

Mit der Migrations-API kann jeweils nur ein Workflow pro Organisation ausgeführt werden. Wenn Sie versuchen, einen neuen Workflow zu erstellen, während ein anderer ausgeführt wird, erhalten Sie eine **409 Conflict**-Fehlerantwort („Ein Workflow ist bereits in Bearbeitung…„).

Warten Sie in diesem Fall, bis der laufende Workflow abgeschlossen ist, oder rufen Sie die Workflow-ID ab und fragen Sie ihren Status ab. Sobald der aktuelle Workflow abgeschlossen ist, können Sie einen neuen erstellen.

## Entitätszuordnungsreferenz {#entity-mapping}

Bei der Migration vom Entscheidungs-Management zum Entscheidungs-Management werden Entitäten wie folgt zugeordnet:

| Entscheidungs-Management | Entscheidungsfindung |
|-------------------|-------------|
| Angebot | Entscheidungselement |
| Angebotssammlung | Artikelsammlung |
| Eignungsregel | Eignungsregel |
| Rangfolgenformel | Rangfolgenformel |
| Entscheidung | Auswahlstrategie + Entscheidungsrichtlinie |
| Campaign | Campaign *(nur grundlegende Inhalte)* |
| Platzierung | Oberfläche + Kanalkonfiguration |
| Tag | Einheitliches Tag |

## Workflow-Bereinigung {#cleanup}

Workflow-Ressourcen können nur von Service-Benutzern gelöscht werden. Löschvorgänge erfordern eine `If-Match` mit dem `_etag` des Workflows.

**Verfügbare Löschvorgänge:**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>Das Löschen von Workflows ist nur für Dienstkonten mit entsprechenden Berechtigungen verfügbar. Wenden Sie sich an Ihren Systemadministrator, wenn Sie eine Workflow-Ressource löschen müssen.

## Verwandte Themen {#related-topics}

* [Migration vom Entscheidungs-Management zum Decisioning](migrate-to-decisioning.md) - Verstehen Sie die Vorteile und Möglichkeiten der Migration zu Decisioning
* [Erste Schritte mit der Entscheidungsfindung](gs-experience-decisioning.md)
* [Leitplanken und Einschränkungen bei Entscheidungen](decisioning-guardrails.md)
* [Erste Schritte mit Decisioning-APIs](api-reference/getting-started.md)
