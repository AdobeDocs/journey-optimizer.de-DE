---
solution: Journey Optimizer
product: journey optimizer
title: Wichtige Terminologie
description: Grundlegende Begriffe und Konzepte in Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 965bb76529f500d6fa4d89fa1d56979afe9d5bb0
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 11%

---

# Wichtige Terminologie {#key-terminology}

In diesem Referenzhandbuch werden die wichtigsten Begriffe definiert, die bei der Verwendung von Adobe Journey Optimizer auftreten. Wenn Sie diese Konzepte verstehen, können Sie sicher in der Plattform navigieren und effektiv mit Ihrem Team zusammenarbeiten.

>[!TIP]
>
>Ausführliche Erläuterungen zu Funktionen und Workflows finden Sie in den spezifischen Dokumentationsabschnitten, auf die in diesem Handbuch verwiesen wird.

## Wichtigste Plattform-Begriffe {#core-terms}

| Begriff | Definition |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | Eine Anwendung zum Erstellen und Versenden personalisierter Nachrichten an Kunden über verschiedene Kanäle (E-Mail, SMS, Push-Benachrichtigungen, Web). Dies ermöglicht es Ihnen, Kunden-Journey zu entwerfen, die auf Echtzeit-Kundenaktionen reagieren. |
| **Adobe Experience Platform (AEP)** | Die Grundlage von Adobe Journey Optimizer, die alle Kundendaten an einem Ort erfasst und organisiert. Dadurch werden einheitliche Kundenprofile erstellt, die Journey Optimizer für die Personalisierung verwendet. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=de){target="_blank"} |
| **Echtzeit-Kundenprofil** | Eine einheitliche Echtzeitansicht jedes Kunden, die Daten aus verschiedenen Kanälen, einschließlich Online-, Offline-, CRM- und Drittanbieterdaten, kombiniert. Jedes Profil wird dynamisch aktualisiert, wenn Kundinnen und Kunden mit Ihrer Marke interagieren. [Weitere Informationen](../audience/get-started-profiles.md) |
| **Sandbox** | Ein separater Arbeitsbereich zum Testen und Experimentieren ohne Beeinträchtigung der Live-Kundenkommunikation. Adobe Journey Optimizer bietet mehrere Sandboxes für Entwicklungs-, Test- und Produktionsumgebungen. [Weitere Informationen](../administration/sandboxes.md) |

## Begriffe in Bezug auf Journeys und Kampagnen {#journey-campaign-terms}

| Begriff | Definition |
|------|------------|
| **Journey** | Eine Reihe miteinander verbundener Schritte, die Kunden im Laufe der Zeit durch Erlebnisse mit Ihrer Marke führen. Jeder Schritt basiert auf Kundenaktionen oder Zeitinteraktionen und ermöglicht sequenzielle, personalisierte Trigger. [Weitere Informationen](../building-journeys/journey.md) |
| **Kampagne** | Eine einzelne Kommunikation oder ein Satz von Nachrichten, die an eine bestimmte Zielgruppe gesendet werden. Im Gegensatz zu Journey, die sich im Laufe der Zeit entfalten, senden Kampagnen Nachrichten entweder sofort oder zu einem bestimmten Zeitpunkt nach einem Zeitplan oder auf einem Trigger. [Weitere Informationen](../campaigns/get-started-with-campaigns.md) |
| **Ereignis** | Eine Aktion oder ein Ereignis, durch die bzw. das eine Journey Trigger oder vorangebracht wird. Bei Ereignissen kann es sich um Kundenaktionen (einen Kauf tätigen, einen Warenkorb verlassen) oder Systemereignisse (Datum/Uhrzeit, Datenänderung) handeln. [Weitere Informationen](../event/about-events.md) |
| **Kanal** | Die Methode, die zur Kommunikation mit Kunden verwendet wird: E-Mail, SMS, Push-Benachrichtigungen, In-App-Nachrichten, Web oder Briefpost. Jeder Kanal erfordert eine bestimmte Konfiguration. [Weitere Informationen](../configuration/get-started-configuration.md) |

## Begriffe in Bezug auf Kundschaft und Zielgruppen {#customer-audience-terms}

