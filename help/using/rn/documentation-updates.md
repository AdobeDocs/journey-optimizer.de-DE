---
solution: Journey Optimizer
product: journey optimizer
title: Dokumentation – Aktualisierungen
description: Erfahren Sie mehr über die letzten Aktualisierungen der Dokumentation
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: e0f7eca8b3313cb5eb8e201c567622ded20a82d2
workflow-type: tm+mt
source-wordcount: '4103'
ht-degree: 97%

---

# Dokumentation – Aktualisierungen {#latest-updates}

Auf dieser Seite werden alle Aktualisierungen der Dokumentation für [!DNL Journey Optimizer] aufgelistet.

## November 2023 {#nov-2023}

* Die Limits, die alle benutzerdefinierten Aktionen einschränken, wurden von 150.000 Aufrufen über 30 Sekunden auf 300.000 Aufrufe über eine Minute geändert. Darüber hinaus gilt die Standardbegrenzung nicht mehr für jeden Endpunkt. Er wird jetzt pro Host und Sandbox ausgeführt. Wenn Sie beispielsweise in einer Sandbox zwei Endpunkte mit demselben Host haben (z. B.: `https://www.adobe.com/endpoint1` und `https://www.adobe.com/endpoint2`), gilt die Begrenzung für alle Endpunkte unter dem Host adobe.com . &quot;endpoint1&quot;und &quot;endpoint2&quot;verwenden dieselbe Begrenzungskonfiguration. Wenn ein Endpunkt die Grenze erreicht, wirkt sich dies auf den anderen Endpunkt aus. [Weitere Informationen](../action/about-custom-action-configuration.md)

