---
solution: Journey Optimizer
product: journey optimizer
title: Fehlerbehebung bei Journey Optimizer
description: Fragen zur Fehlerbehebung bei Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 8fe62d872a06e09072f8cfdac80287057d640308
workflow-type: tm+mt
source-wordcount: '2647'
ht-degree: 1%

---

# Fehlerbehebung {#ajo-troubleshooting}


Im Folgenden finden Sie eine Liste von Artikeln zur Fehlerbehebung bei Adobe Journey Optimizer. Jeder Abschnitt zur Fehlerbehebung enthält Antworten auf häufig gestellte Fragen und Lösungen für Probleme.

Siehe auch Häufig gestellte Fragen zu [Adobe Experience Platform und Dokumentation zur Fehlerbehebung](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## E-Mail-Kanal {#ajo-troubleshooting-email}

+++ Wie können E-Mail-Formatierungsprobleme in Adobe Journey Optimizer mithilfe von Designs verhindert werden?

In Adobe Journey Optimizer (AJO) kann die Änderung der standardmäßigen CSS-Blöcke in der E-Mail-Kopfzeile zu unerwarteten Formatierungsproblemen führen - insbesondere nach dem Entfernen von Inhaltsfragmenten. Diese Probleme treten auf Mobilgeräten deutlicher zutage und können zu Layout-Verschiebungen oder Inkonsistenzen in der Formatierung führen. Um dies zu verhindern, verwenden Sie die Funktion „Designs“, um benutzerdefiniertes CSS sicher anzuwenden, ohne die vom System generierten CSS-Stile zu ändern.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zur E-Mail-Formatierung [auf dieser Seite](../email/get-started-email-design.md).

+++


+++ Warum funktionieren Fragmente mit bearbeitbaren Feldern nicht?

In Adobe Journey Optimizer können Fragmente mit bearbeitbaren Feldern möglicherweise nicht korrekt geladen werden oder unerwartet dupliziert werden, wenn sie zu Vorlagen hinzugefügt werden. Das Problem betrifft normalerweise bestimmte Fragmente in allen Umgebungen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu anpassbaren Fragmenten [auf dieser Seite](../content-management/customizable-fragments.md).

+++

+++ Warum werden HTML-Fragmente in E-Mails nicht korrekt angezeigt?

HTML-Fragmente können möglicherweise nicht ordnungsgemäß in E-Mails gerendert werden, was oft als **Fragment-IDs** anstatt als tatsächlicher Inhalt erscheint. Im Gegensatz zu visuellen Fragmenten müssen HTML-Fragmente sorgfältig konfiguriert werden. Um dies zu beheben, befolgen Sie die Best Practices für die Verwendung von sowohl **visuellen als auch HTML** Ausdrucksfragmenten) in Ihren E-Mail-Kampagnen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu HTML-Fragmenten [auf dieser Seite](../content-management/fragments.md).

+++

+++ Warum verschwinden E-Mail-Vorlagen und -Inhalte aus unveröffentlichten Journey?

Beim Bearbeiten von E-Mail-Vorlagen auf einer unveröffentlichten Journey können Inhalt und Vorlagen bestimmter E-Mails unerwartet verschwinden. Dies kann zu Überarbeitungen und Verzögerungen führen. Um das Risiko dieses Problems zu verringern, vermeiden Sie gleichzeitige Bearbeitungen, begrenzen Sie die Anzahl der geöffneten Registerkarten und speichern Sie häufig Änderungen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu Vorlagen finden [ auf dieser Seite](../email/use-email-templates.md).

+++

+++ Warum wird das Feld „E-Mail-Preheader“ nicht im Modus „Eigenen Code erstellen“ angezeigt? 

Im Modus **Eigenen Code erstellen** wird unter der Funktion **E-Mail-Text bearbeiten** das Eingabefeld Preheader nicht angezeigt. Um Preheader-Text einzuschließen, müssen **den Preheader in** benutzerdefinierten HTML-Inhalt manuell codieren.

