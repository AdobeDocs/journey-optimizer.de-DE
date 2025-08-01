---
solution: Journey Optimizer
product: journey optimizer
title: Warteaktivität
description: Erfahren Sie, wie Sie die Warteaktivität konfigurieren
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Warten, Aktivität, Journey, weiter, Arbeitsfläche
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: db3c87d10469550eb30224c932344ff1e3ae1767
workflow-type: ht
source-wordcount: '649'
ht-degree: 100%

---

# Warteaktivität {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Warteaktivität"
>abstract="Wenn Sie warten möchten, bevor Sie die nächste Aktivität im Pfad ausführen, können Sie eine Warteaktivität verwenden. Sie können den Zeitpunkt festlegen, zu dem die nächste Aktivität ausgeführt wird. Es stehen zwei Optionen zur Verfügung: „Dauer“ und „Benutzerdefiniert“."

Mit einer Aktivität vom Typ **[!UICONTROL Warten]** können Sie eine Dauer definieren, nach deren Ablauf die nächste Aktivität ausgeführt wird.  Die maximale Wartezeit beträgt **90 Tage**.

Sie können zwei Arten der Aktivität vom Typ **Warten** festlegen:

* Eine Wartezeit basierend auf einer relativen Dauer. [Weitere Informationen](#duration)
* Ein benutzerdefiniertes Datum, das mithilfe von Funktionen berechnet wird. [Weitere Informationen](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Empfehlungen {#wait-recommendations}

### Mehrere Warteaktivitäten {#multiple-wait-activities}

Achten Sie bei der Verwendung mehrerer Aktivitäten vom Typ **Warten** in einer Journey darauf, dass die [maximale globale Wartezeit](journey-properties.md#global_timeout) für Journeys 91 Tage beträgt, d. h., Profile werden immer spätestens 91 Tage nach ihrem Eintritt aus der Journey ausgeschlossen. Weitere Informationen finden Sie auf [dieser Seite](journey-properties.md#global_timeout).

Ein Kontakt kann nur dann eine Aktivität vom Typ **Warten** annehmen, wenn noch genügend Zeit bleibt, um die Wartezeit vor Ablauf der 91-tägigen maximalen Wartezeit der Journey zu beenden.

### Warten und erneuter Eintritt {#wait-reentrance}

Eine Best Practice, um keine Aktivitäten vom Typ **Warten** zu verwenden, um den erneuten Eintritt zu blockieren. Verwenden Sie stattdessen die Option **Erneuten Eintritt erlauben** auf der Ebene der Journey-Eigenschaften. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/journey-properties.md#entrance).

### Warten und Testmodus {#wait-test-mode}

Im Testmodus können Sie mit dem Parameter **[!UICONTROL Wartezeit im Test]** die Dauer jeder Aktivität vom Typ **Warten** festlegen. Der Standardwert ist 10 Sekunden. Dadurch erhalten Sie die Testergebnisse schnell. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/testing-the-journey.md).

### Warte- und Mobile-Kanäle {#wait-mobile-channels}

Wenn Sie eine [In-App-Nachricht](../in-app/create-in-app.md) nach dem Versand einer [Push-Benachrichtigung](../push/get-started-push.md) anzeigen möchten, verwenden Sie eine Aktivität **Warten**, damit die Payload-Zeit der In-App-Nachricht weitergegeben wird. Normalerweise wird eine Wartezeit von 5 bis 15 Minuten empfohlen. Die genauen Zeiten können jedoch je nach Payload-Komplexität und Personalisierungsanforderungen variieren.

## Konfiguration {#wait-configuration}

### Dauer der Wartezeit {#duration}

Wählen Sie den Typ **Dauer**, um die relative Dauer der Wartezeit vor der Ausführung der nächsten Aktivität auszuwählen. Die maximale Wartezeit beträgt **90 Tage**.

![Definieren der Wartezeit](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Benutzerdefinierte Wartezeit {#custom}

Wählen Sie den Typ **Benutzerdefiniert** aus, um ein benutzerdefiniertes Datum zu definieren. Dabei verwenden Sie einen erweiterten Ausdruck, der auf einem von einem Ereignis oder einer benutzerdefinierten Aktion stammenden Feld basiert. Sie können eine relative Dauer nicht direkt definieren, z. B. 7 Tage, aber Sie können Funktionen verwenden, um sie bei Bedarf zu berechnen (z. B. 2 Tage nach Kauf).

![Definieren einer benutzerdefinierten Wartezeit mit einem Ausdruck](assets/journey57.png)

Der Ausdruck im Editor sollte ein `dateTimeOnly`-Format aufweisen. Mehr dazu erfahren Sie auf [dieser Seite](expression/expressionadvanced.md). Weitere Informationen zum Format „TimeOnly“ finden Sie auf [dieser Seite](expression/data-types.md).

Es empfiehlt sich, benutzerdefinierte Datumsangaben zu verwenden, die spezifisch für Ihre Profile sind, und zu vermeiden, dass für alle Profile dasselbe Datum verwendet wird. Definieren Sie beispielsweise nicht `toDateTimeOnly('2024-01-01T01:11:00Z')`, sondern `toDateTimeOnly(@event{Event.productDeliveryDate})`, was für jedes Profil spezifisch ist. Beachten Sie, dass die Verwendung von festen Datumsangaben Probleme bei der Ausführung der Journey verursachen kann.


>[!NOTE]
>
>Sie können einen `dateTimeOnly`-Ausdruck nutzen oder eine Funktion zur Konvertierung in ein `dateTimeOnly`-Format verwenden.  Beispiel: `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, das Feld im Ereignis hat folgende Form: 2023-08-12T09:46:06Z.
>
>Die Angabe der **Zeitzone** ist für die Eigenschaften Ihrer Journey erforderlich. Aus diesem Grund ist es nicht möglich, von direkt der Benutzeroberfläche auf eine Zeitstempelmischzeit nach ISO-8601 und einen Zeitzonenversatz wie 2023-08-12T09:46:06.982-05 zu verweisen. [Weitere Informationen](../building-journeys/timezone-management.md).


Um zu überprüfen, ob die Warteaktivität erwartungsgemäß funktioniert, können Sie Schritt-Ereignisse verwenden. [Weitere Informationen](../reports/query-examples.md#common-queries).

## Automatischer Warteknoten  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="Über den automatischen Warteknoten"
>abstract="Nach dieser Aktivität wird automatisch eine **Warteaktivität** hinzugefügt. Sie ist auf 3 Tage eingestellt. Sie können sie entfernen oder nach Bedarf konfigurieren."

Jede Aktivität für eingehende Erlebnisse (In-App-Nachricht, Code-basiertes Erlebnis oder Karte) geht mit einer 3-tägigen **Warteaktivität** einher. Da eingehende Nachrichten automatisch enden, wenn ein Profil das Ende der Journey erreicht, ist davon auszugehen, dass Sie möchten, dass Ihre Benutzenden sie mindestens 3 Tage lang sehen. Sie können bei Bedarf diese **Warteaktivität** entfernen oder ihre Konfiguration ändern.