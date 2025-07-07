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
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: ht
source-wordcount: '710'
ht-degree: 100%

---

# Verwalten von Benutzenden und Rollen {#manage-permissions}

**[!UICONTROL Rollen]** beziehen sich auf eine Sammlung von Benutzenden mit denselben Berechtigungen und Sandboxes. Mit diesen Rollen können Sie den Zugriff und die Berechtigungen für verschiedene Benutzergruppen in Ihrer Organisation einfach verwalten.

In [!DNL Journey Optimizer] besteht die Möglichkeit, aus einer Reihe bereits vorhandener **[!UICONTROL Rollen]** zu wählen, die über jeweils unterschiedliche Berechtigungen verfügen und die Benutzenden zugewiesen werden können. Weitere Informationen zu den verfügbaren **[!UICONTROL Rollen]** finden Sie auf dieser [Seite](ootb-product-profiles.md).

Wenn Benutzende zu einer **[!UICONTROL Rolle]** gehören, erhalten sie Zugriff auf die im Produkt enthaltenen Adobe-Anwendungen und -Dienste.

Wenn die bereits vorhandenen Rollen nicht den spezifischen Anforderungen Ihrer Organisation entsprechen, können Sie auch benutzerdefinierte **[!UICONTROL Rollen]** erstellen, um eine Feinabstimmung für den Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche vorzunehmen. Auf diese Weise kann sichergestellt werden, dass Benutzende nur Zugriff auf die Ressourcen und Tools haben, die sie jeweils für eine effiziente Durchführung ihrer Aufgaben benötigen.


>[!IMPORTANT]
>
>Die im Folgenden beschriebenen Schritte und Verfahren können nur von **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrierenden durchgeführt werden.


## Zuweisen einer Rolle {#assigning-role}

Sie können Benutzenden eine vorkonfigurierte oder eine benutzerdefinierte **[!UICONTROL Rolle]** zuweisen.

Die Liste aller vorkonfigurierten Rollen mit zugewiesenen Berechtigungen ist im Abschnitt [Integrierte Rollen](ootb-product-profiles.md) verfügbar.

So weisen Sie eine **[!UICONTROL Rolle]** zu:

