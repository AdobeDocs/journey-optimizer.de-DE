---
solution: Journey Optimizer
product: journey optimizer
title: Reaktionsereignisse
description: Erfahren Sie, wie Sie mit Reaktionsereignissen auf Nachrichten-Tracking-Daten wie Öffnungen und Klicks in Ihren Journeys reagieren und Timeout-Pfade für nicht antwortende Profile konfigurieren können.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Ereignisse, Reaktion, Tracking, Plattform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 100%

---

# Reaktionsereignisse {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Reaktionsereignisse"
>abstract="Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für [!DNL Adobe Experience Platform] freigegeben werden."

## Überblick {#overview}

Unter den verschiedenen Ereignisaktivitäten, die in der Palette verfügbar sind, finden Sie das integrierte **[!UICONTROL Reaktionsereignis]**. Mit dieser Aktivität können Sie auf Tracking-Daten reagieren, die sich auf eine innerhalb derselben Journey gesendete Nachricht beziehen. Wir erfassen diese Informationen in Echtzeit, sobald sie für [!DNL Adobe Experience Platform] freigegeben werden.

Sie können auf angeklickte oder geöffnete Nachrichten reagieren. Beispielsweise können Sie eine weitere Nachricht senden, wenn eine Person die vorherige E-Mail geöffnet oder darin geklickt hat, oder eine andere Folgenachricht senden, wenn sie nicht mit Ihrer Kommunikation interagiert hat.

Siehe [Aktionsaktivitäten](../building-journeys/about-journey-activities.md#action-activities).

Sie können die Aktivität **[!UICONTROL Reaktion]** auch verwenden, um eine Aktion auszuführen, wenn keinerlei Reaktion auf Ihre Nachrichten erfolgt. Erstellen Sie hierfür einen zweiten Pfad parallel zur Aktivität **[!UICONTROL Reaktion]** und fügen Sie eine Aktivität **[!UICONTROL Warten]** hinzu. Wenn während des in der Aktivität **[!UICONTROL Warten]** definierten Zeitraums keine Reaktion erfolgt, wird der zweite Pfad gewählt. Sie können beispielsweise eine Folgenachricht senden.

## Konfigurieren von Reaktionsereignissen {#configure}

![Konfiguration des Reaktionsereignisses mit Optionen zur Kanalauswahl und zum Ereignistyp](assets/journey45.png)

Führen Sie diese Schritte aus, um die Reaktionsereignisse zu konfigurieren:

1. Platzieren Sie eine Aktivität **[!UICONTROL Reaktion]** in der Journey-Arbeitsfläche **unmittelbar** nach einer [Kanalaktionsaktivität](journey-action.md).
1. Fügen Sie der Reaktion ein **[!UICONTROL Label]** hinzu. Dieser Schritt ist optional.
1. Wählen Sie aus der Dropdown-Liste die Aktionsaktivität aus, auf die Sie reagieren möchten. Sie können jede Aktionsaktivität auswählen, die in den vorherigen Schritten des Pfades platziert wurde.
1. Wählen Sie je nach ausgewählter Aktion, auf was Sie reagieren möchten.
1. Sie können das Timeout für ein Ereignis (zwischen 40 Sekunden und 90 Tagen) und einen Timeout-Pfad definieren. Dadurch wird ein zweiter Pfad für Personen erstellt, die nicht innerhalb der festgelegten Zeitspanne reagiert haben. Beim Testen einer Journey, die ein Reaktionseeignis verwendet, beträgt der Standard- und Mindestwert für die **[!UICONTROL Wartezeit]** im Testmodus 40 Sekunden. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/testing-the-journey.md).

## Leitlinien und Einschränkungen {#guardrails-limitations}

* Eine Aktivität **[!UICONTROL Reaktion]** muss in der Journey-Arbeitsfläche **unmittelbar** nach einer [Kanalaktionsaktivität](journey-action.md) platziert werden.
* Eine Aktivität **[!UICONTROL Reaktion]** kann nur verwendet werden, wenn zuvor eine Kanalaktionsaktivität stattgefunden hat.
* Das Platzieren einer Aktivität **[!UICONTROL Warten]** oder einer anderen Aktivität zwischen der Kanalaktion und der Aktivität **[!UICONTROL Reaktion]** wird nicht unterstützt und kann dazu führen, dass die Reaktion nicht wie erwartet funktioniert.
* Reaktionsereignisse können nur Nachrichten verfolgen, die innerhalb derselben Journey gesendet werden. Meldungen, die in einer anderen Journey stattfinden, können nicht verfolgt werden.
* Reaktionsereignisse verfolgen Klicks auf Links des Typs „verfolgt“. Abmeldungs- und Mirrorseiten-Links werden nicht berücksichtigt.
* Das Öffnen von E-Mails wird anhand eines in der E-Mail enthaltenen 0-Pixel-Bildes nachverfolgt. Wenn E-Mail-Clients (z. B. Gmail) Bilder blockieren, werden E-Mail-Öffnungen nicht berücksichtigt.
