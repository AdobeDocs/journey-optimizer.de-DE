---
solution: Journey Optimizer
product: journey optimizer
title: Optimierung des Versandzeitpunkts
description: Erfahren Sie, wie Sie die Parameter für die Versandzeitoptimierung in Ihren Nachrichten einstellen
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: Versandzeit, senden, Nachricht, Optimierung, Journey, KI, intelligent
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: b9ec336abbe329c33098880b16aaeabd8ec0c310
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 13%

---

# Optimierung des Versandzeitpunkts{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung des Versandzeitpunkts"
>abstract="Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe. Sie kann basierend auf vergangenen Öffnungs- und Klickraten die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion zu maximieren."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung des Versandzeitpunkts"
>abstract="Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den KI-Services von Adobe. Sie kann basierend auf vergangenen Öffnungs- und Klickraten die beste Versandzeit für E-Mails oder Push-Benachrichtigungen vorhersagen, um die Interaktion zu maximieren."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Wählen Sie mithilfe des entsprechenden Radiobuttons aus, ob E-Mail-Öffnungen oder E-Mail-Click-Throughs optimiert werden sollen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Aktivieren der Optimierung des Versandzeitpunkts"
>abstract="Bei Push-Benachrichtigungen wird standardmäßig die Option „Öffnungen“ verwendet, da Klicks für Push-Benachrichtigungen zutreffen. Sie können die vom System verwendeten Versandzeitpunkte auch zusammenfassen, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ eingeben."


Die Funktion zur Optimierung des Versandzeitpunkts von Adobe Journey Optimizer basiert auf den Journey-KI-Services von Adobe und wählt den optimalen Versandzeitpunkt für E-Mail- und Push-Nachrichten aus, um die Kundeninteraktion basierend auf dem bisherigen Öffnungs- und Klickverhalten Ihrer Kunden zu maximieren.

Die Sendezeitoptimierung ist nur für die integrierten Aktionstypen E-Mail und Push von Journey Optimizer verfügbar und derzeit nicht für Nachrichten, die über benutzerdefinierte Aktionen oder für andere Aktionstypen gesendet werden. Die Sendezeitoptimierung ist nur für E-Mail- und Push-Aktionen in Journeys verfügbar und derzeit nicht für Nachrichten, die über Kampagnen gesendet werden.

>[!AVAILABILITY]
>
>* Für die erstmalige Schulung und Bewertung der Sendezeitoptimierung werden mindestens 1.000 Profile mit aktuellen Messaging-Daten empfohlen.
>
>* Die Sendezeitoptimierung gilt nur für die Kanäle **E-Mail** und **Push-Benachrichtigung**.

## Optimierung des Versandzeitpunkts aktivieren{#enable-send-time-optimization}

Die Sendezeitoptimierungsfunktion ist für Adobe Journey Optimizer-Kunden auf Anfrage aktiviert. Wenden Sie sich an die Adobe-Kundenunterstützung oder den Adobe-Support, um die Funktion für Ihr Unternehmen zu aktivieren.

## Verwenden der Sendezeitoptimierung{#use-send-time-optimization}

Verwenden Sie die Sendezeitoptimierung für eine E-Mail- oder Push-Aktion, indem Sie den Umschalter Sendezeitoptimierung in den Aktionsparametern aktivieren.

![](assets/sto-use.png)

>[!TIP]
>
>Die Sendezeitoptimierung sollte nicht für dringende, zeitkritische Betriebsnachrichten verwendet werden - z. B. eine Bestellbestätigung, eine Benachrichtigung zum Zurücksetzen des Kennworts oder eine Benachrichtigung über eine Änderung des Fluggatters. Die Optimierung des Versandzeitpunkts eignet sich am besten für weniger dringende Marketing-Nachrichten, z. B. eine wöchentliche Anzeige, Werbeinformationen zu einem neuen Produkt oder Informationen zu einem einmonatigen Verkauf.

Wählen Sie für E-Mail-Nachrichten durch Auswahl des entsprechenden Radiobuttons aus, ob die E-Mail-Öffnungen oder die E-Mail-Click-Throughs optimiert werden sollen. Push-Benachrichtigungen werden immer für Öffnungen optimiert.

>[!TIP]
>
>Um die besten Ergebnisse zu erzielen, sollten die meisten E-Mail-Nachrichten für Klicks optimiert werden. Wählen Sie „Für Öffnungen optimieren“ aus, wenn Ihre E-Mail-Nachricht informativen Charakter hat und nicht dazu gedacht ist, eine Aktion direkt zu steuern.

Wählen Sie für E-Mail- und Push-Nachrichten die maximale Anzahl der Stunden aus, die das System vor dem Senden der Nachricht warten soll, indem Sie einen Wert für die Option „Senden innerhalb der nächsten“ festlegen. Sie können einen Wert zwischen 1 und 168 Stunden wählen.

