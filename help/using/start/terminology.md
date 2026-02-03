---
solution: Journey Optimizer
product: journey optimizer
title: Wichtige Terminologie
description: Grundlegende Begriffe und Konzepte in Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: ht
source-wordcount: '751'
ht-degree: 100%

---

# Wichtige Terminologie {#key-terminology}

In diesem Referenzhandbuch werden die wichtigsten Begriffe definiert, die bei der Verwendung von Adobe Journey Optimizer vorkommen. Wenn Sie diese Konzepte verstehen, können Sie sicher auf der Plattform navigieren und effektiv mit Ihrem Team zusammenarbeiten.

>[!TIP]
>
>Ausführliche Erläuterungen zu Funktionen und Workflows finden Sie in den spezifischen Dokumentationsabschnitten, auf die in diesem Leitfaden verwiesen wird.

## Wichtigste Plattform-Begriffe {#core-terms}

| Begriff | Definition |
|------|------------|
| **Adobe Journey Optimizer** | Eine Anwendung zum Erstellen und Versenden personalisierter Nachrichten an Kundinnen und Kunden über verschiedene Kanäle (E-Mail, SMS, Push-Benachrichtigungen, Web). Sie können damit Customer Journeys entwerfen, die in Echtzeit auf Kundenaktionen reagieren.  |
| **Adobe Experience Platform** | Das Fundament von Adobe Journey Optimizer, das alle Kundendaten an einem Ort erfasst und organisiert. Damit werden einheitliche Kundenprofile erstellt, die Journey Optimizer für die Personalisierung verwendet. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target="_blank"} |
| **Echtzeit-Kundenprofil** | Eine einheitliche Echtzeitansicht jeder Kundin und jedes Kunden, die Daten aus verschiedenen Kanälen kombiniert, einschließlich Online-, Offline-, CRM- und Drittanbieterdaten. Jedes Profil wird dynamisch aktualisiert, wenn Kundinnen und Kunden mit Ihrer Marke interagieren. [Weitere Informationen](../audience/get-started-profiles.md) |
| **Sandbox** | Ein separater Arbeitsbereich, in dem Sie testen und experimentieren können, ohne die Live-Kundenkommunikation zu beeinträchtigen. Adobe Journey Optimizer bietet mehrere Sandboxes für Entwicklungs-, Test- und Produktionsumgebungen. [Weitere Informationen](../administration/sandboxes.md) |

## Begriffe in Bezug auf Journeys und Kampagnen {#journey-campaign-terms}

| Begriff | Definition |
|------|------------|
| **Journey** | Eine Reihe miteinander verbundener Schritte, um Kundinnen und Kunden im Zeitverlauf durch Erlebnisse mit Ihrer Marke zu führen. Jeder Schritt basiert auf Kundenaktionen oder zeitbasierten Triggern und ermöglicht sequenzielle, personalisierte Interaktionen. [Weitere Informationen](../building-journeys/journey.md) |
| **Kampagne** | Eine einzelne Kommunikation oder ein Satz von Nachrichten, die an eine bestimmte Zielgruppe gesendet werden. Im Gegensatz zu Journeys, die sich im Laufe der Zeit entfalten, senden Kampagnen Nachrichten basierend auf einem Zeitplan oder einem Trigger, entweder unmittelbar oder zu einem festgelegten Zeitpunkt. [Weitere Informationen](../campaigns/get-started-with-campaigns.md) |
| **Ereignis** | Eine Aktion oder ein Auftreten, durch die bzw. das eine Journey ausgelöst oder fortgesetzt wird. Bei Ereignissen kann es sich um Kundenaktionen (einen Kauf tätigen, einen Warenkorb verlassen) oder Systemereignisse (Datum/Uhrzeit, Datenänderung) handeln. [Weitere Informationen](../event/about-events.md) |
| **Kanal** | Die Methode, die zur Kommunikation mit Kundinnen und Kunden verwendet wird: E-Mail, SMS, Push-Benachrichtigungen, In-App-Nachrichten, Web oder Direkt-Mail. Jeder Kanal erfordert eine bestimmte Konfiguration. [Weitere Informationen](../configuration/get-started-configuration.md) |

## Begriffe in Bezug auf Kundschaft und Zielgruppen {#customer-audience-terms}

