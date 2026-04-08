---
title: Erstellen eines Posteingangs
description: Beginnen Sie mit dem Posteingang in Adobe Journey Optimizer, um persistente, nicht aufdringliche Nachrichten für Ihre Benutzerinnen und Benutzer zu senden.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: f7f303685e954614b44a9b62368460e9b07b26b3
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# Erste Schritte mit dem Posteingang {#inbox-gs}

Der Posteingang liefert beständige Nachrichten mit geringem Reibungsaufwand an einem Ort innerhalb Ihrer Mobile App oder Website. In-App- und Push-Benachrichtigungen können nach einem Wischen oder Tippen verschwinden. Im Posteingang sind Nachrichten verfügbar, sodass Benutzer sie öffnen, lesen und bearbeiten können, wenn es ihnen passt.

Der Posteingang baut auf dem Kanal Inhaltskarten auf und fügt hinzu:

* **Persistent Messaging**: Inhalte bleiben im Posteingang, bis Sie sie entfernen oder ablaufen, sodass Benutzer nach dem Schließen einer Benachrichtigung oder dem Verlassen der App dorthin zurückkehren können.
* **Zentraler Speicherort**: Ein einzelnes Postfach in Ihrer App oder Site für relevante Marketing-Nachrichten.
* **Flexible Implementierung**: Verwenden Sie den vorgefertigten Posteingang-Container oder passen Sie das Erlebnis in Ihrer eigenen Benutzeroberfläche an.
* **Lesestatus**: Nachrichten können auf dem Gerät, auf dem sie geöffnet werden, als gelesen oder ungelesen markiert werden.

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um den Posteingang zu konfigurieren und zu verwenden:

1. [Konfigurieren von Adobe Journey Optimizer](inbox-configuration.md)

   Fügen Sie unter **Kanalkonfigurationen** eine Kanalkonfiguration für den Posteingang **hinzu,** Journey Optimizer weiß, wo und wie der Posteingang ausgeführt wird (Webseite oder Regel oder Oberfläche der Mobile App).

1. [Erstellen Ihres Posteingangs in Journey Optimizer](inbox-create.md)

   Erstellen Sie eine Kampagne mit der Aktion **Inhaltskarte** und wählen Sie **Posteingang** als Versandspeicherort aus - geplant über die Benutzeroberfläche oder ausgelöst durch die API.

1. [Gestalten Ihres Posteingangs](inbox-design.md)

   Wählen Sie Posteingangsvorlagen und Listen- oder erweiterte Layouts aus, damit die Nachrichten zu Ihrer Marke und Ihren Benutzererlebnissen passen.

1. [Erstellen Sie Ihre Inhaltskarte und verknüpfen Sie sie mit Ihrem Posteingang](../content-card/create-content-card.md)

   Erstellen Sie den Karteninhalt im Designer, beenden Sie die für den Posteingang spezifischen Optionen und aktivieren Sie dann Ihre Kampagne, damit die Nachrichten den Posteingang erreichen.

## Weitere Ressourcen

* [Posteingang-Benutzeroberfläche (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS/): Anforderungen, öffentliche API-Oberfläche, Posteingangseinstellungen und Links zu Tutorials zur Implementierung des Journey Optimizer-Posteingangs in einer iOS-App mit Adobe Experience Platform Mobile SDK (iOS 15 oder höher, Xcode 15 oder höher, Swift 5.1 oder höher).

* [Posteingang abrufen und anzeigen](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/): Laden Sie Journey Optimizer-Posteingangsnachrichten und rendern Sie die Benutzeroberfläche des Posteingangs auf Android (Dokumentation zu Adobe Developer).

* [Posteingang anpassen](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/): Passen Sie das Layout, den Stil und das Interaktionsverhalten des Posteingangs für Ihre Android-App an (Dokumentation zu Adobe Developer).

* [Überwachen von Posteingangsereignissen](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/): Abonnieren von Posteingangsrückrufen für Benutzeraktionen und Lebenszyklusaktualisierungen auf Android (Dokumentation zu Adobe Developer).
