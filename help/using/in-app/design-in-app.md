---
title: Erstellen von In-App-Inhalten
description: Erfahren Sie, wie Sie In-App-Inhalte in Journey Optimizer erstellen.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Erstellen von In-App-Inhalten {#design-content}

Sie können den In-App-Inhalt bearbeiten, um Erlebnisoptionen zu konfigurieren, einschließlich des Nachrichtenlayouts und der Anzeige-, Text- und Schaltflächenoptionen.

Um den Nachrichteninhalt zu konfigurieren, klicken Sie auf die Schaltfläche **[!UICONTROL Edit content]** und verwenden Sie die Optionen im rechten Bereich des Bildschirms, um den Inhalt Ihrer In-App-Nachricht zu gestalten.

![](assets/edit-in-app-content.png)

Die **[!UICONTROL Advanced formatting]** -Umschalter aktiviert zusätzliche Optionen zum Anpassen des Erlebnisses.

Nachdem Sie Ihre In-App-Nachricht erstellt und deren Inhalt definiert und personalisiert haben, können Sie sie überprüfen und aktivieren. Die Benachrichtigungen werden dann entsprechend dem Kampagnenkalender gesendet. Weitere Informationen finden Sie unter [diese Seite](create-in-app.md#in-app-send).

## Nachrichtenlayout {#message-layout}

Aus dem **[!UICONTROL Message Layout]** eine der vier Layoutoptionen auswählen, die je nach Ihren Anforderungen für Nachrichten ausgewählt werden können.

![](assets/in_app_content_1.png)

* **[!UICONTROL Fullscreen]**: Dieser Layouttyp deckt den gesamten Bildschirm Ihrer Zielgruppengeräte ab.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Modal]**: Dieses Layout wird in einem großen Fenster im Stil eines Warnhinweises angezeigt, wobei Ihre Anwendung noch im Hintergrund sichtbar ist.

   Unterstützt werden Medien- (Bild, Video), Text- und Schaltflächenkomponenten.

* **[!UICONTROL Banner]**: Dieser Layouttyp wird als Warnhinweis für das native Betriebssystem angezeigt.

   Sie können nur eine **[!UICONTROL Header]** und **[!UICONTROL Body]** zu Ihrer Nachricht hinzufügen.

* **[!UICONTROL Custom]**: Im benutzerdefinierten Nachrichtenmodus können Sie eine Ihrer vorkonfigurierten HTML-Nachrichten direkt importieren und bearbeiten.

   * Auswählen **[!UICONTROL Compose]** , um Ihren rohen HTML-Code einzugeben oder einzufügen.

      Verwenden Sie den linken Bereich, um die Personalisierungsfunktionen von Journey Optimizer zu nutzen. Weitere Informationen hierzu finden Sie unter [diesem Abschnitt](../personalization/personalize.md).

   * Auswählen **[!UICONTROL Import]** um die HTML- oder ZIP-Datei zu importieren, die Ihren HTML-Inhalt enthält.

## Registerkarte &quot;Inhalt&quot; {#content-tab}

Aus dem **Inhalt** können Sie Folgendes definieren und personalisieren: Inhalt der Benachrichtigung und Stil der **Schließen** Schaltfläche. Sie können auch Medien zu Ihrer In-App-Benachrichtigung hinzufügen und Aktionsschaltflächen von diesem Tab hinzufügen.

### Schaltfläche schließen {#close-button}

![](assets/in_app_content_2.png)

Wählen Sie die **[!UICONTROL Style]** Ihrer **[!UICONTROL Close button]**.

Verfügbare Stile sind:

* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** von einer Medien-URL oder Ihren Assets.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Advanced formatting mode]** eingeschaltet ist, können Sie die **[!UICONTROL Color]** -Option, um die Farbe und Deckkraft Ihrer Schaltfläche auszuwählen.

+++

### Medien {#add-media}

Die **[!UICONTROL Media]** Mit diesem Feld können Sie Medien zu Ihrer In-App-Nachricht hinzufügen, um für Endbenutzer ein attraktives Erlebnis zu schaffen.

![](assets/in_app_content_3.png)

Geben Sie Ihre Medien-URL ein oder klicken Sie auf die **[!UICONTROL Select Assets]** -Symbol, um Ihrer In-App-Nachricht direkt Assets hinzuzufügen, die in Ihrer Assets-Bibliothek gespeichert sind. [Weitere Informationen zur Asset-Verwaltung](../email/assets-essentials.md).
Sie können auch eine **[!UICONTROL Alternative text]** für Bildschirmlesehilfen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Advanced formatting mode]** aktiviert ist, können Sie die **[!UICONTROL Max height]** und **[!UICONTROL Max width]** Ihrer Medien.

+++

### Kopfzeile und Hauptteil {#title-body}

Um Ihre Nachricht zu erstellen, geben Sie den Inhalt im **[!UICONTROL Header]** und **[!UICONTROL Body]** -Felder.

![](assets/in_app_content_4.png)

