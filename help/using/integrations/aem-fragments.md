---
solution: Journey Optimizer
product: journey optimizer
title: AEM-Inhaltsfragmente
description: Erfahren Sie, wie Sie auf AEM-Inhaltsfragmente zugreifen und diese verwalten
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 7098a643c8026ed00f83a66fd45f957c2403a569
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 22%

---

# Inhaltsfragmente in Adobe Experience Manager {#aem-fragments}

Durch die Integration von Adobe Experience Manager as a Cloud Service mit Adobe Journey Optimizer können Sie jetzt Ihre AEM-Inhaltsfragmente nahtlos in Ihre Journey Optimizer-Inhalte integrieren. Diese optimierte Verbindung vereinfacht den Zugriff auf und die Nutzung von AEM-Inhalten und ermöglicht die Erstellung personalisierter und dynamischer Kampagnen und Journeys.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie unter [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Dokumentation zu Experience Manager.

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenz für die Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Enhanced Security aktiviert.

## Einschränkungen {#limitations}

* Es wird empfohlen, die Anzahl der Benutzer mit Zugriff auf die Veröffentlichung von Inhaltsfragmenten zu begrenzen, um das Risiko versehentlicher Fehler zu reduzieren.

* Bei mehrsprachigen Inhalten wird nur der manuelle Fluss unterstützt.

* Varianten werden derzeit nicht unterstützt.

* Der Korrekturabzug für veröffentlichte Kampagnen und Journey spiegelt Daten aus der neuesten Experience Manager-Inhaltsfragmentveröffentlichung wider.

## Erstellen und Zuweisen eines Tags in Experience Manager

Bevor Sie Ihr Inhaltsfragment in Journey Optimizer verwenden, müssen Sie ein Tag speziell für Journey Optimizer erstellen:

1. Greifen Sie auf Ihre **Experience Manager**-Umgebung zu.

1. Wählen Sie im Menü **Tools** die Option **Tagging** aus.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Klicken Sie **Tag erstellen**.

1. Stellen Sie sicher, dass die ID der folgenden Syntax entspricht: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Klicken Sie auf **Erstellen**.

1. Definieren Sie Ihr Inhaltsfragmentmodell, wie in der [Experience Manager-Dokumentation beschrieben](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} und weisen Sie Ihr neu erstelltes Journey Optimizer-Tag zu.

Sie können jetzt mit der Erstellung und Konfiguration Ihres Inhaltsfragments zur späteren Verwendung in Journey Optimizer beginnen. Weitere Informationen finden Sie in der Dokumentation zu [Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Hinzufügen von Experience Manager-Inhaltsfragmenten {#aem-add}

Nachdem Sie Ihre AEM-Inhaltsfragmente erstellt und personalisiert haben, können Sie sie jetzt in Ihre Journey Optimizer-Kampagne oder auf Ihre Journey importieren.

1. Erstellen Sie [Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Um auf Ihr AEM-Inhaltsfragment zuzugreifen, klicken Sie auf das Symbol ![Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in einem beliebigen Textfeld oder öffnen Sie den Quell-Code über eine HTML-Inhaltskomponente.

   ![](assets/aem_campaign_2.png)

1. Klicken Sie im Menü **[!UICONTROL AEM-Inhaltsfragment]** im linken Bereich auf **[!UICONTROL AEM-Inhaltsfragmentauswahl öffnen]**.

   ![](assets/aem_campaign_3.png)

1. Wählen Sie ein **[!UICONTROL Inhaltsfragment]** aus der verfügbaren Liste aus, das in Ihren Journey Optimizer-Inhalt importiert werden soll.

1. Klicken Sie auf **[!UICONTROL Filter anzeigen]**, um Ihre Inhaltsfragmentliste zu optimieren.

   Standardmäßig ist der Filter „Inhaltsfragment“ so voreingestellt, dass nur genehmigte Inhalte angezeigt werden.

   ![](assets/aem_campaign_4.png)

1. Nachdem Sie Ihr **[!UICONTROL Inhaltsfragment]** ausgewählt haben, klicken Sie auf **[!UICONTROL Auswählen]**, um es zu öffnen.

   ![](assets/aem_campaign_5.png)

1. Klicken Sie **[!UICONTROL Fragment anzeigen]**, um Ihre Fragmentinformationen anzuzeigen. Beachten Sie, dass durch Öffnen **[!UICONTROL Menüs]** Fragmentinformationen“ der Editor in den schreibgeschützten Modus versetzt wird.

   Wählen **[!UICONTROL im]** Menü aus, um Ihr Fragment in Adobe Experience Manager anzuzeigen.

   ![](assets/aem_campaign_7.png)

1. Klicken Sie auf ![Symbol Mehr Aktionen](assets/do-not-localize/Smock_MoreSmallList_18_N.svg), um auf das erweiterte Menü Ihres Fragments zuzugreifen:

   * **[!UICONTROL Fragment austauschen]**
   * **[!UICONTROL Verweise erkunden]**
   * **[!UICONTROL In AEM öffnen]**

   ![](assets/aem_campaign_8.png)

1. Wählen Sie die gewünschten Felder aus Ihrem **[!UICONTROL Fragment]** aus, um sie zu Ihrem Inhalt hinzuzufügen.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Um die Echtzeit-Personalisierung zu aktivieren, müssen alle Platzhalter, die in einem **[!UICONTROL Inhaltsfragment]** verwendet werden, vom Benutzer explizit als Parameter im Fragment-Helper-Tag deklariert werden. Sie können diese Platzhalter mit den folgenden Methoden Profilattributen, kontextuellen Attributen, statischen Zeichenfolgen oder vordefinierten Variablen zuordnen:

   1. **Profil- oder kontextuelle Attributzuordnung**: Weisen Sie den Platzhalter einem Profil oder einem kontextuellen Attribut zu, z. B. name = profile.person.name.firstName.

   1. **Statische Zeichenfolgenzuordnung** Weisen Sie einen festen Zeichenfolgenwert zu, indem Sie ihn in doppelte Anführungszeichen setzen, z. B. name = „John“.

   1. **Variablenzuordnung** Verweisen Sie auf eine Variable, die zuvor innerhalb derselben HTML deklariert wurde, z. B. name = &#39;variableName&#39;.
Stellen Sie in diesem Fall sicher&#x200B;**_dass „variableName_** deklariert wird, bevor Sie die Fragment-ID mit der folgenden Syntax hinzufügen:

      ```html
      {% let variableName = attribute name %} 
      ```

   Im folgenden Beispiel wird der Platzhalter **_name_** dem Attribut **_profile.person.name.firstName_** im Fragment zugeordnet.

   ![](assets/aem_campaign_9.png){zoomable="yes"}


1. Klicken Sie auf **[!UICONTROL Speichern]**. Sie können nun den Inhalt Ihrer Nachricht testen und überprüfen, wie in [diesem Abschnitt](../content-management/preview.md) beschrieben.

Nachdem Sie die Tests und die Validierung des Inhalts durchgeführt haben, können Sie [Ihre Kampagne senden](../campaigns/review-activate-campaign.md) oder [Ihre Journey veröffentlichen](../building-journeys/publishing-the-journey.md) an Ihre Zielgruppe senden.

Mit Adobe Experience Manager können Sie die Journey Optimizer-Kampagnen oder Journey identifizieren, in denen ein Inhaltsfragment verwendet wird. Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).
