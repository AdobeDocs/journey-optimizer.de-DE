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
source-git-commit: 34f6f25560cbe7873f8aea9edda3d63dab63935a
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Erste Schritte mit der Datenverwaltung in [!DNL Journey Optimizer] {#about-data}

Reichweite und Abdeckung von Endkundendaten definiert die Stärke und den Erfolg jeder Customer Experience-Lösung. und diese Daten sind heilig und haben den höchsten Wert für einen bestimmten Kunden. Die Technologieauswahl ist jetzt von Natur aus mit einer strengen Bewertung der Datenverwaltungsfunktionen integriert.

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologiestapels sind.

**Meine Daten, meine Regeln** - Journey Optimizer erstellt kontinuierlich (und in Echtzeit) neben allen Journey-Daten und Angebotsdaten, die mit seinen Vorgängen verbunden sind, einen umfangreichen Satz an Kundenprofildaten. Strawman-Versionen von Benutzerdaten, die aus Ihren Datenbanken erfasst werden, werden angereichert und in hochwertige Daten mit Abdeckung und Tiefe umgewandelt. Sie wollen diese Daten sicher und gleichzeitig allgegenwärtig, damit Sie ihren Wert in Ihrem gesamten IT-Ökosystem nutzen können.

Im Großen und Ganzen ist die Flexibilität, die Sie von Ihren Daten erwarten, dreimal so:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <img alt="Ziele" src="assets/do-not-localize/dest.png" />
    <br>
  </td>
  <td>
    <div>Verfügbar in anderen Zielen - Während Journey Optimizer Daten für ein überaus personalisiertes Kundenerlebnis synchronisiert und integriert, wünschen Sie sich diese Daten in anderen Systemen in Ihrer gesamten Technologielandschaft, während Sie nach anderen Möglichkeiten suchen, diese Daten zu nutzen.
    <div>
     <a href="../start/ajo-integrations.md">Weitere Informationen</a></div>
    </div>
    <br>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="Treue" src="assets/do-not-localize/retention.png" />
  </td>
  <td>
    <div>Beibehalten für eine bestimmte Dauer - Branchen- oder Regionalbestimmungen (wie DSGVO oder CCPA) oder interne Data Governance-Richtlinien legen fest, wie lange oder wie kurz die Dauer ist, Daten im Adobe Experience Platform Data Lake aufbewahrt oder archiviert werden müssen. <a href="../privacy/get-started-privacy.md">Weitere Informationen</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="policy" src="assets/do-not-localize/policy.png" />
    <br>
  </td>
  <td>
    <div>Gelöschte Basis eines vereinbarten Zeitplans für Ihre Richtlinie - Die Löschung von Daten ist ein wichtiger Aspekt des Datenschutzes und ein wichtiger Schritt in allen Data Governance-Prozessen. Journey Optimizer erzeugt möglicherweise mehr Daten als erforderlich. Außerdem sollten Sie darauf achten, was nach der erforderlichen Dauer für einen Datensatz geschieht - sei es aus Gründen der Nützlichkeit oder der Regulierung. Das benötigte Steuerelement besteht darin, Daten jederzeit zu löschen.</div>
  </td>
</tr>
</table>

Adobe Experience Platform, auf dem Journey Optimizer basiert, bietet Ihnen die höchste Datenkontrolle - während der Interaktion und am Ende der Interaktion. Innerhalb von Journey Optimizer haben Sie die vollständige Kontrolle über die Daten (die entweder in Journey Optimizer übertragen oder von generiert werden), die Governance hat sich auf diese Daten und die Ziele, an die diese Daten gesendet werden, überlagert.

Alle Daten werden als Eigentum von Customers betrachtet und können nur auf Anfrage gepflegt, verschlüsselt, verteilt oder zerstört werden. Adobe fungiert als Treuhänder, ohne jegliche Rechte an Ihren Daten.

Sie können die Datenflexibilität von Journey Optimizer nutzen, um Ihre spezifischen Anforderungen in Bezug auf die Datenaufbewahrung, -archivierung oder -löschung zu erfüllen:

* **Datenextraktion/Export**: Sie können die Extraktion von Quelldaten jederzeit über die Data Access API ohne Strafen oder Zeitverzögerungen starten. Die [Data Access API](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) bietet Benutzern eine RESTful-Schnittstelle, die sich auf die Auffindbarkeit und Zugänglichkeit erfasster Datensätze innerhalb der Experience Platform konzentriert. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Beachten Sie, dass in Journey oder Kampagnen verwendete Inhalte nicht über die oben genannten API- oder Zielmethoden extrahiert werden können.

* **Datenaufbewahrung für den Profildienst**: Für an ein Profil angehängte Verhaltens- und Zeitreihendaten können Sie die Standardeinstellung von Journey Optimizer verwenden, diese Daten bis zu 30 Tage lang ab dem Datum der Profileinfügung oder bis zu einem von Ihnen ausgewählten alternativen Zeitraum beizubehalten. Der Zeitpunkt, zu dem die Adobe diese Daten speichert, variiert von Vertrag zu Vertrag und wird in der Datenaufbewahrungsrichtlinie eines Unternehmens beschrieben.

* **Bereinigungs- und Archivierungsmechanismen**: Die Bereinigung von Daten und Archivierung kann in Journey Optimizer frei definiert und automatisiert werden, um die Datenaufbewahrungsrichtlinien zu automatisieren. Es ist möglich, für die verschiedenen Datenentitäten unterschiedliche Alterungsstrategien zu definieren. Exportmechanismen können auch so definiert werden, dass Alterungsdaten vor der Bereinigung oder Archivierung automatisch exportiert werden.

* **Data Lake und Löschungen**: Im Data Lake gespeicherte Kundendaten können von Journey Optimizer beibehalten werden:

   * 7 Tage lang, um das Onboarding von Kundendaten in die Profildienste zu erleichtern, nach denen diese dauerhaft gelöscht werden können, oder
   * bis Sie ausgewählt haben, gelöscht zu werden

* **Datenextraktion bei Beendigung der Interaktion/Ausstieg**: Nach Vertragsende werden Ihre Daten vollständig aus dem Speicher der Adobe entfernt. Außerdem können Sie vor Beendigung einer Vereinbarung die vollständigen Profilextrakte abrufen. Für diese Funktion fallen keine zusätzlichen Kosten an. Dies kann jederzeit und nicht nur nach Beendigung erfolgen.

Die oben genannten Methoden werden vertraglich definiert und im Datenverarbeitungsabkommen (Data Processing Agreement, DPA) detailliert beschrieben, dass die Adobe zu Beginn einer Interaktion mit Ihnen einverstanden ist. Adobe Apps, einschließlich Journey Optimizer, basieren auf dem Prinzip, dass die Daten jedes Kunden als proprietäres Datenasset dieses Kunden behandelt werden.
