---
title: Veröffentlichen und Ändern einer Nachricht
description: Erfahren Sie, wie Sie Nachrichten veröffentlichen und aktualisieren
snippet: y
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Veröffentlichen Sie Ihre Nachrichten {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## Veröffentlichen einer Nachricht {#publish-message}

Nachdem die Nachricht erstellt wurde, können Sie sie veröffentlichen, um sie für die Ausführung verfügbar zu machen.

>[!CAUTION]
>
>Prüfen Sie Warnungen vor der Veröffentlichung und lösen Sie sie. [Weitere Informationen](alerts.md).

![](assets/publish-message.png)

Sobald die Nachricht veröffentlicht wurde, wird sie der Liste mit dem Status **[!UICONTROL Veröffentlicht]** hinzugefügt.

Es kann jetzt von einem oder mehreren [Journey](building-journeys/journey.md) ausgelöst werden.

## Aktualisieren einer schreibgeschützten Meldung {#modify-message}

Nach der Veröffentlichung befindet sich eine Nachricht im schreibgeschützten Modus. Sie können sie dennoch aktualisieren, indem Sie einen neuen Entwurf der Nachricht erstellen.

Dadurch können Sie Inhalte aktualisieren oder beispielsweise ein Problem beheben, ohne die gesamte Journey erneut zu veröffentlichen, auf der Ihre Nachricht verwendet wird.

>[!NOTE]
>
>Die Entwurfsversion kann bearbeitet werden, während die veröffentlichte Version noch veröffentlicht und aktiv ist.

So aktualisieren Sie eine veröffentlichte Nachricht:

1. Wählen Sie in der Liste die Nachricht aus, um sie zu öffnen.

1. Klicken Sie auf **[!UICONTROL Ändern]**.

   ![](assets/message-modify.png)

1. Bestätigen Sie Ihre Wahl. Eine Entwurfsversion der Nachricht wird erstellt.

   ![](assets/message-modify-v2.png)

1. Bearbeiten Sie den Inhalt oder ändern Sie die Einstellungen nach Bedarf.
1. Klicken Sie auf **[!UICONTROL Veröffentlichen]**. Diese Aktion veröffentlicht die neue Version der Nachricht, die für die nächsten Ausführungen verwendet wird.

Sobald die neue Version veröffentlicht ist, wird beim nächsten API-Aufruf eine neue Nachrichtenausführung generiert. Das nächste eingehende Profil erhält die neue Version.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
