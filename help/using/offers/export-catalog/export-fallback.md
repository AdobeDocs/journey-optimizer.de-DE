---
title: Datensatz für Fallback-Angebote
description: In diesem Abschnitt werden alle Felder, die im exportierten Datensatz für Fallback-Angebote verwendet werden, aufgelistet.
source-git-commit: b6364879b2a64ba17f52020f7d27d02459a022b0
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 90%

---

# Datensatz für Fallback-Angebote {#fallback-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für Fallback-Angebote aktualisiert.

![](../../assets/dataset-fallback.png)

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebotsbibliothek zugreifen können.

Hier finden Sie die Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – Fallback-Angebote]** verwendet werden können.

## ID

**Feld:** _id
**Titel:** Kennung 
**Beschreibung:** Eine eindeutige Kennung für den Eintrag.
**Typ:** Zeichenfolge

## _Erlebnis

**Feld:** _Erlebnis 
**Typ:** Objekt

### _experience > decisioning

**Feld:** Entscheidungsfindung 
**Typ:** Objekt

#### _experience > decisioning > features

**Feld:** Merkmale
**Titel:** Entscheidungsoptionenmerkmale
**Beschreibung:** Weitere Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Merkmale aufweisen (Schlüssel in der Zuordnung). Bei den Merkmalen handelt es sich um Name-Wert-Paare, mit denen eine Option von anderen unterschieden wird. Merkmale werden in Inhalten als Werte verwendet, die diese Entscheidungsoption darstellen, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieses als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.
**Typ:** Objekt

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### _experience > decisioning > contents

**Feld:** Inhalt 
**Titel:** Inhaltsdetails
**Beschreibung:** Inhaltselemente, um das Entscheidungselement in verschiedenen Kontexten zu rendern. Eine einzelne Entscheidungsoption kann mehrere Inhaltsvarianten haben. Der Inhalt ist eine Information, die auf eine Zielgruppe für den Verbrauch in einem (digitalen) Erlebnis ausgerichtet ist. Der Inhalt wird über Kanäle an eine bestimmte Platzierung gesendet.
**Typ:** Array

**_experience > decisioning > contents > components**

**Feld:** components 
**Description:** Die Komponenten des Inhalts, die die Entscheidungsoption darstellen, einschließlich aller zugehörigen Sprachvarianten. Spezifische Komponenten werden durch „dx:format“, „dc:subject“ und „dc:language“ oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um die mit einem Angebot verknüpften Inhalte zu suchen oder darzustellen und sie gemäß dem Platzierungsvertrag zu integrieren.
**Typ:** Array 
**erforderlich:**  &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

