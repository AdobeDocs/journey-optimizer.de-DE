---
solution: Journey Optimizer
product: journey optimizer
title: Beheben von Fehlern in einer Journey
description: Informationen zur Fehlerbehebung beim Journey
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Problembehebung, Fehlerbehebung, Journey, Überprüfen, Fehler
source-git-commit: fa53fbe84a0d9c20a47e3d9f312b1673ab0611ca
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 11%

---

# Fehlerbehebung bei Journey {#troubleshooting}

Wenn sich eine Kunden-Journey nicht wie erwartet verhält, kann es schwierig sein, die Grundursache zu ermitteln. Damit Sie Probleme effizient beheben können, finden Sie im Folgenden Ressourcen zur Fehlerbehebung nach den häufigsten Problembereichen. Unabhängig davon, ob Sie Journey-Fehler, Ausführungsinkonsistenzen oder Probleme auf Aktionsebene sehen, bietet jeder Abschnitt eine gezielte Anleitung zur Untersuchung und Lösung dieser Probleme.

Auf den folgenden Seiten erfahren Sie mehr über bestimmte Fehlerbehebungsthemen:



<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="../building-journeys/troubleshooting.md"><img src="../assets/do-not-localize/troubleshooting.jpeg"></a>
    <div><strong>Beheben von Journey-Fehlern</strong><br/> Erfahren Sie, wie Sie Aktivitäts- oder Journey-Fehler vor dem Testen oder der Veröffentlichung identifizieren und beheben und wie Sie eine Ausweichaktion definieren, wenn bei Journey-Aktivitäten ein Fehler auftritt.</div>
    </td>
    <td>
    <a href="../building-journeys/troubleshooting-execution.md"><img src="../assets/do-not-localize/ao-audiences.jpeg"></a>
    <div><strong>Fehlerbehebung bei der Journey-</strong><br/>: Informationen zur Fehlerbehebung bei Journey-Ereignissen, zur Überprüfung, ob Profile auf Ihre Journey gelangt sind, wie sie darin navigieren und ob Nachrichten gesendet werden.</div>
    </td>
    <td>
    <a href="./building-journeys/troubleshooting-inbound.md" "><img src="../assets/do-not-localize/in-app.jpg"></a>
    <div><strong>Fehlerbehebung bei eingehenden Aktionen</strong><br/> Erfahren Sie, wie Sie Probleme im Zusammenhang mit eingehenden Aktionen auf einer Journey debuggen können, um sie selbst zu identifizieren und zu beheben.</div>
    </td>
    <td>
    <a href="../action/troubleshoot-custom-action.md"><img src="../assets/do-not-localize/lp-list.jpg"></a>
    <div><strong>Fehlerbehebung bei benutzerdefinierten Aktionen</strong><br/> Erfahren Sie, wie Sie Ihre benutzerdefinierten Aktionen testen können, indem Sie API-Aufrufe aus dem Abschnitt Administration der Journey Optimizer-Benutzeroberfläche senden. Mit dieser Funktion können Sie Fehler bei benutzerdefinierten Aktionen beheben, bevor oder nachdem diese in einer Journey verwendet werden.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="../building-journeys/troubleshooting.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="../building-journeys/troubleshooting-execution.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="./building-journeys/troubleshooting-inbound.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="../action/troubleshoot-custom-action.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

<!--

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="Troubleshoot journey errors" src="../assets/do-not-localize/troubleshooting.jpeg" /> 
    <br><ul><li><a href="../building-journeys/troubleshooting.md">Troubleshoot journey errors</a> - Learn how to identify and resolve activity or journey errors before test or publication, and how to define a fallback action in case of an error in journey activities.</li>
    <li><a href="../building-journeys/troubleshooting-execution.md">Troubleshoot journey execution</a> - Understand how to troubleshoot journey events, check if profiles entered your journey, how they navigate through it, and if messsages are sent.</li>
     <li><a href="../building-journeys/troubleshooting-inbound.md">Troubleshoot inbound actions</a> - Learn how to debug issues related to inbound actions in a journey, in order to help you identify and resolve them on your own.</li>
     <li><a href="../action/troubleshoot-custom-action.md">Troubleshoot a custom action</a> - Learn how to test your custom actions by sending API calls from the administration section of Journey Optimizer user interface. This capability helps you troubleshoot your custom actions before or after using them in a journey.</li>
    <ul>
    <div>
     <a href="../integrations/ajo-integrations.md">Learn more</a></div>
    </div>
    <br>
  </td>
</tr>
</table>
-->

<!--
* **[Troubleshoot journey errors](../building-journeys/troubleshooting.md)**
  Learn how to identify and resolve activity or journey errors before test or publication, and how to define a fallback action in case of an error in journey activities.

* **[Troubleshoot journey execution](../building-journeys/troubleshooting-execution.md)**
  Understand how to troubleshoot journey events, check if profiles entered your journey, how they navigate through it, and if messsages are sent.

* **[Troubleshoot inbound actions](../building-journeys/troubleshooting-inbound.md)**
  Learn how to debug issues related to inbound actions in a journey, in order to help you identify and resolve them on your own.

* **[Troubleshoot a custom action](../action/troubleshoot-custom-action.md)**
  Learn how to test your custom actions by sending API calls from the administration section of Journey Optimizer user interface. This capability helps you troubleshoot your custom actions before or after using them in a journey.

-->



<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div>
    <a href="https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884">
    <img alt="Grundlegendes zu häufigen Fehlercodes" src="../assets/do-not-localize/icon-quick-start.svg" /></a> 
    <br>Darüber hinaus finden Sie in diesem Blogpost der Adobe-Community Details <strong>allgemeine </strong>) und wie Sie diese effektiv beheben können.
    </div>
      <div>
     <a href="https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884" target="_blank">Weitere Informationen</a></div>
    </div>
  </td>
</tr>
</table>


