---
solution: Journey Optimizer
product: journey optimizer
title: Übersicht über die Freigabe von Journey-Schritten
description: Übersicht über die Freigabe von Journey-Schritten
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 83%

---

# Erstellen von Journey-Berichten {#design-jo-reports}

Zusätzlich zu [Echtzeitberichten](live-report.md) und integrierten [Reporting-Funktionen](report-gs-cja.md) kann [!DNL Journey Optimizer] Journey-Performance-Daten automatisch an Adobe Experience Platform senden, damit sie zu Analysezwecken mit anderen Daten kombiniert werden können.

>[!NOTE]
>
>Diese Funktion ist standardmäßig auf allen Instanzen für Journey-Schrittereignisse aktiviert. Sie können die Schemata und Datensätze, die bei der Bereitstellung für Schrittereignisse erstellt wurden, nicht ändern oder aktualisieren. Standardmäßig sind diese Schemata und Datensätze schreibgeschützt.

Sie haben beispielsweise eine Journey eingerichtet, die mehrere E-Mails sendet. Mit dieser Funktion können Sie [!DNL Journey Optimizer]-Daten mit nachgelagerten Ereignisdaten kombinieren (z. B. der Anzahl der Konversionen, der Interaktionen auf der Website oder der Transaktionen im Store). Die Journey-Daten können entweder über andere digitale Eigenschaften oder über Offline-Eigenschaften mit Daten aus Adobe Experience Platform kombiniert werden, um eine umfassendere Ansicht der Performance zu ermöglichen.

[!DNL Journey Optimizer] erstellt für jeden Schritt, den ein Kontakt bei einer Journey unternimmt, automatisch die erforderlichen Schemata und streamt die Daten in Datensätze zu Adobe Experience Platform. Ein Schrittereignis entspricht einem Kontakt, der bei einer Journey von einem Knoten zu einem anderen wechselt. Beispielsweise werden bei einer Journey, die über ein Ereignis, eine Bedingung und eine Aktion verfügt, drei Schrittereignisse an Adobe Experience Platform gesendet.

>[!NOTE]
>
>Zusätzlich zu Schrittereignissen auf Profilebene generiert das System auch interne Ereignisse für Aktivitäten des Typs **Zielgruppe lesen**. Diese als `segmentExportJob` bezeichneten Ereignisse zeichnen den Lebenszyklus des Knotens „Zielgruppe lesen“ auf (z. B. Erstellung von Exportvorgängen, Warteschlangen, Abschluss und Fehler) und werden pro Aktivität „Zielgruppe lesen“ und nicht pro einzelnem Profil generiert. Infolgedessen haben diese Ereignisse möglicherweise keine zugehörige Profilkennung (UPMID). Diese internen Ereignisse sind für die Überwachung der Leistung von „Zielgruppe lesen“ und zur Fehlerbehebung nützlich und können mithilfe der im Abschnitt „serviceEvents[&#x200B; dokumentierten Felder abgefragt &#x200B;](../reports/sharing-field-list.md#servicevents-field). Abfragebeispiele für die Arbeit mit segmentExportJob-Ereignissen finden Sie unter [Abfragen im Zusammenhang mit „Zielgruppe lesen](../reports/query-examples.md#read-segment-queries).

Es gibt Fälle, in denen mehrere Ereignisse für denselben Knoten erstellt werden können. Beispielsweise im Falle der Warten-Aktivität:

* Ein Ereignis wird generiert, wenn das Profil in die Wartezeit eintritt (Das Attribut „journeyNodeProcessed“ ist gleich „false“)
* Ein Ereignis wird generiert, wenn das Profil es verlässt (Das Attribut „journeyNodeProcessed“ ist gleich „true“)

Die Liste der weitergeleiteten XDM-Felder ist umfassend. Einige enthalten systemgenerierte Codes, andere haben lesbare Anzeigenamen. Beispiele sind die Bezeichnung der Journey-Aktivität und der Schrittstatus: wie oft eine Aktion die Zeit überschritten hat oder fehlerhaft endete.

>[!CAUTION]
>
>Für den Echtzeit-Profildienst können keine Datensätze aktiviert werden. Stellen Sie sicher, dass der Umschalter **[!UICONTROL Profil]** deaktiviert ist.

[!DNL Journey Optimizer] sendet Daten bei ihrem Auftreten direkt im Streaming-Modus. Sie können diese Daten mit dem Query Service abfragen. Sie können eine Verbindung zu Customer Journey Analytics oder anderen BI-Tools herstellen, um Daten anzuzeigen, die mit diesen Schritten in Verbindung stehen.

Die folgenden Schemata werden erstellt:

* Journey Step Event-Schema für [!DNL Journey Orchestration] – Journey-Schrittereignis, das mit Journey-Metadaten verknüpft ist.
* Journey-Schema mit Journey-Feldern für [!DNL Journey Orchestration] – Journey-Metadaten zur Beschreibung von Journeys.

![](assets/sharing1.png)

![](assets/sharing2.png)

Die folgenden Datensätze werden übergeben:

* Journey-Schrittereignisse
* Journeys

![](assets/sharing3.png)

Die Listen der XDM-Felder, die an Adobe Experience Platform übergeben werden, werden hier beschrieben:

* [Liste für Schrittereignisfelder](../reports/sharing-field-list.md)
* [Veraltete Schrittereignisfelder](../reports/sharing-legacy-fields.md)

## Integration mit Customer Journey Analytics {#integration-cja}

Schrittereignisse von [!DNL Journey Optimizer] können mit anderen Datensätzen in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=de){target="_blank"} verknüpft werden.

Der allgemeine Workflow ist:

* [!DNL Customer Journey Analytics] nimmt den Datensatz „Schrittereignis der Journey“ auf.
* Die **profileID** im zugehörigen „Schrittereignisschema der Journey für Journey Orchestration“ wird als Identitätsfeld definiert. In [!DNL Customer Journey Analytics] können Sie diesen Datensatz dann mit jedem anderen Datensatz verknüpfen, der denselben Wert wie die personenbasierte Kennung hat.
* Informationen zur Verwendung dieses Datensatzes in [!DNL Customer Journey Analytics] zur kanalübergreifenden Journey-Analyse finden Sie in der [Dokumentation zu Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html?lang=de){target="_blank"}.

➡️ [Arbeiten mit Customer Journey Analytics](cja-ajo.md){target="_blank"}
