---
solution: Journey Optimizer
product: journey optimizer
title: Artikel zur Fehlerbehebung in Journey Optimizer
description: Artikel zur Fehlerbehebung in Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: c9fd0aeda42f8833a542ecafae8c60aaebde4ef0
workflow-type: tm+mt
source-wordcount: '2942'
ht-degree: 99%

---

# Häufig gestellte Fragen zur Fehlerbehebung {#ajo-troubleshooting}

Im Folgenden finden Sie eine Liste von Artikeln zur Fehlerbehebung in Adobe Journey Optimizer. Jeder Abschnitt zur Fehlerbehebung enthält Antworten auf häufig gestellte Fragen und Lösungen für Probleme.

Siehe auch [Dokumentation mit häufig gestellten Fragen und Fehlerbehebung für Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/landing/troubleshooting){target="_blank"}.

## E-Mail-Kanal {#ajo-troubleshooting-email}

+++ Wie lassen sich E-Mail-Formatierungsprobleme in Adobe Journey Optimizer mithilfe von Themen verhindern?

In Adobe Journey Optimizer (AJO) kann die Änderung der standardmäßigen CSS-Blöcke im E-Mail-Header zu unerwarteten Formatierungsproblemen führen – insbesondere nach dem Entfernen von Inhaltsfragmenten. Solche Probleme treten auf Mobilgeräten deutlicher zutage und können zu Layout-Verschiebungen oder Inkonsistenzen bei der Formatierung führen. Um dies zu verhindern, verwenden Sie die Funktion „Themen“, um benutzerdefiniertes CSS sicher anzuwenden, ohne die vom System generierten CSS-Stile zu ändern.

Weitere Informationen zur Behebung dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}.

Weitere Informationen zur E-Mail-Formatierung finden Sie auf [dieser Seite](../email/get-started-email-design.md).

+++


+++ Warum funktionieren Fragmente mit bearbeitbaren Feldern nicht?

In Adobe Journey Optimizer werden Fragmente mit bearbeitbaren Feldern möglicherweise nicht korrekt geladen oder unerwartet dupliziert, wenn sie zu Vorlagen hinzugefügt werden. Das Problem betrifft normalerweise bestimmte Fragmente in allen Umgebungen.

Weitere Informationen zur Behebung dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}.

Weitere Informationen zu benutzerdefinierten Fragmenten finden Sie [auf dieser Seite](../content-management/customizable-fragments.md).

+++

+++ Warum werden HTML-Fragmente in E-Mails nicht richtig angezeigt?

HTML-Fragmente werden in E-Mails ggf. nicht ordnungsgemäß gerendert und in vielen Fällen als **Fragment-IDs** anstatt als tatsächlicher Content angezeigt. Im Gegensatz zu visuellen Fragmenten müssen HTML-Fragmente sorgfältig konfiguriert werden. Um dieses Problem zu beheben, befolgen Sie in Ihren E-Mail-Kampagnen Best Practices für die Verwendung von **visuellen und HTML-Ausdrucksfragmenten**.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"}.

Weitere Informationen zu HTML-Fragmenten finden Sie [auf dieser Seite](../content-management/fragments.md).

+++

+++ Warum verschwinden E-Mail-Vorlagen und Inhalte aus unveröffentlichten Journeys?

Beim Bearbeiten von E-Mail-Vorlagen in einer unveröffentlichten Journey können die Inhalte und Vorlagen bestimmter E-Mails unerwartet verschwinden. Dies kann zu Überarbeitungsbedarf und Verzögerungen führen. Um das Risiko für das Auftreten dieses Problems zu verringern, vermeiden Sie gleichzeitige Bearbeitungen, begrenzen Sie die Anzahl der geöffneten Registerkarten und speichern Sie Änderungen regelmäßig.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Weitere Informationen zu Vorlagen finden Sie [auf dieser Seite](../email/use-email-templates.md).

+++

+++ Warum wird im Modus „Eigenen Code schreiben“ das Feld „E-Mail-Preheader“ nicht angezeigt? 

Im Modus **Eigenen Code schreiben** wird unter der Funktion **E-Mail-Text bearbeiten** das Eingabefeld „Preheader“ nicht angezeigt. Um Preheader-Text einzuschließen, müssen Benutzende **den Preheader mit ihrem benutzerdefinierten HTML-Content manuell codieren**.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"}.

