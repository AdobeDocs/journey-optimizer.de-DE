---
solution: Journey Optimizer
product: Journey Optimizer
title: Testen, Validieren und Genehmigen
description: Entdecken Sie alle Test- und Genehmigungsfunktionen in Journey Optimizer. Vorschau von Inhalten, Simulieren von Journey, Validieren von E-Mails, Durchführen von Experimenten, Erkennen von Konflikten und Einrichten von Validierungs-Workflows vor dem Start.
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: Testen, Validieren, Genehmigen, Validieren, Validieren, Qualitätssicherung, QA, Testprofile, Personalisierung, Rendering, Spam-Check, Content-Experiment, A/B-Test, Konflikterkennung, Seed-Liste, Testsendungen, Sample-Daten, Validierungs-Workflow, E-Mail-Test, Validierungs-Workflow
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: abb2ed3cfa617bb9afc23c8f69634d5afe89b33e
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 5%

---

# Testen, Validieren und Genehmigen{#section-overview}

Dieser Abschnitt behandelt alle Test- und Genehmigungsfunktionen in Journey Optimizer. Hier finden Sie Tools zur Vorschau von Inhalten mit Testprofilen, zur Validierung der Journey-Logik, zum Überprüfen des E-Mail-Renderings und der Spam-Punktzahl, zum Durchführen von A/B-Experimenten, zum Erkennen von Konflikten und zum Einrichten von Genehmigungs-Workflows.

