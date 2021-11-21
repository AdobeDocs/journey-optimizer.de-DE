---
title: Journey Optimizer - Erste Schritte für Dateningenieure
description: Als Data Engineer erfahren Sie mehr über die Arbeit mit Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 43%

---

# Erste Schritte für Dateningenieure {#data-engineer}

![Data Engineer](assets/do-not-localize/user-1.png)

Als **Adobe Journey Optimizer Data Engineer**, bereiten und verwalten Sie Kundenprofildaten, um die von [!DNL Journey Optimizer], modellieren Kunden- und Geschäftsdaten in Schemas und konfigurieren Quell-Connectoren für die Aufnahme von Daten. Sie können damit beginnen, [!DNL Adobe Journey Optimizer] einmal die [Systemadministrator](administrator.md) gewährt Ihnen Zugriff und vorbereitete Ihre Umgebung.


Erfahren Sie, wie Sie **Daten identifizieren und Schema und Datensatz erstellen** , um Ihre Daten in Adobe Experience Platform auf dieser Seite zu erhalten.

>[!NOTE]
>
>Weitere Informationen **Datenerfassung** in [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target=&quot;_blank&quot;}.

Die Schritte zum Erstellen eines Identitäts-Namespace und eines Datensatzes, die für Profile und Testprofile aktiviert sind, werden in den folgenden Abschnitten beschrieben:

1. **Erstellen eines Identitäts-Namespace**. In Adobe [!DNL Journey Optimizer], **Identitäten** Verbraucher geräteübergreifend und kanalübergreifend verknüpfen, ergibt sich ein Identitätsdiagramm. Das verknüpfte Identitätsdiagramm wird verwendet, um auf Erlebnissen basierende Interaktionen an allen Ihren Touchpoints zu personalisieren.  Weitere Informationen zu Identitäten und Identitäts-Namespaces [auf dieser Seite](../get-started-identity.md).

1. **Schema erstellen** und aktivieren Sie es für Profile. Ein Schema ist ein Regelsatz, der die Datenstruktur und das Datenformat darstellt und überprüft. Auf hoher Ebene bieten Schemas eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legen dar, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtsdatum usw.).  Weitere Informationen zu Schemata [auf dieser Seite](../get-started-schemas.md).

1. **Erstellen von Datensätzen** und aktivieren Sie es für Profile. Ein Datensatz ist ein Konstrukt zur Datenspeicherung und -verwaltung, in dem Daten (in der Regel) in einer Tabelle erfasst werden, die ein Schema (Spalten) und Felder (Zeilen) beinhaltet. Datensätze enthalten auch Metadaten, die verschiedene Aspekte der in ihnen gespeicherten Daten beschreiben. Nachdem ein Datensatz erstellt wurde, können Sie ihn einem vorhandenen Schema zuordnen und ihm Daten hinzufügen. Weitere Informationen zu Datensätzen [auf dieser Seite](../get-started-datasets.md).

1. **Quellen-Connectoren konfigurieren**. Adobe Journey Optimzer ermöglicht die Erfassung von Daten aus externen Quellen und bietet Ihnen gleichzeitig die Möglichkeit, eingehende Daten mithilfe von Platform-Diensten zu strukturieren, zu beschriften und zu erweitern. Daten können aus verschiedensten Quellen aufgenommen werden, darunter etwa Adobe-Anwendungen, Cloud-basierte Datenspeicher und Datenbanken. Weitere Informationen zu Quell-Connectoren [auf dieser Seite](../get-started-sources.md).

1. **Erstellen von Testprofilen**. Testprofile sind bei Verwendung der [Testmodus](../building-journeys/testing-the-journey.md) in einer Journey und [Vorschau und Testen von Nachrichten](../preview.md) vor dem Versand. Schritte zum Erstellen von Testprofilen [auf dieser Seite](../../using/building-journeys/creating-test-profiles.md).


Um Nachrichten in Journeys senden zu können, müssen Sie außerdem **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** konfigurieren. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* Mit der Konfiguration von **Datenquellen** können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen. Weitere Informationen zu Data Sources [in diesem Abschnitt](../datasource/about-data-sources.md).

* Mithilfe von **Ereignissen** können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Weitere Informationen zu Ereignissen [in diesem Abschnitt](../event/about-events.md).

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen: Sie können Ihre Inhalte entwerfen und Ihre Nachricht veröffentlichen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, z. B. Adobe Campaign, erstellen Sie eine **benutzerdefinierte Aktion**. Weitere Informationen zu Aktionen finden Sie in diesem . [in diesem Abschnitt](../action/action.md).