[Auf dieser Seite](../email/header-parameters.md) erfahren Sie mehr über die Konfiguration von E-Mail-Preheadern.

+++

+++ Warum gibt es bei der Verwendung einer HTML-Komponente in E-Mail-Vorlagen eine Diskrepanz im Link-Verhalten?  

Beim Hinzufügen einer **HTML-Komponente** zu einer E-Mail-Vorlage verhalten sich Links je nach **E-Mail-Client**, **Anzeigemodus** oder **Gerät/Browser** unterschiedlich. Anker-Links zum Beispiel können in der **Nebeneinander-Ansicht von Outlook** anders funktionieren als in der Vollbildansicht. Beachten Sie diese Unterschiede beim Gestalten von E-Mail-Vorlagen und beim Testen über verschiedene Clients und Geräte hinweg.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"}.

Siehe auch Best Practices zur Gestaltung von E-Mails [auf dieser Seite](../email/get-started-email-design.md).

+++


+++ Wie kann man verhindern, dass in Berichten E-Mail-Tracking-Links fehlen?

Fehlendes Linktracking in Adobe Journey Optimizer tritt auf, wenn E-Mail-URLs dynamische Variablen verwenden und nicht mit „http“ beginnen oder wenn Logikanweisungen im URL-Feld platziert werden. Um dieses Problem zu beheben, stellen Sie sicher, dass alle URLs mit „http“ beginnen, vermeiden Sie die Verwendung von Logik im URL-Feld und verschieben Sie komplexe Personalisierungslogik in die HTML-Inhalte oder vorverarbeiteten Attribute.


Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}.

Weitere Informationen zum E-Mail-Tracking finden Sie auf [dieser Seite](../email/message-tracking.md).

+++

+++ Wie behebe ich beim Einrichten von per API ausgelösten Transaktions-E-Mail-Kampagnen einen Mail Exchanger-Fehler? 

Wenn beim Erstellen einer Kanalkonfiguration für eine per API ausgelöste Transaktions-E-Mail-Kampagne in Adobe Journey Optimizer ein MX-Fehler (Mail Exchanger) auftritt, kann dies auf **DNS-Fehlkonfigurationen** oder **DMARC-Einschränkungen** zurückzuführen sein. Um dieses Problem zu beheben, stellen Sie sicher, dass Ihr DNS korrekt konfiguriert ist, und vergewissern Sie sich, dass Ihre Domain die Anforderungen an **Domain-based Message Authentication, Reporting, and Conformance (DMARC)** erfüllt.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"}.

[Auf dieser Seite](../configuration/dmarc-record-update.md) erfahren Sie mehr über DMARC-Richtlinien für E-Mails.

Siehe auch [Dokumentation zu per API ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md).
+++

## Push-Kanal {#ajo-troubleshooting-push}

+++ Kann ein Profil in Adobe Journey Optimizer verschiedene Push-Token aufweisen?

Bei der Implementierung von Push-Benachrichtigungen in Journey Optimizer können einem einzelnen Profil tatsächlich verschiedene Push-Token mit unterschiedlichen Geräten zugeordnet sein. Bei einer Push-Benachrichtigungskampagne verwaltet Journey Optimizer diese Token und stellt sicher, dass das Zielgruppenprofil über alle zugehörigen Geräte erreicht werden kann.

Weitere Informationen zur Verwaltung von Push-Token finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}.

Weitere Informationen zur Push-Konfiguration finden Sie auf [dieser Seite](../push/push-configuration.md).

+++

+++ Warum werde ich beim Klicken auf eine Push-Nachricht nicht zur konfigurierten Web-URL umgeleitet?  

Wenn Push-Benachrichtigungen nicht zur vorgesehenen Web-URL umleiten, kann dies an einer falschen Konfiguration der Klickaktion oder an deaktivierten Einstellungen für Push-Benachrichtigungen liegen. Stellen Sie sicher, dass die **Klickaktion** für die Push-Benachrichtigung korrekt eingestellt ist und dass **automatische Anzeige und Tracking** von Push-Benachrichtigungen aktiviert sind, um das Problem zu beheben.

Weitere Informationen zu diesem Problem finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"}.

Weitere Informationen zur Push-Konfiguration finden Sie auf [dieser Seite](../push/push-configuration.md).

