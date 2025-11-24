---
solution: Journey Optimizer
product: journey optimizer
title: E-Mails nur an Wochentagen senden
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer eine Journey so konfigurieren, dass E-Mails nur an Wochentagen gesendet werden
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Anwendungsfall, Wochentage, Bedingung, E-Mail, Planung
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 9b3c9f7c0327c8c3c3d2b7f1b4255b7e1457a51e
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 0%

---

# E-Mails nur an Wochentagen senden {#send-emails-only-on-weekdays}

Dieser Anwendungsfall zeigt, wie Sie eine Journey in Adobe Journey Optimizer konfigurieren, die E-Mails nur an Werktagen (Montag bis Freitag) sendet. Bei Profilen, die an Wochenenden (Samstag oder Sonntag) auf die Journey zugreifen, werden E-Mails automatisch in die Warteschlange gestellt und am Montag zu einer bestimmten Zeit versendet. Dies gewährleistet eine optimale Interaktion durch den Versand von Nachrichten während der Arbeitswoche.

## Anwendungsfall - Übersicht

**Die Herausforderung**: Sicherstellen, dass E-Mails nur an Wochentagen gesendet werden, auch wenn Profile am Wochenende auf die Journey gelangen können. Für Wochenendeinträge sollten E-Mails am Montag zu einer bestimmten Zeit in die Warteschlange gestellt und gesendet werden.

**Die Lösung**: Verwenden Sie eine Aktivität vom Typ Bedingung , um den Wochentag zu identifizieren. Bei Wochenendeinträgen wird die E-Mail durch Warteaktivitäten mit benutzerdefinierten Formeln bis Montag verzögert. Wochentagseinträge gehen direkt zum Schritt E-Mail-Versand über.

Dieser Ansatz zeigt Ihnen, wie Sie mit einer Bedingungsaktivität überprüfen können, ob der aktuelle Tag Samstag oder Sonntag ist, Warteaktivitäten mit benutzerdefinierten Formeln für Wochenendeinträge implementieren, Wochenend-E-Mails für den Montag-Versand zu einer bestimmten Stunde in die Warteschlange stellen und E-Mails sofort für Wochentagseinträge senden (Montag bis Freitag).

Dieser Ansatz ist ideal für B2B-E-Mail-Kampagnen (Business-to-Business), professionelle Newsletter und Kommunikation, geschäftliche Ankündigungen, geschäftliche Produktaktualisierungen und jede Marketing-Kampagne, bei der die Bereitstellung am Wochenende nicht gewünscht ist.

