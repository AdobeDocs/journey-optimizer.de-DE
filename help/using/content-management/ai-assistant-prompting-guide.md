---
solution: Journey Optimizer
product: journey optimizer
title: Leitfaden zu Inhalts-Prompts des KI-Assistenten
description: Erfahren Sie, wie Sie mit dem CO-STAR-Framework effektive Prompts zur KI-gestützten Inhaltsgenerierung erstellen können, um markenkonforme Marketing-Inhalte mit hohen Konversionsraten zu erstellen.
topic: Artificial Intelligence
role: User
level: Intermediate
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 100%

---

# Best Practices für Prompts im KI-Assistenten {#ai-assistant-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_ai_assistant_prompt"
>title="Beispiele für Prompts"
>abstract="In der Journey Optimizer-Dokumentation erfahren Sie, wie Sie effektive Prompts erstellen, die markenkonforme Marketing-Inhalte mit hoher Konversionsrate generieren."

Dieser Leitfaden hilft Ihnen, Ihre Anfragen zu strukturieren, Ihre Absichten klar und deutlich zu kommunizieren und sicherzustellen, dass die KI Nachrichten generiert, die auf Ihre Markenrichtlinien, Zielgruppenanforderungen und Kampagnenziele abgestimmt sind.
Erfahren Sie, wie Sie effektive Prompts schreiben, mit denen der KI-Assistent hochwertige markenkonforme Marketing-Inhalte generieren kann, die auf Ihre Ziele abgestimmt sind.

## Verwenden des CO-STAR-Frameworks {#costar-framework}

Um mit dem KI-Assistenten optimale Ergebnisse zu erzielen, sollten Sie die Prompts mithilfe des CO-STAR-Frameworks organisieren. Dieser strukturierte Ansatz stellt sicher, dass die KI genau versteht, was Sie benötigen.

| Komponente | Bedeutung | Warum dies wichtig ist |
|-|-|-|
| **C – Kontext** | Hintergrund zur Kampagne, zum Produkt oder zur Situation | Hilft der KI, das Gesamtbild zu erfassen |
| **O – Ziel** | Ihr spezifisches Marketing-Ziel | Gibt an, was mit dem Inhalt erreicht werden soll |
| **S – Stil** | Gewünschte Art der Kommunikation | Legt den Ansatz fest |
| **T – Ton** | Die Emotion von Stil und Sprache | Gestaltet das Gefühl Ihrer Nachricht |
| **A – Zielgruppe** | Die angesprochene Zielgruppe | Stellt sicher, dass die Nachricht bei den richtigen Personen Anklang findet |
| **R – Anforderungen** | Spezifische Einschränkungen oder unverzichtbare Komponenten | Definiert Grenzen und kritische Elemente |

## Grundlagen zu KI-Prompts {#key-takeaways}


### Worauf Sie achten müssen


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Empfohlen</th>
<th>Zu vermeiden</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>CO-STAR-Framework zur Strukturierung verwenden</p>
<p>Scharf zwischen neuen und vorhandenen Inhalten trennen</p>
<p>Vor allem Dokumente mit spezifischer Extraktionsanleitung verwenden</p>
<p>Dropdown-Auswahlfelder für Ton, Strategie und Gebietsschema verwenden</p>
<p>Marketing-Ziele auf die Funktionalität der Inhaltstypen abstimmen</p>
<p>Mehrere Varianten für A/B-Tests generieren</p>
</td>
<td>
<p>In Prompts Strukturänderungen, Formate oder Bildbearbeitung anfordern</p>
<p>Ton/Strategie in Prompts erwähnen, obwohl dies in Dropdown-Menüs verfügbar ist</p>
<p>Schwammige Ziele wie „unser Produkt bewerben“ formulieren</p>
<p>Auswahl bedingter Elemente anfordern</p>
<p>Layout-Änderungen über Prompts erwarten</p>
</td>
</tr>
</tbody>
</table>

