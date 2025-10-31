---
source-git-commit: 7e2ed972b85255ccd64cd04d306f7de602b41165
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 2%

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

3. Der Agent wird automatisch:
   - Testen des SSH- und HTTPS-Zugriffs
   - Verwenden der Arbeitsmethode
   - Führen Sie bei Bedarf durch das Setup
4. Fertig! ✨

**Hinweis:** Der Agent erkennt automatisch, ob Sie SSH- oder HTTPS-Zugriff auf `git.corp.adobe.com` haben, und verwendet die entsprechende Methode. Wenn keines von beiden funktioniert, bietet es eine geführte Einrichtung.

### Option 2: Verwenden des Terminals

1. Öffnen Sie Ihr Terminal im Repository-Stammverzeichnis
2. Durchgang:

   ```bash
   ./setup-agents.sh
   ```

   Das Skript wird automatisch:
   - Testen des SSH- und HTTPS-Zugriffs
   - Verwenden der Arbeitsmethode
   - Bei Bedarf Einrichtungsanweisungen anzeigen

   Oder manuell (wenn Sie wissen, dass Ihr Git konfiguriert ist):

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

Unter [AGENTS.md](AGENTS.md) finden Sie eine vollständige Liste der verfügbaren Agenten.

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

Das Untermodul verweist auf:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Dadurch wird sichergestellt, dass alle dieselben, aktuellen Agenten verwenden.

## Für Verantwortliche

### Hinzufügen zu einem neuen Repository

1. Fügen Sie das Untermodul hinzu:

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Kopieren Sie die Setup-Dateien:
   - `setup-agents.sh`
   - `setup-agent.md` (im Stammverzeichnis, nicht im Untermodul)
   - `INSTALL.md`

3. Bestätigung:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### Aktualisieren des zentralen Repositorys

Änderungen an Agenten sollten vorgenommen werden in:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Alle Repositorys erhalten Aktualisierungen über `git submodule update --remote`.

&#x200B;---

**Benötigen Sie Hilfe?** Kontaktieren Sie Ihren Dokumentations-Teamleiter oder sehen Sie sich das interne Wiki an.