+++


## SMS-Kanal {#ajo-troubleshooting-sms}

+++ Warum werden meine Transaktions-SMS nicht zugestellt, obwohl das Einverständnis auf `marketing.sms.value=y` gesetzt ist?

Wenn eine Empfängerin bzw. ein Empfänger auf eine SMS mit **STOPP** antwortet, werden alle zukünftigen Nachrichten von dieser kurzen Nummer blockiert – einschließlich Transaktionsnachrichten. Um einen unterbrechungsfreien Versand von Transaktions-SMS zu gewährleisten, konfigurieren und senden Sie sie über eine **separate kurze Nummer**, von der sich die Empfängerinnen und Empfänger noch nicht abgemeldet haben.

Weitere Informationen zu diesem Problem finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"}.

[Auf dieser Seite](../sms/sms-opt-out.md) erfahren Sie mehr über die Opt-out-Konfiguration für SMS-Nachrichten.

+++

## In-App-Kanal

+++ Warum kann ich keine Berichte zum In-App-Kanal in Customer Journey Analytics erstellen?

Probleme beim Reporting für den **In-App-Kanal** in Adobe Customer Journey Analytics hängen oft mit falsch konfigurierten **Datenansichten**, **Datensätzen** oder **Schemaaktualisierungen** zusammen. Stellen Sie sicher, dass diese Konfigurationen korrekt angewendet sind, um das Problem zu beheben.

Weitere Informationen zu diesem Problem finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"}.

Weitere Informationen zur Integration von Journey Optimizer Analytics-Daten in Customer Journey Analytics finden Sie [auf dieser Seite](https://experienceleague.adobe.com/de/docs/analytics-platform/using/integrations/ajo#automatically-configure-journey-optimizer-integration){target="_blank"}.

Siehe auch [Dokumentation zu Berichten für die gesamte Zeit in Journey Optimizer](../reports/report-gs-cja.md).

+++


## Daten-Management {#ajo-troubleshooting-data-management}

+++ Wie werden TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet, wenn Sie eine neue Sandbox erstellen?

Unternehmen, die in Adobe Journey Optimizer neue Sandboxes bereitstellen, haben die Frage aufgeworfen, wie TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet werden. In diesem Artikel wird klargestellt, dass TTL-Einstellungen keine Auswirkungen auf bestehende Sandboxes haben und automatisch ausschließlich auf neu bereitgestellte Sandboxes angewendet werden.

Informationen zur Handhabung von TTL finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Weitere Informationen zur TTL von Datensätzen finden Sie auf [dieser Seite](../data/datasets-ttl.md).

+++


## Profile und Zielgruppen-Management {#ajo-troubleshooting-audiences}

+++ Wie lassen sich Diskrepanzen bei der Zielgruppengröße beheben?

Die Zahl der verarbeiteten Einträge in der Funktion **Zielgruppe lesen** von Adobe Journey Optimizer kann niedriger sein als die erwartete Zielgruppengröße. Dieses Problem hängt häufig mit falsch konfigurierten Namespaces zusammen, was dazu führt, dass Profile aus Journeys ausgeschlossen werden. Die Lösung umfasst das Überprüfen und Korrigieren von Namespace-Konfigurationen, das Überprüfen der entsprechenden Dokumentation und das Anpassen von Prioritäten, um reibungslosere Abläufe in Adobe Journey Optimizer sicherzustellen.

Weitere Informationen zum Beheben dieses Problems finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}.

