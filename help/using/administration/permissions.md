---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Benutzenden und Produkten
description: Erfahren Sie, wie Sie Benutzende und Produkte verwalten.
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: Produkt, Profile, Sandbox
source-git-commit: 404fffa8d1f2ed40b18246002b67e2b533d8c19e
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 51%

---

# Verwalten von Benutzenden und Rollen {#manage-permissions}

**[!UICONTROL Rollen]** beziehen sich auf eine Sammlung von Benutzenden mit denselben Berechtigungen und Sandboxes. Mit diesen Rollen können Sie den Zugriff und die Berechtigungen für verschiedene Benutzergruppen in Ihrer Organisation einfach verwalten.

Mit dem [!DNL Journey Optimizer] können Sie aus einer Reihe bereits vorhandener **[!UICONTROL Rollen]** mit unterschiedlichen Berechtigungsebenen auswählen, die Sie Ihren Benutzern zuweisen können. Weitere Informationen zu den verfügbaren **[!UICONTROL Rollen]** finden Sie auf dieser [Seite](ootb-product-profiles.md).

Wenn ein(e) Benutzende(r **[!UICONTROL zu einer]** Rolle) gehört, erhält er/sie Zugriff auf die Adobe-Apps und -Services, die im Produkt enthalten sind.

Wenn die bereits vorhandenen Rollen nicht den spezifischen Anforderungen Ihrer Organisation entsprechen, können Sie auch benutzerdefinierte **[!UICONTROL Rollen]** erstellen, um eine Feinabstimmung für den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche vorzunehmen. Auf diese Weise stellen Sie sicher, dass jeder Benutzer nur Zugriff auf die Ressourcen und Tools hat, die er zur effizienten Ausführung seiner Aufgaben benötigt.


