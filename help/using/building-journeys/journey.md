---
solution: Journey Optimizer
product: journey optimizer
title: Allgemeine Funktionsweise
description: Allgemeine Funktionsweise
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 992f1ee215cc7f14d7f29a0bd592838fead2568c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Allgemeine Funktionsweise{#jo-general-principle}

Mit [!DNL Journey Optimizer] können Sie Anwendungsfälle für die Echtzeit-Orchestrierung erstellen und dabei kontextbezogene Daten nutzen, die in Ereignissen oder Datenquellen gespeichert sind.

Erstellen Sie mehrstufige fortgeschrittene Szenarien mit folgenden Funktionen:

* Führen Sie einen **unitären Versand** in Echtzeit aus, ausgelöst durch den Empfang eines Ereignisses, oder **im Batch** unter Verwendung von Adobe Experience Platform-Segmenten.

* Nutzen Sie **Kontextdaten** aus Ereignissen, Informationen aus Adobe Experience Platform oder Daten aus API-Services von Drittanbietern.

* Verwenden Sie die **integrierten Aktionen** zum Senden von in [!DNL Journey Optimizer] entworfenen Nachrichten oder erstellen Sie **benutzerspezifische Aktionen**, wenn Sie zum Senden Ihrer Nachrichten ein Drittanbietersystem verwenden.

* Erstellen Sie mit dem **Journey Designer** Ihre mehrstufigen Anwendungsfälle: Ziehen Sie einfach per Drag-and-Drop ein Eintrittsereignis oder eine Aktivität zum Lesen von Segmenten in den Arbeitsbereich, fügen Sie Bedingungen hinzu und senden Sie personalisierte Nachrichten.

## Lebenszyklus einer Journey{#journey-lifecyle}

### Profile in Journeys{#profile-journey}

In einer unitären Journey gilt folgendes:

* Wenn der erneute Eintritt aktiviert ist, kann ein Profil mehrmals in eine Journey eintreten, aber erst dann, wenn es aus der vorherigen Instanz der Journey vollständig ausgetreten ist.

* Wenn der erneute Eintritt deaktiviert ist, kann ein Profil nicht mehrmals in dieselbe Journey eintreten.

Weiterführende Informationen zum erneuten Eintreten von Profilen finden Sie in [diesem Abschnitt](../building-journeys/journey-gs.md#change-properties).

In einer Journey mit dem Schritt „Segment lesen“ gilt Folgendes:

* Für nicht wiederkehrende Journeys: Das Profil tritt nur einmal in die Journey ein.
* für wiederkehrende Journeys: Das Profil tritt bei jeder Wiederholung in die Journey ein, wenn es sich im Segment / im erwarteten Status befindet. Wenn es sich noch in der Journey einer früheren Wiederholung befindet, fängt es wieder von vorne an.

Bei Journeys mit Geschäftsereignissen, die mit dem Schritt „Segment lesen“ beginnen, gilt Folgendes:

Da diese Journey auf dem Empfang eines Geschäftsereignisses basiert, tritt das Profil, wenn es im erwarteten Segment ist, bei jedem empfangenen Geschäftsereignis in die Journey ein. Dies bedeutet, dass dieses Profil gleichzeitig mehrfach in derselben Journey sein kann, aber im Kontext verschiedener Geschäftsereignisse.

Einzelne Journeys (beginnend mit einem Ereignis oder einer Segmentqualifikation) enthalten eine Schutzvorkehrung, die verhindert, dass Journeys fälschlicherweise mehrmals für dasselbe Ereignis ausgelöst werden. Der erneute Profil-Eintritt wird standardmäßig fünf Minuten lang vorübergehend blockiert. Wenn beispielsweise ein Ereignis um 12:01 Uhr eine Journey für ein bestimmtes Profil auslöst und um 12:03 Uhr ein weiteres eintrifft (unabhängig davon, ob es sich um dasselbe Ereignis oder ein anderes handelt, das dieselbe Journey auslöst), wird diese Journey für dieses Profil nicht erneut gestartet.


### Ende einer Journey{#journey-ending}

Eine Journey kann für eine Person auf zwei Weisen enden:

* Die Person kommt bei der letzten Aktivität eines Pfades an.
* Die Person kommt bei einer **Bedingungs**-Aktivität (oder einer **Warte**-Aktivität mit einer Bedingung) an und erfüllt keine der Bedingungen.

Die Person kann dann wieder in die Journey eintreten, wenn der erneute Zutritt erlaubt ist. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/journey-gs.md#change-properties)

Um eine Live-Journey zu beenden, empfehlen wir, sie zu schließen. Der Eintritt neuer Kunden und Kundinnen in die Journey wird dann blockiert. Kunden und Kundinnen, die bereits in die Journey eingetreten sind, bleiben bis zu deren Ende darin. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey.md#close-journey)

Sie können eine Journey nur stoppen, wenn ein unerwartetes Ereignis eintritt und die gesamte Verarbeitung der Journey unverzüglich abgebrochen werden muss. Personen, die bereits in eine Journey eingetreten sind, sind alle in ihrem Fortschritt angehalten. Weiterführende Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey.md#stop-journey).

>[!NOTE]
>
>Beachten Sie, dass Sie eine geschlossene oder gestoppte Journey nicht fortsetzen können.

#### Journey-End-Tag{#end-tag}

Beim Erstellen einer Journey wird am Ende jedes Pfads ein „End-Tag“ angezeigt. Dieser Knoten kann nicht manuell hinzugefügt oder entfernt werden, und lediglich bei seiner Kennzeichnung sind Änderungen möglich. Er markiert das Ende jedes Pfads der Journey. Wenn die Journey mehrere Pfade hat, empfehlen wir, für jedes Ende eine Kennzeichnung hinzuzufügen, damit Berichte leichter verständlich sind. Weitere Informationen finden Sie auf [dieser Seite](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

#### Schließen einer Journey{#close-journey}

Eine Journey kann aus den folgenden Gründen geschlossen werden:

* Die Journey wird manuell über die Schaltfläche **[!UICONTROL Für neue Eintritte schließen]** geschlossen.
* Eine segmentbasierte Journey zur einmaligen Ausführung wurde abgeschlossen.
* Nach dem letzten Vorkommen einer wiederkehrenden segmentbasierten Journey.

Sie können eine Journey manuell schließen. In diesem Fall können Kunden, die sich bereits in der Journey befinden, ihren Pfad bis zum Ende verfolgen, neue Benutzende können jedoch nicht in die Journey eintreten. Wenn eine Journey geschlossen wird (aus einem der oben genannten Gründe), weist sie den Status **[!UICONTROL Geschlossen]** auf. Die Journey stoppt den Eintritt neuer Personen. Personen, die sich bereits in der Journey befinden, können die Journey wie gewohnt beenden. Nach der standardmäßigen globalen maximalen Wartezeit von 30 Tagen wechselt die Journey zum Status **Beendet**. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey-gs.md#global_timeout).

Eine geschlossene Journey-Version kann weder neu gestartet noch gelöscht werden. Stattdessen können Sie eine neue Version davon erstellen oder sie duplizieren. Nur abgeschlossene Journeys können gelöscht werden.

Um eine Journey in der Liste der Journeys zu schließen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Für neue Eintritte schließen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie schließen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.

   ![](assets/finish_drop_down_list.png)

1. Klicken Sie auf **[!UICONTROL Für neue Eintritte schließen]** und bestätigen Sie diese Auswahl im Dialogfeld.

#### Stoppen einer Journey{#stop-journey}

Sie können nötigenfalls den Fortschritt aller Personen in einer Journey stoppen. In diesem Fall entsteht für alle Personen in der Journey eine Zeitüberschreitung. Wenn Sie eine Journey stoppen, wird der Fortschritt der bereits in der Journey befindlichen Personen angehalten. Die Journey wird praktisch deaktiviert. Wenn Sie ein Journey beenden möchten, empfehlen wir Ihnen, sie zu schließen.

Eine gestoppte Journey-Version kann nicht nochmals gestartet werden.

Beim Stoppen wird der Journey-Status auf **[!UICONTROL Gestoppt]** gesetzt.

Sie können beispielsweise eine Journey stoppen, wenn ein Marketer erkennt, dass die Journey die falsche Zielgruppe anspricht, oder wenn eine benutzerdefinierte Aktion, mit der Nachrichten gesendet werden sollen, nicht ordnungsgemäß funktioniert. Um eine Journey aus der Liste der Journeys zu entfernen, klicken Sie auf den Button mit den **[!UICONTROL Auslassungszeichen]** rechts neben dem Journey-Namen und wählen Sie **[!UICONTROL Stoppen]** aus.

![](assets/journey-finish-quick-action.png)

Alternativ können Sie auch folgendermaßen vorgehen:

1. Wählen Sie in der Liste **[!UICONTROL Journeys]** die Journey aus, die Sie stoppen möchten.
1. Klicken Sie oben rechts auf den Abwärtspfeil.
   ![](assets/finish_drop_down_list.png)
1. Klicken Sie auf **[!UICONTROL Stoppen]** und bestätigen Sie diese Auswahl im Dialogfeld.



## Journey-Versionen{#journey-versions}

In der Liste der Journeys werden alle Journey-Versionen mit der Versionsnummer angezeigt. Weitere Informationen finden Sie auf [dieser Seite](../building-journeys/using-the-journey-designer.md).

Wenn Sie nach einer Journey suchen, werden beim ersten Öffnen der Anwendung die neuesten Versionen oben in der Liste angezeigt. Anschließend können Sie die gewünschte Sortierung definieren und die Anwendung behält sie als Benutzervoreinstellung bei. Die Version der Journey wird auch oben auf der Benutzeroberfläche zum Bearbeiten der Journey (oberhalb der Arbeitsfläche) angezeigt.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In den meisten Fällen kann ein Profil nicht mehrmals zur gleichen Zeit in derselben Journey vorhanden sein. Wenn der erneute Eintritt aktiviert ist, kann ein Profil erneut in eine Journey eintreten, aber erst dann, wenn es die vorherige Instanz der Journey vollständig verlassen hat. [Weitere Informationen](#journey-ending)

Wenn Sie eine Live-Journey ändern müssen, erstellen Sie eine neue Journey-Version.

1. Öffnen Sie die aktuelle Version Ihrer Live-Journey, klicken Sie auf **[!UICONTROL Neue Version erstellen]** und bestätigen Sie.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Sie können nur aus der aktuellen Version einer Journey eine neue Journey erstellen.

1. Nehmen Sie Ihre Änderungen vor, klicken Sie auf **[!UICONTROL Veröffentlichen]** und bestätigen Sie.

   ![](assets/journeyversions3.png)

Ab dem Zeitpunkt der Veröffentlichung der Journey nehmen Kontakte an der neuen Version der Journey teil. Personen, die bereits an einer früheren Version teilnehmen, bleiben in ihr, bis sie die Journey beenden. Wenn sie später wieder in dieselbe Journey eintreten, wechseln sie in die aktuelle Version.

Journey-Versionen können einzeln gestoppt werden. Alle Versionen von Journeys haben denselben Namen.

Wenn Sie eine neue Version einer Journey veröffentlichen, endet die vorherige Version automatisch und wechselt in den Status **Geschlossen**. Es kann kein Eintritt in die Journey erfolgen. Auch wenn Sie die neueste Version stoppen, bleibt die vorherige Version geschlossen.

>[!NOTE]
>
>Weitere Informationen zu den Limits und Einschränkungen von Journey-Versionen finden Sie unter [diese Seite](../start/guardrails.md#journey-versions-limitations)