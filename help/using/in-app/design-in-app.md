---
title: Gestalten Ihrer In-App-Inhalte
description: Erfahren Sie, wie Sie In-App-Inhalte in Journey Optimizer erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
keywords: In-App, Nachricht, Design, Formatierung
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 98%

---

# Gestalten Ihrer In-App-Inhalte {#design-content}

Sie können die In-App-Inhalte bearbeiten, um Erlebnisoptionen zu konfigurieren, einschließlich des Nachrichtenlayouts und der Anzeige-, Text- und Schaltflächenoptionen.

Um den Nachrichteninhalt zu konfigurieren, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** und verwenden Sie die Optionen im rechten Bereich des Bildschirms, um den Inhalt Ihrer In-App-Nachricht zu gestalten.

![](assets/edit-in-app-content.png)

Der Umschalter **[!UICONTROL Erweiterte Formatierung]** aktiviert zusätzliche Optionen zum Anpassen des Erlebnisses.

Nachdem Sie Ihre In-App-Nachricht erstellt und deren Inhalt definiert und personalisiert haben, können Sie sie überprüfen und aktivieren. Die Benachrichtigungen werden dann entsprechend dem Zeitplan für die Kampagne gesendet. Weiterführende Informationen finden Sie auf [dieser Seite](create-in-app.md#in-app-send).

## Nachrichten-Layout {#message-layout}

Wählen Sie eine der vier Layout-Optionen aus dem Bereich **[!UICONTROL Nachrichten-Layout]** aus, die Ihnen je nach Messaging-Anforderung zur Auswahl angeboten werden.

![](assets/in_app_content_1.png)

* **[!UICONTROL Vollbild]**: Mit dieser Einstellung wird der gesamte Bildschirm der Geräte Ihrer Audience ausgefüllt.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Modal]**: Mit dieser Einstellung wird ein großes Fenster im Stil eines Warnhinweises angezeigt, wobei Ihre Anwendung noch im Hintergrund sichtbar ist.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Banner]**: Diese Art von Layout erscheint als systemeigene Warnmeldung.

   Sie können nur jeweils eine **[!UICONTROL Kopfzeile]** und einen **[!UICONTROL Hauptteil]** zu Ihrer Nachricht hinzufügen.

* **[!UICONTROL Benutzerspezifisch]**: Im Modus „Benutzerdefinierte Nachricht“ können Sie eine vorkonfigurierte HTML-Nachricht direkt importieren und bearbeiten.

   * Wählen Sie die Option **[!UICONTROL Erstellen]** aus, um Ihren rohen HTML-Code einzugeben oder einzufügen.

      Verwenden Sie den linken Bereich, um die Personalisierungsfunktionen von Journey Optimizer anzuwenden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../personalization/personalize.md).

   * Wählen Sie **[!UICONTROL Import]** aus, um die HTML- oder ZIP-Datei zu importieren, die Ihren HTML-Inhalt enthält.

## Registerkarte „Inhalt“ {#content-tab}

Über die Registerkarte **Inhalt** können Sie Folgendes definieren und personalisieren: Inhalt der Benachrichtigung und Stil der Schaltfläche **Schließen**. Ebenso können Sie von dieser Registerkarte aus auch Medien zu Ihrer In-App-Benachrichtigung hinzufügen und Aktionsschaltflächen ergänzen.

### Schaltfläche „Schließen“ {#close-button}

![](assets/in_app_content_2.png)

Wählen Sie den **[!UICONTROL Stil]** Ihrer Schaltfläche **[!UICONTROL Schließen]**.

Folgende Stile sind verfügbar:

* **[!UICONTROL Einfach]**
* **[!UICONTROL Kreis]**
* **[!UICONTROL Benutzerdefiniertes Bild]** von einer Medien-URL oder Ihren Assets.

+++Mehr Optionen mit erweiterter Formatierung

Wenn der Modus **[!UICONTROL Erweiterte Formatierung]** eingeschaltet ist, können Sie die Option **[!UICONTROL Farbe]** prüfen, um die Farbe und Deckkraft Ihrer Schaltfläche festzulegen.

+++

### Medien {#add-media}

Über das Feld **[!UICONTROL Medien]** können Sie Medien zu Ihrer In-App-Nachricht hinzufügen, um das Erlebnis für die Endbenutzenden attraktiv zu gestalten.

![](assets/in_app_content_3.png)

Geben Sie Ihre Medien-URL ein oder klicken Sie auf das Symbol **[!UICONTROL Assets auswählen]**, um Ihrer In-App-Nachricht direkt Assets hinzuzufügen, die in Ihrer Assets-Bibliothek gespeichert sind. [Weitere Informationen über Asset-Management](../email/assets-essentials.md).
Sie können auch einen **[!UICONTROL Alternativtext]** für Bildschirmlesehilfen hinzufügen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn der Modus **[!UICONTROL Erweiterte Formatierung]** eingeschaltet ist, können Sie die Variablen **[!UICONTROL Maximale Höhe]** und **[!UICONTROL Maximale Breite]** für Ihre Medien individuell festlegen.

+++

### Kopfzeile und Hauptteil {#title-body}

Um Ihre Nachricht zu erstellen, geben Sie den Inhalt in die Felder **[!UICONTROL Kopfzeile]** und **[!UICONTROL Hauptteil]** ein.

![](assets/in_app_content_4.png)

