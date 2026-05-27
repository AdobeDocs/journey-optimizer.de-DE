---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Entscheidungsdatensatz
description: In diesem Abschnitt werden alle Felder aufgelistet, die im exportierten Datensatz für Entscheidungen verwendet werden
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DTi8clyXof5lmdx0elOPHQGm0cwQuKwAm0KbQ-U-Fmo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: c132d929-fa62-4271-803e-b823be07b914
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1574
ht-degree: 80%

---

# Entscheidungsdatensatz {#decisions-dataset}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../../experience-decisioning/gs-experience-decisioning.md)

Jedes Mal, wenn ein Angebot geändert wird, wird der automatisch generierte Datensatz für Entscheidungen aktualisiert.

![](../assets/dataset-activities.png)

Der letzte erfolgreiche Batch im Datensatz wird rechts angezeigt. Die hierarchische Ansicht des Schemas für den Datensatz wird im linken Bereich angezeigt.

>[!NOTE]
>
>In [diesem Abschnitt](../export-catalog/access-dataset.md) erfahren Sie, wie Sie für die einzelnen Objekte Ihrer Angebotsbibliothek auf die exportierten Datensätze zugreifen können.

Im Folgenden finden Sie eine Liste aller Felder, die im Datensatz **[!UICONTROL Entscheidungsobjekt-Repository – Entscheidungen]** (ehemals „Entscheidungsobjekt-Repository – Aktivitäten“) verwendet werden können.

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ Kennung

**Feld:** _id
**Titel:** Kennung
**Beschreibung:** Eine eindeutige Kennung für den Datensatz.
**Typ:** Zeichenfolge

+++

+++ _experience

**Feld:** _experience
**Typ:** Objekt

+++

+++ _experience > decisioning

**Feld:** decisioning
**Typ:** Objekt

+++

+++ _experience > decisioning > criteria

**Feld:** criteria
**Titel:** Kriterien
**Beschreibung:** Definiert einen Satz von Entscheidungskriterien, bei denen jede eine Reihe von Einschränkungen enthält.
**Typ:** Array

+++

+++ _experience > decisioning > criteria > description

**Feld:** description
**Titel:** Beschreibung
**Beschreibung:** Kriterienbeschreibung. Wird verwendet, um für den Menschen lesbare Absichten zu vermitteln, wie oder warum dieses Kriterium konstruiert wurde und wie es sich auf die Entscheidung auswirkt.
**Typ:** Zeichenfolge

+++

+++_experience > decisioning > criteria > optionSelection

**Feld:** optionSelection
**title:** Optionsauswahl
**Beschreibung:** Die Optionsauswahl definiert die Gültigkeit/Anwendbarkeit von Optionen in diesem Kontext.
**Typ:** Objekt

* Beschreibung

  **Feld:** description
  **Titel:** Beschreibung
  **Beschreibung:** Beschreibung der Optionsauswahl. Sie dient dazu, für Menschen lesbare Absichten darüber zu vermitteln, wie oder warum diese Optionsauswahl erstellt wurde und/oder welche Option passt.
  **Typ:** Zeichenfolge

* Optionsfilter

  **Feld:** filter
  **Titel:** Optionsfilter
  **Beschreibung:** Der Verweis auf einen auf einem Sammlungsqualifizierer (ehemals als „Tag“ bezeichnet) basierenden Filter, der Optionen aus einem Inventar entspricht, das deren angehängte Sammlungsqualifizierer verwendet. Der Wert ist die URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/filter.
  **Typ:** Zeichenfolge

* Profileinschränkungstyp

  **Feld:** optionSelectionType
  **Titel:** Profileinschränkungstyp
  **Beschreibung:** Bestimmt, ob aktuell Einschränkungen festgelegt sind und wie sie ausgedrückt werden. Dies kann über eine Filterabfrage oder durch die Zugehörigkeit zu einer oder mehreren Zielgruppen erfolgen.
  **Typ:** Zeichenfolge
  **Mögliche Werte:** „none“ (Standard), „directList“, „filter“

