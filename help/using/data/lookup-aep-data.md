---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Adobe Experience Platform-Daten
description: Erfahren Sie, wie Sie Adobe Experience Platform-Datensätze in  [!DNL Journey Optimizer] -Funktionen zur Entscheidungsfindung und Personalisierung verwenden.
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor
mini-toc-levels: 1
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 42f231a9b0b34a63d1601dcae653462f6321caed
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 17%

---

# Verwenden von Adobe Experience Platform-Daten {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Für Lookup aktivieren"
>abstract="Für Lookup aktivieren"

>[!AVAILABILITY]
>
>Diese Funktion steht derzeit allen Kunden als eingeschränkte Verfügbarkeitsversion zur Verfügung.

Mit Journey Optimizer können Sie Daten aus Adobe Experience Platform-Daten mit Personalisierungs- und Entscheidungsfunktionen nutzen. Dazu müssen datensatzbasierte Datensätze, die für die Lookup-Personalisierung erforderlich sind, zunächst für den Lookup-Service aktiviert werden, wie unten beschrieben.

## Wichtige Informationen

### Leitplanken und Richtlinien {#guidelines}

Bevor Sie beginnen, lesen Sie sich die folgenden Einschränkungen und Richtlinien durch:

* Datensätze, die für die Suche aktiviert sind, sollten keine personenbezogenen Daten enthalten.
* Datensätze, die für die Suche aktiviert und in der Personalisierung verwendet werden, sind nicht vor dem Löschen geschützt. Sie müssen den Überblick darüber behalten, welche Datensätze für die Personalisierung verwendet werden, um sicherzustellen, dass sie nicht gelöscht oder entfernt werden.
* Datensätze müssen mit einem Schema verknüpft sein, das NICHT vom Typ „Profil“ oder „Ereignis“ ist.
* Schemata müssen eine primäre Identität aufweisen. Für die Suche kann nur ein einziger Primärschlüssel verwendet werden.

### Berechtigung für den Suchdienst

| Funktionskomponente | Produktions-Sandbox-Limit | Anmerkungen |
| ------- | ------- | ------- |
| Datensätze für die Suche aktiviert | Max. 10 pro Organisation | Maximale Anzahl von Datensätzen, die jederzeit für die Suche konfiguriert werden können. Diese Begrenzung gilt für die Gesamtzahl der kombinierten Lookup-Datensätze in Produktions- und Entwicklungs-Sandboxes innerhalb der Kundeninstanz. |
| Anzahl der Datensätze | Bis zu 2 Millionen Datensätze pro Datensatz | Maximal zulässige Anzahl von Datensätzen in einem einzelnen Datensatz, berechnet als Gesamtanzahl aller Batches innerhalb dieses Datensatzes. |
| Datensatzgröße | Bis zu 2 KB pro Datensatz | Standardmäßig unterstützte maximale Datensatzgröße. |
| Datensatzgröße | Bis zu 4 GB | Maximale Größe eines einzelnen Datensatzes, nicht die kombinierte Größe aller Datensätze in einer Sandbox. Die Begrenzung der Datensatzanzahl und der Datensatzgröße sind unabhängige Leitplanken - beide müssen erfüllt sein. |
| Aktualisierungen der Datensatzfrequenz | Bis zu 5 Aktualisierungen pro Tag pro Datensatz | Maximal zulässige Häufigkeit von Aktualisierungsvorgängen für einen einzelnen Datensatz pro Tag. |

>[!NOTE]
>
>Wenn über die oben aufgeführten Leitplanken hinaus zusätzliche Volumes benötigt werden, wenden Sie sich an den Adobe-Support.

### Weitere Überlegungen zur Leistung

Die folgenden Empfehlungen geben Hinweise, wie Sie Verzögerungen bei der Zustellbarkeit vermeiden können:

| Hinweis | Empfohlenes Limit | Beschreibung |
| ------- | ------- | ------- |
| Attribute pro Suche | Bis zu 20 | Anzahl der pro Datensatz in einer einzigen Suchaktivität abgerufenen Datenfelder. |
| Aktivitäten nachschlagen | Bis zu 5 pro Journey | Jede Journey kann bis zu 5 verschiedene Lookup-Aktivitäten enthalten. Bei jeder Suche kann ein anderer Datensatz ausgewählt werden. |

