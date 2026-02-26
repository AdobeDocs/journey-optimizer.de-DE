---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Datentechniker
description: Hier erfahren Datentechniker mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: fd10a600cb54b8c35e2d195be7379b0dd120b6a7
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 95%

---

# Erste Schritte für Datentechniker {#data-engineer}

Als **Datenarchitektin bzw. -architekt** oder **Dateningenieurin bzw. -ingenieur** richten Sie die Kundenprofildaten und andere Datenquellen ein, auf denen die von [!DNL Journey Optimizer] orchestrierten Erlebnisse basieren, und pflegen diese. Dazu gehört die Integration aller Kunden- und Geschäftsdaten (egal ob aus Web-, CRM- oder Offline-Quellen) in eine einheitliche 360-Grad-Sicht auf die Kundin bzw. den Kunden. Sie modellieren Kundenprofildaten und Geschäftsdaten in Schemata, konfigurieren Quell-Connectoren für die Datenaufnahme und stellen einen reibungslosen Datenfluss sicher, um Kundenerkenntnisse und Interaktion in Echtzeit zu ermöglichen. Sobald die oder der [Systemadmin](administrator.md) Ihnen Zugriff gewährt und die Umgebung vorbereitet hat, können Sie mit der Arbeit mit [!DNL Adobe Journey Optimizer] beginnen.

>[!NOTE]
>
>Weitere Informationen zur **Datenaufnahme** finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target="_blank"}.

## Wichtige Schritte zur Datenkonfiguration

Führen Sie die folgenden Schritte aus, um die Datengrundlage für Journey Optimizer einzurichten:

1. **Erstellen Sie Identity-Namespaces**. In Adobe [!DNL Journey Optimizer] verknüpfen **Identitäten** Verbrauchende geräte- und kanalübergreifend. Das Ergebnis ist ein Identitätsdiagramm. Das verknüpfte Identitätsdiagramm wird verwendet, um auf Erlebnissen basierende Interaktionen an allen Ihren Kontaktpunkten zu personalisieren. Weitere Informationen zu Identitäten und Identity-Namespaces finden Sie [auf dieser Seite](../../audience/get-started-identity.md).

   Konfigurieren Sie außerdem **zusätzliche Kennungen**, damit dasselbe Profil basierend auf sekundären Kennungen wie Bestell-IDs oder Buchungs-IDs in mehrere Journey-Instanzen eintreten kann. Erfahren Sie mehr über [zusätzliche Kennungen](../../building-journeys/supplemental-identifier.md).

1. **Erstellen Sie Schemata** und aktivieren Sie sie für Profile. Ein Schema ist ein Regelsatz, der die Datenstruktur und das Datenformat darstellt und überprüft. Auf hoher Ebene bieten Schemata eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legen dar, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtsdatum usw.).

   * Für Standard-Journeys und -Kampagnen: Verwenden Sie [XDM-Schemata](../../data/get-started-schemas.md)
   * Für orchestrierte Kampagnen: Erstellen Sie [relationale Schemata](../../orchestrated/gs-schemas.md), um die Segmentierung in mehrere Entitäten zu ermöglichen

1. **Erstellen Sie Datensätze** und aktivieren Sie sie für Profile. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Datensätze enthalten auch Metadaten, die verschiedene Aspekte der in ihnen gespeicherten Daten beschreiben. Nachdem ein Datensatz erstellt wurde, können Sie ihn einem vorhandenen Schema zuordnen und ihm Daten hinzufügen. Weitere Informationen zu Datensätzen finden Sie [auf dieser Seite](../../data/get-started-datasets.md).

   Bereiten Sie für erweiterte Szenarien **Datensätze für Laufzeitsuchen** vor, um die Journey-Ausführung mit Echtzeitdaten aus Eintragsdatensätzen anzureichern. Erfahren Sie mehr über die [Datensatzsuche](../../building-journeys/dataset-lookup.md).

1. **Konfigurieren Sie Quell-Connectoren**. Adobe Journey Optimizer ermöglicht die Aufnahme von Daten aus externen Quellen und bietet spezielle Platform-Services, mittels derer Sie eingehende Daten strukturieren, beschriften und erweitern können. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken. Weitere Informationen zu Quell-Connectoren finden Sie [auf dieser Seite](../get-started-sources.md).

1. **Erstellen von Testprofilen**. Testprofile sind bei Verwendung des [Testmodus](../../building-journeys/testing-the-journey.md) in einer Journey und [für eine Vorschau sowie zum Testen von Nachrichten](../../content-management/preview-test.md) vor dem Versand erforderlich. Die Schritte zum Erstellen von Testprofilen werden [auf dieser Seite](../../audience/creating-test-profiles.md) beschrieben.

