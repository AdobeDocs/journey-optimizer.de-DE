---
title: Sandbox-Verwaltung
description: Erfahren Sie, wie Sie Sandboxes verwalten
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
exl-id: null
feature: Kontrollgruppen
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 70%

---

# Sandbox-Verwaltung {#sandboxes}

![](../assets/do-not-localize/badge.png)

## Sandboxes {#using-sandbox} verwenden

[!DNL Journey Optimizer] ermöglicht es Ihnen, Ihre Instanz in separate virtuelle Umgebungen, so genannte Sandboxes, zu unterteilen.
Sandboxes werden über Produktprofile in der Admin Console zugewiesen. [Erfahren Sie, wie Sie Sandboxes zuweisen](permissions.md#create-product-profile).

[!DNL Journey Optimizer] spiegelt die Adobe Experience Platform-Sandboxes wider, die für eine bestimmte Organisation erstellt wurden.
Adobe Experience Platform-Sandboxes können über Ihre Adobe Experience Platform-Instanz erstellt oder zurückgesetzt werden. [Weitere Informationen finden Sie im Sandbox-Benutzerhandbuch](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de).

Das Steuerelement für den Sandbox-Umschalter finden Sie oben links auf Ihrem Bildschirm. Um von einer Sandbox zu einer anderen zu wechseln, klicken Sie im Umschalter auf die derzeit aktive Sandbox und wählen dann in der Dropdown-Liste eine andere Sandbox aus.

## Sandboxes zuweisen {#assign-sandboxes}

>[!IMPORTANT]
>
> Die Sandbox-Verwaltung kann nur von einem **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrator durchgeführt werden. Weitere Informationen hierzu finden Sie in der [Dokumentation zur Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Sie können verschiedene Sandboxes vordefinierten oder benutzerdefinierten **[!UICONTROL Produktprofilen]** zuweisen.

So weisen Sie Sandboxes zu:

1. Wählen Sie auf der Registerkarte [!DNL Admin Console] **[!UICONTROL Products]** das Produkt **[!UICONTROL Adobe Experience Platform Apps]** aus.

1. Wählen Sie ein **[!UICONTROL Produktprofil]** aus.

   ![](../assets/sandbox_1.png)

1. Wählen Sie die Registerkarte **[!UICONTROL Berechtigungen]** aus.

1. Wählen Sie die Funktion **[!UICONTROL Sandboxes]** aus.

   ![](../assets/sandbox_2.png)

1. Klicken Sie unter **[!UICONTROL Verfügbare Berechtigungselemente]** auf das Pluszeichen (+), um Ihrem Profil Sandboxes zuzuweisen. [Erfahren Sie mehr über Sandboxes](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=de)

   ![](../assets/sandbox_3.png)

1. Klicken Sie bei Bedarf unter **[!UICONTROL Eingeschlossene Berechtigungselemente]** auf das X-Symbol neben dem Entfernen von Sandboxes-Zugriff auf Ihr **[!UICONTROL Produktprofil]**.

   ![](../assets/sandbox_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Zugriff auf Inhalte {#content-access}

Um die Zugänglichkeit Ihrer Inhalte zu konfigurieren, müssen Sie jeder Ihrer Sandboxes einen gemeinsamen Ordner für Inhalte zuweisen.  Sie können den gemeinsamen Ordner auf der Registerkarte **[!UICONTROL Datenspeicherung]**, die unter [!DNL Admin Console] für Administratoren angezeigt wird, erstellen und konfigurieren. Wenn Sie als Systemadministrator Zugriff auf [!DNL Admin Console] haben, können Sie gemeinsame Ordner erstellen und Vertreter mit unterschiedlicher Zugriffsebene zu Ihren gemeinsamen Ordnern hinzufügen.

![](../assets/do-not-localize/content_access.png)

Beachten Sie, dass Sie für die Synchronisierung Ihres Inhalts mit der richtigen Sandbox dieselbe Syntax verwenden müssen wie die Sandbox, z. B. wenn Ihre Sandbox als „Entwicklung“ bezeichnet wird, sollte Ihr gemeinsamer Ordner denselben Namen haben.

[Erfahren Sie, wie Sie gemeinsame Ordner verwalten](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html).
