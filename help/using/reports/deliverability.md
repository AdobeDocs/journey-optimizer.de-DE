---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Zustellbarkeit
description: Zustellbarkeitsrichtlinien kennenlernen
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 96%

---

# Erste Schritte mit der Zustellbarkeit {#manage-deliverability}

Die Zustellbarkeit ist ein Maßstab für den Erfolg Ihrer Sendungen, die Posteingänge Ihrer Empfänger zu erreichen.

>[!NOTE]
>
>Für Kunden, die den Gesundheitsschild lizenzieren, nutzt Adobe Transport Layer Security (TLS) 1.2, um den Datenaustausch zwischen den Systemen (Empfängern) der Benutzer und Journey Optimizer (Absender) zu sichern. Wenn der empfangende E-Mail-Server TLS 1.2 nicht unterstützt, treten bei Kunden und Kundinnen Probleme mit der Zustellbarkeit auf, einschließlich der Rücksendung der E-Mail zum ursprünglichen Absender.

**E-Mail-Zustellbarkeit** bezieht sich auf jene Merkmale, die über die Fähigkeit einer Nachricht entscheiden, innerhalb kurzer Zeit über eine persönliche E-Mail-Adresse ihr Ziel zu erreichen – mit der erwarteten Qualität in Bezug auf Inhalt und Format. Diese Merkmale lassen sich in vier Kategorien einteilen: Datenqualität, Nachrichten und Inhalte, Sendeinfrastruktur und Reputation. Gemeinsam bilden sie die Grundlage eines erfolgreichen Email Deliverability-Programms.

Die **Zustellrate** ist der Anteil der Nachrichten, die die Posteingänge der Empfänger, im Vergleich zur gesamten Anzahl der versendeten Nachrichten, erreicht haben. Dabei spielen zahlreiche Faktoren eine Rolle, insbesondere:

* Begrenzte Spam-Beschwerden
* Niedrige Hardbounce-Rate
* Qualität der Zielkontakte
* Nachrichteninhalt
* Reputation des Absenders

Um die Zustellbarkeit Ihrer [!DNL Journey Optimizer]-Erlebnisse zu optimieren, empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices. Probleme mit der Zustellbarkeit hängen in der Regel mit Maßnahmen zum Schutz vor Spam zusammen, die von Internet-Service-Anbietern (ISPs) und Mailserver-Administratoren implementiert werden.

Einen tieferen Einblick in das Thema der Zustellbarkeit und weitere Informationen zu den wichtigsten Bedingungen, Konzepten und Ansätzen zur Zustellbarkeit erhalten Sie im [Adobe-Handbuch mit den Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de){target="_blank"}.

## Verringern der Beschwerderate {#reduce-complaint-rate}

ISPs haben in der Regel eine ausgeprägte Möglichkeit, eine empfangene Nachricht als Spam zu melden. Dadurch ist es möglich, unzuverlässige Quellen zu identifizieren. Indem Sie Opt-out-Anfragen schnell befolgen und damit zeigen, dass Sie ein zuverlässiger Absender sind, können Sie die Beschwerderate senken. [Weitere Informationen zum Opt-out-Management](../privacy/opt-out.md#opt-out-management)

Generell empfehlen wir, Empfänger nicht darin zu behindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Landingpage für die Abmeldung sollte nur eine einzige Validierungs-Schaltfläche aufweisen.

Seien Sie besonders vorsichtig, wenn Sie zusätzliche Bestätigungen anfordern: Ein Benutzer kann zwei E-Mail-Adressen auf denselben Posteingang umleiten lassen (zum Beispiel: vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn das Profil sich nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies verweigern, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Nutzen von Unterdrückungslisten {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungsliste, in der Spam-Beschwerden, Hardbounces und Softbounces, die beständig auftreten, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da das Senden an diese Kontakte Ihre Reputation beschädigen könnte.

[Weitere Informationen zur Unterdrückungsliste](suppression-list.md).

## Verwenden von Überwachungs-Tools {#monitoring-tools}

Verwenden Sie die von [!DNL Journey Optimizer] bereitgestellten Funktionen zur Überwachung der Zustellbarkeit.

Auf der Registerkarte **[!UICONTROL Ausführungen]** der Nachrichtenliste können Sie mit einer Reihe von Echtzeitindikatoren überprüfen, wie Ihre Sendungen funktionieren. Auf dieser Registerkarte wird unter anderem Folgendes angezeigt:
* Die Anzahl der erfolgreich ausgeführten, gesendeten und zugestellten Nachrichten.
* Die Anzahl der geöffneten Nachrichten und die Anzahl der Nachrichten/Links, auf die geklickt wurde.

## Anpassen des Nachrichteninhalts {#adapt-message-content}

In geringerem Maße kann der Inhalt bestimmter Nachrichten als Spam erkannt werden.

Um Ihre Zustellbarkeitsrate zu verbessern und sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen, sollten Sie bei der Gestaltung Ihrer Nachrichteninhalte die folgenden Grundsätze beachten:

* **Name und Adresse des Absenders:** Die Adresse muss die Identität eines Absenders enthalten. Die Domain muss im Besitz des Absenders und auf ihn registriert sein. Die Domain-Registrierung darf nicht anonymisiert sein.

* **Abmelde-Link und -Landingpage**: Der Link zum Abmelden ist unverzichtbar. Er muss sichtbar und gültig sein und das Formular muss funktionsfähig sein.

[Erfahren Sie mehr über das Entwerfen von E-Mail-Inhalten](../email/get-started-email-design.md).

## Reputation als Absender etablieren

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Siehe diesen [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).
