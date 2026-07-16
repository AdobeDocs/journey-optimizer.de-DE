---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# augmentedAIContent

Fügt einen automatisch generierten **Schnellverweis** am Ende einer oder mehrerer Markdown-Dateien im Dokumentations-Repository von Journey Optimizer an.

## Ziel-Repository

`help/using/` (relativ zum Repository-Stamm)

## Abschnitt- und Registerkartensyntax (Experience League)

### Abschnittsüberschrift

```
## Quick reference {#quick-reference}
```

### Registerkarten

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**Regeln:**

- `>[!BEGINTABS]` und `>[!ENDTABS]` jeweils auf einer eigenen Linie, umgeben von Leerzeilen
- `>[!TAB Name]` in einer eigenen Zeile, gefolgt von einer leeren Zeile vor dem Inhalt
- Registerkartennamen sind in Großbuchstaben geschrieben, kurz (1-3 Wörter)
- Leerzeile vor `>[!BEGINTABS]` und nach `>[!ENDTABS]`

&#x200B;---

## Workflow

### Schritt 1 — Zielgruppe(n) anfordern

Fragen Sie den Benutzer:
> Welche Datei oder welchen Ordner möchten Sie anreichern?
> - Einzelne Datei: Pfad relativ zum Repository-Stamm (z. B. `help/using/email/get-started-email.md`)
> - Ordner: alle `.md` rekursiv (z. B. `help/using/email`)
> - Liste der Dateien/Ordner

Wenn ein Ordner angegeben ist, listen Sie die gefundenen `.md` auf und bestätigen Sie sie vor der Verarbeitung.

### Schritt 2 - Für jede Datei: lesen und generieren

1. **Lies die** vollständig.
2. **Grundlegendes zum Thema Seite** - welche Funktion, welches Konzept oder welche Aufgabe wird darin abgedeckt?
3. **Generieren Sie den Abschnittsinhalt** mithilfe der folgenden Regeln zur Inhaltserstellung.
4. **Führen Sie die Validierungsprüfliste für die Nachgenerierung aus** (siehe unten) - überspringen Sie nicht.
5. **Überprüfen** ob am Ende bereits ein Schnellverweisabschnitt vorhanden ist (suchen Sie am Ende nach `## Quick reference`). Wenn ja, den Benutzer fragen: Ersetzen oder überspringen?

### Schritt 3: Überprüfen jedes Anspruchs gegenüber dem Seitentext

Lesen Sie vor dem Anhängen den generierten Abschnitt erneut nach Anspruch. Dieser Schritt ist **obligatorisch und kann nicht übersprungen werden** auch nicht bei kurzen Dateien. Korrigieren Sie alle Fehler, bevor Sie mit Schritt 4 fortfahren.

**Terminologie und Kennzeichnungen**

- [ ] Jeder Begriff, jede Beschriftung und jeder Name der Benutzeroberfläche im Abschnitt wird im Hauptteil der Seite angezeigt - nicht von einer anderen Seite importiert oder aus dem allgemeinen Produktwissen abgeleitet
- [ ] Es wird kein Synonym aufgeführt, sofern nicht beide Formulare auf der Seite angezeigt werden
- [ ] Jeder Eintrag mit „Verwechseln Sie nicht“ verweist nur auf Konzepte, die auf dieser Seite erwähnt werden

**Leitplanken und Beschränkungen**

- [ ] Jeder numerische Wert entspricht genau dem Seitentext
- [ ] Ein Limit wird nur dann als **Hard** bezeichnet, wenn der Seitentext dieses Wort verwendet oder das System dies eindeutig durchsetzt (z. B. „Cannot exceeded“, „maximum … allowed“, „only … supported„)
- [ ] Ein Limit wird nur dann **empfohlen** wenn der Seitentext dieses Wort oder ein Äquivalent verwendet („Für optimale Leistung“, „wird empfohlen„).
- [ ] Wenn der Seitentext keinen Qualifizierer enthält, gibt der Abschnitt keinen - erfinden Sie keinen
- [ ] Keine Metakommentare dazu, was auf der Quellseite steht oder nicht (z. B. „auf dieser Seite wird keine bestimmte Zahl angegeben„)

**Glossardefinitionen**

- [ ] Keine Definition enthält technische Details, die nicht im Seitentext enthalten sind
- [ ] Kein Eintrag verwendet Informationen aus anderen Seiten im Dokumentationssatz

**FAQ-Antworten**

- [ ] Jedes bestimmte Detail (Benutzeroberflächen-Eigenschaften, Schaltflächennamen, Feldnamen, Schrittsequenzen) wird im Seitentext angegeben - nicht von anderen Seiten abgeleitet oder importiert
- [ ] Keine Antwort führt zu Informationen, die der Seitentext nicht adressiert.

**Korrekturregel:** Wenn eine Überprüfung fehlschlägt, korrigieren Sie den Inhalt **vor** Anfügen. Protokollieren Sie jede Korrektur im Bericht Schritt 5.