## Aktivieren eines Datensatzes für Datensuchen {#enable}

Um Daten aus Ihrem Datensatz für die Personalisierung nutzen zu können, müssen Sie den Datensatz für die Suche aktivieren.

### Voraussetzungen {#prerequisites-enable}

Das mit Ihrem Datensatz verknüpfte Schema, das Sie für die Suche aktivieren möchten, muss vom Typ Datensatz sein. Das Schema darf NICHT der Profil- oder Ereignisklasse angehören.

+++Beispiel

![](assets/data-lookup-schema.png)

+++

Für das Schema muss eine primäre Identität definiert sein.

+++Beispiel

![](assets/data-lookup-primary.png)

+++

Wenn noch kein benutzerdefinierter Namespace definiert wurde, stellen Sie sicher, dass die Identität eine Nicht-Personen-Kennung ist.

+++Beispiel

![](assets/aep-data-namespace.png)

+++

### Aktivieren des Datensatzes für die Suche in der Oberfläche zur Datensatzverwaltung

Verwenden Sie in der Benutzeroberfläche zur Datensatzverwaltung den Umschalter, um den Datensatz für die Suche zu aktivieren.

![](assets/aep-data-enable.png)

>[!NOTE]
>
>Es wird empfohlen, den Datensatz NICHT auch für das Profil zu aktivieren, da dies zu einer Erhöhung der Profilreichhaltigkeit führen kann und nicht erforderlich ist, um die Suchen durchzuführen.

### API-Methode

Befolgen Sie die Anweisungen in [dieser Dokumentation](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) um Ihre Umgebung für das Senden von API-Befehlen zu konfigurieren.

#### Voraussetzungen

* Für das Entwicklerprojekt müssen die Adobe Journey Optimizer- und Adobe Experience Platform-APIs zum Projekt hinzugefügt werden.

  ![](assets/aep-data-api.png)

* Sie müssen über die Berechtigung zum Verwalten von Datensätzen als Teil Ihrer Rolle verfügen.

* Das Schema, auf dem der Datensatz basiert, muss eine primäre Identität enthalten, die als Lookup-Schlüssel fungieren kann.

#### API-Aufrufstruktur

```shell
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}" 
```

Dabei gilt:

* URL ist `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* Die Datensatz-ID ist der Datensatz, für den Sie aktivieren möchten.
* Aktion ist „Aktivieren“ ODER „Deaktivieren“.
* Das Zugriffstoken kann über die Entwicklerkonsole abgerufen werden.
* Der API-Schlüssel kann über die Entwicklerkonsole abgerufen werden.
* Die IMS-Organisations-ID ist Ihre Adobe-Organisation.
* Sandbox-Name ist der Name der Sandbox, in der sich der Datensatz befindet (d. h. Produktion, Entwicklung usw.).

>[!NOTE]
>
>Wenn beim Versuch, einen API-Aufruf zum Aktivieren von Datensätzen durchzuführen, der unten stehende Fehler auftritt, entfernen Sie die Adobe Journey Optimizer-APIs aus Ihrem Entwicklerkonsolen-Projekt und fügen Sie sie dann erneut hinzu:
>
>`"error_code": "403003",`
>`"message": "Api Key is invalid"`

## Datensatzüberwachung

Sobald ein Datensatz für die Suche aktiviert wurde, können Sie den Status der Aufnahme in den Such-Service überprüfen, indem Sie das Menü **[!UICONTROL Überwachung]** aufrufen und die Registerkarte **[!UICONTROL Journey Optimizer]** auswählen.

Diese Prozessanzeige hilft zu verstehen, wenn neue Datenstapel im Lookup-Service verfügbar sind.

![](assets/aep-data-monitoring.png)

<!--Ivan Mironchuk
Note - we have a bug here currently. Will need to update screenshot once the lookup service will accurately reflect the progress.-->

## Nächste Schritte

Nachdem ein Datensatz mithilfe eines API-Aufrufs für die Suche aktiviert wurde, können Sie die Daten mit [!DNL Journey Optimizer] Personalisierungs- und Entscheidungsfunktionen verwenden. Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Verwenden von Adobe Experience Platform-Daten für die Personalisierung](../personalization/aep-data-perso.md)
* [Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung](../experience-decisioning/aep-data-exd.md)
