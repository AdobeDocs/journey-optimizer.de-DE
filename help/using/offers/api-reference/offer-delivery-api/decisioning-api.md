---
title: Angebote unterbreiten
description: Decision Management ist eine Sammlung von Diensten und Benutzeroberflächenprogrammen, mit denen Marketing-Experten personalisierte Angebotserlebnisse für Endbenutzer erstellen und über Kanäle und Anwendungen hinweg bereitstellen können. Dabei werden Geschäftslogik und Entscheidungsregeln verwendet.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Angebote mithilfe der Decisioning API bereitstellen {#decisioning-api}

Mit der Entscheidungsverwaltung können Sie personalisierte Angebotserlebnisse für Endbenutzer über Kanäle und Anwendungen hinweg mithilfe von Business-Logik und Entscheidungsregeln erstellen und bereitstellen. Ein Angebot ist eine Marketing-Botschaft, der ggf. Regeln zugeordnet sind, die angeben, wer zum Anzeigen des Angebots berechtigt ist.

Sie können Angebote erstellen und bereitstellen, indem Sie eine POST-Anfrage an die [!DNL Decisioning] API.

Dieses Tutorial setzt ein grundlegendes Verständnis der APIs voraus, insbesondere im Hinblick auf die Entscheidungsverwaltung. Weitere Informationen finden Sie unter [Entwicklerhandbuch zur Entscheidungs-API](../getting-started.md). Für dieses Tutorial müssen Sie außerdem über eine eindeutige Platzierungs-ID und einen eindeutigen Entscheidungs-ID-Wert verfügen. Wenn Sie diese Werte nicht erhalten haben, finden Sie in den Tutorials für [Platzierung erstellen](../offers-api/placements/create.md) und [eine Entscheidung erstellen](../activities-api/activities/create.md).

➡️  [Funktion im Video kennenlernen](#video)

## Kopfzeilen &quot;Accept&quot;und &quot;Content-Type&quot; {#accept-and-content-type-headers}

Die folgende Tabelle zeigt die gültigen Werte, aus denen die *Content-Type* und *Accept* -Felder in der Anfragekopfzeile:

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
| `{CONTAINER_ID}` | Der Container, in dem sich die Entscheidungen befinden. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Anfrage**

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
| `xdm:itemCount` | Die Anzahl der zurückzugebenden Angebote. Die maximale Zahl ist 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Dieses Objekt enthält Informationen zum Profil, für das die Entscheidung angefordert wird. Bei einer API-Anfrage enthält dies ein Profil. |
| `xdm:profiles.xdm:identityMap` | Dieses Objekt enthält eine Reihe von Endbenutzer-Identitäten, die auf dem Namespace-Integrationscode der Identität basieren. Die Identitätszuordnung kann mehr als eine Identität jedes Namespace enthalten. Weitere Informationen zu Namespaces finden Sie unter [diese Seite](../../../segment/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | Die vom Client generierte ID, die zur eindeutigen Identifikation einer Anfrage zur Profilentscheidung verwendet werden kann. Diese ID wird in der Antwort widergespiegelt und beeinflusst das Ergebnis der Entscheidung nicht. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Dieses Objekt bildet die Kontrollstruktur der Deduplizierungsregeln. Es besteht aus einer Reihe von Flags, die angeben, ob dieselbe Option für eine bestimmte Dimension vorgeschlagen werden kann. Eine Markierung, die auf &quot;true&quot;gesetzt ist, bedeutet, dass Duplikate zulässig sind und nicht über die durch die Markierung angegebene Kategorie hinweg entfernt werden sollten. Eine Markierung, die auf &quot;false&quot;gesetzt ist, bedeutet, dass die Entscheidungs-Engine nicht denselben Vorschlag für die Dimension erstellen und stattdessen die nächste beste Option für eine der Unterentscheidungen auswählen sollte. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Wenn der Wert auf &quot;true&quot;gesetzt ist, wird möglicherweise mehreren Entscheidungen die gleiche Option zugewiesen. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Wenn der Wert auf &quot;true&quot;gesetzt ist, wird möglicherweise mehreren Platzierungen dieselbe Option zugewiesen. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Gibt die Zusammenführungsrichtlinie an, nach der die vom Profilzugriffsdienst zurückgegebenen Daten verwaltet werden. Wenn in der Anfrage nichts angegeben ist, wird der Entscheidungsmanagement keinen Profilzugriffsdienst weitergeben. Andernfalls wird die vom Aufrufer angegebene ID weitergegeben. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Ein Satz von Flags, die den Antwortinhalt formatieren. |
| `xdm:responseFormat.xdm:includeContent` | Ein boolescher Wert, der, wenn auf `true`, enthält Inhalt für die Antwort. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Ein Objekt, mit dem angegeben wird, welche zusätzlichen Metadaten zurückgegeben werden. Wenn diese Eigenschaft nicht enthalten ist, dann `xdm:id` und `repo:etag` werden standardmäßig zurückgegeben. | `name` |
| `xdm:responseFormat.xdm:activity` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Dieses Flag identifiziert die spezifischen Metadateninformationen, die für `xdm:placement`. | `name`, `channel`, `componentType` |

**Reaktion**

Bei einer erfolgreichen Antwort werden Informationen zu Ihrem Vorschlag zurückgegeben, einschließlich der eindeutigen `xdm:propositionId`.

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
| `xdm:propositionId` | Die eindeutige Kennung für die mit einem XDM-DecisionEvent verknüpfte Vorschlagsentität. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Dieses Objekt enthält einen einzelnen Entscheidungsvorschlag. Für die Entscheidung können mehrere Optionen zurückgegeben werden. Wenn keine Optionen gefunden werden, wird das Fallback-Angebot der Entscheidung zurückgegeben. Einzelne Entscheidungsvorschläge enthalten immer entweder eine `options` -Eigenschaft oder `fallback` -Eigenschaft. Wenn vorhanden, wird die `options` -Eigenschaft darf nicht leer sein. |
| `xdm:propositions.xdm:activity` | Dieses Objekt enthält die eindeutige Kennung für eine Entscheidung. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Dieses Objekt enthält die eindeutige Kennung für eine Angebotsplatzierung. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Dieses Objekt enthält eine einzige Option, einschließlich der eindeutigen Kennung. Falls vorhanden, darf dieses Objekt nicht leer sein. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Definiert den Typ der Komponente. `@type` fungiert als Verarbeitungsvertrag für den Kunden. Wenn das Erlebnis zusammengestellt wird, sucht der Composer nach den Komponenten, die einen bestimmten Typ aufweisen. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Das Format des Antwortinhalts. | Der Antwortinhalt kann lauten: `text`, `html block`oder `image link` |
| `xdm:score` | Die Bewertung für eine Option, die als Ergebnis einer Rangfunktion berechnet wird, die mit der Option oder Entscheidung verknüpft ist. Dieses Feld wird von der API zurückgegeben, wenn eine Rangfunktion bei der Bestimmung des Punkts eines Angebots während des Ranking beteiligt ist. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Dieses Objekt enthält ein einzelnes Fallback-Angebot, einschließlich der eindeutigen Kennung. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zum Anzeigen oder Bedienen der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen, z. B. aus der Liste der [Internet-Medientypen](http://www.iana.org/assignments/media-types/) Definieren von Computermedienformaten. | `"dc:format": "image/png"` oder `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Eine optionale URL zum Lesen des Assets über ein Netzwerk oder einen Service-Endpunkt für die Inhaltsbereitstellung. Diese URL wird verwendet, um von einem Benutzeragenten aus auf das Asset öffentlich zuzugreifen. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Der Zeitpunkt, zu dem die Entscheidungsantwortnachricht erstellt wurde. Dies wird als Epochenzeit dargestellt. | `"ode:createDate": 1566497582038` |

## Tutorial-Video {#video}

Das folgende Video soll Ihr Verständnis der Komponenten der Entscheidungsverwaltung unterstützen.

>[!NOTE]
>
>Dieses Video gilt für den auf Adobe Experience Platform aufbauenden Offer Decisioning-Anwendungsdienst. Es bietet jedoch eine allgemeine Anleitung zur Verwendung von Angeboten im Kontext von Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Nächste Schritte {#next-steps}

In diesem API-Handbuch haben Sie Angebote mit der Variablen [!DNL Decisions] API. Weitere Informationen finden Sie unter [Überblick über die Entscheidungsverwaltung](../../../offers/get-started/starting-offer-decisioning.md).
