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
source-git-commit: 8b0310e91e5b5c1418e8e26f4505bda45146ceba
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 56%

---

# Zugriffssteuerung auf Objektebene {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Labels zur Zugriffsverwaltung"
>abstract="Sie können den Zugriff auf ein Objekt anhand von Zugriffs-Labels einschränken. Dieser Ansatz schützt sensible digitale Assets vor unbefugten Benutzenden und sorgt für einen weiteren Schutz personenbezogener Daten. **Stellen Sie sicher, dass Sie nur Labels auswählen, für die Sie die Berechtigung haben.**"

Sie können den Zugriff auf ein Objekt anhand von Zugriffs-Labels einschränken. Dieser Ansatz schützt sensible digitale Assets vor unbefugten Nutzern und sorgt für einen weiteren Schutz personenbezogener Daten.

Mit der OLAC-Funktion (Object Level Access Control) können Sie Berechtigungen definieren, um den Datenzugriff für eine Auswahl von Objekten zu verwalten:

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


## Voraussetzungen {#prereq-labels}

Um Bezeichnungen erstellen [ können](#create-labels) müssen Sie einer Rolle mit der Berechtigung **[!UICONTROL Verwalten von Nutzungsbezeichnungen]** angehören.

Um Bezeichnungen zuweisen [ können](#assign-labels) müssen Sie einer Rolle mit der Berechtigung **Verwalten** angehören, d. h. [!DNL Manage journeys], [!DNL Manage Campaigns] oder [!DNL Manage decisions]. Ohne diese Berechtigung ist die Schaltfläche **[!UICONTROL Zugriff verwalten]** ausgegraut.

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/permissions.md).

## Erstellen von Labels {#create-labels}

Mit **[!UICONTROL Bezeichnungen]** können Sie Datensätze und Felder entsprechend den für diese Daten geltenden Nutzungsrichtlinien kategorisieren. **[!UICONTROL Beschriftungen]** können jederzeit angewendet werden, was eine flexible Handhabung der Daten ermöglicht.

Verwenden Sie Kennzeichnungen, um Benutzenden Zugriff zu gewähren, und setzen Sie die Richtlinien zu Data Governance und Einverständnis durch. Diese Governance-Labels können sich auf den nachgelagerten Verbrauch auswirken.

Sie können Labels im Produkt [!DNL Permissions] erstellen. Weitere Informationen finden Sie in der Dokumentation zu [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=de){target="_blank"}.

Sie können **[!UICONTROL Labels]** auch direkt in Journey Optimizer erstellen. Gehen Sie wie folgt vor, um ein Label zu erzeugen:

1. Klicken Sie in einem Adobe Journey Optimizer-Objekt, z. B. einer neu erstellten **[!UICONTROL Kampagne]**, auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**.

   ![Verwalten der Zugriffsschaltfläche in Adobe Journey Optimizer](assets/olac_1.png)

1. Klicken Sie im Fenster **[!UICONTROL Zugriff verwalten]** auf **[!UICONTROL Bezeichnung erstellen]**.

   ![](assets/olac_2.png)

1. Konfigurieren Sie Ihre Bezeichnung. Sie müssen Folgendes angeben:

   * **[!UICONTROL Name]**
   * **[!UICONTROL Anzeigename]**
   * **[!UICONTROL Beschreibung]**

   ![Beschriften von Konfigurationsfeldern](assets/olac_3.png)

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um Ihre **[!UICONTROL Bezeichnung]** zu speichern.

Ihre neu erstellte **[!UICONTROL Bezeichnung]** ist jetzt in der Liste verfügbar. Bei Bedarf können Sie sie im Produkt [!DNL Permissions] ändern.

## Zuweisen von Bezeichnungen {#assign-labels}

So weisen Sie Ihren Objekten in Journey Optimizer benutzerdefinierte oder Core-Bezeichnungen für die Datennutzung zu:

1. Klicken Sie in einem Adobe Journey Optimizer-Objekt, z. B. einer neu erstellten **[!UICONTROL Kampagne]**, auf die Schaltfläche **[!UICONTROL Zugriff verwalten]**.

   ![Verwalten der Zugriffsschaltfläche in Adobe Journey Optimizer](assets/olac_1.png)

1. Wählen Sie im Fenster **[!UICONTROL Zugriff verwalten]** Ihre benutzerdefinierte(n) oder Core-Bezeichnungen(en) für die Datennutzung aus, um den Zugriff auf dieses Objekt zu verwalten.

   Weitere Informationen zu Core-Bezeichnungen für die Nutzungsdaten finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de){target="_blank"}.

   ![](assets/olac_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um diese Beschränkung für die Bezeichnung anzuwenden.

Um auf dieses Objekt zugreifen zu können, müssen die Benutzer das spezifische **[!UICONTROL Label]** in ihren **[!UICONTROL Rollen]** haben. Beispielsweise hat ein Benutzer mit der Kennzeichnung C1 nur Zugriff auf Objekte mit der Kennzeichnung C1 oder ohne Kennzeichnung.

Weitere Informationen zum Zuweisen eines **[!UICONTROL Titels]** zu einer **[!UICONTROL Rolle]** finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=de#manage-labels-for-a-role){target="_blank"}.
