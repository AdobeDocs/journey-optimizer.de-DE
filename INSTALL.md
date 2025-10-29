---
source-git-commit: d7bb3424bc6dfb837b47d15c448a2d46bf4b6c3c
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 4%

---
# Installieren von Cursor-Agenten 🚀

Cursor-Agenten sind freigegebene Tools, mit denen Sie die Dokumentation effizienter erstellen und verwalten können.

## Erstmaliges Setup

Dies muss nur (**)** Repository erfolgen.

### Option 1: Verwenden des Cursors (empfohlene ⭐)

1. Cursor-Chat öffnen (`Cmd+L` oder `Ctrl+L`)
2. Typ:

   ```
   @setup-agents
   ```

3. Befolgen der Eingabeaufforderungen
4. Fertig! ✨

### Option 2: Verwenden des Terminals

1. Öffnen Sie Ihr Terminal im Repository-Stammverzeichnis
2. Durchgang:

   ```bash
   ./setup-agents.sh
   ```

   Oder manuell:

   ```bash
   git submodule update --init --recursive
   ```

3. Fertig! ✨

## Verifizierung

Überprüfen Sie nach dem Setup die Installation:

```bash
ls .cursor-agents/agents/
```

Sie sollten Folgendes sehen:
- `draft-page-generator.md`
- `fix-grammar.md`
- usw.

## Nutzung

Nach der Installation können Sie Agenten im Cursor verwenden:

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Siehe `.cursor-agents/AGENTS.md` für eine vollständige Liste der verfügbaren Agenten.

## Aktualisieren von Agenten

So rufen Sie die neueste Version aller Agenten ab:

### Option 1: Cursor verwenden

```
@update-agents
```

### Option 2: Verwenden des Terminals

```bash
git submodule update --remote
```

## Fehlerbehebung

### Fehler „Agent nicht gefunden“

Wenn dieser Fehler angezeigt wird, sind die Agenten noch nicht installiert. Durchgang:

```
@setup-agents
```

### Untermodul ist leer

Wenn `.cursor-agents/` vorhanden, aber leer ist:

```bash
git submodule update --init --recursive --remote
```

### Berechtigung verweigert

Stellen Sie sicher, dass das Setup-Skript ausführbar ist:

```bash
chmod +x setup-agents.sh
```

### Netzwerk-/VPN-Probleme

- Stellen Sie sicher, dass Sie mit Adobe VPN verbunden sind
- Überprüfen der Netzwerkverbindung
- Git-Zugriff überprüfen:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Funktionsweise

Cursor-Agenten werden als **Git-Untermodul“**:

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

Das Untermodul verweist auf:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Dadurch wird sichergestellt, dass alle dieselben, aktuellen Agenten verwenden.

&#x200B;---

**Benötigen Sie Hilfe?** Kontaktieren Sie Ihren Dokumentations-Teamleiter oder sehen Sie sich das interne Wiki an.

