---
product: Journey Optimizer
audience: end-user
user-guide-title: Handbuch für Journey Optimizer
user-guide-description: Mit Journey Optimizer können Sie miteinander verbundene, kontextuelle und personalisierte Erlebnisse für Kunden erstellen und bereitstellen.
type: Documentation
solution: Journey Optimizer
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 98%

---

# Hilfe zu Adobe Journey Optimizer {#using}

+ [Dokumentation zu Journey Optimizer](ajo-home.md)
+ Neue Funktionen {#whats-new}
   + [Neueste Versionshinweise](using/rn/release-notes.md)
   + Frühere Versionshinweise {#previous-rn-new}
      + [Versionshinweise für 2022](using/rn/release-notes-2022.md)
      + [Versionshinweise für 2021](using/rn/release-notes-2021.md)
   + [Dokumentation – Aktualisierungen](using/rn/documentation-updates.md)
+ Erste Schritte{#get-started}
   + [Was ist Journey Optimizer?](using/start/get-started.md)
   + Schnellstartanleitungen{#quick-start}
      + [Übersicht](using/start/quick-start.md)
      + [Erste Schritte als Marketer](using/start/path/marketer.md)
      + [Erste Schritte als Datentechniker](using/start/path/data-engineer.md)
      + [Erste Schritte als Administrator](using/start/path/administrator.md)
      + [Erste Schritte als Entwickler](using/start/path/developer.md)
   + [Benutzeroberfläche](using/start/user-interface.md)
   + [Barrierefreiheit](using/start/accessibility.md)
   + [Integrationen](using/start/ajo-integrations.md)
   + [Leitlinien](using/start/guardrails.md)
+ Journeys {#orchestrate-journeys}
   + [Erste Schritte mit Journeys](using/building-journeys/journey.md)
   + Erstellen einer Journey{#create-journey}
      + [Erstellen Ihrer ersten Journey](using/building-journeys/journey-gs.md)
      + [Gestalten einer Journey](using/building-journeys/using-the-journey-designer.md)
      + [Testen einer Journey](using/building-journeys/testing-the-journey.md)
      + [Veröffentlichen Ihrer Journey](using/building-journeys/publishing-the-journey.md)
   + Verwalten von Journeys{#mannage-journey}
      + [Beenden der Journey](using/building-journeys/end-journey.md)
      + [Zeitzonen-Management](using/building-journeys/timezone-management.md)
      + [Profil-Eintrittsverwaltung](using/building-journeys/entry-management.md)
      + [Kopieren einer Journey in eine andere Sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Fehlerbehebung in einer Journey](using/building-journeys/troubleshooting.md)
      + [Integrieren mit Intelligent Services](using/building-journeys/ai-services-overview.md)
   + Aktivitäten {#about-journey-building}
      + [Erste Schritte mit Journey-Aktivitäten](using/building-journeys/about-journey-activities.md)
      + [Allgemeine Ereignisse](using/building-journeys/general-events.md)
      + [Reaktion](using/building-journeys/reaction-events.md)
      + [Segmentqualifizierung](using/building-journeys/segment-qualification-events.md)
      + [Bedingung](using/building-journeys/condition-activity.md)
      + [Warten](using/building-journeys/wait-activity.md)
      + [Segment lesen](using/building-journeys/read-segment.md)
      + [E-Mail, SMS, Push-Benachrichtigung](using/building-journeys/journeys-message.md)
      + [Benutzerdefinierte Aktionen](using/building-journeys/using-custom-actions.md)
      + [Aktionen in Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Aktionen in Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Sprung](using/building-journeys/jump.md)
      + [Aktualisieren von Profilen](using/building-journeys/update-profiles.md)
   + Erstellen von Ausdrücken {#building-advanced-conditions-journeys}
      + [Übersicht](using/building-journeys/expression/expressionadvanced.md)
      + Syntax {#syntax}
         + [Allgemeines](using/building-journeys/expression/generalities.md)
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
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
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
         + [Dynamisches Übergeben von Sammlungen mithilfe benutzerdefinierter Aktionen](using/building-journeys/collections.md)
         + [Steigern der Versandaktivität](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen](using/building-journeys/limit-throughput.md)
+ Kampagnen{#campaigns}
   + [Erste Schritte mit Kampagnen](using/campaigns/get-started-with-campaigns.md)
   + [Erstellen einer Kampagne](using/campaigns/create-campaign.md)
   + [Überprüfen und Aktivieren einer Kampagne](using/campaigns/review-activate-campaign.md)
   + [Verwalten von Kampagnen](using/campaigns/modify-stop-campaign.md)
   + Inhaltsexperiment {#content-experiment}
      + [Erste Schritte mit dem Inhaltsexperiment](using/campaigns/get-started-experiment.md)
      + [Erstellen eines Inhaltsexperiments](using/campaigns/content-experiment.md)
      + [Verstehen von statistischen Berechnungen](using/campaigns/experiment-calculations.md)
      + [Konfigurieren von Experimentberichten](using/campaigns/reporting-configuration.md)
      + [Statistische Berechnungen im Experimentationsbericht](using/campaigns/experiment-report-calculations.md)
   + [Auslösen von Kampagnen mit APIs](using/campaigns/api-triggered-campaigns.md)
+ E-Mail-Kanal {#email}
   + [Erste Schritte mit E-Mails](using/email/get-started-email.md)
   + [Erstellen einer E-Mail](using/email/create-email.md)
   + Gestalten von E-Mail-Inhalten {#design-email}
      + [Erste Schritte beim Gestalten von E-Mails](using/email/get-started-email-design.md)
      + Erstellen von Inhalten {#start-creating-content}
         + [Von Grund auf neu beginnen](using/email/content-from-scratch.md)
         + [Importieren von E-Mail-Inhalten](using/email/existing-content.md)
         + [Programmieren von eigenem Inhalt](using/email/code-content.md)
         + [Arbeiten mit Vorlagen](using/email/email-templates.md)
      + Gestalten von Inhalten {#add-content}
         + [Verwenden von Inhaltskomponenten](using/email/content-components.md)
         + [Hinzufügen von Links und Verfolgen von Nachrichten](using/email/message-tracking.md)
         + Verwalten von Assets {#manage-asset}
            + [Verwenden von Assets Essentials](using/email/assets-essentials.md)
            + [Arbeiten mit Adobe Stock](using/email/stock.md)
         + [Einfügen von personalisierten Angeboten](using/email/add-offers-email.md)
         + [Generieren der Textversion](using/email/text-version-email.md)
         + [Hinzufügen eines Preheaders](using/email/preheader.md)
      + Bearbeiten des Stils {#edit-style}
         + [Erste Schritte mit E-Mail-Stilen](using/email/get-started-email-style.md)
         + [Bearbeiten von Hintergrundeinstellungen](using/email/backgrounds.md)
         + [Anpassen der vertikalen Ausrichtung und des Abstands](using/email/alignment-and-padding.md)
         + [Definieren eines Stils für Links](using/email/styling-links.md)
         + [Hinzufügen von Inline-Stilattributen](using/email/inline-styling.md)
   + [Vorschau und Testversand von E-Mails](using/email/preview.md)
   + [Erstellen von Inhaltsvorlagen](using/email/content-templates.md)
   + [Verwalten von E-Mail-Opt-outs](using/email/email-opt-out.md)
   + Konfigurieren eines E-Mail-Kanals {#configure-email}
      + [Erste Schritte bei der E-Mail-Konfiguration](using/email/get-started-email-config.md)
      + [Konfigurieren der Oberflächen-Einstellungen von E-Mails](using/email/email-settings.md)
+ In-App-Kanal{#in-app}
   + [Erste Schritte mit dem In-App-Kanal](using/in-app/get-started-in-app.md)
   + [Konfigurieren des In-App-Kanals](using/in-app/inapp-configuration.md)
   + [Erstellen einer In-App-Nachricht](using/in-app/create-in-app.md)
   + [Gestalten Ihrer In-App-Inhalte](using/in-app/design-in-app.md)
   + [In-App-Bericht](using/in-app/inapp-report.md)
+ Push-Benachrichtigungs-Kanal{#push}
   + [Erste Schritte mit Push-Benachrichtigungen](using/push/get-started-push.md)
   + [Erstellen einer Push-Benachrichtigung](using/push/create-push.md)
   + [Gestalten der Push-Benachrichtigung](using/push/design-push.md)
   + [Senden der Push-Benachrichtigung](using/push/send-push.md)
   + Konfigurieren von Push-Benachrichtigungen{#push-config}
      + [Push-Benachrichtigungen und Adobe Journey Optimizer](using/push/push-gs.md)
      + [Konfigurieren eines Kanal für Push-Benachrichtigungen](using/push/push-configuration.md)
+ SMS-Kanal{#sms}
   + [Erste Schritte mit SMS](using/sms/get-started-sms.md)
   + [Erstellen einer SMS-Nachricht](using/sms/create-sms.md)
   + [Senden einer SMS-Nachricht](using/sms/send-sms.md)
   + [Verwalten von SMS-Opt-outs](using/sms/sms-opt-out.md)
   + [Konfigurieren des SMS-Kanals](using/sms/sms-configuration.md)
+ Briefpost {#direct-mail}
   + [Erstellen eines Briefpostversands](using/direct-mail/create-direct-mail.md)
   + [Konfigurieren von Briefpost](using/direct-mail/direct-mail-configuration.md)
+ Web-Kanal{#web}
   + [Erste Schritte mit dem Web-Kanal](using/web/get-started-web.md)
   + [Erstellen von Web-Erlebnissen](using/web/create-web.md)
   + [Verfassen von Web-Seiten](using/web/author-web.md)
   + [Visual Editing Helper-Erweiterung](using/web/visual-editing-helper.md)
   + [Web-Berichte](using/web/web-report.md)
+ Landingpages {#landing-pages}
   + [Erste Schritte mit Landingpages](using/landing-pages/get-started-lp.md)
   + [Erstellen einer Landingpage](using/landing-pages/create-lp.md)
   + Inhaltserstellung {#landing-pages-design}
      + [Über das Design von Landingpages](using/landing-pages/design-lp.md)
      + [Erstellen der Landingpage-Inhalte](using/landing-pages/lp-content.md)
      + [Erstellen von Vorlagen](using/landing-pages/lp-templates.md)
      + [Hinzufügen von benutzerdefiniertem JavaScript](using/landing-pages/lp-custom-js.md)
   + [Erstellen einer Abonnementliste](using/landing-pages/subscription-list.md)
   + [Lernen durch Anwendungsfälle](using/landing-pages/lp-use-cases.md)
   + Konfigurieren von Landingpages {#lp-configuration}
      + [Konfigurieren von Landingpage-Subdomains](using/landing-pages/lp-subdomains.md)
      + [Definieren der Landingpage-Voreinstellungen](using/landing-pages/lp-presets.md)
+ Personalisierung und dynamische Inhalte {#personalized-dynamic-content}
   + Personalisierung {#personalization}
      + [Erste Schritte bei der Personalisierung](using/personalization/personalize.md)
      + [Personalisierungskontexte](using/personalization/personalization-contexts.md)
      + Erstellen von Ausdrücken {#build-expressions}
         + [Personalisierungssyntax](using/personalization/personalization-syntax.md)
         + Arbeiten mit dem Ausdruckseditor {#expression-editor}
            + [Über den Ausdruckseditor](using/personalization/personalization-build-expressions.md)
            + [Hinzufügen von Attributen zu Favoriten](using/personalization/personalization-favorites.md)
            + [Arbeiten mit gespeicherten Ausdrücken](using/personalization/personalization-library.md)
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
      + Anwendungsfälle {#personalization-use-cases}
         + [Benachrichtigung zum Bestellstatus](using/personalization/personalization-use-case.md)
         + [E-Mail zum Warenkorbabbruch](using/personalization/personalization-use-case-helper-functions.md)
   + Dynamische Inhalte {#dynamic}
      + [Erste Schritte mit dynamischen Inhalten](using/personalization/get-started-dynamic-content.md)
      + [Erstellen bedingter Regeln](using/personalization/create-conditions.md)
      + [Erstellen von dynamischen Inhalten](using/personalization/dynamic-content.md)
+ Segmente, Profile und Identität{#segment}
   + Segmente {#segments}
      + [Erste Schritte mit Segmenten](using/segment/about-segments.md)
      + [Erstellen von Segmenten](using/segment/creating-a-segment.md)
   + Profile{#profiles}
      + [Erste Schritte mit Profilen](using/segment/get-started-profiles.md)
      + [Erstellen von Testprofilen](using/segment/creating-test-profiles.md)
   + [Identitäten](using/segment/get-started-identity.md)
   + Erstellen von Audiences {#audience-orchestration}
      + [Erste Schritte mit der Audience-Komposition](using/segment/get-started-audience-orchestration.md)
      + [Erstellen von Kompositions-Workflows](using/segment/create-compositions.md)
      + [Arbeiten mit der Arbeitsfläche für Kompositionen](using/segment/composition-canvas.md)
      + [Zugreifen auf und Verwalten von Audiences](using/segment/access-audiences.md)
   + [Lizenznutzung](using/segment/license-usage.md)
+ Nachverfolgen und Überwachen {#reporting}
   + Live-Bericht {#live-report}
      + [Erste Schritte mit dem Live-Bericht](using/reports/live-report.md)
      + [Live-Bericht zur Journey](using/reports/journey-live-report.md)
      + [Campaign Live-Bericht](using/reports/campaign-live-report.md)
      + [Live-Bericht zu Landingpages](using/reports/lp-report-live.md)
      + [Live-Bericht zur Abonnement-Liste](using/reports/subscription-report-live.md)
   + Globaler Bericht {#global-report}
      + [Erste Schritte mit dem globalen Bericht](using/reports/global-report.md)
      + [Globaler Bericht zur Journey](using/reports/journey-global-report.md)
      + [Globaler Bericht in Campaign](using/reports/campaign-global-report.md)
      + [Globaler Bericht zur Landingpage](using/reports/lp-report-global.md)
      + [Globaler Bericht zur Abonnement-Liste](using/reports/subscription-report-global.md)
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
   + [Warnhinweise](using/reports/alerts.md)
   + [Arbeiten mit Customer Journey Analytics](using/reports/cja-ajo.md)
+ Entscheidungs-Management {#offer-decisioning}
   + Erste Schritte mit Entscheidungs-Management {#get-started-decision}
      + [Über das Entscheidungs-Management](using/offers/get-started/starting-offer-decisioning.md)
      + [Benutzeroberfläche](using/offers/get-started/user-interface.md)
      + [Wichtigste Schritte bei der Angebotserstellung und -verwaltung](using/offers/offer-library/key-steps.md)
      + [Anwendungsfall: Einfügen von Angeboten in eine E-Mail](using/offers/offers-e2e.md)
   + Erstellen von Komponenten {#create-components}
      + [Erstellen von Platzierungen](using/offers/offer-library/creating-placements.md)
      + [Erstellen von Entscheidungsregeln](using/offers/offer-library/creating-decision-rules.md)
      + [Erstellen von Tags](using/offers/offer-library/creating-tags.md)
   + Erstellen von Rankings {#rankings}
      + [Erste Schritte mit Rankings](using/offers/ranking/get-started-rankings.md)
      + [Ranking-Formeln](using/offers/ranking/create-ranking-formulas.md)
      + KI-Modelle {#ai-models}
         + [Über KI-Modelle](using/offers/ranking/ai-models.md)
         + KI-Modelltypen {#ai-model-types}
            + [Modell für automatische Optimierung](using/offers/ranking/auto-optimization-model.md)
            + [Modell zur personalisierten Optimierung](using/offers/ranking/personalized-optimization-model.md)
         + Erstellen von KI-Modellen {#configure-ai-model}
            + [Erstellen eines Datensatzes zum Erfassen von Ereignissen](using/offers/ranking/create-dataset.md)
            + [Erstellen eines KI-Modells](using/offers/ranking/create-ranking-strategies.md)
            + [Konfigurieren der Ereigniserfassung](using/offers/ranking/schema-requirement.md)
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
   + [Batch-Entscheidungsfindung](using/offers/batch-delivery.md)
   + Erstellen von Entscheidungs-Management-Berichten {#create-reports}
      + [Erste Schritte mit Entscheidungs-Management-Ereignissen](using/offers/reports/get-started-events.md)
      + [Wichtige Informationen zu Entscheidungs-Management-Ereignissen](using/offers/reports/key-information.md)
      + [Zugriff auf XDM-Felder von Ereignissen](using/offers/reports/xdm-fields.md)
   + Exportieren des Angebotskatalogs {#export-catalog}
      + [Erste Schritte mit dem Exportieren eines Angebotskatalogs ](using/offers/export-catalog/get-started-export.md)
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
            + [Erstellen von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Aktualisieren von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Löschen von Entscheidungsregeln](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Tags {#tags}
            + [Auflisten von Tags](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Nachschlagen von Tags](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Erstellen von Tags](using/offers/api-reference/offers-api/tags/create.md)
            + [Aktualisieren von Tags](using/offers/api-reference/offers-api/tags/update.md)
            + [Löschen von Tags](using/offers/api-reference/offers-api/tags/delete.md)
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
      + Erstellen und Verwalaten von Entscheidungen mit APIs {#activities-api}
         + [Auflisten von Entscheidungen](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Nachschlagen von Entscheidungen](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Erstellen einer Entscheidung](using/offers/api-reference/activities-api/activities/create.md)
         + [Aktualisieren von Entscheidungen](using/offers/api-reference/activities-api/activities/update.md)
         + [Löschen von Entscheidungen](using/offers/api-reference/activities-api/activities/delete.md)
      + Unterbreiten von Angeboten mithilfe von APIs {#offer-delivery-api}
         + [Erste Schritte mit APIs für die Angebotsbereitstellung](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [Decisioning-API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [Edge Decisioning-API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [Batch Decisioning-API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Daten-Management {#data-management}
   + [Erste Schritte mit dem Daten-Management](using/data/gs-data.md)
   + [Arbeiten mit Schemata](using/data/get-started-schemas.md)
   + Journey Optimizer-Datensätze {#datasets}
      + [Erste Schritte mit Datensätzen](using/data/get-started-datasets.md)
      + [Beispiele für Abfragen](using/data/datasets-query-examples.md)
   + [Abfragen](using/data/get-started-queries.md)
+ Konfiguration{#configuration}
   + [Erste Schritte mit der Konfiguration von Journey Optimizer](using/configuration/get-started-configuration.md)
   + Delegieren von E-Mail-Subdomains {#delegate-subdomains}
      + [Erste Schritte mit der Zuweisung von Subdomains](using/configuration/about-subdomain-delegation.md)
      + [Delegieren einer Subdomain](using/configuration/delegate-subdomain.md)
      + [Hinzufügen eines Google TXT-Eintrags](using/configuration/google-txt.md)
      + [Zugreifen auf und Bearbeiten von PTR-Einträgen](using/configuration/ptr-records.md)
      + [Erstellen von IP-Pools](using/configuration/ip-pools.md)
   + [Einrichten von Kanaloberflächen](using/configuration/channel-surfaces.md)
   + Überwachen von E-Mail-Adressen {#monitor-reputation}
      + [Unterdrückungsliste](using/configuration/manage-suppression-list.md)
      + [Weitere Zustellversuche](using/configuration/retries.md)
      + [Zulassungsliste](using/configuration/allow-list.md)
   + [Unterstützung für Archivierung](using/configuration/archiving-support.md)
   + [Konfigurieren von Häufigkeitsregeln](using/configuration/frequency-rules.md)
   + [Verwalten von Ausführungsadressen](using/configuration/primary-email-addresses.md)
   + Konfigurieren von Journeys {#configure-journeys}
      + [Über Datenquellen, Ereignisse und Aktionen](using/configuration/about-data-sources-events-actions.md)
      + [Integrieren mit externen Systemen](using/configuration/external-systems.md)
      + Ereigniskonfiguration {#events-journeys}
         + [Allgemeine Funktionsweise](using/event/about-events.md)
         + Konfigurieren eines unitären Ereignisses {#unitary-events}
            + [Erste Schritte mit unitären Ereignissen](using/event/about-creating.md)
            + [Informationen zu ExperienceEvent-Schemata](using/event/experience-event-schema.md)
            + [Nutzen von Adobe Analytics](using/event/about-analytics.md)
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
         + [Integration mit Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrieren mit Adobe Campaign v7/v8](using/action/acc-action.md)
   + [Quellen](using/start/get-started-sources.md)
+ Zugriffskontrolle {#access-control}
   + [Zugriffskontrolle – Übersicht](using/administration/permissions-overview.md)
   + [Integrierte Produktprofile](using/administration/ootb-product-profiles.md)
   + [Verwalten von Benutzern und Produktprofilen](using/administration/permissions.md)
   + [Berechtigungsebenen](using/administration/high-low-permissions.md)
   + [Sandbox-Management](using/administration/sandboxes.md)
   + [Attributbasierte Zugriffssteuerung](using/administration/attribute-based-access.md)
   + [Zugriffssteuerung auf Objektebene](using/administration/object-based-access.md)
+ Datenschutz {#privacy}
   + [Erste Schritte beim Datenschutz](using/privacy/get-started-privacy.md)
   + [Datenschutzanfragen](using/privacy/requests.md)
   + [Audit-Aktionen für Ressourcen](using/privacy/audit-logs.md)
   + [Datenhygiene](using/privacy/data-hygiene.md)
   + Einverständnisverwaltung {#consent}
      + [Verwalten von Opt-out](using/privacy/opt-out.md)
      + [Arbeiten mit Einverständnisrichtlinien](using/action/consent.md)
   + [Data Governance](using/action/action-privacy.md)
