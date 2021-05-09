---
title: Datenbestand zu personalisierten Angeboten
description: In diesem Abschnitt werden alle im exportierten Datensatz für Angebot verwendeten Felder Liste.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1794'
ht-degree: 0%

---

# Personalisierte Angebot-Dataset {#offers-dataset}

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für personalisierte Content-Angebot aktualisiert.

![](../assets/dataset-offers.png)

Der letzte erfolgreiche Stapel im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt ](../export-catalog/access-dataset.md) erfahren Sie, wie Sie auf die exportierten Datensätze für die einzelnen Objekte Ihrer Angebot-Bibliothek zugreifen.

Personalisierte Angebot bilden die Entscheidungsgrundlage. Ziel der Entscheidungsfindung ist es, eine große Bestandsaufnahme der Elemente vorzunehmen und zahlreiche Einschränkungen auf dieses Inventar anzuwenden, um es einzuschränken und dann die qualifizierten Optionen nach einem Kriterium einzustufen. Die resultierenden Vorschläge stellen das Erlebnis für bestimmte Personen zusammen und personalisieren es.

Hier finden Sie die Liste aller Felder, die im Dataset **[!UICONTROL Decision Object Repository - Personalized Angebots]** verwendet werden können.

## Bezeichner

Eine eindeutige ID für den Datensatz.
Typ: Zeichenfolge

## _experience

### Entscheidungsfindung

#### calendarConstraints

**Kalendereinschränkungsdetails**. Kalenderbeschränkungen entscheiden, ob eine Entscheidungsoption für einen Datumsbereich gültig ist. Außerhalb dieses Datumsbereichs kann die Option nicht vorgeschlagen werden.
Typ: object

* **Enddatum und -zeit**

   Das Enddatum einer Entscheidungsoption ist gültig. Optionen, die ihr Enddatum überschritten haben, können nicht mehr im Entscheidungsprozess vorgeschlagen werden.

   Typ: string

* **Beginn - Datum und Uhrzeit**

   Das Datum des Beginns der Gültigkeit der Entscheidungsoptionen. Optionen, deren Beginn noch nicht erreicht wurde, können noch nicht im Entscheidungsprozess vorgeschlagen werden.

   Typ: string

#### Merkmale

**Merkmale** der Entscheidungsoption. Zusätzliche Eigenschaften oder Attribute, die zu dieser bestimmten Entscheidungsoption gehören. Verschiedene Instanzen können unterschiedliche Eigenschaften aufweisen (Schlüssel in der Zuordnung). Bei den Eigenschaften handelt es sich um Namenswertpaare, mit denen eine Entscheidungsoption von anderen unterschieden wird. Eigenschaften werden als Werte im Inhalt verwendet, der diese Entscheidungsoption darstellt, und als Funktionen zur Analyse und Optimierung der Leistung einer Option. Wenn jede Instanz dasselbe Attribut oder dieselbe Eigenschaft hat, sollte dieses als Erweiterungsschema modelliert werden, das sich aus den Details der Entscheidungsoptionen ableitet.

Typ: object

#### Inhalt

**Inhaltsdetails**. Inhaltselemente, um das Entscheidungselement in verschiedenen Kontexten wiederzugeben. Eine einzelne Entscheidungsoption kann mehrere Inhaltsvarianten haben. Der Inhalt ist eine Information, die auf eine Audience für den (digitalen) Verbrauch ausgerichtet ist. Die Inhalte werden über Kanal an eine bestimmte Stelle gesendet.

Typ: array

* ****
KomponentenDie Komponenten des Inhalts, die die Entscheidungsoption einschließlich aller zugehörigen Sprachvarianten darstellen. Spezifische Komponenten werden durch &quot;dx:format&quot;, &quot;dc:subject&quot;und &quot;dc:language&quot;oder eine Kombination daraus gefunden. Diese Metadaten werden verwendet, um die mit einem Angebot verknüpften Inhalte zu suchen oder darzustellen und sie gemäß dem Platzierungsvertrag zu integrieren.

   * **Content Component**
TypeEin aufgezählter Satz von URIs, bei denen jeder Wert einem Typ zugeordnet wird, der der Inhaltskomponente angegeben wurde. Einige Benutzer der Inhaltsdarstellungen erwarten, dass der Wert &quot;@type&quot;ein Verweis auf Schema ist, in dem zusätzliche Eigenschaften der Inhaltskomponente beschrieben werden.
Typ: string

   * **_dc**

      * ****
