---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen der Zielgruppendimension
description: Erfahren Sie, wie Sie dem Kundenprofil ein relationales Schema zuordnen.
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 3%

---


# Konfigurieren einer Zielgruppendimension {#configuration}

Mit **[!UICONTROL Orchestrierten Kampagnen]** können Sie zielgerichtete Kommunikation auf Entitätsebene entwerfen und bereitstellen und dabei die relationalen Schemafunktionen von Adobe Experience Platform nutzen. Schemata dienen in Experience Platform zur konsistenten und wiederverwendbaren Beschreibung der Struktur von Daten. Wenn Daten in Experience Platform aufgenommen werden, werden sie nach einem XDM-Schema strukturiert.

Obwohl die Segmentierung für **[!UICONTROL orchestrierte Kampagnen]** hauptsächlich auf relationalen Schemata erfolgt, erfolgt der tatsächliche Nachrichtenversand immer auf der Ebene **Profil**.

Bei der Konfiguration der Zielgruppenbestimmung definieren Sie zwei wichtige Aspekte:

* **Zielgruppenschemata**

  Sie legen fest, welche relationalen Schemata für die Zielgruppenbestimmung infrage kommen. Standardmäßig wird das Schema mit dem Namen `Recipient` verwendet, Sie können jedoch Alternativen wie `Visitors`, `Customers` usw. konfigurieren.

  >[!IMPORTANT]
  >
  > Das Zielschema muss eine 1::1-Beziehung mit dem `Profile` Schema haben. Beispielsweise können Sie `Purchases` nicht als Zielschema verwenden, da es normalerweise eine Eins-zu-viele-Beziehung darstellt.

* **Profilverknüpfung**

  Das System muss verstehen, wie das Zielschema dem `Profile` Schema zugeordnet wird. Dies wird durch ein gemeinsames Identitätsfeld erreicht, das sowohl im Zielschema als auch im `Profile` existiert und als Identity-Namespace konfiguriert ist.

## Erstellen der Zielgruppendimension {#targeting-dimension}

Richten Sie zunächst die Kampagnenorchestrierung ein, indem Sie dem Kundenprofil ein relationales Schema zuordnen.

1. Rufen Sie **[!UICONTROL Administration]** das Menü **[!UICONTROL Konfigurationen]** auf und wählen Sie **[!UICONTROL Campaign Target Dimension]**.

   ![](assets/target-dimension-1.png)

1. Klicken Sie **[!UICONTROL Erstellen]**, um mit der Erstellung Ihrer **[!UICONTROL Zielgruppendimension]** zu beginnen.

1. Wählen Sie Ihr [zuvor konfiguriertes Schema](gs-schemas.md) aus &#x200B; Dropdown-Liste aus.

   Während alle relationalen Schemata sichtbar sind, können nur Schemata mit einer direkten Identitätsbeziehung zum **Profil** ausgewählt werden.

1. Wählen Sie den **[!UICONTROL Identitätswert]** für die Entität aus, die Sie ansprechen möchten.

   In diesem Beispiel ist das Kundenprofil mit mehreren Abonnements verknüpft, die jeweils durch eine eindeutige `crmID` im `Recipient` dargestellt werden. Wenn Sie die **[!UICONTROL Target Dimension]** auf die Verwendung des `Recipient` Schemas und dessen `crmID` festlegen, können Sie Nachrichten auf Abonnementebene und nicht an das Hauptkundenprofil senden, um sicherzustellen, dass jeder Vertrag oder jede Zeile eine eigene personalisierte Nachricht erhält.

   [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity).

   ![](assets/target-dimension-2.png)

1. Klicken Sie **[!UICONTROL Speichern]**, um die Einrichtung abzuschließen. Beachten Sie, dass eine **[!UICONTROL Zieldimension]** nach ihrer Erstellung nicht mehr entfernt oder bearbeitet werden kann.

Fahren Sie nach der Konfiguration **[!UICONTROL Target-Dimension]** mit der Erstellung und Einrichtung Ihrer **[!UICONTROL Kanalkonfiguration]** fort und definieren Sie die entsprechenden **[!UICONTROL Ausführungsdetails]**.

## Konfigurieren der Kanalkonfiguration {#channel-configuration}

