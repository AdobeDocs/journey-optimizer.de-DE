---
source-git-commit: 74723337f97c8196b506ccc1ace11077710494ea
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 1%

---
# Aktualisiertes PDF für Seitenverwaltungsagent (Structure Agent)

## Wiki Page URL
https://wiki.corp.adobe.com/display/~simonetn/%3CUC-12%3E+Structure+Agent

---

# &#x200B;1. Zusammenfassung

Der **Seitenverwaltungs-Agent** (ehemals „Strukturagent„) unterstützt Autoren bei der sicheren Neuorganisation der Dokumentation, indem er Seiten verschiebt, löscht oder umbenennt und dabei automatisch alle Auswirkungen auf das gesamte Repository verwaltet.

**Status:** ✅ **IMPLEMENTIERT** (v1.5.0 - veröffentlicht im November 2025)

**Ziel:** manuelle, fehleranfällige Umgestaltung der Dokumentation durch automatisierte Wirkungsanalysen, transparente Ausführung und umfassende Verifizierung für Verlagerungen, Löschungen und Umbenennungen vermeiden.

JIRA > DOCAC-13695

---

# &#x200B;2. Problembeschreibung

Dokumentations-Repositorys erfordern häufige strukturelle Änderungen. Diese Vorgänge sind derzeit **manuell und extrem**, was zu Folgendem führt:

- **Beschädigte interne Links** - Durch Verschieben einer Seite werden alle Verweise darauf ungültig.
- **Ungültige Ankerlinks** - Deep-Links (`page.md#section`) funktionieren nicht mehr
- **Veraltete Inhaltsverzeichniseinträge** - Inhaltsverzeichnis wird inkonsistent
- **Fehlende Weiterleitungen** - SEO leidet unter fehlerhaften URLs
- **Beschädigte Bildpfade** - Relative Bildpfade werden beschädigt, wenn Seiten Ordner verschieben
- **Veraltete Vorderseite** — Verwandte Seitenverweise werden veraltet
- **Stunden manueller Arbeit** - Autoren müssen Links manuell grappen, suchen und aktualisieren

**Echtes Beispiel:** Um eine Seite von `campaigns/` in `email/` Ordner zu verschieben, müssen mehr als 20 Dateien aktualisiert werden, was 2-3 Stunden dauert und oft Probleme verursacht.

Der **Page Management Agent** automatisiert diesen gesamten Prozess und schließt ihn in weniger als 1 Minute mit 100%iger Genauigkeit ab.

---

# &#x200B;3. Ziele und Schlüsselergebnisse (OKR)

| **Ziel** | **Wichtigste Ergebnisse** | **Status** |
|---------------|-----------------|-----------|
| Vollständigen Umgestaltungs-Workflow automatisieren | 100 % der festgestellten und aktualisierten Auswirkungen | ✅ **ERREICHT** |
| Beseitigen von fehlerhaften Links | 0 fehlerhafte Links nach Vorgängen | ✅ **ERREICHT** |
| Dokumentationsintegrität wahren | 100 % Konsistenz des Inhaltsverzeichnisses/der Umleitung | ✅ **ERREICHT** |
| Zeit für Autoren verkürzen | 95 % Reduktion (3 Stunden → 1 Minute) | ✅ **ERREICHT** |
| Transparente Vorgänge | 100%ige Sichtbarkeit vor der Ausführung | ✅ **ERREICHT** |

---

# &#x200B;4. Drei Kernoperationen

## 📦 Verschieben einer Seite

Verschieben Sie die Seite in einen anderen Ordner und aktualisieren Sie dabei alle Verweise:
- Aktualisiert interne Links (absolut, relativ, stammbezogen)
- Berechnet Bildpfade für neue Ordnerstruktur neu.
- Aktualisiert TOC.md mit neuem Speicherort
- Fügt Umleitungen in redirects.csv hinzu
- Aktualisiert die Frontend-Materie-Referenzen
- Validiert alle Anker-Links

## 🗑️ Löschen einer Seite

Seite mit umfassendem Auswirkungsmanagement entfernen:
- Identifiziert alle Seiten, die mit der gelöschten Seite verknüpft sind
- Richtet optional die Umleitung zur Ersetzungsseite ein
- Entfernt Eintrag aus TOC.md
- Warnt bei fehlerhaften Links, wenn keine Umleitung angegeben wird
- Bereinigt Front-Matter-Verweise

