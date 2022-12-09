---
title: Entscheidungsdatensatz
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Entscheidungen verwendet werden
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 0%

---

# Entscheidungsdatensatz {#decisions-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch erstellte Datensatz für Entscheidungen (ehemals Aktivitäten) aktualisiert.

![](../assets/dataset-activities.png)

Der zuletzt erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>Erfahren Sie, wie Sie für jedes Objekt Ihrer Angebotsbibliothek in auf die exportierten Datensätze zugreifen können. [diesem Abschnitt](../export-catalog/access-dataset.md).

Im Folgenden finden Sie eine Liste aller Felder, die im **[!UICONTROL Decision Object Repository - Decisions]** Datensatz (früher als Entscheidungsobjekt-Repository - Aktivitäten bezeichnet).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

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

#### _experience > decisioning > kriterien

**Feld:** Kriterien
**Titel:** Kriterien
**Beschreibung:** Definiert einen Satz von Entscheidungskriterien, bei denen jeder eine Reihe von Einschränkungen enthält.
**Typ:** array

**_experience > decisioning > kriterien > description**

**Feld:** description
**Titel:** Beschreibung
**Beschreibung:** Beschreibung des Kriteriums. Sie wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum dieses Kriterium konstruiert wurde und wie es die Entscheidung beeinflusst.
**Typ:** Zeichenfolge

**_experience > decisioning > kriterien > optionSelection**

**Feld:** optionSelection
**Titel:** Auswahl der Optionen
**Beschreibung:** Die Option Auswahl definiert die Gültigkeit/Anwendbarkeit der Optionen in diesem Kontext.
**Typ:** Objekt

* **Beschreibung**

   **Feld:** description
   **Titel:** Beschreibung
   **Beschreibung:** Beschreibung der Optionsauswahl. Sie wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Option erstellt wurde und/oder welche Option übereinstimmt.
   **Typ:** Zeichenfolge

* **Optionsfilter**

   **Feld:** filter
   **Titel:** Optionsfilter
   **Beschreibung:** Der Verweis auf einen Tag-basierten Filter, der anhand der angehängten Tags Optionen aus einem Inventar abgleicht. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/filter.
   **Typ:** Zeichenfolge

* **Profilbegrenzungstyp**

   **Feld:** optionSelectionType
   **Titel:** Profilbegrenzungstyp
   **Beschreibung:** Bestimmt, ob derzeit Einschränkungen festgelegt sind und wie die Begrenzungen ausgedrückt werden. Dies kann über eine Filterabfrage oder durch eine oder mehrere Segmentmitgliedschaften erfolgen.
   **Typ:** Zeichenfolge
   **Mögliche Werte:** &quot;none&quot;(Standard), &quot;directList&quot;, &quot;filter&quot;

* **Optionsliste**

   **Feld:** options
   **Titel:** Optionsliste
   **Beschreibung:** Eine Liste, die die Optionen direkt angibt, ohne eine Filterabfrage zu bewerten. Es kann entweder eine Optionsliste oder eine Optionsfilterregel angegeben werden.
   **Typ:** array

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experience > decisioning > Kriterien > Platzierungen**

**Feld:** Platzierungen
**Titel:** Platzierungsbeschränkungen
**Beschreibung:** Die Platzierungsbegrenzung besagt, dass dieses Kriterium nur für die aufgelisteten Platzierungen gilt. Nur, wenn sich die Targeting-Platzierung in der `xdm:placements` list ist die berücksichtigte Optionsauswahl. Andernfalls werden die gesamten Entscheidungskriterien übersprungen. Wenn die Liste &quot;xdm:placements&quot;ausgelassen oder leer ist, wird das Kriterium für jede zielgerichtete Platzierung berücksichtigt. Die hier aufgeführten Platzierungen setzen implizite Kriterien für die Optionsauswahl voraus. Eine zu berücksichtigende Option muss über eine Darstellung für die zielgerichtete Platzierung verfügen.
**Typ:** array

* **Platzierungskennung**

   **Titel:** Platzierungskennung
   **Beschreibung:** Ein Verweis auf eine Platzierungsentität. Der Wert ist der URI (@id) der Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
   **Typ:** Zeichenfolge

**_experience > decisioning > kriterien > profileConstraints**

