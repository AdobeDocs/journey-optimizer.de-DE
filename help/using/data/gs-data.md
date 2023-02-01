---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten in Journey Optimizer
description: Erfahren Sie, wie Sie mit Daten in Journey Optimizer arbeiten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Daten, Management, Plattform
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 96%

---

# Erste Schritte mit dem Daten-Management in [!DNL Journey Optimizer] {#about-data}

Reichhaltigkeit und Abdeckung von Endkundendaten definieren die Stärke und den Erfolg jeder Customer Experience-Lösung. Diese Daten sind für alle Kunden heilig und von höchstem Wert. Die Technologieauswahl ist jetzt inhärent mit einer strengen Auswertung der Datenverwaltungsfunktionen integriert.

Mit [!DNL Adobe Journey Optimizer] können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind.

**Meine Daten, meine Regeln** – [!DNL Adobe Journey Optimizer] Erstellt kontinuierlich (und in Echtzeit) neben allen Journey-Daten und Angebotsdaten, die mit deren Vorgängen verbunden sind, einen umfangreichen Satz an Kundenprofildaten. Strawman-Versionen von Benutzerdaten, die aus Ihren Datenbanken erfasst werden, werden angereichert und in hochwertige Daten mit Abdeckung und Tiefe umgewandelt. Sie wollen, dass diese Daten sicher und gleichzeitig überall verfügbar sind, damit Sie deren Wert in Ihrem gesamten IT-Ökosystem nutzen können.

Im Großen und Ganzen können Sie folgende Flexibilität von Ihren Daten erwarten:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Ziele" src="assets/do-not-localize/dest.png" /> 
 <br>Verfügbar in anderen Zielen – Während [!DNL Adobe Journey Optimizer] Daten für ein extrem personalisiertes Kundenerlebnis synchronisiert und integriert, wünschen Sie sich diese Daten in anderen Systemen in Ihrer gesamten Technologielandschaft, während Sie nach anderen Möglichkeiten suchen, diese Daten zu nutzen.
    <div>
     <a href="../start/ajo-integrations.md">Weitere Informationen</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Richtlinie" src="assets/do-not-localize/policy.png" /> 
 <br>Löschung basierend auf einem vereinbarten Zeitplan oder Ihrer Richtlinie – Die Löschung von Daten ist ein wichtiger Aspekt des Datenschutzes und ein wichtiger Schritt in allen Data-Governance-Prozessen. [!DNL Adobe Journey Optimizer] erzeugt möglicherweise mehr Daten als erforderlich. Außerdem sollten Sie darauf achten, was nach der vorgeschriebenen Aufbewahrungsdauer für einen Datensatz geschieht – sei es aus Gründen der Nützlichkeit oder der Vorschrift. Die Kontrolle, die Sie benötigen, besteht darin, Daten zu einem beliebigen Zeitpunkt löschen zu können. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Weitere Informationen</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], worauf [!DNL Adobe Journey Optimizer] basiert, bietet Ihnen ein höchstes Maß an Datenkontrolle – sowohl während als auch am Ende der Interaktion. Innerhalb von [!DNL Journey Optimizer] haben Sie die volle Kontrolle über die Daten (die entweder in [!DNL Journey Optimizer] eingebracht oder davon generiert werden), die auf diese Daten angewendete Governance und die Ziele, an die diese Daten gesendet werden.

Alle Daten werden als Eigentum von Kunden betrachtet und können nur auf Anfrage gepflegt, verschlüsselt, verteilt oder vernichtet werden. Adobe fungiert als Treuhänder, ohne jegliche Rechte an Ihren Daten.

Sie können die Datenflexibilität von [!DNL Journey Optimizer] nutzen, um Ihre spezifischen Anforderungen in Bezug auf die Aufbewahrung, Archivierung oder Löschung von Daten zu erfüllen:

* **Datenextraktion/Export**: Sie können die Extraktion von Quelldaten jederzeit über die Datenzugriffs-API ohne Strafen oder Zeitverzögerungen starten. Die [Datenzugriffs-API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=de){target="_blank"} bietet Benutzenden eine RESTful-Schnittstelle, die sich auf die Auffindbarkeit und Zugänglichkeit aufgenommener Datensätze innerhalb von [!DNL Adobe Experience Platform] konzentriert. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Beachten Sie, dass in Journeys oder Kampagnen verwendete Inhalte nicht über die oben genannten API- oder Zielmethoden extrahiert werden können.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Bereinigungs- und Archivierungsmechanismen**: Die Bereinigung von Daten und Archivierung kann in [!DNL Adobe Journey Optimizer] frei definiert und automatisiert werden, um die Datenaufbewahrungsrichtlinien zu automatisieren. Es ist möglich, für die verschiedenen Datenentitäten unterschiedliche Alterungsstrategien zu definieren. Exportmechanismen können auch so definiert werden, das alternde Daten vor einer Bereinigung oder Archivierung automatisch exportiert werden.

   Im Arbeitsbereich &quot;Datenhygiene&quot;können Sie verschiedene Aufgaben zur Datenhygiene erstellen und überwachen, darunter das Löschen von Verbraucheridentitäten und das Planen der Ablaufdaten von Datensätzen. Dieser Arbeitsbereich ist mit Security &amp; Privacy Shield und Healthcare Shield verfügbar. Weiterführende Informationen finden Sie auf [dieser Seite](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Datenextraktion bei Beendigung der Interaktion/Ausstieg**: Nach Vertragsende werden Ihre Daten vollständig aus der Datenspeicherung von Adobe entfernt. Außerdem können Sie vor Beendigung einer Vereinbarung die vollständigen Profilextrakte abrufen. Für diese Funktion fallen keine zusätzlichen Kosten an. Dies kann jederzeit und nicht nur bei Beendigung erfolgen.

Die oben genannten Methoden werden vertraglich definiert und im Datenverarbeitungsabkommen (Data Processing Agreement, DPA), das Adobe zu Beginn eines Engagements mit Ihnen abschließt, detailliert beschrieben. Adobe-Anwendungen, einschließlich [!DNL Journey Optimizer], sind so konzipiert, dass die Daten jedes Kunden als proprietäres Daten-Asset dieses Kunden gehandhabt werden.
