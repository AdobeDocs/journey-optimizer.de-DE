---
title: Schritte für die Migration zur Inline-Erstellung von Journeys
description: Schritte für die Migration zur Inline-Erstellung von Journeys
exl-id: 8412a0bd-674c-4d6a-aa5b-443655d2943a
source-git-commit: 1ab038e8b2f0582ad947400c7d070a70e1a84b9b
workflow-type: ht
source-wordcount: '1048'
ht-degree: 100%

---

# Schritte zur Migration zur Inline-Erstellung{#migration-steps}

Der neue Prozess zum Erstellen von Inhalten in Adobe Journey Optimizer wird auf dieser [Seite](../rn/inline-messages.md) beschrieben. Die Journeys werden automatisch für Sie konvertiert. Trotzdem brauchen wir Ihre Hilfe bei ein paar Schritten.

>[!VIDEO](https://video.tv.adobe.com/v/344699)

Im Folgenden finden Sie die wichtigsten Phasen und Schritte:

**[Vor der Migration](../rn/inline-messages-steps.md#migration-step-1)**

1. Beenden Sie in Nicht-Produktions-Sandboxes alle aktiven und geschlossenen Journeys. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-1-1)
1. Beenden Sie in der Produktions-Sandbox alle noch verfügbaren Live-Ad-hoc-Journeys ohne Profil. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-1-2)

**[Nach der ersten Iteration](../rn/inline-messages-steps.md#migration-step-2)**

1. Prüfen Sie Ihre migrierten Live-Journeys auf Fehler. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-1)
1. Listen Sie alle neuen Versionen auf, die durch die Migration erstellt wurden. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-2)
1. Testen und veröffentlichen Sie sie einzeln. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-3)
1. Listen Sie alle Live-Versionen auf. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-4)
1. Prüfen Sie migrierte Entwurfsversionen auf Fehler. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-5)

**[Nach der zweiten Iteration](../rn/inline-messages-steps.md#migration-step-3)**

1. Überprüfen Sie beide Migrationsphasen. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-3-1)
1. Beenden Sie frühere Versionen. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-3-2)

