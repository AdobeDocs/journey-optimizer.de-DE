---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Journey-Aktivitäten
description: Erste Schritte mit Journey-Aktivitäten
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: Journey, Aktivitäten, erste Schritte, Ereignisse, Aktion
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8M5qgoXuziyVXMHPOwiM3xztCSNmglc2fBu-BaXn9mc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: fa683eda-48de-4558-af32-2673edcd44feid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1263
ht-degree: 41%

---

# Erste Schritte mit Journey-Aktivitäten {#about-journey-activities}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie Ereignis-, Orchestrierungs- und Aktionsaktivitäten kombinieren, um mehrstufige kanalübergreifende Journey mit Best Practices für die Kennzeichnung von Aktivitäten, die Verwaltung von Parametern und die Fehlerbehebung zu erstellen.

>[!ENDSHADEBOX]

Kombinieren Sie Ereignis-, Orchestrierungs- und Aktionsaktivitäten, um mehrstufige, kanalübergreifende Szenarien zu erstellen.

## Ereignisaktivitäten {#event-activities}

Personalisierte Journey beginnen mit Ereignissen wie einem Online-Kauf. Sobald ein Profil auf eine Journey gelangt ist, durchläuft es diese selbstständig. Jedes Profil kann einen anderen Pfad und eine andere Geschwindigkeit wählen. Wenn Sie mit einem Ereignis beginnen, wird der Journey bei Eintreffen des Ereignisses Trigger. Jedes Profil folgt dann den Schritten, die in Ihrem Journey definiert sind.

