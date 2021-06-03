---
title: Datensatz für personalisierte Angebote
description: In diesem Abschnitt werden alle im exportierten Datensatz für Angebote verwendeten Felder aufgelistet.
source-git-commit: 57b6ffa4136eda80c41344db15d363d3107d4e32
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 87%

---

# Datensatz für personalisierte Angebote {#offers-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für personalisierte Content-Angebote aktualisiert.

![](../../assets/dataset-offers.png)

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebotsbibliothek zugreifen.

Hier sehen Sie die Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – personalisierte Angebote]** verwendet werden können.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## Kennung

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

#### _experience > decisioning > calendarConstraints

**Feld:** calendarConstraints 
**Titel:** Details zu Kalendereinschränkungen
**Beschreibung:** Kalendereinschränkungen entscheiden, ob eine Entscheidungsoption für einen Datumsbereich gültig ist. Außerhalb dieses Datumsbereichs kann die Option nicht angeboten werden.
**Typ: Objekt**

* **Enddatum und -uhrzeit**

   **Feld:** endDate
   **Titel:** Enddatum und -uhrzeit
   **Beschreibung:** Das Enddatum der Gültigkeit von Entscheidungsoptionen. Optionen, die ihr Enddatum überschritten haben, können nicht mehr für den Entscheidungsprozess angeboten werden.
   **Typ:** Zeichenfolge

* **Anfangsdatum und -uhrzeit**

   **Feld:** startDate
   **Titel:** Anfangsdatum und -uhrzeit
   **Beschreibung:** Das Anfangsdatum der Gültigkeit von Entscheidungsoptionen. Optionen, deren Anfangsdatum noch nicht erreicht wurde, können noch nicht für den Entscheidungsprozess angeboten werden.
   **Typ:** Zeichenfolge

#### _experience > decisioning > features