>[!TIP]
>
>Um die besten Ergebnisse zu erzielen, wählen Sie eine maximale Wartezeit zwischen 6 und 24 Stunden. Die Auswahl eines niedrigeren Werts für die maximale Wartezeit reduziert die Anzahl der verfügbaren Sendezeiten und kann daher den potenziellen Wert der Sendezeitoptimierung verringern. Die Auswahl eines höheren Werts für die maximale Wartezeit kann dazu führen, dass eine Nachricht zum Zeitpunkt ihres Versands veraltet oder irrelevant ist.

Wenn Ihr Journey aktiviert ist und ein Kunde die E-Mail- oder Push-Aktion auf der Journey erreicht, wählt die Sendezeitoptimierung die beste prognostizierte Sendezeit aus, die für jeden Benutzer innerhalb Ihrer festgelegten Limits verfügbar ist.


## Funktionsweise der Sendezeitoptimierung {#how-send-time}

Das Modell „Optimierung des Versandzeitpunkts“ nimmt die Kundenverhaltensdaten Ihres Unternehmens zu Adobe Journey Optimizer auf und untersucht Öffnungs- und Klickereignisse auf Benutzerebene, um zu bestimmen, wann Ihre Kunden mit der größten Wahrscheinlichkeit mit Ihrer Nachricht interagieren.

Die Sendezeitoptimierung trifft für jede Wochenstunde Prognosen für jede Benutzerin und jeden Benutzer basierend auf drei Typen von Verhaltensdaten:

1. Das Verhalten der Benutzer insgesamt
1. Verhalten von Lookalike-Benutzern in derselben Zeitzone
1. Das Verhalten dieses einzelnen Benutzers

Diese Prognosen werden gewichtet und mithilfe eines Bayes&#39;schen Ansatzes kombiniert, was zu einer „Heatmap“ für jede Metrik (E-Mail-Öffnungen, E-Mail-Klicks und Push-Öffnungen) für jeden Kunden führt, die die Stunden der Woche angibt, an denen die Kontaktaufnahme mit diesem Benutzer am wahrscheinlichsten und am wenigsten zum gewünschten Interaktionsergebnis führt (Öffnen/Klicken), wie in der folgenden Beispiel-Heatmap dargestellt:

![](assets/heatmap-1.png)

Wenn ein(e) Benutzende(r) mit der oben prognostizierten Wahrscheinlichkeit für eine Nachricht um 9 Uhr Mittwoch mit aktivierter Sendezeitoptimierung und einer maximalen Wartezeit von 7 Stunden ausgewählt wird, ist die ausgewählte Sendezeit für die Nachricht 12 Uhr:

![](assets/heatmap-2.png)

## Details zum Trainings- und Scoring-Modell für die Sendezeitoptimierung  {#model-send-time}

Sobald die Funktion zur Optimierung des Versandzeitpunkts für Ihr Unternehmen aktiviert ist, wird das Journey-KI-Modell für die letzten 16 Wochen für E-Mail- und Push-Versand-, Öffnungs- und Klickereignisse in allen Journey und Aktionen Ihres Unternehmens trainiert - unabhängig davon, ob bei diesen Aktionen die Optimierung des Versandzeitpunkts verwendet wird. Dadurch kann die Sendezeitoptimierung von allen Daten profitieren, die von Ihren Kunden generiert wurden.

Die Modelle werden zunächst einmal wöchentlich trainiert und bewertet. Nach 16 Wochen werden die Modelle monatlich neu trainiert und neu bewertet. Die Modellbewertung umfasst alle Kundenprofile - sowohl vorhandene als auch neue seit dem letzten Scoring-Durchgang.

Von der Sendezeitoptimierung gesendete Nachrichten erhalten entweder eine Versandzeit zur Untersuchung, die zum Testen verschiedener Sendezeiten ausgewählt wurde, um zu beobachten, wie Kunden reagieren, oder eine optimierte Versandzeit, die zum Maximieren der Klick-/Öffnungsraten ausgewählt wurde. 5 % der Versandereignisse erhalten eine „Exploration“-Versandzeit und 95 % der Versandereignisse sind „optimiert“.

Die Versandzeitpunkte für die Exploration werden zufällig aus den Versandzeiten ausgewählt, die durch die konfigurierte maximale Wartezeit verfügbar sind. Wenn beispielsweise eine Nachricht um 9 Uhr Mittwoch mit aktivierter Sendezeitoptimierung und einer maximalen Wartezeit von 3 Stunden ausgewählt wird, werden die Explorations-Sendezeiten für die Nachricht gleichmäßig zwischen 9 Uhr, 10 Uhr, 11 Uhr und 12 Uhr aufgeteilt.


## Häufig gestellte Fragen {#faq-send-time}

+++Wie lange muss ich warten, bevor ich die Sendezeitoptimierung verwende?

