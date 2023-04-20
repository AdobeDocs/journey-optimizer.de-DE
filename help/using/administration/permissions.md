---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Benutzenden und Produktprofilen
description: Erfahren Sie, wie Sie Benutzende und Produktprofile verwalten
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: Produkt, Profile, Sandbox
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 100%

---

# Verwalten von Benutzenden und Produktprofilen {#manage-permissions}

>[!IMPORTANT]
>
> Die einzelnen im Folgenden beschriebenen Verfahren können nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Produktprofile]** sind Gruppen von Benutzenden, die innerhalb Ihrer Organisation die gleichen Berechtigungen und Sandboxes nutzen.

Mit [!DNL Journey Optimizer] können Sie aus verschiedenen vorkonfigurierten **[!UICONTROL Produktprofilen]** mit unterschiedlichen Berechtigungsebenen auswählen, die Sie Ihren Benutzenden zuweisen können. Weitere Informationen zu den verfügbaren **[!UICONTROL Produktprofilen]** finden Sie auf dieser [Seite](ootb-product-profiles.md).

Jeder Benutzende, der einem **[!UICONTROL Produktprofil]** angehört, hat die Berechtigung für die Adobe-Anwendungen und -Services, die im Produkt enthalten sind.

Sie können auch eigene **[!UICONTROL Produktprofile]** erstellen, wenn Sie den Zugriff Ihrer Benutzenden auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche präziser definieren möchten.

## Zuweisen eines Produktprofils {#assigning-product-profile}

Sie können festlegen, dass Ihren Benutzenden ein vorkonfiguriertes oder ein benutzerdefiniertes **[!UICONTROL Produktprofil]** zugewiesen wird.

Die Liste aller vorkonfigurierten Produktprofile mit zugewiesenen Berechtigungen finden Sie im Abschnitt [Integrierte Produktprofile](ootb-product-profiles.md).

So weisen Sie ein **[!UICONTROL Produktprofil]** zu:

