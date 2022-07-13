---
title: Schritte für die Migration zum Journey Inline-Authoring
description: Schritte für die Migration zum Journey Inline-Authoring
source-git-commit: f98ef26fa9c6075c852d33d19c796351296a3f94
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 2%

---


# Schritte zur Inline-Authoring-Migration{#migration-steps}

Der neue Prozess zum Erstellen von Inhalten in Adobe Journey Optimizer wird in diesem Abschnitt beschrieben. [page](../rn/inline-messages.md). Eine automatische Konvertierung der Journey erfolgt für Sie. Trotzdem brauchen wir Ihre Hilfe mit ein paar Schritten.

>[!VIDEO](https://video.tv.adobe.com/v/344699)

Im Folgenden finden Sie die wichtigsten Schritte:

**[Vor der Migration](../rn/inline-messages-steps.md#migration-step-1)**

1. Beenden Sie in Nicht-Produktions-Sandboxes alle aktiven und geschlossenen Journey. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-1-1)
1. Beenden Sie in der Produktions-Sandbox alle Live-Ad-hoc-Journey ohne Profil, in denen sich noch kein Profil befindet. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-1-2)

**[Nach der ersten Iteration](../rn/inline-messages-steps.md#migration-step-2)**

1. Suchen Sie nach Fehlern in Ihren migrierten Live-Journey. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-1)
1. Listen Sie alle neuen Versionen auf, die durch die Migration erstellt wurden. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-2)
1. Testen und veröffentlichen Sie sie einzeln. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-3)
1. Auflisten aller Live-Versionen. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-4)
1. Überprüfen Sie, ob Fehler in migrierten Entwurfsversionen auftreten. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-2-5)

