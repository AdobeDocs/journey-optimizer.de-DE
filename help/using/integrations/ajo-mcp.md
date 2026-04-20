---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit MCP-Clients (Beta)
description: Erfahren Sie, wie Sie Adobe Journey Optimizer mithilfe des MCP-Servers mit MCP-Clients verbinden
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 31fb00bc82b6bbc664c37beba263ce94851bf8bd
workflow-type: tm+mt
source-wordcount: '1418'
ht-degree: 4%

---

# Arbeiten mit MCP-Clients (Beta) {#ajo-mcp}

Die [!DNL Adobe Journey Optimizer] MCP-Integration ermöglicht die Abfrage von Kampagnen und Angeboten mithilfe von Eingabeaufforderungen in einfacher Sprache - ohne dass API-Aufrufe geschrieben oder durch Produktbildschirme navigiert werden müssen. Auf dieser Seite wird erläutert, wie die Integration funktioniert, was Sie damit tun können und wie Sie beginnen können.

>[!AVAILABILITY]
>
>Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit nur in **Claude Web** und **Claude Desktop** verfügbar. In zukünftigen Versionen wird Unterstützung für weitere MCP-kompatible Anwendungen hinzugefügt.

## Beta, Sicherheit und rechtliche Hinweise {#mcp-notices}

**Hinweis zur Beta-Dokumentation:** Diese Dokumentation behandelt eine Beta-Funktion und stellt keine endgültige Dokumentation dar. Der hier beschriebene Inhalt bezieht sich auf eine Beta-Version und kann sich vor der allgemeinen Verfügbarkeit ändern. Adobe übernimmt keine Gewähr für die Vollständigkeit oder Richtigkeit dieser Dokumentation.

Durch die Verwendung des Adobe Journey Optimizer MCP Servers (Beta) (“Beta„) erkennen Sie hiermit an, dass der Beta **„wie besehen“ und ohne Gewährleistung jeglicher Art bereitgestellt wird**. Adobe ist nicht verpflichtet, die Beta zu pflegen, zu korrigieren, zu aktualisieren, zu ändern oder anderweitig zu unterstützen. Es wird empfohlen, Vorsicht walten zu lassen und sich nicht auf die ordnungsgemäße Funktionsweise oder Leistung solcher Beta und/oder Begleitmaterialien zu verlassen. Die Beta gilt als vertrauliche Information von Adobe. Jedes „Feedback“ (Informationen zur Beta-Version, einschließlich, aber nicht beschränkt auf Probleme oder Mängel, auf die Sie bei der Verwendung der Beta-Version stoßen, Vorschläge, Verbesserungen und Empfehlungen), das Sie Adobe übermitteln, wird hiermit an Adobe übertragen, einschließlich aller Rechte, Titel und Interessen an diesem Feedback.

>[!WARNING]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration. Die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen in einer Sandbox-Umgebung vor der produktiven Verwendung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Kundenerlebnis-Teams verlassen sich zunehmend auf Chat-basierte Programme und Entwickler-Tools wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio, um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Journey Optimizer] bietet jetzt einen MCP-Server, der Kampagnen-, Treueprogramm- und Sandbox-Vorgänge direkt in jeder MCP-kompatiblen Anwendung bereitstellt. Mit der [!DNL Adobe Journey Optimizer] MCP-Integration können verschiedene Rollen um dieselben Orchestrierungsdaten zusammenarbeiten, ohne Abfragen für die [!DNL Adobe Journey Optimizer] REST-API zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren. Kunden können ihre Absichten im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen.

## Wichtigste Funktionen {#mcp-capabilities}

Mit dem [!DNL Adobe Journey Optimizer] MCP-Server können Sie Kampagnen und Angebote direkt über Ihren KI-Assistenten überprüfen, zusammenfassen und Fehler beheben. Alle Vorgänge sind **schreibgeschützt** - Die MCP-Serveroberflächen rufen APIs als Klarsprachenantworten ab, damit Sie Folgendes tun können:

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **Sofortige Sichtbarkeit der Kampagne** - Fragen Sie nach Kampagnenstatus und Kanalkonfigurationen in einfacher Sprache und erhalten Sie sofort Antworten, ohne durch Menüs zu navigieren oder Berichte manuell abzurufen.
* **Probleme frühzeitig erkennen** - In der Oberfläche gestoppte Kampagnen, verwaiste Entwürfe und Probleme mit der Kanalkonfiguration werden sofort angezeigt, sodass Ihr Team schnell reagieren kann.
* **Zusammenarbeit rund um Live-Daten** - Marketing-Experten, Kampagnen-Manager und Stakeholder können über ihren KI-Assistenten alle dieselben Live-[!DNL Adobe Journey Optimizer]-Daten abfragen, was die Abstimmung, Entscheidung und das Zusammengehen erleichtert.
* **Orchestrierungsportfolio überprüfen** — Überprüfen Sie den vollständigen Status von Kampagnen, ohne JSON zu analysieren oder über Produktbildschirme zu springen.

