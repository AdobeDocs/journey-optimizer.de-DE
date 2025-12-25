---
solution: Journey Optimizer
product: Journey Optimizer
title: Testen und Genehmigen
description: Testen und Genehmigen
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# Testen und Genehmigen{#section-overview}

Die Qualitätssicherung ist für die Bereitstellung außergewöhnlicher Kundenerlebnisse von entscheidender Bedeutung. Adobe Journey Optimizer bietet umfassende Test- und Validierungsfunktionen, mit denen Sie Inhalte validieren, die Journey-Logik überprüfen und sicherstellen können, dass Kampagnen die Qualitätsstandards erfüllen, bevor sie Ihre Audience erreichen. Von der Vorschau personalisierter Nachrichten mit Testprofilen bis zur Simulation komplexer Journey-Flüsse ermöglichen diese Tools die frühzeitige Erkennung und Lösung von Problemen, die Reduzierung von Risiken und die Aufrechterhaltung der Markenintegrität. Unabhängig davon, ob Sie das E-Mail-Rendering geräteübergreifend testen, mehrstufige Journey validieren oder formale Validierungs-Workflows einrichten, führt Sie dieser Abschnitt durch Best Practices und schrittweise Prozesse, um Vertrauen in Ihre Kampagnen und Journey zu schaffen. Durch die Implementierung gründlicher Tests und strukturierter Genehmigungen minimieren Sie Fehler, verbessern die Zustellbarkeit und erstellen nahtlose Erlebnisse, die bei Ihren Kunden Anklang finden.

## Warum Tests und Genehmigungen wichtig sind

Test- und Validierungsprozesse dienen als wichtige Qualitätsprüfungen, die den Ruf Ihrer Marke schützen und den Erfolg Ihrer Kampagnen sicherstellen. Hier ist, warum sie wichtig sind:

* **Fehler erkennen, bevor sie Kunden erreichen** - Identifizieren Sie fehlerhafte Links, falsche Personalisierung, Rendering-Probleme und Logikfehler in einer kontrollierten Umgebung, in der Korrekturen schnell und risikolos sind.

* **Zustellbarkeit verbessern** - Spam-Bewertungen testen, die E-Mail-Authentifizierung überprüfen und das Rendering auf allen E-Mail-Clients überprüfen, um die Platzierungs- und Interaktionsraten im Posteingang zu maximieren.

* **Markenkonsistenz sicherstellen** - Vorschau von Inhalten mit verschiedenen Testprofilen, um zu überprüfen, ob die Personalisierung für verschiedene Kundensegmente korrekt angezeigt wird und die Markenstandards einhält.

* **Validieren komplexer Journey** - Simulieren Sie mehrstufige Journey-Flüsse, um sicherzustellen, dass Trigger korrekt ausgelöst werden, Bedingungen ordnungsgemäß ausgewertet werden und Kunden die richtigen Nachrichten zur richtigen Zeit erhalten.

* **Verantwortlichkeit herstellen** - Implementieren formaler Genehmigungs-Workflows, die die Zustimmung der Stakeholder erfordern, wodurch eine klare Eigentümerschaft geschaffen und die Anzahl nicht autorisierter oder vorzeitiger Kampagnenstarts reduziert wird.

* **Zeit und Ressourcen sparen** - Erkennung von Problemen frühzeitig im Entwicklungszyklus, wenn Fehlerbehebungen billiger und schneller sind, wodurch kostspielige Korrekturen nach der Markteinführung oder Eskalationen beim Kundenservice vermieden werden.

## Best Practices für Tests

Befolgen Sie die folgenden empfohlenen Vorgehensweisen, um die Effektivität Ihrer Testaktivitäten zu maximieren:

1. **Früh und häufig testen** - Nicht warten, bis eine Kampagne vollständig erstellt ist. Testen Sie Inhalt, Personalisierung und Logik schrittweise während der Entwicklung.

1. **Verwenden realistischer Testprofile** - [Erstellen Sie Testprofile](../using/audience/creating-test-profiles.md) die Ihre Zielgruppensegmente genau darstellen, einschließlich Edge-Fällen und verschiedener Personalisierungsszenarien.

1. **Testen geräteübergreifend** - Überprüfen Sie [E-Mail-Rendering](../using/content-management/rendering.md) auf gängigen E-Mail-Clients (Gmail, Outlook, Apple Mail) und Geräten (Desktop, Mobile, Tablet), um eine konsistente Anzeige sicherzustellen.

