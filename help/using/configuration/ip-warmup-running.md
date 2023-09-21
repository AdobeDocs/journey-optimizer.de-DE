---
solution: Journey Optimizer
product: journey optimizer
title: IP-Warmup-Plan ausführen
description: Erfahren Sie, wie Sie einen IP-Warmup-Plan ausführen und überwachen.
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, Pools, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 1%

---

# IP-Warmup-Plan ausführen {#ip-warmup-running}

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* [Erste Schritte mit IP-Wärme](ip-warmup-gs.md)
* [Erstellen von IP-Aufwärmekampagnen](ip-warmup-campaign.md)
* [Erstellen eines IP-Warmup-Plans](ip-warmup-plan.md)
* **[IP-Warmup-Plan ausführen](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## Definieren der Phasen {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Auswahl der auszuschließenden Kampagnenzielgruppen"
>abstract="Wählen Sie die Zielgruppen aus anderen Kampagnen aus, die Sie aus der aktuellen Phase ausschließen möchten."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Auswählen von Domänengruppen zum Ausschließen"
>abstract="Wählen Sie die Domänen aus, die Sie aus der aktuellen Phase ausschließen möchten."

Sie müssen die Kampagne und die Zielgruppe auf Phasenebene verknüpfen und aktivieren einige Einstellungen, die für alle mit einer einzelnen Kreativ-/Kampagne verbundenen Ausführungen erforderlich sind

Auf Phasenebene stellt das System sicher, dass zuvor angesprochene + neue Profile abgerufen werden UND auf Iterationsebene, das System stellt sicher, dass jeder Lauf eindeutige Profile hat und die Anzahl mit der im Plan angegebenen übereinstimmt

1. Wählen Sie für jede Phase die Kampagne aus, die Sie mit dieser Phase des IP-Aufwärmungsplans verbinden möchten.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Beachten Sie Folgendes:

   * Nur Kampagnen mit der **[!UICONTROL Aktivierung des IP-Warmlaufplans]** Option aktiviert <!--and live?--> stehen zur Auswahl zur Verfügung. [Weitere Informationen](#create-ip-warmup-campaign)

   * Sie müssen eine Kampagne auswählen, die dieselbe Oberfläche wie die für den aktuellen IP-Aufwärmplan ausgewählte verwendet.

   * Es ist nicht möglich, eine Kampagne auszuwählen, die bereits in einer anderen IP-Warmup-Kampagne verwendet wird.

1. Für jede Phase gilt Folgendes:

   * **[!UICONTROL Profilausschluss]** - Die Profile aus den vorherigen Ausführungen dieser Phase werden immer ausgeschlossen. Wenn beispielsweise Leo beim Ausführen von #1 in den ersten 6300 Personen, die angesprochen werden, behandelt wurde, stellt das System automatisch sicher, dass Leo die E-Mail nicht in Ausführung Nr. 2 erhält.

   * **[!UICONTROL Campaign-Zielgruppen ausgeschlossen]** - Wählen Sie die Zielgruppen aus anderen <!--executed/live?-->Kampagnen, die Sie aus der aktuellen Phase ausschließen möchten.

     Beispielsweise können Sie eine Phase ausführen, die aus jedem Grund geteilt werden musste. In diesem Fall möchten Sie in Phase 2 die in Phase 1 verwendete Kampagne in diesen Abschnitt aufnehmen, damit zuvor kontaktierte Personen aus Phase 1 in Phase 2 nicht einbezogen werden. Dies kann nicht nur mit Kampagnen erfolgen, die im selben IP-Warmup-Plan verwendet werden, sondern auch mit einem anderen IP-Warmup-Plan.

   * **[!UICONTROL Domänengruppen ausgeschlossen]** - Wählen Sie die Domänen aus, die Sie von dieser Phase ausschließen möchten, z. B. Gmail. <!--??-->

     Nachdem Sie einige Tage lang IP-Warmup ausgeführt haben, erkennen Sie, dass der ISP-Ruf bei einer Domain sagt, dass Hotmail nicht gut ist und Sie es mit ISP lösen möchten, aber nicht den IP-Warmup-Plan stoppen möchten. In einem solchen Fall können Sie die Domain-Gruppe Hotmail in die ausgeschlossene Kategorie setzen.

     >[!NOTE]
     >
     >Der Domänenausschluss erfordert eine nicht ausgeführte Phase, daher müssen Sie möglicherweise eine laufende Phase aufteilen, um Ausnahmen hinzuzufügen. Gleichermaßen müssen Sie, wenn die Domain-Gruppe keine OOTB-Domänengruppe ist, in Excel eine Domänengruppe erstellen und diese dann hochladen und ausschließen.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Sie können bei Bedarf eine Phase hinzufügen. Diese wird nach der letzten aktuellen Phase hinzugefügt. Verwenden Sie die **[!UICONTROL Löschphase]** -Schaltfläche, um alle unerwünschten Phasen zu entfernen.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >Sie können die **[!UICONTROL Löschen]** Aktion.
   >
   >Wenn Sie alle Phasen aus dem IP-Warmup-Plan löschen, empfehlen wir, einen Plan erneut hochzuladen.

## Definieren der Ausführungen {#define-runs}

1. Wählen Sie für jeden Lauf einen Zeitplan aus. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Wählen Sie eine Endzeit aus, d. h. im Grunde das Fenster, in dem wir eine Warmup-Kampagne ausführen können, falls es zu Verzögerungen bei der Ausführung des Audience-Auftrags kommt. Wenn nichts angegeben wird, versuchen wir es zur Startzeit und schlagen fehl. Wenn die Endzeit angegeben ist, wird die Ausführung zwischen diesem Fenster ausgeführt.

1. Aktivieren Sie jeden Lauf. Stellen Sie sicher, dass Sie eine Zeit so früh planen, dass der Segmentierungsauftrag ausgeführt werden kann. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Jede Ausführung muss mindestens 12 Stunden vor der tatsächlichen Versandzeit aktiviert werden. Andernfalls kann die Segmentierung nicht abgeschlossen sein. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Wenn die Kampagnenausführung noch nicht gestartet wurde, können Sie den Start stoppen.<!--why?-->

   Sobald die Kampagnenausführung gestartet wurde, wird die **[!UICONTROL Anhalten]** -Schaltfläche nicht mehr verfügbar. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Um eine Ausführung hinzuzufügen, wählen Sie **[!UICONTROL Hinzufügen einer Ausführung unten]** über das Symbol mit den drei Punkten aus.

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. Wenn Sie jederzeit eine andere Kampagne verwenden möchten, die von einem bestimmten Lauf ausgehend beginnt, wählen Sie die **[!UICONTROL Option &quot;In neue Phase aufteilen&quot;]** über das Symbol mit den drei Punkten aus. Für die verbleibenden Phasen der aktuellen Phase wird eine neue Phase erstellt. Führen Sie die Schritte aus [above](#define-phases) , um die neue Phase zu definieren.

   Wenn Sie beispielsweise diese Option für die Ausführung Nr. 4 auswählen, werden die Ausführungen Nr. 4 bis Nr. 8 in eine neue Phase verschoben.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Plan überwachen

Eine Ausführung kann die folgenden Status haben:<!--TBC with Medha-->:

* **[!UICONTROL Abgeschlossen]**:
* **[!UICONTROL Fehlgeschlagen]**:
* **[!UICONTROL Abgebrochen]**: Sie haben die Ausführung angehalten, bevor die Kampagnenausführung gestartet wurde.

Vorteile :

* Berichte werden weiterhin auf Kampagnenebene mit ähnlichen Funktionen wie heute angezeigt. Aber der IP-Aufwärtsplan dient auch als konsolidierter Bericht an einem einzigen Ort, an dem festgestellt wird, wie viele Hinrichtungen durchgeführt wurden und so weiter.

* Zentraler Ort, um zu verwalten und zu sehen, wie IP-Warm geht.

* Konsolidierter Bericht auf Kreativ-/Kampagnenebene, da alle für eine Phase ausgeführt werden