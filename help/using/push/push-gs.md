---
solution: Journey Optimizer
product: journey optimizer
title: Push-Benachrichtigungen und Adobe Journey Optimizer
description: Datenfluss und Komponenten von Push-Benachrichtigungen verstehen
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Push-Benachrichtigungen und Adobe Journey Optimizer {#get-started-push}

Auf dieser Seite erfahren Sie, welche zentralen Dienste und Workflows mit Push-Benachrichtigungen in [!DNL Journey Optimizer]. Erfahren Sie, wie Sie Push-Benachrichtigungen erstellen in [diese Seite](create-push.md).

Schritte zum Konfigurieren des Push-Kanals in [!DNL Adobe Journey Optimizer] sind ausführlich unter [diese Seite](push-configuration.md).

Das folgende Bild zeigt die Systeme und Dienste, die mit den zugehörigen Datenflüssen verbunden sind und beleuchten, wie Push-Benachrichtigungen von einem End-to-End-Service-Standpunkt aus bereitgestellt werden.

![](assets/push-flow.png)

1. Registrierung Ihrer gebrandeten Mobile App (Android oder iOS) mit den Apple-APNs und Google FCM-Push-Messaging-Diensten
1. Messaging Services generieren ein Push-Token, das eine Kennung ist, die [!DNL Adobe Journey Optimizer] verwendet , um das spezifische Gerät mit einer Push-Benachrichtigung anzusprechen.
1. Das zuvor generierte Push-Token wird an Adobe Experience Platform übergeben und mit dem Echtzeit-Kundenprofil synchronisiert. Dies erfolgt OOTB mit einem einfachen Client-SDK.
1. Push-Nachrichten werden in [!DNL Adobe Journey Optimizer], werden Push-Nachrichten für eine Kanaloberfläche erstellt (d. h. eine Nachrichtenvorgabe).
1. Push-Nachrichten können auf der Arbeitsfläche der Orchestrierung in Journeys enthalten sein.
1. Bei der Veröffentlichung in Journey werden Kundenprofile, die auf Journey-Bedingungen basieren, für den Empfang von Push-Benachrichtigungen qualifiziert. In diesem Schritt werden Push-Nachrichten-Payloads personalisiert
1. Personalisierte Push-Payloads werden an einen internen Push-Nachrichtenversanddienst weitergeleitet
1. Dieser interne Dienst überprüft dann die Anmeldeinformationen der App, die mit der Nachricht verknüpft ist, und
1. Sendet die Nachricht zur endgültigen Auslieferung an Apple &amp; Google Messaging Services
1. Feedback von Messaging-Services wird zur Berichterstellung in Journey Live &amp; Global-Berichten aufgeführt, Fehler und Erfolge werden protokolliert
1. Push-Benachrichtigungen werden an Endbenutzergeräte gesendet
1. Push-Benachrichtigungsinteraktionen für Endbenutzer werden über die SDK-Integration als Erlebnisereignisse vom Endbenutzer-Client gesendet

## Rollen von Schlüsseldiensten in Push-Benachrichtigungen {#roles-of-key-services}

* **Push-Benachrichtigungs-Dienstleister** sind die Kernkomponenten-Webdienste, die Benachrichtigungen von Remote-Servern an mobile Apps bereitstellen.

   [!DNL Adobe Journey Optimizer]  unterstützt sowohl Android- als auch iOS-Plattformen und integriert daher in Folgendes:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - zum Senden von Benachrichtigungen an eine mobile Android-App
   * [Apple Push Notification Service (APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - zum Senden von Benachrichtigungen an eine mobile iOS-App

* **Adobe Experience Platform Mobile SDK** , die Client-seitige Integrations-APIs für Ihre Mobiltelefone über Android- und iOS-kompatible SDKs bereitstellt. Das SDK stellt eine [!DNL Adobe Journey Optimizer] Erweiterung, die eine Vielzahl von APIs verfügbar macht, die für Push-Nachrichten spezifisch sind, und Datenfluss ermöglicht, z. B. die Registrierung des Push-Tokens oder das Senden von Push-Tracking-Ereignissen oder anderen benutzerspezifischen Erlebnisereignissen an Adobe Experience Platform. Das SDK bietet außerdem eine Vielzahl anderer Erweiterungen, die andere Adobe Experience Cloud- sowie Drittanbieter-Partnerfunktionen ermöglichen.

   Die SDK-Integration erfordert auch die Einrichtung von Adobe Experience Platform [Datenerfassung](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html){target=&quot;_blank&quot;} Dienste wie:

   * Erstellen eines Datenspeichers zum Konfigurieren der Profil- und Erlebnisereignis-Datensätze, mit denen die Daten in Adobe Experience Platform übertragen werden
   * Erstellen der clientseitigen mobilen Eigenschaft und Hinzufügen von Erweiterungen. Das SDK ist eng mit diesen Erweiterungen integriert, um eine nahtlose Datenerfassung zu ermöglichen.
   * Registrieren der App-Bundle-ID und App-Anmeldeinformationen

* **Echtzeit-Kundenprofil von Adobe Experience Platform**  bietet eine ganzheitliche Sicht auf jeden einzelnen Kunden, indem Daten aus verschiedenen Kanälen, einschließlich Web, Mobile, CRM und Drittanbieter, kombiniert werden. Mit dem Profil können Sie Ihre Kundendaten in einer einheitlichen Ansicht zusammenfassen, die eine umsetzbare, mit Zeitstempel versehene Übersicht über jede Kundeninteraktion bietet. Das Push-Token für einen bestimmten App-Benutzer wird im Profil des Benutzers als Datensatzdaten gespeichert, während die Interaktionen, die der Benutzer mit Push-Benachrichtigungen ausführt, als Zeitreihenereignisdaten verfolgt werden. [Erfahren Sie mehr über das Echtzeit-Kundenprofil von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : Sobald Ihre Mobile-App-Integrationen mit den oben genannten Komponenten eingerichtet sind und Ihre Kundenprofile in Adobe Experience Platform vorhanden sind, können Sie Push-Benachrichtigungen in [!DNL Adobe Journey Optimizer] , um mit Ihren Benutzern zu interagieren.

## Technische Einrichtung und praktische Workflows für Push-Benachrichtigungen {#push-technical-setup}

In der folgenden Abbildung werden die verschiedenen Schritte (End-to-End) gezeigt, die an der Konfiguration der Komponenten beteiligt sind, die das Skelett des Push-Datenflusses bilden. Die Aktionselemente wurden basierend auf der Rolle, die die Konfiguration durchführt, und der zu konfigurierenden Komponente kategorisiert.

![](assets/user-flow.png)
