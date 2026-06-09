---
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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
3. **Generieren Sie den Akkordeoninhalt** den folgenden Regeln.
4. **Überprüfen** ob am Ende bereits ein KI-Akkordeon vorhanden ist (suchen Sie am Ende nach `+++AI Assistant`). Wenn ja, den Benutzer fragen: Ersetzen oder überspringen?

### Schritt 3 — Akkordeon anhängen

Hängen Sie ganz am Ende der Datei an. Ändern Sie keine anderen Inhalte.

### Schritt 4 — Bericht

- Dateien ✓ geändert
- Dateien übersprungen + Grund (hat bereits Akkordeon / leer / Indexseite)

&#x200B;---

## Regeln zur Inhaltserstellung

Analysieren Sie die Seite und erstellen Sie die folgenden Abschnitte **in der richtigen Reihenfolge** als Markdown-Aufzählungslisten. Überspringen Sie Abschnitte, in denen keine aussagekräftigen Inhalte extrahiert werden können.

### Akkordeontitel

`+++AI Assistant — Page context`

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

### &#x200B;4. Leitlinien

Einschränkungen, Voraussetzungen, Berechtigungen oder Einschränkungen, die auf der Seite erwähnt werden.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. Terminologie

Kanonische Namen, Akronyme, akzeptierte Varianten, Synonyme, Uneindeutigkeit. Hauptsächlich für die KI-Pipeline-Normalisierung.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. Häufig gestellte Fragen

3-6 Fragen, die ein Benutzer stellen könnte, mit kurzen Antworten.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### Was NICHT enthalten sein soll

- **nicht** den Hauptteilinhalt neu schreiben oder zusammenfassen (er befindet sich bereits auf der Seite)
- **keine** schrittweisen Anweisungen enthalten
- Erfinden **&#x200B;**&#x200B;Inhalte, die von der Seite nicht unterstützt werden

### Vollständige Vorlage

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## Anmerkungen

- Verarbeiten Sie Dateien einzeln für eine bessere Qualität.
- Markieren Sie sehr kurze oder nur indizierte Seiten und fragen Sie den Benutzer, ob er überspringen soll.
- Erstellen Sie keine neuen Dateien, sondern bearbeiten Sie nur vorhandene `.md`.
