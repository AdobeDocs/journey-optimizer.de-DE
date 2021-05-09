---
title: Fallback-Angebote-Datensatz
description: In diesem Abschnitt werden alle Felder, die im exportierten Datensatz für Fallback-Angebot verwendet werden, Liste.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Fallback-Angebote-Datensatz {#fallback-dataset}

Bei jeder Änderung eines Angebots wird der automatisch generierte Datensatz für Ausweichdaten aktualisiert.

![](../assets/dataset-fallback.png)

Der letzte erfolgreiche Stapel im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebot-Bibliothek zugreifen.

Hier finden Sie die Liste aller Felder, die im Dataset **[!UICONTROL Decision Object Repository - Fallback Angebots]** verwendet werden können.

## Bezeichner

Eine eindeutige ID für den Datensatz.

Typ: Zeichenfolge

## _experience

### Entscheidungsfindung

#### Merkmale

**Merkmale** der Entscheidungsoption. Zusätzliche Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Eigenschaften aufweisen (Schlüssel in der Zuordnung). Bei den Eigenschaften handelt es sich um Namenswertpaare, mit denen eine Entscheidungsoption von anderen unterschieden wird. Eigenschaften werden als Werte im Inhalt verwendet, der diese Entscheidungsoption darstellt, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieses als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.

Typ: object

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### Inhalt

**Inhaltsdetails**. Inhaltselemente, um das Entscheidungselement in verschiedenen Kontexten wiederzugeben. Eine einzelne Entscheidungsoption kann mehrere Inhaltsvarianten haben. Der Inhalt ist eine Information, die auf eine Audience für den (digitalen) Verbrauch ausgerichtet ist. Die Inhalte werden über Kanal an eine bestimmte Stelle gesendet.

Typ: array

* **components**

   Die Komponenten des Inhalts, die die Entscheidungsoption darstellen, einschließlich aller zugehörigen Sprachvarianten. Spezifische Komponenten werden durch &quot;dx:format&quot;, &quot;dc:subject&quot;und &quot;dc:language&quot;oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um die mit einem Angebot verknüpften Inhalte zu suchen oder darzustellen und sie gemäß dem Platzierungsvertrag zu integrieren.

   Typ: array

   * **Content Component Type**

      Ein aufgezählter Satz von URIs, bei dem jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente angegeben wurde. Einige Benutzer der Inhaltsdarstellungen erwarten, dass der Wert &quot;@type&quot;ein Verweis auf Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.

      Typ: string

   * **_dc**

      * **Format**

         Die physische oder digitale Manifestation der Ressource. Normalerweise sollte Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zum Anzeigen oder Betrieb der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (z. B. die Liste von [Internet Media Types](http://www.iana.org/ zuweisungen/media-types/), die Computermedienformate definiert).

         Typ: string

      * **Sprache**

         Die Sprache oder Sprachen der Ressource.\nSprachen werden im Sprachcode wie in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) definiert, der Teil von BCP 47 ist, der an anderer Stelle in XDM verwendet wird.

         Typ: string
   * **_repo**

      * **id**

         Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Plattform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.

         Typ: string

      * **name**

         Einige Hinweise dazu, wo das Repository zu finden ist, in dem das externe Asset durch \&quot;repo:id\&quot; gespeichert wird.

         Typ: string

      * **repositoryID**

         Eine optionale eindeutige Kennung, die auf das Asset in einem Inhalts-Repository verweist. Wenn Plattform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client mit einer zusätzlichen Eigenschaft \&quot;repo:resolveUrl\&quot; rechnen, um das Asset abzurufen.

         Typ: string

      * **resolveURL**

         Eine optionale eindeutige Ressourcensuche zum Lesen des Assets in einem Inhalts-Repository. Dadurch wird es einfacher, das Asset zu erhalten, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden. Dies ist ähnlich wie ein HAL-Link, aber die Semantik ist einfacher und zielgerichteter.

         Typ: string
   * **content**

      Ein optionales Feld zum direkten Speichern von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt aufnehmen. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen und binären Inhalten verwendet.

      Typ: string

   * **deliveryURL**

      Eine optionale eindeutige Ressourcensuche, um das Asset von einem Content Versand-Netzwerk- oder Dienstendpunkt abzurufen. Diese URL wird von einem Benutzeragent verwendet, um auf das Asset öffentlich zuzugreifen.

      Typ: string

   * **linkURL**

      Eine optionale eindeutige Ressourcensuche für Benutzerinteraktionen. Diese URL wird verwendet, um den Endbenutzer in einem Benutzeragent zu verweisen und kann verfolgt werden.

      Typ: string



* **Platzierung**

   Anordnung zur Einhaltung. Der Wert ist der URI (@id) der Angebot-Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.

   Typ: string



#### Lebenszyklusstatus

Der Lebenszyklusstatus ermöglicht die Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Diensten gesteuert, die die Objekte verwenden.

Typ: string

Mögliche Werte: &quot;draft&quot;, &quot;authorised&quot;, &quot;live&quot;, &quot;completed&quot;, &quot;archived&quot;

Standardwert: &quot;draft&quot;

#### Name der Entscheidungsoption

Optionsname, der in verschiedenen Benutzeroberflächen angezeigt wird.

Typ: string

#### Tags

Der Satz von Tags, die dieser Entität zugeordnet sind. Die Tags werden in Filter-Ausdrücken verwendet, um den Gesamtbestand auf eine Untergruppe (Kategorie) zu beschränken.

Typ: array

## _repo

### Entscheidungsoption ETag

Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Snapshots befand.

Typ: string
