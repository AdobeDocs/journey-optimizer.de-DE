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
source-git-commit: 6b9044117dcdd7554dea0c5f791a6dcfb0218010
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 2%

---

# Willkommen beim verbesserten Journey Designer {#new-canvas}

Journey Optimizer bietet jetzt ein **vereinfachtes Journey-Modell**, das das Benutzererlebnis und interne Prozesse verbessern soll. Ab der April-Version können Sie von den folgenden Funktionen profitieren:

* Eine **neu gestaltete Journey-Arbeitsfläche** die für ein modernisiertes Benutzeroberflächenerlebnis sorgt
* Eine **Live-Reporting**-Benutzeroberfläche direkt auf der Journey-Arbeitsfläche verfügbar

>[!NOTE]
>
>Beachten Sie, dass der Rollout für diese Funktion progressiv verläuft. Möglicherweise werden die Änderungen nicht sofort angezeigt.

## Updates zum Journey-Modell

Das neue Journey-Modell wird neben dem bestehenden Modell verwendet, d. h. es wird Journey-Modelle geben, die **zwei verschiedene Modelle**:

* Das Legacy-Modell
* Das neue Modell

Alle Journey des alten Modells bleiben darin. Sie können sie weiterhin bearbeiten, testen oder veröffentlichen. Jede neue Version, die von einer Journey auf dem alten Modell erstellt wurde, bleibt ebenfalls darin enthalten. Es gibt **keine funktionalen Veränderungen** um diese Journey.

Wie Sie im folgenden Screenshot sehen können, sind die -Knoten rund geformt. Dies ist die alte Benutzeroberfläche für Journey im alten Modell.

![](assets/new-canvas.png)

Wenn Sie jedoch **eine neue Journey erstellen** oder **eine vorhandene duplizieren**, befindet sie sich auf dem neuen Modell. Journey mit dem alten Modell werden weiterhin unterstützt, bis eine Mehrheit der Kunden auf das neue Modell umgestellt wird.

Das neue Journey-Modell unterliegt einer Einschränkung. Es ist **möglich, Aktivitäten aus dem alten Modell in das neue zu kopieren und einzufügen und umgekehrt**. Wenn Sie dies tun möchten, empfehlen wir Ihnen, Ihre alte Journey zu duplizieren, um sie auf das neue Modell umzustellen, und dann Ihre Aktivitäten zu kopieren.

Im folgenden Screenshot sehen Sie die neu gestaltete Benutzeroberfläche für die Journey-Arbeitsfläche (nur beim neuen Modell verfügbar):

![](assets/new-canvas2.png)

**Alle neuen Funktionen, die zum Journey-Designer hinzugefügt werden (einschließlich Live-Berichten), stehen ab diesem Zeitpunkt nur noch für Journeys des neuen Modells zur Verfügung.**

## Verbessertes Journey-Leinwanddesign

Mit dem neuen Journey-Modell führen wir eine neue und verbesserte **Journey-Canvas-Benutzeroberfläche** ein, die nahtlos in das Adobe Experience Cloud-Lösungs- und App-Ökosystem passt und ein intuitives und effizientes Anwendererlebnis bietet. Jede Journey des neuen Modells wird dieses neue Design aufweisen.

![](assets/new-canvas3.gif)

Aktivitäten werden jetzt durch quadratische Kästchen mit den folgenden Funktionen dargestellt:

* Die erste Zeile für den Aktivitätstyp, die häufig durch kontextuellere Informationen (unter „Zielgruppen lesen“ enthält sie den Namen der ausgewählten Zielgruppe) oder, falls definiert, durch eine benutzerdefinierte Beschriftung überschrieben wird.
* Die zweite Zeile, die immer den Aktivitätstyp darstellt.

![](assets/new-canvas4.png)

Diese neue Benutzeroberfläche verbessert die Lesbarkeit der Journey-Arbeitsfläche, indem sie (**Aktivitätsbeschriftungen und -typen)**.

Außerdem kann das Produkt-Team mit weniger Klicks weitere Informationen auf der Arbeitsfläche hinzufügen. Ein Beispiel für „weitere Informationen“ wäre die Aufnahme von Live-Berichten in die Journey-Arbeitsfläche, wo Profile zu sehen sind, die aufgrund von Fehlern in Ihre Aktivitäten eintreten oder diese verlassen.

![](assets/new-canvas5.png)

## Live-Berichte auf der Journey-Arbeitsfläche

Zusätzlich zum verbesserten Journey-Arbeitsflächen-Layout wird eine neue Funktion eingeführt, mit der Benutzerinnen und Benutzer Echtzeit-Berichtsmetriken aus den **letzten 24 Stunden**, genannt Live-Berichte, direkt auf der Journey-Arbeitsfläche anzeigen können.

Für jede Aktivität auf jeder Live-Journey mit dem neuen Modell haben Sie Zugriff auf:


* Die Anzahl der Profile, die in diese Aktivität eintreten.
* Anzahl der Profile, die diese Aktivität aufgrund eines Fehlers verlassen haben

![](assets/new-canvas6bis.png)

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
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
