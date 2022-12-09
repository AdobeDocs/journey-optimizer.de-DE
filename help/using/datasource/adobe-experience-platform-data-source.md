---
solution: Journey Optimizer
product: journey optimizer
title: Datenquelle von Adobe Experience Platform
description: Erfahren Sie, wie Sie die Datenquelle von Adobe Experience Platform konfigurieren
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 69037a070f43fa89d0971cedc03adb577e1450d9
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Datenquelle von Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Datenquelle von Adobe Experience Platform"
>abstract="Die Datenquelle von Adobe Experience Platform definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Sie dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofildienst (überprüfen Sie beispielsweise, ob die Person, die an einer Journey teilnimmt, weiblich ist). Damit können Sie Profildaten und Erlebnisereignisdaten verwenden."

Die Datenquelle von Adobe Experience Platform definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Diese Datenquelle dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofildienst (überprüfen Sie beispielsweise, ob die Person, die an einer Journey teilnimmt, weiblich ist). Damit können Sie Profildaten und Erlebnisereignisdaten verwenden. Weitere Informationen zum Echtzeit-Kundenprofil von Adobe finden Sie unter [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.


Um die Verbindung zum Echtzeit-Kundenprofildienst zu ermöglichen, müssen wir einen Schlüssel zur Identifizierung einer Person und einen Namespace verwenden, der den Schlüssel kontextualisiert. Daher können Sie diese Datenquelle nur verwenden, wenn Ihre Journeys mit einem Ereignis beginnen, das einen Schlüssel und einen Namespace enthält. [Weitere Infos](../building-journeys/journey.md).

Sie können die vorkonfigurierte Feldergruppe mit dem Namen &quot;ProfileFieldGroup&quot;bearbeiten, neue hinzufügen und diejenigen entfernen, die nicht in Entwurfs- oder Live-Journeys verwendet werden. [Weitere Infos](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Sie können die 1000 neuesten Erlebnisereignisse abrufen, die vor weniger als einem Jahr erstellt wurden.

Im Folgenden finden Sie die wichtigsten Schritte zum Hinzufügen von Feldergruppen zur integrierten Datenquelle.

1. Wählen Sie aus der Liste der Datenquellen die integrierte Adobe Experience Platform-Datenquelle aus.

   Dadurch wird der Konfigurationsbereich für die Datenquelle auf der rechten Seite des Bildschirms geöffnet.

   ![](assets/journey23.png)

1. Klicken **[!UICONTROL Add a New Field Group]** , um eine neue Reihe von Feldern zu definieren, die abgerufen werden sollen. [Weitere Infos](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Wählen Sie ein Schema aus dem **[!UICONTROL Schema]** Dropdown-Liste. In diesem Feld werden die in Adobe Experience Platform verfügbaren Profil- und Erlebnisereignisschemata aufgelistet. Die Schemaerstellung erfolgt nicht in [!DNL Journey Optimizer]. Sie wird in Adobe Experience Platform durchgeführt.
1. Wählen Sie die Felder aus, die Sie verwenden möchten.
1. Klicken Sie auf **[!UICONTROL Save]**.

Wenn Sie den Cursor auf den Namen einer Feldergruppe setzen, werden rechts zwei Symbole angezeigt. Sie ermöglichen das Löschen und Duplizieren der Feldergruppe. Beachten Sie Folgendes: **[!UICONTROL Delete]** ist nur verfügbar, wenn die Feldergruppe in keiner Live- oder Entwurfs-Journey verwendet wird (Informationen werden im **[!UICONTROL Used in]** -Feld).
