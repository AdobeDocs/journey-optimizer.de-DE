---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen Ihrer ersten Journey
description: Wichtige Schritte zum Erstellen Ihrer ersten Journey mit Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: Journey, erste, Start, Schnellstart, Zielgruppe, Ereignis, Aktion
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 93dab17fc74396887e3b68051be777645e02709f
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 45%

---

# Erstellen Ihrer ersten Journey {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Erstellen von Journeys"
>abstract="Erstellen Sie mit **Adobe Journey Optimizer** anhand von in Ereignissen oder Datenquellen gespeicherten kontexbezogenen Daten Echtzeit-Orchestrierungsfälle."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Journeys"
>abstract="Entwerfen Sie Customer Journeys, um Ihren Kundinnen und Kunden personalisierte, kontextuelle Erlebnisse zu bieten. Mit Journey Optimizer können Sie anhand von in Ereignissen oder Datenquellen gespeicherten kontextbezogenen Daten Echtzeit-Orchestrierungsfälle erstellen. In der Registerkarte **Übersicht** wird ein Dashboard mit Schlüsselmetriken zu Ihren Journeys angezeigt. Auf der Registerkarte **Durchsuchen** wird eine Liste der vorhandenen Journeys angezeigt."

Adobe Journey Optimizer verfügt über eine Arbeitsfläche für die Omnichannel-Orchestrierung, mit der Marketing-Experten Marketing-Maßnahmen mit Eins-zu-eins-Kundeninteraktionen aufeinander abstimmen können. Die Benutzeroberfläche ermöglicht es, Aktivitäten einfach von der Palette in die Arbeitsfläche zu ziehen, um eine Journey zu erstellen. Die Benutzeroberfläche von Journey wird auf [ Seite beschrieben](journey-ui.md).

![Beispiel einer Journey-Arbeitsfläche](assets/journey38.png)


Die wichtigsten Schritte zum Erstellen einer Journey werden auf dieser Seite beschrieben. Sie werden wie folgt gestrafft:

![Schritte zur Erstellung von Journey: Erstellen, Entwerfen, Testen und Veröffentlichen](assets/journey-creation-process.png)


Erstellen Sie mehrstufige Kunden-Journey, um eine Abfolge von Interaktionen, Angeboten und Nachrichten kanalübergreifend in Echtzeit zu initiieren. Dieser Ansatz stellt sicher, dass Kunden zu optimalen Zeitpunkten auf der Grundlage ihrer Aktionen und relevanten Geschäftssignale eingebunden werden. Zielgruppen können basierend auf Verhalten, kontextuellen Daten und Geschäftsereignissen definiert werden. Die Voraussetzungen hängen von Ihrem Anwendungsfall und dem [Typ von Journey](entry-management.md#types-of-journeys) ab, den Sie erstellen. Bevor Sie mit der Entwicklung Ihres Journey beginnen, überprüfen Sie, ob die entsprechenden Konfigurationsschritte ausgeführt wurden:

* Wenn Sie Ihre Journey-Trigger beim Empfang eines Ereignisses einheitlich ausführen möchten, müssen Sie **ein Ereignis konfigurieren**. Sie definieren die erwarteten Informationen sowie deren Verarbeitungsmethode. [Weitere Informationen](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Ihr Journey kann auch Adobe Experience Platform-Zielgruppen überwachen, um Nachrichten als Batch an einen bestimmten Profilsatz zu senden. Dazu müssen Sie **Zielgruppen erstellen**. [Weitere Informationen](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* Sie können eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Journey abzurufen (z. B. in Ihren Bedingungen). Diese Verbindung beruht auf einer **Datenquelle**. [Weitere Informationen](../datasource/about-data-sources.md)

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer verfügt [ integrierte ](../building-journeys/journeys-message.md). Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie **eine benutzerdefinierte Aktion erstellen**. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Für Data Engineers werden die Schritte zur Konfiguration der Journeys, einschließlich Datenquellen, Ereignissen und Aktionen, in [diesem Abschnitt](../configuration/about-data-sources-events-actions.md) beschrieben.


>[!NOTE]
>
>Leitlinien und Einschränkungen für Journeys werden auf [dieser Seite](../start/guardrails.md) detailliert behandelt.

## Erstellen einer Journey {#jo-build}

Gehen Sie wie folgt vor, um eine mehrstufige Journey zu erstellen:

1. Klicken Sie im Menüabschnitt JOURNEY-VERWALTUNG auf **[!UICONTROL Journey]**.

1. Klicken Sie auf **[!UICONTROL Journey erstellen]**, um eine neue Journey zu erstellen.

1. Bearbeiten Sie den Konfigurationsbereich des Journey-Bereichs, um den Namen der Journey zu definieren und ihre Eigenschaften festzulegen. Auf dieser Seite erfahren Sie, wie Sie Ihre Journey-Eigenschaften [](journey-properties.md).

   ![](assets/jo-properties.png)

Anschließend können Sie mit der Gestaltung Ihres Journey beginnen.

## Entwerfen der Journey {#jo-design}

Der Omnichannel-Journey-Designer hilft bei der Erstellung mehrstufiger Journeys – mit entsprechenden Zielgruppen, Aktualisierungen basierend auf Echtzeit-Kunden- bzw. Geschäftsinteraktionen sowie Omnichannel-Nachrichten mithilfe einer intuitiven Drag-&amp;-Drop-Oberfläche.

![](assets/journey38.png)

1. Ziehen Sie zuerst ein Ereignis oder die Aktivität **Zielgruppe lesen** per Drag-and-Drop aus der Palette in die Arbeitsfläche. Weitere Informationen zum Entwerfen von Journeys finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Ziehen Sie die nächsten Schritte, die der Kontakt ausführen soll, per Drag-and-Drop. Sie können beispielsweise eine Bedingung und anschließend eine Kanalaktion hinzufügen. Weitere Informationen zu Aktivitäten finden Sie in [diesem Abschnitt](about-journey-activities.md).

## Testen der Journey {#jo-test}

Nachdem Sie Ihren Journey erstellt haben, können Sie ihn vor dem Veröffentlichen testen. Journey Optimizer bietet den „Testmodus“ als Möglichkeit, Testprofile anzuzeigen, während sie sich auf der Journey bewegen, und potenzielle Fehler vor der Aktivierung zu erkennen. Wenn Sie Schnelltests ausführen, können Sie überprüfen, ob die Journey ordnungsgemäß funktionieren, sodass Sie sie sicher veröffentlichen können.

Weitere Informationen finden Sie in diesem [Abschnitt](testing-the-journey.md)

## Veröffentlichen der Journey {#jo-pub}

Sie müssen eine Journey veröffentlichen, um sie zu aktivieren, und sie für neue Profile verfügbar machen, damit diese sie eingeben können. Vergewissern Sie sich vor der Veröffentlichung, dass die Journey gültig ist und keine Fehler vorliegen. Es ist nicht möglich, eine fehlerhafte Journey zu veröffentlichen. Weitere Informationen zur Journey-Publikation finden Sie in [Abschnitt](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Nach der Veröffentlichung können Sie Ihre Journey mit den dedizierten Reporting-Tools überwachen, um ihre Effektivität zu messen.

![](assets/jo-dynamic_report_journey_12.png)

Weitere Informationen zum Journey von Berichten finden Sie in [Abschnitt](../reports/live-report.md).

>[!NOTE]
>
>Wenn Sie eine Live **Journey ändern müssen** erstellen Sie [eine neue Version](journey-ui.md#journey-versions) Ihrer Journey.
