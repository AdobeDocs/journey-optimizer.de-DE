---
solution: Journey Optimizer
product: journey optimizer
title: Opt-out-Verwaltung für Textnachrichten
description: Erfahren Sie, wie Sie das Opt-out mit SMS- bzw. MMS-Nachrichten verwalten können
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 100%

---

# Opt-out-Verwaltung für Textnachrichten {#sms-opt-out}

In Übereinstimmung mit den Branchenstandards und -vorschriften müssen alle SMS-Marketing-Nachrichten eine Möglichkeit für die Empfängerinnen und Empfänger enthalten, ihr Abo einfach zu kündigen. [Erfahren Sie mehr über Datenschutz und Opt-out-Verwaltung](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Die Kommunikation per Textnachricht kann je nach Art der Nachricht, dem Ort, von dem aus Sie Ihre Textnachrichten versenden, und dem Standort Ihrer Empfängerinnen oder Empfänger verschiedenen rechtlichen Anforderungen unterliegen. Adobe Journey Optimizer verarbeitet die Nachrichten an Kurz-, Lang- und gebührenfreie Nummern wie unten beschrieben. Sie sollten sich jedoch an Ihre Rechtsabteilung wenden, um sicherzustellen, dass Ihre Textnachrichten allen geltenden rechtlichen Anforderungen entsprechen.
>

## Native eingehende Keywords {#sms-native-keywords}

>[!NOTE]
>
> Nur Sinch und Infobip unterstützen native Schlüsselwörter, wenn sie mit Journey Optimizer verwendet werden.

Standardmäßig verarbeitet Adobe Journey Optimizer folgende standardmäßige englischsprachige Antwortnachrichten für Kurzwahlnummern, gebührenfreie Nummern und lange Nummern:

* **Opt-Out**: STOP, QUIT, CANCEL, END, UNSUBSCRIBE, NO.
* **Opt-In**: SUBSCRIBE, YES, UNSTOP, START, CONTINUE, RESUME, BEGIN.
* **Hilfe**: HELP.

Mit diesen Keywords wird in der Regel eine automatische Standardantwort von Ihrem Drittanbieter ausgelöst. Sie können dies direkt mit Ihrem Provider oder über dessen Dokumentations-Website abklären.

Stellen Sie bei Verwendung von Infobip sicher, dass für die Weiterleitungsaktion die Pull-Konfiguration ausgewählt ist.

Es sind keine Schritte erforderlich, um sicherzustellen, dass die SMS-Opt-out-Funktionen in Adobe Journey Optimizer funktionieren, da die Keyword-Antworten STOP, UNSTOP, START, QUIT, CANCEL, END und UNSUBSCRIBE automatisch erkannt werden. Der Opt-out-Status von Profilen wird in Echtzeit in Adobe Journey Optimizer aktualisiert.


## Blockierungslisten {#sms-blocklists}

Zusätzlich zum Stoppen des Versands durch Adobe Journey Optimizer auf der Grundlage des Opt-out-Status (bei direkten Integrationen mit Twilio, Infobip oder Sinch) führen die meisten SMS-Gateway-Anbieter auch eine Blockierungsliste, um sicherzustellen, dass eine SMS-Nachricht nicht an einen Kontakt gesendet wird, die sich für ein Opt-out entschieden hat. Wenn Sie einen anderen Anbieter als Sinch oder Twilio verwenden und eine SMS-Nachricht über einen [benutzerdefinierten Kanal](../building-journeys/using-custom-actions.md) senden, müssen Sie dies von Ihrem Anbieter bestätigen lassen.


## Kurzwahlnummern {#short-codes}

Standardmäßig werden Opt-in- oder Hilfe-Keywords für Kurzwahlnummern von Adobe Journey Optimizer nicht verarbeitet. Um die Einhaltung der Branchenvorschriften und -regeln für den Umgang mit Opt-outs zu gewährleisten, muss unbedingt sichergestellt werden, dass Ihre Kurzwahlnummer allen Richtlinien entspricht.

Allerdings unterstützt Journey Optimizer globale Opt-outs, die auf eingehenden Keywords mit unterschiedlichen Absender-IDs basieren.

## Alphanumerische Sender ID {#alphanumeric}

Alphanumerische Sender IDs sind nur für einseitige Nachrichten gedacht und können keine eingehenden Nachrichten empfangen. Daher sind die SMS-Keywords „STOP“, „START“, „HELP“ von Adobe Journey Optimizer für alphanumerische Sender IDs nicht anwendbar. Sie müssen andere Anweisungen geben, wie z. B. an das Support-Team zu schreiben, eine Support-Telefonnummer anzurufen oder eine andere Telefonnummer oder einen Code per SMS zu senden, damit die Benutzenden sich von den über die alphanumerische Sender ID gesendeten Nachrichten abmelden können.

## Video {#video-sms}

* Im folgenden Video erfahren Sie, wie Sie das Double-Opt-in für SMS konfigurieren.

+++ Siehe Video

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