**[Nach der zweiten Iteration](../rn/inline-messages-steps.md#migration-step-3)**

1. Überprüfen Sie beide Migrationsphasen. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-3-1)
1. Beenden Sie frühere Versionen. [Weitere Informationen](../rn/inline-messages-steps.md#migration-step-3-2)

**[Vor der dritten und letzten Iteration](../rn/inline-messages-steps.md#migration-step-4)**

Überprüfen Sie, ob alles vor der Einstellung migriert wurde.

<br> 

## Vor der Migration (25. Juli){#migration-step-1}

### 1. Beenden Sie alle lebenden und geschlossenen Journey{#migration-step-1-1}

on **Nicht-Produktions-Sandboxes**, stoppen Sie alle Live- und geschlossenen Journey. Dadurch kann der automatisierte Migrationsprozess alle Journey aus diesen Sandboxes ohne Aktion von Ihnen migrieren. Nach der Migration können Sie gestoppte Journey-Versionen duplizieren und verwenden.

### 2. Beenden Sie alle aktiven Ad-hoc-Journey ohne Profil, die noch in{#migration-step-1-2}

Im **Produktions-Sandbox** stoppen Sie alle aktiven Ad-hoc-Journey, die keine Profile mehr enthalten.

+++Wie finde ich diese Journey?

Um diese Journey zu finden, navigieren Sie zum **Journey** und filtern Sie die Liste nach &quot;Status = Live&quot;und &quot;Typ = Segment lesen&quot;. Sie können Journey chronologisch vom frühesten Veröffentlichungsdatum bis zum neuesten Veröffentlichungsdatum bestellen.

![](assets/inline-migration-steps1.png)

Öffnen Sie sie von oben nach unten.

* Vergewissern Sie sich, dass die Journey eine Meldung enthält.
* Vergewissern Sie sich, dass es sich nicht um wiederkehrende Journey handelt. Dies sind keine Ad-hoc-Fälle. Du willst sie wahrscheinlich am Leben erhalten. Dies ist beispielsweise eine wiederkehrende Journey (nicht Ad-hoc-):

   ![](assets/inline-migration-steps2.png)

* Wenn Sie Wartezeit- oder Ereignis-Listener in diesen Journey verwendet haben, befinden sich die Profile möglicherweise noch in diesen. Sehen Sie sich das Ausführungsdatum der Journey an und fügen Sie beliebige Stunden/Tage hinzu, die Sie in Ihren Wartezeiten- oder Ereignis-Listenern definiert haben, um das tatsächliche Datum festzulegen, an dem keine-Profile mehr in der Datenbank gespeichert sind. Wenn dieses Datum in der Vergangenheit liegt, können Sie die Journey stoppen. Andernfalls wechselt diese Journey automatisch 30 Tage nach dem Journey-Ausführungsdatum in den Status &quot;Abgeschlossen&quot;.

+++

**Wichtige Hinweise**

* Schließen Sie Journey nicht vor dem Migrationsdatum (25. Juli). Da das Migrationsskript keine aktiven oder geschlossenen Journey migriert, wird durch die Begrenzung der Anzahl geschlossener Journey in der Produktions-Sandbox die Anzahl der manuellen Aktionen begrenzt, die nach der Migration erforderlich sind.

* Wenn Sie Live-Journey haben, die nicht die neueste Version sind, d. h. eine andere Journey-Version im Entwurf erstellt haben, veröffentlichen Sie sie oder löschen Sie sie.

* Wenn Sie Nachrichten haben, die nicht in Journey verwendet werden und die Sie beibehalten möchten, speichern Sie sie als Vorlagen. Mehr dazu erfahren Sie auf [dieser Seite](../design/email-templates.md#save-as-template). Beachten Sie, dass Sie bis zur Einstellung weiterhin darauf zugreifen können.

## Nach der ersten Migration (25. Juli){#migration-step-2}

Die Migration erfolgt in zwei Phasen: die automatisierte Phase (nächtlich, zwischen dem 25. Juli und dem 26. Juli) und die manuelle Phase (ab dem 26. Juli), die Aktionselemente erfordert.

Informationen zur automatisierten Phase finden Sie in diesem Abschnitt [page](../rn/inline-messages.md#process). Für die manuelle Phase sind hier die Aktionen aufgeführt, die für die **Produktions-Sandbox**:

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

### 1. Suchen Sie nach Fehlern in Ihren migrierten Live-Journey.{#migration-step-2-1}

Prüfen Sie im Statusbericht , ob Fehler bei automatisch migrierten Live-Journey auftreten ([Weitere Informationen](../rn/inline-messages.md#status). Klicken Sie auf **Status überprüfen** im oberen Banner.

![](assets/inline-migration-steps3.png)

Suchen Sie nach &quot;ERROR_NEW_VERSION_CREATION&quot;:

![](assets/inline-migration-steps6.png)

* Wenn kein Fehler auftritt, bedeutet dies, dass alle zu migrierenden Live-Journey-Versionen verarbeitet und automatisch eine neue migrierte Entwurfsversion erstellt wurde.

* Wenn ein Fehler auftritt, können Sie nach &quot;errorMessage&quot;suchen und die Fehlermeldung in den Protokollen überprüfen. Mehrkanalnachrichten werden nicht migriert. Sie müssen eine weitere Journey erstellen.

   ![](assets/inline-migration-steps5.png)

* Wenden Sie sich bei anderen Fehlern an Ihren CSM oder einen anderen Adobe-Support-Mitarbeiter.

### 2. Liste aller neuen, durch die Migration erstellten Versionen{#migration-step-2-2}

Sie werden als [MIGRIERT] im Titel der Journey und das Erstellungsdatum aktualisiert.

![](assets/inline-migration-steps7.png)

### 3. Testen und veröffentlichen Sie sie einzeln.{#migration-step-2-3}

Stellen Sie sicher, dass die Journey noch in der Produktion ausgeführt werden muss. Wenn die Variable [Vorbereitung vor der Migration](../rn/inline-messages-steps.md#migration-step-1) nicht korrekt ausgeführt wurde, könnte eine neue Version für eine einmalige Journey erstellt werden, die nicht mehr benötigt wird.

Testen Sie Ihre Entwurfsversion der Journey, die jetzt Inline-Kanalaktionen enthält.

Veröffentlichen Sie Ihre neue Journey-Version. Ihre vorherige Live-Version wechselt dann zum Status &quot;Geschlossen&quot;.

### 4. Alle Live-Versionen auflisten{#migration-step-2-4}

Sie sollten alle als neueste Version markiert werden. Wenn nicht, suchen Sie nach der neueren Version, testen Sie sie und veröffentlichen Sie sie.

![](assets/inline-migration-steps8.png)

### 5. Überprüfen Sie, ob Fehler in migrierten Entwurfsversionen auftreten {#migration-step-2-5}

Klicken Sie auf **Status überprüfen** im oberen Banner ([Weitere Informationen](../rn/inline-messages.md#status) und überprüfen Sie, dass während der automatischen Migration kein Fehler aufgetreten ist und dass nichts mehr zu migrieren ist. Beachten Sie, dass alle fehlerhaften Journey (mit Meldungen) nach dem 5. September (in allen Sandboxes) eingestellt werden.

![](assets/inline-migration-steps11.png)

Suchen Sie nach dem Status &quot;ERROR&quot;.

![](assets/inline-migration-steps9.png)

* Wenn kein Fehler auftritt, kannst du gehen.

* Wenn Fehler auftreten, suchen Sie nach dem Fehler, indem Sie nach &quot;errorMessage&quot;suchen. Der folgende Fehler wird erwartet, da die Migration von kanalübergreifenden Nachrichten nicht unterstützt wird: &quot;Die Migration von kanalübergreifenden Nachrichten wird nicht unterstützt.&quot; Sie müssen diese Journey neu erstellen.

![](assets/inline-migration-steps5.png)

## Nach der zweiten Iteration (1. August){#migration-step-3}

Die zweite Iteration findet in der Nacht zwischen dem 1. August und dem 2. August statt.

<!--
_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

-->

Wenn alle vorherigen Schritte rechtzeitig ausgeführt wurden, wurden alle Ihre Journey migriert, mit Ausnahme der geschlossenen und der fehlerhaften Schritte. Im Folgenden finden Sie die Schritte zum **Produktions-Sandbox**:

### 1. Überprüfen Sie beide Migrationsphasen.{#migration-step-3-1}

Wenn keine Fehler auftreten, sollten Sie keine Journey in &quot;permissionStatus&quot;, unter &quot;toMigrate&quot; und &quot;createNewVersion&quot; haben. Im folgenden Beispiel gibt es einen &quot;ERROR&quot;und einen &quot;ERROR_NEW_VERSION_CREATION&quot;.

![](assets/inline-migration-steps10.png)

### 2. Beenden früherer Versionen{#migration-step-3-2}

Wenn Sie keine neueren Journey-Versionen veröffentlicht haben (siehe diesen [Abschnitt](../rn/inline-messages-steps.md#migration-step-2-3)) in der Zeit bedeutet vor Iteration 2 (1. August), dann veröffentlichen Sie die neuere Version.

>[!NOTE]
>
>Beenden Sie die vorherige Version, oder Sie verlieren sie und die zugehörigen Berichte.

## Vor der dritten und letzten Iteration (5. September){#migration-step-4}

Zwischen dem 1. August und dem 5. September müssen Sie überprüfen, ob alles migriert wurde und keine Journey mehr Nachrichten verwenden, da sie sonst ab dem 5. September nicht mehr unterstützt werden.

