---
solution: Journey Optimizer
product: journey optimizer
title: Springen zwischen Journeys
description: Springen zwischen Journeys
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Springen, Aktivität, Journey, Aufspaltung, Aufspalten
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
source-git-commit: 817f9c16ae48b1127e5092add6fbcefa8dd3ba9f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Springen zwischen Journeys {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Aktivität „Sprung“"
>abstract="Mit der Aktionsaktivität „Sprung“ können Sie Kontakte von einer Journey in eine andere bewegen. Diese Funktion ermöglicht es Ihnen, das Design sehr komplexer Journeys zu vereinfachen und Journeys basierend auf allgemeinen und wiederverwendbaren Journey-Mustern zu erstellen."

Mit der Aktionsaktivität **[!UICONTROL Sprung]** können Sie Kontakte von einer Journey in eine andere bewegen. Diese Funktion unterstützt:

* Vereinfachung der Gestaltung sehr komplexer Journeys durch Aufteilung in mehrere Journeys
* Erstellung von Journeys anhand allgemeiner und wiederverwendbarer Journey-Muster

Fügen Sie in der Ursprungs-Journey einfach eine **[!UICONTROL Sprungaktivität]** hinzu und wählen Sie eine Ziel-Journey aus. Wenn der Kontakt in den **[!UICONTROL Sprungschritt]** eintritt, wird ein internes Ereignis an das erste Ereignis der Ziel-Journey gesendet. Wenn die **[!UICONTROL Sprungaktion]** erfolgreich ist, schreitet der Kontakt in der Journey fort. Das Verhalten ist mit anderen Aktionen vergleichbar.

In der Ziel-Journey leitet das erste Ereignis, das intern durch die **[!UICONTROL Sprungaktivität]** ausgelöst wurde, den Kontakt in die Journey.

## Lebenszyklus {#jump-lifecycle}

Nehmen wir an, Sie haben in einer Journey A eine **[!UICONTROL Sprungaktivität]** zu einer Journey B hinzugefügt. Journey A ist dann die **Ursprungs-Journey** und Journey B die **Ziel-Journey**.
Im Folgenden finden Sie die verschiedenen Schritte des Ausführungsprozesses:

**Journey A** wird von einem externen Ereignis ausgelöst:

1. Journey A empfängt ein externes Ereignis, das mit einem Kontakt in Verbindung steht.
1. Der Kontakt erreicht den **[!UICONTROL Sprungschritt]**.
1. Der Kontakt wird in Journey B geleitet und fährt nach dem **[!UICONTROL Sprungschritt]** mit den nächsten Schritten in Journey A fort.

In Journey B wird das erste Ereignis intern über die **[!UICONTROL Sprungaktivität]** von Journey A ausgelöst:

1. Journey B erhielt ein internes Ereignis von Journey A.
1. Der Kontakt wird in Journey B geleitet.

>[!NOTE]
>
>Journey B kann auch über ein externes Ereignis ausgelöst werden.

## Best Practices und Einschränkungen {#jump-limitations}

### Authoring {#jump-limitations-authoring}

* Die **[!UICONTROL Sprungaktivität]** ist nur in Journeys verfügbar, die einen Namespace verwenden.
* Sie können nur in eine Journey springen, die denselben Namespace wie die Ursprungs-Journey verwendet.
* Sie können nicht zu einer Journey springen, die mit einem **Zielgruppen-Qualifizierungsereignis** oder einer Aktivität vom Typ **Zielgruppe lesen** beginnt.
* Dieselbe Journey darf nicht gleichzeitig eine **[!UICONTROL Sprungaktivität]** und ein **Zielgruppen-Qualifizierungsereignis** oder eine Aktivität vom Typ **Zielgruppe lesen** enthalten.
* Sie können so viele **[!UICONTROL Sprungaktivitäten]** in eine Journey aufnehmen, wie Sie benötigen. Nach einem **[!UICONTROL Sprung]** können Sie jede erforderliche Aktivität hinzufügen.
* Sie können beliebig viele Sprungstufen einfügen. So kann z. B. Journey A zu Journey B springen, welche zu Journey C springt, usw.
* Auch die Ziel-Journey kann beliebig viele **[!UICONTROL Sprungaktivitäten]** umfassen.
* Schleifenmuster werden nicht unterstützt. Es gibt keine Möglichkeit, zwei oder mehr Journeys miteinander zu verbinden, die eine Endlosschleife erzeugen würden. Der Konfigurationsbildschirm für **[!UICONTROL Sprungaktivitäten]** verhindert dies.

### Ausführung {#jump-limitations-exec}

* Wenn die **[!UICONTROL Sprungaktivität]** ausgeführt wird, wird die aktuelle Version der Ziel-Journey ausgelöst.
* Wie üblich darf sich ein eindeutiger Kontakt nur einmal in einer Journey befinden. Wenn sich der Kontakt, der aus der Ursprungs-Journey bewegt wurde, bereits in der Ziel-Journey befindet, tritt der Kontakt also nicht mehr in die Ziel-Journey ein. Bei der **[!UICONTROL Sprungaktivität]** wird kein Fehler gemeldet, da dies ein normales Verhalten ist.

## Konfigurieren der Sprungaktivität {#jump-configure}

1. Konfigurieren Sie die **Ursprungs-Journey**.

   ![](assets/jump1.png)

1. Fügen Sie einem beliebigen Schritt in der Journey eine **[!UICONTROL Sprungaktivität]** der Kategorie **[!UICONTROL AKTIONEN]** hinzu. Fügen Sie einen Titel und eine Beschreibung hinzu.

   ![](assets/jump2.png)

1. Klicken Sie in das Feld **Ziel-Journey**.
Die Liste zeigt alle Journey-Versionen an, die sich im Entwurfs-, Live- oder Testmodus befinden. Journeys, die einen anderen Namespace verwenden oder mit einem **Zielgruppen-Qualifizierungsereignis** beginnen, sind nicht verfügbar. Ziel-Journeys, die ein Schleifenmuster erzeugen würden, werden ebenfalls herausgefiltert.

   ![](assets/jump3.png)

   >[!NOTE]
   >
   >Sie können rechts auf das Symbol **Zielgruppen-Journey öffnen** klicken, um die Ziel-Journey in einem neuen Tab zu öffnen.

1. Wählen Sie die Ziel-Journey aus, zu der Sie springen möchten.
Das Feld **Erstes Ereignis** wird vorab mit dem Namen des ersten Ereignisses der Ziel-Journey gefüllt. Wenn Ihre Ziel-Journey mehrere Ereignisse umfasst, ist der **[!UICONTROL Sprung]** nur zum ersten Ereignis zulässig.

   ![](assets/jump4.png)

1. Im Abschnitt **Aktionsparameter** werden alle Felder des Zielereignisses angezeigt. Ordnen Sie wie bei anderen Arten von Aktionen jedem Feld Felder aus dem Ursprungsereignis oder der Datenquelle zu. Diese Informationen werden zur Laufzeit an die Ziel-Journey weitergegeben.
1. Fügen Sie die nächsten Aktivitäten hinzu, um Ihre Ursprungs-Journey zu beenden.

   ![](assets/jump5.png)


   >[!NOTE]
   >
   >Die Identität des Kontakts wird automatisch zugeordnet. Diese Informationen sind auf der Benutzeroberfläche nicht sichtbar.

Ihre **[!UICONTROL Sprungaktivität]** ist konfiguriert. Sobald Ihre Journey live oder im Testmodus ist, werden Kontakte, die den **[!UICONTROL Sprungschritt]** erreichen, in die Ziel-Journey geleitet.

Wenn in einer Journey eine **[!UICONTROL Sprungaktivität]** konfiguriert ist, wird zu Beginn der Ziel-Journey automatisch ein **[!UICONTROL Sprungeintrittssymbol]** hinzugefügt. Auf diese Weise können Sie erkennen, dass die Journey sowohl extern als auch intern durch eine **[!UICONTROL Sprungaktivität]** ausgelöst werden kann.

![](assets/jump7.png)

## Fehlerbehebung {#jump-troubleshoot}

Fehler auftreten auf, wenn:
* die Ziel-Journey nicht mehr existiert,
* der Zustand der Ziel-Journey „Entwurf“, „geschlossen“ oder „gestoppt“ ist,
* wenn sich das erste Ereignis der Ziel-Journey geändert hat und die Zuordnung unterbrochen ist.

![](assets/jump6.png)
