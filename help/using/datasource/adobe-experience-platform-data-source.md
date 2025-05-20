---
solution: Journey Optimizer
product: journey optimizer
title: Datenquelle von Adobe Experience Platform
description: Erfahren Sie, wie Sie die Datenquelle von Adobe Experience Platform konfigurieren
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: integriert, Quelle, Daten, Plattform, Integration
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: f5ea4455fc0a8ed9e2819a260a8691fc1237844c
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 63%

---

# Datenquelle von Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Datenquelle von Adobe Experience Platform"
>abstract="Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Diese Datenquelle dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofil-Service (Sie können damit beispielsweise überprüfen, ob es sich bei einer Person, die an eine Journey eingetreten ist, um eine Frau handelt). Sie ermöglicht Ihnen die Verwendung von Profildaten und Erlebnisereignisdaten."

Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Diese Datenquelle dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofildienst (überprüfen Sie beispielsweise, ob es sich bei der Person, die an einer Journey teilnimmt, um eine Frau handelt). Sie ermöglicht Ihnen die Verwendung von Profildaten und Erlebnisereignisdaten. Weitere Informationen zum Echtzeit-Kundenprofil von Adobe finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"}.

Um die Verbindung zum Echtzeit-Kundenprofildienst zu ermöglichen, müssen wir einen Schlüssel zur Identifizierung einer Person und einen Namespace verwenden, der den Schlüssel kontextualisiert. Daher können Sie diese Datenquelle nur verwenden, wenn Ihre Journeys mit einem Ereignis beginnen, das einen Schlüssel und einen Namespace enthält. [Weitere Informationen](../building-journeys/journey.md).

Sie können die vorkonfigurierte Feldergruppe mit dem Namen „ProfileFieldGroup“ bearbeiten, neue hinzufügen und diejenigen entfernen, die nicht in Entwurfs- oder Live-Journeys verwendet werden. [Weitere Informationen](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Sie können die 1.000 neuesten Erlebnisereignisse abrufen, die vor weniger als einem Jahr erstellt wurden.

Die wichtigsten Schritte zum Hinzufügen von Feldergruppen zur integrierten Datenquelle werden unten beschrieben:

1. Wählen Sie aus der Liste der Datenquellen die integrierte Datenquelle **Adobe Experience Platform** aus.

   Dadurch wird der Konfigurationsbereich für die Datenquelle auf der rechten Seite des Bildschirms geöffnet.

   ![](assets/journey23.png)

1. Wählen Sie **[!UICONTROL Neue Feldergruppe hinzufügen]** aus, um eine [neue Reihe abzurufender Felder) ](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Wählen Sie ein Schema aus der Dropdown-Liste **[!UICONTROL Schema]** aus. In diesem Feld werden **Profil** und **Erlebnisereignis** Schemas aufgelistet, die in Adobe Experience Platform verfügbar sind. Die Schemaerstellung erfolgt in Adobe Experience Platform, nicht in Adobe Journey Optimizer.
1. Wählen Sie die zu verwendenden Felder aus und speichern Sie Ihre Änderungen.


>[!TIP]
>
>Bewegen Sie den Mauszeiger über den Namen einer Feldergruppe, um zwei Symbole auf der rechten Seite anzuzeigen. Verwenden Sie diese zum **Duplizieren** oder **Löschen** der Feldergruppe. Das Symbol **[!UICONTROL Löschen]** ist nur verfügbar, wenn die Feldergruppe in keiner der Journey **Live**, **Draft** oder **Finished** verwendet wird. Siehe das Feld **[!UICONTROL Verwendet in]**, um zu überprüfen, ob dies der Fall ist.