| Begriff | Definition |
|------|------------|
| **Zielgruppe** | Eine Gruppe von Kundinnen und Kunden, die gemeinsame Merkmale oder Verhaltensweisen aufweisen, z. B. „Personen, die in den letzten 30 Tagen etwas gekauft haben“ oder „Mitglieder des Treueprogramms“. Zielgruppen werden verwendet, um bestimmte Kundensegmente anzusprechen. [Weitere Informationen](../audience/about-audiences.md) |
| **Zielgruppenqualifizierung** | Der Prozess, der abläuft, wenn eine Kundin bzw. ein Kunde in eine Zielgruppe eintritt oder sie verlässt. Journey Optimizer kann Aktionen auslösen, wenn eine Person in eine Zielgruppe eintritt oder sie verlässt, um eine zeitnahe und relevante Kommunikation sicherzustellen. [Weitere Informationen](../building-journeys/audience-qualification-events.md) |
| **Kontaktierbare Zielgruppe** | Die Anzahl der Kundenprofile, mit denen Sie sich basierend auf Ihrer Lizenzvereinbarung aktiv über Adobe Journey Optimizer in Verbindung setzen können. Dies bezieht sich in der Regel auf Profile, mit denen Sie innerhalb der letzten 12 Monate interagiert haben. |
| **Testprofil** | Fiktive Profile, die zum Testen und zur Vorschau von Nachrichten verwendet werden, bevor sie an echte Kundschaft gesendet werden. Mit Testprofilen können Sie Personalisierung, Inhalte und Journey-Logik prüfen. [Weitere Informationen](../audience/creating-test-profiles.md) |

## Begriffe in Bezug auf Inhalte und Personalisierung {#content-terms}

| Begriff | Definition |
|------|------------|
| **Personalisierung** | Der Prozess der Anpassung von Inhalten an einzelne Kundinnen und Kunden anhand ihrer Profildaten, Präferenzen und Verhaltensweisen. Beispielsweise das Einfügen eines Kundennamens oder das Anzeigen von Produktempfehlungen basierend auf dem Navigationsverlauf. [Weitere Informationen](../personalization/personalize.md) |
| **Inhaltsvorlage** | Ein wiederverwendbares Nachrichten-Design, das in mehreren Kampagnen und Journeys verwendet werden kann, um die Markenkonsistenz zu wahren und die Inhaltserstellung zu beschleunigen. [Weitere Informationen](../content-management/content-templates.md) |
| **Fragment** | Ein wiederverwendbarer Inhaltsbaustein (z. B. Kopfzeile, Fußzeile oder Werbe-Banner), der für mehrere Nachrichten verwendet werden kann, um Konsistenz zu gewährleisten und zentralisierte Aktualisierungen zu ermöglichen. [Weitere Informationen](../content-management/fragments.md) |
| **Landingpage** | Eine eigenständige Web-Seite, auf der Kundinnen und Kunden sich für die Kommunikation anmelden oder abmelden, Services abonnieren oder Informationen über Online-Formulare bereitstellen können. [Weitere Informationen](../landing-pages/get-started-lp.md) |

## Begriffe in Bezug auf Entscheidungen und Angebote {#decision-terms}

| Begriff | Definition |
|------|------------|
| **Entscheidungs-Management** | Eine Funktion, die automatisch den besten Inhalt oder das beste Angebot für jede Person basierend auf Echtzeit-Profildaten, Kontext und Geschäftsregeln auswählt. [Weitere Informationen](../offers/get-started/starting-offer-decisioning.md) |
| **Angebot** | Eine Marketing-Nachricht, ein Rabatt oder eine Promotion, die bzw. der Kundinnen und Kunden präsentiert werden kann. Angebote beinhalten Eignungsregeln, die bestimmen, welche Personen sie erhalten können. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md) |
| **Entscheidungsrichtlinie** | Eine Reihe von Regeln und Strategien, die basierend auf Einschränkungen wie Berechtigung, Priorität und Begrenzungsregeln bestimmen, welches Angebot welcher Person zu welchem Zeitpunkt angezeigt werden soll. [Weitere Informationen](../experience-decisioning/create-decision.md) |

## Begriffe in Bezug auf Daten und Konfiguration {#data-config-terms}

| Begriff | Definition |
|------|------------|
| **Schema** | Die Struktur, die definiert, wie Daten in Adobe Experience Platform organisiert werden, einschließlich Feldnamen, Datentypen und Beziehungen. Schemata stellen die Konsistenz von Daten über Systeme hinweg sicher. [Weitere Informationen](../data/get-started-schemas.md) |
| **Datensatz** | Eine Sammlung von Daten (normalerweise eine Tabelle), die einem bestimmten Schema folgt. Datensätze speichern Kundendaten, Interaktionsereignisse und andere für die Personalisierung verwendete Informationen. [Weitere Informationen](../data/get-started-datasets.md) |

>[!NOTE]
>
>Ein umfassendes Glossar zu Adobe Experience Platform-Begriffen finden Sie im [Adobe Experience Platform-Glossar](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=de){target="_blank"}.

## Verwandte Themen {#related-topics}

* [Grundlegendes zur Funktionsweise von Journey Optimizer](understanding-ajo.md)
* [Erste Schritte mit der Benutzeroberfläche](user-interface.md)
* [Auswählen Ihrer Rolle und Ihres Lernpfads](quick-start.md)

