---
title: Migration zum Journey Inline-Authoring
description: Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 3%

---


# Übersicht über die Inline-Authoring-Migration{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="Erfahren Sie mehr über die neue Inline-Authoring-Funktion"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt von einer Journey verfasst. Vorhandene Nachrichten werden automatisch in das neue Modell migriert. Nach der Migration sind zusätzliche Aktionen erforderlich, wenn Sie derzeit Nachrichten in Ihren Journey verwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="Erfahren Sie, was passiert"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt von einer Journey verfasst. Ihre Umgebung wird migriert. Nach der Migration sind zusätzliche Aktionen erforderlich, wenn Sie derzeit Nachrichten in Ihren Journey verwenden."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können"
>abstract="Ab dem 25. Juli 2022 werden Nachrichten direkt von einer Journey verfasst. Vorhandene Nachrichten wurden nun in das neue Modell migriert. Als Journey-Anwender sind jetzt zusätzliche Aktionen erforderlich, damit Journey Nachrichten verwenden können."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Migrationsschritte"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Hier erfahren Sie, wie Sie Ihre Nachrichten migrieren können"
>abstract="Ab dem 25. Juli 2022 wird das Menü Nachrichten nicht mehr angezeigt und Nachrichten werden direkt von einer Journey verfasst. Wenn Sie Ihre alten Nachrichten in Journey wiederverwenden möchten, müssen Sie sie als Vorlagen speichern."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html#save-as-template" text="Nachrichten als Vorlagen speichern"

Adobe Journey Optimizer bietet eine neue Funktion, mit der Sie Inhalte für Journey Optimizer-Kanäle (E-Mail, Push, SMS) einfacher erstellen können. Als Journey Optimizer-Praktikant erstellen und bearbeiten Sie Ihre Nachrichten jetzt direkt von einer Journey.

Diese Funktion erfordert eine Migration vorhandener Journey, die Nachrichten verwenden. Auf dieser Seite finden Sie die erforderlichen Informationen zu dieser Änderung sowie die Schritte, die von Ihnen erforderlich sind.

