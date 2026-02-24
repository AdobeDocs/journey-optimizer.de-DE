---
solution: Journey Optimizer
product: journey optimizer
title: Einrichten von Mobile und Web
description: Erfahren Sie, wie Sie Mobile- und Web-Kanäle konfigurieren und überwachen.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: Kanal, Oberfläche, technisch, Parameter, Optimizer
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: d793d9eccde3b0b548e778040bdcd8817e80c90a
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 85%

---

# Erste Schritte mit der Anleitung zur Kanaleinrichtung {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Name der Web- und Mobilgeräte-Konfiguration"
>abstract="Geben Sie den Namen Ihrer Mobile- oder Web-Konfiguration ein. Dieser Name wird für jede Ressource verwendet, die automatisch mit der Anleitung zur Kanaleinrichtung erstellt wird."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Mit Assurance validieren"
>abstract="Adobe Experience Platform Assurance ist in diesen Workflow eingebettet, damit Sie Ihre SDK-Implementierung überprüfen und Anwendungsereignisse simulieren und validieren können."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/assurance/home" text="Überblick über Adobe Experience Platform Assurance"

**Geführte Kanaleinrichtung** ist ein optimierter Workflow in Adobe Journey Optimizer, mit dem Sie Mobile- und Web-Marketing-Kanäle schnell konfigurieren können. Sie befindet sich unter **Administration** > **Kanäle** > **Kanalkonfiguration** und automatisiert die Erstellung wesentlicher Ressourcen wie Tag-Eigenschaften, Datenströme und Kanalkonfigurationen in Adobe Experience Platform, Journey Optimizer und der Datenerfassung. Anstatt jede Komponente manuell zu konfigurieren, folgen Sie einem geführten Fluss, der alles für Sie einrichtet, damit Ihr Marketing-Team sofort mit der Erstellung von In-App-Nachrichten, Push-Benachrichtigungen und Web-Erlebnissen beginnen kann.

Die Einrichtung geführter Kanäle unterstützt die folgenden Plattformen und Kanäle.

>[!BEGINTABS]

>[!TAB iOS]

**SDK:** Swift von Apple

**Kanäle:** Mobile In-App-, Mobile-Push-Nachricht

>[!TAB Android]

**SDK:** Kotlin

**Kanäle:** Mobile In-App-, Mobile-Push-Nachricht

>[!TAB Web]

**SDK:** JavaScript

**Kanäle:** Web Basic

>[!ENDTABS]

Beachten Sie, dass für jede Plattform, die Sie einrichten möchten, eine separate Konfiguration erstellt werden muss. Dies liegt daran, dass jede App eine eindeutige Kanalkonfiguration erfordert. So können Sie flexibel festlegen, welche Kanäle Sie für jede Plattform wünschen.

## Voraussetzungen {#prereq}

* Für eine effektive Implementierung ist es wichtig, dass ein Mitglied der Organisation mit der Befugnis und den technischen Fertigkeiten zum Ändern von Website- oder Mobile Code das Setup überwacht.

  Im Folgenden finden Sie die Berechtigungen, die zum Ausführen der Anleitung zur Kanaleinrichtung erforderlich sind.

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
            <li>„Unternehmensrechte“ &gt; „Eigenschaften“</li>
            <li>Eigentumsrechte: Entwickeln, Veröffentlichen, Verwalten von Erweiterungen und Umgebungen</li>
            <li>App-Oberflächen: Verwalten der App-Konfiguration</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>Datenerfassung: Verwalten von Datenströmen</li>
           <li>Sandbox: Gewähren des Zugriffs auf Sandboxes</li>
            <li>Segmente verwalten: Lesen, Erstellen, Bearbeiten und Löschen von Segmenten</li>
            <li>Profile verwalten: Lesen, Erstellen, Bearbeiten und Löschen von Profilen</li>
            <li>Datensätze Lesen: Nur-Lese-Zugriff auf Datensätze</li>
            <li>Schemata lesen: Nur-Lese-Zugriff auf Schemata</li>
            <li>Identity-Namespace lesen: Nur-Lese-Zugriff auf Identity-Namespace</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>Kampagnen: Verwalten und Veröffentlichen von Kampagnen</p>
        </td>
      </tr>
    </tbody>
  </table>

  +++

