---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten in Journey Optimizer
description: Erfahren Sie, wie Sie mit Daten in Journey Optimizer arbeiten.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Daten, Verwaltung, Plattform
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 68%

---

# Erste Schritte mit der Datenverwaltung in [!DNL Journey Optimizer] {#about-data}

Reichweite und Abdeckung von Endkundendaten definiert die Stärke und den Erfolg jeder Customer Experience-Lösung. und diese Daten sind heilig und haben den höchsten Wert für jeden einzelnen Kunden. Die Technologieauswahl ist jetzt von Natur aus mit einer strengen Auswertung der Datenverwaltungsfunktionen integriert.

Mit [!DNL Adobe Journey Optimizer]können Sie diese Daten einfach verwalten, speichern und an Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind.

**Meine Daten, meine Regeln** - [!DNL Adobe Journey Optimizer] kontinuierlich (und in Echtzeit) ein umfangreiches Sortiment von Kundenprofildaten erstellt, zusätzlich zu allen Journey-Daten und Angebotsdaten, die mit den-Aktivitäten verbunden sind. Strawman-Versionen von Benutzerdaten, die aus Ihren Datenbanken erfasst werden, werden angereichert und in hochwertige Daten mit Abdeckung und Tiefe umgewandelt. Sie wollen, dass diese Daten sicher und gleichzeitig überall verfügbar sind, damit Sie deren Wert in Ihrem gesamten IT-Ökosystem nutzen können.

Im Großen und Ganzen ist die Flexibilität, die Sie von Ihren Daten erwarten,:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Ziele" src="assets/do-not-localize/dest.png" /> 
 <br>[!DNL Adobe Journey Optimizer]Verfügbar in anderen Zielen – Während Daten für ein extrem personalisiertes Kundenerlebnis synchronisiert und integriert, wünschen Sie sich diese Daten in anderen Systemen in Ihrer gesamten Technologielandschaft, während Sie nach anderen Möglichkeiten suchen, diese Daten zu nutzen.
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
 <br>Löschung basierend auf einem vereinbarten Zeitplan oder Ihrer Richtlinie – Die Löschung von Daten ist ein wichtiger Aspekt des Datenschutzes und ein wichtiger Schritt in allen Data-Governance-Prozessen. [!DNL Adobe Journey Optimizer] kann mehr Daten erzeugen als erforderlich. Außerdem sollten Sie darauf achten, was nach der vorgeschriebenen Aufbewahrungsdauer für einen Datensatz geschieht – sei es aus Gründen der Nützlichkeit oder der Vorschrift. Die Kontrolle, die Sie benötigen, besteht darin, Daten zu einem beliebigen Zeitpunkt löschen zu können. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html?lang=de">Weitere Informationen zur Datenhygiene finden Sie in der Dokumentation zu Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], worauf basiert, bietet Ihnen ein höchstes Maß an Datenkontrolle – sowohl während der Interaktion als auch am Ende der Interaktion. [!DNL Adobe Journey Optimizer] Within [!DNL Journey Optimizer], haben Sie die volle Kontrolle über die Daten (die entweder in geladen oder von generiert werden). [!DNL Journey Optimizer]), überlagerte die Governance diese Daten und die Ziele, an die diese Daten gesendet werden.

Alle Daten werden als Eigentum von Kunden betrachtet und können nur auf Anfrage gepflegt, verschlüsselt, verteilt oder vernichtet werden. Adobe fungiert als Treuhänder, ohne jegliche Rechte an Ihren Daten.

Sie können die [!DNL Journey Optimizer]Flexibilität der Daten, um Ihre spezifischen Anforderungen in Bezug auf Datenaufbewahrung, -archivierung oder -löschung zu erfüllen:

* **Datenextraktion/Export**: Sie können die Extraktion von Quelldaten jederzeit über die Datenzugriffs-API ohne Strafen oder Zeitverzögerungen starten. Die [Data Access API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=de){target="_blank"} bietet Benutzern eine RESTful-Schnittstelle, die sich auf die Auffindbarkeit und Zugänglichkeit von aufgenommenen Datensätzen in [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Beachten Sie, dass in Journeys oder Kampagnen verwendete Inhalte nicht über die oben genannten API- oder Zielmethoden extrahiert werden können.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Bereinigungs- und Archivierungsmechanismen**[!DNL Adobe Journey Optimizer]: Die Bereinigung von Daten und Archivierung kann in frei definiert und automatisiert werden, um die Datenaufbewahrungsrichtlinien zu automatisieren. Es ist möglich, für die verschiedenen Datenentitäten unterschiedliche Alterungsstrategien zu definieren. Exportmechanismen können auch so definiert werden, das alternde Daten vor einer Bereinigung oder Archivierung automatisch exportiert werden.

   Der Arbeitsbereich Datenhygiene in der Adobe Experience Platform-Benutzeroberfläche ermöglicht Ihnen, verschiedene Aufgaben zur Datenhygiene zu erstellen und zu überwachen, darunter das Löschen von Verbraucheridentitäten und das Planen der Gültigkeitsdauer von Datensätzen. Dieser Arbeitsbereich ist mit Security &amp; Privacy Shield und Healthcare Shield verfügbar. Weitere Informationen finden Sie unter [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html?lang=de){target="_blank"}.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Datenextraktion bei Beendigung der Interaktion/Ausstieg**: Nach Vertragsende werden Ihre Daten vollständig aus der Datenspeicherung von Adobe entfernt. Außerdem können Sie vor Beendigung einer Vereinbarung die vollständigen Profilextrakte abrufen. Für diese Funktion fallen keine zusätzlichen Kosten an. Dies kann jederzeit und nicht nur bei Beendigung erfolgen.

Die oben genannten Methoden werden vertraglich definiert und im Datenverarbeitungsabkommen (Data Processing Agreement, DPA), das Adobe zu Beginn eines Engagements mit Ihnen abschließt, detailliert beschrieben. Adobe-Anwendungen, einschließlich [!DNL Journey Optimizer], werden nach dem Prinzip entwickelt, dass die Daten jedes Kunden als proprietäres Datenasset dieses Kunden behandelt werden.
