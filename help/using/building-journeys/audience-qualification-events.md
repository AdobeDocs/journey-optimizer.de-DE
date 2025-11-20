---
solution: Journey Optimizer
product: journey optimizer
title: Zielgruppen-Qualifizierungsereignisse
description: Informationen zum Verwenden und Konfigurieren von Zielgruppenqualifizierungsereignissen
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: Qualifizierung, Ereignisse, Zielgruppe, Journey, Plattform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
version: Journey Orchestration
source-git-commit: b8c2eced0f517e917021e9f42a8943b4a5e4f287
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 93%

---

# Zielgruppen-Qualifizierungsereignisse {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Zielgruppen-Qualifizierungsereignisse"
>abstract="Mit dieser Aktivität kann eine Journey die Ein- und Austritte von Profilen in Adobe Experience Platform-Zielgruppen überwachen, damit Personen in eine Journey eintreten oder damit fortfahren."

## Informationen zu Zielgruppen-Qualifizierungsereignissen{#about-segment-qualification}

Mit dieser Aktivität kann eine Journey die Ein- und Austritte von Profilen in Adobe Experience Platform-Zielgruppen überwachen, damit Personen in eine Journey eintreten oder damit fortfahren. Weitere Informationen zum Erstellen von Zielgruppen finden Sie in diesem [Abschnitt](../audience/about-audiences.md).

Angenommen, Sie verfügen über eine Zielgruppe für „Silber-Kundinnen und -Kunden“. Mit dieser Aktivität können Sie dafür sorgen, dass alle neuen Silber-Kunden eine Journey beginnen, und ihnen eine Reihe personalisierter Nachrichten senden.

Diese Art von Ereignis kann als erster Schritt oder auch später in der Journey positioniert werden.

