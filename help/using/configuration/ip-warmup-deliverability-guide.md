---
solution: Journey Optimizer
product: journey optimizer
title: Handbuch zur IP-Aufwärmzustellbarkeit
description: Weitere Informationen über die Grundlagen der Zustellbarkeit und Best Practices für die IP-Aufwärmung
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, Zustellbarkeit, Reputation, ISP, Interaktion
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: ht
source-wordcount: '1064'
ht-degree: 100%

---

# Handbuch zur IP-Aufwärmzustellbarkeit {#ip-warmup-deliverability-guide}

Beim Starten von E-Mail-Kampagnen mit neuen IP-Adressen oder Domains in Adobe Journey Optimizer sind die Grundlagen der Zustellbarkeit von entscheidender Bedeutung für den Aufbau einer guten Reputation der Absendenden. In diesem Handbuch werden die wichtigsten Konzepte, Vorbereitungsschritte und Best Practices behandelt, die Ihnen beim Übergang von keiner Reputation zu einer erfolgreichen Platzierung im Posteingang helfen.

➡️ Weitere Informationen über die Grundlagen der Zustellbarkeit, das Aufbauen einer guten Reputation und Best Practices für die IP-Aufwärmung finden Sie im Video in diesem [Adobe-Blogpost](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950){target="_blank"}.

>[!NOTE]
>
>Eine schrittweise Anleitung zur Implementierung von IP-Aufwärmplänen in Adobe Journey Optimizer finden Sie unter [Erste Schritte mit IP-Aufwärmplänen](ip-warmup-gs.md).

## Darum sind IP- und Domain-Reputation wichtig {#reputation-matters}

Postfachanbieter (Gmail, Yahoo, Microsoft, Apple Mail und andere) bewerten jede Absenderin und jeden Absender anhand von vier wichtigen Säulen:

* **Beschwerden:** Haben Empfangende Ihre Nachrichten als Spam gekennzeichnet?
* **Interaktion:** Öffnen und beantworten Empfangende Ihre E-Mails bzw. klicken sie sie an?
* **Infrastruktur:** Ist Ihre Versandinfrastruktur authentifiziert, stabil und vertrauenswürdig?
* **Inhalt:** Erscheint der Inhalt Ihrer Nachricht rechtmäßig und wertvoll?

IP-Aufwärmung bezieht sich in erster Linie auf die ersten drei Säulen, indem Mailbox-Anbietern schrittweise gezeigt wird, dass Ihre neue Infrastruktur legitim und erwünscht ist, bevor Sie auf das gesamte Versandvolumen skalieren.

## Checkliste vor dem Start {#pre-flight-checklist}

Bevor Sie mit dem Aufwärmen Ihrer IP-Adressen beginnen, stellen Sie sicher, dass alle grundlegenden Elemente vorhanden sind. In der folgenden Tabelle sind die wichtigsten Aufgaben aufgeführt, die vor dem Starten Ihres IP-Aufwärmplans ausgeführt werden müssen.

