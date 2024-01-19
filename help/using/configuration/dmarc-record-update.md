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
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 19%

---

# Wichtige Aktualisierung des DMARC-Datensatzes{#dmarc-record}


>[!CAUTION]
>
>Nach den jüngsten Ankündigungen von Gmail und Yahoo für Massen-Absender unterstützt Journey Optimizer jetzt die DMARC-Authentifizierungstechnologie.

Im Rahmen ihrer branchenüblichen Best Practices verlangen Google und Yahoo, dass Sie über einen DMARC-Datensatz für jede Domäne verfügen, mit der Sie E-Mails an sie senden. Diese neue Anforderung beginnt am **1. Februar 2024**.

Erfahren Sie mehr über die Anforderungen von Google und Yahoo an DMARC-Einträge in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Erfahren Sie mehr über die angekündigten Änderungen in Google und Yahoo unter [diese Seite](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Als Nächstes haben Sie noch eine Aktion oder die nächsten Schritte für Ihren Abschnitt, in dem Folgendes aufgeführt wird:

Sie müssen sie für alle Ihre Subdomains einrichten
* Wenn Sie uns die Domain vollständig zugewiesen haben, haben Sie zwei Möglichkeiten
   * Richten Sie DMARC in der übergeordneten Domäne der delegierten Domäne in Ihrer Hosting-Lösung ein, ODER
   * Richten Sie DMARC in delegierter Domäne mithilfe unserer anstehenden Funktion in der Administrator-Benutzeroberfläche ein, ohne dass zusätzliche Arbeit bei der Hosting-Lösung erforderlich ist.
* Wenn Sie CNAME für Ihre Versanddomänen eingerichtet haben, haben Sie zwei Optionen
   * Richten Sie DMARC in der Subdomain ODER der übergeordneten Domäne der Subdomain in Ihrer Hosting-Lösung ein, ODER
   * Richten Sie DMARC mithilfe unserer anstehenden Funktion in der Administrator-Benutzeroberfläche ein. Es erfordert jedoch nicht nur unsere Benutzeroberfläche, sondern auch die Eingabe in die Hosting-Lösung.

Weitere Details zu unserer kommenden Funktion werden bald angezeigt.

Darüber hinaus können Sie die Auswirkung einbeziehen, wenn nicht festgelegt, indem Sie den für DMARC relevanten Abschnitt aus dem folgenden Abschnitt kopieren (kopiert aus dem obigen Link). Entweder ziehen wir einfach DMARC-bezogene Dinge heraus. Oder hier können Sie erklären, dass die Ankündigung für DMARC und einen Klick unsub ist und hier ist die neuesten über Zeitpläne für beide Funktionen.

Seit der ursprünglichen Ankündigung im Oktober wurden Aktualisierungen an den Zeitplänen vorgenommen.

Die neuesten Zeitpläne sehen wie folgt aus:

Gmail:

* Februar 2024 – Beginn von temporären Bounces, die eine Warnung bei Nichterfüllung der Anforderungen bieten sollen. E-Mails werden nach kurzer Verzögerung wie gewohnt zugestellt, wenn Sie die Anforderungen noch nicht erfüllen. Wenn Sie die Anforderungen vollständig erfüllen, gibt es keine temporären Bounces und Sie werden nichts bemerken.
* April 2024 – Beginn der Blockierung von Absendern und Absenderinnen, die nicht die Anforderungen erfüllen, mit Ausnahme der Abmeldung von Listen mit einem Klick. Zunächst wird nur ein Teil der nicht-konformen E-Mails blockiert, wobei der Prozentsatz der blockierten E-Mails im Laufe der Zeit steigt.
* 1. Juni 2024 – Absenderinnen und Absender, die den Anforderungen nicht in vollem Umfang entsprechen, werden blockiert, einschließlich der Abmeldung von Listen mit einem Klick.

Yahoo:

Hat keine genauen Daten angegeben, aber hat gesagt, &quot;die Einführung der Durchsetzung wird im Februar 2024 beginnen. Die Durchsetzung wird schrittweise eingeführt.&quot;
