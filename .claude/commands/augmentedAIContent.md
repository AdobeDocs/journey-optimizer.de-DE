---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# augmentedAIContent

Hängt ein automatisch generiertes Akkordeon des KI-Assistenten an das Ende einer oder mehrerer Markdown-Dateien im Dokumentations-Repository von Journey Optimizer an.

## Ziel-Repository

`help/using/` (relativ zum Repository-Stamm)

## Akkordeonsyntax (Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regeln:**
- `+++Title` in einer Zeile - Titel folgt sofort `+++`
- `+++` allein auf einer Linie schließt das Akkordeon
- Leerzeile vor dem `+++` und nach dem `+++`

---

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
3. **Generieren des Akkordeoninhalts** mithilfe der folgenden Regeln für die Inhaltserstellung.
4. **Führen Sie die Validierungsprüfliste für die Nachgenerierung aus** (siehe unten) - überspringen Sie nicht.
5. **Überprüfen** ob am Ende bereits ein KI-Akkordeon vorhanden ist (suchen Sie am Ende nach `+++AI Knowledge Reference`). Wenn ja, den Benutzer fragen: Ersetzen oder überspringen?

### Schritt 3 — Akkordeon anhängen

Verwenden Sie den festen Eröffnungsblock und die vollständige Vorlage, die in den **Inhaltsgenerierungsregeln“ unten definiert**. Hängen Sie ganz am Ende der Datei an, gefolgt sofort von dem Synchronisierungskommentar:

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

Dieser Kommentar ermöglicht es zukünftigen Tools und Autoren zu erkennen, wann der Seitentext vom Akkordeon abgewichen ist. Ändern Sie keine anderen Inhalte.

### Schritt 4 — Bericht

- Dateien ✓ geändert
- Dateien übersprungen + Grund (hat bereits Akkordeon / leer / Indexseite)
- Alle während Schritt 2 ausgelösten Validierungswarnungen

---

## Regeln zur Inhaltserstellung

Analysieren Sie die Seite und erstellen Sie die folgenden Abschnitte **in der richtigen Reihenfolge** als Markdown-Aufzählungslisten. Überspringen Sie Abschnitte, in denen keine aussagekräftigen Inhalte extrahiert werden können.

### Akkordeontitel und feste Öffnung — wörtlich, nicht modifizieren

Jedes Akkordeon muss mit genau diesem Block beginnen. Kopieren Sie sie wie vorliegend, paraphrasieren, verkürzen oder ordnen Sie sie nicht um:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Die generierten Inhaltsabschnitte folgen unmittelbar nach diesen beiden Absätzen.

### 1. TL;DR

Eine Satzzusammenfassung dessen, was die Seite lehrt oder aktiviert.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. INTENTS

3-6 Dinge, die ein Benutzer nach dem Lesen dieser Seite erreichen kann.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. Glossar