**Feld:** Merkmale
**Titel:** Entscheidungsoptionenmerkmale
**Beschreibung:** Weitere Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Merkmale aufweisen (Schlüssel in der Zuordnung). Bei den Merkmalen handelt es sich um Name-Wert-Paare, mit denen eine Option von anderen unterschieden wird. Merkmale werden in Inhalten als Werte verwendet, die diese Entscheidungsoption darstellen, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieses als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.
**Typ:** Objekt

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
   **Beschreibung:** Eine Auflistung von URIs, bei der jeder Wert einem Typ zugeordnet wird, der der Content-Komponente zugewiesen wurde. Einige Verbraucher der Content-Darstellungen erwarten, dass der Wert „@type“ ein Verweis auf das Schema ist, das zusätzliche Eigenschaften der Content-Komponente beschreibt.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > _dc**

   **Feld:** _dc
   **Typ:** Objekt
   **Erforderlich:** „format“

   * **Format**

      **Feld:** Format
      **Titel:** Format
      **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu ermitteln, die zum Anzeigen oder Verwenden der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (Beispiel: eine Liste mit [Internet-Medientypen](http://www.iana.org/assignments/media-types/), die Computer-Medienformate definieren).
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

#### _experience > decisioning > profileConstraints

**Feld:** profileConstraints 
**Titel:** Details zur Profilbegrenzung 
**Beschreibung:** Die Profilbegrenzungen bestimmen, ob eine Option in diesem Kontext für diese Profil-ID geeignet ist. Wenn die Profilbegrenzung die Werte der einzelnen Optionen nicht berücksichtigen muss und invariant gegenüber der Optionsauswahl ist, wird die gesamte Optionsauswahl durch die Profilbegrenzung, die als „false“ ausgewertet wird, abgebrochen. Andererseits wird eine Profilbegrenzungsregel, die eine Option als Parameter akzeptiert, für jede geeignete Option der Optionsauswahl ausgewertet.
**Typ:** Objekt

**_experience > decisioning > profileConstraints > Beschreibung**

**Feld:** description 
**Title:** Description 
**Description:** Beschreibung der Profilbegrenzung. Es wird verwendet, um für den Menschen lesbare Absichten zu vermitteln, wie oder warum diese Profilbegrenzung konstruiert wurde und/oder welche Option durch sie ein- oder ausgeschlossen wird.
**Typ:** Zeichenfolge

**_experience > decisioning > profileConstraints > Eignungsregel**

**Feld:** Eignungsregel-
**Titel:** Eignungsregel-
**Beschreibung:**  Ein Verweis auf eine Entscheidungsregel, der für ein bestimmtes Profil und/oder andere angegebene kontextbezogene XDM-Objekte als &quot;true&quot;oder &quot;false&quot;ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
**Typ:** Zeichenfolge

**_experience > decisioning > profileConstraints > Profil Constraint Type**

**Feld:** profileConstraintType 
**Title:** Profile Constraint Type 
**Description:** Bestimmt, ob aktuell Einschränkungen festgelegt sind und wie die Einschränkungen ausgedrückt werden. Es könnte durch eine Regel oder durch eine oder mehrere Segmentzugehörigkeiten erfolgen.
**Typ:** Zeichenfolge 
**Mögliche Werte:**
* &quot;none&quot;(Standard)
* „eligibilityRule“: „Die Profilbegrenzung wird als eine einzige Regel ausgedrückt, die als „true“ bewertet werden muss, bevor die eingeschränkte Aktion zulässig ist.“
* „anySegments“: „Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied von mindestens einem von ihnen sein, bevor die eingeschränkte Aktion zulässig ist.“
* „allSegments“: „Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied aller Segmente sein, bevor die eingeschränkte Aktion zulässig ist.“
* „rules“: „Die Profilbegrenzung wird als eine Reihe unterschiedlicher Regeln ausgedrückt, z. B. Eignung, Anwendbarkeit, Zweckmäßigkeit, die alle als „true“ bewertet werden müssen, bevor die eingeschränkte Aktion zulässig ist.“

**_experience > decisioning > profileConstraints > Segment Identifiers**

**Feld:** segmentIdentities 
**Title:** Segment Identifiers 
**Description:** Identifiers of the segments 
**Type:** array

* **ID**

   **Feld:** _id
   **Titel:** Kennung
   **Beschreibung:** Identität des Segments im betreffenden Namespace.
   **Typ:** Zeichenfolge

* **Namespace**

   **Feld:** Namespace
   **Titel:** Namespace
   **Beschreibung:** Der mit dem Attribut `xid` verknüpfte Namespace.
   **Typ:** Objekt
   **Erforderlich:** „Code“

   * **Code**

      **Feld:** Code
      **Titel:** Code
      **Beschreibung:** Der Code ist eine für den Menschen lesbare Kennung für den Namespace und kann verwendet werden, um die technische Namespace-ID anzufordern, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.
      **Typ:** Zeichenfolge

* **Erlebnis-ID**

   **Feld:** xid
   **Titel:** Erlebnis-ID
   **Beschreibung:** Falls vorhanden, stellt dieser Wert eine Namespace-übergreifenden Kennung dar, die über alle Kennungen in allen Namespaces eindeutig ist.
   **Typ:** Zeichenfolge

#### _experience > decisioning > ranking

**Feld:** ranking 
**Titel:** Ranking-Details 
**Beschreibung:** Rangfolge (Priorität) Definiert, was im jeweiligen Kontext des Entscheidungskriteriums als \&quot;beste Aktion\&quot; gilt. Unter allen ausgewählten Optionen im Rahmen der Eignungsbegrenzung entscheidet die Rangfolge über die beste(n) (oder Top-N) Option(en), die vorgeschlagen werden soll(en).
**Typ:** Objekt

**_experience > decisioning > ranking > order Evaluation**

**Feld:** order 
**Title:** Order Evaluation 
**Description:** Bewertung einer relativen Reihenfolge einer oder mehrerer Entscheidungsoptionen. Optionen mit höheren Ordinalwerten werden vor allen Optionen mit niedrigeren Ordinalwerten ausgewählt. Die mit dieser Methode ermittelten Werte können geordnet werden, aber Abstände zwischen ihnen können nicht gemessen werden und es können weder Summen noch Produkte berechnet werden. Der Median und der Modus sind die einzigen Maße der zentralen Tendenz, die für ordinale Daten verwendet werden können.
**Typ:** Objekt

* **Scoring-Funktion**

   **Feld:** Funktion
   **Titel:** Scoring-Funktion
   **Beschreibung:** Ein Verweis auf eine Funktion, die einen numerischen Punktwert für diese Entscheidungsoption berechnet. Die Entscheidungsoptionen werden dann nach diesem Punktwert geordnet (gereiht). Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die mit jeweils einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/function.
   **Typ:** Zeichenfolge

* **Reihenfolgenbewertungstyp**

   **Feld:** orderEvaluationType
   **Titel:** Reihenfolgenbewertungstyp
   **Beschreibung:** Gibt an, welcher Mechanismus zur Bewertung der Reihenfolge verwendet wird, welche statische Priorität der Entscheidungsoptionen verwendet wird, eine Scoring-Funktion, die einen numerischen Wert für jede Option berechnet, oder eine Rangfolgestrategie, die eine Liste zum Ordnen erhält.
   **Typ:** Zeichenfolge
   **Mögliche Werte:** „static“, „scoringFunction“, „rankingStrategy“

* **Rangfolgestrategie**

   **Feld:** rankingStrategy
   **Titel:** Rangfolgestrategie
   **Beschreibung:** Ein Verweis auf eine Strategie, die eine Liste mit Entscheidungsoptionen in eine Rangfolge bringt. Die Entscheidungsoptionen werden in einer geordneten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die mit jeweils einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
   **Typ:** Zeichenfolge

**_experience > decisioning > ranking > Priority**

**Feld:** Priorität 
**Titel:** Priorität 
**Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen, für die keine Ordnungsfunktion angegeben ist, werden mit dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor den Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine davon nach dem Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
**Typ:** integer 
**Minimum value:** 0 
**Standardwert:** 0

#### _experience > decisioning > tags

**Feld:** tags 
**Titel:** Tags 
**Beschreibung:** Der Satz von Tags, die dieser Entität zugeordnet sind. Die Tags werden in Filterausdrücken verwendet, um den Bestand auf eine Teilmenge (Kategorie) zu begrenzen.
**Typ: Array**

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Feld:** _repo
**Typ:** Objekt

### _repo > Decision Option ETag

**Feld:** eTag
**Titel:** Entscheidungsoption ETag
**Beschreibung:** Die Revision, in der sich das Objekt der Entscheidungsoption befand, als der Schnappschuss erstellt wurde.
**Typ:** Zeichenfolge



