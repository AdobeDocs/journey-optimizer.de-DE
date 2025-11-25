---
solution: Journey Optimizer
product: journey optimizer
title: Reaktionsereignisse
description: Erfahren Sie, wie Sie mit Reaktionsereignissen auf Nachrichten-Tracking-Daten wie Öffnungen und Klicks in Ihren Journey reagieren und Zeitüberschreitungspfade für Nicht-Responder konfigurieren können.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Ereignisse, Reaktion, Tracking, Plattform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: d8fa1c7055e4e31e393e36ba16863e0f8f95ca9b
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 48%

---

# Reaktionsereignisse {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reaktionsereignisse"
>abstract="Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit in dem Moment, in dem sie an Adobe Experience Platform weitergegeben werden."

## Überblick {#overview}

Unter den verschiedenen Ereignisaktivitäten, die in der Palette verfügbar sind, finden Sie das integrierte **[!UICONTROL Reaktionsereignis]**. Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit in dem Moment, in dem sie an Adobe Experience Platform weitergegeben werden.

Sie können auf angeklickte oder geöffnete Nachrichten reagieren. Sie können beispielsweise eine weitere Nachricht senden, wenn eine Person die vorherige E-Mail geöffnet oder darin geklickt hat, oder eine andere Folgenachricht senden, wenn sie nicht mit Ihrer Kommunikation interagiert hat.

Siehe [Aktionsaktivitäten](../building-journeys/about-journey-activities.md#action-activities).

Sie können die Aktivität **[!UICONTROL Reaktion]** verwenden, um eine Aktion auszuführen, wenn es keine Reaktion auf Ihre Nachrichten gibt. Erstellen Sie dazu einen zweiten Pfad parallel zur Aktivität **[!UICONTROL Reaktion]** und fügen Sie eine Aktivität **[!UICONTROL Warten“]**. Wenn während des in der Aktivität **[!UICONTROL Warten“ definierten Zeitraums keine Reaktion]**, wird der zweite Pfad ausgewählt. Sie können beispielsweise eine Folgenachricht senden.

## Konfigurieren von Reaktionsereignissen {#configure}

![Konfiguration des Reaktionsereignisses mit Optionen zur Kanalauswahl und zum Ereignistyp](assets/journey45.png)

Führen Sie die folgenden Schritte aus, um die Reaktionsereignisse zu konfigurieren:

1. Platzieren Sie **[!UICONTROL Reaktion]** Aktivität **sofort** nach einer [Kanalaktionsaktivität](journeys-message.md) auf der Journey-Arbeitsfläche.
1. Fügen Sie der Reaktion ein **[!UICONTROL Label]** hinzu. Dieser Schritt ist optional.
1. Wählen Sie aus der Dropdown-Liste die Aktionsaktivität aus, auf die Sie reagieren möchten. Sie können jede Aktionsaktivität auswählen, die in den vorherigen Schritten des Pfades platziert wurde.
1. Wählen Sie je nach ausgewählter Aktion, auf was Sie reagieren möchten.
1. Sie können das Timeout für ein Ereignis (zwischen 40 Sekunden und 90 Tagen) und einen Timeout-Pfad definieren. Dadurch wird ein zweiter Pfad für Personen erstellt, die nicht innerhalb der festgelegten Zeitspanne reagiert haben. Beim Testen einer Journey, die ein Reaktionseeignis verwendet, beträgt der Standard- und Mindestwert für die **[!UICONTROL Wartezeit]** im Testmodus 40 Sekunden. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/testing-the-journey.md).

## Leitlinien und Einschränkungen {#guardrails-limitations}

* Eine **[!UICONTROL Reaktion]**-Aktivität muss **unmittelbar** nach einer [Kanalaktionsaktivität) auf &#x200B;](journeys-message.md) Journey-Arbeitsfläche platziert werden.
* Eine Aktivität vom Typ **[!UICONTROL Reaktion]** kann nur verwendet werden, wenn zuvor eine Kanalaktionsaktivität stattgefunden hat.
* Das Platzieren einer **[!UICONTROL Warten]**-Aktivität oder einer anderen Aktivität zwischen der Kanalaktion und der **[!UICONTROL Reaktion]**-Aktivität wird nicht unterstützt und kann dazu führen, dass die Reaktion nicht wie erwartet funktioniert.
* Reaktionsereignisse können nur Nachrichten verfolgen, die innerhalb derselben Journey gesendet werden. Nachrichten, die auf einer anderen Journey stattfinden, können nicht verfolgt werden.
* Reaktionsereignisse verfolgen Klicks auf Links des Typs „verfolgt“. Abmeldungs- und Mirrorseiten-Links werden nicht berücksichtigt.
* Das Öffnen von E-Mails wird anhand eines in der E-Mail enthaltenen 0-Pixel-Bildes nachverfolgt. Wenn E-Mail-Clients (z. B. Gmail) Bilder blockieren, werden geöffnete E-Mails nicht berücksichtigt.
