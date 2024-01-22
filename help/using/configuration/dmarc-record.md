---
solution: Journey Optimizer
product: journey optimizer
title: DMARC-Eintrag
description: Erfahren Sie, wie Sie DMARC-Datensätze in Journey Optimizer festlegen.
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domäne, E-Mail, Dmarc, Datensatz
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 1%

---

# DMARC-Eintrag {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Festlegen des DMARC-Datensatzes"
>abstract="Legen Sie DMARC-Datensatz fest, um Zustellbarkeitsprobleme mit ISPs zu vermeiden. Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden."

>[!CAUTION]
>
>Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer jetzt die DMARC-Authentifizierungstechnologie.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo von Ihnen, dass Sie über eine **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails verwenden. Diese neue Anforderung beginnt am **1. Februar 2024**.

Erfahren Sie mehr über die Anforderungen von Google und Yahoo in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Wenn diese neue Anforderung von Gmail und Yahoo nicht erfüllt wird, wird erwartet, dass E-Mails in den Spam-Ordner gelangen oder blockiert werden.

Daher empfiehlt Adobe dringend, sicherzustellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie zum Adobe in [!DNL Journey Optimizer]. Führen Sie die folgenden Schritte aus, die auf Ihren Fall zutreffen:

* Wenn Sie [vollständig delegiert](delegate-subdomain.md#full-subdomain-delegation) Führen Sie eine der beiden folgenden Optionen aus, um Ihre Subdomains an Adobe zu senden:

   * Richten Sie DMARC in der übergeordneten Domäne Ihrer delegierten Subdomains ein **in Ihrer Hosting-Lösung**.

   * Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **über die bevorstehende Funktion in der [!DNL Journey Optimizer] Administration-Benutzeroberfläche** - ohne zusätzliche Arbeit an Ihrer Hosting-Lösung.

* Wenn Sie [CNAME-Zuweisung](delegate-subdomain.md#cname-subdomain-delegation) Befolgen Sie für Ihre sendenden Subdomains eine der beiden folgenden Optionen:

   * Richten Sie DMARC auf Ihren Subdomains oder in der übergeordneten Domäne Ihrer Subdomains ein **in Ihrer Hosting-Lösung**.

   * Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **über die bevorstehende Funktion in der [!DNL Journey Optimizer] Administration-Benutzeroberfläche**. Sie erfordert jedoch auch die Eingabe in Ihre Hosting-Lösung. Stellen Sie daher sicher, dass Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die Aktualisierung so bald wie möglich durchführen kann. [!DNL Journey Optimizer] ist verfügbar (am 30. Januar). <!--and be ready on February 1st, 2024-->

**Weitere Informationen über [!DNL Journey Optimizer] Die bevorstehende DMARC-Funktion wird in Kürze verfügbar sein.**

>[!NOTE]
>
>Erfahren Sie mehr über die Implementierung von DMARC im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} , um die Auswirkungen auf die Zustellbarkeit von E-Mails besser zu verstehen.

## Was ist DMARC?

DMARC, das für **Domänenbasierte Nachrichtenauthentifizierung, Berichterstellung und Konformität** ist eine E-Mail-Authentifizierungsmethode/-Protokoll, mit der Domain-Inhaber ihre Domain vor unbefugter Verwendung schützen können.

Dies bietet eine Möglichkeit, die Domain des Absenders zu authentifizieren, und verhindert, dass böswillige Akteure E-Mails senden, die scheinbar von Ihrer Domain stammen.

DMARC bietet außerdem Feedback zum E-Mail-Authentifizierungsstatus und ermöglicht es Absendern, zu steuern, was mit E-Mails mit fehlgeschlagener Authentifizierung passiert. Dies umfasst Optionen zum Überwachen, Quarantänen oder Ablehnen von E-Mails, abhängig davon, welche DMARC-Richtlinie implementiert wurde.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC verfügt über drei Richtlinienoptionen:

* Überwachen (p=none): Weist den Postfachanbieter/ISP an, alles zu tun, was er normalerweise für die Nachricht tun würde.
* Quarantäne (p=quarantine): Weist den Postfachanbieter/ISP an, E-Mails zu senden, die DMARC nicht an den Spam- oder Junk-Ordner des Empfängers weitergeben.
* Ablehnen (p=reject): Weist den Postfachanbieter/ISP an, E-Mails zu blockieren, die DMARC nicht übergeben und zu einem Absprung führen.

## Wie wirkt DMARC?

SPF und DKIM werden beide verwendet, um eine E-Mail mit einer Domäne zu verknüpfen und um E-Mails zu authentifizieren. DMARC geht noch einen Schritt weiter und hilft, das Spoofing zu verhindern, indem die von DKIM und SPF überprüfte Domain abgeglichen wird. Um DMARC zu übergeben, muss eine Nachricht SPF oder DKIM übergeben. Wenn beide diese Authentifizierungsfehler beheben, schlägt DMARC fehl und die E-Mail wird gemäß Ihrer ausgewählten DMARC-Richtlinie zugestellt.

* SPF (Sender Policy Framework): DMARC verlässt sich bei der Authentifizierung der Identität des E-Mail-Servers auf SPF. SPF hilft bei der Überprüfung, ob die E-Mail-Nachricht von einer autorisierten Quelle stammt, indem die IP-Adresse des sendenden Servers mit einer Liste autorisierter IP-Adressen für die Domäne verglichen wird.
* DKIM (DomainKeys Identified Mail): DMARC verwendet DKIM auch zum Hinzufügen einer digitalen Signatur zu E-Mail-Nachrichten, sodass der Empfänger die Integrität und Authentizität der Nachricht überprüfen kann.

>[!NOTE]
>
>DMARC erfordert die Ausrichtung zwischen der Adresse &quot;Von&quot;und der Adresse &quot;Return-Path&quot;.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implementieren von DMARC {#implement-dmarc}

Um DMARC zu implementieren, führen Sie die folgenden Schritte aus, die für Ihren Fall gelten.

* Wenn Sie DMARC nicht hinzufügen, werden Sie (zumindest) unter Quarantäne gestellt.

### Vollständig delegierte Subdomains

Legen Sie die Aktion fest, die der Empfängerserver ausführen soll, wenn DMARC fehlschlägt.

DMARC verfügt über drei Richtlinienoptionen:

* Überwachen (p=none): Weist den Postfachanbieter/ISP an, alles zu tun, was er normalerweise für die Nachricht tun würde. Dies ist der Standardwert.
* Quarantäne (p=quarantine): Weist den Postfachanbieter/ISP an, E-Mails zu senden, die DMARC nicht an den Spam- oder Junk-Ordner des Empfängers weitergeben.
* Ablehnen (p=reject): Weist den Postfachanbieter/ISP an, E-Mails zu blockieren, die DMARC nicht übergeben und zu einem Absprung führen.

E-Mails zum Empfang aggregierter DMARC-Berichte und forensischer DMARC-Fehlerberichte: Sie können bis zu 5 Adressen hinzufügen.

* Stellen Sie sicher, dass Sie einen echten Posteingang haben, in dem Sie den Posteingang empfangen können - Sie verwalten diesen Posteingang (sollte kein Adobe-Posteingang sein).

Anwendbarer Prozentsatz von E-Mails zur Anwendung von DMARC:

Berichtsintervall: Die Empfehlung lautet 24, da ISPs dies im Allgemeinen haben.
falls weniger, bewerten Sie Ihre Kapazität / überprüfen Sie Ihr > Chat-GPT.

Wenn ein DMARC-Datensatz erkannt wird, können Sie dieselben Werte kopieren und einfügen oder bei Bedarf ändern.

Wenn Sie nichts eingeben, werden Standardwerte verwendet.

### Mit CNAME delegierte Subdomains

für CNAME im Bearbeitungsfluss müssen Sie die CSV-Datei erneut herunterladen (nicht vollständig delegiert)





