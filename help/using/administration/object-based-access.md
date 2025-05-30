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
source-git-commit: 3cbda018a1380e13ba3670563240238367517353
workflow-type: ht
source-wordcount: '472'
ht-degree: 100%

---

# Zugriffssteuerung auf Objektebene {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Labels zur Zugriffsverwaltung"
>abstract="Sie können den Zugriff auf ein Objekt anhand von Zugriffs-Labels einschränken. Dies dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten. **Stellen Sie sicher, dass Sie nur Labels auswählen, für die Sie die Berechtigung haben.**"

Sie können den Zugriff auf ein Objekt anhand von Zugriffs-Labels einschränken. Dies dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten.

Mit der Funktion Zugriffssteuerung auf Objektebene (OLAC) können Sie Berechtigungen zum Verwalten des Datenzugriffs für eine Auswahl von Objekten definieren:

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

Um [Labels erstellen](#create-labels) zu können, müssen Sie Teil einer Rolle mit der Berechtigung **[!UICONTROL Verwalten von Nutzungs-Labels]** sein.

Um [Labels zuweisen](#assign-labels) zu können, müssen Sie Teil einer Rolle mit der Berechtigung **Verwalten** sein, d. h. [!DNL Manage journeys], [!DNL Manage Campaigns] oder [!DNL Manage decisions]. Ohne diese Berechtigung ist die Schaltfläche **[!UICONTROL Zugriff verwalten]** ausgegraut.

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/permissions.md).

## Erstellen von Labels {#create-labels}

Mit **[!UICONTROL Bezeichnungen]** können Sie Datensätze und Felder entsprechend den für diese Daten geltenden Nutzungsrichtlinien kategorisieren. **[!UICONTROL Beschriftungen]** können jederzeit angewendet werden, was eine flexible Handhabung der Daten ermöglicht.

Verwenden Sie Labels, um Zugriff für Benutzende bereitzustellen sowie Data Governance- und Einverständnisrichtlinien durchzusetzen. Diese Governance-Labels können sich auf den nachgelagerten Verbrauch auswirken.

Sie können Labels im Produkt [!DNL Permissions] erstellen. Weitere Informationen hierzu finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=de){target="_blank"}.

Sie können **[!UICONTROL Labels]** auch direkt in Journey Optimizer erstellen. Gehen Sie wie folgt vor, um ein Label zu erzeugen:

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

   Weitere Informationen zu Core-Bezeichnungen für die Nutzungsdaten finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de){target="_blank"}.

   ![](assets/olac_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um diese Beschränkung für die Bezeichnung anzuwenden.

Um Zugriff auf dieses Objekt zu erhalten, muss die spezifische **[!UICONTROL Bezeichnung]** in den **[!UICONTROL Rollen]** der Benutzenden enthalten sein.
Beispiel: Eine Benutzerin mit der Bezeichnung C1 hat nur Zugriff auf Objekte mit der Bezeichnung C1 oder ohne Bezeichnung.

Weitere Informationen zur Zuweisung von **[!UICONTROL Bezeichnungen]** zu **[!UICONTROL Rollen]** finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=de#manage-labels-for-a-role){target="_blank"}.