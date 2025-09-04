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
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# Fehlerbehebung {#ajo-troubleshooting}


Im Folgenden finden Sie eine Liste von Artikeln zur Fehlerbehebung bei Adobe Journey Optimizer. Jeder Abschnitt zur Fehlerbehebung enthält Antworten auf häufig gestellte Fragen und Lösungen für Probleme.

Siehe auch Häufig gestellte Fragen zu [Adobe Experience Platform und Dokumentation zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## E-Mail-Kanal {#ajo-troubleshooting-email}

### E-Mail-Design {#ajo-troubleshooting-design}

+++ Wie können E-Mail-Formatierungsprobleme in Adobe Journey Optimizer mithilfe von Designs verhindert werden?

In Adobe Journey Optimizer (AJO) kann die Änderung der standardmäßigen CSS-Blöcke in der E-Mail-Kopfzeile zu unerwarteten Formatierungsproblemen führen - insbesondere nach dem Entfernen von Inhaltsfragmenten. Diese Probleme treten auf Mobilgeräten deutlicher zutage und können zu Layout-Verschiebungen oder Inkonsistenzen in der Formatierung führen. Um dies zu verhindern, verwenden Sie die Funktion „Designs“, um benutzerdefiniertes CSS sicher anzuwenden, ohne die vom System generierten CSS-Stile zu ändern.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zur E-Mail-Formatierung [auf dieser Seite](../email/get-started-email-design.md).

+++


+++ Warum funktionieren Fragmente mit bearbeitbaren Feldern nicht?

In Adobe Journey Optimizer können Fragmente mit bearbeitbaren Feldern möglicherweise nicht korrekt geladen werden oder unerwartet dupliziert werden, wenn sie zu Vorlagen hinzugefügt werden. Das Problem betrifft normalerweise bestimmte Fragmente in allen Umgebungen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu anpassbaren Fragmenten [auf dieser Seite](../content-management/customizable-fragments.md).

+++

+++ Warum verschwinden E-Mail-Vorlagen und -Inhalte aus unveröffentlichten Journey?

Beim Bearbeiten von E-Mail-Vorlagen auf einer unveröffentlichten Journey können Inhalt und Vorlagen bestimmter E-Mails unerwartet verschwinden. Dies kann zu Überarbeitungen und Verzögerungen führen. Um das Risiko dieses Problems zu verringern, vermeiden Sie gleichzeitige Bearbeitungen, begrenzen Sie die Anzahl der geöffneten Registerkarten und speichern Sie häufig Änderungen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zu Vorlagen finden [ auf dieser Seite](../email/use-email-templates.md).

+++

+++ Kann ein Profil mehrere Push-Token in Adobe Journey Optimizer haben?

Bei der Implementierung von Push-Benachrichtigungen in Journey Optimizer kann einem einzelnen Profil tatsächlich mehrere Push-Token mit verschiedenen Geräten zugeordnet sein. Während einer Push-Benachrichtigungskampagne verwaltet Journey Optimizer diese Token und stellt sicher, dass das Zielgruppenprofil über alle zugehörigen Geräte hinweg erreicht werden kann.

Weitere Informationen [ Verwaltung von Push-Token finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} in diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Push-Konfiguration [auf dieser Seite](../push/push-configuration.md).

+++

### E-Mail-Tracking und Reporting {#ajo-troubleshooting-tracking}

+++ Wie lässt sich verhindern, dass in Berichten E-Mail-Tracking-Links fehlen?

Das Tracking fehlender Links in Adobe Journey Optimizer tritt auf, wenn E-Mail-URLs dynamische Variablen verwenden und nicht mit HTTP beginnen oder wenn Logikanweisungen im URL-Feld platziert werden. Um dies zu beheben, stellen Sie sicher, dass alle URLs mit HTTP beginnen, vermeiden Sie die Verwendung von Logik im URL-Feld und verschieben Sie komplexe Personalisierungslogik in die HTML-Inhalte oder vorverarbeiteten Attribute.


Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} unter „Problembehandlung“.

Weitere Informationen zum E-Mail-Tracking [auf dieser Seite](../email/message-tracking.md).

+++

### E-Mail senden {#ajo-troubleshooting-sending}

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


## Daten-Management {#ajo-troubleshooting-data-management}

