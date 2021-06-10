---
title: Erste Schritte mit dem Exportieren eines Angebotskatalogs
description: In diesem Abschnitt werden alle im exportierten Datensatz für Entscheidungen verwendeten Felder aufgelistet.
source-git-commit: 95be47fbf6944f7e6a743056b6cc29b45ae291fe
workflow-type: tm+mt
source-wordcount: '1554'
ht-degree: 83%

---

# Entscheidungsdatensatz {#decisions-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch erstellte Datensatz für Entscheidungen (ehemals Aktivitäten) aktualisiert.

![](../../assets/dataset-activities.png)

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebotsbibliothek zugreifen.

Im Folgenden finden Sie die Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – Entscheidungen]** (ehemals „Entscheidungsobjekt-Repository – Aktivitäten“) verwendet werden können.

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

## Kennung

**Feld:** _id
**Titel:** Kennung
**Beschreibung:** Eindeutige Kennung des Datensatzes.
**Typ:** Zeichenfolge

## _experience

**Feld:** _experience 
**Typ:** Objekt

### _experience > decisioning

**Feld:** decisioning
**Typ:** Objekt

#### _experience > decisioning > kriterien

**Feld:** Kriterien
**Titel:** Kriterien
**Beschreibung:** Definiert einen Satz von Entscheidungskriterien, bei denen jede eine Reihe von Einschränkungen enthält.
**Typ: Array**

**_experience > decisioning > kriterien > description**

**Feld:** description 
**Title:** Description 
**Description:** Kriterienbeschreibung Es wird verwendet, um für den Menschen lesbare Absichten zu vermitteln, wie oder warum dieses Kriterium konstruiert wurde und wie es sich auf die Entscheidung auswirkt.
**Typ:** Zeichenfolge

**_experience > decisioning > kriterien > optionSelection**

**Feld:** optionSelection 
**Title:** Option Selection 
**Description:** Die Optionsauswahl definiert die Gültigkeit/Anwendbarkeit von Optionen in diesem Kontext.
**Typ: Objekt**

* **Beschreibung**

   **Feld:** description
   **Titel:** Beschreibung
   **Beschreibung:** Beschreibung der Optionsauswahl. Wird verwendet, um für den Menschen lesbare Absichten zu vermitteln, wie oder warum diese Optionsauswahl konstruiert wurde und/oder welche Option am besten passt.
   **Typ:** Zeichenfolge

* **Optionsfilter**

   **Feld:** filter
   **Titel:** Optionsfilter
   **Beschreibung:** Der Verweis auf einen Tag-basierten Filter, der Optionen aus einem Bestand anhand ihrer beigefügten Tags zuordnet. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/filter.
   **Typ:** Zeichenfolge

* **Profilbegrenzungstyp**

   **Feld:** optionSelectionType
   **Titel:**Profilbegrenzungstyp
   **Beschreibung:** Bestimmt, ob Begrenzungen derzeit aktiv sind und in welcher Form die Begrenzungen definiert sind. Es kann über eine Filterabfrage oder über eine oder mehrere Segmentzugehörigkeiten erfolgen.
   **Typ:** Zeichenfolge
   **Mögliche Werte:** &quot;none&quot;(Standard), &quot;directList&quot;, &quot;filter&quot;

* **Optionsliste**

   **Feld:** options
   **Titel:** Optionsliste
   **Beschreibung:** Eine Liste, die die Optionen direkt angibt, ohne eine Filterabfrage auszuwerten. Es kann entweder eine Optionsliste oder eine Optionsfilterregel angegeben werden.
   **Typ: Array**

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experience > decisioning > Kriterien > Platzierungen**

**Feld:** Platzierungstitel 
**:** Platzierungsbeschränkungen 
**Beschreibung:** Die Platzierungsbegrenzung gibt an, dass dieses Kriterium nur für die aufgelisteten Platzierungen gilt. Nur wenn sich die Zielplatzierung in der Liste `xdm:placements` befindet, wird die Optionsauswahl berücksichtigt. Andernfalls werden die gesamten Entscheidungskriterien übersprungen. Wenn die Liste „xdm:placements“ ausgelassen wird oder leer ist, wird das Kriterium für jede Zielplatzierung berücksichtigt. Die hier aufgeführten Platzierungen stellen implizite Kriterien für die Optionsauswahl dar. Eine zu berücksichtigende Option muss für die Zielplatzierung repräsentativ sein.
**Typ: Array**