**Feld:** profileConstraints
**Titel:** Profilbegrenzung
**Beschreibung:** Die Profilbegrenzung entscheidet in diesem Zusammenhang, ob eine Optionsauswahl für diese Profilidentität geeignet ist. Wenn die Profilbegrenzung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h. sie invariant für die Optionen aus der Optionsauswahl ist, hebt die als &quot;false&quot;ausgewertete Profilbegrenzung die gesamte Optionsauswahl ab. Andererseits wird eine Profilbegrenzungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierende Option der Optionsauswahl ausgewertet.
**Typ:** Objekt

* **_experience > decisioning > Kriterien > profileConstraints > Beschreibung**

   **Feld:** description
   **Titel:** Beschreibung
   **Beschreibung:** Beschreibung der Profilbegrenzung. Sie wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Profilbegrenzung erstellt wurde und/oder welche Option von ihr einbezogen oder ausgeschlossen werden soll.
   **Typ:** Zeichenfolge

* **_experience > decisioning > kriterien > profileConstraints > Eignungsregel**

   **Feld:** permissionRule
   **Titel:** Eignungsregel
   **Beschreibung:** Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere angegebene kontextbezogene XDM-Objekte als &quot;true&quot;oder &quot;false&quot;ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
   **Typ:** Zeichenfolge

* **_experience > decisioning > kriterien > profileConstraints > Profil Constraint Type**

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

* **_experience > decisioning > kriterien > profileConstraints > segmentIdentities**

   **Feld:** segmentIdentities
   **Titel:** Segment-IDs
   **Beschreibung:** Kennungen der Segmente.
   **Typ:** array

   * **Kennung**

      **Feld:** _id
      **Titel:** Kennung
      **Beschreibung:** Identität des Segments im zugehörigen Namespace.
      **Typ:** Zeichenfolge

   * **namespace**

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


**_experience > decisioning > kriterien > rang**

**Feld:** Ranking
**Titel:** Rangdetails
**Beschreibung:** Rang (Priorität). Definiert, wie die \&quot;beste Option\&quot;im Kontext des Entscheidungskriteriums bestimmt wird. Unter allen ausgewählten Optionen, die die Profilbegrenzungen erfüllen, entscheidet das Ranking über die vorzuschlagenden Top-Optionen (oder Top-N).
**Typ:** Objekt

* **_experience > decisioning > kriterien > ranking > order**

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

* **_experience > decisioning > kriterien > ranking > priority**

   **Feld:** priority
   **Titel:** Priorität
   **Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Vergleich zu allen anderen Optionen. Optionen, für die keine Bestellfunktion angegeben ist, werden mithilfe dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine nach dem einheitlichen Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
   **Typ:** integer
   **Mindestwert:** 0
   **Standardwert:** 0

#### _experience > decisioning > Activity End Date and Time

**Feld:** endTime
**Titel:** Enddatum und -zeit der Aktivität
**Beschreibung:** Enddatum und Endzeit der Entscheidung (ehemals &quot;Aktivität&quot;). Die Eigenschaft hat die Semantik der Eigenschaft &quot;endTime&quot;von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

#### _experience > decisioning > Fallback-Option

**Feld:** Fallback
**Titel:** Fallback-Option
**Beschreibung:** Der Verweis auf eine Ausweichoption, die bei der Entscheidungsfindung im Kontext dieser Entscheidung verwendet wird, qualifiziert keine der regulären Optionen (dies geschieht normalerweise bei Anwendung von Hardbounce-Beschränkungen). Der Wert ist der URI (@id) der Fallback-Option, auf die verwiesen wird.
**Typ:** Zeichenfolge

#### _experience > decisioning > Activity Name

**Feld:** name
**Titel:** Aktivitätsname
**Beschreibung:** Entscheidungsname (ehemals &quot;Aktivität&quot;), der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

#### _experience > decisioning > Activity Start Date and Time

**Feld:** startTime
**Titel:** Anfangsdatum und -zeit der Aktivität
**Beschreibung:** Start- und Endzeit der Entscheidung (ehemals &quot;Aktivität&quot;). Die Eigenschaft hat die Semantik der Eigenschaft &quot;startTime&quot;von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

## _repo {#repo}

**Feld:** _repo
**Typ:** Objekt

### _repo > Activity ETag

**Feld:** etag
**Titel:** Aktivitäts-ETag
**Beschreibung:** Die Revision, die das Entscheidungsobjekt (ehemals &quot;activity&quot;) zum Zeitpunkt der Momentaufnahme war.
**Typ:** Zeichenfolge
