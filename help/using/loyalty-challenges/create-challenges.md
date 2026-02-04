---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen bei der Treue schaffen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit Treueprogrammen erstellen und konfigurieren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 1%

---


# Herausforderungen schaffen {#create-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* **Herausforderungen erstellen** ◀︎ **Sie sind hier** - Herausforderungen erstellen und konfigurieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Erstellen einer Herausforderung für das Treueprogramm"
>abstract="Erstellen Sie eine Herausforderung zum Treueprogramm, um das Interaktionsangebot zu definieren, Inhaltskarten für den Versand zu konfigurieren, Aufgaben hinzuzufügen, Belohnungen einzurichten und optional das Messaging kanalübergreifend zu konfigurieren."

## Bevor Sie beginnen {#before-you-start}

Bevor Sie eine Herausforderung erstellen, stellen Sie sicher, dass Sie Folgendes haben:

* Datenaufnahme über Quell-Connectoren konfiguriert und validiert
* Erforderliche Zielgruppen in Experience Platform erstellt
* Vorbereitete Content-Assets (Bilder, Text usw.) für Ihre Herausforderung
* Sie haben die Aufgaben und Belohnungen definiert, die Sie anbieten möchten

## Erstellen einer Challenge {#create-a-challenge}

Ausführliche Schritte zum Erstellen von Herausforderungen, einschließlich:
* Konfiguration der Challenge-Eigenschaften
* Challenge-Typen (Standard, Streak, sequenziell)
* Zielgruppenauswahl
* Konfiguration des Datums

## Aufgaben hinzufügen {#add-tasks}

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

## Konfigurieren von Inhaltskarten {#configure-content-cards}

Ausführliche Schritte zur Konfiguration von Inhaltskarten, einschließlich:
* Einrichtung der Inhaltskarte
* Design und Personalisierung
* Vorschau und Tests

## Konfigurieren von Messaging {#configure-messaging}

Ausführliche Anweisungen zur Konfiguration von Multi-Channel-Messaging:
* Nachrichtenkanäle (In-App, E-Mail, Push)
* Nachrichtenstadien (Start, in Bearbeitung, abgeschlossen)
* Zeitpunkt und Trigger der Nachricht

## Überprüfen und veröffentlichen {#review-and-publish}

Vor der Veröffentlichung der Herausforderung:

1. **Alle Komponenten überprüfen**: Challenge-Eigenschaften, Aufgaben, Belohnungen, Inhalte, Messaging
2. **Testen des Erlebnisses**: Verwenden Sie Testprofile, um Inhalt und Aufgaben-Trigger zu validieren
3. **Veröffentlichen**: Machen Sie die Herausforderung für Ihre Zielgruppe aktiv

Die automatisch generierte Journey wird am angegebenen Startdatum aktiviert.

## Nächste Schritte {#next-steps}

* [Herausforderungen verwalten](manage-challenges.md) - Erfahren Sie, wie Sie Herausforderungen bearbeiten, überwachen und optimieren können.
* [Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Funktionen und Möglichkeiten überprüfen
