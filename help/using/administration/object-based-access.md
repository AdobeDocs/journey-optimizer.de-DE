---
title: Zugriffskontrolle auf Objektebene
description: Erfahren Sie mehr über die Zugriffskontrolle auf Objektebene.
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 40061255a2fcec3de1b39a168cadbdedd2e12d87
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 14%

---

# Zugriffskontrolle auf Objektebene {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Zugriffskontrolle auf Objektebene"
>abstract="Wenn Sie Beschriftungen anwenden, auf die Sie keinen Zugriff haben, wird Ihr Zugriff auf dieses Objekt widerrufen."

Mit der Zugriffskontrolle auf Objektebene (OLAC) können Sie Berechtigungen zum Verwalten des Datenzugriffs auf eine Auswahl von Objekten definieren:

* Journey
* Campaign
* Landing page
* Angebote
* Angebotskollektion
* Offer decisioning

Sie dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzern und ermöglicht so einen weiteren Schutz personenbezogener Daten.

In Adobe Journey Optimizer können Sie mit OLAC Daten schützen und spezifischen Zugriff auf bestimmte Objekte gewähren.

## Erstellen von Bezeichnungen {#create-assign-labels}

>[!IMPORTANT]
>
>Um Beschriftungen erstellen zu können, müssen Sie Teil einer Rolle mit der **[!UICONTROL Verwalten von Nutzungsbezeichnungen]** Berechtigung.

**[!UICONTROL Bezeichnungen]** ermöglichen es Ihnen, Datensätze und Felder entsprechend den für diese Daten geltenden Nutzungsrichtlinien zu kategorisieren. **[!UICONTROL Beschriftungen können jederzeit angewendet werden, was eine flexible Handhabung der Daten ermöglicht.]**

Sie können Beschriftungen im [!DNL Permissions] Produkt. Weitere Informationen hierzu finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Bezeichnungen]** kann auch direkt in Journey Optimizer erstellt werden:

1. Von einem Adobe Journey Optimizer-Objekt aus erstellen Sie hier ein neu erstelltes **[!UICONTROL Kampagne]**, klicken Sie auf die **[!UICONTROL Zugriff verwalten]** Schaltfläche.

   ![](assets/olac_1.png)

1. Aus dem **[!UICONTROL Zugriff verwalten]** Fenster, klicken Sie auf **[!UICONTROL Titel erstellen]**.

   ![](assets/olac_2.png)

1. Konfigurieren Sie den Titel. Geben Sie dazu Folgendes an:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Anzeigename]**
   * **[!UICONTROL Beschreibung]**

   ![](assets/olac_3.png)

1. Klicken **[!UICONTROL Erstellen]** speichern Sie Ihre **[!UICONTROL Titel]**.

Ihre neu erstellten **[!UICONTROL Titel]** ist jetzt in der Liste verfügbar. Bei Bedarf können Sie die Änderungen im [!DNL Permissions] Produkt.

## Zuweisen von Bezeichnungen {#assign-labels}

>[!IMPORTANT]
>
>Um Beschriftungen zuweisen zu können, müssen Sie Teil einer Rolle mit der Berechtigung &quot;Verwalten&quot;sein, d. h. [!DNL Manage journeys], [!DNL Manage Campaigns] oder [!DNL Manage decisions]. Ohne diese Erlaubnis wird die **[!UICONTROL Zugriff verwalten]** wird ausgegraut.

So weisen Sie Ihren Journey Optimizer-Objekten benutzerdefinierte oder zentrale Datennutzungsbezeichnungen zu:

1. Von einem Adobe Journey Optimizer-Objekt aus erstellen Sie hier ein neu erstelltes **[!UICONTROL Kampagne]**, klicken Sie auf die **[!UICONTROL Zugriff verwalten]** Schaltfläche.

   ![](assets/olac_1.png)

1. Aus dem **[!UICONTROL Zugriff verwalten]** Wählen Sie Ihre benutzerdefinierten oder Core-Datennutzungsbezeichnungen aus, um den Zugriff auf dieses Objekt zu verwalten.

   Weitere Informationen zu den Nutzungsbezeichnungen der Kerndaten finden Sie unter [diese Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de).

   ![](assets/olac_4.png)

1. Klicken **[!UICONTROL Speichern]** um diese Beschriftungsbeschränkung anzuwenden.

Um Zugriff auf dieses Objekt zu erhalten, müssen Benutzer über die spezifische **[!UICONTROL Titel]** in ihre **[!UICONTROL Rollen]**.

Weitere Informationen zur Zuweisung von **[!UICONTROL Titel]** zu **[!UICONTROL Rolle]**, siehe [diese Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).



