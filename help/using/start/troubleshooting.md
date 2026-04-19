---
solution: Journey Optimizer
product: journey optimizer
title: Artikel zur Fehlerbehebung in Journey Optimizer
description: Artikel zur Fehlerbehebung in Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 7755e29c4ad07319dadfb3426c8093199b4f843b
workflow-type: tm+mt
source-wordcount: '4652'
ht-degree: 47%

---

# Häufig gestellte Fragen zur Fehlerbehebung {#ajo-troubleshooting}

Im Folgenden finden Sie eine Liste von Artikeln zur Fehlerbehebung in Adobe Journey Optimizer. Jeder Abschnitt zur Fehlerbehebung enthält Antworten auf häufig gestellte Fragen und Lösungen für Probleme.

Geben Sie bei der Kontaktaufnahme mit dem Adobe-Support bei ungelösten Problemen Umgebungsdetails, Auswirkungsstufe, Replikationsschritte, Protokolle oder Screenshots und relevante IDs an. [Erfahren Sie, was Sie in Support-Tickets einschließen können](user-interface.md#support-ticket-guidelines).

## E-Mail-Kanal {#ajo-troubleshooting-email}

+++ Wie lassen sich E-Mail-Formatierungsprobleme in Adobe Journey Optimizer mithilfe von Themen verhindern?

In Adobe Journey Optimizer (AJO) kann die Änderung der standardmäßigen CSS-Blöcke im E-Mail-Header zu unerwarteten Formatierungsproblemen führen – insbesondere nach dem Entfernen von Inhaltsfragmenten. Solche Probleme treten auf Mobilgeräten deutlicher zutage und können zu Layout-Verschiebungen oder Inkonsistenzen bei der Formatierung führen. Um dies zu verhindern, verwenden Sie die Funktion „Themen“, um benutzerdefiniertes CSS sicher anzuwenden, ohne die vom System generierten CSS-Stile zu ändern.

Weitere Informationen zur E-Mail-Formatierung finden Sie auf [dieser Seite](../email/get-started-email-design.md).

+++


+++ Warum funktionieren Fragmente mit bearbeitbaren Feldern nicht?

In Adobe Journey Optimizer werden Fragmente mit bearbeitbaren Feldern möglicherweise nicht korrekt geladen oder unerwartet dupliziert, wenn sie zu Vorlagen hinzugefügt werden. Das Problem betrifft normalerweise bestimmte Fragmente in allen Umgebungen. Um dies zu beheben, überprüfen Sie die Fragmentkonfiguration, überprüfen Sie sie auf widersprüchliche bearbeitbare Felddefinitionen und testen Sie sie in einer Entwicklungs-Sandbox, bevor Sie sie erneut veröffentlichen.

Weitere Informationen zu benutzerdefinierten Fragmenten finden Sie [auf dieser Seite](../content-management/customizable-fragments.md).

+++

+++ Warum werden HTML-Fragmente in E-Mails nicht richtig angezeigt?

HTML-Fragmente werden in E-Mails ggf. nicht ordnungsgemäß gerendert und in vielen Fällen als **Fragment-IDs** anstatt als tatsächlicher Content angezeigt. Im Gegensatz zu visuellen Fragmenten müssen HTML-Fragmente sorgfältig konfiguriert werden. Um dieses Problem zu beheben, befolgen Sie in Ihren E-Mail-Kampagnen Best Practices für die Verwendung von **visuellen und HTML-Ausdrucksfragmenten**.

Weitere Informationen zu HTML-Fragmenten finden Sie [auf dieser Seite](../content-management/fragments.md).

+++

+++ Warum verschwinden E-Mail-Vorlagen und Inhalte aus unveröffentlichten Journeys?

Beim Bearbeiten von E-Mail-Vorlagen in einer unveröffentlichten Journey können die Inhalte und Vorlagen bestimmter E-Mails unerwartet verschwinden. Dies kann zu Überarbeitungsbedarf und Verzögerungen führen. Um das Risiko für das Auftreten dieses Problems zu verringern, vermeiden Sie gleichzeitige Bearbeitungen, begrenzen Sie die Anzahl der geöffneten Registerkarten und speichern Sie Änderungen regelmäßig.

Weitere Informationen zu Vorlagen finden Sie [auf dieser Seite](../email/use-email-templates.md).

+++

+++ Warum wird im Modus „Eigenen Code schreiben“ das Feld „E-Mail-Preheader“ nicht angezeigt? 

Im Modus **Eigenen Code schreiben** wird unter der Funktion **E-Mail-Text bearbeiten** das Eingabefeld „Preheader“ nicht angezeigt. Um Preheader-Text einzuschließen, müssen Benutzende **den Preheader mit ihrem benutzerdefinierten HTML-Content manuell codieren**.

[Auf dieser Seite](../email/header-parameters.md) erfahren Sie mehr über die Konfiguration von E-Mail-Preheadern.

+++

+++ Warum gibt es bei der Verwendung einer HTML-Komponente in E-Mail-Vorlagen eine Diskrepanz im Link-Verhalten?  

Beim Hinzufügen einer **HTML-Komponente** zu einer E-Mail-Vorlage verhalten sich Links je nach **E-Mail-Client**, **Anzeigemodus** oder **Gerät/Browser** unterschiedlich. Anker-Links zum Beispiel können in der **Nebeneinander-Ansicht von Outlook** anders funktionieren als in der Vollbildansicht. Beachten Sie diese Unterschiede beim Gestalten von E-Mail-Vorlagen und beim Testen über verschiedene Clients und Geräte hinweg.

Siehe auch Best Practices zur Gestaltung von E-Mails [auf dieser Seite](../email/get-started-email-design.md).

+++


+++ Wie kann man verhindern, dass in Berichten E-Mail-Tracking-Links fehlen?

Fehlendes Linktracking in Adobe Journey Optimizer tritt auf, wenn E-Mail-URLs dynamische Variablen verwenden und nicht mit „http“ beginnen oder wenn Logikanweisungen im URL-Feld platziert werden. Um dieses Problem zu beheben, stellen Sie sicher, dass alle URLs mit „http“ beginnen, vermeiden Sie die Verwendung von Logik im URL-Feld und verschieben Sie komplexe Personalisierungslogik in die HTML-Inhalte oder vorverarbeiteten Attribute.

Weitere Informationen zum E-Mail-Tracking finden Sie auf [dieser Seite](../email/message-tracking.md).

+++

+++ Wie behebe ich beim Einrichten von per API ausgelösten Transaktions-E-Mail-Kampagnen einen Mail Exchanger-Fehler? 

Wenn beim Erstellen einer Kanalkonfiguration für eine per API ausgelöste Transaktions-E-Mail-Kampagne in Adobe Journey Optimizer ein MX-Fehler (Mail Exchanger) auftritt, kann dies auf **DNS-Fehlkonfigurationen** oder **DMARC-Einschränkungen** zurückzuführen sein. Um dieses Problem zu beheben, stellen Sie sicher, dass Ihr DNS korrekt konfiguriert ist, und vergewissern Sie sich, dass Ihre Domain die Anforderungen an **Domain-based Message Authentication, Reporting, and Conformance (DMARC)** erfüllt.

[Auf dieser Seite](../configuration/dmarc-record-update.md) erfahren Sie mehr über DMARC-Richtlinien für E-Mails.

Siehe auch [Dokumentation zu per API ausgelösten Kampagnen](../campaigns/api-triggered-campaigns.md).
+++

## Push-Kanal {#ajo-troubleshooting-push}

+++ Kann ein Profil in Adobe Journey Optimizer verschiedene Push-Token aufweisen?

Bei der Implementierung von Push-Benachrichtigungen in Journey Optimizer können einem einzelnen Profil tatsächlich verschiedene Push-Token mit unterschiedlichen Geräten zugeordnet sein. Bei einer Push-Benachrichtigungskampagne verwaltet Journey Optimizer diese Token und stellt sicher, dass das Zielgruppenprofil über alle zugehörigen Geräte erreicht werden kann.

Weitere Informationen zur Push-Konfiguration finden Sie auf [dieser Seite](../push/push-configuration.md).

Siehe auch [Datenfluss von Push-Benachrichtigungen](../push/push-gs.md), um zu verstehen, wie Token End-to-End registriert und verwaltet werden.

+++

+++ Warum werde ich beim Klicken auf eine Push-Nachricht nicht zur konfigurierten Web-URL umgeleitet?  

Wenn Push-Benachrichtigungen nicht zur vorgesehenen Web-URL umleiten, kann dies an einer falschen Konfiguration der Klickaktion oder an deaktivierten Einstellungen für Push-Benachrichtigungen liegen. Stellen Sie sicher, dass die **Klickaktion** für die Push-Benachrichtigung korrekt eingestellt ist und dass **automatische Anzeige und Tracking** von Push-Benachrichtigungen aktiviert sind, um das Problem zu beheben.

Weitere Informationen zur Push-Konfiguration finden Sie auf [dieser Seite](../push/push-configuration.md).

+++

+++ Warum schlagen Push-Benachrichtigungen nach der Aktualisierung der App-Anmeldeinformationen fehl?

Abgelaufene oder falsch konfigurierte Push-Anmeldeinformationen - z. B. ein APNs-Zertifikat für iOS oder ein FCM-Schlüssel für Android - führen zu Bereitstellungsfehlern im Hintergrund. Journey Optimizer kann keine Benachrichtigungen senden, wenn die in der Konfiguration des Push-Kanals gespeicherten Anmeldeinformationen nicht mehr mit den bei der Geräteplattform registrierten übereinstimmen. Aktualisieren Sie die Anmeldeinformationen in der Konfiguration des Push-Kanals und überprüfen Sie, ob die zugehörige Mobile-App-Oberfläche erneut veröffentlicht wird.

Erfahren Sie (auf dieser Seite), wie [&#x200B; Push-Anmeldeinformationen &#x200B;](../push/push-gs.md).

Siehe auch die [Dokumentation zur Konfiguration von Push-Kanälen](../push/push-configuration.md).

+++


## SMS-Kanal {#ajo-troubleshooting-sms}

+++ Warum werden meine Transaktions-SMS nicht zugestellt, obwohl das Einverständnis auf `marketing.sms.value=y` gesetzt ist?

Wenn eine Empfängerin bzw. ein Empfänger auf eine SMS mit **STOPP** antwortet, werden alle zukünftigen Nachrichten von dieser kurzen Nummer blockiert – einschließlich Transaktionsnachrichten. Um einen unterbrechungsfreien Versand von Transaktions-SMS zu gewährleisten, konfigurieren und senden Sie sie über eine **separate kurze Nummer**, von der sich die Empfängerinnen und Empfänger noch nicht abgemeldet haben.

[Auf dieser Seite](../sms/sms-opt-out.md) erfahren Sie mehr über die Opt-out-Konfiguration für SMS-Nachrichten.

+++

+++ Warum schlägt der SMS-Versand fehl, obwohl der Kanal konfiguriert ist?

SMS-Versandfehler nach der Kanaleinrichtung werden meist durch falsche Provider-API-Anmeldeinformationen, eine fehlende Übereinstimmung zwischen der Absender-ID und dem, was der Provider registriert hat, oder Routing-Einschränkungen auf Provider-Ebene verursacht. Überprüfen Sie, ob der in Journey Optimizer eingegebene API-Schlüssel, das Passwort und die Absenderdetails genau mit dem übereinstimmen, was Ihr SMS-Anbieter bereitgestellt hat. Senden Sie dann eine Testnachricht, um die Verbindung zu bestätigen, bevor Sie eine Kampagne starten.

Erfahren Sie auf dieser Seite , wie Sie [&#x200B; SMS-Anbieter &#x200B;](../sms/sms-configuration.md).

+++

+++ Wie kann ich sicherstellen, dass sich ein Profil von der SMS-Kommunikation abgemeldet hat?

Wenn ein Profil den Text STOP schreibt, aktualisiert Journey Optimizer das SMS-Einverständnisattribut des Profils. Um den aktuellen Opt-out-Status zu überprüfen, öffnen Sie das Profil in der Experience Platform-Benutzeroberfläche und überprüfen Sie die Einverständnisfelder unter **Datenschutz** > **Einverständnisse**. Überprüfen Sie zur Fehlerbehebung bei Campaign auch die Ausschlussgründe im Kampagnenbericht . Opt-out-Profile werden unter der **Ausgeschlossen** mit dem Grund „Opt-out“ angezeigt.

Weitere Informationen zur Handhabung des SMS-Opt-outs [&#x200B; Sie auf dieser Seite](../sms/sms-opt-out.md).

+++

## In-App-Kanal {#ajo-troubleshooting-inapp}

+++ Warum kann ich keine Berichte zum In-App-Kanal in Customer Journey Analytics erstellen?

Probleme beim Reporting für den **In-App-Kanal** in Adobe Customer Journey Analytics hängen oft mit falsch konfigurierten **Datenansichten**, **Datensätzen** oder **Schemaaktualisierungen** zusammen. Stellen Sie sicher, dass diese Konfigurationen korrekt angewendet sind, um das Problem zu beheben.

Siehe auch die Dokumentation zu [Journey Optimizer All-Time Reports](../reports/report-gs-cja.md).

+++

+++ Warum wird meine In-App-Nachricht Benutzern nicht angezeigt?

In-App-Nachrichten erfordern, dass Adobe Experience Platform Mobile SDK korrekt installiert und die Messaging-Erweiterung in der App registriert ist. Wenn die Nachricht nicht angezeigt wird, stellen Sie sicher, dass die SDK initialisiert wurde, bevor die App versucht, In-App-Nachrichten abzurufen, dass die richtige Programmoberfläche (Bundle-ID) in Journey Optimizer konfiguriert ist und dass sich die Kampagne im Status **Live** befindet. Bestätigen Sie außerdem, dass das Profil die Zielgruppenkriterien erfüllt und noch nicht durch eine Häufigkeitsregel begrenzt wurde.

Erfahren Sie (auf dieser Seite), wie Sie [&#x200B; In-App-Kanal &#x200B;](../in-app/inapp-configuration.md).

+++

+++ Warum wird meine In-App-Kampagne nicht im erwarteten Ereignis ausgelöst?

In-App-Kampagnen-Trigger basierend auf Ereignisnamen, die genau zwischen der SDK-Implementierung Ihrer App und der in Journey Optimizer definierten Trigger-Bedingung übereinstimmen müssen. Wenn die Schreibweise, die Schreibweise oder die Payload-Struktur des Ereignisses nicht übereinstimmen, kann der Trigger nicht ausgelöst werden. Verwenden Sie das Adobe Experience Platform Assurance-Tool, um SDK-Live-Ereignisse zu untersuchen und sie mit der Trigger-Konfiguration Ihrer Kampagne zu vergleichen.

Erfahren Sie (auf dieser Seite), wie Sie [&#x200B; In-App-Nachricht erstellen &#x200B;](../in-app/create-in-app.md) konfigurieren.

+++


## Inhaltskarten {#ajo-troubleshooting-content-cards}

+++ Warum werden in der App keine Inhaltskarten angezeigt?

Für Inhaltskarten müssen Adobe Experience Platform Mobile SDK und **Messaging SDK** in der App installiert, registriert und konfiguriert werden. Im Gegensatz zu Push- oder In-App-Nachrichten werden Inhaltskarten nicht automatisch gerendert. Ihre App muss die Messaging-SDK-APIs explizit aufrufen, um verfügbare Karten abzurufen und sie dann in Ihrer Benutzeroberfläche zu rendern. Wenn keine Karten angezeigt werden, verwenden Sie **Adobe Experience Platform Assurance**, um zu überprüfen, ob Entscheidungsanfragen beim Auslösen des Target-Ereignisses ausgelöst werden und ob die Antworten von Edge Network zurückgegeben werden.

Erfahren Sie auf dieser Seite , wie Sie die Unterstützung für Inhaltskarten in Mobile [&#x200B; konfigurieren](../content-card/content-card-configuration-sdk.md).

+++

+++ Benötigen Inhaltskarten, dass der Benutzer Berechtigungen für Push-Benachrichtigungen erteilt?

Nein. Inhaltskarten sind stumm und persistent - sie verlassen sich nicht auf Push-Berechtigungen auf Betriebssystemebene und sind nicht von dem Benachrichtigungs-Opt-in-Status eines Benutzers betroffen. Dies macht sie zu einem nützlichen Fallback-Kanal, um Benutzende zu erreichen, die Push-Benachrichtigungen deaktiviert haben. Die Karten werden von der Edge Network abgerufen, während sich der Benutzer in der Sitzung befindet und in der Benutzeroberfläche Ihrer App angezeigt wird.

Weitere Informationen zum Inhaltskarten-Kanal [auf dieser Seite](../content-card/get-started-content-card.md).

+++

+++ Warum werden Inhaltskarten-Impressions nicht in Kampagnenberichten angezeigt?

Impressionen und Interaktionen von Inhaltskarten (Klicks, Abweisungen) werden nicht automatisch verfolgt. Ihre Mobile App muss Tracking-Ereignisse explizit über den Messaging-SDK an Adobe zurücksenden, nachdem eine Karte gerendert und Benutzer mit ihr interagiert haben. Wenn diese Tracking-Aufrufe in der Implementierung fehlen, zeigen Berichte selbst dann keine Impressionen an, wenn die Karten korrekt bereitgestellt werden. Überprüfen Sie, ob die Tracking-Aufrufe in **Assurance ausgelöst werden** bevor Sie die Kampagnenkonfiguration untersuchen.

Erfahren Sie (auf dieser Seite), wie [&#x200B; auf Berichte &#x200B;](../content-card/content-card-report.md) Inhaltskarte zugreifen können.

Siehe auch [Konfiguration der Inhaltskarte für SDK](../content-card/content-card-configuration-sdk.md) für die erforderlichen Tracking-Aufrufe.

+++

## WhatsApp {#ajo-troubleshooting-whatsapp}

+++ Warum werden meine WhatsApp-Nachrichten nicht gesendet?

Für den Versand von WhatsApp-Nachrichten müssen zwei Bedingungen erfüllt sein: Der Empfänger muss sich explizit für den Empfang von WhatsApp-Nachrichten von Ihrer Marke entschieden haben, und die Nachricht muss eine **vorab genehmigte Nachrichtenvorlage) verwenden** die bei der WhatsApp Business-API registriert ist. Wenn eine der Bedingungen nicht erfüllt ist, wird die Nachricht von der WhatsApp-Plattform vor dem Versand stillschweigend blockiert. Überprüfen Sie den Opt-in-Status in den Einverständnisattributen des Empfängerprofils und bestätigen Sie, dass die Vorlage in Ihrem WhatsApp Business **Konto den** Genehmigt“ hat.

Erfahren Sie auf dieser Seite , wie Sie [&#x200B; WhatsApp-Kanal &#x200B;](../whatsapp/whatsapp-configuration.md).

+++

+++ Warum wird meine WhatsApp-Nachricht mit einem Vorlagenfehler abgelehnt?

Die WhatsApp Business-API erlaubt nur vorab genehmigte Nachrichtenvorlagen für ausgehende geschäftlich initiierte Nachrichten. Freiformnachrichten sind nur innerhalb eines **24-Stunden-Kundendienstfensters zulässig** d. h. innerhalb von 24 Stunden, nachdem der Kunde eine Nachricht zuerst an Ihre Marke gesendet hat. Wenn Ihre Nachricht abgelehnt wird, stellen Sie sicher, dass die Vorlage an Meta gesendet und von diesem genehmigt wurde, dass die Vorlagenvariablen (Platzhalter) in der Journey Optimizer-Nachricht genau mit der genehmigten Vorlagenstruktur übereinstimmen und dass die richtige Vorlage in der Kampagne oder der Journey-Aktion ausgewählt ist.

Erfahren Sie (auf dieser [), wie Sie WhatsApp-Nachrichten &#x200B;](../whatsapp/create-whatsapp.md).

+++

+++ Wie erfasse und verifiziere ich das WhatsApp-Opt-in von Benutzern?

WhatsApp erfordert ein explizites Opt-in, bevor Sie Marketing-Nachrichten senden können. Das Opt-in kann über jeden Kanal erfasst werden, den Ihre Marke steuert - z. B. ein Web-Formular, ein doppeltes SMS-Opt-in oder ein In-App-Einverständnisbildschirm -, solange der Prozess klar und dokumentiert ist. Aktualisieren Sie nach der Erfassung das WhatsApp-Einverständnisattribut des Profils in Adobe Experience Platform. Um den aktuellen Einverständnisstatus für ein Profil zu überprüfen, öffnen Sie das Profil in der Experience Platform-Benutzeroberfläche und überprüfen Sie den Abschnitt **Einverständnisse**. Das Senden an Profile ohne gültiges Einverständnis verstößt gegen die WhatsApp-Geschäftsrichtlinien und kann dazu führen, dass Ihr Konto gesperrt wird.

Erste Schritte mit dem WhatsApp-Kanal [auf dieser Seite](../whatsapp/get-started-whatsapp.md).

+++

## Daten-Management {#ajo-troubleshooting-data-management}

+++ Wie werden TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet, wenn Sie eine neue Sandbox erstellen?

Unternehmen, die in Adobe Journey Optimizer neue Sandboxes bereitstellen, haben die Frage aufgeworfen, wie TTL-Einstellungen (Time-to-Live) auf Profil- und Data-Lake-Datensätze angewendet werden. TTL-Einstellungen wirken sich nicht auf bestehende Sandboxes aus und werden automatisch nur auf neu bereitgestellte angewendet.

Weitere Informationen zur TTL von Datensätzen finden Sie auf [dieser Seite](../data/datasets-ttl.md).

+++

+++ Warum wird ein Datensatz nicht für das Echtzeit-Kundenprofil aktiviert?

Damit ein Datensatz die profilbasierte Personalisierung und Journey-Bedingungen in Journey Optimizer unterstützt, müssen zwei Anforderungen erfüllt sein: Für das zugrunde liegende XDM-Schema muss **Profile** aktiviert sein, und der Datensatz selbst muss für **Echtzeit-Kundenprofil** in der Experience Platform-Benutzeroberfläche aktiviert sein. Wenn eines von beiden fehlt, werden die Daten in den Data Lake aufgenommen, aber nicht in einheitlichen Profilen zusammengeführt. Stellen Sie außerdem sicher, dass der Datensatz mindestens ein Identitätsfeld enthält, das einem erkannten Namespace zugeordnet ist.

Erfahren Sie (auf [&#x200B; Seite), wie Sie Datensätze &#x200B;](../data/get-started-datasets.md).

Siehe auch [Übersicht über das Daten-Management](../data/gs-data.md), um die vollständige Setup-Checkliste zu erhalten.

+++

+++ Wie kann ich Datenaufnahmefehler überwachen und beheben?

Aufnahmefehler werden im Dashboard **Überwachung** von Adobe Experience Platform unter **Quellen** > **Datenflüsse** angezeigt. Häufige Ursachen sind Fehler bei der Schemavalidierung (ein Feld in den Quelldaten stimmt nicht mit dem XDM-Schema überein), fehlende erforderliche Identitätsfelder oder falsch formatierte JSON-Payloads. Öffnen Sie den fehlgeschlagenen Batch-Datensatz, um den spezifischen Fehler-Code und die betroffenen Zeilen anzuzeigen. Korrigieren Sie die Quelldaten und nehmen Sie die Schemazuordnung erneut auf bzw. passen Sie sie an, wenn sich das Quellformat geändert hat.

Weitere Informationen zu Schemata und zur Dateneinrichtung [&#x200B; Sie auf dieser Seite](../data/gs-data.md).

+++


## Profile und Zielgruppen-Management {#ajo-troubleshooting-audiences}

+++ Wie lassen sich Diskrepanzen bei der Zielgruppengröße beheben?

Die Zahl der verarbeiteten Einträge in der Funktion **Zielgruppe lesen** von Adobe Journey Optimizer kann niedriger sein als die erwartete Zielgruppengröße. Dieses Problem hängt häufig mit falsch konfigurierten Namespaces zusammen, was dazu führt, dass Profile aus Journeys ausgeschlossen werden. Die Lösung umfasst das Überprüfen und Korrigieren von Namespace-Konfigurationen, das Überprüfen der entsprechenden Dokumentation und das Anpassen von Prioritäten, um reibungslosere Abläufe in Adobe Journey Optimizer sicherzustellen.

Weitere Informationen zur Aktivität **Zielgruppe lesen** in Journeys finden Sie [auf dieser Seite](../building-journeys/read-audience.md).

+++

+++ Warum schlagen Profilaktualisierungen fehl?

In Adobe Journey Optimizer werden bestimmte Feldwerte ggf. nicht richtig aktualisiert, nachdem in einer Journey eine Aktivität vom Typ **Profil aktualisieren** ausgeführt wurde. In einigen Fällen können aktualisierte Felder verschwinden oder zu ihrem vorherigen Status zurückkehren. Prüfen Sie, ob Regeln oder Bedingungen miteinander in Konflikt stehen, prüfen Sie die Berechtigungseinstellungen, verwenden Sie einen eindeutigen Datensatz für die Aktivität **Profil aktualisieren** und vergewissern Sie sich, dass nicht gleichzeitig ein anderer Aufnahmeprozess in dasselbe Profil schreibt.

Weitere Informationen über die Aktivität **Profil aktualisieren** finden Sie auf [dieser Seite](../building-journeys/update-profiles.md).

+++

+++ Warum stimmt die Profilanzahl beim Eintritt in eine Journey nicht mit der Zahl in der zugehörigen Zielgruppe überein?

Die Diskrepanz kann auftreten, wenn der Journey den Profilschnappschuss eines vorherigen Tages verwendet, wenn der aktuelle Tagesschnappschuss zum Zeitpunkt der Journey-Ausführung nicht verfügbar ist. Um zu untersuchen, überprüfen Sie, wann Ihr täglicher Segmentierungsauftrag zuletzt ausgeführt wurde und ob der Journey ausgelöst wurde, bevor der Snapshot bereit war.

Weitere Informationen zur Aktivität **Zielgruppe lesen** und zum Zeitplanverhalten finden [&#x200B; auf dieser Seite](../building-journeys/read-audience.md).

+++

+++ Warum zeigt die Zielgruppenauswahl in Kampagnen und Journeys unterschiedliche Profilzahlen an?

Möglicherweise stellen Sie fest, dass dieselbe Zielgruppe in Kampagnen eine andere Profilanzahl anzeigt als in Journeys. Dies geschieht, weil jede Funktion verschiedene APIs zum Abrufen von Zielgruppendaten verwendet, die unterschiedliche Werte zurückgeben können.

Dieses Verhalten ist normal und wirkt sich nicht auf die Kampagnenausführung aus. Die richtigen Profile werden weiterhin angesprochen. Um die tatsächliche Zielgruppengröße zu prüfen, gehen Sie zu **[!UICONTROL Kundin bzw. Kunde]** > **[!UICONTROL Zielgruppen]** und wählen Sie Ihre Zielgruppe aus.

+++


+++ Wie können Probleme mit der Zielgruppenpopulation gelöst werden?

Probleme mit der Zielgruppenpopulation können auftreten, wenn Komponenten oder Ressourcen fehlen (oft aufgrund von falsch konfigurierten Berechtigungen, Bereitstellungen oder Genehmigungen). Um die Probleme zu beheben, prüfen Sie zunächst die Berechtigungen, stellen Sie eine korrekte Bereitstellung sicher und überprüfen Sie die Genehmigungen. Wenn das Problem weiterhin besteht, eskalieren Sie den Fall und stimmen Sie sich mit Support-Teams ab, um eine vollständige Lösung zu finden.

Weitere Informationen zum Verwalten von Audiences [auf dieser Seite](../audience/about-audiences.md).

+++

+++ Warum ist die Anzahl der ansprechbaren Profile in einem kurzen Zeitraum deutlich gestiegen? 

Die Metrik **Ansprechbare Profile** gibt die Anzahl der eindeutigen Profile an, die von Journeys oder Kampagnen in den letzten 12 Monaten angesprochen wurden. Ein plötzlicher Anstieg kann die Folge von Journey oder Kampagnen sein, die große Zielgruppen ansprechen, die in letzter Zeit nicht kontaktiert wurden, oder von Änderungen an Datensätzen, die für den Profil-Service aktiviert sind.

Um dieses Problem zu untersuchen und zu beheben, müssen Sie die Profilzählungslogik verstehen, Journey und Kampagnen untersuchen, die auf große Zielgruppen abzielen, Zielgruppen angemessen filtern, Datensatzänderungen überwachen und möglicherweise die adressierbare Zielgruppengröße reduzieren.

Erfahren Sie in der Dokumentation zum Lizenznutzungs-Dashboard , wie Sie Probleme mit Engageable Profiles beheben und die Lizenznutzung [&#x200B; Unternehmens &#x200B;](../audience/license-usage.md#troubleshooting-engageable-profiles).

+++

+++ Warum werden anhand von Datumsfunktionen E-Mails an Personen außerhalb der beabsichtigten Zielgruppe gesendet?

E-Mails werden ggf. an Empfängerinnen und Empfänger gesendet **, die die angegebenen Zielgruppenkriterien nicht erfüllen**. Beispielsweise können Mitglieder mit Einlösungsterminen **vor dem 4. Juli 2025** E-Mails erhalten, die nur für Mitglieder nach diesem Datum bestimmt sind. Dieses Verhalten kann aus **falsch konfigurierten Zielgruppensegmentierung** oder **unerwarteten Änderungen in der Profilqualifikationslogik)**. Überprüfen Sie die Zielgruppendefinition und testen Sie sie mit Beispielprofilen, um sicherzustellen, dass die Datumslogik korrekt angewendet wird.

Weitere Informationen zu Datumsfunktionen finden Sie auf [dieser Seite](../building-journeys/functions/date-functions.md).

+++

+++ Warum übersteigt sie Summe aus „Zugestellt“ + „Ausschlüsse“ in den Kampagnenberichten meine Zielgruppengröße?

In Kampagnenberichten kann es vorkommen, dass die Summe aus **Zugestellt** und **Ausschlüsse** die ursprüngliche Zielgruppengröße überschreitet. Dies geschieht, weil die Metrik **Ausschlüsse** alle Ausschlussereignisse zählt, einschließlich doppelter Ausschlussereignisse für dasselbe Profil. Wenn ein Profil während einer Kampagne mehrmals ausgeschlossen wird, wird jedes Ereignis separat gezählt.

**Beispiel**: Eine an 94.000 Profile gerichtete Kampagne zeigt 69.000 zugestellte Nachrichten und 37.000 Ausschlüsse, also insgesamt 106.000 Profile. Dies übersteigt die ursprünglichen 94.000 Zielprofile. Dieses Verhalten ist normal.

Informationen zum Unterschied zwischen Ausschlussereignissen insgesamt und eindeutigen Profilausschlüssen finden Sie unter [Erklärung zur Zählung von Ausschlüssen](../reports/exclusion-list.md#exclusion-list).

Erfahren Sie mehr über [Kampagnenberichte](../reports/campaign-global-report-cja.md) und [Berichtsmetriken](../reports/global-report-components-cja.md).

+++

+++ Wie kann ich beim Speichern von Journeys Probleme bei der Zielgruppenauswahl und Chrome-Fehler beheben?

Das Hinzufügen von Zielgruppen zu Journey-Bedingungen kann manchmal zu **Anwendungsabstürzen** oder einem **Aw Snap-Fehler** in Chrome führen, einschließlich Fehlern beim Speichern von Journeys. Solche Probleme stehen häufig im Zusammenhang mit **Chromium-Services**. Um sie zu beheben, wenden Sie eine **Browser-Aktualisierung** an, löschen Sie den Browser-Cache oder versuchen Sie es mit einer anderen Browser-Sitzung.

Weitere Informationen zum [Navigieren in der Benutzeroberfläche von Journey Optimizer](user-interface.md).

+++

## Journeys {#ajo-troubleshooting-journeys}

Informationen zu Journeys finden Sie in den folgenden Abschnitten zur Fehlerbehebung:

* [Fehlerbehebung vor dem Testen der Journey](../building-journeys/troubleshooting.md)
* [Fehlerbehebung bei eingehenden Aktionen in Journeys](../building-journeys/troubleshooting-inbound.md)
* [Fehlerbehebung bei der Live-Journey-Ausführung](../building-journeys/troubleshooting-execution.md)
* [Fehlerbehebung bei benutzerdefinierten Aktionen](../action/troubleshoot-custom-action.md)


+++ Warum gehen beim Erstellen einer neuen Journey-Version Ausdrücke verloren?  

Beim Erstellen einer neuen Journey-Version können **Ausdrücke in bestimmten Schritten** verloren gehen, was Fehler verursacht und eine erneute manuelle Eingabe erforderlich macht. Gehen Sie wie folgt vor: **Duplizieren Sie die Journey**, testen Sie auf Reproduzierbarkeit, **vermeiden Sie das Neuladen des Browsers** und verwenden Sie für ältere Journeys die **aktualisierte Arbeitsfläche**.

Weitere Informationen zum Duplizieren einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum steigen Profile vorzeitig aus Journeys aus? 

Profile steigen ggf. unerwartet aus einer Journey aus, ohne einen angegebenen Knoten zu durchlaufen, wenn die **Bedingung zur Überprüfung des Feedback-Status** von gesendeten Nachrichten falsch konfiguriert ist. Gehen Sie wie folgt vor: Überprüfen Sie die **Bedingungslogik**, implementieren Sie **alternative Logik** oder wenden Sie sich an Ihr **Implementierungs-Team**.

Siehe auch [Richtlinien zum Entwerfen von Journeys](../building-journeys/using-the-journey-designer.md).

+++


+++ Warum steigen Profile unerwartet aus Journeys aus?

Profile steigen ggf. unerwartet aus einer Journey aus, wenn **Ereignisbegrenzung** auftritt, wodurch einige Profile verworfen werden, falls die Anzahl der verarbeiteten Ereignisse die Systemkapazität überschreitet. Um Profilaustritte zu reduzieren, machen Sie sich mit den **Systembeschränkungen** vertraut, überwachen Sie **Ereignisspitzen** und optimieren Sie den **Datenfluss**, um das Überschreiten von Schwellenwerten zu verhindern.

Siehe auch [Schutzmechanismen für Journeys](../start/guardrails.md#decisioning-guardrails).

+++


+++ Warum löst mein Ereignis nicht die beabsichtigte Journey aus?  

Bei Ereignissen kann der Trigger einer Journey fehlschlagen, selbst wenn alle Kriterien erfüllt sind, falls sie **über Abfrage-Services erstellt** anstatt an den **Data Collection Core Service (DCCS)** gestreamt werden. Gehen Sie wie folgt vor: Überprüfen Sie die Ereigniskonfiguration, stellen Sie sicher, dass Ereignisse **direkt an DCCS gestreamt** werden und überprüfen Sie die Funktionalität mit dem **Testmodus**.

Weitere Informationen zu Ereignissen finden Sie [auf dieser Seite](../event/about-events.md).

Siehe auch [Schutzmechanismen für Journey-Ereignisse](../start/guardrails.md#events-g).

+++


+++ Wie kann ich Probleme beim Auslösen einer Journey nach Zielgruppenänderungen in Adobe Journey Optimizer beheben? 

Wenn eine Journey nach Änderungen an der zugehörigen Zielgruppe (z. B. Änderungen an der Zusammenführungsrichtlinie) nicht mehr ausgelöst wird, kann es zu Unterbrechungen der Datenflüsse kommen. Gehen Sie wie folgt vor: **Duplizieren und veröffentlichen Sie die Journey** mit den aktualisierten Zielgruppeneinstellungen neu, um dafür zu sorgen, dass Trigger ordnungsgemäß funktionieren.

Weitere Informationen zum Duplizieren einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Warum tritt bei einer benutzerdefinierten Aktion, die einen externen Drittanbieter-Endpunkt aufruft, eine Zeitüberschreitung auf?

Zeitüberschreitungsfehler können auftreten, wenn eine **benutzerdefinierte Aktion** einen externen Drittanbieter-Endpunkt aufruft. Gehen Sie wie folgt vor: Stellen Sie sicher, dass der **Endpunkt zugänglich ist**, überprüfen Sie **Server-Protokolle**, vergewissern Sie sich, dass **keine Blockierung von Adobe** erfolgt, aktualisieren Sie Endpunktkonfigurationen nach Bedarf und **testen Sie nach Aktualisierungen**. Achten Sie zudem auf **Zeitüberschreitungsspezifikationen für APIs**.

[Auf dieser Seite](../configuration/throttling.md) erfahren Sie mehr über die Drosselungs-API für Journeys.

Siehe auch [Dokumentation zur Integration mit externen Systemen](../configuration/external-systems.md).

+++

+++ Welche Schritte sollten Sie unternehmen, wenn bei der Veröffentlichung einer Zielgruppe von einer Journey der Fehler 403 mit der Meldung **INVALID_ACCESS** oder **Kein Zugriff auf diese dataId=XX** gewährt?

Um diesen Fehler zu beheben, bitten Sie Ihre bzw. Ihren Admin, sicherzustellen, dass Ihr Benutzerprofil Zugriff auf die erforderlichen Datenansichten für die Zielgruppenveröffentlichung hat, und versuchen Sie dann erneut, die Zielgruppe zu veröffentlichen.

In [der Dokumentation zu Berechtigungen](../administration/permissions.md) erfahren Sie, wie Sie dieses Problem beheben können.

+++

## Regeln {#ajo-troubleshooting-rules}

+++ Warum funktioniert das Dropdown-Menü „Begrenzungsregeln“ nicht?

Probleme mit dem Dropdown-Menü **Begrenzungsregeln** treten häufig auf, wenn Regelsätze **falsch konfiguriert** oder **nicht aufrufbar** sind. Vergewissern Sie sich, dass alle Regelsätze richtig konfiguriert und verfügbar sind, um das Problem zu beheben.

[In diesem Abschnitt](../conflict-prioritization/rule-sets.md) erfahren Sie, wie Sie Begrenzungsregeln anwenden.

+++

+++ Warum wird auf meine Kampagne oder Journey keine Regel zur Frequenzlimitierung angewendet?

Regeln zur Frequenzlimitierung werden nur wirksam, wenn der Regelsatz explizit an die Kampagne oder den Journey angehängt wird. Wenn die Begrenzung nicht funktioniert, stellen Sie sicher, dass in den Kampagnen- oder Journey-Einstellungen der richtige Regelsatz ausgewählt ist, dass der Kanaltyp der Regel mit dem verwendeten Kanal übereinstimmt und dass die Regel den Status **Aktiv** hat. Überprüfen Sie außerdem, ob das Profil bereits in einer vorherigen Ausführung die Begrenzung erreicht hat, wodurch weitere Meldungen verhindert würden, selbst wenn die Regel korrekt konfiguriert erscheinen würde.

Erfahren Sie (auf dieser Seite), wie [&#x200B; Regeln für die Kanalbegrenzung &#x200B;](../conflict-prioritization/channel-capping.md).

+++

+++ Wie konfiguriere ich ruhige Stunden, um zu verhindern, dass Nachrichten nachts gesendet werden?

Ruhestunden sind zeitbasierte Ausschlussregeln, die in einem **Kanalregelsatz“ konfiguriert**. Definieren Sie das Blackout-Fenster (z. B. 22 Uhr bis 8 Uhr morgens) und wenden Sie den Regelsatz auf die entsprechenden Kampagnen oder Journey an. Wenn der Versand einer Nachricht für ruhige Zeiten geplant ist, behält Journey Optimizer die Nachricht entweder bis zum nächsten zulässigen Fenster bei oder verwirft sie je nach Regelkonfiguration.

Erfahren Sie (auf dieser Seite), wie [&#x200B; ruhige Stunden &#x200B;](../conflict-prioritization/quiet-hours.md).

+++

## Entscheidungsfindung {#ajo-troubleshooting-decisioning}

+++ Wie kann ich Probleme beim Erstellen von Angebotssammlungen beheben?

Probleme beim Erstellen von Angebotssammlungen treten häufig auf, wenn für Ihre Organisation **Kataloge nicht bereitgestellt wurden**. Gehen Sie wie folgt vor: Prüfen Sie, ob alle erforderlichen Kataloge korrekt bereitgestellt wurden, bevor Sie versuchen, Angebotssammlungen zu erstellen.

Weitere Informationen zu Angebotssammlungen finden Sie auf [dieser Seite](../offers/offer-library/creating-collections.md).

+++

+++ Warum kann ich nicht auf Offer Decisioning zugreifen?  

Bei der Integration von Adobe Target in eine Anwendung mithilfe von Adobe Journey Optimizer ist die Option **Offer Decisioning** möglicherweise nicht in der Datenstromkonfiguration verfügbar. Die Ursache sind normalerweise **Berechtigungseinstellungen** oder **Bereitstellungsbeschränkungen**. Gehen Sie wie folgt vor: Überprüfen Sie die Benutzerberechtigungen und stellen Sie sicher, dass die erforderliche Bereitstellung vorhanden ist.

Weitere Informationen zu den erforderlichen Berechtigungen für Offer Decisioning finden [auf dieser Seite](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++

+++ Warum wird ein Angebot nicht zurückgegeben, obwohl es die Eignungskriterien erfüllt?

Wenn ein qualifizierendes Angebot nicht in einer Entscheidungsantwort angezeigt wird, überprüfen Sie die folgende Reihenfolge: Überprüfen Sie, ob das Angebot den Status **Genehmigt** (nicht Entwurf) hat; bestätigen Sie, dass die Platzierungs-ID in der Anfrage mit der Darstellungsfläche des Angebots übereinstimmt; überprüfen Sie, ob für dieses Angebot ein Begrenzungslimit (insgesamt oder pro Profil) erreicht wurde; und stellen Sie sicher, dass die Sammlung und der Entscheidungsumfang korrekt konfiguriert sind. Verwenden Sie das **Simulation**-Tool in Experience Decisioning, um Angebotsantworten mit einem bestimmten Profil zu testen, ohne Live-Traffic zu senden.

Informationen zu den ersten Schritten mit Experience Decisioning [&#x200B; Sie auf dieser Seite](../experience-decisioning/gs-experience-decisioning.md).

+++


## Mehrsprachig {#ajo-troubleshooting-multilingual}

+++ Wie kann ich das Problem `Message validation error (CJMMAS - 1069-500)` beheben?

In Adobe Journey Optimizer verhindert ein mit der mehrsprachigen Funktion verknüpfter Nachrichtenvalidierungsfehler (CJMMAS - 1069-500), dass die Journey in den Testmodus versetzt oder veröffentlicht werden. Vergewissern Sie sich, dass alle Gebietsschema-Inhalte vollständig sind, dass die primäre Sprache korrekt festgelegt ist und dass keine erforderlichen Übersetzungsfelder leer sind, bevor Sie versuchen, zu veröffentlichen.

Weitere Informationen zu mehrsprachigem Inhalt finden Sie auf [dieser Seite](../content-management/multilingual-gs.md).

+++

+++ Warum stellt der Übersetzungsanbieter keine Verbindung in Journey Optimizer her?

Verbindungsfehler beim Übersetzungsanbieter werden in der Regel durch falsche API-Anmeldeinformationen oder eine fehlende Anbieterkonfiguration in den mehrsprachigen Einstellungen verursacht. Überprüfen Sie, ob der API-Schlüssel, die Endpunkt-URL und alle erforderlichen Authentifizierungstoken in Journey Optimizer genau mit dem übereinstimmen, was Ihr Übersetzungsanbieter bereitgestellt hat. Wenn die Anmeldeinformationen korrekt sind, überprüfen Sie, ob das Anbieterkonto über ein ausreichendes Kontingent oder einen aktiven Abonnementstatus verfügt, speichern Sie die Verbindung und testen Sie sie erneut.

Erfahren Sie (auf dieser Seite), wie [&#x200B; einen Übersetzungsanbieter &#x200B;](../content-management/multilingual-provider.md).

+++

+++ Was passiert, wenn eine Übersetzung für ein Gebietsschema fehlt?

Wenn für ein bestimmtes Gebietsschema keine Übersetzung bereitgestellt wurde, greift Journey Optimizer auf die Inhalte zurück, die in der **Primärsprache** (Fallback-Gebietsschema) definiert sind, die in Ihren Spracheinstellungen konfiguriert ist. Wenn kein Fallback konfiguriert ist, kann die Nachricht als leer gerendert werden oder die Validierung vor dem Senden schlägt fehl. Um dies zu verhindern, definieren Sie in Ihren mehrsprachigen Projekteinstellungen immer ein Fallback-Gebietsschema und stellen Sie sicher, dass alle Gebietsschemata genehmigte Übersetzungen haben, bevor Sie die Kampagne oder den Journey aktivieren.

Weitere Informationen zum Einrichten mehrsprachiger Inhalte [&#x200B; Sie auf dieser Seite](../content-management/multilingual-gs.md).

+++


## Konfiguration {#ajo-troubleshooting-config}

+++ Wie aktiviere ich TLS v1.3 für benutzerdefinierte Aktionen?  

Um beim Herstellen einer Verbindung zu Drittanbietersystemen die **Integrität und Sicherheit von Daten** zu wahren, sorgen Sie dafür, dass für Ihre benutzerdefinierten Aktionen Transport Layer Security (**TLS**) v1.3 aktiviert ist. Dadurch wird die Kommunikation geschützt und werden potenzielle Sicherheitslücken vermieden.

Weitere Informationen zur Konfiguration benutzerdefinierter Aktionen finden Sie [auf dieser Seite](../action/about-custom-action-configuration.md).

+++

+++ Warum kann ich direkt aus einer Abfrage in Adobe Journey Optimizer kein Dashboard erstellen? 

In Adobe Journey Optimizer lassen sich Dashboards nicht direkt aus Abfragen erstellen. Verwenden Sie zum Erstellen von Dashboards die verfügbaren **Funktionen zur Erstellung von Dashboards** in Adobe Experience Platform. Damit können Sie Abfragedaten effektiv visualisieren und analysieren.

Weitere Informationen zu Abfragen in Journey Optimizer [auf dieser Seite](../data/get-started-queries.md).

+++

+++ Warum werden meine Nachrichten von der Unterdrückungsliste blockiert?

Adressen werden nach Hardbounces, Spam-Beschwerden oder manuellen Hinzufügungen durch einen Administrator automatisch zur Unterdrückungsliste hinzugefügt. Nach der Unterdrückung erhält ein Profil unabhängig vom Kampagnen- oder Journey-Targeting keine Nachrichten von diesem Kanal. Öffnen Sie zur Untersuchung **Administration** > **Kanäle** > **Unterdrückungsliste** und suchen Sie nach der Adresse. Wenn die Unterdrückung irrtümlich hinzugefügt wurde, kann sie direkt aus der Schnittstelle entfernt werden. Überprüfen Sie bei Unterdrückungen von Hardbounces auch das zugrunde liegende Zustellbarkeitsproblem, bevor Sie die Adresse entfernen.

Erfahren Sie (auf dieser Seite), wie [&#x200B; Unterdrückungsliste &#x200B;](../configuration/manage-suppression-list.md).

+++

## APIs {#ajo-troubleshooting-apis}

+++ Wie kann ich Zugriffsprobleme bei der Abfrage-Service-API beheben?  

Zugriffsfehler bei Verwendung der **Abfrage-Service-API** über Postman oder ähnliche Tools werden in der Regel durch **unzureichende Berechtigungen** verursacht. Um dies zu beheben, überprüfen Sie die Benutzerberechtigungen, überprüfen Sie die API-Anmeldeinformationen mit den in Ihrer Organisation konfigurierten Rollen und geben Sie detaillierte Informationen an, um bei Bedarf zu unterstützen.

Weitere Informationen über Berechtigungen in Journey Optimizer [auf dieser Seite](../administration/permissions.md).

+++

+++ Wie behebe ich Fehler des Typs „429 - Zu viele Anfragen“ beim Aufrufen von Journey Optimizer-APIs?

Eine 429-Antwort bedeutet, dass Ihre Integration das API-Ratenlimit für den Endpunkt überschritten hat. Jede Journey Optimizer-API verfügt über definierte Durchsatzschwellen. Um dies zu beheben, implementieren Sie **exponentielles Backoff**-Logik in Ihrer Integration: Warten Sie die in der `Retry-After`-Antwortkopfzeile angegebene Dauer, bevor Sie es erneut versuchen. Überprüfen Sie für Anwendungsfälle mit anhaltendem hohem Volumen die Konfiguration der Drosselung und Begrenzung für Ihre benutzerdefinierten Aktionen und Datenquellen, um die API-Aufrufraten an die Systembeschränkungen anzupassen.

Weitere Informationen zu Einschränkungen bei Journey Optimizer [auf dieser Seite](../configuration/throttling.md).

Siehe auch die [Dokumentation zur Integration externer Systeme](../configuration/external-systems.md).

+++

+++ Warum wird meine API-ausgelöste Kampagne nach dem API-Aufruf nicht ausgeführt?

Wenn keine API-ausgelöste Kampagne ausgeführt wird, überprüfen Sie Folgendes: Die Kampagne befindet sich im **Live**-Status (nicht Entwurf oder gestoppt); der API-Aufruf enthält die richtige Kampagnen-ID im Endpunktpfad; die Anfrage-Payload entspricht dem von der Kampagne erwarteten Profilkennungsschema; und die verwendeten API-Anmeldeinformationen verfügen über die Berechtigung **Kampagnen verwalten**. Überprüfen Sie die Ausführungsprotokolle der Kampagne im Reporting-Dashboard, um festzustellen, ob das Profil empfangen, aber ausgeschlossen wurde oder ob der Aufruf die Kampagne überhaupt nicht erreicht hat.

Weitere Informationen über API-ausgelöste Kampagnen [auf dieser Seite](../campaigns/api-triggered-campaigns.md).

+++