FormatDie physische oder digitale Manifestation der Ressource. Normalerweise sollte Format den Medientyp der Ressource enthalten. Das Format kann verwendet werden, um die Software, Hardware oder andere Geräte zu bestimmen, die zum Anzeigen oder Betrieb der Ressource erforderlich sind. Es wird empfohlen, einen Wert aus einem kontrollierten Vokabular auszuwählen (z. B. die Liste von [Internet Media Types](http://www.iana.org/ zuweisungen/media-types/), die Computermedienformate definiert).

         Typ: string

         Beispiel: &quot;application/vnd.adobe.photoshop&quot;

      * ****
SpracheDie Sprache oder Sprachen der Ressource.\nSprachen werden im Sprachcode wie in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) definiert, der Teil von BCP 47 ist, der an anderer Stelle in XDM verwendet wird.

         Typ: string

         Beispiele: &quot;/n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
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

         Beispiel: &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         Eine optionale eindeutige Ressourcensuche zum Lesen des Assets in einem Inhalts-Repository. Dadurch wird es einfacher, das Asset zu erhalten, ohne dass der Client weiß, wo das Asset verwaltet wird und welche APIs aufgerufen werden. Dies ist ähnlich wie ein HAL-Link, aber die Semantik ist einfacher und zielgerichteter.

         Typ: string

         Beispiel: &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&amp;quot&quot;
   * **content**

      Ein optionales Feld zum direkten Speichern von Inhalten. Anstatt auf Inhalte in einem Asset-Repository zu verweisen, kann die Komponente einfache Inhalte direkt aufnehmen. Dieses Feld wird nicht für Assets mit zusammengesetzten, komplexen und binären Inhalten verwendet.

      Typ: string

   * **deliveryURL**

      Eine optionale eindeutige Ressourcensuche, um das Asset von einem Content Versand-Netzwerk- oder Dienstendpunkt abzurufen. Diese URL wird von einem Benutzeragent verwendet, um auf das Asset öffentlich zuzugreifen.

      Typ: string

      Beispiel: &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      Eine optionale eindeutige Ressourcensuche für Benutzerinteraktionen. Diese URL wird verwendet, um den Endbenutzer in einem Benutzeragent zu verweisen und kann verfolgt werden.

      Typ: string

      Beispiel: &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg



* **Platzierung**

   Anordnung zur Einhaltung. Der Wert ist der URI (@id) der Angebot-Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.

#### Lebenszyklusstatus

Der Lebenszyklusstatus ermöglicht die Workflows mit einem Objekt. Der Status kann sich auf die Sichtbarkeit oder Relevanz eines Objekts auswirken. Statusänderungen werden von den Clients oder Diensten gesteuert, die die Objekte verwenden.
Typ: string
Mögliche Werte: Entwurf, Genehmigt, Live, Abgeschlossen, Archiviert

#### Name der Entscheidungsoption

Optionsname. Der Name wird in verschiedenen Benutzeroberflächen angezeigt.
Typ: string

#### Details zur Profil-Beschränkung

Die Einschränkungen des Profils entscheiden, ob eine Option in diesem Kontext für diese Profil-ID geeignet ist. Wenn die Profil-Beschränkung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h., sie ist von den Optionen aus der Optionsauswahl ungültig, wird die gesamte Optionsauswahl durch die Profil-Beschränkung, die als &quot;false&quot;ausgewertet wird, abgebrochen. Andererseits wird eine Profil-Beschränkungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierte Option der Optionsauswahl ausgewertet.
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
Mögliche Werte:

   * none

   * &quot;permissionRule&quot;: &quot;Die Profil-Beschränkung wird als eine einzige Regel ausgedrückt, die als &quot;true&quot;ausgewertet werden muss, bevor die eingeschränkte Aktion zulässig ist.&quot;

   * &quot;Beliebige Segmente&quot;: &quot;Die Profil-Beschränkung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied von mindestens einem von ihnen sein, bevor die eingeschränkte Aktion zulässig ist.&quot;

   * &quot;Alle Segmente&quot;: &quot;Die Profil-Beschränkung wird als ein oder mehrere Segmente ausgedrückt und das Profil muss Mitglied aller Segmente sein, bevor die eingeschränkte Aktion zulässig ist&quot;,

   * &quot;Regeln&quot;: &quot;Die Beschränkung des Profils wird als eine Reihe unterschiedlicher Regeln ausgedrückt, z. B. Förderfähigkeit, Anwendbarkeit, Eignung, die alle als &quot;true&quot;bewertet werden müssen, bevor die eingeschränkte Aktion zulässig ist.&quot;

* **Segmentkennung**

   Bezeichner der Segmente

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


#### Rangdetails

Rang (Priorität). Definiert, was angesichts des Kontexts des Entscheidungskriteriums als \&quot;beste Aktion\&quot; gilt. Unter allen ausgewählten Optionen, die die Förderungsbeschränkung erfüllen, entscheidet die Rangreihenfolge über die beste (oder Top-N) Option(en), die vorgeschlagen werden soll.

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

      Mögliche Werte: &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot; <!--(TBC)-->

   * **Rangstrategie**

      Ein Verweis auf eine Strategie, die eine Liste der Entscheidungsoption einstuft. Die Entscheidungsoptionen werden in einer bestellten Liste zurückgegeben. Der Wert dieser Eigenschaft ist der URI (@id) der Funktion, die jeweils mit der Option &quot;on&quot;aufgerufen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.

      Typ: string

* **Versandpriorität**

   Die Priorität einer einzigen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen, für die keine Bestellfunktion angegeben wird, werden mit dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor den Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine nach dem gleichen Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.

   Typ: integer

   Mindestwert: 0

   Standardwert: 0

#### Tags

Der Satz von Tags, die dieser Entität zugeordnet sind. Die Tags werden in Filter-Ausdrücken verwendet, um den Gesamtbestand auf eine Untergruppe (Kategorie) zu beschränken.

* **items**

   Ein Bezeichner eines Tag-Objekts. Der Wert ist die @id des Tags, auf das verwiesen wird. Siehe Tag-Schema: https://ns.adobe.com/experience/decisioning/tag.

## _repo

### Entscheidungsoption ETag

Die Revision, bei der sich das Entscheidungsoptionsobjekt zum Zeitpunkt des Snapshots befand.

Typ: string



