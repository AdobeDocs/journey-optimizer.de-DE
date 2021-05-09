---
title: Überwachung der Nachrichtenausführung
description: Richtlinien zur Überwachung und Bereitstellung
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Zustellbarkeit verwalten {#manage-deliverability}

![](assets/do-not-localize/badge.png)

Die Lieferbarkeit ist ein Maßstab für den Erfolg Ihrer Versand, die Ihre Empfänger in Postfächern erreichen.

**Email Deliverability bezieht sich auf jene Merkmale, die über die Fähigkeit einer Nachricht bestimmen, innerhalb kurzer Zeit über eine persönliche E-Mail-Adresse ihr Ziel zu erreichen – mit der erwarteten Qualität in Bezug auf Inhalt und Format.** Diese Merkmale lassen sich in vier Kategorien einteilen: Datenqualität, Nachrichten und Inhalte, Sendeninfrastruktur und Ruf. Gemeinsam bilden sie die Grundlage eines erfolgreichen Email Deliverability-Programms.

Die **Auslieferungsrate** ist die Anzahl der Nachrichten, die die Postfächer der Empfänger im Vergleich zur Anzahl der ausgelieferten Nachrichten erreicht haben. Dabei spielen zahlreiche Faktoren eine Rolle, insbesondere:

* Eingeschränkte Spam-Beschwerden
* Niedrige Hartabstoßungsraten
* der Qualität der Zielkontakte;
* Nachrichteninhalt
* der Reputation des Absenders.

Um die Lieferbarkeit Ihrer [!DNL Journey Optimizer]-Erlebnisse zu optimieren, empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices. Probleme mit der Lieferbarkeit stehen in der Regel im Zusammenhang mit dem Schutz vor Spam, der von Internet-Dienstleistern (ISPs) und E-Mail-Serveradministratoren implementiert wurde.

## Verringerung der Beschwerderate {#reduce-complaint-rate}

ISPs haben in der Regel eine auffällige Möglichkeit, eine empfangene Nachricht als Spam Berichte. Dadurch können unzuverlässige Quellen identifiziert werden. Indem Sie schnell Abmeldeanfragen berücksichtigen und damit nachweisen, dass Sie ein zuverlässiger Absender sind, können Sie die Raten der Beschwerde reduzieren. [Erfahren Sie mehr über die Abmeldeverwaltung](consent.md#opt-out-management).

In der Regel sollten Sie Empfängern, die sich für eine Teilnahme ausschließen möchten, nicht die Möglichkeit geben, sich auszuschließen, indem Sie beispielsweise Felder wie die E-Mail-Adresse oder den Namen ausfüllen. Die Landingpage der Abmeldung sollte nur eine Schaltfläche zum Bestätigen enthalten.

Bezahlen Sie zusätzliche Vorsicht, wenn Sie eine zusätzliche Bestätigung anfordern: Ein Benutzer kann zwei E-Mail-Adressen in dasselbe Feld umgeleitet haben (z. B. firstname.lastname@club.com und firstname.lastname@internet-club.com). Wenn das Profil sich nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies verweigern, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Listen zur Fremdunterdrückung {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungs-Liste, die Spam-Beschwerden, feste Absprünge und weiche Absprünge erfasst, die konsistent ablaufen.

Zum Schutz Ihrer Lieferbarkeit werden die Empfänger, deren Adressen auf der Unterdrückungs-Liste stehen, standardmäßig von allen zukünftigen Versänden ausgeschlossen, da das Senden an diese Kontakte Ihren Ruf beschädigen könnte.

[Erfahren Sie mehr über die Unterdrückung von Listen](suppression-lists.md).

## Überwachungstools verwenden {#monitoring-tools}

Verwenden Sie die von [!DNL Journey Optimizer] angebotenen Funktionen, um Ihre Lieferbarkeit zu überwachen.

Auf der Registerkarte **[!UICONTROL Execution]** der Liste können Sie überprüfen, wie Ihre Versand mit einer Reihe von Echtzeitindikatoren arbeiten. Auf dieser Registerkarte wird unter anderem Folgendes angezeigt:
* Die Anzahl der erfolgreich ausgeführten, gesendeten und zugestellten Nachrichten.
* Die Anzahl der geöffneten Nachrichten und die Anzahl der Nachrichten/Links, auf die geklickt wurde.

[Erfahren Sie mehr über die Ausführung](message-monitoring.md) von Überwachungsmeldungen.

## Inhalt der adaptiven Nachricht {#adapt-message-content}

In geringerem Maße kann der Inhalt bestimmter Nachrichten als Spam erkannt werden.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Um Ihre Auslieferungsrate zu verbessern und sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen, befolgen Sie beim Entwerfen Ihres Nachrichteninhalts die folgenden Grundsätze:

* **Name und Anschrift** des Absenders: Die Adresse muss den Absender explizit identifizieren. Die Domain muss im Besitz des Absenders und auf ihn registriert sein. Die Domain-Registrierung darf nicht privat erfolgen.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Link und Landingpage** zum Abmelden: Der Link zum Abbestellen ist unverzichtbar. Es muss sichtbar und gültig sein, und das Formular muss funktionsfähig sein.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Weitere Informationen zum Entwerfen von E-Mail-Inhalten](design-emails.md).
