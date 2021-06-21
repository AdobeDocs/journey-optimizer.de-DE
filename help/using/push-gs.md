---
title: Erste Schritte mit der Konfiguration von Push-Benachrichtigungen
description: Datenfluss und Komponenten von Push-Benachrichtigungen verstehen
feature: Anwendungskonfiguration
topic: Push-Benachrichtigung
role: Administrator
level: Intermediate
source-git-commit: 9872df0ac91fff249a7b41ecd99b7c25c25463a9
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 3%

---

# Erste Schritte mit der Konfiguration von Push-Benachrichtigungen {#get-started-push}

Push-Benachrichtigungen helfen Ihnen, Ihre Mobile-App-Benutzer jederzeit zu erreichen - insbesondere dann, wenn sie Ihre App nicht aktiv verwenden. Push-Benachrichtigungen können Ihnen dabei helfen, eine Vielzahl von Anwendungsfällen zu erreichen, z. B. die Bereitstellung von Aktualisierungen zu Ihrem Dienst, die Aufforderung eines Benutzers, Maßnahmen zu ergreifen, den Benutzer auf ein neues Geschäft aufmerksam zu machen usw. Geräteplattformen erfordern eine Anmeldung, bevor Endbenutzer Ihre Benachrichtigungen empfangen oder anzeigen können. Die Anmeldung für den Benutzer kann so früh erfolgen, nachdem die App zum ersten Mal nach der Installation oder in einer nachfolgenden Sitzung oder einem entsprechenden Workflow gestartet wurde. [!DNL Journey Optimizer] unterstützt Push-Benachrichtigungen und unterstützt Sie beim Senden hochrelevanter Benachrichtigungen mit branchenführenden Durchsatzraten. Push-Benachrichtigungen können Personalisierung und Journey-basierten Kontext enthalten, um Dateneinblicke zu nutzen, die Ihre Marke mit Adobe Experience Cloud hat.

Diese Seite hilft Ihnen beim Einrichten und Verstehen wichtiger Dienste und Workflows, die mit Push-Benachrichtigungen in [!DNL Journey Optimizer] verbunden sind.

Die Schritte zum Konfigurieren des Push-Kanals in [!DNL Adobe Journey Optimizer] werden auf [dieser Seite](push-configuration.md) beschrieben.

## Push-Benachrichtigungen und Adobe Journey Optimizer

Das folgende Bild zeigt die Systeme und Dienste, die mit den zugehörigen Datenflüssen verbunden sind und beleuchten, wie Push-Benachrichtigungen von einem End-to-End-Service-Standpunkt aus bereitgestellt werden.

![](assets/push-flow.png)

1. Registrierung Ihrer gebrandeten Mobile App (Android oder iOS) mit den Apple-APNs und Google FCM-Push-Messaging-Diensten
1. Messaging Services generieren ein Push-Token, das eine Kennung ist, die Adobe Journey Optimizer verwendet, um das jeweilige Gerät mit einer Push-Benachrichtigung als Ziel auszuwählen.
1. Das zuvor generierte Push-Token wird an Adobe Experience Platform übergeben und mit dem Echtzeit-Kundenprofil synchronisiert. Dies erfolgt OOTB mit einem einfachen Client-SDK.
1. Push-Nachrichten werden in Adobe Journey Optimizer erstellt, Push-Nachrichten werden mit einer Nachrichtenvorgabe erstellt
1. Push-Nachrichten können in die Orchestrierungsarbeitsfläche von Journey aufgenommen werden
1. Nach der Journey-Publikation werden Kundenprofile, die auf Journey-Bedingungen basieren, für den Empfang von Push-Benachrichtigungen qualifiziert. In diesem Schritt werden Push-Nachrichten-Payloads personalisiert
1. Personalisierte Push-Payloads werden an einen internen Push-Nachrichtenversanddienst weitergeleitet
1. Dieser interne Dienst überprüft dann die Anmeldeinformationen der App, die mit der Nachricht verknüpft ist, und
1. Sendet die Nachricht zur endgültigen Auslieferung an Apple &amp; Google Messaging Services
1. Feedback von Messaging-Services wird zur Berichterstellung in Journey Live &amp; Global-Berichten aufgeführt, Fehler und Erfolge werden protokolliert
1. Push-Benachrichtigungen werden an Endbenutzergeräte gesendet
1. Push-Benachrichtigungsinteraktionen für Endbenutzer werden über die SDK-Integration als Erlebnisereignisse vom Endbenutzer-Client gesendet