1. **Personalisierung gründlich validieren** - Testen Sie mit mehreren [Testprofilen](../using/content-management/test-profiles.md) die unterschiedliche Attributwerte aufweisen, um zu bestätigen, dass Personalisierungs-Token korrekt gerendert werden und Fallback-Werte funktionieren.

1. **Journey-Pfade simulieren** - Verwenden Sie bei komplexen Journey mit mehreren Verzweigungen [Testmodus](../using/building-journeys/testing-the-journey.md), um verschiedene Einstiegsbedingungen und Profilattribute zu testen, um alle möglichen Pfade zu validieren.

1. **Zustellbarkeitsindikatoren überprüfen** - Überprüfen Sie [Spam-](../using/content-management/spam-report.md), den Authentifizierungsstatus und die Metriken zum E-Mail-Status vor großen Sendungen.

1. **Dokumentieren von Testergebnissen** - Führen Sie Aufzeichnungen über Testergebnisse, gefundene Probleme und Lösungen, um zukünftige Testprozesse zu verbessern, und tauschen Sie die Erkenntnisse mit Ihrem Team aus.

1. **frühzeitige Einbeziehung von Stakeholdern** - Teilen Sie Vorschauen und Testergebnisse mit Stakeholdern, bevor [formelle Genehmigung](../using/test-approve/gs-approval.md) erfolgt, um Feedback zu sammeln und Erwartungen abzustimmen.

## Empfohlener Test-Workflow

Folgen Sie diesem systematischen Ansatz, um gründliche Tests und reibungslose Genehmigungen sicherzustellen:

### &#x200B;1. Inhaltsentwicklung und -vorschau

Erstellen Sie zunächst Ihren Inhalt und verwenden Sie die Vorschaufunktionen, um das anfängliche Design und die Personalisierung zu überprüfen:

* Gestalten Sie Ihre [E](../using/email/create-email.md), [SMS](../using/sms/create-sms.md), [Push-Benachrichtigung](../using/push/create-push.md) oder anderen Kanalinhalt
* Verwenden der **[Inhalt simulieren](../using/content-management/preview-test.md)** für die Vorschau mit Testprofilen
* Überprüfen [Personalisierungs-Token](../using/personalization/personalization-syntax.md), dynamischen Inhalte und Fallback-Werte
* Überprüfen [Rendering](../using/content-management/rendering.md) über verschiedene Bildschirmgrößen und E-Mail-Clients hinweg

### &#x200B;2. Technische Validierung

Validieren Sie technische Aspekte, die sich auf Zustellbarkeit und Funktionalität auswirken:

* Führen Sie [Spam-Score-Prüfungen](../using/content-management/spam-report.md) aus, um potenzielle Probleme mit der Zustellbarkeit zu identifizieren
* Testen Sie Links, um sicherzustellen, dass sie nicht beschädigt sind, und verfolgen Sie sie ordnungsgemäß
* Konfiguration [E-Mail-Authentifizierung](../using/configuration/dmarc-record.md) (SPF, DKIM, DMARC) überprüfen
* Überprüfen des HTML-Renderings und Überprüfen der CSS-Kompatibilität
* Testen [responsiven Designs](../using/email/content-from-scratch.md) auf mobilen und Desktop-Geräten

### &#x200B;3. Journey-Prüfung

Validieren Sie für Journey die Orchestrierungslogik:

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

* **[Senden von Multi-Channel-Nachrichten](../using/building-journeys/journeys-uc.md)** - Dieser Anwendungsfall zeigt, wie Sie eine Journey testen, die „Zielgruppe lesen“, Reaktionsereignisse und E-Mail-/Push-Nachrichten kombiniert. Erfahren Sie, wie Sie den gesamten Fluss von der Zielgruppenbestimmung bis zum Nachrichtenversand validieren, und sehen Sie sich die Schritte zum Testen und Veröffentlichen in Aktion an.

* **[Nachricht an Abonnenten senden](../using/building-journeys/message-to-subscribers-uc.md)** - Erfahren Sie, wie Sie Journey testen können, die Abonnementlisten mit dynamischer E-Mail-Adressierung ansprechen. In diesem Beispiel wird gezeigt, wie Personalisierungsausdrücke validiert werden können und wie sichergestellt werden kann, dass Nachrichten die richtigen Abonnenten erreichen.

* **[Senden von zeitgebundenen Nachrichten](../using/building-journeys/weekday-email-uc.md)** - Erfahren Sie, wie Sie Journey mit zeitbasierten Bedingungen testen können, um sicherzustellen, dass Nachrichten an bestimmten Tagen gesendet werden. Siehe Validieren von Warteaktivitäten und Planungslogik.

