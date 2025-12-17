---
solution: Journey Optimizer
product: journey optimizer
title: Senden von E-Mails nur an Werktagen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer eine Journey so konfigurieren, dass E-Mails nur an Werktagen gesendet werden
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: Journey, Anwendungsfall, Werktage, Bedingung, E-Mail, Planung
version: Journey Orchestration
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: ht
source-wordcount: '1070'
ht-degree: 100%

---

# Senden von E-Mails nur an Werktagen {#send-emails-only-on-weekdays}

Dieser Anwendungsfall zeigt, wie Sie in Adobe Journey Optimizer eine Journey konfigurieren, die E-Mails nur an Werktagen (Montag bis Freitag) sendet. Bei Profilen, die an Wochenenden (Samstag oder Sonntag) in die Journey eintreten, werden E-Mails automatisch in die Warteschlange gestellt und am Montag zu einer festgelegten Zeit versendet. Dies gewährleistet optimale Interaktion, da Nachrichten während der Arbeitswoche versendet werden.

## Anwendungsfälle – Überblick

**Die Herausforderung**: Sicherstellen, dass E-Mails nur an Werktagen gesendet werden, auch wenn Profile am Wochenende in die Journey eintreten. Für Eintritte am Wochenende sollten E-Mails in die Warteschlange gestellt und am Montag zu einer festgelegten Zeit gesendet werden.

**Die Lösung**: Verwenden Sie eine Bedingungsaktivität, um den Wochentag zu identifizieren. Bei Eintritten am Wochenende wird die E-Mail durch Warteaktivitäten mit benutzerdefinierten Formeln bis Montag verzögert. Eintritte an Werktagen gehen direkt zum Schritt für den E-Mail-Versand über.

Dieser Ansatz zeigt, wie Sie mit einer Bedingungsaktivität überprüfen, ob der aktuelle Tag ein Samstag oder Sonntag ist, Warteaktivitäten mit benutzerdefinierten Formeln für Eintritte am Wochenende implementieren, Wochenend-E-Mails zum Versand am Montag zu einer bestimmten Uhrzeit in die Warteschlange stellen und E-Mails für Eintritte an Werktagen (Montag bis Freitag) sofort senden.

Dies ist ideal für B2B-E-Mail-Kampagnen (Business-to-Business), professionelle Newsletter und Kommunikation, geschäftliche Ankündigungen, arbeitsbezogene Produktaktualisierungen und alle Marketing-Kampagnen, bei denen ein Versand am Wochenende nicht gewünscht ist.

>[!NOTE]
>
>Um diesen Anwendungsfall zu implementieren, benötigen Sie eine aktive Adobe Journey Optimizer-Instanz mit einer konfigurierten [E-Mail-Kanaloberfläche](../configuration/channel-surfaces.md), einer [Zielgruppe](../audience/about-audiences.md) oder einem [Ereignis](../event/about-events.md) zum Auslösen der Journey sowie ein grundlegendes Verständnis von [Journey-Bedingungen](condition-activity.md) und [Ausdrücken](expression/expressionadvanced.md).


## Implementierungsschritte

### Schritt 1: Erstellen der Journey

1. Navigieren Sie in Adobe Journey Optimizer zu **[!UICONTROL Journey-Management]** > **[!UICONTROL Journeys]**.

1. Klicken Sie auf **[!UICONTROL Journey erstellen]**, um [eine neue Journey zu erstellen](journey-gs.md).

1. Konfigurieren Sie die [Journey-Eigenschaften](journey-properties.md).

1. Wählen Sie den Journey-Eintrittspunkt aus:
   * **[Zielgruppe lesen](read-audience.md)**: Für Batch-Kampagnen, die eine bestimmte Zielgruppe ansprechen
   * **[Ereignis](../event/about-events.md)**: Für Journeys, die in Echtzeit basierend auf dem Kundenverhalten ausgelöst werden

### Schritt 2: Hinzufügen einer Bedingungsaktivität zum Prüfen des Wochentags

Fügen Sie direkt nach dem Start der Journey eine Aktivität des Typs **[!UICONTROL Bedingung]** hinzu, um zu prüfen, ob der aktuelle Tag ein Samstag oder Sonntag ist. Dadurch wird der Workflow entsprechend verzweigt.

