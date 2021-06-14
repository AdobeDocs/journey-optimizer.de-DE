---
title: Überwachen der Nachrichtenausführung
description: Lernen Sie Richtlinien zur Überwachung und Zustellbarkeit kennen
feature: Zustellbarkeit
topic: Content Management
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 98%

---

# Zustellbarkeit verwalten {#manage-deliverability}

![](assets/do-not-localize/badge.png)

Die Zustellbarkeit ist ein Maßstab für den Erfolg Ihrer Sendungen, die Posteingänge Ihrer Empfänger zu erreichen.

**E-Mail-Zustellbarkeit** bezieht sich auf jene Merkmale, die über die Fähigkeit einer Nachricht entscheiden, innerhalb kurzer Zeit über eine persönliche E-Mail-Adresse ihr Ziel zu erreichen – mit der erwarteten Qualität in Bezug auf Inhalt und Format. Diese Merkmale lassen sich in vier Kategorien einteilen: Datenqualität, Nachrichten und Inhalte, Sendeinfrastruktur und Reputation. Gemeinsam bilden sie die Grundlage eines erfolgreichen Email Deliverability-Programms.

Die **Zustellrate** ist der Anteil der Nachrichten, die die Posteingänge der Empfänger, im Vergleich zur gesamten Anzahl der versendeten Nachrichten, erreicht haben. Dabei spielen zahlreiche Faktoren eine Rolle, insbesondere:

* Begrenzte Spam-Beschwerden
* Niedrige Hardbounce-Rate
* Qualität der Zielkontakte
* Nachrichteninhalt
* Reputation des Absenders

Um die Zustellbarkeit Ihrer [!DNL Journey Optimizer]-Erlebnisse zu optimieren, empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices. Probleme mit der Zustellbarkeit hängen in der Regel mit Maßnahmen zum Schutz vor Spam zusammen, die von Internet-Service-Anbietern (ISPs) und Mailserver-Administratoren implementiert werden.

## Verringern der Beschwerderate {#reduce-complaint-rate}

ISPs haben in der Regel eine ausgeprägte Möglichkeit, eine empfangene Nachricht als Spam zu melden. Dadurch ist es möglich, unzuverlässige Quellen zu identifizieren. Indem Sie Opt-out-Anfragen schnell befolgen und damit zeigen, dass Sie ein zuverlässiger Absender sind, können Sie die Beschwerderate senken. [Weitere Informationen zum Opt-out-Management](consent.md#opt-out-management)

Generell empfehlen wir, Empfänger nicht darin zu behindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Landingpage für die Abmeldung sollte nur eine einzige Validierungs-Schaltfläche aufweisen.

Seien Sie besonders vorsichtig, wenn Sie zusätzliche Bestätigungen anfordern: Ein Benutzer kann zwei E-Mail-Adressen auf denselben Posteingang umleiten lassen (zum Beispiel: vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn das Profil sich nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies verweigern, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Nutzen von Unterdrückungslisten {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungsliste, in der Spam-Beschwerden, Hardbounces und Softbounces, die beständig auftreten, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da das Senden an diese Kontakte Ihre Reputation beschädigen könnte.

[Erfahren Sie mehr über die Unterdrückungsliste](suppression-list.md).

## Verwenden von Überwachungs-Tools {#monitoring-tools}

Verwenden Sie die von [!DNL Journey Optimizer] bereitgestellten Funktionen zur Überwachung der Zustellbarkeit.

Auf der Registerkarte **[!UICONTROL Ausführungen]** der Nachrichtenliste können Sie mit einer Reihe von Echtzeitindikatoren überprüfen, wie Ihre Sendungen funktionieren. Auf dieser Registerkarte wird unter anderem Folgendes angezeigt:
* Die Anzahl der erfolgreich ausgeführten, gesendeten und zugestellten Nachrichten.
* Die Anzahl der geöffneten Nachrichten und die Anzahl der Nachrichten/Links, auf die geklickt wurde.

[Weitere Informationen über die Überwachung der Nachrichtenausführung](message-monitoring.md).

## Anpassen des Nachrichteninhalts {#adapt-message-content}

In geringerem Maße kann der Inhalt bestimmter Nachrichten als Spam erkannt werden.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Um Ihre Zustellbarkeitsrate zu verbessern und sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen, sollten Sie bei der Gestaltung Ihrer Nachrichteninhalte die folgenden Grundsätze beachten:

* **Name und Adresse des Absenders:** Die Adresse muss die Identität eines Absenders enthalten. Die Domain muss im Besitz des Absenders und auf ihn registriert sein. Die Domain-Registrierung darf nicht anonymisiert sein.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Abmelde-Link und -Landingpage**: Der Link zum Abmelden ist unverzichtbar. Er muss sichtbar und gültig sein und das Formular muss funktionsfähig sein.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Erfahren Sie mehr über das Entwerfen von E-Mail-Inhalten](design-emails.md).
