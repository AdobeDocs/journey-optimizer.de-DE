---
solution: Journey Optimizer
product: journey optimizer
title: Anbieterintegration
description: Verwenden Sie Adobe Journey Optimizer-Integrationen mit jeder externen Plattform, die eine gültige API bereitstellt, sowie technisch getestete Anbietermuster, um die Sicherheit beim Entwurf Ihres Setups zu gewährleisten.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: Integration, Anbieter, Drittanbieter
source-git-commit: 3733c9ab401f85b22e1d6e07dbf4db535ff8a96d
workflow-type: tm+mt
source-wordcount: '9157'
ht-degree: 7%

---

# Verfügbare Anbieter

>[!BEGINSHADEBOX]

Inhaltsverzeichnis:

* [Arbeiten mit Integrationen](external-sources.md)
* [Erste Schritte mit der Vendors-Integration](vendor-integration-gs.md)
* **[Verfügbare Anbieter](vendor-integration.md)**
* [FAQs](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Inhalt und CMS {#content-and-cms}

### zufrieden {#contentful}

>[!BEGINSHADEBOX]

Contentful ist eine Headless-CMS für strukturierte Einträge und Assets über REST oder GraphQL, sodass Journey Optimizer Inhalte zum Versand- oder Öffnungszeitpunkt abrufen kann.

Typische Anwendungsfälle sind lokalisierte Hero-Blöcke, Alt-Text und CTAs in E-Mails sowie Produkt- oder Promotioneinträge in dynamischen Modulen. Ein weiteres gängiges Muster besteht darin, einen bestimmten Eintrag anhand der ID für personalisierte Nachrichten abzurufen.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für „Inhaltsvoll“.

Es gelten die folgenden Voraussetzungen:

* Inhalte mit Zugriff auf die Bereitstellungs-API und einem leseorientierten API-Schlüssel
* Löschen von Inhaltstypen und Feld-IDs; Administratorzugriff in Journey Optimizer zum Erstellen von Integrationen.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Eine weite Auflistung oder paginierte Inhalts-APIs passen nicht zu diesem Muster. Sie bevorzugen Abrufaufrufe, die auf einen bestimmten Eintrag oder ein bestimmtes Asset abzielen.
* Rückschreibungen oder bidirektionale Synchronisationen würden den Rahmen dieses Beispiels sprengen.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Content Delivery API (CDA)-URL: `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. Wählen Sie die HTTP-Methode: GET.

1. Authentifizierungskopfzeile hinzufügen:

Autorisierung: Bearer &lt;CONTENTFUL_DELIVERY_TOKEN>

1. Fügen Sie bei Bedarf Pfadvariablen hinzu (z. B. Eintrags-ID, Gebietsschema).

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der erforderlichen Felder für die Personalisierung

1. Konfigurieren Sie Zeitüberschreitung und Caching nach Bedarf.

1. Verbindung testen und aktivieren.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder (Abstimmung mit der [Content Delivery API](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"} für Ihren Bereich und Ihre Umgebung):

| Feld | Wert |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/entries/environments/{{environment_id}}` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **HTTP-Methode** | `GET` |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | `access_token` | `<YOUR_API_KEY>` | Abfrageparameter |

+++

### Sitecore {#sitecore}

>[!BEGINSHADEBOX]

Sitecore Content Hub und zugehörige Cloud-APIs unterstützen DAM-artige Download- und Metadatenflüsse. Im folgenden Beispielmuster wird eine Download-Reihenfolge nach ID dargestellt.

Typische Anwendungsfälle sind Asset- oder Download-Metadaten in E-Mail-Inhalten und die Ausrichtung an in Sitecore verwalteten DAM-Workflows.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Sitecore.

Es gelten die folgenden Voraussetzungen:

* Mandanten-URL und -Anmeldeinformationen (Träger oder Token pro API-Oberfläche).
* Administratorzugriff in Journey Optimizer zum Erstellen von Integrationen.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Hostnamen und Pfade variieren je nach SiteCore-Produkt. Verwenden Sie nur Endpunkte, die Ihr Mandant bereitstellt.
* OAuth-Zugriffstoken, -Aktualisierungen und -Lebensdauern müssen der Sitecore-Sicherheitsrichtlinie entsprechen.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Konfigurieren Sie **GET** in Ihrem Download-Auftragspfad, legen Sie Autorisierungskopfzeilen pro Sitecore fest, ordnen Sie `id` aus dem Kontext zu, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu und stimmen Sie Zeitüberschreitungen für die Asset-Latenz ab.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Content Hub-API (Beispiel: Download order by ID). Beispiel für URL-Muster:

1. `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Verwenden Sie die folgenden Felder, wenn Sie diesen Beispielaufruf in Journey Optimizer konfigurieren. Bestätigen Sie den Host-Namen und die API-Version für Ihr Produkt (Content Hub, XM Cloud usw.) in der [Sitecore-Dokumentation](https://doc.sitecore.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Autorisierung | Autorisierung | Konstante | `<token>` | Ja (ein) |
| If-Modified-Since | If-Modified-Since | Variable | 24.08.2019 T14:15:22Z | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | X-Auth-Token | `<token>` | Header |

+++

### Bocksbart {#salsify}

>[!BEGINSHADEBOX]

Salsify ist ein PIM mit APIs für Produkte, Kanäle und digitale Assets.

Typische Anwendungsfälle sind Produktattribute oder Medien-URLs in E-Mails und Messaging, die auf syndizierte Katalogdaten abgestimmt sind.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Salsify.

Es gelten die folgenden Voraussetzungen:

* API-Token und Organisationskontext; Produkt-IDs, die aus Profil oder Kontext aufgelöst werden können.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Sehr große Kataloge: Vermeiden Sie Massenlisten-Endpunkte, wenn Integrationen einen Entitätenabruf erwarten.
* Die Sichtbarkeit von Attributen kann durch Berechtigungen für die Rolle „Fälschung“ eingeschränkt werden.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Einzelproduktabruf gegenüber Massenaufrufen im Katalog vorziehen, Bearer-Authentifizierung festlegen, Beispiel-JSON einfügen, Felder zuordnen, testen, aktivieren.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Salsify Product-API. Beispiel für URL-Muster:

1. `https://api.salsify.com/v1/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Einige ältere Referenzen haben einen Pfad für den Download-Order-Stil für Salsify wiederverwendet. Ihr Mandant kann stattdessen `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` oder Ähnliches verwenden. Bestätigen Sie dies in [Salsify-Entwickler](https://developers.salsify.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Typ (Standardparameter) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Autorisierung | Autorisierung | Konstante | `Bearer <YOUR_TOKEN_HERE>` | Ja (ein) |
| If-Modified-Since | If-Modified-Since | Variable | 24.08.2019 T14:15:22Z | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | `apiKey` | `<your_api_key>` | Header |

+++

### contentStack {#contentstack}

>[!BEGINSHADEBOX]

ContentStack ist eine Headless-CMS. REST-Bereitstellung ist typisch für die JSON-Feldzuordnung in Journey Optimizer.

Ein typischer Anwendungsfall ist die Verwendung von Einträgen für Banner oder Promos mit Parametern, die das Gebietsschema enthalten.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für ContentStack.

Es gelten die folgenden Voraussetzungen:

* Stack-API-Schlüssel, Versand-Token, Umgebungsname und Inhaltstyp-UIDs.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Dieses Muster verwendet REST JSON für die Feldzuordnung. Die GraphQL-Bereitstellung folgt einem anderen Integrationspfad.
* Verwenden Sie produktionsspezifische Versand-Token. Vorschau und veröffentlichte Flüsse sind nicht austauschbar.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Fügen Sie sowohl `api_key`- als auch `access_token`-Kopfzeilen hinzu, wie es der Content-Stack erfordert, schließen Sie den `environment` Abfrageparameter ein, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Content Delivery API. Beispiel für URL-Muster:

1. `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder. Siehe [ContentStack Content Delivery API](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| Kopfzeilen | Keine zusätzlichen Kopfzeilen erforderlich. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `content_type_uid` | Content-Typ UID | `<your_content_type_uid>` |
| `entry_uid` | Eintritt UID | `<your_entry_uid>` |

**Authentifizierung**

| Schlüsselname | Schlüsselwert | Hinzufügen zu |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

ContentStack erwartet **beide** Schlüssel als Kopfzeilen für Versandanfragen.

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `environment` | Umgebungsname | Variable | `<your_environment_name>` | Ja (ein) |

+++

### Akeneo {#akeneo}

>[!BEGINSHADEBOX]

Akeneo PIM stellt REST-APIs für Produkte, Attribute und Medien bereit.

Typische Anwendungsfälle sind geregelte Produktdaten in E-Mail-Modulen und Attribute für einen bestimmten Kanal in Journey.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Akeneo.

Es gelten die folgenden Voraussetzungen:

* PIM-Basis-URL und OAuth-Client; Produkt-UUID oder Kennungsstrategie.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* PIM-Antworten können groß sein. Ordnen Sie nur die für die Personalisierung erforderlichen Attribute zu.
* Schreibvorgänge liegen außerhalb des Bereichs typischer schreibgeschützter Personalisierungsbeispiele.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie **GET** mit Bearer-Token, fordern Sie nur erforderliche Attributoptionen in Abfrage-Flags an, fügen Sie Beispiel-JSON ein, ordnen Sie einen minimalen Attributsatz zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der AEM-REST-API. Beispiel für URL-Muster:

1. `https://{pim-host}/api/rest/v1/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispielmuster: `https://{pim-host}/api/rest/v1/products-uuid/{uuid}` mit `Accept: application/json`. Siehe [Akeneo-API](https://api.akeneo.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Autorisierung | Autorisierung | Konstante | `Bearer <YOUR_TOKEN>` | Ja (ein) |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | Attributoptionen einschließen | Variable | false | Nein (aus) |
| `with_quality_scores` | Qualitätsprüfungen einschließen | Variable | false | Nein (aus) |
| `with_completenesses` | Vollständigkeiten einschließen | Variable | false | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### Magnolie {#magnolia}

>[!BEGINSHADEBOX]

Magnolia bietet Headless- und REST-Bereitstellungsendpunkte je nach Bereitstellung.

Ein typischer Anwendungsfall ist die Bereitstellung von Inhaltsknoten oder Fragmenten für Marketing-Module.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Magnolia.

Es gelten die folgenden Voraussetzungen:

* Instanz-URL und Token oder einfache Authentifizierung; Arbeitsbereich und Pfade für den Versand.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die REST-Bereitstellungs-URLs hängen von den installierten Magnolia-Modulen und der Konfiguration ab.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie das URL-Muster für die öffentliche Bereitstellung, das Ihre Module bereitstellen, authentifizieren Sie sich gemäß der Magnolia-Anleitung (anonymer Versand vs. Token für geschützte Inhalte), fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mit Magnolia REST (Versand). Beispiel für URL-Muster:

1. `https://{author-or-public}/.rest/delivery/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispielmuster: URLs im Stil von `https://{domain}/magnoliaAuthor/.rest/delivery/...` oder öffentlichen Sendungen. Ihre Pfade hängen von den installierten Modulen ab. Siehe [Magnolia-Dokumentation](https://docs.magnolia-cms.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Inhaltstyp | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | `<bearer_token>` | Header |

Hinweis: Die Bereitstellungs-API dient der Verwendung der REST-anonymen Rolle für Inhalte, für die keine Anmeldung erforderlich ist. Für einen sicheren Zugriff auf geschützte Daten wird eine robustere Methode wie API-Token oder OAuth 2.0 bevorzugt

+++


## Loyalität und Prämien {#loyalty-and-rewards}

### beglaubigen {#voucherify}

>[!BEGINSHADEBOX]

Voucherify bietet Promotions und Treue-REST-APIs (Kampagnen, Gutscheine, Treueprogramme).

Typische Anwendungsfälle sind das Lesen des Treue- oder Promotion-Status für Angebote im Inhalt und die Anzeige einer Ebene oder eines Gleichgewichts, wo dies angemessen ist.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Gutscheine.

Es gelten die folgenden Voraussetzungen:

* Anwendungs-ID und Geheimnis (pro Region/Cluster); Klarheit darüber, welche Treue- oder Kampagnen-Endpunkte Sie aufrufen.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Vermeiden Sie es, interne Promotion- oder Kampagnenkennungen in kundenorientierten Fehlern oder Nachrichteninhalten anzuzeigen.
* Es gelten Limits auf Anwendungsebene. Konfigurieren Sie weitere Zustellversuche und das Caching gemäß Gutscheinanleitung.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Festlegen der Basis-URL für Ihren Cluster, Hinzufügen erforderlicher Kopfzeilen (`X-APP-ID`, `X-APP-TOKEN`), Einschränken von Listenendpunkten mit Filtern oder IDs, Einfügen von Beispiel-JSON, Zuordnen von Feldern, Testen, Aktivieren.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Treue-/REST-APIs. Beispiel für URL-Muster:

1. OpenAPI-Basis-URL pro Gutschein für Ihre Region

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder. Vollständige Referenz: [Gutschein-API](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| X-APP-ID | X-APP-ID | Konstante | `<YOUR-APP-ID>` | Ja (ein) |
| X-Voucherify-Channel | X-Voucherify-Channel | Konstante | Dokumentation zu Gutscheinen | Nein (aus) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | Nein (aus) |
| `page` | `page` | Variable | 1 | Nein (aus) |
| `customer` | `customer` | Variable | `<customer_identifier>` | Nein (aus) |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | Nein (aus) |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | Nein (aus) |
| `order` | `order` | Variable | `<sort_field>` | Nein (aus) |
| `code` | `code` | Variable | `<loyalty_card_code>` | Nein (aus) |
| `ids` | `ids` | Variable | `<array_of_ids>` | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### Talon.One {#talon-one}

>[!BEGINSHADEBOX]

Talon.One ist eine Promotion- und Treueregeln-Engine mit REST-APIs für Sitzungen, Effekte und Profile.

Typische Anwendungsfälle sind Promotions auf Warenkorb- oder Profilebene in personalisierten Inhalten und Anzeige des Treueprogramms oder der Belohnungen.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Talon.One.

Es gelten die folgenden Voraussetzungen:

* API-Schlüssel und bereitstellungsspezifische Basis-URLs; Kennungen für den Anwendungs- oder Kampagnenbereich.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Sitzungslastige Flüsse können eine sorgfältige Zuordnung zum Integrations-Anfragemodell erfordern.
* Bitte Talon.One-Ratenbeschränkungen und die Anleitung zur Idempotenz beachten.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie **GET** auf dem benötigten Profil- oder Erfolgspfad, legen Sie `Authorization: ApiKey-v1 <key>` wie dokumentiert fest, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Talon.One-Integrations-API. Beispiel für URL-Muster:

1. `https://{your-domain}.talon.one/v1/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **HTTP-Methode** | `GET` |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | In Bearbeitung/Abgeschlossen/Abgelaufen | Nein (aus) |
| `startDate` | `startDate` | Variable | 29.05.2024 T15:04:05+07:00 | Nein (aus) |
| `endDate` | `endDate` | Variable | 29.05.2024 T15:04:05+07:00 | Nein (aus) |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | Nein (aus) |
| `skip` | `skip` | Variable | `<items_to_skip>` | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | ApiKey-v1-`<YOUR_API_KEY>` | Header |

+++

### Antavo {#antavo}

>[!BEGINSHADEBOX]

Antavo ist eine Enterprise-Treueplattform mit REST-APIs für Mitglieder, Belohnungen und Veranstaltungen.

Typische Anwendungsfälle sind Punkte, Stufen oder Belohnungen in E-Mails oder Push-Benachrichtigungen und Angebote, die vom Treuestatus gesteuert werden.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Antavo.

Es gelten die folgenden Voraussetzungen:

* Stapeln von URL- und API-Anmeldeinformationen sowie Programm- oder Shop-IDs nach Bedarf.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Kunden-PII müssen gemäß den Antavo-Vereinbarungen und Ihren Datenschutzrichtlinien verarbeitet werden.
* Bestätigen Sie API-Versionen und stabile Endpunkte mit Antavo für Ihre Umgebung.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Konfigurieren Sie **GET** mit der Authentifizierung des Anbieters (z. B. API-Schlüssel in der Abfrage), vermeiden Sie die Offenlegung von PII für Richtlinien, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Antavo Enterprise-API. Beispiel für URL-Muster:

1. Pro Antavo-Stack-Basis-URL in Ihrem Mandanten dokumentiert

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder verwenden den **Staging**-Host. Die Produktion verwendet den Hostnamen Ihres Antavo-Stacks. Siehe [Antavo-](https://antavo.com/docs/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Akzeptieren | Akzeptieren | Konstante | application/json | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | `api_key` | `<YOUR_API_KEY>` | Abfrageparameter |

+++

### Salesforce-Treue {#salesforce-loyalty}

>[!BEGINSHADEBOX]

Salesforce Loyalty Management stellt REST-APIs auf der Salesforce-Plattform für Mitglieder, Programme und Transaktionen bereit.

Typische Anwendungsfälle sind die Aufdeckung von Ebenen, Punkten oder Vorteilen in Journey und die Abstimmung von Messaging mit CRM- und Treuedaten.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über die Voraussetzungen und Einschränkungen für die Salesforce-Treue.

Es gelten die folgenden Voraussetzungen:

* Salesforce-Instanz, verbundener App- oder Integrationsbenutzer und OAuth entsprechend Ihrer Organisation.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Salesforce-API-Beschränkungen und die Aktualisierung von OAuth-Token müssen in Ihre Integration integriert werden.
* Regeln für Sicherheit und Freigabe auf Feldebene steuern, welche Felder in API-Antworten angezeigt werden.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie den Treueprogramm-Integrationsendpunkt, den Ihr Team genehmigt, Salesforce OAuth abschließt, JSON-Beispielfelder einfügt, Felder zuordnet, zusammengesetzte API-Limits einhält, testet, aktiviert.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mit dem Salesforce Loyalty Management-REST. Beispiel für URL-Muster:

1. `https://{instance}.salesforce.com/services/data/vXX.X/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Verwenden Sie den GET-Vorgang **Treueverwaltung** Mitgliederprofil), der für die API-Versionsnummer Ihrer Organisation dokumentiert ist. Pfade enthalten Programm- und Mitgliedskennungen. Siehe [Salesforce-Entwickler](https://developer.salesforce.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Akzeptieren | Akzeptieren | Konstante | application/json | Nein (aus) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | Nein (aus) * |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | Nein (aus) * |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | Nein (aus) * |

\* Mindestens einer der drei Werte ist erforderlich.

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | `<access_token>` | Header |

+++

### kapillar {#capillary}

>[!BEGINSHADEBOX]

Capillary bietet Treue- und Interaktions-APIs, die in Einzelhandels-Stacks üblich sind.

Typische Anwendungsfälle sind Punkte, Stufen oder Angebote innerhalb personalisierter Journey.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Kapillare.

Es gelten die folgenden Voraussetzungen:

* API-Host und Authentifizierung (häufig signierte Anfragen; befolgen Sie die Dokumente der Kapillare).
* Programmkennungen für Ihren Endpunkt.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Authentifizierungsschemata und regionale Hosts variieren je nach Bereitstellung. Bestätigen Sie mit Kapillare für Ihren Stack.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Konfigurieren Sie Kopfzeilen wie `CAP-API-ACCESS-TOKEN` nach Bedarf, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Kapillaren-APIs. Beispiel für URL-Muster:

1. Handbuch zur Kapillarintegration für Ihre Region

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiel: `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` (Host variiert je nach Region). Validieren des Host- und Authentifizierungsschemas mit [Capillary](https://capillarytech.com/){target="_blank"}.


| Feld | Wert |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `reward_id` | Belohnungs-ID | `<your_reward_id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Inhaltstyp | Inhaltstyp | Konstante | application/json | Ja (ein) |
| CAP-API-ACCESS-TOKEN | Zugriffs-Token | Konstante | `<YOUR_ACCESS_TOKEN>` | Ja (ein) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## Vorlagen und Messaging {#templates-and-messaging}

### Stensul {#stensul}

>[!BEGINSHADEBOX]

Stensul ist eine E-Mail-Erstellungsplattform für genehmigte Vorlagen. Journey Optimizer kann über seine API Vorlagenmetadaten und strukturierte Regionen nutzen.

Typische Anwendungsfälle sind der Import genehmigter Vorlagen und die Zuordnung von Regionen zu Profilattributen sowie die Wiederverwendung von gesteuerten Blöcken für skalierbare Kampagnen-Builds.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für Stensul.

Es gelten die folgenden Voraussetzungen:

* Stensul-Konto mit API-Zugriff und veröffentlichten Vorlagen mit definierten Token.
* Administratorzugriff in Journey Optimizer zum Erstellen von Integrationen.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die In-Place-Bearbeitung von Stensul-Vorlagen in Journey Optimizer durch WYSIWYG wird hier nicht behandelt.
* Große oder komplexe HTML in Vorlagen-Payloads müssen möglicherweise überprüft und bereinigt werden.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Stensul-Vorlagen-API-URL (Beispielmuster): `https://api.stensul.com/v1/templates/{template_id}`

1. Konfigurieren der Authentifizierung (API-Schlüssel oder OAuth gemäß Stensul-API-Dokumentation).

1. Definieren Sie Pfadvariablen (z. B. Vorlagen-ID).

1. Fügen Sie eine JSON-Beispielantwort zur Felderkennung ein.

1. Zuordnen erforderlicher Vorlagenfelder zu Journey Optimizer-Personalisierungsfeldern.

1. Verbindung testen und aktivieren.

### Ringelblume {#marigold}

>[!BEGINSHADEBOX]

Marigold stellt APIs für Treue und Interaktion bereit. Die Hosts unterscheiden sich je nach Geografie (EU- vs. US-Modul-Hostnamen).

Ein typischer Anwendungsfall besteht darin, Nachrichten mit Treue- oder Präferenzdaten aus Ringelblumen-Programmen anzureichern.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Ringelblume.

Es gelten die folgenden Voraussetzungen:

* Basis-URL und Anmeldeinformationen aus Ihrem Vertrag; API-Benutzer mit den geringsten Berechtigungen, sofern möglich.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die Endpunkte variieren je nach Ringelblumen-Produkt. Validieren Sie mit Ringelblumen-Unterstützung für Ihre -Bereitstellung.
* Personenbezogene Daten in Antworten müssen mit Ihren DPA- und Aufbewahrungsrichtlinien übereinstimmen.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Zeigen Sie auf den Ringelblumen-Host für Ihre Region, legen Sie die Authentifizierung fest (das folgende Beispiel verwendet `X-Api-Key` mit Schlüssel und Geheimnis), fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Marigold-REST-API (Endpunkt gemäß Ihrem Integrationshandbuch). Beispiel für URL-Muster:

1. Verwenden Sie die Basis-URL und den Pfad, die in Ihrer Marigold-API-Dokumentation angegeben sind.

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

1. Marigold verwendet zwei Endpunkte, die auf dem geografischen Gebiet basieren, für das die Kundeninstanz aktiv ist:

1. Europa: https://{{customername}}.module.slgnt.eu
USA: https://{{customername}}.module.slgnt.us

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Basishost hängt von der Region ab (z. B. `https://{{customername}}.module.slgnt.eu` oder `https://{{customername}}.module.slgnt.us`). Bestätigen Sie die Pfade mit Ringelblume für Ihre Bereitstellung.

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | x-api-key | `<apiKey>:<apiSecret>` | Header |

+++

### Adobe Target Recommendations {#adobe-target-recommendations}

>[!BEGINSHADEBOX]

Adobe Target umfasst Recommendations- und Bereitstellungs-APIs für Server-seitige oder integrierte Erlebnisse, je nach Berechtigungen.

Typische Anwendungsfälle sind das Einfügen von Empfehlungen in von Ihnen in Journey Optimizer erstellte Erlebnisse und das Ausrichten von Schlüsseln am Profil- oder Experience Platform-Kontext.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Adobe Target Recommendations.

Es gelten die folgenden Voraussetzungen:

* Target mit Recommendations; IMS-Organisation und unterstützte Authentifizierung.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Recommendations- und Bereitstellungs-APIs erfordern bestimmte Parameter (z. B. Mbox- oder Produkt-IDs). Befolgen Sie die Dokumentation zu Adobe Target.
* Passen Sie die Latenz und das Caching für Ihr Versandvolumen und Ihren Anwendungsfall an.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Versandaufrufe erfolgen häufig **POST** mit einem JSON-Text. Konfigurieren Sie OAuth pro [Target-Authentifizierung](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"} fügen Sie eine Beispielantwort ein, ordnen Sie Felder zu und testen Sie unter dem erwarteten Volumen.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Target Recommendations-/Bereitstellungs-APIs (gemäß Adobe-Dokumentation für Ihr Integrationsmuster). Beispiel für URL-Muster:

1. Siehe Dokumentation zur Adobe Target Recommendations-API für Ihren Anwendungsfall

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **HTTP-Methode** | `POST` |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Kunde | Kunde | Variable | `<customer_client_code>` | Ja (ein) |
| sessionId | sessionId | Variable | ` <session_identifier>` | Ja (ein) |

**Authentifizierung**

Siehe [Target-Authentifizierungskonfiguration](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication) und fügen Sie JSON zur Payload hinzu.

**Anfrage-Payload**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## Daten, Wetter und Vorgänge {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!BEGINSHADEBOX]

AccuWeather stellt Vorhersage- und Standort-REST-APIs bereit, damit Nachrichten wetterabhängige Snippets enthalten können.

Typische Anwendungsfälle sind kurze Prognosen in E-Mails oder Push-Benachrichtigungen und die Anpassung von Inhalten mithilfe von Prognosewerten, die an das Profil oder den Kontext gebunden sind.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für AccuWeather.

Es gelten die folgenden Voraussetzungen:

* API-Abonnement und -Schlüssel; Standortschlüssel oder Stadtsuchfluss.
* Administratorzugriff in Journey Optimizer zum Erstellen von Integrationen.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Bestätigen Sie die JSON-Antwort-Form für Ihre AccuWeather-Abonnementebene. Integrations ordnet Felder aus JSON-Antworten zu.
* Beachten Sie die AccuWeather-Ratenbeschränkungen und die empfohlene Zwischenspeicherung.
* Die Lösung von `locationKey` erfordert häufig eine separate Geolokalisierungs- oder Stadtsuchanfrage, bevor Prognoseaufrufe durchgeführt werden können.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie **GET** Sofern Ihr Abonnement nichts anderes erfordert, fügen Sie den `apiKey` Abfrageparameter (oder wie dokumentiert) hinzu, ordnen Sie `locationKey` und andere Variablen aus dem Profil/Kontext zu, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu und testen Sie dann.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der API für tägliche Prognosen . Beispiel für URL-Muster:

1. `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++Beispiele für Integrationsfelder

Beispiele für Integrationsfelder. Details und Ebenen werden unter [AccuWeather-APIs](https://developer.accuweather.com/apis){target="_blank"} beschrieben. Häufig lösen Sie `locationKey` mit einem separaten Ortssuchaufruf auf (z. B. `.../locations/v1/cities/search?q={{cityName}}`).

| Feld | Wert |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | JSON | Nein (aus) |
| `language` | `language` | Variable | en-US | Nein (aus) |
| `details` | `details` | Variable | False | Nein (aus) |
| `metric` | `metric` | Variable | False | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | `apiKey` | `<YOUR_API_KEY>` | Abfrageparameter |

+++

### Schiffsstation {#shipstation}

>[!BEGINSHADEBOX]

ShipStation bietet Versand- und Auftrags-APIs für Spediteure, Labels und Tracking.

Typische Anwendungsfälle sind Bestellstatus, Tracking-Links oder Versand-ETAs in Transaktionsnachrichten.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für ShipStation.

Es gelten die folgenden Voraussetzungen:

* API-Schlüssel und Geheimnis (Standardauthentifizierung gemäß ShipStation-Dokumenten).
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* ShipStation-API-Schlüssel nicht im Nachrichteninhalt offenlegen; Anmeldeinformationen nur in der Integrationskonfiguration beibehalten.
* Paginierte Listenendpunkte eignen sich möglicherweise nicht für Integrationen. Ziehen Sie nach Möglichkeit GETs mit einer Ressource vor.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Targeting der benötigten Ressource (Bestellungen vs. Sendungen), Authentifizierung pro [ShipStation-API](https://www.shipstation.com/docs/api/){target="_blank"}, Einfügen von Beispiel-JSON, Zuordnen von Feldern, Testen, Aktivieren.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der ShipStation-REST-API. Beispiel für URL-Muster:

1. `https://ssapi.shipstation.com/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Das folgende **Get Timer**-Beispiel veranschaulicht einen ShipStation-Automatisierungszeitaufruf. Verwenden Sie bei der Wiedergabe in Journey Optimizer den genauen Pfad und die Authentifizierungsdaten aus Ihrem ShipStation-Integrationshandbuch.

| Feld | Wert |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **HTTP-Methode** | `POST` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | apiKey | `<your_api_key>` | Header |

**Anfrage-Payload**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### Umsatzsteuer {#revenuecat}

>[!BEGINSHADEBOX]

RevenueCat stellt APIs für Abonnementstatus und Berechtigungen für Apps bereit.

Ein typischer Anwendungsfall ist der Abonnementstatus in Lebenszykluskampagnen, für die die Richtlinie Folgendes zulässt.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für RevenueCat.

Es gelten die folgenden Voraussetzungen:

* Geheime API-Schlüssel- und App-Kennungen; stabile Zuordnung zwischen Profilen und RevenueCat-Kunden-IDs.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Schützen Sie geheime API-Schlüssel und befolgen Sie Ihre Rotationsrichtlinien.
* Abonnement- und Berechtigungsdaten sind vertraulich. Erfüllen Sie Datenschutz- und Einverständnisanforderungen.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Rufen Sie den unten modellierten REST **GET** auf, authentifizieren Sie sich mit der Kopfzeile des geheimen Schlüssels, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der RevenueCat-REST-API. Beispiel für URL-Muster:

1. `https://api.revenuecat.com/v1/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispielmuster: Verwenden Sie die **Produkt abrufen** (oder eine entsprechende Produkt-/Berechtigungs-GET) von [RevenueCat-](https://docs.revenuecat.com/){target="_blank"} mit der Basis-URL und -Version Ihres Projekts.

| Feld | Wert |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Nein (aus) |
| `locale` | `locale` | Variable | `<locale_code>` | Nein (aus) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!BEGINSHADEBOX]

Databricks stellt SQL- und REST-APIs über Lakehouse-Daten bereit; frühere Entwürfe kombinierten Anleitungen zur Anweisungsausführung mit einem **jobs/get**-Beispiel.

Ein typischer Anwendungsfall ist die Verwendung kleiner, denormalisierter Attribute aus verwalteten Tabellen zur Personalisierung mit den geringsten Berechtigungen.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für Datenblöcke.

Es gelten die folgenden Voraussetzungen:

* Workspace-Host, -Token oder OAuth pro Organisationsrichtlinie; Service-Prinzipal mit minimalem Umfang.
* Administratorzugriff in Journey Optimizer.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Engere Lesepfade werden empfohlen. Wenn Sie die **POST**-Anweisungsausführung verwenden, fügen Sie den von der API benötigten JSON-Text ein, fügen Sie eine Beispiel-Erfolgsantwort für die Zuordnung ein, testen Sie die Latenz sorgfältig und aktivieren Sie sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der DataBricks SQL-Anweisungsausführungs-API. Beispiel für URL-Muster:

1. `https://{workspace-host}/api/2.0/sql/statements/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++Beispiele für Integrationsfelder

Das folgende Beispiel für einen **GET**-Auftrag ist anschaulich. Für eine SQL-gesteuerte Personalisierung sollten Sie das Muster [Anweisungsausführungs-API](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} verwenden, das Ihr Arbeitsbereich unterstützt.

| Feld | Wert |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| Authentifizierung | OAuth |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | Ja |

+++

## Bewertungen, Einverständnis und Social Media {#reviews-consent-and-social}

### Bindemittel {#bynder}

>[!BEGINSHADEBOX]

Bynder ist ein DAM mit REST-APIs. Integrationen verwenden häufig OAuth 2.0 für schreibgeschützte Metadaten oder Asset-URLs.

Typische Anwendungsfälle sind das Abrufen von Asset-Metadaten oder Versand-URLs in Nachrichten und die Abstimmung der in Bynder genehmigten Kreativen mit den Journey.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Binder.

Es gelten die folgenden Voraussetzungen:

* Portaldomäne und OAuth-Client (oder Ansatz mit genehmigten Token).
* Bereiche für schreibgeschützten Zugriff; Admin-Zugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die Aktualisierung von Paginierung und OAuth-Token muss den API-Regeln von Bynder entsprechen.
* Große paginierte Antworten: Ordnen Sie nur die für die Personalisierung erforderlichen Felder zu.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Konfigurieren Sie **GET** für den ausgewählten Endpunkt (ein gängiges Muster ist eine Benutzerauflistung), schließen Sie OAuth pro [Bynder](https://developer.bynder.com/){target="_blank"} ab, vermeiden Sie das Abrufen unnötiger Datenseiten, ordnen Sie Felder zu, testen Sie und aktivieren Sie dann.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Bynder-API v4 (Beispiel: Benutzerauflistungsmuster). Beispiel für URL-Muster:

1. `https://{your-bynder-domain}/api/v4/users/`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder. Weitere Informationen [&#x200B; OAuth 2.0-Payload finden Sie in der &#x200B;](https://developer.bynder.com/){target="_blank"} zur Bynder-API .

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| Autorisierung | Autorisierung | Konstante | `<token>` | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | False | Nein (aus) |
| `limit` | `limit` | Variable | 100 | Nein (aus) |
| `page` | `page` | Variable | 1 | Nein (aus) |

**Authentifizierung**

| Typ | Payload |
| --- | --- |
| OAuth 2.0 | OAuth 2.0-Payload (siehe Bynder-Dokumentation) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Vertrauensführer {#trustpilot}

>[!BEGINSHADEBOX]

Trustpilot stellt APIs für geschäftliche und Überprüfungszusammenfassungsdaten bereit, sofern Ihr Anwendungsfall und Ihr Vertrag dies zulassen.

Ein typischer Anwendungsfall ist die Anzeige von Rezensionszählungen oder Bewertungen in Marketing-Inhalten, die den Trustpilot-Bedingungen entsprechen.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Trustpilot.

Es gelten die folgenden Voraussetzungen:

* API-Schlüssel und genehmigter Anwendungsfall; Geschäftskennungen für Abfragen.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die Verwendung von Trustpilot-Daten muss den Branding- und Datennutzungsrichtlinien von Trustpilot entsprechen.
* Die Ratenbeschränkungen gelten für die Prüfungszusammenfassung und die zugehörigen Endpunkte.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). **GET** mit der erforderlichen Abfrageauthentifizierung konfigurieren, Kennungen aus Profil oder Kontext zuordnen, Beispiel-JSON einfügen, Felder zuordnen, testen, aktivieren.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Trustpilot-APIs. Beispiel für URL-Muster:

1. `https://api.trustpilot.com/v1/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Verwenden Sie den Kategorienlistenvorgang von [Trustpilot-Entwickler](https://developers.trustpilot.com/){target="_blank"} für Ihr Integrationsmuster. Parameter variieren je nach Ressource.

| Feld | Wert |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Nein (aus) |
| `locale` | `locale` | Variable | `<locale_code>` | Nein (aus) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!BEGINSHADEBOX]

Bazaarvoice bietet Bewertungen, Bewertungen und UGC-APIs.

Ein typischer Anwendungsfall ist die Anzeige von Prüfungszusammenfassungen oder Bewertungen in E-Mails, wenn die Richtlinie dies zulässt.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Bazaarvoice.

Es gelten die folgenden Voraussetzungen:

* API-Passkey- und Client-IDs aus Ihrem Vertrag.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die Anzeige von Bewertungen und Rezensionen muss den Inhaltsrichtlinien von Bazaarvoice entsprechen.
* Es gelten Ratenbeschränkungen und Zwischenspeicherungsregeln pro API-Schlüssel.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie **GET** mit `passkey` als Abfrageparameter in der Conversations-API, legen Sie `Accept: application/json` fest, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Bazaarvoice Conversations-API. Beispiel für URL-Muster:

1. `https://api.bazaarvoice.com/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiel-Einstiegspunkt: `https://api.bazaarvoice.com/data/products.json` mit Abfrageparametern für Version und Filter. Siehe [Bazaarvoice-](https://developer.bazaarvoice.com/){target="_blank"}.

| Feld | Wert |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Authentifizierung**

| Typ | Schlüsselwert | Standort |
| --- | --- | --- |
| Hauptschlüssel | `<YOUR_ACCESS_TOKEN>` | Abfrageparameter |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | Konstante | 5,4 | Ja (ein) |
| `filter` | `filter` | Variable | ID:47950830 | Nein (aus) |
| `stats` | `stats` | Variable | all | Nein (aus) |

+++

### OneTrust {#onetrust}

>[!BEGINSHADEBOX]

OneTrust stellt Datenschutz- und Einverständnis-APIs (produktspezifische URLs und Schemas) bereit.

Ein typischer Anwendungsfall ist das Lesen von Einverständnis- oder Präferenzsignalen für bedingte Inhalte, wenn die Architektur und die rechtliche Überprüfung dies zulassen.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für OneTrust.

Es gelten die folgenden Voraussetzungen:

* API-Anmeldeinformationen und regionale Basis-URL; rechtliche Genehmigung für Felder, die im Messaging verwendet werden.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Einverständnis- und Präferenzdaten sind stark reguliert. Koordinieren Sie sich mit Datenschutz- und Rechtsabteilungen.
* API-Pfade und Payloads unterscheiden sich je nach OneTrust-Produkt. Verwenden Sie die Dokumentation für Ihr Abonnement.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie das veröffentlichte Schema oder den Pfad zum Präferenzcenter in Ihren Abonnementdokumenten, füllen Sie bei Bedarf OAuth aus, fügen Sie JSON-Beispieldateien ein, ordnen Sie Felder zu, testen Sie sie, aktivieren Sie sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der OneTrust-API. Beispiel für URL-Muster:

1. Basis-URL des OneTrust-Entwicklerportals

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

| Feld | Wert |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| **Authentifizierung** | OAuth |

**Pfadparameter**

| Parameter | Name | Wert |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `state` | `state` | Konstante | VERÖFFENTLICHT | Ja |

+++

#### Schema des Präferenzzentrums (veröffentlicht)

Beispielmuster (Fragment): `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. Bestätigen Sie den genauen Pfad in [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}.

### Meta {#meta}

>[!BEGINSHADEBOX]

Meta Graph- und Marketing-APIs stellen Katalog- und Kampagnenobjekte für autorisierte Geschäftsintegrationen bereit.

Ein typischer Anwendungsfall besteht darin, Inhalte mit Attributen aus Meta anzureichern, wo Token und Richtlinien dies zulassen.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Meta.

Es gelten die folgenden Voraussetzungen:

* Systembenutzer oder App-Token mit korrekten Berechtigungen; Business Manager-Ausrichtung.
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Für kurzlebige Zugriffs-Token ist eine Erneuerung oder eine langlebige Strategie erforderlich, die für Server-seitige Integrationen geeignet ist.
* Halten Sie sich an die Meta Platform-Bedingungen. Protokollieren Sie keine Token oder anderen Geheimnisse in den Nachrichten-Payloads.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Diagrammaufrufe sind häufig **GET** mit einem versionierten Pfad; verarbeiten Token-Ablauf, fügen Beispiel-JSON ein, mappen Felder, testen, aktivieren.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Meta Graph-API. Beispiel für URL-Muster:

1. `https://graph.facebook.com/vXX.X/...`
1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispiele für Integrationsfelder. Versionierung [&#x200B; Zugriffstoken finden Sie unter &#x200B;](https://developers.facebook.com/docs/graph-api){target="_blank"}Graph-API“.

| Feld | Wert |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **HTTP-Methode** | `GET` |
| Antwort-Payload | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |
| Richtlinie | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| Authentifizierung | OAuth |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Akzeptieren | Akzeptieren | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | id | Nein |
| `filter` | `filter` | Variable | — | Nein |

+++

### Aprimo {#aprimo}

>[!BEGINSHADEBOX]

Aprimo kombiniert Marketing-Vorgänge und DAM-APIs für Datensätze, Assets und Metadaten.

Typische Anwendungsfälle sind genehmigte Datensatz- oder Asset-Felder in dynamischen Inhalten und geregelte DAM-Workflows in regulierten Branchen.

>[!ENDSHADEBOX]

+++ Weitere Informationen zu Voraussetzungen und Einschränkungen für Aprimo.

Es gelten die folgenden Voraussetzungen:

* Mandanten-URL und -Anmeldeinformationen (OAuth- oder API-Schlüssel gemäß Ihrer Einrichtung).
* Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Die Sicherheit auf Feldebene von Aprimo muss mit den Attributen übereinstimmen, die Sie in Journey Optimizer zuordnen.
* Große HAL- oder JSON-Payloads: Beschränken Sie zugeordnete Felder auf den erforderlichen Mindestsatz.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Verwenden Sie **GET** auf dem gewünschten Datensatzpfad, senden Sie erforderliche Kopfzeilen wie `API-VERSION`, fügen Sie Beispiel-JSON (HAL oder JSON als Rückgabe) ein, ordnen Sie einen minimalen Feldsatz zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Aprimo DAM / Records API. Beispiel für URL-Muster:

1. Per Aprimo API Basis-URL und Ressourcenpfad für Ihren Mandanten

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

| Feld | Wert |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **HTTP-Methode** | `GET` |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |
| API-VERSION | API-VERSION | Konstante | 1 | Ja (ein) |
| Akzeptieren | Akzeptieren | Konstante | application/hal+json ODER application/json | Nein (aus) |
| select-record | select-record | Variable | `<selection_type>` | Nein (aus) |
| select-record-fields | select-record-fields | Variable | `<field_list>` | Nein (aus) |
| select-field | select-field | Variable | `<field_selection>` | Nein (aus) |

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | Autorisierung | `<token>` | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!BEGINSHADEBOX]

Epsilon stellt APIs gemäß Enterprise Agreement bereit. Basis-URLs und Autorisierung stammen von Ihrem Konto-Team (das Beispiel der Ereignis-API unten ist nur beispielhaft).

Ein typischer Anwendungsfall besteht darin, Treue- oder Angebotsattribute über unterstützte JSON-APIs verfügbar zu machen.

>[!ENDSHADEBOX]

+++ Erfahren Sie mehr über Voraussetzungen und Einschränkungen für Epsilon (Epsilon3).

Es gelten die folgenden Voraussetzungen:

* Anmeldedaten und Endpunkte von Epsilon; Administratorzugriff in Journey Optimizer.

Die folgenden Einschränkungen und Ausschlüsse gelten:

* Endpunkte und Hosts sind kundenspezifisch. Stellen Sie nur mit der Dokumentation Ihres Epsilon-Account-Teams bereit.

+++

Gehen Sie wie folgt vor, um diese Integration in Journey Optimizer zu konfigurieren. Siehe **Beispiele für Integrationsfelder** z. B. Anfragedetails, und bestätigen Sie diese Werte mit der Anbieterdokumentation für Ihre Umgebung.

1. Folgen Sie [Arbeiten mit Integrationen](external-sources.md). Raten Sie keine öffentlichen URLs. Verwenden Sie die Spezifikation aus Epsilon, fügen Sie Beispiel-JSON ein, ordnen Sie Felder zu, testen Sie, aktivieren Sie.

1. Gehen Sie in Journey Optimizer zu Konfigurationen > Verwalten und klicken Sie auf Integration erstellen .

1. Geben Sie einen Integrationsnamen ohne Leerzeichen ein.

1. Konfigurieren Sie den Endpunkt mithilfe der Epsilon-API (gemäß Ihrer Integrationsspezifikation). Beispiel für URL-Muster:

1. Bildmaterial von Epsilon für Ihr Programm

1. Wählen Sie die HTTP-Methode aus, die in der Konfigurationstabelle angezeigt wird (normalerweise GET, sofern nicht anders angegeben).

1. Konfigurieren Sie die Authentifizierung (Kopfzeilen, Abfrageparameter oder OAuth) genau wie in der Tabelle und in der Anbieterdokumentation angegeben.

1. Definieren Sie Pfad-, Abfrage- und Kopfzeilenparameter und ordnen Sie Variablen ggf. Profil- oder kontextuellen Daten zu.

1. Fügen Sie eine JSON-Beispielantwort ein, damit Felder erkannt und zugeordnet werden können.

1. Auswahl der für die Personalisierung erforderlichen Felder in der Antwort-Payload-Zuordnung.

1. Konfigurieren Sie die Richtlinien für Zeitüberschreitung, Wiederholung und Zwischenspeicherung basierend auf dem erwarteten Volumen.

1. Testen Sie die Verbindung und aktivieren Sie dann die Integration.

In der folgenden Tabelle sind Beispielwerte für diese Integrationsanfrage aufgeführt.

+++ Beispiele für Integrationsfelder

Beispielmuster: `https://{your-instance}.epsilon3.io/api/v1/planning/events` mit `start` und `end` Abfrageparametern und kopfzeilenbasierten API-Schlüsseln. Mit Epsilon vor der Produktion bestätigen.

| Feld | Wert |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **HTTP-Methode** | `GET` |
| **Richtlinie** | Konfigurieren Sie Details auf Richtlinienebene nach Bedarf. |
| **Antwort-Payload** | Wählen Sie die gewünschten Antwortfelder aus und konfigurieren Sie sie für die Verwendung beim Authoring basierend auf der API-Antwort. |

**Pfadparameter**

| Pfadparameter | Name | Standardwert |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**Kopfzeilen**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| Content-Type (Standard) | Inhaltstyp | Konstante | application/json | Ja (ein) |

**Abfrageparameter**

| Parameter | Name | Typ | Wert | Obligatorisch |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 24.08.2019 T14:15:22Z | Ja (ein) * |
| `end` | `end` | Variable | 24.08.2019 T14:15:22Z | Ja (ein) * |
| `eventType` | `eventType` | Variable | Geplant/Nicht geplant | Nein (aus) |
| `exclude_recurrences` | `exclude_recurrences` | Variable | true/false | Nein (aus) |

\* Optional für `eventType` = `unscheduled` und für `exclude_recurrences` = `true`.

**Authentifizierung**

| Typ | API-Schlüsselname | API-Schlüsselwert | Standort |
| --- | --- | --- | --- |
| API-Schlüssel | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

