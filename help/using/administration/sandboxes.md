---
solution: Journey Optimizer
product: journey optimizer
title: Sandbox-Verwaltung
description: Informationen zur Verwaltung von Sandboxes
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: Sandboxes, virtuell, Umgebungen, Organisation, Plattform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 97%

---

# Sandbox-Verwaltung {#sandboxes}

## Verwenden von Sandboxes {#using-sandbox}

[!DNL Journey Optimizer] ermöglicht es Ihnen, Ihre Instanz in separate virtuelle Umgebungen, so genannte Sandboxes, zu unterteilen.
Sandboxes werden über Produktprofile in der Admin Console zugewiesen. [Erfahren Sie, wie Sie Sandboxes zuweisen](permissions.md#create-product-profile).

[!DNL Journey Optimizer] spiegelt die Adobe Experience Platform-Sandboxes wider, die für eine bestimmte Organisation erstellt wurden.
Adobe Experience Platform-Sandboxes können über Ihre Adobe Experience Platform-Instanz erstellt oder zurückgesetzt werden. [Weitere Informationen finden Sie im Sandbox-Benutzerhandbuch](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

Das Steuerelement „Sandbox-Schalter“ finden Sie oben rechts auf Ihrem Bildschirm neben dem Namen Ihrer Organisation. Um von einer Sandbox zu einer anderen zu wechseln, klicken Sie im Schalter auf die derzeit aktive Sandbox und wählen Sie dann in der Dropdown-Liste eine andere Sandbox aus.

![](assets/sandbox_5.png)

➡️ [Weitere Informationen zu Sandboxes finden Sie in diesem Video](#video)

## Zuweisen von Sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> Die Sandbox-Verwaltung kann nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target="_blank"}.

Sie können verschiedene Sandboxes vordefinierten oder benutzerdefinierten **[!UICONTROL Produktprofilen]** zuweisen.

So weisen Sie Sandboxes zu:

1. Wählen Sie in der [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** das Produkt **[!UICONTROL Adobe Experience Platform Apps]** aus.

1. Wählen Sie ein **[!UICONTROL Produktprofil]** aus.

   ![](assets/sandbox_1.png)

1. Wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

1. Wählen Sie die Funktion **[!UICONTROL Sandboxes]** aus.

   ![](assets/sandbox_2.png)

1. Klicken Sie unter **[!UICONTROL Verfügbare Berechtigungselemente]** auf das Pluszeichen (+), um Ihrem Profil Sandboxes zuzuweisen. [Weitere Informationen zu Sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de){target="_blank"}.

   ![](assets/sandbox_3.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Einbezogene Berechtigungselemente]** auf das X-Symbol, um Sandbox-Zugriffsberechtigungen auf Ihr **[!UICONTROL Produktprofil]** zu entfernen.

   ![](assets/sandbox_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zugriff auf Inhalte {#content-access}

Um die Zugänglichkeit Ihrer Inhalte zu konfigurieren, müssen Sie jeder Ihrer Sandboxes einen gemeinsamen Ordner für Inhalte zuweisen. Sie können den gemeinsamen Ordner auf der Registerkarte **[!UICONTROL Datenspeicherung]**, die unter [!DNL Admin Console] für Administratoren angezeigt wird, erstellen und konfigurieren. Wenn Sie als Systemadministrator Zugriff auf [!DNL Admin Console] haben, können Sie gemeinsame Ordner erstellen und Vertreter mit unterschiedlicher Zugriffsebene zu Ihren gemeinsamen Ordnern hinzufügen.

![](assets/do-not-localize/content_access.png)

Beachten Sie, dass Sie für die Synchronisierung Ihres Inhalts mit der richtigen Sandbox dieselbe Syntax verwenden müssen wie die Sandbox, z. B. wenn Ihre Sandbox als „Entwicklung“ bezeichnet wird, sollte Ihr gemeinsamer Ordner denselben Namen haben.

[Erfahren Sie, wie Sie gemeinsame Ordner verwalten](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Anleitungsvideo{#video}

Erfahren Sie, was Sandboxes sind und wie Sie zwischen Entwicklungs- und Produktions-Sandboxes unterscheiden. Erfahren Sie, wie Sie Sandboxes erstellen, zurücksetzen und löschen.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
