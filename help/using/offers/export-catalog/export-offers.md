---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Datensatz für personalisierte Angebote
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Angebote verwendet werden
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ZnlEExKq7uM-qxcva2e0MxLFHXwGoW00axWjS-XaTZo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 873
ht-degree: 76%

---

# Datensatz für personalisierte Angebote {#offers-dataset}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Bei jeder Änderung eines Angebots wird der automatisch erstellte Datensatz für personalisierte Inhaltsangebote aktualisiert.

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

![](../assets/dataset-offers.png)

>[!NOTE]
>
>Gelöschte personalisierte Angebote werden im Datensatz als archiviert markiert.

Im Folgenden finden Sie eine Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – Personalisierte Angebote]** verwendet werden können.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ Kennung

**Feld:** _id
**title:** Kennung
**Beschreibung:** Eine eindeutige Kennung für den Datensatz.
**Type:** String

+++

+++ _experience {#experience}

**Feld:** _experience
**Typ:** Objekt

+++

+++ _experience > decisioning

**Feld:** decisioning
**Typ:** Objekt

+++

+++ _experience > decisioning > calendarConstraints 

**Feld:** calendarConstraints
**title:** Details zur Kalendereinschränkung
**Beschreibung:** Kalendereinschränkungen entscheiden, ob eine Entscheidungsoption für einen Datumsbereich gültig ist. Außerhalb dieses Datumsbereichs kann die Option nicht vorgeschlagen werden.
**Typ:** Objekt

* **Enddatum und -zeit**

  **Feld:** endDate
  **Titel:** Enddatum und -zeit
  **Beschreibung:** Das Enddatum der Gültigkeit einer Entscheidungsoption. Optionen, die ihr Enddatum überschritten haben, können im Entscheidungsprozess nicht mehr vorgeschlagen werden.
  **Typ:** Zeichenfolge

* **Startdatum und -zeit**

  **Feld:** startDate
  **Titel:** Startdatum und -zeit
  **Beschreibung:** Das Startdatum der Gültigkeit einer Entscheidungsoption. Optionen, deren Startdatum noch nicht erreicht wurde, können im Entscheidungsprozess noch nicht vorgeschlagen werden.
  **Typ:** Zeichenfolge

+++

+++ _experience > decisioning > characteristics

**Feld:** characteristics
**title:** Merkmale der Entscheidungsoption
**Beschreibung:** Merkmale sind die zusätzlichen Attribute oder Eigenschaften von Angeboten, die zu einer bestimmten Entscheidungsoption gehören. Bei diesen Attributen handelt es sich um Schlüssel-Wert-Paare, d. h. sie enthalten einen Attributnamen (manchmal auch als Schlüssel bezeichnet), dem ein Wert zugeordnet ist, und werden verwendet, um eine Entscheidungsoption von den anderen Angeboten zu unterscheiden. Beispiel: Für einen Attributnamen „color“ kann der Wert für ein bestimmtes Angebot „green“ lauten.<!--Characteristics are used as values in content that represents this decision option and as features to analyze and optimize the performance of an offer. When every instance has the same attribute or property, that aspect should be modeled as an extension schema that derives from the decision option detail.-->
**Typ:** Objekt

+++

+++ _experience > decisioning > contents

**Feld:** contents
**title:** Inhaltsdetails
**Beschreibung:** Inhaltselemente zum Rendern des Entscheidungselements in verschiedenen Kontexten. Eine einzelne Entscheidungsoption kann mehrere Inhaltsvarianten haben. Inhalte sind Informationen, die sich an eine Audience richten und in einem (digitalen) Erlebnis genutzt werden können. Inhalte werden über Kanäle in einer bestimmten Platzierung bereitgestellt.
**Typ:** Array

+++

+++_experience > decisioning > contents > components

**Feld:** components
**Beschreibung:** Die Komponenten des Inhalts, der die Entscheidungsoption einschließlich aller zugehörigen Sprachvarianten darstellt. Spezifische Komponenten werden durch „dx:format&quot;, „dc:subject&quot; und „dc:language&quot; oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um den mit einem Angebot verknüpften Inhalt zu finden oder darzustellen und ihn gemäß dem Platzierungsvertrag zu integrieren.
**Typ:** Array
**Erforderlich:** „_type“, „_dc“ <!--TBC?-->

+++

* **_experience > decisioning > contents > components > Content Component Type**

  **Feld:** _type
  **Titel:** Inhaltskomponententyp
  **Beschreibung:** Eine Auflistung von URIs, bei der jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente zugewiesen wurde. Einige Verbraucher der Inhaltsdarstellungen erwarten, dass der @type ein Verweis auf das Schema ist, das zusätzliche Eigenschaften der Inhaltskomponente beschreibt.
  **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > _dc**

  **Feld:** _dc
  **Typ:** Objekt
  **Erforderlich:** „format“

   * **Format**

     **Feld:** format
     **Titel:** Format
     **Beschreibung:** Die physische oder digitale Manifestation der Ressource. Normalerweise sollte das Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die für die Anzeige oder den Betrieb der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen, z. B. aus der Liste von [Internet-Medientypen](https://www.iana.org/assignments/media-types/), die Computer-Medienformate definieren.
     **Typ:** Zeichenfolge
     **Beispiel:** &quot;application/vnd.adobe.photoshop&quot;

   * **Sprache**
     **Feld:** language
     **Titel:** Sprache
     **Beschreibung:** Die Sprache(n) der Ressource. \nSprachen werden im Sprach-Code angegeben, wie in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) definiert. Dieser Standard ist Teil von BCP 47, der an anderer Stelle in XDM verwendet wird.
     **Typ:** Array
     **Beispiele:** „\n“, „pt-BR“, „es-ES“

* **_experience > decisioning > contents > components > _repo**

  **Feld:** _repo
  **Typ:** Objekt

   * **id**

     **Feld:** id
     **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Content-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client erwarten, dass eine zusätzliche Eigenschaft \„repo:resolveUrl\&quot; das Asset abruft.
     **Typ:** String
     **Beispiel:** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

     **Feld:** name
     **Beschreibung:** Einige Hinweise zum Speicherort des Repositorys, in dem das externe Asset durch „repo:id“ gespeichert wird.
     **Typ:** Zeichenfolge

   * **repositoryID**

     **Feld:** repositoryID
     **Beschreibung:** Eine optionale eindeutige Kennung, die auf das Asset in einem Content-Repository verweist. Wenn Platform-APIs zum Abrufen der Darstellung verwendet werden, kann der Client erwarten, dass eine zusätzliche Eigenschaft \„repo:resolveUrl\&quot; das Asset abruft.
     **Typ:** String
     **Beispiel:** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **Feld:** resolveURL
     **Beschreibung:** Ein optionaler eindeutiger Ressourcen-Locator zum Lesen des Assets in einem Content-Repository. Dadurch wird es einfacher, das Asset abzurufen, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden müssen. Dies ähnelt einem HAL-Link, die Semantik ist jedoch einfacher und zweckmäßiger.
     **Typ:** Zeichenfolge
     **Beispiel:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > decisioning > contents > components > content**

  **Feld:** content
  **Beschreibung:** Ein optionales Feld für die direkte Speicherung von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt speichern. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen oder binären Inhalten verwendet.
  **Typ:** Zeichenfolge

* **_experience > decisioning > contents > components > deliveryURL**

  **Feld:** deliveryURL
  **Beschreibung:** Ein optionaler eindeutiger Ressourcen-Locator, der das Asset über ein Content Delivery Network oder einen Service-Endpunkt abruft. Diese URL wird verwendet, um von einem Benutzeragenten öffentlich auf das Asset zuzugreifen.
  **Typ:** Zeichenfolge
  **Beispiel:** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

  **Feld:** linkURL
  **Beschreibung:** Eine optionale URL für Benutzerinteraktionen. Diese URL wird verwendet, um den Endbenutzer auf einen User Agent zu verweisen, und kann verfolgt werden.
  **Typ:** Zeichenfolge
  **Beispiel:** „https://cdn.adobe.io/tracker?code=23432&redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg“

+++_experience > decisioning > contents > Placement

**Feld:** placement
**title:** Platzierung
**Beschreibung:** Platzierung einzuhalten. Der Wert ist die URI (@id) der Angebotsplatzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
**Type:** String

+++

+++ _experience > decisioning > Lifecycle Status

**Feld:** lifecycleStatus
**title:** Lebenszyklusstatus
**Beschreibung:** Lebenszyklusstatus ermöglicht die Ausführung von Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Services gesteuert, die die Objekte verwenden.
**Type:** String
**Mögliche Werte:** „Entwurf“ (Standard), „Genehmigt“, „Live“, „Abgeschlossen“, „Archiviert“

+++

+++ _experience > decisioning > Decision Option Name

**Feld:** name
**title:** Name der Entscheidungsoption
**Beschreibung:** Optionsname, der in verschiedenen Benutzeroberflächen angezeigt wird.
**Type:** String

+++

+++ _experience > decisioning > profileConstraints

**Feld:** profileConstraints
**title:** Details zur Profilbegrenzung
**Beschreibung:** Die Profilbegrenzungen entscheiden, ob eine Option in diesem Kontext für diese Profil-ID geeignet ist. Wenn die Profilbegrenzung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h. sie gegenüber den Optionen aus der Optionsauswahl invariant ist, hebt die als „false“ ausgewertete Profilbegrenzung die gesamte Optionsauswahl auf. Dagegen wird eine Profileinschränkungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierte Option der Optionsauswahl ausgewertet.
**Typ:** Objekt

+++

+++_experience > decisioning > profileConstraints > Description

**Feld:** description
**Titel:** Beschreibung
**Beschreibung:** Beschreibung der Profileinschränkung. Sie dient dazu, für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Profilbegrenzung erstellt wurde und/oder welche Option von ihr eingeschlossen oder ausgeschlossen wird.
**Type:** String

+++

+++_experience > decisioning > profileConstraints > Eligibility Rule

**Feld:** eligibilityRule
**Titel:** Eignungsregel
**Beschreibung:** Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere kontextuelle XDM-Objekte als „true“ oder „false“ ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
**Type:** String

+++

+++_experience > decisioning > profileConstraints > Profile Constraint Type

**Feld:** profileConstraintType
**title:** Profileinschränkungstyp
**Beschreibung:** Bestimmt, ob aktuell Einschränkungen festgelegt sind und wie sie ausgedrückt werden. Dies kann durch eine Regel oder durch eine oder mehrere Zielgruppenzugehörigkeiten erfolgen.
**Type:** String
**Mögliche Werte:**

* „none“ (Standard)
* „eligibilityRule“: „Die Profileinschränkung wird als einzelne Regel ausgedrückt, die als „true“ ausgewertet werden muss, bevor die einschränkende Aktion zulässig ist.“
* „anySegments“: „Die Profileinschränkung wird als eine oder mehrere Zielgruppen ausgedrückt und das Profil muss mindestens einer dieser Zielgruppen angehören, damit die eingeschränkte Aktion zulässig ist.“
* „allSegments“: „Die Profileinschränkung wird als eine oder mehrere Zielgruppen ausgedrückt und das Profil muss allen Zielgruppen angehören, damit die eingeschränkte Aktion zulässig ist.“
* „rules“: „Die Profileinschränkung wird als eine Reihe verschiedener Regeln ausgedrückt, z. B. Gültigkeit, Anwendbarkeit, Eignung, die alle als „true“ ausgewertet werden müssen, bevor die eingeschränkte Aktion zulässig ist.“

+++

+++_experience > decisioning > profileConstraints > Segment Identifiers

**Feld:** segmentIdentities
**title:** Segmentkennungen
**Beschreibung:** Kennungen der Zielgruppen
**Typ:** Array

* **ID**

  **Feld:** _id
  **Titel:** Kennung
  **Beschreibung:** Identität der Zielgruppen im betreffenden Namespace.
  **Typ:** Zeichenfolge

* **Namespace**

  **Feld:** namespace
  **Titel:** Namespace
  **Beschreibung**: Der mit dem Attribut `xid` verknüpfte Namespace.
  **Typ:** Objekt
  **Erforderlich:** „code“

   * **Code**

     **Feld:** code
     **Titel:** Code
     **Beschreibung:** Der Code ist eine von Menschen lesbare Kennung für den Namespace und kann verwendet werden, um die technische Namespace-ID anzufordern, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.
     **Typ:** Zeichenfolge

* **Erlebnis-ID**

  **Feld:** xid
  **Titel:** Erlebnis-ID
  **Beschreibung:** Falls vorhanden, stellt dieser Wert eine Namespace-übergreifende Kennung dar, die unter allen Kennungen in allen Namespaces eindeutig ist.
  **Typ:** Zeichenfolge

+++

+++ _experience > decisioning > ranking

**Feld:** ranking
**title:** Ranking-Details
**Beschreibung:** Rang (Priorität). Definiert, was angesichts des Kontexts des Entscheidungskriteriums als die „beste Aktion“ gilt. Unter allen ausgewählten Optionen, die die Eignungsbegrenzung erfüllen, entscheidet die Rangfolge über die vorzuschlagenden Top-Optionen (oder Top-N).
**Typ:** Objekt

+++

+++_experience > decisioning > ranking > Order Evaluation

**Feld:** order
**Titel:** Evaluierung der Rangfolge
**Beschreibung:** Bewertung einer relativen Reihenfolge für eine oder mehrere Entscheidungsoptionen. Optionen mit höheren Ordinalzahlen werden vor Optionen mit niedrigeren Ordinalzahlen ausgewählt. Die durch diese Methode ermittelten Werte können sortiert werden, die Entfernungen zwischen ihnen können jedoch nicht gemessen werden, und es können weder Summen noch Produkte berechnet werden. Der Median und der Modus sind die einzigen Messwerte der zentralen Tendenz, die für ordinale Daten verwendet werden können.
**Typ:** Objekt

* **Scoring-Funktion**

  **Feld:** function
  **Titel:** Scoring-Funktion
  **Beschreibung:** Ein Verweis auf eine Funktion, die einen numerischen Wert für diese Entscheidungsoption berechnet. Die Entscheidungsoptionen werden dann nach diesem Wert sortiert (nach Rang geordnet). Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/function.
  **Typ:** Zeichenfolge

* **Reihenfolgenauswertungstyp**

  **Feld:** orderEvaluationType
  **Titel:** Reihenfolgenauswertungstyp
  **Beschreibung:** Gibt an, welcher Mechanismus zur Auswertung der Reihenfolge verwendet wird: eine statische Priorität von Entscheidungsoptionen, eine Scoring-Funktion, die für jede Option einen numerischen Wert berechnet, oder ein KI-Modell, das eine Liste erhält, um eine Sortierung vorzunehmen.
  **Typ:** Zeichenfolge
  **Mögliche Werte:** „static“, „scoringFunction“, „rankingStrategy“

* **Rangfolgestrategie**

  **Feld:** rankingStrategy
  **Titel:** Rangfolgestrategie
  **Beschreibung:** Ein Verweis auf eine Strategie, die eine Liste von Entscheidungsoptionen in eine Reihenfolge bringt. Entscheidungsoptionen werden in einer sortierten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Typ:** Zeichenfolge

+++

+++_experience > decisioning > ranking > Priority

**Feld:** priority
**Titel:** Priorität
**Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen, für die keine Reihenfolgenfunktion angegeben ist, werden mithilfe dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine Option nach dem Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
**type:** Integer
**Mindestwert:** 0
**Standardwert:** 0

+++

+++ _experience > decisioning > tags

**Feld:** Tags
**title:** Tags
**Beschreibung:** Die Gruppe von Sammlungsqualifizierern (ehemals als „Tags“ bezeichnet), die mit dieser Entität verknüpft sind. Die Sammlungsqualifizierer werden in Filterausdrücken verwendet, um den Gesamtbestand auf eine Teilmenge (Kategorie) einzuschränken.
**Typ:** Array

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**Feld:** _repo
**Typ:** Objekt

+++ 

+++ _repo > Decision Option ETag

**Feld:** eTag
**Titel:** E-Tag für Entscheidungsoption
**Beschreibung:** Die Überprüfung, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Speicherauszugs befand.
**Type:** String

+++
