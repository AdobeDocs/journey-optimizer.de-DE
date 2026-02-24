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
source-git-commit: be05bb72ace2e2084675f4278501a520d592e304
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 70%

---

# Zielgruppen-Qualifizierungsereignisse {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Zielgruppen-Qualifizierungsereignisse"
>abstract="Diese Aktivität überwacht die Ein- und Ausstiege von Profilen in [!DNL Adobe Experience Platform] Zielgruppen, um Personen durch eine Journey zu bewegen."

## Informationen zu Zielgruppen-Qualifizierungsereignissen{#about-segment-qualification}

Diese Aktivität überwacht den Ein- und Austritt von Profilen in [!DNL Adobe Experience Platform] Audiences. Sie kann Personen dazu bringen, eine Journey zu betreten oder fortzufahren. Weitere Informationen zum Erstellen von Zielgruppen finden Sie in diesem [Abschnitt](../audience/about-audiences.md).

Angenommen, Sie verfügen über eine Zielgruppe für „Silber-Kundschaft“. Mit dieser Aktivität können Sie dafür sorgen, dass alle neuen Silber-Kunden eine Journey beginnen, und ihnen eine Reihe personalisierter Nachrichten senden.

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

   ![Schaltfläche „Kopieren“ zum Kopieren von Zielgruppenname und -ID im JSON-Format](assets/segment-copy.png)

