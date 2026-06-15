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
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 5%

---

# Arbeiten mit MCP-Clients {#ajo-mcp}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Verschaffen Sie sich einen schrittweisen Überblick über den [!DNL Adobe Journey Optimizer] MCP-Server - von den Grundlagen des Model Context Protocol und den unterstützten Clients bis hin zu den verfügbaren Tools, Beispielaufforderungen, Setup-Voraussetzungen, Verbindungsschritten und Antworten auf häufig gestellte Fragen.

>[!ENDSHADEBOX]

Die [!DNL Adobe Journey Optimizer] MCP-Integration ermöglicht die Abfrage von Kampagnen, Journey und Angeboten mithilfe von Eingabeaufforderungen in einfacher Sprache - ohne dass API-Aufrufe verfasst oder durch Produktbildschirme navigiert werden müssen. Auf dieser Seite wird erläutert, wie die Integration funktioniert, was Sie damit tun können und wie Sie beginnen können.

>[!AVAILABILITY]
>
>Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit in **Claude Web**, **Claude Desktop** und **Cursor** verfügbar. In zukünftigen Versionen wird Unterstützung für weitere MCP-kompatible Anwendungen hinzugefügt.

## Beta, Sicherheit und rechtliche Hinweise {#mcp-notices}

**Hinweis zur Beta-Dokumentation:** Diese Dokumentation behandelt eine Beta-Funktion und stellt keine endgültige Dokumentation dar. Der hier beschriebene Inhalt bezieht sich auf eine Beta-Version und kann sich vor der allgemeinen Verfügbarkeit ändern. Adobe übernimmt keine Gewähr für die Vollständigkeit oder Richtigkeit dieser Dokumentation.

Durch die Verwendung des Adobe Journey Optimizer MCP Servers (Beta) (“Beta„) erkennen Sie hiermit an, dass der Beta **„wie besehen“ und ohne Gewährleistung jeglicher Art bereitgestellt wird**. Adobe ist nicht verpflichtet, die Beta zu pflegen, zu korrigieren, zu aktualisieren, zu ändern oder anderweitig zu unterstützen. Es wird empfohlen, Vorsicht walten zu lassen und sich nicht auf die ordnungsgemäße Funktionsweise oder Leistung solcher Beta und/oder Begleitmaterialien zu verlassen. Die Beta-Version wird als vertrauliche Information von Adobe betrachtet. Jedes „Feedback“ (Informationen zur Beta-Version, einschließlich, aber nicht beschränkt auf Probleme oder Mängel, auf die Sie bei der Verwendung der Beta-Version stoßen, Vorschläge, Verbesserungen und Empfehlungen), das Sie Adobe übermitteln, wird hiermit an Adobe übertragen, einschließlich aller Rechte, Titel und Interessen an diesem Feedback.

>[!WARNING]
>
>Das Model Context Protocol (MCP) ist ein aufstrebender Open-Source-Standard, der Sicherheits- oder Zuverlässigkeitsrisiken mit sich bringen kann. Adobe MCP-Server-Integrationen und die zugehörige Dokumentation werden ohne Mängelgewähr und ohne Gewährleistung jeglicher Art bereitgestellt.
>
>Die Verbindung von MCP-Clients oder -Servern mit Adobe-Produkten ist eine vom Kunden gewählte Konfiguration. Die Kunden sind dafür verantwortlich, die Sicherheit und Eignung jeder MCP-Integration zu bewerten. Adobe übernimmt keine Verantwortung für Probleme, die sich aus einer Fehlkonfiguration, einer fehlerhaften Verwendung des MCP, Sicherheitslücken in Drittanbieterimplementierungen oder unbeabsichtigten Aktionen ergeben, die über MCP-fähige Workflows ausgeführt werden.
>
>Um Risiken zu reduzieren, empfiehlt Adobe, Integrationen in einer Sandbox-Umgebung vor der produktiven Verwendung zu testen und alle MCP-initiierten Aktionen und Antworten sorgfältig zu überprüfen und zu validieren, bevor sie bestätigt oder sich auf sie verlassen.

## Was ist das Modell-Kontextprotokoll? {#mcp-overview}

