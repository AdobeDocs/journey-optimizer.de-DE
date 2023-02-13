---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Opt-out-Verwaltung
description: Erfahren Sie, wie Sie das Opt-out mit SMS-Nachrichten verwalten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 676e2d6788c8110b76a38e857a62ba9c1be5842c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 48%

---

# SMS-Opt-out-Verwaltung {#sms-opt-out}

In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketing-Nachrichten eine Möglichkeit für die Empfänger enthalten, ihr Abo einfach zu kündigen. [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Für die Kommunikation von Textnachrichten können je nach Art der Nachricht, Ort des Versands und Ort der Empfänger unterschiedliche gesetzliche Anforderungen gelten. Während Adobe Journey Optimizer die Nachrichten über lange Codes und gebührenfreie Nummern wie unten beschrieben verarbeitet, wenden Sie sich an Ihren Rechtsbeistand, um sicherzustellen, dass Ihre SMS-Kommunikation allen geltenden gesetzlichen Compliance-Anforderungen entspricht.

## Native eingehende Suchbegriffe{#sms-native-keywords}

Standardmäßig verarbeitet Adobe Journey Optimizer englischsprachige Standard-Antwortnachrichten wie STOP, UNSTOP und START für Nachrichten von gebührenfreien und von normalen Nummern in Übereinstimmung mit den Industriestandards für native Integration wie Sinch und Twilio.

Diese Suchbegriffe werden in der Regel als Trigger für eine automatische Standardantwort von Ihrem Drittanbieter (z. B. Twilio oder Sinch) verwendet. Sie können dies direkt mit Ihrem Provider oder über dessen Dokumentations-Website abklären.

Es sind keine Schritte erforderlich, um sicherzustellen, dass die Funktionen zum Abmelden von SMS in Adobe Journey Optimizer funktionieren, da die Keyword-Antworten STOP, UNSTOP und START automatisch erkannt werden. Der Opt-out-Status von Profilen wird in Adobe Journey Optimizer in Echtzeit aktualisiert.


## Blockierungslisten{#sms-blocklists}

Zusätzlich zum Anhalten des Versands durch Adobe Journey Optimizer basierend auf dem Opt-out-Status (für direkte Integrationen mit Twilio oder Sinch) verfügen die meisten SMS-Gateway-Provider über eine Blockierungsliste, mit der sichergestellt wird, dass eine SMS-Nachricht nicht an eine Person gesendet wird, die sich für eine Abmeldung entschieden hat. Wenn Sie einen anderen Anbieter als Sinch oder Twilio verwenden und eine SMS per senden [benutzerspezifischer Kanal](../building-journeys/using-custom-actions.md)müssen Sie dies mit Ihrem Provider bestätigen.


## Kurzwahlnummern {#short-codes}

Standardmäßig verarbeitet Adobe Journey Optimizer keine Opt-out-, Opt-in- oder Hilfe-Suchbegriffe für Kurzwahlnummern. Sie müssen sicherstellen, dass Ihre Kurzwahlnummer allen Branchenregeln und -vorschriften für die Handhabung von Opt-outs gerecht wird.

## Alphanumerische Sender ID {#alphanumeric}

Alphanumerische Sender IDs sind nur für einseitige Nachrichten gedacht und können keine eingehenden Nachrichten empfangen. Daher sind die SMS-Keywords STOP, START, HELP von Adobe Journey Optimizer für alphanumerische Sender IDs nicht anwendbar. Sie müssen andere Anweisungen geben, wie z. B. an das Support-Team zu schreiben, eine Support-Telefonnummer anzurufen oder eine andere Telefonnummer oder einen Code per SMS zu senden, damit die Benutzenden sich von den über die alphanumerische Sender ID gesendeten Nachrichten abmelden können.

## Video {#video-sms}

Weiterführende Informationen über die Unterstützung nativer eingehender Keywords (START, STOP und UNSTOP) für SMS finden Sie in dem folgenden Video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
