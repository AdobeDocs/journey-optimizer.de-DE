---
title: Technische Einstellungen
description: Richtlinien zu Administration und Einstellungen
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Technische Einstellungen

![](assets/do-not-localize/badge.png)

## Einrichten von Branding-Parametern{#cjm-branding}

Jedes Unternehmen verfügt über Richtlinien bezüglich der Darstellung und technischen Charakteristika seiner Marke. Sie können eine Reihe von Spezifikationen definieren, um Ihren Kunden eine einheitliche Markendarstellung zu bieten, von Logos bis hin zu technischen Aspekten wie E-Mail-Absender, Domäne der URL der Mirrorseiten oder Einstellungen zur Verfolgung von Nachrichten.
Marken können von Endbenutzern nicht erstellt oder geändert werden: Diese Konfiguration wird von der Adobe verwaltet.

Um Branding-Parameter für Ihre [!DNL Journey Optimizer]-Instanz einzurichten, müssen Sie sich an die Adobe wenden und die folgenden Details freigeben:

* Unternehmensname

* E-Mail-Adresse des Absenders (von)

* Name des Absenders (von)

* Antwort-Adresse

Sobald die Branding-Parameter konfiguriert wurden, können Sie sie beim Erstellen von Nachrichten auswählen.

Nachdem die Branding-Parameter konfiguriert wurden, können Sie sie beim Erstellen von Meldungen aus der Liste **[!UICONTROL Vorgaben]** auswählen. [Erfahren Sie mehr über die Inhaltserstellung](create-message.md).

## Push-Benachrichtigungs-Kanal konfigurieren

Erfahren Sie, wie Sie Push-Kanal in diesem [Abschnitt](configure-push.md) konfigurieren.

## Subdomänendelegation

Für jede neue Subdomäne, die in [!DNL Journey Optimizer] verwendet werden soll, besteht der erste Schritt darin, sie zu delegieren. Sie müssen sich an Ihren technischen Ansprechpartner bei der Adobe wenden.

Bei der Implementierung einer Lösung gibt es Anforderungen an nach außen gerichtete Komponenten: Dazu gehören das Einrichten von Links und Webseiten, die verfolgt werden sollen, das Anzeigen von Mirrorseiten usw.

Während diese Anforderungen über Komponenten verwaltet werden, die sowohl von der Adobe als auch vom Kunden gehostet werden, enthalten sie URLs, die vom Empfänger der E-Mails gesehen werden können.  Um zu vermeiden, dass URLs vorhanden sind, die die zugrunde liegende technische Lösung oder den Hosting-Anbieter angeben, können Subdomänen eingerichtet werden, um dies für den Empfänger der E-Mails transparent zu machen.

Im Anschluss an diese Delegationen stellt die von der Adobe eingerichtete Infrastruktur sicher, dass für jede übertragene oder CNAME-Alias übertragene Sendeindustrie folgende Dienste erbracht werden:

* Postmaster@- und Missbrauchs@-Postfächer erstellen

* Einrichtung von Feedback-Schleifen für die delegierte Domäne

* Grundlegende DMARC-Datensatzkonfiguration

Die von der Adobe festgelegten Parameter gelten erst ab dem Zeitpunkt, zu dem die Übertragung abgeschlossen und dann durch Adobe überprüft wurde, und bleiben funktionsfähig.

[Erfahren Sie mehr über die Domänendelegation](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html).


## Erstellen von Datenquellen, Ereignissen und Aktionen

Verwenden Sie den Abschnitt **[!UICONTROL Admin]**, um **[!UICONTROL Datenquellen]**, **[!UICONTROL Ereignis]** und **[!UICONTROL Aktionen]** zu verwalten.

![](assets/admin-menu.png)

### Datenquellen

Mit der Datenquellenkonfiguration können Sie eine Systemverbindung definieren, um zusätzliche Informationen abzurufen, die in Ihren Journey verwendet werden.

Weitere Informationen zu Datenquellen finden Sie in diesem [Abschnitt](../using/datasource/about-data-sources.md)

### Ereignisse

Mit Ereignissen können Sie Ihre Journey einheitlich Trigger haben, um Nachrichten in Echtzeit an die Einzelperson zu senden, die in die Journey fließt.

In der Konfiguration des Ereignisses konfigurieren Sie die in den Journey erwarteten Ereignis. Die Daten der eingehenden Ereignis werden nach dem Adobe Experience Data Model (XDM) normalisiert. Die Ereignisse stammen von Streaming-Aufnahme-APIs für authentifizierte und nicht authentifizierte Ereignisse (z. B. Adobe Mobile SDK-Ereignisse).

Weitere Informationen zu Ereignissen finden Sie in diesem [Abschnitt](../using/event/about-events.md)

### Aktionen

[!DNL Journey Optimizer] Nachrichtenfunktionen sind integriert: Sie müssen nur Ihren Inhalt entwerfen und Ihre Nachricht veröffentlichen. Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen.

Weitere Informationen zu Aktionen in diesem [Abschnitt](../using/action/action.md)
