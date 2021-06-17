---
solution: Journey Orchestration
title: Allgemeine Ereignisse
description: Erfahren Sie, wie Sie allgemeine Ereignisse verwenden
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 285942ec51859a4cea888d9974f79f52acf3aabf
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 63%

---

# Allgemeine Ereignisse {#section_ofg_jss_dgb}

Für diesen Ereignistyp können Sie nur einen Titel und eine Beschreibung hinzufügen. Der Rest der Konfiguration kann nicht bearbeitet werden. Dies wurde vom technischen Anwender durchgeführt. Weitere Informationen finden Sie auf [dieser Seite](../event/about-events.md).

![](../assets/general-events.png)

Wenn Sie ein Geschäftsereignis ablegen, wird automatisch die Aktivität **Segment lesen** hinzugefügt. Weiterführende Informationen zu Geschäftsereignissen finden Sie in [diesem Abschnitt](../event/about-events.md).

## Überwachen von Ereignissen während eines bestimmten Zeitraums {#events-specific-time}

Eine in der Journey positionierte Ereignisaktivität überwacht Ereignisse auf unbestimmte Zeit. Damit ein Ereignis nur während einer bestimmten Zeit überwacht wird, müssen Sie für das Ereignis eine maximale Wartezeit konfigurieren.

Die Journey überwacht dann das Ereignis während der in der maximalen Wartezeit angegebenen Zeit. Wenn ein Ereignis während dieses Zeitraums empfangen wird, wird die Person in den Ereignispfad geleitet. Ist dies nicht der Fall, wird der Kunde entweder in einen Zeitüberschreitungspfad geleitet oder seine Journey wird beendet.

Gehen Sie wie folgt vor, um für ein Ereignis eine maximale Wartezeit zu konfigurieren:

1. Aktivieren Sie die Option **[!UICONTROL Definieren Sie den Ereignis-Timeout]** in den Ereigniseigenschaften.

1. Legen Sie fest, wie lange die Journey auf das Ereignis warten soll.

1. Wenn Sie die Kontakte in einen Zeitüberschreitungspfad senden möchten, wenn innerhalb der angegebenen Zeitüberschreitung kein Ereignis empfangen wird, aktivieren Sie die Option **[!UICONTROL Zeitüberschreitungspfad festlegen]** . Wenn diese Option nicht aktiviert ist, wird die Journey für den betreffenden Kontakt beendet, sobald die maximale Wartezeit erreicht wird.

   ![](../assets/event-timeout.png)

In diesem Beispiel sendet die Journey einen ersten Willkommens-Push an einen Kunden. Es wird nur dann ein Essensrabatt-Push gesendet, wenn der Kunde das Restaurant innerhalb des nächsten Tages betritt. Deshalb wurde das Restaurantereignis mit einer maximalen Wartezeit von 1 Tag konfiguriert:

* Wenn das Restaurantereignis weniger als 1 Tag nach der Begrüßungs-Push-Benachrichtigung empfangen wird, wird die Push-Aktivität für den Rabatt gesendet.
* Wenn innerhalb des nächsten Tags kein Restaurantereignis eingeht, wird die Person durch den Zeitüberschreitungspfad geleitet.

Wenn Sie eine Zeitüberschreitung für mehrere Ereignisse konfigurieren möchten, die nach einer **[!UICONTROL Wait]** -Aktivität positioniert sind, müssen Sie die Zeitüberschreitung nur für eines dieser Ereignisse konfigurieren.

Die Zeitüberschreitung gilt für alle Ereignisse, die nach der Aktivität **[!UICONTROL Warten]** positioniert werden. Wenn vor der angegebenen Zeitüberschreitung kein Ereignis empfangen wird, fließen die Kontakte in einen einzigen Zeitüberschreitungspfad oder beenden ihre Journey.

![](../assets/event-timeout-group.png)
