---
title: Erste Schritte mit Journeys
description: Erste Schritte mit Journeys
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
source-git-commit: f2c280ba3d2148a62eebff421ef6c8c3c0352936
workflow-type: tm+mt
source-wordcount: '1747'
ht-degree: 78%

---

# Erste Schritte mit Journeys{#jo-quick-start}

## Voraussetzungen

Um Nachrichten mit Journeys zu senden, ist folgende Konfiguration notwendig:

1. **Ereignis konfigurieren**: Wenn Sie Ihre Journeys beim Empfang eines Ereignisses unitär triggern möchten, müssen Sie zunächst ein Ereignis konfigurieren. Sie definieren die erwarteten Informationen sowie deren Verarbeitungsmethode. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../event/about-events.md).

   ![](../assets/jo-event7bis.png)

1. **Segment erstellen**: Ihre Journey kann auch Adobe Experience Platform-Segmente überwachen, um Nachrichten als Batch an einen bestimmten Satz von Profilen zu senden. Dazu müssen Sie Segmente erstellen. [Mehr dazu](../segment/about-segments.md).

   ![](../assets/segment2.png)

1. **Datenquelle konfigurieren**: Sie können eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung bei Ihren Journeys abzurufen (z. B. in Ihren Bedingungen). Außerdem wird zur Bereitstellungszeit eine integrierte Adobe Experience Platform-Datenquelle konfiguriert. Dieser Schritt ist nicht erforderlich, wenn Sie ausschließlich Daten aus den Ereignissen Ihrer Journey nutzen. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../datasource/about-data-sources.md)

   ![](../assets/jo-datasource.png)

1. **Aktion konfigurieren**: Die Journey Optimizer-Nachrichtenfunktionen sind integriert. Sie müssen lediglich Ihren Inhalt entwerfen und Ihre Nachricht veröffentlichen. Weitere Informationen finden Sie in [diesem Abschnitt](../get-started-content.md). Wenn Sie für den Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weitere Informationen finden Sie in diesem [Abschnitt](../action/action.md). Dieser Schritt wird von einem **technischen Anwender** ausgeführt.

   ![](../assets/create-content-push.png)

## Erstellen Ihrer Journey {#jo-build}

Dieser Schritt wird vom **Business-Anwender** ausgeführt. Hier erstellen Sie Ihre Journeys. Kombinieren Sie die verschiedenen Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um Ihre mehrstufigen kanalübergreifenden Szenarien zu erstellen.

Hier finden Sie die wichtigsten Schritte zum Senden von Nachrichten über Journeys:

1. Klicken Sie im Menüabschnitt JOURNEY MANAGEMENT auf **[!UICONTROL Journey]**. Die Liste der Journeys wird angezeigt.

   ![](../assets/interface-journeys.png)

1. Klicken Sie auf **[!UICONTROL Journey]** erstellen , um eine neue Journey zu erstellen.