Weiterführende Informationen zu Ihren Rollen und Zuständigkeiten als Journey Optimizer-Experten finden Sie in diesem Abschnitt [page](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## Wichtige Einstiegsmöglichkeiten{#keys}

* **Bin ich betroffen?**: Sie sind betroffen, wenn Sie Nachrichten aus dem **Nachrichten** in der linken Navigation und verwenden Sie sie in Ihren Journey. Wenn Sie ein Drittanbietersystem (z. B. Adobe Campaign) verwenden, sind Sie von dieser Migration nicht betroffen.

* **Produktänderungen**: Bei GA (25. Juli) wird Ihr Kanalinhalt innerhalb jeder Journey erstellt und verwaltet. Die **Nachrichten** im linken Navigationsmenü nicht mehr verfügbar ist ([Weitere Informationen](../rn/inline-messages.md#change)). Wir werden mit der Migration Ihrer bestehenden Journey fortfahren.

* **Timeline**: Die Migration erfolgt für jede Region nachts durch mehrere [iterations](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **Erforderliche Aktionen**: eine automatische Konvertierung der Journey erfolgt für Sie. Trotzdem brauchen wir Ihre Hilfe mit ein paar Schritten. Weitere Informationen zu den erforderlichen Schritten finden Sie in diesem [page](../rn/inline-messages-steps.md).

* **Veraltet**: Nach dem 6. September werden alle Journey, die noch ältere Nachrichten verwenden, gestoppt und später gelöscht.

## Vorteile und Produktänderungen{#change}

Die Adobe strebt an, das Produkt kontinuierlich zu vereinfachen, um effiziente und optimierte Benutzerabläufe zu ermöglichen. Diese neue Methode zur Erstellung von Nachrichten sorgt für einen optimierten Benutzerprozess.

Wir haben diesen neuen Workflow entwickelt, um Inhalte an einem Ort zu zentralisieren, direkt dort, wo sie verwendet werden.

Die Inhaltserstellung erfolgt nun direkt innerhalb der Journey. Die sofortige **Vorteile** Sie erhalten Folgendes:

* Schnellere Journey-Erstellung mithilfe von Journey Optimizer-Kanälen in einem Durchgang.
* Schnelle Visualisierung von Inhalten durch nahtlosen Wechsel zwischen allen E-Mail-, Push- und SMS-Inhalten in einer Journey.
* Verbesserter Fluss für E-Mails und Push-Benachrichtigungen mithilfe einer kontextbezogenen Personalisierung von der Arbeitsfläche.
* Journey Reporting zentralisiert detaillierte Kanalberichterstellungsinformationen.

Hier finden Sie die **Produktänderungen** wurde durch diese neue Funktion eingeführt:

<table>
<tr>
<th>Vor der Migration</th>
<th>Nach Migration</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>Zuvor haben Sie Ihre Nachricht aus dem <strong>Nachrichten</strong> Menü. </p></td>
<td><img src="assets/inline-migration-after.png"><p>Nun, die <strong>Nachrichten</strong> -Menü in der linken Navigation nicht mehr verfügbar. </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>Sie haben dann eine Journey erstellt und eine <strong>Nachricht</strong> und die zuvor erstellte Nachricht ausgewählt.</p></td>
<td><img src="assets/inline-migration-after2.png"><p>Fügen Sie nun einfach die gewünschte Kanalaktionsaktivität (E-Mail, SMS, Push) zu Ihrer Journey hinzu. Konfigurieren Sie in der Aktivität direkt die Nachrichtenparameter und greifen Sie auf den Inhaltseditor zu.</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>Zuvor war der Zugriff auf die Berichterstellung sowohl auf Meldungs- als auch auf Journey-Ebene möglich. Sie mussten zwischen dem Tab Ausführung der Nachricht und dem Bericht Journey navigieren.</p></td>
<td><img src="assets/inline-migration-after3.png"><p>Alle Berichte werden nun auf Journey-Ebene zentralisiert. Dies verbessert die Navigation und das Benutzererlebnis. Wenn eine Journey mehrere E-Mails enthält, können Sie die <strong>Aktion</strong> Dropdown-Menü, um den entsprechenden Bericht anzuzeigen.
</p></td>
</tr>
</table>

Bei GA (25. Juli) gilt dieser neue Benutzerfluss für alle neuen Journey. Die **Nachrichten** -Menü in der linken Navigation nicht mehr verfügbar.

## Migrationszeitleiste{#iterations}

Eine Migration ist erforderlich, um Ihre vorhandenen Journey mithilfe von **Nachrichten** in Journey mit inline erstellten Aktionen. Eine automatische Konvertierung der Journey erfolgt für Sie. Trotzdem brauchen wir Ihre Hilfe mit ein paar Schritten.

Die Migration erfolgt für jede Region nachts durch mehrere Iterationen. Hier finden Sie die Timeline zur Migration:

* 25. Juli 2022: GA - 1. Iteration
* 1. August 2022: 2. Iteration
* 5. September 2022: 3. Iteration
* 6. September 2022: veraltet

Warum brauchen wir mehrere Iterationen?

Während einer Iteration durchlaufen wir jede Journey und migrieren sie nach Möglichkeit. Es gibt Fälle, in denen wir nicht automatisch migrieren möchten: wenn die Journey live ist (d. h., es kann noch Profile enthalten). In diesen Fällen bitten wir Sie, eine Aktion durchzuführen. Anschließend migriert die nächste Iteration diese Journey, die in der vorherigen Iteration nicht migriert werden konnten.

## FAQs {#faq}

### Wie werde ich über die Änderung informiert?{#inform}

Adobe kommuniziert mit Ihnen vor der ersten Iteration.

Die Änderung wird über Nacht durch mehrere Iterationen bereitgestellt. Weitere Informationen finden Sie unter [iterations](../rn/inline-messages.md#inline-authoring).

Darüber hinaus werden Sie durch produktinterne Benachrichtigungen auf den Bildschirmen der Journey informiert:

* Vor der Implementierung

   ![](assets/inline-migration-banner1.png)

* Während der Iteration

   ![](assets/inline-migration-banner2.png)

* Nach einer Iteration

   ![](assets/inline-migration-banner3.png)

   Nach einer Iteration wird die **Status überprüfen** angezeigt. Auf diese Weise können Sie alle Journey im JSON-Format und ihren jeweiligen Migrationsstatus anzeigen. Weitere Informationen finden Sie in diesem [Abschnitt](../rn/inline-messages.md#status).

* Wenn das Banner ausgeblendet wird, können Sie loslegen. Von Ihnen ist keine weitere Aktion erforderlich.

### Was ist der Migrationsprozess?{#process}

Die Migration erfolgt vollständig automatisch für Journey, die nicht live oder geschlossen sind. Wir wollen keine Live- oder geschlossenen Journey beeinflussen, um Produktionsauswirkungen zu vermeiden. Wir bitten Sie, die neue Version zu veröffentlichen, die wir für Sie erstellt haben.

Alle Sandboxes einer Kunden-ORG werden gleichzeitig verarbeitet. Während der Bereitstellung der Änderungen werden die folgenden Aktionen ausgeführt:

**BELIEBIGE Journey, die keine Nachrichten verwendet**

Diese sind von der Änderung nicht betroffen. Nur Journey, die Nachrichten verwenden, werden in die Zielgruppe der Migration aufgenommen. Sie können jedoch weiterhin über die folgende URL auf Nachrichten zugreifen, die nicht in einer Journey verwendet werden: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/Journey-optimizer/messages/

**ENTWÜRFE VON Journey, die mindestens eine Nachricht verwenden**

Die Entwurfsversionen von Nachrichten werden während der Migration geändert. Sie verweisen nicht mehr auf eine Nachricht. Die **Nachricht** -Aktivitäten durch die entsprechenden Kanalaktionsaktivitäten ersetzt. Jeder von ihnen enthält die Kanalparameter und den Inhalt.

Testen Sie wie gewohnt Ihren Entwurf-Journey, bevor Sie ihn veröffentlichen.

**LIVE-Journey, die mindestens eine Nachricht verwenden**

Die Live-Version einer Journey läuft weiter, um Produktionsauswirkungen zu vermeiden.

Eine neue Entwurfsversion dieser Journey wird während der Migration erstellt. Diese neue Entwurfsversion ist eine Kopie Ihrer Live-Version, aber Nachrichten werden durch inline erstellte Kanalaktionen ersetzt. Jede Kanalaktionsaktivität enthält die Kanalparameter und den Inhalt. Inhalt geht nicht verloren. Die Berichterstellung geht nicht verloren.

Wir erwarten von Ihnen, dass Sie diese Entwurfsversion überprüfen, testen und veröffentlichen, damit diese die Live-Version wird.

**Journey, die mindestens eine Nachricht erhalten haben,**

Diese Journey werden ebenfalls migriert.

Beim Betrachten des Journey-Berichts sind die Berichte nun umfangreicher und enthalten den Informationsstand, der zuvor im Nachrichtenbericht verfügbar war.

**GESCHLOSSENE Journey, die mindestens eine Nachricht verwenden**

Die geschlossene Version einer Journey läuft für jedes Profil in der Anwendung, um Produktionsauswirkungen zu vermeiden.

Geschlossene Journey werden nach 30 Tagen automatisch auf den Status &quot;Abgeschlossen&quot;umgestellt. Sie werden bei der nächsten Iteration berücksichtigt, wenn sie fertig sind.

**Journey mit mehreren Kanälen**

Diese werden nicht migriert. Sie müssen sie neu erstellen.

### Was sind meine Aktionselemente als Kunde?{#actions}

Eine automatische Konvertierung von Journey erfolgt für Sie, es sind jedoch einige Schritte erforderlich. Weitere Informationen zu den erforderlichen Schritten finden Sie in diesem [page](../rn/inline-messages-steps.md).

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

Klicken Sie auf **Status überprüfen** im oberen Banner. Die folgende Seite wird angezeigt.

![](assets/inline-migration-log.png)

Der Statusbericht befindet sich auf Sandbox-Ebene. Dieser Bericht enthält einige nützliche Abschnitte:

**migrationStatus**

In diesem Abschnitt werden die Migrationsinformationen seit der ersten Iteration angezeigt. Nach jeder Iteration werden die Zahlen erhöht.

* MIGRIERT: Anzahl der erfolgreich migrierten Entwurfs-, Fertigungs- und gestoppten Journey.
* NEW_VERSION_CREATED: Anzahl der migrierten Live-Journey. Für jede Live-Journey wird eine neue Entwurfsversion erstellt: Sie müssen diese Version testen und veröffentlichen.
* FEHLER: Anzahl der Entwurfs-, Fertigungs- und gestoppten Journey, die aufgrund eines Fehlers nicht migriert wurden. Sie müssen sie neu erstellen.
* ERROR_ON_NEW_VERSION_CREATION: Anzahl der Live-Journey, die aufgrund eines Fehlers nicht migriert wurden. neue Entwurfs-Journey-Versionen wurden aufgrund eines Fehlers nicht migriert. Neue Entwurfsversionen wurden für sie nicht erstellt. Sie müssen sie manuell neu erstellen.

**permissionStatus**

In diesem Abschnitt werden die verbleibenden Elemente nach der letzten Iteration aufgelistet:

* toMigrate: Anzahl der zu migrierenden Entwurfs-, Fertigungs- und gestoppten Journey.
* createNewVersion: Anzahl der zu migrierenden Live-Journey.
* noMigration_live: Anzahl der Live-Journey, die nicht migriert werden müssen. Geschlossene Journey sind auch hier aufgeführt.
* noMigration: Anzahl der Journey, die nicht migriert werden müssen.

Die **details** enthält für jeden der oben genannten Bereiche die Liste der zugehörigen Journey.

### Wird diese Änderung zu einer Unterbrechung des Dienstes führen?{#interruption}

Es wird keine Unterbrechung des Dienstes geben.

* Live-Journey: ohne Auswirkungen, sie laufen weiter.
* Auf erstellten Journey: während der Migration (nachts) empfehlen wir dringend, keine Journey zu erstellen, zu bearbeiten oder zu löschen.

### Werden Daten verloren gehen? {#data}

Es gibt keinen Datenverlust und keine Auswirkungen auf Live-Journey. Sie haben die Kontrolle über die Veröffentlichung aktualisierter Journey-Versionen.

### Wird es zu Funktionsverlust kommen?{#functionality}

Die Art und Weise, wie Sie Nachrichten erstellen, wird sich ändern. Funktionalität wird nicht verloren gehen.

### Wird während des Migrationsprozesses Zugriff auf die Umgebung gewährt?

Die Migration erfolgt nachts. Sie können das Produkt verwenden. Erstellen, bearbeiten oder löschen Sie jedoch keine Journey.

### Werden die Nachrichten weiterhin gesendet?

Ja, Live-Journey laufen weiter.

### Woher weiß ich, dass die Migration abgeschlossen ist?

Die Migration ist abgeschlossen, wenn das Banner ausgeblendet wird. Weitere Informationen finden Sie in diesem [Abschnitt](../rn/inline-messages.md#inform).

### Wie wirkt sich dies auf die Berechtigungen im Zusammenhang mit Nachrichten aus?

Die Inline-Authoring-Funktion wirkt sich auf Berechtigungen aus. Jede Berechtigung im Zusammenhang mit Nachrichten, z. B. [!DNL View Messages] oder [!DNL Manage Messages]automatisch in die mit der Journey-Funktion verknüpften Berechtigungen aufgenommen.

Weiterführende Informationen finden Sie auf dieser [Seite](../administration/ootb-product-profiles.md).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