## Oktober 2023 {#oct-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Oktober 2023 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Es wurden GIFs hinzugefügt, um einige wichtige Funktionen zu veranschaulichen, z. B.: [Inhaltsvorlagen](../content-management/content-templates.md), [Fragmente](../content-management/fragments.md), [Berechnete Attribute](../audience/computed-attributes.md), [Briefpost](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Optimierungsmodelle für das Entscheidungs-Management](../offers/ranking/personalized-optimization-model.md), [API-gesteuerte Kampagnen](../campaigns/api-triggered-campaigns.md) und [Inhaltsexperimente](../campaigns/content-experiment.md).
* Der Prozess zur Schemaerstellung wurde aktualisiert, um die neuesten Aktualisierungen der Benutzeroberfläche widerzuspiegeln, die mit Änderungen an Adobe Experience Platform eingeführt wurden. [Weitere Informationen](../audience/creating-test-profiles.md)
* Auf der Seite „Limits und Einschränkungen“ wurden Leitlinien für das Entscheidungs-Management hinzugefügt. [Weitere Informationen](../start/guardrails.md#decision-management)
* Der Abschnitt zu Kopfzeilenparametern wurde aktualisiert, um die Handhabung von Abwesenheitsbenachrichtigungen und Challenge-Responses widerzuspiegeln (sie werden an der **[!UICONTROL Fehler-E-Mail-Adresse]** empfangen). [Weitere Informationen](../email/email-settings.md#email-header)
* Es wurde ein neuer Abschnitt dazu erstellt, wie Sie Ihren Inhalt in der Vorschau anzeigen und testen können. [Weitere Informationen](../content-management/preview-test.md)
* Die Seite zum Implementieren von Einzelseitenanwendungen wurde in die Dokumentation zum Adobe Experience Platform Web SDK verschoben. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=de){target="_blank"}
* Der Abschnitt „Begrenzung“ wurde aktualisiert, um die Beschriftungsänderungen im Zusammenhang mit der Angebotsbegrenzung in der Entscheidungs-Management-Oberfläche widerzuspiegeln. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping)
* Der Abschnitt zum Hinzufügen dynamischer Inhalte zu E-Mails wurde aktualisiert und enthält jetzt auch Informationen zum Löschen einer Variante. [Weitere Informationen](../personalization/dynamic-content.md#emails)
* Das Beispiel für Konfigurationen für Begrenzungen und Einschränkungen wurde aktualisiert. [Weitere Informationen](../configuration/external-systems.md)
* Die Beschränkung für skalare Arrays wurde aus dem Abschnitt zur externen Datenquelle entfernt. [Weitere Informationen](../datasource/external-data-sources.md)
* Der Anwendungsfall für Journeys mit mehreren Kanälen wurde aktualisiert. [Weitere Informationen](../building-journeys/journeys-uc.md)
* Der Journey Optimizer-Dokumentationssatz wurde aktualisiert, um den neuen Erstellungsprozess für Experience Platform-Schemata widerzuspiegeln.

## September 2023 {#september-2023}

* Alle neuen Funktionen und Verbesserungen, die mit der Version September 2023 von [!DNL Journey Optimizer] erscheinen, werden in der Dokumentation detailliert beschrieben. [Weitere Informationen](release-notes.md)
* Es wurde eine neue Seite mit Best Practices für die Skalierung und einer Anleitung für das Zuordnen in Echtzeit hinzugefügt. [Weitere Informationen](../start/best-practices.md)

  <!--  * The maximum wait duration has been changed from 30 to 29 days. [Read more](../building-journeys/wait-management.md) -->

* Für die Sendezeitoptimierung wurde ein Abschnitt „Häufig gestellte Fragen“ hinzugefügt. [Weitere Informationen](../building-journeys/journeys-message.md#faq-send-time)
* Für die Aktivität „Zielgruppenqualifizierung“ wurde ein Hinweis hinzugefügt. Es kann bis zu 10 Minuten dauern, bis die Aktivität aktiv ist und Profile überwacht, die in die Zielgruppe eintreten oder sie verlassen. [Weitere Informationen](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* Eine Liste der Einschränkungen, die bei der Erstellung von Entscheidungsregeln zu beachten sind, wurde der Dokumentation zum Entscheidungs-Management hinzugefügt. [Weitere Informationen](../offers/offer-library/creating-decision-rules.md)
* Die Links zur Dokumentation zur Zugriffssteuerung wurden aktualisiert. [Weitere Informationen](../administration/permissions.md)
* Die Voraussetzungen für In-App-Kanäle wurden mit Details zur Datenerfassung von Adobe Experience Platform aktualisiert. [Weitere Informationen](../in-app/inapp-configuration.md)
* Einige der in Beispielen für Ranking-Formeln dargestellten Ausdrücke wurden aktualisiert, um Validierungsfehler zu vermeiden. [Weitere Informationen](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* Es wurde ein Warnhinweis zum Abschnitt „Definieren von Entscheidungsbereichen“ hinzugefügt. Bei der Verwendung eines KI-Modells in einer Bewertungskriterien-Gruppe müssen alle Bewertungskriterien in dieser Gruppe die KI-Rangfolgenmethode mit demselben spezifischen KI-Modell verwenden. Darüber hinaus kann nur eine Bewertungskriterien-Gruppe das KI-Modell verwenden. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version von August 2023 wurden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Der Hinweis zur **Verwaltung des Authentifizierungs-Caches** in einer Journey wurde aktualisiert, um zu präzisieren, dass das Token nicht zwischen verschiedenen Journeys geteilt wird. [Weitere Informationen](../datasource/external-data-sources.md#custom-authentication-mode)
* Die Seite zur **Eintragsverwaltung** für Journeys wurde aktualisiert, um das Verhalten besser zu verdeutlichen. [Weitere Informationen](../building-journeys/entry-management.md)
* **Export-Datensätze** für Offer Decisioning sind jetzt standardmäßig aktiviert. Der Hinweis zum vorherigen Verhalten wurde entfernt.  [Weitere Informationen](../offers/export-catalog/get-started-export.md)
* Verschiedene **Kampagnenberichtsmetriken** wurden sowohl in den Live-Berichten als auch in den globalen Berichten umbenannt. [Weitere Informationen](../reports/campaign-global-report.md)
* Es wurde ein neuer Abschnitt zu den Voraussetzungen für Inhaltsexperimente für den Web-Kanal hinzugefügt. [Weitere Informationen](../web/web-prerequisites.md#experiment-prerequisites)
* Es wurde ein Warnhinweis zur Seite **Arbeiten mit Inhaltsvorlagen** hinzugefügt, um anzugeben, dass Tracking beim Testen von E-Mail-Inhaltsvorlagen derzeit nicht unterstützt wird. Zum Testen des Trackings müssen Sie die Inhaltsvorlage in einer E-Mail verwenden und einen Testversand durchführen. [Weitere Informationen](../content-management/content-templates.md#test-template)
* Es wurden mehrere Warnungen im Abschnitt **Erstellen und Veröffentlichen von Landingpages** hinzugefügt, um anzugeben, dass Sie nicht auf Ihre Landingpage zugreifen können, indem Sie die bei der Erstellung der Seite definierte URL einfach in einen Webbrowser kopieren, selbst wenn die Seite bereits veröffentlicht wurde. Stattdessen können Sie sie mit der Vorschaufunktion testen. [Weitere Informationen](../landing-pages/create-lp.md)
* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie für den Briefpost-Kanal das **Einverständnis verwaltet wird**. [Weitere Informationen](../direct-mail/test-send-direct-mail.md)

## Juli 2023 {#july-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Juli 2023 wurden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Die Seite mit der Dokumentation zur Warteaktivität wurde um zusätzliche Informationen und Best Practices im Zusammenhang mit der globalen Zeitüberschreitung und der Verwendung von Wiedereintritten erweitert. [Weitere Informationen](../building-journeys/wait-activity.md)
* Die Seite zur Einstiegsverwaltung wurde verbessert. [Weitere Informationen](../building-journeys/entry-management.md)
* In der Dokumentation zur Aktivität „Zielgruppe lesen“ wurden zusätzliche Informationen zur Drosselungsrate hinzugefügt. [Weitere Informationen](../building-journeys/read-audience.md)
* Es wurden zusätzliche Informationen zu erneuten Zustellversuchen hinzugefügt. [Weitere Informationen](../start/guardrails.md#general-actions-g)
* Der Abschnitt **Implementieren der Personalisierungszustimmung** wurde aktualisiert, um zu beschreiben, wie die Personalisierungszustimmung in Kampagnen manuell erzwungen werden kann: Sie können den Segment-Regel-Builder verwenden, um eine Zielgruppe zu erstellen, die Opt-out-Profile enthält, oder eine Aufspaltungsaktivität zu einem Kompositions-Workflow hinzufügen. [Weitere Informationen](../privacy/opt-out.md#opt-out-expression-editor)

## Juni 2023 {#june-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Juni 2023 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Im Übersichtsbildschirm der Journey wurden Informationen zum Verhältnis der Verwerfnisrate hinzugefügt. [Weitere Informationen](../building-journeys/journey-gs.md#journey-access)
* Es wurde ein Hinweis mit Schritten hinzugefügt, mit denen Sie nach dem Erstellen eines Ereignisses Ihr Schema mit neuen Nummerierungswerten versehen können. [Weitere Informationen](../event/about-creating.md)
* Es wurde eine Empfehlung hinzugefügt, dass bei der Abfrage von Journeys „JourneyVersionID“ anstelle von „journeyVersionName“ verwendet werden sollte. [Weitere Informationen](../reports/sharing-common-fields.md#journeyversionid-field)
* Es wurden weitere Beispiele zur Reihenfolge der Auswertungskriterien zum Abschnitt **Erstellen von Entscheidungen** hinzugefügt, um Fälle zu veranschaulichen, in denen mehrere Kriterien und mehrere Entscheidungsbereiche verwendet werden. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Die Dokumentation zum Entscheidungs-Management wurde mit dem Hinweis ergänzt, dass die Verwendung der Zugriffskontrolle auf Objektebene nicht für dynamische Sammlungen verfügbar ist. [Weitere Informationen](../offers/offer-library/creating-collections.md)

## Mai 2023 {#may-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom Mai 2023 werden in der Dokumentation ausführlich beschrieben. [Weitere Informationen](release-notes.md)
* Es wurde eine neue Seite hinzugefügt, auf der beschrieben wird, wie Sie die Subdomain einrichten, die zum Veröffentlichen von Inhalten aus Adobe Experience Manager Assets Essentials in Ihren Web-Erlebnissen verwendet wird. [Weitere Informationen](../web/web-delegated-subdomains.md)
* Es wurde ein neuer Unterabschnitt hinzugefügt, in dem erläutert wird, wie Sie im E-Mail-Designer personalisierte Tracking-Parameter zu URLs hinzufügen. [Weitere Informationen](../email/message-tracking.md#url-tracking)
* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Sie sicherstellen können, dass die Auswahl Ihrer Kundschaft, die sich gegen die Verwendung ihrer Profildaten für die Personalisierung entscheidet, berücksichtigt wird. [Weitere Informationen](../privacy/opt-out.md#opt-out-personalization)
* Es wurde ein Hinweis zur Verwendung von internationalen Sonderzeichen in URLs hinzugefügt, die in E-Mail-Inhalten enthalten sind. [Weitere Informationen](../email/message-tracking.md#insert-links)
* Die zum Testen und Veröffentlichen von Landingpages erforderliche Berechtigung wurde hinzugefügt. [Weitere Informationen](../landing-pages/create-lp.md)
* Es wurde ein Hinweis zu den Adobe Experience Platform-Endpunkten hinzugefügt, die erforderlich sind, damit Ihre benutzerdefinierten Ereignisse bei der Frequenzlimitierung im Entscheidungs-Management berücksichtigt werden. [Weitere Informationen](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version April 2023 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Es wurde ein Hinweis hinzugefügt, dass integrierte Aktionen nicht entfernt werden können. [Weitere Informationen](../start/guardrails.md#custom-actions-g)
* Es wurden Informationen zu serviceEvents sowie ein Abfragebeispiel hinzugefügt, um die Details eines serviceEvent zu überprüfen. [Weitere Informationen](../reports/query-examples.md#common-queries)
* Es wurde ein Hinweis hinzugefügt, dass Sie keine Abfragen zu Zeitreihen durchführen können. [Weitere Informationen](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials und Adobe Stock wurden zur Seite für lösungsübergreifende Integrationen hinzugefügt. [Weitere Informationen](../start/ajo-integrations.md)
* Die Warnung, dass E-Mail-Subdomains mit mehreren Ebenen nicht zulässig seien, wurde entfernt, da diese jetzt unterstützt werden. [Weitere Informationen](../configuration/delegate-subdomain.md)
* Es wurde ein Hinweis hinzugefügt, dass Sie bei Änderungen an einer Angebotsentscheidung, die in einer Journey-Nachricht verwendet wird, die Veröffentlichung der Journey aufheben und sie dann erneut veröffentlichen müssen. [Weitere Informationen](../building-journeys/publishing-the-journey.md)
* Erläuterungen dazu, wie sichergestellt werden kann, dass Ereignisse im Begrenzungszähler korrekt berücksichtigt werden, werden im Entscheidungs-Management-Abschnitt **Begrenzungsereignis** klargestellt. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping-event)
* Es wurde ein neuer Abschnitt zur Seite **Ändern von Ausführungsadressen** hinzugefügt. Dort wird angegeben, dass das in den erweiterten Journey-Parametern festgelegte Ausführungsfeld global überschrieben werden kann. Das Überschreiben von E-Mail-Adressen sollte jedoch nur für bestimmte Anwendungsfälle verwendet werden. Meistens ist der Wert, der als primäre Adresse in den **Ausführungsfeldern** definiert ist, derjenige, der verwendet werden sollte. [Mehr dazu](../configuration/primary-email-addresses.md#journey-parameters)
* Der Abschnitt **URL-Tracking** bietet nun die Liste und Beschreibung aller kontextbezogenen Attribute, die für das URL-Tracking auf einer E-Mail-Kanal-Oberfläche festgelegt werden können. [Weitere Informationen](../email/email-settings.md#url-tracking)

## März 2023 {#march-2023}

* Das Schema-Wörterbuch für Journey Optimizer ist jetzt verfügbar. Es sind darin vollständige Listen der Felder und Attribute für jedes Schema vorhanden.  [Weitere Informationen](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=de)
* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom 23. März werden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Es wurde ein Schritt zur Aktivierung von Adobe Analytics-Ereignissen in Ihren Journeys hinzugefügt. [Weitere Informationen](../event/about-analytics.md)
* Im Entscheidungs-Management-Handbuch wurde ein neuer Abschnitt erstellt, in dem beschrieben wird, wie in Adobe Experience Platform Feedback zu Angebotsentscheidungen eingeholt werden kann, einschließlich, welche Angebote angezeigt werden und wie Benutzende mit ihnen interagieren. [Weitere Informationen](../offers/data-collection/data-collection.md)
* Es wurde ein neuer Unterabschnitt zum Abschnitt **Entscheidung erstellen** hinzugefügt, um den Unterschied zwischen der Auswertung von Kriterien in einer sequenziellen Reihenfolge oder zur gleichen Zeit zu erklären. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Es wurde ein Schutzmechanismus für „Zielgruppe lesen“-Journeys mit inkrementellem Lesen hinzugefügt. Sie können keine neue Version erstellen, sondern müssen die Journey duplizieren. [Weitere Informationen](../start/guardrails.md#journey-versions-g)
* Der Anwendungsfall zur Begrenzung des Durchsatzes wurde mit Informationen zu den Einschränkungsfunktionen aktualisiert. [Weitere Informationen](../building-journeys/limit-throughput.md)
* Es wurde ein Hinweis hinzugefügt, dass skalare Arrays in der Definition der Antwort-Payload nicht unterstützt werden. [Weitere Informationen](../datasource/external-data-sources.md)
* Der Abschnitt zu Profilbegrenzungsbedingungen wurde aktualisiert. [Weitere Informationen](../building-journeys/condition-activity.md#profile_cap)

## Februar 2023 {#feb-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Februar 2023 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Es wurden Informationen zur Symbolleiste der Arbeitsfläche hinzugefügt. [Weitere Informationen](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Es wurden Informationen hinzugefügt, dass interne Adobe-Adressen in URLs und APIs nicht zulässig sind. [Weitere Informationen](../start/guardrails.md)
* In der Dokumentation zu API-ausgelösten Kampagnen wurde ein Hinweis hinzugefügt, in dem festgelegt wird, dass die in die Anfrage übergebenen kontextuellen Attribute 50 KB nicht überschreiten dürfen. [Mehr dazu](../campaigns/api-triggered-campaigns.md#contextual)
* Es wurden Informationen darüber hinzugefügt, wie Opt-out-Informationen im **Einverständnis-Service-Datensatz** gespeichert werden, nachdem Empfängerinnen oder Empfänger über eine Landingpage das Abonnement storniert haben. [Mehr dazu](../landing-pages/lp-use-cases.md#configure-opt-out)

## Januar 2023 {#jan-2023}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Januar 2023 sind in der Dokumentation beschrieben. [Mehr dazu](release-notes.md)
* In der Dokumentation zu Begrenzung wurden Informationen zu benutzerdefinierten Authentifizierungsendpunkten hinzugefügt. [Weitere Informationen](../configuration/external-systems.md)
* Im Abschnitt zu externen Datenquellen wurde ein neues Beispiel für die benutzerdefinierte Authentifizierung hinzugefügt. [Weitere Informationen](../datasource/external-data-sources.md#custom-authentication-mode)
* Es wurde ein Hinweis zum Data Collection Core Service (DCCS) für Journeys hinzugefügt, die durch ein Ereignis ausgelöst werden. [Weitere Informationen](../start/guardrails.md#events-g)
* Ein Hinweis zum Abrufen von Identity-Namespaces wurde zu den Abschnitten [Zielgruppe lesen](../building-journeys/read-audience.md), [Zielgruppen-Qualifizierung](../building-journeys/audience-qualification-events.md) und [Ereigniserstellung](../event/about-creating.md) hinzugefügt.
* Barrierefreiheitsfunktionen in [!DNL Journey Optimizer] sind nun auf einer eigenen Seite gruppiert. [Mehr dazu](../start/accessibility.md)
* Die Beispiele wurden im Abschnitt „Operatoren“ der Dokumentation zum erweiterten Ausdruckseditor aktualisiert. [Weitere Informationen](../building-journeys/expression/operators.md)
* Es wurde ein Hinweis zu den Einschränkungen bei der Suche mit einem Array von Objekten hinzugefügt. [Mehr erfahren](../event/experience-event-schema.md#relationships_limitations)
* Es wurde eine neue Seite zur Datenverwaltung in [!DNL Journey Optimizer] hinzugefügt. [Mehr erfahren](../data/gs-data.md)
* Es wurde eine Tabelle mit allen Codes hinzugefügt, die in der Antwort zurückgegeben werden können, wenn Angebote mithilfe der Decisioning-API bereitgestellt werden. [Mehr erfahren](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++ 2022

## Dezember 2022 {#december-2022}

* Das Nachrichten-Handbuch wurde umstrukturiert und in dedizierte Handbücher für jeden Kanal unterteilt:

   * [E-Mail-Kanal](../email/get-started-email.md)
   * [Kanal für Push-Benachrichtigungen](../push/get-started-push.md)
   * [SMS-Kanal](../sms/get-started-sms.md)

* Das Konfigurationshandbuch wurde neu strukturiert, um die Verständlichkeit zu verbessern. [Mehr erfahren](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Es wurde eine neue Seite über Journey Optimizer-Integrationen hinzugefügt. [Mehr dazu](../start/ajo-integrations.md)
* Es wurde eine Empfehlung zur Länge der URLs von Mirror-Seiten hinzugefügt. [Mehr dazu](../email/message-tracking.md)
* In der Konfiguration der E-Mail-Einstellungen wurde ein neuer Unterabschnitt über die E-Mail-Adresse, an die geantwortet werden soll, hinzugefügt, der Empfehlungen für eine ordnungsgemäße Antwortverwaltung enthält. [Mehr dazu](../email/email-settings.md#reply-to-email)
* Es wurde ein Abschnitt hinzugefügt, in dem beschrieben wird, wie der Inhalt einer Nachricht in einer Live-Journey geändert werden kann. [Mehr dazu](../building-journeys/journeys-message.md#update-live-content)

## Oktober 2022 {#october-2022}

* Es wurde ein Journey-Anwendungsfall zur Begrenzung des Durchsatzes mithilfe von externen Datenquellen und benutzerdefinierten Aktionen hinzugefügt. [Mehr dazu](../building-journeys/limit-throughput.md)
* Der Abschnitt zum Journey-Anwendungsfall wurde in zwei Kategorien umstrukturiert: [Geschäftliche Anwendungsfälle](../building-journeys/journeys-uc.md) und [Technische Anwendungsfälle](../building-journeys/collections.md).
* Der Abschnitt zu **Entitätsdatensätzen** wurde mit weiteren Details aktualisiert. [Mehr dazu](../data/datasets-query-examples.md#entity-dataset)
* Die Abschnitte zur Opt-out-Verwaltung und zu den Zustimmungsrichtlinien wurden neu strukturiert. [Mehr dazu](../privacy/opt-out.md)
* Der Abschnitt zu erweiterten Parametern in Journey-Nachrichten wurde klarer formuliert und betont nun, dass das Überschreiben von E-Mail-Adressen nur für bestimmte Anwendungsfälle verwendet werden sollte. Meistens ist der Wert, der als primäre Adresse in den **Ausführungsfeldern** definiert ist, derjenige, der verwendet werden sollte.
* Es wurde ein Hinweis zum Abschnitt **Konfigurieren von Landingpage-Subdomains** hinzugefügt, um anzugeben, dass Großbuchstaben in Subdomains von Landingpages nicht zulässig sind. [Mehr dazu](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* Alle neuen Funktionen und Verbesserungen, die mit der [!DNL Journey Optimizer]-Version September 2022 kommen, werden in der Dokumentation detailliert beschrieben. [Mehr dazu](release-notes.md)
* Es wurde eine Best Practice zur Verwendung von Warteaktivitäten in wiederkehrenden „Zielgruppe lesen“-Journeys hinzugefügt. [Mehr dazu](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Neue Beispiele für den Schritt „Ereignisabfrage“ sowie Informationen über den Unterschied zwischen ID, instanceID und profileID hinzugefügt. [Weitere Informationen](../reports/query-examples.md).
* Die Seiten zu den Funktionen [toDateOnly](../building-journeys/functions/functiontodateonly.md) und [toString](../building-journeys/functions/functiontostring.md) wurden aktualisiert.
* Details zu den Zeitbedingungsparametern hinzugefügt. [Mehr dazu](../building-journeys/condition-activity.md#time_condition)
* Informationen über integrierte Datensätze wurden hinzugefügt. [Mehr dazu](../data/get-started-datasets.md#access-datasets)
* Die Abschnitte „Globaler Bericht“ und „Live-Bericht“ wurden verbessert und neu angeordnet. [Mehr dazu](../reports/global-report.md)
* Eine Liste aller in Adobe Journey Optimizer verfügbaren Berichtsmetriken wurde hinzugefügt -
  [Mehr dazu](../reports/global-report.md#email-and-sms-metrics)
* Der Abschnitt zur BCC-E-Mail wurde auf die neue Seite „Support für Archivierung“ verschoben. [Mehr dazu](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version August 2022 wurden in der Dokumentation beschrieben. [Mehr dazu](release-notes.md)
* Der Abschnitt zu den Häufigkeitsregeln wurde aktualisiert, um den neuen Ablauf für Inline-Messaging widerzuspiegeln. [Mehr dazu](../configuration/frequency-rules.md#apply-frequency-rule)
* Im Abschnitt zu den ersten Schritten mit Landingpages wird jetzt auf ein Video verwiesen, in dem die Konfiguration von Abonnements und die Erstellung von Landingpages erläutert wird. [Mehr dazu](../landing-pages/get-started-lp.md#video)
* Für Journeys, bei denen Aktivitäten vom Typ „Zielgruppe lesen“ verwendet werden, wurde eine Einschränkung hinzugefügt. [Weitere Informationen](../building-journeys/read-audience.md)
* Die Seite mit den Operatoren des Ausdruckseditors wurde verbessert. [Mehr dazu](../building-journeys/expression/operators.md)
* Es wurde ein Abschnitt über die Planung einer Kampagne hinzugefügt. [Mehr dazu](../campaigns/create-campaign.md)
* Der Abschnitt mit allgemeinen Syntaxregeln für den Ausdruckseditor wurde aktualisiert, um die neue Regel bezüglich Escaping des umgekehrten Schrägstrichs in literalen Funktionen zu berücksichtigen. Die vorhandenen veröffentlichten Nachrichten sind von dieser Änderung nicht betroffen. Nur neue Nachrichten oder Nachrichtenentwürfe müssen aktualisiert werden. [Mehr dazu](../personalization/personalization-syntax.md#general-rules)

## Juli 2022 {#july-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Juli &#39;22 wurden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Der Abschnitt **Kanaloberflächen einrichten** wurde präzisiert und mit Links zu der Seite aktualisiert, die beschreibt, wie der SMS-Kanal konfiguriert wird. [Weitere Informationen](../configuration/channel-surfaces.md#create-channel-surface)
* In den Journey-Eigenschaften ist die Option **Profil-Zeitzone** jetzt standardmäßig deaktiviert. [Weitere Informationen](../building-journeys/timezone-management.md#timezone-from-profiles)
* In der Aktivität **Warten** ist die Option **Festes Datum** nicht mehr verfügbar. [Weitere Informationen](../building-journeys/wait-activity.md)
* Es wurden weitere Informationen über die Option **Inkrementelles Lesen** in der Aktivität **Zielgruppe lesen** hinzugefügt. [Weitere Informationen](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Es wurden Empfehlungen für die Bedingungsart **Profilobergrenze** hinzugefügt. [Weitere Informationen](../building-journeys/condition-activity.md#profile_cap)
* Es wurde eine Einschränkung für Geschäftsereignisse hinzugefügt. [Weitere Informationen](../start/guardrails.md#events-g)

## Juni 2022 {#june-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Juni 2022 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Es wurde ein neuer Abschnitt über Datenschutzanfragen zur Dokumentation hinzugefügt. [Weitere Informationen](../privacy/requests.md)
* Es wurde ein neuer Abschnitt über Auditprotokolle zu Ressourcen zur Dokumentation hinzugefügt. [Weitere Informationen](../privacy/audit-logs.md)
* Es wurde ein neuer Abschnitt zur Dokumentation hinzugefügt, in dem beschrieben wird, wie HTML- oder JSON-Inhalte aus der Adobe Experience Cloud Asset-Bibliothek zu einer Angebotsdarstellung hinzugefügt werden. [Weitere Informationen](../offers/offer-library/add-representations.md#html-json)
* Es wurde eine neue Seite zum Journey-Lebenszyklus hinzugefügt. [Weitere Informationen](../building-journeys/journey.md#journey-versions)
* Die Seite mit der Warteaktivität wurde aktualisiert. [Weitere Informationen](../building-journeys/wait-activity.md)
* Die Liste der Adobe Journey Optimizer-Datensätze mit Abfragebeispielen wurde hinzugefügt. [Weitere Informationen](../data/datasets-query-examples.md)
* Die Seite mit der Zulassungsliste wurde in den Abschnitt „Konfiguration“ verschoben. [Weitere Informationen](../configuration/allow-list.md)
* Die Seite mit der Unterdrückungsliste wurde aktualisiert, um einige Informationen zu verdeutlichen, darunter die Tatsache, dass alle ASCII-Zeichen zwischen 32 und 126 im Feld für den Unterdrückungsgrund zulässig sind. [Weitere Informationen](../configuration/manage-suppression-list.md)
* Der Link zu Leitplanken und statischen Limits für das Entscheidungs-Management wurde hinzugefügt. [Weitere Informationen](../start/guardrails.md)
* Die Sendezeitoptimierung ist jetzt für alle Kundinnen und Kunden verfügbar. Die Erwähnung der Betaversion wurde entfernt. [Weitere Informationen](../building-journeys/journeys-message.md#send-time-optimization)
* Die Batch Decisioning-API wurde zur Liste der verfügbaren APIs für die Bereitstellung personalisierter Angebote hinzugefügt. [Weitere Informationen](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mai 2022 {#may-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom Mai 2022 wurden in der Dokumentation ausführlich beschrieben. [Weitere Informationen](release-notes.md)
* Es wurden neue Abfragebeispiele für die [Zielgruppenqualifizierung](../reports/query-examples.md#segment-qualification-queries) und [Ereignisse](../reports/query-examples.md#event-based-queries) hinzugefügt.
* Im Abschnitt zum Entwerfen von E-Mails werden jetzt neue integrierte Vorlagen erwähnt, mit denen Inhalte erstellt werden können. Die entsprechenden Screenshots wurden aktualisiert. [Weitere Informationen](../email/get-started-email-design.md)
* Auf der Startseite der Journey Optimizer-Dokumentation wurden die Links zu wichtigen Ressourcen aktualisiert.
* Screenshots für Landingpages und Abonnementberichte wurden aktualisiert. [Weitere Informationen](../reports/live-report.md)
* Es wurde ein Hinweis hinzugefügt, dass die Methode „Delete“ in benutzerdefinierten Aktionen nicht unterstützt wird. [Weitere Informationen](../action/about-custom-action-configuration.md)
* Die Links zu Anleitungsvideos wurden aktualisiert.
* Die Abschnitte [E-Mail-Konfiguration](../configuration/about-subdomain-delegation.md), [Nachrichtenvoreinstellungen](../configuration/channel-surfaces.md) und [Konfigurieren von Landingpages](../landing-pages/lp-subdomains.md) wurden neu strukturiert, um die Lesbarkeit zu verbessern.
* Der Abschnitt „URL-Tracking“ wurde aktualisiert und mit Beispielen ergänzt. [Weitere Informationen](../email/email-settings.md#url-tracking)
* Ein neuer Unterabschnitt zur Einrichtung einer Weiterleitungs-E-Mail-Adresse wurde hinzugefügt. Beachten Sie, dass Sie dies nicht über die Benutzeroberfläche tun können. [Weitere Informationen](../email/email-settings.md#forward-email)

## April 2022 {#april-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version April 2022 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* In der Dokumentation wurde die Seite zum Ereignis **Reaktionen** aktualisiert. [Weitere Informationen](../building-journeys/reaction-events.md)
* Die Videos zu den Funktionen des Entscheidungs-Managements wurden entsprechend der Benutzeroberfläche von Journey Optimizer aktualisiert. [Weitere Informationen](../offers/get-started/starting-offer-decisioning.md)
* Der Abschnitt **Erste Schritte mit Datensätzen** wurde verbessert, es wird nun detailliert beschrieben, wie auf Datensätze zugegriffen werden kann und wie diese erstellt werden. [Weitere Informationen](../data/get-started-datasets.md)
* Links zu Hilfehandbüchern und Versionshinweisen zu Produkten wurden zur Homepage der **Dokumentation zu Adobe Journey Optimizer** hinzugefügt. [Weitere Informationen](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=de)
* Der Abschnitt **Nachrichtenvoreinstellungen erstellen** weist nun darauf hin, dass Sie mit der Voreinstellungserstellung nicht fortfahren können, wenn sich der ausgewählte IP-Pool in Bearbeitung befindet (Status **[!UICONTROL Verarbeitung läuft]**) und noch nie mit der ausgewählten Subdomain verknüpft wurde. [Weitere Informationen](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* Der Abschnitt zum **URL-Tracking** bei Nachrichtenvoreinstellungen wurde aktualisiert, um geringfügige Änderungen an der Benutzeroberfläche widerzuspiegeln. [Weitere Informationen](../configuration/channel-surfaces.md#url-tracking)

## März 2022 {#march-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom 22. März wurden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Im Abschnitt **Offer Decisioning** wurde eine neue Seite über die ersten Schritte mit KI-Modellen hinzugefügt, die eine ausführliche Beschreibung des [automatischen Optimierungsmodells](../offers/ranking/auto-optimization-model.md), des verwendeten Algorithmus und weitere technische Details enthält. [Weitere Informationen](../offers/ranking/ai-models.md)
* Die Seite zur Erstellung von Testprofilen wurde in den Abschnitt **Zielgruppen, Profile und Identität** verschoben. [Weitere Informationen](../audience/creating-test-profiles.md)
* Es wurde ein Beispiel hinzugefügt, das erläutert, wie im Ausdruckseditor ein Ausdruck als Standardwert hinzugefügt wird. [Weitere Informationen](../building-journeys/expression/field-references.md#default-value)
* Der Abschnitt **Personalisierte Angebote erstellen** wurde neu geordnet, um die Lesbarkeit zu verbessern. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md)
* Ein neuer Abschnitt wurde hinzugefügt, in dem die Auswirkungen beschrieben werden, die eine Änderung des Start- und/oder Enddatums eines Angebots auf die Frequenzlimitierung dieses Angebots haben kann. [Weitere Informationen](../offers/offer-library/add-constraints.md#capping-change-date)
* Der Abschnitt **Ändern von primären E-Mail-Adressen** wurde aktualisiert und erläutert jetzt die Änderungen an der Benutzeroberfläche. [Weitere Informationen](../configuration/primary-email-addresses.md)

## Februar 2022 {#feb-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version Februar 2022 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Die Dokumentationsseiten der Funktionen [replace](../building-journeys/functions/functionreplace.md#example_2) und [replaceAll](../building-journeys/functions/functionreplaceall.md#example) wurden mit zusätzlichen Informationen und Beispielen zum Zielparameter aktualisiert.
* Auf der Seite [Operatoren](../building-journeys/expression/operators.md#important-notes) wurden Best Practices hinzugefügt.

## Januar 2022 {#january-2022}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom Januar 2022 sind in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Der Abschnitt **KI-Ranglisten für Offer Decisioning** wurde mit einer detaillierteren Beschreibung des Modells für die automatische Optimierung aktualisiert. [Weitere Informationen](../offers/ranking/auto-optimization-model.md)
* Es wurde ein neuer Abschnitt zu den Schemaanforderungen hinzugefügt, die erforderlich sind, wenn Ereignistypen unter Verwendung eines KI-Modells gesendet werden. [Weitere Informationen](../offers/data-collection/schema-requirement.md)
* Der Abschnitt zu [!DNL Journey Optimizer] Personalisierungsfunktionen wurde neu angeordnet, um die Übersichtlichkeit zu verbessern. [Weitere Informationen](../personalization/personalize.md)
* Der Abschnitt **Erstellen von Nachrichtenvoreinstellungen** wurde zur besseren Übersichtlichkeit in mehrere Abschnitte unterteilt. [Weitere Informationen](../configuration/channel-surfaces.md#create-channel-surface)
* Der Abschnitt **Opt-out-Verwaltung** wurde klarer formuliert und leicht umstrukturiert. [Weitere Informationen](../privacy/opt-out.md#opt-out-management)
* Der Abschnitt **Einfügen von Links** wurde aktualisiert, um die jüngsten Änderungen an der Benutzeroberfläche zu berücksichtigen. [Weitere Informationen](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* Eine vollständige Beschreibung des **erweiterten Ausdruckseditors**, der in Journeys verwendet wird, ist jetzt verfügbar. [Weitere Informationen](../building-journeys/expression/expressionadvanced.md)
* Es wurde ein neuer Abschnitt zur **Methode der CNAME-Subdomain-Zuweisung** hinzugefügt. [Weitere Informationen](../configuration/delegate-subdomain.md#cname-subdomain-delegation)

## Oktober 2021 {#october-2021}

* Alle neuen Funktionen und Verbesserungen der Version vom Oktober 2021 von [!DNL Journey Optimizer] wurden in der Dokumentation beschrieben. [Weitere Informationen](release-notes.md)
* Die Liste **Datums-/Uhrzeitfunktion** wurde hinzugefügt. [Weitere Informationen](../personalization/functions/dates.md)
* Neue **Abschnitte über „Erste Schritte“ für jede Benutzerrolle**. Nehmen Sie Ihren eigenen Weg, um schneller an Ihr Ziel zu kommen! [Weitere Informationen](../start/quick-start.md)
* Neuer Abschnitt **Bearbeiten einer Nachrichtenvoreinstellung**. [Weitere Informationen](../configuration/channel-surfaces.md#edit-channel-surface)
* Neuer Abschnitt **Bearbeiten eines PTR-Eintrags**. [Weitere Informationen](../configuration/ptr-records.md#edit-ptr-record)
* Neuer Abschnitt **Deaktivieren einer Nachrichtenvoreinstellung**. [Weitere Informationen](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Im **Entwicklerhandbuch zur Entscheidungs-Management-API** wurden neue Einschränkungen zu den Angebotsbegrenzungen hinzugefügt, die von mobilen [!DNL Experience Edge]-Workflows nicht unterstützt werden. [Weitere Informationen](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Neuer Abschnitt **Erstellen von Simulationen**. [Weitere Informationen](../offers/offer-activities/simulation.md)
* Der Abschnitt **Hinzufügen von Entscheidungsumfängen** wurde aktualisiert. [Weitere Informationen](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Der Abschnitt **Definieren von Inhalten für Ihre Darstellungen** wurde aktualisiert, einschließlich eines neuen [Unterabschnitts](../offers/offer-library/creating-personalized-offers.md#custom-text) mit Informationen zur Definition und Personalisierung von benutzerdefiniertem Text. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* Die folgenden Funktionsseiten wurden aktualisiert: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* Die folgenden Funktionen wurden hinzugefügt: [filter](../building-journeys/functions/functionfilter.md), [intersect](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* Der Datentyp „dateOnly“ wurde in der Dokumentation zum Ausdruckseditor hinzugefügt. [Mehr dazu](../building-journeys/expression/data-types.md)

* Es wurden Details zur Aufbewahrungsfrist im Cache für benutzerdefinierte Aktionen hinzugefügt. [Mehr dazu](../datasource/external-data-sources.md#custom-authentication-mode)

* Es wurden Informationen zu Standard-Ports für benutzerdefinierten Aktionen hinzugefügt. [Mehr dazu](../action/about-custom-action-configuration.md#url-configuration)

* Es wurden Informationen zu Anwendungsfällen für mehrere Geschäftsereignisse hinzugefügt. [Mehr dazu](../event/about-creating-business.md#multiple-business-events)

* Es wurden häufig verwendete Beispiele zur Abfrage von Journey-Schrittereignissen im Data Lake hinzugefügt. [Mehr dazu](../reports/query-examples.md)

* Es wurde eine neue Seite über **Einschränkungen** hinzugefügt. [Mehr dazu](../start/guardrails.md)

* Die Seite **Schnellstart** mit Schritten für verschiedene Personas wurde verbessert. [Mehr dazu](../start/quick-start.md)

*  Alle im entsprechenden Abschnitt beschriebenen Funktionen des Entscheidungs-Managements gelten nun auch für Benutzende der Adobe Experience Platform, die den Anwendungsdienst „Offer Decisioning“ nutzen. [Mehr dazu](../offers/get-started/starting-offer-decisioning.md)

* Es wurde ein Unterabschnitt hinzugefügt, in dem die Unterschiede zwischen der Verwendung von Zielgruppen und Entscheidungsregeln erläutert werden, wenn eine Einschränkung angewendet wird, mit der die Auswahl von Angeboten für eine bestimmte Platzierung eingeschränkt wird. [Mehr dazu](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Es wurden spezifische Beispiele für Rangfolgeformeln hinzugefügt, die einige Anwendungsfälle aus der Praxis veranschaulichen. [Mehr dazu](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Es wurde ein Unterabschnitt zur Bearbeitung von IP-Pools hinzugefügt. [Mehr dazu](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom 21. August wurden in der Dokumentation beschrieben. [Mehr dazu](release-notes.md)
* Die Berechtigungen für das Entscheidungs-Management wurden aktualisiert. [Mehr dazu](../administration/ootb-product-profiles.md)
* Die Screenshots von E-Mail-Designer wurden mit den neuesten Optionen der Benutzeroberfläche aktualisiert.
* Das Konfigurationsverfahren für benutzerdefinierte Aktionen mit dynamischen URL-Pfaden und dynamischen Headern wurde aktualisiert. [Mehr dazu](../action/about-custom-action-configuration.md#url-configuration)
* Es wurde ein Abschnitt über barrierefreie Funktionen und Tastaturbefehle hinzugefügt. [Mehr dazu](../start/user-interface.md#accessibility)
* Es wurde ein Abschnitt über Methoden zur Zielgruppenauswertung hinzugefügt. [Mehr dazu](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Es wurden Hinweise zu den Abschnitten „Unterdrückungsliste“, „Zulassungsliste“ und „Globaler/Live-Bericht zum E-Mail-Versand“ hinzugefügt, in denen erläutert wird, dass Profile mit dem Status „Unterdrückt“ und „Nicht erlaubt“ aus der Metrik „Gesendet“ des E-Mail-Berichts ausgeschlossen werden. [Mehr dazu](../reports/global-report.md)
* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie E-Mail-Adressen oder Domains abgerufen werden, die vom Versand ausgeschlossen wurden, weil sie sich nicht auf der Zulassungsliste befanden. [Mehr dazu](../configuration/allow-list.md#reporting)
* Der Abschnitt „Zulassungsliste aktivieren“ wurde aktualisiert. [Weitere Informationen](../configuration/allow-list.md#enable-allow-list)
* Der Abschnitt „Überwachen von Nachrichtenvoreinstellungen“ wurde mit möglichen Ursachen für eine fehlgeschlagene Durchführung von Voreinstellungen sowie den Fehlerdetails ergänzt. [Mehr dazu](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Der Abschnitt zum Zeitraum für weitere Zustellversuche wurde aktualisiert und umbenannt, um der Tatsache Rechnung zu tragen, dass Sie jetzt die Einstellung für weitere Zustellversuche bei E-Mails in den Nachrichtenvoreinstellungen anpassen können. [Mehr dazu](../configuration/retries.md#retry-duration)
* Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Sie einen Ein-Klick-Opt-out-Link in E-Mail-Inhalte einfügen können. [Mehr dazu](../privacy/opt-out.md#one-click-opt-out-link)
* Der Abschnitt „Subdomain delegieren“ wurde mit detaillierteren Informationen zum Validierungsprozess von Adobe aktualisiert. [Mehr dazu](../configuration/delegate-subdomain.md#subdomain-validation)
* Es wurde ein Abschnitt hinzugefügt, in dem beschrieben wird, wie E-Mail-Adressen und Domains manuell zur Unterdrückungsliste hinzugefügt werden. [Mehr dazu](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Die Abschnitte [Zugriff auf die Unterdrückungsliste](../configuration/manage-suppression-list.md#access-suppression-list) und [Weitere Zustellversuche](../configuration/retries.md) wurden entsprechend der neuen Benutzeroberfläche aktualisiert.
* Der neue Fluss zum Hinzufügen und Konfigurieren von Darstellungen beim Erstellen eines Angebots wurde dokumentiert. [Mehr dazu](../offers/offer-library/creating-personalized-offers.md#representations)

## Juli 2021 {#july-2021}

* Alle neuen Funktionen und Verbesserungen der [!DNL Journey Optimizer]-Version vom 21. Juli wurden in der Dokumentation beschrieben. [Mehr dazu](release-notes.md)
* Auf der Startseite und im Inhaltsverzeichnis von [!DNL Journey Optimizer] wurden direkte Links zur Experience Platform-Services-Dokumentation hinzugefügt.
* In [!DNL Journey Optimizer] sind neue Landingpages für Experience Platform-Services verfügbar.
* Auf der Startseite wurden Links zur Produktbeschreibung von [!DNL Journey Optimizer] hinzugefügt.
* Auf mehreren Seiten wurden Anleitungsvideos hinzugefügt.
* Optimierte Bilder auf der Startseite
* Der Abschnitt „Nachrichten-Tracking“ wurde in „Hinzufügen von Links und Verfolgen von Nachrichten“ verschoben, verbessert und umbenannt. [Mehr dazu](../email/message-tracking.md)
* Es wurde ein Unterabschnitt über Mirrorseiten hinzugefügt. [Mehr dazu](../email/message-tracking.md#mirror-page)
* In der Dokumentation und deren Abbildungen wurden „Angebotsaktivitäten“ in „Entscheidungen“ und „Entscheidungen“ in „Entscheidungsumfänge“ umbenannt. [Mehr dazu](../offers/get-started/starting-offer-decisioning.md)
* Neuer Anwendungsfall: [Personalisieren einer Nachricht mit Hilfsfunktionen](../personalization/personalization-use-case-helper-functions.md)
* Die Dokumentation zum Lesen von Zielgruppen wurde aktualisiert, um die Auswirkungen materialisierter Segmente zu erläutern. [Mehr dazu](../building-journeys/read-audience.md)
* Die Journey-Einschränkungen wurden aktualisiert. [Mehr dazu](../start/guardrails.md)
* Der Abschnitt „Konfiguration von Angeboten“ heißt jetzt „Entscheidungen“. [Mehr dazu](../offers/offer-activities/configure-offer-selection.md)
* Es wurde ein Warnhinweis hinzugefügt, der darauf hinweist, dass ereignisbasierte Angebote derzeit nicht unterstützt werden. [Mehr dazu](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Die neue Registerkarte **[!UICONTROL Überblick]** im Entscheidungs-Management wurde vorgestellt. [Mehr dazu](../offers/get-started/user-interface.md#overview)
* Es wurden neue Abschnitte hinzugefügt, um die in den Angebots- und Entscheidungslisten verfügbaren Aktionen zu beschreiben: [Angebotsliste](../offers/offer-library/creating-personalized-offers.md#offer-list) und [Entscheidungsliste](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