| Aufgabe | Warum dies wichtig ist | Umsetzung |
|------|----------------|-------------------|
| Reservieren fester IP(s) und Delegieren von Subdomains in AJO | Jegliche zukünftige Reputation hängt mit diesen Infrastrukturelementen zusammen. | Navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Subdomains]**. [Weitere Informationen](delegate-subdomain.md) |
| Konfigurieren von SPF und DKIM | Bestätigt, dass der Versand-Server legitim und autorisiert ist. | Wird von Adobe nach der [Subdomain-Delegierung](delegate-subdomain.md) und [Erstellung der Kanalkonfiguration](channel-surfaces.md) automatisch verarbeitet. |
| Sicherstellen, dass der DMARC-Eintrag konfiguriert ist (p=none) | Aktiviert das Reporting zur E-Mail-Authentifizierung und zukünftige Durchsetzungsrichtlinien. | Überprüfen Sie, ob für alle delegierten Subdomains ein DMARC-Eintrag eingerichtet ist. Wenn Sie eine neue Subdomain delegieren, können Sie DMARC direkt in der Benutzeroberfläche einrichten. [Weitere Informationen](dmarc-record.md) |
| Konfigurieren der Überwachung der Testadressenliste | Erkennt Platzierungsprobleme im Posteingang frühzeitig im Aufwärmprozess. | Fügen Sie bei der Erstellung Ihrer Kanalkonfiguration Testadressen hinzu. [Weitere Informationen](seed-lists.md) |
| Erstellen einer Zielgruppe mit hoher Interaktion in Phase 1 | Steigert die Interaktionsmetriken für die aktivsten Empfangenden. | Erstellen Sie eine Zielgruppe mit weniger als 5.000 Kontakten, die in den letzten 30 Tagen geöffnet oder geklickt haben. [Weitere Informationen](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Authentifizierungsprobleme (SPF, DKIM, DMARC) können nicht durch Steigerung des Volumens gelöst werden. Stellen Sie sicher, dass diese korrekt konfiguriert sind, bevor Sie mit dem Versand beginnen.

## Beispiel für vierwöchigen Aufwärmkalender {#warmup-calendar}

Dieser Beispielkalender bietet eine progressive Volumensteigerung basierend auf dem Prozentsatz Ihres endgültigen Tagesvolumens (UDV). Passen Sie diese Zahlen an Ihre spezifischen Versandanforderungen an und erstellen Sie gemeinsam mit Ihrer Beratungsfachkraft für Zustellbarkeit einen individuellen Plan.

| Tage | % des UDV | Zielgruppe | Inhaltsempfehlungen |
|------|----------|-----------------|------------------------|
| 1–3 | 0,5 % | Ihre aktivsten Empfängerinnen und Empfänger | Verwenden Sie ein kurzes, einfaches Textformat mit einem deutlichen Handlungsaufruf im sichtbaren Bereich. |
| 4–7 | 1 % | Benutzende mit hoher Interaktion und Personen, die kürzlich etwas gekauft haben | Fügen Sie ein schlankes Hero Image hinzu, begrenzen Sie Links auf höchstens 3. |
| 8–14 | 5 % | Erweiterte Liste aktiver Abonnentinnen und Abonnenten | Nutzen Sie Ihre Standard-E-Mail-Vorlage, vermeiden Sie jedoch umfangreiche Werbeinhalte. |
| 15–21 | 25 % | Aktive und geringfügig inaktive Abonnentinnen und Abonnenten | Nutzen Sie normale Marketing-Inhalte und überwachen Sie gleichzeitig die Beschwerderate genau. |
| 22–28 | 50–100 % | Vollständige Liste (unter Berücksichtigung der Unterdrückungslisten) | Gehen Sie zu Ihrer dauerhaften Versandkadenz über. |

## Verwenden der Funktion „IP-Aufwärmpläne“ {#ajo-warmup-feature}

Adobe Journey Optimizer enthält eine optimierte Funktion [IP-Aufwärmpläne](ip-warmup-gs.md), mit der die Notwendigkeit manueller Volumenbegrenzungen durch komplexe Journey-Setups entfällt. Diese Funktion stellt einen standardisierten Ansatz zum Aufbau der Reputation von Absendenden sicher.

### Funktionsweise

1. **Erstellen von IP-Aufwärmkampagnen:** Erstellen Sie eine oder mehrere Kampagnen mit aktivierter Option **[!UICONTROL Aktivierung des IP-Aufwärmplans]**. [Weitere Informationen](ip-warmup-campaign.md)

1. **Einrichten des Plans:** Greifen Sie auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL IP-Aufwärmpläne]** zu und laden Sie die mit Ihrer Beratungsfachkraft für Zustellbarkeit vorbereitete Vorlage für die Aufwärmung in Phasen hoch. [Weitere Informationen](ip-warmup-plan.md)

1. **Ausführen der Phasen:** Wählen Sie für jede Phase eine Kampagne aus und aktivieren Sie die entsprechenden Ausführungen. Das System schließt automatisch Profile aus vorherigen Ausführungen aus, um eine Überkontaktierung zu vermeiden. [Weitere Informationen](ip-warmup-execution.md)

