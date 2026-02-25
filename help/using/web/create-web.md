---
title: Erstellen von Web-Erlebnissen
description: Erfahren Sie, wie Sie in Journey Optimizer eine Web-Seite erstellen und ihren Inhalt bearbeiten
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 91%

---

# Erstellen von Web-Erlebnissen {#create-web}

[!DNL Journey Optimizer] ermöglicht es Ihnen, das Web-Erlebnis, das Sie Ihrer Kundschaft bieten, durch eingehende Journeys oder Kampagnen zu personalisieren.

## Definieren eines Web-Erlebnisses über eine Journey oder eine Kampagne {#create-web-experience}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definieren einer Web-Konfiguration"
>abstract="Eine Web-Konfiguration kann einer einzelnen Seiten-URL oder mehreren Seiten entsprechen, sodass inhaltliche Änderungen auf einer oder mehreren Web-Seiten vorgenommen werden können."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Erstellen einer Regel zum Seitenabgleich"
>abstract="Eine Regel zum Seitenabgleich macht es möglich, mehrere URLs, die derselben Regel entsprechen, als Ziel auszuwählen. Dies ist zum Beispiel praktisch, wenn die Änderungen an einem Hero Banner auf einer ganzen Website angewendet oder oben ein Bild hinzugefügt werden soll, das auf allen Produktseiten einer Website angezeigt wird."

Um mit dem Aufbau Ihres Web-Erlebnisses über eine Kampagne oder eine Journey zu beginnen, folgen Sie den nachstehenden Schritten.

>[!NOTE]
>
>Wenn Sie zum ersten Mal ein Web-Erlebnis erstellen, stellen Sie sicher, dass Sie die in [diesem Abschnitt](web-prerequisites.md) beschriebenen Voraussetzungen befolgen.

>[!BEGINTABS]

>[!TAB Hinzufügen eines Web-Erlebnisses zu einer Journey]

Um einer Journey eine Aktivität **Web** hinzuzufügen, gehen Sie folgendermaßen vor:

1. [Erstellen einer Journey](../building-journeys/journey-gs.md)

1. Beginnen Sie Ihre Journey mit einem [Ereignis](../building-journeys/general-events.md) oder einer Aktivität vom Typ [Zielgruppe lesen](../building-journeys/read-audience.md).

