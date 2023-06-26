---
solution: Journey Optimizer
product: journey optimizer
title: Reaktionsereignisse
description: Informationen über Reaktionsereignisse
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Ereignisse, Reaktion, Tracking, Plattform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: b011b979aaab7568ca951982a59ad676d05c5595
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Reaktionsereignisse {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reaktionsereignisse"
>abstract="Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit in dem Moment, in dem sie an Adobe Experience Platform weitergegeben werden."

Unter den verschiedenen Ereignisaktivitäten, die in der Palette verfügbar sind, finden Sie das integrierte **[!UICONTROL Reaktionsereignis]**. Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit in dem Moment, in dem sie an Adobe Experience Platform weitergegeben werden.

Sie können auf angeklickte oder geöffnete Nachrichten reagieren.

Sie können diesen Mechanismus auch verwenden, um eine Aktion auszuführen, wenn keine Reaktion auf Ihre Nachrichten erfolgt. Erstellen Sie dazu einen zweiten Pfad parallel zur Reaktionsaktivität und fügen Sie eine Warteaktivität hinzu. Wenn während des in der Warteaktivität definierten Zeitraums keine Reaktion erfolgt, wird der zweite Pfad ausgewählt. Sie können beispielsweise eine Folgenachricht senden.

Beachten Sie, dass Sie auf der Arbeitsfläche eine Reaktionsaktivität nur dann verwenden können, wenn zuvor eine Kanalaktionsaktivität stattgefunden hat (E-Mail oder Push-Benachrichtigung).

Siehe [Informationen zu Aktionsaktivitäten](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

Im Folgenden werden die verschiedenen Schritte zum Konfigurieren der Reaktionsereignisse beschrieben:

1. Fügen Sie der Reaktion einen **[!UICONTROL Titel]** hinzu. Dieser Schritt ist optional.
1. Wählen Sie aus der Dropdown-Liste die Aktionsaktivität aus, auf die Sie reagieren möchten. Sie können jede Aktionsaktivität auswählen, die in den vorherigen Schritten des Pfades platziert wurde.
1. Wählen Sie je nach ausgewählter Aktion, auf was Sie reagieren möchten.
1. Sie können die maximale Wartezeit für ein Ereignis (zwischen 40 Sekunden und 30 Tagen) und einen Pfad für die maximale Wartezeit definieren. Dadurch wird ein zweiter Pfad für Personen erstellt, die nicht während der festgelegten Zeitspanne reagiert haben. Beim Testen einer Journey, die ein Reaktionseeignis verwendet, beträgt der Standard- und Mindestwert für die **[!UICONTROL Wartezeit]** im Testmodus 40 Sekunden. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Reaktionsereignisse können Meldungen, die in einer anderen Journey stattfinden, nicht verfolgen.
>
>Reaktionsereignisse verfolgen Klicks auf Links des Typs „verfolgt“. Abmeldungs- und Mirrorseiten-Links werden nicht berücksichtigt.

>[!IMPORTANT]
>
>E-Mail-Clients wie Gmail erlauben die Blockierung von Bildern. E-Mail-Öffnungen werden anhand eines in der E-Mail enthaltenen 0-Pixel-Bildes nachverfolgt. Wenn Bilder blockiert werden, wird das Öffnen von E-Mails nicht berücksichtigt.