1. **Überwachen und Anpassen:** Verwenden Sie das Dashboard für konsolidiertes Reporting, um den Fortschritt zu verfolgen, den Ausführungsstatus zu überwachen und Ihren Plan bei Problemen zu ändern. [Weitere Informationen](ip-warmup-execution.md#monitor-plan)

## Echtzeit-Überwachung und Schlüsselmetriken {#monitoring}

Adobe Journey Optimizer bietet integrierte Reporting-Funktionen zur Nachverfolgung der IP-Aufwärmleistung:

* **Live-Berichte:** Greifen Sie über die Registerkarte **[!UICONTROL Letzte 24 Std.]** auf Echtzeit-Messungen und Visualisierungen Ihrer Kampagnen zu. [Weitere Informationen](../reports/campaign-live-report.md#email-live)

* **Berichte für die gesamte Zeit:** Nutzen Sie Customer Journey Analytics, um Daten aus Adobe Experience Platform zu analysieren und benutzerdefinierte Visualisierungen zu erstellen, um detailliertere Erkenntnisse zu gewinnen. [Weitere Informationen](../reports/report-gs-cja.md)

### Zielmetriken

Überwachen Sie diese KPIs während der gesamten Aufwärmphase:

| Metrik | Zielschwellenwert | Korrekturmaßnahme |
|--------|-----------------|-------------------|
| Beschwerderate | ≤ 0,1 % | Bei Überschreitung Segment prüfen und chronische Beschwerden unterdrücken. |
| Hardbounce-Rate | ≤ 2 % | Bei Überschreitung Listenqualität und Hygienemaßnahmen prüfen. |
| Öffnungsrate | ≥ 10 % | Wenn zu niedrig, prüfen, ob Sie interaktive Zielgruppen ansprechen. |

## Playbook zur Fehlerbehebung {#troubleshooting}

Verwenden Sie diese Entscheidungsmatrix, um häufige Probleme während der Aufwärmphase zu beheben:

| Symptom | Wahrscheinliche Ursache | Empfohlene Aktion |
|---------|--------------|-------------------|
| Vorübergehende Yahoo-Fehler (Fehler 421) | Volumen zu schnell erhöht | Versand 24 Stunden aussetzen und dann auf der vorherigen Ebene neu starten. |
| Öffnungsrate unter 2 % für Testversandkonten | IP-Blockierungslisten | [Google Postmaster Tools](https://postmaster.google.com/) und [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/) prüfen; bei Bedarf ein Zustellbarkeits-Ticket übermitteln. |
| Beschwerderate übersteigt 0,3 % | Falsch angesprochene oder veraltete Zielgruppe | Segmentdefinitionen prüfen und Personen, die sich häufig beschweren, über die [Unterdrückungsliste](manage-suppression-list.md) ausschließen. |

>[!IMPORTANT]
>
>Verlangsamen Sie lieber das Aufwärmen, anstatt später eine beschädigte Absenderreputation reparieren zu müssen. Priorisieren Sie stets die Aufrechterhaltung intakter Metriken über eine aggressive Volumensteigerung.

## Best Practices nach dem Aufwärmen {#post-warmup}

Gehen Sie wie folgt vor, sobald Sie Ihren Aufwärmplan abgeschlossen haben und sich die Metriken stabilisiert haben:

* **Wahrung der Konsistenz:** Die tägliche Volumensteigerung sollte im Wochenvergleich unter 30 % liegen, um Ihre Reputation zu wahren.

* **Fortlaufende Überwachung:** Planen Sie vierteljährliche Statusprüfungen hinsichtlich der Reputation, um Probleme proaktiv zu identifizieren und zu beheben.

* **Respektieren der Interaktionssignale:** Priorisieren Sie interaktive Empfängerinnen und Empfänger weiterhin und implementieren Sie Kampagnen zur Wiederaufnahme der Interaktion für inaktive Abonnentinnen und Abonnenten.

* **Aktualisieren der Authentifizierung:** Überprüfen Sie regelmäßig, ob Ihre SPF-, DKIM- und DMARC-Einträge ordnungsgemäß konfiguriert bleiben.

## Wichtige Schlussfolgerungen {#key-takeaways}

* **IP-Aufwärmphase ist essenziell:** Das Überspringen des Aufwärmvorgangs kostet mehr Zeit und Reputation als der Aufwand, ihn ordnungsgemäß durchzuführen.

* **Datengestützte Entscheidungen:** Verfolgen Sie Beschwerde-, Bounce- und Interaktionsraten täglich nach und passen Sie Ihre Strategie an, bevor die ISPs Sie bestrafen.

* **Authentifizierung vor Volumen:** Lösen Sie alle SPF-, DKIM- und DMARC-Probleme, bevor Sie mit der Steigerung des Volumens beginnen.

* **Konsistenz ist entscheidend:** Postfachanbieter bevorzugen vorhersehbare Versandmuster. Vermeiden Sie plötzliche Volumenspitzen oder unregelmäßige Versandzeitpläne.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## Verwandte Themen {#related-topics}

* [Erste Schritte mit IP-Aufwärmplänen](ip-warmup-gs.md)
* [Erstellen von IP-Aufwärmkampagnen](ip-warmup-campaign.md)
* [Erstellen eines IP-Aufwärmplans](ip-warmup-plan.md)
* [Ausführen des IP-Aufwärmplans](ip-warmup-execution.md)
* [Einrichten von Kanalkonfigurationen](channel-surfaces.md)
* [Delegieren von Subdomains](delegate-subdomain.md)
* [Verwalten der Unterdrückungsliste](manage-suppression-list.md)
* [Handbuch mit Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de)

