---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten in  [!DNL Journey Optimizer]
description: Erfahren Sie, wie Sie in  [!DNL Journey Optimizer] mit Daten arbeiten
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 100%

---

# Erste Schritte mit der Datenverwaltung in [!DNL Journey Optimizer] {#about-data}

Reichhaltigkeit und Abdeckung von Endkundendaten definieren die Stärke und den Erfolg jeder Customer Experience-Lösung. Diese Daten sind für jeden Kunden heilig und sind für ihn von höchstem Wert. Die Technologieauswahl ist jetzt von Natur aus mit einer strengen Auswertung der Datenverwaltungsfunktionen integriert.

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind.

**Meine Daten, meine Regeln** – Journey Optimizer erstellt kontinuierlich (und in Echtzeit) neben allen Journey-Daten und Angebotsdaten, die mit deren Vorgängen verbunden sind, einen umfangreichen Satz an Kundenprofildaten. Strawman-Versionen von Benutzerdaten, die aus Ihren Datenbanken erfasst werden, werden angereichert und in hochwertige Daten mit Abdeckung und Tiefe umgewandelt. Sie wollen, dass diese Daten sicher und gleichzeitig überall verfügbar sind, damit Sie deren Wert in Ihrem gesamten IT-Ökosystem nutzen können.

Im Großen und Ganzen ist die Flexibilität, die Sie von Ihren Daten erwarten, dreifacher Art:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Ziele" src="assets/do-not-localize/dest.png" /> 
 <br>Verfügbar in anderen Zielen – Während Journey Optimizer Daten für ein extrem personalisiertes Kundenerlebnis synchronisiert und integriert, wünschen Sie sich diese Daten in anderen Systemen in Ihrer gesamten Technologielandschaft, während Sie nach anderen Möglichkeiten suchen, diese Daten zu nutzen.
    <div>
     <a href="../start/ajo-integrations.md">Weitere Informationen</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="Aufbewahrung" src="assets/do-not-localize/retention.png" />  
 <br>Aufbewahrung für eine bestimmte Dauer – Branchen- oder Regionalbestimmungen (wie DSGVO oder CCPA) oder interne Data-Governance-Richtlinien legen fest, wie lange oder wie kurz die Dauer ist, Daten im Data Lake von Adobe Experience Platform aufbewahrt oder archiviert werden müssen. <a href="../privacy/get-started-privacy.md">Weitere Informationen</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="Richtlinie" src="assets/do-not-localize/policy.png" /> 
 <br>Löschung basierend auf einem vereinbarten Zeitplan oder Ihrer Richtlinie – Die Löschung von Daten ist ein wichtiger Aspekt des Datenschutzes und ein wichtiger Schritt in allen Data-Governance-Prozessen. Journey Optimizer erzeugt möglicherweise mehr Daten als erforderlich. Außerdem sollten Sie darauf achten, was nach der vorgeschriebenen Aufbewahrungsdauer für einen Datensatz geschieht – sei es aus Gründen der Nützlichkeit oder der Vorschrift. Die Kontrolle, die Sie benötigen, besteht darin, Daten zu einem beliebigen Zeitpunkt löschen zu können. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Weitere Informationen zur Datenhygiene finden Sie in der Dokumentation zu Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform, worauf Journey Optimizer basiert, bietet Ihnen ein höchstes Maß an Datenkontrolle – sowohl während der Interaktion als auch am Ende der Interaktion. Innerhalb von Journey Optimizer haben Sie die volle Kontrolle über die Daten (die entweder in Journey Optimizer eingebracht oder von Journey Optimizer generiert werden), die auf diese Daten angewendete Governance und die Ziele, an die diese Daten gesendet werden.

Alle Daten werden als Eigentum von Kunden betrachtet und können nur auf Anfrage gepflegt, verschlüsselt, verteilt oder vernichtet werden. Adobe fungiert als Treuhänder, ohne jegliche Rechte an Ihren Daten.

Sie können die Datenflexibilität von Journey Optimizer nutzen, um Ihre spezifischen Anforderungen in Bezug auf die Aufbewahrung, Archivierung oder Löschung von Daten zu erfüllen:

* **Datenextraktion/Export**: Sie können die Extraktion von Quelldaten jederzeit über die Datenzugriffs-API ohne Strafen oder Zeitverzögerungen starten. Die [Datenzugriffs-API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=de){target=&quot;_blank&quot;} bietet Benutzenden eine RESTful-Schnittstelle, die sich auf die Auffindbarkeit und Zugänglichkeit erfasster Datensätze innerhalb von Experience Platform konzentriert. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Beachten Sie, dass in Journeys oder Kampagnen verwendete Inhalte nicht über die oben genannten API- oder Zielmethoden extrahiert werden können.

* **Datenaufbewahrung durch Profile Service**: Für an ein Profil angehängte Verhaltens- und Zeitreihendaten können Sie die Standardeinstellung von Journey Optimizer verwenden, diese Daten bis zu 30 Tage lang ab dem Datum der Profileinfügung oder bis zu einem von Ihnen ausgewählten alternativen Zeitpunkt beizubehalten. Der Zeitraum, über den Adobe diese Daten speichert, ist von Vertrag zu Vertrag unterschiedlich und wird in der Richtlinie zur Datenaufbewahrung des jeweiligen Unternehmens beschrieben.

   Weitere Informationen zur Gültigkeitsdauer von Experience-Ereignissen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html?lang=de){target=&quot;_blank&quot;}.

* **Bereinigungs- und Archivierungsmechanismen**: Die Bereinigung von Daten und Archivierung kann in Journey Optimizer frei definiert und automatisiert werden, um die Datenaufbewahrungsrichtlinien zu automatisieren. Es ist möglich, für die verschiedenen Datenentitäten unterschiedliche Alterungsstrategien zu definieren. Exportmechanismen können auch so definiert werden, das alternde Daten vor einer Bereinigung oder Archivierung automatisch exportiert werden.

   Der Arbeitsbereich Datenhygiene in der Adobe Experience Platform-Benutzeroberfläche ermöglicht Ihnen, verschiedene Aufgaben zur Datenhygiene zu erstellen und zu überwachen, darunter das Löschen von Verbraucheridentitäten und das Planen der Gültigkeitsdauer von Datensätzen. Dieser Arbeitsbereich ist mit Security &amp; Privacy Shield und Healthcare Shield verfügbar. Weitere Informationen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html?lang=de){target=&quot;_blank&quot;}.

* **Data Lake und Löschungen**: Im Data Lake gespeicherte Kundendaten können von Journey Optimizer wie folgt beibehalten werden:

   * 7 Tage lang, um das Onboarding von Kundendaten in die Profil-Services zu erleichtern, wonach diese dauerhaft gelöscht werden können, oder
   * bis zur Löschung durch Sie


* **Datenextraktion bei Beendigung der Interaktion/Ausstieg**: Nach Vertragsende werden Ihre Daten vollständig aus der Datenspeicherung von Adobe entfernt. Außerdem können Sie vor Beendigung einer Vereinbarung die vollständigen Profilextrakte abrufen. Für diese Funktion fallen keine zusätzlichen Kosten an. Dies kann jederzeit und nicht nur bei Beendigung erfolgen.

Die oben genannten Methoden werden vertraglich definiert und im Datenverarbeitungsabkommen (Data Processing Agreement, DPA), das Adobe zu Beginn eines Engagements mit Ihnen abschließt, detailliert beschrieben. Adobe-Anwendungen, einschließlich Journey Optimizer, sind so konzipiert, dass die Daten jedes Kunden als proprietäres Daten-Asset dieses Kunden gehandhabt werden.
