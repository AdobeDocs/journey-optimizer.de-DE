---
title: Datensatz für personalisierte Angebote
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Angebote verwendet werden
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1951'
ht-degree: 0%

---

# Datensatz für personalisierte Angebote {#offers-dataset}

Bei jeder Änderung eines Angebots wird der automatisch erstellte Datensatz für personalisierte Inhaltsangebote aktualisiert.

![](../assets/dataset-offers.png)

Der zuletzt erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>Erfahren Sie, wie Sie für jedes Objekt Ihrer Angebotsbibliothek in auf die exportierten Datensätze zugreifen können. [diesem Abschnitt](../export-catalog/access-dataset.md).

Im Folgenden finden Sie eine Liste aller Felder, die im **[!UICONTROL Decision Object Repository - Personalized Offers]** Datensatz.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

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

#### _experience > decisioning > calendarConstraints

**Feld:** calendarConstraints
**Titel:** Details zur Kalenderbegrenzung
**Beschreibung:** Durch kalendarische Begrenzungen wird bestimmt, ob eine Entscheidungsoption für einen Datumsbereich gültig ist. Außerhalb dieses Datumsbereichs kann die Option nicht vorgeschlagen werden.
**Typ:** Objekt

* **Enddatum und -zeit**

   **Feld:** endDate
   **Titel:** Enddatum und -zeit
   **Beschreibung:** Das Enddatum einer Entscheidungsoptionen ist gültig. Optionen, die ihr Enddatum überschritten haben, können nicht mehr im Entscheidungsprozess vorgeschlagen werden.
   **Typ:** Zeichenfolge

* **Startdatum und -zeit**

   **Feld:** startDate
   **Titel:** Startdatum und -zeit
   **Beschreibung:** Das Anfangsdatum einer Entscheidungsoptionen ist gültig. Optionen, deren Startdatum noch nicht erreicht ist, können noch nicht im Entscheidungsprozess vorgeschlagen werden.
   **Typ:** Zeichenfolge

#### _experience > decisioning > features

