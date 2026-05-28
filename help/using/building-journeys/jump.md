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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qCnWzqjO5YRbKO-WHUo950uoHS0skcZT6sdYyNJ4esE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1405
ht-degree: 60%

---

# Springen zwischen Journeys {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Aktivität „Springen“"
>abstract="Mit der Aktionsaktivität „Sprung“ können Sie Kontakte von einer Journey in eine andere bewegen. Diese Funktion ermöglicht es Ihnen, das Design sehr komplexer Journeys zu vereinfachen und Journeys basierend auf allgemeinen und wiederverwendbaren Journey-Mustern zu erstellen."

Mit der Aktionsaktivität **[!UICONTROL Sprung]** können Sie Kontakte von einer Journey in eine andere bewegen. Diese Funktion unterstützt:

* Vereinfachung der Gestaltung sehr komplexer Journeys durch Aufteilung in mehrere Journeys
* Erstellung von Journeys anhand allgemeiner und wiederverwendbarer Journey-Muster

Fügen Sie in der Ursprungs-Journey eine **[!UICONTROL Sprungaktivität]** hinzu und wählen Sie eine Ziel-Journey aus. Wenn der Kontakt in den **[!UICONTROL Sprungschritt]** eintritt, wird ein internes Ereignis an das erste Ereignis der Ziel-Journey gesendet. Wenn die **[!UICONTROL Sprungaktion]** erfolgreich ist, setzt der Kontakt die Journey fort. Das Verhalten ist mit anderen Aktionen vergleichbar.

In der Ziel-Journey leitet das erste intern durch die **[!UICONTROL Sprungaktivität]** ausgelöste Ereignis den Kontakt in die Journey.

## Lebenszyklus {#jump-lifecycle}

Angenommen Sie haben eine **[!UICONTROL Sprungaktivität]** in Journey A zu Journey B hinzugefügt. Journey A ist die **Ursprungs-Journey** und Journey B die **Ziel-Journey**.

Im Folgenden finden Sie die verschiedenen Schritte des Ausführungsprozesses:

**Journey A** wird von einem externen Ereignis ausgelöst:

1. Journey A empfängt ein externes Ereignis, das mit einem Kontakt in Verbindung steht.
1. Der Kontakt erreicht den **[!UICONTROL Sprungschritt]**.
1. Der Kontakt wird in Journey B geleitet und fährt nach dem **[!UICONTROL Sprungschritt]** mit den nächsten Schritten in Journey A fort.

In Journey B wird das erste Ereignis intern über die **[!UICONTROL Sprungaktivität]** von Journey A ausgelöst:

1. Journey B erhält ein internes Ereignis von Journey A.
1. Der Kontakt wird in Journey B geleitet.

>[!NOTE]
>
>Journey B kann auch über ein externes Ereignis ausgelöst werden.

### Profilverhalten während eines Sprungs {#jump-profile-behavior}

Wenn ein Profil den **[!UICONTROL Sprung]**-Schritt erreicht, schreitet es auf der Ursprungs-Journey (Journey A) weiter voran, während es gleichzeitig auf die Ziel-Journey (Journey B) gelangt. Das Profil ist daher in beiden Journey gleichzeitig aktiv.

Das bedeutet:

* Das Profil führt alle verbleibenden Schritte in Journey A nach der Sprungaktivität aus (z. B. eine Folgewartezeit oder eine schließende Aktion).
* Das Profil beginnt auch unabhängig von Journey A von seinem ersten Ereignis an durch Journey B zu fließen.
* Wenn das Profil **bereits aktiv** in Journey B ist, wenn der Sprung ausgeführt wird, wird **nicht** erneut in Journey B eingegeben. Journey A läuft normal weiter; es wird kein Fehler gemeldet.