Konsultieren Sie auch [diesen Artikel über veraltete Zielgruppengrößen](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Weitere Informationen zur Aktivität **Zielgruppe lesen** in Journeys finden Sie [auf dieser Seite](../building-journeys/read-audience.md).

+++

+++ Warum schlagen Profilaktualisierungen fehl?

In Adobe Journey Optimizer werden bestimmte Feldwerte ggf. nicht richtig aktualisiert, nachdem in einer Journey eine Aktivität vom Typ **Profil aktualisieren** ausgeführt wurde. In einigen Fällen können aktualisierte Felder verschwinden oder zu ihrem vorherigen Status zurückkehren. Prüfen Sie, ob Regeln oder Bedingungen miteinander in Konflikt stehen, prüfen Sie die Berechtigungseinstellungen, verwenden Sie einen eindeutigen Datensatz für die Aktivität **Profil aktualisieren** und vergewissern Sie sich, dass nicht gleichzeitig ein anderer Aufnahmeprozess in dasselbe Profil schreibt.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen über die Aktivität **Profil aktualisieren** finden Sie auf [dieser Seite](../building-journeys/update-profiles.md).

Siehe auch [Dokumentation zur Datenaufnahme in Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/tutorials/ingest-batch-data#dataset-activity){target="_blank"}.

+++

+++ Warum stimmt die Profilanzahl beim Eintritt in eine Journey nicht mit der Zahl in der zugehörigen Zielgruppe überein?

Die Diskrepanz kann auftreten, wenn die Journey den Profil-Snapshot eines vorherigen Tages verwendet und der Snapshot des aktuellen Tages zum Zeitpunkt der Journey-Ausführung nicht verfügbar ist.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen finden Sie in [diesem Beitrag in der Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998?profile.language=de){target="_blank"}.

Konsultieren Sie außerdem die [Dokumentation zur API für Adobe Experience Platform-Zeitpläne](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/api/schedules){target="_blank"}, um zu überprüfen, wann Ihr täglicher Auftrag geplant ist.

+++

+++ Warum zeigt die Zielgruppenauswahl in Kampagnen und Journeys unterschiedliche Profilzahlen an?

Möglicherweise stellen Sie fest, dass dieselbe Zielgruppe in Kampagnen eine andere Profilanzahl anzeigt als in Journeys. Dies geschieht, weil jede Funktion verschiedene APIs zum Abrufen von Zielgruppendaten verwendet, die unterschiedliche Werte zurückgeben können.

Dieses Verhalten ist normal und wirkt sich nicht auf die Kampagnenausführung aus. Die richtigen Profile werden weiterhin angesprochen. Um die tatsächliche Zielgruppengröße zu prüfen, gehen Sie zu **[!UICONTROL Kundin bzw. Kunde]** > **[!UICONTROL Zielgruppen]** und wählen Sie Ihre Zielgruppe aus.

+++


+++ Wie können Probleme mit der Zielgruppenpopulation gelöst werden?

Probleme mit der Zielgruppenpopulation können auftreten, wenn Komponenten oder Ressourcen fehlen (oft aufgrund von falsch konfigurierten Berechtigungen, Bereitstellungen oder Genehmigungen). Um die Probleme zu beheben, prüfen Sie zunächst die Berechtigungen, stellen Sie eine korrekte Bereitstellung sicher und überprüfen Sie die Genehmigungen. Wenn das Problem weiterhin besteht, eskalieren Sie den Fall und stimmen Sie sich mit Support-Teams ab, um eine vollständige Lösung zu finden.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen über die Aktivität **Profil aktualisieren** finden Sie auf [dieser Seite](../building-journeys/update-profiles.md).

Siehe auch [Dokumentation zu Adobe Real-Time CDP-Profilen](https://experienceleague.adobe.com/de/docs/experience-platform/profile/ui/user-guide#profile-detail){target="_blank"}.

+++

+++ Warum ist die Anzahl der ansprechbaren Profile in einem kurzen Zeitraum deutlich gestiegen? 

Die Metrik **Ansprechbare Profile** gibt die Anzahl der eindeutigen Profile an, die von Journeys oder Kampagnen in den letzten 12 Monaten angesprochen wurden. Ein plötzlicher Anstieg kann auftreten, wenn große Zielgruppen angesprochen werden oder sich Datensätze ändern. Gehen Sie wie folgt vor: Überprüfen Sie die **Logik zum Zählen von Profilen**, untersuchen Sie Journeys, die große Zielgruppen ansprechen, **filtern Sie Zielgruppen** auf der Journey-Ebene, reduzieren Sie die **Größe der ansprechbaren Zielgruppe** und überwachen Sie **Datensatzänderungen**.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Überwachen Sie die Lizenznutzung Ihres Unternehmens und die ansprechbaren Profile mithilfe des [Lizenznutzungs-Dashboards](../audience/license-usage.md).

Siehe auch [Überblick über den Abfrage-Service von Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/query/home){target="_blank"}.

+++

+++ Warum werden anhand von Datumsfunktionen E-Mails an Personen außerhalb der beabsichtigten Zielgruppe gesendet?

E-Mails werden ggf. an Empfängerinnen und Empfänger gesendet **, die die angegebenen Zielgruppenkriterien nicht erfüllen**. Beispielsweise können Mitglieder mit Einlösungsterminen **vor dem 4. Juli 2025** E-Mails erhalten, die nur für Mitglieder nach diesem Datum bestimmt sind. Dieses Verhalten kann mit einer **falsch konfigurierten Zielgruppensegmentierung** oder **unerwarteten Änderungen in der Profilqualifizierungslogik** zusammenhängen.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zu Datumsfunktionen finden Sie auf [dieser Seite](../building-journeys/functions/date-functions.md).

+++

+++ Warum übersteigt sie Summe aus „Zugestellt“ + „Ausschlüsse“ in den Kampagnenberichten meine Zielgruppengröße?

In Kampagnenberichten kann es vorkommen, dass die Summe aus **Zugestellt** und **Ausschlüsse** die ursprüngliche Zielgruppengröße überschreitet. Dies geschieht, weil die Metrik **Ausschlüsse** alle Ausschlussereignisse zählt, einschließlich doppelter Ausschlussereignisse für dasselbe Profil. Wenn ein Profil während einer Kampagne mehrmals ausgeschlossen wird, wird jedes Ereignis separat gezählt.

**Beispiel**: Eine an 94.000 Profile gerichtete Kampagne zeigt 69.000 zugestellte Nachrichten und 37.000 Ausschlüsse, also insgesamt 106.000 Profile. Dies übersteigt die ursprünglichen 94.000 Zielprofile. Dieses Verhalten ist normal.

Informationen zum Unterschied zwischen Ausschlussereignissen insgesamt und eindeutigen Profilausschlüssen finden Sie unter [Erklärung zur Zählung von Ausschlüssen](../reports/exclusion-list.md#exclusion-list).

Erfahren Sie mehr über [Kampagnenberichte](../reports/campaign-global-report-cja.md) und [Berichtsmetriken](../reports/global-report-components-cja.md).

+++

+++ Wie kann ich beim Speichern von Journeys Probleme bei der Zielgruppenauswahl und Chrome-Fehler beheben?

Das Hinzufügen von Zielgruppen zu Journey-Bedingungen kann manchmal zu **Anwendungsabstürzen** oder einem **Aw Snap-Fehler** in Chrome führen, einschließlich Fehlern beim Speichern von Journeys. Solche Probleme stehen häufig im Zusammenhang mit **Chromium-Services**. Wenden Sie zur Behebung ein **Browser-Update** an oder wenden Sie eine geeignete **Umgehungslösung** an.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

+++

## Journeys {#ajo-troubleshooting-journeys}

Informationen zu Journeys finden Sie in den folgenden Abschnitten zur Fehlerbehebung:

* [Fehlerbehebung vor dem Testen der Journey](../building-journeys/troubleshooting.md)
* [Fehlerbehebung bei eingehenden Aktionen in Journeys](../building-journeys/troubleshooting-inbound.md)
* [Fehlerbehebung bei der Live-Journey-Ausführung](../building-journeys/troubleshooting-execution.md)
* [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md)


+++ Warum gehen beim Erstellen einer neuen Journey-Version Ausdrücke verloren?  

Beim Erstellen einer neuen Journey-Version können **Ausdrücke in bestimmten Schritten** verloren gehen, was Fehler verursacht und eine erneute manuelle Eingabe erforderlich macht. Gehen Sie wie folgt vor: **Duplizieren Sie die Journey**, testen Sie auf Reproduzierbarkeit, **vermeiden Sie das Neuladen des Browsers** und verwenden Sie für ältere Journeys die **aktualisierte Arbeitsfläche**.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zum Duplizieren einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum steigen Profile vorzeitig aus Journeys aus? 

Profile steigen ggf. unerwartet aus einer Journey aus, ohne einen angegebenen Knoten zu durchlaufen, wenn die **Bedingung zur Überprüfung des Feedback-Status** von gesendeten Nachrichten falsch konfiguriert ist. Gehen Sie wie folgt vor: Überprüfen Sie die **Bedingungslogik**, implementieren Sie **alternative Logik** oder wenden Sie sich an Ihr **Implementierungs-Team**.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Siehe auch [Richtlinien zum Entwerfen von Journeys](../building-journeys/using-the-journey-designer.md).

+++


+++ Warum steigen Profile unerwartet aus Journeys aus?

Profile steigen ggf. unerwartet aus einer Journey aus, wenn **Ereignisbegrenzung** auftritt, wodurch einige Profile verworfen werden, falls die Anzahl der verarbeiteten Ereignisse die Systemkapazität überschreitet. Um Profilaustritte zu reduzieren, machen Sie sich mit den **Systembeschränkungen** vertraut, überwachen Sie **Ereignisspitzen** und optimieren Sie den **Datenfluss**, um das Überschreiten von Schwellenwerten zu verhindern.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Siehe auch [Schutzmechanismen für Journeys](../start/guardrails.md#decisioning-guardrails).

+++


+++ Warum löst mein Ereignis nicht die beabsichtigte Journey aus?  

Bei Ereignissen kann der Trigger einer Journey fehlschlagen, selbst wenn alle Kriterien erfüllt sind, falls sie **über Abfrage-Services erstellt** anstatt an den **Data Collection Core Service (DCCS)** gestreamt werden. Gehen Sie wie folgt vor: Überprüfen Sie die Ereigniskonfiguration, stellen Sie sicher, dass Ereignisse **direkt an DCCS gestreamt** werden und überprüfen Sie die Funktionalität mit dem **Testmodus**.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zu Ereignissen finden Sie [auf dieser Seite](../event/about-events.md).

Siehe auch [Schutzmechanismen für Journey-Ereignisse](../start/guardrails.md#events-g).

+++


+++ Wie kann ich Probleme beim Auslösen einer Journey nach Zielgruppenänderungen in Adobe Journey Optimizer beheben? 

Wenn eine Journey nach Änderungen an der zugehörigen Zielgruppe (z. B. Änderungen an der Zusammenführungsrichtlinie) nicht mehr ausgelöst wird, kann es zu Unterbrechungen der Datenflüsse kommen. Gehen Sie wie folgt vor: **Duplizieren und veröffentlichen Sie die Journey** mit den aktualisierten Zielgruppeneinstellungen neu, um dafür zu sorgen, dass Trigger ordnungsgemäß funktionieren.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zum Duplizieren einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum tritt bei einer benutzerdefinierten Aktion, die einen externen Drittanbieter-Endpunkt aufruft, eine Zeitüberschreitung auf?

Zeitüberschreitungsfehler können auftreten, wenn eine **benutzerdefinierte Aktion** einen externen Drittanbieter-Endpunkt aufruft. Gehen Sie wie folgt vor: Stellen Sie sicher, dass der **Endpunkt zugänglich ist**, überprüfen Sie **Server-Protokolle**, vergewissern Sie sich, dass **keine Blockierung von Adobe** erfolgt, aktualisieren Sie Endpunktkonfigurationen nach Bedarf und **testen Sie nach Aktualisierungen**. Achten Sie zudem auf **Zeitüberschreitungsspezifikationen für APIs**.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

[Auf dieser Seite](../configuration/throttling.md) erfahren Sie mehr über die Drosselungs-API für Journeys.

Siehe auch [Dokumentation zur Integration mit externen Systemen](../configuration/external-systems.md).

+++

+++ Welche Schritte sollten Sie unternehmen, wenn bei der Veröffentlichung einer Zielgruppe über einen Pfeil ein Fehler des Typs „403“ mit der Meldung **invalid_access** oder **Kein Zugriff auf diese dataId=XX gewährt** auftritt?

Um diesen Fehler zu beheben, bitten Sie Ihre bzw. Ihren Admin, sicherzustellen, dass Ihr Benutzerprofil Zugriff auf die erforderlichen Datenansichten für die Zielgruppenveröffentlichung hat, und versuchen Sie dann erneut, die Zielgruppe zu veröffentlichen.

In [der Dokumentation zu Berechtigungen](../administration/permissions.md){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

+++

## Regeln {#ajo-troubleshooting-rules}

+++ Warum funktioniert das Dropdown-Menü „Begrenzungsregeln“ nicht?

Probleme mit dem Dropdown-Menü **Begrenzungsregeln** treten häufig auf, wenn Regelsätze **falsch konfiguriert** oder **nicht aufrufbar** sind. Vergewissern Sie sich, dass alle Regelsätze richtig konfiguriert und verfügbar sind, um das Problem zu beheben.

Weitere Informationen finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"}.

[In diesem Abschnitt](../conflict-prioritization/rule-sets.md) erfahren Sie, wie Sie Begrenzungsregeln anwenden.

+++

## Entscheidungsfindung {#ajo-troubleshooting-decisioning}

+++ Wie kann ich Probleme beim Erstellen von Angebotssammlungen beheben?

Probleme beim Erstellen von Angebotssammlungen treten häufig auf, wenn für Ihre Organisation **Kataloge nicht bereitgestellt wurden**. Gehen Sie wie folgt vor: Prüfen Sie, ob alle erforderlichen Kataloge korrekt bereitgestellt wurden, bevor Sie versuchen, Angebotssammlungen zu erstellen.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zu Angebotssammlungen finden Sie auf [dieser Seite](../offers/offer-library/creating-collections.md).

+++

+++ Warum kann ich nicht auf Offer Decisioning zugreifen?  

Bei der Integration von Adobe Target in eine Anwendung mithilfe von Adobe Journey Optimizer ist die Option **Offer Decisioning** möglicherweise nicht in der Datenstromkonfiguration verfügbar. Die Ursache sind normalerweise **Berechtigungseinstellungen** oder **Bereitstellungsbeschränkungen**. Gehen Sie wie folgt vor: Überprüfen Sie die Benutzerberechtigungen und stellen Sie sicher, dass die erforderliche Bereitstellung vorhanden ist.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zu den erforderlichen Berechtigungen für Offer Decisioning finden [auf dieser Seite](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Mehrsprachig {#ajo-troubleshooting-multilingual}

+++ Wie kann ich das Problem `Message validation error (CJMMAS - 1069-500)` beheben?

Ein Fehler bei der Nachrichtenvalidierung (CJMMAS – 1069-500), der mit der mehrsprachigen Funktion zusammenhängt, verhindert in Adobe Journey Optimizer, dass Journeys in den Testmodus versetzt oder veröffentlicht werden.

In [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} erfahren Sie, wie Sie das Problem beheben können.

Weitere Informationen zu mehrsprachigem Inhalt finden Sie auf [dieser Seite](../content-management/multilingual-gs.md).

+++


## Konfiguration {#ajo-troubleshooting-config}

+++ Wie aktiviere ich TLS v1.3 für benutzerdefinierte Aktionen?  

Um beim Herstellen einer Verbindung zu Drittanbietersystemen die **Integrität und Sicherheit von Daten** zu wahren, sorgen Sie dafür, dass für Ihre benutzerdefinierten Aktionen Transport Layer Security (**TLS**) v1.3 aktiviert ist. Dadurch wird die Kommunikation geschützt und werden potenzielle Sicherheitslücken vermieden.


Weitere Informationen finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}.

Weitere Informationen zu mehrsprachigem Inhalt finden Sie auf [dieser Seite](../action/about-custom-action-configuration.md).

+++

+++ Warum kann ich direkt aus einer Abfrage in Adobe Journey Optimizer kein Dashboard erstellen? 

In Adobe Journey Optimizer lassen sich Dashboards nicht direkt aus Abfragen erstellen. Verwenden Sie zum Erstellen von Dashboards die verfügbaren **Funktionen zur Erstellung von Dashboards** in Adobe Experience Platform. Damit können Sie Abfragedaten effektiv visualisieren und analysieren.

Weitere Informationen finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}.

+++

## APIs {#ajo-troubleshooting-apis}

+++ Wie kann ich Zugriffsprobleme bei der Abfrage-Service-API beheben?  

Zugriffsfehler bei Verwendung der **Abfrage-Service-API** über Postman oder ähnliche Tools werden in der Regel durch **unzureichende Berechtigungen** verursacht. Gehen Sie wie folgt vor: Überprüfen Sie die Benutzerberechtigungen, prüfen Sie die API-Anmeldeinformationen und übermitteln Sie bei Bedarf detaillierte Informationen an den Support.

Weitere Informationen finden Sie in [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"}.

Siehe auch [Dokumentation zur Verwaltung von API-Anmeldeinformationen](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/permissions#manage-api-credentials-for-role){target="_blank"}.

+++
