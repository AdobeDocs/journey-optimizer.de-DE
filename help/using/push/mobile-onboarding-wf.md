---
solution: Journey Optimizer
product: journey optimizer
title: Schnellstart-Workflow für die Mobile-Integration
description: Erfahren Sie, wie Sie den Schnellstart-Workflow für das Mobile Onboarding verwenden.
topic: Mobile
feature: Push
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
source-git-commit: 145d2a60bc5dbd6e2a92f13afbf2db662f465e36
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---


# Schnellstart-Workflow für die Mobile-Integration {#mobile-wf}

Die neue **Schnellstartworkflow für mobile Onboarding** ist eine neue Produktfunktion, mit der das Mobile SDK schnell konfiguriert, mit der Erfassung und Validierung von Mobilereignisdaten begonnen und Push-Benachrichtigungen mit [!DNL Journey Optimizer].

Auf diese Funktion kann über die **[!DNL Adobe Experience Platform Data Collection]** Startseite für alle Kunden als öffentliche Beta-Version.

## Erste Schritte  {#gs-mobile-wf}

Dieser neue Workflow automatisiert die Einrichtung der Datenerfassung, indem die Gesamtzahl der Klicks reduziert und die mobile Konfiguration für Journey Optimizer beschleunigt wird. Dieser Schnellstart-Workflow führt Sie durch vier einfache Schritte [einrichten](##setup-mobile-wf), [implementieren](#implement-mobile-wf), [validate](#valid-mobile-wf)und [Überprüfung](#review-mobile-wf) Ihre Mobile-Konfiguration.

Navigieren Sie zum neuen Schnellstartworkflow für das mobile Onboarding zu **[!DNL Data Collection]** aus dem Lösungsschalter. Wählen Sie dann die **[!DNL Start Collecting Mobile Data]** auf der Startseite angezeigt.

![](assets/mobile-wf-home.png)

Im Folgenden finden Sie einige zusätzliche Funktionen:

* Einfache, vierstufige Arbeitsabläufe und Benutzeroberfläche.
* Bietet eine grundlegende Einrichtung, um in Minutenschnelle mit der Erfassung von Mobilereignisdaten über das Mobile SDK zu beginnen.
* Möglichkeit zum Testen und Validieren eines einfachen mobilen Push-Ereignisses mithilfe von Assurance.
* Erstellt und konfiguriert automatisch alle erforderlichen Datenerfassungs- und Journey Optimizer-Assets.
* In Produktanleitungen und QuickInfos.
* Bietet bei Bedarf eine natürliche Transition für eine erweiterte Implementierung.

## Einrichten {#setup-mobile-wf}

Im ersten Schritt dieses Workflows werden automatisch alle erforderlichen Datenerfassungs- und Journey Optimizer-Assets erstellt und konfiguriert, z. B. Eigenschaften für Mobilgeräte, mobile Erweiterungen, Journey Optimizer-Erweiterung, Regeln, Datenelemente usw.

Geben Sie nach Annahme der Nutzungsbedingungen von Beta den Namen Ihrer Mobile App ein und klicken Sie auf **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Geben Sie Informationen für iOS- und Android-Plattformen an, einschließlich Ihrer App-ID und Authentifizierungsschlüssel oder Schlüsseldatei.

## Implementierung{#implement-mobile-wf}

Der nächste Schritt enthält eine schrittweise Anleitung zur Installation des Codes für Ihre mobile App.

![](assets/mobile-wf-add-code.png)


## Überprüfen{#valid-mobile-wf}

Überprüfen und überprüfen Sie die Implementierung, um sie zu validieren. Sie können eine Test-Push-Benachrichtigung senden.

![](assets/mobile-wf-valid.png)


## Überprüfung {#review-mobile-wf}

Die automatisierte Einrichtung erfolgt. Sie können jetzt Ihre mobile Tag-Eigenschaft aufrufen, Ihre Regeln oder Datenelemente konfigurieren und mit dem Senden von Push-Benachrichtigungen mit Adobe Journey Optimizer beginnen.

![](assets/mobile-wf-done.png)


**Verwandte Themen**

* [Erste Schritte mit Push-Benachrichtigungen](get-started-push.md)
* [Datenfluss und Komponenten von Push-Benachrichtigungen](push-gs.md)
* [Push-Kanal konfigurieren](push-configuration.md)
* [Bericht zu Push-Benachrichtigungen](../reports/journey-global-report.md#push-global)
* [Erstellen einer Push-Benachrichtigung](create-push.md)
