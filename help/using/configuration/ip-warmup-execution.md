---
solution: Journey Optimizer
product: journey optimizer
title: Ausführen des IP-Aufwärmplans
description: Erfahren Sie, wie Sie einen IP-Aufwärmplan ausführen und überwachen
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, Gruppe, Subdomains, Zustellbarkeit
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: 52021f85658fe37e5cd9b66e4e764ccc1c790b38
workflow-type: tm+mt
source-wordcount: '2730'
ht-degree: 99%

---

# Ausführen des IP-Aufwärmplans {#ip-warmup-running}

Wenn Sie [einen IP-Aufwärmplan erstellt haben](ip-warmup-plan.md) und die Datei hochgeladen haben, die Sie mit Ihren Fachleuten für Zustellbarkeit vorbereitet haben, können Sie die Phasen und Ausführungen Ihres Plans definieren.

Jede Phase besteht aus mehreren Ausführungen, denen Sie eine einzelne Kampagne zuweisen.

## Definieren der Phasen {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Ausschließen von Kampagnenzielgruppen"
>abstract="Kampagnen auswählen, um ihre Zielgruppen aus der aktuellen Phase auszuschließen. Dadurch wird verhindert, dass zuvor kontaktierte Profile erneut angesprochen werden. Es werden nur diejenigen, die Nachrichten über die Journey erhalten haben, ausgeschlossen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Ausschließen von Domain-Gruppen"
>abstract="Die Domains auswählen, die aus der aktuellen Phase ausgeschlossen werden sollen. Der Ausschluss von Domains erfordert eine nicht ausgeführte Phase, daher muss möglicherweise eine laufende Phase aufgeteilt werden, um Ausschlüsse hinzuzufügen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html?lang=de#split-phase" text="Aufspalten einer Phase"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="Definieren der Phasen Ihres Plans"
>abstract="Jede Phase besteht aus mehreren Ausführungen, denen Sie eine einzelne Kampagne zuweisen."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

Um die Phasen Ihres IP-Aufwärmplans zu definieren, müssen Sie für jede Phase eine Kampagne auswählen, Ausschlüsse für Domains und Zielgruppen konfigurieren und das Profil-Targeting verwalten. Jede Phase kann mehrere Ausführungen umfassen, die im nächsten Abschnitt konfiguriert werden. Führen Sie folgende Schritte aus:

