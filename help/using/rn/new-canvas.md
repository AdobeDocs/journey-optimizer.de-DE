---
solution: Journey Optimizer
product: journey optimizer
title: Neue Journey-Benutzeroberfläche
feature: Release Notes
topic: Content Management
description: Neue Journey-Benutzeroberfläche
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 87e3ba96d05d41c87f314773e95eb0fcf0a2cfe3
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 1%

---

# Willkommen beim verbesserten Journey-Designer {#new-canvas}

Journey Optimizer bietet jetzt eine **vereinfachtes Journey-Modell** zur Verbesserung der internen Verfahren. Obwohl dieses neue Modell eine Backend-Verbesserung ist, hat unser Team die Gelegenheit genutzt, Funktionen hinzuzufügen, die für Journey Optimizer-Benutzer sichtbar und von Vorteil sind:

* A **neu entworfene Journey-Arbeitsfläche** wurde für ein modernisiertes Benutzeroberflächenerlebnis entwickelt
* A **Live-Reporting** Direkt auf der Journey-Arbeitsfläche verfügbare Benutzeroberfläche

>[!NOTE]
>
>Beachten Sie, dass der Rollout für diese Funktion progressiv sein wird. Möglicherweise sehen Sie die Änderungen nicht sofort.

## Aktualisierungen des Journey-Modells

Das neue Journey-Modell wird neben dem vorhandenen Modell existieren, was bedeutet, dass Journey mit **zwei verschiedene Modelle**:

* Das alte Modell
* Das neue Modell

Alle Journey im alten Modell bleiben darin. Sie können sie weiterhin bearbeiten, testen oder veröffentlichen. Jede neue Version, die von einer Journey auf dem Legacy-Modell erstellt wurde, bleibt dabei erhalten. Es gibt **keine funktionalen Änderungen** um diese Journey herum.

Wie Sie im folgenden Screenshot sehen, sind die Knoten rund, was die alte Benutzeroberfläche für Journey auf dem alten Modell ist.

![](assets/new-canvas.png)

Wenn Sie **eine neue Journey erstellen** oder **Duplizieren einer vorhandenen**, wird es sich auf dem neuen Modell. Journey zum alten Modell werden weiterhin unterstützt, bis die Mehrheit der Kunden zum neuen Modell übergeht.

Es gibt eine Einschränkung für das neue Journey-Modell; es wird **Es ist nicht möglich, Aktivitäten aus dem alten Modell in das neue zu kopieren und einzufügen und umgekehrt**. Wenn Sie dies wünschen, empfehlen wir Ihnen, Ihre alte Journey zu duplizieren, um sie in das neue Modell zu wechseln, und dann Ihre Aktivitäten zu kopieren.

Im folgenden Screenshot sehen Sie die neu entworfene Benutzeroberfläche für die Journey-Arbeitsfläche (nur mit dem neuen Modell verfügbar):

![](assets/new-canvas2.png)

**Neue Funktionen, die dem Journey-Designer hinzugefügt wurden (einschließlich Live-Reporting), stehen ab diesem Zeitpunkt nur noch Journey auf dem neuen Modell zur Verfügung.**

## Verbessertes Journey-Arbeitsflächendesign

Mit dem neuen Journey-Modell führen wir ein neues und verbessertes **Benutzeroberfläche für Journey-Arbeitsfläche**, das nahtlos in das Adobe Experience Cloud-Lösungs- und App-Ökosystem passt und so eine intuitive und effiziente Benutzererfahrung ermöglicht. Jede Journey im neuen Modell wird auf diesem neuen Design stehen.

![](assets/new-canvas3.gif)

Aktivitäten werden jetzt durch eckige Kästchen mit den folgenden Funktionen dargestellt:

* Die erste Zeile, die den Aktivitätstyp darstellt, der häufig durch kontextbezogene Informationen überschrieben wird (z. B. bei &quot;Zielgruppen lesen&quot;, enthält sie den Namen der ausgewählten Zielgruppe), oder eine benutzerdefinierte Bezeichnung, wenn Sie eine definieren.
* Die zweite Zeile, die immer den Aktivitätstyp darstellt.

![](assets/new-canvas4.png)

Diese neue Benutzeroberfläche verbessert die Lesbarkeit der Journey-Arbeitsfläche durch Bereitstellung von **klarere Aktivitätsbezeichnungen und -typen**.

Außerdem kann das Produktteam mehr Informationen auf der Arbeitsfläche mit weniger Klicks hinzufügen. Ein Beispiel für &quot;weitere Informationen&quot;wäre die Einbeziehung von Live-Berichten in die Journey-Arbeitsfläche, in der Sie sehen können, wie Profile aufgrund von Fehlern in Ihre Aktivitäten eintreten und diese beenden.

![](assets/new-canvas5.png)


## Live-Reporting auf der Journey-Arbeitsfläche

Neben dem verbesserten Journey-Canvas-Design bieten wir die Möglichkeit, **Berichtsmetriken der letzten 24 Stunden** (als &quot;Live-Reporting&quot;bezeichnet) direkt auf der Journey-Arbeitsfläche.

![](assets/new-canvas6bis.png)

Mit jeder Live-Journey auf dem neuen Modell können Sie sehen, **für jede Aktivität**, die Anzahl der Profile, die an dieser Aktivität teilgenommen haben, und die Anzahl der Profile, die aufgrund eines Fehlers beendet wurden:

![](assets/new-canvas8.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->

Die Benutzeroberfläche wird jede Minute automatisch aktualisiert.

<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