Weitere Informationen [ Beheben dieses Problems finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Konfiguration von E-Mail-Preheadern [auf dieser Seite](../email/header-parameters.md).

+++

+++ Warum gibt es eine Diskrepanz im Link-Verhalten bei der Verwendung einer HTML-Komponente in E-Mail-Vorlagen?  

Beim Hinzufügen einer **HTML** Komponente zu einer E-Mail-Vorlage verhalten sich Links je nach E **Mail-Client**, **Anzeigemodus** oder **Gerät/Browser** unterschiedlich. Ankerlinks können beispielsweise in der Seitenansicht von **Outlook“ anders funktionieren als** Vollbildansicht. Beachten Sie diese Varianten beim Entwerfen von E-Mail-Vorlagen und beim Testen über mehrere Clients und Geräte hinweg.

Weitere Informationen [ Beheben dieses Problems finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"} diesem Artikel zur Fehlerbehebung .

Siehe auch Best Practices für das Entwerfen von E-Mails [auf dieser Seite](../email/get-started-email-design.md).

+++


+++ Wie lässt sich verhindern, dass in Berichten E-Mail-Tracking-Links fehlen?

Das Tracking fehlender Links in Adobe Journey Optimizer tritt auf, wenn E-Mail-URLs dynamische Variablen verwenden und nicht mit HTTP beginnen oder wenn Logikanweisungen im URL-Feld platziert werden. Um dies zu beheben, stellen Sie sicher, dass alle URLs mit HTTP beginnen, vermeiden Sie die Verwendung von Logik im URL-Feld und verschieben Sie komplexe Personalisierungslogik in die HTML-Inhalte oder vorverarbeiteten Attribute.


Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zum E-Mail-Tracking [auf dieser Seite](../email/message-tracking.md).

+++

+++ Wie behebe ich einen Mail-Exchange-Fehler beim Einrichten von API-ausgelösten Transaktions-E-Mail-Kampagnen? 

Wenn beim Erstellen einer Kanalkonfiguration für eine API-ausgelöste Transaktions-E-Mail-Kampagne in Adobe Journey Optimizer ein MX-Fehler (Mail Exchange) auftritt, kann dies auf **DNS-Fehlkonfigurationen** oder **DMARC-** zurückzuführen sein. Um dies zu beheben, stellen Sie sicher, dass Ihr DNS korrekt konfiguriert ist, und stellen Sie sicher, dass Ihre Domain die **Domain-basierten Anforderungen an die Nachrichtenauthentifizierung, Berichterstellung und Konformität (DMARC)**.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu E-Mail-DMARC[Richtlinien finden Sie auf dieser Seite](../configuration/dmarc-record-update.md).

Siehe auch [Dokumentation zu API-ausgelösten ](../campaigns/api-triggered-campaigns.md).
+++

## Push-Kanal {#ajo-troubleshooting-push}

+++ Kann ein Profil mehrere Push-Token in Adobe Journey Optimizer haben?

Bei der Implementierung von Push-Benachrichtigungen in Journey Optimizer kann einem einzelnen Profil tatsächlich mehrere Push-Token mit verschiedenen Geräten zugeordnet sein. Während einer Push-Benachrichtigungskampagne verwaltet Journey Optimizer diese Token und stellt sicher, dass das Zielgruppenprofil über alle zugehörigen Geräte hinweg erreicht werden kann.

Weitere Informationen [ Verwaltung von Push-Token finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} in diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Push-Konfiguration [auf dieser Seite](../push/push-configuration.md).

+++

+++ Warum wird ich beim Klicken auf eine Push-Nachricht nicht zur konfigurierten Web-URL weitergeleitet?  

Wenn Push-Benachrichtigungen nicht zur vorgesehenen Web-URL umgeleitet werden, kann dies an einer falschen Konfiguration der Klickaktion oder an deaktivierten Push-Benachrichtigungseinstellungen liegen. Stellen Sie sicher **dass die** für die Push-Benachrichtigung korrekt eingestellt ist und dass **automatische Anzeige und Tracking** von Push-Benachrichtigungen aktiviert sind, um dieses Problem zu beheben.

Weitere Informationen zu [ Problem finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Push-Konfiguration [auf dieser Seite](../push/push-configuration.md).

+++


## SMS-Kanal {#ajo-troubleshooting-sms}

+++ Warum werden meine Transaktions-SMS nicht zugestellt, obwohl das Einverständnis auf `marketing.sms.value=y` gesetzt ist?

Wenn ein Empfänger **STOP** auf eine SMS antwortet, werden alle zukünftigen Nachrichten von dieser kurzen Nummer blockiert - einschließlich Transaktionsnachrichten. Um den unterbrechungsfreien Versand von Transaktions-SMS zu gewährleisten, konfigurieren und senden Sie sie über eine **separate Kurzwahlnummer** von der die Empfänger noch nicht abgemeldet haben.

Weitere Informationen zu [ Problem finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Opt-out-Konfiguration für SMS [auf dieser Seite](../sms/sms-opt-out.md).

+++

## In-App-Kanal

+++ Warum kann ich keine Berichte über den In-App-Kanal in Customer Journey Analytics erstellen?

Probleme beim Reporting für den **In-App** Kanal) in Adobe Customer Journey Analytics stammen oft aus falsch konfigurierten **Datenansichten**, **Datensätzen** oder **Schemaaktualisierungen**. Stellen Sie sicher, dass diese Konfigurationen korrekt angewendet werden, um das Problem zu beheben.

Weitere Informationen zu [ Problem finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Integration von Journey Optimizer-Analysedaten in Customer Journey Analytics [ Sie auf dieser Seite](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}.

Siehe auch die Dokumentation zu [Journey Optimizer All-Time Reports](../reports/report-gs-cja.md)

+++


## Daten-Management {#ajo-troubleshooting-data-management}

+++ Wie gelten TTL-Einstellungen (Time-to-Live) für Profil- und Data-Lake-Datensätze, wenn Sie eine neue Sandbox erstellen?

Unternehmen, die neue Sandboxes in Adobe Journey Optimizer bereitstellen, haben Fragen darüber aufgeworfen, wie die TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet werden. In diesem Artikel wird klargestellt, dass TTL-Einstellungen keine Auswirkungen auf bestehende Sandboxes haben und automatisch nur auf neu bereitgestellte angewendet werden.

Informationen [ Umgang mit TTL finden Sie ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Lebensdauer von Datensätzen finden Sie [auf dieser Seite](../data/datasets-ttl.md).

+++


## Profil- und Zielgruppen-Management {#ajo-troubleshooting-audiences}

+++ Wie lassen sich Diskrepanzen bei der Zielgruppenanzahl beheben?

Die Anzahl der verarbeiteten Einträge in der Funktion **Zielgruppe lesen** von Adobe Journey Optimizer kann niedriger sein als die erwartete Zielgruppenanzahl. Dieses Problem tritt häufig aufgrund falscher Namespace-Konfigurationen auf, was dazu führt, dass Profile aus Journey ausgeschlossen werden. Die Lösung umfasst das Überprüfen und Korrigieren von Namespace-Konfigurationen, das Überprüfen der entsprechenden Dokumentation und das Anpassen von Prioritäten, um einen reibungsloseren Betrieb in Adobe Journey Optimizer sicherzustellen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} unter „Problembehandlung“.

Siehe auch [diesen Artikel über veraltete Zielgruppenzahlen](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Weitere Informationen zur Aktivität **Zielgruppe lesen** in Journey finden [ auf dieser Seite](../building-journeys/read-audience.md).

+++

+++ Warum schlagen Profilaktualisierungen fehl?

In Adobe Journey Optimizer werden bestimmte Feldwerte möglicherweise nicht korrekt aktualisiert, nachdem eine Aktivität vom Typ **Profil aktualisieren** auf einer Journey ausgeführt wurde. In einigen Fällen können aktualisierte Felder verschwinden oder zu ihrem vorherigen Status zurückkehren. Überprüfen Sie dazu, ob Regeln oder Bedingungen miteinander in Konflikt stehen, überprüfen Sie die Berechtigungseinstellungen, verwenden Sie einen eindeutigen Datensatz für die Aktivität **Profil aktualisieren** und stellen Sie sicher, dass nicht gleichzeitig ein anderer Aufnahmeprozess in dasselbe Profil schreibt.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zur Aktivität **Profil aktualisieren** in Journey finden Sie [ dieser Seite](../building-journeys/update-profiles.md).

Siehe auch die Dokumentation zu Adobe Experience Platform [](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Warum stimmt die Profilanzahl beim Eingeben einer Journey nicht mit der der zugehörigen Zielgruppe überein?

Die Diskrepanz kann auftreten, wenn der Journey den Profilschnappschuss eines vorherigen Tages verwendet, wenn der aktuelle Tagesschnappschuss zum Zeitpunkt der Journey-Ausführung nicht verfügbar ist.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen finden Sie in [diesem Journey Optimizer-Community-Beitrag](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Siehe auch die [Adobe Experience Platform-Zeitpläne-API](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} um zu überprüfen, wann Ihr täglicher Auftrag geplant ist.

+++


+++ Wie können Probleme mit der Zielgruppenpopulation gelöst werden?

Probleme mit der Zielgruppenpopulation können auftreten, wenn Komponenten oder Ressourcen fehlen, häufig aufgrund von Berechtigungs-, Bereitstellungs- oder Berechtigungsfehlkonfigurationen. Um diese Probleme zu beheben, überprüfen Sie zunächst die Berechtigungen, stellen Sie die korrekte Bereitstellung sicher und überprüfen Sie die Berechtigungen. Wenn das Problem weiterhin besteht, eskalieren Sie den Fall und stimmen Sie sich mit den Support-Teams ab, um eine vollständige Lösung zu finden.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zur Aktivität **Profil aktualisieren** in Journey finden Sie [ dieser Seite](../building-journeys/update-profiles.md).

Siehe auch die [Adobe Real-Time CDP-Profildokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Warum ist die Anzahl der aktivierbaren Profile in einem kurzen Zeitraum deutlich gestiegen? 

Die **Engageable Profiles**-Metrik gibt die Anzahl der eindeutigen Profile an, die von Journey oder Kampagnen in den letzten 12 Monaten aktiviert wurden. Ein plötzlicher Anstieg kann auftreten, wenn große Zielgruppen angesprochen werden oder sich die Datensätze ändern. Um dies zu verwalten, überprüfen Sie die **Profilzählungslogik** untersuchen Sie Journey, die auf große Zielgruppen abzielen **filtern Sie Zielgruppen** auf Journey-Ebene, reduzieren Sie die **adressierbare Zielgruppengröße** und überwachen Sie **Datensatzänderungen**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Überwachen Sie die Lizenznutzung Ihres Unternehmens und ansprechbare Profile mithilfe des [Lizenznutzungs-Dashboards](../audience/license-usage.md)

Siehe auch die [Übersicht über den Adobe Experience Platform Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home?lang=en){target="_blank"}.

+++

+++ Warum werden E-Mails an Personen außerhalb der vorgesehenen Zielgruppe basierend auf Datumsfunktionen gesendet?

E-Mails können an Empfängerinnen und Empfänger gesendet werden **die die angegebenen Zielgruppenkriterien nicht**. Beispielsweise können Mitglieder mit Einlösungsterminen **vor dem 4. Juli 2025** E-Mails erhalten, die nur für diejenigen nach diesem Datum bestimmt sind. Dieses Verhalten kann aus **falsch konfigurierten Zielgruppensegmentierung** oder **unerwarteten Änderungen in der Profilqualifikationslogik)**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu Datumsfunktionen [auf dieser Seite](../../rp_landing_pages/date-landing-page.md).

+++

+++ Wie kann ich beim Speichern von Journey Probleme bei der Zielgruppenauswahl und Chrome-Fehler beheben?

Das Hinzufügen von Zielgruppen zu Journey-Bedingungen kann manchmal zu **Anwendungsabstürzen** oder einem „Aw **Snap-Fehler“** Chrome führen, einschließlich der Fehler beim Speichern von Journey. Diese Probleme stehen häufig im Zusammenhang mit **Chromium-Services**. Um sie zu beheben, wenden Sie ein **Browser-Update** an oder verwenden Sie eine geeignete **Problemumgehung**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

+++

## Journeys {#ajo-troubleshooting-journeys}

+++ Warum gehen Ausdrücke beim Erstellen einer neuen Journey-Version verloren?  

Beim Erstellen einer neuen Journey-Version **Ausdrücke in bestimmten Schritten** verloren gehen, was zu Fehlern führen kann und eine erneute manuelle Eingabe erforderlich macht. Um dies zu beheben, **duplizieren Sie die Journey**, testen Sie auf Reproduzierbarkeit **vermeiden Sie Browser-** und verwenden Sie die **aktualisierte Arbeitsfläche** für ältere Journey.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Wie man eine Journey dupliziert ([ dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum verlassen Profile Journey vorzeitig? 

Profile verlassen möglicherweise unerwartet eine Journey, ohne einen angegebenen Knoten zu durchlaufen, wenn die **Bedingung zur Überprüfung des Feedback-Status** der gesendeten Nachrichten falsch konfiguriert ist. Um dies zu beheben, überprüfen Sie die **Bedingungslogik**, implementieren Sie **alternative Logik** oder wenden Sie sich an Ihr **Implementierungs-Team**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Siehe auch [Design-Richtlinien für Journey](../building-journeys/using-the-journey-designer.md).

+++


+++ Warum verlassen Profile unerwartet die Journey?

Profile verlassen eine Journey möglicherweise unerwartet, wenn **Ereignisbegrenzung** auftritt, wodurch einige Profile verworfen werden, wenn die Anzahl der verarbeiteten Ereignisse die Systemkapazität überschreitet. Um Profilaustritte zu reduzieren, verstehen Sie die **Systembeschränkungen**, überwachen Sie **Ereignisspitzen** und optimieren Sie **Datenfluss**, um das Überschreiten von Schwellenwerten zu verhindern.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Siehe auch [Journey-Schutzmechanismen](../start/guardrails.md#journey-guardrails).

+++


+++ Warum löst mein Ereignis nicht die beabsichtigte Journey aus?  

Bei Ereignissen kann der Trigger einer Journey fehlschlagen, auch wenn alle Kriterien erfüllt sind, wenn sie **über Abfrage-Services erstellt** anstatt an den **Datenerfassungs-Core-Service (DCCS) gestreamt zu werden**. Um dies zu beheben, überprüfen Sie die Ereigniskonfiguration, stellen Sie sicher, dass Ereignisse **direkt an DCCS gestreamt** und überprüfen Sie die Funktionalität mit **Testmodus**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu Ereignissen [auf dieser Seite](../event/about-events.md).

Siehe auch [Schutzmechanismen für Journey-Ereignisse](../start/guardrails.md#events).

+++


+++ Wie kann ich Probleme mit dem Journey-Trigger nach Zielgruppenänderungen in Adobe Journey Optimizer beheben? 

Wenn ein Journey nach Änderungen an seiner zugehörigen Zielgruppe, z. B. Änderungen an der Zusammenführungsrichtlinie, nicht mehr ausgelöst wird, kann es zu Unterbrechungen der Datenflüsse kommen. Um dies zu beheben, **duplizieren und veröffentlichen Sie die Journey erneut** mit den aktualisierten Zielgruppeneinstellungen, um sicherzustellen, dass die Trigger ordnungsgemäß funktionieren.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Wie man eine Journey dupliziert ([ dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum tritt bei einer benutzerdefinierten Aktion, die einen externen Drittanbieter-Endpunkt aufruft, eine Zeitüberschreitung auf?

Zeitüberschreitungsfehler können auftreten, wenn eine **benutzerdefinierte Aktion** einen externen Drittanbieter-Endpunkt aufruft. Um dies zu beheben, stellen Sie sicher, dass der **Endpunkt zugänglich ist**, überprüfen Sie **Serverprotokolle**, stellen Sie sicher, dass **keine Blockierung von Adobe** erfolgt, aktualisieren Sie die Endpunktkonfigurationen nach Bedarf und **Sie nach Aktualisierungen testen**. Achten Sie außerdem auf **API-Aufruf-Zeitüberschreitungsspezifikationen**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zur Journey-Einschränkungs-API [auf dieser Seite](../configuration/throttling.md).

Siehe auch die [Dokumentation zur Integration in externe Systeme](../configuration/external-systems.md).

+++

## Regeln {#ajo-troubleshooting-rules}

+++ Warum funktioniert das Dropdown-Menü „Begrenzungsregeln“ nicht?

Probleme mit dem **Dropdown „Begrenzungsregeln** treten häufig auf, wenn Regelsätze **falsch konfiguriert** oder nicht **werden**. Stellen Sie sicher, dass alle Regelsätze korrekt konfiguriert und verfügbar sind, um das Problem zu beheben.

Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"} zur Fehlerbehebung“.

Erfahren Sie in [ Abschnitt, wie Sie Begrenzungsregeln ](../conflict-prioritization/rule-sets.md).

+++

## Entscheidungsfindung {#ajo-troubleshooting-decisioning}

+++ Wie kann ich Probleme beim Erstellen von Angebotssammlungen beheben?

Schwierigkeiten beim Erstellen von Angebotssammlungen treten häufig auf **wenn für Ihr Unternehmen** Kataloge nicht bereitgestellt wurden. Um dies zu beheben, überprüfen Sie, ob alle erforderlichen Kataloge korrekt bereitgestellt wurden, bevor Sie versuchen, Angebotssammlungen zu erstellen.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu Angebotssammlungen [auf dieser Seite](../offers/offer-library/creating-collections.md).

+++

+++ Warum kann ich nicht auf Offer Decisioning zugreifen?  

Bei der Integration von Adobe Target in eine Anwendung mithilfe von Adobe Journey Optimizer ist die Option **Offer Decisioning** möglicherweise nicht in der Datenstromkonfiguration verfügbar. Dies geschieht normalerweise aufgrund von **Berechtigungseinstellungen** oder **Bereitstellungsbeschränkungen**. Um das Problem zu beheben, überprüfen Sie die Benutzerberechtigungen und stellen Sie sicher, dass die erforderliche Bereitstellung vorhanden ist.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu den erforderlichen Berechtigungen für Offer Decisioning finden [ auf dieser Seite ](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Mehrsprachig {#ajo-troubleshooting-multilingual}

+++ Wie kann ich dieses Problem `Message validation error (CJMMAS - 1069-500)` beheben?

In Adobe Journey Optimizer verhindert ein mit der mehrsprachigen Funktion verknüpfter Nachrichtenvalidierungsfehler (CJMMAS - 1069-500), dass die Journey in den Testmodus versetzt oder veröffentlicht werden.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu mehrsprachigen Inhalten [ Sie auf dieser Seite](../content-management/multilingual-gs.md).

+++


## Konfiguration {#ajo-troubleshooting-config}

+++ Wie aktiviere ich TLS v1.3 für benutzerdefinierte Aktionen?  

Um **Datenintegrität und Sicherheit** beim Herstellen einer Verbindung zu Drittanbietersystemen sicherzustellen, stellen Sie sicher, dass Transport Layer Security (**TLS**) v1.3 für Ihre benutzerdefinierten Aktionen aktiviert ist. Dadurch wird die Kommunikation geschützt und potenzielle Sicherheitslücken werden vermieden.


Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} zur Fehlerbehebung“.

Weitere Informationen zu mehrsprachigen Inhalten [ Sie auf dieser Seite](../action/about-custom-action-configuration.md).

+++

+++ Warum kann ich ein Dashboard nicht direkt aus einer Abfrage in Adobe Journey Optimizer erstellen? 

In Adobe Journey Optimizer können Dashboards nicht direkt aus Abfragen erstellt werden. Verwenden Sie zum Erstellen von Dashboards die **Funktionen zur Dashboard** Erstellung in Adobe Experience Platform, mit denen Sie Abfragedaten effektiv visualisieren und analysieren können.

Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} zur Fehlerbehebung“.

+++

## APIs {#ajo-troubleshooting-apis}

+++ Wie kann ich Zugriffsprobleme mit der Abfrage-Service-API beheben?  

Zugriffsfehler bei Verwendung der **Abfrage-Service-API** über Postman oder ähnliche Tools werden in der Regel durch **unzureichende Berechtigungen** verursacht. Um dies zu beheben, überprüfen Sie Benutzerberechtigungen, überprüfen Sie die API-Anmeldeinformationen und geben Sie detaillierte Informationen an, um bei Bedarf zu unterstützen.

Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"} zur Fehlerbehebung“.

Siehe auch die Dokumentation [Verwalten von API-Anmeldeinformationen](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}.

+++