>[!NOTE]
>
>Um diesen Anwendungsfall zu implementieren, benötigen Sie eine aktive Adobe Journey Optimizer-Instanz mit einer konfigurierten [E-Mail](../configuration/channel-surfaces.md)Kanaloberfläche[&#x200B; einer &#x200B;](../audience/about-audiences.md) oder einem [Ereignis](../event/about-events.md) zum Trigger der Journey sowie ein grundlegendes Verständnis von [Journey-Bedingungen](condition-activity.md) und [Ausdrücken](expression/expressionadvanced.md).


## Implementierungsschritte

### Schritt 1: Journey erstellen

1. Navigieren Sie zu **[!UICONTROL Journey-Verwaltung]** > **[!UICONTROL Journey]** in Adobe Journey Optimizer.

1. Klicken Sie **[!UICONTROL Journey erstellen]**, um [eine neue Journey zu erstellen](journey-gs.md).

1. Konfigurieren Sie die [Journey-Eigenschaften](journey-properties.md).

1. Journey-Einstiegspunkt auswählen:
   * **[Zielgruppe lesen](read-audience.md)**: Für Batch-Kampagnen, die auf eine bestimmte Zielgruppe abzielen
   * **[Ereignis](../event/about-events.md)**: Für Journey, die in Echtzeit ausgelöst werden und auf dem Kundenverhalten basieren

### Schritt 2: Fügen Sie die Aktivität Bedingung hinzu, um den Wochentag zu überprüfen

Fügen Sie direkt nach dem Start des Journey eine **[!UICONTROL Bedingung]**-Aktivität hinzu, um zu überprüfen, ob der aktuelle Tag Samstag oder Sonntag ist. Dadurch wird der Workflow entsprechend verzweigt.

1. Ziehen Sie eine Aktivität [**[!UICONTROL Bedingung &#x200B;]**&#x200B;auf &#x200B;](condition-activity.md) Arbeitsfläche nach Ihrem Einstiegspunkt.

1. Klicken Sie auf die **[!UICONTROL Bedingung]**-Aktivität, um das Konfigurationsfenster zu öffnen.

1. Wählen Sie **[!UICONTROL Bedingung]** als Bedingungstyp aus.

1. Wählen Sie **[!UICONTROL Wochentag]** als Zeitfilteroption aus.

1. Wählen Sie für **ersten Pfad (Samstag)** nur **Samstag** aus. Beschriften Sie diesen Pfad mit „Samstag“.

1. Klicken Sie **[!UICONTROL Pfad hinzufügen]**, um eine zweite Bedingung zu erstellen.

1. Wählen Sie für **zweiten Pfad (Sonntag)** die Option **[!UICONTROL Wochentag]** und wählen Sie **Sonntag** aus. Beschriften Sie diesen Pfad mit „Sonntag“.

   ![Konfigurieren der Samstag- und Sonntagsbedingungen im Ausdruckseditor](assets/weekday-email-uc-condition-expression.png)


1. Aktivieren Sie **[!UICONTROL Pfad für andere Fälle als die obigen anzeigen]**, um einen Pfad für Wochentagseinträge (Montag bis Freitag) zu erstellen.

>[!NOTE]
>
>Die Zeitzone, die für die Auswertung des Wochentags verwendet wird, wird auf Journey-Ebene in den Journey-Eigenschaften definiert, nicht auf Bedingungsebene. Die in [&#x200B; Formel verwendete Journey &#x200B;](timezone-management.md)Zeitzone) ist die konfigurierte Zeitzone der Journey, nicht die der Empfängerin oder des Empfängers.

### Schritt 3: Warteaktivitäten für Wochenendeinträge konfigurieren

Verwenden Sie für Profile, die am Samstag oder Sonntag eingehen **[!UICONTROL Aktivitäten vom Typ „Warten]** mit benutzerdefinierten Formeln, um die E-Mail bis Montag zur gewünschten Stunde zu verschieben.

Verwenden Sie in **[!UICONTROL Aktivität]** Warten“ die folgende Formel:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Dabei gilt:

* **X** ist die Anzahl der Tage bis zum Warten:
   * Verwenden Sie **2** für Samstag (warten Sie bis Montag)
   * Verwenden Sie **1** für Sonntag (warten Sie bis Montag)
* **H** ist die Stunde, die Sie senden möchten (z. B. **9** für 9 Uhr)


**Beispiel für Samstag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Beispiel für Sonntag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

So implementieren Sie dies auf Ihrem Journey:

1. Fügen Sie im **Samstagspfad** eine Aktivität **[!UICONTROL Warten]** nach der Bedingung hinzu.

1. Wählen **[!UICONTROL als Wartetyp]** Dauer“ aus.

1. Klicken Sie **[!UICONTROL Erweiterter Modus]**, um die benutzerdefinierte Formel einzugeben.

1. Eingeben: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Journey mit drei Bedingungspfaden - Samstag, Sonntag und Wochentag](assets/weekday-email-uc-paths.png)

1. Wiederholen Sie die gleichen Schritte für den **Sonntagspfad** mit: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Für komplexere Geschäftszeiten (z. B. nur zwischen 9 und 17 Uhr an Wochentagen) können Sie die Formel und die Bedingungen weiter verbessern.

### Schritt 4: Wochentagsverzweigung

Für Profile, die Montag bis Freitag eintreten, fahren Sie mit dem Schritt E-Mail senden wie gewohnt fort.

1. Fügen Sie im **Wochentagspfad** (dem Pfad „Andere Fälle„) direkt die Aktionsaktivität **[!UICONTROL E-Mail]** hinzu. Für **[!UICONTROL -]** ist keine Warteaktivität erforderlich.

1. Konfigurieren Sie Ihre E-Mail-Nachricht nach Bedarf.

### Schritt 5: Journey-Fluss abschließen

Nach den **[!UICONTROL Warten]**-Aktivitäten sowohl für den Samstag- als auch für den Sonntagspfad sollten alle drei Pfade (Samstag, Sonntag und Wochentag) zur gleichen **[!UICONTROL E-Mail]**-Aktionsaktivität führen. Fügen Sie nach **[!UICONTROL E-Mail]** Aktivität „Ende“ hinzu.

### Visuelle Workflow-Übersicht

Der vollständige Journey-Workflow folgt dieser Logik:

* **Start** → **[!UICONTROL Bedingung]**: Ist es Samstag oder Sonntag?
   * **Ja (Samstag):** **[!UICONTROL Warten]** bis Montag 9 → **[!UICONTROL E-Mail senden]**
   * **Ja (Sonntag):** **[!UICONTROL Warten]** bis Montag 9 → **[!UICONTROL E-Mail senden]**
   * **Nein (Montag-Freitag):** **[!UICONTROL E-Mail]**

Dadurch wird sichergestellt, dass alle E-Mails nur an Wochentagen gesendet werden und die Wochenendeinträge automatisch für den Versand am Montag in die Warteschlange gestellt werden.

### Schritt 6: Journey testen

Testen Sie vor der Veröffentlichung Ihre Journey-Logik gründlich im Testmodus von Adobe Journey Optimizer, um zu bestätigen, dass alles erwartungsgemäß funktioniert:

1. Klicken Sie auf **[!UICONTROL Test]**-Schaltfläche oben rechts.

1. Aktivieren [Testmodus](testing-the-journey.md).

1. Erstellen [Testprofile](../audience/creating-test-profiles.md) mit simulierten Eingabezeiten an verschiedenen Wochentagen:
   * **Samstagseingabe**: Überprüfen Sie, ob das Profil dem Samstagspfad folgt, am Montag zur angegebenen Stunde wartet und E-Mails erhält
   * **Sonntagseintrag**: Überprüfen Sie, ob das Profil dem Sonntagspfad folgt, am Montag zur angegebenen Stunde wartet und E-Mails erhält
   * **Montag-Freitag-Einträge**: Überprüfen Sie, ob E-Mails sofort und ohne Wartezeit gesendet werden

1. Überprüfen Sie die Journey-Visualisierung, um sicherzustellen, dass die Profile den richtigen bedingten Pfaden folgen (Samstag, Sonntag oder Wochentag).

1. Prüfen Sie die Journey auf [Fehler oder &#x200B;](troubleshooting.md)).

1. Überprüfen Sie, ob die Warteformeln die richtige Dauer für Ihre gewünschte Montag-Lieferzeit berechnen.

>[!IMPORTANT]
>
>Testen Sie Ihre Journey-Logik immer im Testmodus, um sicherzustellen, dass sich die Warteaktivitäten wie erwartet verhalten. Verwenden Sie den Testmodus, um verschiedene Eintrittsszenarien zu simulieren und zu überprüfen, ob die Wochenendeinträge korrekt in die Warteschlange der Montagsbereitstellung gestellt werden. Weitere Informationen finden Sie unter Best Practices für das {[}Journey von Tests.](testing-the-journey.md)

### Schritt 7: Veröffentlichen des Journey

Sobald der Test abgeschlossen ist:

1. Klicken **[!UICONTROL oben]** auf „Veröffentlichen“.

1. Bestätigen Sie die [Veröffentlichung](publish-journey.md).

1. Überwachen Sie die Journey-Leistung mithilfe von [Journey](report-journey.md)Berichten und [Live-Berichten](../reports/journey-live-report.md).


## Verwandte Themen

* [Bedingungsaktivitäten](condition-activity.md) - Erfahren Sie, wie Sie verschiedene Pfade in Ihrem Journey erstellen.
* [Bedingungen auf einer Journey verwenden](conditions.md) - Detaillierte Anleitung zu Journey-Bedingungen
* [Warteaktivität](wait-activity.md) - Konfigurieren der Wartezeiten und Formeln
* [Datumsfunktionen](functions/date-functions.md) - Vollständige Referenz für Datums- und Uhrzeitfunktionen
* [Ausdruckseditor](expression/expressionadvanced.md) - Erstellen komplexer Ausdrücke
* [Best Practices für das Journey](journey-gs.md#best-practices) - Empfohlene Ansätze für das Journey-Design
