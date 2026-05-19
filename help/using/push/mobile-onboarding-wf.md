---
solution: Journey Optimizer
product: journey optimizer
title: Schnellstart-Workflow für Mobile-Onboarding
description: Erfahren Sie, wie Sie den Schnellstart-Workflow für das Mobile-Onboarding verwenden.
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
TQID: https://experienceleague.adobe.com/bqHcFNTpsuA6--8RiSjygD-8wsx4uwLeWqw9MBtby-4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 369
ht-degree: 98%

---

# Schnellstart-Workflow für Mobile-Onboarding {#mobile-wf}

Der neue **Schnellstart-Workflow für Mobile-Onboarding** ist eine neue Produktfunktion, die dazu dient, das Mobile SDK schnell zu konfigurieren, mit dem Erfassen und Überprüfen von Mobile-Ereignisdaten zu beginnen und Push-Benachrichtigungen mit [!DNL Journey Optimizer] zu senden.

Diese Funktion ist als eine öffentliche Beta-Version über die **[!DNL Adobe Experience Platform Data Collection]**-Startseite für alle Kunden verfügbar.

## Erste Schritte{#gs-mobile-wf}

Dieser neue Workflow automatisiert die Einrichtung der Datenerfassung, indem die Gesamtzahl der Klicks reduziert und die Mobile-Konfiguration für Journey Optimizer beschleunigt wird. Dieser Schnellstart-Workflow führt Sie durch vier einfache Schritte, um Ihre Mobile-Konfiguration [einzurichten](#gs-mobile-wf), zu [implementieren](#implement-mobile-wf), zu [validieren](#valid-mobile-wf) und zu [überprüfen](#review-mobile-wf).

Navigieren Sie vom Lösungsumschalter aus zum neuen Schnellstart-Workflow für das Mobile-Onboarding in **[!DNL Data Collection]**. Wählen Sie dann die **[!DNL Start Collecting Mobile Data]**-Karte auf der Startseite aus.

![](assets/mobile-wf-home.png)

Im Folgenden finden Sie einige zusätzliche Funktionen:

* Einfacher, vierstufiger Workflow und Benutzeroberfläche.
* Bietet eine grundlegende Einrichtung, um in Minutenschnelle mit der Erfassung von Mobile-Ereignisdaten über das [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation){target="_blank"} zu beginnen.
* Möglichkeit zum Testen und Validieren eines einfachen mobilen Push-Ereignisses mithilfe von [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=de){target="_blank"}.
* Erstellt und konfiguriert automatisch alle erforderlichen Datenerfassungs- und Journey Optimizer-Assets.
* In Produktanleitungen und QuickInfos.
* Bietet bei Bedarf einen natürlichen Übergang für eine erweiterte Implementierung.

## Einrichten {#setup-mobile-wf}

Im ersten Schritt dieses Workflows werden automatisch alle erforderlichen Datenerfassungs- und Journey Optimizer-Assets erstellt und konfiguriert, z. B. Eigenschaften für Mobilgeräte, Mobile-Erweiterungen, Journey Optimizer-Erweiterung, Regeln, Datenelemente usw.

Geben Sie, wenn Sie die Nutzungsbedingungen der Beta-Version akzeptiert haben, den Namen Ihrer Mobile App ein und klicken Sie auf **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Geben Sie Informationen für iOS- und Android-Plattformen an, einschließlich Ihrer App-ID und des Authentifizierungsschlüssel oder der Schlüsseldatei.

## Implementierung{#implement-mobile-wf}

Der nächste Schritt enthält eine Schritt-für-Schritt-Anleitung zur Installation des Codes für Ihre Mobile App.

![](assets/mobile-wf-add-code.png)


## Überprüfen{#valid-mobile-wf}

Überprüfen und checken Sie die Implementierung, um sie zu validieren. Sie können eine Test-Push-Benachrichtigung senden.

![](assets/mobile-wf-valid.png)


## Überprüfung {#review-mobile-wf}

Die automatisierte Einrichtung ist abgeschlossen. Sie können jetzt Ihre mobile Tag-Eigenschaft aufrufen, Ihre Regeln oder Datenelemente konfigurieren und mit dem Senden von Push-Benachrichtigungen mit Adobe Journey Optimizer beginnen.

![](assets/mobile-wf-done.png)


**Verwandte Themen**

* [Erste Schritte mit Push-Benachrichtigungen](../../rp_landing_pages/push-landing-page.md)
* [Datenfluss und Komponenten von Push-Benachrichtigungen](push-gs.md)
* [Kanal der Push-Benachrichtigung konfigurieren](push-configuration.md)
* [Bericht zu Push-Benachrichtigungen](../reports/journey-global-report-cja-push.md#track-link-url-push)
* [Erstellen einer Push-Benachrichtigung](create-push.md)
