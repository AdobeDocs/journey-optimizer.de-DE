---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Daten in [!DNL Journey Optimizer]
description: Erfahren Sie, wie Sie mit Daten in [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Erste Schritte mit der Datenverwaltung in [!DNL Journey Optimizer] {#about-data}

Reichweite und Abdeckung von Endkundendaten definiert die Stärke und den Erfolg jeder Customer Experience-Lösung. und diese Daten sind heilig und haben den höchsten Wert für einen bestimmten Kunden. Die Technologieauswahl ist jetzt von Natur aus mit einer strengen Bewertung der Datenverwaltungsfunktionen integriert.

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind.

**Meine Daten, meine Regeln** - Journey Optimizer erstellt kontinuierlich (und in Echtzeit) einen umfangreichen Satz von Kundenprofildaten zusätzlich zu allen Journey-Daten und Angebotsdaten, die mit seinen Vorgängen verbunden sind. Strawman-Versionen von Benutzerdaten, die aus Ihren Datenbanken erfasst werden, werden angereichert und in hochwertige Daten mit Abdeckung und Tiefe umgewandelt. Sie wollen diese Daten sicher und gleichzeitig allgegenwärtig, damit Sie ihren Wert in Ihrem gesamten IT-Ökosystem nutzen können.

Im Großen und Ganzen ist die Flexibilität, die Sie von Ihren Daten erwarten, dreimal so:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Ziele" src="assets/do-not-localize/dest.png" /> 
    <br>Verfügbar in anderen Zielen - Während Journey Optimizer Daten für ein überaus personalisiertes Kundenerlebnis synchronisiert und integriert, wünschen Sie sich diese Daten in anderen Systemen in Ihrer gesamten Technologielandschaft, während Sie nach anderen Möglichkeiten zur Nutzung dieser Daten suchen.
    <div>
     <a href="../start/ajo-integrations.md">Weitere Infos</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="Treue" src="assets/do-not-localize/retention.png" />  
    <br>Wird für eine bestimmte Dauer beibehalten - Branchen- oder regionale Regelungen (wie DSGVO oder CCPA) oder interne Richtlinien zur Data Governance legen fest, wie lange oder wie kurz eine Dauer sein muss, Daten im Adobe Experience Platform Data Lake aufbewahrt oder archiviert werden müssen. <a href="../privacy/get-started-privacy.md">Weitere Infos</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="policy" src="assets/do-not-localize/policy.png" /> 
    <br>Gelöschte Basis eines vereinbarten Zeitplans für Ihre Richtlinie - Die Löschung von Daten ist ein wichtiger Aspekt des Datenschutzes und ein wichtiger Schritt in allen Data Governance-Prozessen. Journey Optimizer kann mehr Daten als erforderlich produzieren. Außerdem sollten Sie darauf achten, was nach der erforderlichen Dauer für einen Datensatz geschieht - sei es aus Gründen der Nützlichkeit oder der Regulierung. Das benötigte Steuerelement besteht darin, Daten jederzeit zu löschen. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Weitere Informationen zur Datenhygiene finden Sie in der Dokumentation zu Adobe Experience Platform .</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform, auf der Journey Optimizer basiert, bietet Ihnen die höchste Datenkontrolle - während der Interaktion und am Ende der Interaktion. In Journey Optimizer haben Sie die vollständige Kontrolle über die Daten (die entweder in Journey Optimizer integriert oder von Journey Optimizer generiert werden), die Governance hat sich auf diese Daten und die Ziele, an die diese Daten gesendet werden, überlagert.

Alle Daten werden als Eigentum von Customers betrachtet und können nur auf Anfrage gepflegt, verschlüsselt, verteilt oder zerstört werden. Adobe fungiert als Treuhänder und hat absolut keine Rechte an Ihren Daten.

Sie können die Datenflexibilität von Journey Optimizer nutzen, um Ihre spezifischen Anforderungen im Zusammenhang mit der Datenaufbewahrung, -archivierung oder -löschung zu erfüllen:

* **Datenextraktion/Export**: Sie können die Extraktion von Quelldaten jederzeit über die Data Access API ohne Strafen oder Zeitverzögerungen starten. Die [Data Access API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} bietet Benutzern eine RESTful-Schnittstelle, die sich auf die Auffindbarkeit und Zugänglichkeit erfasster Datensätze innerhalb der Experience Platform konzentriert. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Beachten Sie, dass in Journeys oder Kampagnen verwendete Inhalte nicht über die oben genannten API- oder Zielmethoden extrahiert werden können.

* **Datenaufbewahrung für den Profildienst**: Für an ein Profil angehängte Verhaltens- und Zeitreihendaten können Sie die Standardeinstellung von Journey Optimizer verwenden, diese Daten bis zu 30 Tage lang ab dem Datum der Hinzufügung eines Profils oder bis zu einem von Ihnen ausgewählten alternativen Zeitraum beizubehalten. Der Zeitpunkt, zu dem Adobe diese Daten speichert, variiert von Vertrag zu Vertrag und wird in der Datenaufbewahrungsrichtlinie eines Unternehmens beschrieben.

   Erfahren Sie mehr über die Ablauf von Erlebnisereignissen in [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}.

* **Bereinigungs- und Archivierungsmechanismen**: Die Bereinigung von Daten und Archivierung kann in Journey Optimizer frei definiert und automatisiert werden, um Richtlinien zur Datenaufbewahrung zu automatisieren. Es ist möglich, für die verschiedenen Datenentitäten unterschiedliche Alterungsstrategien zu definieren. Exportmechanismen können auch so definiert werden, dass Alterungsdaten vor der Bereinigung oder Archivierung automatisch exportiert werden.

   Der Arbeitsbereich &quot;Datenhygiene&quot;in der Benutzeroberfläche von Adobe Experience Platform ermöglicht Ihnen die Erstellung und Überwachung verschiedener Datenhygiene-Aufgaben, einschließlich des Löschens von Kundenidentitäten und der Planung von Datensatzabläufen. Dieser Arbeitsbereich ist mit dem Sicherheits- und Datenschutzschild und dem Gesundheitsschild verfügbar. Weitere Informationen finden Sie unter [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

* **Data Lake und Löschungen**: Im Data Lake gespeicherte Kundendaten können von Journey Optimizer beibehalten werden:

   * 7 Tage lang, um das Onboarding von Kundendaten in die Profildienste zu erleichtern, nach denen diese dauerhaft gelöscht werden können, oder
   * bis Sie ausgewählt haben, gelöscht zu werden


* **Datenextraktion bei Beendigung der Interaktion/Ausstieg**: Wenn der Vertrag gekündigt wird, werden Ihre Daten vollständig aus dem Speicher von Adobe entfernt. Außerdem können Sie vor Beendigung einer Vereinbarung die vollständigen Profilextrakte abrufen. Für diese Funktion fallen keine zusätzlichen Kosten an. Dies kann jederzeit und nicht nur nach Beendigung erfolgen.

Die oben genannten Methoden sind vertraglich definiert und im Datenverarbeitungsabkommen (Data Processing Agreement, DPA) ausführlich beschrieben, dass Adobe zu Beginn einer Interaktion mit Ihnen einverstanden ist. Adobe-Anwendungen, einschließlich Journey Optimizer, basieren auf dem Prinzip, dass die Daten jedes Kunden als proprietäres Datenasset dieses Kunden behandelt werden.
