---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Abmeldeverwaltung
description: Erfahren Sie, wie Sie das Opt-out mit SMS verwalten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# SMS-Abmeldeverwaltung {#sms-opt-out}

In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketingnachrichten eine Möglichkeit für die Empfänger enthalten, sich einfach abzumelden. [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

Adobe Journey Optimizer verarbeitet standardmäßig englischsprachige Antwortnachrichten wie STOP, UNSTOP und START für gebührenfreie und lange Code-Nachrichten gemäß Industriestandards für die native Integration wie Sinch und Twilio. Diese Suchbegriffe lösen in der Regel eine automatische Standardantwort von Ihrem Drittanbieter aus (z. B. Twilio, Sinch usw.). Sie können dies direkt bei Ihrem Anbieter oder über dessen Dokumentations-Website bestätigen.

Es sind keine Schritte erforderlich, um sicherzustellen, dass die Funktionen zum Abmelden von SMS in Adobe Journey Optimizer funktionieren, da die Keyword-Antworten STOP, UNSTOP und START automatisch erkannt werden.

Zusätzlich zum Abbrechen des Versands durch Adobe Journey Optimizer basierend auf dem Opt-out-Status (für direkte Integrationen mit Twilio oder Sinch) führen die meisten SMS-Gateway-Anbieter auch eine Blockierungsliste auf, um sicherzustellen, dass eine SMS-Nachricht nicht an eine Person gesendet wird, die sich für eine Abmeldung entschieden hat. Wenn Sie einen anderen Anbieter als Sinch oder Twilio verwenden und eine SMS per senden [benutzerspezifischer Kanal](../building-journeys/using-custom-actions.md)müssen Sie dies mit Ihrem Provider bestätigen.

>[!IMPORTANT]
>
>Für Textnachrichten-Kampagnen können je nach Art Ihrer Textnachrichten-Kampagne, Ort des Versands Ihrer Textnachrichten und Ort der Empfänger verschiedene gesetzliche Anforderungen gelten. <br>Obwohl Adobe Journey Optimizer die Nachrichten wie oben beschrieben auf langen Codes und gebührenfreien Nummern verarbeitet, sollten Sie sich an Ihren Rechtsbeistand wenden, um sicherzustellen, dass Ihre Textnachrichten-Kampagne allen geltenden gesetzlichen Compliance-Anforderungen entspricht.

## Kurzwahlnummern {#short-codes}

Adobe Journey Optimizer verarbeitet standardmäßig keine Opt-out-, Opt-in- oder Hilfe-Suchbegriffe für Kurzwahlnummern.

Sie müssen sicherstellen, dass Ihre Kurzwahlnummer allen Branchenregeln und -vorschriften für den Opt-out-Umgang entspricht.

## Alphanumerische Sender-ID {#alphanumeric}

Alphanumerische Sender-IDs dienen nur für einmalige Nachrichten und können keine eingehenden Nachrichten empfangen. Daher sind die SMS STOP-, START- und HELP-Schlüsselwörter von Adobe Journey Optimizer nicht für Alpha Sender IDs anwendbar. Sie müssen weitere Anweisungen geben, z. B. Schreiben an das Supportteam, Anrufen einer Telefonleitung beim Support oder SMS an eine andere Telefonnummer oder einen anderen Code, damit sich Benutzer von Nachrichten abmelden können, die über die alphanumerische Sender-ID gesendet werden.

## Video {#video-sms}

Weiterführende Informationen zur Unterstützung von nativen eingehenden Keywords (START, STOP und UNSTOP) für SMS finden Sie im folgenden Video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
