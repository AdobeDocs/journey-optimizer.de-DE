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
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 71%

---

# Erste Schritte mit der Zustellbarkeit {#manage-deliverability}

Die Zustellbarkeit ist ein Maßstab für den Erfolg Ihrer Sendungen, die Posteingänge Ihrer Empfänger zu erreichen.

>[!NOTE]
>
>Für Kundinnen und Kunden mit einer Lizenz für Healthcare Shield nutzt Adobe Transport Layer Security (TLS) 1.2, um den Datenaustausch zwischen den Systemen der Benutzenden (Empfänger) und Journey Optimizer (Absender) zu schützen. Wenn der empfangende E-Mail-Server TLS 1.2 nicht unterstützt, treten bei Kunden und Kundinnen Probleme mit der Zustellbarkeit auf, einschließlich der Rücksendung der E-Mail zum ursprünglichen Absender.

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

ISPs haben in der Regel eine ausgeprägte Möglichkeit, eine empfangene Nachricht als Spam zu melden. Dadurch ist es möglich, unzuverlässige Quellen zu identifizieren. Indem Sie Opt-out-Anfragen schnell befolgen und damit zeigen, dass Sie ein zuverlässiger Absender sind, können Sie die Beschwerderate senken. [Erfahren Sie mehr über die Opt-out-Verwaltung](../privacy/opt-out.md#opt-out-management)

Generell empfehlen wir, Empfänger nicht darin zu behindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Landingpage für die Abmeldung sollte nur eine einzige Validierungs-Schaltfläche aufweisen.

Seien Sie besonders vorsichtig, wenn Sie zusätzliche Bestätigungen anfordern: Ein Benutzer kann zwei E-Mail-Adressen auf denselben Posteingang umleiten lassen (zum Beispiel: vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn das Profil sich nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies verweigern, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Nutzen von Unterdrückungslisten {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungsliste, in der Spam-Beschwerden, Hardbounces und Softbounces, die beständig auftreten, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da das Senden an diese Kontakte Ihre Reputation beschädigen könnte.

[Weitere Informationen zur Unterdrückungsliste](suppression-list.md)

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

[Erfahren Sie mehr über die Erstellung von E-Mail-Inhalten](../email/get-started-email-design.md)

## Reputation als Absender etablieren {#reputation}

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Weitere Informationen finden Sie in diesem [Anwendungsfall](../building-journeys/ramp-up-deliveries-uc.md).

## Implementieren von DMARC {#dmarc}

Um das Risiko zu verringern, dass E-Mails als Spam gekennzeichnet oder abgelehnt werden, und Probleme mit der Zustellbarkeit zu vermeiden, [!DNL Journey Optimizer] ermöglicht Ihnen, den DMARC-Datensatz für alle Subdomains einzurichten, die Sie an Adobe delegieren.

Domain-based Message Authentication, Reporting and Conformance (DMARC) ist eine E-Mail-Authentifizierungsmethode, mit der Domain-Inhaber ihre Domain vor nicht autorisierter Verwendung durch böswillige Akteure schützen können.

[Weitere Informationen zu DMARC-Datensätzen](../configuration/dmarc-record.md)

## Feedback-Schleifen {#feedback-loops}

Eine Feedback Loop (FBL) ist ein von einigen ISPs angebotener Dienst, mit dem der E-Mail-Absender automatisch benachrichtigt werden kann, wenn der Benutzer, der eine E-Mail erhält, diese als Spam kennzeichnet (auch als &quot;Beschwerde&quot;bezeichnet).

Nachdem ein Endbenutzer eine Beschwerde generiert hat, die vom ISP an die Adobe zurückgesendet wurde, wird die E-Mail-Adresse automatisch zum [Unterdrückungsliste](../reports/suppression-list.md) und von künftigen Sendungen ausgeschlossen sind. Der Versand von E-Mails an Benutzer, die sie als Spam gekennzeichnet haben, wirkt sich negativ auf die Reputation des Absenders aus und kann Probleme bei der Zustellbarkeit verursachen. [Weitere Informationen zu Spam-Beschwerden](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Nicht alle ISPs bieten eine herkömmliche FBL, z. B. Gmail. Gmail bietet kein Feedback auf individueller Ebene und kann nicht dazu verwendet werden, Spam-Beschwerden an einzelne Empfänger zu verfolgen, sondern sich stattdessen auf die Berichterstellung auf aggregierter Ebene in den Google Postmaster Tools zu konzentrieren. [Weitere Informationen](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Alle Adobe-Kunden werden automatisch in die herkömmlichen FBLs der folgenden ISPs eingeschrieben:

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* locaweb

* Mail.RU

* Microsoft

* OpenSRS

* rackspace

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Italia

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Virgin Media

* Yahoo

* Ziggo

Adobe überprüft diese FBLs regelmäßig, um sicherzustellen, dass die neuesten verfügbaren FBLs hinzugefügt werden.