| Begriff | Definition |
|------|------------|
| **Zielgruppe** | Eine Gruppe von Kunden, die gemeinsame Merkmale oder Verhaltensweisen aufweisen, z. B. „Kunden, die in den letzten 30 Tagen gekauft haben“ oder „Mitglieder des Treueprogramms“. Zielgruppen werden verwendet, um bestimmte Kundensegmente anzusprechen. [Weitere Informationen](../audience/about-audiences.md) |
| **Zielgruppenqualifizierung** | Der automatische Prozess, der stattfindet, wenn ein Kunde einer Zielgruppe beitritt oder sie verlässt. Journey Optimizer kann Trigger-Aktionen durchführen, wenn eine Person eine Zielgruppe betritt oder verlässt, um eine zeitnahe und relevante Kommunikation sicherzustellen. [Weitere Informationen](../building-journeys/audience-qualification-events.md) |
| **Kontaktierbare Zielgruppe** | Die Anzahl der Kundenprofile, mit denen Sie sich basierend auf Ihrer Lizenzvereinbarung aktiv über Adobe Journey Optimizer in Verbindung setzen können. Dies bezieht sich in der Regel auf Profile, die innerhalb der letzten 12 Monate eingestellt wurden. |
| **Testprofil** | Fiktive Profile, die zum Testen und zur Vorschau von Nachrichten verwendet werden, bevor sie an echte Kunden gesendet werden. Mit Testprofilen können Sie Personalisierung, Inhalte und Journey-Logik überprüfen. [Weitere Informationen](../audience/creating-test-profiles.md) |

## Inhalte und Personalization-Begriffe {#content-terms}

| Begriff | Definition |
|------|------------|
| **Personalisierung** | Der Prozess der Anpassung von Inhalten an einzelne Kunden mithilfe ihrer Profildaten, Voreinstellungen und Verhaltensweisen. Beispielsweise das Einfügen eines Kundennamens oder das Anzeigen von Produktempfehlungen basierend auf dem Navigationsverlauf. [Weitere Informationen](../personalization/personalize.md) |
| **Inhaltsvorlage** | Ein wiederverwendbares Nachrichten-Design, das in mehreren Kampagnen und Journey verwendet werden kann, um die Markenkonsistenz zu wahren und die Inhaltserstellung zu beschleunigen. [Weitere Informationen](../content-management/content-templates.md) |
| **Fragment** | Ein wiederverwendbarer Inhaltsbaustein (z. B. Kopf- oder Fußzeile oder Werbe-Banner), der für mehrere Nachrichten verwendet werden kann, um Konsistenz zu gewährleisten und zentralisierte Aktualisierungen zu ermöglichen. [Weitere Informationen](../content-management/fragments.md) |
| **Landingpage** | Eine eigenständige Web-Seite, auf der Kundinnen und Kunden sich für die Kommunikation anmelden oder abmelden, Services abonnieren oder Informationen über Online-Formulare bereitstellen können. [Weitere Informationen](../landing-pages/get-started-lp.md) |

## Entscheidungs- und Angebotsbedingungen {#decision-terms}

| Begriff | Definition |
|------|------------|
| **Entscheidungs-Management** | Eine Funktion, die automatisch den besten Inhalt oder das beste Angebot für jeden Kunden basierend auf Echtzeit-Profildaten, Kontext und Geschäftsregeln auswählt. [Weitere Informationen](../offers/get-started/starting-offer-decisioning.md) |
| **Angebot** | Eine Marketing-Nachricht, ein Rabatt oder eine Promotion, die Kunden präsentiert werden kann. Angebote beinhalten Eignungsregeln, die bestimmen, welche Kunden sie erhalten können. [Weitere Informationen](../offers/offer-library/creating-personalized-offers.md) |
| **Entscheidungsrichtlinie** | Eine Reihe von Regeln und Strategien, die basierend auf Einschränkungen wie Berechtigung, Priorität und Begrenzungsregeln bestimmen, welches Angebot welchem Kunden zu welchem Zeitpunkt angezeigt werden soll. [Weitere Informationen](../experience-decisioning/create-decision.md) |

## Daten- und Konfigurationsbedingungen {#data-config-terms}

| Begriff | Definition |
|------|------------|
| **Schema** | Die Struktur, die definiert, wie Daten in Adobe Experience Platform organisiert werden, einschließlich Feldnamen, Datentypen und Beziehungen. Schemata stellen die Konsistenz von Daten über Systeme hinweg sicher. [Weitere Informationen](../data/get-started-schemas.md) |
| **Datensatz** | Eine Sammlung von Daten (normalerweise eine Tabelle), die einem bestimmten Schema folgt. Datensätze speichern Kundendaten, Interaktionsereignisse und andere für die Personalisierung verwendete Informationen. [Weitere Informationen](../data/get-started-datasets.md) |

>[!NOTE]
>
>Ein umfassendes Glossar zu Adobe Experience Platform-Begriffen finden Sie im [Adobe Experience Platform-Glossar](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=de){target="_blank"}.

## Verwandte Themen {#related-topics}

* [Funktionsweise von Journey Optimizer](understanding-ajo.md)
* [Erste Schritte mit der Benutzeroberfläche](user-interface.md)
* [Wählen Sie Ihre Rolle und Ihren Lernpfad](quick-start.md)