* **[Weitere Journey-Anwendungsfälle](../using/building-journeys/jo-use-cases.md)** - Greifen Sie auf eine umfassende Sammlung praktischer Beispiele zu, die Erlebnisereignisse, Multi-Channel-Messaging und externe Systemintegrationen abdecken.

## Testen und Genehmigen von Inhalten

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=de)

Vorschau, Testen und Validieren von Inhalten

Erfahren Sie, wie Sie personalisierte Inhalte mithilfe von Testprofilen, E-Mail-Render-Tests, Spam-Bewertungen und mehr in der Vorschau anzeigen, testen und validieren können.

[Vorschau und Testen der Inhalte erkunden](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=de)

Validierungs-Workflows für Journeys und Kampagnen

Erfahren Sie, wie Sie Validierungsprozesse einrichten, verwalten und ausführen, um eine Qualitätskontrolle für Journeys und Kampagnen sicherzustellen.

[Informationen zu Validierungs-Workflows](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=de)

Testen der Journey

Validieren Sie Ihre Journey vor der Veröffentlichung, indem Sie sie mit bestimmten Profilen testen, um sicherzustellen, dass Ereignisse, Bedingungen und Aktionen erwartungsgemäß funktionieren.

[Journey testen](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=de)

Journey-Probelauf

Führen Sie einen Probelauf durch, um Ihren Journey-Ausführungspfad zu simulieren und zu validieren und potenzielle Probleme zu identifizieren, bevor Sie live gehen.

[Informationen zu Journey-Probeläufen](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=de)

Monitoring und Fehlerbehebung

Zugriff auf umfassende Ressourcen zur Fehlerbehebung, Systemwarnungen und Fehler-Codes zur Behebung von Journey-Ausführungs- und Leistungsproblemen.

[Monitoring und Fehlerbehebung anzeigen](troubleshoot-journey-landing-page.md)
:::

::::

## Weitere Ressourcen

### Grundlegende Test- und Validierungshandbücher

* [Live-Bericht auf Ihrem Journey](../using/building-journeys/report-journey.md) - Überwachen Sie Journey-Metriken in Echtzeit, um die Leistung zu verfolgen und Probleme während der Ausführung zu identifizieren. Zugriff auf detaillierte Aufschlüsselungen des Profilfortschritts, der Ereignis-Trigger und der Aktionsabschlussraten.

* [Erstellen von Testprofilen](../using/audience/creating-test-profiles.md) - Erstellen und verwalten Sie Testprofile, um echte Kundenszenarien zu simulieren und die Personalisierung zu validieren. Erfahren Sie, wie Sie Profile für Tests kennzeichnen, Attributwerte festlegen und Testprofilsegmente organisieren.

* [E-Mail-Spam-Bericht](../using/content-management/spam-report.md) - Überprüfen Sie Ihre E-Mail-Spam-Punktzahl vor dem Versand, um die Zustellbarkeit und die Platzierung im Posteingang zu verbessern. Erfahren Sie, wie Spam-Filter Ihre Inhalte auswerten und erhalten Sie Empfehlungen zur Verbesserung.

* [Häufig gestellte Fragen zum Journey](../using/building-journeys/journey-faq.md) - Hier finden Sie Antworten auf häufig gestellte Fragen zur Erstellung, zum Testen, zur Ausführung und zur Fehlerbehebung von Journey. Kurzanleitung zur Behebung häufiger Probleme und zum Verständnis des Journey-Verhaltens.

### Verwandte Themen

* [Content-Management](content-management-landing-page.md) - Erfahren Sie, wie Sie Inhalte mithilfe von Vorlagen, Fragmenten und der E-Mail-Designer entwerfen, in der Vorschau anzeigen und verwalten. Übergeordnete Best Practices für die Inhaltserstellung für konsistentes Branding

* [Reporting und &#x200B;](reporting-landing-page.md): Analysieren der Kampagnen- und Journey-Performance mit umfassenden Berichten, Dashboards und Metriken. Treffen von datengesteuerten Entscheidungen zur Optimierung von Kundenerlebnissen.

* [Journey-Konfiguration](configure-journeys-landing-page.md) - Konfigurieren von Datenquellen, Ereignissen und benutzerdefinierten Aktionen, um eine ausgefeilte Journey-Orchestrierung zu ermöglichen. Einrichten der technischen Grundlagen für die Erstellung von Journey.

* [Kampagnenverwaltung](../using/campaigns/get-started-with-campaigns.md) - Erfahren Sie mehr über die verschiedenen Kampagnentypen und darüber, wie Sie Batch- und Echtzeit-Kampagnen erstellen, planen und optimieren können, um eine maximale Wirkung zu erzielen.