## Rollen von Schlüsseldiensten in Push-Benachrichtigungen

* **Push-Benachrichtigungs-Service-** Anbieter sind die Kernkomponenten-Webdienste, die Benachrichtigungen von Remote-Servern an mobile Apps senden.

   [!DNL Adobe Journey Optimizer]  unterstützt sowohl Android- als auch iOS-Plattformen und integriert daher in Folgendes:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)  - zum Senden von Benachrichtigungen an eine Android Mobile App
   * [Apple Push Notification Service (APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  - zum Senden von Benachrichtigungen an eine iOS-Mobile-App

* **Adobe Experience Platform Mobile** SDK, das clientseitige Integrations-APIs für Ihre Mobiltelefone über Android- und iOS-kompatible SDKs bereitstellt. Das SDK bietet eine Adobe Journey Optimizer-Erweiterung, die eine Vielzahl von APIs verfügbar macht, die für Push-Nachrichten spezifisch sind, und Datenfluss ermöglicht, z. B. die Registrierung des Push-Tokens oder das Senden von Push-Tracking-Ereignissen oder anderen benutzerspezifischen Erlebnisereignissen an Adobe Experience Platform. Das SDK bietet außerdem eine Vielzahl anderer Erweiterungen, die andere Adobe Experience Cloud- sowie Drittanbieter-Partnerfunktionen ermöglichen.

   Die SDK-Integration erfordert auch die Einrichtung von Adobe Experience Platform [Datenerfassungsdiensten](https://experienceleague.adobe.com/docs/launch/using/home.html?lang=de), z. B.:

   * Erstellen eines Datenspeichers zum Konfigurieren der Profil- und Erlebnisereignis-Datensätze, anhand derer die Daten in Adobe Experience Platform fließen
   * Erstellen der clientseitigen mobilen Eigenschaft und Hinzufügen von Erweiterungen. Das SDK ist eng mit diesen Erweiterungen integriert, um eine nahtlose Datenerfassung zu ermöglichen.
   * Registrieren der App-Bundle-ID und App-Anmeldeinformationen

* **Das Echtzeit-Kundenprofil von Adobe Experience Platform**  bietet eine ganzheitliche Sicht auf jeden einzelnen Kunden, indem es Daten aus verschiedenen Kanälen, einschließlich Web, Mobile, CRM und Drittanbieter, kombiniert. Mit dem Profil können Sie Ihre Kundendaten in einer einheitlichen Ansicht zusammenfassen, die eine umsetzbare, mit Zeitstempel versehene Übersicht über jede Kundeninteraktion bietet. Das Push-Token für einen bestimmten App-Benutzer wird im Profil des Benutzers als Datensatzdaten gespeichert, während die Interaktionen, die der Benutzer mit Push-Benachrichtigungen ausführt, als Zeitreihenereignisdaten verfolgt werden. [Erfahren Sie mehr über das Echtzeit-Kundenprofil von Adobe Experience Platform.](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de)

* **[!DNL Adobe Journey Optimizer]** : Sobald Ihre Mobile-App-Integrationen mit den oben genannten Komponenten eingerichtet sind und Ihre Kundenprofile in Adobe Experience Platform vorhanden sind, können Sie Push-Benachrichtigungen in Adobe Journey Optimizer erstellen und koordinieren, um mit Ihren Benutzern zu interagieren.

## Technische Einrichtung und praktische Workflows für Push-Benachrichtigungen

In der folgenden Abbildung werden die verschiedenen Schritte (End-to-End) gezeigt, die an der Konfiguration der Komponenten beteiligt sind, die das Skelett des Push-Datenflusses bilden. Die Aktionselemente wurden basierend auf der Rolle, die die Konfiguration durchführt, und der zu konfigurierenden Komponente kategorisiert.

![](assets/user-flow.png)
