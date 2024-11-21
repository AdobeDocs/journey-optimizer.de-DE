---
solution: Journey Optimizer
product: journey optimizer
title: Zugriffssteuerung auf Objektebene
description: 'Erfahren Sie mehr über die Zugriffssteuerung auf Objektebene, mit der Sie Berechtigungen zum Verwalten des Datenzugriffs für eine Auswahl von Objekten definieren können:'
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: Objekt, Ebene, Zugriff, Kontrolle, Kennzeichnungen, OLAC, Autorisierung
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 60%

---

# Zugriffssteuerung auf Objektebene {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Kennzeichnungen zur Zugriffsverwaltung"
>abstract="Sie können den Zugriff auf diese Kampagne anhand von Zugriffsbeschriftungen einschränken. Um eine Zugriffsbeschränkung hinzuzufügen, navigieren Sie zur Schaltfläche **Zugriff verwalten** oben auf dieser Seite. Stellen Sie sicher, dass Sie nur Beschriftungen auswählen, für die Sie berechtigt sind."

Mit der Funktion Zugriffskontrolle auf Objektebene (OLAC) können Sie Berechtigungen zum Verwalten des Datenzugriffs auf eine Auswahl von Objekten definieren:

* Journey
* Campaign
* Vorlage
* Fragment
* Landingpage
* Angebot
* Statische Angebotssammlung
* Angebotsentscheidung
* Kanalkonfiguration
* IP-Aufwärmplan

Sie dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten.

## Voraussetzungen {#prereq-labels}

Um [Beschriftungen erstellen](#create-labels) zu können, müssen Sie Teil einer Rolle sein, die über die Berechtigung **[!UICONTROL Nutzungsbezeichnungen verwalten]** verfügt.

Um [Beschriftungen zuweisen](#assign-labels) zu können, müssen Sie Teil einer Rolle mit der Berechtigung **Verwalten** sein, d. h. [!DNL Manage journeys], [!DNL Manage Campaigns] oder [!DNL Manage decisions]. Ohne diese Berechtigung ist die Schaltfläche **[!UICONTROL Zugriff verwalten]** grau ausgeblendet.

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/permissions.md).

## Erstellen von Kennzeichnungen {#create-labels}

Mit **[!UICONTROL Bezeichnungen]** können Sie Datensätze und Felder entsprechend den für diese Daten geltenden Nutzungsrichtlinien kategorisieren. **[!UICONTROL Beschriftungen]** können jederzeit angewendet werden, was eine flexible Handhabung der Daten ermöglicht.

Verwenden Sie Beschriftungen, um den Zugriff für Benutzer bereitzustellen sowie Data Governance- und Zustimmungsrichtlinien zu erzwingen. Diese Governance-Beschriftungen können sich auf den nachgelagerten Verbrauch auswirken.

Sie können Bezeichnungen im Produkt [!DNL Permissions] erstellen. Weitere Informationen hierzu finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=de){target="_blank"}.

Sie können auch **[!UICONTROL Beschriftungen]** direkt in Journey Optimizer erstellen. Gehen Sie wie folgt vor, um eine Bezeichnung zu erstellen:

1. Klicken Sie in einem Objekt in Adobe Journey Optimizer auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**, wie hier an einer neu erstellten **[!UICONTROL Kampagne]** gezeigt.

   ![](assets/olac_1.png)

1. Klicken Sie im Fenster **[!UICONTROL Zugriff verwalten]** auf **[!UICONTROL Bezeichnung erstellen]**.

   ![](assets/olac_2.png)

1. Konfigurieren Sie die Bezeichnung. Geben Sie dazu Folgendes an:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Anzeigename]**
   * **[!UICONTROL Beschreibung]**

   ![](assets/olac_3.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um Ihre **[!UICONTROL Bezeichnung]** zu speichern.

Ihre neu erstellte **[!UICONTROL Bezeichnung]** ist jetzt in der Liste verfügbar. Bei Bedarf können Sie sie im Produkt [!DNL Permissions] ändern.

## Zuweisen von Bezeichnungen {#assign-labels}

So weisen Sie Ihren Objekten in Journey Optimizer benutzerdefinierte oder Core-Bezeichnungen für die Datennutzung zu:

1. Klicken Sie in einem Objekt in Adobe Journey Optimizer auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**, wie hier an einer neu erstellten **[!UICONTROL Kampagne]** gezeigt.

   ![](assets/olac_1.png)

1. Wählen Sie im Fenster **[!UICONTROL Zugriff verwalten]** Ihre benutzerdefinierte(n) oder Core-Bezeichnungen(en) für die Datennutzung aus, um den Zugriff auf dieses Objekt zu verwalten.

   Weitere Informationen zu den Kerndatennutzungsbezeichnungen finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de){target="_blank"}.

   ![](assets/olac_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um diese Beschränkung für die Bezeichnung anzuwenden.

Um Zugriff auf dieses Objekt zu erhalten, muss die spezifische **[!UICONTROL Bezeichnung]** in den **[!UICONTROL Rollen]** der Benutzenden enthalten sein.
Beispiel: Eine Benutzerin mit der Bezeichnung C1 hat nur Zugriff auf Objekte mit der Bezeichnung C1 oder ohne Bezeichnung.

Weitere Informationen zum Zuweisen von **[!UICONTROL Beschriftung]** zu einer **[!UICONTROL Rolle]** finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=de#manage-labels-for-a-role){target="_blank"}.