---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen einer Zielgruppendimension
description: Erfahren Sie, wie Sie dem Kundenprofil ein relationales Schema zuordnen.
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: ht
source-wordcount: '372'
ht-degree: 100%

---


# Konfigurieren einer Zielgruppendimension {#configuration}

Mit **[!UICONTROL orchestrierten Kampagnen]** können Sie zielgerichtete Kommunikation auf Entitätsebene gestalten und bereitstellen und dabei die Funktionen von relationalen Schemata von Adobe Experience Platform nutzen. Schemata dienen in Experience Platform zur konsistenten und wiederverwendbaren Beschreibung der Struktur von Daten. Wenn Daten in Experience Platform aufgenommen werden, werden sie nach einem XDM-Schema strukturiert.

Auch wenn die Segmentierung für **[!UICONTROL orchestrierte Kampagnen]** hauptsächlich in relationalen Schemata erfolgt, erfolgt der tatsächliche Nachrichtenversand immer auf der Ebene **Profil**.

Bei der Konfiguration der Zielgruppenbestimmung definieren Sie zwei wichtige Aspekte:

* **Targetierbare Schemata**

  Sie legen fest, welche relationalen Schemata für die Zielgruppenbestimmung infrage kommen. Standardmäßig wird das Schema mit dem Namen `Recipient` verwendet, Sie können jedoch Alternativen wie `Visitors`, `Customers` usw. konfigurieren.

  >[!IMPORTANT]
  >
  > Das Zielschema muss eine 1::1-Beziehung mit dem Schema `Profile` haben. Beispielsweise können Sie `Purchases` nicht als Zielschema verwenden, da es in der Regel eine Eins-zu-viele-Beziehung darstellt.

* **Profilverknüpfung**

  Das System muss verstehen, wie das Zielschema dem `Profile`-Schema zugeordnet ist. Dies wird durch ein gemeinsames Identitätsfeld erreicht, das sowohl im Zielschema als auch im `Profile`-Schema existiert und als Identity-Namespace konfiguriert ist.

## Erstellen einer Zielgruppendimension {#targeting-dimension}

Richten Sie zunächst die Kampagnenorchestrierung ein, indem Sie dem Kundenprofil ein relationales Schema zuordnen.

1. Rufen Sie unter **[!UICONTROL Administration]** das Menü **[!UICONTROL Konfigurationen]** auf und wählen Sie **[!UICONTROL Zieldimension für Kampagne]**.

   ![](assets/target-dimension-1.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um mit der Erstellung Ihrer **[!UICONTROL Zielgruppendimension]** zu beginnen.

1. Wählen Sie Ihr [zuvor konfiguriertes Schema](gs-schemas.md) aus der Dropdown-Liste aus.

   Es sind zwar alle relationalen Schemata sichtbar, doch können nur Schemata mit einer direkten Identitätsbeziehung zum **Profil** ausgewählt werden.

1. Wählen Sie den **[!UICONTROL Identitätswert]** für die Entität aus, die Sie ansprechen möchten.

   In diesem Beispiel ist das Kundenprofil mit mehreren Abonnements verknüpft, die jeweils durch einen eindeutigen `crmID` im `Recipient`-Schema dargestellt werden. Wenn Sie die **[!UICONTROL Zieldimension]** auf die Verwendung des `Recipient`-Schemas und dessen Identität `crmID` festlegen, können Sie Nachrichten auf Abonnementebene anstatt an das Hauptkundenprofil senden. Dadurch wird sichergestellt, dass jeder Vertrag oder jede Zeile eine eigene personalisierte Nachricht erhält.

   [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um die Einrichtung abzuschließen. Beachten Sie, dass eine **[!UICONTROL Zieldimension]** nach ihrer Erstellung nicht mehr entfernt oder bearbeitet werden kann.

Fahren Sie nach der Konfiguration der **[!UICONTROL Zieldimension]** mit der Erstellung und Einrichtung Ihrer **[!UICONTROL Kanalkonfiguration]** fort und definieren Sie die entsprechenden **[!UICONTROL Ausführungsdetails]**.