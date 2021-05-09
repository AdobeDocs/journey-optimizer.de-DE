---
title: Ausführung der Überwachungsnachricht
description: Hinweise zur Überwachung
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Nachrichtenüberwachung {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

Um sicherzustellen, dass Ihre Nachrichten erfolgreich ausgeführt, gesendet und gesendet werden, können [!DNL Journey Optimizer]-Angebote die aktuell veröffentlichten und ausgelösten Meldungen überwachen. Sie können sehen, wie Ihre Meldungen in Echtzeit von der **[!UICONTROL Liste]** auf Journey <!--and APIs-->-Ebene abschneiden.

Um auf diese Liste zuzugreifen, wählen Sie in der Startseite **[!DNL Journey Optimizer]** die Option **[!UICONTROL Nachrichten]** und klicken Sie auf die Registerkarte **[!UICONTROL Ausführen]**.

Diese Registerkarte bietet zwei Ansichten: **[!UICONTROL Live-Ansicht]** und **[!UICONTROL Globale Ansicht]**.

* Die Registerkarte **[!UICONTROL Live-Ansicht]** bietet einen **Echtzeitüberblick über alle ausgeführten Nachrichten**, die von einem oder mehreren [Journey](building-journeys/journey.md) **in den letzten 24 Stunden ausgelöst wurden.**

   ![](assets/message-execution-tab-live.png)

   Diese Liste wird alle sechzig Sekunden automatisch aktualisiert. Wenn in den letzten 24 Stunden keine Ausführung für eine bestimmte Meldung stattgefunden hat, zeigen alle Spalten für diese Meldung Null-Werte (0) an.

* Die Registerkarte **[!UICONTROL Globale Ansicht]** enthält einen **Überblick über alle ausgeführten Meldungen**, die von einem oder mehreren [Journey](building-journeys/journey.md) **seit dem Beginn der Nachricht** ausgelöst werden.

   ![](assets/message-execution-tab-global.png)

   Diese Liste wird alle neunzig Minuten automatisch aktualisiert. Die Daten werden im Zeitverlauf seit dem Beginn der einzelnen Meldungen aggregiert.

Wenn eine Nachricht veröffentlicht, aber noch nicht durch eine Journey ausgelöst wird, wird sie nicht auf einer der Registerkarten angezeigt. Es werden nur die folgenden Elemente aufgelistet:
* Nachrichten, die ausgelöst, aber noch nicht gestartet wurden (ausstehend).
* Nachrichten, die ausgelöst wurden und die derzeit ausgeführt werden (in Bearbeitung).

Bei Mehrkanalmeldungen wird für jede Nachricht eine Zeile pro Kanal angezeigt.

![](assets/message-execution-multichannel.png)

Wenn eine Meldung in mehreren Journey verwendet wurde, wird in der Spalte **[!UICONTROL Quelle]** **[!UICONTROL Mehrere]** angezeigt.

Standardmäßig werden die Meldungen ab dem letzten Ausführungsdatum angezeigt. Klicken Sie auf das Symbol **[!UICONTROL Filter]**, um die Meldungen nach dem Kanal, dem Datum des Beginns und/oder dem Enddatum zu durchsuchen.

![](assets/message-execution-tab-filters.png)

Die zweite Spalte <!--**[!UICONTROL Quick action]**-->ermöglicht es Ihnen, die entsprechende [Meldung](create-message.md) zu öffnen und auf den [Live-Bericht](reports/live-report.md) zuzugreifen, wenn Sie sich in der **[!UICONTROL Live-Ansicht]** befinden, oder den [Globalen Bericht](reports/global-report.md), wenn Sie sich in der **[!UICONTROL Ansicht]** befinden.

![](assets/message-execution-open-live-report.png)

Für jede Nachrichtenausführung werden eine Reihe von Indikatoren angezeigt:

* **[!UICONTROL Meldungsbeschriftung]**: Nachrichtentitel, den Sie beim  [Erstellen der Nachricht](create-message.md) definiert haben.
* **[!UICONTROL Execution-ID]**: Automatisch generierter Bezeichner.
* **[!UICONTROL Quelle]**: Name der Journey, die diese Meldung nutzt.
* **[!UICONTROL Beginn]**: Datum und Uhrzeit der Ausführung der Meldung von der Journey.
* **[!UICONTROL Ausgeschlossen]**: Anzahl der Profil, die aufgrund von Ausschlussregeln von der ursprünglichen Zielgruppe ausgeschlossen wurden.
* **[!UICONTROL Gesendet]**: Anzahl der gesendeten Nachrichten.
* **[!UICONTROL Ausgeliefert]**: Anzahl der erfolgreich im Postfach (E-Mail) oder auf dem Gerät (Push) des Empfängers ausgelieferten Nachrichten, ohne dass ein Absprung- oder ein sonstiger Versand-Fehler erzeugt wird.
* **[!UICONTROL Absprünge]**: Anzahl der Meldungen, die aufgrund eines Fehlers des Versands nicht gesendet werden können. [Erfahren Sie mehr über Absprünge](suppression-lists.md#delivery-failures).
* **[!UICONTROL Öffnet]**: Anzahl der Nachrichten, die geöffnet wurden.
* **[!UICONTROL Klicks]**: Anzahl der Klicks auf Links in einer E-Mail.

   >[!NOTE]
   >
   >Für Push-Benachrichtigungen sind keine Klicks vorhanden: Wenn ein Benutzer auf eine Push-Benachrichtigung klickt, wird die App geöffnet, die nur als geöffnet betrachtet werden kann.

* **[!UICONTROL Fehler]**: Anzahl der Nachrichten, die aufgrund eines technischen Fehlers nicht gesendet werden können.

Wenn Sie auf jeden Hyperlink klicken, wird die zugehörige Ansicht für die Nachrichtenübersicht geöffnet. [Weitere Informationen zu Nachrichten](create-message.md).
