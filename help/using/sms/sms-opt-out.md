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
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: ht
source-wordcount: '415'
ht-degree: 100%

---

# SMS-Opt-out-Verwaltung {#sms-opt-out}

In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketing-Nachrichten eine Möglichkeit für die Empfänger enthalten, ihr Abo einfach zu kündigen. [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

Standardmäßig verarbeitet Adobe Journey Optimizer englischsprachige Standard-Antwortnachrichten wie STOP, UNSTOP und START für Nachrichten von gebührenfreien und von normalen Nummern in Übereinstimmung mit den Industriestandards für native Integration wie Sinch und Twilio. Diese Keywords lösen normalerweise eine automatische Standardantwort von Ihrem Dritt-Provider (wie beispielsweise Twilio, Sinch, etc.) aus. Sie können dies direkt mit Ihrem Provider oder über dessen Dokumentations-Website abklären.

Es sind keine Schritte erforderlich, um sicherzustellen, dass SMS-Opt-out-Funktionen in Adobe Journey Optimizer funktionieren, da die Keyword-Antworten STOP, UNSTOP und START automatisch erkannt werden.

Zusätzlich zum Abbrechen des Versands durch Adobe Journey Optimizer basierend auf dem Opt-out-Status (für direkte Integrationen mit Twilio oder Sinch) verfügen die meisten Provider von SMS-Gateways auch über eine Blockierungsliste, mit der sichergestellt wird, dass eine SMS-Nachricht nicht an einen Kontakt gesendet wird, der sich für einen Opt-out entschieden hat. Wenn Sie einen anderen Provider als Sinch oder Twilio verwenden und eine SMS über einen [benutzerdefinierten Kanal](../building-journeys/using-custom-actions.md) versenden, müssen Sie dies mit Ihrem Provider abklären.

>[!IMPORTANT]
>
>SMS-Kampagnen können je nach Art Ihrer SMS-Kampagne, dem Standort, von dem aus Sie Ihre SMS versenden, und dem Standort Ihrer Empfänger unterschiedliche rechtlichen Anforderungen unterliegen. <br>Auch wenn Adobe Journey Optimizer die Nachrichten an lange und gebührenfreie Nummern wie oben beschrieben verarbeitet, sollten Sie sich an Ihren Rechtsbeistand wenden, um sicherzustellen, dass Ihre SMS-Kampagne alle geltenden gesetzlichen Bestimmungen erfüllt.

## Kurzwahlnummern {#short-codes}

Adobe Journey Optimizer verarbeitet standardmäßig keine Opt-Out-, Opt-In- oder Hilfe-Keywords für Kurzwahlnummern.

Sie müssen sicherstellen, dass Ihre Kurzwahlnummer allen Branchenregeln und -vorschriften für die Handhabung von Opt-outs gerecht wird.

## Alphanumerische Sender ID {#alphanumeric}

Alphanumerische Sender IDs sind nur für einseitige Nachrichten gedacht und können keine eingehenden Nachrichten empfangen. Daher sind die SMS-Keywords STOP, START, HELP von Adobe Journey Optimizer für alphanumerische Sender IDs nicht anwendbar. Sie müssen andere Anweisungen geben, wie z. B. an das Support-Team zu schreiben, eine Support-Telefonnummer anzurufen oder eine andere Telefonnummer oder einen Code per SMS zu senden, damit die Benutzenden sich von den über die alphanumerische Sender ID gesendeten Nachrichten abmelden können.

## Video {#video-sms}

Weiterführende Informationen über die Unterstützung nativer eingehender Keywords (START, STOP und UNSTOP) für SMS finden Sie in dem folgenden Video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