➡️ [Funktion im Video kennenlernen](#video)


>[!CAUTION]
>
>Bevor Sie mit der Konfiguration einer Zielgruppenqualifizierung beginnen, [lesen Sie die Informationen zu Leitlinien und Einschränkungen](#audience-qualification-guardrails).


## Konfigurieren der Aktivität {#configure-segment-qualification}

Gehen Sie wie folgt vor, um die Aktivität **[!UICONTROL Zielgruppen-Qualifizierung]** zu konfigurieren:

1. Erweitern Sie die Kategorie **[!UICONTROL Ereignisse]** und legen Sie eine Aktivität vom Typ **[!UICONTROL Zielgruppen-Qualifizierung]** in Ihrer Arbeitsfläche ab.

   ![Zielgruppen-Qualifizierungsereignis in der Journey-Palette](assets/segment5.png)

1. Fügen Sie der Aktivität ein **[!UICONTROL Label]** hinzu. Dieser Schritt ist optional.

1. Klicken Sie in das Feld **[!UICONTROL Zielgruppe]** und wählen Sie die gewünschten Zielgruppen aus.

   >[!NOTE]
   >
   >Die in der Liste angezeigten Spalten können angepasst und sortiert werden.

   ![Dropdown-Liste zur Zielgruppenauswahl für die Konfiguration von Qualifizierungsereignissen](assets/segment6.png)

   Nachdem die Zielgruppe hinzugefügt wurde, können Sie mit der Schaltfläche **[!UICONTROL Kopieren]** deren Namen und ID kopieren:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![Schaltfläche „Kopieren“ zum Kopieren von Zielgruppenname und ID im JSON-Format](assets/segment-copy.png)

1. Wählen Sie im Feld **[!UICONTROL Verhalten]** aus, ob Zielgruppeneintritte, -austritte oder beides überwacht werden soll.

   >[!NOTE]
   >
   >**[!UICONTROL Eintreten]** und **[!UICONTROL Aussteigen]** entsprechen den Zielgruppenzugehörigkeitsstatus **Realisiert** und **Ausgestiegen** von Adobe Experience Platform. Weitere Informationen zum Auswerten einer Zielgruppe finden Sie in der [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/tutorials/evaluate-a-segment#interpret-segment-results){target="_blank"}.

1. Wählen Sie einen Namespace aus. Dies ist nur erforderlich, wenn das Ereignis als erster Schritt der Journey positioniert wird. Standardmäßig ist das Feld mit dem zuletzt verwendeten Namespace vorausgefüllt.

   >[!NOTE]
   >
   >Sie können nur einen personenbasierten Identity-Namespace auswählen. Wenn Sie einen Namespace für eine Suchtabelle definiert haben (z. B.: Produkt-ID-Namespace für eine Produktsuche), ist er nicht in der Dropdown-Liste **Namespace** verfügbar.

   ![Namespace-Auswahl für die Zielgruppen-Qualifizierungs-Identität](assets/segment7.png)

Die Payload enthält die folgenden Kontextinformationen, die Sie in Bedingungen und Aktionen verwenden können:

* Verhalten (Eintritt, Austritt)
* Zeitstempel der Qualifizierung
* Zielgruppen-ID

Wenn Sie den Ausdruckseditor in einer Bedingung oder Aktion verwenden, die einer Aktivität vom Typ **[!UICONTROL Zielgruppen-Qualifizierung]** folgt, können Sie auf den Knoten **[!UICONTROL AudienceQualification]** zugreifen. Sie können zwischen der **[!UICONTROL letzten Qualifizierungszeit]** und dem **[!UICONTROL Status]** (Einstieg oder Ausstieg) wählen.

Siehe [Bedingungsaktivität](../building-journeys/condition-activity.md#about_condition).

Eine neue Journey, die ein Ereignis **Zielgruppen-Qualifizierung** enthält, ist zehn Minuten nach der Veröffentlichung einsatzbereit. Dieses Zeitintervall entspricht dem Cache-Aktualisierungsintervall des dedizierten Services. Daher müssen Sie zehn Minuten warten, bevor Sie diese Journey verwenden.

## Best Practices {#best-practices-segments}

Mit der Aktivität **[!UICONTROL Zielgruppen-Qualifizierung]** wird der sofortige Eintritt in Journeys von Kontakten möglich, die über eine Adobe Experience Platform-Zielgruppe qualifiziert oder disqualifiziert werden.

Die Empfangsgeschwindigkeit dieser Daten ist hoch. Durchgeführte Messungen zeigen eine Geschwindigkeit von 10.000 empfangenen Ereignissen pro Sekunde. Daher sollten Sie wissen, wie Eintrittsspitzen auftreten können, wie sie sich vermeiden lassen und wie Sie Ihren Journey darauf vorbereiten können. Weitere Informationen zu Journey-Verarbeitungsraten und Durchsatzbeschränkungen finden Sie in [diesem Abschnitt](entry-management.md#journey-processing-rate).

### Batch-Zielgruppen {#batch-speed-segment-qualification}

Bei Verwendung der Zielgruppen-Qualifizierung für eine Batch-Zielgruppe tritt zum Zeitpunkt der täglichen Berechnung eine Eintrittsspitze auf. Der Umfang dieser Spitze hängt von der Zahl der Kontakte ab, die täglich in die Zielgruppe eintreten (bzw. aus ihr aussteigen).

Wenn die Batch-Zielgruppe neu erstellt und unmittelbar in einer Journey verwendet wird, kann der erste Berechnungs-Batch außerdem dazu führen, dass sehr viele Kontakte in die Journey eintreten.

### Streaming-Zielgruppen {#streamed-speed-segment-qualification}

Bei Verwendung der Zielgruppen-Qualifizierung für Streaming-Zielgruppen besteht aufgrund der kontinuierlichen Auswertung der Zielgruppe ein geringeres Risiko, dass es bei Ein-/Austritten zu großen Spitzen kommt. Wenn die Zielgruppendefinition jedoch dazu führt, dass eine große Anzahl von Kundinnen und Kunden sich gleichzeitig qualifiziert, sind ebenfalls Spitzen möglich.

Vermeiden Sie die Verwendung von Öffnungs- und Sendeereignissen bei der Streaming-Segmentierung. Verwenden Sie stattdessen echte Nutzeraktivitätssignale wie Klicks, Käufe oder Beacon-Daten. Verwenden Sie für die Häufigkeits- oder Unterdrückungslogik eher Geschäftsregeln als Sendeereignisse. [Weitere Informationen](../audience/about-audiences.md)

Weitere Informationen zur Streaming-Segmentierung finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

### Vermeiden von Überlastungen {#overloads-speed-segment-qualification}

Die folgenden Best Practices helfen dabei, eine Überlastung der für Journeys genutzten Systeme zu verhindern (Datenquellen, benutzerdefinierte Aktionen, Kanalaktionsaktivitäten):

* Verwenden Sie die Batch-Zielgruppe nicht unmittelbar nach ihrer Erstellung in einer Aktivität vom Typ **[!UICONTROL Zielgruppen-Qualifizierung]**. Dadurch wird die erste Berechnungsspitze vermieden. Auf der Journey-Arbeitsfläche wird eine gelbe Warnung angezeigt, wenn Sie im Begriff sind, eine bislang noch nie berechnete Zielgruppe zu verwenden.

  ![Fehlermeldung, wenn Zielgruppe in Adobe Experience Platform nicht gefunden wurde](assets/segment-error.png)

* Legen Sie eine Begrenzungsregel für Datenquellen und Aktionen fest, die in Journeys verwendet werden, um eine Überlastung zu vermeiden. Weitere Informationen sind in der [Dokumentation zu Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=de){target="_blank"} verfügbar. Beachten Sie, dass die Begrenzungsregel nicht erneut versucht wird. Für einen erneuten Versuch müssen Sie einen alternativen Pfad in der Journey verwenden, indem Sie in den Bedingungen oder Aktionen das Kontrollkästchen **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** aktivieren.

* Bevor Sie die Zielgruppe in einer Produktions-Journey verwenden, sollten Sie die Anzahl der Kontakte auswerten, die sich für diese Zielgruppe täglich qualifizieren. Wählen Sie dazu das Menü **[!UICONTROL Zielgruppe]** aus, öffnen Sie die Zielgruppe und sehen Sie sich das Diagramm **[!UICONTROL Profile im Verlauf der Zeit]** an.

  ![Warnmeldung, wenn die Zielgruppe zu viele Ereignisse für die Echtzeitverarbeitung hat](assets/segment-overload.png)

Weitere Informationen zu Einstiegsbeschränkungen und zum Durchsatz finden Sie in [diesem Abschnitt](entry-management.md#profile-entrance-rate).

## Leitlinien und Einschränkungen {#audience-qualification-guardrails}

Die nachstehenden Schutzmechanismen und Empfehlungen müssen befolgt werden, um Journeys vom Typ „Zielgruppen-Qualifizierung“ zu erstellen. Siehe auch [Best Practices für die Zielgruppen-Qualifizierung](#best-practices-segments).


* Journeys vom Typ „Zielgruppen-Qualifizierung“ wurden in erster Linie für die Verwendung mit Streaming-Zielgruppen entwickelt. Diese Kombination garantiert ein besseres Echtzeit-Erlebnis. Es wird dringend empfohlen, **Streaming-Zielgruppen** in der Aktivität „Zielgruppen-Qualifizierung“ zu verwenden.

  Wenn Sie jedoch auf der Batch-Aufnahme basierende Attribute in Ihrer Streaming-Zielgruppe verwenden möchten oder eine Batch-Zielgruppe für eine Journey vom Typ „Zielgruppen-Qualifizierung“, müssen Sie die Zeitspanne für die Zielgruppen-Auswertung/-Aktivierung berücksichtigen. Eine Batch-Zielgruppe oder Streaming-Zielgruppe, die auf der Batch-Aufnahme basierende Attribute verwendet, ist ungefähr **2 Stunden** nach Abschluss des Segmentierungsauftrags für die Verwendung in der Aktivität **Zielgruppen-Qualifizierung** bereit. Dieser Auftrag wird einmal täglich zu der Zeit ausgeführt, die von der bzw. dem Adobe-Organisationsadmin definiert wurde.

* Adobe Experience Platform-Zielgruppen werden entweder einmal täglich (**Batch**-Zielgruppen) oder in Echtzeit (für **Streaming-Zielgruppen** mithilfe der Option „Hochfrequenz-Zielgruppen“ von Adobe Experience Platform) berechnet.

   * Wenn die ausgewählte Zielgruppe gestreamt wird, können die zu dieser Zielgruppe gehörenden Kontakte in Echtzeit in die Journey eintreten. 
   * Bei einer Batch-Zielgruppe treten die für diese Zielgruppe neu qualifizierten Kontakte in die Journey ein, sobald die Zielgruppenberechnung in Adobe Experience Platform ausgeführt wird.

  Als Best Practice wird empfohlen, Streaming-Zielgruppen für die Aktivität **Zielgruppen-Qualifizierung** zu verwenden. Für Batch-Anwendungsfälle verwenden Sie bitte die Aktivität **[Zielgruppe lesen](read-audience.md)**.

  >[!NOTE]
  >
  >Aufgrund der Batch-Beschaffenheit von Zielgruppen, die mithilfe von Kompositions-Workflows und benutzerdefinierten Uploads erstellt wurden, können diese Zielgruppen nicht in einer Aktivität „Zielgruppen-Qualifizierung“ ausgewählt werden. In dieser Aktivität können nur Zielgruppen genutzt werden, die mithilfe von Segmentdefinitionen erstellt wurden.


* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ **Zielgruppe lesen**, **Zielgruppen-Qualifizierung** oder **Geschäftsereignis** beginnen. 

* Bei Verwendung einer Aktivität **Zielgruppenqualifizierung** in einer Journey kann es bis zu 10 Minuten dauern, bis die Aktivität aktiv ist und die Profile überwacht, die in die Zielgruppe eintreten oder sie verlassen.


>[!CAUTION]
>
>[Leitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=de){target="_blank"} gelten auch für Adobe Journey Optimizer.



## Anleitungsvideo {#video}

Machen Sie sich mit den entsprechenden Anwendungsszenarien für Journeys vom Typ „Zielgruppenqualifizierung“ in diesem Video vertraut. Erfahren Sie, wie Sie eine Journey mit Zielgruppenqualifizierung erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/3446213?captions=ger&quality=12)
