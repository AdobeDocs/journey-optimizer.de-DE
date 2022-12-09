---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journeys
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---


# Erste Schritte mit Journeys{#jo-general-principle}

Verwendung [!DNL Journey Optimizer] zum Erstellen von Anwendungsfällen für die Echtzeit-Orchestrierung der Customer Journey mithilfe von Kontextdaten, die in Ereignissen oder Datenquellen gespeichert sind.

Erstellen Sie mehrstufige erweiterte Szenarien mit folgenden Funktionen:

* Echtzeit-Versand **Einzelversand** ausgelöst wird, wenn ein Ereignis empfangen wird, oder **in Batch** Verwendung von Adobe Experience Platform-Segmenten.

* Nutzung **Kontextdaten** aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Diensten von Drittanbietern.

* Verwenden Sie die **integrierte Aktionen** zum Senden von Nachrichten, die in [!DNL Journey Optimizer] oder erstellen **benutzerdefinierte Aktionen** wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden.

* Mit dem **Journey-Designer**, erstellen Sie Ihre mehrstufigen Anwendungsfälle: Fügen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität vom Typ Segment lesen hinzu, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

## Schritte zum Erstellen einer Journey{#steps-journey}

Verwenden Sie Adobe Journey Optimizer, um personalisierte Journeys aus einer einzigen Arbeitsfläche zu entwerfen und zu orchestrieren.

Adobe Journey Optimizer enthält eine Arbeitsfläche für die Omnichannel-Orchestrierung, die es Marketing-Experten ermöglicht, die Marketing-Interaktion mit einer Eins-zu-Eins-Kundeninteraktion zu harmonisieren. Über die Benutzeroberfläche können Sie Aktivitäten einfach aus der Palette in die Arbeitsfläche ziehen, um Ihre Journey zu erstellen.

![](assets/interface-journeys.png)

Erfahren Sie, wie Sie Ihre erste Journey in starten und erstellen [diese Seite](journey-gs.md).

Mit dem Omnichannel-Journey-Designer können Sie mehrstufige Journeys mit zielgerichteten Zielgruppen, Aktualisierungen basierend auf Echtzeit-Kunden- oder Geschäftsinteraktionen und Omnichannel-Nachrichten mithilfe einer intuitiven Drag &amp; Drop-Oberfläche erstellen.

![](assets/journey38.png)

Mehr dazu in [diesem Abschnitt](using-the-journey-designer.md).

Die Schritte zum Konfigurieren Ihrer Journeys, einschließlich Datenquellen, Ereignissen und Aktionen, werden als Data Engineer im Abschnitt [diesem Abschnitt](../configuration/about-data-sources-events-actions.md).


## Anwendungsbeispiele{#uc-journey}

In den folgenden durchgehenden Anwendungsfällen erfahren Sie, wie Sie Journeys erstellen.

Anwendungsfälle für Unternehmen:

* [Senden von kanalübergreifenden Nachrichten](journeys-uc.md)
* [Nachricht mit Campaign v7/v8 senden](ajo-ac.md)
* [Nachricht an Abonnenten senden](message-to-subscribers-uc.md)

Technische Anwendungsfälle:

* [Dynamisches Übergeben von Sammlungen mithilfe benutzerdefinierter Aktionen](collections.md)
* [Sendungen vorantreiben](ramp-up-deliveries-uc.md)
* [Begrenzen des Durchsatzes mit externen Datenquellen und benutzerdefinierten Aktionen](limit-throughput.md)

## Journey-Versionen{#journey-versions}

In der Liste der Journeys werden alle Journey-Versionen mit der Versionsnummer angezeigt. Siehe [diese Seite](../building-journeys/using-the-journey-designer.md).

Wenn Sie nach einer Journey suchen, werden beim ersten Öffnen der Anwendung die neuesten Versionen oben in der Liste angezeigt. Anschließend können Sie die gewünschte Sortierung definieren und die Anwendung behält sie als Benutzervoreinstellung bei. Die Version der Journey wird auch oben auf der Benutzeroberfläche zur Journey-Bearbeitung über der Arbeitsfläche angezeigt.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Normalerweise kann ein Profil nicht mehrmals in derselben Journey gleichzeitig vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, dies jedoch erst tun, wenn er die vorherige Instanz der Journey vollständig verlassen hat. [Mehr dazu](end-journey.md).

Wenn Sie eine Live-Journey ändern müssen, erstellen Sie eine neue Version Ihrer Journey.

1. Öffnen Sie die neueste Version Ihrer Live-Journey und klicken Sie auf **[!UICONTROL Create a new version]** und bestätigen Sie.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Sie können nur eine neue Version aus der neuesten Version einer Journey erstellen.

1. Nehmen Sie Ihre Änderungen vor, klicken Sie auf **[!UICONTROL Publish]** und bestätigen Sie.

   ![](assets/journeyversions3.png)

Ab dem Zeitpunkt der Veröffentlichung der Journey beginnen Kontakte, in die aktuelle Version der Journey zu gelangen. Personen, die bereits eine frühere Version eingegeben haben, verbleiben darin, bis sie die Journey beenden. Wenn sie später wieder in dieselbe Journey eintreten, wechseln sie zur neuesten Version.

Journey-Versionen können einzeln angehalten werden. Alle Versionen von Journeys haben denselben Namen.

Wenn Sie eine neue Version einer Journey veröffentlichen, endet die vorherige Version automatisch und wechselt zur **Geschlossen** Status. Es kann kein Eintritt in die Journey stattfinden. Auch wenn Sie die neueste Version stoppen, bleibt die vorherige Version geschlossen.

>[!NOTE]
>
>Erfahren Sie mehr über die Limits und Einschränkungen von Journey-Versionen in [diese Seite](../start/guardrails.md#journey-versions-limitations)