&#x200B;---

### Schritt 4 — Abschnitt anhängen

Verwenden Sie den festen Eröffnungsblock und die vollständige Vorlage, die in den **Inhaltsgenerierungsregeln“ unten definiert**. Hängen Sie ganz am Ende der Datei an, gefolgt sofort von dem Synchronisierungskommentar:

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

Mit diesem Kommentar können zukünftige Tools und Writer erkennen, wann der Seitentext aus dem Abschnitt gewechselt ist. Ändern Sie keine anderen Inhalte.

### Schritt 5 — Bericht

- Dateien ✓ geändert
- Übersprungene Dateien + Grund (hat bereits einen Abschnitt / leere Seite / Index)
- Alle während Schritt 2 ausgelösten Validierungswarnungen

&#x200B;---

## Regeln zur Inhaltserstellung

Analysieren Sie die Seite und erstellen Sie die folgenden Registerkarten **in der richtigen Reihenfolge**. Wenn dafür kein aussagekräftiger Inhalt extrahiert werden kann, kann eine Registerkarte vollständig übersprungen werden.

### Abschnittsüberschrift und feste Öffnung — wörtlich, nicht ändern

Jeder Schnellverweisabschnitt muss mit diesem exakten Block beginnen. Kopieren Sie sie wie vorliegend, paraphrasieren, verkürzen oder ordnen Sie sie nicht um:

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Der `>[!BEGINTABS]` folgt unmittelbar nach diesen beiden Absätzen.

### Registerkarte 1 — Übersicht

Ein Satz TL;DR Zusammenfassung dessen, was die Seite lehrt oder aktiviert, gefolgt von 3-6 Dingen, die ein Benutzer nach dem Lesen dieser Seite erreichen kann.

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### Registerkarte 2 — Glossar

Schlüsselbegriffe, die für diese Seite/Funktion spezifisch sind, mit kurzen Definitionen. Markieren Sie produktspezifische Begriffe.

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

Nur Begriffe einschließen, die für diese Seite relevant sind. Verwenden Sie keine allgemeinen Marketing-Begriffe.

**Präzisionsregel für den Validierungsmodus - obligatorisch:**
Wenn die Seite alle Arten von Tests, einer Vorschau oder simulierten Ausführungen abdeckt, MÜSSEN Sie zwischen allen Modi unterscheiden, die die Seite tatsächlich beschreibt. Reduzieren Sie keine verschiedenen Modi in einen einzelnen kurzen Eintrag:
- **Simulation** - rendert den Nachrichteninhalt ohne zu senden, wobei echte Profile verwendet werden
- **Testmodus** - sendet nur an bestimmte Testprofile; verwendet persistente AEP-Testprofile (keine synthetischen oder gefälschten Profile)
- **Probelauf** - Führt die vollständige Journey-Logik aus, ohne Aktionen zu aktivieren; verwendet echte Zielgruppendaten

Nur die auf der Seite vorhandenen Modi einbeziehen. Kopieren Sie den produktgenauen Begriff aus dem Seitentext - ersetzen Sie keine „synthetischen Profile“, „falsche Daten“ oder „ohne echte Daten“.

### Registerkarte 3 — Terminologie

Kanonische Namen, Akronyme, akzeptierte Varianten, Synonyme, Uneindeutigkeit. Hauptsächlich für die KI-Pipeline-Normalisierung.

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**Präzisionsregel für Status und Lebenszyklus:**
Wenn die Seite einen Lebenszyklus beschreibt (Journey-Status, Nachrichtenstatus, Kampagnenstatus usw.), kopieren Sie die genauen Statuskennzeichnungen aus dem Seitentext. Nicht umschreiben. Verwenden Sie „Verwechseln Sie nicht“-Einträge, um Status zu unterscheiden, die ein Wurzelwort gemeinsam haben, aber eine unterschiedliche Bedeutung haben. Beispiel:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### Registerkarte 4 - Leitplanken und Einschränkungen

Einschränkungen, Voraussetzungen, Berechtigungen oder Einschränkungen, die auf der Seite erwähnt werden.

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**Präzisionsregeln für Leitplanken — obligatorisch:**

- **Qualifizieren Sie jedes numerische Limit** entweder als empfohlen oder als fest. Beispiel: „Maximal 10 Datensatzsuchen pro Nachricht (feste Grenze)“ statt „Maximal 10 Datensatzsuchen“.
- **Qualifizieren Sie jeden Durchsatz oder jede** mit seinem Umfang. Beispiel: „Begrenzung auf 150.000 Nachrichten/Stunde (pro Sandbox)“ statt „Begrenzung auf 150.000 Nachrichten/Stunde“.
- **Überprüfen Sie alle Leitplanken mit dem Seitentext,** Sie ihn einbeziehen. Wenn auf der Seite „10“ steht und im Abschnitt „5“, ist der Abschnitt falsch. Der Seitentext ist verbindlich.
- **Keine Leitplanken ableiten** die nicht auf der Seite angegeben sind. Wenn eine Begrenzung vorhanden ist, die Seite sie jedoch nicht angibt, lassen Sie sie weg.

