---
solution: Journey Optimizer
product: journey optimizer
title: Zugriffskontrolle auf Objektebene
description: Informationen zur Zugriffskontrolle auf Objektebene
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Zugriffskontrolle auf Objektebene {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Zugriffskontrolle auf Objektebene"
>abstract="Wenn Sie Beschriftungen anwenden, auf die Sie keinen Zugriff haben, wird Ihr Zugriff auf dieses Objekt widerrufen."

>[!IMPORTANT]
>
>Die Zugriffskontrolle auf Objektebene ist derzeit auf ausgewählte Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.

Mit der Zugriffskontrolle auf Objektebene (OLAC) können Sie Berechtigungen zum Verwalten des Datenzugriffs auf eine Auswahl von Objekten definieren:

* Journey
* Kampagne
* Landingpage
* Angebote
* Angebotskollektion
* Angebotsentscheidungen

Sie dient dem Schutz sensibler digitaler Assets vor unbefugten Nutzern, die einen weiteren Schutz personenbezogener Daten ermöglichen.

In Adobe Journey Optimizer können Sie mit OLAC Daten schützen und spezifischen Zugriff auf bestimmte Objekte gewähren.

## Erstellen von Bezeichnungen {#create-assign-labels}

>[!IMPORTANT]
>
>Um Beschriftungen erstellen zu können, müssen Sie Teil einer Rolle mit der **[!UICONTROL Manage usage labels]** Berechtigung.

**[!UICONTROL Labels]** ermöglichen es Ihnen, Datensätze und Felder entsprechend den für diese Daten geltenden Nutzungsrichtlinien zu kategorisieren. **[!UICONTROL Labels]** kann jederzeit angewendet werden, was Ihnen eine flexible Handhabung der Daten ermöglicht.

Sie können Beschriftungen im [!DNL Permissions] Produkt. Weitere Informationen hierzu finden Sie unter [diese Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Labels]** kann auch direkt in Journey Optimizer erstellt werden:

1. Von einem Adobe Journey Optimizer-Objekt aus erstellen Sie hier ein neu erstelltes **[!UICONTROL Campaign]**, klicken Sie auf die **[!UICONTROL Manage access]** Schaltfläche.

   ![](assets/olac_1.png)

1. Aus dem **[!UICONTROL Manage access]** Fenster, klicken Sie auf **[!UICONTROL Create label]**.

   ![](assets/olac_2.png)

1. Konfigurieren Sie den Titel. Geben Sie dazu Folgendes an:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Klicken **[!UICONTROL Create]** speichern Sie Ihre **[!UICONTROL Label]**.

Ihre neu erstellten **[!UICONTROL Label]** ist jetzt in der Liste verfügbar. Bei Bedarf können Sie die Änderungen im [!DNL Permissions] Produkt.

## Zuweisen von Bezeichnungen {#assign-labels}

>[!IMPORTANT]
>
>Um Beschriftungen zuweisen zu können, müssen Sie Teil einer Rolle mit der Berechtigung &quot;Verwalten&quot;sein, d. h. [!DNL Manage journeys], [!DNL Manage Campaigns] oder [!DNL Manage decisions]. Ohne diese Erlaubnis wird die **[!UICONTROL Manage access]** wird ausgegraut.

So weisen Sie Ihren Journey Optimizer-Objekten benutzerdefinierte oder Core-Datennutzungsbezeichnungen zu:

1. Von einem Adobe Journey Optimizer-Objekt aus erstellen Sie hier ein neu erstelltes **[!UICONTROL Campaign]**, klicken Sie auf die **[!UICONTROL Manage access]** Schaltfläche.

   ![](assets/olac_1.png)

1. Aus dem **[!UICONTROL Manage access]** Wählen Sie Ihre benutzerdefinierten oder Core-Datennutzungsbezeichnungen aus, um den Zugriff auf dieses Objekt zu verwalten.

   Weitere Informationen zu den Nutzungsbezeichnungen der Kerndaten finden Sie unter [diese Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Klicken **[!UICONTROL Save]** um diese Beschriftungsbeschränkung anzuwenden.

Um Zugriff auf dieses Objekt zu erhalten, müssen Benutzer über die spezifische **[!UICONTROL Label]** in ihre **[!UICONTROL Roles]**.
Beispiel: Ein Benutzer mit der Beschriftung C1 hat nur Zugriff auf C1-beschriftete oder unbeschriftete Objekte.

Weitere Informationen zur Zuweisung von **[!UICONTROL Label]** zu **[!UICONTROL Role]**, siehe [diese Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
