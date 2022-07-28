---
title: Migrieren zur Inline-Erstellung von Journeys
description: Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 96%

---


# Übersicht über die Migration zur Inline-Erstellung{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="Erfahren Sie mehr über die neue Funktion zur Inline-Erstellung"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt aus einer Journey erstellt. Vorhandene Nachrichten werden automatisch in das neue Modell migriert. Nach der Migration sind zusätzliche Aktionen erforderlich, wenn Sie aktuell Nachrichten in Ihren Journeys verwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html?lang=de" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="Erfahren Sie, was passiert"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt aus einer Journey erstellt. Ihre Umgebung wird migriert. Nach der Migration sind zusätzliche Aktionen erforderlich, wenn Sie aktuell Nachrichten in Ihren Journeys verwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt aus einer Journey erstellt. Vorhandene Nachrichten wurden nun in das neue Modell migriert. Wenn Sie Journey verwenden, sind jetzt zusätzliche Aktionen für Journeys erforderlich, die Nachrichten verwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können"
>abstract="Ab dem 25. Juli 2022 wird das Menü „Nachrichten“ nicht mehr angezeigt und Nachrichten werden direkt aus einer Journey erstellt. Wenn Sie Ihre alten Nachrichten in Journeys wiederverwenden möchten, müssen Sie sie als Vorlagen speichern."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html?lang=de#save-as-template" text="Speichern von Nachrichten als Vorlagen"

Adobe Journey Optimizer bietet eine neue Funktion zur Optimierung der Art und Weise, wie Sie Inhalte für Journey Optimizer-Kanäle (E-Mail, Push und SMS) erstellen können. Wenn Sie Journey Optimizer verwenden, können Sie Ihre Nachrichten jetzt direkt aus einer Journey erstellen.

Diese Funktion erfordert eine Migration vorhandener Journeys, die Nachrichten verwenden. Auf dieser Seite finden Sie die erforderlichen Informationen in Bezug auf diese Änderung sowie die Schritte, die Sie unternehmen müssen.

