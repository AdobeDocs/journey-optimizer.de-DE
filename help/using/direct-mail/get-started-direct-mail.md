---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Direkt-Mail
description: Erfahren Sie, wie Sie in Journey Optimizer eine Direkt-Mail-Nachricht erstellen
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: Direkt-Mail, Nachricht, Kampagne
exl-id: bb52f400-6289-4a7f-a34f-98eb5d27c76a
TQID: https://experienceleague.adobe.com/Gmtr-7HW70-cg7va8iHfR5xKdYts-ZdDCm6CeQHJ0tg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: e7702a4706509a8181ee39cccc510656c5230a16
workflow-type: tm+mt
source-wordcount: 487
ht-degree: 89%

---

# Erste Schritte mit Direkt-Mail {#create-direct}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie der Briefpostkanal funktioniert, damit Sie die Extraktionsdateien generieren können, die Drittanbieter verwenden, um physische Post an Ihre Kunden zu senden.

>[!ENDSHADEBOX]

Direkt-Mail ist ein Offline-Kanal, mit dem Sie die Extraktionsdateien personalisieren und generieren können, die Direkt-Mail-Drittanbieter zum Senden von Nachrichten an Ihre Kunden und Kundinnen benötigen.

Bei der Erstellung einer Direkt-Mail-Kampagne oder -Journey generiert Journey Optimizer automatisch eine Datei, die alle Zielgruppenprofile und ausgewählten Daten enthält, z. B. Postanschriften und Profilattribute. Diese Datei wird an den Server Ihrer Wahl gesendet, sodass der von Ihnen gewählte Direkt-Mail-Anbieter darauf zugreifen kann, der den eigentlichen Mailing-Prozess für Sie übernimmt.

Sie müssen ggf. mit Ihrem ausgewählten Direkt-Mail-Drittanbieter zusammenarbeiten, um die erforderliche Zustimmung von Ihren Kundinnen und Kunden zu erhalten, damit diese E-Mails von Ihnen erhalten können.

Die Nutzung von Mailing-Services unterliegt den zusätzlichen Bedingungen des jeweiligen Direkt-Mail-Drittanbieters.  Adobe hat keine Kontrolle über die Produkte von Drittanbietern und ist nicht für Ihre Nutzung dieser Produkte verantwortlich. Bei Problemen oder Fragen im Zusammenhang mit dem Versand Ihrer Direkt-Mail-Kampagne wenden Sie sich bitte an den von Ihnen gewählten Direkt-Mail-Anbieter.

## Vorbereitung {#before-you-start}

Bevor Sie Direkt-Mail-Nachrichten erstellen, konfigurieren Sie [Datei-Routing und eine Konfiguration des Direkt-Mail-Kanals](direct-mail-configuration.md). Außerdem benötigen Sie Zielgruppen und Profildaten (z. B. Postanschriften) in Adobe Experience Platform.

Die wichtigsten Schritte zum Senden von Direkt-Mail-Nachrichten sind:

![Erstellungs-Workflow für Direkt-Mail von der Konfiguration bis zum Versand](assets/dm-creation-process.png)

>[!AVAILABILITY]
>
>Direkt-Mail-Nachrichten können nur im Rahmen von Journeys und Kampagnen erstellt werden. Sie sind nicht für die Verwendung in durch API ausgelösten Kampagnen verfügbar.

![Animierte Übersicht über den Direkt-Mail-Kanal in Journey Optimizer](../rn/assets/do-not-localize/gif-dm.gif)

## Zusätzliche Ressourcen {#additional-resources}

* **[Erstellen von Direkt-Mail](create-direct-mail.md)** – Erfahren Sie, wie Sie Direkt-Mail-Sendungen erstellen und Extraktionsdateien für Offline-Kanäle konfigurieren.
* **[Konfigurieren des Direkt-Mail-Kanals](direct-mail-configuration.md)** – Richten Sie Direkt-Mail-Oberflächen und Datei-Routing-Konfigurationen ein.
* **[Batch Decisioning in Briefpost](../experience-decisioning/batch-decisioning-direct-mail.md)** - Verwenden Sie Decisioning, um Extraktionsdateien für Briefpost zu personalisieren oder um Entscheidungsdaten für nachgelagerte Systeme zu exportieren.
* **[Testen und Senden von Direkt-Mail](test-send-direct-mail.md)** – Erfahren Sie, wie Sie Ihre Direkt-Mail-Sendungen testen, validieren und veröffentlichen.
* **[Tutorials zu Direkt-Mail](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}** – Erkunden Sie die schrittweisen Video-Tutorials zu den Funktionen von Direkt-Mail und Best Practices.

## Anleitungsvideo {#how-to-video}

Erfahren Sie, wie Sie den Direkt-Mail-Kanal in Adobe Journey Optimizer nutzen, um Direkt-Mail-Sendungen in Ihren Journeys zu automatisieren und zu planen.

+++ Video ansehen

>[!VIDEO](https://video.tv.adobe.com/v/3479171?captions=ger&quality=12)

+++

Eine schriftliche Anleitung derselben Schritte finden Sie in den [Tutorials zum Direkt-Mail-Kanal](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}.

Häufige Fragen zu Direkt-Mail finden Sie oben im Abschnitt [Zusätzliche Ressourcen](#additional-resources).