Marketing- und Kundenerlebnis-Teams verlassen sich zunehmend auf Chat-basierte Programme und Entwickler-Tools wie Anthropic Claude, OpenAI ChatGPT, Cursor und Microsoft Copilot Studio, um ihre tägliche Arbeit zu optimieren. Diese Anwendungen unterstützen das **Model Context Protocol (MCP)**, einen offenen Standard, der es Anwendungen ermöglicht, Backend-Tools auf einheitliche Weise für große Sprachmodelle (LLMs) verfügbar zu machen.

[!DNL Adobe Journey Optimizer] bietet jetzt einen MCP-Server, der Kampagnen- und Sandbox-Vorgänge direkt in jeder MCP-kompatiblen Anwendung aufbereitet. Mit der [!DNL Adobe Journey Optimizer] MCP-Integration können verschiedene Rollen um dieselben Orchestrierungsdaten zusammenarbeiten, ohne Abfragen für die [!DNL Adobe Journey Optimizer] REST-API zu schreiben oder durch mehrere Bildschirme der Benutzeroberfläche zu navigieren. Kunden können ihre Absichten im Gespräch beschreiben und das LLM die entsprechenden MCP-Tools aufrufen lassen.

## Wichtigste Funktionen {#mcp-capabilities}

Mit dem [!DNL Adobe Journey Optimizer] MCP-Server können Sie Kampagnen, Journey und Angebote direkt von Ihrem KI-Assistenten aus überprüfen, zusammenfassen und Fehler beheben. Alle Vorgänge sind **schreibgeschützt** - Die MCP-Serveroberflächen rufen APIs als Klarsprachenantworten ab, damit Sie Folgendes tun können:

* **Grundlegendes zur Journey-**) - Eine menschenlesbare Zusammenfassung aller Verzweigungen, Bedingungen und Aktionen auf der Journey.
* **Sofortige Sichtbarkeit der Kampagne** - Fragen Sie nach Kampagnenstatus und Kanalkonfigurationen in einfacher Sprache und erhalten Sie sofort Antworten, ohne durch Menüs zu navigieren oder Berichte manuell abzurufen.
* **Probleme frühzeitig erkennen** - In der Oberfläche gestoppte Kampagnen, verwaiste Entwürfe und Probleme mit der Kanalkonfiguration werden sofort angezeigt, sodass Ihr Team schnell reagieren kann.
* **Zusammenarbeit rund um Live-Daten** - Marketing-Experten, Kampagnen-Manager und Stakeholder können über ihren KI-Assistenten alle dieselben Live-[!DNL Adobe Journey Optimizer]-Daten abfragen, was die Abstimmung, Entscheidung und das Zusammengehen erleichtert.
* **Orchestrierungsportfolio überprüfen** — Überprüfen Sie den vollständigen Status von Kampagnen, ohne JSON zu analysieren oder über Produktbildschirme zu springen.

## Verfügbare Tools {#mcp-tools}

Die folgenden Tools werden vom [!DNL Adobe Journey Optimizer] MCP-Server verfügbar gemacht:

**Campaign-Tools**

| Tool | Beschreibung |
|---|---|
| **Kampagnen auflisten** | Durchsuchen Sie Ihre [!DNL Adobe Journey Optimizer] Marketing-Kampagnen. Unterstützt das Filtern nach Status (ENTWURF, LIVE, ANGEHALTEN, ABGESCHLOSSEN). |
| **Kampagne abrufen** | Rufen Sie vollständige Details und Konfigurationen für eine bestimmte Kampagne nach ID ab, einschließlich Zielgruppen-Targeting, Zeitplan, Kanal und Inhaltseinstellungen. |
| **Kanalkonfigurationen auflisten** | Anzeigen von Oberflächenvorgaben und Branding-Einstellungen für E-Mail-, SMS-, Push- oder WhatsApp-Kanäle. |

**Journey-Tools**

| Tool | Beschreibung |
|---|---|
| **Alle Journey abrufen** | Durchsuchen Sie alle Journey in Ihrer [!DNL Adobe Journey Optimizer] Sandbox. |
| **Journey abrufen** | Abrufen aller Details für eine bestimmte Journey nach ID, einschließlich Verzweigung, Bedingungen und Aktionen. |
| **Journey visualisieren** | Rendern Sie Ihre Journey mit interaktiven Tools, damit Sie ihre Struktur und ihren Fluss visuell untersuchen können. |

