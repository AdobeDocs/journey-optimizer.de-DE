---
solution: Journey Optimizer
product: journey optimizer
title: Mobile und Web einrichten
description: Erfahren Sie, wie Sie mobile und Web-Kanäle konfigurieren und überwachen.
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Kanal, Oberfläche, technisch, Parameter, Optimizer
hide: true
hidefromtoc: true
source-git-commit: 4a089308cfc2fa90cc4c0a6baa15a89598e8edd6
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 25%

---

# Erste Schritte mit der Einrichtung von geführten Kanälen {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Name der Web- und Mobilgeräte-Konfiguration"
>abstract="Geben Sie den Namen Ihrer Mobile- oder Web-Konfiguration ein. Dieser Name wird für jede Ressource verwendet, die automatisch mit der Konfiguration des geführten Kanals erstellt wird."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Mit Assurance validieren"
>abstract="Adobe Experience Platform Assurance ist in diesen Workflow eingebettet, damit Sie Ihre SDK-Implementierung überprüfen und Anwendungsereignisse simulieren und überprüfen können."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Überblick über die Adobe Experience Platform-Assetbildung"


Diese Einrichtung erleichtert die schnelle Konfiguration von Marketing-Kanälen, sodass alle erforderlichen Ressourcen in Experience Platform, Journey Optimizer und der Datenerfassung sofort verfügbar sind. Dadurch kann Ihr Marketing-Team sofort mit der Erstellung von Kampagnen und Journeys beginnen.

Um dies effektiv zu implementieren, ist es wichtig, dass ein Mitglied der Organisation mit der Befugnis und technischen Fähigkeit, Website- oder Mobilcode zu ändern, die Einrichtung überwacht.

Im Folgenden finden Sie die Berechtigungen, die zum Ausführen der Einrichtung des geführten Kanals erforderlich sind.

+++ Erforderliche Berechtigungen

<table>
  <thead>
    <tr>
      <th><strong>Lösung</strong></th>
      <th><strong>Berechtigungen</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p>Datenerfassung</p>
      </td>
      <td>
        <ul>
          <li>Unternehmensrechte &gt; Eigenschaften</li>
          <li>Eigenschaftsrechte: Entwickeln, Veröffentlichen, Verwalten von Erweiterungen und Umgebungen</li>
          <li>App-Oberflächen: App-Konfiguration verwalten</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <p>Adobe Experience Platform</p>
      </td>
      <td>
        <ul>
          <li>Datenerfassung: Verwalten von Datenspeichern</li>
          <li>Sandbox: Zugriff auf Sandboxes gewähren</li>
          <li>Segmente verwalten: Segmentdefinitionen lesen, erstellen, bearbeiten und löschen</li>
          <li>Profile verwalten: Profile lesen, erstellen, bearbeiten und löschen</li>
          <li>Datensätze lesen: schreibgeschützter Zugriff auf Datensätze</li>
          <li>Schemas lesen: schreibgeschützter Zugriff auf Schemas</li>
          <li>Identitäts-Namespace lesen: schreibgeschützter Zugriff auf Identitäts-Namespace</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <p>Adobe Journey Optimizer</p>
      </td>
      <td>
        <p>Kampagnen: Kampagnen verwalten und veröffentlichen</p>
      </td>
    </tr>
  </tbody>
</table>
+++

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="set-mobile-android.md">
<img alt="Lead" src="assets/do-not-localize/config-android.jpeg">
</a>
<div><a href="set-mobile-android.md"><strong>Einrichten der mobilen Android-Konfiguration</strong>
</div>
<p>
</td>
<td>
<a href="set-mobile-ios.md">
<img alt="Gelegentlich" src="assets/do-not-localize/config-ios.jpeg">
</a>
<div>
<a href="set-mobile-ios.md"><strong>Einrichten der mobilen iOS-Konfiguration</strong></a>
</div>
<p></td>
<td>
<a href="set-mobile-web.md">
<img alt="Validierung" src="assets/do-not-localize/config-web.jpeg">
</a>
<div>
<a href="set-mobile-web.md"><strong>Web-Konfiguration einrichten</strong></a>
</div>
<p>
</td>
</tr></table>
