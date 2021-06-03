---
title: Erste Schritte mit der Konfiguration von Push-Benachrichtigungen
description: Datenfluss und Komponenten von Push-Benachrichtigungen verstehen
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Erste Schritte mit der Konfiguration von Push-Benachrichtigungen {#get-started-push}

![](assets/do-not-localize/badge.png)

Push-Benachrichtigungen dienen als schnelle Kommunikationskanäle, über die Sie Nachrichten, Angebote oder andere Informationen an Ihre Mobile-App-Benutzer übermitteln können. In der Regel muss sich der Endbenutzer für den Empfang von Push-Benachrichtigungen anmelden. -Opt-in findet in der Regel während des Installationsprozesses statt und Endbenutzer erhalten eine Möglichkeit, Benachrichtigungen zu verwalten, wenn sie später ihre Meinung ändern. Ein wichtiger Vorteil von Push-Benachrichtigungen in der Mobilgeräteverarbeitung besteht darin, dass für die Zustellung einer Nachricht keine spezifischen Anwendungen auf einem Mobilgerät erforderlich sind. Dadurch kann ein Smartphone Benachrichtigungen empfangen und anzeigen, selbst wenn der Bildschirm des Geräts gesperrt ist und sich die App im Hintergrund befindet oder geschlossen ist.

**[!DNL Adobe Journey Optimizer]**  ermöglicht den Versand zeitkritischer, relevanter und personalisierter Push-Nachrichten in großem Maßstab. Ein Segment mit Kundenprofilen kann angesprochen werden, um Rich-Push-Benachrichtigungen auf ihren iOS- und Android-Mobilgeräten zu erhalten. Diese Segmente können auf der Grundlage vergangener oder Live-Benutzererlebnisereignisse, Benutzerdatensatzdaten oder einer Kombination aus Benutzerinteraktionen und Daten erstellt werden. Sobald eine Journey live ist, können Sie detaillierte Berichte zur Anzahl der gesendeten Nachrichten, zu fehlgeschlagenen Nachrichten aus welchen Gründen und zu Push-Tracking-Informationen anzeigen, z. B. wie viele Benutzer darauf geklickt haben.

In diesem Dokument werden Sie durch einen einfachen Datenfluss von End-to-End-Push-Benachrichtigungen mit [!DNL Journey Optimizer] und einem Diagramm zum Benutzerfluss geführt, um zu erklären, wie jede Rolle ihre Aufgaben erfüllt und zusammenarbeitet, um den Push-Datenfluss zusammenzuführen.


## Beteiligte Komponenten und Dienste

* **Cloud Messaging-** Anbieter sind Drittanbieterdienste, mit denen wir Benachrichtigungen von Remote-Servern an mobile Apps senden können.

   [!DNL Adobe Journey Optimizer]  unterstützt sowohl Android- als auch iOS-Plattformen und behandelt zwei primäre Cloud-Messaging-Dienste:
   * Firebase Cloud Messaging (FCM) - zum Senden von Benachrichtigungen an eine mobile Android-App
   * Apple Push Notification Service (APNs) - zum Senden von Benachrichtigungen an eine mobile iOS-App

* **Mobile App mit Adobe Mobile** SDK integriert, wodurch mobile Apps mit Adobe Experience Cloud-Lösungen integriert werden können. Das Mobile SDK besteht aus verschiedenen Experience Cloud-Lösungserweiterungen, um Funktionen bereitzustellen, die für den von ihnen repräsentierten Dienst spezifisch sind. Diese Erweiterungen stellen verschiedene APIs bereit, um Datenflüsse zu ermöglichen, z. B. die Registrierung des Push-Tokens oder das Senden von Push-Tracking-Ereignissen oder anderen benutzerspezifischen Erlebnisereignissen an Adobe Experience Platform.

* **Adobe Launch**  (oder Datenerfassung) ist die nächste Generation von mobilen SDK-Verwaltungsfunktionen, die den Datenfluss vom Mobile SDK zu  [!DNL Adobe Experience Platform]ermöglichen. Es bietet Funktionen zum Registrieren von Erweiterungen, Erstellen von Regeln und Datenelementen, um Daten von Ihrer App an die Adobe Experience Cloud-Lösungen zu senden. In Bezug auf den Datenfluss von Push-Benachrichtigungen sind in Adobe Launch folgende Hauptkonfigurationen erforderlich:

   * Erstellen eines Datenspeichers zum Konfigurieren der Profil- und Erlebnisereignis-Datensätze, anhand derer die Daten in die Erlebnisplattform fließen.
   * Erstellen einer clientseitigen mobilen Eigenschaft und Hinzufügen von Erweiterungen. Das Mobile SDK lässt sich eng mit diesen Erweiterungen integrieren, um eine nahtlose Datenerfassung zu ermöglichen.
   * Registrieren der App-Bundle-ID und der App-Anmeldeinformationen, die dabei helfen, die Integrität der App zum Zeitpunkt der Bereitstellung der Push-Benachrichtigung eindeutig zu identifizieren und zu validieren.

* **Echtzeit-Kundenprofil** ist die Komponente in Adobe Experience Platform, mit der Sie eine ganzheitliche Sicht auf jeden einzelnen Kunden anzeigen können, indem Daten aus verschiedenen Kanälen kombiniert werden, einschließlich Web, Mobile, CRM und Drittanbieter. Mit dem Profil können Sie Ihre Kundendaten in einer einheitlichen Ansicht zusammenfassen, die eine umsetzbare, mit Zeitstempel versehene Übersicht über jede Kundeninteraktion bietet. Statische Daten, die den Benutzer der Mobile App identifizieren, z. B. ein Push-Token, werden unter dem Profil des Benutzers als Datensatzdaten gespeichert, während die Interaktionen, die der Benutzer mit Push-Benachrichtigungen ausführt, als Zeitreihenereignisdaten verfolgt werden.

* **[!DNL Adobe Journey Optimizer]** : Sobald Ihre Mobile-App-Integrationen mit den oben genannten Komponenten eingerichtet sind und Ihre Kundenprofile als Echtzeit-Kundenprofile verfügbar sind, können Sie leistungsstarke Funktionen zur Zielgruppensegmentierung in nutzen,  [!DNL Adobe Journey Optimizer]  um für jede Person ein optimales Erlebnis sicherzustellen.


## Push-Datenfluss

Dieses Diagramm zeigt einen grundlegenden Datenfluss von Push-Nachrichten und bietet einen Einblick in die verschiedenen Adoben, die am Datenfluss beteiligt sind.

![](assets/push-flow.png)


1. Der Kunde entwickelt eine mobile App unter Android oder iOS, die er für seine Benutzer freigeben würde. Um die von Push-Anbietern bereitgestellte Push-Funktion (APNS von Apple und FCM von Google) zu nutzen, registriert sich die Mobile App und aktiviert die Push-Funktion.
1. Die Push-Provider generieren und senden ein Push-Token an die mobile App. Ein Push-Token ist eine Kennung, mit der Absender bestimmte Geräte mit einer Push-Benachrichtigung ansprechen.
1. Die mobile App ist in das Adobe Mobile SDK integriert, das verschiedene Erweiterungen und APIs verfügbar macht. Die Messaging-Erweiterung stellt eine API zum Registrieren des Push-Tokens in Adobe Experience Platform anhand des Kundenprofils bereit.
1. Sobald die Mobile App fertig ist, wird sie unter **[!DNL Journey Launch]** `>` **App-Konfigurationen** sowie die Anmeldeinformationen konfiguriert.
Der Marketingexperte verfasst jetzt eine Push-Benachrichtigung in **[!DNL Adone Journey Optimizer]** `>` **Nachrichten** für die registrierte Mobile App.
1. Der Marketingexperte orchestriert eine Journey, die den Fluss von Ereignissen und Aktionen definiert. Um eine Push-Benachrichtigung in einer Phase des Journey zu senden, fügt der Marketingexperte eine Aktion vom Typ &#39;Nachricht&#39; hinzu und ordnet sie der im vorherigen Schritt erstellten Nachricht zu.
1. Wenn ein Kundenprofil berechtigt ist, die Push-Benachrichtigung aus einem beliebigen Grund, z. B. zum Trigger eines Ereignisses oder zur Segmentqualifikation, zu erhalten, wird die Nachricht gegebenenfalls entsprechend dem Profil personalisiert.
1. Die personalisierte Push-Nachricht wird zur weiteren Verarbeitung an den Push-Versand-Dienst gesendet.
1. Der Push-Versand-Dienst überprüft die Anmeldeinformationen der App, die mit der Nachricht verknüpft ist.
1. Die Nachricht wird an die Push-Provider gesendet, um sie mit dem entsprechenden Push-Token und den entsprechenden Anmeldeinformationen an die Mobile App zu senden.
1. Die Push-Provider senden ein Feedback, aus dem hervorgeht, ob die Nachricht erfolgreich an den Provider gesendet wurde oder nicht. Andernfalls ist die entsprechende Fehlermeldung Teil des Feedbacks. Dieses Feedback wird an die Adobe-Berichterstellung gesendet, damit der Kunde die Journey [Live](reports/live-report.md) und [Globale Berichte](reports/global-report.md) anzeigen kann.
1. In der Zwischenzeit übermitteln die Push-Provider die erfolgreiche Push-Benachrichtigung asynchron an die Mobile App.
1. Wenn der Kunde mit der Benachrichtigung interagiert, können die Impressionen wie Klicks/Öffnungen als **Erlebnisereignisse** verfolgt werden. Die Messaging-Erweiterung stellt APIs zum Senden von Tracking-Ereignissen an Adobe Experience Platform für das Kundenprofil bereit.

## Push-Benutzerfluss

In diesem Diagramm werden die verschiedenen Schritte zum Konfigurieren der Komponenten dargestellt, die das Skelett des Push-Datenflusses bilden. Die Aktionselemente wurden basierend auf der Rolle, die die Konfiguration durchführt, und der zu konfigurierenden Komponente kategorisiert. Wie Sie sehen können, müssen Sie vor dem Start des Versands von Push-Benachrichtigungen mit **[!DNL Adobe Journey Optimizer]** sicherstellen, dass Konfigurationen und Integrationen in der Mobile App vorhanden sind, **[!DNL Adobe Launch]** und **[!DNL Adobe Experience Platform]**.

![](assets/user-flow.png)

Detaillierte Schritte zum Konfigurieren des Push-Kanals und zum Aktivieren von Push-Benachrichtigungen in [!DNL Journey Optimizer] finden Sie auf [dieser Seite](push-configuration.md).