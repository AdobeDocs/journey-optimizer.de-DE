---
solution: Journey Optimizer
product: journey optimizer
title: Journey-Bericht
description: Informationen zum Verwenden von Daten aus dem Journey-Bericht
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 30d4f967-e085-44f1-973d-11e79f693e6e
source-git-commit: 158d9d9a1070e1d842183e5bd6cb5ce8e38834c5
workflow-type: ht
source-wordcount: '971'
ht-degree: 100%

---

# Journey-Bericht {#journey-global-report}

Der **Journey-Bericht** dient als allumfassendes Dashboard, das eine Analyse der wichtigsten Metriken bereitstellt, die mit Ihrer Journey verknüpft sind. Dies umfasst Details wie die Anzahl der eingetretenen Profile und Instanzen fehlgeschlagener individueller Journeys und bietet einen umfassenden Einblick in die Effektivität Ihrer Journey und den Grad der Interaktion.

Über die Schaltfläche **[!UICONTROL Bericht anzeigen]** können Sie direkt von Ihrer Journey auf den **Journey-Bericht** zugreifen.

![](assets/gs-cja-report-3.png)

Weitere Informationen zu Customer Journey Analytics Workspace und zum Filtern und Analysieren von Daten finden Sie auf [dieser Seite](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/home).

## Journey-Überblick {#journey-global}

Mit dem **[!UICONTROL Journey-Bericht]** erhalten Sie einen klaren Überblick über die wichtigsten Tracking-Daten zu Ihrer Journey.

### Journey-KPIs {#journey-perfomance}

![](assets/cja-journey-kpis.png)

Die **[!UICONTROL Journey-KPIs]** (Key Performance Indicators) dienen als allumfassendes Dashboard und liefern eine Analyse der wichtigsten Metriken, die mit Ihrer Journey verknüpft sind. Dies umfasst Details wie die Anzahl der eingetretenen Profile und die Instanzen der fehlgeschlagenen einzelnen Journeys und bietet einen umfassenden Einblick in die Effektivität und den Grad der Interaktion Ihrer Journeys.

+++ Weitere Informationen zu den Metriken „Journey-KPIs“

* **[!UICONTROL Journey-Interaktion]**: Gesamtzahl der eindeutigen Kontakte, die über die Journey gesendete Nachrichten empfangen haben und bestimmte Profile repräsentieren, die einen bestimmten Aktionspunkt in der Journey erreicht haben.

* **[!UICONTROL Journey-Eintritte]**: Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben.

* **[!UICONTROL Journey-Austritte]**: Gesamtzahl der Kontakte, die die Journey verlassen haben.

+++

### Journey-Statistiken {#journey-stats}

![](assets/cja-journey-stats.png)

Die Tabelle **[!UICONTROL Journey-Statistiken]** bietet eine detaillierte Zusammenfassung wichtiger Daten zu Ihren Journeys. Sie enthält Schlüsselmetriken wie die Anzahl der Fehler und erfolgreichen Eintritte und bietet wertvolle Erkenntnisse zur Performance und Reichweite Ihrer E-Mails und Journeys.

+++ Weitere Informationen zu den Metriken „Journey-Statistiken“

* **[!UICONTROL Journey-Ausschluss]**: Gesamtzahl der Kontakte, die aufgrund vordefinierter Kriterien oder Unterdrückungsregeln von der Journey ausgeschlossen wurden.

* **[!UICONTROL Journey-Interaktion]**: Gesamtzahl der eindeutigen Kontakte, die über die Journey gesendete Nachrichten empfangen haben und bestimmte Profile repräsentieren, die einen bestimmten Aktionspunkt in der Journey erreicht haben.

* **[!UICONTROL Journey-Eintritte]**: Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben.

* **[!UICONTROL Journey-Austritte]**: Gesamtzahl der Kontakte, die die Journey verlassen haben.

* **[!UICONTROL Fehlgeschlagene Journeys]**: Gesamtzahl der individuellen Journeys, die nicht erfolgreich ausgeführt wurden.

* **[!UICONTROL Eindeutige Journey-Eintritte]**: Gesamtzahl der Kontakte, die das Eintrittsereignis der Journey erreicht haben, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.

* **[!UICONTROL Eindeutige Journey-Austritte]**: Gesamtzahl der Kontakte, die die Journey verlassen haben, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.

* **[!UICONTROL Eindeutige Journey-Fehler]**: Gesamtzahl der individuellen Journeys, die nicht erfolgreich ausgeführt wurden, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.

+++

## Journey-Ausschluss {#journey-exclusion}

Die Tabelle **[!UICONTROL Journey-Ausschluss]** bietet einen umfassenden Überblick über die verschiedenen Faktoren, die zum Ausschluss von Benutzerprofilen geführt haben.

## Aktionsfehler {#action-error}

![](assets/cja-journey-action-error.png)

Das Widget **[!UICONTROL Aktionsfehler]** zeigt die verschiedenen Fehler an, die bei Ihren Journey-Aktionen aufgetreten sind.

## Journey-Arbeitsfläche {#journey-canvas}

![](assets/cja-journey-canvas.png)