Weiterführende Informationen zu Ihren Rollen und Zuständigkeiten als Person, die Journey Optimizer verwendet, finden Sie auf dieser [Seite](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## Wichtige Erkenntnisse{#keys}

* **Bin ich betroffen?**: Sie sind betroffen, wenn Sie Nachrichten über das Menü **Nachrichten** in der linken Navigationsleiste erstellen und in Ihren Journeys verwenden. Wenn Sie ein Drittanbietersystem (z. B. Adobe Campaign) verwenden, sind Sie von dieser Migration nicht betroffen.

* **Produktänderungen**: Ab Einführung (25. Juli) wird Ihr Kanalinhalt in den einzelnen Journeys erstellt und verwaltet. Das Menü **Nachrichten** im Navigationsbereich auf der linken Seite steht nicht mehr zur Verfügung. ([Weitere Informationen](../rn/inline-messages.md#change)). Wir werden Ihre bestehenden Journeys für Sie migrieren.

* **Zeitplan**: Die Migration wird für jede Region nachts und in Form von mehreren [Iterationen](../rn/inline-messages.md#iterations) durchgeführt.

   ![](assets/inline-migration-timeline.png)

* **Erforderliche Aktionen**: Die Journeys werden automatisch für Sie konvertiert. Trotzdem brauchen wir Ihre Hilfe bei ein paar Schritten. Weitere Informationen zu den erforderlichen Schritten finden Sie auf dieser [Seite](../rn/inline-messages-steps.md).

* **Einstellung**: Nach dem 6. September werden alle Journeys, die noch immer veraltete Nachrichten verwenden, gestoppt und dann später gelöscht.

## Vorteile und Produktänderungen{#change}

Adobe strebt an, das Produkt kontinuierlich zu vereinfachen, um effiziente und optimierte Abläufe bei der Verwendung zu ermöglichen. Diese neue Methode zur Erstellung von Nachrichten optimiert den Prozess bei der Verwendung.

Wir haben diesen neuen Workflow entwickelt, um Inhalte an einem Ort zu zentralisieren – direkt dort, wo sie verwendet werden.

Die Inhaltserstellung erfolgt nun direkt innerhalb der Journey. Dadurch profitieren Sie von folgenden direkten **Vorteilen**:

* Schnellere Journey-Erstellung mithilfe von Journey Optimizer-Kanälen in einem einzigen Arbeitsablauf.
* Schnelle Visualisierung von Inhalten durch nahtlosen Wechsel zwischen allen E-Mail-, Push- und SMS-Inhalten in einer Journey.
* Verbesserter Fluss für E-Mails und Push-Benachrichtigungen mit kontextbezogener Personalisierung von der Arbeitsfläche.
* Journey-Reporting zentralisiert detaillierte Informationen zum Kanal-Reporting.

Hier finden Sie die **Produktänderungen**, die mit dieser neuen Funktion eingeführt werden:

<table>
<tr>
<th>Vor der Migration</th>
<th>Nach der Migration</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>Zuvor haben Sie Ihre Nachricht über das Menü <strong>Nachrichten</strong> erstellt. </p></td>
<td><img src="assets/inline-migration-after.png"><p>Nun steht das Menü <strong>Nachrichten</strong> im Navigationsbereich auf der linken Seite nicht mehr zur Verfügung. </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>Anschließend haben Sie eine Journey erstellt, eine Aktivität des Typs <strong>Nachricht</strong> hinzugefügt und die zuvor erstellte Nachricht ausgewählt.</p></td>
<td><img src="assets/inline-migration-after2.png"><p>Jetzt fügen Sie einfach die gewünschte Kanalaktionsaktivität (E-Mail, SMS, Push) zu Ihrer Journey hinzu. In der Aktivität können Sie die Parameter für die Nachricht direkt konfigurieren und auf den Inhalts-Editor zugreifen.</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>Zuvor war der Zugriff auf das Reporting sowohl auf Nachrichten- als auch auf Journey-Ebene möglich. Sie mussten zwischen der Registerkarte für die Nachrichtenausführung und dem Journey-Bericht navigieren.</p></td>
<td><img src="assets/inline-migration-after3.png"><p>Jetzt wird das komplette Reporting auf Journey-Ebene zentralisiert. Dies verbessert die Navigation und das Benutzererlebnis. Wenn eine Journey mehrere E-Mails enthält, können Sie über das Dropdown-Menü <strong>Aktion</strong> auf den entsprechenden Bericht zugreifen.
</p></td>
</tr>
</table>

Ab Einführung (25. Juli) gilt dieser neue Ablauf bei der Benutzung für alle neuen Journeys. Das Menü **Nachrichten** im Navigationsbereich auf der linken Seite steht nicht mehr zur Verfügung.

## Zeitplan für die Migration{#iterations}

Es ist eine Migration erforderlich, um Ihre vorhandenen Journeys, in denen **Nachrichten** verwendet werden, in Journeys mit inline erstellten Aktionen umzuwandeln. Die Journeys werden automatisch für Sie konvertiert. Trotzdem brauchen wir Ihre Hilfe bei ein paar Schritten.

Die Migration wird für jede Region nachts und in Form von mehreren Iterationen durchgeführt. Hier finden Sie den Zeitplan für die Migration:

* 25. Juli 2022: Einführung – 1. Iteration
* 1. August 2022: 2. Iteration
* 5. September 2022: 3. Iteration
* 6. September 2022: Einstellung

Warum brauchen wir mehrere Iterationen?

Während einer Iteration sehen wir uns alle Journeys an und migrieren sie nach Möglichkeit. Es gibt Fälle, in denen wir nicht automatisch migrieren möchten: wenn die Journey live ist (d. h., es kann noch Profile enthalten). In diesen Fällen bitten wir Sie, eine Aktion durchzuführen. Diese Journeys, die bei der vorherigen Iteration nicht migriert werden konnten, werden dann bei der nächsten Iteration migriert.

## FAQs {#faq}

### Wie werde ich über den Wechsel informiert?{#inform}

Adobe kommuniziert vor der ersten Iteration mit Ihnen.

Der Wechsel wird über Nacht und in Form von mehreren Iterationen implementiert. Weitere Informationen zu [Iterationen](../rn/inline-messages.md#inline-authoring).

Darüber hinaus werden Sie durch produktinterne Benachrichtigungen informiert, die auf den Bildschirmen der Journeys angezeigt werden:

* Vor der Implementierung der Änderung

   ![](assets/inline-migration-banner1.png)

* Während der Iteration

   ![](assets/inline-migration-banner2.png)

* Nach einer Iteration

   ![](assets/inline-migration-banner3.png)

   Nach einer Iteration wird die Schaltfläche **Status überprüfen** angezeigt. Auf diese Weise können Sie alle Journey im JSON-Format und mit ihrem jeweiligen Migrationsstatus anzeigen. Weitere Informationen finden Sie in diesem [Abschnitt](../rn/inline-messages.md#status).

* Wenn das Banner ausgeblendet wird, sind Sie bereit. Dann ist von Ihnen keine weitere Aktion erforderlich.

### Was ist der Migrationsprozess?{#process}

Die Migration erfolgt vollständig automatisch für Journeys, die nicht live oder geschlossen sind. Wir wollen keine Live- oder geschlossenen Journeys beeinflussen, um Auswirkungen im Betrieb zu vermeiden. Wir bitten Sie, die neue Version zu veröffentlichen, die wir für Sie erstellt haben.

Alle Sandboxes einer Kundenorganisation werden gleichzeitig verarbeitet. Während der Implementierung der Änderungen werden die folgenden Aktionen ausgeführt:

**ALLE Journeys, die keine Nachrichten verwenden**

Diese sind von der Änderung nicht betroffen. Die Migration betrifft nur Journeys, die Nachrichten verwenden. Sie können jedoch weiterhin über die folgende URL auf Nachrichten zugreifen, die nicht in einer Journey verwendet werden: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

**Journey-ENTWÜRFE, die mindestens eine Nachricht verwenden**

Die Entwurfsversionen von Nachrichten werden während der Migration geändert. Sie verweisen nicht mehr auf eine Nachricht. Die Aktivitäten des Typs **Nachricht** werden durch die entsprechenden Kanalaktionsaktivitäten ersetzt. Jede von ihnen enthält die Kanalparameter und Inhalte.

Testen Sie wie gewohnt Ihren Journey-Entwurf, bevor Sie ihn veröffentlichen.

**LIVE-Journeys, die mindestens eine Nachricht verwenden**

Die Live-Version einer Journey wird weiter ausgeführt, um Auswirkungen auf die Produktion zu vermeiden.

Während der Migration wird eine neue Entwurfsversion dieser Journey erstellt. Diese neue Entwurfsversion ist eine Kopie Ihrer Live-Version, Nachrichten werden jedoch durch inline erstellte Kanalaktionen ersetzt. Jede Kanalaktionsaktivität enthält die Kanalparameter und Inhalte. Inhalte gehen nicht verloren. Das Reporting geht nicht verloren.

Sie müssen diesen Entwurf überprüfen, testen und veröffentlichen, damit daraus die Live-Version wird.

**BEENDETE oder ANGEHALTENE Journeys, die mindestens eine Nachricht verwenden**

Diese Journeys werden ebenfalls migriert.

Wenn Sie sich den Journey-Bericht anschauen, sehen Sie, dass die Berichte jetzt umfangreicher sind und die Informationen enthalten, die vorher im Nachrichtenbericht verfügbar waren.

**GESCHLOSSENE Journeys, die mindestens eine Nachricht verwenden**

Die geschlossene Version einer Journey wird für jedes darin enthaltene Profil weiter ausgeführt, um Auswirkungen auf die Produktion zu vermeiden.

Geschlossene Journeys werden nach 30 Tagen automatisch auf den Status „Abgeschlossen“ umgestellt. Sie werden bei der nächsten Iteration berücksichtigt, wenn sie abgeschlossen sind.

**Multi-Channel-Journeys**

Diese werden nicht migriert. Sie müssen sie neu erstellen.

### Was muss ich als Kunde tun?{#actions}

Für die Journeys wird eine automatische Konvertierung durchgeführt, Sie müssen jedoch auch einige Schritte durchführen. Weitere Informationen zu den erforderlichen Schritten finden Sie auf dieser [Seite](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### Wie kann ich den Migrationsstatus überprüfen?{#status}

Klicken Sie auf die Schaltfläche **Status überprüfen** im oberen Banner. Daraufhin wird die folgende Seite angezeigt.

![](assets/inline-migration-log.png)

Der Statusbericht befindet sich auf der Sandbox-Ebene. Dieser Bericht enthält einige nützliche Abschnitte:

**migrationStatus**

In diesem Abschnitt werden die Migrationsinformationen seit der ersten Iteration angezeigt. Nach jeder Iteration werden die Zahlen erhöht.

* MIGRIERT: Anzahl der erfolgreich migrierten Journeys mit den Staus „Entwurf“, „Abgeschlossen“ und „Angehalten“.
* NEW_VERSION_CREATED: Anzahl der migrierten Live-Journeys. Für jede Live-Journey wird eine neue Entwurfsversion erstellt: Sie müssen diese Version testen und veröffentlichen.
* ERROR: Anzahl der Journeys mit den Status „Entwurf“, „Abgeschlossen“ und „Angehalten“, die aufgrund eines Fehlers nicht migriert wurden. Sie müssen sie neu erstellen.
* ERROR_ON_NEW_VERSION_CREATION: Anzahl der Live-Journeys, die aufgrund eines Fehlers nicht migriert wurden. Neue Journey-Versionen mit dem Status „Entwurf“, die aufgrund eines Fehlers nicht migriert wurden. Für sie wurden keine neuen Entwurfsversionen erstellt. Sie müssen sie manuell neu erstellen.

**eligibilityStatus**

In diesem Abschnitt werden die nach der letzten Iteration verbleibenden Elemente aufgelistet:

* toMigrate: Anzahl der zu migrierenden Journeys mit den Status „Entwurf“, „Abgeschlossen“ und „Angehalten“.
* createNewVersion: Anzahl der zu migrierenden Live-Journeys.
* noMigration_live: Anzahl der Live-Journeys, die nicht migriert werden müssen. Geschlossene Journey sind ebenfalls hier aufgeführt.
* noMigration: Anzahl der Journeys, die nicht migriert werden müssen.

Der Abschnitt **Details** enthält für jeden der oben genannten Abschnitte die Liste der zugehörigen Journeys.

### Wird diese Änderung zu einer Unterbrechung des Service führen?{#interruption}

Es wird keine Unterbrechung des Service geben.

* Für alle Live-Journeys gilt: keine Auswirkungen, sie laufen weiter.
* Für erstellte Journeys gilt: Während der Migration (nachts) empfehlen wir dringend, keine Journeys zu erstellen, zu bearbeiten oder zu löschen.

### Werden Daten verloren gehen? {#data}

Bei Live-Journeys gibt es keinen Datenverlust und keine Auswirkungen. Sie haben die Kontrolle über die Veröffentlichung aktualisierter Journey-Versionen.

### Wird es zu einem Verlust bei der Funktionalität kommen?{#functionality}

Die Art und Weise, wie Sie Nachrichten erstellen, wird sich ändern. Funktionalität wird nicht verloren gehen.

### Kann während des Migrationsprozesses auf die Umgebung zugegriffen werden?

Die Migration erfolgt nachts. Sie können das Produkt verwenden. Erstellen, bearbeiten oder löschen Sie jedoch keine Journeys.

### Werden Nachrichten weiterhin gesendet?

Ja, Live-Journeys laufen weiter.

### Woher weiß ich, dass die Migration abgeschlossen ist?

Die Migration ist abgeschlossen, wenn das Banner nicht mehr angezeigt wird. Weitere Informationen finden Sie in diesem [Abschnitt](../rn/inline-messages.md#inform).

### Wie wirkt sich dies auf die Berechtigungen im Zusammenhang mit Nachrichten aus?

Die Inline-Authoring-Funktion wirkt sich auf Berechtigungen aus. Jede Berechtigung im Zusammenhang mit Nachrichten, z. B. [!DNL View Messages] oder [!DNL Manage Messages]automatisch in die mit der Journey-Funktion verknüpften Berechtigungen aufgenommen.

Weiterführende Informationen finden Sie auf dieser [Seite](../administration/ootb-product-profiles.md).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
