---
title: Konfigurieren von Journey Optimizer-Berichten für Experimente
description: Erfahren Sie, wie Sie eine Berichtsdatenquelle einrichten.
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 16c156d715a6b39652191909ca88f90e7f971706
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 4%

---

# Reporting für Experimente konfigurieren {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Einrichten von Datensätzen für die Berichterstellung"
>abstract="Mit der Berichtskonfiguration können Sie zusätzliche Metriken abrufen, die im Tab Ziele Ihrer Kampagnenberichte verwendet werden. Sie muss von einem technischen Anwender durchgeführt werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Auswählen eines Datensatzes"
>abstract="Sie können nur einen Datensatz vom Typ Ereignis auswählen, der mindestens eine der unterstützten Feldgruppen enthalten muss: Anwendungsdetails, Commerce-Details, Web-Details."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

Mit der Konfiguration der Berichtsdatenquelle können Sie zusätzliche Metriken abrufen, die in der Variablen **[!UICONTROL Ziele]** in den Kampagnenberichten. [Weitere Informationen](content-experiment.md#objectives-global)

>[!NOTE]
>
>Die Berichtskonfiguration muss von einem technischen Anwender vorgenommen werden. <!--Rights?-->

Für diese Konfiguration müssen Sie einen oder mehrere Datensätze hinzufügen, die die zusätzlichen Elemente enthalten, die Sie für Ihre Berichte verwenden möchten. Gehen Sie dazu wie folgt vor: [below](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Voraussetzungen


Bevor Sie der Berichtskonfiguration einen Datensatz hinzufügen können, müssen Sie diesen Datensatz erstellen. Erfahren Sie mehr über [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.

* Sie können nur Datensätze vom Typ Ereignis hinzufügen.

* Diese Datensätze müssen mindestens einen der folgenden Datensätze enthalten: [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **Anwendungsdetails**, **Commerce-Details**, **Webdetails**.

   >[!NOTE]
   >
   >Derzeit werden nur diese Feldergruppen unterstützt.

   Wenn Sie beispielsweise wissen möchten, wie sich eine E-Mail-Kampagne auf Commerce-Daten wie Käufe oder Bestellungen auswirkt, müssen Sie einen Erlebnisereignis-Datensatz mit dem **Commerce-Details** Feldergruppe.

   Wenn Sie einen Bericht über mobile Interaktionen erstellen möchten, müssen Sie außerdem einen Erlebnisereignis-Datensatz mit der Variablen **Anwendungsdetails** Feldergruppe.

   Die den einzelnen Feldergruppen entsprechenden Metriken werden aufgelistet [here](#objective-list).

* Sie können diese Feldergruppen zu einem oder mehreren Schemas hinzufügen, die in einem oder mehreren Datensätzen verwendet werden.

>[!NOTE]
>
>Weitere Informationen zu XDM-Schemata und Feldergruppen finden Sie im Abschnitt [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;}.

## Ziele für jede Feldergruppe {#objective-list}

Die nachstehende Tabelle zeigt, welche Metriken zum **[!UICONTROL Ziele]** in den Kampagnenberichten für jede Feldergruppe.

| Feldergruppe | Ziele |
|--- |--- |
| Commerce-Details | Preis gesamt<br>Zahlungsbetrag<br>(Eindeutige Checkouts)<br>(Eindeutige Produktlistenhinweise)<br>(Eindeutige Produktlisten-Öffnungen)<br>(Eindeutige) Entfernung der Produktliste<br>(Eindeutige) Produktlistenansichten<br>(Eindeutige) Produktansichten<br>(Einzelkäufe)<br>(Eindeutig) Für spätere speichern<br>Produktpreis gesamt<br>Produktmenge |
| Anwendungsdetails | (Eindeutige) App-Starts<br>Erste App-Starts<br>(Unique) App-Installationen<br>(Unique) App-Upgrades |
| Web-Details | (Eindeutige) Seitenansichten |

## Hinzufügen von Datensätzen {#add-datasets}

1. Aus dem **[!UICONTROL VERWALTUNG]** Menü auswählen **[!UICONTROL Konfigurationen]**. Im  **[!UICONTROL Berichterstellung]** Abschnitt, klicken Sie auf **[!UICONTROL Verwalten]**.

   ![](assets/reporting-config-menu.png)

   Die Liste der bereits hinzugefügten Datensätze wird angezeigt.

1. Aus dem **[!UICONTROL Datensatz]** Registerkarte, klicken Sie auf **[!UICONTROL Datensatz hinzufügen]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Wenn Sie die **[!UICONTROL Systemdatensatz]** angezeigt werden, werden nur vom System erstellte Datensätze angezeigt. Sie können keine anderen Datensätze hinzufügen.

1. Aus dem **[!UICONTROL Datensatz]** Dropdownliste den Datensatz auswählen, den Sie für Ihre Berichte verwenden möchten.

   >[!CAUTION]
   >
   >Sie können nur einen Datensatz vom Typ Ereignis auswählen, der mindestens einen der unterstützten Datensätze enthalten muss [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **Anwendungsdetails**, **Commerce-Details**, **Webdetails**. Wenn Sie einen Datensatz auswählen, der diesen Kriterien nicht entspricht, können Sie Ihre Änderungen nicht speichern.

   ![](assets/reporting-config-datasets.png)

   Weitere Informationen zu Datensätzen finden Sie im Abschnitt [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target=&quot;_blank&quot;}.

1. Aus dem **[!UICONTROL Profil-ID]** wählen Sie in der Dropdown-Liste das Datensatzfeldattribut aus, das zur Identifizierung der einzelnen Profile in Ihren Berichten verwendet wird.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Es werden nur IDs angezeigt, die für Berichte verfügbar sind.

1. Die **[!UICONTROL Verwenden des Primären ID-Namespace]** ist standardmäßig aktiviert. Wenn ausgewählt **[!UICONTROL Profil-ID]** is **[!UICONTROL Identitätszuordnung]** können Sie diese Option deaktivieren und einen anderen Namespace aus der angezeigten Dropdownliste auswählen.

   ![](assets/reporting-config-namespace.png)

   Weitere Informationen zu Namespaces finden Sie im Abschnitt [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=de){target=&quot;_blank&quot;}.

1. Speichern Sie Ihre Änderungen, um den ausgewählten Datensatz zur Liste der Berichtskonfigurationen hinzuzufügen.

   >[!CAUTION]
   >
   >Wenn Sie einen Datensatz ausgewählt haben, der kein Ereignistyp ist, können Sie nicht fortfahren.

Beim Erstellen Ihrer Kampagnenberichte können Sie nun die Metriken sehen, die den in den hinzugefügten Datensätzen verwendeten Feldgruppen entsprechen. Navigieren Sie zu **[!UICONTROL Ziele]** und wählen Sie die gewünschten Metriken aus, um Ihre Berichte besser anzupassen. [Weitere Informationen](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Wenn Sie mehrere Datensätze hinzufügen, stehen alle Daten aus allen Datensätzen für die Berichterstellung zur Verfügung.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
