---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journeys
feature: Journeys
role: User
level: Beginner
keywords: Journey, Entdecken, erste Schritte
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: cd154b137d7b4e5a3b35948241d2bbbb18265903
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 100%

---


# Erste Schritte mit Journeys{#jo-general-principle}

Bitte [!DNL Journey Optimizer] verwenden, um Anwendungsfälle für die Echtzeit-Orchestrierung mithilfe von kontextuellen Daten aus Ereignissen oder Datenquellen zu erstellen.

Erstellen Sie mehrstufige fortgeschrittene Szenarien mit folgenden Funktionen:

* Führen Sie einen **unitären Versand** in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder **im Batch** unter Verwendung von Adobe Experience Platform-Segmenten.

* Nutzen Sie **kontextuelle Daten** aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

* Verwenden Sie die **integrierten Aktionen** zum Senden von in [!DNL Journey Optimizer] entworfenen Nachrichten oder erstellen Sie **benutzerspezifische Aktionen**, wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden.

* Erstellen Sie mit dem **Journey Designer** Ihre mehrstufigen Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität zum Lesen von Segmenten in den Arbeitsbereich, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

## Schritte zum Erstellen einer Journey{#steps-journey}

Verwenden Sie Adobe Journey Optimizer, um personalisierte Journeys auf einer einzigen Arbeitsfläche zu entwerfen und zu orchestrieren. Die wichtigsten Schritte zum Erstellen einer Journey sind wie folgt:

![](assets/journey-creation-process.png)

Adobe Journey Optimizer verfügt über eine Arbeitsfläche für die Omnichannel-Orchestrierung, mit der Marketing-Experten Marketing-Maßnahmen mit Eins-zu-eins-Kundeninteraktionen aufeinander abstimmen können. Die Benutzeroberfläche ermöglicht es, Aktivitäten einfach von der Palette in die Arbeitsfläche zu ziehen, um eine Journey zu erstellen.

![](assets/interface-journeys.png)

Auf [dieser Seite](journey-gs.md) finden sich Informationen zum Erstellen der ersten Journey.

Der Omnichannel-Journey-Designer hilft bei der Erstellung mehrstufiger Journeys – mit entsprechenden Zielgruppen, Aktualisierungen basierend auf Echtzeit-Kunden- bzw. Geschäftsinteraktionen sowie Omnichannel-Nachrichten mithilfe einer intuitiven Drag-&amp;-Drop-Oberfläche.

![](assets/journey38.png)

Weiterführende Informationen finden sich in [diesem Abschnitt](using-the-journey-designer.md).

Für Data Engineers werden die Schritte zur Konfiguration der Journeys, einschließlich Datenquellen, Ereignissen und Aktionen, in [diesem Abschnitt](../configuration/about-data-sources-events-actions.md) beschrieben.


## Anwendungsfälle{#uc-journey}

In den folgenden End-to-End-Anwendungsfällen wird das Erstellen von Journeys erläutert.

Geschäftliche Anwendungsfälle:

* [Senden von Multi-Channel-Nachrichten](journeys-uc.md)
* [Senden einer Nachricht mit Campaign v7/v8](ajo-ac.md)
* [Senden einer Nachricht an Abonnenten](message-to-subscribers-uc.md)

Technische Anwendungsfälle:

* [Dynamisches Übergeben von Sammlungen mithilfe benutzerdefinierter Aktionen](collections.md)
* [Steigern der Versandaktivität](ramp-up-deliveries-uc.md)
* [Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen](limit-throughput.md)

## Journey-Versionen{#journey-versions}

In der Liste der Journeys werden alle Journey-Versionen mit der Versionsnummer angezeigt. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/using-the-journey-designer.md).

Wenn Sie nach einer Journey suchen, werden beim ersten Öffnen der Anwendung die neuesten Versionen oben in der Liste angezeigt. Anschließend können Sie die gewünschte Sortierung definieren und die Anwendung behält sie als Benutzervoreinstellung bei. Die Version der Journey wird auch oben auf der Benutzeroberfläche zum Bearbeiten der Journey (oberhalb der Arbeitsfläche) angezeigt.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In der Regel kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](end-journey.md).

Wenn eine Live-Journey geändert werden muss, bitte eine neue Version der Journey erstellen.

1. Öffnen Sie die aktuelle Version Ihrer Live-Journey, klicken Sie auf **[!UICONTROL Neue Version erstellen]** und bestätigen Sie.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Sie können nur aus der aktuellen Version einer Journey eine neue Journey erstellen.

1. Nehmen Sie Ihre Änderungen vor, klicken Sie auf **[!UICONTROL Veröffentlichen]** und bestätigen Sie.

   ![](assets/journeyversions3.png)

Ab dem Zeitpunkt der Veröffentlichung der Journey nehmen Kontakte an der neuen Version der Journey teil. Personen, die bereits an einer früheren Version teilnehmen, bleiben in ihr, bis sie die Journey beenden. Wenn sie später wieder in dieselbe Journey eintreten, wechseln sie in die aktuelle Version.

Journey-Versionen können einzeln gestoppt werden. Alle Versionen von Journeys haben denselben Namen.

Wenn Sie eine neue Version einer Journey veröffentlichen, endet die vorherige Version automatisch und wechselt in den Status **Geschlossen**. Es kann kein Eintritt in die Journey stattfinden. Selbst wenn Sie die aktuelle Version stoppen, bleibt die vorherige Version geschlossen.

>[!NOTE]
>
>Weitere Informationen zu den Schutzmechanismen und Einschränkungen von Journey-Versionen finden Sie auf [dieser Seite](../start/guardrails.md#journey-versions-limitations)