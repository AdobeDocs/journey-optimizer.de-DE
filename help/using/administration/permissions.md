---
title: Verwalten von Benutzern und Produktprofilen
description: Erfahren Sie, wie Sie Berechtigungen verwalten.
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Kontrollgruppen
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 97%

---

# Verwalten von Benutzern und Produktprofilen {#manage-permissions}

>[!IMPORTANT]
>
> Die einzelnen im Folgenden beschriebenen Verfahren können nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Produktprofile]** sind Gruppen von Benutzern, die innerhalb Ihrer Organisation die gleichen Berechtigungen und Sandboxes nutzen.

Mit [!DNL Journey Optimizer] können Sie zwischen verschiedenen vorkonfigurierten **[!UICONTROL Produktprofilen]** mit unterschiedlichen Berechtigungsebenen auswählen, die Sie Ihren Benutzern zuweisen können. Weitere Informationen zu den verfügbaren **[!UICONTROL Produktprofilen]** finden Sie auf dieser [Seite](ootb-product-profiles.md).

Jeder Benutzer, der einem **[!UICONTROL Produktprofil]** angehört, hat die Berechtigung für die Adobe-Programme und -Services, die im Produkt enthalten sind.

Sie können auch eigene **[!UICONTROL Produktprofile]** erstellen, wenn Sie den Zugriff Ihrer Benutzer auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche präziser definieren möchten.

## Zuweisen eines Produktprofils {#assigning-product-profile}

Sie können festlegen, dass Ihren Benutzern ein vorkonfiguriertes oder ein benutzerdefiniertes **[!UICONTROL Produktprofil]** zugewiesen wird.

Die Liste aller vorkonfigurierten Produktprofile mit zugewiesenen Berechtigungen finden Sie im Abschnitt [Integrierte Produktprofile](ootb-product-profiles.md).

So weisen Sie ein **[!UICONTROL Produktprofil]** zu:

1. Wählen Sie in der [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. **[!UICONTROL Produktprofil]** auswählen.

   ![](../assets/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](../assets/access_control_3.png)

1. Geben Sie den Namen oder die E-Mail-Adresse Ihres Benutzers ein und wählen Sie den Benutzer aus.

   Wenn der Benutzer vorher noch nicht in der [!DNL Admin Console] erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/access_control_4.png)

1. Führen Sie die gleichen Schritte wie oben aus, um weitere Benutzer zu Ihrem **[!UICONTROL Produktprofil]** hinzuzufügen. Klicken Sie dann auf **[!UICONTROL Speichern]**.

Ihr Benutzer sollte dann eine E-Mail mit einer Umleitung zur Instanz erhalten.

Weiterführende Informationen zur Benutzerverwaltung finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Beim Zugriff auf die Instanz wird Ihrem Benutzer je nach den im **[!UICONTROL Produktprofil]** zugewiesenen Berechtigungen eine bestimmte Ansicht angezeigt. Wenn der Benutzer nicht den richtigen Zugriff auf eine Funktion hat, wird der folgende Bildschirm angezeigt.

![](../assets/access_control_1.png)

## Bearbeiten eines vorhandenen Produktprofils {#edit-product-profile}

Für vorkonfigurierte oder benutzerdefinierte **[!UICONTROL Produktprofile]** können Sie jederzeit Berechtigungen hinzufügen oder löschen.

In diesem Beispiel möchten wir **[!UICONTROL Berechtigungen]** im Zusammenhang mit der **[!UICONTROL Nachrichten]**-Funktion für Benutzer hinzufügen, die dem **[!UICONTROL Produktprofil]** „Journey-Viewer“ zugewiesen sind. Diese Benutzer können dann Nachrichten veröffentlichen.

Wenn Sie ein vordefiniertes oder benutzerdefiniertes **[!UICONTROL Produktprofil]** ändern, wirkt sich dies auf jeden Benutzer aus, der diesem **[!UICONTROL Produktprofil]** zugewiesen ist.

