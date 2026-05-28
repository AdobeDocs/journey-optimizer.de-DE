---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Journey Optimizer-Reporting für Experimente
description: Erfahren Sie, wie Sie eine Reporting-Datenquelle einrichten.
feature: Experimentation, Reporting
topic: Administration
role: Admin
level: Intermediate
keywords: Konfiguration, Experiment, Reporting, Optimizer
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
TQID: https://experienceleague.adobe.com/GiszI8Z-dWb13HjGdIVPEKwdSw8DwesEadPBbbqhUkM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 656
ht-degree: 100%

---

# Reporting- und Experimentiervoraussetzungen {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Einrichten von Datensätzen für das Reporting"
>abstract="Mit der Reporting-Konfiguration können Sie zusätzliche Metriken abrufen, die in Ihren Kampagnenberichten verwendet werden. Sie muss von einem/r technischen Anwender(in) durchgeführt werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Auswählen eines Datensatzes"
>abstract="Sie können nur einen Ereignistyp-Datensatz auswählen, der mindestens eine der unterstützten Feldergruppen enthält: Anwendungsdetails, Commerce-Details, Web-Details."

>[!NOTE]
>
>Die Konfiguration des Reportings muss von technischen Benutzenden vorgenommen werden.

Mit der Konfiguration von Berichtsdatenquellen können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen zur Verwendung in Ihren Berichten abzurufen.

Für diese Konfiguration müssen Sie einen oder mehrere Datensätze hinzufügen, die die zusätzlichen Elemente enthalten, die Sie für Ihre Berichte verwenden möchten. Gehen Sie dazu [wie folgt](#add-datasets) vor.

Beachten Sie, dass Sie beim Web-, Code-basierten und beim In-App-Kanal sicherstellen müssen, dass der [Datensatz](../data/get-started-datasets.md), der für die Datenerfassung konfiguriert wurde, auch zu dieser Reporting-Konfiguration hinzugefügt wird. Andernfalls werden Web- und In-App-Daten nicht in den Inhaltsexperimentberichten angezeigt.

## Voraussetzungen

Bevor Sie der Reporting-Konfiguration einen Datensatz hinzufügen können, müssen Sie diesen Datensatz erstellen. Weitere Informationen hierzu sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de#create){target="_blank"} verfügbar.

* Sie können nur Datensätze vom Typ „Ereignis“ hinzufügen.

* Diese Datensätze müssen die [Feldergruppe](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} `Experience Event - Proposition Interactions` enthalten.

* Diese Datensätze können auch eine der folgenden [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} enthalten: `Application Details`, `Commerce Details` und `Web Details`.

  >[!NOTE]
  >
  >Es können auch andere Feldergruppen einbezogen werden, aber in Journey Optimizer-Berichten werden derzeit nur die oben genannten Feldergruppen unterstützt.

  Wenn Sie beispielsweise wissen möchten, wie sich eine E-Mail-Kampagne auf Commerce-Daten wie Käufe oder Bestellungen auswirkt, müssen Sie einen Erlebnisereignis-Datensatz mit der Feldergruppe `Commerce Details` erstellen.

  Wenn Sie einen Bericht über Mobile-Interaktionen erstellen möchten, müssen Sie außerdem einen Erlebnisereignis-Datensatz mit der Feldergruppe `Application Details` erstellen.

  <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* Sie können diese Feldergruppen zu einem oder mehreren Schemata hinzufügen, die in einem oder mehreren Datensätzen verwendet werden.

>[!NOTE]
>
>Weitere Informationen zu XDM-Schemata und Feldergruppen sind in der [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"} verfügbar.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## Hinzufügen von Datensätzen {#add-datasets}

>[!NOTE]
>
>Alle neu erstellten Datensätze stehen nur in Customer Journey Analytics-Berichten zur Verfügung.

1. Wählen Sie im Menü **[!UICONTROL Administration]** die Option **[!UICONTROL Konfigurationen]** aus. Klicken Sie im Abschnitt **[!UICONTROL Reporting]** auf **[!UICONTROL Verwalten]**.

   ![](assets/reporting-config-menu.png)

   Die Liste der bereits hinzugefügten Datensätze wird angezeigt.

1. Klicken Sie in der Registerkarte **[!UICONTROL Datensatz]** auf **[!UICONTROL Datensatz hinzufügen]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Wenn Sie die Registerkarte **[!UICONTROL Systemdatensatz]** auswählen, werden nur vom System erstellte Datensätze angezeigt. Sie können keine anderen Datensätze hinzufügen.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Datensatz]** den Datensatz aus, den Sie für Ihre Berichte verwenden möchten.

   >[!CAUTION]
   >
   >Es kann nur ein Datensatz vom Typ „Ereignis“ ausgewählt werden, der mindestens eine der unterstützten [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} enthält: **Anwendungsdetails**, **Commerce-Details**, **Web-Details**. Wenn Sie einen Datensatz auswählen, der diesen Kriterien nicht entspricht, können Sie Ihre Änderungen nicht speichern.

   ![](assets/reporting-config-datasets.png)

   Weitere Informationen zu Datensätzen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target="_blank"} verfügbar.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Profilkennung]** das Datensatzfeldattribut aus, das zur Identifizierung der einzelnen Profile in Ihren Berichten verwendet wird.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Es werden nur IDs angezeigt, die für das Reporting verfügbar sind.

1. Die Option **[!UICONTROL Verwenden des primären ID-Namespace]** ist standardmäßig aktiviert. Wenn die ausgewählte **[!UICONTROL Profilkennung]** **[!UICONTROL Identitätszuordnung]** lautet, können Sie diese Option deaktivieren und einen anderen Namespace aus der angezeigten Dropdown-Liste auswählen.

   ![](assets/reporting-config-namespace.png)

   Weitere Informationen zu Namespaces sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=de){target="_blank"} verfügbar.

1. Speichern Sie Ihre Änderungen, um den ausgewählten Datensatz zur Liste der Reporting-Konfigurationen hinzuzufügen.

   >[!CAUTION]
   >
   >Wenn Sie einen Datensatz ausgewählt haben, der nicht vom Typ „Ereignis“ ist, können Sie nicht fortfahren.


<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