* Wenn Sie die Option „Vorhandene Konfiguration“ verwenden, stellen Sie sicher, dass Sie die folgenden Adobe Experience Platform Mobile SDK-Erweiterungsversionen verwenden. Weitere Informationen zum SDK-Setup, einschließlich der erforderlichen Abhängigkeiten und des Initialisierungs-Codes, finden Sie in der [folgenden Dokumentation](https://experienceleague.adobe.com/de/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks).

  Für Android

   * Mobile Core v3.1.0 oder höher
   * Adobe Journey Optimizer v3.1.0 oder höher

  Für iOS

   * Mobile Core v5.2.0 oder höher
   * Adobe Journey Optimizer v5.1.1 oder höher

## Automatisch erstellte Ressourcen {#auto-create-resources}

Die Anleitung zur Kanaleinrichtung vereinfacht die schnelle Konfiguration von Marketing-Kanälen, sodass alle wichtigen Ressourcen in den Apps Experience Platform, Journey Optimizer und Datenerfassung verfügbar sind. Dadurch kann Ihr Marketing-Team schnell mit der Erstellung von Kampagnen und Journeys beginnen. Nachfolgend finden Sie eine Liste der Ressourcen, die im Rahmen der Anleitung zur Kanaleinrichtung automatisch generiert und konfiguriert werden.

Durchsuchen Sie die folgenden Registerkarten, um auf die umfassenden Listen aller automatisch generierten Ressourcen zuzugreifen:

>[!BEGINTABS]

>[!TAB iOS]

Für die **Erstkonfiguration** finden Sie unten auf dem Bildschirm **Konfigurationsdetails** eine umfassende Liste aller erstellten Ressourcen, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

<table>
  <thead>
  <tr>
  <th><strong>Lösung</strong></th>
  <th><strong>Automatisch erstellte Ressourcen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Mobile Tag-Eigenschaft</li>
  <li>Regeln</li>
  <li>Datenelemente</li>
  <li>Bibliothek</li>
  <li>Umgebungen (Staging, Produktion, Entwicklung)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Tag-Erweiterungen</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP-Sicherheit</li>
  <li>Einverständnis (mit aktivierten standardmäßigen Einverständnisrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Zuordnungsregeln)</li>
  <li>Core für Mobilgeräte</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-Sitzung</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Datenströme</p>
  </td>
  <td>
  <p>Datenstrom mit Diensten</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Datensatz</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Für die **Kanaleinrichtung** finden Sie unten auf dem Bildschirm **Kanäle hinzufügen** eine umfassende Liste aller erstellten Ressourcen.

<table>
  <thead>
  <tr>
  <th><strong>Lösung</strong></th>
  <th><strong>Automatisch erstellte Ressourcen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Kanalkonfiguration</li>
  <li>Hochladen von Push-Anmeldedaten (nur Push-Nachrichten für Mobilgeräte)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Für die **Erstkonfiguration** finden Sie unten auf dem Bildschirm **Konfigurationsdetails** eine umfassende Liste aller erstellten Ressourcen, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

<table>
  <thead>
  <tr>
  <th><strong>Lösung</strong></th>
  <th><strong>Automatisch erstellte Ressourcen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Mobile Tag-Eigenschaft</li>
  <li>Regeln</li>
  <li>Datenelemente</li>
  <li>Bibliothek</li>
  <li>Umgebungen (Staging, Produktion, Entwicklung)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Tag-Erweiterungen</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP-Sicherheit</li>
  <li>Einverständnis (mit aktivierten standardmäßigen Einverständnisrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Zuordnungsregeln)</li>
  <li>Core für Mobilgeräte</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-Sitzung</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Datenströme</p>
  </td>
  <td>
  <p>Datenstrom mit Diensten</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Datensatz</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Für die **Kanaleinrichtung** finden Sie unten auf dem Bildschirm **Kanäle hinzufügen** eine umfassende Liste aller erstellten Ressourcen.

<table>
  <thead>
  <tr>
  <th><strong>Lösung</strong></th>
  <th><strong>Automatisch erstellte Ressourcen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Kanalkonfiguration</li>
  <li>Hochladen von Push-Anmeldedaten (nur Push-Nachrichten für Mobilgeräte)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Für die **Erstkonfiguration** finden Sie unten auf dem Bildschirm **Konfigurationsdetails** eine umfassende Liste aller erstellten Ressourcen, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

<table>
  <thead>
  <tr>
  <th><strong>Lösung</strong></th>
  <th><strong>Automatisch erstellte Ressourcen</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tags</p>
  </td>
  <td>
  <ul>
  <li>Mobile Tag-Eigenschaft</li>
  <li>Regeln</li>
  <li>Datenelemente</li>
  <li>Bibliothek</li>
  <li>Umgebungen (Staging, Produktion, Entwicklung)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Tag-Erweiterungen</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP-Sicherheit</li>
  <li>Einverständnis (mit aktivierten standardmäßigen Einverständnisrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Zuordnungsregeln)</li>
  <li>Core für Mobilgeräte</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Assurance-Sitzung</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Datenströme</p>
  </td>
  <td>
  <p>Datenstrom mit Diensten</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Datensatz</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

