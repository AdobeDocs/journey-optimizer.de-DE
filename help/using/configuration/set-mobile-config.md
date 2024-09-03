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
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 17%

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

Diese Einrichtung erleichtert die schnelle Konfiguration von Marketing-Kanälen, sodass alle erforderlichen Ressourcen in Experience Platform, Journey Optimizer und der Datenerfassung sofort verfügbar sind. Dadurch kann Ihr Marketingteam mit der Erstellung von Kampagnen und Journey beginnen.

Die Einrichtung des Guided Channel unterstützt die folgenden Plattformen und Kanäle.

* Plattformen und SDK:

   * Swift by Apple, iOS

   * Kotlin, Android

   * JavaScript, Web

* Kanäle:

   * Mobile In-App

   * Mobile Push-Nachricht

   * Web Basic


Beachten Sie, dass für jede Plattform, die Sie einrichten möchten, eine separate Konfiguration erstellt werden muss. Dies liegt daran, dass jede App eine eindeutige Kanalkonfiguration erfordert und so flexibel festgelegt werden kann, welche Kanäle Sie für jede Plattform wünschen.

## Voraussetzungen {#prereq}

* Um dies effektiv zu implementieren, ist es wichtig, dass ein Mitglied der Organisation mit der Befugnis und technischen Fähigkeit, Website- oder Mobilcode zu ändern, die Einrichtung überwacht.

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

* Wenn Sie die Option Vorhandene Konfiguration verwenden, stellen Sie sicher, dass Sie die folgenden Adobe Experience Platform Mobile SDK-Erweiterungsversionen verwenden. Weitere Informationen zum SDK-Setup, einschließlich der erforderlichen Abhängigkeiten und des Initialisierungscodes, finden Sie in der [folgenden Dokumentation](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en).

  Für Android

   * Mobile Core v3.1.0 oder höher
   * Adobe Journey Optimizer v3.1.0 oder höher

  Für iOS

   * Mobile Core v5.2.0 oder höher
   * Adobe Journey Optimizer v5.1.1 oder höher

## Automatisch erstellte Ressourcen {#auto-create-resources}

Die Einrichtung geführter Kanäle vereinfacht die schnelle Konfiguration von Marketingkanälen, sodass alle wichtigen Ressourcen in den Experience Platform-, Journey Optimizer- und Datenerfassungs-Apps verfügbar sind. Dadurch kann Ihr Marketing-Team schnell mit der Erstellung von Kampagnen und Journey beginnen. Im Folgenden finden Sie eine Liste der Ressourcen, die im Rahmen der Einrichtung des geführten Kanals automatisch generiert und konfiguriert werden.

Durchsuchen Sie die folgenden Registerkarten, um auf die umfassenden Listen aller automatisch generierten Ressourcen zuzugreifen:

>[!BEGINTABS]

>[!TAB iOS]

Für die **Erstkonfiguration** ist unten eine umfassende Liste aller Ressourcen, die auf dem Bildschirm **Konfigurationsdetails** erstellt wurden, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

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
  <li>Einverständnis (mit aktivierten standardmäßigen Zustimmungsrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Stitching-Regeln)</li>
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
  <p>Datenspeicher mit Diensten</p>
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

Für das **Kanal-Setup** ist unten eine umfassende Liste aller Ressourcen, die auf dem Bildschirm **Kanäle hinzufügen** erstellt wurden.

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
  <li>Push-Anmeldedaten hochladen (nur mobile Push-Nachrichten)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Für die **Erstkonfiguration** ist unten eine umfassende Liste aller Ressourcen, die auf dem Bildschirm **Konfigurationsdetails** erstellt wurden, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

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
  <li>Einverständnis (mit aktivierten standardmäßigen Zustimmungsrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Stitching-Regeln)</li>
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
  <p>Datenspeicher mit Diensten</p>
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

Für das **Kanal-Setup** ist unten eine umfassende Liste aller Ressourcen, die auf dem Bildschirm **Kanäle hinzufügen** erstellt wurden.

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
  <li>Push-Anmeldedaten hochladen (nur mobile Push-Nachrichten)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Für die **Erstkonfiguration** ist unten eine umfassende Liste aller Ressourcen, die auf dem Bildschirm **Konfigurationsdetails** erstellt wurden, wenn Sie auf **Ressourcen automatisch erstellen** klicken.

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
  <li>Einverständnis (mit aktivierten standardmäßigen Zustimmungsrichtlinien)</li>
  <li>Identität (mit Standard-ECID, mit standardmäßigen Stitching-Regeln)</li>
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
  <p>Datenspeicher mit Diensten</p>
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

