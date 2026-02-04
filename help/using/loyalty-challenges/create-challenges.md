---
solution: Journey Optimizer
product: journey optimizer
title: Herausforderungen bei der Treue schaffen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Herausforderungen im Zusammenhang mit Treueprogrammen erstellen und konfigurieren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: 5120eb51311348b8561b0a20f982576f6c945921
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 2%

---


# Herausforderungen schaffen {#create-challenges}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* **Herausforderungen erstellen** ◀︎ **Sie sind hier** - Herausforderungen erstellen und konfigurieren
* [Aufgaben erstellen](create-tasks.md) - Herausforderungen definieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Funktionsweise {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

Dieser Workflow ermöglicht das Erstellen und Starten einer Herausforderung zum Treueprogramm:

1. **Herausforderung erstellen** - Definiert die grundlegenden Eigenschaften der Herausforderung, einschließlich Name, Typ (Standard, Streak oder Sequenziell), Zielgruppe und Datumsbereich.

1. **Aufgaben hinzufügen** - Definiert die spezifischen Aktionen, die Kunden durchführen müssen, einschließlich Aufgabentypen (Kauf, Ausgaben, Besuch usw.), Mengen, Produktfiltern und Belohnungen.

1. **Erstellen von Inhaltskarten** - Erstellen Sie die visuelle Darstellung Ihrer Challenge mit Journey Optimizer-Inhaltskarten, die auf Kundengeräten angezeigt werden.

1. **Messaging konfigurieren** (Optional) - Richten Sie Multi-Channel-Nachrichten (In-App, E-Mail, Push, SMS) für die wichtigsten Phasen ein: Start, in Bearbeitung und Abschluss.

1. **Überprüfen und**: Testen Sie Ihre Herausforderung mit Testprofilen und veröffentlichen Sie sie dann, um sie Ihrer Zielgruppe verfügbar zu machen.

## Herausforderung erstellen {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

So erstellen Sie eine neue Herausforderung für das Treueprogramm:

1. Navigieren Sie zu **[!UICONTROL Herausforderungen]** Treue“ in Journey Optimizer.

1. Wählen Sie die **[!UICONTROL Herausforderungen]** aus.

1. Wählen Sie **[!UICONTROL Herausforderung erstellen]** aus.

1. Konfigurieren Sie die Challenge-Eigenschaften:

   **Challenge-Name**: Geben Sie einen beschreibenden Namen für Ihre Challenge ein. Dieser Name wird im Challenges-Inventar angezeigt und hilft Ihnen, die Challenge zu identifizieren.

   **Challenge type**: Wählen Sie einen der folgenden Typen:
   * **[!UICONTROL Standard]**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
   * **[!UICONTROL Streak]**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
   * **[!UICONTROL Sequenziell]**: Kunden führen Aufgaben in einer definierten Reihenfolge aus

   **Zielgruppe**: Wählen Sie das Zielgruppensegment aus, das definiert, wer an dieser Herausforderung teilnehmen kann. Sie müssen Zielgruppen in Experience Platform erstellen, bevor Sie Herausforderungen erstellen können. Weitere Informationen finden Sie unter [Erste Schritte mit Audiences](../audience/about-audiences.md).

   **Startdatum**: Legen Sie fest, wann die Challenge für Kundinnen und Kunden verfügbar sein soll.

   **Enddatum**: Legt fest, wann die Challenge abläuft und keine neuen Abschlüsse mehr akzeptiert.

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### Aufgaben hinzufügen {#add-tasks}

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um Prämien zu erhalten. Sie konfigurieren Aufgabentypen (Kauf, Ausgaben, Besuch, Interaktion, benutzerdefinierte Ereignisse), Mengen, Produktfilter und Belohnungen.

Je nach Challenge-Typ führen Kundinnen und Kunden Aufgaben unterschiedlich aus:

* **Standardherausforderungen**: Führen Sie eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
* **Streak Challenges**: Dieselbe Aufgabe mehrmals hintereinander ausführen
* **Sequenzielle Herausforderungen**: Aufgaben in einer definierten Reihenfolge erledigen

Um Aufgaben zu Ihrer Herausforderung hinzuzufügen, wählen Sie **[!UICONTROL Aufgabe hinzufügen]** im Abschnitt Aufgaben aus und konfigurieren Sie die Eigenschaften der Aufgabe.

Detaillierte Anweisungen zum Erstellen und Konfigurieren von Aufgaben finden Sie unter [Aufgaben erstellen](create-tasks.md).

### Konfigurieren von Inhaltskarten {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

Inhaltskarten bieten eine visuelle Darstellung Ihrer Challenge auf Kundengeräten und zeigen Challenge-Informationen, Fortschritt und Belohnungen an. Weitere Informationen zu [Inhaltskarten](../content-card/create-content-card.md).

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

So konfigurieren Sie Inhaltskarten für Ihre Challenge:

1. Navigieren Sie im Challenge-Editor zum Abschnitt **[!UICONTROL Inhaltskarten]** .

1. Wählen Sie **[!UICONTROL Inhaltskarte erstellen]** oder eine vorhandene Vorlage aus.

1. Gestalten der Inhaltskarte:
   * Bilder, Text und Branding-Elemente hinzufügen
   * Personalisierungs[Token &#x200B;](../personalization/personalization-syntax.md) Anzeige kundenspezifischer Informationen einschließen
   * Challenge-Fortschrittsindikatoren anzeigen
   * Belohnungen und Anreize anzeigen

1. Konfigurieren Sie, wann die Inhaltskarte angezeigt wird:
   * **Challenge start**: Zeigt an, wann die Challenge verfügbar wird
   * **In Bearbeitung**: Wird angezeigt, während Kunden aktiv teilnehmen
   * **Fertigstellung**: Anzeigen, nachdem Kunden alle Aufgaben abgeschlossen haben

1. Zeigen Sie eine Vorschau der Inhaltskarte auf verschiedenen Geräten an, um eine ordnungsgemäße Anzeige sicherzustellen.

1. Speichern Sie die Konfiguration der Inhaltskarte.

Weitere Informationen zum Entwerfen und Personalisieren von Inhaltskarten finden Sie unter [Entwerfen von Inhaltskarten](../content-card/design-content-card.md).

### Konfigurieren von Messaging {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

Richten Sie Multi-Channel-Nachrichten ein, um Kunden in wichtigen Phasen des Challenge-Lebenszyklus anzusprechen.

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

So konfigurieren Sie Messaging für Ihre Challenge:

1. Navigieren Sie im Challenge-Editor zum Abschnitt **[!UICONTROL Messaging]** .

1. Konfigurieren Sie Nachrichten für jede Lebenszyklusphase:

   **Launch-Nachrichten** - Benachrichtigen Sie Kunden, wenn die Challenge beginnt:
   * Kanäle auswählen: [In-App](../in-app/get-started-in-app.md), [E-Mail](../email/get-started-email.md), [Push-Benachrichtigung](../push/get-started-push.md) oder [SMS](../sms/get-started-sms.md)
   * Gestalten der Nachricht mit Challenge-Details und call-to-action
   * Zeitvorgabe festlegen: Sofort senden, wenn die Herausforderung für einen bestimmten Zeitpunkt live geht oder geplant wird

   **Nachrichten in Bearbeitung** - Halten Sie Kunden während der Challenge bei der Stange:
   * Bedingungen für den Trigger definieren (z. B. 50 % Abschluss, spezifische Aufgabe abgeschlossen)
   * Erinnerungsnachrichten erstellen, um die weitere Teilnahme zu fördern
   * Schließen Sie Fortschrittsaktualisierungen und die nächsten Schritte ein

   **Abschlussnachrichten** - Feiern Sie Erfolg und übersenden Sie Belohnungen:
   * Kunden zum Abschluss der Herausforderung gratulieren
   * Belohnungsverteilung bestätigen
   * Anweisungen zum Anfordern von Prämien bereitstellen
   * Vorschläge für nächste Herausforderungen oder Maßnahmen

Weitere Informationen zum Erstellen von Nachrichten für bestimmte Kanäle finden Sie unter:

* [Dokumentation zu In-App-Nachrichten](../in-app/get-started-in-app.md)
* [Dokumentation zu E-Mail-Nachrichten](../email/get-started-email.md)
* [Dokumentation zu Push-Benachrichtigungen](../push/get-started-push.md)
* [Dokumentation zu SMS-Nachrichten](../sms/get-started-sms.md)

## Challenge überprüfen und veröffentlichen {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

Vor der Veröffentlichung der Herausforderung:

1. **Alle Komponenten überprüfen** Überprüfen Sie Eigenschaften, Aufgaben, Belohnungen, Inhaltskarten und Messaging-Konfigurationen von Herausforderungen.

1. **Erlebnis testen**: Verwenden Sie [Testprofile](../content-management/test-profiles.md) um die Anzeige der Inhaltskarte und das Verhalten des Task-Triggers zu überprüfen.

1. **Veröffentlichen**: Wählen Sie **[!UICONTROL Veröffentlichen]** aus, um die Herausforderung für Ihre Zielgruppe verfügbar zu machen.

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

Wenn Sie eine Challenge veröffentlichen, erstellt Journey Optimizer automatisch eine [Journey](../building-journeys/journey-gs.md) im Entwurfsstatus. Die automatisch generierte Journey wird in Ihrem Journey-Inventar mit dem Namensformat „Challenge: [Challenge Name]&quot; angezeigt.

So stellen Sie die Herausforderung für Kunden bereit:

1. Navigieren Sie zum **[!UICONTROL Journey]**-Inventar in Journey Optimizer.

1. Suchen Sie die automatisch generierte Journey (sie hat „Challenge:“ als Präfix im Namen).

1. [Journey aktivieren](../building-journeys/publish-journey.md).

Die Journey startet automatisch am angegebenen Startdatum der Challenge.

>[!NOTE]
>
>Die automatisch generierte Journey wird in Ihrem Journey-Inventar angezeigt und kann bei Bedarf angepasst werden. Direkt am Journey vorgenommene Änderungen werden jedoch nicht mit der Challenge-Konfiguration synchronisiert.

## Nächste Schritte {#next-steps}

* [Herausforderungen verwalten](manage-challenges.md) - Erfahren Sie, wie Sie Herausforderungen bearbeiten, überwachen und optimieren können.
* [Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Funktionen und Möglichkeiten überprüfen

