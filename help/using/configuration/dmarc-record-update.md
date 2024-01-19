---
solution: Journey Optimizer
product: journey optimizer
title: Obligatorische DMARC-Aktualisierung
description: Erfahren Sie, warum und wann Sie DMARC-Datensätze in Journey Optimizer festlegen müssen
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Subdomain, Domäne, E-Mail, Dmarc, Datensatz
source-git-commit: 7cbd6a9e80a8d6b87b3c3011db80549a3b5f6e73
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 3%

---

# Obligatorische DMARC-Aktualisierung {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Weitere Informationen zur obligatorischen DMARC-Aktualisierung"
>abstract="Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo von Ihnen, dass Sie über eine **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails verwenden. Diese neue Anforderung beginnt am **1. Februar 2024**. <br>Daher empfiehlt Adobe dringend, sicherzustellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie an Adobe in Journey Optimizer delegiert haben."

Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo von Ihnen, dass Sie über eine **DMARC-Eintrag** für jede Domain, die Sie zum Senden von E-Mails verwenden. Diese neue Anforderung beginnt am **1. Februar 2024**.

Erfahren Sie mehr über die Anforderungen von Google und Yahoo in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Wenn diese neue Anforderung von Gmail und Yahoo nicht erfüllt wird, wird erwartet, dass E-Mails in den Spam-Ordner gelangen oder blockiert werden.

Daher empfiehlt Adobe dringend, sicherzustellen, dass Sie DMARC-Datensätze für alle Subdomains eingerichtet haben, die Sie zum Adobe in [!DNL Journey Optimizer]. Führen Sie eine der beiden folgenden Optionen aus:

* Richten Sie DMARC in Ihren Subdomains oder in der übergeordneten Domäne Ihrer Subdomains ein. **in Ihrer Hosting-Lösung**.

* Richten Sie DMARC auf Ihren zugewiesenen Subdomains ein **über die bevorstehende Funktion in der [!DNL Journey Optimizer] Administration-Benutzeroberfläche** - ohne zusätzliche Arbeit an Ihrer Hosting-Lösung.

  >[!CAUTION]
  >
  >Wenn Sie [CNAME-Zuweisung](delegate-subdomain.md#cname-subdomain-delegation) Für Ihre sendenden Subdomains ist auch ein Eintrag in Ihre Hosting-Lösung erforderlich. Stellen Sie sicher, dass Sie sich mit Ihrer IT-Abteilung abstimmen, damit diese die Aktualisierung so bald wie möglich durchführen kann [!DNL Journey Optimizer] ist verfügbar (am 30. Januar 2024). <!--and be ready on February 1st, 2024-->

  Weitere Informationen über [!DNL Journey Optimizer] Die bevorstehende DMARC-Funktion wird in Kürze verfügbar sein.

<!--
* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:
    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.
    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30) - and be ready on February 1st, 2024.
    
-->

>[!NOTE]
>
>Wenden Sie sich bei Fragen oder Support an Ihren Adobe Deliverability Consultant oder Ihren Adobe-Support-Mitarbeiter.

Die neuesten Zeitpläne, die von Google und Yahoo gemeinsam genutzt werden, lauten wie folgt:

* Google:

   * **Februar 2024** - Vorübergehende Bounces, die eine Warnung vor Nichteinhaltung enthalten sollen, beginnen. E-Mails werden nach kurzer Verzögerung wie gewohnt zugestellt, wenn Sie die Anforderungen noch nicht erfüllen. Wenn Sie die Anforderungen vollständig erfüllen, gibt es keine temporären Bounces und Sie werden nicht betroffen sein.

   * **April 2024** - Für Absender, die nicht den DMARC-Anforderungen entsprechen, werden Blöcke gestartet. Zunächst wird nur ein Teil der nicht kompatiblen E-Mails blockiert, wobei der Prozentsatz der blockierten E-Mails im Laufe der Zeit steigt.

   * **1. Juni 2024** - Bei allen Absendern, die nicht der vollen Compliance entsprechen, kommt es zu Blockierungen.

* Yahoo hat keine genauen Termine angegeben, hat aber gesagt: &quot;Die Einführung der Durchsetzung wird im Februar 2024 beginnen. Die Durchsetzung wird schrittweise eingeführt.&quot;

>[!NOTE]
>
>Erfahren Sie mehr über die Implementierung von DMARC im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} , um die Auswirkungen auf die Zustellbarkeit von E-Mails besser zu verstehen.
