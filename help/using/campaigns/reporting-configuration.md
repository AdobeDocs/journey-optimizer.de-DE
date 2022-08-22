---
title: Berichtskonfiguration
description: Erfahren Sie, wie Sie eine Berichtsdatenquelle einrichten.
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 5%

---

# Berichtskonfiguration {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Einrichten von Datensätzen für die Berichterstellung"
>abstract="Mit der Berichtskonfiguration können Sie eine Verbindung zu einem System definieren, um zusätzliche benutzerdefinierte Informationen abzurufen, die in Ihren Berichten verwendet werden. Sie muss von einem technischen Anwender durchgeführt werden."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Auswählen eines Datensatzes"
>abstract="Sie können nur einen Datensatz vom Typ Ereignis auswählen, der mindestens eine der unterstützten Feldgruppen enthalten muss: experienceevent-web, experienceevent-application, experienceevent-commerce."

Mit der Konfiguration der Berichtsdatenquelle können Sie eine Verbindung zu einem System definieren, um zusätzliche Informationen abzurufen, die in Ihren Berichten verwendet werden.

>[!NOTE]
>
>Die Konfiguration der Datenquelle muss von einem technischen Anwender durchgeführt werden. <!--Rights?-->

Für diese Konfiguration müssen Sie einen oder mehrere Datensätze hinzufügen, die die Attribute enthalten, die Sie für Ihre Berichte verwenden möchten. Gehen Sie dazu wie folgt vor.

>[!CAUTION]
>
>Bevor Sie einen Datensatz zur Berichtskonfiguration hinzufügen können, müssen Sie ihn erstellen. Erfahren Sie mehr über [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>Sie können nur Datensätze vom Typ Ereignis hinzufügen, die mindestens einen der unterstützten Datensätze enthalten müssen [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experience-event-web**, **experience-event-application**, **experience-event-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Wenn Sie beispielsweise wissen möchten, wie sich eine E-Mail-Kampagne auf Commerce-Daten wie Käufe oder Bestellungen auswirkt, müssen Sie einen Erlebnisereignis-Datensatz mit dem **experience-event-commerce** Feldergruppe. Wenn Sie einen Bericht über mobile Interaktionen erstellen möchten, müssen Sie außerdem einen Erlebnisereignis-Datensatz mit der Variablen **experience-event-application** Feldergruppe. <!--If you want to report on web interactions then you need to include the web field group.--> Sie können diese Feldergruppen zu einem oder mehreren Schemas hinzufügen, die in einem Datensatz oder in verschiedenen Datensätzen verwendet werden.

>[!NOTE]
>
>Weitere Informationen zu XDM-Schemata und Feldergruppen finden Sie im Abschnitt [Dokumentation zur XDM-Systemübersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target=&quot;_blank&quot;}.

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
   >Sie können nur einen Datensatz vom Typ Ereignis auswählen, der mindestens einen der unterstützten Datensätze enthalten muss [Feldergruppen](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **experience-event-web**, **experience-event-application**, **experience-event-commerce**. Wenn Sie einen Datensatz auswählen, der diesen Kriterien nicht entspricht, können Sie Ihre Änderungen nicht speichern.

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

Beim Erstellen von Versandberichten können Sie jetzt Daten aus diesem Datensatz verwenden, um zusätzliche benutzerdefinierte Informationen abzurufen und Ihre Berichte besser anzupassen. [Weitere Informationen](campaign-global-report.md#objectives-global)

>[!NOTE]
>
>Wenn Sie mehrere Datensätze hinzufügen, stehen alle Daten aus allen Datensätzen für die Berichterstellung zur Verfügung.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
