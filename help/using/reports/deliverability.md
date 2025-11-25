---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Zustellbarkeit
description: 'Zustellbarkeitsrichtlinien kennenlernen '
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '1138'
ht-degree: 100%

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
* Qualität der Zieladressen
* Nachrichteninhalt
* Reputation des Absenders

Um die Zustellbarkeit Ihrer [!DNL Journey Optimizer]-Erlebnisse zu optimieren, empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices. Probleme mit der Zustellbarkeit hängen in der Regel mit Maßnahmen zum Schutz vor Spam zusammen, die von Internet-Service-Anbietern (ISPs) und Mailserver-Administratoren implementiert werden.

Einen tieferen Einblick in das Thema der Zustellbarkeit und weitere Informationen zu den wichtigsten Bedingungen, Konzepten und Ansätzen zur Zustellbarkeit erhalten Sie im [Adobe-Handbuch mit den Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de){target="_blank"}.

## Verringern der Beschwerderate {#reduce-complaint-rate}

ISPs haben in der Regel eine ausgeprägte Möglichkeit, eine empfangene Nachricht als Spam zu melden. Dadurch ist es möglich, unzuverlässige Quellen zu identifizieren. Indem Sie Opt-out-Anfragen schnell befolgen und damit zeigen, dass Sie ein zuverlässiger Absender sind, können Sie die Beschwerderate senken. [Weitere Informationen zum Opt-out-Management](../privacy/opt-out.md#opt-out-decision-management)

Generell empfehlen wir, Empfänger nicht darin zu behindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Landingpage für die Abmeldung sollte nur eine einzige Validierungs-Schaltfläche aufweisen.

Seien Sie besonders vorsichtig, wenn Sie zusätzliche Bestätigungen anfordern: Ein Benutzer kann zwei E-Mail-Adressen auf denselben Posteingang umleiten lassen (zum Beispiel: vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn das Profil sich nur an die erste Adresse erinnern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies verweigern, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Nutzen von Unterdrückungslisten {#suppression-lists}

[!DNL Journey Optimizer] verwaltet eine Unterdrückungsliste, in der Spam-Beschwerden, Hardbounces und Softbounces, die beständig auftreten, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da das Senden an diese Kontakte Ihre Reputation beschädigen könnte.

[Weitere Informationen zur Unterdrückungsliste](suppression-list.md)

## Verwenden von Überwachungs-Tools {#monitoring-tools}

Verwenden Sie die von [!DNL Journey Optimizer] bereitgestellten Funktionen zur Überwachung der Zustellbarkeit.

Mithilfe der Kampagnen- und Journey-Berichte können Sie mit einer Reihe von Echtzeitindikatoren überprüfen, wie gut Ihre Sendungen funktionieren. Darin wird unter anderem Folgendes angezeigt:

* Die Anzahl der erfolgreich ausgeführten, gesendeten und zugestellten Nachrichten.
* Die Anzahl der geöffneten Nachrichten und die Anzahl der Nachrichten/Links, auf die geklickt wurde.

Erfahren Sie mehr über [Live-Berichte](../reports/live-report.md) und [Berichte für die gesamte Zeit](../reports/report-gs-cja.md).

## Anpassen des Nachrichteninhalts {#adapt-message-content}

In geringerem Maße kann der Inhalt bestimmter Nachrichten als Spam erkannt werden.

Um Ihre Zustellbarkeitsrate zu verbessern und sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen, sollten Sie bei der Gestaltung Ihrer Nachrichteninhalte die folgenden Grundsätze beachten:

* **Name und Adresse des Absenders:** Die Adresse muss die Identität eines Absenders enthalten. Die Domain muss im Besitz des Absenders und auf ihn registriert sein. Die Domain-Registrierung darf nicht anonymisiert sein.

* **Abmelde-Link und -Landingpage**: Der Link zum Abmelden ist unverzichtbar. Er muss sichtbar und gültig sein und das Formular muss funktionsfähig sein.

[Weitere Informationen zum Entwerfen von E-Mail-Inhalten](../email/get-started-email-design.md)

## Reputation als Absender etablieren {#reputation}

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden.

Beim Versenden von E-Mails an eine brandneue IP-Adresse können Sie nun IP-Aufwärm-Workflows einfach direkt über die Benutzeroberfläche ausführen. 

Adobe Journey Optimizer bietet eine standardisierte und effiziente Methode zum Aufwärmen von IP-Adressen, die den Best Practices für optimale Zustellbarkeit entspricht.

[Weitere Informationen zu IP-Aufwärmplänen](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## Implementieren von DMARC {#dmarc}

Um das Risiko zu verringern, dass E-Mails als Spam gekennzeichnet oder abgelehnt werden, und Probleme mit der Zustellbarkeit zu vermeiden, ermöglicht [!DNL Journey Optimizer] Ihnen, den DMARC-Eintrag für alle Subdomains einzurichten, die Sie an Adobe delegieren.

Die Domain-basierte Nachrichtenauthentifizierung mit Berichten und Konformität (DMARC) ist eine E-Mail-Authentifizierungsmethode, mit der der Inhaberinnen und Inhaber einer Domain ihre Domain vor unbefugter Verwendung durch boshafte Akteure schützen können. 

[Weitere Informationen zu DMARC-Einträgen](../configuration/dmarc-record.md)

## Informationen zu Feedback-Schleifen {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Einige Subdomains sind möglicherweise nicht verfügbar"
>abstract="Bestimmte Subdomains sind aufgrund einer ausstehenden Feedback-Schleifen-Registrierung derzeit nicht zur Auswahl verfügbar. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss kann aus allen verfügbaren Subdomains ausgewählt werden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Erste Schritte mit der Delegierung von Subdomains"

Eine Feedback-Schleife (Feedback Loop, FBL) ist ein von einigen ISPs angebotener Dienst, mit dem die Absenderin bzw. der Absender einer E-Mail automatisch benachrichtigt werden kann, wenn Benutzende, die eine E-Mail erhalten, diese als Spam kennzeichnen (auch als „Beschwerde“ bezeichnet).

Nachdem eine Endbenutzerin oder ein Endbenutzer eine Beschwerde generiert hat, die vom ISP an Adobe zurückgesendet wurde, wird die E-Mail-Adresse automatisch zur [Unterdrückungsliste](../reports/suppression-list.md) hinzugefügt und von künftigen Sendungen ausgeschlossen. Der Versand von E-Mails an Benutzende, die sie als Spam gekennzeichnet haben, wirkt sich negativ auf die Reputation der Absenderin oder des Absenders aus und kann Probleme bei der Zustellbarkeit verursachen. [Weitere Informationen zu Spam-Beschwerden](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Nicht alle ISPs bieten eine herkömmliche FBL, z. B. Gmail. Gmail bietet kein Feedback auf individueller Ebene und kann nicht dazu verwendet werden, Spam-Beschwerden bis hin zu einzelnen Empfängerinnen oder Empfängern nachzuverfolgen, sondern konzentriert sich stattdessen auf die Berichterstellung auf aggregierter Ebene in den Google Postmaster Tools. [Weitere Informationen](https://support.google.com/a/answer/6254652?hl=de){target="_blank"}

Alle Adobe-Kundinnen und -Kunden werden automatisch in die herkömmlichen FBLs der folgenden ISPs eingeschrieben:

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

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

## Verwenden von SMTP-Relais {#smtp-relay}

[!DNL Journey Optimizer] verwendet Mail Transfer Agents (MTAs) und IPs von Adobe, um Ihre E-Mails an Internet-Dienstanbieter (Internet Service Providers, ISPs) zu senden. Unter bestimmten Umständen sollten Sie jedoch ggf. die endgültigen E-Mail-Sendungen über Ihre eigenen MTAs und IPs routen oder endgültige Validierungen der E-Mails durchführen, bevor Sie sie an Ihre Empfängerinnen und Empfänger senden.

In diesem Fall können Sie festlegen, dass Ihre E-Mails an SMTP-Server Ihrer Organisation weitergeleitet werden, anstatt direkt von Journey Optimizer an ISPs gesendet zu werden.

>[!AVAILABILITY]
>
>Die SMTP-Relais-Kapazität ist auf Anfrage verfügbar. Wenden Sie sich an den Adobe-Support.