Schlüsselbegriffe, die für diese Seite/Funktion spezifisch sind, mit kurzen Definitionen. Markieren Sie produktspezifische Begriffe.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
```

Nur Begriffe einschließen, die für diese Seite relevant sind. Verwenden Sie keine allgemeinen Marketing-Begriffe.

**Präzisionsregel für den Validierungsmodus - obligatorisch:**
Wenn die Seite alle Arten von Tests, einer Vorschau oder simulierten Ausführungen abdeckt, MÜSSEN Sie zwischen allen Modi unterscheiden, die die Seite tatsächlich beschreibt. Reduzieren Sie keine verschiedenen Modi in einen einzelnen kurzen Eintrag:
- **Simulation** - rendert den Nachrichteninhalt ohne zu senden, wobei echte Profile verwendet werden
- **Testmodus** - sendet nur an bestimmte Testprofile; verwendet persistente AEP-Testprofile (keine synthetischen oder gefälschten Profile)
- **Probelauf** - Führt die vollständige Journey-Logik aus, ohne Aktionen zu aktivieren; verwendet echte Zielgruppendaten

Nur die auf der Seite vorhandenen Modi einbeziehen. Kopieren Sie den produktgenauen Begriff aus dem Seitentext - ersetzen Sie keine „synthetischen Profile“, „falsche Daten“ oder „ohne echte Daten“.

### &#x200B;4. Leitlinien

Einschränkungen, Voraussetzungen, Berechtigungen oder Einschränkungen, die auf der Seite erwähnt werden.

```
**Guardrails:**
- [guardrail]
```

**Präzisionsregeln für Leitplanken — obligatorisch:**

- **Qualifizieren Sie jedes numerische Limit** entweder als empfohlen oder als fest. Beispiel: „Maximal 10 Datensatzsuchen pro Nachricht (feste Grenze)“ statt „Maximal 10 Datensatzsuchen“.
- **Qualifizieren Sie jeden Durchsatz oder jede** mit seinem Umfang. Beispiel: „Begrenzung auf 150.000 Nachrichten/Stunde (pro Sandbox)“ statt „Begrenzung auf 150.000 Nachrichten/Stunde“.
- **Überprüfen Sie alle Leitplanken mit dem Seitentext,** Sie ihn einbeziehen. Wenn auf der Seite 10 steht und das Akkordeon 5, ist das Akkordeon falsch. Der Seitentext ist verbindlich.
- **Keine Leitplanken ableiten** die nicht auf der Seite angegeben sind. Wenn eine Begrenzung vorhanden ist, die Seite sie jedoch nicht angibt, lassen Sie sie weg.

### &#x200B;5. Terminologie

Kanonische Namen, Akronyme, akzeptierte Varianten, Synonyme, Uneindeutigkeit. Hauptsächlich für die KI-Pipeline-Normalisierung.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**Präzisionsregel für Status und Lebenszyklus:**
Wenn die Seite einen Lebenszyklus beschreibt (Journey-Status, Nachrichtenstatus, Kampagnenstatus usw.), kopieren Sie die genauen Statuskennzeichnungen aus dem Seitentext. Nicht umschreiben. Verwenden Sie „Verwechseln Sie nicht“-Einträge, um Status zu unterscheiden, die ein Wurzelwort gemeinsam haben, aber eine unterschiedliche Bedeutung haben. Beispiel:

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Häufig gestellte Fragen

3-6 Fragen, die ein Benutzer stellen könnte, mit kurzen Antworten.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**FAQ-Präzisionsregel:**
Antworten müssen dieselben Verb- und Substantivoptionen wie der Seitentext verwenden. Verben wie „Zurücksetzen“, „Zurücksetzen“ oder „Zurücksetzen“ sollten nicht eingeführt werden, es sei denn, die Seite verwendet sie. Wenn ein Übergang eine Sitzung beendet (z. B. wenn beim Beenden des Testmodus die Journey in den vorherigen Zustand zurückversetzt wird), sagen Sie genau das — sagen Sie nicht „die Journey kehrt zum Entwurf zurück“.

### Was NICHT enthalten sein soll

- **nicht** den Hauptteilinhalt neu schreiben oder zusammenfassen (er befindet sich bereits auf der Seite)
- **keine** schrittweisen Anweisungen enthalten
- Erfinden **** Inhalte, die von der Seite nicht unterstützt werden
- Verwenden **nicht** folgenden ungenauen Begriffe, es sei denn, sie erscheinen wörtlich im Seitentext: „synthetisch“, „falsche Daten“, „ohne echte Daten“, „Zurücksetzen“, „Zurücksetzen“ (bei der Beschreibung von Produktzustandsübergängen)

---

## Checkliste für die Validierung nach der Generierung

Diese Checkliste vor dem Anhängen für jedes Akkordeon ausführen. Markieren Sie den Benutzer auf einen Fehler, bevor Sie fortfahren.

### Leitplankenprüfung
- [ ] Jeder numerische Wert im Akkordeon ist wörtlich vorhanden oder kann vom Seitentext abgeleitet werden
- [ ] Jedes Limit ist als empfohlen oder hart eingestuft
- [ ] Jede Durchsatzzahl beinhaltet ihren Umfang (Sandbox / Organisation / Instanz)

### Terminologieprüfung
- [ ] Alle auf der Seite vorhandenen Validierungsmodi (Simulation, Testmodus, Probelauf) werden eingeschlossen und mit seitengenauen Begriffen benannt
- [ ] Alle Lebenszyklusstatus verwenden exakte Beschriftungen aus dem Seitentext
- [ ] Keine unpräzisen Verben in FAQ-Antworten („revert“, „synthetisch“, „falsche Daten“, „ohne echte Daten„), es sei denn, sie werden wörtlich auf der Seite präsentiert

### Umfangsüberprüfung
- [ ] Glossar enthält keine allgemeinen Marketing-Begriffe, die nichts mit der Seite zu tun haben
- [ ] FAQ-Antworten führen nicht zu Informationen, die auf der Seite fehlen

Wenn eine Überprüfung fehlschlägt, korrigieren Sie das Akkordeon, bevor Sie anhängen. Protokollieren Sie die Korrektur im Bericht zu Schritt 4.

---

## Verantwortung synchronisieren

Das Akkordeon ist eine Ableitung des Seitentextes zu einem bestimmten Zeitpunkt. Sie muss als Teil der Seite behandelt werden.

**Wenn der Seitentext aktualisiert wird (Release-PRs, Korrekturen usw.):**
- Wenn durch die Aktualisierung eine Leitplanke, ein Limit, eine Statusbeschriftung oder ein Validierungsmodus geändert wird, die bzw. der im Akkordeon beschrieben ist, → das Akkordeon in derselben PR neu generiert oder manuell aktualisiert werden.
- Wenn die Aktualisierung nicht mit dem Akkordeoninhalt in Zusammenhang steht (z. B. Verfahrensschritte, Screenshot-Updates), kann → Akkordeon unverändert bleiben, es aber kurz überprüfen.

Der Synchronisationskommentar, der nach dem Akkordeon angehängt wird (`<!-- ai-accordion-version -->`), ist das Signal: Wenn sich der Dateiinhalt vor dem Akkordeon seit dem Schreiben dieses Hashs geändert hat, ist das Akkordeon ein Kandidat für eine Überprüfung.

---

## Vollständige Vorlage

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

---

## Anmerkungen

- Verarbeiten Sie Dateien einzeln für eine bessere Qualität.
- Markieren Sie sehr kurze oder nur indizierte Seiten und fragen Sie den Benutzer, ob er überspringen soll.
- Erstellen Sie keine neuen Dateien, sondern bearbeiten Sie nur vorhandene `.md`.
- Die Checkliste für die Validierung nach der Generierung ist nicht optional. Führen Sie sie für jede Datei aus, einschließlich Massenvorgängen.