Mit dem Widget **[!UICONTROL Journey-Arbeitsfläche]** können Sie den Weg Ihrer Zielprofile durch die Journey visuell verfolgen. [Weitere Informationen finden Sie in der Customer Journey Analytics-Dokumentation](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

Verbessern Sie die Anpassung Ihrer Arbeitsfläche mit den folgenden Optionen:

* Fügen Sie den gewünschten Aktivitätstyp, z. B. Nachrichten oder Bedingungen, hinzu oder entfernen Sie ihn aus dem Dropdown-Menü **[!UICONTROL Knotentyp]**.
* Passen Sie den **[!UICONTROL Prozentwert]** an, um die Flussverteilung zwischen verschiedenen Journey-Pfaden zu bestimmen.
* Passen Sie Ihre **[!UICONTROL Pfeileinstellungen]** an, um Labels und Bedingungen einzuschließen, oder entscheiden Sie sich für eine saubere Anzeige.
* Aktivieren Sie die Option **[!UICONTROL Fallout anzeigen]**, um direkt auf der Arbeitsfläche Profile zu visualisieren, die Ihre Journey verlassen haben.

Bei Verwendung der Filterung **[!UICONTROL Knotentyp]** gelten die folgenden Regeln:

* Beim Erstellen eines Segments auf einem Knoten umfasst es weiterhin Knoten aus früheren Phasen der Journey, selbst wenn diese Knoten über den Filter **[!UICONTROL Knotentyp]** ausgeschlossen wurden.

* Es ist nicht möglich, über einen Pfeil geformte Segmente zu erstellen, wenn Knoten in früheren Phasen der Journey über den Filter **[!UICONTROL Knotentyp]** ausgeschlossen wurden. In diesem Fall wird die Rechtsklickfunktion für diese Pfeile deaktiviert.

## Aktions-Performance {#action-performance}

### Performance im Zeitverlauf {#action-overtime}

![](assets/cja-journey-action-performance.png)

Anhand des Graphs **[!UICONTROL Performance im Zeitverlauf]** können Sie die Anzahl der Profile identifizieren und analysieren, die den Kriterien entsprechen, damit sie für Ihre Aktionen als Zielprofile gelten. Diese Visualisierung bietet wertvolle Erkenntnisse zur Effektivität Ihrer Strategien und hilft Ihnen, datengesteuerte Entscheidungen zur Leistungsoptimierung zu treffen.

### Aktionsüberblick {#action-overview}

![](assets/cja-journey-action-overview.png)

Die Tabelle **[!UICONTROL Aktionsüberblick]** dient als umfassendes Dashboard, das eine Analyse der Schlüsselmetriken im Zusammenhang mit den Aktionen in Ihrer Journey bietet. Dazu gehören wichtige Details wie die Anzahl der Interaktionen und die Klickrate.

+++ Weitere Informationen zu den Metriken „Aktionsüberblick“

* **[!UICONTROL Knoteneintritte]**: Gesamtzahl der Kontakte, die in einen bestimmten Knoten der Journey eingetreten sind.

* **[!UICONTROL Journey-Fehler]**: Gesamtzahl der einzelnen Journeys, die nicht erfolgreich ausgeführt wurden.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzenden, die mit der Aktion interagiert haben.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren Aktionen.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Aktionen im Verhältnis zur Gesamtzahl der gesendeten Aktionen.

+++

## Ereignis-Performance {#events-performance}

### Performance im Zeitverlauf {#event-overtime}

![](assets/cja-journey-performance-event.png)

Anhand des Graphen **[!UICONTROL Performance im Zeitverlauf]** können Sie die Anzahl der Profile identifizieren und analysieren, die sich als Zielprofile für Ihre Ereignisse eignen. Mit diesem leistungsstarken Tool können Sie Trends und Muster im Zeitverlauf verfolgen und erhalten wertvolle Erkenntnisse zur Optimierung Ihrer Ereignisstrategien.

### Ereignisüberblick {#event-overview}

![](assets/cja-journey-events-overview.png)

Die Tabelle **[!UICONTROL Ereignisüberblick]** zeigt an, wie viele Profile im Zeitverlauf Ihren Ereigniskriterien entsprechen. Mit diesem Tool können Sie Muster in Qualifizierungsraten identifizieren, um Ihre Ereignisstrategie zu verfeinern.

+++ Weitere Informationen zu den Metriken „Journey-Statistiken“

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Ereignisse eignen.

+++

## Targeting-Überblick {#targeting}

![](assets/cja-journey-targeting-overview.png)

Wenn Sie **[!UICONTROL Targeting-Regeln]** für Ihre Inhalte einrichten, bietet die Tabelle **[!UICONTROL Targeting-Überblick]** eine detaillierte Ansicht der wichtigsten Interaktionsmetriken und zeigt, wie die Zielgruppenprofile für die einzelnen Regeln mit Ihren Inhalten interagiert haben.

➡️ [Weitere Informationen zu Targeting-Regeln](../campaigns/campaigns-message-optimization.md)

+++ Weitere Informationen zu den Metriken „Targeting-Überblick“

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Ereignisse eignen.

* **[!UICONTROL Einzelklicks]**: Die Anzahl der Profile, die auf einen Inhalt in einer E-Mail geklickt haben.

* **[!UICONTROL Einzelklickrate]**: Prozentsatz der Zielgruppenprofile, die mindestens einmal geklickt haben.

+++