1. Wählen Sie in der [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. Wählen Sie das **[!UICONTROL Produktprofil]** „Journey-Viewer“ aus.

1. Wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

   Auf der Registerkarte **[!UICONTROL Berechtigungen]** wird die Liste der Funktionen angezeigt, die für das Produkt **[!UICONTROL Experience Cloud – von Platform unterstützte Anwendungen]** gelten.

   ![](../assets/access_control_5.png)

1. Wählen Sie die Funktion **[!UICONTROL Nachrichten]** aus.

   ![](../assets/access_control_6.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Plussymbol (+) klicken.

   Hier fügen wir die Berechtigung **[!UICONTROL Nachrichten veröffentlichen]** hinzu.

   ![](../assets/access_control_7.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Einbezogene Berechtigungselemente]** auf das X-Symbol, um Berechtigungen für das Produktprofil zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

   ![](../assets/access_control_8.png)

Bei Bedarf können Sie auch ein neues Produktprofil mit bestimmten Berechtigungen erstellen. Weitere Informationen hierzu finden Sie unter [Erstellen eines Produktprofils](#create-product-profile).

## Erstellen eines Produktprofils {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene **[!UICONTROL Produktprofile]** zu erstellen und Ihren Benutzern eine Reihe von Berechtigungen und Sandboxes zuzuweisen. Mit **[!UICONTROL Produktprofilen]** können Sie Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target=&quot;_blank&quot;}.

In diesem Beispiel erstellen wir ein Produktprofil mit dem Namen **Journeys nur lesen**, in dem wir Leseberechtigungen für die Journey-Funktion erteilen. Benutzer können nur auf Journeys zugreifen und diese anzeigen und nicht auf andere Funktionen wie **[!UICONTROL Entscheidungs-Management]** oder **[!UICONTROL Nachrichten]** in [!DNL Journey Optimizer] zugreifen.

So erstellen Sie unsere **[!UICONTROL Produktprofile]** **Journeys nur lesen**:

1. Greifen Sie auf die [!DNL Admin Console] zu.

1. Wählen Sie in der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud – Plattformgestützte Anwendungen]** aus.

1. Klicken Sie auf **[!UICONTROL Neues Profil]**.

   ![](../assets/access_control_9.png)

1. Fügen Sie einen **[!UICONTROL Produktprofilnamen]**, einen **[!UICONTROL Anzeigenamen]** und eine **[!UICONTROL Beschreibung]** für Ihre neuen **[!UICONTROL Produktprofile]** hinzu.

   ![](../assets/access_control_10.png)

1. Wählen Sie in der Kategorie **[!UICONTROL Benachrichtigungen]** aus, ob Benutzer per E-Mail benachrichtigt werden sollen, wenn sie diesem Produktprofil hinzugefügt oder daraus entfernt werden.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]** und wählen Sie die neu erstellten **[!UICONTROL Produktprofile]** aus.

1. Um Benutzern Berechtigungen für den Zugriff auf verschiedene Funktionen hinzuzufügen, wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

1. Wählen Sie zwischen den verschiedenen Funktionen wie **[!UICONTROL Nachrichten]**, **[!UICONTROL Segmente]** oder **[!UICONTROL Entscheidungs-Management]** aus, die in [!DNL Journey Optimizer] im Menü links verfügbar sind.

   Hier wählen wir die Funktion **[!UICONTROL Journeys]** aus.

   ![](../assets/access_control_11.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Plussymbol (+) klicken.

   Hier wählen wir **[!UICONTROL Journeys anzeigen]** und **[!UICONTROL Ereignisse, Datenquellen, Aktionen für Journeys anzeigen]** aus.

   ![](../assets/access_control_12.png)

1. Wählen Sie die Funktion **[!UICONTROL Zugriff auf Sandbox]** aus, um zu entscheiden, welche Sandbox(es) Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten.

   ![](../assets/access_control_13.png)

1. Klicken Sie unter **[!UICONTROL Verfügbare Berechtigungselemente]** auf das Pluszeichen (+), um Ihrem Profil Sandboxes zuzuweisen. [Erfahren Sie mehr über Sandboxes](sandboxes.md)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihr **[!UICONTROL Produktprofil]** wurde erstellt und konfiguriert. Jetzt müssen Sie es Benutzern zuweisen.

Weitere Informationen zur Erstellung und Verwaltung von Produktprofilen finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
