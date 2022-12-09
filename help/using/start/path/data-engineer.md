---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer - Erste Schritte für Data Engineer
description: Als Data Engineer erfahren Sie mehr über die Arbeit mit Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Erste Schritte für Dateningenieure {#data-engineer}

Als **Data Engineer für Adobe Journey Optimizer**, bereiten und verwalten Sie Kundenprofildaten, um die von [!DNL Journey Optimizer], modellieren Kunden- und Geschäftsdaten in Schemas und konfigurieren Quell-Connectoren für die Aufnahme von Daten. Sie können damit beginnen, [!DNL Adobe Journey Optimizer] einmal die [Systemadministrator](administrator.md) gewährt Ihnen Zugriff und vorbereitete Ihre Umgebung.


Erfahren Sie, wie Sie **Daten identifizieren und Schema und Datensatz erstellen** , um Ihre Daten in Adobe Experience Platform auf dieser Seite aufzurufen.

>[!NOTE]
>
>Weitere Informationen **Datenerfassung** in [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}.

Die Schritte zum Erstellen eines Identitäts-Namespace und eines Datensatzes, die für Profile und Testprofile aktiviert sind, werden in den folgenden Abschnitten beschrieben:

1. **Erstellen eines Identitäts-Namespace**. In Adobe [!DNL Journey Optimizer], **Identitäten** Verbraucher geräteübergreifend und kanalübergreifend verknüpfen, ergibt sich ein Identitätsdiagramm. Das verknüpfte Identitätsdiagramm wird verwendet, um Erlebnisse basierend auf Interaktionen über all Ihre geschäftlichen Touchpoints hinweg zu personalisieren.  Weitere Informationen zu Identitäten und Identitäts-Namespaces [auf dieser Seite](../../segment/get-started-identity.md).

1. **Schema erstellen** und aktivieren Sie es für Profile. Ein Schema ist ein Regelsatz, der die Datenstruktur und das Datenformat darstellt und validiert. Auf hoher Ebene bieten Schemas eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legen dar, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtstag usw.).  Weitere Informationen zu Schemata [auf dieser Seite](../../data/get-started-schemas.md).

1. **Erstellen von Datensätzen** und aktivieren Sie es für Profile. Ein Datensatz ist ein Speicher- und Verwaltungskonstrukt für eine Sammlung von Daten, normalerweise eine Tabelle, die ein Schema (Spalten) und Felder (Zeilen) enthält. Datensätze enthalten auch Metadaten, die verschiedene Aspekte der in ihnen gespeicherten Daten beschreiben. Nachdem ein Datensatz erstellt wurde, können Sie ihn einem vorhandenen Schema zuordnen und ihm Daten hinzufügen. Weitere Informationen zu Datensätzen [auf dieser Seite](../../data/get-started-datasets.md).

1. **Quellen-Connectoren konfigurieren**. Adobe Journey Optimzer ermöglicht die Erfassung von Daten aus externen Quellen und bietet Ihnen gleichzeitig die Möglichkeit, eingehende Daten mithilfe von Platform-Diensten zu strukturieren, zu beschriften und zu erweitern. Sie können Daten aus verschiedenen Quellen erfassen, z. B. aus Adobe-Anwendungen, Cloud-basierten Speichern, Datenbanken und vielen anderen. Weitere Informationen zu Quell-Connectoren [auf dieser Seite](../get-started-sources.md).

1. **Testprofile erstellen**. Testprofile sind bei Verwendung der [Testmodus](../../building-journeys/testing-the-journey.md) in einer Journey und [Vorschau und Testen von Nachrichten](../../email/preview.md) vor dem Versand. Die Schritte zum Erstellen von Testprofilen werden im Detail beschrieben. [auf dieser Seite](../../segment/creating-test-profiles.md).


Um in Journeys Nachrichten senden zu können, müssen Sie außerdem **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** und **[!UICONTROL Actions]**. Weitere Infos [in diesem Abschnitt](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* Die **Datenquelle** Mit der -Konfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden. Weitere Informationen zu Data Sources [in diesem Abschnitt](../../datasource/about-data-sources.md).

* **Veranstaltungen** ermöglichen es Ihnen, Ihre Journeys einheitlich auszulösen, um in Echtzeit Nachrichten an den Kontakt zu senden, der in die Journey gelangt. In der Ereigniskonfiguration konfigurieren Sie die Ereignisse, die in den Journeys erwartet werden. Die Daten der eingehenden Ereignisse werden nach dem Adobe Experience-Datenmodell (XDM) normalisiert. Ereignisse stammen aus Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse). Weitere Informationen zu Ereignissen [in diesem Abschnitt](../../event/about-events.md).

* [!DNL Journey Optimizer] verfügt über integrierte Nachrichtenfunktionen: Sie können Ihre Nachrichten in einer Journey erstellen und Ihre Inhalte entwerfen. Wenn Sie zum Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, z. B. Adobe Campaign, erstellen Sie eine **benutzerdefinierte Aktion**. Weitere Informationen zu Aktionen finden Sie in diesem . [in diesem Abschnitt](../../action/action.md).