* **Platzierungs-ID**

   **Titel:** Platzierungs-ID
   **Beschreibung:** Ein Verweis auf eine Platzierungsentität. Der Wert ist der URI (@id) der Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
   **Typ:** Zeichenfolge

**_experience > decisioning > kriterien > profileConstraints**

**Feld:** profileConstraints 
**Title:** Profile Constraint 
**Description:**  Die Profilbegrenzung entscheidet, ob eine Optionsauswahl in diesem Moment, in diesem Kontext, für diese Profilidentität geeignet ist. Wenn die Profilbegrenzung die Werte der einzelnen Optionen nicht berücksichtigen muss und invariant gegenüber der Optionsauswahl ist, wird die gesamte Optionsauswahl durch die Profilbegrenzung abgebrochen, die als „false“ ausgewertet wird. Andererseits wird eine Profilbegrenzungsregel, die eine Option als Parameter akzeptiert, für jede geeignete Option der Optionsauswahl ausgewertet.
**Typ: Objekt**

* **_experience > decisioning > Kriterien > profileConstraints > Beschreibung**

   **Feld:** description
   **Titel:** Beschreibung
   **Beschreibung:** Beschreibung der Profilbegrenzung. Die Beschreibung soll in für Menschen verständlicher Form vermitteln, wie oder warum diese Profilbegrenzung erstellt wurde und/oder welche Option ein- oder ausgeschlossen wird.
   **Typ:** Zeichenfolge

* **_experience > decisioning > kriterien > profileConstraints > Eignungsregel**

   **Feld:** eligibilityRule
   **Titel:** Eignungsregel
   **Beschreibung:** Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere kontextuelle XDM-Objekte als „true“ oder „false“ ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob eine Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
   **Typ:** Zeichenfolge

* **_experience > decisioning > kriterien > profileConstraints > Profil Constraint Type**

   **Feld:** profileConstraintType
   **Titel:**Profilbegrenzungstyp
   **Beschreibung:** Bestimmt, ob Begrenzungen derzeit aktiv sind und in welcher Form die Begrenzungen definiert sind. Begrenzungen können durch eine Regel oder durch eine oder mehrere Segmentzugehörigkeiten festgelegt sein.
   **Typ:** Zeichenfolge
   **Mögliche Werte:**
   * „none“ (Standard)
   * „eligibilityRule“: „Die Profilbegrenzung wird als eine einzige Regel ausgedrückt, die als „true“ ausgewertet werden muss, bevor die eingeschränkte Aktion zulässig ist.“
   * „anySegments“: „Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss mindestens einem Segment angehören, damit die begrenzte Aktion zulässig ist.“
   * „allSegments“: „Die Profilbegrenzung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss allen Segmenten angehören, damit die eingeschränkte Aktion zulässig ist.“
   * „rules“: „Die Profilbegrenzung wird als eine Reihe von verschiedenen Regeln ausgedrückt, wie Qualifizierung, Anwendbarkeit, Eignung, die alle als „true“ ausgewertet werden müssen, damit die eingeschränkte Aktion zulässig ist.“

* **_experience > decisioning > kriterien > profileConstraints > segmentIdentities**

   **Feld:** segmentIdentities
   **Titel:** Segmentkennungen
   **Beschreibung:** Kennungen der Segmente.
   **Typ: Array**

   * **ID**

      **Feld:** _id
      **Titel:** Kennung
      **Beschreibung:** Identität des Segments im betreffenden Namespace.
      **Typ:** Zeichenfolge

   * **namespace**

      **Feld:** namespace
      **Titel:** Namespace
      **Beschreibung:** Der mit dem `xid`-Attribut verknüpfte Namespace.
      **Typ: Objekt**
      **Erforderlich:** „code“

      * **Code**

         **Feld:** code
         **Titel:** Code
         **Beschreibung:** Der Code ist eine von Personen lesbare Kennung für den Namespace und kann verwendet werden, um die technische Namespace-ID anzufordern, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.
         **Typ:** Zeichenfolge
   * **Erlebniskennung**

      **Feld:** xid
      **Titel:** Erlebniskennung
      **Beschreibung:** Falls vorhanden, stellt dieser Wert eine Namespace-übergreifenden Kennung dar, die über alle Kennungen in allen Namespaces eindeutig ist.
      **Typ:** Zeichenfolge


**_experience > decisioning > kriterien > rang**