Nach der Einrichtung Ihrer **[!UICONTROL Target Dimension]** müssen Sie Ihre E-Mail- oder SMS-**[!UICONTROL Kanalkonfiguration]** konfigurieren und die entsprechenden **[!UICONTROL Ausführungsdetails]** definieren. Auf diese Weise können Sie definieren:

* **Die Ebene des Nachrichtenversands** z. B. eine Nachricht pro Empfänger, z. B. eine einzelne E-Mail pro Person.

* **Die Ausführungsadresse**: Das spezifische Kontaktfeld, das zum Senden verwendet werden soll, z. B. eine E-Mail-Adresse oder Telefonnummer.

So konfigurieren Sie die Kanalkonfiguration:

1. Erstellen und konfigurieren Sie zunächst Ihre **[!UICONTROL Kanalkonfiguration]**.

   Sie können auch eine vorhandene **[!UICONTROL Kanalkonfiguration“]**.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus](../email/surface-personalization.md)

1. Rufen Sie im **[!UICONTROL Ausführungsdetails]** Ihrer **[!UICONTROL Kanalkonfiguration]** die Registerkarte **[!UICONTROL Orchestrierte Kampagnen]** auf.

   ![](assets/target-dimension-3.png)

1. Klicken Sie auf **[!UICONTROL Aktiviert]**, um sie mit orchestrierten Kampagnen kompatibel zu machen.

1. Wählen Sie Ihre Versandmethode:

   * **[!UICONTROL Target Dimension]**: An die primäre Entität, z. B. den Empfänger, senden.

   * **[!UICONTROL Target + Sekundäre Dimension]**: Senden Sie Daten sowohl über primäre als auch sekundäre Entitäten, z. B. Empfänger + Vertrag.

1. Wählen Sie aus der Dropdown-Liste Ihre [zuvor erstellte Target-Dimension](#targeting-dimension) aus.

   ![](assets/target-dimension-4.png)

1. Wenn Sie **[!UICONTROL Target + Sekundäre Dimension]** als Versandmethode ausgewählt haben, wählen Sie eine **[!UICONTROL Sekundäre Dimension]**, um den Kontext für den Nachrichtenversand zu definieren.

1. Wählen Sie **[!UICONTROL Abschnitt]** Ausführungsadresse) aus, welche **[!UICONTROL Source]** zum Abrufen der Versandadresse verwendet werden soll, z. B. die E-Mail-Adresse oder Telefonnummer:

   * **[!UICONTROL Profil]**: Wählen Sie diese Option aus, wenn die Versandadresse, z. B. die E-Mail, direkt im Hauptkundenprofil gespeichert wird.

     Nützlich beim Senden von Nachrichten an den Hauptkunden, nicht an eine bestimmte zugehörige Entität.

   * **[!UICONTROL Target Dimension]**: Wählen Sie diese Option, wenn die Versandadresse in der Hauptentität, z. B. einer Empfängerin oder einem Empfänger, gespeichert ist.

     Dies ist nützlich, wenn jeder Empfänger eine eigene Versandadresse hat, z. B. eine andere E-Mail-Adresse oder Telefonnummer.

   * **[!UICONTROL Sekundäre Dimension]**: Wählen Sie bei Verwendung von **[!UICONTROL Target + Sekundäre Dimension]** als Versandmethode die entsprechende **[!UICONTROL Sekundäre Dimension]**, die Sie zuvor konfiguriert haben.

     Wenn die sekundäre Dimension beispielsweise eine Buchung oder ein Abonnement darstellt, kann die Ausführungsadresse, z. B. eine E-Mail, aus dieser Ebene übernommen werden. Dies ist nützlich, wenn Profile bei der Buchung oder beim Abonnieren eines Service andere Kontaktdetails verwenden.

1. Klicken Sie im Feld **[!UICONTROL Versandadresse]** auf ![Bearbeiten](assets/do-not-localize/edit.svg), um das spezifische Feld auszuwählen, das für Ihren Nachrichtenversand verwendet werden soll.

   ![](assets/target-dimension-4.png)

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Senden]**.

Ihr Kanal kann jetzt mit &quot;**Kampagnen“ verwendet** und Nachrichten werden entsprechend der ausgewählten Zielgruppendimension zugestellt.
