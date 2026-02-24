---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden und Zuweisen von Sandboxes
description: Informationen zur Verwaltung von Sandboxes
feature: Sandboxes
topic: Administration
role: Admin, Developer
level: Experienced
keywords: Sandboxes, virtuell, Umgebungen, Organisation, Plattform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 56faee8badff99ff9a39cfd85a78c1ed272cd2ca
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 79%

---

# Verwenden und Zuweisen von Sandboxes {#sandboxes}

**Sandboxes** sind virtuelle Umgebungen, die Ihre Adobe Journey Optimizer-Instanz in separate, isolierte Workspaces für Entwicklung, Tests oder Produktion unterteilen. Die Sandbox-Verwaltung finden Sie unter **Administration** > **Kanäle** > **Verbinden Ihrer Systeme und Umgebungen** (oder über den Sandbox-Umschalter oben rechts in der Benutzeroberfläche). Sandboxes helfen Ihnen, sicher zu experimentieren, unterschiedliche Zugriffsrechte pro Rolle zuzuweisen und Inhalte zu organisieren. Auf dieser Seite wird beschrieben, wie Sie Sandboxes verwenden und zuweisen, den Inhaltszugriff konfigurieren und - im Artikel [Objekte in eine andere Sandbox exportieren](../configuration/copy-objects-to-sandbox.md) wie Sie Journey und Vorlagen zwischen Sandboxes kopieren.

## Verwenden von Sandboxes {#using-sandbox}

[!DNL Journey Optimizer] ermöglicht das Unterteilen von Instanzen in separate virtuelle Umgebungen, sogenannte Sandboxes. Sandboxes werden über Rollen unter „Berechtigungen“ zugewiesen. [Erfahren Sie, wie Sie Sandboxes zuweisen](permissions.md#create-product-profile).

[!DNL Journey Optimizer] spiegelt die Adobe Experience Platform-Sandboxes wider, die für eine bestimmte Organisation erstellt wurden. Adobe Experience Platform-Sandboxes können über Ihre Adobe Experience Platform-Instanz erstellt oder zurückgesetzt werden. [Weitere Informationen finden Sie im Sandbox-Benutzerhandbuch](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=de){target="_blank"}.

Das Steuerelement zum Wechseln zwischen Sandboxes befindet sich oben rechts auf dem Bildschirm neben dem Namen der Organisation. Um von einer Sandbox zu einer anderen zu wechseln, klicken Sie im Schalter auf die derzeit aktive Sandbox und wählen Sie dann in der Dropdown-Liste eine andere Sandbox aus.

![](assets/sandbox_5.png)

➡️ [Weitere Informationen zu Sandboxes sind in diesem Video verfügbar](#video)

## Zuweisen von Sandboxes {#assign-sandboxes}

>[!IMPORTANT]
>
> Die Sandbox-Verwaltung kann nur von **[!UICONTROL Produkt]**- oder **[!UICONTROL System]**-Administrierenden durchgeführt werden.

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

Um die Barrierefreiheit von Inhalten zu konfigurieren, muss jeder Sandbox ein gemeinsamen Ordner für Inhalte zugewiesen werden. Der gemeinsame Ordner kann auf der Registerkarte **[!UICONTROL Datenspeicherung]**, die unter [!DNL Admin Console] für Administrierende angezeigt wird, erstellt und konfiguriert werden. Wenn Sie als Systemadmin Zugriff auf [!DNL Admin Console] haben, können Sie gemeinsame Ordner erstellen und Delegierte mit unterschiedlichen Zugriffsebenen zu den gemeinsamen Ordnern hinzugefügen.

![](assets/do-not-localize/content_access.png)

Für die Synchronisierung des Inhalts mit der richtigen Sandbox muss dieselbe Syntax verwendet werden wie für die Sandbox. Wenn die Sandbox beispielsweise „Entwicklung“ heißt, sollte Ihr gemeinsamer Ordner denselben Namen haben.

[Erfahren Sie, wie Sie gemeinsame Ordner verwalten](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Anleitungsvideo{#video}

Erfahren Sie, was Sandboxes sind und wie Sie zwischen Entwicklungs- und Produktions-Sandboxes unterscheiden. Erfahren Sie, wie Sie Sandboxes erstellen, zurücksetzen und löschen.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)