1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie die gewünschte Rolle aus.

   ![](assets/do-not-localize/access_control_2.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Geben Sie Name oder E-Mail-Adresse der jeweiligen Benutzenden ein oder wählen Sie die Person aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   Wenn Benutzende vorher noch nicht in der [!DNL Admin Console] erstellt wurden, lesen Sie die [Dokumentation zum Hinzufügen von Benutzern](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html?lang=de){target="_blank"}.

   ![](assets/do-not-localize/access_control_4.png)

Die Benutzenden erhalten eine E-Mail, in der sie auf die Instanz umgeleitet werden.

Weiterführende Informationen zur Verwaltung von Benutzenden sind in der [Dokumentation zur Zugriffssteuerung](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=de){target="_blank"} verfügbar.

Beim Zugriff auf die Instanz wird den Benutzenden je nach den in der **[!UICONTROL Rolle]** zugewiesenen Berechtigungen eine bestimmte Ansicht angezeigt. Wenn Benutzende nicht den richtigen Zugriff auf eine Funktion haben, wird die folgende Meldung angezeigt:

`You do not have permission to access this feature. Permission needed: XX.`

## Bearbeiten einer vorhandenen Rolle {#edit-product-profile}

Für vorkonfigurierte oder benutzerdefinierte **[!UICONTROL Rollen]** können Berechtigungen jederzeit hinzugefügt oder gelöscht werden.

In Beispiel unten sollen **[!UICONTROL Berechtigungen]** im Zusammenhang mit der Ressource **[!UICONTROL Journeys]** für Benutzende hinzugefügt werden, die der **[!UICONTROL Rolle]** „Journey-Betrachterin bzw. Journey-Betrachter“ zugewiesen sind. Diese Benutzenden können dann Journeys veröffentlichen.

>[!IMPORTANT]
>
>Änderungen an einer integrierten oder benutzerdefinierten Rolle wirken sich auf alle Benutzenden aus, die dieser Rolle zugewiesen sind.

1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie die gewünschte Rolle aus (hier die **[!UICONTROL Rolle]** „Journey-Betrachterin bzw. Journey-Betrachter“).
   ![](assets/do-not-localize/access_control_5.png)

1. Klicken Sie im Dashboard **[!UICONTROL Rolle]** auf **[!UICONTROL Bearbeiten]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Im Menü **[!UICONTROL Ressourcen]** wird die Liste der Ressourcen angezeigt, die für das Produkt **[!UICONTROL Experience Cloud – von Platform unterstützte Anwendungen]** gelten. Legen Sie Ressourcen per Drag-and-drop ab, um Berechtigungen zuzuweisen.

   Wählen Sie nun aus dem Ressourcen-Dropdown **[!UICONTROL Journey]** die **[!UICONTROL Berechtigung]** zum Veröffentlichen von Journeys.

   ![](assets/do-not-localize/access_control_14.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Eingeschlossene Berechtigungseinträge]** auf das X-Symbol, um Berechtigungen oder Ressourcen für die Rolle zu entfernen.

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Gegebenenfalls kann auch eine neue Rolle mit bestimmten Berechtigungen erstellt werden. 

## Erstellen einer neuen Rolle {#create-product-profile}

[!DNL Journey Optimizer] ermöglicht es Ihnen, eigene **[!UICONTROL Rollen]** zu erstellen und Ihren Benutzenden eine Reihe von Berechtigungen und Sandboxes zuzuweisen. Mit **[!UICONTROL Rollen]** können Sie Zugriff auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche zulassen oder verweigern.

Weitere Informationen zum Erstellen und Verwalten von Sandboxes finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

In diesem Beispiel soll eine Rolle mit dem Namen **Journeys nur lesen** erstellt werden, in der Leseberechtigungen für die Journey-Funktion erteilt werden. Benutzende können nur auf Journeys zugreifen und diese anzeigen, können aber nicht auf andere Funktionen wie **[!DNL Decision management]** oder [!DNL Journey Optimizer] zugreifen.

So erstellen Sie die **[!UICONTROL Rolle]** **Journeys nur lesen**:

1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und klicken Sie auf **[!UICONTROL Rolle erstellen]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Fügen Sie einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** für Ihre neue **[!UICONTROL Rolle]** hinzu. Klicken Sie anschließend auf **[!UICONTROL Bestätigen]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Wählen Sie im Ressourcen-Dropdown **[!UICONTROL Sandbox]** die Sandboxes aus, die Ihrer **[!UICONTROL Rolle]** zugewiesen werden sollen. [Erfahren Sie mehr über Sandboxes](sandboxes.md)

   ![](assets/do-not-localize/access_control_13.png)

1. Wählen Sie zwischen verschiedenen Ressourcen wie **[!DNL Journeys]**, **[!DNL Segments]** oder **[!DNL Decision management]** aus, die in [!DNL Journey Optimizer] im Menü links verfügbar sind.

   Wählen Sie hier die Ressource **[!UICONTROL Journeys]** aus.

   ![](assets/do-not-localize/access_control_11.png)

1. Wählen Sie im Dropdown-Menü **[!UICONTROL Journeys]** die Berechtigungen aus, die Ihrer **[!UICONTROL Rolle]** zugewiesen werden sollen.

   Wählen Sie hier **[!DNL View journeys]**, **[!DNL View journeys report]** und **[!DNL View journeys event, data sources, actions]** aus.

   ![](assets/do-not-localize/access_control_12.png)

1. Klicken Sie abschließend auf **[!UICONTROL Speichern]**.

Ihre **[!UICONTROL Rolle]** wurde nun erstellt und konfiguriert. Jetzt müssen Sie sie den Benutzenden zuweisen.

Weitere Informationen zum Erstellen und Verwalten von Rollen sind in der [Adobe Admin Console-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=de){target="_blank"} verfügbar.