Verwenden Sie das Symbol **[!UICONTROL Personalisierung]**, um für eine persönlichere Gestaltung zu sorgen. Weitere Informationen zur Personalisierung im Ausdruckseditor von Adobe Journey Optimizer finden Sie [in diesem Abschnitt](../personalization/personalize.md).

+++Mehr Optionen mit erweiterter Formatierung

Wenn der Modus **[!UICONTROL Erweiterte Formatierung]** eingeschaltet ist, können Sie folgende Parameter für Ihre **[!UICONTROL Kopfzeile]** und Ihren **[!UICONTROL Hauptteil]** wählen:

* die **[!UICONTROL Schriftart]**
* die **[!UICONTROL Punkt-Größe]**
* die **[!UICONTROL Schriftfarbe]**
* die **[!UICONTROL Ausrichtung]**
+++

### Schaltflächen        {#add-buttons}

Fügen Sie Schaltflächen hinzu, über die Benutzende mit Ihrer In-App-Nachricht interagieren können.

![](assets/in_app_content_5.png)

So personalisieren Sie Ihre Schaltfläche:

1. Bearbeiten Sie das primäre Textfeld (#1) für die Schaltfläche. Sie können auch das Symbol **[!UICONTROL Personalisierung]** verwenden, um Inhalte und Personalisierungsdaten zu definieren.

1. Wählen Sie Ihr **[!UICONTROL Interaktionsereignis]**. Es definiert die Aktion Ihrer Schaltfläche, nachdem Benutzende damit interagiert haben.

1. Geben Sie Ihre Web-URL oder Ihren Deeplink im Feld **[!UICONTROL Zielgruppe]** an.

1. Um mehrere Schaltflächen hinzuzufügen, klicken Sie auf **[!UICONTROL Schaltfläche hinzufügen]**.

+++Mehr Optionen mit erweiterter Formatierung

Wenn der Modus **[!UICONTROL Erweiterte Formatierung]** aktiviert ist, können Sie für Ihre **[!UICONTROL Schaltflächen]** Folgendes auswählen:

* **[!UICONTROL Schriftart]**
* die **[!UICONTROL Punkt-Größe]**
* die **[!UICONTROL Schriftfarbe]**
* **[!UICONTROL Ausrichtung]**
* **[!UICONTROL Schaltflächenstil]**
* **[!UICONTROL Radius]**
* **[!UICONTROL Schaltflächenfarbe]**

+++

## Einstellungen  Registerkarte {#settings-tab}

Auf der Registerkarte **Einstellungen** können Sie das Nachrichten-Layout definieren und eine Vorschau Ihrer In-App-Nachricht anzeigen. Sie können auch auf erweiterte Formatierungsoptionen zugreifen.

### Vorschau {#preview-tab}

![](assets/in_app_content_6.png)

Die **[!UICONTROL App-Vorschau]** ermöglicht das Hinzufügen eines Hintergrunds hinter Ihrer In-App-Nachricht:

* Ein Medium von einem URL-Link.

* Ein Asset aus Ihrer Assets-Bibliothek.

* Eine Hintergrundfarbe.

### Layout {#layout-options}

![](assets/in_app_content_7.png)

Mit dem Feld **[!UICONTROL Hintergrundbild]** können Sie Ihrer In-App-Nachricht einen Hintergrund hinzufügen:

* Ein Medium von einem URL-Link.

* Eine Hintergrundfarbe.

### Nachricht {#message-tab}

![](assets/in_app_content_8.png)

Die standardmäßig aktivierte Option „UI-Übernahme“ ermöglicht es Ihnen, den Hintergrund hinter Ihrer In-App-Nachricht abzudunkeln, um den Fokus auf Ihren Inhalt zu legen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn der Modus **[!UICONTROL Erweiterte Formatierung]** aktiviert ist, können Sie Ihre Nachricht mit den folgenden Optionen weiter personalisieren:

* **[!UICONTROL Gesten anpassen]**: Damit können Sie anpassen, was die Benutzer-Wischinteraktion ist. Wenn „Verwerfen“ ausgewählt ist, können Sie ein benutzerdefiniertes Interaktionsereignis und/oder ein Ziel hinzufügen.

* **[!UICONTROL UI-Übernahme anpassen]**: Ermöglicht die Auswahl einer im Hintergrund anzuzeigenden Farbe und ihrer Deckkraft.

* **[!UICONTROL Größe anpassen]**: Damit können Sie die Breite und Höhe Ihrer In-App-Benachrichtigung anpassen.

* **[!UICONTROL Position anpassen]**: Damit können Sie die Position Ihrer In-App-Nachrichten auf dem Bildschirm Ihrer Benutzenden anpassen. Sie können die vertikale und die horizontale Ausrichtung ändern.

* **[!UICONTROL Animation anpassen]**: Damit können Sie Ihre Anzeigen- und Verwerfen-Animationen anpassen, z. B. wenn Ihre In-App-Benachrichtigung von links oder oben auf dem Gerät des Benutzers angezeigt wird.

* **[!UICONTROL Nachricht mit abgerundeter Ecke]**: Ermöglicht es Ihnen, Ihrer In-App-Benachrichtigung eine runde Ecke hinzuzufügen, indem Sie den **[!UICONTROL Eckenradius]** ändern.

+++

**Verwandte Themen:**

* [Erstellen einer In-App-Nachricht](create-in-app.md)
* [In-App-Bericht](inapp-report.md)
* [In-App-Konfiguration](inapp-configuration.md)

## Anleitungsvideo{#video}

Das folgende Video zeigt, wie Sie Ihre In-App-Nachrichten erstellen und testen können.

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
