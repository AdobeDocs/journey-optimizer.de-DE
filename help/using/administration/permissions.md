---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Benutzenden und Produkten
description: Erfahren Sie, wie Sie Benutzer und Rollen verwalten
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: Produkt, Profile, Sandbox
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 26%

---

# Verwalten von Benutzenden und Produkten {#manage-permissions}

>[!IMPORTANT]
>
> Die einzelnen im Folgenden beschriebenen Verfahren können nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Rollen]** eine Sammlung von Benutzern referenzieren, die dieselben Berechtigungen und Sandboxes verwenden. Mit diesen Rollen können Sie den Zugriff und die Berechtigungen für verschiedene Benutzergruppen in Ihrer Organisation einfach verwalten.

Mit dem [!DNL Journey Optimizer] -Produkt können Sie aus einer Reihe bereits vorhandener **[!UICONTROL Rollen]**, mit jeweils unterschiedlichen Berechtigungen, die Sie Ihren Benutzern zuweisen können. Weitere Informationen über **[!UICONTROL Rollen]**, siehe hierzu [page](ootb-product-profiles.md).

Wenn ein Benutzer zu einer **[!UICONTROL Rolle]**, erhalten sie Zugriff auf die Adobe-Apps und -Dienste, die im Produkt enthalten sind.

Wenn die bereits vorhandenen Rollen nicht den spezifischen Anforderungen Ihres Unternehmens entsprechen, können Sie auch benutzerdefinierte **[!UICONTROL Rollen]** , um den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zu optimieren. Auf diese Weise können Sie sicherstellen, dass jeder Benutzer nur Zugriff auf die Ressourcen und Tools hat, die er benötigt, um seine Aufgaben effizient durchzuführen.

## Rollen zuweisen {#assigning-role}

Sie können eine vordefinierte oder benutzerdefinierte **[!UICONTROL Rolle]** an Ihre Benutzer.

Die Liste aller vordefinierten Rollen mit zugewiesenen Berechtigungen finden Sie im Abschnitt [Integrierte Rollen](ootb-product-profiles.md) Abschnitt.

So weisen Sie eine **[!UICONTROL Rolle]**:

1. So weisen Sie Benutzern eine Rolle im [!DNL Permissions] Produkt, navigieren Sie zur **[!UICONTROL Rollen]** und wählen Sie die gewünschte Rolle aus.

   ![](assets/do-not-localize/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Geben Sie den Namen oder die E-Mail-Adresse Ihres Benutzers ein oder wählen Sie den Benutzer aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn der Benutzende vorher noch nicht in der [!DNL Admin Console] erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zur Instanz erhalten.

Weiterführende Informationen zur Benutzerverwaltung finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Beim Zugriff auf die Instanz wird Ihrem Benutzer je nach den zugewiesenen Berechtigungen in der **[!UICONTROL Rolle]**. Wenn der Benutzende nicht den richtigen Zugriff auf eine Funktion hat, wird die folgende Meldung angezeigt:

`You don't have permission to access this feature. Permission needed: XX.`

## Vorhandene Rolle bearbeiten {#edit-product-profile}

Für native oder benutzerdefinierte **[!UICONTROL Rollen]** können Sie jederzeit Berechtigungen hinzufügen oder löschen.

In diesem Beispiel möchten wir **[!UICONTROL Berechtigungen]** im Zusammenhang mit **[!UICONTROL Journey]** -Ressource für Benutzer, die dem Journey-Viewer zugewiesen sind **[!UICONTROL Rolle]**. Diese Benutzenden können dann Journeys veröffentlichen.

Beachten Sie Folgendes: Wenn Sie eine vordefinierte oder benutzerdefinierte **[!UICONTROL Rolle]**, wirkt sich dies auf jeden Benutzer aus, der dieser **[!UICONTROL Rolle]**.

1. So weisen Sie Benutzern eine Rolle im [!DNL Permissions] Produkt, navigieren Sie zur **[!UICONTROL Rollen]** Registerkarte und wählen Sie die gewünschte Rolle aus, hier den Journey-Viewer **[!UICONTROL Rolle]**.
   ![](assets/do-not-localize/access_control_5.png)

1. Von Ihrem **[!UICONTROL Rolle]** Dashboard, klicken Sie auf **[!UICONTROL Bearbeiten]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Die **[!UICONTROL Ressourcen]** zeigt die Liste der Ressourcen an, die für die **[!UICONTROL Experience Cloud - Plattformbasierte Anwendungen]** Produkt. Ziehen Sie Ressourcen in den Arbeitsbereich, um Berechtigungen zuzuweisen.

   Aus dem **[!UICONTROL Journey]** Ressourcen-Dropdown, wählen wir hier die Journey Veröffentlichen aus. **[!UICONTROL Berechtigung]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Bei Bedarf können Sie unter **[!UICONTROL Eingeschlossene Berechtigungselemente]** klicken Sie auf das X-Symbol neben, um Berechtigungen oder Ressourcen für Ihre Rolle zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Bei Bedarf können Sie auch eine neue Rolle mit bestimmten Berechtigungen erstellen. Weitere Informationen hierzu finden Sie unter [Neue Rolle erstellen](#create-product-profile).

## Erstellen einer neuen Rolle {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene **[!UICONTROL Rollen]** und weisen Sie Ihren Benutzern eine Reihe von Berechtigungen und Sandboxes zu. Mit **[!UICONTROL Rollen]** können Sie den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

In diesem Beispiel erstellen wir eine Rolle mit dem Namen **Journey schreibgeschützt** wo wir Leseberechtigungen für die Journey-Funktion erteilen. Benutzende können nur auf Journeys zugreifen und diese anzeigen, können aber nicht auf andere Funktionen wie **[!DNL  Decision management]** oder [!DNL Journey Optimizer] zugreifen.

Erstellen Sie unsere **Journey schreibgeschützt** **[!UICONTROL Rolle]**:

1. So weisen Sie Benutzern eine Rolle im [!DNL Permissions] Produkt, navigieren Sie zur **[!UICONTROL Rollen]** Registerkarte und klicken Sie auf **[!UICONTROL Rolle erstellen]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Hinzufügen einer **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** für neue **[!UICONTROL Rolle]**. Klicken Sie anschließend auf **[!UICONTROL Bestätigen]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Aus dem **[!UICONTROL Sandbox]** Ressourcen-Dropdown auswählen, welche Sandbox(s) Sie Ihrer **[!UICONTROL Rolle]**. [Erfahren Sie mehr über Sandboxes](sandboxes.md)

   ![](assets/do-not-localize/access_control_13.png)

1. Wählen Sie zwischen den verschiedenen Ressourcen aus, z. B. **[!DNL Journeys]**, **[!DNL Segments]** oder **[!DNL Decision management]** verfügbar unter [!DNL Journey Optimizer] im Menü auf der linken Seite.

   Hier wählen wir die **[!UICONTROL Journey]** Ressource.

   ![](assets/do-not-localize/access_control_11.png)

1. Aus dem **[!UICONTROL Journey]** in der Dropdown-Liste die Berechtigungen auswählen, die Sie Ihrem **[!UICONTROL Rolle]**.

   Hier wählen wir **[!DNL View journeys]**, **[!DNL View journeys report]**  und **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihre **[!UICONTROL Rolle]** wurde erstellt und konfiguriert. Jetzt müssen Sie es den Benutzenden zuweisen.

Weiterführende Informationen zur Erstellung und Verwaltung von Rollen finden Sie im Abschnitt [Dokumentation zur Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=de).