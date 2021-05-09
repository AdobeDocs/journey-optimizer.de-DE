---
title: Erste Schritte mit dem Angebotskatalog-Export
description: In diesem Abschnitt werden alle im exportierten Datensatz für Entscheidungen verwendeten Felder Liste.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Entscheidungsdataset {#decisions-dataset}

Bei jeder Änderung eines Angebots wird der automatisch generierte Datensatz für Entscheidungen aktualisiert.

![](../assets/dataset-activities.png)

Der letzte erfolgreiche Stapel im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebot-Bibliothek zugreifen.

Die Entscheidungsfindung wird mithilfe einer Entscheidung (früher Angebot Decision) gesteuert. Er gibt den Filter an, der auf das Gesamtinventar angewendet wird, um die Angebot nach Thema/Kategorie einzugrenzen, die Platzierung, um das Inventar auf die Angebot einzuschränken, die technisch in den reservierten Bereich für das Angebot passen, und gibt eine Ausweichoption an, falls die kombinierten Beschränkungen alle verfügbaren PersonalisierungsAngebot ausschließen.

Im Folgenden finden Sie die Liste aller Felder, die im Dataset **[!UICONTROL Decision Object Repository - Decision]** (ehemals &quot;Decision Object Repository - Aktivitäten&quot;) verwendet werden können.

## Bezeichner

Eine eindeutige ID für den Datensatz.

Typ: Zeichenfolge

## _experience

### Entscheidungsfindung

#### Kriterien

Definiert einen Satz von Entscheidungskriterien, bei denen jeder eine Reihe von Einschränkungen enthält.

Typ: array

* **Beschreibung**

   Beschreibung des Kriteriums. Es wird verwendet, um für Menschen verständliche Absichten darüber zu vermitteln, wie oder warum dieses Kriterium aufgebaut wurde und wie es die Entscheidung beeinflusst.

   Typ: string

* **Auswahl der Optionen**

   Die Auswahl der Option definiert die Gültigkeit/Anwendbarkeit der Optionen in diesem Kontext.

   Typ: object

   * **Beschreibung**

      Beschreibung der Optionsauswahl. Es wird verwendet, um für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Option konstruiert wurde und/oder welche Option übereinstimmt.

      Typ: string

   * **Optionsfilter**

      Der Verweis auf einen Tag-basierten Filter, der die Optionen aus einem Bestand mit den angehängten Tags abgleicht. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/filter.

      Typ: string

   * **Profil-Beschränkungstyp**

      Bestimmt, ob Einschränkungen aktuell festgelegt sind und wie die Kontraste ausgedrückt werden. Es könnte über eine Filterfunktion oder über eine oder mehrere Segmentmitgliedschaften erfolgen.

      Typ: string

   * **Option Liste**

      Eine Liste, die die Optionen direkt angibt, ohne eine Filter-Abfrage zu bewerten. Es kann entweder eine Liste für Optionen oder eine Filterregel für Optionen angegeben werden.

      Typ: array

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option.-->

* **Platzierungen**

   Die Platzierungsbeschränkung besagt, dass dieses Kriterium nur für die aufgelisteten Platzierungen gilt. Nur wenn sich die Zielplatzierung in der Liste `xdm:placements` befindet, wird die Option ausgewählt. Andernfalls werden die gesamten Entscheidungskriterien übersprungen. Wenn die Liste &quot;xdm:placements&quot;ausgelassen oder leer ist, wird das Kriterium für jede zielgerichtete Platzierung berücksichtigt. Die hier aufgeführten Platzierungen stellen implizite Kriterien für die Auswahl der Option dar. Eine zu berücksichtigende Option muss für die zielgerichtete Platzierung repräsentativ sein.

   Typ: array

   * **Platzierungs-ID**

   Ein Verweis auf eine Platzierungsentität. Der Wert ist der URI (@id) der Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.

   Typ: string

* **Profil-Beschränkung**

   Die Profil-Beschränkung entscheidet, ob eine Optionsauswahl in diesem Moment für diese Profil-ID geeignet ist. Wenn die Profil-Beschränkung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h., sie ist von den Optionen aus der Optionsauswahl ungültig, wird die gesamte Optionsauswahl durch die Profil-Beschränkung, die als &quot;false&quot;ausgewertet wird, abgebrochen. Andererseits wird eine Profil-Beschränkungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierte Option der Optionsauswahl ausgewertet.

   Typ: object

   * **Beschreibung**

      Beschreibung der Profil-Beschränkung. Es wird verwendet, um für Menschen verständliche Absichten darüber zu vermitteln, wie oder warum diese Profil-Beschränkung aufgebaut wurde und/oder welche Option von ihr ausgeschlossen oder ausgeschlossen wird.

      Typ: string

   * **Eignungsregel**

      Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere kontextuelle XDM-Objekte als &quot;true&quot;oder &quot;false&quot;ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist der URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.

      Typ: string

   * **Profil-Beschränkungstyp**

      Bestimmt, ob Einschränkungen aktuell festgelegt sind und wie die Kontraste ausgedrückt werden. Es könnte eine Regel oder eine oder mehrere Segmentmitgliedschaften sein.

      Typ: string

      Mögliche Werte: &quot;none&quot;, &quot;permissionRule&quot;, &quot;anySegments&quot;, &quot;allSegments&quot;, &quot;rules&quot;

      Standardwert: &quot;none&quot;

   * **Segmentkennung**

      Bezeichner der Segmente

      Zeichenfolge: array

      * **Bezeichner**

         Identität des Segments im zugehörigen Namensraum.

         Typ: string

      * **Namensraum**

         Der mit dem Attribut `xid` verknüpfte Namensraum.

         Typ: object

         * **Code**

            Der Code ist ein für Menschen lesbarer Bezeichner für den Namensraum und kann verwendet werden, um die technische Namensraum-ID anzufordern, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.

            Typ: string
      * **Erlebnis-ID**

         Wenn dieser Wert vorhanden ist, stellt er eine Kennung für Namensraum dar, die in allen Namensräumen für alle Namensraum-Scoped-Bezeichner eindeutig ist.

         Typ: string


* **Rangdetails**

   Rang (Priorität). Definiert, wie die \&quot;beste Option\&quot; angesichts des Kontexts des Entscheidungskriteriums bestimmt wird. Unter allen ausgewählten Optionen, die den Einschränkungen des Profils entsprechen, entscheidet die Rangliste, welche Option(n) am oberen oder oberen Ende (n) vorgeschlagen werden soll.

   Typ: object

   * **Auftragsauswertung**

      Bewertung einer relativen Reihenfolge einer oder mehrerer Entscheidungsoptionen. Optionen mit höheren Ordinalwerten werden über allen Optionen mit niedrigeren Ordinalwerten ausgewählt. Die durch diese Methode bestimmten Werte können bestellt werden, die Entfernungen zwischen ihnen können jedoch nicht gemessen werden und es können weder Summen noch Produkte berechnet werden. Der Median und der Modus sind die einzigen Messgrößen der zentralen Tendenz, die für Ordinaldaten verwendet werden können.

      Typ: object

      * **Bewertungsfunktion**

         Ein Verweis auf eine Funktion, die eine numerische Bewertung für diese Entscheidungsoption berechnet. Die Entscheidungsoptionen werden dann nach diesem Ergebnis geordnet (geordnet). Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option &quot;on&quot;aufgerufen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/function.

         Typ: string

      * **Art der Auftragsauswertung**

         Gibt an, welcher Auftragsauswertungsmechanismus verwendet wird, welche statische Priorität der Entscheidungsoptionen verwendet wird, eine Bewertungsfunktion, die einen numerischen Wert für jede Option berechnet, oder eine Rangstrategie, die eine Liste zur Bestellung erhält.

         Typ: string

      * **Rangstrategie**

         Ein Verweis auf eine Strategie, die eine Liste der Entscheidungsoption einstuft. Die Entscheidungsoptionen werden in einer bestellten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option &quot;on&quot;aufgerufen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.

         Typ: string
   * **Versandpriorität**

      Die Priorität einer einzigen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen, für die keine Bestellfunktion angegeben wird, werden mit dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor den Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine nach dem gleichen Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.

      Typ: integer

      Mindestwert: 0

      Standardwert: 0


#### Enddatum und -zeit der Aktivität

Enddatum und Endzeit der Entscheidung. Eigenschaft hat die Semantik der Eigenschaft &#39;endTime&#39; von Schema.org, die auf http://schema.org/Action definiert ist.

Typ: string

#### Fallback-Option

Der Verweis auf eine Ausweichoption, die bei der Entscheidungsfindung im Rahmen dieser Entscheidung verwendet wird, stellt keine der regulären Optionen in Frage (dies geschieht normalerweise, wenn feste Beschränkungen angewendet werden). Der Wert ist der URI (@id) der Ausweichoption, auf die verwiesen wird.

Typ: string

#### Name der Aktivität

Entscheidungsname, der in verschiedenen Benutzeroberflächen angezeigt wird.

Typ: string

#### Datum und Uhrzeit des Beginns der Aktivität

Datum und Beginn der Entscheidung Eigenschaft hat die Semantik der Eigenschaft &quot;startTime&quot;von Schema.org, die auf http://schema.org/Action definiert ist.

Typ: string

## _repo

### Aktivität ETag

Die Revision, bei der sich das Entscheidungsobjekt zum Zeitpunkt der Snapshot-Erstellung befand.

Typ: string
