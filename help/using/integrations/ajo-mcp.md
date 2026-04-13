---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit KI-Assistenten über MCP
description: Erfahren Sie, wie Sie Adobe Journey Optimizer mithilfe des MCP-Servers (Model Context Protocol) mit KI-Assistenten verbinden
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: b92ef33b03e0bdcd6e615846cd7654aaab1b4a1a
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---

# Arbeiten mit KI-Assistenten über MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit nur in **Claude Web** und **Claude Desktop** verfügbar.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Kundenerlebnis-Teams verlassen sich zunehmend auf Chat-basierte Programme und Entwickler-Tools wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio, um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Journey Optimizer] bietet jetzt einen MCP-Server, der Kampagnen-, Journey-, Treueprogramm- und Sandbox-Vorgänge direkt in einer MCP-kompatiblen Anwendung aufbereitet. Mit der [!DNL Adobe Journey Optimizer] MCP-Integration können verschiedene Rollen um dieselben Orchestrierungsdaten zusammenarbeiten, ohne Abfragen für die [!DNL Adobe Journey Optimizer] REST-API zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren. Kunden können ihre Absichten im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen.

## Wichtigste Funktionen {#mcp-capabilities}

Mit dem [!DNL Adobe Journey Optimizer] MCP-Server können Sie [!DNL Adobe Journey Optimizer] Journey, Kampagnen und Angebote direkt von Ihrem KI-Assistenten aus überprüfen, zusammenfassen und Fehler beheben. Die Abruf-APIs von [!DNL Adobe Journey Optimizer] werden in Nur-Sprache-Antworten umgewandelt, sodass Sie:

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

Stellen Sie vor dem Anschließen des [!DNL Adobe Journey Optimizer] MCP-Servers an Ihren KI-Assistenten Folgendes sicher:

* Sie verfügen über eine aktive [!DNL Adobe Journey Optimizer].
* Sie haben Zugriff auf eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web oder Claude Desktop).
* Sie verfügen in [!DNL Adobe Journey Optimizer] über die erforderlichen Berechtigungen zum Anzeigen von Kampagnen, Journey und Angeboten.

## MCP-Server [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Detaillierte Einrichtungsschritte werden hinzugefügt, sobald die Integration allgemein verfügbar ist. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um frühzeitig Zugang zu erhalten.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Häufig gestellte Fragen {#mcp-faq}

+++Welche KI-Assistenten werden unterstützt?

Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit für **Claude Web** und **Claude Desktop** verfügbar. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Journey Optimizer] Objekte kann ich über MCP zugreifen?

Sie können auf Kampagnen, Journey, Angebote, Treuedaten und Sandbox-Informationen zugreifen. Vorgänge sind schreibgeschützt (APIs abrufen); Schreibvorgänge werden in der aktuellen Version nicht unterstützt.
+++

+++Benötige ich Entwicklerzugriff, um den [!DNL Adobe Journey Optimizer] MCP-Server zu verwenden?

Nein. Der MCP-Server ist sowohl für Marketing- als auch für technische Personas konzipiert. Marketing-Experten können damit interagieren, indem sie in Claude natürliche Eingabeaufforderungen verwenden, während Entwickler es auch in Entwickler-Tools verwenden können, die MCP unterstützen.
+++

+++Werden meine Daten an den KI-Assistentenanbieter gesendet?

Wenn Sie eine Eingabeaufforderung senden, kann der KI-Assistent relevanten Kontext (einschließlich [!DNL Adobe Journey Optimizer] vom MCP-Server zurückgegebenen Daten) zur Verarbeitung an sein Modell senden. Lesen Sie die Datenschutz- und Datenverarbeitungsrichtlinien Ihres KI-Assistentenanbieters, bevor Sie eine Verbindung zu Produktionsdaten herstellen.
+++

