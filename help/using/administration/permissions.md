---
title: Verwalten von Benutzern und Produktprofilen
description: Erfahren Sie, wie Sie Berechtigungen verwalten.
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Kontrollgruppen
topic: Administration.
role: Administrator
level: Intermediate
source-git-commit: f2c280ba3d2148a62eebff421ef6c8c3c0352936
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 17%

---

# Verwalten von Benutzern und Produktprofilen {#manage-permissions}

>[!IMPORTANT]
>
> Die einzelnen im Folgenden beschriebenen Verfahren können nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weitere Informationen hierzu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Produktprofile]** sind Benutzergruppen, die innerhalb Ihres Unternehmens dieselben Berechtigungen und Sandboxes besitzen.

Mit dem Produkt [!DNL Journey Optimizer] können Sie zwischen verschiedenen nativen **[!UICONTROL Produktprofilen]** mit unterschiedlichen Berechtigungsstufen auswählen, die Sie Ihren Benutzern zuweisen können. Weitere Informationen zu den verfügbaren **[!UICONTROL Produktprofilen]** finden Sie auf dieser [Seite](ootb-product-profiles.md).

Jeder Benutzer, der zu **[!UICONTROL Produktprofilen]** gehört, hat die Berechtigung für die Adobe Apps und Dienste, die im Produkt enthalten sind.

Sie können auch eigene **[!UICONTROL Produktprofile]** erstellen, wenn Sie den Zugriff Ihrer Benutzer auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche optimieren möchten.

## Zuweisen eines Produktprofils {#assigning-product-profile}

Sie können festlegen, dass Ihren Benutzern ein vordefiniertes oder benutzerdefiniertes **[!UICONTROL Produktprofil]** zugewiesen wird.

Die Liste aller nativen Produktprofile mit zugewiesenen Berechtigungen finden Sie im Abschnitt [Integrierte Produktprofile](ootb-product-profiles.md) .

So weisen Sie ein **[!UICONTROL Produktprofil]** zu:

1. Wählen Sie im Tab [!DNL Admin Console] im Bereich **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud - Plattformgestützte Anwendungen]** aus.

1. Wählen Sie ein **[!UICONTROL Produktprofil]** aus.

   ![](../assets/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](../assets/access_control_3.png)

1. Geben Sie den Namen oder die E-Mail-Adresse Ihres Benutzers ein und wählen Sie den Benutzer aus.

   Wenn der Benutzer zuvor nicht in [!DNL Admin Console] erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/access_control_4.png)

1. Führen Sie dieselben Schritte wie oben aus, um Ihrem **[!UICONTROL Produktprofil]** weitere Benutzer hinzuzufügen. Klicken Sie dann auf **[!UICONTROL Speichern]**.

Ihr Benutzer sollte dann eine E-Mail mit einer Umleitung zur Instanz erhalten.

Weitere Informationen zur Benutzerverwaltung finden Sie in der [Admin Console-Dokumentation](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Beim Zugriff auf die Instanz wird Ihrem Benutzer je nach den zugewiesenen Berechtigungen im **[!UICONTROL Produktprofil]** eine bestimmte Ansicht angezeigt. Wenn der Benutzer keinen Zugriff auf eine Funktion hat, wird der folgende Bildschirm angezeigt.

![](../assets/access_control_1.png)

## Bearbeiten eines vorhandenen Produktprofils {#edit-product-profile}

Für native oder benutzerdefinierte **[!UICONTROL Produktprofile]** können Sie jederzeit Berechtigungen hinzufügen oder löschen.

In diesem Beispiel möchten wir **[!UICONTROL Berechtigungen]** im Zusammenhang mit der **[!UICONTROL Message]**-Funktion für Benutzer hinzufügen, die dem Journey-Viewer **[!UICONTROL Produktprofil]** zugewiesen sind. Benutzer können dann Nachrichten veröffentlichen.

Wenn Sie ein vordefiniertes oder benutzerdefiniertes **[!UICONTROL Produktprofil]** ändern, wirkt sich dies auf jeden Benutzer aus, der diesem **[!UICONTROL Produktprofil]** zugewiesen ist.

1. Wählen Sie im Tab [!DNL Admin Console] im Bereich **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud - Plattformgestützte Anwendungen]** aus.

1. Wählen Sie den Journey-Viewer **[!UICONTROL Produktprofil]** aus.

1. Wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

   Im Tab **[!UICONTROL Berechtigungen]** wird die Liste der Funktionen angezeigt, die für das Produkt **[!UICONTROL Experience Cloud - Plattformgestützte Anwendungen]** gelten.

   ![](../assets/access_control_5.png)

1. Wählen Sie die Funktion **[!UICONTROL Nachrichten]** aus.

   ![](../assets/access_control_6.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Pluszeichen (+) klicken.

   Hier fügen wir die Berechtigung **[!UICONTROL Nachrichten veröffentlichen]** hinzu.

   ![](../assets/access_control_7.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Einbezogene Berechtigungselemente]** auf das X-Symbol, um Berechtigungen für das Produktprofil zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

   ![](../assets/access_control_8.png)

Bei Bedarf können Sie auch ein neues Produktprofil mit bestimmten Berechtigungen erstellen. Weitere Informationen hierzu finden Sie unter [Erstellen eines Produktprofils](#create-product-profile).

## Erstellen eines Produktprofils {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene  **[!UICONTROL Produktprofile zu erstellen]** und Ihren Benutzern eine Reihe von Berechtigungen und Sandboxes zuzuweisen. Mit **[!UICONTROL Produktprofilen]** können Sie den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de).

In diesem Beispiel erstellen wir ein Produktprofil mit dem Namen **Journey, das schreibgeschützt** ist, wo wir Leseberechtigungen für die Journey-Funktion erteilen. Benutzer können nur auf Journey zugreifen und diese anzeigen und nicht auf andere Funktionen wie **[!UICONTROL Entscheidungsverwaltung]** oder **[!UICONTROL Nachrichten]** in [!DNL Journey Optimizer] zugreifen.

So erstellen Sie unsere **Journey schreibgeschützt** **[!UICONTROL Produktprofile]**:

1. Greifen Sie auf [!DNL Admin Console] zu.

1. Wählen Sie im Tab **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Experience Cloud - Plattformgestützte Anwendungen]** aus.

1. Klicken Sie auf **[!UICONTROL Neues Profil]**.

   ![](../assets/access_control_9.png)

1. Fügen Sie einen **[!UICONTROL Produktprofilnamen]**, **[!UICONTROL Anzeigenamen]** und **[!UICONTROL Beschreibung]** für Ihre neuen **[!UICONTROL Produktprofile]** hinzu.

   ![](../assets/access_control_10.png)

1. Wählen Sie in der Kategorie **[!UICONTROL Benachrichtigungen]** aus, ob Benutzer per E-Mail benachrichtigt werden sollen, wenn sie diesem Produktprofil hinzugefügt oder daraus entfernt werden.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]** und wählen Sie die neu erstellten **[!UICONTROL Produktprofile]** aus.

1. Um Benutzern Berechtigungen für den Zugriff auf verschiedene Funktionen hinzuzufügen, wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

1. Wählen Sie zwischen den verschiedenen Funktionen wie **[!UICONTROL Nachrichten]**, **[!UICONTROL Segmente]** oder **[!UICONTROL Entscheidungsverwaltung]** aus, die im Menü links unter [!DNL Journey Optimizer] verfügbar sind.

   Hier wählen wir die Funktion **[!UICONTROL Journey]** aus.

   ![](../assets/access_control_11.png)

1. Wählen Sie in der Liste **[!UICONTROL Verfügbare Berechtigungselemente]** die Berechtigungen aus, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten, indem Sie auf das Pluszeichen (+) klicken.

   Hier wählen wir **[!UICONTROL Journey anzeigen]** und **[!UICONTROL Journey-Ereignis, Datenquellen, Aktionen]** anzeigen.

   ![](../assets/access_control_12.png)

1. Wählen Sie die Funktion **[!UICONTROL Sandbox-Zugriff]** aus, um die Sandboxes auszuwählen, die Sie Ihrem **[!UICONTROL Produktprofil]** zuweisen möchten.

   ![](../assets/access_control_13.png)

1. Klicken Sie unter **[!UICONTROL Verfügbare Berechtigungselemente]** auf das Pluszeichen (+), um Ihrem Profil Sandboxes zuzuweisen. [Erfahren Sie mehr über Sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihr **[!UICONTROL Produktprofil]** wird jetzt erstellt und konfiguriert. Jetzt müssen Sie sie Benutzern zuweisen.

Weitere Informationen zur Erstellung und Verwaltung von Produktprofilen finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
