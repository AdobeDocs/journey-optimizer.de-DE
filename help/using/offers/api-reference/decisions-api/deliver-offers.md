---
title: Angebot bereitstellen
description: Decision Management ist eine Sammlung von Services- und UI-Programmen, mit denen Marketingexperten personalisierte Angebot-Erlebnisse für Endbenutzer erstellen und bereitstellen können. Dabei werden Geschäftslogik und Entscheidungsregeln verwendet.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 0%

---

# Bereitstellen von Angeboten mithilfe der Entscheidungs-API

Mit der Entscheidungsverwaltung können Sie personalisierte Angebot-Erlebnisse für Endbenutzer erstellen und bereitstellen, und zwar über Kanal und Anwendungen hinweg mithilfe von Geschäftslogik und Entscheidungsregeln. Ein Angebot ist eine Marketingmeldung, der möglicherweise Regeln zugeordnet sind, die angeben, wer zum Anzeigen des Angebots berechtigt ist.

Sie können Angebot erstellen und bereitstellen, indem Sie eine POST an die [!DNL Decisions]-API anfordern.

Dieses Lernprogramm erfordert ein Verständnis der APIs, insbesondere im Hinblick auf die Entscheidungsverwaltung. Weitere Informationen finden Sie im Handbuch [API-Entwickler für Entscheidungsverwaltung](../getting-started.md). Für dieses Lernprogramm müssen Sie außerdem über eine eindeutige Platzierungs-ID und einen Wert für die Entscheidungs-ID verfügen. Wenn Sie diese Werte nicht erhalten haben, finden Sie weitere Informationen in den Übungen zum [Erstellen einer Platzierung](../offers-api/placements/create.md) und [Erstellen einer Entscheidung](../activities-api/activities/create.md).

