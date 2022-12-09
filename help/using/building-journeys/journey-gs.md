---
solution: Journey Optimizer
product: journey optimizer
title: Erste Journey erstellen
description: Wichtige Schritte beim Aufbau Ihrer ersten Journey mit Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 978751263ba2ed21e35e41e767f1e31ddbe59d53
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# Erste Journey erstellen{#jo-quick-start}

## Voraussetzungen{#start-prerequisites}

Um Nachrichten mit Journeys zu senden, sind die folgenden Konfigurationen erforderlich:

1. **Ereignis konfigurieren**: Wenn Sie Ihre Journeys beim Empfang eines Ereignisses einheitlich auslösen möchten, müssen Sie ein Ereignis konfigurieren. Sie definieren die erwarteten Informationen und deren Verarbeitung. Dieser Schritt wird von einem **technischer Anwender**. [Mehr dazu](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Segment erstellen**: Ihre Journey kann auch Adobe Experience Platform-Segmente überwachen, um Nachrichten im Batch-Modus an eine bestimmte Gruppe von Profilen zu senden. Dazu müssen Sie Segmente erstellen. [Mehr dazu](../segment/about-segments.md).

   ![](assets/segment2.png)

1. **Konfigurieren der Datenquelle**: Sie können eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Journeys verwendet werden, z. B. in Ihren Bedingungen. Eine integrierte Adobe Experience Platform-Datenquelle wird ebenfalls zur Bereitstellungszeit konfiguriert. Dieser Schritt ist nicht erforderlich, wenn Sie nur Daten aus den Ereignissen in Ihrer Journey nutzen. Dieser Schritt wird von einem **technischer Anwender**. [Mehr dazu](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Konfigurieren einer Aktion**: Wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden, können Sie eine benutzerdefinierte Aktion erstellen. Weitere Informationen finden Sie hier . [Abschnitt](../action/action.md). Dieser Schritt wird von einem **technischer Anwender**. Wenn Sie die integrierten Nachrichtenfunktionen von Journey Optimizer verwenden, müssen Sie Ihrer Journey lediglich eine Kanalaktion hinzufügen und Ihre Inhalte entwerfen.

   ![](assets/custom2.png)

## Erstellen Ihrer Journey{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Erstellen Ihrer Journey"
>abstract="Auf diesem Bildschirm wird die Liste der vorhandenen Journeys angezeigt. Öffnen Sie eine Journey oder klicken Sie auf &quot;Journey erstellen&quot;und kombinieren Sie die verschiedenen Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um Ihre mehrstufigen kanalübergreifenden Szenarien zu erstellen."

Dieser Schritt wird von der **Business-Anwender**. Hier erstellen Sie Ihre Journeys. Kombinieren Sie die verschiedenen Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um Ihre mehrstufigen kanalübergreifenden Szenarien zu erstellen.

Im Folgenden finden Sie die wichtigsten Schritte zum Senden von Nachrichten durch Journeys:

1. Klicken Sie im Menüabschnitt JOURNEY MANAGEMENT auf **[!UICONTROL Journeys]**. Die Liste der Journeys wird angezeigt.

   ![](assets/interface-journeys.png)

1. Klicken **[!UICONTROL Create Journey]** , um eine neue Journey zu erstellen.

1. Bearbeiten Sie die Eigenschaften der Journey im Konfigurationsbereich, der auf der rechten Seite angezeigt wird. Weitere Informationen finden Sie hier . [Abschnitt](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Beginnen Sie mit dem Ziehen und Ablegen eines Ereignisses oder eines **Segment lesen** Aktivität von der Palette in die Arbeitsfläche. Weitere Informationen zum Design von Journeys finden Sie unter [diesem Abschnitt](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Ziehen Sie die nächsten Schritte, denen der Kontakt folgen wird, per Drag-and-Drop in den Arbeitsbereich. Sie können beispielsweise eine Bedingung und danach eine Kanalaktion hinzufügen. Weitere Informationen zu Aktivitäten finden Sie unter [diesem Abschnitt](using-the-journey-designer.md).

1. Testen Sie Ihre Journey mit Testprofilen. Weitere Informationen finden Sie hier . [Abschnitt](testing-the-journey.md)

1. Veröffentlichen Sie Ihre Journey, um sie zu aktivieren. Weitere Informationen finden Sie hier . [Abschnitt](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Überwachen Sie Ihre Journey mithilfe der dedizierten Reporting-Tools, um die Effektivität Ihrer Journey zu messen. Weitere Informationen finden Sie hier . [Abschnitt](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Eigenschaften Ihrer Journey definieren {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Journey-Eigenschaften"
>abstract="Dieser Abschnitt zeigt die Eigenschaften der Journey. Standardmäßig sind schreibgeschützte Parameter ausgeblendet. Die verfügbaren Einstellungen hängen vom Status der Journey, von Ihren Berechtigungen und der Produktkonfiguration ab."

Klicken Sie oben rechts auf das Stiftsymbol, um auf die Eigenschaften der Journey zuzugreifen.

Sie können den Namen der Journey ändern, eine Beschreibung hinzufügen, den erneuten Eintritt erlauben, Start- und Enddaten auswählen und als Administrator eine **[!UICONTROL Timeout and error]** Dauer.

Bei Live-Journeys zeigt dieser Bildschirm das Veröffentlichungsdatum und den Namen des Benutzers an, der die Journey veröffentlicht hat.

Die **Technische Details kopieren** können Sie technische Informationen über die Journey kopieren, die das Supportteam zur Fehlerbehebung verwenden kann. Die folgenden Informationen werden kopiert: JourneyVersion UID, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Eintritt{#entrance}

Standardmäßig ist bei neuen Journeys der erneute Eintritt erlaubt. Sie können die Option für &quot;einmalige&quot;Journeys deaktivieren, z. B. wenn Sie ein einmaliges Geschenk anbieten möchten, wenn eine Person einen Shop betritt.

Erfahren Sie mehr über die Verwaltung des Profileintritts in [diesem Abschnitt](entry-management.md).

### Zeitüberschreitung und Fehler in Journey-Aktivitäten {#timeout_and_error}

Beim Bearbeiten einer Aktion- oder Bedingungsaktivität können Sie im Falle von Fehlern oder Timeouts einen alternativen Pfad definieren. Wenn die Verarbeitung der Aktivität, die ein Drittanbietersystem abfragt, die in den Eigenschaften der Journey definierte Timeout-Dauer überschreitet (**[!UICONTROL Timeout and  error]** ), wird der zweite Pfad ausgewählt, um eine potenzielle Ausweichaktion durchzuführen.

Die zulässigen Werte liegen zwischen 1 und 30 Sekunden.

Es wird empfohlen, eine sehr kurze **[!UICONTROL Timeout and error]** Wert, wenn Ihre Journey zeitkritisch ist (Beispiel: Reaktion auf den Echtzeitstandort einer Person), da Sie Ihre Aktion nicht länger als einige Sekunden verzögern können. Wenn Ihre Journey weniger zeitkritisch ist, können Sie einen längeren Wert verwenden, um dem aufgerufenen System mehr Zeit zum Senden einer gültigen Antwort zu geben.

Journeys verwenden auch eine globale Zeitüberschreitung. Siehe [nächster Abschnitt](#global_timeout).

### Globale Journey-Zeitüberschreitung {#global_timeout}

Zusätzlich zu den [timeout](#timeout_and_error) in Journey-Aktivitäten verwendet wird, gibt es auch einen globalen Journey-Timeout, der nicht in der Benutzeroberfläche angezeigt wird und nicht geändert werden kann. Diese Zeitüberschreitung stoppt den Fortschritt von Kontakten in der Journey 30 Tage nach ihrem Eintritt. Das bedeutet, dass die Journey eines Kontakts nicht länger als 30 Tage dauern kann. Nach dem Timeout-Zeitraum von 30 Tagen werden die Daten des Kontakts gelöscht. Kontakte, die sich noch am Ende des Timeout-Zeitraums in der Journey befinden, werden gestoppt und bei der Berichterstellung als Fehler berücksichtigt.

>[!NOTE]
>
>Journeys reagieren nicht direkt auf Datenschutz-Opt-out-, Zugriffs- oder Löschanfragen. Die globale Zeitüberschreitung stellt jedoch sicher, dass Kontakte in keiner Journey länger als 30 Tage bleiben.

Aufgrund des 30-Tage-Journey-Timeouts können wir nicht sicherstellen, dass die Sperrung des erneuten Eintritts länger als 30 Tage funktioniert, wenn der erneute Eintritt in die Journey nicht erlaubt ist. Da wir alle Informationen über Personen entfernen, die 30 Tage nach ihrem Eintritt in die Journey eingestiegen sind, können wir nicht wissen, dass die Person vor mehr als 30 Tagen bereits eingestiegen ist.

### Zeitzone und Zeitzone des Profils {#timezone}

Die Zeitzone wird auf Journey-Ebene definiert.

Sie können eine feste Zeitzone eingeben oder Adobe Experience Platform-Profile verwenden, um die Zeitzone der Journey zu definieren.

Wenn eine Zeitzone im Adobe Experience Platform-Profil definiert ist, kann sie in der Journey abgerufen werden.

Weitere Informationen zum Zeitzonen-Management finden Sie unter [diese Seite](../building-journeys/timezone-management.md).

### Zugriff verwalten {#access}

Um der Journey benutzerspezifische oder zentrale Datennutzungsbezeichnungen zuzuweisen, klicken Sie auf das **[!UICONTROL Manage access]** Schaltfläche. [Weitere Informationen zur Zugriffskontrolle auf Objektebene (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)
