---
title: Technische Einstellungen
description: Erfahren Sie mehr über Richtlinien zu Administration und Einstellungen
hidefromtoc: true
hide: true
feature: Anwendungskonfiguration
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 100%

---

# Technische Einstellungen

![](../assets/do-not-localize/badge.png)

## Einrichten von Branding-Parametern{#cjm-branding}

Jedes Unternehmen verfügt über Richtlinien bezüglich der Darstellung und technischen Charakteristika seiner Marke. Sie können eine Reihe von Spezifikationen definieren, um Ihren Kunden eine einheitliche Markendarstellung zu bieten, von Logos bis hin zu technischen Aspekten wie E-Mail-Absender, Domain der URL der Mirror-Seiten oder Einstellungen zum Tracking von Nachrichten.
Marken können von Endbenutzern nicht erstellt oder geändert werden: Diese Konfiguration wird von Adobe verwaltet.

Um Branding-Parameter für Ihre [!DNL Journey Optimizer]-Instanz einzurichten, müssen Sie sich an Adobe wenden und die folgenden Details mitteilen:

* Firmenname

* E-Mail-Adresse des Absenders (von)

* Name des Absenders (von)

* Antwortadresse

Sobald die Branding-Parameter konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten auswählen.

Nachdem die Branding-Parameter konfiguriert wurden, können Sie sie beim Erstellen von Meldungen aus der Liste **[!UICONTROL Voreinstellungen]** auswählen. [Erfahren Sie mehr über die Inhaltserstellung](../create-message.md).

## Push-Benachrichtigungs-Kanal konfigurieren

In diesem [Abschnitt](../create-push.md) erfahren Sie, wie Sie den Push-Benachrichtigungs-Kanal konfigurieren.

## Zuweisen von Subdomains

Für jede neue Subdomain, die in [!DNL Journey Optimizer] verwendet werden soll, besteht der erste Schritt darin, sie zuzuweisen. Sie müssen sich an Ihren technischen Ansprechpartner bei Adobe wenden.

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Web-Seiten, die verfolgt werden sollen, das Anzeigen von Mirror-Seiten usw.

Diese Anforderungen werden über Komponenten verwaltet, die sowohl von Adobe als auch vom Kunden gehostet werden, und enthalten URLs, die für die Empfänger der E-Mails sichtbar sind.  Um URLs zu vermeiden, die auf die zugrunde liegende technische Lösung oder den Hosting-Anbieter hinweisen, können Subdomains eingerichtet werden, die diese Informationen vor den Empfängern der E-Mails verbergen.

Im Anschluss an diese Zuweisungen stellt die von Adobe eingerichtete Infrastruktur sicher, dass die folgenden Services für jede zugewiesene Domain oder Versand-Domain mit CNAME-Alias ausgeführt werden:

* Erstellen von postmaster@- und abuse@-Posteingängen

* Einrichten von Feedback-Schleifen für die zugewiesene Domain

* Grundlegende DMARC-Datensatzkonfiguration

Von Adobe festgelegte Parameter sind ab dem Zeitpunkt gültig, an dem die Zuweisung abgeschlossen und anschließend von Adobe überprüft wurde, und bleiben funktionsfähig, bis der Service gekündigt wird.

[Erfahren Sie mehr über die Zuweisung von Domains](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).


## Erstellen von Datenquellen, Ereignissen und Aktionen

Verwenden Sie den Abschnitt **[!UICONTROL Admin]**, um **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignisse]** und **[!UICONTROL Aktionen]** zu verwalten.

![](../assets/admin-menu.png)

### Datenquellen

Mit der Datenquellenkonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journeys abzurufen.

Weitere Informationen zu Datenquellen finden Sie in diesem [Abschnitt](../datasource/about-data-sources.md).

### Ereignisse

Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten.

In der Konfiguration von Ereignissen konfigurieren Sie die in den Journeys erwarteten Ereignisse. Die eingehenden Ereignisdaten werden mit dem Experience-Datenmodell (XDM) von Adobe normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse).

Weitere Informationen zu Ereignissen finden Sie in [diesem Abschnitt](../event/about-events.md).

### Aktionen

Die Nachrichtenfunktionen von [!DNL Journey Optimizer] sind integriert: Sie müssen nur Ihren Inhalt entwerfen und Ihre Nachricht veröffentlichen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen.

Weitere Informationen zu Aktionen finden Sie in [diesem Abschnitt](../action/action.md).
