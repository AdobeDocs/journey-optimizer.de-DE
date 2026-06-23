---
name: ajo-ai-accordion
description: Die Adobe Journey Optimizer-Dokumentationsseiten werden um einen Akkordeon-Abschnitt des KI-Assistenten erweitert, der am Ende jeder Markdown-Datei angehängt wird. liest jede Seite, generiert automatisch relevante KI-Assistenten-Inhalte basierend auf dem Seitenthema und fügt sie als ausblendbares Akkordeon ein. Verwenden Sie diese Option, wenn Benutzende KI-Informationen zu AJO-Dokumenten hinzufügen, AJO-Markdown-Seiten mit KI-Inhalten anreichern oder eine Datei oder einen Ordner mit Markdown-Dateien mit KI-Akkordeon-Abschnitten verarbeiten möchten.
disable-model-invocation: true
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# AJO AI-Akkordeon-Anreicherung

Hängt ein automatisch generiertes Akkordeon des KI-Assistenten an das Ende einer oder mehrerer Markdown-Dateien im Dokumentations-Repository von Journey Optimizer an.

## Ziel-Repository

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## Akkordeonsyntax (Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regeln:**
- `+++Title` in einer Zeile - Der Titel folgt sofort `+++`, kein Leerzeichen dazwischen
- `+++` allein auf einer Linie schließt das Akkordeon
- Leerzeile vor dem `+++` und nach dem `+++`

---

## Workflow

### Schritt 1 — Zielgruppe(n) anfordern

Fragen Sie den Benutzer:

> Welche Datei oder welchen Ordner möchten Sie anreichern?
> - Einzelne Datei: Pfad relativ zum Repository-Stamm (z. B. `help/using/email/get-started-email.md`)
> - Ordner : verarbeitet alle `.md` Dateien in rekursiv (z. B. `help/using/email`)
> - Liste der Dateien/Ordner

Verwenden Sie `AskQuestion`, falls verfügbar, andernfalls fragen Sie im Gespräch.

Wenn ein Ordner angegeben ist, listen Sie alle gefundenen `.md` auf und bestätigen Sie die Suche vor der Verarbeitung mit dem Benutzer.

### Schritt 2 - Für jede Datei: lesen und generieren

Für jede Zieldatei gilt:

1. **Lies die** vollständig.
2. **Grundlegendes zum Thema Seite** - welche Funktion, welches Konzept oder welche Aufgabe wird darin abgedeckt?
3. **Generieren des Akkordeoninhalts** mithilfe der folgenden Regeln für die Inhaltserstellung.
4. **Überprüfen** ob am Ende der Datei bereits ein KI-Akkordeon vorhanden ist (suchen Sie am Ende nach `+++`). Ist dies der Fall, fragen Sie den Benutzer, ob er ersetzen oder überspringen soll.

### Schritt 3 — Akkordeon anhängen

Am Ende der Datei anhängen:

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

Es sollten keine anderen Inhalte in der Datei geändert werden.

### Schritt 4 — Bericht

Nachdem alle Dateien verarbeitet wurden:
- Auflisten der ✓ geänderten Dateien
- Übersprungene Dateien auflisten und Ursache angeben (hat bereits Akkordeon, leere Datei, ist nicht relevant usw.)

---

## Regeln zur Inhaltserstellung

Erzeugen Sie den Akkordeon-Inhalt durch Analysieren der Markdown-Seite. Erstellen Sie die folgenden Abschnitte **in der richtigen Reihenfolge** formatiert als Markdown-Aufzählungslisten. Überspringen Sie jeden Abschnitt, für den keine aussagekräftigen Inhalte aus der Seite extrahiert werden können.

---

### Akkordeontitel

Verwenden Sie: `+++AI Assistant — Page context`

---

### Zu erzeugende Abschnitte (in der richtigen Reihenfolge)

**1. TL;DR**

Ein Satz. Was wird auf dieser Seite gelehrt bzw. aktiviert?

```markdown
- **TL;DR:** [one sentence summary]
```

---

**2. Absicht**

Vollständige Liste der Möglichkeiten, die ein Benutzer nach dem Lesen dieser Seite hat (3-6 Elemente).

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

---

**3. Glossar**

Schlüsselbegriffe, die für diese Seite/Funktion spezifisch sind, mit einer kurzen Definition. Markieren Sie produktspezifische Begriffe.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

Nur Begriffe einschließen, die für das Thema dieser Seite relevant sind. Verwenden Sie keine allgemeinen Marketing-Begriffe.

---

**4. Schutzmechanismen**

Einschränkungen, Voraussetzungen, Berechtigungen oder Einschränkungen, die auf der Seite erwähnt werden.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

---

**5. Terminologie**

Kanonische Produktnamen, Akronyme, akzeptierte Varianten, Synonyme und eindeutige Hinweise. Dieser Abschnitt dient in erster Linie der KI-Pipeline-Normalisierung.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

Nur Einträge einschließen, die auf der Seite vorhanden oder impliziert sind.

---

**6. Häufig gestellte Fragen**

3-6 Fragen, die ein Benutzer möglicherweise zum Inhalt dieser Seite stellt, mit kurzen Antworten.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

---

### Was NICHT enthalten sein soll

- Schreiben **den** der Seite (die bereits vorhanden ist) nicht um oder fassen Sie ihn zusammen.
- **keine** Schritt-für-Schritt-Anweisungen enthalten (diese befinden sich auf der Seite).
- Erfinden **** Inhalte, die von der Seite nicht unterstützt werden.

---

### Vollständige Akkordeon-Vorlage

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
- [guardrail]

**Terminology:**
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## Anmerkungen

- Verarbeiten Sie Dateien einzeln, nicht in großen Mengen, um eine hohe Generierungsqualität zu gewährleisten.
- Wenn die Seite sehr kurz oder nur eine Umleitungs-/Indexseite ist, markieren Sie sie und fragen Sie den Benutzer, ob er sie überspringen möchte.
- Erstellen Sie keine neuen Dateien, sondern bearbeiten Sie nur vorhandene `.md`.