1. Bearbeiten Sie im Konfigurationsbereich auf der rechten Seite die Eigenschaften der Journey. Weitere Informationen finden Sie in diesem [Abschnitt](journey-gs.md#change-properties).

   ![](../assets/jo-properties.png)

1. Ziehen Sie zunächst ein Ereignis oder eine Aktivität vom Typ **Segment lesen** aus der Palette in die Arbeitsfläche. Weitere Informationen zum Entwerfen von Journeys finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

   ![](../assets/read-segment.png)

1. Ziehen Sie die nächsten Schritte, die der Kontakt ausführen soll, per Drag-and-Drop. Sie können beispielsweise eine Bedingung und anschließend eine Nachricht hinzufügen. Weitere Informationen zu Aktivitäten finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

1. Testen Sie Ihre Journey mit Testprofilen. Weitere Informationen finden Sie in diesem [Abschnitt](testing-the-journey.md)

1. Veröffentlichen Sie Ihre Journey, um sie zu aktivieren. Weitere Informationen finden Sie in diesem [Abschnitt](publishing-the-journey.md).

   ![](../assets/jo-journeyuc2_32bis.png)

1. Überwachen Sie Ihre Journey mithilfe der dedizierten Reporting-Tools, um die Effektivität Ihrer Journey zu messen. Weitere Informationen finden Sie in diesem [Abschnitt](../reports/live-report.md).

   ![](../assets/jo-dynamic_report_journey_12.png)

## Ändern von Eigenschaften {#change-properties}

Klicken Sie auf das Bleistiftsymbol oben rechts, um auf die Eigenschaften der Journey zuzugreifen. 

Wenn Sie ein Administrator sind, können Sie den Namen der Journey ändern, eine Beschreibung hinzufügen, den erneuten Eintritt erlauben, Start- und Enddatum auswählen und eine Dauer für **[!UICONTROL Zeitüberschreitung und Fehler]** festlegen.

Mit der Schaltfläche **Technische Details kopieren** lassen sich jederzeit technische Informationen zur Journey kopieren, die dem Support-Team bei der Problembehebung helfen. Dabei werden die folgenden Informationen kopiert: JourneyVersion UID, OrgID, orgName, sandboxName.

![](../assets/journey32.png)

### Eintritt{#entrance}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt. In diesem Fall möchten Sie nicht, dass der Kunde die Journey erneut betreten und das Angebot erneut wahrnehmen kann.

Wenn eine Journey &quot;endet&quot;, hat sie den Status **[!UICONTROL Geschlossen]**. Die Journey erlaubt den Eintritt neuer Kontakte nicht mehr. Personen, die sich bereits in der Journey befinden, beenden die Journey wie gewohnt.

Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wechselt die Journey zum Status **Beendet**. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey-gs.md#global_timeout).

### Zeitüberschreitung und Fehler bei Journey-Aktivitäten {#timeout_and_error}

Beim Bearbeiten einer Aktions- oder Bedingungsaktivität können Sie im Falle eines Fehlers oder einer Zeitüberschreitung einen alternativen Pfad definieren. Wenn die Verarbeitung der Aktivität, die ein Drittanbietersystem abfragt, die in den Eigenschaften der Journey festgelegte Dauer der maximalen Wartezeit überschreitet (Feld **[!UICONTROL Zeitüberschreitung und Fehler]**), wird der zweite Pfad ausgewählt, um eine potenzielle Ausweichaktion durchzuführen.

Die zulässigen Werte liegen zwischen 1 und 30 Sekunden.

Es wird empfohlen, unter **[!UICONTROL Zeitüberschreitung und Fehler]** einen sehr kurzen Wert festzulegen, wenn Ihre Journey zeitkritisch ist (z. B. Reaktion auf den Echtzeit-Standort einer Person), da Sie Ihre Aktion nicht länger als einige Sekunden verzögern können. Wenn Ihre Journey weniger zeitkritisch ist, können Sie einen längeren Wert verwenden, um dem aufgerufenen System mehr Zeit zum Senden einer gültigen Antwort zu geben.

Bei Journeys wird auch eine maximale globale Wartezeit verwendet. Siehe [nächster Abschnitt](#global_timeout).

### Maximale globale Wartezeit der Journey {#global_timeout}

Zusätzlich zu der in den Journey-Aktivitäten verwendeten [maximalen Wartezeit](#timeout_and_error) gibt es auch eine maximale globale Journey-Wartezeit, die nicht auf der Benutzeroberfläche angezeigt wird und nicht geändert werden kann. Diese maximale Wartezeit stoppt den Fortschritt von Kontakten in der Journey 30 Tage nach ihrem Eintritt. Das bedeutet, dass die Journey eines Kontakts nicht länger als 30 Tage dauern kann. Nach Ablauf der maximalen Wartezeit von 30 Tagen werden die Daten des Kontakts gelöscht. Kontakte, die sich nach der maximalen Wartezeit noch in der Journey befinden, werden gestoppt und beim Reporting als Fehler gewertet.

>[!NOTE]
>
>Journeys reagieren nicht direkt auf Datenschutz-Opt-out-, Zugriffs- oder Löschanfragen. Die maximale globale Wartezeit stellt jedoch sicher, dass Kontakte auf keinen Fall länger als 30 Tage in der Journey bleiben.

Aufgrund der maximalen Journey-Wartezeit von 30 Tagen können wir, wenn der erneute Eintritt nicht erlaubt ist, nicht sicherstellen, dass die Sperrung des erneuten Eintritts nach mehr als 30 Tagen erhalten bleibt. Da wir alle Informationen über Personen, die an der Journey teilgenommen haben, 30 Tage nach deren Eintritt entfernen, können wir nicht wissen, dass die Person vor mehr als 30 Tagen bereits Eintritt hatte.

### Zeitzone und Zeitzone des Profils {#timezone}

Die Zeitzone wird auf Journey-Ebene definiert.

Sie können eine feste Zeitzone eingeben oder Adobe Experience Platform-Profile verwenden, um die Zeitzone der Journey festzulegen.

Weitere Informationen zum Zeitzonen-Management finden Sie auf [dieser Seite](../building-journeys/timezone-management.md).

### Burst-Modus {#burst}

Der Burst-Modus ist ein kostenpflichtiges Add-on, das den sehr schnellen Versand großer Mengen von Push-Nachrichten ermöglicht. Sie wird für einfache Journey verwendet, die ein Lesesegment und eine einfache Push-Nachricht enthalten. Burst wird verwendet, wenn eine Verzögerung beim Nachrichtenversand geschäftskritisch ist, wenn Sie eine dringende Push-Benachrichtigung auf Mobiltelefone senden möchten, z. B. eine brechende Nachricht an Benutzer, die Ihre News-Kanal-App installiert haben.

Einschränkungen:

* Die Journey muss mit einem Lesesegment beginnen. Ereignisse sind nicht zulässig.
* Der nächste Schritt muss eine Push-Nachricht sein. Es ist keine andere Aktivität oder ein anderer Schritt zulässig (mit Ausnahme der optionalen Endaktivität):
   * Nur Push-Kanal
   * In der Nachricht ist keine Personalisierung zulässig
   * Die Nachricht muss klein sein (&lt;2 KB)

Wichtiger Hinweis:

Wenn eine der Anforderungen nicht erfüllt ist, ist der Burst-Modus im Journey nicht verfügbar.

Um den Burst-Modus zu aktivieren, öffnen Sie Ihre Journey und klicken Sie auf das Stiftsymbol oben rechts, um auf die Eigenschaften des Journey zuzugreifen. Aktivieren Sie dann den Umschalter **Burst-Modus** aktivieren.

![](../assets/burst.png)

Der Burst-Modus wird deaktiviert, wenn Sie eine Burst-Journey ändern und eine Aktivität hinzufügen, die nicht mit Burst konform ist (Nachricht, andere Aktionen, ein Ereignis usw.). Daraufhin wird eine Nachricht angezeigt.

![](../assets/burst2.png)

Testen und veröffentlichen Sie dann Ihre Journey normal. Testmodus-Nachrichten werden nicht über den Burst-Modus gesendet.

## Beenden einer Journey

Eine Journey kann für einen Kontakt aus zwei Gründen enden:

* Die Person kommt bei der letzten Aktivität eines Pfades an. Diese letzte Aktivität kann eine Endaktivität oder eine andere Aktivität sein. Sie müssen einen Pfad nicht mit einer Endaktivität beenden. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/end-activity.md).
* Die Person kommt bei einer Bedingungsaktivität (oder einer Warteaktivität mit einer Bedingung) an und erfüllt keine der Bedingungen.

Die Person kann dann wieder in die Journey eintreten, wenn der erneute Zutritt erlaubt ist. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/journey-gs.md#change-properties)

Eine Journey kann aus den folgenden Gründen geschlossen werden:

* Die Journey wird manuell über die Schaltfläche **[!UICONTROL Für neue Eintritte schließen]** geschlossen.
* Eine segmentbasierte Journey zur einmaligen Ausführung wurde abgeschlossen.
* Nach dem letzten Auftreten einer wiederkehrenden segmentbasierten Journey.

Wenn eine Journey geschlossen wird (aus einem der oben genannten Gründe), erhält sie den Status **[!UICONTROL Geschlossen]**. Die Journey stoppt den Eintritt neuer Kontakte. Personen, die sich bereits in der Journey befinden, beenden die Journey wie gewohnt. Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wechselt die Journey zum Status **Beendet**. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey-gs.md#global_timeout).

Falls Sie den Fortschritt aller Personen in der Journey stoppen müssen, können Sie das tun. In diesem Fall entsteht für alle Personen in der Journey eine Zeitüberschreitung.

So kann eine Journey manuell geschlossen oder gestoppt werden:

Mit den Optionen **[!UICONTROL Stoppen]** und **[!UICONTROL Für neue Eintritte schließen]** können Sie **Live**-Journeys beenden. Wenn Sie eine Journey schließen, wird **der Eintritt neuer Kunden in die Journey blockiert** und die bereits in der Journey befindlichen Kunden können diese bis zum Ende durchlaufen. Dies ist die empfohlene Art, eine Journey zu beenden, da sie für die Kunden das beste Erlebnis bietet. Wenn Sie hingegen eine Journey stoppen, wird die Reise der bereits in der Journey befindlichen Personen abgebrochen. Die Journey wird praktisch deaktiviert.

>[!NOTE]
>
>Beachten Sie, dass Sie eine geschlossene oder gestoppte Journey nicht fortsetzen können.

### Schließen einer Journey

Sie können eine Journey manuell schließen. In diesem Fall können Kunden, die sich bereits in der Journey befinden, ihren Pfad bis zum Ende verfolgen, neue Anwender können jedoch nicht in die Journey eintreten.

Wenn eine Journey geschlossen wird, erhält sie den Status **[!UICONTROL Geschlossen]**. Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wechselt die Journey zum Status **Beendet**. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey-gs.md#global_timeout).

Eine geschlossene Journey-Version kann weder neu gestartet noch gelöscht werden. Stattdessen können Sie eine neue Version davon erstellen oder sie duplizieren. Nur abgeschlossene Journeys können gelöscht werden.

Um eine Journey aus der Liste der Journey zu schließen, klicken Sie auf die Schaltfläche **[!UICONTROL Ellipsis]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

![](../assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie schließen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](../assets/finish_drop_down_list.png)

1. Klicken Sie auf **[!UICONTROL Für neue Eintritte schließen]**. Das folgende Dialogfeld wird angezeigt.
1. Klicken Sie zur Bestätigung auf **[!UICONTROL Für neue Eintritte schließen]**.

### Stoppen einer Journey

Sie können eine Journey stoppen, wenn ein unerwartetes Ereignis eintritt und die gesamte Verarbeitung der Journey unverzüglich abgebrochen werden muss.

Eine gestoppte Journey-Version kann nicht nochmals gestartet werden.

Wird eine Journey gestoppt, hat sie den Status **[!UICONTROL Gestoppt]**.

Sie können beispielsweise eine Journey stoppen, wenn ein Marketingspezialist erkennt, dass die Journey auf die falsche Audience ausgerichtet ist, oder wenn eine benutzerdefinierte Aktion, mit der Nachrichten gesendet werden sollen, nicht ordnungsgemäß funktioniert. Um eine Journey aus der Liste der Journey zu entfernen, klicken Sie auf die Schaltfläche **[!UICONTROL Ellipsis]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Stopp]** aus.

![](../assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie stoppen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

![](../assets/finish_drop_down_list.png)

1. Klicken Sie auf **[!UICONTROL Anhalten]**. Das folgende Dialogfeld wird angezeigt.
1. Klicken Sie zur Bestätigung auf **[!UICONTROL Stoppen]**.
