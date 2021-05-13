---
title: Fallback-Angebote-Datensatz
description: In diesem Abschnitt werden alle Felder, die im exportierten Datensatz für Fallback-Angebot verwendet werden, Liste.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 7%

---

# Fallback-Angebote-Datensatz {#fallback-dataset}

Bei jeder Änderung eines Angebots wird der automatisch generierte Datensatz für Ausweichdaten aktualisiert.

![](../../assets/dataset-fallback.png)

Der letzte erfolgreiche Stapel im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebot-Bibliothek zugreifen.

Hier finden Sie die Liste aller Felder, die im Dataset **[!UICONTROL Decision Object Repository - Fallback Angebots]** verwendet werden können.

## ID

**Feld:** _id 
**Title:** Identifier 
**Description:** Eine eindeutige Kennung für den Datensatz.
**Typ:** Zeichenfolge

## _Erlebnis

**Feld:** _experience 
**Type:** Objekt

### Entscheidungsfindung

**Feld:** Entscheidungstyp 
**:** Objekt

#### Merkmale

**Feld:** Merkmale 
**Titel:** Entscheidungsoptionenmerkmale 
**Beschreibung:** Weitere Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Eigenschaften aufweisen (Schlüssel in der Zuordnung). Bei den Eigenschaften handelt es sich um Namenswertpaare, mit denen eine Entscheidungsoption von anderen unterschieden wird. Eigenschaften werden als Werte im Inhalt verwendet, der diese Entscheidungsoption darstellt, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieses als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.
**Typ:** Objekt

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### Inhalt

**Feld:** Inhaltstitel 
**:** Inhaltsdetails 
**Beschreibung:** Inhaltselemente, um das Entscheidungselement in verschiedenen Kontexten wiederzugeben. Eine einzelne Entscheidungsoption kann mehrere Inhaltsvarianten haben. Der Inhalt ist eine Information, die auf eine Audience für den (digitalen) Verbrauch ausgerichtet ist. Die Inhalte werden über Kanal an eine bestimmte Stelle gesendet.
**Typ:** Array

* **Komponenten**

   **Feld:** Komponenten
   **Beschreibung:** Die Komponenten des Inhalts, die die Entscheidungsoption einschließlich aller zugehörigen Sprachvarianten darstellen. Spezifische Komponenten werden durch &quot;dx:format&quot;, &quot;dc:subject&quot;und &quot;dc:language&quot;oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um die mit einem Angebot verknüpften Inhalte zu suchen oder darzustellen und sie gemäß dem Platzierungsvertrag zu integrieren.
   **Typ:** Array
   **Erforderlich:** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **Content Component Type**

      **Feld:** _type
      **Titel:** Inhaltskomponententyp
      **Beschreibung:** Ein aufgezählter Satz von URIs, bei dem jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente angegeben wurde. Einige Benutzer der Inhaltsdarstellungen erwarten, dass der Wert &quot;@type&quot;ein Verweis auf Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.
      **Typ:** Zeichenfolge

   * **_dc**

      **Feld:** _dc
      **Typ:** Objekt
      **Erforderlich:** &quot;format&quot;

      * **Format**

         **Feld:** Format
         **Titel:** Format
         **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu ermitteln, die zum Anzeigen oder Verwenden der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (z. B. die Liste von [Internet Media Types](http://www.iana.org/ zuweisungen/media-types/), die Computermedienformate definiert).
         **Typ:** Zeichenfolge
         **Beispiel:** &quot;application/vnd.adobe.photoshop&quot;

      * **Sprache**

         **Feld:** Sprache
         **Titel:** Sprache
         **Beschreibung:** Die Sprache oder Sprachen der Ressource. \nSprachen werden im Sprachcode wie in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) definiert, der Teil von BCP 47 ist, der an anderer Stelle in XDM verwendet wird.
         **Typ:** Array
         **Beispiele:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      **Feld:** _repo
      **Typ:** Objekt

      * **id**

         **Feld:** id
         **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Plattform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.
         **Typ:** Zeichenfolge
         **Beispiel:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **name**

         **Feld:** Name
         **Beschreibung:** Einige Hinweise zum Speicherort des Repositorys, in dem das externe Asset durch \&quot;repo:id\&quot; gespeichert wird.
         **Typ:** Zeichenfolge

      * **repositoryID**

         **Feld:** repositoryID
         **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Plattform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.
         **Typ:** Zeichenfolge
         **Beispiel:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **Feld:** resolveURL
         **Beschreibung:** Ein optionaler eindeutiger Ressourcenstandort zum Lesen des Assets in einem Inhalts-Repository. Dadurch wird es einfacher, das Asset abzurufen, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden müssen. Dies ist ähnlich wie ein HAL-Link, aber die Semantik ist einfacher und zweckmäßiger.
         **Typ:** Zeichenfolge
         **Beispiel:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;
   * **content**

      **Feld:** Inhalt
      **Beschreibung:** Ein optionales Feld zum direkten Speichern von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt aufnehmen. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen und binären Inhalten verwendet.
      **Typ:** Zeichenfolge

   * **deliveryURL**

      **Feld:** deliveryURL
      **Beschreibung:** Ein optionaler eindeutiger Ressourcenstandort, der das Asset über einen Content Versand-Netzwerk- oder -Dienstendpunkt abruft. Diese URL wird von einem Benutzeragent verwendet, um auf das Asset öffentlich zuzugreifen.
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **Feld:** linkURL
      **Beschreibung:** Ein optionaler eindeutiger Ressourcenstandort für Benutzerinteraktionen. Diese URL wird verwendet, um den Endbenutzer in einem Benutzeragent zu verweisen und kann verfolgt werden.
      **Typ:** Zeichenfolge
      **Beispiel:** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **Platzierung**

   **Feld:** Platzierung
   **Titel:** Platzierung
   **Beschreibung:** Platzierung, die einzuhalten ist. Der Wert ist der URI (@id) der Angebotsplatzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
   **Typ:** Zeichenfolge

#### Lebenszyklusstatus

**Feld:** Lebenszyklusstatus 
**Titel:** Lebenszyklusstatus 
**Beschreibung:** Lebenszyklusstatus ermöglicht die Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Diensten gesteuert, die die Objekte verwenden.
**Typ:** Zeichenfolge 
**Mögliche Werte:** &quot;Entwurf&quot;, &quot;Genehmigt&quot;, &quot;Live&quot;, &quot;Abgeschlossen&quot;, &quot;Archiviert&quot;, 
**Standardwert:** &quot;Entwurf&quot;

#### Name der Entscheidungsoption

**Feld:** name 
**Title:** Decision Options Name 
**Description:** Optionsname, der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

#### Tags

**Feld:** Tags 
**Titel:** Tags 
**Beschreibung:** Der Satz von Tags, die dieser Entität zugeordnet sind. Die Tags werden in Filter-Ausdrücken verwendet, um den Gesamtbestand auf eine Untergruppe (Kategorie) zu beschränken.
**Typ:** Array

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

### Entscheidungsoption ETag

**Feld:** Tag-
**Titel:** Entscheidungsoption ETag-
**Beschreibung:** Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Snapshots befand.
**Typ:** Zeichenfolge
