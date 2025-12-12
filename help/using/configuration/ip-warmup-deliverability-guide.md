---
solution: Journey Optimizer
product: journey optimizer
title: Leitfaden zur Zustellbarkeit von IP-Aufwärmung
description: Erfahren Sie mehr über die Grundlagen der Zustellbarkeit und Best Practices für die IP-Aufwärmung
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, Zustellbarkeit, Reputation, ISP, Interaktion
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 6%

---

# Leitfaden zur Zustellbarkeit von IP-Aufwärmung {#ip-warmup-deliverability-guide}

Beim Starten von E-Mail-Kampagnen mit neuen IP-Adressen oder Domains in Adobe Journey Optimizer sind die Grundlagen der Zustellbarkeit von entscheidender Bedeutung für den Aufbau einer guten Reputation bei Absendern. In diesem Handbuch werden die wichtigsten Konzepte, Vorbereitungsschritte und Best Practices behandelt, die Ihnen beim Übergang von der Reputation auf eine erfolgreiche Platzierung im Posteingang helfen.

➡️ Erfahren Sie in diesem [Adobe-Blogpost&rbrace; im Video mehr über die Grundlagen der Zustellbarkeit, die Schaffung einer guten Reputation und Best Practices für die IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950){target="_blank"}Aufwärmung.

>[!NOTE]
>
>Eine schrittweise Anleitung zur Implementierung von IP-Aufwärmplänen in Adobe Journey Optimizer finden Sie unter [Erste Schritte mit IP-Aufwärmplänen](ip-warmup-gs.md).

## Warum IP- und Domain-Reputation wichtig sind {#reputation-matters}

Postfachanbieter (Gmail, Yahoo, Microsoft, Apple Mail und andere) bewerten jeden Absender anhand von vier wichtigen Säulen:

* **Beschwerden**: Haben Empfänger Ihre Nachrichten als Spam gekennzeichnet?
* **Interaktion**: Öffnen, klicken oder beantworten Empfänger Ihre E-Mails?
* **Infrastruktur**: Ist Ihre sendende Infrastruktur authentifiziert, stabil und vertrauenswürdig?
* **Inhalt**: Erscheint der Inhalt Ihrer Nachricht rechtmäßig und wertvoll?

IP-Aufwärmung bezieht sich in erster Linie auf die ersten drei Säulen, indem Mailbox-Anbietern schrittweise gezeigt wird, dass Ihre neue Infrastruktur legitim und erwünscht ist, bevor Sie auf das gesamte Versandvolumen skalieren.

## Checkliste vor dem Flug {#pre-flight-checklist}

Bevor Sie mit dem Aufwärmen Ihrer IP-Adressen beginnen, stellen Sie sicher, dass alle grundlegenden Elemente vorhanden sind. In der folgenden Tabelle sind die wichtigsten Aufgaben aufgeführt, die vor dem Starten Ihres IP-Aufwärmplans ausgeführt werden müssen.

