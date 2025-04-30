---
solution: Journey Optimizer
product: journey optimizer
title: Anwendungsfall-Playbooks
description: Erfahren Sie, wie Sie mit Adobe Journey Optimizer Anwendungsfall-Playbooks von Adobe Experience Platform nutzen können.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2214ec90-580e-469e-9b14-d8cb2d4bb050
source-git-commit: 7bb46f33d877d0a1976e8d74b88a5cccb81c1d4e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 69%

---

# Anwendungsfall-Playbooks {#playbooks}

## Anwendungsfall-Playbooks {#gs}

Anwendungsfall-Playbooks sind vordefinierte Workflows, die häufige Anwendungsfälle behandeln, die Sie mit Adobe Experience Platform und Journey Optimizer ausführen können.

![Animiertes Bild, das Anwendungsfall-Playbooks zeigt](../rn/assets/do-not-localize/playbooks.gif){width="85%"}

Jedes Playbook bietet einen umfassenden Überblick, einschließlich Absicht, Zielen, Zielgruppen und Ressourcen, die für die Implementierung benötigt werden. Darüber hinaus ist in jedem Playbook eine Übersicht verfügbar, um Touchpoints der Kundschaft aus der Praxis visuell darzustellen, die mit dem Playbook in Zusammenhang stehen.

![Playbook für abgebrochenen Warenkorb wird im Entdeckungs-Playbook angezeigt](assets/playbooks-detail.png){width="85%"}

## Voraussetzungen {#prerequisites}

Die folgenden Konfigurationsschritte sind erforderlich, bevor Sie mit Anwendungsfall-Playbooks arbeiten können. Detaillierte Informationen zu den einzelnen Schritten finden Sie in der Dokumentation zu Anwendungsfällen und Playbooks [Erste Schritte](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/get-started.html?lang=de){target="_blank"} Seite.

* Erstellen einer Sandbox
* Konfigurieren von Benutzerberechtigungen
* Konfigurieren von Journey Optimizer-Kanalkonfigurationen für E-Mail-, Push- und SMS-Benachrichtigungen

## Zugreifen auf und Aktivieren eines Playbooks {#access}

Um auf die Playbooks zuzugreifen, navigieren Sie zum Menü **[!UICONTROL Playbooks]** in der linken Navigationsleiste. Die Bibliothek enthält mehrere Playbooks, die mit Adobe Journey Optimizer implementiert wurden. Verwenden Sie die Filter neben der Suchleiste, um auf sie zuzugreifen. Eine umfassende Liste der Journey Optimizer-Playbooks finden Sie in der [ zu Anwendungsfällen ](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/playbooks-list.html?lang=de){target="_blank"}.

![Playbook-Liste mit geöffnetem Filterbereich](assets/playbooks-filter.png){width="85%"}

Nachdem Sie das Playbook ausgewählt haben, das Ihren Bedürfnissen am besten entspricht, können Sie es aktivieren. Dadurch wird eine Instanz des Playbooks erstellt und es werden automatisch die Ressourcen generiert, die zur Unterstützung Ihres spezifischen Anwendungsfalls erforderlich sind. Zu den Ressourcen gehören Journey Optimizer-Assets wie Journeys, Nachrichten sowie Adobe Experience Platform-Assets wie Schemata oder Segmente.

>[!NOTE]
>
>Diese Objekte sollen Ihnen dabei helfen, alle Ressourcen zu verstehen, die zur Implementierung Ihres spezifischen Anwendungsfalls erforderlich sind. Sie enthalten keine Daten und werden in Entwicklungs-Sandboxes erstellt.

Um Ihren Anwendungsfall zu implementieren, können Sie zu jedem Objekt navigieren und es an Ihre Anforderungen anpassen. Sie können auch die URL der Seite der Playbook-Instanz für Ihr Team freigeben, um bei der Implementierung des Anwendungsfalls zusammenzuarbeiten.

Darüber hinaus können Sie die Playbook-Assets in andere Sandboxes importieren. Auf diese Weise können Sie die generierten Assets an Ihren vorhandenen Assets ausrichten und sicherstellen, dass sie mit Ihren Daten kompatibel sind, falls Sie bereits eigene Schemata, Felder und Feldergruppen eingerichtet haben. Diese Schritte werden in der Dokumentation zu Anwendungsfall-Playbooks beschrieben: [Veröffentlichen von Playbook-generierten Assets in anderen Sandboxes](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/data-awareness.html?lang=de){target="_blank"}.

## Erstellen eigener Playbooks (Beta) {#create}

>[!AVAILABILITY]
>
>Die Erstellung von Playbooks für Anwendungsfälle steht derzeit allen Kunden als öffentliche Beta-Version zur Verfügung.

Zusätzlich zur Nutzung vordefinierter Playbooks können Sie Ihre eigenen Playbooks in Adobe Experience Platform erstellen und freigeben.

Sie können Metadaten mithilfe von KI-Unterstützung oder manueller Eingabe definieren, technische Assets wie Schemata und Segmente verknüpfen und Ihre Playbooks für verschiedene IMS-Organisationen freigeben.

Weitere Informationen zum Erstellen und Freigeben von Playbooks finden Sie in der Dokumentation zu Anwendungsfällen für Playbooks: [Erstellen und Freigeben eigener Playbooks mit dem KI-Assistenten](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/author.html?lang=en#sharing-playbooks-sandboxes){target="_blank"}.