* Optionsliste

  **Feld:** options
  **Titel:** Optionsliste
  **Beschreibung:** Eine Liste, die die Optionen direkt angibt, ohne eine Filterabfrage auszuwerten. Es kann entweder eine Optionsliste oder eine Optionsfilterregel angegeben werden.
  **Typ:** Array

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_experience > decisioning > criteria > placements

**Feld:** placements
**title:** Platzierungsbeschränkungen
**Beschreibung:** Die Platzierungsbeschränkung besagt, dass dieses Kriterium nur für die aufgelisteten Platzierungen gilt. Nur wenn sich die beabsichtigte Platzierung in der Liste `xdm:placements` befindet, wird die Option ausgewählt. Andernfalls werden die gesamten Entscheidungskriterien übersprungen. Wenn die Liste „xdm:placements“ ausgelassen wird oder leer ist, wird das Kriterium für jede Zielplatzierung berücksichtigt. Die hier aufgeführten Platzierungen erzwingen implizite Kriterien für die Optionsauswahl. Eine zu berücksichtigende Option muss für die Zielplatzierung repräsentativ sein.
**Typ:** Array

* Platzierungskennung

  **Titel:** Platzierungskennung
  **Beschreibung:** Ein Verweis auf eine Platzierungsentität. Der Wert ist die URI (@id) der Platzierung, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/placement.
  **Typ:** Zeichenfolge

+++

+++_experience > decisioning > criteria > profileConstraints

**Feld:** profileConstraints
**title:** Profilbegrenzung
**Beschreibung:** Die Profilbegrenzung entscheidet, ob eine Optionsauswahl zu diesem Zeitpunkt und in diesem Kontext für diese Profil-ID geeignet ist. Wenn die Profileinschränkung die Werte der einzelnen Optionen nicht berücksichtigen muss, d. h. sie gegenüber den Optionen aus der Optionsauswahl invariant ist, hebt die als „false“ ausgewertete Profileinschränkung die gesamte Optionsauswahl auf. Dagegen wird eine Profileinschränkungsregel, die eine Option als Parameter akzeptiert, für jede qualifizierte Option der Optionsauswahl ausgewertet.
**Typ:** Objekt

+++

+++_experience > decisioning > criteria > profileConstraints > Description

**Feld:** description
**Titel:** Beschreibung
**Beschreibung:** Beschreibung der Profileinschränkung. Die Beschreibung soll in für Menschen verständlicher Form vermitteln, wie oder warum diese Profilbegrenzung erstellt wurde und/oder welche Option ein- oder ausgeschlossen wird.
**Typ:** Zeichenfolge

+++

+++ _experience > decisioning > criteria > profileConstraints > Eligibility Rule

**Feld:** eligibilityRule
**Titel:** Eignungsregel
**Beschreibung:** Ein Verweis auf eine Entscheidungsregel, die für ein bestimmtes Profil und/oder andere kontextuelle XDM-Objekte als „true“ oder „false“ ausgewertet wird. Die Regel wird verwendet, um zu entscheiden, ob die Option für ein bestimmtes Profil geeignet ist. Der Wert ist die URI (@id) der Entscheidungsregel, auf die verwiesen wird. Siehe Schema https://ns.adobe.com/experience/decisioning/rule.
**Typ:** Zeichenfolge

+++

+++ _experience > decisioning > criteria > profileConstraints > Profile Constraint Type

**Feld:** profileConstraintType
**Titel:** Profileinschränkungstyp
**Beschreibung:** Bestimmt, ob aktuell Einschränkungen festgelegt sind und wie sie ausgedrückt werden. Dies kann durch eine Regel oder durch die Zugehörigkeit zu einer oder mehreren Zielgruppen erfolgen.
**Typ:** Zeichenfolge
**Mögliche Werte:**

