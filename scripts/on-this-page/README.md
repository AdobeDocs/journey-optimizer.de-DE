---
source-git-commit: f59dc265b0de732b52e9d26b6ee510733d0d760e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---
# Box-Tools „Auf dieser Seite“

Tools zum Hinzufügen und Überprüfen des **„Auf dieser Seite** schattierten Felds oben in
Dokumentationsseiten zu AJO. Siehe die Spezifikation in `.cursor/rules/on-this-page-box.mdc`.
Der Rollout wird unter episch verfolgt **DOCAC-14936** (eine Aufgabe pro Ordner der obersten Ebene).

## Wie die Kiste aussieht

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## Empfohlener Workflow (pro Ordner/Jira-Aufgabe)

Führen Sie aus dem Repository-Stamm aus (`journey-optimizer.en/`).

1. **Felder einfügen** (Übergabe eines Satzes im ersten Entwurf aus der Frontansicht jeder Seite)
   `description`). Mechanisch, idempotent, berührt nie die Schriftart:

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   Vorschau zuerst mit `--dry-run`.

2. **Verfeinern Sie den Wortlaut.** Der Startpunkt des Testversands ist — jeden Satz so bearbeiten, dass er erscheint
Liest als Zielsetzung (ein Satz, einfacher Text, amerikanisches Englisch). **Leitung
Mit dem**: Geben Sie das Ergebnis/den Nutzen des Lesers an (“…so können Sie &lt;outcome>„), nicht
Nur eine Liste der Inhalte der Seite. Passen Sie Funktionsnamen im Hausstil an (z. B.
„Orchestrierte Kampagne“ (In-App). Siehe `.cursor/rules/on-this-page-box.mdc`. Wenn Sie
`--seed-from-description` überspringen wird stattdessen ein `{{TODO...}}` Platzhalter eingefügt und
Der Validator kennzeichnet alle verbleibenden Elemente.

3. **Validieren** vor dem Öffnen des PR:

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   Bei einem Fehler ist der Exitcode ungleich null, sodass eine CI-Abfrage durchgeführt werden kann.

## Umfang/Ausschlüsse

Referenz- und Syntaxseiten sind standardmäßig ausgeschlossen (Pfadteile `api-reference`,
`expression`, `functions`). Überschreiben Sie bei Bedarf mit `--exclude ...`.

## Repo-weite Fortschrittsüberprüfung

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

Ohne `--require` werden Seiten, denen noch ein Feld fehlt, als `pending` (nicht als
Fehler), sodass Sie den Rollout-Fortschritt über den gesamten Guide hinweg verfolgen können.