+++ Wie gelten TTL-Einstellungen (Time-to-Live) für Profil- und Data-Lake-Datensätze, wenn Sie eine neue Sandbox erstellen?

Unternehmen, die neue Sandboxes in Adobe Journey Optimizer bereitstellen, haben Fragen darüber aufgeworfen, wie die TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet werden. In diesem Artikel wird klargestellt, dass TTL-Einstellungen keine Auswirkungen auf bestehende Sandboxes haben und automatisch nur auf neu bereitgestellte angewendet werden.

Informationen [ Umgang mit TTL finden Sie ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} diesem Artikel zur Fehlerbehebung .

Weitere Informationen zur Lebensdauer von Datensätzen finden Sie [auf dieser Seite](../data/datasets-ttl.md).

+++


## Profil- und Zielgruppen-Management {#ajo-troubleshooting-audiences}

+++ Wie lassen sich Diskrepanzen bei der Zielgruppenanzahl beheben?

Die Anzahl der verarbeiteten Einträge in der Funktion **Zielgruppe lesen** von Adobe Journey Optimizer kann niedriger sein als die erwartete Zielgruppenanzahl. Dieses Problem tritt häufig aufgrund falscher Namespace-Konfigurationen auf, was dazu führt, dass Profile aus Journey ausgeschlossen werden. Die Lösung umfasst das Überprüfen und Korrigieren von Namespace-Konfigurationen, das Überprüfen der entsprechenden Dokumentation und das Anpassen von Prioritäten, um einen reibungsloseren Betrieb in Adobe Journey Optimizer sicherzustellen.

Weitere Informationen [ Beheben dieses Problems finden ](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} unter „Problembehandlung“.