* „none“ (Standard)
* „eligibilityRule“: „Die Profileinschränkung wird als einzelne Regel ausgedrückt, die als „true“ ausgewertet werden muss, bevor die einschränkende Aktion zulässig ist.“
* „anySegments“: „Die Profileinschränkung wird als eine oder mehrere Zielgruppen ausgedrückt und das Profil muss mindestens einer dieser Zielgruppen angehören, damit die eingeschränkte Aktion zulässig ist.“
* „allSegments“: „Die Profileinschränkung wird als eine oder mehrere Zielgruppen ausgedrückt und das Profil muss allen Zielgruppen angehören, damit die eingeschränkte Aktion zulässig ist.“
* „rules“: „Die Profileinschränkung wird als eine Reihe verschiedener Regeln ausgedrückt, z. B. Gültigkeit, Anwendbarkeit, Eignung, die alle als „true“ ausgewertet werden müssen, bevor die eingeschränkte Aktion zulässig ist.“

+++

+++ _experience > decisioning > criteria > profileConstraints > segmentIdentities

**Feld:** segmentIdentities
**title:** Segmentkennungen
**Beschreibung:** Kennungen der Zielgruppe.
**Typ:** Array

* Kennung

  **Feld:** _id
  **Titel:** Kennung
  **Beschreibung:** Identität der Zielgruppe im betreffenden Namespace.
  **Typ:** Zeichenfolge

* Namespace

  **Feld:** namespace
  **Titel:** Namespace
  **Beschreibung**: Der mit dem Attribut `xid` verknüpfte Namespace.
  **Typ:** Objekt
  **Erforderlich:** „code“

   * Code

     **Feld:** code
     **Titel:** Code
     **Beschreibung:** Der Code ist eine von Menschen lesbare Kennung für den Namespace und kann verwendet werden, um die technische Namespace-ID anzufordern, die für die Verarbeitung von Identitätsdiagrammen verwendet wird.
     **Typ:** Zeichenfolge

* Erlebniskennung

  **Feld:** xid
  **Titel:** Erlebnis-ID
  **Beschreibung:** Falls vorhanden, stellt dieser Wert eine Namespace-übergreifende Kennung dar, die unter allen Kennungen in allen Namespaces eindeutig ist.
  **Typ:** Zeichenfolge

+++

+++_experience > decisioning > criteria > ranking

**Feld:** ranking
**title:** Ranking-Details
**Beschreibung:** Rang (Priorität). Definiert, wie die „beste Option“ angesichts des Kontexts des Entscheidungskriteriums bestimmt wird. Unter allen ausgewählten Optionen, die den Profilbegrenzungen entsprechen, entscheidet die Rangfolge über die beste oder die besten n Optionen, die vorgeschlagen werden.
**Typ:** Objekt

+++ 

+++_experience > decisioning > criteria > ranking > order

**Feld:** order
**Titel:** Evaluierung der Rangfolge
**Beschreibung:** Bewertung einer relativen Reihenfolge für eine oder mehrere Entscheidungsoptionen. Optionen mit höheren Ordinalzahlen werden vor Optionen mit niedrigeren Ordinalzahlen ausgewählt. Die durch diese Methode ermittelten Werte können geordnet werden, die Entfernungen zwischen ihnen können jedoch nicht gemessen werden. Außerdem können weder Summen noch Produkte berechnet werden. Der Medianwert und der Modus sind als einzige Messgrößen der zentralen Tendenz für Ordinaldaten verfügbar.
**Typ:** Objekt

* Scoring-Funktion

  **Feld:** function
  **Titel:** Scoring-Funktion
  **Beschreibung:** Ein Verweis auf eine Funktion, die einen numerischen Wert für diese Entscheidungsoption berechnet. Entscheidungsoptionen werden dann nach diesem Wert sortiert (nach Rang geordnet). Der Wert dieser Eigenschaft ist die URI (@id) der Funktion, die jeweils mit einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/function.
  **Typ:** Zeichenfolge