Ihr Unternehmen sollte die E-Mail-Aktion in Journey Optimizer mindestens 30 Tage lang verwenden, bevor die Sendezeitoptimierung in E-Mails verwendet wird, um die Erfassung einiger E-Mail-Versand-, Öffnungs- und Klickereignisse zu ermöglichen.

Ihr Unternehmen sollte die Push-Aktion in Journey Optimizer mindestens 30 Tage lang verwenden, bevor die Sendezeitoptimierung in Push verwendet wird, um die Erfassung einiger Push-Sendeereignisse und offener Ereignisse zu ermöglichen.

Wenn Ihr Unternehmen bereits seit mindestens 30 Tagen die Aktionstypen E-Mail und/oder Push verwendet, muss Ihr Unternehmen nicht länger warten, um die Sendezeitoptimierung zu verwenden, nachdem sie durch Adobe aktiviert wurde. Die Ergebnisse werden sich weiter verbessern, wenn Ihr Unternehmen Daten für bis zu 16 Wochen erfasst.

+++

+++Wie kann ich den Versandzeitpunkt sehen, zu dem ein bestimmter Benutzer eine Nachricht erhält?

Um die Auswirkungen des Modells auf die Profilreichhaltigkeit zu minimieren, werden Modellbewertungen in drei in `_experience.intelligentServices.journeyAI.sendTimeOptimization` gespeicherten Profilattributen komprimiert gespeichert und sind nicht für die menschliche Lesbarkeit konzipiert.

+++


+++Was ist der durchschnittliche Vorteil der Sendezeitoptimierung?

Die Optimierung des Versandzeitpunkts kann die E-Mail-Klickrate und die Push-Öffnungsrate in allen von einem Unternehmen optimierten Nachrichten im Bereich von etwa 2 % bis 10 % erhöhen.

Wenn beispielsweise ein Unternehmen, das E-Mails ohne Sendezeitoptimierung sendet, eine durchschnittliche Klickrate von 5,0 % aufweist, kann derselbe Satz von E-Mails mit Sendezeitoptimierung zu einer durchschnittlichen Klickrate von 5,5 % führen (5,0 % * (1 + 10 %) = 5,5 %).

Aufgrund von Variabilität innerhalb kleiner Stichprobengrößen kann ein Vorteil der Sendezeitoptimierung bei einzelnen Nachrichtensendungen möglicherweise nicht beobachtet werden.

Unternehmen profitieren in den folgenden Fällen mit höherer Wahrscheinlichkeit von den Vorteilen der Sendezeitoptimierung:

* Bestehende Journey verwenden feste und nicht gut optimierte Versandzeitpunkte
* Variables Kundenverhalten (Klicks und Öffnungen) entspricht Kundenstandort und Kundenpräferenzen
* Unternehmen verwenden die Sendezeitoptimierung für einen größeren Teil der E-Mail- und Push-Nachrichten
* Unternehmen wählen maximale Wartezeiten innerhalb des empfohlenen Bereichs von 6 bis 12 Stunden aus

+++

+++Ich klicke immer um 12 Uhr auf E-Mails oder Push-Nachrichten, warum hat mir der Algorithmus nicht um 12 Uhr eine Nachricht geschickt?


Dies kann verschiedene Ursachen haben:

* Ihre Nachricht wurde als Versandzeit der Nachricht „Exploration“ anstelle einer Versandzeit der Nachricht „Optimiert“ ausgewählt.
* Das Verhalten von Lookalike-Benutzern beeinflusste das Modell, eine weitere Versandzeit zu empfehlen.

+++

+++Wie erkennt die Sendezeitoptimierung die Zeitzone eines Benutzers?

Die Sendezeitoptimierung verwendet das `timeZone` Profilfeld, um die Zeitzone eines Benutzers zu bestimmen. Wenn die Sendezeitoptimierung für diesen Benutzer nicht verfügbar ist, versucht sie, die Zeitzone eines Benutzers aus anderen geografischen Informationen im Profil des Benutzers abzuleiten, z. B. Land und Bundesland.

+++


+++Wird die Sendezeitoptimierung nachts Push-Nachrichten an Benutzer in ihrer lokalen Zeitzone senden?

Die Sendezeitoptimierung kann unter folgenden Umständen Push-Nachrichten an Benutzer während der Nacht in ihrer lokalen Zeitzone senden:

* Wenn Benutzerinnen und Benutzer ein Verhalten zeigen, das darauf hinweist, dass sie wahrscheinlich mit einer nachts gesendeten Nachricht interagieren
* Wenn das Modell einen Versandzeitpunkt für die „Exploration“ auswählt

Um zu vermeiden, dass Push-Nachrichten nachts an Kunden gesendet werden, planen Sie Batch-Push-Nachrichten-Sendungen für morgens oder am frühen Nachmittag und wählen Sie eine kürzere Dauer für die Optimierung des Versandzeitpunkts aus. (Zum Beispiel eine Versandzeit von 9 Uhr und eine maximale Wartezeit von 8 Stunden.)

+++



