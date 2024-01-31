---
solution: Journey Optimizer
product: journey optimizer
title: Einhalten der neuen DMARC-Anforderung
description: Erfahren Sie, warum und wann Sie DMARC-Datensätze in Journey Optimizer festlegen müssen
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domäne, E-Mail, Dmarc, Datensatz
source-git-commit: c5da9e9cfd5c03d7c6898e492582e5cc3e466447
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 4%

---

# Einhalten der neuen DMARC-Anforderung {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Weitere Informationen zur obligatorischen DMARC-Aktualisierung"
>abstract="Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo von Ihnen, dass Sie über eine **DMARC-Eintrag** für alle Domänen, die Sie zum Senden von E-Mails an sie verwenden, beginnend mit **1. Februar 2024**.<br>Daher müssen Sie sicherstellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie an Adobe in Journey Optimizer delegiert haben."

Domain-based Message Authentication, Reporting and Conformance (DMARC) ist eine E-Mail-Authentifizierungsmethode, mit der Domain-Inhaber ihre Domain vor nicht autorisierter Verwendung schützen können. Durch eine klare Richtlinie für E-Mail-Anbieter/ISPs verhindert sie, dass böswillige Akteure E-Mails versenden, die behaupten, von Ihrer Domäne zu sein. Die Implementierung von DMARC verringert das Risiko, dass E-Mails als Spam gekennzeichnet oder abgelehnt werden, und verbessert die Zustellbarkeit Ihrer E-Mail.


Im Rahmen ihrer branchenüblichen Best Practices erzwingen Google und Yahoo! müssen beide **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails verwenden. Diese neue Anforderung gilt ab **1. Februar 2024**. [Weitere Informationen](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}

>[!CAUTION]
>
>Diese neue Anforderung von Gmail und Yahoo wird nicht erfüllt! wird erwartet, dass E-Mails in den Spam-Ordner gelangen oder blockiert werden.

Daher empfiehlt Adobe dringend, sicherzustellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie zum Adobe in [!DNL Journey Optimizer]. Führen Sie die folgenden Schritte aus, die auf Ihren Fall zutreffen:

* Wenn Sie [vollständig delegiert](delegate-subdomain.md#full-subdomain-delegation) Befolgen Sie eine der folgenden Optionen, um Ihre Subdomains an Adobe zu senden:

   * Richten Sie DMARC in der übergeordneten Domäne Ihrer delegierten Subdomains ein **in Ihrer Hosting-Lösung**.
oder
   * Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **im[!DNL Journey Optimizer]** Konfigurationsoberfläche - ohne zusätzliche Arbeit an Ihrer Hosting-Lösung. [Weitere Informationen](dmarc-record.md#implement-dmarc)

* Wenn Sie Ihre Versandsubdomains mit [CNAME](delegate-subdomain.md#cname-subdomain-delegation), führen Sie eine der folgenden Optionen aus:

   * Richten Sie DMARC auf Ihren Subdomains oder in der übergeordneten Domäne Ihrer Subdomains ein **in Ihrer Hosting-Lösung**.
oder
   * Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **im[!DNL Journey Optimizer]** Konfigurationsoberfläche. [Weitere Informationen](dmarc-record.md#implement-dmarc)

  Mit der CNAME-Zuweisung ist jedoch auch ein Eintrag in Ihrer Hosting-Lösung erforderlich. Stellen Sie daher sicher, dass Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die unter [diesem Abschnitt](dmarc-record.md#implement-dmarc).


Die neuesten Zeitpläne, die von Google und Yahoo gemeinsam genutzt werden, lauten wie folgt:

* Google:

   * **Februar 2024** - Vorübergehende Bounces, die eine Warnung vor Nichteinhaltung enthalten sollen, beginnen. E-Mails werden nach kurzer Verzögerung wie gewohnt zugestellt, wenn Sie die Anforderungen noch nicht erfüllen. Wenn Sie die Anforderungen vollständig erfüllen, gibt es keine temporären Bounces und Sie werden nicht betroffen sein.

   * **April 2024** - Für Absender, die nicht den DMARC-Anforderungen entsprechen, werden Blöcke gestartet. Zunächst wird nur ein Teil der nicht kompatiblen E-Mails blockiert, wobei der Prozentsatz der blockierten E-Mails im Laufe der Zeit steigt.

   * **1. Juni 2024** - Bei allen Absendern, die nicht der vollen Compliance entsprechen, kommt es zu Blockierungen.

* Yahoo hat keine genauen Termine angegeben, hat aber gesagt: &quot;Die Einführung der Durchsetzung wird im Februar 2024 beginnen. Die Durchsetzung wird schrittweise eingeführt.&quot;

>[!NOTE]
>
>Wenden Sie sich bei Fragen oder Support an Ihren Adobe Deliverability Consultant oder Ihren Adobe-Support-Mitarbeiter.

**Nützliche Links**

* Weitere Informationen zu DMARC finden Sie im Abschnitt [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Weitere Informationen zu diesen Änderungen finden Sie in der [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Lesen [Google Gmail-Mitteilung](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lesen [Yahoo! Mitteilung](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
