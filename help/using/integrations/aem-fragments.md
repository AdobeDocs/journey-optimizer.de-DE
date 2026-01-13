---
solution: Journey Optimizer
product: journey optimizer
title: AEM-Inhaltsfragmente
description: Erfahren Sie, wie Sie auf AEM-Inhaltsfragmente zugreifen und diese verwalten
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 780c197da342968c6dc125277f325219e0717082
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 91%

---

# Inhaltsfragmente in Adobe Experience Manager {#aem-fragments}

Durch die Integration von Adobe Experience Manager as a Cloud Service mit Adobe Journey Optimizer können Sie jetzt Ihre AEM-Inhaltsfragmente nahtlos in Journey Optimizer in Ihre Inhalte integrieren. Diese optimierte Verbindung vereinfacht den Zugriff auf und die Nutzung von AEM-Inhalten und ermöglicht die Erstellung personalisierter und dynamischer Kampagnen und Journeys.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie unter [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Dokumentation zu Experience Manager.

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenzierung der Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Enhanced Security aktiviert.

## Einschränkungen {#limitations}

* Es wird empfohlen, die Anzahl der Benutzenden mit Zugriff auf die Veröffentlichung von Inhaltsfragmenten zu begrenzen, um das Risiko versehentlicher Fehler zu reduzieren.

* Bei mehrsprachigen Inhalten wird nur der manuelle Fluss unterstützt.

* Varianten werden derzeit nicht unterstützt.

* Der Testversand für veröffentlichte Kampagnen und Journeys spiegelt Daten aus der neuesten Experience Manager-Inhaltsfragmentveröffentlichung wider.

## Erstellen und Zuweisen eines Tags in Experience Manager

>[!IMPORTANT]
>
>Damit Journey Optimizer über die Inhaltsfragmentverwaltungs-API auf Adobe Experience Manager-Inhaltsfragmente zugreifen kann, müssen Sie zunächst [Dispatcher konfigurieren](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration).

Bevor Sie Ihr Inhaltsfragment in Journey Optimizer verwenden, müssen Sie ein Tag speziell für Journey Optimizer erstellen:

1. Greifen Sie auf Ihre **Experience Manager**-Umgebung zu.

1. Wählen Sie im Menü **Tools** die Option **Tagging** aus.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Klicken Sie auf **Tag erstellen**.

1. Stellen Sie sicher, dass die ID der folgenden Syntax entspricht: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Klicken Sie auf **Erstellen**.

1. Definieren Sie Ihr Inhaltsfragmentmodell, wie in der [Dokumentation zu Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} beschrieben und weisen Sie Ihr neu erstelltes Journey Optimizer-Tag zu.

Sie können jetzt mit der Erstellung und Konfiguration Ihres Inhaltsfragments zur späteren Verwendung in Journey Optimizer beginnen. Weitere Informationen hierzu finden Sie in der [Dokumentation zu Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Hinzufügen von Experience Manager-Inhaltsfragmenten {#aem-add}

Nachdem Sie Ihre AEM-Inhaltsfragmente erstellt und personalisiert haben, können Sie sie in Ihre Journey Optimizer-Kampagne oder -Journey importieren.

1. Erstellen Sie Ihre [Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Um auf Ihr AEM-Inhaltsfragment zuzugreifen, klicken Sie auf ![Personalisierungssymbol](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in einem beliebigen Textfeld oder öffnen Sie den Quell-Code über eine HTML-Inhaltskomponente.

   ![](assets/aem_campaign_2.png)

1. Klicken Sie im Menü **[!UICONTROL AEM-Inhaltsfragment]** im linken Bereich auf **[!UICONTROL AEM-Inhaltsfragmentauswahl öffnen]**.

   ![](assets/aem_campaign_3.png)

1. Wählen Sie ein **[!UICONTROL Inhaltsfragment]** aus der verfügbaren Liste aus, das in Ihren Journey Optimizer-Inhalt importiert werden soll.

1. Klicken Sie auf **[!UICONTROL Filter anzeigen]**, um Ihre Inhaltsfragmentliste zu optimieren.

   Standardmäßig ist der Filter „Inhaltsfragment“ so voreingestellt, dass nur genehmigte Inhalte angezeigt werden.

   ![](assets/aem_campaign_4.png)

1. Nachdem Sie Ihr **[!UICONTROL Inhaltsfragment]** ausgewählt haben, klicken Sie auf **[!UICONTROL Auswählen]**, um es zu öffnen.

   ![](assets/aem_campaign_5.png)

1. Klicken Sie auf **[!UICONTROL Fragment anzeigen]**, um Ihre Fragmentinformationen anzuzeigen. Beachten Sie, dass durch Öffnen des Menüs **[!UICONTROL Fragmentinformationen]** der Editor in den schreibgeschützten Modus versetzt wird.

   Wählen Sie im Menü rechts **[!UICONTROL Vorschau]** aus, um Ihr Fragment in Adobe Experience Manager anzuzeigen.

   ![](assets/aem_campaign_7.png)

1. Klicken Sie auf ![Symbol für weitere Aktionen](assets/do-not-localize/Smock_MoreSmallList_18_N.svg), um auf das erweiterte Menü Ihres Fragments zuzugreifen:

   * **[!UICONTROL Fragment austauschen]**
   * **[!UICONTROL Verweise durchsuchen]**
   * **[!UICONTROL In AEM öffnen]**

   ![](assets/aem_campaign_8.png)

1. Wählen Sie die gewünschten Felder aus Ihrem **[!UICONTROL Fragment]** aus, um sie zu Ihrem Inhalt hinzuzufügen.

   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Wählen Sie **Pillen: Aus**, um das Pillenerlebnis zu aktivieren und die Lesbarkeit durch Ausblenden langer Attributpfade zu verbessern.

   ![](assets/aem_campaign_10.png)

1. Um die Echtzeit-Personalisierung zu aktivieren, müssen alle in einem **[!UICONTROL Inhaltsfragment]** verwendeten Platzhalter von der Benutzerin bzw. vom Benutzer explizit als Parameter im Fragment-Helfer-Tag deklariert werden. Sie können diese Platzhalter mit den folgenden Methoden Profilattributen, kontextuellen Attributen, statischen Zeichenfolgen oder vordefinierten Variablen zuordnen:

   1. **Zuordnung zu Profilen oder kontextuellen Attributen**: Weisen Sie den Platzhalter einem Profil oder einem kontextuellen Attribut zu, z. B. name = profile.person.name.firstName.

   1. **Statische Zeichenfolgenzuordnung**: Weisen Sie einen festen Zeichenfolgenwert zu, indem Sie ihn in doppelte Anführungszeichen setzen, z. B. name = „John“.

   1. **Variablenzuordnung**: Verweisen Sie auf eine Variable, die zuvor innerhalb derselben HTML deklariert wurde, z. B. name = &#39;variableName&#39;.
Stellen Sie in diesem Fall mit der folgenden Syntax sicher, dass **_variableName_** deklariert wird, bevor Sie die Fragment-ID hinzufügen:

      ```html
      {% let variableName = attribute name %} 
      ```

   Im folgenden Beispiel wird der Platzhalter **_month_** dem Attribut **_profile.person.BirthDate_** im Fragment zugeordnet.

   ![](assets/aem_campaign_9.png){zoomable="yes"}


1. Klicken Sie auf **[!UICONTROL Speichern]**. Sie können nun den Inhalt Ihrer Nachricht testen und überprüfen, wie in [diesem Abschnitt](../content-management/preview.md) beschrieben.

Sobald Sie Ihre Tests durchgeführt und den Inhalt validiert haben, können Sie Ihrer Zielgruppe [Ihre Kampagne senden](../campaigns/review-activate-campaign.md) oder für sie [Ihre Journey veröffentlichen](../building-journeys/publish-journey.md).

Mit Adobe Experience Manager können die Journey Optimizer-Kampagnen oder -Journeys identifiziert werden, in denen ein Inhaltsfragment verwendet wird. Weitere Informationen hierzu sind in der [Dokumentation zu Adobe Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references) verfügbar.
