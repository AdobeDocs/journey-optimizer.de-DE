---
title: Übersicht über die Freigabe von Journey-Schritten
description: Übersicht über die Freigabe von Journey-Schritten
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 70%

---

# Erstellen von Journey-Berichten{#design-jo-reports}

![](../assets/do-not-localize/badge.png)

Zusätzlich zu [Echtzeitberichten](live-report.md) und integrierten [Funktionen für globale Berichte](global-report.md) können [!DNL Journey Optimizer] Journey-Leistungsdaten automatisch an Adobe Experience Platform senden, damit sie zu Analysen mit anderen Daten kombiniert werden können.

>[!NOTE]
>
>Diese Funktion ist nicht bei allen neu bereitgestellten Instanzen standardmäßig aktiviert. Die Aktivierung erfolgt auf Anfrage.

Sie haben beispielsweise eine Journey eingerichtet, die mehrere E-Mails sendet. Mit dieser Funktion können Sie [!DNL Journey Optimizer]-Daten mit nachgelagerten Ereignisdaten kombinieren (z. B. der Anzahl der Konversionen, der Interaktionen auf der Website oder der Transaktionen im Store). Die Journey-Informationen können mit Daten auf Adobe Experience Platform kombiniert werden, entweder von anderen digitalen Eigenschaften oder von Offline-Eigenschaften, um eine umfassendere Ansicht der Leistung zu erhalten.

[!DNL Journey Optimizer] erstellt automatisch die erforderlichen Schema und streamt die Daten für jeden Schritt, den ein Einzelner in einer Journey unternimmt, in Adobe Experience Platform zu. Ein Schrittereignis entspricht einem Kontakt, der bei einer Journey von einem Knoten zu einem anderen wechselt. In einer Journey mit einem Ereignis, einer Bedingung und einer Aktion werden beispielsweise drei Ereignis an Adobe Experience Platform gesendet.

Die Liste der weitergeleiteten XDM-Felder ist umfassend. Einige enthalten systemgenerierte Codes, andere haben lesbare Anzeigenamen. Beispiele sind die Bezeichnung der Journey-Aktivität und der Schrittstatus: wie oft eine Aktion die Zeit überschritten hat oder fehlerhaft endete.

>[!CAUTION]
>
>Für den Echtzeit-Profildienst können keine Datensätze aktiviert werden. Stellen Sie sicher, dass der Umschalter **[!UICONTROL Profil]** deaktiviert ist..

Journeys sendet Daten direkt im Streaming-Modus. Sie können diese Daten mit dem Query Service abfragen. Sie können eine Verbindung zu Customer Journey Analytics oder anderen BI-Tools herstellen, um Daten anzuzeigen, die mit diesen Schritten in Verbindung stehen.

Die folgenden Schemata werden erstellt:

* Journey Step Profile Event-Schema für [!DNL Journey Orchestration] – Erlebnisereignisse für Schritte, die in einer Journey unternommen werden, zusammen mit einer Identitätszuordnung, die der Zuordnung zu einem einzelnen Journey-Teilnehmer dient.
* Journey Step Event-Schema für [!DNL Journey Orchestration] – Journey-Schrittereignis, das mit Journey-Metadaten verknüpft ist.
* Journey-Schema mit Journey-Feldern für [!DNL Journey Orchestration] – Journey-Metadaten zur Beschreibung von Journeys.

![](../assets/sharing1.png)

![](../assets/sharing2.png)

Die folgenden Datensätze werden übergeben:

* Journey Step Profile Event-Schema für [!DNL Journey Orchestration]
* Journey-Schrittereignisse
* Journeys

![](../assets/sharing3.png)

Die Listen der XDM-Felder, die an Adobe Experience Platform übergeben werden, sind hier aufgeführt:

* [Gemeinsame Felder für journeyStep-Ereignisse](../reports/sharing-common-fields.md)
* [Aktionsausführungsfelder für journeyStep-Ereignisse](../reports/sharing-execution-fields.md)
* [Datenabruffelder für journeyStep-Ereignisse](../reports/sharing-fetch-fields.md)
* [Identitätsfelder für journeyStep-Ereignisse](../reports/sharing-identity-fields.md)
* [Journey-Felder](../reports/sharing-journey-fields.md)

Weiterführende Informationen zu Berichten über Schrittereignisse an Adobe Experience Platform finden Sie in diesem [Anleitungsvideo](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html).
