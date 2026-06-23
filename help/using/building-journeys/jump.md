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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1982
ht-degree: 38%

---

# Springen zwischen Journeys {#jump}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mit der Sprungaktivität Einzelanwender von einer Journey zur anderen pushen, komplexe Designs vereinfachen und wiederverwendbare, gängige Journey-Muster erstellen können.

>[!ENDSHADEBOX]

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

1. Klicken Sie in das Feld **Target-Journey**.
Die Liste zeigt alle Journey-Versionen an, die entweder den Entwurfs-, Live- oder den Testmodus aufweisen. Journey, die einen anderen Namespace verwenden oder mit einem „Zielgruppen&#x200B;**Qualifizierungsereignis** beginnen, sind nicht verfügbar. Target-Journey, die ein Schleifenmuster erzeugen würden, werden ebenfalls herausgefiltert.

   ![Sprungaktivität mit Ziel-Journey und Aktionsparametern](assets/jump3.png)

   >[!NOTE]
   >
   >Sie können rechts auf das Symbol **Zielgruppen-Journey öffnen** klicken, um die Ziel-Journey in einem neuen Tab zu öffnen.

1. Wählen Sie die Ziel-Journey aus, zu der Sie springen möchten.
Das Feld **Erstes**) ist mit dem Namen des ersten Zielereignisses der Journey vorausgefüllt. Wenn Ihr Ziel-Journey mehrere Ereignisse enthält, ist **[!UICONTROL Springen]** nur beim ersten Ereignis erlaubt.

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

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite wird die Sprungaktivität erläutert, die Profile von einer Journey zur anderen verschiebt, um komplexe Journey-Designs durch wiederverwendbare Sub-Journey-Muster zu vereinfachen.

**intents:**

* Verwenden Sie die Sprungaktivität, um Profile von einer Ursprungs-Journey auf eine Ziel-Journey zu übertragen
* Zerlegen Sie eine komplexe Journey in kleinere, verwaltbare Unter-Journey, die durch Sprungaktivitäten verbunden sind.
* Konfigurieren Sie die Sprungaktivität, indem Sie einen Ziel-Journey auswählen und Aktionsparameter zuordnen.
* Profilverhalten bei Ausführung eines Sprungs verstehen (Profil ist in beiden Journey gleichzeitig aktiv)
* Fehlerbehebung bei Fehlern in der Jump-Konfiguration und Laufzeitfehlern
* Vermeiden Sie Schleifenmuster beim Verketten mehrerer Journey mit Sprungaktivitäten

**Glossar:**

* **Sprungaktivität** Eine Aktionsaktivität, die ein internes Ereignis an das erste Ereignis einer Ziel-Journey sendet und bewirkt, dass das Profil beginnt, durch diese Journey zu fließen. *(produktspezifisch)*
* **Ursprungs-Journey**: Die Journey, die die Sprungaktivität enthält und die Übertragung eines Profils auf eine andere Journey initiiert. *(produktspezifisch)*
* **Target-Journey**: Die Journey, die das Profil über den internen Ereignis-Trigger der Sprungaktivität erhält. *(produktspezifisch)*
* **Stille Überspringen**: Das Verhalten, wenn ein Profil zum Zeitpunkt eines Sprungs bereits auf der Ziel-Journey aktiv ist - der Sprung wird fehlerfrei übersprungen und die Ursprungs-Journey wird normal fortgesetzt. *(produktspezifisch)*

**Leitplanken:**

* Sprungaktivität ist nur in Journey verfügbar, die einen Namespace verwenden. Ursprungs- und Ziel-Journey müssen denselben Namespace verwenden
* Es kann nicht zu einer Journey gesprungen werden, die mit einem Zielgruppen-Qualifizierungsereignis oder „Zielgruppe lesen“ beginnt.
* Sprungaktivität und Zielgruppen-Qualifizierungsereignis oder „Zielgruppe lesen“ können nicht auf derselben Journey verwendet werden
* Schleifenmuster (zirkuläre Journey-Ketten) werden nicht unterstützt und von der Konfigurations-Benutzeroberfläche verhindert
* Zur Laufzeit wird die neueste Live-Version der Ziel-Journey ausgelöst
* Ein Profil kann immer nur einmal auf derselben Journey vorhanden sein. Wenn es bereits auf der Ziel-Journey aktiv ist, wird der Sprung übersprungen
* Wenn die Ziel-Journey entworfen, geschlossen, gestoppt, gelöscht oder die erste Ereigniszuordnung beschädigt ist, führt der Sprung zu einem Konfigurationsfehler

**Terminologie:**

* Kanonischer Name: Sprungaktivität — Akronym: none — Varianten: Sprungaktion, Journey-Sprung
* Synonyme: „origin Journey&quot; = „Quell-Journey&quot;; „target Journey&quot; = „Ziel-Journey&quot;
* Verwechseln Sie nicht: „Stilles Überspringen“ ≠ „Laufzeitfehler“ - Ein stilles Überspringen tritt auf, wenn sich das Profil bereits auf der Ziel-Journey befindet (kein Fehler ausgelöst). Ein Laufzeitfehler tritt auf, wenn die Ziel-Journey nicht erreichbar ist oder nicht erneut eintritt (als fehlgeschlagene Aktion behandelt)

**FAQ:**

* **F: Was passiert mit einem Profil auf der Ursprungs-Journey nach einem Sprung?** — Das Profil durchläuft nach dem Sprungschritt alle verbleibenden Schritte auf der Ursprungs-Journey, während es gleichzeitig auf die Ziel-Journey einläuft; es ist in beiden Journey gleichzeitig aktiv.
* **F: Kann ich zu einer „Zielgruppen-Journey lesen“ springen?** — Nein; Sie können nicht zu einer Journey springen, die mit einem „Zielgruppe lesen“- oder „Zielgruppen-Qualifizierungsereignis“ beginnt.
* **F: Welche Trigger gibt es auf der Ziel-Journey, wenn ein Jump ausgeführt wird?** — Ein internes Ereignis wird durch die Sprungaktivität an das erste Ereignis der Ziel-Journey gesendet. Das Profil durchläuft dann von diesem ersten Ereignis an die Ziel-Journey.
* **Q: Wie vermeide ich unendliche Schleifen bei der Verkettung von Journey mit Jump?** — Schleifenmuster werden von der Benutzeroberfläche für die Konfiguration von Sprungaktivitäten blockiert, die Ziel-Journey herausfiltert, die eine Kreiskette erstellen würden.
* **F: Welche Version der Ziel-Journey wird durch einen Sprung ausgelöst?** — Die neueste Live-Version (oder Testmodus) der Ziel-Journey wird zur Laufzeit ausgelöst.

+++
