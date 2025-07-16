---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Adobe Experience Platform-Daten (Beta)
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in  [!DNL Journey Optimizer] -Funktionen zur Entscheidungsfindung und Personalisierung verwenden.
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 416f82a932f0b484d8463ff24090a7061461822f
workflow-type: ht
source-wordcount: '435'
ht-degree: 100%

---

# Verwenden von Adobe Experience Platform-Daten {#aep-data}

>[!AVAILABILITY]
>
>Diese Funktion steht derzeit allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung.
>
>Um diese Funktion nutzen zu können, müssen Sie zunächst die Bedingungen für Beta-Versionen für Ihre Organisation akzeptieren.

Mit Journey Optimizer können Sie Daten aus Adobe Experience Platform in [!DNL Journey Optimizer] nutzen. Dazu müssen Datensätze, die für die Personalisierung der Suche erforderlich sind, zunächst wie nachfolgend beschrieben über einen API-Aufruf aktiviert werden. Anschließend können Sie deren Daten mit [!DNL Journey Optimizer]-Funktionen zur Personalisierung und Entscheidungsfindung verwenden.

## Einschränkungen und Richtlinien der Beta-Version {#guidelines}

Bevor Sie beginnen, lesen Sie sich die folgenden Einschränkungen und Richtlinien durch:

* Die **Datensatzgröße** ist für Produktionsdatensätze auf 5 GB und für Entwicklungs-Sandbox-Datensätze auf 1 GB beschränkt.
* **Es können jeweils maximal 50 Datensätze** pro Organisation für die Suche aktiviert werden.
* Die **Anzahl der Einträge** ist in Produktionsdatensätzen auf 5 Millionen und in Entwicklungs-Sandbox-Datensätzen auf 1 Million beschränkt.
* **Data Usage Labelling and Enforcement** wird derzeit nicht für Datensätze erzwungen, die für die Suche aktiviert sind.
* **Datensätze, die für die Suche aktiviert sind und bei der Personalisierung verwendet werden, sind nicht vor Löschvorägngen geschützt**. Sie müssen den Überblick darüber behalten, welche Datensätze für die Personalisierung verwendet werden, um sicherzustellen, dass sie nicht gelöscht oder entfernt werden.

## Aktivieren eines Datensatzes für Datensuchen {#enable}

Um Daten aus Ihrem Datensatz für die Personalisierung nutzen zu können, müssen Sie einen API-Aufruf verwenden, um seinen Status abzurufen und den Suchdienst zu aktivieren.

### Voraussetzungen {#prerequisites-enable}

* Befolgen Sie die Anweisungen in [dieser Dokumentation](https://developer.adobe.com/journey-optimizer-apis/references/authentication/), um Ihre Umgebung für das Senden von API-Befehlen zu konfigurieren.
* Für das Entwicklerprojekt müssen die Adobe Journey Optimizer- und Adobe Experience Platform-APIs zum Projekt hinzugefügt werden.

  ![](assets/aep-data-api.png)

* Sie müssen über die Berechtigung zum Verwalten von Datensätzen als Teil Ihrer Rolle verfügen.
* Das Schema, auf dem der Datensatz basiert, muss eine **primäre Identität** enthalten, die als Suchschlüssel fungieren kann.

### API-Aufrufstruktur {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Dabei gilt:

* Die **URL** lautet `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **Dataset ID** ist der Datensatz, den Sie aktivieren möchten.
* **Action** ist „Aktivieren“ ODER „Deaktivieren“.
* **Access token** kann aus der Developer Console abgerufen werden.
* **API Key** kann aus der Developer Console abgerufen werden.
* **IMS Org ID** ist Ihre Adobe-Organisation.
* **Sandbox Name** ist der Name der Sandbox, in der sich der Datensatz befindet (d. h. prod, dev usw.).

>[!NOTE]
>
>Wenn beim Durchführen eines API-Aufrufs zum Aktivieren von Datensätzen der folgende Fehler auftritt, versuchen Sie, die Adobe Journey Optimizer-APIs aus Ihrem Developer Console-Projekt zu entfernen und sie dann erneut hinzuzufügen.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

Nachdem ein Datensatz mithilfe eines API-Aufrufs für die Suche aktiviert wurde, können Sie seine Daten mit [!DNL Journey Optimizer]-Funktionen zur Personalisierung und Entscheidungsfindung verwenden.

* [Verwenden von Adobe Experience Platform-Daten für die Personalisierung](../personalization/aep-data-perso.md)
* [Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung](../experience-decisioning/aep-data-exd.md)