* **_experience > decisioning > contents > components > Content Component Type**

   **Feld:** _Typ
   **Titel:** Typ der Inhaltskomponente
   **Beschreibung:** Ein aufgelisteter Satz von URIs bei dem jeder Wert einem Typ zugeordnet ist, der der Inhaltskomponente zugewiesen wurde. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der Wert „@type“ ein Verweis auf das Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > _dc**

   **Feld:** _dc
   **Typ:** Objekt
   **Erforderlich:** „format“

   * **Format**

      **Feld:** Format
      **Titel:** Format
      **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu ermitteln, die zum Anzeigen oder Verwenden der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen, z. B. aus der Liste von [Internet-Medientypen](http://www.iana.org/ assignments/media-types/), die Computermedienformate definieren.
      **Typ:** Zeichenfolge
      **Beispiel:** „application/vnd.adobe.photoshop“

   * **Sprache**

      **Feld:** Sprache
      **Titel:** Sprache
      **Beschreibung:** Die Sprache oder Sprachen der Ressource. \nSprachen werden im Sprachcode angegeben, wie er in der Norm [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) definiert ist, die Teil von BCP 47 ist, die an anderer Stelle in XDM verwendet wird.
      **Typ:** Array
      **Beispiele:** „\n“, „pt-BR“, „es-ES“

* **_experience > decisioning > contents > components > _repo**

   **Feld:** _repo
   **Typ:** Objekt

   * **id**

      **Feld:** id
      **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.
      **Typ:** Zeichenfolge
      **Beispiel:** „urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e“

   * **name**

      **Feld:** Name
      **Beschreibung:** Einige Hinweise zum Speicherort des Repositorys, in dem das externe Asset durch die \&quot;repo:id\&quot; gespeichert wird.
      **Typ:** Zeichenfolge

   * **repositoryID**

      **Feld:** repositoryID
      **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.
      **Typ:** Zeichenfolge
      **Beispiel:** „C87932A55B06F7070A49412D@AdobeOrg“

   * **resolveURL**

      **Feld:** resolveURL
      **Beschreibung:** Ein optionaler eindeutiger Ressourcen-Locator zum Lesen des Assets in einem Inhalts-Repository. Dadurch wird es einfacher, das Asset abzurufen, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden müssen. Dies ist ähnlich wie ein HAL-Link, aber die Semantik ist einfacher und zweckmäßiger.
      **Typ:** Zeichenfolge
      **Beispiel:** „https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;“

* **_experience > decisioning > contents > components > content**

   **Feld:** Inhalt
   **Beschreibung:** Ein optionales Feld zum direkten Speichern von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt aufnehmen. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen und binären Inhalten verwendet.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > deliveryURL**

   **Feld:** deliveryURL
   **Beschreibung:** Ein optionaler eindeutiger Ressourcen-Locator, um das Asset von einem Content Delivery Network (CDN) oder Service-Endpunkt zu beziehen. Diese URL wird verwendet, um von einem User Agent aus öffentlich auf das Asset zuzugreifen.
   **Typ:** Zeichenfolge
   **Beispiel:** „https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg“

* **_experience > decisioning > contents > components > linkURL**

   **Feld:** linkURL
   **Beschreibung:** Ein optionaler eindeutiger Ressourcen-Locator für Benutzerinteraktionen. Diese URL wird verwendet, um in einem User Agent auf den Endbenutzer zu verweisen und kann nachverfolgt werden.
   **Typ:** Zeichenfolge
   **Beispiel:** „https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg“

**_experience > decisioning > contents > Platzierung**

**Feld:** placement 
**Title:** Placement 
**Description:** Platzierung, die einzuhalten ist. Der Wert ist der URI (@id) der Angebotsplatzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
**Typ:** Zeichenfolge

#### _Erlebnis > Entscheidung > Lebenszyklusstatus

**Feld:** Lebenszyklusstatus
**Titel:** Lebenszyklusstatus 
**Beschreibung:** Der Lebenszyklusstatus ermöglicht die Durchführung von Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Services gesteuert, die die Objekte verwenden.
**Typ:** Zeichenfolge 
**Mögliche Werte:** &quot;Entwurf&quot; (Standard), &quot;Genehmigt&quot;, &quot;Live&quot;, &quot;Abgeschlossen&quot;, &quot;Archiviert&quot;

#### _experience > decisioning > Decision Options Name

**Feld:** Name 
**Title:** Name der Entscheidungsoption 
**Beschreibung:** Optionsname, der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

#### _experience > decisioning > tags

**Feld:** Tags
**Titel:** Tags 
**Beschreibung:** Der Satz von Tags, die dieser Entität zugeordnet sind. Die Tags werden in Filter-Ausdrücken verwendet, um den Gesamtbestand auf eine Untergruppe (Kategorie) einzuschränken.
**Typ:** Array

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Feld:** _repo
**Typ:** Objekt

### _repo > Decision Option ETag

**Feld:** eTag
**Titel:** Entscheidungsoption ETag
**Beschreibung:** Die Revision, in der sich das Objekt der Entscheidungsoption befand, als der Schnappschuss erstellt wurde.
**Typ:** Zeichenfolge