1. Wählen Sie im Feld **[!UICONTROL Verhalten]** aus, ob Zielgruppeneintritte, -ausstiege oder beides überwacht werden sollen.

   >[!NOTE]
   >
   >**[!UICONTROL Eintreten]** und **[!UICONTROL Verlassen]** entsprechen den **Realisiert** und **Ausgetreten** Zielgruppenteilnahmestatus aus [!DNL Adobe Experience Platform].
   >Siehe die [Dokumentation zum Segmentierungs-Service](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/tutorials/evaluate-a-segment#interpret-segment-results){target="_blank"}.

1. Wählen Sie einen Namespace aus. Dies ist nur erforderlich, wenn das Ereignis als erster Schritt der Journey positioniert wird. Standardmäßig ist das Feld mit dem zuletzt verwendeten Namespace vorausgefüllt.

   >[!NOTE]
   >
   >Sie können nur einen personenbasierten Identity-Namespace auswählen.
   >Namespaces von Lookup-Tabellen (z. B. ProductID für eine Produktsuche) sind in der Dropdown-Liste **Namespace** nicht verfügbar.

   ![Namespace-Auswahl für die Zielgruppen-Qualifizierungs-Identität](assets/segment7.png)

Die Payload enthält die folgenden Kontextinformationen, die Sie in Bedingungen und Aktionen verwenden können:

* Verhalten (Eintritt, Austritt)
* Zeitstempel der Qualifizierung
* Zielgruppen-ID

Wenn Sie den Ausdruckseditor in einer Bedingung oder Aktion verwenden, die einer Aktivität vom Typ **[!UICONTROL Zielgruppen-Qualifizierung]** folgt, können Sie auf den Knoten **[!UICONTROL AudienceQualification]** zugreifen. Sie können zwischen der **[!UICONTROL letzten Qualifizierungszeit]** und dem **[!UICONTROL Status]** (Einstieg oder Ausstieg) wählen.

Siehe [Bedingungsaktivität](../building-journeys/condition-activity.md#about_condition).

Eine neue Journey, die ein Ereignis **Zielgruppen-Qualifizierung** enthält, ist zehn Minuten nach der Veröffentlichung einsatzbereit. Dieses Intervall entspricht dem Cache-Aktualisierungsintervall des dedizierten Services. Warten Sie 10 Minuten, bevor Sie diese Journey verwenden.

## Best Practices {#best-practices-segments}

Die **[!UICONTROL Zielgruppen-]**) ermöglicht Personen, die sich für eine [!DNL Adobe Experience Platform] Zielgruppe qualifizieren oder deren Qualifizierung sie verweigern, den sofortigen Eintritt in die Journey.

Die Empfangsgeschwindigkeit dieser Daten ist hoch. Messungen zeigen, dass pro Sekunde 10.000 Ereignisse empfangen werden. Planen Sie Eintrittsspitzen, vermeiden Sie sie nach Möglichkeit, und bereiten Sie Ihren Journey darauf vor. Weitere Informationen zu Journey-Verarbeitungsraten und Durchsatzbeschränkungen finden Sie in [diesem Abschnitt](entry-management.md#journey-processing-rate).

### Batch-Zielgruppen {#batch-speed-segment-qualification}

Bei Verwendung der Zielgruppen-Qualifizierung für eine Batch-Zielgruppe tritt zum Zeitpunkt der täglichen Berechnung eine Eintrittsspitze auf. Die Größe der Spitze hängt davon ab, wie viele Personen die Zielgruppe jeden Tag betreten oder verlassen.

Wenn die Batch-Zielgruppe neu erstellt und sofort auf einer Journey verwendet wird, kann der erste Berechnungs-Batch viele Einträge erfordern. Planen Sie für diese Spitze.

### Timing der Aktualisierungen der Segmentzugehörigkeit {#timing-segment-membership}

Bei Verwendung von Batch-Momentaufnahmen auf einer Journey dürfen neue Segmentzugehörigkeiten nur in nachfolgenden Momentaufnahmen widergespiegelt werden. Wenn sofortige oder am selben Tag erfolgende Segmenthinzufügungen wichtig sind, sollten Sie die Streaming-Segmentierung in Betracht ziehen oder überprüfen, ob Segmentaktualisierungen vom nächsten Schnappschuss erfasst werden.

### Streaming-Zielgruppen {#streamed-speed-segment-qualification}

Bei Verwendung der Zielgruppen-Qualifizierung für gestreamte Zielgruppen besteht ein geringeres Risiko großer Ein- und Ausstiegsspitzen, da die Auswertung kontinuierlich erfolgt. Wenn die Zielgruppendefinition viele Kundinnen und Kunden gleichzeitig qualifiziert, kann es dennoch zu einer Spitze kommen.

Vermeiden Sie die Verwendung von Öffnungs- und Sendeereignissen bei der Streaming-Segmentierung. Verwenden Sie stattdessen echte Nutzeraktivitätssignale wie Klicks, Käufe oder Beacon-Daten. Verwenden Sie für die Häufigkeits- oder Unterdrückungslogik Geschäftsregeln anstelle von Ereignissen senden. [Weitere Informationen](../audience/about-audiences.md)

Siehe die [[!DNL Adobe Experience Platform] Dokumentation zur Streaming-](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

>[!NOTE]
>
>Bei der Streaming-Segmentierung kann es bis zu **2 Stunden dauern,** neu aufgenommene Daten innerhalb von [!DNL Adobe Experience Platform] vollständig für die Echtzeit-Nutzung übertragen werden. Zielgruppen, die auf tages- oder zeitbasierte Bedingungen angewiesen sind (z. B. „Ereignisse, die heute stattgefunden haben“), können zu zusätzlicher Komplexität bei der Qualifizierungszeitplanung führen. Wenn Ihr Journey von der sofortigen Zielgruppen-Qualifizierung abhängt, sollten Sie zu Beginn [ kurze Aktivität ](wait-activity.md)Warten“ hinzufügen. Um eine genaue Qualifizierung sicherzustellen, können Sie auch Pufferzeiten zulassen.

#### Darum treten möglicherweise nicht alle qualifizierten Profile in die Journey ein {#streaming-entry-caveats}

Bei Verwendung von Streaming-Zielgruppen mit der Aktivität **Zielgruppen-Qualifizierung** treten nicht unbedingt alle Profile, die für die Zielgruppe qualifiziert sind, in die Journey ein. Dieses Verhalten kann aus den folgenden Gründen auftreten:

* **Bereits in der Zielgruppe enthaltene Profile**: Nur Profile, die sich nach der Veröffentlichung der Journey neu für die Zielgruppe qualifizieren, lösen den Eintritt aus. Profile, die sich bereits vor der Veröffentlichung in der Zielgruppe befinden, treten nicht ein.

* **Journey-Aktivierungszeit**: Wenn Sie eine Journey veröffentlichen, dauert es bis zu **10 Minuten**, bis die Aktivität **Zielgruppen-Qualifizierung** aktiv wird und Profileintritte und -ausstiege überwacht. [Weitere Informationen zur Journey-Aktivierung](#configure-segment-qualification).

* **Schnelle Zielgruppenaustritte**: Wenn ein Profil sich für die Zielgruppe qualifiziert, aber aussteigt, bevor der Journey-Eintritt ausgelöst wird, tritt dieses Profil möglicherweise nicht in die Journey ein.

* **Timing zwischen Qualifizierung und Journey-Verarbeitung**: Aufgrund der verteilten Natur von [!DNL Adobe Experience Platform] kann es zu Zeitlücken kommen. Ein Profil kann sich qualifizieren, bevor die Journey das Qualifizierungsereignis verarbeitet.

**Empfehlungen:**

* Warten Sie nach dem Veröffentlichen einer Journey mindestens 10 Minuten, bevor Sie Ereignisse oder Daten senden, die die Profilqualifizierung auslösen. Dadurch wird sichergestellt, dass die Journey vollständig aktiviert ist und Eintritte verarbeitet werden können.

* Für kritische Anwendungsfälle, bei denen Sie sicherstellen müssen, dass alle qualifizierten Profile eintreten, sollten Sie stattdessen eine Aktivität [Zielgruppe lesen](read-audience.md) verwenden. Es verarbeitet alle Profile in einer Zielgruppe zu einem bestimmten Zeitpunkt.

* Überwachen Sie [die Eintrittsrate und den Durchsatz](entry-management.md#profile-entrance-rate) Ihrer Journey, um Muster im Profilfluss zu erkennen.

* Wenn Profile nicht erwartungsgemäß eintreten, finden Sie im [Leitfaden zur Fehlerbehebung](troubleshooting-execution.md#checking-if-people-enter-the-journey) weitere Diagnoseschritte.

### Vermeiden von Überlastungen {#overloads-speed-segment-qualification}

Die folgenden Best Practices helfen dabei, eine Überlastung der für Journeys genutzten Systeme zu verhindern (Datenquellen, benutzerdefinierte Aktionen, Kanalaktionsaktivitäten):

* Verwenden Sie die Batch-Zielgruppe nicht unmittelbar nach ihrer Erstellung in einer Aktivität vom Typ **[!UICONTROL Zielgruppen-Qualifizierung]**. Dadurch wird die erste Berechnungsspitze vermieden. Auf der Journey-Arbeitsfläche wird eine gelbe Warnung angezeigt, wenn Sie im Begriff sind, eine bislang noch nie berechnete Zielgruppe zu verwenden.

  ![Fehlermeldung, wenn Zielgruppe nicht in [!DNL Adobe Experience Platform]](assets/segment-error.png) gefunden wurde

* Legen Sie eine Begrenzungsregel für Datenquellen und Aktionen fest, die in Journeys verwendet werden, um eine Überlastung zu vermeiden. Weitere Informationen sind in der [Dokumentation zu Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=de){target="_blank"} verfügbar. Beachten Sie, dass die Begrenzungsregel nicht erneut versucht wird. Für einen erneuten Versuch müssen Sie einen alternativen Pfad in der Journey verwenden, indem Sie in den Bedingungen oder Aktionen das Kontrollkästchen **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** aktivieren.

* Bevor Sie die Zielgruppe in einer Produktions-Journey verwenden, sollten Sie die Anzahl der Kontakte auswerten, die sich für diese Zielgruppe täglich qualifizieren. Wählen Sie dazu das Menü **[!UICONTROL Zielgruppe]** aus, öffnen Sie die Zielgruppe und sehen Sie sich das Diagramm **[!UICONTROL Profile im Verlauf der Zeit]** an.

  ![Warnmeldung, wenn die Zielgruppe zu viele Ereignisse für die Echtzeitverarbeitung hat](assets/segment-overload.png)

Weitere Informationen zu Eintrittsratenbeschränkungen und zum Durchsatz finden Sie in [diesem Abschnitt](entry-management.md#profile-entrance-rate).

## Leitlinien und Einschränkungen {#audience-qualification-guardrails}

Die nachstehenden Schutzmechanismen und Empfehlungen müssen befolgt werden, um Journeys vom Typ „Zielgruppen-Qualifizierung“ zu erstellen. Siehe auch [Best Practices für die Zielgruppen-Qualifizierung](#best-practices-segments).


* Journeys vom Typ „Zielgruppen-Qualifizierung“ wurden in erster Linie für die Verwendung mit Streaming-Zielgruppen entwickelt. Diese Kombination garantiert ein besseres Echtzeit-Erlebnis. Es wird dringend empfohlen, **Streaming-Zielgruppen** in der Aktivität „Zielgruppen-Qualifizierung“ zu verwenden.

  Wenn Sie jedoch auf der Batch-Aufnahme basierende Attribute in Ihrer Streaming-Zielgruppe verwenden möchten oder eine Batch-Zielgruppe für eine Journey vom Typ „Zielgruppen-Qualifizierung“, müssen Sie die Zeitspanne für die Zielgruppen-Auswertung/-Aktivierung berücksichtigen. Eine Batch-Zielgruppe oder Streaming-Zielgruppe, die auf der Batch-Aufnahme basierende Attribute verwendet, ist ungefähr **2 Stunden** nach Abschluss des Segmentierungsauftrags für die Verwendung in der Aktivität **Zielgruppen-Qualifizierung** bereit. Dieser Auftrag wird einmal täglich zu der Zeit ausgeführt, die von der bzw. dem Adobe-Organisationsadmin definiert wurde.

* [!DNL Adobe Experience Platform] Zielgruppen werden entweder einmal täglich (**Batch**-Zielgruppen) oder in Echtzeit berechnet (für **Streaming**-Zielgruppen mithilfe der Option „Zielgruppen mit hoher Häufigkeit“ von [!DNL Adobe Experience Platform]).

   * Wenn die ausgewählte Zielgruppe gestreamt wird, können die zu dieser Zielgruppe gehörenden Kontakte in Echtzeit in die Journey eintreten. 
   * Wenn es sich bei der Zielgruppe um einen Batch-Vorgang handelt, geben Personen, die sich neu für diese Zielgruppe qualifiziert haben, möglicherweise die Journey ein, wenn die Zielgruppenberechnung auf [!DNL Adobe Experience Platform] ausgeführt wird.

  Als Best Practice wird empfohlen, Streaming-Zielgruppen für die Aktivität **Zielgruppen-Qualifizierung** zu verwenden. Für Batch-Anwendungsfälle verwenden Sie bitte die Aktivität **[Zielgruppe lesen](read-audience.md)**.

  >[!NOTE]
  >
  >Aufgrund der Batch-Beschaffenheit von Zielgruppen, die mithilfe von Kompositions-Workflows und benutzerdefinierten Uploads erstellt wurden, können diese Zielgruppen nicht in einer Aktivität „Zielgruppen-Qualifizierung“ ausgewählt werden. In dieser Aktivität können nur Zielgruppen genutzt werden, die mithilfe von Segmentdefinitionen erstellt wurden.


* Feldergruppen für Erlebnisereignisse können nicht in Journeys verwendet werden, die mit einer Aktivität vom Typ **Zielgruppe lesen**, **Zielgruppen-Qualifizierung** oder **Geschäftsereignis** beginnen. 

* Bei Verwendung einer Aktivität **Zielgruppenqualifizierung** in einer Journey kann es bis zu 10 Minuten dauern, bis die Aktivität aktiv ist und die Profile überwacht, die in die Zielgruppe eintreten oder sie verlassen.


>[!CAUTION]
>
>[Leitlinien für Echtzeit-Kundenprofildaten und Segmentierung](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=de){target="_blank"} gelten auch für [!DNL Adobe Journey Optimizer].



## Anleitungsvideo {#video}

Machen Sie sich mit den entsprechenden Anwendungsszenarien für Journeys vom Typ „Zielgruppenqualifizierung“ in diesem Video vertraut. Erfahren Sie, wie Sie eine Journey mit Zielgruppenqualifizierung erstellen und welche Best Practices anzuwenden sind.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