**Feld:** Merkmale
**Titel:** Entscheidungsoptionseigenschaften
**Beschreibung:** Zusätzliche Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Merkmale aufweisen (Schlüssel in der Zuordnung). Die Merkmale sind Namenswertpaare, mit denen eine Entscheidungsoption von anderen unterschieden wird. Eigenschaften werden als Werte im Inhalt verwendet, der diese Entscheidungsoption darstellt, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieser Aspekt als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.
**Typ:** Objekt

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
   **Beschreibung:** Ein Auflistungssatz von URIs, bei dem jeder Wert einem Typ zugeordnet ist, der der Inhaltskomponente angegeben ist. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der @type-Wert ein Verweis auf das Schema ist, das zusätzliche Eigenschaften der Inhaltskomponente beschreibt.
   **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > _dc**

   **Feld:** _dc
   **Typ:** Objekt
   **Erforderlich:** &quot;format&quot;

   * **Format**

      **Feld:** format
      **Titel:** Format
      **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zum Anzeigen oder Betreiben der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (z. B. aus der Liste der [Internet-Medientypen](http://www.iana.org/assignments/media-types/) Computermedienformate definieren).
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

#### _experience > decisioning > profileConstraints

**Feld:** profileConstraints
**Titel:** Profilbegrenzungsdetails
**Beschreibung:** Die Profilbegrenzungen bestimmen, ob eine Option in diesem Kontext für diese Profilidentität geeignet ist. Wenn die Profilbegrenzung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h. sie invariant für die Optionen aus der Optionsauswahl ist, hebt die als &quot;false&quot;ausgewertete Profilbegrenzung die gesamte Optionsauswahl ab. Andererseits wird eine Profilbegrenzungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierende Option der Optionsauswahl ausgewertet.
**Typ:** Objekt

**_experience > decisioning > profileConstraints > Beschreibung**

**Feld:** description
**Titel:** Beschreibung
**Beschreibung:** Beschreibung der Profilbegrenzung. Sie wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Profilbegrenzung erstellt wurde und/oder welche Option von ihr einbezogen oder ausgeschlossen werden soll.
**Typ:** Zeichenfolge

**_experience > decisioning > profileConstraints > Eignungsregel**

**Feld:** permissionRule
**Titel:** Eignungsregel
**Beschreibung:** Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere angegebene kontextbezogene XDM-Objekte als &quot;true&quot;oder &quot;false&quot;ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
**Typ:** Zeichenfolge

**_experience > decisioning > profileConstraints > Profil Constraint Type**

**Feld:** profileConstraintType
**Titel:** Profilbegrenzungstyp
**Beschreibung:** Bestimmt, ob derzeit Einschränkungen festgelegt sind und wie die Begrenzungen ausgedrückt werden. Dies kann durch eine Regel oder durch ein oder mehrere Segmentmitgliedschaften erfolgen.
**Typ:** Zeichenfolge
**Mögliche Werte:**
* &quot;none&quot;(Standard)
* &quot;permissionRule&quot;: &quot;Die Profilbegrenzung wird als einzelne Regel ausgedrückt, die als &quot;true&quot;ausgewertet werden muss, bevor die eingeschränkte Aktion zulässig ist.&quot;
* &quot;anySegments&quot;: &quot;Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied mindestens eines dieser Segmente sein, bevor die eingeschränkte Aktion zulässig ist.&quot;
* &quot;allSegments&quot;: &quot;Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied aller sein, bevor die eingeschränkte Aktion zulässig ist.&quot;
* &quot;rules&quot;: &quot;Die Profilbegrenzung wird als eine Reihe verschiedener Regeln ausgedrückt, z. B. Eignung, Anwendbarkeit, Eignung, die alle als &quot;true&quot;bewertet werden müssen, bevor die eingeschränkte Aktion zulässig ist.&quot;

**_experience > decisioning > profileConstraints > Segment Identifiers**

**Feld:** segmentIdentities
**Titel:** Segment-IDs
**Beschreibung:** Kennungen der Segmente
**Typ:** array

* **Kennung**

   **Feld:** _id
   **Titel:** Kennung
   **Beschreibung:** Identität des Segments im zugehörigen Namespace.
   **Typ:** Zeichenfolge

* **Namespace**

   **Feld:** namespace
   **Titel:** Namespace
   **Beschreibung:** Der mit dem `xid` -Attribut.
   **Typ:** Objekt
   **Erforderlich:** &quot;code&quot;

   * **Code**

      **Feld:** code
      **Titel:** Code
      **Beschreibung:** Der Code ist eine für Menschen lesbare Kennung für den Namespace und kann zum Anfordern der technischen Namespace-ID verwendet werden, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.
      **Typ:** Zeichenfolge

* **Erlebnis-ID**

   **Feld:** xid
   **Titel:** Erlebnis-ID
   **Beschreibung:** Wenn dieser Wert vorhanden ist, stellt er eine Namespace-übergreifende Kennung dar, die über alle Namespaces hinweg eindeutigen Bezeichner eindeutig ist.
   **Typ:** Zeichenfolge

#### _experience > decisioning > ranking

**Feld:** Ranking
**Titel:** Rangdetails
**Beschreibung:** Rang (Priorität). Definiert, was angesichts des Kontexts des Entscheidungskriteriums als \&quot;beste Aktion\&quot; gilt. Unter allen ausgewählten Optionen, die die Eignungsbegrenzung erfüllen, entscheidet die Rangordnung über die vorzuschlagenden Top-Optionen (oder Top-N).
**Typ:** Objekt

**_experience > decisioning > ranking > order Evaluation**

**Feld:** order
**Titel:** Bestellauswertung
**Beschreibung:** Bewertung einer relativen Reihenfolge einer oder mehrerer Entscheidungsoptionen. Optionen mit höheren Ordinalwerten werden über allen Optionen mit niedrigeren Ordinalwerten ausgewählt. Die durch diese Methode ermittelten Werte können geordnet werden, die Entfernungen zwischen ihnen können jedoch nicht gemessen werden und weder Summen noch Produkte können berechnet werden. Der Median und der Modus sind die einzigen Messwerte der zentralen Tendenz, die für ordinale Daten verwendet werden können.
**Typ:** Objekt

* **Scoring-Funktion**

   **Feld:** function
   **Titel:** Scoring-Funktion
   **Beschreibung:** Ein Verweis auf eine Funktion, die einen numerischen Wert für diese Entscheidungsoption berechnet. Entscheidungsoptionen werden dann nach diesem Ergebnis sortiert (nach Rang geordnet). Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option &quot;on&quot;aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/function.
   **Typ:** Zeichenfolge

* **Bestellauswertungstyp**

   **Feld:** orderEvaluationType
   **Titel:** Bestellauswertungstyp
   **Beschreibung:** Gibt an, welcher Mechanismus zur Bewertung der Reihenfolge verwendet wird, welche statische Priorität der Entscheidungsoptionen verwendet wird, welche Scoring-Funktion einen numerischen Wert für jede Option berechnet oder welche Rangstrategie eine Liste erhält, um sie zu ordnen.
   **Typ:** Zeichenfolge
   **Mögliche Werte:** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* **Ranking Strategy**

   **Feld:** rankingStrategy
   **Titel:** Ranking Strategy
   **Beschreibung:** Ein Verweis auf eine Strategie, die eine Liste von Entscheidungsoptionen angibt. Entscheidungsoptionen werden in einer geordneten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option &quot;on&quot;aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
   **Typ:** Zeichenfolge

**_experience > decisioning > ranking > Priority**

**Feld:** priority
**Titel:** Priorität
**Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Vergleich zu allen anderen Optionen. Optionen, für die keine Bestellfunktion angegeben ist, werden mithilfe dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine nach dem einheitlichen Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
**Typ:** integer
**Mindestwert:** 0
**Standardwert:** 0

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
