---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journeys
description: Wichtige Schritte zum Erstellen Ihrer ersten Journey mit Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 412f7efe2da9f9b1a8fa49f1243ca63c4e0d01c0
workflow-type: ht
source-wordcount: '1012'
ht-degree: 100%

---

# Erste Schritte mit Journeys{#jo-quick-start}

## Voraussetzungen{#start-prerequisites}

Um Nachrichten mit Journeys zu senden, sind folgende Konfigurationen notwendig:

1. **Ereignis konfigurieren**: Wenn Sie Ihre Journeys beim Empfang eines Ereignisses unitär triggern möchten, müssen Sie zunächst ein Ereignis konfigurieren. Sie definieren die erwarteten Informationen sowie deren Verarbeitungsmethode. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Segment erstellen**: Ihre Journey kann auch Adobe Experience Platform-Segmente überwachen, um Nachrichten als Batch an einen bestimmten Satz von Profilen zu senden. Dazu müssen Sie Segmente erstellen. [Weitere Informationen](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Konfigurieren einer Datenquelle**: Sie können eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung bei Ihren Journeys abzurufen (z. B. in Ihren Bedingungen). Außerdem wird zur Bereitstellungszeit eine integrierte Adobe Experience Platform-Datenquelle konfiguriert. Dieser Schritt ist nicht erforderlich, wenn Sie ausschließlich Daten aus den Ereignissen Ihrer Journey nutzen. Dieser Schritt wird von einem **technischen Anwender** ausgeführt. [Mehr dazu](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Konfigurieren einer Aktion**: Wenn Sie für den Versand Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../action/action.md). Dieser Schritt wird von einem **technischen Anwendenden** ausgeführt. Wenn Sie integrierte Nachrichtenfunktionen von Journey Optimizer verwenden, müssen Sie lediglich eine Kanalaktion zu Ihrer Journey hinzufügen und Inhalte entwerfen. Weitere Informationen finden Sie in [diesem Abschnitt](../messages/get-started-content.md).

   ![](assets/custom2.png)

## Erstellen Ihrer Journey{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Erstellen Ihrer Journey"
>abstract="Auf diesem Bildschirm wird die Liste der vorhandenen Journey angezeigt. Öffnen Sie eine Journey oder klicken Sie auf „Journey erstellen“ und kombinieren Sie die verschiedenen Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um mehrstufige kanalübergreifende Szenarien zu erstellen."

Dieser Schritt wird vom **Business-Anwender** ausgeführt. Hier erstellen Sie Ihre Journeys. Kombinieren Sie die verschiedenen Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um Ihre mehrstufigen kanalübergreifenden Szenarien zu erstellen.

Hier finden Sie die wichtigsten Schritte zum Senden von Nachrichten über Journeys:

1. Klicken Sie im Menü JOURNEY-MANAGEMENT auf **[!UICONTROL Journeys]**. Die Liste der Journeys wird angezeigt.

   ![](assets/interface-journeys.png)

1. Klicken Sie auf **[!UICONTROL Journey erstellen]**, um eine neue Journey zu erstellen.

1. Bearbeiten Sie im Konfigurationsbereich auf der rechten Seite die Eigenschaften der Journey. Weiterführende Informationen finden Sie in diesem [Abschnitt](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Ziehen Sie zuerst ein Ereignis oder die Aktivität **Segment lesen** per Drag-and-Drop aus der Palette in die Arbeitsfläche. Weitere Informationen zum Entwerfen von Journeys finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Ziehen Sie die nächsten Schritte, die der Kontakt ausführen soll, per Drag-and-Drop. Sie können beispielsweise eine Bedingung und anschließend eine Kanalaktion hinzufügen. Weitere Informationen zu Aktivitäten finden Sie in [diesem Abschnitt](using-the-journey-designer.md).

1. Testen Sie Ihre Journey mit Testprofilen. Weitere Informationen finden Sie in diesem [Abschnitt](testing-the-journey.md)

1. Veröffentlichen Sie Ihre Journey, um sie zu aktivieren. Weitere Informationen finden Sie in diesem [Abschnitt](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Überwachen Sie Ihre Journey mithilfe der dedizierten Reporting-Tools, um die Effektivität Ihrer Journey zu messen. Weiterführende Informationen finden Sie in diesem [Abschnitt](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Definieren der Journey-Eigenschaften {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journey-Eigenschaften"
>abstract="In diesem Abschnitt werden die Journey-Eigenschaften angezeigt. Standardmäßig sind schreibgeschützte Parameter ausgeblendet. Die verfügbaren Einstellungen hängen vom Status der Journey, von Ihren Berechtigungen und der Produktkonfiguration ab."

Klicken Sie auf das Bleistiftsymbol oben rechts, um auf die Eigenschaften der Journey zuzugreifen.

Sie können den Namen der Journey ändern, eine Beschreibung hinzufügen, den erneuten Eintritt erlauben, Start- und Enddatum auswählen und, wenn Sie ein Administrator sind, eine Dauer für **[!UICONTROL Zeitüberschreitung und Fehler]** festlegen.

Für Live-Journeys werden in diesem Bildschirm das Veröffentlichungsdatum und der Name des Benutzers angezeigt, der die Journey veröffentlicht hat.

Mit der Schaltfläche **Technische Details kopieren** lassen sich jederzeit technische Informationen zur Journey kopieren, die dem Support-Team bei der Problembehebung helfen. Dabei werden die folgenden Informationen kopiert: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Eintritt{#entrance}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für „einmalige“ Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt.

Weitere Informationen zur Verwaltung des Profileintritts finden sich in [diesem Abschnitt](entry-management.md).

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

Wenn eine Zeitzone im Adobe Experience Platform-Profil definiert ist, kann sie in der Journey abgerufen werden.

Weitere Informationen zum Zeitzonen-Management finden Sie auf [dieser Seite](../building-journeys/timezone-management.md).

### Verwalten des Zugriffs {#access}

Um der Journey benutzerdefinierte oder Core-Datennutzungsbezeichnungen zuzuweisen, klicken Sie auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**. [Weitere Informationen zur Zugriffssteuerung auf Objektebene (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