| Aufgabe | Warum dies wichtig ist | Vorgehensweise |
|------|----------------|-------------------|
| Feste IP(s) reservieren und Subdomains in AJO delegieren | Alle zukünftigen Reputationen hängen mit diesen Infrastrukturelementen zusammen. | Navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL Subdomains]**. [Weitere Informationen](delegate-subdomain.md) |
| Konfigurieren von SPF und DKIM | Bestätigt, dass der Versand-Server legitim und autorisiert ist. | Wird von Adobe nach der [Subdomain-Delegierung](delegate-subdomain.md) und [Erstellung der Kanalkonfiguration](channel-surfaces.md) automatisch verarbeitet. |
| Stellen Sie sicher, dass der DMARC-Eintrag konfiguriert ist (p=none) | Aktiviert das Reporting zur E-Mail-Authentifizierung und zukünftige Durchsetzungsrichtlinien. | Überprüfen Sie, ob für alle delegierten Subdomains ein DMARC-Eintrag eingerichtet ist. Beim Delegieren einer neuen Subdomain können Sie DMARC direkt auf der Benutzeroberfläche einrichten. [Weitere Informationen](dmarc-record.md) |
| Konfigurieren der Überwachung der Testadressenliste | Erkennt Platzierungsprobleme im Posteingang frühzeitig im Warmlaufprozess. | Fügen Sie bei der Erstellung Ihrer Kanalkonfiguration Testadressen hinzu. [Weitere Informationen](seed-lists.md) |
| Erstellen einer Audience mit hoher Interaktion in Phase 1 | Steigert die Interaktionsmetriken für die aktivsten Empfänger. | Erstellen Sie eine Zielgruppe von weniger als 5.000 Kontakten, die in den letzten 30 Tagen geöffnet oder geklickt haben. [Weitere Informationen](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Authentifizierungsprobleme (SPF, DKIM, DMARC) können nicht durch Volume-Ramping gelöst werden. Stellen Sie sicher, dass diese korrekt konfiguriert sind, bevor Sie mit dem Versand beginnen.

## Beispiel für vierwöchigen Aufwärmkalender {#warmup-calendar}

Dieser Beispielkalender bietet eine progressive Volumenrampe, die auf dem Prozentsatz Ihres endgültigen täglichen Volumens (UDV) basiert. Passen Sie diese Zahlen an Ihre spezifischen Versandanforderungen an und erstellen Sie gemeinsam mit Ihrem Zustellbarkeitsberater einen benutzerdefinierten Plan.

| Tage | % UDV | Zielgruppe | Inhaltsempfehlungen |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5 % | Ihre aktivsten Empfänger | Verwenden Sie ein kurzes, einfaches Textformat mit einer deutlichen call-to-action über dem Falz. |
| 4-7 | 1 % | Engagierte Benutzer und aktuelle Käufer | Fügen Sie ein leichtes Hero-Bild hinzu, begrenzen Sie Links auf 3 oder weniger. |
| 8-14 | 5 % | Erweiterte Liste aktiver Abonnenten | Stellen Sie Ihre Standard-E-Mail-Vorlage vor, vermeiden Sie jedoch umfangreiche Werbeinhalte. |
| 15-21 | 25 % | Aktive und leicht inaktive Abonnentinnen und Abonnenten | Nutzen Sie normale Marketing-Inhalte und überwachen Sie gleichzeitig die Beschwerderate genau. |
| 22-28 | 50-100 % | Vollständige Liste (unter Berücksichtigung der Unterdrückungslisten) | Übergang zu Ihrer Steady-State-Sendungskadenz. |

## Verwenden der IP-Aufwärmpläne-Funktion {#ajo-warmup-feature}

Adobe Journey Optimizer enthält eine optimierte Funktion [IP-Aufwärmpläne](ip-warmup-gs.md) mit der die Notwendigkeit manueller Volume-Begrenzungen durch komplexe Journey-Setups entfällt. Diese Funktion stellt einen standardisierten Ansatz zum Aufbau der Reputation des Absenders sicher.

### Funktionsweise

1. **Erstellen von IP-Aufwärmkampagnen**: Erstellen Sie eine oder mehrere Kampagnen mit aktivierter Option **[!UICONTROL Aktivierung]** IP-Aufwärmplans. [Weitere Informationen](ip-warmup-campaign.md)

1. **Richten Sie Ihren Plan ein**: Gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Einstellungen]** > **[!UICONTROL IP-Aufwärmpläne]** und laden Sie Ihre mit Ihrem Zustellbarkeitsberater vorbereitete Vorlage für die schrittweise Aufwärmung hoch. [Weitere Informationen](ip-warmup-plan.md)

1. **Phasen ausführen**: Wählen Sie für jede Phase eine Kampagne aus und aktivieren Sie die entsprechenden Ausführungen. Das System schließt Profile automatisch aus vorherigen Durchläufen aus, um eine Überkontaktierung zu vermeiden. [Weitere Informationen](ip-warmup-execution.md)