Vom technischen Anwender konfigurierte Ereignisse (siehe [diese Seite](../event/about-events.md) werden in der ersten Kategorie der Palette angezeigt. Diese Kategorie befindet sich auf der linken Bildschirmseite. Folgende Ereignisaktivitäten sind verfügbar:

* [Allgemeine Ereignisse](../building-journeys/general-events.md)
* [Reaktion](../building-journeys/reaction-events.md)
* [Zielgruppenqualifizierung](../building-journeys/audience-qualification-events.md)

![Palette „Ereignisaktivitäten“ im Journey-Designer](assets/journey43.png)

Legen Sie zum Starten der Journey eine Ereignisaktivität per Drag-and-Drop ab. Sie können auch auf sie doppelklicken.

![Ablegen einer Ereignisaktivität per Drag-and-Drop im Journey-Designer](assets/journey44.png)

## Orchestrierungsaktivitäten {#orchestration-activities}

Orchestrierungsaktivitäten sind Bedingungen, die bei der Bestimmung des nächsten Schritts im Journey helfen. Zu diesen Bedingungen kann gehören, ob die Person einen offenen Support-Fall hat oder einen Kauf abgeschlossen hat. Sie können auch die lokale Wettervorhersage enthalten oder angeben, ob die Person 10.000 Treuepunkte erreicht hat.

In der Palette auf der linken Seite des Bildschirms stehen die folgenden Orchestrierungsaktivitäten zur Verfügung:

* [Optimieren](optimize.md)
* [Zielgruppe lesen](read-audience.md)
* [Warten](wait-activity.md)
* [Journey-Fragmente](journey-fragments.md)
* [Inhaltsentscheidung](content-decision.md)
* [Datensatzsuche](dataset-lookup.md)

![Palette „Orchestrierungsaktivitäten“ im Journey-Designer](assets/journey-orchestration-activities.png)

## Aktionsaktivitäten {#action-activities}

Aktionen sind das Ergebnis eines Auslösers, wie das Senden einer Nachricht. Sie sind die Teile der Journey, die die Kundin bzw. der Kunde wahrnimmt.

In der Palette auf der linken Seite des Bildschirms finden Sie unter **[!UICONTROL Ereignisse]** und **[!UICONTROL Orchestrierung]** die Kategorie **[!UICONTROL Aktionen]**. Folgende Aktionsaktivitäten sind verfügbar:

* [Integrierte Kanalaktionen](../building-journeys/journey-action.md) verfügbar über die Aktivität **Aktion** .
* [Benutzerdefinierte Aktionen](../building-journeys/using-custom-actions.md)
* [Sprung](../building-journeys/jump.md)

![Palette „Aktionsaktivitäten“ im Journey-Designer](assets/journey58.png)

Diese Aktivitäten repräsentieren die verschiedenen Kommunikationskanäle. Sie können sie zu einem kanalübergreifenden Szenario verbinden.

Es können auch bestimmte Aktionen zum Senden von Nachrichten eingerichtet werden:

* Wenn zum Versenden von Nachrichten ein Drittanbietersystem verwendet wird, kann eine bestimmte benutzerdefinierte Aktion erstellt werden. [Weitere Informationen](../action/action.md)

* Wenn Sie mit [!DNL Adobe Campaign] und [!DNL Adobe Journey Optimizer] arbeiten, lesen Sie diese Abschnitte:

   * [[!DNL Adobe Journey Optimizer] und [!DNL Adobe Campaign] v7/v8](../action/acc-action.md)
   * [[!DNL Adobe Journey Optimizer] und [!DNL Adobe Campaign] Standard](../action/acs-action.md)
   * [[!DNL Adobe Journey Optimizer] und [!DNL Adobe Marketo Engage]](../action/marketo-engage.md)

## Best Practices {#best-practices}

Verwenden Sie diese Empfehlungen, um Journey lesbar, konsistent und leicht zu beheben.

### Hinzufügen eines Labels

Die meisten Aktivitäten ermöglichen es Ihnen, ein **[!UICONTROL Label]** zu definieren. Auf diese Weise wird dem Namen, der unter der Aktivität auf der Arbeitsfläche angezeigt wird, ein Suffix hinzugefügt. Dies ist nützlich, wenn Sie dieselbe Aktivität mehrmals in Ihrer Journey verwenden und sie leichter identifizieren möchten. Außerdem wird das Debugging bei Fehlern und das Lesen von Berichten erleichtert. Sie können auch eine optionale **[!UICONTROL Beschreibung]** hinzufügen.

![Label- und Beschreibungsfelder in den Eigenschaften der Journey-Aktivität](assets/journey-action-label.png)

>[!NOTE]
>
>Bei einigen Aktivitäten ist ihre ID auch im Bereich sichtbar. Diese ID kann beim Reporting als stabilerer Schlüssel verwendet werden als das Label, da letzteres sich ändern kann.

### Verwalten erweiterter Parameter {#advanced-parameters}

Die meisten Aktivitäten zeigen eine Reihe erweiterter und/oder technischer Parameter an, die Sie nicht ändern können.

![Felder für erweiterte Parameter in den Eigenschaften der Journey-Aktivität](assets/journey-advanced-parameters.png)

Zur besseren Lesbarkeit können Sie diese Parameter mithilfe der Schaltfläche **[!UICONTROL Schreibgeschützte Felder ausblenden]** oben im rechten Bereich ausblenden.

![Symbol „Schreibgeschützte Felder ausblenden“ in den Eigenschaften der Journey-Aktivität](assets/journey-hide-read-only-fields.png)

In bestimmten Kontexten können Sie die Werte dieser Parameter für eine bestimmte Verwendung überschreiben. Um einen bestimmten Wert zu erzwingen, können Sie das Symbol **[!UICONTROL Parameterüberschreibung aktivieren]** rechts neben dem Feld anklicken. [Weitere Informationen](../configuration/primary-email-addresses.md#override-execution-address-journey)

![Option „Parameterüberschreibung aktivieren“ in den Eigenschaften der E-Mail-Aktivität](assets/journey-enable-parameter-override.png)

>[!NOTE]
>
>Wenn die erweiterten Parameter ausgeblendet sind, klicken Sie auf die Schaltfläche **[!UICONTROL Schreibgeschützte Felder anzeigen]**.
>
>![Symbol „Schreibgeschützte Felder anzeigen“ in den Eigenschaften der Journey-Aktivität](assets/journey-show-read-only-fields.png){width=60%}

### Hinzufügen eines alternativen Pfads

Wenn in einer Aktion oder einer Bedingung ein Fehler auftritt, wird die Journey des Kontakts gestoppt. Die einzige Möglichkeit zum Fortsetzen des Vorgangs besteht darin, das Kontrollkästchen **[!UICONTROL Alternativen Pfad hinzufügen, falls eine Zeitüberschreitung oder ein Fehler auftritt]** zu aktivieren. Siehe [diesen Abschnitt](../building-journeys/using-the-journey-designer.md#paths)

![Option „Alternativen Pfad hinzufügen“ in den Eigenschaften der Bedingungsaktivität](assets/journey42.png)

## Fehlerbehebung {#troubleshooting}

Überprüfen Sie vor dem Testen und Veröffentlichen Ihrer Journey, ob alle Aktivitäten ordnungsgemäß konfiguriert sind. Es können keine Tests oder Veröffentlichungen vorgenommen werden, solange das System noch Fehler findet.

[Auf dieser Seite](troubleshooting.md) erfahren Sie, wie Sie Fehler in Aktivitäten und in der Journey beheben.

Siehe auch [Überwachung und Fehlerbehebung](../../rp_landing_pages/troubleshoot-journey-landing-page.md)

+++ KI-Wissensreferenz

Dieser Abschnitt enthält strukturiertes Wissen zur Unterstützung von Interpretation, Abrufen und Antworten auf Fragen zu diesem Thema.

Zum vollständigen Verständnis sollten diese Informationen mit der Dokumentation auf dieser Seite kombiniert werden. Keine der beiden Quellen ist für Einzelpersonen gedacht. Die Seite beschreibt die Funktion, während dieser Abschnitt zusätzlichen Kontext bietet, der dabei hilft, Begriffe, Absichten, Anwendbarkeit und Begrenzungen zu unterscheiden.

* **TL;DR:** Auf dieser Seite werden die drei Kategorien von Journey-Aktivitäten - Ereignisse, Orchestrierung und Aktionen - vorgestellt und Best Practices für die Kennzeichnung, Verwaltung von Parametern und Fehlerbehandlung in Adobe Journey Optimizer-Journey erläutert.

**intents:**
* Ermitteln und Unterscheiden zwischen Ereignis-, Orchestrierungs- und Aktionsaktivitäten in einer Journey
* Hinzufügen von Beschriftungen und Beschreibungen zu Journey-Aktivitäten, um die Identifizierung und Berichterstellung zu erleichtern
* Konfigurieren eines alternativen Pfads zur Verarbeitung von Zeitüberschreitungen oder Fehlern in einer Journey-Aktivität
* Erweiterte Parameter einer bestimmten Journey-Aktivität überschreiben
* Kombinieren mehrerer Aktivitätstypen zum Erstellen kanalübergreifender Journey-Szenarien
* Fehlerbehebung bei Konfigurationsfehlern in Aktivitäten vor der Veröffentlichung einer Journey

**Glossar:**
* **Ereignisaktivität** Eine durch ein eingehendes Ereignis ausgelöste Journey-Aktivität (z. B. Kauf, Zielgruppen-Qualifizierung), die ein Profil über die Journey-*startet oder voranbringt (produktspezifisch)*
* **Orchestrierungsaktivität**: Eine Journey-Aktivität (z. B. Optimieren, Zielgruppe lesen, Warten), die die Fluss- und Verzweigungslogik eines Journey-*(produktspezifisch) steuert*
* **Aktionsaktivität** Eine Journey-Aktivität, die eine Kommunikation bereitstellt oder als Ergebnis eines Triggers ein externes System aufruft *produktspezifisch)*
* **Benutzerdefinierte Aktion**: Eine benutzerkonfigurierte Aktion, die Journey Optimizer zum Senden von Nachrichten oder *(produktspezifisch) mit einem Drittanbietersystem verbindet*
* **Alternativpfad**: Eine Fallback-Verzweigung, die zu einer Aktivität hinzugefügt wird, sodass der Journey auch dann fortgesetzt wird, wenn eine Zeitüberschreitung oder ein Fehler auftritt *(produktspezifisch)*

**Leitplanken:**
* Tests und Veröffentlichungen können nicht durchgeführt werden, wenn in einer Aktivität weiterhin Konfigurationsfehler erkannt werden
* Erweiterte/technische Parameter sind für die meisten Aktivitäten schreibgeschützt und können nicht ohne Verwendung der Parameterüberschreibungsfunktion geändert werden

**Terminologie:**
* Kanonischer Name: Journey Aktivität — Akronym: none — Varianten: Aktivität, Knoten, Schritt
* Synonyme: „action activity“ = „Kanalaktion“ = „Nachrichtenaktion“
* Verwechseln Sie nicht: „Orchestrierungsaktivität“ ≠ „Aktionsaktivität“ (Orchestrierung steuert den Fluss; Aktionen liefern Kommunikation)

**FAQ:**
* **F: Was ist der Unterschied zwischen Ereignis-, Orchestrierungs- und Aktionsaktivitäten?** — Ereignisaktivitäten Trigger Journey-Eintritt oder -Fortschritt; Orchestrierungsaktivitäten steuern Verzweigungs- und Flusslogik; Aktionsaktivitäten liefern Nachrichten oder rufen externe Systeme auf.
* **F: Wie füge ich einer Journey-Aktivität einen Titel hinzu?** - Öffnen Sie den Bereich für die Aktivitätseigenschaften und füllen Sie das Feld Titel aus. Die Bezeichnung wird als Suffix unter dem Aktivitätsknoten auf der Arbeitsfläche angezeigt.
* **F: Was passiert, wenn ein Fehler in einer Aktion- oder Bedingungsaktivität auftritt?** - Die Journey des Profils wird angehalten, es sei denn, Sie aktivieren die Option „Alternativen Pfad im Falle einer Zeitüberschreitung oder eines Fehlers hinzufügen“ für diese Aktivität.
* **F: Kann ich Adobe Campaign verwenden, um Nachrichten von einer Journey zu senden?** - Ja, Journey Optimizer unterstützt die Integration mit Adobe Campaign v7/v8, Campaign Standard und Marketo Engage für das Senden von Nachrichten über benutzerdefinierte Aktionsaktivitäten.
* **F: Wie kann ich einen schreibgeschützten erweiterten Parameter einer Aktivität überschreiben?** — Klicken Sie auf das Symbol „Parameterüberschreibungen aktivieren“ rechts neben dem Parameterfeld, um einen benutzerdefinierten Wert zu erzwingen.

+++