Siehe auch [diesen Artikel über veraltete Zielgruppenzahlen](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Weitere Informationen zur Aktivität **Zielgruppe lesen** in Journey finden [ auf dieser Seite](../building-journeys/read-audience.md).

+++

+++ Warum schlagen Profilaktualisierungen fehl?

In Adobe Journey Optimizer werden bestimmte Feldwerte möglicherweise nicht korrekt aktualisiert, nachdem eine Aktivität vom Typ **Profil aktualisieren** auf einer Journey ausgeführt wurde. In einigen Fällen können aktualisierte Felder verschwinden oder zu ihrem vorherigen Status zurückkehren. Überprüfen Sie dazu, ob Regeln oder Bedingungen miteinander in Konflikt stehen, überprüfen Sie die Berechtigungseinstellungen, verwenden Sie einen eindeutigen Datensatz für die Aktivität **Profil aktualisieren** und stellen Sie sicher, dass nicht gleichzeitig ein anderer Aufnahmeprozess in dasselbe Profil schreibt.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zur Aktivität **Profil aktualisieren** in Journey finden Sie [ dieser Seite](../building-journeys/update-profiles.md).

Siehe auch die Dokumentation zu Adobe Experience Platform [&#128279;](https://experienceleague.adobe.com/de/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Warum stimmt die Profilanzahl beim Eingeben einer Journey nicht mit der der zugehörigen Zielgruppe überein?

Die Diskrepanz kann auftreten, wenn der Journey den Profilschnappschuss eines vorherigen Tages verwendet, wenn der aktuelle Tagesschnappschuss zum Zeitpunkt der Journey-Ausführung nicht verfügbar ist.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen finden Sie in [diesem Journey Optimizer-Community-Beitrag](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998?profile.language=de){target="_blank"}.

Siehe auch die [Adobe Experience Platform-Zeitpläne-API](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} um zu überprüfen, wann Ihr täglicher Auftrag geplant ist.

+++


+++ Wie können Probleme mit der Zielgruppenpopulation gelöst werden?

Probleme mit der Zielgruppenpopulation können auftreten, wenn Komponenten oder Ressourcen fehlen, häufig aufgrund von Berechtigungs-, Bereitstellungs- oder Berechtigungsfehlkonfigurationen. Um diese Probleme zu beheben, überprüfen Sie zunächst die Berechtigungen, stellen Sie die korrekte Bereitstellung sicher und überprüfen Sie die Berechtigungen. Wenn das Problem weiterhin besteht, eskalieren Sie den Fall und stimmen Sie sich mit den Support-Teams ab, um eine vollständige Lösung zu finden.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zur Aktivität **Profil aktualisieren** in Journey finden Sie [ dieser Seite](../building-journeys/update-profiles.md).

Siehe auch die [Adobe Real-Time CDP-Profildokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Wie kann ich Probleme mit dem Journey-Trigger nach Zielgruppenänderungen in Adobe Journey Optimizer beheben? 

Wenn ein Journey nach Änderungen an seiner zugehörigen Zielgruppe, z. B. Änderungen an der Zusammenführungsrichtlinie, nicht mehr ausgelöst wird, kann es zu unterbrochenen Kampagnenflüssen kommen. Um dies zu beheben, **duplizieren und veröffentlichen Sie die Journey erneut** mit den aktualisierten Zielgruppeneinstellungen, um sicherzustellen, dass die Trigger ordnungsgemäß funktionieren.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Wie man eine Journey dupliziert ([ dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++


## Journeys

### Ereignisse

+++ Warum löst mein Ereignis nicht die beabsichtigte Journey aus?  

Bei Ereignissen kann der Trigger einer Journey fehlschlagen, auch wenn alle Kriterien erfüllt sind, wenn sie **über Abfrage-Services erstellt** anstatt an den **Datenerfassungs-Core-Service (DCCS) gestreamt zu werden**. Um dies zu beheben, überprüfen Sie die Ereigniskonfiguration, stellen Sie sicher, dass Ereignisse **direkt an DCCS gestreamt** und überprüfen Sie die Funktionalität mit **Testmodus**.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu Ereignissen [auf dieser Seite](../event/about-events.md).

Siehe auch [Schutzmechanismen für Journey-Ereignisse](../start/guardrails.md#events).

+++

## Entscheidungsfindung {#ajo-troubleshooting-decisioning}

+++ Wie kann ich Probleme beim Erstellen von Angebotssammlungen beheben?

Schwierigkeiten beim Erstellen von Angebotssammlungen treten häufig auf **wenn für Ihr Unternehmen** Kataloge nicht bereitgestellt wurden. Um dies zu beheben, überprüfen Sie, ob alle erforderlichen Kataloge korrekt bereitgestellt wurden, bevor Sie versuchen, Angebotssammlungen zu erstellen.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu Angebotssammlungen [auf dieser Seite](../offers/offer-library/creating-collections.md).

+++


## Mehrsprachig {#ajo-troubleshooting-multilingual}

+++ Wie kann ich dieses Problem `Message validation error (CJMMAS - 1069-500)` beheben?

In Adobe Journey Optimizer verhindert ein mit der mehrsprachigen Funktion verknüpfter Nachrichtenvalidierungsfehler (CJMMAS - 1069-500), dass die Journey in den Testmodus versetzt oder veröffentlicht werden.

Unter [diesem Artikel zur Fehlerbehebung](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} erfahren Sie, wie Sie dieses Problem beheben können.

Weitere Informationen zu mehrsprachigen Inhalten [ Sie auf dieser Seite](../content-management/multilingual-gs.md).

++


## Konfiguration {#ajo-troubleshooting-config}

### Sicherheit {#ajo-troubleshooting-security}

+++ Wie aktiviere ich TLS v1.3 für benutzerdefinierte Aktionen?  

Um **Datenintegrität und Sicherheit** beim Herstellen einer Verbindung zu Drittanbietersystemen sicherzustellen, stellen Sie sicher, dass Transport Layer Security (**TLS**) v1.3 für Ihre benutzerdefinierten Aktionen aktiviert ist. Dadurch wird die Kommunikation geschützt und potenzielle Sicherheitslücken werden vermieden.


Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} zur Fehlerbehebung“.

Weitere Informationen zu mehrsprachigen Inhalten [ Sie auf dieser Seite](../action/about-custom-action-configuration.md).

+++

### Dashboards {#ajo-troubleshooting-dashboards}

+++ Warum kann ich ein Dashboard nicht direkt aus einer Abfrage in Adobe Journey Optimizer erstellen? 

In Adobe Journey Optimizer können Dashboards nicht direkt aus Abfragen erstellt werden. Verwenden Sie zum Erstellen von Dashboards die **Funktionen zur Dashboard** Erstellung in Adobe Experience Platform, mit denen Sie Abfragedaten effektiv visualisieren und analysieren können.

Weitere Informationen finden [ unter &quot;](https://experienceleague.adobe.com/de/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} zur Fehlerbehebung“.

++