1. Ziehen Sie eine Aktivität **[!UICONTROL Aktion]** per Drag-and-Drop aus dem Abschnitt **[!UICONTROL Aktionen]** der Palette. Weitere Informationen über die [Aktionsaktivität](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Da nun über die Aktivität Aktion auf alle nativen Kanäle zugegriffen werden kann, werden alte native Kanalaktivitäten mit der März-Version eingestellt. Vorhandene Journey mit Legacy-Aktionen funktionieren weiterhin wie bisher - es ist keine Migration erforderlich.

1. Wählen **[!UICONTROL als]** „Web“ aus.

   ![](assets/web-activity-journey.png)

   >[!NOTE]
   >
   >Da es sich bei **Web** um eine Aktivität für eingehende Erlebnisse handelt, geht sie mit einer 3-tägigen **Warteaktivität** einher. [Weitere Informationen](../building-journeys/wait-activity.md#auto-wait-node)

1. Geben Sie einen **[!UICONTROL Titel]** ein, um Ihre Aktion auf der Journey-Arbeitsfläche zu identifizieren.

1. Klicken Sie auf **[!UICONTROL Schaltfläche „Aktion konfigurieren]**.

1. Sie werden zur Registerkarte **[!UICONTROL Aktionen]** geleitet. Wählen oder erstellen Sie dort die [Web-Konfiguration](web-configuration.md) die verwendet werden soll.

   ![](assets/web-activity-configuration.png)

1. Sie können eine oder mehrere eingehende Aktionen zu Ihrem Web-Erlebnis hinzufügen, indem Sie auf die Schaltfläche **[!UICONTROL Aktion hinzufügen]** klicken. [Weitere Informationen](../building-journeys/journey-action.md#multi-action)

1. Zurück zur Journey-Arbeitsfläche. Schließen Sie bei Bedarf Ihren Journey-Fluss ab, indem Sie zusätzliche Aktionen oder Ereignisse per Drag-and-Drop verschieben. [Weitere Informationen](../building-journeys/about-journey-activities.md)

1. Wählen Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** und bearbeiten Sie Ihren Inhalt wie gewünscht. [Weitere Informationen](#edit-web-content)

Weitere Informationen zum Erstellen, Konfigurieren und Veröffentlichen einer Journey finden Sie auf [dieser Seite](../building-journeys/journey-gs.md).

>[!TAB Erstellen einer Web-Kampagne]

Gehen Sie wie folgt vor, um mit der Erstellung Ihres Web-Erlebnisses durch eine Kampagne zu beginnen.

1. Erstellen einer Kampagne. [Weitere Informationen](../campaigns/create-campaign.md)

1. Wählen Sie den Typ der Kampagne aus, die Sie ausführen möchten.

   * **Geplant – Marketing**: die Kampagne wird sofort oder an einem bestimmten Datum ausgeführt. Geplante Kampagnen dienen dem Versand von Marketing-Nachrichten. Sie werden über die Benutzeroberfläche konfiguriert und ausgeführt.

   * **API-ausgelöst – Marketing/Transaktion**: die Kampagne wird mithilfe eines API-Aufrufs ausgeführt.  API-ausgelöste Kampagnen zielen auf den Versand von Nachrichten des Typs „Marketing“ oder „Transaktion“ ab. Beim Typ „Transaktion“ handelt es sich um Nachrichten, die nach einer von einem Kontakt durchgeführten Aktion verschickt werden: Zurücksetzen des Passworts und Verlassen des Warenkorbs. [Erfahren Sie, wie Sie eine Kampagne mithilfe von APIs auslösen](../campaigns/api-triggered-campaigns.md)

1. Führen Sie die Schritte zur Erstellung einer Web-Kampagne aus, z. B. die Kampagneneigenschaften, [Zielgruppe](../audience/about-audiences.md) und [Zeitplan](../campaigns/create-campaign.md#schedule).

1. Wählen Sie die Aktion **[!UICONTROL Web]**.

1. Wählen oder erstellen Sie die Web-Konfiguration. [Weitere Informationen zur Web-Konfiguration](web-configuration.md)

   ![](assets/web-campaign-steps.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt bearbeiten]**, um Ihren Inhalt wie gewünscht zu bearbeiten. [Weitere Informationen](#edit-web-content)

   <!--![](assets/web-campaign-edit-content.png)-->

Weitere Informationen zur Konfiguration Ihrer Kampagne finden Sie auf [dieser Seite](../campaigns/get-started-with-campaigns.md).

➡️ [In diesem Video erfahren Sie, wie Sie eine Web-Kampagne erstellen.](#video)

>[!ENDTABS]

## Bearbeiten von Web-Inhalten {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Bestätigen der URL zum Bearbeiten"
>abstract="Bestätigen Sie die URL der spezifischen Web-Seite, die für die Bearbeitung des Inhalts verwendet werden soll, welcher auf die oben definierte Web-Konfiguration angewendet wird. Die Web-Seite muss mithilfe des Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Geben Sie die zu bearbeitende URL ein"
>abstract="Geben Sie die URL einer bestimmten Web-Seite ein, die zum Bearbeiten des Inhalts verwendet werden soll. Sie wird auf alle Seiten angewendet, die der Regel entsprechen. Die Web-Seite muss mithilfe des Adobe Experience Platform Web SDK implementiert werden."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=de" text="Weitere Informationen"

Sobald Sie einer Journey oder einer Kampagne eine [Web-Aktion hinzugefügt haben](#create-web-experience), können Sie den Inhalt Ihrer Site mit einer der beiden Optionen bearbeiten:

* dem [Web-Designer](web-visual-editor.md), um Ihr Erlebnis mit einem visuellen Editor zu erstellen,
* oder dem [nicht visuellen Editor](web-non-visual-editor.md).

Gehen Sie wie folgt vor, um mit der Erstellung Ihres Web-Erlebnisses zu beginnen.

1. Wählen Sie auf der Registerkarte **[!UICONTROL Aktion]** der Kampagne oder über die **[!UICONTROL Web]**-Aktivität in der Journey die Option **[!UICONTROL Inhalt bearbeiten]** aus.

   ![](assets/web-campaign-edit-content.png)

1. Der Bearbeitungsbildschirm wird angezeigt.  Sie haben folgende Möglichkeiten:

   * Klicken Sie auf die Schaltfläche **[!UICONTROL Web-Seite bearbeiten]**, um mit der Bearbeitung Ihres Inhalts mit dem Web-Designer für ein visuelles Erlebnis zu beginnen. [Weitere Informationen](web-visual-editor.md)

     ![](assets/web-campaign-edit-web-page.png)

   * Heben Sie die Auswahl für die Option **[!UICONTROL Visueller Editor]** auf, um stattdessen den nicht visuellen Bearbeitungsmodus zu verwenden, und klicken Sie auf **[!UICONTROL Eine Änderung hinzufügen]**, um mit der Bearbeitung des Web-Inhalts zu beginnen, ohne den visuellen Editor zu laden. [Weitere Informationen](web-non-visual-editor.md)

     ![](assets/web-campaign-add-modification.png)

## Testen des Web-Erlebnisses {#test-web-experience}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Vorschau des Web-Erlebnisses"
>abstract="Betrachten Sie in einer Simulation, wie Ihr Web-Erlebnis aussehen wird."

Sobald Sie mit dem Web-Designer [das Web-Erlebnis erstellt haben](web-visual-editor.md), können Sie mithilfe der Testprofile eine Vorschau der geänderten Web-Seiten anzeigen. Wenn Sie personalisierte Inhalte eingefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie diese Inhalte angezeigt werden.

Klicken Sie dazu entweder im Bildschirm zur Inhaltsbearbeitung einer Journey oder einer Kampagne auf **[!UICONTROL Inhalt simulieren]** und fügen Sie dann ein Testprofil hinzu, um Ihre Web-Seite mithilfe der Testprofildaten zu überprüfen.

![](assets/web-designer-preview.png)

Sie können sie auch im Standard-Browser öffnen oder die Test-URL kopieren, um sie in einen beliebigen Browser einzufügen. Auf diese Weise können Sie den Link für Ihr Team und Ihre Interessensgruppen freigeben, damit sie in der Lage sind, das neue Web-Erlebnis in einem beliebigen Browser in der Vorschau zu betrachten, bevor die Kampagne live geschaltet wird.

>[!NOTE]
>
>Beim Kopieren der Test-URL ist der angezeigte Inhalt derjenige, der für das Testprofil personalisiert wurde, das zum Zeitpunkt der Erstellung der Inhaltsimulation in [!DNL Journey Optimizer] verwendet wurde.

Detaillierte Informationen zur Auswahl von Testprofilen und zur Vorschau Ihres Inhalts finden Sie im Abschnitt [Content-Management](../content-management/preview-test.md).

## Umleiten zu einer URL {#web-redirect-to-url}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_redirect"
>title="Umleiten zu einer anderen URL"
>abstract="Geben Sie eine vorhandene URL ein, zu der die Besuchenden Ihrer Seite weitergeleitet werden sollen."

Beim Erstellen eines Web-Erlebnisses können Sie Besuchende zu einer anderen vorhandenen URL umleiten, anstatt eine neue Variante im Web-Designer zu erstellen.

Mit dieser Kapazität können Sie ein [Inhaltsexperiment](../content-management/content-experiment.md) ausführen, bei dem zwei verschiedene Erlebnisse verglichen werden und nicht nur einige Elemente innerhalb einer Seite geändert werden.

Erstellen Sie beispielsweise eine Web-Kampagne mit zwei Abwandlungen:

* Erstellen Sie in **Abwandlung A** ein Web-Erlebnis mit dem Web-Designer für die Hälfte Ihrer Zielpopulation.

* Wählen Sie in **Abwandlung B** die Option **[!UICONTROL Zu URL umleiten]** für die andere Hälfte der Zielpopulation aus. Geben Sie die URL einer Seite mit einem alternativen Design ein, das Sie außerhalb von [!DNL Journey Optimizer] erstellt haben.

  ![](assets/web-campaign-redirect-to-url.png)

  >[!NOTE]
  >
  >Die Website-Vorschau wird nicht mehr angezeigt und der Umschalter **[!UICONTROL Visueller Editor]** ist deaktiviert.

Sobald Ihre Web-Kampagne live ist, können Sie verfolgen, wie das von Ihnen in [!DNL Journey Optimizer] erstellte Web-Erlebnis für die Besuchenden Ihrer Seite im Vergleich zu den Besuchenden funktioniert, die zur externen Landingpage weitergeleitet wurden. Erfahren Sie mehr dazu im [Experimentkampagnenbericht](../reports/campaign-global-report-cja-experimentation.md)

## Live-Schalten Ihres Web-Erlebnisses {#web-experience-live}

>[!IMPORTANT]
>
> Wenn Ihre Kampagne einer Genehmigungsrichtlinie unterliegt, müssen Sie eine Genehmigung anfordern, um Ihre Web-Erlebnisse aktivieren zu können.  [Weitere Informationen](../test-approve/gs-approval.md)

Sobald Sie Ihr Web-Erlebnis definiert und Ihre Inhalte wie gewünscht bearbeitet haben, können Sie Ihre Journey oder Kampagne aktivieren, um die Änderungen für Ihre Zielgruppe sichtbar zu machen.

Sie können auch eine Vorschau Ihrer Web-Erlebnis-Inhalte anzeigen, bevor Sie sie live schalten. [Weitere Informationen](#test-web-experience)

>[!NOTE]
>
>Wenn Sie eine Web-Journey/-Kampagne aktivieren, die sich auf dieselben Seiten auswirkt wie eine andere bereits aktive Journey oder Kampagne, werden alle Änderungen auf Ihre Web-Seiten angewendet.
>
>Wenn mehrere Journeys oder Kampagnen dieselben Elemente Ihrer Website aktualisieren, hat die Journey/Kampagne mit der höchsten Priorität Vorrang.

### Veröffentlichen einer Web-Journey {#activate-web-journey}

Gehen Sie wie folgt vor, um Ihr Web-Erlebnis von einer Journey live zu stellen.

1. Stellen Sie sicher, dass Ihre Journey gültig ist und kein Fehler vorliegt. [Weitere Informationen](../building-journeys/troubleshooting.md#activity-errors)

1. Wählen Sie in der Journey im Dropdown-Menü oben rechts die Option **[!UICONTROL Veröffentlichen]** aus.

   ![](assets/web-journey-publish.png)

   >[!NOTE]
   >
   >Weitere Informationen zur Veröffentlichung von Journeys finden Sie in [diesem Abschnitt](../building-journeys/publish-journey.md).

Ihre Web-Journey erhält den Status **[!UICONTROL Live]** und ist jetzt schreibgeschützt. Alle Empfängerinnen und Empfänger Ihrer Journey können die Änderungen sehen, die Sie an Ihrer Website vorgenommen haben.

>[!NOTE]
>
>Nachdem Sie auf **[!UICONTROL Veröffentlichen]** geklickt haben, kann es bis zu 15 Minuten dauern, bis die Änderungen live auf Ihrer Website verfügbar sind.

### Aktivieren einer Web-Kampagne {#activate-web-campaign}

Nachdem Sie Ihre Web-Kampagneneinstellungen festgelegt und Ihren Inhalt wie gewünscht bearbeitet haben, können Sie Ihre Web-Kampagne überprüfen und aktivieren. Gehen Sie wie folgt vor.

1. Wählen Sie in Ihrer Web-Kampagne die Option **[!UICONTROL Zur Aktivierung überprüfen]** aus.

1. Überprüfen und bearbeiten Sie bei Bedarf Inhalt, Eigenschaften, Konfiguration, Zielgruppe und Zeitplan.

1. Wählen Sie **[!UICONTROL Aktivieren]** aus.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Weitere Informationen zur Aktivierung von Kampagnen finden Sie in [diesem Abschnitt](../campaigns/review-activate-campaign.md).

Ihre Web-Kampagne geht in den [Status](../campaigns/manage-campaigns.md#statuses) **[!UICONTROL Live]** über und ist nun für die ausgewählte Zielgruppe sichtbar. Alle Empfängerinnen und Empfänge Ihrer Kampagne können die Änderungen sehen, die Sie an Ihrer Website vorgenommen haben.

>[!NOTE]
>
>Nachdem Sie auf **[!UICONTROL Aktivieren]** geklickt haben, kann es bis zu 15 Minuten dauern, bis Web-Kampagnenänderungen auf Ihrer Website live sind.
>
>Wenn Sie einen Zeitplan für Ihre Web-Kampagne definiert haben, hat sie den [Status](../campaigns/manage-campaigns.md#statuses) **[!UICONTROL Geplant]**, bis das Startdatum und die Startzeit erreicht werden.

Sobald Ihr Erlebnis live ist, können Sie Ihre Web-Journeys und -Kampagnen überwachen. [Weitere Informationen](monitor-web-experiences.md)

## Stoppen einer Web-Journey oder Kampagne {#stop-web-experience}

Wenn eine Web-Journey oder Kampagne live ist, können Sie diese stoppen, um zu verhindern, dass Ihre Zielgruppe Ihre Änderungen sieht. Gehen Sie wie folgt vor.

1. Wählen Sie eine Live-Journey oder -Kampagne aus der entsprechenden Liste aus.

1. Führen Sie je nach Fall die entsprechende Aktion aus:

   * Wählen Sie im oberen Menü der Kampagne **[!UICONTROL Kampagne stoppen]**.

     ![](assets/web-campaign-stop.png)

   * Klicken Sie im oberen Menü der Journey auf die Schaltfläche **[!UICONTROL Mehr]** und wählen Sie **[!UICONTROL Stoppen]**.

     ![](assets/web-journey-stop.png)

1. Die hinzugefügten Änderungen werden für die von Ihnen definierte Zielgruppe nicht mehr sichtbar sein.

>[!NOTE]
>
>Sobald eine Web-Journey oder Kampagne gestoppt wurde, können Sie diese nicht mehr bearbeiten oder erneut aktivieren. Sie können sie nur duplizieren und die duplizierte Journey/Kampagne aktivieren.

## Anleitungsvideo{#video}

Im folgenden Video erfahren Sie, wie Sie eine Web-Kampagne erstellen, ihre Eigenschaften konfigurieren, sie überprüfen und veröffentlichen.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)