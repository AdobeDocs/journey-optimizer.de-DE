---
solution: Journey Optimizer
product: journey optimizer
title: Allgemeine Ereignisse
description: Erfahren Sie, wie Sie allgemeine Ereignisse verwenden
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: benutzerdefiniert, allgemein, Ereignisse, Journey
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 74%

---

# Allgemeine Ereignisse {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Unitäre Ereignisse"
>abstract="Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten. Für diesen Ereignistyp können Sie nur einen Titel und eine Beschreibung hinzufügen. Die Ereigniskonfiguration wird von einem Datentechniker vorgenommen und kann nicht bearbeitet werden."

Mit Hilfe von Ereignissen können Sie Ihre Journeys einheitlich auslösen, um Nachrichten in Echtzeit an die Kontakte zu senden, die in die Journey eintreten.

Für diesen Ereignistyp können Sie nur einen Titel und eine Beschreibung hinzufügen. Der Rest der Konfiguration kann nicht bearbeitet werden. Dies wurde vom technischen Anwender durchgeführt. Weitere Informationen finden Sie auf [dieser Seite](../event/about-events.md).

![](assets/general-events.png)

Wenn Sie ein Geschäftsereignis einfügen, wird automatisch eine Aktivität **Zielgruppe lesen** hinzugefügt. Weiterführende Informationen zu Geschäftsereignissen finden Sie in [diesem Abschnitt](../event/about-events.md).

## Überwachen von Ereignissen während eines bestimmten Zeitraums {#events-specific-time}

Eine in der Journey positionierte Ereignisaktivität überwacht Ereignisse auf unbestimmte Zeit. Damit ein Ereignis nur während einer bestimmten Zeit überwacht wird, müssen Sie für das Ereignis eine maximale Wartezeit konfigurieren.

Die Journey überwacht dann das Ereignis während der in der maximalen Wartezeit angegebenen Zeit. Wenn ein Ereignis während dieses Zeitraums empfangen wird, wird die Person in den Ereignispfad geleitet. Andernfalls gelangt die Person in den Pfad für die maximale Wartezeit, sofern er definiert ist, oder setzt die Journey fort.

Wenn kein Pfad für die maximale Wartezeit definiert ist, fungiert die Einstellung für die maximale Wartezeit als Warteaktivität. Dadurch wartet das Profil für einen Zeitraum, der beendet werden kann, wenn ein Ereignis vor dem Ende dieser Wartezeit eintritt. Wenn Sie möchten, dass Profile nach einer maximalen Wartezeit von dieser Journey ausgeschlossen werden, müssen Sie einen Pfad für die maximale Wartezeit festlegen.

Gehen Sie wie folgt vor, um für ein Ereignis eine maximale Wartezeit zu konfigurieren:

1. Aktivieren Sie die Option **[!UICONTROL Maximale Wartezeit für das Ereignis definieren]** in den Eigenschaften des Ereignisses.

1. Legen Sie fest, wie lange die Journey auf das Ereignis warten soll. Die maximale Wartezeit beträgt 29 Tage.

1. Wenn Sie die Kontakte in einen Zeitüberschreitungspfad senden möchten, falls innerhalb der angegebenen maximalen Wartezeit kein Ereignis empfangen wird, aktivieren Sie die Option **[!UICONTROL Zeitüberschreitungspfad einrichten]**. Wenn diese Option nicht aktiviert ist, wird die Journey für die Person fortgesetzt, sobald die Zeitüberschreitung erreicht ist. Wir empfehlen, dass Sie immer die **Zeitüberschreitungspfad festlegen** -Option.

   ![](assets/event-timeout.png)

In diesem Beispiel sendet die Journey eine erste Begrüßungs-E-Mail an einen Kunden, nachdem er die Lobby betritt. Es wird dann nur dann eine E-Mail mit einem Rabatt für Mahlzeiten gesendet, wenn der Kunde innerhalb des nächsten Tages das Restaurant betritt. Deshalb wurde das Restaurantereignis mit einer maximalen Wartezeit von 1 Tag konfiguriert:

* Wenn das Restaurantereignis weniger als 1 Tag nach der Begrüßungs-E-Mail empfangen wird, wird die E-Mail mit dem Rabatt für die Mahlzeit gesendet.
* Wenn innerhalb des nächsten Tages kein Restaurantereignis eingeht, wird die Person durch den Zeitüberschreitungspfad geleitet.

Wenn Sie eine maximale Wartezeit für mehrere Ereignisse konfigurieren möchten, die sich hinter einer **[!UICONTROL Warteaktivität]** befinden, müssen Sie die maximale Wartezeit nur für eines dieser Ereignisse konfigurieren.

Die definierte Zeitüberschreitung gilt für alle Ereignisse, die nach der **[!UICONTROL Warten]** Aktivität:

* Wenn ein Ereignis innerhalb der Zeitüberschreitungsdauer erneut ausgeführt wird, fließt der Kontakt in den Pfad des empfangenen Ereignisses.
* Wenn innerhalb der Timeout-Dauer kein Ereignis empfangen wird, fließt der Kontakt in den Timeout-Zweig des Ereignisses, in dem die Zeitüberschreitung definiert wurde.

![](assets/event-timeout-group.png)
