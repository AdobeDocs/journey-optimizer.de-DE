---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer – Erste Schritte für Datentechniker
description: Hier erfahren Datentechniker mehr über die Arbeit mit Journey Optimizer.
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 52%

---

# Erste Schritte für Datentechniker {#data-engineer}

Als **Adobe Journey Optimizer-Dateningenieur** bereiten Sie Kundenprofildaten für die von [!DNL Journey Optimizer] orchestrierten Erlebnisse vor und pflegen diese, modellieren Kunden- und Geschäftsdaten in Schemata und konfigurieren Quell-Connectoren für die Datenaufnahme. Sobald der [Systemadministrator](administrator.md) Ihnen Zugriff gewährt und die Umgebung vorbereitet hat, können Sie mit der Arbeit mit [!DNL Adobe Journey Optimizer] beginnen.

>[!NOTE]
>
>Weitere Informationen zur **Datenaufnahme** finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target="_blank"}.

## Wichtige Schritte zur Datenkonfiguration

Führen Sie die folgenden Schritte aus, um die Datengrundlage für Journey Optimizer einzurichten:

1. **Erstellen von Identity-Namespaces**. In Adobe [!DNL Journey Optimizer] verknüpfen **Identitäten** Verbraucher geräteübergreifend und kanalübergreifend. Das Ergebnis ist ein Identitätsdiagramm. Das verknüpfte Identitätsdiagramm wird verwendet, um Erlebnisse auf der Grundlage von Interaktionen an allen Ihren Touchpoints zu personalisieren. Weitere Informationen zu Identitäten und Identity-Namespaces finden Sie [auf dieser Seite](../../audience/get-started-identity.md).

   Konfigurieren Sie außerdem **zusätzliche Kennungen**, damit dasselbe Profil basierend auf sekundären Kennungen wie Bestell-IDs oder Buchungs-IDs mehrere Journey-Instanzen eingeben kann. Erfahren Sie mehr über [zusätzliche Kennungen](../../building-journeys/supplemental-identifier.md).

1. **Schemata erstellen** und für Profile aktivieren. Ein Schema ist ein Regelsatz, der die Datenstruktur und das Datenformat darstellt und überprüft. Auf hoher Ebene bieten Schemata eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legen dar, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtsdatum usw.).

   * Für Standard-Journey und -Kampagnen: Verwenden Sie [XDM-Schemata](../../data/get-started-schemas.md)
   * Für orchestrierte Kampagnen: Erstellen Sie [relationale Schemata](../../orchestrated/gs-schemas.md), um die Segmentierung mehrerer Entitäten zu ermöglichen

1. **Erstellen Sie Datensätze** und aktivieren Sie sie für Profile. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Datensätze enthalten auch Metadaten, die verschiedene Aspekte der in ihnen gespeicherten Daten beschreiben. Nachdem ein Datensatz erstellt wurde, können Sie ihn einem vorhandenen Schema zuordnen und ihm Daten hinzufügen. Weitere Informationen zu Datensätzen finden Sie [auf dieser Seite](../../data/get-started-datasets.md).

   Bereiten Sie für erweiterte Szenarien **Datensätze für Laufzeitsuchen** vor, um die Journey-Ausführung mit Echtzeitdaten aus Datensatzdatensätzen anzureichern. Weitere Informationen [Datensatzsuche](../../building-journeys/dataset-lookup.md).

1. **Konfigurieren von Quell-Connectoren**. Adobe Journey Optimizer ermöglicht die Aufnahme von Daten aus externen Quellen und bietet spezielle Platform-Services, mittels derer Sie eingehende Daten strukturieren, beschriften und erweitern können. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken. Weitere Informationen zu Quell-Connectoren finden Sie [auf dieser Seite](../get-started-sources.md).

1. **Erstellen von Testprofilen**. Testprofile sind bei Verwendung des [Testmodus](../../building-journeys/testing-the-journey.md) in einer Journey und [für eine Vorschau sowie zum Testen von Nachrichten](../../content-management/preview-test.md) vor dem Versand erforderlich. Die Schritte zum Erstellen von Testprofilen werden [auf dieser Seite](../../audience/creating-test-profiles.md) beschrieben.

1. **Berechnete Attribute konfigurieren** (optional) Erstellen abgeleiteter Attribute aus Profildaten, um die Segmentierung und Personalisierung zu vereinfachen. Berechnete Attribute berechnen automatisch komplexe Metriken wie „Gesamtkäufe in den letzten 90 Tagen“ oder „Durchschnittlicher Bestellwert“. Erfahren Sie mehr über [berechnete Attribute](../../audience/computed-attributes.md).

Um Nachrichten in Journey senden zu können, müssen Sie außerdem **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** konfigurieren. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* Mit der Konfiguration von **Datenquellen** können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen. Weitere Informationen zu Datenquellen finden Sie [in diesem Abschnitt](../../datasource/about-data-sources.md).

* Mithilfe von **Ereignissen** können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Weitere Informationen zu Ereignissen finden Sie [in diesem Abschnitt](../../event/about-events.md).

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen: Sie können Ihre Nachrichten innerhalb einer Journey erstellen und Ihren Inhalt gestalten. Wenn Sie zum Senden Ihrer Nachrichten ein externes System wie beispielsweise Adobe Campaign verwenden, erstellen Sie eine **benutzerdefinierte Aktion**. Weitere Informationen zu Aktionen [in diesem Abschnitt](../../action/action.md).

## Journey-Daten überwachen und analysieren

Sobald Journey ausgeführt werden, können Sie Journey-Schrittereignisse im Data Lake abfragen, um die Leistung zu überwachen, Probleme zu beheben und das Kundenverhalten zu analysieren. SQL-Abfragen zur Analyse verwenden:

* Muster für Profileintritte und -austritte
* Fehlerquoten und Verwerfungsursachen
* Leistung beim Audience-Exportvorgang lesen
* Leistungsmetriken für benutzerdefinierte Aktionen
* Journey-Instanzstatus und Engpässe

Erkunden Sie einsatzbereite ([ für die Journey-Analyse](../../reports/query-examples.md), um mit der Datenanalyse und Fehlerbehebung zu beginnen.

## Auf dem Laufenden bleiben

Bleiben Sie auf dem Laufenden mit den neuesten Funktionen und Verbesserungen von Journey Optimizer:

* **[Versionshinweise](../../rn/release-notes.md)** Überprüfen Sie jeden Monat neue Funktionen, Verbesserungen und Fehlerbehebungen
* **[Dokumentationsaktualisierungen](../../rn/documentation-updates.md)**: Verfolgen Sie aktuelle Änderungen an der Dokumentation, einschließlich neuer Seiten und aktualisierter Inhalte
* **Produktbenachrichtigungen**: Aktivieren Sie Benachrichtigungen in Ihrem [Adobe Experience Cloud-Profil](https://experience.adobe.com/preferences){target="_blank"} um Warnhinweise zu erhalten:
   * Neue Produktversionen und Funktionen
   * Wartungsfenster und Systemaktualisierungen
   * Wichtige Ankündigungen und Änderungen

  Um Benachrichtigungen zu aktivieren, klicken Sie auf Ihr Profilsymbol oben rechts in Adobe Experience Cloud, gehen Sie zu **Voreinstellungen > Benachrichtigungen** und konfigurieren Sie Ihre Journey Optimizer-Benachrichtigungseinstellungen.
