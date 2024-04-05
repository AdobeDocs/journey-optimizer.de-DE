---
title: Erstellen einer Web-In-App-Nachricht in Journey Optimizer
description: Erfahren Sie, wie Sie in Journey Optimizer eine Web-In-App-Nachricht erstellen.
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 100%

---


# Konfigurieren des Web-In-App-Kanals {#configure-in-app-web}

## Voraussetzungen {#prerequisites}

* Stellen Sie sicher, dass Sie die neueste Version für Ihre **Adobe Experience Platform Web SDK**-Erweiterung verwenden.

* Installieren Sie die **Adobe Experience Platform Web SDK**-Erweiterung unter den **Tag-Eigenschaften** und aktivieren Sie die Option für den **Personalisierungsspeicher**.

  Diese Konfiguration ist für das Speichern von Ereignisverläufen auf dem Client unerlässlich. Sie ist eine Voraussetzung für die Implementierung von Häufigkeitsregeln im Regel-Builder. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=de)

  ![](assets/configure_web_inapp_1.png)

## Konfigurieren einer „Daten an Platform gesendet“-Regel {#configure-sent-data-trigger}

1. Navigieren Sie in Ihrer Instanz für die **Adobe Experience Platform-Datenerfassung** zu den mit der **Adobe Experience Platform Web SDK**-Erweiterung konfigurierten **Tag-Eigenschaften**.

1. Wählen Sie im Menü **Authoring** die Option **Regeln** und dann **Neue Regel erstellen** oder **Regel hinzufügen** aus.

   ![](assets/configure_web_inapp_2.png)

1. Klicken Sie im Abschnitt **Ereignisse** auf **Hinzufügen** und legen Sie folgende Konfiguration fest:

   * **Erweiterung**: Core

   * **Ereignistyp**: Bibliothek geladen (Seitenanfang)

   ![](assets/configure_web_inapp_3.png)

1. Wählen Sie **Änderungen beibehalten** aus, um die Ereigniskonfiguration zu speichern.

1. Klicken Sie im Abschnitt **Aktionen** auf **Hinzufügen** und legen Sie folgende Konfiguration fest:

   * **Erweiterung**: Adobe Experience Platform Web SDK

   * **Aktionstyp**: Ereignis senden

   ![](assets/configure_web_inapp_4.png)

1. Aktivieren Sie im Abschnitt **Personalisierung** Ihres **Aktionstyps** die Option zum **Rendern visueller Personalisierungsentscheidungen**.

   ![](assets/configure_web_inapp_5.png)

1. Definieren Sie im Abschnitt **Entscheidungskontext** die **Schlüssel**-**Wert**-Paare, die bestimmen, welches Erlebnis bereitgestellt werden soll.

   ![](assets/configure_web_inapp_6.png)

1. Speichern Sie Ihre **Aktionskonfiguration**, indem Sie auf **Änderungen beibehalten** klicken.

1. Navigieren Sie zum Menü für den **Veröffentlichungsfluss**. Erstellen Sie eine neue **Bibliothek** oder wählen Sie eine vorhandene **Bibliothek** aus und fügen Sie Ihre neu erstellte **Regel** hinzu. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=de#create-a-library)

1. Wählen Sie über Ihre **Bibliothek** die Option **Speichern und für Entwicklung erstellen** aus.

   ![](assets/configure_web_inapp_7.png)

## Konfigurieren einer manuellen Regel {#configure-manual-trigger}

1. Navigieren Sie in Ihrer Instanz für die **Adobe Experience Platform-Datenerfassung** zu den mit der **Adobe Experience Platform Web SDK**-Erweiterung konfigurierten **Tag-Eigenschaften**.

1. Wählen Sie im Menü **Authoring** die Option **Regeln** und dann **Neue Regel erstellen** oder **Regel hinzufügen** aus.

   ![](assets/configure_web_inapp_8.png)

1. Klicken Sie im Abschnitt **Ereignisse** auf **Hinzufügen** und legen Sie folgende Konfiguration fest:

   * **Erweiterung**: Core

   * **Ereignistyp**: Klick

   ![](assets/configure_web_inapp_9.png)

1. Definieren Sie in der **Klickkonfiguration** den **Selektor**, der ausgewertet werden soll.

   ![](assets/configure_web_inapp_10.png)

1. Klicken Sie auf **Änderungen beibehalten**, um die **Ereigniskonfiguration** zu speichern.

1. Klicken Sie im Abschnitt **Aktionen** auf **Hinzufügen** und legen Sie folgende Konfiguration fest:

   * **Erweiterung**: Adobe Experience Platform Web SDK

   * **Aktionstyp**: Regelsätze auswerten

   ![](assets/configure_web_inapp_11.png)

1. Aktivieren Sie im Abschnitt **Aktion zum Auswerten von Regelsätzen** Ihres **Aktionstyps** die Option zum **Rendern visueller Personalisierungsentscheidungen**.

   ![](assets/configure_web_inapp_13.png)

1. Definieren Sie im Abschnitt **Entscheidungskontext** die **Schlüssel**-**Wert**-Paare, die bestimmen, welches Erlebnis bereitgestellt werden soll.

1. Rufen Sie das Menü **Veröffentlichungsfluss** auf, erstellen Sie eine neue **Bibliothek** oder wählen Sie eine vorhandene **Bibliothek** aus und fügen Sie Ihre neu erstellte **Regel** hinzu. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=de#create-a-library)

1. Wählen Sie über Ihre **Bibliothek** die Option **Speichern und für Entwicklung erstellen** aus.

   ![](assets/configure_web_inapp_14.png)

