---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit MCP-Clients
description: Erfahren Sie, wie Sie Adobe Journey Optimizer mithilfe des MCP-Servers mit MCP-Clients verbinden
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 7ae497e7a0e4d1652413a5a6dbd5d617a3ec31fe
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Arbeiten mit MCP-Clients {#ajo-mcp}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit nur in **Claude Web** und **Claude Desktop** verfügbar. In zukünftigen Versionen wird Unterstützung für weitere MCP-kompatible Anwendungen hinzugefügt.

Die [!DNL Adobe Journey Optimizer] MCP-Integration ermöglicht die Abfrage von Kampagnen, Journey und Angeboten mithilfe von Eingabeaufforderungen in einfacher Sprache - ohne dass API-Aufrufe verfasst oder durch Produktbildschirme navigiert werden müssen. Auf dieser Seite wird erläutert, wie die Integration funktioniert, was Sie damit tun können und wie Sie beginnen können.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Kundenerlebnis-Teams verlassen sich zunehmend auf Chat-basierte Programme und Entwickler-Tools wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio, um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Journey Optimizer] bietet jetzt einen MCP-Server, der Kampagnen-, Journey-, Treueprogramm- und Sandbox-Vorgänge direkt in einer MCP-kompatiblen Anwendung aufbereitet. Mit der [!DNL Adobe Journey Optimizer] MCP-Integration können verschiedene Rollen um dieselben Orchestrierungsdaten zusammenarbeiten, ohne Abfragen für die [!DNL Adobe Journey Optimizer] REST-API zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren. Kunden können ihre Absichten im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen.

## Wichtigste Funktionen {#mcp-capabilities}

Mit dem [!DNL Adobe Journey Optimizer] MCP-Server können Sie Journey, Kampagnen und Angebote direkt von Ihrem KI-Assistenten aus überprüfen, zusammenfassen und Fehler beheben. Alle Vorgänge sind **schreibgeschützt** - Die MCP-Serveroberflächen rufen APIs als Klarsprachenantworten ab, damit Sie Folgendes tun können:

* **Grundlegendes zur Journey-**) - Eine menschenlesbare Zusammenfassung aller Verzweigungen, Bedingungen und Aktionen auf der Journey.
* **Kampagnenbereitschaft überprüfen** - Blocker identifizieren, die die Veröffentlichung einer Kampagne verhindern.
* **Lücken in der Live-** und -Kampagnen erkennen, welche Kanäle abgedeckt werden und wo Lücken bestehen.
* **Orchestrierungsportfolio prüfen** - Überprüfen Sie den vollständigen Status von Kampagnen und Journey, ohne JSON zu analysieren oder über Produktbildschirme zu springen.

## Anwendungsfälle {#mcp-use-cases}

Die folgenden Beispiele zeigen, wie Sie mit dem [!DNL Adobe Journey Optimizer] MCP-Server in natürlicher Sprache interagieren:

| Ziel | Beispiel-Eingabeaufforderung |
|---|---|
| **Kampagnendetails zusammenfassen** | „Rufen Sie Campaign CMP456 ab und fassen Sie Zielgruppe, Zeitplan, Status und Pakete zusammen.“ |
| **Inventar- und Statusprüfung** | „Was haben wir und in welchem Zustand ist es? Anzeigen von Live- vs. Entwurfs- vs. abgeschlossenen/gestoppten/archivierten Zählungen für Kampagnen.“ |
| **Überprüfen der Veröffentlichungsbereitschaft** | „Warum ist Campaign CMP456 nicht zur Veröffentlichung bereit? Zeigen Sie mir die Blocker.“ |
| **Objekte vergleichen** | „Kampagnen abc123 und xyz789 vergleichen - was hat sich in Status und Zeitplan geändert?“ |
| **Prüfen Sie Ihr Portfolio** | „In allen Live-Journey und -Kampagnen: Welche Kanäle werden abgedeckt und wo sind die Lücken?“ |
| **Kanalabdeckung und -mix** | „Zeigt den Channel-Platzbedarf für Journey, Kampagnen und Angebotsplatzierungen an - Nur-E-Mail im Vergleich zu kanalübergreifender Nutzung, Push-/SMS-/In-App-Nutzung und Diskrepanzen zwischen Journey-Kanälen.“ |

## Voraussetzungen {#mcp-prerequisites}

Bevor Sie den [!DNL Adobe Journey Optimizer] MCP-Server an Ihren MCP-Client anschließen, stellen Sie Folgendes sicher:

* Sie verfügen über eine aktive [!DNL Adobe Journey Optimizer].
* Sie haben Zugriff auf eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web oder Claude Desktop).
* Sie verfügen in [!DNL Adobe Journey Optimizer] über die erforderlichen Berechtigungen zum Anzeigen von Kampagnen, Journey und Angeboten.

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

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit für **Claude Web** und **Claude Desktop** verfügbar. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Journey Optimizer] Objekte kann ich über MCP zugreifen?

Sie können auf Kampagnen, Journey, Angebote, Treuedaten und Sandbox-Informationen zugreifen. Vorgänge sind schreibgeschützt (APIs abrufen); Schreibvorgänge werden in der aktuellen Version nicht unterstützt.
+++

+++Benötige ich Entwicklerzugriff, um den [!DNL Adobe Journey Optimizer] MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können damit interagieren, indem sie natürliche Spracheingaben in jedem unterstützten MCP-Client verwenden, während Entwickler es auch in Entwickler-Tools verwenden können, die MCP unterstützen.
+++

+++Werden meine Daten an den MCP Client Provider gesendet?

Wenn Sie eine Eingabeaufforderung senden, kann der MCP-Client relevanten Kontext (einschließlich [!DNL Adobe Journey Optimizer] vom MCP-Server zurückgegebenen Daten) zur Verarbeitung an sein Modell senden. Überprüfen Sie die Datenschutz- und Datenverarbeitungsrichtlinien Ihres MCP-Client-Anbieters, bevor Sie eine Verbindung zu Produktionsdaten herstellen.
+++

+++Welche Berechtigungen benötige ich in [!DNL Adobe Journey Optimizer]?

Sie benötigen mindestens **Anzeigen**-Berechtigungen für die Objekte, die Sie abfragen möchten - Kampagnen, Journey oder Angebote. Es sind keine Schreibberechtigungen erforderlich, da der MCP-Server nur Lesevorgänge ausführt. Wenden Sie sich an Ihren [!DNL Adobe Journey Optimizer], wenn Sie sich bezüglich Ihrer aktuellen Zugriffsebene nicht sicher sind.
+++

+++Kann ich den MCP-Server in Sandbox-Umgebungen verwenden?

Ja. Der MCP-Server berücksichtigt Ihre [!DNL Adobe Journey Optimizer] Sandbox-Konfiguration. Sie können Sandbox-spezifische Daten abfragen, indem Sie die Sandbox in Ihrer Eingabeaufforderung angeben oder eine Verbindung mit Anmeldeinformationen herstellen, die für eine bestimmte Sandbox gelten.
+++