## Verfügbare Tools {#mcp-tools}

Die folgenden Tools werden vom [!DNL Adobe Journey Optimizer] MCP-Server verfügbar gemacht:

| Tool | Beschreibung |
|---|---|
| **Kampagnen auflisten** | Durchsuchen Sie Ihre [!DNL Adobe Journey Optimizer] Marketing-Kampagnen. Unterstützt das Filtern nach Status (ENTWURF, LIVE, ANGEHALTEN, ABGESCHLOSSEN). |
| **Kampagne abrufen** | Rufen Sie vollständige Details und Konfigurationen für eine bestimmte Kampagne nach ID ab, einschließlich Zielgruppen-Targeting, Zeitplan, Kanal und Inhaltseinstellungen. |
| **Kanalkonfigurationen auflisten** | Anzeigen von Oberflächenvorgaben und Branding-Einstellungen für E-Mail-, SMS-, Push- oder WhatsApp-Kanäle. |

>[!NOTE]
>
>Alle Tools sind schreibgeschützt. Schreibvorgänge (Erstellen, Aktualisieren oder Löschen von Objekten) werden in der aktuellen Beta-Version nicht unterstützt.

## Anwendungsfälle {#mcp-use-cases}

Die folgenden Beispiele zeigen, wie Sie mit dem [!DNL Adobe Journey Optimizer] MCP-Server in natürlicher Sprache interagieren:

| Ziel | Beispiel-Eingabeaufforderung |
|---|---|
| **Kampagnenübersicht** | „Alle meine AJO-Kampagnen anzeigen“ / „Wie viele Kampagnen werden in AJO eingerichtet?“ |
| **Statusprüfung** | „Welche Kampagnen sind derzeit aktiv?“ / „Listet alle pausierten oder gestoppten Kampagnen auf.“ |
| **Kampagnendetails** | „Erhalten Sie die vollständigen Details der Kampagne [ID] / „Führen Sie mich durch alles, was in Campaign eingerichtet wurde [ID].“ |
| **Zielgruppe und Zielgruppenbestimmung** | „Welche Zielgruppe wird in der Kampagne angesprochen [ID]?“ / „Welche Eignungsregeln werden für die Kampagne (ID[ festgelegt]&quot; |
| **Zeitplan und Zeitplan** | „Wann soll [ Kampagne ]ID) ausgeführt werden?“ / „Ist Campaign [ID] ein einmaliger Versand oder ein wiederkehrender Versand?“ |
| **Fehlerbehebung** | „Warum könnte Campaign [ID] nicht senden?“ / „Überprüfen Sie die Einrichtung von Campaign [ID] auf Probleme.“ |
| **Kanalkonfiguration** | „Welche Kanalvorgaben sind in meiner Sandbox verfügbar?“ / „Alle E-Mail-Kanal-Konfigurationen anzeigen.“ |
| **Kanalprüfung** | „Welche Kanalkonfigurationen fehlen oder sind unvollständig?“ / „Wie viele Kanalkonfigurationen gibt es in allen Kanälen?“ |

## Voraussetzungen {#mcp-prerequisites}

Bevor Sie den [!DNL Adobe Journey Optimizer] MCP-Server an Ihren MCP-Client anschließen, stellen Sie Folgendes sicher:

* Sie verfügen über eine aktive [!DNL Adobe Journey Optimizer].
* Sie haben Zugriff auf eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web oder Claude Desktop).
* Sie verfügen in [!DNL Adobe Journey Optimizer] über die erforderlichen Berechtigungen, um Kampagnen und Angebote anzuzeigen.

## MCP-Server [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Diese Integration befindet sich in Beta. Detaillierte Einrichtungsschritte werden veröffentlicht, sobald sie die allgemeine Verfügbarkeit erreichen. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um frühzeitig Zugriff auf zu erhalten und Konfigurationsanweisungen zu erhalten.

Während der Beta-Phase wird Ihr Adobe-Support-Mitarbeiter Folgendes bereitstellen:

* Die für Ihre Organisation spezifische MCP Server-Endpunkt-URL.
* Authentifizierungsdaten für die Verbindung Ihres KI-Assistenten mit [!DNL Adobe Journey Optimizer].
* Anleitung zum Konfigurieren des MCP-Servers in Claude Desktop oder Claude Web.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Bekannte Einschränkungen (Beta) {#mcp-limitations}

Die folgenden Einschränkungen gelten für die aktuelle Beta-Version des [!DNL Adobe Journey Optimizer] MCP-Servers:

| Einschränkung | Beschreibung | Problemumgehung |
|---|---|---|
| **Keine Interaktion oder Leistungsmetriken** | Der MCP-Server stellt keine Berichtsdaten bereit. Tools geben keine Impressionen, Clickthrough-Raten, Konversionen oder Versandstatistiken zurück. | Verwenden Sie die AJO-Reporting-Benutzeroberfläche, CJA MCP oder Adobe Analytics MCP für Metriken. AEP Query Service kann Rohdaten zu Ereignissen mit der Kampagnenausführungs-ID abfragen. |
| **Die Paginierung der Kampagnenliste ist begrenzt** | `List Campaigns` gibt immer die erste Ergebnisseite zurück (bis zu 50 Kampagnen, alphabetisch sortiert). Versatz- und Grenzwerte werden nicht angewendet, sodass eine vollständige Auflistung für große Sandboxes nicht sinnvoll ist. | Direkte Verwendung von `Get Campaign`, wenn die Kampagnen-ID oder der Name bekannt ist. Verwenden Sie die AJO-Benutzeroberfläche zum Durchsuchen und Filtern der vollständigen Liste. |
| **Keine Server-seitige Filterung nach Datum, Kanal oder Zeitplan** | `List Campaigns` unterstützt nur das Filtern nach Status. Die Filterung nach Veröffentlichungsdatum, Zeitplandatum, Kanal oder Kampagnentyp ist nicht Server-seitig verfügbar. | Verwenden Sie die Kampagnenliste der AJO-Benutzeroberfläche, die die native Datums- und Kanalfilterung unterstützt. |
| **Abruf des Nachrichteninhalts nicht verfügbar** | Das Tool für Nachrichteninhalte gibt HTTP 502 für alle Kanaltypen (E-Mail, Code-basiert und andere) zurück. Nachrichten-HTML, Betreffzeilen, Personalisierungs-Token und Angebotsinhalte können nicht über MCP abgerufen werden. | Zeigen Sie den Nachrichteninhalt und die Personalisierungs-Token direkt in der AJO-Benutzeroberfläche unter **Kampagnen > [Kampagne] > Inhalt** an. |

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit für **Claude Web** und **Claude Desktop** verfügbar. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Journey Optimizer] Objekte kann ich über MCP zugreifen?

Sie können auf Kampagnen, Angebote, Treueprogramm-Daten und Sandbox-Informationen zugreifen. Vorgänge sind schreibgeschützt (APIs abrufen); Schreibvorgänge werden in der aktuellen Version nicht unterstützt.
+++

+++Benötige ich Entwicklerzugriff, um den [!DNL Adobe Journey Optimizer] MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können damit interagieren, indem sie natürliche Spracheingaben in jedem unterstützten MCP-Client verwenden, während Entwickler es auch in Entwickler-Tools verwenden können, die MCP unterstützen.
+++

+++Werden meine Daten an den MCP Client Provider gesendet?

Wenn Sie eine Eingabeaufforderung senden, kann der MCP-Client relevanten Kontext (einschließlich [!DNL Adobe Journey Optimizer] vom MCP-Server zurückgegebenen Daten) zur Verarbeitung an sein Modell senden. Überprüfen Sie die Datenschutz- und Datenverarbeitungsrichtlinien Ihres MCP-Client-Anbieters, bevor Sie eine Verbindung zu Produktionsdaten herstellen.
+++

+++Welche Berechtigungen benötige ich in [!DNL Adobe Journey Optimizer]?

Sie benötigen mindestens **Anzeigen**-Berechtigungen für die Objekte, die Sie abfragen möchten - Kampagnen oder Angebote. Es sind keine Schreibberechtigungen erforderlich, da der MCP-Server nur Lesevorgänge ausführt. Wenden Sie sich an Ihren [!DNL Adobe Journey Optimizer], wenn Sie sich bezüglich Ihrer aktuellen Zugriffsebene nicht sicher sind.
+++

+++Kann ich den MCP-Server in Sandbox-Umgebungen verwenden?

Ja. Der MCP-Server berücksichtigt Ihre [!DNL Adobe Journey Optimizer] Sandbox-Konfiguration. Sie können Sandbox-spezifische Daten abfragen, indem Sie die Sandbox in Ihrer Eingabeaufforderung angeben oder eine Verbindung mit Anmeldeinformationen herstellen, die für eine bestimmte Sandbox gelten.
+++