* Reihenfolgenauswertungstyp**

  **Feld:** orderEvaluationType
  **Titel:** Reihenfolgenauswertungstyp
  **Beschreibung:** Gibt an, welcher Mechanismus zur Auswertung der Reihenfolge verwendet wird: eine statische Priorität von Entscheidungsoptionen, eine Scoring-Funktion, die einen numerischen Wert für jede Option berechnet, oder ein KI-Modell, das eine Liste erhält, um eine Sortierung vorzunehmen.
  **Typ:** Zeichenfolge
  **Mögliche Werte:** „static“, „scoringFunction“, „rankingStrategy“

* Rangfolgestrategie

  **Feld:** rankingStrategy
  **Titel:** Rangfolgestrategie
  **Beschreibung:** Ein Verweis auf eine Strategie, die eine Liste von Entscheidungsoptionen in eine Reihenfolge bringt. Entscheidungsoptionen werden in einer geordneten Liste zurückgegeben. Der Wert dieser Eigenschaft ist die URI (@id) der Funktion, die jeweils mit einer Option aufgerufen werden soll. Siehe Schema https://ns.adobe.com/experience/decisioning/rankingStrategy.
  **Typ:** Zeichenfolge

+++

+++ _experience > decisioning > criteria > ranking > Priority

**Feld:** priority
**Titel:** Priorität
**Beschreibung:** Die Priorität einer einzelnen Entscheidungsoption im Verhältnis zu allen anderen Optionen. Optionen, für die keine Reihenfolgefunktion angegeben ist, werden mithilfe dieser Eigenschaft priorisiert. Optionen mit höheren Prioritätswerten werden vor Optionen mit niedrigerer Priorität ausgewählt. Wenn zwei oder mehr qualifizierte Optionen den höchsten Prioritätswert aufweisen, wird eine Option nach demselben Zufallsprinzip ausgewählt und für den Entscheidungsvorschlag verwendet.
**type:** Integer
**Mindestwert:** 0
**Standardwert:** 0

+++

+++ _experience > decisioning > Activity End Date and Time

**Feld:** endTime
**Titel:Enddatum und -zeit** Aktivität
**Beschreibung:** Enddatum und Endzeit der Entscheidung (früher als Aktivität bezeichnet). Die Eigenschaft hat die Semantik der Eigenschaft „endTime“ von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

+++

+++ _experience > decisioning > Fallback Option

**Feld:** fallback
**title:** Fallback-Option
**Beschreibung:** Der Verweis auf eine Fallback-Option, die bei der Entscheidung im Kontext dieser Entscheidung verwendet wird, qualifiziert keine der regulären Optionen (dies geschieht typischerweise, wenn harte Begrenzungen angewendet werden). Der Wert ist die URI (@id) der Fallback-Option, auf die verwiesen wird.
**Typ:** Zeichenfolge

+++

+++ _experience > decisioning > Activity Name

**Feld:** name
**Titel:** Aktivitätsname
**Beschreibung:** Name der Entscheidung (früher als Aktivität bezeichnet), der in verschiedenen Benutzeroberflächen angezeigt wird.
**Typ:** Zeichenfolge

+++

+++_experience > decisioning > Activity Start Date and Time

**Feld:** startTime
**Titel:** Startdatum und -zeit der Aktivität
**Beschreibung:** Startdatum und Endzeit der Entscheidung (früher als Aktivität bezeichnet). Die Eigenschaft hat die Semantik der Eigenschaft „startTime“ von schema.org, die auf http://schema.org/Action definiert ist.
**Typ:** Zeichenfolge

+++

+++ _repo

**Feld:** _repo
**Typ:** Objekt

+++

+++ _repo > Activity Etag

**Feld:** eTag
**Titel:** Aktivitäts-E-Tag
**Beschreibung:** Die Überprüfung, bei der sich das Entscheidungsobjekt (früher als Aktivität bezeichnet) zum Zeitpunkt des Speicherauszugs befand.
**Typ:** Zeichenfolge

+++