1. **Konfigurieren Sie berechnete Attribute** (optional). Erstellen Sie abgeleitete Attribute aus Profildaten, um die Segmentierung und Personalisierung zu vereinfachen. Berechnete Attribute berechnen automatisch komplexe Metriken wie „Käufe in den letzten 90 Tagen insgesamt“ oder „Durchschnittlicher Bestellwert“. Erfahren Sie mehr über [berechnete Attribute](../../audience/computed-attributes.md).

1. **Nachrichtenexport-Datensätze** (optional). Wenn der Nachrichtenexport auf der Kanalkonfigurationsebene aktiviert ist, werden gesendete E-Mail- und SMS-Inhalte automatisch in einen dedizierten Experience Platform-Datensatz exportiert, um die Einhaltung der Vorschriften zu gewährleisten, die Archivierung zu ermöglichen oder nachgelagerte Analysen durchzuführen. Informationen zum [Nachrichtenexport](../../configuration/message-export.md).

Um Nachrichten in Journeys senden zu können, müssen Sie außerdem **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** konfigurieren. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* Mit der Konfiguration von **Datenquellen** können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen. Weitere Informationen zu Datenquellen finden Sie [in diesem Abschnitt](../../datasource/about-data-sources.md).

* Mithilfe von **Ereignissen** können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Weitere Informationen zu Ereignissen finden Sie [in diesem Abschnitt](../../event/about-events.md).

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen: Sie können Ihre Nachrichten innerhalb einer Journey erstellen und Ihren Inhalt gestalten. Wenn Sie zum Senden Ihrer Nachrichten ein externes System wie beispielsweise Adobe Campaign verwenden, erstellen Sie eine **benutzerdefinierte Aktion**. Weitere Informationen zu Aktionen finden Sie [in diesem Abschnitt](../../action/action.md).

## Überwachen und Analysieren von Journey-Daten

Sobald Journeys ausgeführt werden, können Sie Journey-Schrittereignisse im Data Lake abfragen, um die Leistung zu überwachen, Probleme zu beheben und das Kundenverhalten zu analysieren. Verwenden Sie SQL-Abfragen, um Folgendes zu analysieren:

* Profileintritts- und -ausstiegsmuster
* Fehlerraten und Verwerfungsursachen
* Leistung des Exportauftrags von „Zielgruppe lesen“
* Leistungsmetriken für benutzerdefinierte Aktionen
* Journey-Instanzstatus und -Engpässe

Erkunden Sie einsatzbereite [Abfragebeispiele für die Journey-Analyse](../../reports/query-examples.md), um mit der Datenanalyse und Fehlerbehebung loszulegen.

## Rollenübergreifendes Zusammenarbeiten

Ihre Datenkonfigurationsarbeit ist für andere Teams von entscheidender Bedeutung:

>[!BEGINTABS]

>[!TAB Arbeiten mit Admins]

Arbeiten Sie mit [Admins](administrator.md) bei Zugriff und Governance zusammen:

* Anfordern von notwendigen Berechtigungen für das Daten-Management und die Schemaerstellung
* Koordinieren des Sandbox-Zugriffs für Entwicklung und Tests
* Abstimmen von Data-Governance-Richtlinien und Einverständnisverwaltung
* Besprechen von Datenspeicherungsrichtlinien und Datenspeicherungsanforderungen

>[!TAB Arbeiten mit Entwickelnden]

Arbeiten Sie mit [Entwickelnden](developer.md) bei Datenstruktur und Ereignissen zusammen:

* Bereitstellen von XDM-Schemata und Ereignisstrukturen, die von ihnen implementiert werden müssen
* Definieren der zu sendenden Ereignisse und des erforderlichen Payload-Formats
* Abstimmen der Anforderungen an die Datenerfassung und der Datenqualitätsstandards
* Gemeinsames Testen des Ereignisversands und der Datenaufnahme

>[!TAB Arbeiten mit Marketing-Fachleuten]

Arbeiten Sie mit [Marketing-Fachleuten](marketer.md) bei Zielgruppen und Daten zusammen:

* Erstellen von berechneten Attributen für Personalisierung und Segmentierung
* Erstellen von Zielgruppen basierend auf ihren Kampagnen- und Journey-Anforderungen
* Konfigurieren relationaler Schemata für orchestrierte Kampagnen
* Unterstützen der Segmentierung in mehrere Entitäten für erweiterte Anwendungsfälle

>[!ENDTABS]