## ✏️ Umbenennen einer Seite

Dateinamen ändern, während der Ordner beibehalten wird:
- Aktualisiert alle Verweise auf den neuen Dateinamen
- Aktualisiert den Eintrag TOC.md
- Fügt Umleitung für SEO-Kontinuität hinzu
- Behält alle Ankerlinks bei
- Aktualisiert die zugehörigen Seitenverweise

---

# &#x200B;5. Workflow (16 Schritte)

| **Schritt** | **Aktion** | **Details** |
|----------|-----------|-------------|
| &#x200B;1. Aufruf | Benutzertypen `@page-management` | Sofortiges Laden des Agenten |
| &#x200B;2. Repository-Suche | Analysieren der Struktur | Dateien zählen, Inhaltsverzeichnis/Umleitungen suchen, Linkdiagramm erstellen |
| &#x200B;3. Betriebsauswahl | Verschieben/Löschen/Umbenennen auswählen | Interaktives Menü |
| &#x200B;4. Pfaderfassung | Quelle und Ziel abrufen | Validieren von Pfaden |
| &#x200B;5. Folgenabschätzung | Umfassender Scan | grep + semantische Suche für alle Verweise |
| &#x200B;6. Bericht über die Auswirkungen | Detailliert vor/nach | Dateipfade, Zeilennummern, Änderungen |
| &#x200B;7. Benutzerbestätigung | Explizite Genehmigung erforderlich | Ja/Nein/Ändern |
| &#x200B;8. Dateifunktionen | Datei verschieben/löschen/umbenennen | Dateisystemvorgang |
| &#x200B;9. Link-Updates | Alle Links aktualisieren | Interne und Anker-Links |
| &#x200B;10. Inhaltsverzeichnisaktualisierung | Inhaltsverzeichnis aktualisieren | Hierarchie beibehalten |
| &#x200B;11. Umleitungsverwaltung | Zu redirects.csv hinzufügen | Für SEO |
| &#x200B;12. Aktualisierung des Bildpfads | Pfade neu berechnen (nur Verschieben) | Beibehalten der Bildauflösung |
| &#x200B;13. Aktualisierung der Frontanfrage | YAML-Verweise aktualisieren | Verwandte Seiten, Voraussetzungen |
| &#x200B;14. Überprüfung | Alle Änderungen validieren | Auf fehlerhafte Links prüfen |
| &#x200B;15. Vorbereitung bestätigen | Commit-Nachricht generieren | Detaillierte Zusammenfassung mit Statistiken |
| &#x200B;16. Optionales Staging | Git hinzufügen, falls angefordert | Convenience-Funktion |

---

# &#x200B;6. Funktionale Anforderungen

| **Kennung** | **Anforderung** | **Priorität** | **Status** |
|--------|----------------|-------------|-----------|
| FR-1 | Unterstützen von Vorgängen zum Verschieben, Löschen und Umbenennen | P1 | ✅ implementiert |
| FR-2 | Erkennen aller internen Links (absolut, relativ, stammrelativ) | P1 | ✅ implementiert |
| FR-3 | Ankerlinks validieren und aktualisieren | P1 | ✅ implementiert |
| FR-4 | Inhaltsverzeichnis automatisch aktualisieren | P1 | ✅ implementiert |
| FR-5 | Verwalten von redirects.csv für SEO | P1 | ✅ implementiert |
| FR-6 | Bildpfade beim Verschieben von Seiten neu berechnen | P1 | ✅ implementiert |
| FR-7 | Frontend-Materie-Referenzen aktualisieren | P1 | ✅ implementiert |
| FR-8 | Erstellen eines umfassenden Wirkungsberichts | P1 | ✅ implementiert |
| FR-9 | Bereitstellen vor/nach der Vorschau | P1 | ✅ implementiert |
| FR-10 | Explizite Benutzerbestätigung verlangen | P1 | ✅ implementiert |
| FR-11 | Transparenten Fortschritt anzeigen | P1 | ✅ implementiert |
| FR-12 | Alle Änderungen überprüfen | P1 | ✅ implementiert |