### Registerkarte 5 - Häufig gestellte Fragen

3-6 Fragen, die ein Benutzer stellen könnte, mit kurzen Antworten. Jeden als fette Fragenüberschrift formatieren, gefolgt von einer Absatzantwort.

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
```

**FAQ-Präzisionsregel:**
Antworten müssen dieselben Verb- und Substantivoptionen wie der Seitentext verwenden. Verben wie „Zurücksetzen“, „Zurücksetzen“ oder „Zurücksetzen“ sollten nicht eingeführt werden, es sei denn, die Seite verwendet sie. Wenn ein Übergang eine Sitzung beendet (z. B. wenn beim Beenden des Testmodus die Journey in den vorherigen Zustand zurückversetzt wird), sagen Sie genau das — sagen Sie nicht „die Journey kehrt zum Entwurf zurück“.

### Was NICHT enthalten sein soll

- **nicht** den Hauptteilinhalt neu schreiben oder zusammenfassen (er befindet sich bereits auf der Seite)
- **keine** schrittweisen Anweisungen enthalten
- Erfinden **&#x200B;**&#x200B;Inhalte, die von der Seite nicht unterstützt werden
- Verwenden **nicht** folgenden ungenauen Begriffe, es sei denn, sie erscheinen wörtlich im Seitentext: „synthetisch“, „falsche Daten“, „ohne echte Daten“, „Zurücksetzen“, „Zurücksetzen“ (bei der Beschreibung von Produktzustandsübergängen)

&#x200B;---

## Checkliste für die Validierung nach der Generierung

Führen Sie diese Checkliste für jeden Abschnitt aus, bevor Sie anhängen. Markieren Sie den Benutzer auf einen Fehler, bevor Sie fortfahren.

### Leitplankenprüfung

- [ ] Jeder numerische Wert im Abschnitt ist wörtlich oder vom Seitentext abgeleitet
- [ ] Jedes Limit ist als empfohlen oder hart eingestuft
- [ ] Jede Durchsatzzahl beinhaltet ihren Umfang (Sandbox / Organisation / Instanz)

### Terminologieprüfung
- [ ] Alle auf der Seite vorhandenen Validierungsmodi (Simulation, Testmodus, Probelauf) werden eingeschlossen und mit seitengenauen Begriffen benannt
- [ ] Alle Lebenszyklusstatus verwenden exakte Beschriftungen aus dem Seitentext
- [ ] Keine unpräzisen Verben in FAQ-Antworten („revert“, „synthetisch“, „falsche Daten“, „ohne echte Daten„), es sei denn, sie werden wörtlich auf der Seite präsentiert

### Umfangsüberprüfung
- [ ] Glossar enthält keine allgemeinen Marketing-Begriffe, die nichts mit der Seite zu tun haben
- [ ] FAQ-Antworten führen nicht zu Informationen, die auf der Seite fehlen

Wenn eine Überprüfung fehlschlägt, korrigieren Sie den Abschnitt, bevor Sie anhängen. Protokollieren Sie die Korrektur im Bericht zu Schritt 4.

&#x200B;---

## Verantwortung synchronisieren

Der Schnellverweisabschnitt ist eine Ableitung des Seitentextes zu einem bestimmten Zeitpunkt. Sie muss als Teil der Seite behandelt werden.

**Wenn der Seitentext aktualisiert wird (Release-PRs, Korrekturen usw.):**

- Wenn durch die Aktualisierung Leitplanken, Beschränkungen, Statuskennzeichnungen oder Validierungsmodi geändert werden, die im Abschnitt beschrieben werden, → Sie den Abschnitt in derselben PR neu generieren oder manuell aktualisieren.
- Wenn die Aktualisierung nicht mit dem Abschnittsinhalt zusammenhängt (z. B. Verfahrensschritte, Screenshot-Aktualisierungen), → der Abschnitt möglicherweise unverändert bleibt, ihn jedoch kurz überprüfen.

Der Synchronisationskommentar, der nach dem Abschnitt (`<!-- ai-section-version -->`) angehängt wird, ist das Signal: Wenn sich der Dateiinhalt vor dem Abschnitt geändert hat, seit dieser Hash geschrieben wurde, ist der Abschnitt ein Kandidat für eine Überprüfung.

&#x200B;---

## Vollständige Vorlage

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## Anmerkungen

- Verarbeiten Sie Dateien einzeln für eine bessere Qualität.
- Markieren Sie sehr kurze oder nur indizierte Seiten und fragen Sie den Benutzer, ob er überspringen soll.
- Erstellen Sie keine neuen Dateien, sondern bearbeiten Sie nur vorhandene `.md`.
- Die Checkliste für die Validierung nach der Generierung ist nicht optional. Führen Sie sie für jede Datei aus, einschließlich Massenvorgängen.
