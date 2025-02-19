---
product: Journey Optimizer
audience: end-user
user-guide-title: Handbuch für Journey Optimizer
user-guide-description: Mit Journey Optimizer können Sie miteinander verbundene, kontextuelle und personalisierte Erlebnisse für Kunden erstellen und bereitstellen.
type: Documentation
solution: Journey Optimizer
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '2174'
ht-degree: 97%

---

# Hilfe zu Adobe Journey Optimizer {#using}

+ [Dokumentation zu Journey Optimizer](ajo-home.md)
+ Neue Funktionen {#whats-new}
   + [Frühzeitige Versionshinweise](using/rn/e-release-notes.md)
   + [Neueste Versionshinweise](using/rn/release-notes.md)
   + Frühere Versionshinweise {#previous-rn-new}
      + [2024](using/rn/release-notes-2024.md)
      + [2023](using/rn/release-notes-2023.md)
      + [2022](using/rn/release-notes-2022.md)
      + [2021](using/rn/release-notes-2021.md)
   + [Dokumentationsaktualisierungen](using/rn/documentation-updates.md)
   + [Verbesserte Journey-Arbeitsfläche](using/rn/new-canvas.md)
+ Erste Schritte{#get-started}
   + [Was ist Journey Optimizer?](using/start/get-started.md)
   + Schnellstartanleitungen{#quick-start}
      + [Übersicht](using/start/quick-start.md)
      + [Erste Schritte als Marketer](using/start/path/marketer.md)
      + [Erste Schritte als Datentechniker](using/start/path/data-engineer.md)
      + [Erste Schritte als Administrator](using/start/path/administrator.md)
      + [Erste Schritte als Entwickler](using/start/path/developer.md)
   + [Benutzeroberfläche](using/start/user-interface.md)
   + [Suchen, Filtern, Kategorisieren](using/start/search-filter-categorize.md)
   + [Barrierefreiheit](using/start/accessibility.md)
   + [Anwendungsfall-Playbooks](using/start/playbooks.md)
   + [Arbeiten mit dem KI-Assistenten](using/start/ai-assistant.md)
   + [Leitplanken](using/start/guardrails.md)
   + [Best Practices](using/start/best-practices.md)
+ Journeys {#orchestrate-journeys}
   + [Erste Schritte mit Journeys](using/building-journeys/journey.md)
   + Erstellen einer Journey{#create-journey}
      + [Erstellen Ihrer ersten Journey](using/building-journeys/journey-gs.md)
      + [Festlegen der Journey-Eigenschaften](using/building-journeys/journey-properties.md)
      + [Gestalten einer Journey](using/building-journeys/using-the-journey-designer.md)
      + [Testen einer Journey](using/building-journeys/testing-the-journey.md)
      + [Simulieren der Journey](using/building-journeys/journey-simulation.md)
      + [Veröffentlichen Ihrer Journey](using/building-journeys/publishing-the-journey.md)
      + [Live-Bericht in Ihrer Journey](using/building-journeys/report-journey.md)
   + Verwalten von Journeys{#manage-journey}
      + [Profileintrittsverwaltung](using/building-journeys/entry-management.md)
      + [Zeitzonen-Management](using/building-journeys/timezone-management.md)
      + [Optimierung des Versandzeitpunkts](using/building-journeys/send-time-optimization.md)
      + [Beenden der Journey](using/building-journeys/end-journey.md)
      + [Kopieren einer Journey in eine andere Sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Beheben von Fehlern in einer Journey](using/building-journeys/troubleshooting.md)
      + [Integrieren mit Intelligent Services](using/building-journeys/ai-services-overview.md)
   + Aktivitäten {#about-journey-building}
      + [Erste Schritte mit Journey-Aktivitäten](using/building-journeys/about-journey-activities.md)
      + [Allgemeine Ereignisse](using/building-journeys/general-events.md)
      + [Reaktion](using/building-journeys/reaction-events.md)
      + [Zielgruppen-Qualifizierung](using/building-journeys/audience-qualification-events.md)
      + [Bedingung](using/building-journeys/condition-activity.md)
      + [Warten](using/building-journeys/wait-activity.md)
      + [Lesen der Zielgruppe](using/building-journeys/read-audience.md)
      + [Integrierte Kanalaktionen](using/building-journeys/journeys-message.md)
      + [Benutzerdefinierte Aktionen](using/building-journeys/using-custom-actions.md)
      + [Aktionen in Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Aktionen in Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [Sprung](using/building-journeys/jump.md)
      + [Aktualisieren des Profils](using/building-journeys/update-profiles.md)
   + Erstellen von Ausdrücken {#building-advanced-conditions-journeys}
      + [Arbeiten mit dem erweiterten Ausdruckseditor](using/building-journeys/expression/expressionadvanced.md)
      + Syntax {#syntax}
         + [Syntax des erweiterten Ausdruckseditors](using/building-journeys/expression/generalities.md)
         + [Bedingte Anweisung](using/building-journeys/expression/conditional-instruction.md)
         + [Datentypen](using/building-journeys/expression/data-types.md)
         + [Feldverweise](using/building-journeys/expression/field-references.md)
         + [Funktionen zur Verwaltung von Sammlungen](using/building-journeys/expression/collection-management-functions.md)
         + [Operatoren](using/building-journeys/expression/operators.md)
         + [Journey-Eigenschaften](using/building-journeys/expression/journey-properties.md)
         + [Beispiele](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Funktionen {#main-functions-journey}
         + [Hauptfunktionen](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inAudience](using/building-journeys/functions/functioninaudience.md)
         + Aggregation {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Konversion {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Datum {#date}
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Liste {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [Limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Math {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + Zeichenfolge {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Anwendungsfälle {#journey-use-cases}
      + Geschäftliche Anwendungsfälle {#business-use-cases}
         + [Senden von Multi-Channel-Nachrichten](using/building-journeys/journeys-uc.md)
         + [Senden einer Nachricht mit Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Senden einer Nachricht an Abonnenten](using/building-journeys/message-to-subscribers-uc.md)
      + Technische Anwendungsfälle {#technical-use-cases}
         + [Dynamisches Übergeben von Kollektionen mithilfe benutzerdefinierter Aktionen](using/building-journeys/collections.md)
         + [Steigern der Versandaktivität](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen](using/building-journeys/limit-throughput.md)
         + [Verwenden von benutzerdefinierten Aktionen zum Schreiben von Journey-Ereignissen in Experience Platform](using/building-journeys/custom-action-aep.md)
+ Kampagnen{#campaigns}
   + [Erste Schritte mit Kampagnen](using/campaigns/get-started-with-campaigns.md)
   + [Erstellen einer Kampagne](using/campaigns/create-campaign.md)
   + [Überprüfen und Aktivieren einer Kampagne](using/campaigns/review-activate-campaign.md)
   + [Verwalten von Kampagnen](using/campaigns/modify-stop-campaign.md)
   + [Auslösen von Kampagnen mit APIs](using/campaigns/api-triggered-campaigns.md)
+ Konflikt-Management und Priorisierung {#conflict-prioritization}
   + [Erste Schritte mit Konflikt-Management und Priorisierung](using/conflict-prioritization/gs-conflict-prioritization.md)
   + [Identifizieren potenzieller Konflikte](using/conflict-prioritization/conflicts.md)
   + [Zuweisen von Prioritätswerten](using/conflict-prioritization/priority-scores.md)
   + [Journey-Begrenzung und Arbitration](using/conflict-prioritization/journey-capping.md)
+ Testen und Genehmigen {#test}
   + Vorschau und Testen der Inhalte {#preview-test}
      + [Erste Schritte mit Vorschau und Test](using/content-management/preview-test.md)
      + [Auswählen der Testprofile](using/content-management/test-profiles.md)
      + [Anzeigen Ihres Inhalts in der Vorschau](using/content-management/preview.md)
      + [Senden von E-Mail-Testsendungen](using/content-management/proofs.md)
      + [Testen des E-Mail-Rendering](using/content-management/rendering.md)
      + [Testen von Inhalten mit Beispieleingabedaten (Beta)](using/test-approve/simulate-sample-input.md)
      + [E-Mail-Spam-Bericht](using/content-management/spam-report.md)
   + Genehmigen von Journeys und Kampagnen {#approve}
      + [Erste Schritte mit Genehmigungen](using/test-approve/gs-approval.md)
      + [Erstellen und Verwalten von Genehmigungsrichtlinien](using/test-approve/approval-policies.md)
      + [Anfragen einer Genehmigung](using/test-approve/request-approval.md)
      + [Genehmigen einer Anfrage](using/test-approve/review-approve-request.md)
+ Kommunikationskanäle{#channels}
   + [Erste Schritte mit Kommunikationskanälen](using/channels/gs-channels.md)
   + E-Mail-Kanal {#email}
      + [Erste Schritte mit E-Mails](using/email/get-started-email.md)
      + [Erstellen einer E-Mail](using/email/create-email.md)
      + Gestalten von E-Mail-Inhalten {#design-email}
         + [Erste Schritte beim Gestalten von E-Mails](using/email/get-started-email-design.md)
         + Erstellen von Inhalten {#start-creating-content}
            + [Inhalte von Grund auf gestalten](using/email/content-from-scratch.md)
            + [Importieren von Content](using/email/existing-content.md)
            + [Programmieren von eigenem Inhalt](using/email/code-content.md)
            + [Verwenden von E-Mail-Vorlagen](using/email/use-email-templates.md)
         + Gestalten von Inhalten {#add-content}
            + [Verwenden von Inhaltskomponenten](using/email/content-components.md)
            + [Nutzen von visuellen Fragmenten](using/email/use-visual-fragments.md)
            + [Hinzufügen von Links und Verfolgen von Nachrichten](using/email/message-tracking.md)
            + [Einfügen von personalisierten Angeboten](using/email/add-offers-email.md)
            + [Generieren der Textversion](using/email/text-version-email.md)
            + [Hinzufügen eines Preheaders](using/email/preheader.md)
         + Bearbeiten des Stils {#edit-style}
            + [Erste Schritte mit E-Mail-Stilen](using/email/get-started-email-style.md)
            + [Bearbeiten von Hintergrundeinstellungen](using/email/backgrounds.md)
            + [Anpassen der vertikalen Ausrichtung und des Abstands](using/email/alignment-and-padding.md)
            + [Hinzufügen von Inline-Stilattributen](using/email/inline-styling.md)
      + [Verwalten von E-Mail-Opt-outs](using/email/email-opt-out.md)
      + Konfigurieren eines E-Mail-Kanals {#configure-email}
         + [Erste Schritte bei der E-Mail-Konfiguration](using/email/get-started-email-config.md)
         + [E-Mail-Konfigurationseinstellungen definieren](using/email/email-settings.md)
         + [Abmelden von der Liste aktivieren](using/email/list-unsubscribe.md)
         + [Kopfzeilenparameter](using/email/header-parameters.md)
         + [URL-Tracking](using/email/url-tracking.md)
         + [Personalisieren der E-Mail-Konfiguration](using/email/surface-personalization.md)
   + In-App-Kanal{#in-app}
      + [Erste Schritte mit dem In-App-Kanal](using/in-app/get-started-in-app.md)
      + [Voraussetzungen für In-App-Kanäle](using/in-app/inapp-configuration.md)
      + [Erstellen einer Mobile-In-App-Nachricht](using/in-app/create-in-app.md)
      + [Erstellen einer Web-In-App-Nachricht](using/in-app/create-in-app-web.md)
      + [Gestalten der App-Inhalte](using/in-app/design-in-app.md)
      + [Überprüfen und Senden von In-App-Benachrichtigungen](using/in-app/send-in-app.md)
   + Push-Benachrichtigungs-Kanal{#push}
      + [Erste Schritte mit Push-Benachrichtigungen](using/push/get-started-push.md)
      + [Erstellen einer Push-Benachrichtigung](using/push/create-push.md)
      + [Gestalten der Push-Benachrichtigung](using/push/design-push.md)
      + [Überprüfen und Senden Ihrer Push-Benachrichtigung](using/push/send-push.md)
      + Konfigurieren von Push-Benachrichtigungen{#push-config}
         + [Fluss der Push-Benachrichtigung](using/push/push-gs.md)
         + [Konfigurieren des Kanals für Push-Benachrichtigungen](using/push/push-configuration.md)
         + [Schnellstart-Workflow für Mobile-Onboarding](using/push/mobile-onboarding-wf.md)
   + SMS/MMS-Kanal{#sms}
      + [Erste Schritte mit Textnachrichten](using/sms/get-started-sms.md)
      + [Erstellen einer Textnachricht (SMS/MMS)](using/sms/create-sms.md)
      + [Überprüfen und Senden Ihrer Textnachrichten](using/sms/send-sms.md)
      + [Verwalten der Abmeldung von Textnachrichten](using/sms/sms-opt-out.md)
      + [Einrichten von SMS-Subdomains](using/sms/sms-subdomains.md)
      + Konfigurieren des SMS-/MMS-Kanals{#configure-sms}
         + [Erste Schritte bei der SMS-Konfiguration](using/sms/sms-configuration.md)
         + [Konfigurieren eines Sinch-Anbieters](using/sms/sms-configuration-sinch.md)
         + [Konfigurieren eines Infobip-Anbieters](using/sms/sms-configuration-infobip.md)
         + [Konfigurieren eines Twilio-Anbieters](using/sms/sms-configuration-twilio.md)
         + [Konfigurieren eines benutzerdefinierten Anbieters (Beta)](using/sms/sms-configuration-custom.md)
         + [Erstellen einer SMS-Konfiguration](using/sms/sms-configuration-surface.md)
   + Briefpost {#direct-mail}
      + [Erste Schritte mit Briefpost](using/direct-mail/get-started-direct-mail.md)
      + [Erstellen einer Briefpost](using/direct-mail/create-direct-mail.md)
      + [Überprüfen und Senden einer Briefpost-Nachricht](using/direct-mail/test-send-direct-mail.md)
      + [Konfigurieren von Briefpost](using/direct-mail/direct-mail-configuration.md)
   + Web-Kanal {#web}
      + [Erste Schritte mit dem Web-Kanal](using/web/get-started-web.md)
      + Konfigurieren des Webkanals {#configure-web-channel}
         + [Voraussetzungen für Web-Kanäle](using/web/web-prerequisites.md)
         + [Konfigurieren von Web-Subdomains](using/web/web-delegated-subdomains.md)
         + [Erstellen einer Web-Kanalkonfiguration](using/web/web-configuration.md)
      + [Erstellen von Web-Erlebnissen](using/web/create-web.md)
      + Verfassen von Web-Seiten{#author-web-pages}
         + [Arbeiten mit dem Web-Designer](using/web/web-visual-editor.md)
         + [Verwenden des nicht visuellen Editors](using/web/web-non-visual-editor.md)
         + [Verwalten von Änderungen](using/web/manage-web-modifications.md)
         + [Überwachen Ihrer Web-Erlebnisse](using/web/monitor-web-experiences.md)
         + [Erstellen von Einzelseitenanwendungen](using/web/web-spa.md)
   + Code-basiertes Erlebnis {#code-based-experience}
      + [Erste Schritte mit dem Code-basierten Kanal](using/code-based/get-started-code-based.md)
      + Konfigurieren des Code-basierten Kanals {#configure-code-based-channel}
         + [Schutzmechanismen und Voraussetzungen](using/code-based/code-based-prerequisites.md)
         + [Code-basierte Erlebnisoberflächen](using/code-based/code-based-surface.md)
         + [Beispiele für Implementierungsmethoden](using/code-based/code-based-implementation-samples.md)
         + [Erstellen einer Konfiguration von Code-basierten Erlebnissen](using/code-based/code-based-configuration.md)
      + Erstellen von Code-basierten Erlebnissen {#create-code-based-experiences}
         + [Aufbauen und Entwerfen von Code-basierten Erlebnissen](using/code-based/create-code-based.md)
         + [Testen von Code-basierten Erlebnissen](using/code-based/test-code-based.md)
         + [Verwalten von Code-basierten Erlebnissen](using/code-based/publish-code-based.md)
   + Inhaltskarten{#content-card}
      + [Erste Schritte mit Inhaltskarten](using/content-card/get-started-content-card.md)
      + Konfigurieren des Inhaltskartenkanals {#configure}
         + [Voraussetzungen für Inhaltskarten](using/content-card/content-card-configuration-prereq.md)
         + [Konfigurieren eines Inhaltskartenkanals in Journey Optimizer](using/content-card/content-card-configuration.md)
         + [Konfigurieren der Unterstützung für Inhaltskarten in Web-SDK](using/content-card/content-card-configuration-sdk.md)
      + [Erstellen von Inhaltskarten](using/content-card/create-content-card.md)
      + [Entwerfen von Inhaltskarten](using/content-card/design-content-card.md)
+ Landingpages {#landing-pages}
   + [Erste Schritte mit Landingpages](using/landing-pages/get-started-lp.md)
   + [Erstellen einer Landingpage](using/landing-pages/create-lp.md)
   + Inhaltserstellung {#landing-pages-design}
      + [Über das Design von Landingpages](using/landing-pages/design-lp.md)
      + [Erstellen der Landingpage-Inhalte](using/landing-pages/lp-content.md)
      + [Erstellen von Vorlagen](using/landing-pages/lp-templates.md)
      + [Hinzufügen von benutzerdefiniertem JavaScript](using/landing-pages/lp-custom-js.md)
   + [Erstellen einer Abonnement-Liste](using/landing-pages/subscription-list.md)
   + [Lernen durch Anwendungsfälle](using/landing-pages/lp-use-cases.md)
   + Konfigurieren von Landingpages {#lp-configuration}
      + [Konfigurieren von Landingpage-Subdomains](using/landing-pages/lp-subdomains.md)
      + [Definieren der Landingpage-Voreinstellungen](using/landing-pages/lp-presets.md)
+ Content Management {#content-management}
   + Arbeiten mit dem KI-Assistenten{#ai-assistant}
      + [Erste Schritte mit dem KI-Assistenten](using/content-management/gs-generative.md)
      + [Generierung von E-Mails mit KI](using/content-management/generative-email.md)
      + [Generierung von Push-Benachrichtungen mit KI](using/content-management/generative-push.md)
      + [Generierung von SMS mit KI](using/content-management/generative-sms.md)
      + [Generierung von Web-Seiten mit KI](using/content-management/generative-web.md)
      + [Inhaltsexperiment mit KI](using/content-management/generative-experimentation.md)
      + [Landingpage mit KI](using/content-management/generative-lp.md)
      + [Anwendungsfälle für den KI-Assistenten](using/content-management/generative-uc.md)
      + [Erstellen und Verwalten von Marken (Beta)](using/content-management/brands.md)
   + Arbeiten mit mehrsprachigen Inhalten{#content-multilingual}
      + [Erste Schritte mit mehrsprachigen Inhalten](using/content-management/multilingual-gs.md)
      + [Erstellen eines Gebietsschemas](using/content-management/multilingual-locale.md)
      + [Erstellen eines Sprachdienstleisters](using/content-management/multilingual-provider.md)
      + [Erstellen von mehrsprachigen Inhalten mit manueller Übersetzung](using/content-management/multilingual-manual.md)
      + [Erstellen von mehrsprachigen Inhalten mit automatisierter Übersetzung](using/content-management/multilingual-automated.md)
   + Arbeiten mit dem Inhaltsexperiment {#content-experiment}
      + [Erste Schritte mit dem Inhaltsexperiment](using/content-management/get-started-experiment.md)
      + [Erstellen eines Inhaltsexperiments](using/content-management/content-experiment.md)
      + Technotes {#technotes}
         + [Verstehen von statistischen Berechnungen](using/content-management/experiment-calculations.md)
         + [Verstehen der statistischen Berechnungen im Versuchsbericht](using/content-management/experiment-report-calculations.md)
   + Personalisierung {#personalization}
      + [Erste Schritte bei der Personalisierung](using/personalization/personalize.md)
      + [Personalisierungskontexte](using/personalization/personalization-contexts.md)
      + [Personalisierungssyntax](using/personalization/personalization-syntax.md)
      + [Verwenden von Adobe Experience Platform-Daten für die Personalisierung (Beta)](using/personalization/lookup-aep-data.md)
      + Arbeiten mit dem Personalisierungseditor {#expression-editor}
         + [Über den Personalisierungseditor](using/personalization/personalization-build-expressions.md)
         + [Hinzufügen von Attributen zu Favoriten](using/personalization/personalization-favorites.md)
         + [Verwenden von Ausdrucksfragmenten](using/personalization/use-expression-fragments.md)
         + [Validierung der Personalisierung](using/personalization/personalization-validation.md)
      + Helper-Funktionen {#functions}
         + [Erste Schritte mit Helper-Funktionen](using/personalization/functions/functions.md)
         + [Aggregationsfunktionen](using/personalization/functions/aggregation.md)
         + [Arithmetische Funktionen](using/personalization/functions/arithmetic-functions.md)
         + [Arrays und Listenfunktionen](using/personalization/functions/arrays-list.md)
         + [Datumsfunktionen](using/personalization/functions/dates.md)
         + [Boolesche Funktionen und Vergleichsfunktionen](using/personalization/functions/operators.md)
         + [Helper](using/personalization/functions/helpers.md)
         + [Zuordnungsfunktionen](using/personalization/functions/maps.md)
         + [Mathematische Funktionen](using/personalization/functions/math.md)
         + [Objektfunktionen](using/personalization/functions/objects.md)
         + [Zeichenfolgen-Funktionen](using/personalization/functions/string.md)
      + Anwendungsfälle für die Personalisierung{#personalization-use-cases}
         + [Benachrichtigung zum Bestellstatus](using/personalization/personalization-use-case.md)
         + [E-Mail zum Warenkorbabbruch](using/personalization/personalization-use-case-helper-functions.md)
         + [E-Mail mit den Rezepten eines Gesundheitsplans](using/personalization/perso-uc-plan-prescriptions.md)
   + Inhaltsvorlagen {#content-templates}
      + [Erste Schritte mit Inhaltsvorlagen](using/content-management/content-templates.md)
      + [Zugreifen auf und Verwalten von Vorlagen](using/content-management/access-content-templates.md)
      + [Erstellen von Inhaltsvorlagen](using/content-management/create-content-templates.md)
      + [Sperren von Inhalten in E-Mail-Vorlagen](using/content-management/content-locking.md)
      + [Testen von Inhaltsvorlagen](using/content-management/test-content-templates.md)
      + [Verwenden von Inhaltsvorlagen](using/content-management/use-content-templates.md)
   + Wiederverwendbare Inhaltsfragmente {#fragments}
      + [Erste Schritte mit Fragmenten](using/content-management/fragments.md)
      + [Erstellen eines Fragments](using/content-management/create-fragments.md)
      + [Speichern des vorhandenen Inhalts als Fragment](using/content-management/save-fragments.md)
      + [Anpassbare Fragmente](using/content-management/customizable-fragments.md)
      + [Verwalten von Fragmenten](using/content-management/manage-fragments.md)
   + Dynamische Inhalte {#dynamic}
      + [Erste Schritte mit dynamischen Inhalten](using/personalization/get-started-dynamic-content.md)
      + [Erstellen bedingter Regeln](using/personalization/create-conditions.md)
      + [Erstellen von dynamischen Inhalten](using/personalization/dynamic-content.md)
+ Zielgruppen, Profile und Identität{#audiences-profiles-identities}
   + Zielgruppen {#audiences}
      + [Erste Schritte mit Zielgruppen](using/audience/about-audiences.md)
      + Erstellen von Zielgruppen {#create}
         + [Segmentdefinitionen](using/audience/creating-a-segment-definition.md)
         + [Zielgruppenkomposition](using/audience/get-started-audience-orchestration.md)
         + [Benutzerdefinierter Upload](using/audience/custom-upload.md)
         + [Komposition föderierter Zielgruppen](using/audience/federated-audience-composition.md)
      + [Zielgruppenaktivierung in Kampagnen und Journey](using/audience/target-audiences.md)
      + [Anreicherungsattribute nutzen](using/audience/enrichment-attributes.md)
   + Profile{#profiles}
      + [Erste Schritte mit Profilen](using/audience/get-started-profiles.md)
      + [Erstellen von Testprofilen](using/audience/creating-test-profiles.md)
      + [Arbeiten mit berechneten Attributen](using/audience/computed-attributes.md)
   + [Identitäten](using/audience/get-started-identity.md)
   + [Lizenznutzung](using/audience/license-usage.md)
+ Integrationen{#assets-images}
   + [Integrationen mit anderen Lösungen](using/integrations/ajo-integrations.md)
   + [Arbeiten mit Experience Manager Assets](using/integrations/assets.md)
   + [Arbeiten mit Adobe Stock](using/integrations/stock.md)
   + [Arbeiten mit Experience Manager-Vorlagen](using/integrations/aem-templates.md)
   + [Arbeiten mit Experience Manager-Inhaltsfragmenten](using/integrations/aem-fragments.md)
   + [Arbeiten mit Dynamic Media](using/integrations/aem-dynamic.md)
+ Nachverfolgen und Überwachen {#reporting}
   + Live-Bericht {#live-report}
      + [Erste Schritte mit dem Live-Bericht](using/reports/live-report.md)
      + [Liste von Komponenten](using/reports/live-report-components.md)
      + [Live-Bericht zur Journey](using/reports/journey-live-report.md)
      + [Kampagnen-Live-Bericht](using/reports/campaign-live-report.md)
      + [Live-Bericht zu Landingpages](using/reports/lp-report-live.md)
      + [Live-Bericht zur Abonnement-Liste](using/reports/subscription-report-live.md)
   + Bericht für gesamte Zeit{#channel-report}
      + [Erste Schritte mit dem Bericht für die gesamte Zeit](using/reports/report-gs-cja.md)
      + [Manuelles Konfigurieren von Customer Journey Analytics](using/reports/cja-ajo.md)
      + [Verwalten Ihrer Berichte](using/reports/report-cja-manage.md)
      + [Voraussetzungen für Reporting und Experimente](using/reports/reporting-configuration.md)
      + Kampagnenberichte{#reporting}
         + [Kampagnenbericht](using/reports/campaign-global-report-cja.md)
         + [Code-basierter Kampagnenbericht](using/reports/campaign-global-report-cja-code.md)
         + [Inhaltskarten-Kampagnenbericht](using/reports/campaign-global-report-cja-content.md)
         + [Direkt-Mail-Kampagnenbericht](using/reports/campaign-global-report-cja-direct.md)
         + [E-Mail-Kampagnenbericht](using/reports/campaign-global-report-cja-email.md)
         + [Experimente – Kampagnenbericht](using/reports/campaign-global-report-cja-experimentation.md)
         + [In-App-Kampagnenbericht](using/reports/campaign-global-report-cja-inapp.md)
         + [Push-Benachrichtungs-Kampagnenbericht](using/reports/campaign-global-report-cja-push.md)
         + [SMS-Kampagnenbericht](using/reports/campaign-global-report-cja-sms.md)
         + [Web-Kampagnenbericht](using/reports/campaign-global-report-cja-web.md)
      + Journey-Berichte{#reporting}
         + [Journey-Bericht](using/reports/journey-global-report-cja.md)
         + [Code-basierter Journey-Bericht](using/reports/journey-global-report-cja-code.md)
         + [Inhaltskarten-Journey-Bericht](using/reports/journey-global-report-cja-content.md)
         + [Direkt-Mail-Journey-Bericht](using/reports/journey-global-report-cja-direct.md)
         + [E-Mail-Journey-Bericht](using/reports/journey-global-report-cja-email.md)
         + [In-App-Journey-Bericht](using/reports/journey-global-report-cja-inapp.md)
         + [Push-Journey-Bericht](using/reports/journey-global-report-cja-push.md)
         + [SMS-Journey-Bericht](using/reports/journey-global-report-cja-sms.md)
         + [Web-Journey-Bericht](using/reports/journey-global-report-cja-web.md)
      + [Übersichtsbericht](using/reports/channel-report-cja.md)
      + [Landingpage-Bericht](using/reports/lp-report-global-cja.md)
      + [Abonnement-Listen-Bericht](using/reports/subscription-report-global-cja.md)
   + Journey-Berichte {#reports}
      + [Erstellen von Journey-Berichten](using/reports/sharing-overview.md)
      + [Liste für Schrittereignisfelder](using/reports/sharing-field-list.md)
      + Veraltete Schrittereignisfelder {#legacy-step-event-fields}
         + [Über veraltete Felder](using/reports/sharing-legacy-fields.md)
         + [Journey-Felder](using/reports/sharing-journey-fields.md)
         + [Allgemeine Felder](using/reports/sharing-common-fields.md)
         + [Aktionsausführungsfelder](using/reports/sharing-execution-fields.md)
         + [Datenabruffelder](using/reports/sharing-fetch-fields.md)
         + [Identitätsfelder](using/reports/sharing-identity-fields.md)
      + [Beispiele für Abfragen](using/reports/query-examples.md)
   + Zustellbarkeit {#deliverability}
      + [Erste Schritte mit der Zustellbarkeit](using/reports/deliverability.md)
      + [Verständnis der Unterdrückungsliste](using/reports/suppression-list.md)
      + [Neue DMARC-Anforderung](using/configuration/dmarc-record-update.md)
   + [Warnhinweise](using/reports/alerts.md)
   + [Ausschlussgründe](using/reports/exclusion-list.md)
+ Entscheidungsfunktionen {#decisioning}
   + [Erste Schritte mit Entscheidungsfunktionen](using/experience-decisioning/gs-decision.md)
   + Entscheidungsfindung {#experience-decisioning}
      + [Erste Schritte mit der Entscheidungsfindung](using/experience-decisioning/gs-experience-decisioning.md)
      + [Leitplanken und Einschränkungen bei Entscheidungen](using/experience-decisioning/decisioning-guardrails.md)
      + API-Verweis{#api-reference}
         + Entscheidungselemente{#decision-items}
            + [Erstellen von Entscheidungselementen](using/experience-decisioning/api-reference/decisions-items/create.md)
            + [Liste der Entscheidungselemente](using/experience-decisioning/api-reference/decisions-items/decision-items-list.md)
            + [Löschen von Entscheidungselementen](using/experience-decisioning/api-reference/decisions-items/delete.md)
            + [Nachschlagen von Entscheidungselementen](using/experience-decisioning/api-reference/decisions-items/lookup.md)
            + [Aktualisieren von Entscheidungselementen](using/experience-decisioning/api-reference/decisions-items/update.md)
         + Elementsammlungen{#items-collections}
            + [Erstellen von Elementsammlungen](using/experience-decisioning/api-reference/items-collections/create.md)
            + [Löschen von Elementsammlungen](using/experience-decisioning/api-reference/items-collections/delete.md)
            + [Liste der Elementsammlungen](using/experience-decisioning/api-reference/items-collections/items-collections-list.md)
            + [Nachschlagen von Elementsammlungen](using/experience-decisioning/api-reference/items-collections/lookup.md)
            + [Aktualisieren von Elementsammlungen](using/experience-decisioning/api-reference/items-collections/update.md)
         + Auswahlstrategien{#selection-strategies}
            + [Erstellen von Auswahlstrategien](using/experience-decisioning/api-reference/selection-strategies/create.md)
            + [Löschen von Auswahlstrategien](using/experience-decisioning/api-reference/selection-strategies/delete.md)
            + [Nachschlagen von Auswahlstrategien](using/experience-decisioning/api-reference/selection-strategies/lookup.md)
            + [Liste der Auswahlstrategien](using/experience-decisioning/api-reference/selection-strategies/selection-strategies-list.md)
            + [Aktualisieren von Auswahlstrategien](using/experience-decisioning/api-reference/selection-strategies/update.md)
      + Verwalten von Entscheidungselementen {#decision-items}
         + [Konfigurieren des Elementkatalogs](using/experience-decisioning/catalogs.md)
         + [Erstellen von Entscheidungselementen](using/experience-decisioning/items.md)
         + [Verwalten von Elementsammlungen](using/experience-decisioning/collections.md)
      + Konfigurieren der Elementauswahl {#selection}
         + [Erstellen von Entscheidungsregeln](using/experience-decisioning/rules.md)
         + [Erstellen von Rangfolgenmethoden](using/experience-decisioning/ranking.md)
         + [Verwenden von Kontextdaten](using/experience-decisioning/context-data.md)
      + [Erstellen von Auswahlstrategien](using/experience-decisioning/selection-strategies.md)
      + [Erstellen von Entscheidungsrichtlinien](using/experience-decisioning/create-decision.md)
      + [Berichten über Entscheidungsfindung](using/experience-decisioning/cja-reporting.md)
      + [Anwendungsfall für die Entscheidungsfindung](using/experience-decisioning/experience-decisioning-uc.md)
   + Entscheidungs-Management {#offer-decisioning}
      + Erste Schritte mit Entscheidungs-Management {#get-started-decision}
         + [Über das Entscheidungs-Management](using/offers/get-started/starting-offer-decisioning.md)
         + [Leitplanken und Einschränkungen beim Entscheidungs-Management](using/offers/decision-management-guardrails.md)
         + [Benutzeroberfläche](using/offers/get-started/user-interface.md)
         + [Wichtigste Schritte bei der Angebotserstellung und -verwaltung](using/offers/offer-library/key-steps.md)
         + [Nutzen benutzerdefinierter Upload-Zielgruppen zur Entscheidungsfindung](using/offers/custom-upload-decisioning.md)
         + [Anwendungsfall: Einfügen von Angeboten in eine E-Mail](using/offers/offers-e2e.md)
      + Erstellen von Komponenten {#create-components}
         + [Erstellen von Platzierungen](using/offers/offer-library/creating-placements.md)
         + [Erstellen von Entscheidungsregeln](using/offers/offer-library/creating-decision-rules.md)
         + [Erstellen von Sammlungsqualifizierern](using/offers/offer-library/creating-tags.md)
      + Erstellen von Rankings {#rankings}
         + [Erste Schritte mit Rankings](using/offers/ranking/get-started-rankings.md)
         + [Rangfolgeformeln](using/offers/ranking/create-ranking-formulas.md)
         + KI-Modelle {#ai-models}
            + [Über KI-Modelle](using/offers/ranking/ai-models.md)
            + KI-Modelltypen {#ai-model-types}
            + [Modell für automatische Optimierung](using/offers/ranking/auto-optimization-model.md)
            + [Modell zur personalisierten Optimierung](using/offers/ranking/personalized-optimization-model.md)
            + [Erstellen von KI-Modellen](using/offers/ranking/create-ranking-strategies.md)
      + Erstellen und Verwalten von Angeboten {#managing-offers-in-the-offer-library}
         + Konfigurieren von Angeboten {#configure-offers}
            + [Erstellen von personalisierten Angeboten](using/offers/offer-library/creating-personalized-offers.md)
            + [Hinzufügen von Darstellungen](using/offers/offer-library/add-representations.md)
            + [Hinzufügen von Einschränkungen](using/offers/offer-library/add-constraints.md)
         + [Erstellen von Fallback-Angeboten](using/offers/offer-library/creating-fallback-offers.md)
         + [Erstellen von Sammlungen](using/offers/offer-library/creating-collections.md)
      + Erstellen und Verwalten von Entscheidungen {#create-manage-activities}
         + [Erstellen von Entscheidungen](using/offers/offer-activities/create-offer-activities.md)
         + [Konfigurieren der Auswahl von Angeboten in Entscheidungen](using/offers/offer-activities/configure-offer-selection.md)
         + [Erstellen von Simulationen](using/offers/offer-activities/simulation.md)
      + [Verwenden der Batch-Entscheidungsfindung](using/offers/batch-delivery.md)
      + Erfassen von Ereignisdaten {#collect-event-data}
         + [Erste Schritte mit der Datenerfassung](using/offers/data-collection/data-collection.md)
         + [Erstellen eines Datensatzes zum Erfassen von Ereignissen](using/offers/data-collection/create-dataset.md)
         + [Konfigurieren der Ereigniserfassung](using/offers/data-collection/schema-requirement.md)
      + Erstellen von Entscheidungs-Management-Berichten {#create-reports}
         + [Arbeiten mit Entscheidungs-Management-Ereignissen](using/offers/reports/get-started-events.md)
         + [Zugriff auf XDM-Felder von Ereignissen](using/offers/reports/xdm-fields.md)
      + Exportieren des Angebotskatalogs {#export-catalog}
         + [Erste Schritte mit dem Exportieren eines Angebotskatalogs](using/offers/export-catalog/get-started-export.md)
         + [Zugriff auf den exportierten Angebotskatalog](using/offers/export-catalog/access-dataset.md)
         + [Datensatz für personalisierte Angebote](using/offers/export-catalog/export-offers.md)
         + [Entscheidungsdatensatz](using/offers/export-catalog/export-decisions.md)
         + [Platzierungsdatensatz](using/offers/export-catalog/export-placements.md)
         + [Fallback-Datensatz](using/offers/export-catalog/export-fallback.md)
      + API-Referenz {#api-reference}
         + [Erste Schritte](using/offers/api-reference/getting-started.md)
         + Erstellen und Verwalten von Angeboten mit APIs {#offers-api}
            + Platzierungen {#placements}
               + [Auflisten von Platzierungen](using/offers/api-reference/offers-api/placements/placements-list.md)
               + [Nachschlagen von Platzierungen](using/offers/api-reference/offers-api/placements/lookup.md)
               + [Erstellen von Platzierungen](using/offers/api-reference/offers-api/placements/create.md)
               + [Aktualisieren von Platzierungen](using/offers/api-reference/offers-api/placements/update.md)
               + [Löschen von Platzierungen](using/offers/api-reference/offers-api/placements/delete.md)
            + Entscheidungsregeln {#decision-rules}
               + [Auflisten von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
               + [Nachschlagen von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/lookup.md)
               + [Erstellen einer Entscheidungsregel](using/offers/api-reference/offers-api/decision-rules/create.md)
               + [Aktualisieren von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/update.md)
               + [Entscheidungsregel löschen](using/offers/api-reference/offers-api/decision-rules/delete.md)
            + Sammlungsqualifizierer {#tags}
               + [Auflisten von Sammlungskennzeichnern](using/offers/api-reference/offers-api/tags/tags-list.md)
               + [Nachschlagen eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/tags/lookup.md)
               + [Erstellen eines Sammlungskennzeichners](using/offers/api-reference/offers-api/tags/create.md)
               + [Aktualisieren eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/tags/update.md)
               + [Löschen eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/tags/delete.md)
            + Personalisierte Angebote {#personalized-offers}
               + [Auflisten personalisierter Angebote](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
               + [Nachschlagen personalisierter Angebote](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
               + [Erstellen personalisierter Angebote](using/offers/api-reference/offers-api/personalized-offers/create.md)
               + [Aktualisieren personalisierter Angebote](using/offers/api-reference/offers-api/personalized-offers/update.md)
               + [Löschen personalisierter Angebote](using/offers/api-reference/offers-api/personalized-offers/delete.md)
            + Sammlungen {#collections}
               + [Auflisten von Sammlungen](using/offers/api-reference/offers-api/collections/collections-list.md)
               + [Nachschlagen von Sammlungen](using/offers/api-reference/offers-api/collections/lookup.md)
               + [Erstellen einer Sammlung](using/offers/api-reference/offers-api/collections/create.md)
               + [Aktualisieren von Sammlungen](using/offers/api-reference/offers-api/collections/update.md)
               + [Löschen von Sammlungen](using/offers/api-reference/offers-api/collections/delete.md)
            + Fallback-Angebote {#fallback-offers}
               + [Auflisten von Fallback-Angeboten](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
               + [Nachschlagen von Fallback-Angeboten](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
               + [Erstellen eines Fallback-Angebotes](using/offers/api-reference/offers-api/fallback-offers/create.md)
               + [Aktualisieren von Fallback-Angeboten](using/offers/api-reference/offers-api/fallback-offers/update.md)
               + [Löschen von Fallback-Angeboten](using/offers/api-reference/offers-api/fallback-offers/delete.md)
            + Entscheidungen {#decisions-api}
               + [Auflisten von Entscheidungen](using/offers/api-reference/activities-api/activities/activities-list.md)
               + [Nachschlagen von Entscheidungen](using/offers/api-reference/activities-api/activities/lookup.md)
               + [Erstellen einer Entscheidung](using/offers/api-reference/activities-api/activities/create.md)
               + [Aktualisieren von Entscheidungen](using/offers/api-reference/activities-api/activities/update.md)
               + [Löschen von Entscheidungen](using/offers/api-reference/activities-api/activities/delete.md)
            + Veraltete APIs {#legacy-api}
               + [Informationen zu veralteten APIs](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
               + Platzierungen {#placements}
                  + [Auflisten von Platzierungen](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
                  + [Nachschlagen von Platzierungen](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
                  + [Erstellen von Platzierungen](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
                  + [Aktualisieren von Platzierungen](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
                  + [Löschen von Platzierungen](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
               + Entscheidungsregeln {#decision-rules}
                  + [Auflisten von Entscheidungsregeln](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
                  + [Nachschlagen von Entscheidungsregeln](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
                  + [Erstellen einer Entscheidungsregel](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
                  + [Aktualisieren von Entscheidungsregeln](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
                  + [Entscheidungsregel löschen](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
               + Sammlungsqualifizierer {#tags}
                  + [Auflisten von Sammlungskennzeichnern](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
                  + [Nachschlagen eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
                  + [Erstellen eines Sammlungskennzeichners](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
                  + [Aktualisieren eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
                  + [Löschen eines Sammlungsqualifizierers](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
               + Personalisierte Angebote {#personalized-offers}
                  + [Auflisten personalisierter Angebote](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
                  + [Nachschlagen personalisierter Angebote](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
                  + [Erstellen personalisierter Angebote](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
                  + [Aktualisieren personalisierter Angebote](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
                  + [Löschen personalisierter Angebote](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
               + Fallback-Angebote {#fallback-offers}
                  + [Auflisten von Fallback-Angeboten](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
                  + [Nachschlagen von Fallback-Angeboten](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
                  + [Erstellen eines Fallback-Angebotes](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
                  + [Aktualisieren von Fallback-Angeboten](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
                  + [Löschen von Fallback-Angeboten](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
               + Sammlungen {#collections}
                  + [Auflisten von Sammlungen](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
                  + [Nachschlagen von Sammlungen](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
                  + [Erstellen einer Sammlung](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
                  + [Aktualisieren von Sammlungen](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
                  + [Löschen von Sammlungen](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
               + Entscheidungen {#decisions-api}
                  + [Auflisten von Entscheidungen](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
                  + [Nachschlagen von Entscheidungen](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
                  + [Erstellen einer Entscheidung](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
                  + [Aktualisieren von Entscheidungen](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
                  + [Löschen von Entscheidungen](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
         + Unterbreiten von Angeboten mithilfe von APIs {#offer-delivery-api}
            + [Erste Schritte mit APIs für den Angebotsversand](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
            + [Decisioning-API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
            + [Edge Decisioning-API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
            + [Batch Decisioning-API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Daten-Management {#data-management}
   + [Erste Schritte mit dem Daten-Management](using/data/gs-data.md)
   + [Arbeiten mit Schemata](using/data/get-started-schemas.md)
   + Journey Optimizer-Datensätze {#datasets}
      + [Erste Schritte mit Datensätzen](using/data/get-started-datasets.md)
      + [Schutzmaßnahmen bei der Time-to-Live (TTL) von Datensätzen](using/data/datasets-ttl.md)
      + [Exportieren von Journey Optimizer-Datensätzen](using/data/export-datasets.md)
      + [Beispiele für Abfragen](using/data/datasets-query-examples.md)
      + [Integrierte Schemata >](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de)
   + [Abfragen](using/data/get-started-queries.md)
+ Konfiguration {#configuration}
   + [Erste Schritte mit der Konfiguration von Journey Optimizer](using/configuration/get-started-configuration.md)
   + [Einrichten von Kanalkonfigurationen](using/configuration/channel-surfaces.md)
   + Anleitung zur Kanaleinrichtung{#guided-setup}
      + [Erste Schritte mit der Anleitung zur Kanaleinrichtung](using/configuration/set-mobile-config.md)
      + [Erstellen einer Kanaleinrichtung](using/configuration/create-channel-set-up.md)
   + Delegieren von E-Mail-Subdomains {#delegate-subdomains}
      + [Erste Schritte mit der Delegierung von Subdomains](using/configuration/about-subdomain-delegation.md)
      + [Delegieren einer Subdomain](using/configuration/delegate-subdomain.md)
      + [Festlegen des DMARC-Eintrags](using/configuration/dmarc-record.md)
      + [Hinzufügen eines Google TXT-Eintrags](using/configuration/google-txt.md)
      + [Zugreifen auf und Bearbeiten von PTR-Einträgen](using/configuration/ptr-records.md)
      + [Erstellen von IP-Pools](using/configuration/ip-pools.md)
   + Implementieren eines IP-Aufwärmplans {#implement-ip-warmup-plan}
      + [Erste Schritte mit IP-Aufwärmplänen](using/configuration/ip-warmup-gs.md)
      + [Erstellen von IP-Aufwärmkampagnen](using/configuration/ip-warmup-campaign.md)
      + [Erstellen eines IP-Aufwärmplans](using/configuration/ip-warmup-plan.md)
      + [Ausführen des IP-Aufwärmplans](using/configuration/ip-warmup-execution.md)
      + [Dateien für den IP-Aufwärmplan](using/configuration/ip-warmup-plan-files.md)
   + Überwachen von E-Mail-Adressen {#monitor-reputation}
      + [Unterdrückungsliste](using/configuration/manage-suppression-list.md)
      + [Weitere Zustellversuche](using/configuration/retries.md)
      + [Zulassungsliste](using/configuration/allow-list.md)
   + [Verwenden von Testadressenlisten](using/configuration/seed-lists.md)
   + [Unterstützung für Archivierung](using/configuration/archiving-support.md)
   + [Ändern von Ausführungsadressen](using/configuration/primary-email-addresses.md)
   + [Konfigurieren von Verfahrensregeln](using/configuration/frequency-rules.md)
   + [Arbeiten mit Regelsätzen](using/configuration/rule-sets.md)
   + Konfigurieren von Journeys {#configure-journeys}
      + [Über Datenquellen, Ereignisse und Aktionen](using/configuration/about-data-sources-events-actions.md)
      + Integrieren mit externen Systemen {#external-systems}
         + [Journey-Integration in externe Systeme](using/configuration/external-systems.md)
         + [Capping-API](using/configuration/capping.md)
         + [Einschränkungs-API](using/configuration/throttling.md)
      + Ereigniskonfiguration {#events-journeys}
         + [Arbeiten mit Journey-Ereignissen](using/event/about-events.md)
         + Konfigurieren eines unitären Ereignisses {#unitary-events}
            + [Erste Schritte mit unitären Ereignissen](using/event/about-creating.md)
            + [Informationen zu ExperienceEvent-Schemata](using/event/experience-event-schema.md)
            + [Arbeiten mit Adobe Analytics](using/event/about-analytics.md)
         + [Konfigurieren eines Geschäftsereignisses](using/event/about-creating-business.md)
         + [Zusätzliche Schritte zum Senden von Ereignissen](using/event/additional-steps-to-send-events-to-journey.md)
      + Konfiguration von Datenquellen{#data-source-journeys}
         + [Informationen zu Datenquellen](using/datasource/about-data-sources.md)
         + [Konfigurieren einer Datenquelle](using/datasource/configure-data-sources.md)
         + [Datenquelle von Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Externe Datenquellen](using/datasource/external-data-sources.md)
      + Aktionskonfiguration {#action-journeys}
         + [Informationen zu Aktionen](using/action/action.md)
         + [Konfigurieren einer Aktion](using/action/about-custom-action-configuration.md)
         + [Fehlerbehebung bei benutzerdefinierten Aktionen](using/action/troubleshoot-custom-action.md)
         + [Integration mit Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrieren mit Adobe Campaign v7/v8](using/action/acc-action.md)
         + [Verwenden von API-Aufrufantworten in benutzerdefinierten Aktionen](using/action/action-response.md)
         + [Integrieren mit Marketo Engage](using/action/marketo-engage.md)
   + [Quellen](using/start/get-started-sources.md)
   + [Exportieren von Objekten in eine andere Sandbox](using/configuration/copy-objects-to-sandbox.md)
+ Zugriffskontrolle {#access-control}
   + Zugriffskontrolle – Übersicht{#privacy}
      + [Erste Schritte in der Benutzerverwaltung](using/administration/permissions-overview.md)
      + [Integrierte Rollen](using/administration/ootb-product-profiles.md)
      + [Integrierte Berechtigungen](using/administration/ootb-permissions.md)
      + [Berechtigungsstufen](using/administration/high-low-permissions.md)
   + [Verwalten von Benutzenden und Produkten](using/administration/permissions.md)
   + [Attributbasierte Zugriffssteuerung](using/administration/attribute-based-access.md)
   + [Zugriffssteuerung auf Objektebene](using/administration/object-based-access.md)
   + [Sandbox-Verwaltung](using/administration/sandboxes.md)
+ Datenschutz {#privacy}
   + [Erste Schritte beim Datenschutz](using/privacy/get-started-privacy.md)
   + [Datenschutzanfragen](using/privacy/requests.md)
   + [Audit-Aktionen für Ressourcen](using/privacy/audit-logs.md)
   + [Durchführen von Datenhygienevorgängen](using/privacy/data-hygiene.md)
   + Einverständnisverwaltung {#consent}
      + [Verwalten von Opt-out](using/privacy/opt-out.md)
      + [Arbeiten mit Einverständnisrichtlinien](using/action/consent.md)
   + [Data Governance](using/action/action-privacy.md)
   + [Einrichten und Verwalten von Customer Managed Keys](using/privacy/cmk.md)
