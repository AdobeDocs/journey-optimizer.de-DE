---
title: Live-Bericht zum E-Mail-Versand
description: Erfahren Sie, wie Sie Daten aus dem E-Mail-Live-Bericht verwenden
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: 5bb7df1b02712da3b496aa92be30d4ea02750c39
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 90%

---

# Live-Bericht zum E-Mail-Versand {#email-live-report}

Der **[!UICONTROL E-Mail-Live-Bericht]** bezieht sich nur auf einen bestimmten E-Mail-Versand.

Wählen Sie auf der Registerkarte **[!UICONTROL Ausführungen]** des Menüs **[!UICONTROL Nachrichten]** die Option **[!UICONTROL Live-Ansicht]** und wählen Sie dann im erweiterten Menü des ausgewählten Versands **[!UICONTROL Live-Bericht]**.

![](assets/live_report.png)

Der **[!UICONTROL E-Mail-Live-Bericht]** ist in verschiedene Widgets unterteilt, die den Erfolg und die Fehler Ihres Versands detailliert beschreiben. Jedes Widget kann bei Bedarf angepasst und gelöscht werden. Weiterführende Informationen dazu finden Sie in diesem [Abschnitt](live-report.md#modify-dashboard).

![](assets/live_report_5.png)

**[!UICONTROL E-Mail-Leistung]** und **[!UICONTROL Email summary]** Widgets beschreiben die wichtigsten Informationen zu Ihrer Nachricht mit einem Diagramm und KPIs:

* **[!UICONTROL Ausgewählt]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für diesen Versand eignen.

* **[!UICONTROL Gesendet]**: Gesamtzahl der Sendevorgänge für den Versand.

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Öffnungen]**: Anzahl der Öffnungen einer Nachricht in einem Versand.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in einem Versand.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

* **[!UICONTROL Beschwerden wegen Spam]**: Anzahl der als Spam klassifizierten Nachrichten.

* **[!UICONTROL Kündigungen von Abos]**: Zahl der Klicks auf den Abmelde-Link.

* **[!UICONTROL Ausgeschlossen]**: Anzahl der Benutzerprofile, die von den Zielgruppenprofilen ausgeschlossen waren und die die Nachricht nicht erhalten haben.

Das Widget **[!UICONTROL Versandstatistik]** stellt den Erfolg Ihres Versands dar:

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung.

* **[!UICONTROL Fehler]**: Gesamtanzahl der Fehler, die während des Versands aufgetreten sind und die Zustellung an Profile verhinderten.

![](assets/live_report_6.png)

In der Grafik **[!UICONTROL Fehlergründe]** und der Tabelle unten können Sie sehen, welcher Fehler während des Versands aufgetreten ist.

Die Widgets **[!UICONTROL Bounce-Gründe]** und **[!UICONTROL Bounce-Kategorien]** enthalten die verfügbaren Daten zu unzustellbaren Nachrichten wie:

* **[!UICONTROL Hardbounce]**: die Gesamtzahl der permanenten Fehler, wie eine falsche E-Mail-Adresse. Dazu gehören Fehlermeldungen, die explizit eine ungültige Adresse anzeigen, wie etwa „Benutzer unbekannt“.

* **[!UICONTROL Softbounce]**: die Gesamtzahl der temporären Fehler, wie ein voller Posteingang.

* **[!UICONTROL Ignoriert]**: Die Gesamtzahl der temporären Ereignisse, beispielsweise Abwesenheit, oder technischer Fehler, zum Beispiel wenn der Absendertyp Postmaster ist.

>[!NOTE]
>
>Die Angebots-Widgets und -Metriken sind nur verfügbar, wenn eine Entscheidung in eine E-Mail eingefügt wurde. Weiterführende Informationen zum Entscheidungs-Management finden Sie auf dieser [Seite](../offers/get-started/starting-offer-decisioning.md).

Die Widgets **[!UICONTROL Angebotsstatistiken]** und **[!UICONTROL Angebotsstatistiken]** im Zeitverlauf messen den Erfolg und die Wirkung Ihres Angebots auf Ihre Audience. Sie enthalten die wichtigsten Informationen zu Ihrer Nachricht in Form von KPIs:

* **[!UICONTROL Gesendete Angebote]**: Gibt an, wie oft das Angebot gesendet wurde.

* **[!UICONTROL Angebots-Impression]**: Gibt an, wie oft das Angebot in einem Versand geöffnet wurde.

* **[!UICONTROL Angebotsklicks]**: Gibt an, wie oft ein Angebot in einem Versand angeklickt wurde.

>[!NOTE]
>
>Die Profile mit dem Status **[!UICONTROL Unterdrückt]** oder **[!UICONTROL Nicht erlaubt]** werden während des Nachrichtenversands ausgeschlossen. Daher zeigen die **Journey-Berichte** zwar an, dass sich diese Profile durch die Journey bewegt haben (Aktivitäten [Segment lesen](../building-journeys/read-segment.md) und [Nachricht](../building-journeys/journeys-message.md)), sie sind aber nicht in der Metrik **[!UICONTROL Gesendet]** der **E-Mail-Berichte** enthalten, da sie vor dem E-Mail-Versand herausgefiltert werden.
>
>Erfahren Sie mehr über die [Unterdrückungsliste](suppression-list.md) und die [Zulassungsliste](../configuration/allow-list.md). Um den Grund für alle Ausschlussfälle zu ermitteln, können Sie den [Abfrage-Service von Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=de){target=&quot;_blank&quot;} verwenden.
