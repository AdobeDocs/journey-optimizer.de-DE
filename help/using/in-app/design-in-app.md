---
title: Erstellen von In-App-Inhalten
description: Erfahren Sie, wie Sie In-App-Inhalte in Journey Optimizer erstellen
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 5%

---

# Erstellen von In-App-Inhalten {#design-content}

Sie können den In-App-Inhalt bearbeiten, um Erlebnisoptionen zu konfigurieren, einschließlich des Nachrichtenlayouts und der Anzeige-, Text- und Schaltflächenoptionen.

Um den Nachrichteninhalt zu konfigurieren, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** und verwenden Sie die Optionen im rechten Bereich des Bildschirms, um den Inhalt Ihrer In-App-Nachricht zu gestalten.

![](assets/edit-in-app-content.png)

Die **[!UICONTROL Erweiterte Formatierung]** -Umschalter aktiviert zusätzliche Optionen zum Anpassen des Erlebnisses.

Nachdem Sie Ihre In-App-Nachricht erstellt und deren Inhalt definiert und personalisiert haben, können Sie sie überprüfen und aktivieren. Die Benachrichtigungen werden dann entsprechend dem Kampagnenkalender gesendet. Weiterführende Informationen finden Sie auf [dieser Seite](create-in-app.md#in-app-send).

## Nachrichtenlayout {#message-layout}

Aus dem **[!UICONTROL Nachrichtenlayout]** eine der vier Layoutoptionen auswählen, die je nach Ihren Anforderungen für Nachrichten ausgewählt werden können.

![](assets/in_app_content_1.png)

* **[!UICONTROL Vollbild]**: Dieser Layouttyp deckt den gesamten Bildschirm Ihrer Zielgruppengeräte ab.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Modal]**: Dieses Layout wird in einem großen Fenster im Stil eines Warnhinweises angezeigt, wobei Ihre Anwendung noch im Hintergrund sichtbar ist.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Banner]**: Dieser Layouttyp wird als Warnhinweis für das native Betriebssystem angezeigt.

   Sie können nur eine **[!UICONTROL Kopfzeile]** und **[!UICONTROL body]** zu Ihrer Nachricht hinzufügen.

* **[!UICONTROL Benutzerdefiniert]**: Im benutzerdefinierten Nachrichtenmodus können Sie eine vorkonfigurierte HTML direkt importieren und bearbeiten.

   * Auswählen **[!UICONTROL Erstellen]** , um Ihren HTML-Rohcode einzugeben oder einzufügen.

      Verwenden Sie den linken Bereich, um die Personalisierungsfunktionen von Journey Optimizer zu nutzen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../personalization/personalize.md).

   * Auswählen **[!UICONTROL Import]** um die HTML- oder ZIP-Datei zu importieren, die Ihren HTML-Inhalt enthält.

## Registerkarte &quot;Inhalt&quot; {#content-tab}

Aus dem **Inhalt** können Sie Folgendes definieren und personalisieren: Inhalt der Benachrichtigung und Stil der **Schließen** Schaltfläche. Sie können auch Medien zu Ihrer In-App-Benachrichtigung hinzufügen und Aktionsschaltflächen von diesem Tab hinzufügen.

### Schaltfläche schließen {#close-button}

![](assets/in_app_content_2.png)

Wählen Sie die **[!UICONTROL Stil]** Ihrer **[!UICONTROL Schaltfläche schließen]**.

Verfügbare Stile sind:

* **[!UICONTROL Partizipative Kampagne (ohne Konfiguration)]**
* **[!UICONTROL Kreis]**
* **[!UICONTROL Benutzerdefiniertes Bild]** von einer Medien-URL oder Ihren Assets.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Erweiterter Formatierungsmodus]** eingeschaltet ist, können Sie die **[!UICONTROL Farbe]** -Option, um die Farbe und Deckkraft Ihrer Schaltfläche auszuwählen.

+++

### Medien {#add-media}

Die **[!UICONTROL Medien]** Mit diesem Feld können Sie Medien zu Ihrer In-App-Nachricht hinzufügen, um für Endbenutzer ein attraktives Erlebnis zu schaffen.

![](assets/in_app_content_3.png)

Geben Sie Ihre Medien-URL ein oder klicken Sie auf **[!UICONTROL Auswählen von Assets]** -Symbol, um Ihrer In-App-Nachricht direkt Assets hinzuzufügen, die in Ihrer Assets-Bibliothek gespeichert sind. [Weitere Informationen über Asset-Management](../design/assets-essentials.md).
Sie können auch eine **[!UICONTROL Alternativtext]** für Bildschirmlesehilfen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Erweiterter Formatierungsmodus]** aktiviert ist, können Sie die **[!UICONTROL Max. Höhe]** und **[!UICONTROL Max. Breite]** Ihrer Medien.

+++

### Kopfzeile und Hauptteil {#title-body}

Um Ihre Nachricht zu erstellen, geben Sie den Inhalt im **[!UICONTROL Kopfzeile]** und **[!UICONTROL body]** -Felder.

![](assets/in_app_content_4.png)

