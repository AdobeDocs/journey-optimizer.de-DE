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
source-wordcount: '573'
ht-degree: 0%

---

# Integration mit anderen Lösungen {#integration}

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind. Mithilfe dieser Integrationen können Sie Ihre spezifischen Anwendungsfälle bearbeiten und den Funktionsumfang von Adobe Journey Optimizer erweitern.

>[!NOTE]
>
> Auf der Grundlage von Adobe Experience Platform ist Adobe Journey Optimizer nativ mit [Adobe Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}. Diese integrierte Datenquelle ist vorkonfiguriert und soll Daten aus dem Echtzeit-Kundenprofil abrufen und verwenden (überprüfen Sie beispielsweise, ob die Person, die an einer Journey teilnimmt, ein Kunde ist oder nicht). Damit können Sie Profildaten und Erlebnisereignisdaten verwenden. [Weitere Infos](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Sie können Customer Journey Analytics verwenden, um erweiterte Analysen von Daten durchzuführen, die von Journey Optimizer generiert wurden.

Journey Optimizer speichert Daten in Adobe Experience Platform. Mit Customer Journey Analytics erhalten Sie eine ganzheitliche Sicht auf all Ihre Journeys, Kampagnen und Angebote mit automatisierter Berichtverteilung und benutzerdefinierten Visualisierungen der Daten.

Nachdem Sie Ihre Journey in Journey Optimizer erstellt haben, kann Customer Journey Analytics Daten von der Plattform erfassen, um Berichte zu starten und die Auswirkungen jeder Interaktion eines Kunden mit Ihren Journeys zu verstehen.

Weitere Informationen [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Sie können alle verhaltensbezogenen Ereignisdaten, die Sie in Adobe Analytics bereits erfassen und an Adobe Experience Platform streamen, nutzen, um Echtzeit-Journeys auszulösen und Erlebnisse für Ihre Kunden zu automatisieren. Diese Daten können auch verwendet werden, um Segmente zu erstellen, die mit Journey Optimizer interagiert werden können.

Weitere Informationen [Journey Optimizer + Analytics](../event/about-analytics.md).

## Adobe Intelligent Services{#integration-intelligent-service}

Mit den nativen Adobe Intelligent Services der Echtzeit-Kundendatenplattform können Sie die Leistungsfähigkeit von künstlicher Intelligenz und maschinellem Lernen in Anwendungsfällen mit Kundenerlebnissen nutzen. So können Marketing-Analysten mithilfe von Konfigurationen auf Unternehmensebene spezifische Prognosen für die Anforderungen eines Unternehmens erstellen, ohne dass datenwissenschaftliche Kenntnisse erforderlich sind.

Mit Customer AI können Marken auf maschinellem Lernen basierende Abwanderungs- oder Konversionswerte erstellen, die als Profilattribute in Adobe Experience Platform verfügbar sind und zur Personalisierung einer Journey verwendet werden können.

[Weitere Infos](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

Wenn Sie über Adobe Campaign v7 oder v8 verfügen, ist eine Integration verfügbar. Verwenden Sie diese Integration, um E-Mails, Push-Benachrichtigungen und SMS mithilfe der Transaktionsnachrichten-Funktionen von Adobe Campaign zu versenden.

Weitere Informationen [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Sie können auch eine Integration mit Adobe Campaign Standard einrichten, um Nachrichten in Ihren Journeys zu senden.

Weitere Informationen [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Benutzerdefinierte Kanäle{#integration-custom}

Wenn Sie zum Senden von Nachrichten ein Drittanbietersystem verwenden oder möchten, dass Journeys API-Aufrufe an ein Drittanbietersystem senden, verwenden Sie benutzerdefinierte Aktionen, um eine Verbindung zu Ihrer Journey herzustellen. Sie können beispielsweise mit benutzerdefinierten Aktionen eine Verbindung zu den folgenden Systemen herstellen: Epsilon, Slack, [Adobe-Entwickler](https://developer.adobe.com){target=&quot;_blank&quot;}, Firebase usw.

Benutzerdefinierte Aktionen sind zusätzliche Aktionen, die von technischen Benutzern definiert und Marketing-Experten zur Verfügung gestellt werden. Nach der Konfiguration werden sie in der linken Palette Ihrer Journey im **[!UICONTROL Action]** Kategorie. Weitere Informationen finden Sie unter [diese Seite](../building-journeys/about-journey-activities.md#action-activities).

Weitere Informationen [benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md).

## Externe Datenquellen{#integration-external-systems}

Mit Journey Optimizer können Sie Verbindungen zu externen Systemen über benutzerdefinierte Datenquellen und benutzerdefinierte Aktionen konfigurieren. Auf diese Weise können Sie beispielsweise Ihre Journeys mit Daten aus einem externen Reservierungssystem anreichern.

Erfahren Sie, wie Sie mit externen Datenquellen eine Verbindung zu einem Drittanbietersystem definieren können in [diesem Abschnitt](../datasource/external-data-sources.md).