1. Wählen Sie die Kampagne aus, die Sie mit der ersten Phase des IP-Aufwärmplans verbinden möchten.

   >[!NOTE]
   >
   >Eine Kampagne, die bereits in einem anderen IP-Aufwärmplan verwendet wird, kann nicht ausgewählt werden. Dieselbe Kampagne kann jedoch in einer oder mehreren Phasen desselben IP-Aufwärmplans verwendet werden.

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* Nur Kampagnen, für die die Option **[!UICONTROL Aktivierung des IP-Aufwärmplans]** aktiviert ist, stehen zur Auswahl zur Verfügung. [Weitere Informationen](#create-ip-warmup-campaign)
   >
   >* Zur Auswahl stehen nur Kampagnen, die dieselbe Konfiguration wie der ausgewählte IP-Aufwärmplan verwenden.

1. Sobald eine Kampagne für die aktuelle Phase ausgewählt wurde, werden die Abschnitte zum Ausschließen von Profilen, Kampagnenzielgruppen und Domain-Gruppen angezeigt.

   >[!NOTE]
   >
   >Nachdem eine Ausführung aktiviert wurde, können Ausschlüsse nur geändert werden, wenn Sie [die Ausführung in eine neue Phase aufteilen](#split-phase).

   1. Wählen Sie im Abschnitt **[!UICONTROL Ausgeschlossene Domain-Gruppen]** die Domains aus, die Sie aus der Phase ausschließen möchten.

      >[!NOTE]
      >
      >Der Ausschluss von Domains erfordert eine nicht ausgeführte Phase, daher müssen Sie möglicherweise [eine laufende Phase aufteilen](#split-phase), um Ausschlüsse hinzuzufügen.

      ![](assets/ip-warmup-plan-exclude-domains.png)

      Zum Beispiel: Sie haben einige Tage lang ein IP-Aufwärmen ausgeführt und Sie erkennen, dass Ihr ISP-Ruf bei einer Domain (z. B. Adobe) nicht gut ist. Sie möchten dies beheben, ohne Ihren IP-Aufwärmplan zu stoppen. In einem solchen Fall können Sie die Adobe-Domain-Gruppe ausschließen.

      >[!NOTE]
      >
      >Sie können nur eine benutzerdefinierte Domain-Gruppe ausschließen, die der [IP-Aufwärmplan-Vorlage](ip-warmup-plan.md#prepare-file) hinzugefügt wurde. Andernfalls müssen Sie die Vorlage mit der benutzerdefinierten Domain-Gruppe aktualisieren, die Sie ausschließen möchten, und [den Plan erneut hochladen](#re-upload-plan).

      >[!CAUTION]
      >
      >Wenn Sie nach Ausführung des IP-Aufwärmplans die [Ausführungsadresse](../email/email-settings.md#execution-address) im in der IP-Aufwärmkampagne verwendeten E-Mail-Kanal [Konfiguration](channel-surfaces.md) aktualisieren, kann der Domain-Ausschluss fehlschlagen. Bearbeiten Sie die Konfiguration des E-Mail-Kanals nicht, nachdem der IP-Aufwärmplan gestartet wurde.

   1. Wählen Sie im Abschnitt **[!UICONTROL Kampagne zum Ausschluss von Profilen]** die Kampagnen, deren Zielgruppen Sie aus der aktuellen Phase ausschließen möchten.

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      Zum Beispiel: Sie mussten bei der Ausführung von Phase 1 aus irgendeinem Grund die Phase [aufteilen](#split-phase). Daher können Sie die in Phase 1 verwendete Kampagne ausschließen, sodass die zuvor kontaktierten Profile aus Phase 1 nicht in Phase 2 eingeschlossen sind. Sie können auch Kampagnen aus anderen IP-Aufwärmplänen ausschließen.

   1. Wählen Sie im Abschnitt **[!UICONTROL Journeys zum Ausschluss von Profilen]** die Journeys mit den Zielgruppen aus, die Sie aus der aktuellen Phase ausschließen möchten.

      +++ Um die Option „Journeys zum Ausschluss von Profilen“ zu verwenden, müssen Sie eine Beziehung zwischen den Schemata „AJO Message Feedback Event“ und „AJO Entity Record“ herstellen.

      1. Erstellen Sie einen benutzerdefinierten **Namespace**, der als Identitätstyp für die folgenden Schritte dient.

      1. Greifen Sie über das Menü **Schemata** auf Adobe Experience Platform zu, wählen Sie das Schema **AJO Entity Record**, legen Sie das Feld **_id** als primäre Identität fest und wählen Sie den zuvor erstellten Namespace als **Identity-Namespace**.

      1. Wählen Sie im Menü **Schemata** das Schema **AJO Message Feedback Event** und navigieren Sie zum Feld **_messageID**. Wählen Sie **Beziehung hinzufügen** und wählen Sie das Schema **AJO Entity Record Schema** als **Referenzschema** und Ihren zuvor erstellten Namespace als **Referenz-Identity-Namespace**.
      +++

   1. Im Abschnitt **[!UICONTROL In vorherigen Ausführungen angesprochene Profile]** können Sie sehen, dass die Profile aus den früheren Durchläufen dieser Phase immer ausgeschlossen werden. Wenn beispielsweise in der Ausführung Nr. 1 ein Profil aus den ersten 4.800 angesprochenen Personen behandelt wurde, stellt das System automatisch sicher, dass dasselbe Profil die E-Mail in Ausführung Nr. 2 nicht erhält.

      >[!NOTE]
      >
      >Dieser Abschnitt kann nicht bearbeitet werden.

1. Bei Bedarf können Sie die Kampagne über die Schaltfläche **[!UICONTROL Ersetzen]** austauschen. Sie können die ausgewählte Kampagne auch über die Schaltfläche **[!UICONTROL Löschen]** **[!UICONTROL löschen]**. Mit dieser Aktion wird nicht nur die Kampagne gelöscht, sondern auch andere Eigenschaften auf Phasenebene wie Domain-Gruppenausschluss, Campaign oder Journey-Ausschluss und weitere. Nach dem Löschen können Sie entweder sofort oder zu einem späteren Zeitpunkt eine neue Kampagne auswählen.

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >Dieser Vorgang kann nur vor der ersten Ausführung der Phase ausgeführt werden. Nach der Aktivierung einer Ausführung kann die Kampagne nur ersetzt werden, wenn Sie [die Ausführung in eine neue Phase aufteilen](#split-phase).

1. Sie können bei Bedarf eine Phase hinzufügen. Sie wird nach der letzten Phase hinzugefügt.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Verwenden Sie die Schaltfläche **[!UICONTROL Phase löschen]**, um alle unerwünschten Phasen zu entfernen. Dieser Vorgang ist nur verfügbar, wenn in einer Phase keine Ausführung stattgefunden hat. <!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >Sie können die Aktion **[!UICONTROL Phase löschen]** nicht rückgängig machen.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >Wenn Sie alle Phasen aus dem IP-Aufwärmplan löschen, wird empfohlen, einen Plan erneut hochzuladen. [Weitere Informationen](#re-upload-plan)

## Definieren der Ausführungen {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="Definieren jeder Ausführung"
>abstract="Definieren und aktivieren Sie jede Auführung für alle Phasen."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="Nach Interaktion filtern"
>abstract="Diese Spalte ist ein Filter, der nur auf die Benutzerinnen und Benutzer abzielt, die beispielsweise in den letzten 20 Tagen mit Ihrer Marke interagiert haben. Sie können diese Einstellung auch über die Option **Ausführen bearbeiten** ändern."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="Festlegen eines Zeitfensters"
>abstract="Sie können ein Zeitfenster definieren, in dem die IP-Aufwärmkampagne ausgeführt werden kann, falls sich der Segmentierungsauftrag verzögert."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="Ausführungen mit Zielgruppenfehlern abbrechen"
>abstract="Wählen Sie diese Option, um eine Ausführung abzubrechen, wenn die qualifizierten Profile weniger sind als die angesprochenen Zielgruppenprofile, sobald die Zielgruppe für diese Ausführung ausgewertet wurde."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="Anzeigen der qualifizierten Profile"
>abstract="In dieser Spalte wird die Anzahl der qualifizierten Profile angezeigt. Wenn die Zielgruppe für eine Ausführung ausgewertet wurde und mehr angesprochene als qualifizierte Profile vorhanden sind, wird die Ausführung weiterhin durchgeführt, es sei denn, die Option **Aktivierte Ausführungen im Falle von Fehlern abbrechen** ist aktiviert. In diesem Fall wird die Ausführung abgebrochen."

Nachdem Sie die Phasen Ihres IP-Aufwärmplans definiert haben, müssen Sie die einzelnen Ausführungen innerhalb jeder Phase konfigurieren. Jede Ausführung erfordert einen Zeitplan und Sie können optional Interaktionsfilter, Fehlerbehandlung und Wiederholungsfenster konfigurieren, um eine optimale Ausführung sicherzustellen. Führen Sie folgende Schritte aus:

1. Wählen Sie für jede Ausführung einen Zeitplan aus, um sicherzustellen, dass sie zum angegebenen Zeitpunkt durchgeführt wird.

   ![](assets/ip-warmup-plan-send-time.png)

1. Optional können Sie ein Zeitfenster definieren, in dem die IP-Aufwärmkampagne ausgeführt werden kann, falls sich die [Zielgruppenauswertung](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de#how-segmentation-works){target="_blank"} verzögert. Klicken Sie dazu auf das Symbol „Eigenschaften“ oben links neben dem Namen des Plans und verwenden Sie die Dropdown-Liste **[!UICONTROL Zeit bis zum nächsten Versuch der Ausführung]**, um eine Dauer auszuwählen – bis zu 240 Minuten (4 Stunden).

   >[!NOTE]
   >
   >Weitere Zustellversuche werden alle 30 Minuten bis zum Ende des definierten Zeitfensters durchgeführt.

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Wenn Sie beispielsweise eine Sendezeit für einen bestimmten Tag auf 9:00 Uhr und als Wartezeit für einen erneuten Versuch 120 Minuten festlegen, können Sie bei unerwarteten Verzögerungen bei der Zielgruppenbewertung ein Zeitfenster von 2 Stunden (9:00 – 11:00 Uhr) für die Ausführung nutzen.

   >[!NOTE]
   >
   >Wenn kein Zeitfenster angegeben ist, wird die Ausführung zum Versandzeitpunkt gestartet und schlägt fehl, falls die Bewertung der Zielgruppe nicht abgeschlossen ist.

1. Wählen Sie bei Bedarf **[!UICONTROL Ausführen bearbeiten]** über das Symbol „Mehr Aktionen“ aus. Dort können Sie die Anzahl der Adressen in jeder Spalte aktualisieren. Sie können auch das Feld **[!UICONTROL Letzte Interaktion]** aktualisieren, um beispielsweise nur die Benutzerinnen und Benutzer anzusprechen, die in den letzten 20 Tagen mit Ihrer Marke interagiert haben.

   >[!NOTE]
   >
   >Es wird empfohlen, diese Zahlen in Absprache mit Ihrer Zustellbarkeitsfachkraft zu ändern.

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >Wenn Sie auf eine Ausführung keinen Interaktionszeitraum anwenden möchten, geben Sie 0 in das Feld **[!UICONTROL Letzte Interaktion]** ein.

1. Wählen Sie die Option **[!UICONTROL Aktivierte Ausführungen im Fall von Fehlern abbrechen]** aus, um eine Ausführung abzubrechen, wenn es weniger qualifizierte Profile als Zielgruppenprofile gibt, nachdem die Zielgruppe für diese Ausführung ausgewertet wurde.

   ![](assets/ip-warmup-plan-pause.png)

   Sollte die Anzahl der qualifizierten Profile nicht mit der Anzahl der Zielgruppenprofile übereinstimmen (z. B. werden 1.500 Gmail-Adressen in der Ausführung angesprochen, es gibt jedoch nur 700 qualifizierte Gmail-Profile):

   * Wenn die Option aktiviert ist, schlägt die Ausführung fehl und die Ausführung erhält den Status **[!UICONTROL Fehlgeschlagen]**. <!--You can then either choose to target less profiles in the next run, or to [split the run](#split-phase) to a new phase and select a new campaign for the new phase to target the same profiles again.-->

   * Wenn die Option nicht aktiviert ist, findet die Ausführung statt, es wird jedoch nur die verfügbare Anzahl von Profilen angesprochen.

1. **[!UICONTROL Aktivieren]** Sie die Ausführung. [Weitere Informationen](#activate-run)

1. Der Status dieser Ausführung ändert sich in **[!UICONTROL Live]**, was bedeutet, dass das System die Anfrage zur Planung der Ausführung akzeptiert hat.

   >[!NOTE]
   >
   >Die verschiedenen Ausführungsstatus werden in [diesem Abschnitt](#monitor-plan) aufgeführt.

1. Wenn die Ausführung der Kampagne noch nicht gestartet wurde, können Sie eine Live-Ausführung abbrechen. Mit dieser Aktion wird der Ausführungsplan abgebrochen, der Versand jedoch nicht gestoppt.

   ![](assets/ip-warmup-plan-stop-run.png)

1. Um einen Entwurf, eine Live- oder eine abgeschlossene Ausführung zu duplizieren, wählen Sie **[!UICONTROL Ausführung duplizieren]**. Nach der Duplizierung erscheint das Menü „Ausführung bearbeiten“, in dem Sie die **[!UICONTROL Gesamtzahl der Zielgruppenprofile]** und die **[!UICONTROL Versandzeit]** nach Bedarf anpassen können.

   ![](assets/ip-warmup-duplicate.png)

## Aktivieren von Ausführungen {#activate-run}

Um eine Ausführung zu aktivieren, wählen Sie die Schaltfläche **[!UICONTROL Aktivieren]** aus. Dann können Sie die nächsten Ausführungen täglich aktivieren.

Wenn Sie mehrere IP-Aufwärmpläne gleichzeitig ausführen, die alle auf denselben IP-Pool und dieselben Domains abzielen, ist es entscheidend, die potenziellen Auswirkungen vorherzusehen. Wenn beispielsweise ein ISP eine tägliche Beschränkung von 100 E-Mails durchsetzt, könnte die Ausführung mehrerer Pläne, die auf dieselben Domains abzielen, diesen Schwellenwert überschreiten.

Achten Sie darauf, dass Sie ausreichend Zeit für die Ausführung der [Zielgruppenauswertung](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=de#how-segmentation-works){target="_blank"} eingeplant haben.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>Jeder Durchlauf muss mindestens 12 Stunden vor der tatsächlichen Versandzeit und vor dem täglichen Batch-Segmentierungsauftrag aktiviert werden. Andernfalls kann die Zielgruppenbewertung möglicherweise nicht abgeschlossen werden.

Wenn Sie eine Ausführung aktivieren, werden automatisch mehrere Zielgruppen erstellt.

* Wenn Sie die erste Ausführung einer Phase aktivieren:

   * Es wird eine [Zielgruppe](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de){target="_blank"} für die ausgeschlossenen Kampagnenzielgruppen (sofern vorhanden) mit folgender Namenskonvention erstellt: `<warmupName>-Phase<phaseNo>-Audience Exclusion`.

   * Eine Zielgruppe wird für die ausgeschlossenen Domain-Gruppen (sofern vorhanden) mit folgender Namenskonvention erstellt: `<warmupName>-Phase<phaseNo>-Domain Exclusion`.

   * Es wird eine weitere Zielgruppe für die ausgeschlossenen Journey-Zielgruppen (sofern vorhanden) mit folgender Namenskonvention erstellt: `<warmupName>-Phase<phaseNo>-Journey Audience Exclusion`.

  >[!NOTE]
  >
  >Die Zielgruppen werden bereinigt, nachdem der Aufwärmplan als abgeschlossen markiert wurde.
  >
  >Das System erstellt keine neue Zielgruppe, wenn sich die ausgeschlossenen Kampagnenzielgruppen, ausgeschlossenen Journey-Zielgruppen oder Domain-Gruppen in den nachfolgenden Phasen nicht ändern.

* Beim Aktivieren einer Ausführung:

   * Für den letzten Interaktionsfilter wird eine weitere Zielgruppe mit folgender Namenskonvention erstellt: `<warmupName>-Phase<phaseNo>_Run<runNo>-Engagement Filter`.

     >[!NOTE]
     >
     >Die Zielgruppe wird bereinigt, nachdem der Aufwärmplan als abgeschlossen markiert wurde.
     >
     >Das System erstellt keine neue Zielgruppe, wenn sich der letzte Interaktionsfilter in den nachfolgenden Phasen nicht ändert.

   * Entsprechend der Zielgruppe, an die die Kampagne gesendet wird, wird eine [Zielgruppenkomposition](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=de){target="_blank"} mit folgender Namenskonvention erstellt: `<warmupName>-Phase<phaseNo>-Run<runNo>`.

     >[!NOTE]
     >
     >Für jede Ausführung wird eine neue Zielgruppenkomposition erstellt. Bei einem Limit von 10 müssen Benutzende, die mehrere Kampagnen, Journeys und IP-Aufwärmpläne gleichzeitig ausführen und dabei veröffentlichte Zielgruppenkompositionen verwenden, im Voraus planen, um dieses Limit für parallele Vorgänge einzuhalten.
     >
     >Die Zielgruppenkomposition (und damit die Ausgabe-Zielgruppe) wird bei der Aktivierung der nächsten Iteration bereinigt.

   * Eine Ausgabe-Zielgruppe wird mit der folgenden Namenskonvention erstellt: `IP Warmup Audience-<warmupName>-Phase<phaseNo>-Run<runNo>`.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## Überwachen des Plans {#monitor-plan}

Um Ihren IP-Aufwärmplan erfolgreich ausführen zu können, müssen Sie die Berichte überwachen, die Ausführungen aktivieren und ihren Status täglich überprüfen.

### Arbeiten mit dem Abschnitt „Hervorhebungen“ {#highlights}

Sobald die erste Ausführung einer Phase aktiviert wurde, wird der Abschnitt **[!UICONTROL Hervorhebungen]** angezeigt.

Er bietet einen schnellen Überblick über die aktuelle und die bevorstehende Ausführung. In diesem Abschnitt können Sie auch die nächste Ausführung bearbeiten und aktivieren.

![](assets/ip-warmup-plan-highlights.png)

### Überprüfen des Ausführungsstatus {#run-statuses}

Der IP-Aufwärmplan selbst dient auch als zentraler konsolidierter Bericht. Sie können Elemente wie die Anzahl der **[!UICONTROL Live]**- oder **[!UICONTROL abgeschlossenen]** Ausführungen für jede Phase überprüfen und anzeigen, wie der IP-Aufwärmplan voranschreitet.

>[!NOTE]
>
>Als Best Practice wird empfohlen, Ihren IP-Aufwärmplan täglich zu überwachen.

Eine Ausführung kann folgende Status haben:

* **[!UICONTROL Entwurf]** : Sobald eine Ausführung erstellt wurde, entweder durch [Einen neuen Plan erstellen](ip-warmup-plan.md) oder durch [Einen Vorgang hinzufügen](#define-runs) von der Benutzeroberfläche aus, erhält sie den Status **[!UICONTROL Entwurf]**.
* **[!UICONTROL Live]**: Sobald eine Ausführung aktiviert wurde, erhält sie den Status **[!UICONTROL Live]**. Das bedeutet, dass das System die Anfrage zur Planung der Ausführung akzeptiert hat, aber nicht, dass der Versand gestartet wurde. In dieser Phase können Sie den Status der Live- Ausführung beobachten, indem Sie in der Tabelle auf die Schaltfläche **[!UICONTROL Status anzeigen]** klicken. Auf diese Weise können Sie verfolgen, wie viele Zielgruppenprofile sich tatsächlich qualifiziert haben.
* **[!UICONTROL Abgeschlossen]**: Die Kampagnenausführung für diesen Durchlauf ist abgeschlossen. Sie können einen detaillierten Ausführungsbericht aufrufen, indem Sie in der Tabelle auf die Schaltfläche **[!UICONTROL Bericht anzeigen]** klicken. Mit dieser Option können Sie den E-Mail-Versandstatus des Vorgangs verfolgen, einschließlich Aufschlüsselungen speziell für Domain-Gruppen, um die Überwachung zu verbessern. Beachten Sie, dass die damit verknüpfte Kampagne als „Gestoppt“ festgelegt wird.[Weitere Informationen](#reports)
* **[!UICONTROL Abgebrochen]**: Eine **[!UICONTROL Live]**-Ausführung wurde mit der Schaltfläche **[!UICONTROL Abbrechen]** abgebrochen. [Weitere Informationen](#define-runs)
* **[!UICONTROL Fehlgeschlagen]**: Beim System ist ein Fehler aufgetreten, oder die für die aktuelle Phase verwendete Kampagne wurde gestoppt oder Sie haben die Option **[!UICONTROL Aktivierte Ausführungen im Falle von Fehlern abbrechen]** aktiviert und ein Fehler ist aufgetreten. Wenn eine Ausführung fehlschlägt, können Sie eine weitere Ausführung für den nächsten Tag planen.

### Arbeiten mit Berichten {#reports}

Ganz allgemein können Sie die Auswirkung Ihres Plans messen, indem Sie die Performance Ihrer IP-Aufwärmkampagnen mithilfe der [!DNL Journey Optimizer]-Kampagnenberichte überprüfen. Dazu können Sie für jede abgeschlossene Ausführung auf die Schaltfläche **[!UICONTROL Berichte anzeigen]** klicken. Erfahren Sie mehr über den [Live-Bericht](../reports/campaign-live-report.md#email-live) und den [Customer Journey Analytics-Bericht](../reports/campaign-global-report-cja-email.md) zu Kampagnen-E-Mails.

![](assets/ip-warmup-plan-reports.png)

Sie können auf die Berichte auch über das [Kampagnen-Menü](../campaigns/manage-campaigns.md#access) zugreifen, da Ihr Plan möglicherweise unterschiedliche Kampagnen beinhaltet.


## Verwalten Ihres Plans {#manage-plan}

Wenn Ihr IP-Aufwärmplan nicht die erwartete Leistung erzielt, können Sie die folgenden Maßnahmen ergreifen.

### Aufspalten einer Phase {#split-phase}

Wenn Sie eine neue Phase hinzufügen möchten, die ab einer bestimmten Ausführung beginnt, wählen Sie die Option **[!UICONTROL Ausführungen in neue Phase aufteilen]** über das Symbol „Weitere Aktionen“ aus.

![](assets/ip-warmup-plan-run-split-run.png)

Für die verbleibenden Ausführungen der aktuellen Phase wird eine neue Phase erstellt.

Wenn Sie beispielsweise diese Option für die Ausführung Nr. 4 auswählen, werden die Ausführungen Nr. 4 bis 8 direkt nach der aktuellen Phase in eine neue Phase verschoben.

Führen Sie die [obigen](#define-phases) Schritte aus, um die neue Phase zu definieren.

* Sie können für diese neue Phase die Optionen **[!UICONTROL Ersetzen]** oder **[!UICONTROL Löschen]** verwenden.

* Sie können auch die vorherige Kampagne oder eine Domain ausschließen, die nicht gut abschneidet. Mehr dazu erfahren Sie in [diesem Abschnitt](#define-phases).

<!--
You do not have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Erneutes Hochladen eines IP-Aufwärmplans {#re-upload-plan}

Wenn der IP-Aufwärmplan nicht wie erwartet funktioniert (z. B. wenn Sie feststellen, dass einige ISPs Ihre Nachrichten als Spam markieren), können Sie eine Fachkraft für Zustellbarkeit bitten, eine weitere IP-Aufwärmplan-Datei einzurichten und sie über die entsprechende Schaltfläche erneut hochzuladen.

![](assets/ip-warmup-re-upload-plan.png)

Alle zuvor ausgeführten Ausführungen sind schreibgeschützt. Der neue Plan wird im ersten Plan dargestellt.

Führen Sie die Schritte [oben](#define-phases) aus, um die Phasen des neuen Plans zu definieren.

>[!NOTE]
>
>Die Details des IP-Aufwärmplans ändern sich entsprechend der neu hochgeladenen Datei. Die zuvor ausgeführten Ausführungen (unabhängig von deren [Status](#monitor-plan)) sind nicht betroffen.

Nehmen wir ein Beispiel:

* Im ursprünglichen IP-Aufwärmplan hatte Phase 2 neun Ausführungen.

* Es gab vier Ausführungen (unabhängig davon, ob fehlgeschlagen, abgeschlossen oder abgebrochen<!--as long as a run has been attempted, it is an executed run-->).

* Wenn ein neuer Plan erneut hochgeladen wird, wird Phase 2 mit den ersten vier ausgeführten Läufen in den schreibgeschützten Modus versetzt.

* Die verbleibenden fünf Ausführungen (die sich im Entwurfsstatus befinden) werden in eine neue Phase (Phase 3) verschoben, die gemäß dem neu hochgeladenen Plan angezeigt wird.

### Markieren eines Plans als abgeschlossen {#mark-as-completed}

Wenn Ihre IPs mit dem gewünschten Volumen aufgewärmt wurden, das Ergebnis Ihres Plans nicht gut genug ist oder wenn Sie einen anderen Plan erstellen möchten, können Sie ihn als abgeschlossen markieren.

Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Mehr]** oben rechts im IP-Aufwärmplan und wählen Sie **[!UICONTROL Als abgeschlossen markieren]** aus.

![](assets/ip-warmup-plan-mark-completed.png)

Diese Option ist nur verfügbar, wenn sich alle im Plan ausgeführten Ausführungen im Status **[!UICONTROL Abgeschlossen]** oder **[!UICONTROL Entwurf]** befinden. Wenn eine Ausführung **[!UICONTROL Live]** ist, ist die Option ausgegraut.

Die verschiedenen Ausführungsstatus werden in [diesem Abschnitt](#monitor-plan) aufgeführt.