Auf dieser Landingpage können Sie den richtigen Testansatz auswählen, der auf dem basiert, was Sie erstellen (Kampagnen vs. Journey), führt Sie durch empfohlene Test-Workflows und bietet schnellen Zugriff auf alle Test- und Genehmigungsressourcen. Beginnen Sie [&#x200B; unten mit „Wählen Sie &#x200B;](#choose-your-testing-approach) Testansatz aus“, um festzustellen, welche Tools für Ihren Anwendungsfall gelten.

## Warum Tests und Genehmigungen wichtig sind

Test- und Validierungsprozesse dienen als wichtige Qualitätsprüfungen, die den Ruf Ihrer Marke schützen und den Erfolg Ihrer Kampagnen sicherstellen. Hier ist, warum sie wichtig sind:

* **Fehler erkennen, bevor sie Kunden erreichen** - Identifizieren Sie fehlerhafte Links, falsche Personalisierung, Rendering-Probleme und Logikfehler in einer kontrollierten Umgebung, in der Korrekturen schnell und risikolos sind.

* **Zustellbarkeit verbessern** - Spam-Bewertungen testen, die E-Mail-Authentifizierung überprüfen und das Rendering auf allen E-Mail-Clients überprüfen, um die Platzierungs- und Interaktionsraten im Posteingang zu maximieren.

* **Markenkonsistenz sicherstellen** - Vorschau von Inhalten mit verschiedenen Testprofilen, um zu überprüfen, ob die Personalisierung für verschiedene Kundensegmente korrekt angezeigt wird und die Markenstandards einhält.

* **Validieren komplexer Journey** - Simulieren Sie mehrstufige Journey-Flüsse, um sicherzustellen, dass Trigger korrekt ausgelöst werden, Bedingungen ordnungsgemäß ausgewertet werden und Kunden die richtigen Nachrichten zur richtigen Zeit erhalten.

* **Verantwortlichkeit herstellen** - Implementieren formaler Genehmigungs-Workflows, die die Zustimmung der Stakeholder erfordern, wodurch eine klare Eigentümerschaft geschaffen und die Anzahl nicht autorisierter oder vorzeitiger Kampagnenstarts reduziert wird.

* **Zeit und Ressourcen sparen** - Erkennung von Problemen frühzeitig im Entwicklungszyklus, wenn Fehlerbehebungen billiger und schneller sind, wodurch kostspielige Korrekturen nach der Markteinführung oder Eskalationen beim Kundenservice vermieden werden.

## Übersicht über Testfunktionen

**Verfügbare Testtypen:**

* [&#x200B; Inhaltstests: Vorschau und Validierung des Nachrichteninhalts vor dem Senden →Testkampagnen](#testing-campaigns), [Personalisierung testen](#testing-personalization)
* Journey-Logiktests: Simulieren des Kundenfortschritts über Journey-Pfade → [Testen von Journey](#testing-journeys)
* Technische Tests: Validieren von Rendering, Zustellbarkeit und Authentifizierung → [Technische Validierung](#2-technical-validation)
* Leistungstests: Vergleichen von Inhaltsvarianten mithilfe von A/B-Experimenten → [Inhaltsexperimente](#content-experiments--ab-testing)
* Konflikttests: Überschneidungen zwischen Kampagnen und Journey erkennen → [Konflikterkennung](#conflict-detection)
* Validierungstests: Strukturierte Prüfungs-Workflows vor der Aktivierung → [Genehmigungs-Workflows](#approval-workflows-for-journeys-and-campaigns)

**Schlüsselfunktionen nach Kontext:**

| Funktion | Gilt für | Kanalbeschränkungen | Voraussetzungen | Primärer Zweck |
|------------|-----------|---------------------|--------------|-----------------|
| [Testprofile](../using/content-management/test-profiles.md) | Journey | Alle Kanäle | Erstellte Testprofile | Vorschau personalisierter Inhalte |
| [Beispieleingabedaten](../using/test-approve/simulate-sample-input.md) | Journey | E-Mail, SMS, Push, Web, Code-basiert, In-App, Inhaltskarten | CSV-/JSON-Datei | Testen mehrerer Personalisierungsvarianten |
| [Testmodus](../using/building-journeys/testing-the-journey.md) | Nur Journey | k. A. | Entwurfs-Journey, konfigurierter Namespace | Profilfortschritt simulieren |
| [Probelauf](../using/building-journeys/journey-dry-run.md) | Nur Journey | k. A. | Journey erstellt | Ausführungspfade analysieren |
| [E-Mail-Rendering](../using/content-management/rendering.md) | Journey | Nur E-Mail | Litmus-Integration | Überprüfen der Anzeige auf allen Clients |
| [Spam-Punktzahl](../using/content-management/spam-report.md) | Journey | Nur E-Mail | Keine | Validierung der Zustellbarkeit |
| [Testadressenlisten](../using/configuration/seed-lists.md) | Journey | Nur E-Mail | Liste der konfigurierten Testadressen | Überwachung durch Stakeholder |
| [Inhaltsexperimente](../using/content-management/get-started-experiment.md) | Nur Kampagnen | Alle Kanäle | Keine | A/B- und Multi-Armed-Bandit-Tests |
| [Konflikterkennung](../using/conflict-prioritization/conflicts.md) | Kampagnen, Journey (eingeschränkt) | Alle Kanäle | Keine | Vermeidung von Kunden-Übermeldungen |
| [Genehmigungs-Workflows](../using/test-approve/gs-approval.md) | Journey | Alle Kanäle | Genehmigungsrichtlinie erstellt | Strukturierter Überprüfungsprozess |
| [Personalization Playground](../using/personalization/personalize.md#playground) | Alle | Alle Kanäle | Keine | Kennenlernen und Testen der Personalisierungssyntax |

**Allgemeine Test-Workflows:**

1. Vorentwicklung: Verwenden des [Personalisierungsspielplatzes](#testing-personalization) um die Syntax zu erlernen
2. Während der Entwicklung: Vorschau mit [Testprofilen](#testing-campaigns), Validierung mit [Beispieleingabedaten](#simulate-content-variations)
3. Pre-Launch: Ausführen [technischen Tests](#2-technical-validation) (Rendering, Spam), Überprüfen [Konflikte](#conflict-detection), Senden zur [Genehmigung](#approval-workflows-for-journeys-and-campaigns)
4. Nach dem Launch: Überwachung mit Live-Berichten (siehe [Überwachung und Fehlerbehebung](#monitoring--troubleshooting)), Iteration auf der Grundlage der Ergebnisse


## Wichtige Terminologie

**[Testprofile](../using/content-management/test-profiles.md)** = Synthetische Kundenprofile (keine echten Kunden), die für die Vorschau personalisierter Inhalte verwendet werden. Im Echtzeit-Kundenprofil-Service gekennzeichnet. Erforderlich für Testmodus und Inhaltsvorschau. [Informationen zum Erstellen von Testprofilen](../using/audience/creating-test-profiles.md)

**[Testmodus](../using/building-journeys/testing-the-journey.md)** = Journey-Simulationsfunktion, die Testprofile über Journey-Pfade sendet. Einschränkungen: Nur Entwurfs-Journey, erfordert Namespace, nur Testprofile. [Siehe Dokumentation zum Testmodus](../using/building-journeys/testing-the-journey.md)

**[Probelauf](../using/building-journeys/journey-dry-run.md)** = Journey-Ausführungs-Analyse-Tool, das Pfade verfolgt, ohne Nachrichten zu senden oder API-Aufrufe durchzuführen. Anwendungsfall: Logik validieren, ohne Ressourcen zu verbrauchen. [Erfahren Sie mehr über Probelauf](../using/building-journeys/journey-dry-run.md)

**[Beispieleingabedaten](../using/test-approve/simulate-sample-input.md)** = CSV- oder JSON-Dateien mit Profilattributwerten zum Testen der Personalisierung. Unterstützt bis zu 30 Varianten. Alternative zur Erstellung von Testprofilen. [Simulieren von Inhaltsvarianten](../using/test-approve/simulate-sample-input.md)

**[Testadressen](../using/configuration/seed-lists.md)** = E-Mail-Adressen interner Stakeholder, die automatisch in die tatsächlichen Sendungen einbezogen werden (keine Testsendungen). Nur E-Mail-Kanal Anwendungsfall: Qualitätsüberwachung und Compliance. [Konfigurieren von Testadressenlisten](../using/configuration/seed-lists.md)

**[Inhaltsexperimente](../using/content-management/get-started-experiment.md)** = A/B-Tests oder Experimente mit mehrarmigen Banditen, bei denen Inhaltsvarianten verglichen werden. Nur Kampagnen, in Journey nicht verfügbar. [Erste Schritte mit Experimenten](../using/content-management/get-started-experiment.md) | [Experimente erstellen](../using/content-management/content-experiment.md)

**[Testsendungen](../using/content-management/proofs.md)** = E-Mail-Testsendungen an bestimmte E-Mail-Adressen, die Testprofildaten verwenden. Anders als Seed-Listen (Testsendungen sind manuelle Testsendungen, Seed-Listen sind automatische Stakeholder-Kopien). [Testsendungen durchführen](../using/content-management/proofs.md)

**[Konflikterkennung](../using/conflict-prioritization/conflicts.md)** = Tool, mit dem sich überschneidende Kampagnen und Journey identifiziert werden, die auf dieselben Zielgruppen abzielen. Eingeschränkte Journey-Unterstützung: nur unitäre, Zielgruppen-Qualifizierungs- und „Zielgruppe lesen“-Typen. [Erfahren Sie mehr über Konfliktmanagement](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[Genehmigungs-Workflows](../using/test-approve/gs-approval.md)** = mehrstufiger Überprüfungsprozess, der vor der Aktivierung von den Stakeholdern genehmigt werden muss. Erfordert die Konfiguration der Genehmigungsrichtlinie. [Genehmigungen einrichten](../using/test-approve/gs-approval.md) | [Richtlinien erstellen](../using/test-approve/approval-policies.md)

**[Rendering-Tests](../using/content-management/rendering.md)** = Validierung der E-Mail-Anzeige auf allen E-Mail-Clients (Gmail, Outlook, Apple Mail) und Geräten. Erfordert Litmus-Integration. [E-Mail-Rendering testen](../using/content-management/rendering.md)

**[Personalization Playground](../using/personalization/personalize.md#playground)** = interaktive Lernumgebung zum Experimentieren mit Personalisierungssyntax und Testausdrücken mit Beispieldaten. Keine Live-Datensätze erforderlich. [Zugang zum Spielplatz](../using/personalization/personalize.md#playground)

## Entscheidungsbaum für die Auswahl der Testmethode

Verwenden Sie diesen Entscheidungsbaum, um schnell die richtigen Test-Tools für Ihr spezifisches Szenario zu ermitteln. Beantworten Sie jede Frage basierend auf Ihrem Kontext (was Sie erstellen, was Sie validieren müssen und welchen Kanal Sie verwenden), um direkt zu den relevanten Funktionen und zur entsprechenden Dokumentation zu navigieren.

+++ **Frage 1: Was wird getestet?**

* Campaign → [Testen von Kampagnen](#testing-campaigns)
* Journey → [Journey testen](#testing-journeys)
* Personalization-Ausdrücke → [Personalization-Playground](#testing-personalization)
+++

+++**Frage 2: Welche Aspekte müssen validiert werden?**

* Inhalt und Personalisierung → [Testprofile](#testing-campaigns) oder [Beispieleingabedaten](#simulate-content-variations)
* E-Mail→Anzeige [E-Mail-Rendering-Tests](#2-technical-validation)
* Zustellbarkeit → [Spam-Punkteprüfungen](#2-technical-validation)
* Journey-Logik und → [Testmodus](#testing-journeys) oder [Probelauf](#journey-dry-run)
* Leistungsvergleich → [Inhaltsexperiment](#content-experiments--ab-testing) (nur Kampagnen)
* Zeitkonflikte → [Konflikterkennung](#conflict-detection)
* Stakeholder-Überprüfung → [Genehmigungs-Workflow](#approval-workflows-for-journeys-and-campaigns)
+++

+++**Frage 3: Welcher Kanal?**

* E-Mail → Alle verfügbaren Testmethoden (siehe [Testkampagnen](#testing-campaigns))
* SMS, Push→ [Inhaltstests](#testing-campaigns), [Beispieleingabedaten](#simulate-content-variations), [Genehmigungs-Workflows](#approval-workflows-for-journeys-and-campaigns)
* Web, In-App, Code-basiert → [&#128279;](#testing-campaigns), [Beispieleingabedaten](#simulate-content-variations), [Genehmigungs-Workflows](#approval-workflows-for-journeys-and-campaigns)
* Mehrere Kanäle → Jeden Kanal separat testen
+++

+++**Frage 4: Wann im Workflow?**

* Vor dem Erstellen → [Personalization-](#personalization-playground) zum Lernen
* Beim Erstellen → [Testprofile](#testing-campaigns) und [Beispieleingabedaten](#simulate-content-variations) zur Validierung
* Vor dem Start → [Rendering](#2-technical-validation), [Spam-](#email-spam-report), [Konflikterkennung](#conflict-detection), [Genehmigungen](#approval-workflows-for-journeys-and-campaigns)
* Nach dem Start → [Live-](../using/building-journeys/report-journey.md)) und [Monitoring](#monitoring--troubleshooting)
+++


## Wählen Sie Ihren Testansatz

Der richtige Testansatz hängt davon ab, was Sie erstellen und was Sie validieren müssen. Verwenden Sie diese Anleitung, um die wichtigsten Test-Tools für Ihr Szenario zu ermitteln.

>[!BEGINTABS]

>[!TAB Testen von Kampagnen]

**Für alle Kampagnen:**

* Vorschau und Testinhalt mit [Testprofilen](../using/content-management/test-profiles.md) oder [Beispieleingabedaten](../using/test-approve/simulate-sample-input.md)
* Überprüfen [E-Mail-Rendering](../using/content-management/rendering.md) auf Geräten und Clients (nur E-Mail-Kanal)
* Ausführen [Spam-Score-Prüfungen](../using/content-management/spam-report.md) (nur E-Mail-Kanal)
* Überprüfen Sie [Konflikte](../using/conflict-prioritization/conflicts.md) mit anderen Kampagnen und Journey
* Einrichten [Testlisten](../using/configuration/seed-lists.md) für die Überwachung durch Stakeholder (nur E-Mail-Kanal)
* Vor der Aktivierung [Genehmigung](../using/test-approve/gs-approval.md) einreichen

**Für A/B-Tests und -Optimierung:**

* Erstellen [Inhaltsexperimente](../using/content-management/get-started-experiment.md) um mehrere Behandlungen zu testen und die Leistung zu messen

**Für API-ausgelöste Kampagnen:**

* Verwenden Sie die [Kampagnensimulations-API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} um Trigger-Korrekturabzugsaufträge programmgesteuert auszuführen

>[!TAB Testen von Journey]

**Für alle Journey:**

* Journey Verwenden Sie [Testmodus](../using/building-journeys/testing-the-journey.md) um den Profilfortschritt (nur Entwurfsmodelle, erfordert Namespace) oder [Probelauf) zu simulieren, &#x200B;](../using/building-journeys/journey-dry-run.md) Ausführungspfade ohne Senden von Nachrichten zu analysieren
* Testen einzelner Nachrichten mit [Vorschau und Testsendungen](../using/content-management/preview-test.md)
* Überprüfen [Konflikte](../using/conflict-prioritization/conflicts.md) mit anderen Journey und Kampagnen
* Vor der Veröffentlichung [Genehmigung](../using/test-approve/gs-approval.md) einreichen

**Für komplexe Journey:**

* Testmodus und Probelauf gemeinsam verwenden, um Verzweigungslogik und Ausführungspfade gründlich zu validieren
* Systematisches Testen unterschiedlicher Einstiegsbedingungen und Profilattribute

**Hinweis** Die Konflikterkennung und die Journey-Begrenzung sind nur für die Journey der unitären und der Zielgruppen-Qualifizierung sowie für die Aktivität „Zielgruppe lesen“ verfügbar.

>[!TAB Testen der Personalisierung]

**Vor dem Erstellen von Inhalten:**

* Experimentieren Sie im [Personalisierungs-Playground](../using/personalization/personalize.md#playground) um Syntax- und Testausdrücke mit Beispieldaten zu erlernen

**Bei der Inhaltserstellung:**

* Vorschau mit [Testprofilen](../using/content-management/test-profiles.md) um zu überprüfen, ob die Personalisierung korrekt dargestellt wird
* Testen mehrerer Szenarien mit [Beispieleingabedaten](../using/test-approve/simulate-sample-input.md) aus CSV-/JSON-Dateien (unterstützt bis zu 30 Varianten)

>[!ENDTABS]

## Best Practices für Tests

Befolgen Sie die folgenden empfohlenen Vorgehensweisen, um die Effektivität Ihrer Testaktivitäten zu maximieren:

1. **Früh und häufig testen** - Nicht warten, bis eine Kampagne vollständig erstellt ist. Testen Sie Inhalt, Personalisierung und Logik schrittweise während der Entwicklung.

1. **Verwenden realistischer Testprofile** - [Erstellen Sie Testprofile](../using/audience/creating-test-profiles.md) die Ihre Zielgruppensegmente genau darstellen, einschließlich Edge-Fällen und verschiedener Personalisierungsszenarien.

1. **Testen geräteübergreifend** - Überprüfen Sie [E-Mail-Rendering](../using/content-management/rendering.md) auf gängigen E-Mail-Clients (Gmail, Outlook, Apple Mail) und Geräten (Desktop, Mobile, Tablet), um eine konsistente Anzeige sicherzustellen (nur E-Mail-Kanal).

1. **Personalisierung gründlich validieren** - Testen Sie mit mehreren [Testprofilen](../using/content-management/test-profiles.md) die unterschiedliche Attributwerte aufweisen, um zu bestätigen, dass Personalisierungs-Token korrekt gerendert werden und Fallback-Werte funktionieren. Verwenden Sie den [Personalisierungs-Playground](../using/personalization/personalize.md#playground) um mit Personalisierungsausdrücken zu experimentieren und Code mit Beispieldaten zu testen, bevor Sie sie auf Ihre Kampagnen anwenden.

1. **Testen von Inhaltsvarianten mit Beispieldaten** - Verwenden Sie [Beispieleingabedaten](../using/test-approve/simulate-sample-input.md) aus CSV- oder JSON-Dateien, um bis zu 30 Personalisierungsszenarien zu testen, ohne zahlreiche Testprofile zu erstellen, was Zeit spart und gleichzeitig eine umfassende Abdeckung gewährleistet. Unterstützt die Kanäle E-Mail, SMS, Push, Web, Code-basiertes Erlebnis, In-App und Inhaltskarten .

1. **Testadressenlisten für die Überwachung durch Stakeholder verwenden** - Konfigurieren Sie [Testadressenlisten](../using/configuration/seed-lists.md) so, dass interne Stakeholder automatisch einbezogen werden, die zur Qualitätsüberwachung und Kompatibilitätsüberprüfung Kopien aller Sendungen zur Ausführungszeit erhalten (nur E-Mail-Kanal).

1. **Journey-Pfade simulieren** - Verwenden Sie bei komplexen Journey mit mehreren Verzweigungen [Testmodus](../using/building-journeys/testing-the-journey.md), um verschiedene Einstiegsbedingungen und Profilattribute zu testen, um alle möglichen Pfade zu validieren. Verfügbar für Journey-Entwürfe, die einen Namespace verwenden.

1. **Zustellbarkeitsindikatoren überprüfen** - Überprüfen Sie [Spam-](../using/content-management/spam-report.md), den Authentifizierungsstatus und die Metriken zum E-Mail-Status vor großen Sendungen (nur E-Mail-Kanal).

1. **Dokumentieren von Testergebnissen** - Führen Sie Aufzeichnungen über Testergebnisse, gefundene Probleme und Lösungen, um zukünftige Testprozesse zu verbessern, und tauschen Sie die Erkenntnisse mit Ihrem Team aus.

1. **frühzeitige Einbeziehung von Stakeholdern** - Teilen Sie Vorschauen und Testergebnisse mit Stakeholdern, bevor [formelle Genehmigung](../using/test-approve/gs-approval.md) erfolgt, um Feedback zu sammeln und Erwartungen abzustimmen.

## Empfohlener Test-Workflow

Folgen Sie diesem systematischen Ansatz, um gründliche Tests und reibungslose Genehmigungen sicherzustellen:

### &#x200B;1. Inhaltsentwicklung und -vorschau

Erstellen Sie zunächst Ihren Inhalt und verwenden Sie die Vorschaufunktionen, um das anfängliche Design und die Personalisierung zu überprüfen:

* Gestalten Sie Ihre [E](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [Push-Benachrichtigung](../using/push/create-push.md) oder anderen Kanalinhalt

* Verwenden der **[Inhalt simulieren](../using/content-management/preview-test.md)** für die Vorschau mit Testprofilen

* Überprüfen [Personalisierungs-Token](../using/personalization/personalization-syntax.md), dynamischen Inhalte und Fallback-Werte

* Experimentieren Sie mit Personalisierungsausdrücken im **[Personalisierungs-Playground](../using/personalization/personalize.md#playground)** um Ihren Code mit Beispieldaten zu testen und zu verfeinern, bevor Sie ihn auf Live-Inhalte anwenden

* Testen Sie mehrere Varianten mithilfe **[Beispieleingabedaten)](../using/test-approve/simulate-sample-input.md)** CSV-/JSON-Dateien, um die Personalisierung in verschiedenen Profilszenarien zu validieren

* Überprüfen [Rendering](../using/content-management/rendering.md) über verschiedene Bildschirmgrößen und E-Mail-Clients hinweg

### &#x200B;2. Technische Validierung

Validieren Sie technische Aspekte, die sich auf Zustellbarkeit und Funktionalität auswirken:

* Führen Sie [Spam-Score-Prüfungen](../using/content-management/spam-report.md) aus, um potenzielle Probleme mit der Zustellbarkeit zu identifizieren

* Testen Sie Links, um sicherzustellen, dass sie nicht beschädigt sind, und verfolgen Sie sie ordnungsgemäß

* Konfiguration [E-Mail-Authentifizierung](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC) überprüfen

* Überprüfen des HTML-Renderings und Überprüfen der CSS-Kompatibilität

* Testen [responsiven Designs](../using/email/content-from-scratch.md) auf mobilen und Desktop-Geräten

* Suchen Sie nach [potenziellen Konflikten](../using/conflict-prioritization/conflicts.md) mit anderen Kampagnen und Journey, um die Ermüdung von Kundennachrichten und Timing-Probleme zu vermeiden.

### &#x200B;3. Journey-Tests (nur Journey)

Wenn Sie eine Journey testen, validieren Sie die Orchestrierungslogik:

* Aktivieren Sie **[Testmodus](../using/building-journeys/testing-the-journey.md)**, um den Profilverlauf über den Journey zu simulieren

* Unterschiedliche [&#x200B; (Eintrittsbedingungen](../using/building-journeys/entry-management.md) und Zielgruppenqualifikationen testen

* Überprüfen[&#x200B; ob &#x200B;](../using/building-journeys/wait-activity.md), [Bedingungen](../using/building-journeys/condition-activity.md) und Verzweigungslogik ordnungsgemäß funktionieren

* Verwenden **[Probelauf](../using/building-journeys/journey-dry-run.md)** für komplexe Journey, um Ausführungspfade zu analysieren, ohne Nachrichten zu senden

* Überprüfen Sie[&#x200B; ob &#x200B;](../using/event/about-events.md) Trigger und [benutzerdefinierte Aktionen](../using/action/about-custom-action-configuration.md) erwartungsgemäß ausgeführt werden

### &#x200B;4. Einreichung der Genehmigung

Sobald der Test abgeschlossen und die Probleme behoben sind:

* Senden Sie die Kampagne oder Journey zur Validierung gemäß der [&#x200B; Ihres Unternehmens](../using/test-approve/approval-policies.md)

* Fügen Sie Testergebnisse und Dokumentation mit der [Genehmigungsanfrage“ &#x200B;](../using/test-approve/request-approval.md)

* Adressieren von Feedback- oder Änderungsanforderungen von [genehmigenden Personen](../using/test-approve/review-approve-request.md)

* Erforderliche Revisionen vornehmen und bei signifikanten Änderungen erneut testen

### &#x200B;5. Verifizierung vor dem Start

Vor der Aktivierung der Kampagne oder des Journey:

* Abschließende Überprüfung aller Einstellungen, Zielgruppen und [Zeitpläne](../using/building-journeys/journey-properties.md)

* Überprüfen, ob alle Genehmigungen vorliegen und dokumentiert sind

* Bestätigen Sie, dass Versandzeiten [Zeitzonen](../using/building-journeys/timezone-management.md) korrekt sind

* Aktivieren [Überwachung und Warnhinweise](../using/reports/alerts.md) um die Leistung nach dem Start zu verfolgen

### &#x200B;6. Überwachen und Wiederholen

Setzen Sie die Überwachung nach dem Launch fort, um Probleme frühzeitig zu erkennen:

* Einrichten [Systemwarnungen](../using/reports/alerts.md) für Journey-Fehler, hohe Absprungraten oder geringe Interaktion

* Überprüfen Sie [Live-Berichte](../using/building-journeys/report-journey.md), um die Leistung im Vergleich zu den Erwartungen zu verfolgen.

* Seien Sie darauf vorbereitet[&#x200B; Journey bei kritischen &#x200B;](../using/building-journeys/journey-pause.md) anzuhalten oder zu ändern

* Dokumentieren der gewonnenen Erkenntnisse zur Verbesserung zukünftiger Testprozesse

## Testen in Aktion: Anwendungsfälle

Hier erfahren Sie, wie Testkonzepte auf reale Szenarien angewendet werden:

| Anwendungsfall | Was Sie lernen werden | Wichtiger Testschwerpunkt |
|----------|-------------------|-------------------|
| **[Senden von Multi-Channel-Nachrichten](../using/building-journeys/journeys-uc.md)** | Testen Sie eine Journey, die „Zielgruppe lesen“, Reaktionsereignisse und E-Mail-/Push-Nachrichten kombiniert. Validieren des gesamten Flusses von der Audience bis zum Nachrichtenversand. | Multi-Channel-Koordination, Reaktionsereignisse, End-to-End-Flussvalidierung, Tests und Veröffentlichungsschritte |
| **[Senden einer Nachricht an Abonnenten](../using/building-journeys/message-to-subscribers-uc.md)** | Testen Sie Journey, die Abonnement-Listen mit dynamischer E-Mail-Adressierung ansprechen. Validieren von Personalisierungsausdrücken für das korrekte Abonnenten-Targeting. | Personalization-Ausdrücke, dynamische Adressierung, Targeting von Abonnement-Listen |
| **[Senden von zeitgebundenen Nachrichten](../using/building-journeys/weekday-email-uc.md)** | Testen Sie Journey mit zeitbasierten Bedingungen, um sicherzustellen, dass Nachrichten an bestimmten Tagen gesendet werden. Warteaktivitäten und Planungslogik validieren | Zeitbasierte Bedingungen, Warteaktivitäten, Validierung planen |
| **[Erkunden Sie weitere Journey-Anwendungsfälle](../using/building-journeys/jo-use-cases.md)** | Zugriff auf eine umfassende Sammlung praktischer Beispiele zu Erlebnisereignissen, Multi-Channel-Messaging und externen Systemintegrationen. | Verschiedene Szenarien, erweiterte Muster, Integrationstests |

## Testen und Genehmigen von Inhalten

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Vorschau, Testen und Validieren von Inhalten

Erfahren Sie, wie Sie personalisierte Inhalte mithilfe von Testprofilen, E-Mail-Render-Tests, Spam-Bewertungen und mehr in der Vorschau anzeigen, testen und validieren können.

[Vorschau und Testen der Inhalte erkunden](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

Validierungs-Workflows für Journeys und Kampagnen

Erfahren Sie, wie Sie Validierungsprozesse einrichten, verwalten und ausführen, um eine Qualitätskontrolle für Journeys und Kampagnen sicherzustellen.

[Informationen zu Validierungs-Workflows](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Testen der Journey

Validieren Sie Ihren Journey vor der Veröffentlichung, indem Sie ihn mit bestimmten Profilen testen, um sicherzustellen, dass Ereignisse, Bedingungen und Aktionen erwartungsgemäß funktionieren. Verfügbar für Journey-Entwürfe, die einen Namespace verwenden.

[Journey testen](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Journey-Probelauf

Führen Sie einen Probelauf durch, um Ihren Journey-Ausführungspfad zu simulieren und zu validieren und potenzielle Probleme zu identifizieren, bevor Sie live gehen.

[Informationen zu Journey-Probeläufen](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Monitoring und Fehlerbehebung

Zugriff auf umfassende Ressourcen zur Fehlerbehebung, Systemwarnungen und Fehler-Codes zur Behebung von Journey-Ausführungs- und Leistungsproblemen.

[Monitoring und Fehlerbehebung anzeigen](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization Playground

Experimentieren Sie mit Personalisierungsausdrücken in einer sicheren Umgebung. Testen Sie den Code mit Beispieldaten und sehen Sie sich die Ergebnisse in der Vorschau an, bevor Sie ihn auf Ihre Kampagnen und Journey anwenden.

[Informationen zum Personalization Playground](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

Inhaltsexperimente und A/B-Tests

Optimieren Sie Ihre Kampagnen, indem Sie mehrere Inhaltsvarianten testen und die Leistung messen, um die Behandlungen mit der besten Leistung zu ermitteln. Nur für Kampagnen verfügbar (unterstützt A/B- und Multi-Armed-Bandit-Experimente).

[Informationen zu Inhaltsexperimenten](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Testadressenlisten für die Überwachung durch Stakeholder

Automatische Einbeziehung interner Stakeholder-Adressen in Sendungen, um tatsächliche Nachrichten zu überwachen, die zur Qualitätssicherung und Compliance an Kunden gesendet werden. Nur für E-Mail-Kanal verfügbar.

[Konfigurieren von Testadressenlisten](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

Konflikterkennung

Identifizieren Sie potenzielle Überschneidungen zwischen Kampagnen und Journey, um zu verhindern, dass Kunden mit zu vielen gleichzeitigen Nachrichten überhäuft werden. Verfügbar für Kampagnen und Einzelkampagnen, Zielgruppen-Qualifizierung und Journey-Liste „Zielgruppe lesen“.

[Konflikte erkennen](../using/conflict-prioritization/conflicts.md)
:::

::::

## Weitere Ressourcen

>[!BEGINTABS]

>[!TAB Grundlegende Handbücher]

* [Inhaltsvarianten simulieren](../using/test-approve/simulate-sample-input.md) - Testen von bis zu 30 Personalisierungsszenarien mithilfe von CSV- oder JSON-Dateien. Ideal für mehrsprachige Inhaltstests ohne Erstellung mehrerer Testprofile. Unterstützt E-Mail, SMS, Push, Web, Code-basiert, In-App und Inhaltskarten.

* [Erstellen von Testprofilen](../using/audience/creating-test-profiles.md) - Erstellen und Verwalten von Testprofilen zur Simulation von Kundenszenarien. Erfahren Sie, wie Sie Profile für Tests kennzeichnen, Attribute festlegen und Testsegmente organisieren.

* [E-Mail-Spam-Bericht](../using/content-management/spam-report.md) - Spam-Bewertungen vor dem Versand überprüfen, um die Zustellbarkeit und die Platzierung im Posteingang zu verbessern. Erhalten Sie umsetzbare Empfehlungen für die Inhaltsoptimierung.

* [Häufig gestellte Fragen zum Journey](../using/building-journeys/journey-faq.md) - Kurzanleitung zu häufigen Fragen zu Journey-Tests, Ausführung und Fehlerbehebung.

>[!TAB Abhängigkeiten und Beziehungen]

Erfahren Sie, wie Testfunktionen miteinander und mit Ihren Journey Optimizer-Workflows im weiteren Sinne verbunden sind. In diesem Abschnitt werden Voraussetzungen, Upstream-/Downstream-Abhängigkeiten und allgemeine Funktionskombinationen beschrieben.

+++**Voraussetzungen (vor dem Testen erforderlich)**

* Testprofile müssen vor der Verwendung des Testmodus oder der Inhaltsvorschau erstellt werden
* Genehmigungsrichtlinien müssen konfiguriert werden, bevor sie zur Genehmigung eingereicht werden
* Testadressenlisten müssen vor dem Hinzufügen zu Kampagnen/Journey erstellt werden
* Litmus-Integration für E-Mail-Rendering-Tests erforderlich
* Journey muss sich im Entwurfsstatus befinden, um den Testmodus zu verwenden
* Für Journey muss der Namespace konfiguriert sein, um den Testmodus zu verwenden

+++

+++**Welche Tests hängen von (Upstream) ab**

* Inhaltserstellung: Testen von Kampagnen oder Journey erforderlich
* Testprofile: Erforderlich für Testmodus und Inhaltsvorschau
* Genehmigungsrichtlinien: Für Genehmigungs-Workflows erforderlich
* Konfiguration: Kanalkonfigurationen, E-Mail-Authentifizierung, Domain-Einstellungen

+++

+++**Was hängt von Tests ab (nachgelagert)**

* Aktivierung von Kampagnen/Journey: Aktivierung ohne Behebung von Fehlern nicht möglich
* Veröffentlichung: Vor der Veröffentlichung kann eine Genehmigung erforderlich sein
* Live-Überwachung: Überwachung und Reporting nach der Markteinführung
* Optimierung: Verwenden von Testergebnissen zur Verfeinerung künftiger Kampagnen

+++

+++**Verwandte Funktionen**

* Test- und Genehmigungs-Workflows = Qualitätssicherungsprozess
* Testen + Konflikterkennung = Vermeidung von Kunden-Übermeldungen
* Tests + Inhaltsexperimente = Leistungsoptimierung
* Tests + Reporting = kontinuierlicher Verbesserungszyklus
* Testprofile + Personalization = Inhaltsvalidierung
* Probelauf + Testmodus = Umfassende Journey-Validierung

+++

+++**Allgemeine Funktionskombinationen**

* Inhaltstests: Testprofile + Beispieleingabedaten + Personalization Playground
* E-Mail-Validierung: Rendering-Tests + Spam-Bewertungen + Testprofile + Testsendungen
* Journey-Validierung: Testmodus + Probelauf + Testprofile
* Checkliste vor dem Start: Alle technischen Tests + Konflikterkennung + Validierungs-Workflows

+++

>[!TAB Häufige Fragen]

+++**F: Welche Tests sind erforderlich, bevor eine Kampagne gestartet wird?**

**Minimum:** Inhaltsvorschau mit Testprofilen + Spam-Score-Prüfung (E-Mail)
**Empfohlen:** + E-Mail-Rendering + Konflikterkennung + Genehmigungs-Workflow
**Best Practice:** + Tests von Beispieleingabedaten + Testlisten + A/B-Experiment (bei Optimierung)

+++

+++**F: Wie kann ich die Personalisierung testen, ohne viele Testprofile zu erstellen?**

**Primäre Lösung:** Verwenden von [Beispieleingabedaten](../using/test-approve/simulate-sample-input.md) mit CSV-/JSON-Dateien (unterstützt bis zu 30 Varianten)
**Alternative:** Erstellen Sie 3-5 repräsentative [Testprofile](../using/audience/creating-test-profiles.md) die wichtige Segmente abdecken.
**Lernwerkzeug:** Experimentieren Sie zuerst in [Personalisierungs-Playground](../using/personalization/personalize.md#playground)

+++

+++**F: Was ist der Unterschied zwischen Testmodus und Probelauf für Journey?**

**Testmodus:** Sendet Testprofile über Journey, Trigger-Aktionen tatsächlich, generiert Testnachrichten. Erfordert Entwurfs-Journey + -Namespace.
**Probelauf:** Verfolgt Ausführungspfade, ohne etwas zu senden. Funktioniert mit jedem Journey-Status. Keine Nachrichten gesendet, keine Aktionen ausgeführt.
**Gemeinsam verwenden** Testmodus für Nachrichtentests + Probelauf für logische Validierung = umfassende Abdeckung.

+++

+++**F: Kann ich Journey im Produktions-/Live-Status testen?**

**Testmodus:** Nein - nur Entwurfs-Journey
**Probelauf:** Ja - funktioniert mit jedem Journey-Status
**Inhaltsvorschau:** Ja - Sie können jederzeit eine Vorschau einzelner Nachrichten anzeigen.
**Problemumgehung:** Duplizieren von Live-Journey zum Entwurf für die vollständige Testmodusvalidierung

+++

+++**F: Welche Testfunktionen erfordern externe Integrationen?**

**E-Mail-Rendering:** erfordert Litmus-Integration (separate Lizenz)
**Alle anderen:** In Journey Optimizer integriert, keine zusätzlichen Integrationen erforderlich
**Hinweis:** Testprofile erfordern den Echtzeit-Kundenprofil-Service (enthalten)

+++

+++**F: Wie kann ich API-ausgelöste Kampagnen testen?**

**Option 1:** Verwenden [Kampagnensimulations-API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} für programmatische Tests
**Option 2:** Vorschau des Inhalts mit Testprofilen in der Benutzeroberfläche
**Option 3:** Testsendungen an Test-E-Mail-Adressen durchführen
**Best Practice:** Alle drei für eine umfassende Validierung kombinieren

+++

>[!ENDTABS]
