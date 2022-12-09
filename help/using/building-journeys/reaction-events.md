---
solution: Journey Optimizer
product: journey optimizer
title: Reaktionsereignisse
description: Informationen zu Reaktionsereignissen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
source-git-commit: 9b7898d0fe008a0e7ef711b1303230c6f901b712
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Reaktionsereignisse {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reaktionsereignisse"
>abstract="Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine in derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für Adobe Experience Platform freigegeben werden."

Unter den verschiedenen Ereignisaktivitäten, die in der Palette verfügbar sind, finden Sie die **[!UICONTROL Reactions]** -Ereignis. Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine in derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für Adobe Experience Platform freigegeben werden.

Sie können auf angeklickte oder geöffnete Nachrichten reagieren.

Sie können diesen Mechanismus auch verwenden, um eine Aktion durchzuführen, wenn auf Ihre Nachrichten keine Reaktion erfolgt. Erstellen Sie dazu einen zweiten Pfad parallel zur Reaktionsaktivität und fügen Sie eine Warteaktivität hinzu. Wenn während des in der Warteaktivität definierten Zeitraums keine Reaktion erfolgt, wird der zweite Pfad ausgewählt. Sie können beispielsweise eine Folgenachricht senden.

Beachten Sie, dass Sie eine Reaktionsaktivität auf der Arbeitsfläche nur verwenden können, wenn zuvor eine Kanalaktionsaktivität aufgetreten ist (E-Mail und Push-Benachrichtigung).

Siehe [Über Aktionsaktivitäten](../building-journeys/about-journey-activities.md#action-activities).

![](assets/journey45.png)

Im Folgenden werden die verschiedenen Schritte zum Konfigurieren der Reaktionsereignisse beschrieben:

1. Hinzufügen einer **[!UICONTROL Label]** auf die Reaktion. Dieser Schritt ist optional.
1. Wählen Sie aus der Dropdown-Liste die Aktionsaktivität aus, auf die Sie reagieren möchten. Sie können jede Aktionsaktivität auswählen, die in den vorherigen Schritten des Pfads positioniert wurde.
1. Wählen Sie je nach ausgewählter Aktion aus, worauf Sie reagieren möchten.
1. Sie können einen Ereignis-Timeout (zwischen 40 und 30 Tagen) und einen Timeout-Pfad definieren. Dadurch wird ein zweiter Pfad für Personen erstellt, die nicht innerhalb der definierten Dauer reagiert haben. Beim Testen einer Journey, die ein Reaktionsereignis verwendet, wird der Testmodus **[!UICONTROL Wait time]** Standardwert und Mindestwert sind 40 Sekunden. Siehe [diesem Abschnitt](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Reaktionsereignisse können keine Nachrichten verfolgen, die in einer anderen Journey stattfinden.
>
>Reaktionsereignisse verfolgen Klicks auf Links des Typs &quot;verfolgt&quot;. Abmelde- und Mirrorseiten-Links werden nicht berücksichtigt.

>[!IMPORTANT]
>
>E-Mail-Clients wie Gmail erlauben die Blockierung von Bildern. Das Öffnen von E-Mails wird mit einem 0-Pixel-Bild verfolgt, das in der E-Mail enthalten ist. Wenn Bilder blockiert werden, werden E-Mail-Öffnungen nicht berücksichtigt.
