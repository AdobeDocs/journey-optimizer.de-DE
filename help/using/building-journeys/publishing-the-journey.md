---
solution: Journey Optimizer
product: journey optimizer
title: Veröffentlichen der Journey
description: Erfahren Sie, wie Sie eine Journey veröffentlichen
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: veröffentlichen, Journey, live, Gültigkeit, prüfen
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 5bdacef2196592776c6b37708b0df0986460ca1f
workflow-type: ht
source-wordcount: '613'
ht-degree: 100%

---

# Veröffentlichen Ihrer Journey {#publishing-the-journey}

Um eine Journey zu aktivieren und neuen Profilen den Eintritt zu ermöglichen, müssen Sie sie veröffentlichen. Durch die Veröffentlichung wird die Journey aktiviert und einsatzbereit. Vor der Veröffentlichung müssen Sie sicherstellen, dass die Journey vollständig und gültig ist, und etwaige Fehler beheben, da eine Journey nicht veröffentlicht werden kann, wenn sie Fehler enthält.

➡️ [Funktion im Video kennenlernen](#video)

## Veröffentlichungsprozess {#journey-publication}

Die Schritte zum Veröffentlichen einer Journey werden nachfolgend beschrieben:

1. Bevor Sie Ihre Journey veröffentlichen, stellen Sie sicher, dass sie gültig und fehlerfrei ist. Journeys können nicht veröffentlicht werden, wenn sie Fehler enthalten.

   * Auf [dieser Seite](testing-the-journey.md) erfahren Sie, wie Sie Journeys testen können.
   * In [diesem Abschnitt](../building-journeys/troubleshooting.md#checking-for-errors-before-testing) erfahren Sie, wie Sie Fehler in Ihrer Journey beheben können.

1. Klicken Sie zum Veröffentlichen der Journey oben rechts im Dropdown-Menü auf die Option **[!UICONTROL Veröffentlichen]**.

   >[!NOTE]
   >
   > Wenn Ihre Journey einer Genehmigungsrichtlinie unterliegt, müssen Sie eine Genehmigung anfordern, um sie veröffentlichen zu können. [Weitere Informationen](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

Nachdem die Journey veröffentlicht wurde, ist sie **schreibgeschützt**. Wenn eine Journey schreibgeschützt ist, können Sie nur die Titel und Beschreibungen der Aktivitäten, den Namen der Journey und die Beschreibung der Journey ändern. Wenn Sie Änderungen an einer veröffentlichten Journey vornehmen müssen, erstellen Sie [ eine neue Version](journey-ui.md#journey-versions) Ihrer Journey.

Wenn Sie eine Journey stoppen, wird sie dauerhaft gestoppt: Alle Personen, die die Journey durchlaufen, werden dauerhaft gestoppt, und die Journey erlaubt keine neuen Eintritte mehr. Wenn Sie die Journey erneut ausführen müssen, müssen Sie sie duplizieren und die neue Journey veröffentlichen.


>[!IMPORTANT]
>
>Wenn Änderungen an einer Angebotsentscheidung vorgenommen werden, die in einer Journey-Nachricht verwendet wird, müssen Sie die Veröffentlichung der Journey aufheben und sie dann erneut veröffentlichen.  Dadurch wird sichergestellt, dass die Änderungen in die Journey aufgenommen werden und die Nachricht den neuesten Aktualisierungen entspricht.


## Journey-Versionen {#journey-versions}

In der Liste der Journeys werden alle Journey-Versionen mit der Versionsnummer angezeigt. Wenn Sie nach einer Journey suchen, werden beim ersten Öffnen der Anwendung die neuesten Versionen oben in der Liste angezeigt. Anschließend können Sie die gewünschte Sortierung definieren und die Anwendung behält sie als Benutzerpräferenz bei. Die Version der Journey wird auch oben auf der Journey-Bearbeitungsoberfläche über der Arbeitsfläche angezeigt.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In der Regel kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey für alle aktiven Journey-Versionen vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](entry-management.md).

### Erstellen einer neuen Version einer Journey {#journey-create-new-version}

Wenn Sie eine Live-Journey ändern müssen, erstellen Sie eine neue Version Ihrer Journey. Gehen Sie wie folgt vor, um eine neue Version einer vorhandenen Journey zu erstellen:

1. Öffnen Sie die neueste Version Ihrer Live-Journey, klicken Sie auf **[!UICONTROL Neue Version erstellen]** und bestätigen Sie.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Sie können eine neue Version nur über die letzte Version einer Journey erstellen.

1. Nehmen Sie Ihre Änderungen vor, klicken Sie auf **[!UICONTROL Veröffentlichen]** und bestätigen Sie.

Ab dem Zeitpunkt der Veröffentlichung der Journey treten Personen in die neueste Version der Journey ein.  Personen, die bereits in einer früheren Version eingetreten sind, bleiben bis zum Ende der Journey darin. Bei einem späteren erneuten Eintritt in dieselbe Journey treten sie in die neueste Version ein.

Journey-Versionen können einzeln angehalten werden. Alle Versionen einer Journey haben denselben Namen.

Wenn Sie eine neue Version einer Journey veröffentlichen, endet die vorherige Version automatisch und wechselt in den Status **Geschlossen**. Es kann kein Eintritt in die Journey stattfinden. Selbst wenn Sie die aktuelle Version stoppen, bleibt die vorherige Version geschlossen.


>[!NOTE]
>
>Für die Versionierung der Journeys gelten bestimmte Schutzmechanismen und Einschränkungen. Weitere Informationen finden Sie auf [dieser Seite](../start/guardrails.md#journey-versions-journey-versions-g).


## Anleitungsvideo {#video}

In diesem Video erfahren Sie, wie Sie eine Journey veröffentlichen:

>[!VIDEO](https://video.tv.adobe.com/v/3427932?quality=12&captions=ger)