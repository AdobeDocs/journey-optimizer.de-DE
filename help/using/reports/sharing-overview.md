---
solution: Journey Optimizer
product: journey optimizer
title: Übersicht über die Freigabe von Journey-Schritten
description: Übersicht über die Freigabe von Journey-Schritten
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Erstellen von Journey-Berichten {#design-jo-reports}

Zusätzlich zu [Echtzeitberichte](live-report.md) und integriert [globale Berichtsfunktionen](global-report.md), [!DNL Journey Optimizer] kann Journey-Leistungsdaten automatisch an Adobe Experience Platform senden, damit sie zu Analysezwecken mit anderen Daten kombiniert werden können.

>[!NOTE]
>
>Diese Funktion wird standardmäßig in allen Instanzen für Ereignisse bei Journey-Schritten aktiviert. Sie können die Schemas und Datensätze, die bei der Bereitstellung für Schrittereignisse erstellt wurden, nicht ändern oder aktualisieren. Standardmäßig sind diese Schemas und Datensätze schreibgeschützt.

Sie haben beispielsweise eine Journey eingerichtet, die mehrere E-Mails sendet. Mit dieser Funktion können Sie [!DNL Journey Optimizer] Daten mit nachgelagerten Ereignisdaten wie der Anzahl der Konversionen, der Interaktionen auf der Website oder der Transaktionen im Store. Die Journey-Informationen können mit Daten aus Adobe Experience Platform kombiniert werden, entweder aus anderen digitalen Eigenschaften oder aus Offline-Eigenschaften, um eine umfassendere Ansicht der Leistung zu ermöglichen.

[!DNL Journey Optimizer] erstellt für jeden Schritt, den ein Kontakt in einer Journey unternimmt, automatisch die erforderlichen Schemata und streamt die Daten in Datensätze zu Adobe Experience Platform. Ein Schrittereignis entspricht einer Person, die in einer Journey von einem Knoten zu einem anderen wechselt. Beispiel: In einer Journey, die über ein Ereignis, eine Bedingung und eine Aktion verfügt, werden drei Schrittereignisse an Adobe Experience Platform gesendet.

Die Liste der weitergeleiteten XDM-Felder ist umfassend. Einige enthalten systemgenerierte Codes und andere haben lesbare Anzeigenamen. Beispiele sind der Titel der Journey-Aktivität oder der Schrittstatus: wie oft eine Aktion abgelaufen ist oder fehlerhaft endete.

>[!CAUTION]
>
>Datensätze können für den Echtzeit-Profildienst nicht aktiviert werden. Stellen Sie sicher, dass die Variable **[!UICONTROL Profile]** -Umschalter ist deaktiviert.

[!DNL Journey Optimizer] sendet Daten im Streaming-Modus, sobald sie auftreten. Sie können diese Daten mit dem Query Service abfragen. Sie können eine Verbindung zu Customer Journey Analytics oder anderen BI-Tools herstellen, um Daten zu diesen Schritten anzuzeigen.

Die folgenden Schemata werden erstellt:

* Journey Step Event-Schema für [!DNL Journey Orchestration] - Journey-Schrittereignis, das mit Journey-Metadaten verknüpft ist.
* Journey-Schema mit Journey-Feldern für [!DNL Journey Orchestration] - Journey-Metadaten zur Beschreibung von Journeys.

![](assets/sharing1.png)

![](assets/sharing2.png)

Die folgenden Datensätze werden übergeben:

* Journey-Schrittereignisse
* Journeys

![](assets/sharing3.png)

Die Listen der XDM-Felder, die an Adobe Experience Platform übergeben werden, werden hier beschrieben:

* [Schrittereignisfeldliste](../reports/sharing-field-list.md)
* [Ereignisfelder für veraltete Schritte](../reports/sharing-legacy-fields.md)

## Integration mit Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] Schrittereignisse können mit anderen Datensätzen in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html){target=&quot;_blank&quot;}.

Der allgemeine Workflow lautet:

* [!DNL Customer Journey Analytics] erfasst den Datensatz &quot;Journey Step Event&quot;.
* Die **profileID** im zugehörigen Feld &quot;Journey Step Event schema for Journey Orchestration&quot;als Identitätsfeld definiert ist. In [!DNL Customer Journey Analytics]können Sie diesen Datensatz dann mit einem anderen Datensatz verknüpfen, der denselben Wert wie die personenbasierte Kennung aufweist.
* So verwenden Sie diesen Datensatz in [!DNL Customer Journey Analytics]Informationen zur kanalübergreifenden Journey-Analyse finden Sie unter [Dokumentation zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

