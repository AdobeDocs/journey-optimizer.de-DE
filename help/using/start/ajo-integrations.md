---
solution: Journey Optimizer
product: journey optimizer
title: Integration mit anderen Lösungen
description: Erfahren Sie mehr über die Integration von Journey Optimizer in andere Lösungen.
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Integration mit anderen Lösungen {#integration}

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologiestapels sind. Mithilfe dieser Integrationen können Sie Ihre spezifischen Anwendungsfälle bearbeiten und den Funktionsumfang von Adobe Journey Optimizer erweitern.

>[!NOTE]
>
> Auf Adobe Experience Platform aufbauend ist Adobe Journey Optimizer nativ mit [Adobe Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target=&quot;_blank&quot;}. Diese integrierte Datenquelle ist vorkonfiguriert und dient dem Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofil (überprüfen Sie beispielsweise, ob die Person, die an einer Journey teilgenommen hat, ein Kunde ist oder nicht). Sie ermöglicht Ihnen die Verwendung von Profildaten und Erlebnisereignisdaten. [Weitere Informationen](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Mit Customer Journey Analytics können Sie erweiterte Analysen von in Journey Optimizer generierten Daten durchführen.

Journey Optimizer speichert Daten in der Adobe Experience Platform und bietet mit Customer Journey Analytics eine ganzheitliche Sicht auf all Ihre Journey, Kampagnen und Angebote mit automatisierter Berichtverteilung und benutzerdefinierten Datenvisualisierungen.

Nach der Erstellung Ihrer Journey in Journey Optimizer können Customer Journey Analytics Daten aus der Plattform erfassen, um Berichte zu erstellen und die Auswirkungen jeder Interaktion eines Kunden mit Ihren Journey zu verstehen.

Weitere Informationen [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Sie können alle verhaltensbezogenen Ereignisdaten, die Sie in Adobe Analytics bereits erfassen und an Adobe Experience Platform streamen, nutzen, um Echtzeit-Journey in Trigger zu senden und Erlebnisse für Ihre Kunden zu automatisieren. Diese Daten können auch verwendet werden, um Segmente zu erstellen, die mit Journey Optimizer interagiert werden können.

Weitere Informationen [Journey Optimizer + Analytics](../event/about-analytics.md).

## Adobe Intelligent Services{#integration-intelligent-service}

Mit Adobe Intelligent Services, die in der Echtzeit-Kundendatenplattform integriert sind, können Sie die Leistungsfähigkeit von künstlicher Intelligenz und maschinellem Lernen in Anwendungsfällen mit Kundenerlebnissen nutzen. So können Marketing-Analysten mithilfe von Konfigurationen auf Unternehmensebene spezifische Prognosen für die Anforderungen der Firma erstellen, ohne dass hierfür Kenntnisse aus der Datenwissenschaft erforderlich wären.

Mit Customer AI können Marken auf maschinellem Lernen basierende Abwanderungs- oder Konversionswerte erstellen, die als Profilattribute in Adobe Experience Platform verfügbar sind und zur Personalisierung einer Journey verwendet werden können.

[Weitere Informationen](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

Für Adobe Campaign v7 und v8 ist eine Integration verfügbar. Verwenden Sie diese Integration, um E-Mails, Push-Benachrichtigungen und SMS mit den Funktionen für Transaktionsnachrichten von Adobe Campaign zu senden.

Weitere Informationen [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Sie können auch eine Integration mit Adobe Campaign Standard einrichten, um Nachrichten in Ihren Journey zu senden.

Weitere Informationen [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Benutzerdefinierte Kanäle{#integration-custom}

Wenn Sie zum Senden von Nachrichten ein Drittanbietersystem verwenden oder möchten, dass Journey API-Aufrufe an ein Drittanbietersystem senden, verwenden Sie benutzerdefinierte Aktionen, um eine Verbindung zu Ihrer Journey herzustellen. Sie können beispielsweise mit benutzerdefinierten Aktionen eine Verbindung zu den folgenden Systemen herstellen: Epsilon, Slack [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase usw.

Benutzerdefinierte Aktionen sind zusätzliche Aktionen, die von technischen Benutzern definiert und Marketing-Experten zur Verfügung gestellt werden. Nach der Konfiguration werden sie in der linken Palette Ihrer Journey im **[!UICONTROL Aktion]** Kategorie. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/about-journey-activities.md#action-activities).

Weitere Informationen [benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md).

## Externe Datenquellen{#integration-external-systems}

Mit Journey Optimizer können Sie Verbindungen zu externen Systemen über benutzerdefinierte Datenquellen und Aktionen konfigurieren. So können Sie beispielsweise Ihre Journey mit Daten aus einem externen Reservierungssystem anreichern.

Erfahren Sie, wie Sie mit externen Datenquellen eine Verbindung zu einem Drittanbietersystem definieren können in [diesem Abschnitt](../datasource/external-data-sources.md).