>[!IMPORTANT]
>
>Die im Folgenden beschriebenen Schritte und Verfahren können nur von einem (Produkt **[!UICONTROL oder]** System ]**Administrator durchgeführt**[!UICONTROL .


## Zuweisen einer Rolle {#assigning-role}

Sie können Ihren Benutzern eine vordefinierte oder benutzerdefinierte **[!UICONTROL Rolle]** zuweisen.

Die Liste aller vordefinierten Rollen mit zugewiesenen Berechtigungen ist im Abschnitt [Integrierte Rollen](ootb-product-profiles.md) verfügbar.

So weisen Sie eine **[!UICONTROL Rolle]** zu:

1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie die gewünschte Rolle aus.

   ![](assets/do-not-localize/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Geben Sie den Namen oder die E-Mail-Adresse Ihres Benutzers ein oder wählen Sie den Benutzer in der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn der Benutzer vorher noch nicht in der [!DNL Admin Console] erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html?lang=de){target="_blank"}.

   ![](assets/do-not-localize/access_control_4.png)

Ihr Benutzer erhält eine E-Mail, in der er zu Ihrer Instanz weitergeleitet wird.

Weitere Informationen zur Benutzerverwaltung finden Sie in der [Dokumentation zur Zugriffssteuerung](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=de){target="_blank"}.

Beim Zugriff auf die Instanz wird Ihren Benutzenden je nach den in der Rolle **[!UICONTROL Berechtigungen eine bestimmte Ansicht]**. Wenn der/die Benutzende nicht den richtigen Zugriff auf eine Funktion hat, wird die folgende Meldung angezeigt:

`You don't have permission to access this feature. Permission needed: XX.`

## Bearbeiten einer vorhandenen Rolle {#edit-product-profile}

Für integrierte oder benutzerdefinierte **[!UICONTROL Rollen]** können Sie sich jederzeit entscheiden, Berechtigungen hinzuzufügen oder zu löschen.

Im folgenden Beispiel möchten wir „Berechtigungen **[!UICONTROL im Zusammenhang mit]** **[!UICONTROL Journey]**-Ressource für Benutzende hinzufügen, die der Journey-Viewer-Rolle **[!UICONTROL sind]**. Diese Benutzenden können dann Journeys veröffentlichen.

>[!IMPORTANT]
>
>Änderungen an einer integrierten oder benutzerdefinierten Rolle wirken sich auf alle Benutzenden aus, die dieser Rolle zugewiesen sind.

1. Um eine Rolle im [!DNL Permissions] Produkt zu bearbeiten, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie die gewünschte Rolle aus, hier den Journey-Viewer **[!UICONTROL Rolle]**.
   ![](assets/do-not-localize/access_control_5.png)

1. Klicken Sie im Dashboard **[!UICONTROL Rolle]** auf **[!UICONTROL Bearbeiten]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Im Menü **[!UICONTROL Ressourcen]** wird die Liste der Ressourcen angezeigt, die für das Produkt **[!UICONTROL Experience Cloud – von Platform unterstützte Anwendungen]** gelten. Ziehen Sie Ressourcen per Drag-and-Drop, um Berechtigungen zuzuweisen.

   Wählen Sie nun aus dem Ressourcen-Dropdown **[!UICONTROL Journey]** die **[!UICONTROL Berechtigung]** zum Veröffentlichen von Journeys.

   ![](assets/do-not-localize/access_control_14.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Eingeschlossene Berechtigungselemente]** auf das X-Symbol, um Berechtigungen oder Ressourcen aus Ihrer Rolle zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Bei Bedarf können Sie auch eine neue Rolle mit bestimmten Berechtigungen erstellen.

## Erstellen einer neuen Rolle {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene **[!UICONTROL Rollen]** zu erstellen und Ihren Benutzenden eine Reihe von Berechtigungen und Sandboxes zuzuweisen. Mit **[!UICONTROL Rollen]** können Sie Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

In diesem Beispiel erstellen wir eine Rolle mit dem Namen **Journey** schreibgeschützt, in der wir Leseberechtigungen für die Journey-Funktion erteilen. Benutzende können nur auf Journeys zugreifen und diese anzeigen, können aber nicht auf andere Funktionen wie **[!DNL Decision management]** oder [!DNL Journey Optimizer] zugreifen.

So erstellen Sie die **[!UICONTROL Rolle]** **Journeys nur lesen**:

1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und klicken Sie auf **[!UICONTROL Rolle erstellen]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Fügen Sie einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** für Ihre neue **[!UICONTROL Rolle]** hinzu. Klicken Sie anschließend auf **[!UICONTROL Bestätigen]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Wählen Sie im Ressourcen-Dropdown **[!UICONTROL Sandbox]** die Sandboxes aus, die Ihrer **[!UICONTROL Rolle]** zugewiesen werden sollen. [Erfahren Sie mehr über Sandboxes](sandboxes.md)

   ![](assets/do-not-localize/access_control_13.png)

1. Wählen Sie aus den verschiedenen Ressourcen wie **[!DNL Journeys]**, **[!DNL Segments]** oder **[!DNL Decision management]** aus, die in [!DNL Journey Optimizer] im Menü links verfügbar sind.

   Wählen Sie hier die Ressource **[!UICONTROL Journeys]** aus.

   ![](assets/do-not-localize/access_control_11.png)

1. Wählen Sie im Dropdown-Menü **[!UICONTROL Journeys]** die Berechtigungen aus, die Ihrer **[!UICONTROL Rolle]** zugewiesen werden sollen.

   Wählen Sie hier **[!DNL View journeys]**, **[!DNL View journeys report]** und **[!DNL View journeys event, data sources, actions]** aus.

   ![](assets/do-not-localize/access_control_12.png)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihre **[!UICONTROL Rolle]** wurde nun erstellt und konfiguriert. Jetzt müssen Sie sie den Benutzenden zuweisen.

Weitere Informationen zur Erstellung und Verwaltung von Rollen finden Sie in der [Dokumentation zu Adobe Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=de){target="_blank"}.
