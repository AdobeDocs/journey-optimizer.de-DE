---
solution: Journey Optimizer
product: journey optimizer
title: Integration mit anderen Lösungen
description: Erfahren Sie mehr über die Integration von Journey Optimizer in andere Lösungen.
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 12ae84646e69870564406066e102c540ac920df7
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 33%

---

# Integration mit anderen Lösungen {#integration}

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologiestapels sind. Mithilfe dieser Integrationen können Sie Ihre spezifischen Anwendungsfälle bearbeiten und den Funktionsumfang von Adobe Journey Optimizer erweitern.

>[!NOTE]
>
> Auf Adobe Experience Platform aufbauend ist Adobe Journey Optimizer nativ mit [Adobe Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target=&quot;_blank&quot;}. Diese integrierte Datenquelle ist vorkonfiguriert und dient dem Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofil (überprüfen Sie beispielsweise, ob die Person, die an einer Journey teilgenommen hat, ein Kunde ist oder nicht). Sie ermöglicht Ihnen die Verwendung von Profildaten und Erlebnisereignisdaten. [Weitere Informationen](../datasource/adobe-experience-platform-data-source.md).

## Reporting{#integration-reporting}

### Adobe Customer Journey Analytics{#integration-cja}

Sie können von Journey Optimizer generierte Daten exportieren, um eine erweiterte Analyse in Customer Journey Analytics durchzuführen.

Die Journey Optimizer-Integration mit Customer Journey Analytics bietet eine ganzheitliche Sicht auf all Ihre Journey mit automatisierter Berichtverteilung und benutzerdefinierten Visualisierungen der Daten.

Nachdem Sie Ihre Journey in Journey Optimizer erstellt haben, können Sie Ihre Kundendaten in Customer Journey Analytics importieren, um Berichte zu erstellen und die Auswirkungen jeder Interaktion eines Kunden mit Ihren Journey zu verstehen.

Weitere Informationen [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

### Adobe Analytics{#integration-aa}

Sie können alle verhaltensbezogenen Ereignisdaten, die Sie in Adobe Analytics bereits erfassen und an Adobe Experience Platform streamen, nutzen, um Journey von Triggern zu erhalten und Erlebnisse für Ihre Kunden zu automatisieren.

Weitere Informationen [Journey Optimizer + Analytics](../event/about-analytics.md).

## Maschinelles Lernen{#integration-intelligent-service}

Durch die Integration mit Adobe Intelligent Services können Sie die Leistungsfähigkeit von künstlicher Intelligenz und maschinellem Lernen in Anwendungsfällen für Kundenerlebnisse nutzen. So können Marketing-Analysten mithilfe von Konfigurationen auf Unternehmensebene spezifische Prognosen für die Anforderungen der Firma erstellen, ohne dass hierfür Kenntnisse aus der Datenwissenschaft erforderlich wären. [Weitere Informationen](../building-journeys/ai-services-overview.md).

## Nachrichten senden {#integration-messages}

Sie können zum Senden von Nachrichten ein Drittanbietersystem verwenden.

### Adobe Campaign{#integration-ac}

Für Adobe Campaign v7 und v8 ist eine Integration verfügbar. Verwenden Sie diese Integration, um E-Mails, Push-Benachrichtigungen und SMS mit den Funktionen für Transaktionsnachrichten von Adobe Campaign zu senden.

Weitere Informationen [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Sie können auch eine Integration mit Adobe Campaign Standard einrichten, um Nachrichten in Ihren Journey zu senden.

Weitere Informationen [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

### Benutzerdefinierte Kanäle{#integration-custom}

Wenn Sie ein Drittanbietersystem zum Nachrichtenversand verwenden oder wenn Sie möchten, dass von Journeys API-Aufrufe an ein Drittanbietersystem gesendet werden, verwenden Sie benutzerdefinierte Aktionen, um die Verbindung zwischen dem System und Ihrer Journey zu konfigurieren. Sie können mit benutzerdefinierten Aktionen beispielsweise eine Verbindung zu den folgenden Systemen herstellen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase usw.

Benutzerdefinierte Aktionen sind zusätzliche Aktionen, die von technischen Benutzern definiert und Marketing-Experten zur Verfügung gestellt werden. Nach der Konfiguration erscheinen sie in der linken Palette Ihrer Journey in der Kategorie **[!UICONTROL Aktion]**. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/about-journey-activities.md#action-activities).

Weitere Informationen [benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md).

## Externe Systeme{#integration-external-systems}

Mit Journey Optimizer können Sie Verbindungen zu externen Systemen über benutzerdefinierte Datenquellen und Aktionen konfigurieren. So können Sie beispielsweise Ihre Journey mit Daten aus einem externen Reservierungssystem anreichern.

Erfahren Sie, wie Sie mit externen Datenquellen eine Verbindung zu einem Drittanbietersystem definieren können in [diesem Abschnitt](../datasource/external-data-sources.md).
