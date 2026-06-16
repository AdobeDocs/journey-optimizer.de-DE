---
title: Erstellen eines Posteingangs
description: Beginnen Sie mit dem Posteingang in Adobe Journey Optimizer, um persistente, nicht aufdringliche Nachrichten an Ihre Benutzerinnen und Benutzer zu senden.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# Erste Schritte mit dem Posteingang {#inbox-gs}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie der Posteingangskanal Marketing-Nachrichten an einem beständigen Ort innerhalb Ihrer App oder Website speichert, damit Benutzer zum Lesen zurückkehren und sie nach Belieben bearbeiten können.

>[!ENDSHADEBOX]

Der Posteingang liefert persistente Nachrichten mit geringer Reibung an einem Ort innerhalb Ihrer App oder Website. In-App- und Push-Benachrichtigungen können nach einem Wischen oder Tippen verschwinden. Im Posteingang bleiben Nachrichten verfügbar, sodass Benutzende sie öffnen, lesen und bearbeiten können, wenn es ihnen passt.

Der Posteingang baut auf dem Inhaltskarten-Kanal auf und fügt Folgendes hinzu:

* **Persistentes Messaging:** Inhalte bleiben im Posteingang, bis Sie sie entfernen oder sie ablaufen, sodass Benutzende nach dem Schließen einer Benachrichtigung oder dem Verlassen der App dorthin zurückkehren können.
* **Zentraler Speicherort:** Ein einzelnes Postfach in Ihrer App oder auf Ihrer Site für relevante Marketing-Nachrichten.
* **Flexible Implementierung:** Verwenden Sie den vorgefertigten Posteingang-Container oder passen Sie das Erlebnis in Ihrer eigenen Benutzeroberfläche an.
* **Lesestatus:** Nachrichten können auf dem Gerät, auf dem sie geöffnet werden, als gelesen oder ungelesen markiert werden.

## Schnellstartanleitung

Führen Sie die folgenden Schritte aus, um den Posteingang zu konfigurieren und zu verwenden:

1. [Konfigurieren von Adobe Journey Optimizer](inbox-configuration.md)

   Fügen Sie unter **Kanalkonfigurationen** eine Kanalkonfiguration für den **Posteingang** hinzu, damit Journey Optimizer weiß, wo und wie der Posteingang ausgeführt wird (Web-Seite oder Regel oder Oberfläche der App).

1. [Erstellen des Posteingangs in Journey Optimizer](inbox-create.md)

   Erstellen Sie eine Kampagne mit der Aktion **Inhaltskarte** und wählen Sie **Posteingang** als Versandspeicherort aus – geplant über die Benutzeroberfläche oder durch API ausgelöst.

1. [Gestalten des Posteingangs](inbox-design.md)

   Wählen Sie Posteingangsvorlagen und Listen- oder erweiterte Layouts aus, damit die Nachrichten zu Ihrer Marke und Ihren Benutzererlebnissen passen.

1. [Erstellen der Inhaltskarte und Verknüpfen mit dem Posteingang](../content-card/create-content-card.md)

   Erstellen Sie den Karteninhalt im Designer, wählen Sie die für den Posteingang spezifischen Optionen aus und aktivieren Sie dann Ihre Kampagne, damit die Nachrichten den Posteingang erreichen.

## Zusätzliche Ressourcen

* [Posteingang-Benutzeroberfläche (iOS):](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS) Anforderungen, öffentliche API-Oberfläche, Posteingangseinstellungen und Links zu Tutorials zur Implementierung des Journey Optimizer-Posteingangs in einer iOS-App mit Adobe Experience Platform Mobile SDK (iOS 15 oder höher, Xcode 15 oder höher, Swift 5.1 oder höher).

* [Abrufen und Anzeigen des Posteingangs:](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox) Laden Sie Journey Optimizer-Posteingangsnachrichten und rendern Sie die Benutzeroberfläche des Posteingangs auf Android (Adobe Developer-Dokumentation).

* [Anpassen des Posteingangs:](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox) Passen Sie das Layout, den Stil und das Interaktionsverhalten des Posteingangs für Ihre Android-App an (Adobe Developer-Dokumentation).

* [Überwachen von Posteingangsereignissen:](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events) Abonnieren Sie Posteingangsrückrufe für Benutzeraktionen und Lebenszyklusaktualisierungen auf Android (Adobe Developer-Dokumentation).