![](../../assets/do-not-localize/how-to-video.png) [Diese Funktion im Video entdecken](#video)

## Überschriften vom Typ &quot;Accept&quot;und &quot;Content&quot;

Die folgende Tabelle zeigt die gültigen Werte, die die Felder *Content-Type* und *Accept* im Anforderungsheader enthalten:

| Kopfzeilenname | Wert |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**API-Format**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parameter | Beschreibung | Beispiel |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Der Endpunktpfad für Repository-APIs. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | Der Container, in dem die Entscheidungen getroffen werden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anforderung**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
        },
        "xdm:responseFormat": {
            "xdm:includeContent": true,
            "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
            }
        }
      }'
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Dieses Objekt enthält die Platzierungs- und Entscheidungskennungen. |
| `xdm:propositionRequests.xdm:placementId` | Die eindeutige Platzierungskennung. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Die eindeutige Entscheidungskennung. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Die Anzahl der zurückzugebenden Angebot. Die Höchstzahl ist 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Dieses Objekt enthält Informationen über das Profil, für das die Entscheidung angefordert wird. Bei einer API-Anforderung enthält diese ein Profil. |
| `xdm:profiles.xdm:identityMap` | Dieses Objekt enthält eine Reihe von Endbenutzer-IDs, die auf dem Identitätscode des Namensraums basieren. Die Identitätskarte kann mehr als eine Identität jedes Namensraums enthalten. Weitere Informationen zu Namensräumen finden Sie unter [Übersicht über Identitäts-Namensraum](https://docs.adobe.com/content/help/en/experience-platform/identity/namespaces.html). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | Die vom Client erzeugte ID, mit der eine Profil-Entscheidungsanforderung eindeutig identifiziert werden kann. Diese ID wird in der Antwort widergespiegelt und hat keinen Einfluss auf das Ergebnis der Entscheidung. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Dieses Objekt dient der Steuerungsstruktur der Deduplizierungsregeln. Es besteht aus einer Reihe von Flags, die angeben, ob dieselbe Option für eine bestimmte Dimension vorgeschlagen werden kann. Eine auf &quot;true&quot;eingestellte Kennzeichnung bedeutet, dass Duplikat zulässig sind und nicht über die durch die Kennzeichnung angegebene Kategorie entfernt werden sollten. Ein auf &quot;false&quot;eingestelltes Flag bedeutet, dass die Entscheidungs-Engine nicht dieselbe Aussage über die Dimension hinweg treffen und stattdessen die nächste beste Option für eine der Unterentscheidungen auswählen sollte. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Bei der Einstellung &quot;true&quot;wird möglicherweise dieselbe Option mehreren Entscheidungen zugewiesen. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Bei Festlegung auf &quot;true&quot;wird möglicherweise dieselbe Option mehreren Platzierungen zugewiesen. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Gibt die Richtlinie zum Zusammenführen an, nach der die vom Profil-Zugriffsdienst zurückgegebenen Daten verwaltet werden. Wenn in der Anforderung keiner angegeben ist, wird kein Profil-Zugriffsdienst von der Entscheidungsverwaltung weitergeleitet, andernfalls wird die vom Aufrufer angegebene ID übergeben. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Eine Reihe von Flags, die den Antwortinhalt formatieren. |
| `xdm:responseFormat.xdm:includeContent` | Ein boolescher Wert, der, wenn er auf `true` eingestellt ist, Inhalte für die Antwort enthält. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Ein Objekt, mit dem festgelegt wird, welche zusätzlichen Metadaten zurückgegeben werden. Wenn diese Eigenschaft nicht enthalten ist, werden standardmäßig `xdm:id` und `repo:etag` zurückgegeben. | `name` |
| `xdm:responseFormat.xdm:activity` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:activity` zurückgegeben werden. | `name` |
| `xdm:responseFormat.xdm:option` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:option` zurückgegeben werden. | `name`,  `characteristics` |
| `xdm:responseFormat.xdm:placement` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:placement` zurückgegeben werden. | `name`,  `channel`,  `componentType` |

**Reaktion**

Eine erfolgreiche Antwort gibt Informationen zu Ihrem Vorschlag zurück, einschließlich der eindeutigen `xdm:propositionId`.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Eigenschaft | Beschreibung | Beispiel |
| -------- | ----------- | ------- |
| `xdm:propositionId` | Der eindeutige Bezeichner für die mit einem XDM-DecisionEvent verknüpfte Propositionentität. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Dieses Objekt enthält einen einzigen Entscheidungsvorschlag. Für die Entscheidung können mehrere Optionen zurückgegeben werden. Wenn keine Optionen gefunden werden, wird das Fallback-Angebot der Entscheidung zurückgegeben. Einzelne Entscheidungsvorschläge enthalten immer entweder eine `options`-Eigenschaft oder eine `fallback`-Eigenschaft. Wenn vorhanden, kann die `options`-Eigenschaft nicht leer sein. |
| `xdm:propositions.xdm:activity` | Dieses Objekt enthält die eindeutige Kennung für eine Entscheidung. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Dieses Objekt enthält den eindeutigen Bezeichner für die Platzierung eines Angebots. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Dieses Objekt enthält eine einzige Option einschließlich der eindeutigen Kennung. Falls vorhanden, kann dieses Objekt nicht leer sein. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definiert den Typ der Komponente. `@type` fungiert als Verarbeitungsvertrag für den Kunden. Wenn das Erlebnis zusammengestellt wird, sucht der Komponist nach den Komponenten, die einen bestimmten Typ aufweisen. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Das Format des Antwortinhalts. | Antwortinhalte können sein: `text`, `html block` oder `image link` |
| `xdm:score` | Das Ergebnis für eine Option, das aufgrund einer Rangfunktion berechnet wird, die der Option oder der Entscheidung zugeordnet ist. Dieses Feld wird von der API zurückgegeben, wenn eine Rangfunktion an der Ermittlung des Ergebnisses eines Angebots während der Rangansicht beteiligt ist. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Dieses Objekt enthält ein einzelnes Ausweichcookie-Angebot, einschließlich der eindeutigen Kennung. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zur Anzeige oder zum Betrieb der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen, z. B. die Liste von [Internet Media Types](http://www.iana.org/assignments/media-types/), die Computermedienformate definiert. | `"dc:format": "image/png"` oder  `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Eine optionale URL zum Lesen des Assets über einen Content Versand-Netzwerk- oder Dienstendpunkt. Diese URL wird verwendet, um von einem Benutzeragent aus auf das Asset öffentlich zuzugreifen. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Antwortmeldung zur Entscheidung erstellt wurde. Dies wird als Epochenzeit dargestellt. | `"ode:createDate": 1566497582038` |

## Lernvideo {#video}

Das folgende Video soll Ihnen dabei helfen, die Komponenten von Decision Management besser zu verstehen.

>[!NOTE]
>
>Dieses Video bezieht sich auf den auf Adobe Experience Platform aufbauenden Offer decisioning-Anwendungsdienst. Sie enthält jedoch allgemeine Leitlinien für die Verwendung von Angebot im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Nächste Schritte

Durch Befolgen dieses API-Handbuchs haben Sie Angebot mit der API [!DNL Decisions] erstellt und bereitgestellt. Weitere Informationen finden Sie unter [Übersicht über die Entscheidungsverwaltung](../../../offers/get-started/starting-offer-decisioning.md).