1. Wählen Sie in der [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. **[!UICONTROL Produktprofil]** auswählen.

   ![](assets/do-not-localize/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzende hinzufügen]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Geben Sie den Namen oder die E-Mail-Adresse des Benutzenden ein und wählen Sie den Benutzenden aus.

   Wenn der Benutzende vorher noch nicht in der [!DNL Admin Console] erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Führen Sie die gleichen Schritte wie oben aus, um weitere Benutzende zu Ihrem **[!UICONTROL Produktprofil]** hinzuzufügen. Klicken Sie dann auf **[!UICONTROL Speichern]**.

Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zur Instanz erhalten.

Weiterführende Informationen zur Benutzerverwaltung finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Beim Zugriff auf die Instanz wird Ihren Benutzenden je nach den im **[!UICONTROL Produktprofil]** zugewiesenen Berechtigungen eine bestimmte Ansicht angezeigt. Wenn der Benutzende nicht den richtigen Zugriff auf eine Funktion hat, wird die folgende Meldung angezeigt:

`You don't have permission to access this feature. Permission needed: XX.`

## Bearbeiten eines vorhandenen Produktprofils {#edit-product-profile}

Für vorkonfigurierte oder benutzerdefinierte **[!UICONTROL Produktprofile]** können Sie jederzeit Berechtigungen hinzufügen oder löschen.

In diesem Beispiel möchten wir **[!UICONTROL Berechtigungen]** im Zusammenhang mit der Funktion **[!UICONTROL Journeys]** für Benutzende hinzufügen, die dem **[!UICONTROL Produktprofil]** „Journey-Viewer“ zugewiesen sind. Diese Benutzenden können dann Journeys veröffentlichen.

Wenn Sie ein vordefiniertes oder benutzerdefiniertes **[!UICONTROL Produktprofil]** ändern, wirkt sich dies auf jeden Benutzenden aus, der diesem **[!UICONTROL Produktprofil]** zugewiesen ist.

1. Wählen Sie in der [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. Wählen Sie das **[!UICONTROL Produktprofil]** „Journey-Viewer“ aus.

1. Wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

   Auf der Registerkarte **[!UICONTROL Berechtigungen]** wird die Liste der Funktionen angezeigt, die für das Produkt **[!UICONTROL Experience Cloud – von Platform unterstützte Anwendungen]** gelten.

   ![](assets/do-not-localize/access_control_5.png)

1. Wählen Sie die Funktion **[!UICONTROL Journeys]** aus.

   ![](assets/do-not-localize/access_control_6.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Plussymbol (+) klicken.

   Hier wird die Berechtigung **[!UICONTROL Journeys veröffentlichen]** hinzugefügt.

1. Klicken Sie bei Bedarf unter **[!UICONTROL Einbezogene Berechtigungselemente]** auf das X-Symbol, um Berechtigungen für das Produktprofil zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Bei Bedarf können Sie auch ein neues Produktprofil mit bestimmten Berechtigungen erstellen. Weitere Informationen hierzu finden Sie unter [Erstellen eines Produktprofils](#create-product-profile).

## Erstellen eines Produktprofils {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene **[!UICONTROL Produktprofile]** zu erstellen und Ihren Benutzenden eine Reihe von Berechtigungen und Sandboxes zuzuweisen. Mit **[!UICONTROL Produktprofilen]** können Sie Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

In diesem Beispiel erstellen wir ein Produktprofil mit dem Namen **Journeys nur lesen**, in dem wir Leseberechtigungen für die Journey-Funktion erteilen. Benutzende können nur auf Journeys zugreifen und diese anzeigen, können aber nicht auf andere Funktionen wie **[!DNL  Decision management]** oder [!DNL Journey Optimizer] zugreifen.

So erstellen Sie unsere **[!UICONTROL Produktprofile]** **Journeys nur lesen**:

1. Greifen Sie auf die [!DNL Admin Console] zu.

1. Wählen Sie in der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. Klicken Sie auf **[!UICONTROL Neues Profil]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Fügen Sie einen **[!UICONTROL Produktprofilnamen]**, einen **[!UICONTROL Anzeigenamen]** und eine **[!UICONTROL Beschreibung]** für Ihre neuen **[!UICONTROL Produktprofile]** hinzu.

   ![](assets/do-not-localize/access_control_10.png)

1. Wählen Sie in der Kategorie **[!UICONTROL Benachrichtigungen]** aus, ob Benutzende per E-Mail benachrichtigt werden sollen, wenn sie diesem Produktprofil hinzugefügt oder daraus entfernt werden.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]** und wählen Sie die neu erstellten **[!UICONTROL Produktprofile]** aus.

1. Um Benutzenden Berechtigungen für den Zugriff auf verschiedene Funktionen hinzuzufügen, wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

1. Sie können zwischen den verschiedenen Funktionen wie **[!DNL Journeys]**, **[!DNL Segments]** oder **[!DNL Decision management]** auswählen, die in [!DNL Journey Optimizer] im Menü links verfügbar sind.

   Hier wählen wir die Funktion **[!UICONTROL Journeys]** aus.

   ![](assets/do-not-localize/access_control_11.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Plussymbol (+) klicken.

   Hier wählen wir **[!DNL View journeys]** und **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Wählen Sie die Funktion **[!UICONTROL Zugriff auf Sandbox]** aus, um zu entscheiden, welche Sandbox(es) Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten.

   ![](assets/do-not-localize/access_control_13.png)

1. Klicken Sie unter **[!UICONTROL Verfügbare Berechtigungselemente]** auf das Pluszeichen (+), um Ihrem Profil Sandboxes zuzuweisen. [Erfahren Sie mehr über Sandboxes](sandboxes.md)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihr **[!UICONTROL Produktprofil]** wurde erstellt und konfiguriert. Jetzt müssen Sie es den Benutzenden zuweisen.

Weitere Informationen zur Erstellung und Verwaltung von Produktprofilen finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
