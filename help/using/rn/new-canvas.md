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
source-git-commit: 0b1b1440d43ceadf4d943011d5e30e6ad0a64dbb
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 1%

---

# Willkommen beim verbesserten Journey-Designer {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Neue Funktionen"
>abstract="Neue Arbeitsfläche"

Herzlich Willkommen beim verbesserten Journey Designer!

Wir haben eine **vereinfachtes Journey-Modell** zur Verbesserung der internen Verfahren. Obwohl dieses neue Modell eine Backend-Verbesserung ist, hat unser Team die Gelegenheit genutzt, Funktionen hinzuzufügen, die für Journey Optimizer-Benutzer sichtbar und von Vorteil sind:

* A **neu entworfene Journey-Arbeitsfläche** wurde für ein modernisiertes Benutzeroberflächenerlebnis entwickelt
* A **Live-Reporting** Direkt auf der Journey-Arbeitsfläche verfügbare Benutzeroberfläche

## Aktualisierungen des Journey-Modells

Das neue Journey-Modell wird neben dem vorhandenen Modell existieren, was bedeutet, dass Journey mit **zwei verschiedene Modelle**:

* Die alte Version heißt &quot;v1&quot;
* Und das neue, &quot;v2&quot;genannt

Alle Journey in v1 bleiben in v1. Sie können sie weiterhin bearbeiten, testen oder veröffentlichen. Jede neue Version, die von einer v1 erstellt wurde, verbleibt ebenfalls in v1. Es gibt **keine funktionalen Änderungen** um v1 Journey.

Wie Sie im folgenden Screenshot sehen, sind die Knoten rund, was der alten Benutzeroberfläche für Journey des v1-Modells entspricht.

![](assets/new-canvas.png)

Wenn Sie **Erstellen einer neuen Journey** oder **Duplizieren einer vorhandenen**, wird es eine v2-Journey sein.  Wir planen, die Journey von v1 weiterhin zu unterstützen, bis die Mehrheit der Kunden auf v2-Journey umgestellt wird.

Es gibt eine Einschränkung für das neue Journey-Modell; es wird **Es ist nicht möglich, Aktivitäten von einer v1-Journey in eine v2 zu kopieren und einzufügen und umgekehrt**. Wenn Sie dies wünschen, empfehlen wir Ihnen, Ihre v1-Journey zu duplizieren, um sie zu einer v2 zu machen, und dann Ihre Aktivitäten zu kopieren.

Im folgenden Screenshot sehen Sie die neu entworfene Benutzeroberfläche für die Journey-Arbeitsfläche (nur verfügbar mit dem v2-Modell):

![](assets/new-canvas2.png)

**Neue Funktionen, die zum Journey-Designer hinzugefügt wurden (einschließlich Live-Reporting), sind ab diesem Zeitpunkt nur für Journey mit v2 verfügbar.**

## Verbessertes Journey-Arbeitsflächendesign

Mit dem neuen Journey-Modell führen wir ein neues und verbessertes Modell ein **Benutzeroberfläche für Journey-Arbeitsfläche**, das nahtlos in das Adobe Experience Cloud-Lösungs- und App-Ökosystem passt und so eine intuitive und effiziente Benutzererfahrung ermöglicht. Jegliche Journey im v2-Stapel wird in diesem neuen Design verwendet.

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

![](assets/new-canvas6.png)

Bei jeder Live-Journey auf dem neuen Modell können Sie zwei Arten von &quot;letzten 24 Stunden&quot;Berichtsdaten sehen:

* Auf **neue einfügen** angezeigt wird:
   * Die Anzahl der Profile, die für zielgruppengesteuerte Journey exportiert wurden. Die Anzahl der im letzten Exportauftrag verfügbaren Profile wird zusammen mit dem Zeitpunkt angezeigt, zu dem dieser Export durchgeführt wurde.
   * Die Anzahl der Profile, die die Journey verlassen haben
   * Fehlerprozentsatz
     ![](assets/new-canvas7.png)
* **Bei jeder Aktivität**angezeigt, sehen Sie die Anzahl der Profile, die in diese Aktivität eingestiegen sind, und die Anzahl der Profile, die aufgrund eines Fehlers beendet wurden:
  ![](assets/new-canvas8.png)

Die Benutzeroberfläche wird jede Minute automatisch aktualisiert.

Beachten Sie, dass sich die Anzahl der exportierten Profile und die Anzahl der Profile, die durch die Journey geleitet werden, unterscheiden können. Die Anzahl der exportierten Profile liefert nur Informationen zum letzten Exportauftrag, während die Anzahl der Profile, die eine Aktivität aufrufen, nur Profile enthält, die diesen Vorgang in den letzten 24 Stunden ausgeführt haben. Dies ist insbesondere bei wiederkehrenden täglichen Journey sichtbar, da es zwischen zwei Tagen zu einer Datenüberlappung kommen kann.