**Feld:** ranking 
**Titel:** Ranking-Details 
**Beschreibung:** Rangfolge (Priorität) Definiert, wie die „beste Option“ angesichts des Kontexts des Entscheidungskriteriums bestimmt wird. Unter allen ausgewählten Optionen, die den Profilbegrenzungen entsprechen, entscheidet die Rangfolge über die beste oder die besten n Optionen, die vorgeschlagen werden.
**Typ: Objekt**

* **_experience > decisioning > kriterien > ranking > order**

   **Feld:** order
   **Titel:** Evaluierung der Rangfolge
   **Beschreibung:** Evaluierung einer relativen Rangfolge von einer oder mehreren Entscheidungsoptionen. Optionen mit höheren Ordinalwerten werden vor allen Optionen mit niedrigeren Ordinalwerten ausgewählt. Die durch diese Methode ermittelten Werte können sortiert werden, die Abstände zwischen den Werten lassen sich jedoch nicht bestimmen und es können weder Summen noch Produkte berechnet werden. Der Medianwert und der Modus sind als einzige Messgrößen der zentralen Tendenz für Ordinaldaten verfügbar.
   **Typ: Objekt**

   * **Scoring-Funktion**

      **Feld:** function
      **Titel:** Scoring-Funktion
      **Beschreibung:** Ein Verweis auf eine Funktion, die ein numerisches Scoring für diese Entscheidungsoption berechnet. Die Entscheidungsoptionen werden dann entsprechend diesem Ergebnis geordnet (sortiert). Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option „on“ aufgerufen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/function.
      **Typ:** Zeichenfolge

   * **Typ der Rangfolgenevaluierung**

      **Feld:** orderEvaluationType
      **Titel:** Typ der Rangfolgenevaluierung
      **Beschreibung:** Bestimmt den Mechanismus zur Evaluierung der Rangfolge, die statische Priorität der Entscheidungsoptionen, eine Scoring-Funktion, die einen numerischen Wert für jede Option berechnet, oder eine Strategie zur Bestimmung der Rangfolge, die auf eine Liste angewendet wird.
      **Typ:** Zeichenfolge
      **Mögliche Werte:** „static“, „scoringFunction“, „rankingStrategy“

   * **Ranking-Strategie**

      **Feld:** rankingStrategy
      **Titel:** Ranking-Strategie
      **Beschreibung:** Ein Verweis auf eine Strategie, die eine Liste der Entscheidungsoption nach ihrer Rangfolge sortiert. Die Entscheidungsoptionen werden in einer sortierten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option „on“ aufgerufen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
      **Typ:** Zeichenfolge

* **_experience > decisioning > kriterien > ranking > priority**

   **Feld:** priority
   **Titel:** Priorität
   **Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen ohne definierte Rangfolgen-Funktion werden anhand dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor den Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine Option nach demselben Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
   **Typ:** integer
   **Mindestwert:** 0
   **Standardwert:** 0

#### _experience > decisioning > Activity End Date and Time

**Feld:** endTime 
**Title:** Activity End Date and Time 
**Description:** Enddatum und Endzeit der Entscheidung (ehemals &quot;activity&quot;). Die Eigenschaft hat die Semantik der Eigenschaft „endTime“ von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

#### _experience > decisioning > Fallback-Option

**Feld:** fallback 
**Titel:** Fallback-Option 
**Beschreibung:** Der Verweis auf eine Fallback-Option, die bei der Entscheidung im Kontext dieser Entscheidung verwendet wird, qualifiziert keine der regulären Optionen (dies geschieht typischerweise, wenn harte Begrenzungen angewendet werden). Der Wert ist der URI (@id) der Fallback-Option, auf die verwiesen wird.
**Typ:** Zeichenfolge

#### _experience > decisioning > Activity Name

**Feld:** name 
**Title:** Activity Name 
**Description:** Entscheidungsname (ehemals &quot;activity&quot;), der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

#### _experience > Entscheidung > Anfangsdatum und -zeit der Aktivität

**Feld:** startTime 
**Title:** Activity Start Date and Time 
**Description:** Entscheidung (ehemals &quot;activity&quot;) Startdatum und Endzeit. Die Eigenschaft hat die Semantik der Eigenschaft „startTime“ von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

## _repo

**Feld:** _repo-
**Typ:** Objekt

### _repo > Activity ETag

**Feld:** Tag-
**Titel:** Activity ETag-
**Beschreibung:** Die Überarbeitung, die das Entscheidungsobjekt (ehemals &quot;activity&quot;) zum Zeitpunkt der Momentaufnahme vorgenommen wurde.
**Typ:** Zeichenfolge
