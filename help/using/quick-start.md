---
title: Schnellstart
description: Journey Optimizer – Schnellstart
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
source-git-commit: 9c1edc8d79c58fcf4f2048b9fe81cd31ea621777
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 100%

---

# Schnellstart {#cjm-quick-start}

## Wichtige Schritte für den Start {#cjm-key-steps}

Mit [!DNL Adobe Journey Optimizer] können Sie bestehende Nachrichteninhalte importieren und neue Inhalte entwerfen, Nachrichten mit Kundenprofildaten personalisieren, Ereignisse erstellen, die Nachrichten auslösen, Segmente definieren und Audiences verfeinern, Multi-Channel-Nachrichten versenden, Angebote erstellen und hinzufügen und auf einen kompletten Satz von Reporting- und Überwachungs-Tools zugreifen, um die Wirkung Ihrer Nachrichten und Customer Journeys zu messen.

Abhängig von Ihrem Unternehmen können Sie verschiedene Typen von Benutzern definieren und ihnen je nach deren Berechtigungen Zugriff auf bestimmte Funktionen gewähren.

## Vorbereiten und Konfigurieren der Umgebung

Bevor Sie mit der Verwendung von [!DNL Adobe Journey Optimizer] beginnen, sind mehrere Schritte erforderlich, um Ihre Umgebung vorzubereiten.

Als Systemadministrator müssen Sie **Produktprofile verstehen und Berechtigungen** für die Sandbox-Verwaltung und Kanalkonfiguration zuweisen. Außerdem müssen Sie Sandboxes einrichten und entsprechend den verfügbaren Produktprofilen verwalten.
Anschließend können Sie Produktprofilen Team-Mitglieder zuweisen und die **Kanalkonfiguration** für das Messaging einrichten.

Weitere Informationen finden Sie auf den folgenden Seiten:

* **Legen Sie Benutzerberechtigungen fest** und gewähren Sie Ihren Team-Mitgliedern Zugriff. [Mehr dazu](../using/administration/permissions.md)

* **Stellen Sie[!DNL Adobe Experience Manager Assets Essentials]** zum Verwalten von Assets und Bildern in Ihren Nachrichten bereit: Benutzer, die Zugriff auf [!DNL Assets Essentials] benötigen, müssen Teil der Produktprofile **Assets Essentials Consumer-Benutzer** und/oder **Assets Essentials-Benutzer** sein. [Weitere Informationen finden Sie in der Dokumentation zu Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=de){target=&quot;_blank&quot;}

* **Konfigurieren Sie Ihre Kanäle** und definieren Sie die Einstellungen für E-Mails und Push-Benachrichtigungen. [Mehr dazu](../using/configuration/get-started-configuration.md)

* **Definieren Sie Ihre Voreinstellungen** und konfigurieren Sie Ihre Branding-Parameter. [Mehr dazu](../using/configuration/message-presets.md)

* **Verwalten Sie Sandboxes**, um Ihre Instanz in separate virtuelle Umgebungen zu unterteilen. [Mehr dazu](../using/administration/sandboxes.md)


## Vorbereiten der Daten und Konfigurieren der Journeys

Als Datenadministrator müssen Sie **Daten identifizieren und Schemas und Datensätze erstellen**, um Ihre Daten in Adobe Experience Platform transferieren zu können.

Die Schritte zum Erstellen eines Identity-Namespace und eines Datensatzes, der zur Verwendung in Profilen sowie zum Erstellen von Segmenten und Testprofilen aktiviert ist, werden in den folgenden Abschnitten beschrieben:

* In der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de){target=&quot;_blank&quot;} erfahren Sie, wie Sie einen **Datensatz** erstellen und ihn in der Vorschau anzeigen.

* In der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=de#manage-namespaces){target=&quot;_blank&quot;} erfahren Sie, wie Sie einen **Identity-Namespace** erstellen.

* Auf [dieser Seite](../using/building-journeys/creating-test-profiles.md) erfahren Sie, wie Sie **Testprofile** erstellen.

* Weitere Informationen zur **Datenaufnahme** finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=de){target=&quot;_blank&quot;}.

* Auf [dieser Seite](../using/segment/about-segments.md) erfahren Sie, wie Sie **eine Audience definieren**, Segmente erstellen sowie das Einverständnis und den Datenschutz verwalten.

Um Nachrichten in Journeys senden zu können, müssen Sie außerdem **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** konfigurieren. Weiterführende Informationen finden Sie in diesem [Abschnitt](../using/configuration/about-data-sources-events-actions.md)

## Nachrichten, Angebote und Journeys erstellen

Als Journey-Verantwortlicher können Sie anhand der folgenden Abschnitte Ihre erste Journey einrichten, Angebote und Assets hinzufügen und Nachrichten versenden:

* **Nachrichten erstellen**: Greifen Sie auf Nachrichten zu, entwerfen oder laden Sie Inhalte für E-Mails und Push-Benachrichtigungen, fügen Sie Personalisierungen hinzu und sehen Sie sich eine Vorschau der Nachrichten an. [Mehr dazu](create-message.md)

* **Assets hochladen**: Verwenden Sie Adobe Experience Manager Assets Essentials, um Assets und Bilder zu verwalten. [Mehr dazu](assets-essentials.md)

* **Angebote hinzufügen**: Verwenden Sie das Entscheidungs-Management in Journey Optimizer, um Ihren Nachrichten personalisierte Angebote hinzuzufügen. [Mehr dazu](../using/offers/get-started/starting-offer-decisioning.md)

* **Journeys erstellen**: Senden Sie Nachrichten, nutzen Sie kontextbezogene Daten, verfeinern Sie Audiences, entwerfen Sie mehrstufige Anwendungsfälle und führen Sie diese aus. [Mehr dazu](building-journeys/journey.md)

* **Nachrichten und Journeys überwachen**: Kontrollieren Sie den Versand von Nachrichten, prüfen Sie Nachrichten- und Journey-Berichte, verfolgen Sie Zustellbarkeitsmetriken. [Mehr dazu](message-monitoring.md)
