---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden und Zuweisen von Sandboxes
description: Informationen zur Verwaltung von Sandboxes
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: Sandboxes, virtuell, Umgebungen, Organisation, Plattform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 8093af8c3e7484f9ebed8dbc50065bcff0459581
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 52%

---

# Verwenden und Zuweisen von Sandboxes {#sandboxes}

## Verwenden von Sandboxes {#using-sandbox}

[!DNL Journey Optimizer] ermöglicht es Ihnen, Ihre Instanz in separate virtuelle Umgebungen, so genannte Sandboxes, zu unterteilen. Sandboxes werden über Rollen unter „Berechtigungen“ zugewiesen. [Erfahren Sie, wie Sie Sandboxes zuweisen](permissions.md#create-product-profile).

[!DNL Journey Optimizer] spiegelt die für eine bestimmte Organisation erstellten Adobe Experience Platform-Sandboxes wider. Adobe Experience Platform-Sandboxes können über Ihre Adobe Experience Platform-Instanz erstellt oder zurückgesetzt werden. [Weitere Informationen finden Sie im Sandbox-Benutzerhandbuch](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

Das Steuerelement „Sandbox-Schalter“ finden Sie oben rechts im Bildschirm neben dem Namen Ihrer Organisation. Um von einer Sandbox zu einer anderen zu wechseln, klicken Sie im Schalter auf die derzeit aktive Sandbox und wählen Sie dann in der Dropdown-Liste eine andere Sandbox aus.

![](assets/sandbox_5.png)

➡️ [Weitere Informationen zu Sandboxes finden Sie in diesem Video](#video)

## Zuweisen von Sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> Die Sandbox-Verwaltung kann nur von einem **[!UICONTROL Produkt-]**/**[!UICONTROL -]** ausgeführt werden.

Sie können vorkonfigurierten oder benutzerdefinierten **[!UICONTROL Rollen]** verschiedene Sandboxes zuweisen.

So weisen Sie Sandboxes zu:

1. Wählen Sie unter [!DNL Permissions] auf der Registerkarte **[!UICONTROL Rollen]** eine **[!UICONTROL Rolle]** aus.

   ![](assets/sandbox_1.png)

1. Klicken Sie auf **[!UICONTROL Bearbeiten]**.

1. Wählen Sie aus dem Ressourcen-Dropdown **[!UICONTROL Sandboxes]** die Sandbox aus, die Ihrer Rolle zugewiesen werden soll.

   ![](assets/sandbox_3.png)

1. Klicken Sie bei Bedarf auf das X-Symbol daneben, um den Sandbox-Zugriff auf Ihre **[!UICONTROL Rolle]** zu entfernen.

   ![](assets/sandbox_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zugriff auf Inhalte {#content-access}

Um die Barrierefreiheit von Inhalten zu konfigurieren, weisen Sie jeder Ihrer Sandboxes einen Ordner mit freigegebenen Inhalten zu. Sie können freigegebene Ordner auf der Registerkarte **[!UICONTROL Speicher]**, die im [!DNL Admin Console] für Administratoren angezeigt wird, erstellen und konfigurieren. Wenn Sie als Systemadministrator Zugriff auf die [!DNL Admin Console] haben, können Sie freigegebene Ordner erstellen und Vertreter mit unterschiedlichen Zugriffsebenen zu Ihren freigegebenen Ordnern hinzufügen.

![](assets/do-not-localize/content_access.png)

Beachten Sie, dass Sie für die Synchronisierung Ihres Inhalts mit der richtigen Sandbox dieselbe Syntax verwenden müssen wie die Sandbox. Wenn Ihre Sandbox beispielsweise „Entwicklung“ heißt, sollte Ihr freigegebener Ordner denselben Namen haben.

[Erfahren Sie, wie Sie gemeinsame Ordner verwalten](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Anleitungsvideo{#video}

Erfahren Sie, was Sandboxes sind und wie Sie zwischen Entwicklungs- und Produktions-Sandboxes unterscheiden. Erfahren Sie, wie Sie Sandboxes erstellen, zurücksetzen und löschen.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)