Verwenden Sie die **[!UICONTROL Personalisierung]** zum Hinzufügen einer Personalisierung. Weitere Informationen zur Personalisierung im Ausdruckseditor von Adobe Journey Optimizer [in diesem Abschnitt](../personalization/personalize.md).

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Erweiterter Formatierungsmodus]** eingeschaltet ist, können Sie für Ihre **[!UICONTROL Kopfzeile]** und **[!UICONTROL body]**:

* die **[!UICONTROL Schriftart]**
* die **[!UICONTROL Pt-Größe]**
* die **[!UICONTROL Schriftfarbe]**
* die **[!UICONTROL Ausrichtung]**
+++

### Schaltflächen        {#add-buttons}

Fügen Sie Schaltflächen hinzu, über die Benutzer mit Ihrer In-App-Nachricht interagieren können.

![](assets/in_app_content_5.png)

So personalisieren Sie Ihre Schaltfläche:

1. Bearbeiten Sie das Textfeld Schaltfläche 1 (primär) . Sie können auch die **[!UICONTROL Personalisierung]** -Symbol, um Inhalt und Personalisierungsdaten zu definieren.

1. Wählen Sie Ihre **[!UICONTROL Interaktionsereignis]** definiert die Aktion Ihrer Schaltfläche, nachdem Benutzer damit interagiert haben.

1. Geben Sie Ihre Web-URL oder Ihren Deeplink im **[!UICONTROL Target]** -Feld.

1. Um mehrere Schaltflächen hinzuzufügen, klicken Sie auf **[!UICONTROL Schaltfläche hinzufügen]**.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Erweiterter Formatierungsmodus]** eingeschaltet ist, können Sie für Ihre **[!UICONTROL Schaltflächen]**:

* die **[!UICONTROL Schriftart]**
* die **[!UICONTROL Pt-Größe]**
* die **[!UICONTROL Schriftfarbe]**
* die **[!UICONTROL Ausrichtung]**
* die **[!UICONTROL Schaltflächenstil]**
* die **[!UICONTROL Radius]**
* die **[!UICONTROL Schaltflächenfarbe]**

+++

## Einstellungen  Registerkarte {#settings-tab}

Aus dem **Einstellungen** können Sie das Nachrichtenlayout definieren und eine Vorschau Ihrer In-App-Nachricht anzeigen. Sie können auch auf erweiterte Formatierungsoptionen zugreifen.

### Vorschau {#preview-tab}

![](assets/in_app_content_6.png)

Die **[!UICONTROL App-Vorschau]** ermöglicht das Hinzufügen eines Hintergrunds hinter Ihrer In-App-Nachricht:

* Ein Medium aus einem URL-Link.

* Ein Asset aus Ihrer Assets-Bibliothek.

* Eine Hintergrundfarbe.

### Layout {#layout-options}

![](assets/in_app_content_7.png)

Die **[!UICONTROL Hintergrundbild]** -Feld können Sie Ihrer In-App-Nachricht einen Hintergrund hinzufügen:

* Ein Medium aus einem URL-Link.

* Eine Hintergrundfarbe.

### Nachricht {#message-tab}

![](assets/in_app_content_8.png)

Die standardmäßig aktivierte Übernahmeoption der Benutzeroberfläche ermöglicht es Ihnen, den Hintergrund hinter Ihrer In-App-Nachricht zu dunkeln, um den Fokus auf Ihren Inhalt zu legen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Erweiterter Formatierungsmodus]** aktiviert ist, können Sie Ihre Nachricht mit den folgenden Optionen weiter personalisieren:

* **[!UICONTROL Gesten anpassen]**: können Sie anpassen, was die Benutzer-Wischinteraktion ist. Wenn &quot;dismiss&quot;ausgewählt ist, können Sie ein benutzerdefiniertes Interaktionsereignis und/oder ein Zielziel hinzufügen.

* **[!UICONTROL Übernahme der Benutzeroberfläche anpassen]**: ermöglicht die Auswahl einer im Hintergrund anzuzeigenden Farbe und ihrer Deckkraft.

* **[!UICONTROL Größe anpassen]**: können Sie die Breite und Höhe Ihrer In-App-Benachrichtigung anpassen.

* **[!UICONTROL Position anpassen]**: können Sie die Position Ihrer In-App-Nachrichten auf dem Bildschirm Ihrer Benutzer anpassen. Sie können die senkrechte und die horizontale Ausrichtung ändern.

* **[!UICONTROL Animation anpassen]**: Sie können Ihre Anzeige- und Verwerfen-Animationen anpassen, z. B. wenn Ihre In-App-Benachrichtigung von links oder oben auf dem Gerät des Benutzers angezeigt wird.

* **[!UICONTROL Rundmeldung]**: ermöglicht es Ihnen, Ihrer In-App-Benachrichtigung eine runde Ecke hinzuzufügen, indem Sie die **[!UICONTROL Eckenradius]**.

+++

**Verwandte Themen:**

* [In-App-Nachricht erstellen](create-in-app.md)
* [In-App-Bericht](inapp-report.md)
* [In-App-Konfiguration](inapp-configuration.md)

