---
solution: Journey Optimizer
product: journey optimizer
title: Datenquelle von Adobe Experience Platform
description: Erfahren Sie, wie Sie die Datenquelle von Adobe Experience Platform konfigurieren
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: integriert, Quelle, Daten, Plattform, Integration
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
TQID: https://experienceleague.adobe.com/tvO8GjVADFHV1i6ff5krss2YyS-rtnQZ4BHcvvhG-t4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e366af78935405cd5acb15269194875098b20914
workflow-type: tm+mt
source-wordcount: 481
ht-degree: 87%

---

# Datenquelle von Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Sie Feldergruppen in der integrierten Adobe Experience Platform-Datenquelle ein, damit Sie Echtzeit-Kundenprofildaten in Ihren Journey abrufen und verwenden können.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Datenquelle von Adobe Experience Platform"
>abstract="Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Sie dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofil-Service (Sie können damit beispielsweise überprüfen, ob es sich bei einer Person, die in eine Journey eingetreten ist, um eine Frau handelt)."

Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ist integriert und vorkonfiguriert und kann nicht gelöscht werden. Diese Datenquelle dient zum Abrufen und Verwenden von Daten aus dem Echtzeit-Kundenprofildienst (überprüfen Sie beispielsweise, ob es sich bei der Person, die in eine Journey eingetreten ist, um eine Frau handelt). Weitere Informationen zum Adobe Echtzeit-Kundenprofil finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de){target="_blank"}.

Um die Verbindung zum Echtzeit-Kundenprofildienst zu ermöglichen, müssen wir einen Schlüssel zur Identifizierung einer Person und einen Namespace verwenden, der den Schlüssel kontextualisiert. Daher können Sie diese Datenquelle nur verwenden, wenn Ihre Journeys mit einem Ereignis beginnen, das einen Schlüssel und einen Namespace enthält. [Weitere Informationen](../building-journeys/journey.md).

Sie können die vorkonfigurierte Feldergruppe mit dem Namen „ProfileFieldGroup“ bearbeiten, neue hinzufügen und diejenigen entfernen, die nicht in Entwurfs- oder Live-Journeys verwendet werden. [Weitere Informationen](../datasource/configure-data-sources.md#define-field-groups).

>[!CAUTION]
>
>Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht unterstützt. Wenn Ihr Anwendungsfall die Verwendung von Erlebnisereignissen erfordert, sollten Sie alternative Methoden in Betracht ziehen. [Weitere Informationen](../building-journeys/exp-event-lookup.md)

Im Folgenden finden Sie die wichtigsten Schritte, um der integrierten Datenquelle Feldergruppen hinzuzufügen:

1. Wählen Sie in der Liste der Datenquellen die integrierte Datenquelle von **Adobe Experience Platform** aus.

   Dadurch wird der Konfigurationsbereich für die Datenquelle auf der rechten Seite des Bildschirms geöffnet.

   ![](assets/journey23.png)

1. Wählen Sie **[!UICONTROL Neue Feldergruppe hinzufügen]** aus, um eine [neue Reihe von Feldern zum Abrufen](../datasource/configure-data-sources.md#define-field-groups) zu definieren.

   ![](assets/journey24.png)

1. Wählen Sie ein Schema aus der Dropdown-Liste **[!UICONTROL Schema]** aus. Die Schemaerstellung erfolgt in Adobe Experience Platform, nicht in Adobe Journey Optimizer.

   >[!NOTE]
   >
   >In der [!DNL Journey Optimizer] Data Source-Konfiguration werden nur XDM Individual Profile-basierte Schemata unterstützt. Weitere Informationen finden Sie unter [Klasse „XDM Individual Profile](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile){target="_blank"}.

1. Wählen Sie die zu verwendenden Felder aus und speichern Sie Ihre Änderungen.

>[!TIP]
>
>Bewegen Sie den Mauszeiger über den Namen einer Feldergruppe, um zwei Symbole auf der rechten Seite anzuzeigen. Verwenden Sie diese zum **Duplizieren** oder **Löschen** der Feldergruppe. Beachten Sie, dass das Symbol **[!UICONTROL Löschen]** nur verfügbar ist, wenn die Feldergruppe in keiner **Live**- oder **Entwurfs**-Journey und in keiner **abgeschlossenen** Journey verwendet wird. Überprüfen Sie im Feld **[!UICONTROL Verwendet in]**, ob dies der Fall ist.