>[!NOTE]
>
>Der obige Fall - Profil ist bereits auf Journey B aktiv - führt zu einem **stillen Überspringen**: Es wird kein Fehler ausgelöst und Journey A wird normal fortgesetzt. In anderen Situationen kann der Sprung **fehlschlagen** und Journey A wendet die standardmäßige Aktionsfehlerbehandlung an. Siehe [Laufzeitfehler](#jump-troubleshoot) für die vollständige Liste der Fälle.

## Best Practices und Einschränkungen {#jump-limitations}

Verwenden Sie diese Richtlinien, um das Verhalten von Sprungaktivitäten vorhersehbar und sicher zu halten.

### Authoring {#jump-limitations-authoring}

* Die **[!UICONTROL Sprungaktivität]** ist nur in Journeys verfügbar, die einen Namespace verwenden.
* Sie können nur in eine Journey springen, die denselben Namespace wie die Ursprungs-Journey verwendet.
* Sie können nicht zu einer Journey springen, die mit einem **Zielgruppen-Qualifizierungsereignis** oder einer Aktivität vom Typ **Zielgruppe lesen** beginnt.
* Dieselbe Journey darf nicht gleichzeitig eine **[!UICONTROL Sprungaktivität]** und ein **Zielgruppen-Qualifizierungsereignis** oder eine Aktivität vom Typ **Zielgruppe lesen** enthalten.
* Sie können so viele **[!UICONTROL Sprungaktivitäten]** wie nötig in eine Journey aufnehmen. Nach einem **[!UICONTROL Sprung]** können Sie jede erforderliche Aktivität hinzufügen.
* Sie können beliebig viele Sprungstufen einfügen. Beispielsweise springt Journey A zu Journey B, die zu Journey C springt, usw.
* Auch die Ziel-Journey kann beliebig viele **[!UICONTROL Sprungaktivitäten]** umfassen.
* Schleifenmuster werden nicht unterstützt. Es gibt keine Möglichkeit, zwei oder mehr Journeys miteinander zu verknüpfen. Das würde eine Endlosschleife erzeugen. Der Konfigurationsbildschirm für **[!UICONTROL Sprungaktivitäten]** verhindert dies.

### Ausführung {#jump-limitations-exec}

* Wenn die **[!UICONTROL Sprungaktivität]** ausgeführt wird, wird die aktuelle Version der Ziel-Journey ausgelöst.
* Ein eindeutiger Kontakt kann sich nur einmal in einer Journey befinden. Wenn sich der aus der Ursprungs-Journey geleitete Kontakt bereits in der Ziel-Journey befindet, tritt der Kontakt also nicht noch einmal in die Ziel-Journey ein. Bei der **[!UICONTROL Sprungaktivität]** wird kein Fehler gemeldet, da dies normales Verhalten ist.

## Design-Strategie: Beißgroße Unter-Journey {#jump-strategy}

Komplexe Kundenkanäle und Journey können schnell schwer zu erstellen und zu warten sein, insbesondere wenn zusätzliche Kanäle oder Touchpoints eingeführt werden. Selbst eine Journey mit einer Handvoll Meilensteinen kann 20 oder mehr einzigartige Pfade aufzeigen, die ein Kunde einschlagen kann, und diese Komplexität wächst exponentiell mit jeder Ergänzung.

Ein praktischer Ansatz zur Verwaltung dieses Problems besteht darin, große Journey in kleinere, fokussierte Untergruppen zu unterteilen - eine pro Geschäftsphase oder Meilenstein - und sie mithilfe der Aktivität &quot;**[!UICONTROL &quot;]** verbinden. Dadurch bleibt jede Journey lesbar, testbar und unabhängig wartbar.

**Schritt 1: Visualisieren Sie das End-to-End-Journey**

Ordnen Sie die vollständige Kunden-Journey zu und identifizieren Sie deren allgemeine Phasen. Eine Onboarding-Journey für Treueprogramme kann beispielsweise drei verschiedene Phasen umfassen: Herunterladen der Mobile App, Ausführen einer ersten Transaktion und Durchführen einer zweiten Transaktion.

**Schritt 2: Anmerkungen zu Phasen vornehmen und Unter-Journey definieren**

Markieren Sie die Grenze jeder Phase und definieren Sie deren Geschäftsziel. Jede Phase wird zu einer potenziellen Sub-Journey mit einer eindeutigen Einstiegsbedingung und einem eindeutigen Ziel.

**Schritt 3 - Erstellen und Verbinden von Unter-Journey**

Erstellen Sie jede Phase als separate Journey in Journey Optimizer und verwenden Sie dann **[!UICONTROL Jump]**-Aktivitäten, um Profile von einem Sub-Journey zum nächsten zu übergeben. Das Ergebnis ist eine Reihe einfacherer, wiederverwendbarer Journey, die zusammenarbeiten, um das gesamte End-to-End-Erlebnis zu erzielen - mit geringerem Fehlerrisiko.

>[!TIP]
>
>Ein funktionierendes Beispiel mit einem mehrphasigen Treueprogramm finden Sie unter [Mehrphasen-Treueprogramm-Journey](journeys-uc.md#multi-phase-loyalty).

## Konfigurieren der Sprungaktivität {#jump-configure}

1. Konfigurieren Sie die **Ursprungs-Journey**.

   ![Sprungaktivität in der Journey-Palette für den Übergang zwischen Journeys](assets/jump1.png)

1. Fügen Sie einem beliebigen Schritt in der Journey eine **[!UICONTROL Sprungaktivität]** der Kategorie **[!UICONTROL AKTIONEN]** hinzu. Fügen Sie ein Label und eine Beschreibung hinzu.

   ![Dropdown-Liste zur Auswahl der Ziel-Journey in der Konfiguration der Sprungaktivität](assets/jump2.png)

1. Klicken Sie in das Feld **Ziel-Journey**.
Die Liste zeigt alle Journey-Versionen an, die sich im Entwurfs-, Live- oder Testmodus befinden. Journeys, die einen anderen Namespace verwenden oder mit einem **Zielgruppen-Qualifizierungsereignis** beginnen, sind nicht verfügbar. Ziel-Journeys, die ein Schleifenmuster erzeugen würden, werden ebenfalls herausgefiltert.

   ![Sprungaktivität mit Ziel-Journey und Aktionsparametern](assets/jump3.png)

   >[!NOTE]
   >
   >Sie können rechts auf das Symbol **Zielgruppen-Journey öffnen** klicken, um die Ziel-Journey in einem neuen Tab zu öffnen.

1. Wählen Sie die Ziel-Journey aus, zu der Sie springen möchten.
Das Feld **Erstes Ereignis** wird vorab mit dem Namen des ersten Ereignisses der Ziel-Journey gefüllt. Wenn Ihre Ziel-Journey mehrere Ereignisse umfasst, ist der **[!UICONTROL Sprung]** nur zum ersten Ereignis zulässig.

   ![Konfiguration der Parameterzuordnung für Sprungaktivität mit Ausdruckseditor](assets/jump4.png)

1. Im Abschnitt **Aktionsparameter** werden alle Felder des Zielereignisses angezeigt. Ordnen Sie wie bei anderen Aktionstypen jedes Feld Feldern aus dem Ursprungs-Ereignis oder der Ursprungs-Datenquelle zu. Diese Informationen werden zur Laufzeit an die Ziel-Journey weitergegeben.
1. Fügen Sie die nächsten Aktivitäten hinzu, um Ihre Ursprungs-Journey zu beenden.

   ![Schnittstelle für Testmodus zum Testen der Sprungaktivität zwischen Journeys](assets/jump5.png)


   >[!NOTE]
   >
   >Die Identität des Kontakts wird automatisch zugeordnet. Diese Informationen sind auf der Benutzeroberfläche nicht sichtbar.

Ihre **[!UICONTROL Sprungaktivität]** ist konfiguriert. Sobald Ihre Journey live oder im Testmodus ist, werden Kontakte, die den **[!UICONTROL Sprungschritt]** erreichen, in die Ziel-Journey geleitet.

Wenn in einer Journey eine **[!UICONTROL Sprungaktivität]** konfiguriert ist, wird zu Beginn der Ziel-Journey automatisch ein **[!UICONTROL Sprungeintrittssymbol]** hinzugefügt. Auf diese Weise können Sie erkennen, dass die Journey sowohl extern als auch intern durch eine **[!UICONTROL Sprungaktivität]** ausgelöst werden kann.

![Journey-Fluss mit Sprung von der Quell-Journey zur Ziel-Journey](assets/jump7.png)

## Fehlerbehebung {#jump-troubleshoot}

### Konfigurationsfehler

Die folgenden Probleme verhindern, dass der Sprung ordnungsgemäß funktioniert und auf der Journey-Arbeitsfläche als Fehler angezeigt werden:

* Die Ziel-Journey existiert nicht mehr.
* Die Ziel-Journey ist Entwurf, geschlossen oder gestoppt.
* Das erste Ereignis der Ziel-Journey hat sich geändert und die Zuordnung ist beschädigt.

![Journey-Analysen mit Ausführungsmetriken zur Sprungaktivität](assets/jump6.png)

### Laufzeitfehler

In den folgenden Fällen wird der Sprungschritt in Journey A als **fehlgeschlagene Aktion** behandelt. Journey A wendet die standardmäßige Aktionsfehlerbehandlung an und fährt fort:

* Die bestehende Ziel-Journey-Instanz wurde beendet, und die Ziel-Journey ist nicht wiedereintrittspflichtig.
* Auf der Ziel-Journey wird eine Periode für den erneuten Eintritt konfiguriert. Selbst wenn der erneute Eintritt grundsätzlich zulässig ist, kann das Profil erst wieder eintreten, wenn der Zeitraum abgelaufen ist (der Sprung schlägt mit dem Status „Kein Eintritt für den Zeitraum“ fehl).
* Die Ziel-Journey-Version kann nicht gefunden werden, wurde gelöscht, befindet sich in einem fertigen Zustand oder wurde gestoppt.
