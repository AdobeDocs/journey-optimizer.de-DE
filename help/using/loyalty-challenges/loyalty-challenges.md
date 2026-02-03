---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen bezüglich der Treue
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit dem Treueprogramm erstellen und verwalten, um ansprechende Treueprogramme zu erstellen.
feature: Loyalty challenges
topic: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
version: Journey Orchestration
source-git-commit: ee67a1a9270c12fdf199bc378deaa6006553533c
workflow-type: tm+mt
source-wordcount: '4925'
ht-degree: 1%

---


# Herausforderungen bezüglich der Treue {#loyalty-challenges}

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Mit den Herausforderungen im Zusammenhang mit der Treue können Sie personalisierte Interaktionsangebote für Ihre Kunden erstellen und so Treueprogramme in jedem Maßstab orchestrieren. Sie können Herausforderungen mit bestimmten Aufgaben und Meilensteinen entwerfen, Kunden für deren Erfüllung belohnen und das Erlebnis über Adobe Journey Optimizer-Kanäle bereitstellen.

>[!BEGINSHADEBOX]
>
>**In diesem Handbuch:**
>
>* [Überblick](#overview) - Erfahren Sie mehr über die Herausforderungen im Zusammenhang mit der Treue
>* [Voraussetzungen](#prerequisites) - Einrichten der Datenaufnahme und der Berechtigungen
>* [Herausforderungen im Zusammenhang mit Treueprogrammen](#access) - Öffnen Sie das Menü und sehen Sie sich Herausforderungen an.
>* [Herausforderungen schaffen](#create-challenges) - Neue Herausforderungen im Bereich Kundentreue
>* [Aufgaben erstellen](#create-tasks) - Festlegen, was Kunden tun müssen
>* [Herausforderungen verwalten](#manage-challenges) - Bearbeiten, Überwachen und Optimieren
>
>[!ENDSHADEBOX]

## Übersicht {#overview}

Mit den Herausforderungen im Zusammenhang mit der Kundentreue können Sie personalisierte Interaktionsangebote entwerfen und bereitstellen, die Kunden dazu motivieren, bestimmte Aktionen durchzuführen und Belohnungen zu sammeln. Die Funktion bietet eine Komplettlösung für die Erstellung von Treueprogrammen in großem Maßstab, von der Definition von Aufgaben und Meilensteinen bis zur Bereitstellung von Inhalten und der Verfolgung der Leistung über verschiedene Kanäle hinweg. Sie können drei Arten von Challenge-Erlebnissen erstellen, Belohnungen konfigurieren, Multi-Channel-Benachrichtigungen in wichtigen Lebenszyklusphasen senden und die Leistung mithilfe automatisch generierter Journey überwachen - und das alles unter Beibehaltung der Integration mit Ihrem externen Treueprogramm-System.

## Wichtigste Funktionen

Herausforderungen im Zusammenhang mit der Treue nutzen, um:

* **Erstellen Sie drei Arten von Herausforderungen**:
   * **Standard**: Kunden führen eine beliebige Anzahl von Aufgaben aus, um Prämien zu erhalten.
   * **Streak**: Kundinnen und Kunden führen dieselbe Aufgabe mehrmals aus.
   * **Sequenziell**: Kunden führen Aufgaben in einer bestimmten Reihenfolge aus.

* **Design Challenge-Inhalte**: Verwenden Sie Journey Optimizer-Inhaltskarten, um die visuelle Darstellung Ihrer Challenge auf Kundengeräten zu erstellen. Auf Inhaltskarten werden die Challenge-Informationen, der Fortschritt und die Belohnungen auf dem Gerät des Kunden angezeigt.

* **Aufgabenanforderungen einrichten** Definieren Sie, was Kunden tun müssen, um Prämien zu verdienen, darunter:
   * Aufgabentypen (Kauf, Ausgabenbetrag, Besuch usw.)
   * Mengenbedarf
   * Produkteinschlüsse/-ausschlüsse mithilfe von SKUs
   * Benutzerdefinierte Attribute und Bedingungen

* **Belohnungen konfigurieren**: Belohnungen definieren, die Kunden entweder bei Aufgabenabschluss oder nach Abschluss der gesamten Challenge erhalten

* **Benachrichtigungen senden**: Versand von Nachrichten über mehrere Kanäle (In-App, E-Mail, Push) in wichtigen Phasen:
   * **Launch**: Wenn die Challenge beginnt
   * **In Bearbeitung**: Wenn Kundinnen und Kunden teilweise durchgekommen sind
   * **Abschließen**: Wenn Kunden die Challenge abgeschlossen haben

* **Performance verfolgen** Überwachen automatisch generierter Journeys und Überprüfen der Challenge-Performance

### Wichtige Einschränkungen {#limitations}

* **Kein Sachkontensystem**: Treueprobleme verfolgen keine Geldwerte oder Punktesalden. Wenn Kundinnen und Kunden eine Challenge abschließen und eine Belohnung erhalten, ruft Journey Optimizer Ihr externes Treueprogramm-Management-System an, um die Punktzuweisung zu bearbeiten.

* **Nur Zielgruppenauswahl**: Sie können vorhandene Zielgruppen auswählen, aber keine neuen Zielgruppen über die Benutzeroberfläche „Herausforderungen im Treueprogramm“ erstellen.

## Voraussetzungen {#prerequisites}

Bevor Sie Herausforderungen im Zusammenhang mit dem Treueprogramm nutzen, stellen Sie Folgendes sicher:

* Einrichtung der Datenaufnahme

  Herausforderungen im Zusammenhang mit der Kundentreue beruhen auf Daten, die über Experience Platform-Quell-Connectoren aufgenommen werden, um den Kundenfortschritt und den Abschluss von Aufgaben zu verfolgen.

   1. **Konfigurieren eines unterstützten Quell-Connectors**: Derzeit ist der Kapillaranschluss allgemein verfügbar. Weitere Connectoren sind geplant.

   2. **Validieren der Datenaufnahme**: Stellen Sie sicher, dass Treueereignisse und Kundendaten nach Experience Platform fließen und in Journey Optimizer verfügbar sind.

  Detaillierte Anweisungen finden Sie unter:

   * [Dokumentation zu Experience Platform-Quellen](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
   * [Konfigurieren von Quell-Connectoren in Journey Optimizer](../start/get-started-sources.md)

* Erforderliche Berechtigungen {#required-permissions}

Um Herausforderungen im Zusammenhang mit der Treue nutzen zu können, benötigen Sie in Journey Optimizer die entsprechenden Berechtigungen. Wenden Sie sich an Ihren Administrator, wenn Sie auf die Funktion nicht zugreifen können.

## Herausforderungen beim Treueprogramm {#access}

So greifen Sie auf Herausforderungen im Zusammenhang mit der Treue zu:

1. Wählen Sie in Adobe Journey Optimizer **[!UICONTROL Navigationsmenü]** Herausforderungen bezüglich der Treue“ aus.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. Im Inventar der Herausforderungen im Treueprogramm werden alle bestehenden Herausforderungen mit Informationen wie den folgenden angezeigt:
   * Name und Beschreibung der Herausforderung
   * Status (Entwurf, Live, gestoppt usw.)
   * Challenge-Typ (Standard, Streak, sequenziell)
   * Start- und Enddatum
   * Datum der letzten Änderung

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Wählen Sie **[!UICONTROL Herausforderung erstellen]**, um eine neue Herausforderung zu erstellen.

### Herausforderungen beim Suchen und Filtern {#search-filter}

Verwenden Sie Such- und Filterfunktionen, um bestimmte Herausforderungen schnell zu finden:

#### Suche {#search}

Geben Sie den Namen oder die Keywords der Challenge ein, um im Feld **[!UICONTROL Suche]** passende Challenges zu finden.

#### Nach Status filtern {#filter-by-status}

Herausforderungen mit bestimmten Status in anzeigen **[!UICONTROL Nach Status filtern]**:

* Entwurf
* Geplant
* Live
* Abgeschlossen
* Gestoppt
* Archiviert

#### Nach Typ filtern {#filter-by-type}

Nur Standard-, Streak- oder sequenzielle Challenges mit &quot;**[!UICONTROL nach Typ]** anzeigen.

#### Nach Datum filtern {#filter-by-date}

Herausforderungen innerhalb eines bestimmten Datumsbereichs mit „Nach Datum **[!UICONTROL &quot;]**.

#### Nach Tags filtern {#filter-by-tags}

Herausforderungen bei der Anwendung bestimmter Tags anzeigen (**[!UICONTROL nach Tags]**.

## Herausforderungen schaffen {#create-challenges}

Erstellen Sie eine Herausforderung zum Treueprogramm, um das Interaktionsangebot zu definieren, Inhaltskarten für den Versand zu konfigurieren, Aufgaben hinzuzufügen, Belohnungen einzurichten und optional das Messaging kanalübergreifend zu konfigurieren.

### Bevor Sie beginnen {#before-you-start}

Bevor Sie eine Herausforderung erstellen, stellen Sie sicher, dass Sie Folgendes haben:

* Datenaufnahme über Quell-Connectoren konfiguriert und validiert
* Erforderliche Zielgruppen in Experience Platform erstellt
* Vorbereitete Content-Assets (Bilder, Text usw.) für Ihre Herausforderung
* Sie haben die Aufgaben und Belohnungen definiert, die Sie anbieten möchten

### Erstellen einer Challenge {#create-a-challenge}

So erstellen Sie eine neue Herausforderung für das Treueprogramm:

1. Wählen Sie in Journey Optimizer **[!UICONTROL Navigationsmenü]** Herausforderungen bezüglich der Treue“ aus.

2. Wählen **[!UICONTROL oben]** „Herausforderung erstellen“ aus.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. Konfigurieren Sie im Bildschirm Challenge Properties Folgendes:

#### Allgemeine Eigenschaften {#basic-properties}

**[!UICONTROL Name]**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Inventar angezeigt und ist im automatisch generierten Journey-Namen enthalten.

**[!UICONTROL Beschreibung]**: (Optional) Fügen Sie eine Beschreibung hinzu, um Ihnen und Ihrem Team zu helfen, den Zweck und die Details dieser Herausforderung zu verstehen.

**[!UICONTROL Challenge type]**: Wählen Sie die Art der Challenge aus, die Sie erstellen möchten:

* **[!UICONTROL Standard]**: Kunden können beliebig viele bestimmte Aufgaben ausführen, um die Belohnung zu erhalten. Beispiel: „Diesen Monat 5 Käufe tätigen.“

* **[!UICONTROL Streak]**: Kunden müssen dieselbe Aufgabe wiederholt abschließen. Beispiel: „Besuchen Sie unseren Shop 10-mal hintereinander.“

* **[!UICONTROL Sequenziell]**: Kunden müssen Aufgaben in einer bestimmten Reihenfolge ausführen. Beispiel: „Zuerst einen Kauf tätigen, dann eine Bewertung schreiben und dann einen Freund verweisen.“

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Startdatum]**: Wählen Sie aus, wann die Challenge aktiv und für Kunden verfügbar wird.

**[!UICONTROL Enddatum]**: Wählen Sie aus, wann die Challenge abläuft. Kunden, die die Challenge bis zu diesem Datum nicht abgeschlossen haben, können die Belohnung nicht mehr erhalten.

#### Zielgruppenauswahl {#audience-selection}

**[!UICONTROL Audience auswählen]**: Wählen Sie die Audience aus, die für diese Challenge geeignet ist. Sie können nur vorhandene Audiences auswählen. Sie können keine neuen Audiences über die Benutzeroberfläche „Herausforderungen im Zusammenhang mit dem Treueprogramm“ erstellen.

Informationen zum Erstellen oder Verfeinern von Zielgruppen finden Sie unter [Erstellen von Zielgruppen in Journey Optimizer](../audience/about-audiences.md).

&#x200B;4. Wählen Sie **[!UICONTROL Als Entwurf speichern]**, um mit der Konfiguration Ihrer Challenge fortzufahren.

## Aufgaben erstellen {#create-tasks}

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um bei einer Herausforderung im Rahmen des Treueprogramms Belohnungen zu erhalten. Sie können Aufgabentypen, Mengen, Produktanforderungen und Belohnungswerte konfigurieren, um ansprechende und personalisierte Treueerlebnisse zu schaffen.

### Aufgabenübersicht {#task-overview}

Jede Aufgabe stellt eine messbare Aktion dar, die zum Abschluss der Herausforderung beiträgt. Je nach Challenge-Typ (Standard, Streak oder Sequential) führen Kunden Aufgaben unterschiedlich aus:

* **Standardherausforderungen**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus

### Aufgabe hinzufügen {#add-task}

So fügen Sie eine Aufgabe zu Ihrer Challenge hinzu:

1. Öffnen Sie eine Challenge oder erstellen Sie eine neue.

2. Navigieren Sie zum Abschnitt **[!UICONTROL Aufgaben]** .

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

3. Wählen **[!UICONTROL Aufgabe hinzufügen]** oder **[!UICONTROL Neue Aufgabe erstellen]**.

4. Konfigurieren Sie im Bildschirm „Aufgabenerstellung“ die folgenden Eigenschaften.

### Aufgabeneigenschaften {#task-properties}

#### Grundlegende Informationen zu Aufgaben {#basic-info}

**[!UICONTROL Aufgabenname]**: Geben Sie einen beschreibenden Namen für die Aufgabe ein. Dieser Name ist für Sie und Ihr Team sichtbar, wird Kunden jedoch möglicherweise nicht angezeigt, je nach Design Ihrer Inhaltskarte.

**[!UICONTROL Aufgabenbeschreibung]**: (Optional) Fügen Sie Details zum Zweck oder zu den Anforderungen der Aufgabe hinzu.

**[!UICONTROL Aufgabentyp]**: Wählen Sie den Aktionstyp aus, den Kundinnen und Kunden durchführen müssen. Zu den verfügbaren Aufgabentypen gehören:

* **[!UICONTROL Kauf]**: Kunde tätigt eine Kauftransaktion
* **[!UICONTROL Ausgabenbetrag]**: Kunde gibt einen bestimmten Geldbetrag aus
* **[!UICONTROL Besuch]**: Der Kunde besucht einen physischen Standort oder eine digitale Eigenschaft
* **[!UICONTROL Interaktion]**: Der Kunde interagiert mit Inhalten, z. B. mit der Anzeige eines Videos oder dem Lesen eines Artikels
* **[!UICONTROL Benutzerspezifisches Ereignis]**: Kundenspezifische Trigger haben ein benutzerspezifisches Ereignis erfasst, das über Ihre Datenaufnahme verfolgt wurde

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

#### Mengenbedarf {#quantity-requirements}

**[!UICONTROL Erforderliche Menge]**: Geben Sie an, wie oft der Kunde die Aufgabe ausführen muss, um sie abzuschließen.

Beispiel:

* Für eine Kaufaufgabe: „2 Artikel kaufen“ (Menge = 2)
* Für eine Aufgabe des Ausgabenbetrags: „50 USD ausgeben“ (Menge = 50)
* Für eine Besuchsaufgabe: „5-mal besuchen“ (Menge = 5)

**[!UICONTROL Tracking-Zeitraum]**: (Optional) Definieren Sie das Zeitfenster für die Durchführung dieser Aufgabe:

* Dauer pro Challenge (Standard)
* pro Tag
* Pro Woche
* Pro Monat
* Benutzerdefinierter Datumsbereich

### Produkt- und SKU-Filterung {#product-filtering}

Für Kauf- und Ausgabenbetragsaufgaben können Sie angeben, welche Produkte für die Aufgabenfertigstellung qualifiziert sind.

#### Produkteinschlüsse {#product-inclusions}

Definieren, welche Produkte oder Kategorien für die Aufgabe gezählt werden:

1. Wählen **[!UICONTROL Produktkriterien hinzufügen]** aus.

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

2. Wählen Sie aus, wie qualifizierte Produkte definiert werden sollen:
   * **[!UICONTROL Nach SKU]**: Geben Sie bestimmte Produkt-SKU-Codes ein
   * **[!UICONTROL Nach Kategorie]**: Wählen Sie Produktkategorien aus Ihrem Katalog
   * **[!UICONTROL Nach Attribut]**: Filtern nach Produktattributen wie Marke, Größe, Farbe oder benutzerdefinierten Attributen

3. Produktkennungen eingeben oder auswählen:

   **Beispiel - nach SKU**:

   ```text
   SKU001, SKU002, SKU003
   ```

   **Beispiel - Nach Kategorie**:

   * Getränke > Kaffee
   * Bäckerei > Gebäck

   **Beispiel - Nach Attribut**:

   * Marke = „Premium-Marke“
   * Kategorie = „Saisonale Artikel“
   * Preis > $20

4. Wählen **[!UICONTROL Hinzufügen]**, um die Produktkriterien zu speichern.

#### Produktausschlüsse {#product-exclusions}

Optional können Sie bestimmte Produkte von der Zählung für die Aufgabe ausschließen:

1. Wählen Sie **[!UICONTROL Ausschlüsse hinzufügen]** aus.

2. Verwenden Sie dieselben Filtermethoden wie Produkteinschlüsse, um anzugeben, welche Produkte ausgeschlossen werden sollen.

3. Häufige Ausschlussszenarien:

   * Verkaufs- oder Abfertigungsartikel
   * Geschenkkarten
   * Werbeartikel oder Gratis-Artikel
   * Spezifische Marken oder Kategorien

>[!NOTE]
>
>**Ein- und Ausschlusslogik**: Wenn sowohl Ein- als auch Ausschlüsse definiert sind:
>
>* Produkte müssen Einschlusskriterien entsprechen
>* Produkte, die den Ausschlusskriterien entsprechen, werden entfernt, auch wenn sie den Einschlüssen entsprechen
>* Wenn keine Einschlüsse definiert sind, sind alle Produkte qualifiziert, mit Ausnahme der ausdrücklich ausgeschlossenen Produkte

#### Beispiele für die Produktfilterung {#product-filtering-examples}

##### Beispiel 1: Kaffeefrage {#example-1}

* Aufgabentyp: Kauf
* Erforderliche Menge: 3
* Einschlüsse: Kategorie = „Getränke > Kaffee“
* Ergebnis: Der Kunde muss 3 Kaffeegetränke kaufen

##### Beispiel 2: Ausgaben für Prämien {#example-2}

* Aufgabentyp: Ausgabenbetrag
* Erforderliche Menge: $100
* Einschlüsse: Marke = „Premium-Marke“
* Ausnahmen: Kategorie = „Freigabe“
* Ergebnis: Der Kunde muss 100 USD für Premium-Markenartikel ausgeben, ausgenommen Clearance-Artikel

##### Beispiel 3: Spezifischer Produktkauf {#example-3}

* Aufgabentyp: Kauf
* Erforderliche Menge: 1
* Lieferumfang: SKU = „NEWPRODUCT2024“
* Ergebnis: Der Kunde muss das spezifische Produkt mit SKU „NEWPRODUCT2024“ erwerben

### Konfigurieren von Belohnungen {#configure-rewards}

Definieren, was Kundinnen und Kunden durch die Durchführung von Aufgaben verdienen. Belohnungen können auf Aufgabenebene oder auf Challenge-Ebene gewährt werden, nachdem alle Aufgaben abgeschlossen sind.

#### Belohnungs-Timing {#reward-timing}

Wählen Sie aus, wann Kunden Belohnungen erhalten:

**[!UICONTROL Nach Abschluss der]**: Kunden erhalten sofort nach Abschluss dieser spezifischen Aufgabe eine Belohnung (auch als „progressive Belohnungen“ oder „Meilenstein-Belohnungen“ bezeichnet).

**[!UICONTROL Nach Abschluss der Herausforderung]**: Kunden erhalten eine Belohnung erst, nachdem sie alle erforderlichen Aufgaben in der Herausforderung abgeschlossen haben (auch als „endgültige Belohnungen“ oder „Hauptpreise“ bezeichnet).

>[!TIP]
>
>Sie können beide Belohnungstypen in einer einzigen Herausforderung kombinieren, um während des gesamten Kunden-Journey Interaktionen aufrechtzuerhalten. Beispiel:
>
>* 10 Punkte nach jeder Aufgabenfertigstellung vergeben (progressive Belohnungen)
>* Geben Sie weitere 100 Punkte nach Abschluss der gesamten Herausforderung (letzte Belohnung).

#### Belohnungstypen und -werte {#reward-types}

**[!UICONTROL Punkte]**: Vergabe von Treuepunkten an das Konto des Kunden.

* Anzahl der Punkte eingeben (z. B. 100)
* Punkte werden über eine API an Ihr externes Treueprogramm-Management-System übermittelt.

**[!UICONTROL Rabatt]**: Geben Sie einen Rabattcode oder -wert an.

* Rabatttyp eingeben (Prozentsatz oder fester Betrag)
* Rabattwert eingeben
* Geben Sie optional einen Rabattcode an oder lassen Sie ihn vom System generieren.

**[!UICONTROL Kostenloser Artikel]**: Gewähren Sie ein kostenloses Produkt oder eine kostenlose Dienstleistung.

* Geben Sie die Artikel-SKU oder Beschreibung an
* Geben Sie an, wie das kostenlose Element beansprucht werden soll

**[!UICONTROL Benutzerdefinierte Belohnung]**: Definieren Sie einen benutzerdefinierten Belohnungstyp.

* Belohnungsbeschreibung eingeben
* Angabe aller relevanten Codes oder Kennungen
* Konfigurieren, wie die Belohnung zugestellt oder beansprucht wird

#### Beispiel für eine Belohnungskonfiguration {#reward-example}

**Challenge**: „Coffee Lover Challenge“

**Aufgabe 1**: 3 Kaffee kaufen

* Belohnung: 30 Punkte (10 Punkte pro Kaffee)
* Zeit: Nach Abschluss der Aufgabe

**Aufgabe 2**: 2 neue saisonale Getränke ausprobieren

* Belohnung: 50 Punkte
* Zeit: Nach Abschluss der Aufgabe

**Challenge Completion Belohnung**:

* Prämie: Gratis Kaffee + 100 Bonuspunkte
* Zeit: Nach Abschluss aller Aufgaben

**Total mögliche Prämien**: 180 Punkte + 1 kostenloser Kaffee

### Erweiterte Aufgabenattribute {#advanced-attributes}

Für erweiterte Anwendungsfälle können Sie zusätzliche Aufgabenattribute konfigurieren:

**[!UICONTROL Benutzerdefinierte Bedingungen]**: Fügen Sie mithilfe von Experience Platform-Segmenten oder -Regeln benutzerdefinierte Logik oder Bedingungen hinzu, die über die standardmäßigen Aufgabentypen hinausgehen.

**[!UICONTROL Geofencing]**: (Für Besuchsaufgaben) Erfordert Besuche an bestimmten Orten, die durch geografische Koordinaten und Radius definiert sind.

**[!UICONTROL Zeitbasierte Anforderungen]**: Aufgaben müssen zu bestimmten Zeiten, Tagen oder Datumsbereichen ausgeführt werden.

**[!UICONTROL Abklingzeit]**: Legen Sie eine Mindestzeit zwischen den Aufgabenabschlüssen fest, um schnelle wiederholte Aktionen zu verhindern.

**[!UICONTROL Aufgabenabhängigkeiten]**: (Für sequenzielle Herausforderungen) Definieren Sie Voraussetzungen, die erfüllt sein müssen, bevor diese Aufgabe verfügbar wird.

## Konfigurieren von Inhaltskarten {#configure-content-cards}

Inhaltskarten sind die primäre Methode, mit der Kunden Herausforderungen auf ihren Geräten angezeigt werden. Für die Challenge müssen Sie eine Inhaltskarte konfigurieren.

1. Navigieren Sie in Ihrer Challenge zur Registerkarte **[!UICONTROL Inhalt]** .

2. Wählen Sie **[!UICONTROL Inhalt bearbeiten]** aus, um den Inhaltskarten-Editor zu öffnen.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Konfigurieren Sie die Eigenschaften der Inhaltskarte:

   **[!UICONTROL Konfigurationsname]**: Geben Sie einen Namen für diese Inhaltskartenkonfiguration ein.

   **[!UICONTROL Konfiguration]**: Wählen oder erstellen Sie eine Inhaltskartenkonfiguration. Dadurch werden technische Einstellungen für die Bereitstellung der Inhaltskarte definiert.

4. Entwerfen Sie im Inhaltskarten-Editor Ihre Challenge-Karte:

   * Text hinzufügen, um die Herausforderungen, Aufgaben und Belohnungen zu beschreiben
   * Bilder oder andere visuelle Elemente einschließen
   * Personalisierung verwenden, um kundenspezifische Informationen einzuschließen
   * Anzeigen von Fortschrittsanzeigen, falls zutreffend
   * Call-to-action-Schaltflächen hinzufügen

   Der Inhaltskarten-Editor bietet dieselben Funktionen wie andere Journey Optimizer-Kanäle. Detaillierte Anleitungen finden Sie unter [Erstellen von Inhaltskarten](../content-card/design-content-card.md).

5. Wählen Sie **[!UICONTROL Speichern]** aus, um Ihre Inhaltskartenkonfiguration zu speichern.

>[!NOTE]
>
>Die Inhaltskarte wird über die automatisch generierte Journey bereitgestellt. Sie wird berechtigten Zielgruppenmitgliedern angezeigt, wenn die Challenge aktiv ist.

## Konfigurieren von Messaging {#configure-messaging}

Sie können optional Nachrichten konfigurieren, die an Kunden in wichtigen Phasen des Challenge-Lebenszyklus gesendet werden. Messaging ist für drei Phasen verfügbar:

* **[!UICONTROL Launch]**: Eine Nachricht senden, wenn die Challenge aktiv wird
* **[!UICONTROL In Bearbeitung]**: Senden Sie eine Nachricht, wenn Kunden die Challenge zum Teil bewältigt haben
* **[!UICONTROL Abschließen]**: Senden Sie eine Nachricht, wenn Kunden die Herausforderung abgeschlossen haben

### Hinzufügen von Nachrichten {#add-messages}

1. Navigieren Sie in Ihrer Challenge zur Registerkarte **[!UICONTROL Messaging]** .

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Wählen Sie die Phase aus, zu der Sie eine Nachricht hinzufügen möchten: Launch, In Bearbeitung oder Abgeschlossen.

3. Wählen Sie **[!UICONTROL Nachricht hinzufügen]** aus.

4. Kanal für die Nachricht auswählen:
   * **[!UICONTROL In-App]**: Eine Nachricht in Ihrer Anwendung anzeigen
   * **[!UICONTROL E-Mail]**: Senden einer E-Mail-Benachrichtigung
   * **[!UICONTROL Push]**: Senden einer Push-Benachrichtigung

5. Wählen Sie **[!UICONTROL Inhalt bearbeiten]**, um den Inhaltseditor für den ausgewählten Kanal zu öffnen.

6. Gestalten Sie Ihre Nachricht mit dem standardmäßigen Inhaltseditor:
   * Hinzufügen von Text, Bildern und anderen Inhaltselementen
   * Personalisierung verwenden, um kundenspezifische Informationen einzuschließen
   * Challenge-Details wie Fortschritt oder Belohnungen einschließen
   * Hinzufügen dynamischer Inhalte basierend auf Kundenattributen oder -verhalten

   Eine kanalspezifische Anleitung finden Sie unter:
   * [Erstellen von In-App-Nachrichten](../in-app/create-in-app.md)
   * [Erstellen von E-Mails](../email/create-email.md)
   * [Push-Benachrichtigungen erstellen](../push/create-push.md)

7. Wählen Sie **[!UICONTROL Speichern]**, um Ihre Nachricht zu speichern.

8. Wiederholen Sie diese Schritte, um bei Bedarf Nachrichten für andere Phasen oder Kanäle hinzuzufügen.

>[!NOTE]
>
>Sie können mehrere Nachrichten pro Stadium hinzufügen, sodass Sie Kunden über verschiedene Kanäle hinweg erreichen können. Sie können beispielsweise sowohl eine E-Mail als auch eine Push-Benachrichtigung senden, wenn eine Challenge gestartet wird.

### Zeitpunkt und Trigger der Nachricht {#message-timing}

**Startnachrichten** Werden gesendet, wenn die Challenge für die geeignete Zielgruppe aktiv wird.

**In Bearbeitung**: Wird ausgelöst, wenn Kunden einen bestimmten Fortschrittspunkt erreichen. Die Trigger-Bedingungen können wie folgt konfiguriert werden:

* Anzahl der abgeschlossenen Aufgaben
* Prozentsatz der abgeschlossenen Herausforderung
* Spezifische Aufgabenfertigstellung
* Verstrichene Zeit seit Beginn der Challenge

**Abgeschlossene Nachrichten**: Wird gesendet, wenn Kunden alle erforderlichen Aufgaben erfolgreich erledigen.

>[!TIP]
>
>**Best Practices für Messaging**:
>
>* Halten Sie die Botschaften kurz und konzentrieren Sie sich auf die Herausforderung
>* Deutliche Kommunikation des Werts und des Nutzens
>* Verwenden von konsistentem Branding und Ton
>* Klare Handlungsaufforderungen einschließen
>* Testen von Nachrichten vor der Veröffentlichung der Challenge

## Journey erstellen und anpassen {#generate-journey}

Wenn Sie eine Challenge mit konfigurierten Inhalten und Nachrichten speichern, generiert Journey Optimizer automatisch eine Journey im Backend.

### Funktionsweise der Journey-Generierung {#journey-generation-process}

1. Wenn Sie eine Challenge speichern und auf **[!UICONTROL Journey generieren]** klicken, erstellt Journey Optimizer eine neue Journey.

2. Die Journey wird automatisch nach dem Challenge-Namen benannt (z. B. „Challenge: [Your Challenge Name]„).

3. Die Journey-Arbeitsfläche umfasst:
   * **[!UICONTROL Audience lesen]**-Aktivität mit der ausgewählten Audience
   * **Inhaltskarte** Versandaktion
   * **Nachrichtenaktivitäten** für alle konfigurierten Nachrichten (Launch, In Bearbeitung, Abgeschlossen)
   * **Warten** und **Bedingung** Aktivitäten nach Bedarf basierend auf Ihrer Konfiguration

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. Die Journey wird im Journey-Inventar angezeigt und ist für alle Benutzerinnen und Benutzer mit entsprechenden Berechtigungen sichtbar.

### Anzeigen der generierten Journey {#view-journey}

So zeigen Sie die automatisch generierte Journey an:

1. Navigieren Sie im linken Navigationsmenü **&#x200B;**&#x200B;Journey.

2. Suchen Sie nach der Journey anhand des Challenge-Namens oder filtern Sie nach Tags, wenn Sie sie zugewiesen haben.

3. Wählen Sie die Journey aus, um die Arbeitsfläche und Konfiguration anzuzeigen.

### Journey anpassen {#customize-journey}

Sie können die automatisch generierte Journey bearbeiten, um benutzerdefinierte Logik, zusätzliche Aktivitäten oder erweiterte Konfigurationen hinzuzufügen.

>[!IMPORTANT]
>
>**Wichtige Überlegungen beim Bearbeiten von Journey**:
>
>* Änderungen, die an der Journey-Arbeitsfläche vorgenommen **nicht synchronisiert werden** mit der Benutzeroberfläche „Herausforderungen im Treueprogramm“
>* Die Herausforderung bleibt die Quelle der Wahrheit für die Definition des grundlegenden Erlebnisses
>* Journey Optimizer zeigt eine Warnung an, wenn Sie den benutzerdefinierten Bearbeitungsmodus aktivieren
>* Wenn Sie Änderungen an Aufgaben, Belohnungen oder Core-Challenge-Eigenschaften vornehmen müssen, bearbeiten Sie diese in der Benutzeroberfläche „Herausforderungen im Treueprogramm“, nicht auf der Journey
>* Benutzerdefinierte Journey-Bearbeitungen eignen sich für erweitertes Routing, Timing oder Integrationslogik

So passen Sie die Journey an:

1. Öffnen Sie die generierte Journey aus dem Journey-Inventar.

2. Journey Optimizer zeigt eine Warnung zur benutzerdefinierten Bearbeitung an. Lesen Sie die Warnung sorgfältig durch und bestätigen Sie sie.

3. Nehmen Sie die gewünschten Änderungen über die Journey-Arbeitsfläche vor:
   * Zusätzliche Aktivitäten hinzufügen (Wartezeiten, Bedingungen, Aktionen)
   * Konfigurieren von erweiterten Zeit- oder Häufigkeitsregeln
   * Hinzufügen benutzerdefinierter Aktionen oder Integrationen
   * Ändern der Einstiegsbedingungen für die Zielgruppe

4. Testen Sie Ihre Änderungen gründlich vor der Veröffentlichung.

5. Veröffentlichen Sie die Journey, wenn sie bereit ist.

Ausführliche Anleitungen zum Bearbeiten von Journey finden Sie unter [Erstellen von Journey](../building-journeys/journey-gs.md).

### Überlegungen zur Journey-Arbeitsfläche {#journey-considerations}

Beim Arbeiten mit automatisch generierten Journeys:

* **Zielgruppe kann nicht auf Journey bearbeitet werden**: Wenn Sie die Zielgruppe ändern müssen, wählen Sie diese Option in der Benutzeroberfläche „Herausforderungen im Treueprogramm“ aus und generieren Sie die Journey neu.

* **Aktualisierungen des Nachrichteninhalts**: Änderungen am Nachrichteninhalt sollten in der Benutzeroberfläche des Treueprogramms vorgenommen werden, um die Konsistenz zu gewährleisten.

* **Journey-Status**: Der Journey-Status (Entwurf, Live, Angehalten) wird unabhängig vom Challenge-Status verwaltet.

* **Testen**: Testen Sie das gesamte Challenge-Erlebnis, nicht nur das Journey, um sicherzustellen, dass alle Komponenten korrekt zusammenarbeiten.

## Überprüfen und veröffentlichen {#review-and-publish}

Vor der Veröffentlichung der Herausforderung:

1. **Überprüfen Sie alle Komponenten**:
   * Challenge-Eigenschaften und -Daten
   * Aufgaben und Aufgabenanforderungen
   * Konfiguration von Belohnungen
   * Gestaltung der Inhaltskarte
   * Nachrichteninhalt und -zeitpunkt
   * Erzeugte Journey-Struktur

2. **Testen des Erlebnisses**:
   * Testprofile zur Validierung des Inhalts-Renderings verwenden
   * Überprüfen, ob der Aufgaben-Trigger auf der Grundlage von Testdaten korrekt ausgeführt wurde
   * Belohnungsverteilungs-Logik überprüfen
   * Testen von Messaging über alle konfigurierten Kanäle hinweg
   * Überprüfen der Journey-Ausführung mit Testzielgruppen

3. **Veröffentlichen Sie Ihre Herausforderung**:
   * Wenn Sie bereit sind, wählen **[!UICONTROL in den Challenge]** Eigenschaften „Veröffentlichen“ aus.
   * Die Challenge wird am angegebenen Startdatum aktiv
   * Die automatisch generierte Journey wird aktiviert
   * Berechtigte Zielgruppenmitglieder können die Challenge sehen und an ihr teilnehmen.

## Herausforderungen bewältigen {#manage-challenges}

Nachdem Sie Herausforderungen im Zusammenhang mit dem Treueprogramm erstellt und veröffentlicht haben, können Sie diese anzeigen, bearbeiten, überwachen und optimieren, um sicherzustellen, dass sie die gewünschten Ergebnisse für Ihr Treueprogramm liefern.

### Status der Herausforderung {#challenge-statuses}

Jede Herausforderung durchläuft einen Lebenszyklus, der sich in ihrem Status widerspiegelt:

**[!UICONTROL Entwurf]**: Herausforderung wird erstellt oder bearbeitet, aber noch nicht veröffentlicht. Sie können alle Änderungen an den Herausforderungen für Entwürfe vornehmen.

**[!UICONTROL Geplant]**: Die Challenge wird veröffentlicht und am Startdatum aktiv. Kundinnen und Kunden können geplante Herausforderungen noch nicht sehen oder daran teilnehmen.

**[!UICONTROL Live]**: Die Challenge ist aktiv und Kundinnen und Kunden in der geeigneten Zielgruppe können sie sehen und daran teilnehmen. Dieser Status wird angezeigt, wenn das aktuelle Datum zwischen dem Start- und dem Enddatum liegt.

**[!UICONTROL Abgeschlossen]**: Die Herausforderung hat ihr Enddatum überschritten oder alle Ziele wurden erreicht. Kundinnen und Kunden können nicht mehr teilnehmen, Sie können jedoch historische Daten und Ergebnisse anzeigen.

**[!UICONTROL Angehalten]**: Die Herausforderung wurde vor dem Abschluss manuell angehalten. Kunden können nicht mehr teilnehmen. Um eine gestoppte Herausforderung erneut zu aktivieren, müssen Sie sie duplizieren und eine neue Version erstellen.

**[!UICONTROL Archiviert]**: Die Herausforderung wurde zu Organisationszwecken archiviert. Archivierte Challenges können mithilfe von Filtern abgerufen, aber in der Standardansicht ausgeblendet werden.

### Challenge-Details anzeigen {#view-details}

So zeigen Sie detaillierte Informationen zu einer Herausforderung an:

1. Klicken Sie im Inventar auf den Namen der Herausforderung oder wählen Sie das Menü **[!UICONTROL Mehr Aktionen]** (drei Punkte) und wählen Sie **[!UICONTROL Details anzeigen]**.

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. Der Bildschirm mit den Challenge-Details wird angezeigt:

   Registerkarte **[!UICONTROL Übersicht]**:
   * Allgemeine Eigenschaften (Name, Beschreibung, Typ, Datum)
   * Aktuelle Status- und Lebenszyklusinformationen
   * Zielgruppeninformationen
   * Erstellungs- und Änderungsverlauf

   Registerkarte **[!UICONTROL Aufgaben]**:
   * Liste aller Aufgaben in der Challenge
   * Aufgabentypen, Anforderungen und Bedingungen
   * Konfigurierte Belohnungen pro Aufgabe

   Registerkarte **[!UICONTROL Inhalt]**:
   * Konfiguration und Vorschau der Inhaltskarte
   * Visuelles Rendering der Herausforderungen für Kunden

   Registerkarte **[!UICONTROL Messaging]**:
   * Nachrichten für die Phasen Launch, In Bearbeitung und Abgeschlossen konfiguriert
   * Kanalzuweisungen und Inhaltsvorschauen

   Registerkarte **[!UICONTROL Leistung]** (für Live- und abgeschlossene Herausforderungen):
   * Teilnahmemetriken
   * Abschlussraten
   * Belohnungsverteilung
   * Statistiken zu Nachrichteninteraktionen

### Herausforderungen bearbeiten {#edit-challenges}

Herausforderungen können je nach ihrem aktuellen Status bearbeitet werden.

#### Entwurf von Herausforderungen bearbeiten {#edit-draft}

Für Herausforderungen im **[!UICONTROL Entwurf]**-Status:

1. Klicken Sie auf den Namen der Herausforderung oder wählen **[!UICONTROL Bearbeiten]** aus dem Aktionsmenü aus.

2. Ändern Sie einen beliebigen Aspekt der Herausforderung:
   * Allgemeine Eigenschaften
   * Aufgaben und Belohnungen
   * Inhaltskarten
   * Messaging
   * Zielgruppenauswahl

3. Wählen Sie **[!UICONTROL Als Entwurf speichern]**, um Änderungen ohne Veröffentlichung zu speichern, oder **[!UICONTROL Veröffentlichen]**, um die Herausforderung aktiv zu machen.

#### Veröffentlichte Herausforderungen bearbeiten {#edit-published}

Für Herausforderungen, die **[!UICONTROL Geplant]** oder **[!UICONTROL Live]** sind:

>[!IMPORTANT]
>
>**Auswirkungen der Bearbeitung von Live-Herausforderungen**: Änderungen an Live-Herausforderungen können sich auf bereits teilnehmende Kunden auswirken. Beachten Sie Folgendes, bevor Sie Änderungen vornehmen:
>
>* Durch die Änderung von Aufgabenanforderungen wird der Kundenfortschritt möglicherweise ungültig
>* Das Ändern von Belohnungen kann bei Kunden, die bereits Belohnungen erhalten haben, zu Inkonsistenzen führen
>* Zielgruppenänderungen können Kunden ausschließen, die zuvor berechtigt waren
>* Inhaltsänderungen werden Kunden sofort angezeigt
>
>Für wichtige Änderungen sollten Sie die aktuelle Herausforderung stoppen und eine neue Version erstellen.

**Eingeschränkte Bearbeitung für Live-**:

Sie können diese Änderungen an Live-Herausforderungen vornehmen, ohne sie zu stoppen:

* Beschreibung der Herausforderung aktualisieren (nach innen gerichtet)
* Ändern von Visualisierungen und Text auf der Inhaltskarte
* Nachrichteninhalt aktualisieren
* Enddatum anpassen (nur verlängern, nicht verkürzen)
* Hinzufügen oder Ändern von Tags

**Änderungen, die Duplizierungen erfordern**:

Um diese Eigenschaften zu ändern, müssen Sie die Challenge duplizieren und eine neue Version erstellen:

* Challenge-Typ (Standard, Streak, sequenziell)
* Aufgabenanforderungen und -bedingungen
* Belohnungswerte und Zuordnungsregeln
* Startdatum (für Live-Challenges)
* Zielgruppe (wesentliche Änderungen)

### Herausforderung duplizieren {#duplicate-challenge}

Beim Duplizieren wird eine Kopie einer bestehenden Challenge erstellt, die Sie ändern und als neue Challenge veröffentlichen können:

1. Wählen Sie im Inventar das Menü **[!UICONTROL Mehr Aktionen]** (drei Punkte) für die Herausforderung aus, die Sie duplizieren möchten.

2. Wählen Sie **[!UICONTROL Duplizieren]** aus.

3. Im Dialogfeld Duplizierung :
   * Einen neuen Namen für die duplizierte Challenge eingeben
   * Optional können Sie die Beschreibung ändern
   * Auswählen, ob Zielgruppeneinstellungen kopiert werden sollen
   * Auswählen, ob Nachrichtenkonfigurationen kopiert werden sollen

4. Wählen Sie **[!UICONTROL Duplizieren]** aus.

5. Die duplizierte Challenge wird im Entwurfsmodus geöffnet, in dem Sie vor der Veröffentlichung Änderungen vornehmen können.

**Häufige Duplizierungsszenarien**:

* Erneutes Ausführen einer erfolgreichen Challenge für einen neuen Zeitraum
* Varianten einer Herausforderung für verschiedene Zielgruppen erstellen
* Aufgabenanforderungen oder Prämien für eine neue Version aktualisieren
* Reaktivieren einer gestoppten oder abgeschlossenen Herausforderung

### Stoppen einer Challenge {#stop-challenge}

So stoppen Sie eine Live- oder geplante Herausforderung vor ihrem natürlichen Enddatum:

1. Wählen Sie die Herausforderung im Inventar aus.

2. Wählen **[!UICONTROL Herausforderung anhalten]** aus dem Aktionsmenü aus.

3. Überprüfen Sie im Bestätigungsdialog die Auswirkungen:
   * Derzeit teilnehmende Kunden können keine Fortschritte mehr machen
   * Kunden, die Aufgaben abgeschlossen haben, aber nicht die gesamte Herausforderung bewältigt haben, erhalten keine endgültigen Belohnungen
   * Die zugehörige Journey wird gestoppt
   * Die Challenge kann nicht neu gestartet werden (muss dupliziert werden, damit sie wiederverwendet werden kann)

4. Wählen Sie **[!UICONTROL STOP]** zur Bestätigung aus.

>[!NOTE]
>
>**Beenden vs. Abschließen**: Eine gestoppte Challenge endet vorzeitig und folgt nicht dem normalen Fertigstellungsprozess. Kunden erhalten bereits zugewiesene Teilprämien, jedoch keine Abschlussbelohnungen für die endgültige Herausforderung. Erwägen Sie, den betroffenen Kunden das frühe Ende zu kommunizieren.

### Herausforderungen bei der Archivierung {#archive}

Archivieren Sie abgeschlossene oder gestoppte Herausforderungen, um Ihren Bestand zu organisieren:

1. Wählen Sie das **[!UICONTROL Mehr Aktionen]** Menü (drei Punkte) für die Challenge aus.

2. Klicken Sie auf **[!UICONTROL Archivieren]**.

3. Die Challenge wechselt in den Status Archiviert und wird in der standardmäßigen Bestandsansicht ausgeblendet.

So zeigen Sie archivierte Herausforderungen an:

1. Wenden Sie im Inventar den Filter **[!UICONTROL Status]** an.

2. Wählen Sie **[!UICONTROL Archiviert]** aus.

3. Archivierte Challenges werden mit denselben Informationen angezeigt wie aktive Challenges.

So heben Sie die Archivierung einer Herausforderung auf:

1. Suchen Sie mithilfe von Filtern nach der archivierten Herausforderung.

2. Wählen **[!UICONTROL im]** die Option „Archivierung aufheben“.

3. Die Herausforderung kehrt zum vorherigen Status (Abgeschlossen oder Gestoppt) zurück.

### Herausforderungen löschen {#delete}

Löschen Sie nicht mehr benötigte Herausforderungen:

>[!IMPORTANT]
>
>**Löschung ist dauerhaft**: Gelöschte Herausforderungen können nicht wiederhergestellt werden. Löschen Sie Herausforderungen nur, wenn Sie sicher sind, dass Sie sie in Zukunft nicht mehr benötigen werden. Zur Pflege historischer Datensätze sollten Sie lieber archivieren anstatt löschen.

**Löschregeln**:

* Sie können Herausforderungen nur im Status **[!UICONTROL Entwurf]** löschen
* Veröffentlichte, geplante, Live- oder abgeschlossene Herausforderungen können nicht gelöscht werden
* Um eine veröffentlichte Herausforderung zu entfernen, müssen Sie sie zuerst stoppen und dann archivieren

So löschen Sie eine Entwurfsherausforderung:

1. Wählen Sie das **[!UICONTROL Mehr Aktionen]** Menü (drei Punkte) für die Challenge aus.

2. Wählen Sie **[!UICONTROL Löschen]** aus.

3. Bestätigen Sie den Löschvorgang im Bestätigungsdialogfeld.

## Überwachen der Leistung {#monitor-performance}

Verfolgen Sie mithilfe integrierter Leistungsmetriken, wie Kunden mit Ihren Herausforderungen interagieren.

### Leistungsmetriken {#performance-metrics}

Auf der Registerkarte Performance werden Schlüsselmetriken für Live- und abgeschlossene Herausforderungen angezeigt:

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Teilnahmemetriken]**:

* **Berechtigte Kunden insgesamt**: Anzahl der Kunden in der Zielgruppe
* **Registrierte Kunden**: Anzahl der Kunden, die die Challenge angesehen oder an ihr teilgenommen haben
* **Enrollment rate**: Prozentsatz der berechtigten Kunden, die sich registriert haben
* **Aktive Teilnehmer**: Anzahl der Kunden, die derzeit Fortschritte machen

**[!UICONTROL Abschlussmetriken]**:

* **Abgeschlossene Kunden**: Anzahl der Kunden, die alle Aufgaben abgeschlossen haben
* **Abschlussrate**: Prozentsatz der registrierten Kunden, die die Herausforderung abgeschlossen haben
* **Durchschnittliche Abschlusszeit**: Durchschnittliche Zeit von der Registrierung bis zum Abschluss
* **Abgeschlossene Aufgaben**: Gesamtzahl der individuellen Aufgaben, die für alle Kunden abgeschlossen wurden

**[!UICONTROL Belohnungsmetriken]**:

* **Gesamtprämien verteilt**: Summe aller zugewiesenen Prämien
* **Belohnungen nach**: Aufschlüsselung nach Punkten, Rabatten, kostenlosen Artikeln usw.
* **Durchschnittliche Belohnung pro Kunde**: Durchschnittlicher Belohnungswert für teilnehmende Kunden

**[!UICONTROL Interaktionsmetriken]**:

* **Impressions der Inhaltskarte**: Anzahl der Fälle, in denen die Challenge angezeigt wurde
* **Inhaltskarten-Klicks**: Anzahl der Interaktionen von Kunden mit der Challenge-Karte
* **Nachrichtenversand**: Anzahl der Nachrichten, die für die Phasen „Launch“, „In Bearbeitung“ und „Abgeschlossen“ gesendet wurden
* **Interaktion mit Nachrichten**: Öffnungsraten, Klickraten für Nachrichten nach Stadium und Kanal

### Anzeigen von Leistungsberichten {#view-reports}

So greifen Sie auf detaillierte Leistungsdaten zu:

1. Öffnen Sie die Challenge und navigieren Sie zur Registerkarte **[!UICONTROL Performance]** .

2. Wählen Sie den Datumsbereich für das Reporting aus (heute, letzte 7 Tage, letzte 30 Tage, benutzerdefinierter Bereich).

3. Metriken überprüfen nach:
   * **Übersicht**: Allgemeine Zusammenfassung der Schlüsselmetriken
   * **Zeitleiste**: Leistungstrends im Zeitverlauf
   * **Aufschlüsselung**: Metriken segmentiert nach Kundenattributen, Kanälen oder Aufgaben

4. Exportieren Sie Berichte mithilfe der **[!UICONTROL Exportieren]**-Schaltfläche zur weiteren Analyse.

### Überwachen der generierten Journey {#monitor-journey}

Die automatisch generierte Journey enthält wertvolle Ausführungsdaten:

1. Wählen Sie in den Challenge-Details **[!UICONTROL Journey anzeigen]**, um die zugehörige Journey zu öffnen.

2. Überprüfen Sie auf der Journey-Arbeitsfläche Folgendes:
   * **Journey-Bericht**: Gesamtausführungsstatistiken
   * **Aktivitätsberichte**: Leistung einzelner Aktivitäten
   * **Eintritts- und Ausstiegsmetriken**: Wie viele Kunden eingetreten und ausgetreten sind
   * **Fehlerprotokolle**: Alle Ausführungsprobleme oder Fehler

3. Verwenden Sie die Journey-Überwachung zur Identifizierung von:
   * Engpässe, bei denen Kunden abbrechen
   * Technische Probleme mit dem Versand
   * Nachrichtenleistung nach Kanal
   * Zeitliche Optimierungsmöglichkeiten

Ausführliche Anleitungen zur Journey-Überwachung finden Sie unter [Überwachen Ihrer Journey](../building-journeys/report-journey.md).

### Herausforderungen optimieren {#optimize}

Leistungsdaten zur Verbesserung aktueller und künftiger Herausforderungen verwenden:

**[!UICONTROL Testvarianten]**: Erstellen Sie doppelte Herausforderungen mit verschiedenen Aufgaben, Belohnungen oder Botschaften, um die Leistung zu vergleichen.

**[!UICONTROL Zeitplan anpassen]**: Ändern Sie die Aufgabendauer oder Aufgabenfristen basierend auf Fertigstellungsmustern.

**[!UICONTROL Zielgruppe verfeinern]**: Erweitern oder grenzen Sie die Zielgruppenauswahl auf der Grundlage der Interaktions- und Abschlussraten ein.

**[!UICONTROL Inhalt aktualisieren]**: Aktualisieren Sie Inhaltskarten und Messaging, um Interesse und Klarheit zu wahren.

**[!UICONTROL Belohnungsoptimierung]**: Passen Sie Belohnungswerte an, um Kosten und Beteiligung auszugleichen.

**[!UICONTROL Schwierigkeit der Aufgabe]**: Ändern Sie Aufgabenanforderungen, wenn sie basierend auf Abschlussdaten zu einfach oder zu schwierig sind.

## Validierung und Testen von Aufgaben {#validation-testing}

Überprüfen Sie vor dem Veröffentlichen der Challenge, ob die Aufgaben korrekt konfiguriert sind:

1. **Aufgabenlogik überprüfen**:
   * Überprüfen, ob die Mengenanforderungen realistisch sind
   * Sicherstellen, dass die Produktfilterkriterien korrekt sind
   * Überprüfen, ob die Belohnungen ordnungsgemäß konfiguriert sind

2. **Testen mit Testprofilen**:
   * Erstellen von Testprofilen für verschiedene Kundenszenarien
   * Senden von Testereignissen über die Datenaufnahme-Pipeline
   * Überprüfen, ob der Aufgaben-Trigger korrekt ist
   * Belohnungen werden wie erwartet zugewiesen

3. **Datenzuordnung überprüfen**:
   * Sicherstellen, dass eingehende Ereignisdaten den Aufgabenanforderungen korrekt zugeordnet werden
   * Überprüfen Sie, ob SKUs, Kategorien und Attribute zwischen Ihrem Quellsystem und Journey Optimizer übereinstimmen
   * Testen von Edge-Fällen (fehlende Daten, ungültige Werte usw.)

## Best Practices {#best-practices}

### Challenge-Erstellung

**Einfach beginnen**: Beginnen Sie Ihre erste Herausforderung mit einer einfachen Standardaufgabe, um sich mit dem Prozess vertraut zu machen.

**Gründlich testen** Testen Sie Ihre Herausforderung immer mit Testprofilen und Audiences, bevor Sie sie in Ihrem gesamten Kundenstamm veröffentlichen.

**Klare Kommunikation** Stellen Sie sicher, dass Kunden verstehen, was sie tun müssen, was sie verdienen werden und bis wann.

**Realistisches Timing**: Legen Sie ein angemessenes Start- und Enddatum fest, sodass Kunden genügend Zeit haben, die Herausforderung zu bewältigen.

**Attraktive Prämien**: Machen Sie Prämien wertvoll und für Ihre Zielgruppe relevant, um die Teilnahme zu fördern.

### Aufgabenkonfiguration

**Klare Anforderungen**: Machen Sie Aufgabenanforderungen klar und erreichbar. Übermäßig komplexe Bedingungen vermeiden.

**Angemessene Schwierigkeit**: Schwierigkeit der Aufgabe mit Belohnungswert in Einklang bringen. Schwierige Aufgaben sollten sich besser auszahlen.

**Genauigkeit der Produktfilterung**: Überprüfen Sie SKUs, Kategorien und Attribute genau, um einen genauen Produktabgleich sicherzustellen.

**Progressive Prämien**: Verwenden Sie Meilenstein-Prämien (nach Abschluss der Aufgabe), um die Kundeninteraktion während der gesamten Challenge aufrechtzuerhalten.

**Flexibilität**: Geben Sie Kunden bei standardmäßigen Herausforderungen Flexibilität bei der Ausführung von Aufgaben, um verschiedene Verhaltensweisen und Vorlieben zu berücksichtigen.

### Verwaltung und Überwachung

**Regelmäßiges Monitoring**: Überprüfen Sie die Challenge-Leistung mindestens einmal wöchentlich auf Live-Challenges, um Probleme frühzeitig zu erkennen.

**Eindeutige Benennung**: Verwenden Sie beschreibende Namen, die den Challenge-Zweck, die Audience oder den Zeitraum für eine einfache Organisation angeben.

**Tags verwenden**: Wenden Sie konsistente Tags an, um Herausforderungen nach Kampagne, Saison, Zielgruppensegment oder anderen relevanten Attributen zu kategorisieren.

**Dokumentänderungen**: Notieren Sie sich, warum Sie Änderungen an den Herausforderungen vorgenommen haben, damit Sie sie später kennenlernen und nutzen können.

**Konsistent archivieren**: Archivieren Sie abgeschlossene Herausforderungen regelmäßig, um Ihr Inventar überschaubar zu halten.

**Änderungen mitteilen**: Wenn Sie eine Live-Challenge ändern, informieren Sie die betroffenen Kunden über Änderungen, die sich auf ihre Teilnahme auswirken.

**Analysieren nach Abschluss**: Überprüfen Sie die Leistung nach dem Ende jeder Herausforderung, um Erkenntnisse für künftige Herausforderungen zu ermitteln.

**Schrittweiser Rollout**: Bei neuen Herausforderungen oder wichtigen Änderungen sollten Sie vor der vollständigen Bereitstellung mit einer kleineren Zielgruppe beginnen.

**Versionskontrolle**: Verwenden Sie beim Erstellen von Iterationen eine klare Versionierung in Challenges (z. B. „Holiday Challenge 2024 - v2„).

## Fehlerbehebung {#troubleshooting}

**Herausforderung erscheint Kunden nicht**:

* Überprüfen Sie, ob die Challenge im Live-Status ist
* Überprüfen, ob sich Kundinnen und Kunden in der zulässigen Zielgruppe befinden
* Bestätigen Sie, dass die Konfiguration der Inhaltskarte korrekt ist
* Überprüfen der Journey-Ausführungsprotokolle auf Versandprobleme

**Niedrige Beteiligungsquoten**:

* Sichtbarkeit und Attraktivität der Inhaltskarte überprüfen
* Prüfen, ob Messaging den Wert klar vermittelt
* Sicherstellen, dass Aufgaben erreichbar und Belohnungen attraktiv sind
* Überprüfen, ob die Zielgruppenbestimmung geeignet ist

**Aufgaben werden nicht**:

* Überprüfen, ob Daten korrekt von den Quell-Connectoren aufgenommen werden
* Überprüfen, ob die Ereignisattribute den Aufgabenanforderungen entsprechen
* Berechtigung der Zielgruppe überprüfen

**Belohnungen werden nicht zugewiesen**:

* Bestätigen, dass die Belohnungskonfiguration korrekt ist
* Verbindung mit externem Treueprogramm überprüfen
* Fehlersuche in den Belohnungsversand-Logs

**Produktfilter funktionieren nicht**:

* SKU-Codes und Kategorienamen überprüfen
* Sicherstellen, dass die Attributzuordnung korrekt ist
* Testen mit Beispielkaufdaten

**Journey wird nicht generiert**:

* Bestätigen, dass alle erforderlichen Konfigurationen abgeschlossen sind
* Fehlersuche in der Registerkarte „Messaging“
* Überprüfen, ob die Inhaltskarte konfiguriert ist
* Überprüfen der Systemfehlerprotokolle

**Leistungsdaten werden nicht**:

* Warten Sie bis zur Ausbreitung von Daten (bis zu 24 Stunden)
* Überprüfen, ob Ereignisse korrekt verfolgt werden
* Überprüfen des Datenerfassungsstatus
* Sicherstellen, dass Kunden begonnen haben, teilzunehmen

## Beta-Feedback {#beta-feedback}

Während der Beta-Phase ist Ihr Feedback nützlich, um uns bei der Verbesserung der Herausforderungen im Zusammenhang mit der Kundentreue zu unterstützen. Bitte teilen Sie Ihre Erfahrungen, Fragen und Vorschläge mit Ihrem Adobe-Support-Mitarbeiter oder über die Beta-Feedback-Kanäle, die beim Start bereitgestellt wurden.

## Verwandte Themen {#related-topics}

* [Erstellen von Zielgruppen in Journey Optimizer](../audience/about-audiences.md)
* [Entwerfen von Inhaltskarten](../content-card/design-content-card.md)
* [Erstellen von In-App-Nachrichten](../in-app/create-in-app.md)
* [Erstellen von E-Mails](../email/create-email.md)
* [Push-Benachrichtigungen erstellen](../push/create-push.md)
* [Journey erstellen](../building-journeys/journey-gs.md)
* [Journey überwachen](../building-journeys/report-journey.md)
* [Dokumentation zu Experience Platform-Quellen](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [Konfigurieren von Quell-Connectoren in Journey Optimizer](../start/get-started-sources.md)
