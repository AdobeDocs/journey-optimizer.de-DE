---
solution: Journey Optimizer
product: journey optimizer
title: Integration mit anderen Lösungen
description: Erfahren Sie mehr über die Integration von Journey Optimizer in andere Lösungen.
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 4899dbe71243184b6283a32a4fe7eb2edb82f872
workflow-type: ht
source-wordcount: '709'
ht-degree: 100%

---

# Integration mit anderen Lösungen {#integration}

Mit Adobe Journey Optimizer können Sie diese Daten einfach verwalten, speichern und in Plattformen oder Systeme exportieren, die Teil Ihres Technologie-Stacks sind. Mithilfe dieser Integrationen können Sie Ihre spezifischen Anwendungsfälle abdecken und den Funktionsumfang von Adobe Journey Optimizer erweitern.

>[!NOTE]
>
> Adobe Journey Optimizer basiert auf Adobe Experience Platform und ist nativ mit dem [Adobe Echtzeit-Kundenprofil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"} verbunden. Diese integrierte Datenquelle ist vorkonfiguriert und dient dem Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofil (beispielsweise um zu überprüfen, ob die Person, die an einer Journey teilgenommen hat, ein Kunde ist oder nicht). Sie ermöglicht Ihnen die Verwendung von Profildaten und Erlebnisereignisdaten. [Weitere Informationen](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Mit Customer Journey Analytics können Sie erweiterte Analysen der von Journey Optimizer generierten Daten durchführen.

Journey Optimizer speichert Daten in Adobe Experience Platform und bietet mit Customer Journey Analytics eine ganzheitliche Sicht auf alle Ihre Journeys, Kampagnen und Angebote mit automatisierter Berichtverteilung und benutzerdefinierten Datenvisualisierungen.

Nach der Erstellung Ihrer Journey in Journey Optimizer kann Customer Journey Analytics Daten aus der Plattform aufnehmen, um Berichte zu erstellen und die Auswirkungen jeder Interaktion eines Kunden mit Ihren Journeys zu verstehen.

Weitere Informationen über [Journey Optimizer und Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics {#integration-aa}

Sie können alle bereits erfassten und in die Adobe Experience Platform gestreamten verhaltensbezogenen Ereignisdaten aus Adobe Analytics nutzen, um in Echtzeit Journeys auszulösen und Erlebnisse für Ihre Kunden zu automatisieren. Diese Daten können auch verwendet werden, um Zielgruppen zu erstellen, die mithilfe von Journey Optimizer einbezogen werden können.

Weitere Informationen über [Journey Optimizer und Analytics](../event/about-analytics.md).


## Adobe Experience Manager Assets {#integration-assets}

Zusammenführen von Marketing- und Kreativ-Workflows mithilfe von [!DNL Adobe Experience Manager Assets]. Nutzen Sie [!DNL Adobe Experience Manager Assets], das nativ mit [!DNL Adobe Journey Optimizer] integriert ist, um digitale Assets zu speichern, zu verwalten, zu erkunden und weiterzugeben. Dies bietet ein zentrales Repository für Assets, die Sie für Ihre Nachrichten verwenden können.

[!DNL Adobe Experience Manager Assets] kann direkt von [!DNL Adobe Journey Optimizer] aus über den Abschnitt **[!UICONTROL Assets]** im linken Menü aufgerufen werden.

Erfahren Sie mehr über [Journey Optimizer + Adobe Experience Manager Assets](../content-management/assets.md).


## Adobe Stock {#integration-stock}

Das Plug-in für die Integration von E-Mail-Designer mit [!DNL Adobe Stock] und [!DNL Adobe Journey Optimizer] bietet Kundinnen und Kunden eine einfache Möglichkeit, zur Nachrichtenerstellung durch Bilder zu navigieren, sie zu lizenzieren und sie zu speichern.

Mit [!DNL Adobe Journey Optimizer] können Sie Bilder direkt aus [!DNL Adobe Stock] in Ihre E-Mails hochladen und mit der Option **[!UICONTROL Adobe Stock-Fotos suchen]** zu Ihrem Ordner **[!UICONTROL Assets]** hinzufügen. Darüber hinaus hilft Ihnen die Option **[!UICONTROL Ähnliche Stockfotos suchen]**, Bilder zu finden, die in Inhalt, Farbe und Komposition dem in Ihrem Versand verwendeten Asset entsprechen.

Erfahren Sie mehr über [Journey Optimizer + Stock](../content-management/stock.md).


## Adobe Intelligent Services {#integration-intelligent-service}

Mit Adobe Intelligent Services, die in der Echtzeit-Kundendatenplattform integriert sind, können Sie die Leistungsfähigkeit von künstlicher Intelligenz und maschinellem Lernen in Anwendungsfällen für Kundenerlebnisse nutzen. So können Marketing-Analystinnen und -Analysten mithilfe von Konfigurationen auf geschäftlicher Ebene spezifische Prognosen für die Anforderungen der Firma erstellen, ohne dass hierfür Kenntnisse aus der Datenwissenschaft erforderlich sind.

Mit Kunden-KI können Marken auf maschinellem Lernen basierende Abwanderungs- oder Konversionswerte erstellen, die als Profilattribute in Adobe Experience Platform verfügbar sind und zur Personalisierung einer Journey verwendet werden können.

[Weitere Informationen](../building-journeys/ai-services-overview.md).


## Adobe Campaign {#integration-ac}

Für Adobe Campaign v7 und v8 ist eine Integration verfügbar. Diese Integration ermöglicht Ihnen das Senden von E-Mails, Push-Benachrichtigungen und SMS mithilfe der Transaktionsnachrichtenfunktionen von Adobe Campaign 

Weitere Informationen zu [Journey Optimizer und Campaign](../building-journeys/ajo-ac.md).

Sie können auch eine Integration mit Adobe Campaign Standard einrichten, um Nachrichten in Ihren Journeys zu senden.

Weitere Informationen zu [Journey Optimizer und Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).

## Benutzerdefinierte Kanäle {#integration-custom}

Wenn Sie ein Drittanbietersystem für das Versenden von Nachrichten verwenden oder wenn Sie möchten, dass von Journeys API-Aufrufe an ein Drittanbietersystem gesendet werden, verwenden Sie benutzerdefinierte Aktionen, um die Verbindung zwischen dem System und Ihrer Journey zu konfigurieren. Sie können mit benutzerdefinierten Aktionen beispielsweise eine Verbindung zu den folgenden Systemen herstellen: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase usw.

Benutzerdefinierte Aktionen sind zusätzliche Aktionen, die von technischen Benutzern definiert und Marketing-Experten zur Verfügung gestellt werden. Nach der Konfiguration erscheinen sie in der linken Palette Ihrer Journey in der Kategorie **[!UICONTROL Aktion]**. Weiterführende Informationen finden Sie auf [dieser Seite](../building-journeys/about-journey-activities.md#action-activities).

Weitere Informationen über [benutzerdefinierte Aktionen](../action/about-custom-action-configuration.md).

## Externe Datenquellen {#integration-external-systems}

Mit Journey Optimizer können Sie Verbindungen zu externen Systemen über benutzerdefinierte Datenquellen und Aktionen konfigurieren. So können Sie beispielsweise Ihre Journey mit Daten aus einem externen Reservierungssystem anreichern.

Erfahren Sie in [diesem Abschnitt](../datasource/external-data-sources.md), wie Sie mit externen Datenquellen eine Verbindung zu einem Drittanbietersystem definieren können.