---

# &#x200B;7. Technische Umsetzung

## Algorithmus der Link-Erkennung

Mehrstrategischer Ansatz:
- **Regex-Muster:** `\[([^\]]+)\]\(([^)]+\.md(?:#[^)]*)?)\)`
- **Handles:** Absolute, relative, root-relative Pfade + Anker
- **Tools:** grep (exakte Übereinstimmung) + codebase_search (semantisch)

## Auflösung des Pfads

Intelligente Algorithmen:
1. Link-Dateiverzeichnis abrufen
2. Relativ zum absoluten Pfad auflösen
3. Pfade normalisieren (`./` entfernen, `..` auflösen)
4. Mit Zielpfad vergleichen
5. Neuen relativen Pfad für Ziel berechnen

## Neuberechnung des Bildpfads

Wenn Sie Seiten zwischen Ordnern verschieben, berechnet relative Pfade neu, um die korrekte Bildauflösung beizubehalten.

**Beispiel:**

```
Original:  help/using/campaigns/page.md
Image:     ![](assets/image.png)
Resolves:  help/using/campaigns/assets/image.png

Moving to: help/using/email/page.md
New image: ![](../campaigns/assets/image.png)
Resolves:  help/using/campaigns/assets/image.png ✅
```

---

# &#x200B;8. Format der Folgenabschätzung

Umfassender Bericht mit folgenden Informationen:

1. **Vorgangszusammenfassung** — Source, Ziel, Typ
2. **Zusammenfassungstabelle der Auswirkungen** — Anzahl jedes Auswirkungstyps
3. **Interne Links** - Datei, Zeile, vor/nach jedem Link
4. **Anker-Links** - Deep-Links mit Abschnittsverweisen
5. **Inhaltsverzeichnisaktualisierungen** — Änderungen des Inhaltsverzeichnisses
6. **Redirects** — Neue Umleitungseinträge
7. **Bildpfade** - Aktualisierte Bildverweise (für Verschiebevorgänge)
8. **Front Matter** - Aktualisierungen der Metadatenreferenz
9. **Mögliche Probleme** - Warnungen
10. **Ausführungsplan** — Schrittweise Vorschau

**Beispiel für einen Wirkungsbericht:**
- 23 interne Links in 15 Dateien aktualisiert
- 5 Anker-Links aktualisiert
- 1 Inhaltsverzeichnis aktualisiert
- 1 Umleitung hinzugefügt
- 4 Bildpfade neu berechnet
- 2 Front Matter-Verweise aktualisiert
- **Insgesamt: 18 Dateien in ~30 Sekunden geändert**

---

# &#x200B;9. Nicht funktionale Anforderungen

| **Kategorie** | **Anforderung** | **Erreicht** |
|--------------|----------------|-------------|
| **Leistung** | Abschluss innerhalb von 60 Sekunden | ✅ 30-45 Sekunden |
| **Genauigkeit** | 100%-Erkennung | ✅ 100 % |
| **Skalierbarkeit** | 1.000 Seiten verarbeiten | ✅ 500+ getestet |
| **Transparenz** | Alle Änderungen anzeigen | ✅ Vorschau abschließen |
| **Sicherheit** | Kein Datenverlust | ✅ explizit bestätigen |
| **Überprüfung** | Änderungen validieren | Automatisierte Prüfungen ✅ |
| **Prüffähigkeit** | Änderungsprotokoll abschließen | Detaillierte Commits ✅ |

---

# &#x200B;10. Erfolgsmetriken

## quantitativ
- **Zeitersparnis:** 95 % Reduktion (2-3 Stunden → &lt;1 Minute)
- **Genauigkeit:** 100 % der Verweise erkannt und aktualisiert
- **Zuverlässigkeit:** 0 fehlerhafte Links nach der Umgestaltung
- **Leistung:** 30-45 Sekunden für typische Vorgänge
- **Abdeckung:** 7 Auswirkungstypen analysiert

## qualitativ
- ✅ Autoren können sicher refaktorieren
- ✅ Vollständige Transparenz
- ✅ Explizite Sicherheitskontrollen
- ✅ Keine manuelle Bereinigung erforderlich
- ✅ vollständige Prüfbarkeit