Verwenden Sie die **[!UICONTROL Personalization]** zum Hinzufügen einer Personalisierung. Erfahren Sie mehr über die Personalisierung im Ausdruckseditor für Adobe Journey Optimizer [in diesem Abschnitt](../personalization/personalize.md).

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Advanced formatting mode]** eingeschaltet ist, können Sie für Ihre **[!UICONTROL Header]** und **[!UICONTROL Body]**:

* die **[!UICONTROL Font]**
* die **[!UICONTROL Pt size]**
* die **[!UICONTROL Font Color]**
* die **[!UICONTROL Alignment]**
+++

### Schaltflächen {#add-buttons}

Fügen Sie Schaltflächen hinzu, über die Benutzer mit Ihrer In-App-Nachricht interagieren können.

![](assets/in_app_content_5.png)

So personalisieren Sie Ihre Schaltfläche:

1. Bearbeiten Sie das Textfeld Schaltfläche 1 (primär) . Sie können auch die **[!UICONTROL Personalization]** -Symbol, um Inhalt und Personalisierungsdaten zu definieren.

1. Wählen Sie Ihre **[!UICONTROL Interact event]** definiert die Aktion Ihrer Schaltfläche, nachdem Benutzer damit interagiert haben.

1. Geben Sie Ihre Web-URL oder Ihren Deeplink im **[!UICONTROL Target]** -Feld.

1. Um mehrere Schaltflächen hinzuzufügen, klicken Sie auf **[!UICONTROL Add button]**.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Advanced formatting mode]** eingeschaltet ist, können Sie für Ihre **[!UICONTROL Buttons]**:

* die **[!UICONTROL Font]**
* die **[!UICONTROL Pt size]**
* die **[!UICONTROL Font Color]**
* die **[!UICONTROL Alignment]**
* die **[!UICONTROL Button style]**
* die **[!UICONTROL Radius]**
* die **[!UICONTROL Button color]**

+++

## Registerkarte Einstellungen {#settings-tab}

Aus dem **Einstellungen** können Sie das Nachrichtenlayout definieren und eine Vorschau Ihrer In-App-Nachricht anzeigen. Sie können auch auf erweiterte Formatierungsoptionen zugreifen.

### Vorschau {#preview-tab}

![](assets/in_app_content_6.png)

Die **[!UICONTROL App Preview]** ermöglicht das Hinzufügen eines Hintergrunds hinter Ihrer In-App-Nachricht:

* Ein Medium aus einem URL-Link.

* Ein Asset aus Ihrer Assets-Bibliothek.

* Eine Hintergrundfarbe.

### Layout {#layout-options}

![](assets/in_app_content_7.png)

Die **[!UICONTROL Background image]** -Feld können Sie Ihrer In-App-Nachricht einen Hintergrund hinzufügen:

* Ein Medium aus einem URL-Link.

* Eine Hintergrundfarbe.

### Nachricht {#message-tab}

![](assets/in_app_content_8.png)

Die standardmäßig aktivierte Übernahmeoption der Benutzeroberfläche ermöglicht es Ihnen, den Hintergrund hinter Ihrer In-App-Nachricht zu dunkeln, um den Fokus auf Ihren Inhalt zu legen.

+++Mehr Optionen mit erweiterter Formatierung

Wenn die Variable **[!UICONTROL Advanced formatting mode]** aktiviert ist, können Sie Ihre Nachricht mit den folgenden Optionen weiter personalisieren:

* **[!UICONTROL Customize gestures]**: können Sie anpassen, was die Benutzer-Wischinteraktion ist. Wenn &quot;dismiss&quot;ausgewählt ist, können Sie ein benutzerdefiniertes Interaktionsereignis und/oder ein Zielziel hinzufügen.

* **[!UICONTROL Customize UI takeover]**: ermöglicht die Auswahl einer im Hintergrund anzuzeigenden Farbe und ihrer Deckkraft.

* **[!UICONTROL Customize size]**: können Sie die Breite und Höhe Ihrer In-App-Benachrichtigung anpassen.

* **[!UICONTROL Customize position]**: können Sie die Position Ihrer In-App-Nachrichten auf dem Bildschirm Ihrer Benutzer anpassen. Sie können die senkrechte und die horizontale Ausrichtung ändern.

* **[!UICONTROL Customize animation]**: Sie können Ihre Anzeige- und Verwerfen-Animationen anpassen, z. B. wenn Ihre In-App-Benachrichtigung von links oder oben auf dem Gerät des Benutzers angezeigt wird.

* **[!UICONTROL Message round corner]**: ermöglicht es Ihnen, Ihrer In-App-Benachrichtigung eine runde Ecke hinzuzufügen, indem Sie die **[!UICONTROL Corner radius]**.

+++

**Verwandte Themen:**

* [In-App-Nachricht erstellen](create-in-app.md)
* [In-App-Bericht](inapp-report.md)
* [In-App-Konfiguration](inapp-configuration.md)