1. Ziehen Sie eine Aktivität des Typs [**[!UICONTROL Bedingung ]**](condition-activity.md) nach dem Eintrittspunkt auf die Arbeitsfläche.

1. Klicken Sie auf die Aktivität des Typs **[!UICONTROL Bedingung]**, um das zugehörige Konfigurations-Panel zu öffnen.

1. Wählen Sie **[!UICONTROL Zeitbedingung]** als Bedingungstyp aus.

1. Wählen Sie **[!UICONTROL Wochentag]** als Zeitfilteroption aus.

1. Wählen Sie als **ersten Pfad (Samstag)** nur **Samstag** aus. Beschriften Sie diesen Pfad mit „Samstag“.

1. Klicken Sie auf **[!UICONTROL Pfad hinzufügen]**, um eine zweite Bedingung zu erstellen.

1. Wählen Sie als **zweiten Pfad (Sonntag)** die Option **[!UICONTROL Wochentag]** aus und wählen Sie nur **Sonntag**. Beschriften Sie diesen Pfad mit „Sonntag“.

   ![Konfigurieren der Bedingungen für Samstag und Sonntag im Ausdruckseditor](assets/weekday-email-uc-condition-expression.png)


1. Aktivieren Sie **[!UICONTROL Pfad für andere Fälle als die obigen anzeigen]**, um einen Pfad für Eintritte an Werktagen (Montag bis Freitag) zu erstellen.

>[!NOTE]
>
>Die Zeitzone, die für die Auswertung des Wochentags verwendet wird, wird auf Journey-Ebene in den Journey-Eigenschaften definiert, nicht auf Bedingungsebene. Die in der Formel verwendete [Zeitzone](timezone-management.md) der Journey ist die konfigurierte Zeitzone der Journey, nicht die der Empfängerin oder des Empfängers.

### Schritt 3: Konfigurieren von Warteaktivitäten für Eintritte am Wochenende

Verwenden Sie für Profile, die am Samstag oder Sonntag eintreten, Aktivitäten des Typs **[!UICONTROL Warten]** mit benutzerdefinierten Formeln, um die E-Mail bis zur gewünschten Uhrzeit am Montag zu verschieben.

Verwenden Sie in der Aktivität **[!UICONTROL Warten]** die folgende Formel:

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Dabei gilt:

* **X** ist die Anzahl der Tage, die gewartet werden soll:
   * Verwenden Sie **2** für Samstag (bis Montag warten)
   * Verwenden Sie **1** für Sonntag (bis Montag warten)
* **H** ist die Uhrzeit, zu der Sie senden möchten (z. B. **9** für 9 Uhr)


**Beispiel für Samstag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Beispiel für Sonntag:**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Implementierung in der Journey:

1. Fügen Sie im Pfad **Samstag** nach der Bedingung eine Aktivität **[!UICONTROL Warten]** hinzu.

1. Wählen Sie **[!UICONTROL Dauer]** als Wartetyp aus.

1. Klicken Sie auf **[!UICONTROL Erweiterter Modus]**, um die benutzerdefinierte Formel einzugeben.

1. Geben Sie Folgendes ein: `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Journey mit drei Bedingungspfaden: Samstag, Sonntag und Werktag](assets/weekday-email-uc-paths.png)

1. Wiederholen Sie dieselben Schritte für den Pfad **Sonntag** wie folgt: `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Für komplexere Geschäftszeiten (z. B. nur zwischen 9 und 17 Uhr an Werktagen) können Sie die Formel und die Bedingungen zusätzlich erweitern.

### Schritt 4: Werktagsverzweigung

Für Profile, die von Montag bis Freitag eintreten, fahren Sie wie gewohnt mit dem Schritt zum E-Mail-Versand fort.

1. Fügen Sie im Pfad **Werktag** (dem Pfad „Andere Fälle“) direkt eine Aktionsaktivität **[!UICONTROL E-Mail]** hinzu. Für Eintritte an Werktagen ist keine Aktivität **[!UICONTROL Warten]** erforderlich.

1. Konfigurieren Sie Ihre E-Mail-Nachricht wie benötigt.

### Schritt 5: Abschließen des Journey Flows