---

# &#x200B;11. Risiken und Risikominderungen

| **Risiko** | **Impact** | **Abmilderung** |
|----------|-----------|---------------|
| Falsche Pfadberechnungen | Beschädigte Links | ✅ Umfassender Algorithmus + Verifizierung |
| Fehlende Verweise | Beschädigte Links in Randfällen | ✅ Suche mit mehreren Strategien (grep + semantisch) |
| Nicht überprüfte Ausführung | Unbeabsichtigte Änderungen | ✅ Bestätigung erforderlich |
| Dateikonflikte | Datenverlust oder -überschreibungen | ✅ Prüfungen vor dem Flug auf Konflikte |
| Nicht zugesicherte Änderungen | Laufende Arbeiten verloren | ✅ Warnung zu beschädigtem Arbeitsbaum |
| Komplexe relative Pfade | Beschädigte Bildverweise | ✅ Auflösung des getesteten Pfads |
| Großprojekte | Unvollständige Aktualisierungen | ✅ Algorithmen |

---

# &#x200B;12. Gebrauchsanweisung

## Schnellstart

```
@page-management
```

## Befehle in natürlicher Sprache

```
move a page
delete a page
rename a page
refactor documentation
```

## Beispielsitzung

```
User: @page-management

Agent: 🔧 Page Management Agent
       [Scans repository...]
       ✅ Found 487 Markdown files
       
       What would you like to do?
       1. Move a page
       2. Delete a page
       3. Rename a page

User: 1

Agent: Which page do you want to move?

User: help/using/campaigns/setup.md

Agent: Where should it go?

User: help/using/email/setup.md

Agent: [Analyzes impacts...]
       📊 Impact Report:
       - 23 internal links → update needed
       - 5 anchor links → update needed
       - 1 TOC entry → update needed
       - 4 image paths → update needed
       Total: 18 files will be modified
       
       Proceed? (Yes/No)

User: Yes

Agent: ✅ Complete! All changes verified.
       Ready to commit.
```

---

# &#x200B;13. Künftige Verbesserungen

**Geplante Funktionen:**
- Batch-Vorgänge (Verschieben/Umbenennen mehrerer Seiten)
- Dry-Run-Modus (Auswirkungen anzeigen, ohne ausgeführt zu werden)
- Funktion zum Rückgängigmachen/Rollback
- Intelligente Zusammenführungsvorschläge beim Löschen
- Link-Text wird aktualisiert, wenn sich der Titel ändert
- Asset-Verschieben (Verschieben von Bildern mit Seite)
- Umgang mit Repository-übergreifenden Links
- Option für automatische Bestätigung
- Vergleichsvorschau
- Wirkungsberichte exportieren

---

# &#x200B;14. Dokumentation und Ressourcen

- **Agentendatei:** `.cursor-agents/agents/page-management-agent.md`
- **Kurzanleitung:** `.cursor-agents/AGENTS.md`
- **Version:** 1.5.0 (November 2025)
- **repository:** `git@git.corp.adobe.com:AdobeDocs/CursorAgents.git`

**Zusätzliche Dokumentation:**
- Einrichtungshandbuch: `INSTALL.md`
- Fehlerbehebung: `TROUBLESHOOTING.md`
- Alle Agenten: `AGENTS.md`

---

# &#x200B;15. Versionshinweise

## v1.5.0 (November 2025) — Erste Version
- ✅ Vollständige Implementierung von Vorgängen zum Verschieben/Löschen/Umbenennen
- ✅ Umfassende Folgenabschätzung (7 Referenztypen)
- Transparente Ausführung mit Fortschrittsverfolgung ✅
- Automatisierte Überprüfung und Validierung ✅
- ✅ Erstellung einer detaillierten Commit-Nachricht
- ✅ der automatischen Versionsüberprüfung
- ✅ Neustartrichtlinie (kein Kontext erforderlich)

## Bekannte Einschränkungen
- Nur Einzelseitenvorgänge (Batch kommt bald)
- Sauberer Arbeitsbaum für Sicherheit erforderlich (Warnung bereitgestellt)
- Manueller Commit erforderlich (automatischer Commit kommt bald)

---

*Letzte Aktualisierung: 6. November 2025*