### In Prompts nicht unterstützte Inhalte

>[!TIP]
>
>Verwenden Sie den **E-Mail-Editor** oder **Adobe Express** für Änderungen an visuellen Komponenten/Bildern.

Diese Anfragen werden nicht unterstützt und sollten über andere Tools verarbeitet werden:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✕ Änderungen an der E-Mail-Struktur</th>
<th>✕ Änderungen am visuellen Stil</th>
<th>✕ Bildbearbeitungsvorgänge</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Auswählen bestimmter zu ändernder Abschnitte</li>
<li>Löschen oder Klonen von Elementen</li>
<li>Bedingte Auswahlen</li>
<li>Hinzufügen oder Entfernen von Layout-Abschnitten</li>
</ul>
</td>
<td>
<ul>
<li>Textformatierung (fett, kursiv, Schriftgröße)</li>
<li>Farbänderungen</li>
<li>Layout-Stile (Rahmen, Abstände, Ränder)</li>
<li>Visuelle Effekte (Schatten)</li>
</ul>
</td>
<td>
<ul>
<li>Hintergrundänderungen</li>
<li>Hinzufügen von Textüberlagerungen oder Logos</li>
<li>Zuschneiden oder Ändern der Größe von Bildern</li>
<li>Farbkorrekturen</li>
<li>Bildersetzung</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Qualitäts-Checkliste {#quality-checklist}

Stellen Sie vor dem Generieren von Inhalten Folgendes sicher:

&amp;check; **Klares Ziel**: Gibt die Aktion, das Produkt/den Service, den Wert und den Kontext klar an.

&amp;check; **Zielgruppe definiert**: Gibt die Demografie, die Rolle oder das Segment an.

&amp;check; **Inhaltstypen abgestimmt**: Ziel passt zum ausgewählten Kanal oder Format.

&amp;check; **Dropdown-Auswahl konfiguriert**: Ton, Strategie und Gebietsschema sind ausgewählt, nicht im Prompt enthalten.

&amp;check; **Dokumentfokus festgelegt**: Hebt hervor, welche Inhalte oder Abschnitte referenziert werden.

&amp;check; **Marke angewendet**: Passende Markenrichtlinien sind ausgewählt.

&amp;check; **Realistischer Umfang**: Vermeiden Sie Anfragen nach Layout-Änderungen, Formatierungen oder Bearbeitungen der Struktur.

## Formulieren effektiver Marketing-Ziele {#marketing-objectives}

### Seien Sie präzise und aktionsorientiert.

Achten Sie bei der Formulierung von Marketing-Zielen darauf, dass diese klar, umsetzbar und messbar sind. Vermeiden Sie schwammige oder generische Aussagen.

**Beispiele für gute Ziele:**

&amp;check; „Fördere die Anmeldungen bei unserer kostenlosen 30-tägigen Testversion des neuen KI-gestützten Analyse-Dashboards“

&amp;check; „Generiere Leads für unser B2B-Webinar zum Thema ,Reduzieren der Cloud-Kosten um 40 %‘, das am 15. März stattfindet“

&amp;check; „Bewirb unseren zeitlich begrenzten Weihnachtsrabatt von 25 % auf Premium-Abonnements, der am 25. Dezember endet“

**Beispiele zu vermeidender Formulierungen:**

✕ „Bewirb unser Produkt“ (zu schwanmig)

✕ „Sorg dafür, dass Produkte gekauft werden“ (unklarer Wert)

✕ „Sende E-Mails zu neuen Funktionen“ (fehlende Absicht)

### Strukturieren des Ziels

Geben Sie immer den Kontext und das Wertversprechen an, damit die KI relevante Inhalte generieren kann.
Verwenden Sie diese Formel, um effektive Ziele zu formulieren: **Aktion + Produkt/Service + Wert/Nutzen + Dringlichkeit/Kontext**

**Beispiele für gute Ziele:**

&amp;check; „Fordere zu Downloads unserer neuen App auf, die Benutzerinnen und Benutzern dabei hilft, nachhaltige Lebensgewohnheiten mit personalisierten umweltfreundlichen Empfehlungen zu verfolgen“

&amp;check; „Bewirb die Anmeldung für unseren exklusiven Workshop über fortschrittliche Datenvisualisierungstechniken für Marketing-Fachleute“

&amp;check; „Erhöhe die Teilnehmerzahl bei unserer Produkteinführungsveranstaltung, auf der der revolutionäre KI-Schreibassistent vorgestellt wird, der mehr als 5 Stunden pro Woche einspart“

**Beispiele zu vermeidender Formulierungen:**

✕ „Kündige die neue App an“ (Wertversprechen und Kontext fehlen)

✕ „Veranlasse Personen, sich für den Workshop anzumelden“ (Spezifizierung von Zielgruppe und Nutzen fehlt)

✕ „Bewirb eine Veranstaltung“ (Aktion, Wert und Dringlichkeit nicht klar)

## Erstellen neuer Inhalte oder Ändern vorhandener Inhalte {#new-vs-modify}

Geben Sie klar an, ob Ihre Anfrage die Erstellung neuer Inhalte oder die Aktualisierung vorhandener Materialien beinhaltet. Diese Unterscheidung ist wichtig, da sie die KI bei der Auswahl des geeigneten Ansatzes anleitet und ein genaueres und hilfreicheres Ergebnis sicherstellt.

### Erstellen neuer Inhalte

Wenden Sie diese Strategie an, wenn Sie Marketing-Kampagnen starten, neue Produkte vorstellen oder eine beliebige Form von aktualisierter oder neu gestalteter Kommunikation beginnen. So stellen Sie sicher, dass Ihre Botschaft von Anfang an erfolgreich ist und sich an Ihren Zielen ausrichtet.

**So formulieren Sie Prompts** ➤ Konzentrieren Sie sich bei der Erstellung neuer Inhalte auf Ihr Marketing-Ziel, ohne auf vorhandene Inhalte zu verweisen.

>[!BEGINSHADEBOX]

**Beispiele:**

* **SaaS-Testversion**: „Präsentiere Kleinunternehmen unsere neue CRM-Software, betone die Zeitersparnis von 50 %, die 90 % schnellere Lead-Qualifizierung und das Angebot einer 30-tägigen kostenlosen Testversion mit personalisiertem Onboarding“
* **Funktionsankündigung**: „Kündige neue API-Integrationsfunktionen an, die die Entwicklungszeit für Unternehmenskunden um 60 % verkürzen und sich an technische Entscheidungstragende richten.“
* **Bewerbung einer Veranstaltung**: „Fördere Anmeldungen bei unserem Webinar zu ,Digital Marketing Trends 2024‘, in dem Fachleute von Google, Meta und Adobe vertreten sind, und betone die umsetzbaren Erkenntnisse und die begrenzte Anzahl von Plätzen (max. 500).“

>[!ENDSHADEBOX]

### Ändern vorhandener Inhalte

>[!TIP]
>
>Bei Standardänderungen, z. B. Ausarbeitung, Zusammenfassung oder Vereinfachung verwenden Sie die Funktion **Verfeinern**, anstatt benutzerdefinierte Prompts zu formulieren. [Weitere Informationen](generative-uc.md##refine)

Gehen Sie so vor, wenn Sie Ihre aktuellen Marketing-Kampagnen aktualisieren oder anpassen müssen. Diese Methode unterstützt inkrementelle Verbesserungen, um sicherzustellen, dass Ihr Messaging relevant bleibt, ohne dass Sie von Grund auf neu beginnen müssen.

**So formulieren Sie Prompts** ➤ Geben Sie beim Ändern vorhandener Inhalte klar an, was Sie ändern möchten und wie dies erfolgen soll.

>[!BEGINSHADEBOX]

**Beispiele:**

* **Kampagnenaktualisierung**: „Ändere die E-Mail zur Produkteinführung so, dass der Fokus auf Unternehmenssicherheitsfunktionen statt auf allgemeinen Produktivitätsvorteilen liegt und Entscheidungstragende aus der IT mit Compliance-Zertifizierungen angesprochen werden.“
* **Zielgruppe ausrichten**: „Passe unsere Software-Demoeinladung an, damit gezielt das Gesundheitswesen angesprochen wird, und ersetze allgemeine Beispiele durch Anwendungsfälle aus dem Gesundheitswesen und Vorteile bei der HIPAA-Compliance“
* **Saisonale Aktualisierung**: „Aktualisiere unsere Werbekampagne für das 4. Quartal zum Geschenkekauf und verschiebe den Fokus vom Schulanfang auf Weihnachtsgeschenke mit Betonung auf schnellem Versand.“

>[!ENDSHADEBOX]

## Verbessern von Prompts mit erweiterten Einstellungen {#personalize-prompt}

### Arten von Kommunikationsstrategie

>[!TIP]
>
>Verwenden Sie für eine spezielle Verarbeitung das Dropdown-Menü „Kommunikationsstrategie“ im Menü „Texteinstellungen“, anstatt die Strategie im Prompt zu erwähnen.

Ihre Kommunikationsstrategie bestimmt, wie Sie Ihre Botschaft präsentieren, um die Wirkung zu maximieren. Je nach den Zielen eignen sich unterschiedliche Strategien besser, sei es beim Vermitteln von Dringlichkeit, beim Aufbau von Vertrauen oder beim Fördern sofortiger Handlungen. Wählen Sie die Strategie aus, die am besten zu Ihren Kampagnenzielen und zur Mentalität Ihrer Zielgruppe passt.

| **Strategie** | **Geeignet für** | **Messaging-Stil** | **Beispiele** |
|--------------|--------------|------------------------|--------------|
| **Dringlich** | Zeitkritische Angebote, Fristen, sofortiges Handeln | Erstellt unmittelbaren Druck durch zeitbasierte Sprache | „Jetzt handeln: Angebot läuft um Mitternacht ab“ <br> „Registrieren Sie sich noch heute, bevor alle Plätze besetzt sind“ <br> „Der 48-Stunden-Blitzverkauf beginnt jetzt“ |
| **FOMO (Angst, etwas zu verpassen)** | Zeitlich begrenzte Angebote, Veranstaltungen, exklusiver Zugriff | Verwendet Signale, die Dringlichkeit, begrenzte Stückzahlen und Zeitdruck vermitteln | „Nur noch 24 Stunden! Begrenzter Bestand mit 40 % Rabatt“ <br> „Letzte Chance: Frühbucherpreis endet morgen“ <br> „Nur noch 100 Plätze im Beta-Programm“ |
| **Social Proof** | Vertrauensbildung, Erfahrungsberichte, beliebte Produkte | Nutzt die Erfahrungen und Bewertungen anderer Benutzerinnen und Benutzer | „Schließen Sie sich unseren mehr als 50.000 zufriedenen Kundinnen und Kunden an“ <br> „Von Branchenfachleuten mit 4,9/5 Sternen bewertet“ <br> „Die Lösung, der Fortune 500-Unternehmen vertrauen“ |
| **Begrenzte Stückzahlen** | Begrenzter Bestand, exklusive Versionen, stark nachgefragte Artikel | Betont begrenzte Verfügbarkeit und Exklusivität | „Nur noch 5 Stück auf Lager“ <br> „Limitierte Auflage: 100 Stück verfügbar“ <br> „Exklusive Veröffentlichung: Wer zuerst kommt, mahlt zuerst“ |
| **Incentive** | Werbeaktionen, Prämienprogramme, Sonderangebote | Hebt konkrete Vorteile und Prämien hervor | „Erhalten Sie 20 % Rabatt auf Ihre erste Bestellung“ <br> „Verdienen Sie an diesem Wochenende doppelte Punkte“ <br> „Kostenloser Versand bei Bestellungen über 50 Euro“ |
| **Exklusivität** | Premium-Produkte, VIP-Erlebnisse, Angebote nur für Mitglieder | Verwendet Premium-Positionierung und Sprache für speziellen Zugang | „Exklusive Einladung zu unserer privaten Vorschau“ <br> „Erweiterte Analysen mit der Elite-Mitgliedschaft“ <br> „Schließen Sie sich ausgewählten Fortune 500-Unternehmen an, die bereits mit uns arbeiten“ |
| **Gamification** | Interaktionskampagnen, Treueprogramme, interaktive Inhalte | Verwendet Spielmechanik und auf Erfolge bezogene Sprache | „Schalten Sie Ihre nächste Prämienstufe frei“ <br> „Schließen Sie Herausforderungen ab und verdienen Sie Abzeichen“ <br> „Erobern Sie die Spitze der Rangliste und erhalten Sie exklusive Preise“ |
| **Information** | Bildung, Forschung, komplexe Produkte, Innovationen | Verwendet Fakten, Daten, Erkenntnisse und Erklärungen | „5 Erkenntnisse aus der Analyse von über 10.000 Interaktionen“ <br> „Neue Forschung zeigt 3 bahnbrechende Ansätze“ <br> „Vollständiger Leitfaden zur Implementierung von KI im Marketing“ |
| **Bildung und Erkenntnisse** | Lerninhalte, Branchen-Trends, Best Practices | Bietet wertvolles Wissen und umsetzbare Erkenntnisse | „Meistern Sie fortschrittliche Techniken mit unserem Expertenhandbuch“ <br> „Entdecken Sie 7 Strategien der Top-Marketing-Fachleute“ <br> „Erfahren Sie in 5 Schritten, wie Sie Ihren Workflow optimieren können“ |

### Festlegen des passenden Tons {#tone}

>[!TIP]
>
>Verwenden Sie die Dropdown-Liste „Ton“ im Menü „Texteinstellungen“, anstatt den Ton im Prompt anzugeben.

Der Ton bestimmt, wie Ihre Zielgruppe Ihre Nachricht wahrnimmt und darauf reagiert. Wählen Sie stets einen Ton aus, der zu Ihrer Markensprache und der Journey-Phase des Profils passt.

In der folgenden Tabelle finden Sie Details zu jedem Ton sowie die geeigneten Anwendungsfälle und Beispiele für Inhalte, die zum jeweiligen Stil passen.

| Tonalität | Geeignet für | Inhaltsbeispiel |
|-|-|-|
| Professionell | B2B-Kommunikation, formelle Ankündigungen | „Wir freuen uns, unsere strategische Partnerschaft mit … bekannt geben zu können“ |
| Einfühlsam | Kunden-Support, sensible Themen | „Wir verstehen, wie frustrierend das für Sie sein muss …“ |
| Humorvoll | Ansprechende Kampagnen, heitere Inhalte | „Warnung: Kann zu erheblichen Produktivitätssteigerungen führen!“ |
| Spannend | Produkteinführungen, Veranstaltungswerbung | „Das ist der Moment, auf den Sie gewartet haben!“ |
| Inspirierend | Motivationskampagnen, Markenzweck | „Gemeinsam können wir die Welt verändern …“ |
| Überzeugend | Verkaufskampagnen, Konversionen | „Verpassen Sie nicht diese befristete Gelegenheit, um …“ |
| Freundlich | Kundeninteraktion, Begrüßungsnachrichten | „Wir freuen uns, Sie bei uns begrüßen zu dürfen!“ |
| Förmlich | Rechtliche Kommunikation, amtliche Mitteilungen | „Hiermit informieren wir Sie über folgende Änderungen …“ |
| Entschuldigend | Service-Wiederherstellung, Problembehebung | „Wir entschuldigen uns aufrichtig für eventuelle Unannehmlichkeiten …“ |
| Bestimmt | Inhalt für Führungskräfte, verbindliches Messaging | „Das müssen Sie jetzt tun …“ |
| Storytelling | Markenerzählungen, emotionale Verknüpfungen | „Alles fing mit einer einfachen Frage an …“ |
| Dialogorientiert | Nurturing-Kampagnen, Aufbau von Beziehungen | „Sprechen wir darüber, wie Sie hiervon profitieren können …“ |

### Optimieren von Marken-Assets {#brand-assets}

>[!TIP]
>
>Wenn Sie bereits ein Marken-Asset über das Menü **Marken-Assets** hochgeladen haben, müssen Sie im Prompt nicht darauf verweisen. Das System verwendet automatisch alle ausgewählten Dokumente.

Marken-Assets bieten sachliche Informationen, die Ihre generierten Inhalte mit spezifischen, genauen Details anreichern.
Wenn Sie umfangreiche Dokumente wie Produktbroschüren hochladen, geben Sie in Ihrem Prompt an, welche Abschnitte im Vordergrund stehen:

* **Anstelle von** _„Verwende die Produktbroschüre“_ **sollten Sie** _„Lege den Fokus auf die erweiterten Sicherheitsfunktionen und Compliance-Zertifizierungen, insbesondere auf die SOC 2-Konformität und die Datenverschlüsselung“_ verwenden

* **Anstelle von** _„Verweise auf die Fallstudien“_ **sollten Sie** _„Hebe die ROI-Ergebnisse von Kundinnen und Kunden im Gesundheitswesen hervor, insbesondere die Kostenreduzierung um 40 % im regionalen Medizinzentrum“_ verwenden

* **Anstelle von** _„Beziehe technische Details ein“_ **sollten Sie** _„Betone die API-Integrationsfunktionen und die Entwicklervorteile und lege den Fokus auf REST-API-Endpunkte und den SLA-Wert von 99,9 %&quot;_ verwenden

### Inhaltsverfeinerung

>[!TIP]
>
>Verwenden Sie die Funktion „Verfeinern“ anstelle von Prompts, wenn Sie vorhandene Inhalte ausarbeiten, zusammenfassen, vereinfachen, den Ton ändern oder übersetzen möchten. [Weitere Informationen](generative-uc.md#refine)

Sobald der Inhalt generiert wurde, verwenden Sie die Funktion **Verfeinern**, um ihn zu iterieren und mit den folgenden Optionen zu erweitern:

| **Aktion** | **Anwendungsfall** | **Beispiel-Prompt** |
|-|-|-|
| **Ausarbeiten** | Hinzufügen von Tiefe und Details zu kurzen Inhalten | „Erläutere die technischen Vorteile unserer Sicherheitsfunktionen“ |
| **Zusammenfassen** | Zusammenfassen langer Inhalte für verschiedene Formate | „Fasse diese Produktübersicht für einen Social-Media-Beitrag zusammen“ |
| **Vereinfachen** | Verbessern der Zugänglichkeit komplexer Inhalte | „Vereinfache diese technische Erklärung für eine allgemeine Zielgruppe“ |
| **Ton ändern** | Anpassen von Inhalten für verschiedene Zielgruppen | „Lockere den Ton für jüngere Bevölkerungsgruppen auf“ |
| **Transkreation** | Kulturelle Anpassung über reine Übersetzung hinaus | „Erstelle eine Transkreation dieser Kampagne für den japanischen Markt“ |

## Beispiele für szenariobasierte Prompts

### Basierend auf Inhaltstyp {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Kanal</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-Mail</strong></td>
<td>„Fördere potenzielle Unternehmenskundschaft durch Präsentation von drei Kundenerfolgsgeschichten mit detaillierten ROI-Metriken (IBM: 45 % Kostensenkung, Accenture: 200 % Lead-Steigerung, Microsoft: 60 % Zeitersparnis) und sprich IT-Führungspersonal in Unternehmen mit mehr als 1.000 Beschäftigten an.“</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>„Benachrichtige VIP-Kundschaft über einen 4-stündigen Blitzverkauf von Premium-Elektronik mit 40 % Rabatt, der auf die ersten 100 Kundinnen und Kunden beschränkt ist“</td>
</tr>
<tr>
<td><strong>Push-Benachrichtigungen</strong></td>
<td>„Sprich Benutzerinnen und Benutzer, die die App seit 7 Tagen nicht geöffnet haben, mit personalisierten Inhaltsempfehlungen basierend auf ihrem Leseverlauf erneut an“</td>
</tr>
<tr>
<td><strong>Landingpages</strong></td>
<td>„Konvertiere B2B-Besuchende in qualifizierte Leads, indem du demonstrierst, wie unsere Unternehmenssicherheitslösung 99,9 % der Cyber-Angriffe verhindert, schließe Fortune 500-Erfahrungsberichte ein und erwähne den kostenlosen Sicherheits-Audit.“</td>
</tr>
</tbody>
</table>

### Basierend auf branchenspezifischen Ansätzen {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Branche</th>
<th>Beispiel-Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B-Technologie</strong></td>
<td>„Demonstriere den ROI und die technischen Spezifikationen und greife Sicherheitsbedenken von IT-Entscheidungstragenden auf, indem du unsere Cloud-Infrastrukturlösung bewertest, und betone dabei den SLA-Wert von 99,9 %, die SOC 2-Konformität und Kosteneinsparungen von 40 %.“</td>
</tr>
<tr>
<td><strong>E-Commerce – Einzelhandel</strong></td>
<td>„Vermittle Dringlichkeit für Weihnachtsartikel mit begrenzten Stückzahlen und hebe gleichzeitig den kostenlosen Versand und einfache Retouren für Last-Minute-Kaufende hervor, betone dabei die begrenzte Verfügbarkeit (weniger als 50 Artikel verbleibend) und den Stichtag für den 24-Stunden-Versand.“</td>
</tr>
<tr>
<td><strong>Finanzdienstleistungen</strong></td>
<td>„Informiere die Kundschaft über Strategien zur Diversifizierung des Anlageportfolios unter Einhaltung behördlicher Auflagen, mit Erkenntnissen zertifizierter Finanzberatungsfachleute und Haftungsausschlüssen zu Risiken.“</td>
</tr>
<tr>
<td><strong>Gesundheitswesen und Wellness</strong></td>
<td>„Bewirb die Vorteile von Vorsorgeuntersuchungen und jährlichen Gesundheits-Screenings, verwende medizinisch korrekte Begriffe, schließe Empfehlungen zertifizierter Ärztinnen und Ärzte ein und erwähne Datenschutzgarantien für Patientinnen und Patienten.“</td>
</tr>
<tr>
<td><strong>Allgemeine und berufliche Bildung</strong></td>
<td>„Hebe Karrierefortschritte und Branchenzertifizierungen hervor, präsentiere dabei das Know-how der Dozentinnen und Dozenten und betone die Vermittlungsquote von 92 % und den projektbasierten Lehrplan.“</td>
</tr>
<tr>
<td><strong>SaaS-Plattformen</strong></td>
<td>„Zeige die Vorteile durch Zeitersparnisse und Automatisierung mit spezifischen Metriken auf und gehe auf Bedenken hinsichtlich der Integration ein, nenne die Vorteile der wöchentlichen Zeitersparnis von durchschnittlich 25 Stunden und der Integration mit über 200 beliebten Tools.“</td>
</tr>
</tbody>
</table>