Nach den Aktivitäten **[!UICONTROL Warten]** für die Pfade „Samstag“ und „Sonntag“ sollten alle drei Pfade (Samstag, Sonntag und Werktag) zur selben Aktivität für die Aktion **[!UICONTROL E-Mail]** fließen. Fügen Sie nach der E-Mail eine Aktivität **[!UICONTROL Ende]** hinzu.

### Visuelle Workflow-Übersicht

Der vollständige Journey-Workflow folgt dieser Logik:

* **Start** → **[!UICONTROL Bedingung]**: Ist heute Samstag oder Sonntag?
   * **Ja (Samstag):** **[!UICONTROL Warten]** bis Montag 9 Uhr → **[!UICONTROL E-Mail senden]**
   * **Ja (Sonntag):** **[!UICONTROL Warten]** bis Montag 9 Uhr → **[!UICONTROL E-Mail senden]**
   * **Nein (Montag–Freitag):** Sofort **[!UICONTROL E-Mail senden]**

Dadurch wird sichergestellt, dass alle E-Mails nur an Werktagen gesendet werden und die Eintritte an Wochenenden automatisch für den Versand am Montag in die Warteschlange gestellt werden.

### Schritt 6: Testen der Journey

Testen Sie vor der Veröffentlichung Ihre Journey-Logik gründlich im Testmodus von Adobe Journey Optimizer, um sich zu vergewissern, dass alles wie erwartet funktioniert:

1. Klicken Sie hierfür oben rechts auf die Schaltfläche **[!UICONTROL Testen]**.

1. Aktivieren Sie den [Testmodus](testing-the-journey.md).

1. Erstellen Sie [Testprofile](../audience/creating-test-profiles.md) mit simulierten Eintrittszeiten an verschiedenen Wochentagen:
   * **Eintritt am Samstag**: Prüfen Sie, ob das Profil dem Pfad „Samstag“ folgt, wartet und am Montag zur angegebenen Uhrzeit E-Mails erhält
   * **Eintritt am Sonntag**: Prüfen Sie, ob das Profil dem Pfad „Sonntag“ folgt, wartet und am Montag zur angegebenen Uhrzeit E-Mails erhält
   * **Eintritte Montag–Freitag**: Prüfen Sie, ob E-Mails sofort und ohne Wartezeit gesendet werden

1. Prüfen Sie die Journey-Visualisierung, um sicherzustellen, dass die Profile den richtigen Bedingungspfaden folgen (Samstag, Sonntag oder Werktag).

1. Prüfen Sie auf [Fehler oder Warnungen](troubleshooting.md) in der Journey.

1. Prüfen Sie, ob die Warteformeln die richtige Dauer für die gewünschte Versandzeit am Montag berechnen.

>[!IMPORTANT]
>
>Testen Sie Ihre Journey-Logik immer im Testmodus, um sicherzustellen, dass sich die Warteaktivitäten wie erwartet verhalten. Verwenden Sie den Testmodus, um verschiedene Eintrittsszenarien zu simulieren und zu prüfen, ob die Eintritte an Wochenenden korrekt in die Warteschlange zum Versand am Montag gestellt werden. Weitere Informationen finden Sie unter [Best Practices für Journeys](testing-the-journey.md).

### Schritt 7: Veröffentlichen der Journey

Nach Abschluss der Tests:

1. Klicken Sie rechts oben auf **[!UICONTROL Veröffentlichen]**.

1. Bestätigen Sie die [Veröffentlichung](publish-journey.md).

1. Überwachen Sie die Journey-Leistung mithilfe von [Journey-Berichten](report-journey.md) und [Live-Berichten](../reports/journey-live-report.md).


## Verwandte Themen

* [Bedingungsaktivitäten](condition-activity.md): Erfahren Sie, wie Sie verschiedene Pfade in Ihrer Journey erstellen.
* [Verwenden von Bedingungen in einer Journey](conditions.md): Detaillierte Anleitung zu Journey-Bedingungen
* [Aktivität „Warten“](wait-activity.md): Konfigurieren der Wartezeiten und Formeln
* [Datumsfunktionen](functions/date-functions.md): Vollständige Referenz für Datums- und Uhrzeitfunktionen
* [Ausdruckseditor](expression/expressionadvanced.md): Erstellen komplexer Ausdrücke
* [Best Practices für Journeys](journey-gs.md#best-practices): Empfohlene Ansätze für das Journey-Design
