---
title: Fallback-Angebote-Datensatz
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Fallback-Angebote verwendet werden
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Fallback-Angebote-Datensatz {#fallback-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für Fallback-Angebote aktualisiert.

![](../assets/dataset-fallback.png)

Der zuletzt erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>Erfahren Sie, wie Sie für jedes Objekt Ihrer Angebotsbibliothek in auf die exportierten Datensätze zugreifen können. [diesem Abschnitt](../export-catalog/access-dataset.md).

Im Folgenden finden Sie eine Liste aller Felder, die im **[!UICONTROL Decision Object Repository - Fallback Offers]** Datensatz.

## Kennung {#identifier}

**Feld:** _id
**Titel:** Kennung
**Beschreibung:** Eine eindeutige Kennung für den Datensatz.
**Typ:** Zeichenfolge

## _experience {#experience}

**Feld:** _experience
**Typ:** Objekt

### _experience > decisioning

**Feld:** Entscheidungsfindung
**Typ:** Objekt

#### _experience > decisioning > features

**Feld:** Merkmale
**Titel:** Entscheidungsoptionseigenschaften
**Beschreibung:** Zusätzliche Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Merkmale aufweisen (Schlüssel in der Zuordnung). Die Merkmale sind Namenswertpaare, mit denen eine Entscheidungsoption von anderen unterschieden wird. Eigenschaften werden als Werte im Inhalt verwendet, der diese Entscheidungsoption darstellt, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieser Aspekt als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.
**Typ:** Objekt

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### _experience > decisioning > contents

**Feld:** Inhalt
**Titel:** Inhaltsdetails
**Beschreibung:** Inhaltselemente zum Rendern des Entscheidungselements in verschiedenen Kontexten. Eine Entscheidungsoption kann mehrere Inhaltsvarianten aufweisen. Inhalt ist eine Information, die an eine Zielgruppe für die Verwendung in einem (digitalen) Erlebnis gerichtet ist. Inhalte werden über Kanäle an eine bestimmte Platzierung bereitgestellt.
**Typ:** array

**_experience > decisioning > contents > components**

**Feld:** Komponenten
**Beschreibung:** Die Komponenten des Inhalts, die die Entscheidungsoption darstellen, einschließlich aller Sprachvarianten. Spezifische Komponenten werden durch &quot;dx:format&quot;, &quot;dc:subject&quot;und &quot;dc:language&quot;oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um den mit einem Angebot verknüpften Inhalt zu lokalisieren oder darzustellen und gemäß dem Platzierungsvertrag zu integrieren.
**Typ:** array
**Erforderlich:** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contents > components > Content Component Type**

   **Feld:** _type
   **Titel:** Content Component Type
   **Beschreibung:** Ein Auflistungssatz von URIs, bei dem jeder Wert einem Typ zugeordnet ist, der der Inhaltskomponente angegeben ist. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der @type-Wert ein Verweis auf ein Schema ist, das zusätzliche Eigenschaften der Inhaltskomponente beschreibt.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > _dc**

   **Feld:** _dc
   **Typ:** Objekt
   **Erforderlich:** &quot;format&quot;

   * **Format**

      **Feld:** format
      **Titel:** Format
      **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zum Anzeigen oder Betreiben der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (z. B. aus der Liste der [Internet-Medientypen](http://www.iana.org/ assignments/media-types/), die Computermedienformate definieren).
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;application/vnd.adobe.photoshop&quot;

   * **Sprache**

      **Feld:** language
      **Titel:** Sprache
      **Beschreibung:** Die Sprache(n) der Ressource. \nSprachen werden in Sprachcode angegeben, wie definiert in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), der Teil von BCP 47 ist und an anderer Stelle in XDM verwendet wird.
      **Typ:** array
      **Beispiele:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > decisioning > contents > components > _repo**

   **Feld:** _repo
   **Typ:** Objekt

   * **id**

      **Feld:** id
      **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client erwarten, dass eine zusätzliche Eigenschaft \&quot;repo:resolveUrl\&quot; das Asset abruft.
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **Feld:** name
      **Beschreibung:** Einige Hinweise dazu, wo das Repository zu finden ist, in dem das externe Asset von der \&quot;repo:id\&quot; gespeichert wird.
      **Typ:** Zeichenfolge

   * **repositoryID**

      **Feld:** repositoryID
      **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client erwarten, dass eine zusätzliche Eigenschaft \&quot;repo:resolveUrl\&quot; das Asset abruft.
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Feld:** resolveURL
      **Beschreibung:** Ein optionaler eindeutiger Locator für die Ressource, der das Asset in einem Inhalts-Repository liest. Dies erleichtert das Abrufen des Assets, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden sollen. Dies ähnelt einem HAL-Link, aber die Semantik ist einfacher und zweckmäßiger.
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience > decisioning > contents > components > content**

   **Feld:** content
   **Beschreibung:** Ein optionales Feld für die direkte Speicherung von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt enthalten. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen und binären Inhalten verwendet.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > deliveryURL**

   **Feld:** deliveryURL
   **Beschreibung:** Ein optionaler eindeutiger Locator für Ressourcen, der das Asset aus einem Inhaltsbereitstellungsnetzwerk oder einem Dienstendpunkt abruft. Diese URL wird verwendet, um von einem Benutzeragenten öffentlich auf das Asset zuzugreifen.
   **Typ:** Zeichenfolge
   **Beispiel:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **Feld:** linkURL
   **Beschreibung:** Ein optionaler eindeutiger Locator für Benutzerinteraktionen. Diese URL wird verwendet, um den Endbenutzer in einem Benutzeragenten auf zu verweisen und kann verfolgt werden.
   **Typ:** Zeichenfolge
   **Beispiel:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning > contents > Platzierung**

**Feld:** placement
**Titel:** Platzierung
**Beschreibung:** Eingehaltene Platzierung. Der Wert ist der URI (@id) der Angebotsplatzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
**Typ:** Zeichenfolge

#### _experience > decisioning > Lebenszyklusstatus

**Feld:** lifecycleStatus
**Titel:** Lebenszyklus-Status
**Beschreibung:** Der Lebenszyklusstatus ermöglicht die Ausführung von Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Diensten gesteuert, die die Objekte verwenden.
**Typ:** Zeichenfolge
**Mögliche Werte:** &quot;Entwurf&quot;(Standard), &quot;Genehmigt&quot;, &quot;Live&quot;, &quot;Abgeschlossen&quot;, &quot;Archiviert&quot;

#### _experience > decisioning > Decision Options Name

**Feld:** name
**Titel:** Name der Entscheidungsoption
**Beschreibung:** Optionsname, der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

#### _experience > decisioning > tags

**Feld:** tags
**Titel:** Tags
**Beschreibung:** Der Satz von Tags, die mit dieser Entität verknüpft sind. Die Tags werden in Filterausdrücken verwendet, um den Gesamtbestand auf eine Untergruppe (Kategorie) zu beschränken.
**Typ:** array

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**Feld:** _repo
**Typ:** Objekt

### _repo > Decision Option ETag

**Feld:** etag
**Titel:** Entscheidungsoption ETag
**Beschreibung:** Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt der Momentaufnahme befand.
**Typ:** Zeichenfolge
