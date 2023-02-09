---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Journey Optimizer-Reporting für Experimente
description: Erfahren Sie, wie Sie eine Reporting-Datenquelle einrichten.
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: Konfiguration, Experiment, Reporting, Optimizer
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 100%

---

# Konfigurieren der Berichterstellung für Experimente {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Einrichten von Datensätzen für das Reporting"
>abstract="Mit der Reporting-Konfiguration können Sie zusätzliche Metriken abrufen, die in der Registerkarte „Ziele“ Ihrer Kampagnenberichte verwendet werden. Sie muss von einem/r technischen Anwender(in) durchgeführt werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Auswählen eines Datensatzes"
>abstract="Sie können nur einen Ereignistyp-Datensatz auswählen, der mindestens eine der unterstützten Feldergruppen enthält: Anwendungsdetails, Commerce-Details, Web-Details."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

Mit der Konfiguration der Reporting-Datenquelle können Sie zusätzliche Metriken abrufen, die in der Registerkarte **[!UICONTROL Ziele]** in den Kampagnenberichten verwendet werden. [Weitere Informationen](content-experiment.md#objectives-global)

>[!NOTE]
>
>Die Reporting-Konfiguration muss von einem/r technischen Anwender(in) vorgenommen werden. <!--Rights?-->

Für diese Konfiguration müssen Sie einen oder mehrere Datensätze hinzufügen, die die zusätzlichen Elemente enthalten, die Sie für Ihre Berichte verwenden möchten. Gehen Sie dazu [wie folgt](#add-datasets) vor.

<!--
➡️ [Discover this feature in video](#video)
-->

## Voraussetzungen


Bevor Sie der Reporting-Konfiguration einen Datensatz hinzufügen können, müssen Sie diesen Datensatz erstellen. Weitere Informationen hierzu finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de#create){target="_blank"}.

* Sie können nur Datensätze vom Typ „Ereignis“ hinzufügen.

* Diese Datensätze müssen mindestens eine der folgenden [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} enthalten: **Anwendungsdetails**, **Commerce-Details**, **Web-Details**.

   >[!NOTE]
   >
   >Derzeit werden nur diese Feldergruppen unterstützt.

   Wenn Sie beispielsweise wissen möchten, wie sich eine E-Mail-Kampagne auf Commerce-Daten wie Käufe oder Bestellungen auswirkt, müssen Sie einen Erlebnisereignis-Datensatz mit der **Commerce-Details**-Feldergruppe erstellen.

   Wenn Sie einen Bericht über mobile Interaktionen erstellen möchten, müssen Sie außerdem einen Erlebnisereignis-Datensatz mit der Feldergruppe **Anwendungsdetails** erstellen.

   Die den einzelnen Feldergruppen entsprechenden Metriken werden [hier](#objective-list) aufgelistet.

* Sie können diese Feldergruppen zu einem oder mehreren Schemata hinzufügen, die in einem oder mehreren Datensätzen verwendet werden.

>[!NOTE]
>
>Weitere Informationen zu XDM-Schemata und Feldergruppen finden Sie in der [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}.

## Ziele für jede Feldergruppe {#objective-list}

Die nachstehende Tabelle zeigt, welche Metriken für jede Feldergruppe zur Registerkarte **[!UICONTROL Ziele]** in Ihren Kampagnenberichten hinzugefügt werden.

| Feldergruppe | Ziele |
|--- |--- |
| Commerce-Details | Preis gesamt<br>Zahlungsbetrag<br>(Eindeutige) Checkouts<br>(Eindeutige) Produktlisten-Hinzufügungen<br>(Eindeutige) Produktlisten-Öffnungen<br>(Eindeutige) Produktlisten-Entfernungen<br>(Eindeutige) Produktlisten-Ansichten<br>(Eindeutige) Produktansichten<br>(Eindeutige) Käufe<br>(Eindeutig) Speicherungen für später<br>Produktpreis gesamt<br>Produktmenge |
| Anwendungsdetails | (Eindeutige) App-Starts<br>Erste App-Starts<br>(Eindeutige) App-Installationen<br>(Eindeutige) App-Upgrades |
| Web-Details | (Eindeutige) Seitenansichten |

## Hinzufügen von Datensätzen {#add-datasets}

1. Wählen Sie im Menü **[!UICONTROL ADMINISTRATION]** **[!UICONTROL Konfigurationen]** aus. Klicken Sie im Abschnitt **[!UICONTROL Reporting]** auf **[!UICONTROL Verwalten]**.

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
   >Sie können nur einen Datensatz vom Typ „Ereignis“ auswählen, der mindestens eine der unterstützten [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=de#field-group){target="_blank"} enthält: **Anwendungsdetails**, **Commerce-Details**, **Web-Details**. Wenn Sie einen Datensatz auswählen, der diesen Kriterien nicht entspricht, können Sie Ihre Änderungen nicht speichern.

   ![](assets/reporting-config-datasets.png)

   Weitere Informationen zu Datensätzen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=de){target="_blank"}.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Profilkennung]** das Datensatzfeldattribut aus, das zur Identifizierung der einzelnen Profile in Ihren Berichten verwendet wird.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Es werden nur IDs angezeigt, die für das Reporting verfügbar sind.

1. Die Option **[!UICONTROL Verwenden des primären ID-Namespace]** ist standardmäßig aktiviert. Wenn die ausgewählte **[!UICONTROL Profilkennung]** **[!UICONTROL Identitätszuordnung]** lautet, können Sie diese Option deaktivieren und einen anderen Namespace aus der angezeigten Dropdown-Liste auswählen.

   ![](assets/reporting-config-namespace.png)

   Weitere Informationen zu Namespaces finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=de){target="_blank"}.

1. Speichern Sie Ihre Änderungen, um den ausgewählten Datensatz zur Liste der Reporting-Konfigurationen hinzuzufügen.

   >[!CAUTION]
   >
   >Wenn Sie einen Datensatz ausgewählt haben, der nicht vom Typ „Ereignis“ ist, können Sie nicht fortfahren.

Beim Erstellen Ihrer Kampagnenberichte können Sie nun die Metriken sehen, die den in den hinzugefügten Datensätzen verwendeten Feldergruppen entsprechen. Gehen Sie zur Registerkarte **[!UICONTROL Ziele]** und wählen Sie die gewünschten Metriken aus, um Ihre Berichte entsprechend Ihren Anforderungen anzupassen. [Weitere Informationen](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Wenn Sie mehrere Datensätze hinzufügen, stehen alle Daten aus allen Datensätzen für das Reporting zur Verfügung.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
