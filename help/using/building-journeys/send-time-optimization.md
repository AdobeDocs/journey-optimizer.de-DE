---
solution: Journey Optimizer
product: journey optimizer
title: Versandzeitoptimierung
description: Erfahren Sie, wie Sie die Versandzeitoptimierung in Ihren Nachrichten parametrieren
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Sendezeitoptimierung{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Über die Optimierung der Versandzeit"
>abstract="Die Sendezeitoptimierungsfunktion von Adobe Journey Optimizer, die auf den KI-Diensten von Adobe basiert, kann die beste Zeit für den Versand einer E-Mail oder Push-Nachricht vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren."

Die Sendezeitoptimierungsfunktion von Adobe Journey Optimizer, die auf den KI-Diensten von Adobe basiert, kann die beste Zeit für den Versand einer E-Mail oder Push-Nachricht vorhersagen, um die Interaktion basierend auf historischen Öffnungs- und Klickraten zu maximieren. Verwenden Sie unser Modell für maschinelles Lernen, um personalisierte Sendezeiten für jeden Benutzer zu planen, um die Öffnungs- und Klickraten Ihrer Nachrichten zu erhöhen.

Das Modell &quot;Send-Time Optimization&quot;erfasst Ihre Adobe Journey Optimizer-Daten, betrachtet die Öffnungsraten auf Benutzerebene (für E-Mail und Push-Benachrichtigungen) und klickt (für E-Mails), um festzustellen, wann Ihre Kunden mit hoher Wahrscheinlichkeit mit Ihrer Nachrichten interagieren. Die Sendezeitoptimierung erfordert für fundierte Empfehlungen mindestens einen Monat an Nachrichten-Tracking-Daten. Für jeden Benutzer wählt das System automatisch die beste Zeit mit den folgenden Werten aus:

* Die beste Stunde jedes Wochentags, um die Interaktion zu maximieren
* Der beste Wochentag zur Maximierung der Interaktion
* Die beste Stunde des besten Wochentags, um die Interaktion zu maximieren

Das Modell variiert, ob Sie über Scoring oder Training sprechen. Die Schulung wird wöchentlich und danach vierteljährlich durchgeführt. Die Auswertung erfolgt zunächst wöchentlich und dann monatlich.

* Training - die Entwicklung des Algorithmus für die Ermittlung des Werts
* Scoring - die Anwendung eines Punkts auf einzelne Profile basierend auf dem trainierten Modell

Diese Informationen werden mit dem Profil des Benutzers gespeichert und bei der Ausführung der Journey referenziert, um Adobe Journey Optimizer mitzuteilen, wann Ihre Nachricht gesendet werden soll.

>[!CAUTION]
>
>Diese Funktion ist nicht mit dem Burst-Modus kompatibel.

## Aktivieren der Sendezeitoptimierung{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Aktivieren der Sendezeitoptimierung"
>abstract="Wählen Sie mithilfe der entsprechenden Optionsschaltfläche aus, ob E-Mail-Öffnungen oder E-Mail-Clickthroughs optimiert werden sollen. Sie können die vom System verwendeten Versandzeiten auch vereinheitlichen, indem Sie innerhalb der nächsten Option einen Wert für die Option Senden eingeben."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Aktivieren der Sendezeitoptimierung"
>abstract="Bei Push-Nachrichten wird standardmäßig die Option &quot;Öffnungen&quot;verwendet, da Klicks nicht für Push-Nachrichten gelten. Sie können die vom System verwendeten Versandzeiten auch vereinheitlichen, indem Sie innerhalb der nächsten Option einen Wert für die Option Senden eingeben."

Aktivieren Sie die Sendezeitoptimierung für eine E-Mail oder Push-Nachricht, indem Sie die **Sendezeitoptimierung** von den Aktivitätsparametern umschalten.

![](../building-journeys/assets/jo-message5.png)

Wählen Sie für E-Mail-Nachrichten durch Auswahl des entsprechenden Optionsfeldes aus, ob die E-Mail-Öffnungen oder der E-Mail-Clickthrough optimiert werden sollen. Bei Push-Nachrichten wird standardmäßig die Option &quot;Öffnungen&quot;verwendet, da Klicks nicht für Push-Nachrichten gelten.

Sie können die vom System verwendeten Versandzeiten auch durch Eingabe eines Werts für **Senden innerhalb des nächsten** -Option. Wenn Sie als Wert &quot;sechs Stunden&quot;wählen, [!DNL Journey Optimizer] prüft jedes Benutzerprofil und wählt die optimale Sendezeit innerhalb von sechs Stunden ab der Ausführungszeit der Journey aus.