1. **Überwachen und Anpassen**: Verwenden Sie das Dashboard für konsolidierte Berichte, um den Fortschritt zu verfolgen, den Ausführungsstatus zu überwachen und Ihren Plan bei Problemen zu ändern. [Weitere Informationen](ip-warmup-execution.md#monitor-plan)

## Echtzeit-Überwachung und Schlüsselmetriken {#monitoring}

Adobe Journey Optimizer bietet integrierte Reporting-Funktionen zur Verfolgung der IP-Aufwärmleistung:

* **Live-Berichte**: Greifen Sie über die Registerkarte &quot;**[!UICONTROL 24 Stunden“ auf die Echtzeit-Messung]** Visualisierung Ihrer Kampagnen zu. [Weitere Informationen](../reports/campaign-live-report.md#email-live)

* **Alle Zeitberichte**: Nutzen Sie Customer Journey Analytics, um Daten aus Adobe Experience Platform zu analysieren und benutzerdefinierte Visualisierungen zu erstellen. [Weitere Informationen](../reports/report-gs-cja.md)

### Zielmetriken

Überwachen Sie diese wichtigen Leistungsindikatoren während Ihrer gesamten Aufwärmphase:

| Metrik | Zielschwellenwert | Korrekturmaßnahmen |
|--------|-----------------|-------------------|
| Beschwerderate | ≤ 0,1 % | Bei Überschreitung Segment prüfen und chronische Beschwerden unterdrücken. |
| Hardbounce-Rate | ≤ 2 % | Wenn sie überschritten wird, sollten Sie die Qualitäts- und Hygienemaßnahmen des Listeneintrags überprüfen. |
| Öffnungsrate | ≥ 10 % | Wenn dies zu niedrig ist, überprüfen Sie, ob Sie interaktive Zielgruppen ansprechen. |

## Fehlerbehebung im Playbook {#troubleshooting}

Verwenden Sie diese Entscheidungsmatrix, um häufige Probleme während der Aufwärmphase zu beheben:

| Symptom | Wahrscheinliche Ursache | Empfohlene Aktion |
|---------|--------------|-------------------|
| Vorübergehende Yahoo-Fehler (421 Fehler) | Volumen zu schnell erhöht | Senden für 24 Stunden pausieren und dann auf der vorherigen Ebene neu starten. |
| Öffnungsrate unter 2 % für Testkonten | IP-Blockierungsauflistung | Überprüfen Sie [Google Postmaster Tools](https://postmaster.google.com/) und [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/); öffnen Sie bei Bedarf ein Zustellbarkeits-Ticket. |
| Die Beschwerderate liegt über 0,3 % | Falsch angesprochene oder veraltete Zielgruppe | Prüfen Sie Segmentdefinitionen und schließen Sie chronische Beschwerdeführer von Ihrer [Unterdrückungsliste](manage-suppression-list.md) aus. |

>[!IMPORTANT]
>
>Es ist besser, das Aufwärmen zu verlangsamen, als später zu versuchen, eine beschädigte Absenderreputation zu reparieren. Achten Sie darauf, stets die Aufrechterhaltung einer intakten Metrik vor einer aggressiven Volumenzunahme zu priorisieren.

## Best Practices für die Zeit nach der Aufwärmung {#post-warmup}

Sobald Sie Ihren Aufwärmplan abgeschlossen haben und sich die Metriken stabilisiert haben:

* **Konsistenz wahren**: Die tägliche Volumenzunahme soll Woche für Woche unter 30 % liegen, um Ihre Reputation zu wahren.

* **Fortlaufende Überwachung**: Planen Sie vierteljährliche Zustandsprüfungen für die Reputation, um Probleme proaktiv zu identifizieren und zu beheben.

* **Interaktionssignale respektieren**: Interaktive Empfängerinnen und Empfänger weiterhin priorisieren und Kampagnen zur erneuten Interaktion für inaktive Abonnentinnen und Abonnenten implementieren.

* **Authentifizierung aktuell halten**: Überprüfen Sie regelmäßig, ob Ihre SPF-, DKIM- und DMARC-Datensätze ordnungsgemäß konfiguriert bleiben.

## Wichtige Erkenntnisse {#key-takeaways}

* **IP-Aufwärmphase ist essenziell**: Das Überspringen des Aufwärmvorgangs kostet mehr Zeit und Reputation als der Aufwand, um ihn ordnungsgemäß durchzuführen.

* **Datengestützte Entscheidungen**: Verfolgen Sie Beschwerde-, Bounce- und Interaktionsraten täglich und passen Sie Ihre Strategie an, bevor die ISPs Sie bestrafen.

* **Authentifizierung zuerst, zweiter Datenträger**: Lösen Sie alle SPF-, DKIM- und DMARC-Probleme, bevor Sie mit dem Anheben des Volumens beginnen.

* **Konsistenz ist wichtig**: Postfachanbieter bevorzugen vorhersehbare Versandmuster; vermeiden Sie plötzliche Volumenspitzen oder unregelmäßige Versandzeitpläne.

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
* [Best Practice-Handbuch zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de)