**[Vor der dritten und letzten Iteration](../rn/inline-messages-steps.md#migration-step-4)**

Überprüfen Sie vor der Einstellung, ob alles migriert wurde.

<br> 

## Vor der Migration (25. Juli){#migration-step-1}

### 1. Beenden Sie alle Live-Journeys und geschlossenen Journeys.{#migration-step-1-1}

Beenden Sie in **Nicht-Produktions-Sandboxes** alle Live-Journeys und geschlossenen Journeys. Dadurch kann der automatisierte Migrationsprozess alle Journey aus diesen Sandboxes ohne Aktion Ihrerseits migrieren. Nach der Migration können Sie gestoppte Journey-Versionen duplizieren und verwenden.

### 2. Beenden Sie alle Live-Ad-hoc-Journeys, in denen es keine Profile mehr gibt.{#migration-step-1-2}

Beenden Sie in der **Produktions-Sandbox** alle Live-Ad-hoc-Journeys, die keine Profile mehr enthalten.

+++Wie finde ich diese Journeys?

Um diese Journeys zu finden, navigieren Sie zum Menü **Journeys** und filtern Sie die Liste nach „Status = Live“ und „Typ = Segment lesen“. Sie können Journeys auch chronologisch vom frühesten bis hin zum neuesten Veröffentlichungsdatum sortieren.

![](assets/inline-migration-steps1.png)

Öffnen Sie sie von oben nach unten.

* Vergewissern Sie sich, dass die Journey eine Nachricht enthält.
* Vergewissern Sie sich, dass es sich nicht um wiederkehrende Journeys handelt. Dies sind keine Ad-hoc-Journeys. Sehr wahrscheinlich möchten Sie sie beibehalten. Dies ist beispielsweise eine wiederkehrende Journey (also keine Ad-hoc-Journey):

   ![](assets/inline-migration-steps2.png)

* Wenn Sie Warte- oder Ereignis-Listener in diesen Journeys verwendet haben, befinden sich möglicherweise noch Profile darin. Sehen Sie sich das Ausführungsdatum der Journey an und fügen Sie beliebige Stunden/Tage hinzu, die Sie in Ihren Warte- oder Ereignis-Listenern definiert haben, um das tatsächliche Datum festzulegen, wenn keine Profile mehr in der Journey enthalten sind. Wenn dieses Datum in der Vergangenheit liegt, können Sie die Journey beenden. Andernfalls wechselt diese Journey automatisch 30 Tage nach dem Journey-Ausführungsdatum in den Status „Abgeschlossen“.

+++

**Wichtige Hinweise**

* Vermeiden Sie es, Journeys vor dem Migrationsdatum (25. Juli) zu beenden. Da das Migrationsscript keine Live-Journeys oder geschlossenen Journeys migriert, wird durch die Begrenzung der Anzahl geschlossener Journey in der Produktions-Sandbox die Anzahl der manuellen Aktionen begrenzt, die nach der Migration erforderlich sind.

* Wenn Sie Live-Journey haben, bei denen es sich nicht um die neueste Version handelt – wenn Sie also eine andere Journey-Version als Entwurf erstellt haben –, veröffentlichen Sie die neueste Version oder löschen Sie sie.

* Wenn Sie Nachrichten haben, die zwar nicht in Journeys verwendet werden, aber trotzdem beibehalten werden sollen, speichern Sie sie als Vorlage. Mehr dazu erfahren Sie auf [dieser Seite](../design/email-templates.md#save-as-template). Beachten Sie, dass Sie bis zur Einstellung weiterhin darauf zugreifen können.

## Nach der ersten Migrationsiteration (25. Juli){#migration-step-2}

Die Migration erfolgt in zwei Phasen: in einer automatisierten Phase (nachts, zwischen dem 25. Juli und dem 26. Juli) und in einer manuellen Phase (ab dem 26. Juli), die Aktionen erfordert.

Informationen zur automatisierten Phase finden Sie auf dieser [Seite](../rn/inline-messages.md#process). Hier finden Sie die Aktionen, die im Rahmen der manuellen Phase in der **Produktions-Sandbox** ausgeführt werden müssen:

<!--
_On non-production sandboxes:_

**1. Check the migration status report for any error**

Click the **Check status** button in the top banner and check that there has been no error during the automatic migration and that there is nothing left to migrate. 

![](assets/inline-migration-steps3.png)

Look for the "ERROR" status. 

![](assets/inline-migration-steps4.png)

* If there is no error, you are good to go.
* If there are errors, look for the error by searching "errorMessage". The following error is expected as migration of multi-channel messages is not supported: "Migration of multi-channel messages is not supported". You will have to rebuild this journey.

    ![](assets/inline-migration-steps5.png)

_On the production sandbox:_

-->

### 1. Prüfen Sie Ihre migrierten Live-Journeys auf Fehler.{#migration-step-2-1}

Prüfen Sie im Statusbericht, ob Fehler bei automatisch migrierten Live-Journeys auftreten ([weitere Informationen](../rn/inline-messages.md#status)). Klicken Sie auf die Schaltfläche **Status prüfen** in der oberen Leiste.

![](assets/inline-migration-steps3.png)

Suchen Sie nach „ERROR_NEW_VERSION_CREATION“:

![](assets/inline-migration-steps6.png)

* Wenn kein Fehler auftritt, bedeutet dies, dass alle Live-Journey-Versionen, die migriert werden müssen, verarbeitet wurden und automatisch eine neue migrierte Entwurfsversion erstellt wurde.

* Wenn Sie einen Fehler sehen, können Sie nach „errorMessage“ suchen und die Fehlermeldung in den Protokollen überprüfen. Multi-Channel-Nachrichten werden nicht migriert. Sie müssen eine weitere Journey erstellen.

   ![](assets/inline-migration-steps5.png)

* Bei anderen Fehlern wenden Sie sich bitte an Ihren CSM oder einen Adobe-Support-Mitarbeitenden, der Sie berät.

### 2. Listen Sie alle neuen Versionen auf, die durch die Migration entstanden sind{#migration-step-2-2}

Sie werden im Titel der Journey als [MIGRIERT] gekennzeichnet und das Erstellungsdatum wird aktualisiert.

![](assets/inline-migration-steps7.png)

### 3. Testen und veröffentlichen Sie eine nach der anderen{#migration-step-2-3}

Stellen Sie sicher, dass die Journey noch in der Produktion ausgeführt werden muss. Wenn die [Vorbereitung vor der Migration](../rn/inline-messages-steps.md#migration-step-1) nicht korrekt ausgeführt wurde, könnte eine neue Version für eine einmalige Journey erstellt werden, die nicht mehr benötigt wird.

Testen Sie Ihre Entwurfsversion der Journey, die jetzt Inline-Kanalaktionen enthält.

Veröffentlichen Sie Ihre neue Journey-Version. Ihre bisherige Live-Version wechselt dann in den Status „Geschlossen“.

### 4. Listen Sie alle Live-Versionen auf{#migration-step-2-4}

Sie sollten alle als aktuell gekennzeichnet sein. Suchen Sie anderenfalls nach der neueren Version, testen Sie sie und veröffentlichen Sie sie.

![](assets/inline-migration-steps8.png)

### 5. Überprüfen Sie die migrierten Entwurfsversionen auf Fehler {#migration-step-2-5}

Klicken Sie auf die Schaltfläche **Status prüfen** im oberen Banner ([weitere Informationen](../rn/inline-messages.md#status)) und stellen Sie sicher, dass bei der automatischen Migration kein Fehler aufgetreten ist und dass nichts mehr migriert werden muss. Beachten Sie, dass alle fehlerhaften Journeys (mit Meldungen) nach dem 5. September (in allen Sandboxes) eingestellt werden.

![](assets/inline-migration-steps11.png)

Achten Sie auf den Status „ERROR“.

![](assets/inline-migration-steps9.png)

* Wenn kein Fehler auftritt, sind Sie bereit.

* Wenn es Fehler gibt, suchen Sie nach dem Fehler, indem Sie nach „errorMessage“ suchen. Der folgende Fehler tritt erwartungsgemäß auf, da die Migration von Multi-Channel-Nachrichten nicht unterstützt wird: „Die Migration von Mehrkanalnachrichten wird nicht unterstützt“. Sie müssen diese Journey neu erstellen.

![](assets/inline-migration-steps5.png)

## Nach der zweiten Iteration (1. August){#migration-step-3}

Die zweite Iteration findet in der Nacht zwischen dem 1. August und dem 2. August statt.

<!--
_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

-->

Wenn alle vorherigen Schritte rechtzeitig ausgeführt wurden, wurden alle Ihre Journey migriert, mit Ausnahme der geschlossenen und der fehlerhaften. Die folgenden Schritte sind in der **Produktions-Sandbox** zu befolgen:

### 1. Überprüfen Sie beide Migrationsphasen.{#migration-step-3-1}

Wenn keine Fehler auftreten, sollten Sie in „eligibilityStatus“, unter „toMigrate“ und „createNewVersion“ keine Journeys haben. Im folgenden Beispiel gibt es einen „ERROR“ und einen „ERROR_NEW_VERSION_CREATION“.

![](assets/inline-migration-steps10.png)

### 2. Beenden Sie frühere Versionen{#migration-step-3-2}

Wenn Sie neuere Journey-Versionen (siehe diesen [Abschnitt](../rn/inline-messages-steps.md#migration-step-2-3)) nicht rechtzeitig, d. h. vor der Iteration 2 (1. August), veröffentlicht haben, dann veröffentlichen Sie die neuere Version.

>[!NOTE]
>
>Beenden Sie die vorherige Version, sonst verlieren Sie sie und das damit verbundene Reporting.

## Vor der dritten und letzten Iteration (5. September){#migration-step-4}

Zwischen dem 1. August und dem 5. September müssen Sie überprüfen, ob alles migriert wurde und ob es keine Journeys mehr gibt, die noch Nachrichten verwenden, da diese sonst am 5. September eingestellt werden.
