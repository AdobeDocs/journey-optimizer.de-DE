---
solution: Journey Optimizer
product: journey optimizer
title: Einhalten der neuen DMARC-Anforderung
description: Erfahren Sie, warum und wann Sie einen DMARC-Eintrag in Journey Optimizer festlegen müssen
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domain, Mail, DMARC, Eintrag
source-git-commit: cdc3e0ffaddb2ad83ad1703c1858773d09557859
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 88%

---

# Einhalten der neuen DMARC-Anforderung {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Erfahren Sie mehr über die obligatorische DMARC-Aktualisierung"
>abstract="Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo, dass Sie über eine **DMARC-Eintrag** für alle Domänen, die Sie zum Senden von E-Mails an sie verwenden, beginnend mit **1. Februar 2024**.<br>Daher müssen Sie unbedingt für alle Subdomains, die Sie in Journey Optimizer an Adobe delegiert haben, einen DMARC-Eintrag einrichten."

Domain-basierte Nachrichtenauthentifizierung, Berichte und Konformität (DMARC) und ist eine E-Mail-Authentifizierungsmethode, mit der Domain-Besitzende ihre Domain vor unbefugter Verwendung schützen können. Durch eine klare Richtlinie für E-Mail-Anbieter/ISPs verhindert sie, dass auf böswillige Weise E-Mails gesendet werden, die scheinbar von Ihrer Domain stammen. Die Implementierung von DMARC verringert das Risiko, dass legitime E-Mails als Spam gekennzeichnet oder abgelehnt werden, und verbessert die Zustellbarkeit Ihrer E-Mails.

Zur Einhaltung der Best Practices in der Branche verlangen Google und Yahoo! einen **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails an sie verwenden. Diese neue Anforderung gilt ab dem **1. Februar 2024**. [Weitere Informationen](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=de#dmarc){target="_blank"}

>[!CAUTION]
>
>Bei Nichteinhaltung dieser neuen Anforderung von Gmail und Yahoo! werden E-Mails wahrscheinlich im Spam-Ordner landen oder blockiert.

Adobe empfiehlt daher dringend, DMARC-Einträge für alle Subdomains einzurichten, die Sie in [!DNL Journey Optimizer] an Adobe delegiert haben. Befolgen Sie die folgenden Schritte, die auf Ihren Fall zutreffen:

* Wenn Sie Ihre sendenden Subdomains [vollständig an Adobe delegiert](delegate-subdomain.md#full-subdomain-delegation) haben, führen Sie eine der folgenden Optionen aus:

   * Richten Sie DMARC auf der übergeordneten Domain Ihrer delegierten Subdomains **in Ihrer Hosting-Lösung** ein.
oder
   * Richten Sie DMARC in Ihren delegierten Subdomains **in der Konfigurations-Benutzeroberfläche von[!DNL Journey Optimizer]** ein – ohne zusätzliche Arbeit an Ihrer Hosting-Lösung. [Weitere Informationen](dmarc-record.md#implement-dmarc)

* Wenn Sie Ihre Versand-Subdomains mit [CNAME](delegate-subdomain.md#cname-subdomain-delegation) eingerichtet haben, führen Sie eine der folgenden Optionen aus:

   * Richten Sie DMARC auf Ihren Subdomains oder auf der übergeordneten Domain Ihrer Subdomains **in Ihrer Hosting-Lösung** ein.
oder
   * Richten Sie DMARC auf Ihren delegierten Subdomains **in der[!DNL Journey Optimizer]** Konfigurations-Benutzeroberfläche ein. [Weitere Informationen](dmarc-record.md#implement-dmarc)

  Allerdings ist für die CNAME-Delegierung auch ein Eintrag in Ihre Hosting-Lösung erforderlich. Daher sollten Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die in [diesem Abschnitt](dmarc-record.md#implement-dmarc) beschriebene Aktualisierung durchführen kann.


Die neuesten Zeitpläne, die von Google und Yahoo! wie folgt aussehen:

* Google:

   * **Februar 2024** – Beginn der temporären Bounces, die eine Warnung bei Nichterfüllung der Anforderungen bieten sollen. E-Mails werden nach kurzer Verzögerung wie gewohnt zugestellt, wenn Sie die Anforderungen noch nicht erfüllen. Wenn Sie die Anforderungen vollständig erfüllen, gibt es keine temporären Bounces und Sie werden nichts bemerken.

   * **April 2024** – Beginn der Blockierung von Absenderinnen und Absendern, die die DMARC-Anforderungen erfüllen. Zunächst wird nur ein Teil der nicht-konformen E-Mails blockiert, wobei der Prozentsatz der blockierten E-Mails im Laufe der Zeit steigt.

   * **1. Juni 2024** – Absenderinnen und Absender, die den Anforderungen nicht in vollem Umfang entsprechen, werden blockiert.

* Yahoo! hat keine genauen Daten angegeben, hat aber gesagt, &quot;die Einführung der Durchsetzung wird im Februar 2024 beginnen. Die Durchsetzung wird schrittweise eingeführt.“

>[!NOTE]
>
>Wenn Sie Fragen haben oder Unterstützung benötigen, wenden Sie sich an Ihren Kontakt bei der Adobe-Zustellbarkeitsabteilung bzw. beim Adobe-Support.

**Nützliche Links**

* Im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=de#about){target="_blank"} erfahren Sie mehr über DMARC
* Weitere Informationen zu diesen Änderungen finden Sie im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=de){target="_blank"}
* Die [Ankündigung von Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"} lesen
* Die [Yahoo- Ankündigung](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"} lesen