>[!NOTE]
>
>Alle Tools sind schreibgeschützt. Schreibvorgänge (Erstellen, Aktualisieren oder Löschen von Objekten) werden in der aktuellen Beta-Version nicht unterstützt.

## Anwendungsfälle {#mcp-use-cases}

Die folgenden Beispiele zeigen, wie Sie mit dem [!DNL Adobe Journey Optimizer] MCP-Server in natürlicher Sprache interagieren:

| Ziel | Beispiel-Eingabeaufforderung |
|---|---|
| **Übersicht über Campaign und Journey** | Alle meine Journey Optimizer-Kampagnen/Journey anzeigen / Wie viele Kampagnen/Journey werden in Journey Optimizer eingerichtet? |
| **Statusprüfung** | Welche Kampagnen/Journey sind derzeit aktiv? / Listet alle pausierten oder gestoppten Kampagnen/Journey auf. |
| **Kampagnen- und Journey-Details** | Holen Sie sich die vollständigen Details der Kampagne [ID] / Führen Sie mich durch alles, was in Campaign (ID[ eingerichtet ]. / Holen Sie sich die vollständigen Details von Journey [ID] / Führen Sie mich durch alles, was in Journey eingerichtet [ID]. |
| **Zielgruppe und Zielgruppenbestimmung** | Welche Zielgruppe wird in Campaign/Journey [ID] angesprochen? / Welche Eignungsregeln werden für Kampagnen/Journey (ID[ festgelegt]? |
| **Zeitplan und Zeitplan** | Wann soll [ Kampagne ]ID) ausgeführt werden? / Handelt es [ Kampagne ]ID) um einen einmaligen Versand oder einen wiederkehrenden Versand? |
| **Fehlerbehebung** | Warum sendet [ID] die Kampagne möglicherweise nicht? / Überprüfen Sie die Einrichtung von Campaign [ID] auf Probleme. |
| **Kanalkonfiguration** | Welche Kanalvorgaben sind in meiner Sandbox verfügbar? / Alle E-Mail-Kanal-Konfigurationen anzeigen. |
| **Kanalprüfung** | Welche Kanalkonfigurationen fehlen oder sind unvollständig? / Wie viele Kanalkonfigurationen gibt es in allen Kanälen? |

## Voraussetzungen {#mcp-prerequisites}

Bevor Sie den [!DNL Adobe Journey Optimizer] MCP-Server an Ihren MCP-Client anschließen, stellen Sie Folgendes sicher:

* Sie verfügen über eine aktive [!DNL Adobe Journey Optimizer].
* Sie haben Zugriff auf eine unterstützte MCP-kompatible Anwendung (derzeit Claude Web, Claude Desktop oder Cursor).
* Sie verfügen in [!DNL Adobe Journey Optimizer] über die erforderlichen Berechtigungen zum Anzeigen von Kampagnen, Journey und Angeboten.

## MCP-Server [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Diese Integration befindet sich in Beta.

Sie können den [!DNL Adobe Journey Optimizer] MCP-Server über Ihren bevorzugten MCP-Client verbinden, einschließlich **Claude Web**, **Claude Desktop** und **Cursor**.

**Über einen MCP-Client verbinden**

Verwenden Sie beim Einrichten des MCP-Servers in Ihrem MCP-Client die folgende Server-Endpunkt-URL:

`https://ajo-mcp.adobe.io/mcp`

**Verbinden über Claude Web oder Claude Desktop**

Um den MCP-Server in Claude Web oder Claude Desktop einzurichten, gehen Sie zu **Connectoren** und wählen Sie **Adobe Journey Optimizer**.

## Häufig gestellte Fragen {#mcp-faq}

+++Welche MCP-Clients werden unterstützt?

Der [!DNL Adobe Journey Optimizer] MCP-Server ist derzeit für **Claude Web**, **Claude Desktop** und **Cursor** verfügbar. Die Unterstützung für weitere MCP-kompatible Anwendungen kann in zukünftigen Versionen hinzugefügt werden.
+++

+++Auf welche [!DNL Adobe Journey Optimizer] Objekte kann ich über MCP zugreifen?

Sie können auf Kampagnen, Journey, Angebote und Sandbox-Informationen zugreifen. Vorgänge sind schreibgeschützt (APIs abrufen); Schreibvorgänge werden in der aktuellen Version nicht unterstützt.
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

