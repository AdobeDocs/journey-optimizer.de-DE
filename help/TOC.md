---
product: Journey Optimizer
audience: end-user
user-guide-title: Handbuch für Journey Optimizer
user-guide-description: Verwenden Sie Journey Optimizer, um Ihren Kunden vernetzte, kontextbezogene und personalisierte Erlebnisse bereitzustellen.
type: Documentation
solution: Journey Optimizer
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 0%

---

# Hilfe zu Adobe Journey Optimizer {#using}

+ [Dokumentation zu Journey Optimizer](ajo-home.md)
+ Neue Funktionen {#whats-new}
   + [Neueste Versionshinweise](using/rn/release-notes.md)
   + Frühere Versionshinweise {#previous-rn-new}
      + [Versionshinweise für 2022](using/rn/release-notes-2022.md)
      + [Versionshinweise für 2021](using/rn/release-notes-2021.md)
   + [Dokumentationsaktualisierungen](using/rn/documentation-updates.md)
+ Erste Schritte{#get-started}
   + [Was ist Journey Optimizer](using/start/get-started.md)
   + Schnellstartanleitungen{#quick-start}
      + [Übersicht](using/start/quick-start.md)
      + [Erste Schritte als Marketer](using/start/path/marketer.md)
      + [Erste Schritte als Data Engineer](using/start/path/data-engineer.md)
      + [Erste Schritte als Administrator](using/start/path/administrator.md)
      + [Erste Schritte als Entwickler](using/start/path/developer.md)
   + [Benutzeroberfläche](using/start/user-interface.md)
   + [Integrationen](using/start/ajo-integrations.md)
   + [Schutzschilde](using/start/guardrails.md)
+ Journeys {#orchestrate-journeys}
   + [Erste Schritte mit Journeys](using/building-journeys/journey.md)
   + Eine Journey erstellen{#create-journey}
      + [Erste Journey erstellen](using/building-journeys/journey-gs.md)
      + [Gestalten Ihrer Journey](using/building-journeys/using-the-journey-designer.md)
      + [Testen der Journey](using/building-journeys/testing-the-journey.md)
      + [Journey veröffentlichen](using/building-journeys/publishing-the-journey.md)
   + Journeys verwalten{#mannage-journey}
      + [Journey beenden](using/building-journeys/end-journey.md)
      + [Zeitzonen-Management](using/building-journeys/timezone-management.md)
      + [Profil-Eingangsverwaltung](using/building-journeys/entry-management.md)
      + [Eine Journey in eine andere Sandbox kopieren](using/building-journeys/copy-to-sandbox.md)
      + [Fehlerbehebung für Ihre Journey](using/building-journeys/troubleshooting.md)
      + [Integration mit Intelligent Services](using/building-journeys/ai-services-overview.md)
   + Tätigkeiten {#about-journey-building}
      + [Erste Schritte mit Journey-Aktivitäten](using/building-journeys/about-journey-activities.md)
      + [Allgemeine Ereignisse](using/building-journeys/general-events.md)
      + [Reaktion](using/building-journeys/reaction-events.md)
      + [Segmentqualifizierung](using/building-journeys/segment-qualification-events.md)
      + [Bedingung](using/building-journeys/condition-activity.md)
      + [Warten](using/building-journeys/wait-activity.md)
      + [Segment lesen](using/building-journeys/read-segment.md)
      + [E-Mail, SMS, Push](using/building-journeys/journeys-message.md)
      + [Benutzerdefinierte Aktionen](using/building-journeys/using-custom-actions.md)
      + [Aktionen in Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Aktionen in Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Sprung](using/building-journeys/jump.md)
      + [Profil aktualisieren](using/building-journeys/update-profiles.md)
   + Ausdrücke erstellen {#building-advanced-conditions-journeys}
      + [Übersicht](using/building-journeys/expression/expressionadvanced.md)
      + Syntax {#syntax}
         + [Allgemeines](using/building-journeys/expression/generalities.md)
         + [Bedingte Anweisung](using/building-journeys/expression/conditional-instruction.md)
         + [Datentypen](using/building-journeys/expression/data-types.md)
         + [Feldverweise](using/building-journeys/expression/field-references.md)
         + [Funktionen zur Verwaltung von Sammlungen](using/building-journeys/expression/collection-management-functions.md)
         + [Benutzer](using/building-journeys/expression/operators.md)
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
            + [currentTime &#x200B; InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
            + [Schnittmenge](using/building-journeys/functions/functionintersect.md)
            + [limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Mathematisch {#math}
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
   + Anwendungsbeispiele {#journey-use-cases}
      + Anwendungsfälle für Unternehmen {#business-use-cases}
         + [Senden von kanalübergreifenden Nachrichten](using/building-journeys/journeys-uc.md)
         + [Nachricht mit Campaign v7/v8 senden](using/building-journeys/ajo-ac.md)
         + [Nachricht an Abonnenten senden](using/building-journeys/message-to-subscribers-uc.md)
      + Technische Anwendungsfälle {#technical-use-cases}
         + [Dynamisches Übergeben von Sammlungen mithilfe benutzerdefinierter Aktionen](using/building-journeys/collections.md)
         + [Sendungen vorantreiben](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen](using/building-journeys/limit-throughput.md)
+ Kampagnen{#campaigns}
   + [Erste Schritte mit Kampagnen](using/campaigns/get-started-with-campaigns.md)
   + [Kampagne erstellen](using/campaigns/create-campaign.md)
   + [Kampagne überprüfen und aktivieren](using/campaigns/review-activate-campaign.md)
   + [Verwalten von Kampagnen](using/campaigns/modify-stop-campaign.md)
   + Inhaltsexperiment {#content-experiment}
      + [Erste Schritte mit dem Inhaltsexperiment](using/campaigns/get-started-experiment.md)
      + [Erstellen eines Inhaltsexperiments](using/campaigns/content-experiment.md)
      + [Statistische Berechnungen verstehen](using/campaigns/experiment-calculations.md)
      + [Konfigurieren von Experimentberichten](using/campaigns/reporting-configuration.md)
   + [Auslösen von Kampagnen mithilfe von APIs](using/campaigns/api-triggered-campaigns.md)
+ Email-Kanal {#email}
   + [Erste Schritte mit E-Mails](using/email/get-started-email.md)
   + [E-Mail erstellen](using/email/create-email.md)
   + E-Mail-Inhalt gestalten {#design-email}
      + [Erste Schritte mit E-Mail-Design](using/email/get-started-email-design.md)
      + Erstellen von Inhalten {#start-creating-content}
         + [Neu beginnen](using/email/content-from-scratch.md)
         + [E-Mail-Inhalt importieren](using/email/existing-content.md)
         + [Code Ihres eigenen Inhalts](using/email/code-content.md)
         + [Arbeiten mit Vorlagen](using/email/email-templates.md)
      + Inhaltserstellung {#add-content}
         + [Inhaltskomponenten verwenden](using/email/content-components.md)
         + [Links hinzufügen und Nachrichten verfolgen](using/email/message-tracking.md)
         + Verwalten von Assets {#manage-asset}
            + [Arbeiten mit Assets Essentials](using/email/assets-essentials.md)
            + [Arbeiten mit Adobe Stock](using/email/stock.md)
         + [Personalisierte Angebote einfügen](using/email/add-offers-email.md)
         + [Textversion generieren](using/email/text-version-email.md)
         + [Preheader hinzufügen](using/email/preheader.md)
      + Stil bearbeiten {#edit-style}
         + [Erste Schritte mit E-Mail-Stil](using/email/get-started-email-style.md)
         + [Hintergrundeinstellungen bearbeiten](using/email/backgrounds.md)
         + [Anpassen der vertikalen Ausrichtung und des Abstands](using/email/alignment-and-padding.md)
         + [Definieren eines Stils für Links](using/email/styling-links.md)
         + [Inline-Styling-Attribute hinzufügen](using/email/inline-styling.md)
   + [Vorschau erstellen und E-Mail testen](using/email/preview.md)
   + [Verwalten des E-Mail-Opt-outs](using/email/email-opt-out.md)
   + E-Mail-Kanal konfigurieren {#configure-email}
      + [Erste Schritte mit der E-Mail-Konfiguration](using/email/get-started-email-config.md)
      + [E-Mail-Oberflächeneinstellungen konfigurieren](using/email/email-settings.md)
+ In-App-Kanal{#in-app}
   + [Erste Schritte mit dem In-App-Kanal](using/in-app/get-started-in-app.md)
   + [In-App-Kanal konfigurieren](using/in-app/inapp-configuration.md)
   + [In-App-Nachricht erstellen](using/in-app/create-in-app.md)
   + [Erstellen von In-App-Inhalten](using/in-app/design-in-app.md)
   + [In-App-Bericht](using/in-app/inapp-report.md)
+ Push-Benachrichtigungskanal{#push}
   + [Erste Schritte mit Push-Benachrichtigungen](using/push/get-started-push.md)
   + [Push-Benachrichtigung erstellen](using/push/create-push.md)
   + [Push-Benachrichtigung erstellen](using/push/design-push.md)
   + [Push-Benachrichtigung senden](using/push/send-push.md)
   + Push-Benachrichtigungen konfigurieren{#push-config}
      + [Push-Benachrichtigungen und Adobe Journey Optimizer](using/push/push-gs.md)
      + [Push-Benachrichtigungskanal konfigurieren](using/push/push-configuration.md)
+ SMS-Kanal{#sms}
   + [Erste Schritte mit SMS](using/sms/get-started-sms.md)
   + [SMS erstellen](using/sms/create-sms.md)
   + [SMS senden](using/sms/send-sms.md)
   + [SMS-Abmeldung verwalten](using/sms/sms-opt-out.md)
   + [SMS-Kanal konfigurieren](using/sms/sms-configuration.md)
+ Briefpost {#direct-mail}
   + [Briefpost erstellen](using/direct-mail/create-direct-mail.md)
   + [Briefpost konfigurieren](using/direct-mail/direct-mail-configuration.md)
+ Webkanal{#web}
   + [Erste Schritte mit dem Webkanal](using/web/get-started-web.md)
   + [Weberfahrungen erstellen](using/web/create-web.md)
   + [Autoren-Webseiten](using/web/author-web.md)
   + [Visual Editing Helper-Erweiterung](using/web/visual-editing-helper.md)
   + [Webberichte](using/web/web-report.md)
+ Landingpages {#landing-pages}
   + [Erste Schritte mit Landingpages](using/landing-pages/get-started-lp.md)
   + [Landingpage erstellen](using/landing-pages/create-lp.md)
   + Inhaltserstellung {#landing-pages-design}
      + [Über die Landingpage-Erstellung](using/landing-pages/design-lp.md)
      + [Landingpage-Inhalt erstellen](using/landing-pages/lp-content.md)
      + [Vorlagen erstellen](using/landing-pages/lp-templates.md)
      + [Benutzerdefiniertes JavaScript hinzufügen](using/landing-pages/lp-custom-js.md)
   + [Abonnementliste erstellen](using/landing-pages/subscription-list.md)
   + [Anwendungsbeispiele](using/landing-pages/lp-use-cases.md)
   + Landingpages konfigurieren {#lp-configuration}
      + [Landingpage-Subdomains konfigurieren](using/landing-pages/lp-subdomains.md)
      + [Landingpage-Vorgaben definieren](using/landing-pages/lp-presets.md)
+ Personalisierung und dynamischer Inhalt {#personalized-dynamic-content}
   + Personalisierung {#personalization}
      + [Erste Schritte mit der Personalisierung](using/personalization/personalize.md)
      + [Personalisierungskontexte](using/personalization/personalization-contexts.md)
      + Ausdrücke erstellen {#build-expressions}
         + [Personalisierungssyntax](using/personalization/personalization-syntax.md)
         + Arbeiten mit dem Ausdruckseditor {#expression-editor}
            + [Über den Ausdruckseditor](using/personalization/personalization-build-expressions.md)
            + [Hinzufügen von Attributen zu Favoriten](using/personalization/personalization-favorites.md)
            + [Arbeiten mit gespeicherten Ausdrücken](using/personalization/personalization-library.md)
            + [Personalisierungsvalidierung](using/personalization/personalization-validation.md)
         + Hilfsfunktionen{#functions}
            + [Erste Schritte mit Hilfsfunktionen](using/personalization/functions/functions.md)
            + [Aggregationsfunktionen](using/personalization/functions/aggregation.md)
            + [Arithmetische Funktionen](using/personalization/functions/arithmetic-functions.md)
            + [Arrays und Listenfunktionen](using/personalization/functions/arrays-list.md)
            + [Datumsfunktionen](using/personalization/functions/dates.md)
            + [Boolesche und Vergleichsfunktionen](using/personalization/functions/operators.md)
            + [Helfer](using/personalization/functions/helpers.md)
            + [Zuordnungsfunktionen](using/personalization/functions/maps.md)
            + [Objektfunktionen](using/personalization/functions/objects.md)
            + [Zeichenfolgen-Funktionen](using/personalization/functions/string.md)
      + Anwendungsbeispiele{#personalization-use-cases}
         + [Benachrichtigung zum Bestellstatus](using/personalization/personalization-use-case.md)
         + [E-Mail zum Warenkorbabbruch](using/personalization/personalization-use-case-helper-functions.md)
   + Dynamische Inhalte {#dynamic}
      + [Erste Schritte mit dynamischen Inhalten](using/personalization/get-started-dynamic-content.md)
      + [Bedingte Regeln erstellen](using/personalization/create-conditions.md)
      + [Dynamischen Inhalt erstellen](using/personalization/dynamic-content.md)
+ Segmente, Profile und Identität{#segment}
   + Segmente {#segments}
      + [Erste Schritte mit Segmenten](using/segment/about-segments.md)
      + [Segmente erstellen](using/segment/creating-a-segment.md)
   + Profile{#profiles}
      + [Erste Schritte mit Profilen](using/segment/get-started-profiles.md)
      + [Testprofile erstellen](using/segment/creating-test-profiles.md)
   + [Identitäten](using/segment/get-started-identity.md)
   + Erstellen von Zielgruppen {#audience-orchestration}
      + [Erste Schritte mit der Komposition von Zielgruppen](using/segment/get-started-audience-orchestration.md)
      + [Erstellen von Komposition-Workflows](using/segment/create-compositions.md)
      + [Arbeiten mit der Arbeitsfläche für Kompositionen](using/segment/composition-canvas.md)
      + [Zielgruppen aufrufen und verwalten](using/segment/access-audiences.md)
   + [Lizenzverwendung](using/segment/license-usage.md)
+ Tracken und überwachen {#reporting}
   + Live-Bericht {#live-report}
      + [Erste Schritte mit dem Live-Bericht](using/reports/live-report.md)
      + [Journey Live-Bericht](using/reports/journey-live-report.md)
      + [Kampagnen-Live-Bericht](using/reports/campaign-live-report.md)
      + [Live-Bericht für Landingpage](using/reports/lp-report-live.md)
      + [Live-Bericht zur Abonnementliste](using/reports/subscription-report-live.md)
   + Gesamtbericht {#global-report}
      + [Erste Schritte mit dem globalen Bericht](using/reports/global-report.md)
      + [Journey Global-Bericht](using/reports/journey-global-report.md)
      + [Campaign Global-Bericht](using/reports/campaign-global-report.md)
      + [Landingpage Globaler Bericht](using/reports/lp-report-global.md)
      + [Abonnementliste Allgemeiner Bericht](using/reports/subscription-report-global.md)
   + Journey-Berichte {#reports}
      + [Erstellen von Journey-Berichten](using/reports/sharing-overview.md)
      + [Schrittereignisfeldliste](using/reports/sharing-field-list.md)
      + Ereignisfelder für veraltete Schritte {#legacy-step-event-fields}
         + [Über veraltete Felder](using/reports/sharing-legacy-fields.md)
         + [Journey-Felder](using/reports/sharing-journey-fields.md)
         + [Allgemeine Felder](using/reports/sharing-common-fields.md)
         + [Aktionsausführungsfelder](using/reports/sharing-execution-fields.md)
         + [Datenabruffelder](using/reports/sharing-fetch-fields.md)
         + [Identitätsfelder](using/reports/sharing-identity-fields.md)
      + [Beispiele für Abfragen](using/reports/query-examples.md)
   + Zustellbarkeit {#deliverability}
      + [Erste Schritte mit der Zustellbarkeit](using/reports/deliverability.md)
      + [Unterdrückungsliste verstehen](using/reports/suppression-list.md)
   + [Warnhinweise](using/reports/alerts.md)
   + [Arbeiten mit Customer Journey Analytics](using/reports/cja-ajo.md)
+ Entscheidungsmanagement {#offer-decisioning}
   + Erste Schritte mit der Entscheidungsverwaltung {#get-started-decision}
      + [Über die Entscheidungsverwaltung](using/offers/get-started/starting-offer-decisioning.md)
      + [Benutzeroberfläche](using/offers/get-started/user-interface.md)
      + [Wichtige Schritte zum Erstellen und Verwalten von Angeboten](using/offers/offer-library/key-steps.md)
      + [Anwendungsfall: Angebote in eine E-Mail einfügen](using/offers/offers-e2e.md)
   + Erstellen von Komponenten {#create-components}
      + [Platzierungen erstellen](using/offers/offer-library/creating-placements.md)
      + [Entscheidungsregeln erstellen](using/offers/offer-library/creating-decision-rules.md)
      + [Tags erstellen](using/offers/offer-library/creating-tags.md)
   + Rankings erstellen {#rankings}
      + [Erste Schritte mit Ranglisten](using/offers/ranking/get-started-rankings.md)
      + [Ranking-Formeln](using/offers/ranking/create-ranking-formulas.md)
      + AI-Modelle {#ai-models}
         + [Über KI-Modelle](using/offers/ranking/ai-models.md)
         + AI-Modelltypen {#ai-model-types}
            + [Automatisierte Optimierungsmodelle](using/offers/ranking/auto-optimization-model.md)
            + [Personalisiertes Optimierungsmodell](using/offers/ranking/personalized-optimization-model.md)
         + Erstellen von KI-Modellen {#configure-ai-model}
            + [Datensatz zum Erfassen von Ereignissen erstellen](using/offers/ranking/create-dataset.md)
            + [Erstellen eines KI-Modells](using/offers/ranking/create-ranking-strategies.md)
            + [Ereigniserfassung konfigurieren](using/offers/ranking/schema-requirement.md)
   + Angebote erstellen und verwalten {#managing-offers-in-the-offer-library}
      + Angebote konfigurieren {#configure-offers}
         + [Personalisierte Angebote erstellen](using/offers/offer-library/creating-personalized-offers.md)
         + [Hinzufügen von Darstellungen](using/offers/offer-library/add-representations.md)
         + [Einschränkungen hinzufügen](using/offers/offer-library/add-constraints.md)
      + [Fallback-Angebote erstellen](using/offers/offer-library/creating-fallback-offers.md)
      + [Kollektionen erstellen](using/offers/offer-library/creating-collections.md)
   + Entscheidungen erstellen und verwalten {#create-manage-activities}
      + [Entscheidungen erstellen](using/offers/offer-activities/create-offer-activities.md)
      + [Angebotsauswahl in Entscheidungen konfigurieren](using/offers/offer-activities/configure-offer-selection.md)
      + [Simulationen erstellen](using/offers/offer-activities/simulation.md)
   + [Batch-Entscheidungsfindung](using/offers/batch-delivery.md)
   + Erstellen von Entscheidungsverwaltungsberichten {#create-reports}
      + [Erste Schritte mit Entscheidungsverwaltungsereignissen](using/offers/reports/get-started-events.md)
      + [Wichtige Informationen zu Entscheidungsverwaltungsereignissen](using/offers/reports/key-information.md)
      + [Zugreifen auf Ereignisse XDM-Felder](using/offers/reports/xdm-fields.md)
   + Angebotskatalog exportieren {#export-catalog}
      + [Erste Schritte mit dem Export von Angebotskatalogen ](using/offers/export-catalog/get-started-export.md)
      + [Zugriff auf den exportierten Angebotskatalog](using/offers/export-catalog/access-dataset.md)
      + [Datensatz für personalisierte Angebote](using/offers/export-catalog/export-offers.md)
      + [Entscheidungsdatensatz](using/offers/export-catalog/export-decisions.md)
      + [Platzierungs-Datensatz](using/offers/export-catalog/export-placements.md)
      + [Fallback-Datensatz](using/offers/export-catalog/export-fallback.md)
   + API-Referenz {#api-reference}
      + [Erste Schritte](using/offers/api-reference/getting-started.md)
      + Angebote mithilfe von APIs erstellen und verwalten {#offers-api}
         + Praktika {#placements}
            + [Platzierungen auflisten](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Platzierung nachschlagen](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Platzierung erstellen](using/offers/api-reference/offers-api/placements/create.md)
            + [Platzierung aktualisieren](using/offers/api-reference/offers-api/placements/update.md)
            + [Platzierung löschen](using/offers/api-reference/offers-api/placements/delete.md)
         + Entscheidungsregeln {#decision-rules}
            + [Entscheidungsregeln auflisten](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Entscheidungsregel nachschlagen](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Entscheidungsregel erstellen](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Entscheidungsregel aktualisieren](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Entscheidungsregel löschen](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Tags {#tags}
            + [Tags auflisten](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Tag nachschlagen](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Tag erstellen](using/offers/api-reference/offers-api/tags/create.md)
            + [Tag aktualisieren](using/offers/api-reference/offers-api/tags/update.md)
            + [Tag löschen](using/offers/api-reference/offers-api/tags/delete.md)
         + Personalisierte Angebote {#personalized-offers}
            + [Personalisierte Angebote auflisten](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [Personalisiertes Angebot nachschlagen](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [Personalisiertes Angebot erstellen](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [Personalisiertes Angebot aktualisieren](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [Personalisiertes Angebot löschen](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + Sammlungen {#collections}
            + [Kollektionen auflisten](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [Kollektion nachschlagen](using/offers/api-reference/offers-api/collections/lookup.md)
            + [Kollektion erstellen](using/offers/api-reference/offers-api/collections/create.md)
            + [Kollektion aktualisieren](using/offers/api-reference/offers-api/collections/update.md)
            + [Kollektion löschen](using/offers/api-reference/offers-api/collections/delete.md)
         + Fallback-Angebote {#fallback-offers}
            + [Fallback-Angebote auflisten](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Fallback-Angebot nachschlagen](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Fallback-Angebot erstellen](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Fallback-Angebot aktualisieren](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Fallback-Angebot löschen](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Entscheidungen mithilfe von APIs erstellen und verwalten {#activities-api}
         + [Entscheidungen auflisten](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Entscheidung nachschlagen](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Entscheidung erstellen](using/offers/api-reference/activities-api/activities/create.md)
         + [Entscheidung aktualisieren](using/offers/api-reference/activities-api/activities/update.md)
         + [Entscheidung löschen](using/offers/api-reference/activities-api/activities/delete.md)
      + Angebote mithilfe von APIs bereitstellen {#offer-delivery-api}
         + [Erste Schritte mit APIs für die Angebotsbereitstellung](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [Decisioning API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [Edge Decisioning-API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [Batch Decisioning-API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Data Management {#data-management}
   + [Erste Schritte mit der Datenverwaltung](using/data/gs-data.md)
   + [Arbeiten mit Schemata](using/data/get-started-schemas.md)
   + Journey Optimizer-Datensätze {#datasets}
      + [Erste Schritte mit Datensätzen](using/data/get-started-datasets.md)
      + [Beispiele für Abfragen](using/data/datasets-query-examples.md)
   + [Abfragen](using/data/get-started-queries.md)
+ Konfiguration{#configuration}
   + [Erste Schritte mit der Konfiguration von Journey Optimizer](using/configuration/get-started-configuration.md)
   + E-Mail-Subdomains zuweisen {#delegate-subdomains}
      + [Erste Schritte mit der Zuweisung von Subdomains](using/configuration/about-subdomain-delegation.md)
      + [Zuweisen einer Subdomain](using/configuration/delegate-subdomain.md)
      + [Hinzufügen eines Google TXT-Eintrags](using/configuration/google-txt.md)
      + [Zugreifen auf und Bearbeiten von PTR-Datensätzen](using/configuration/ptr-records.md)
      + [Erstellen von IP-Pools](using/configuration/ip-pools.md)
   + [Einrichten von Kanaloberflächen](using/configuration/channel-surfaces.md)
   + E-Mail-Adressen überwachen {#monitor-reputation}
      + [Unterdrückungsliste](using/configuration/manage-suppression-list.md)
      + [Weitere Zustellversuche](using/configuration/retries.md)
      + [Zulässige Liste](using/configuration/allow-list.md)
   + [Unterstützung für Archivierung](using/configuration/archiving-support.md)
   + [Häufigkeitsregeln konfigurieren](using/configuration/frequency-rules.md)
   + [Verwalten von Ausführungsadressen](using/configuration/primary-email-addresses.md)
   + Journeys konfigurieren {#configure-journeys}
      + [Über Datenquellen, Ereignisse und Aktionen](using/configuration/about-data-sources-events-actions.md)
      + [Integration mit externen Systemen](using/configuration/external-systems.md)
      + Ereigniskonfiguration {#events-journeys}
         + [Allgemeine Funktionsweise](using/event/about-events.md)
         + Einzelereignisse konfigurieren {#unitary-events}
            + [Erste Schritte mit Einzelereignissen](using/event/about-creating.md)
            + [Informationen zu ExperienceEvent-Schemata](using/event/experience-event-schema.md)
            + [Nutzung von Adobe Analytics](using/event/about-analytics.md)
         + [Business-Ereignis konfigurieren](using/event/about-creating-business.md)
         + [Zusätzliche Schritte zum Senden von Ereignissen](using/event/additional-steps-to-send-events-to-journey.md)
      + Datenquellenkonfiguration{#data-source-journeys}
         + [Über Datenquellen](using/datasource/about-data-sources.md)
         + [Datenquelle konfigurieren](using/datasource/configure-data-sources.md)
         + [Datenquelle von Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Externe Datenquellen](using/datasource/external-data-sources.md)
      + Aktionskonfiguration {#action-journeys}
         + [Über Aktionen](using/action/action.md)
         + [Konfigurieren einer Aktion](using/action/about-custom-action-configuration.md)
         + [Integration mit Adobe Campaign Standard](using/action/acs-action.md)
         + [Integration mit Adobe Campaign v7/v8](using/action/acc-action.md)
   + [Quellen](using/start/get-started-sources.md)
+ Zugriffskontrolle {#access-control}
   + [Zugriffskontrolle - Übersicht](using/administration/permissions-overview.md)
   + [Integrierte Produktprofile](using/administration/ootb-product-profiles.md)
   + [Benutzer und Produktprofile verwalten](using/administration/permissions.md)
   + [Berechtigungsebenen](using/administration/high-low-permissions.md)
   + [Sandbox-Verwaltung](using/administration/sandboxes.md)
   + [Attributbasierte Zugriffssteuerung](using/administration/attribute-based-access.md)
   + [Zugriffskontrolle auf Objektebene](using/administration/object-based-access.md)
+ Datenschutz {#privacy}
   + [Erste Schritte mit Datenschutz](using/privacy/get-started-privacy.md)
   + [Datenschutzanfragen](using/privacy/requests.md)
   + [Prüfmaßnahmen für Ressourcen](using/privacy/audit-logs.md)
   + Einverständnis verwalten {#consent}
      + [Opt-out verwalten](using/privacy/opt-out.md)
      + [Arbeiten mit Zustimmungsrichtlinien](using/action/consent.md)
   + [Data Governance](using/action/action-privacy.md)
