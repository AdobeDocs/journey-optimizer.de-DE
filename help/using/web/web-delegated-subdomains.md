---
solution: Journey Optimizer
product: journey optimizer
title: Konfigurieren von Web-Subdomains
description: Erfahren Sie, wie Sie mit Journey Optimizer Web-Subdomains einrichten.
role: Admin
level: Intermediate
keywords: Web, Subdomains, Konfiguration
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: b05c7e88c223af44cd2f7d10ea76c39359662cbd
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 7%

---

# Konfigurieren von Web-Subdomains {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Web-Subdomain zuweisen"
>abstract="Sie richten Ihre Subdomain für die Verwendung von Webkanälen ein. Wählen Sie aus den Subdomains aus, die bereits an Adobe delegiert sind."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Web-Subdomain zuweisen"
>abstract="Wenn Sie Inhalte aus Adobe Experience Manager Assets Essentials zu Ihren Web-Erlebnissen hinzufügen, müssen Sie die Subdomain einrichten, die zum Veröffentlichen dieses Inhalts verwendet wird. Wählen Sie unter den bereits an Adobe delegierten Subdomains aus."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Web-Subdomain festlegen"
>abstract="Wählen Sie eine Subdomain aus der Liste der der Adobe zugewiesenen Subdomains aus. Sie können diese Web-Subdomäne als Standard festlegen, es kann jedoch immer nur eine Standard-Subdomäne verwendet werden."

Wenn Sie beim Erstellen von Web-Erlebnissen Inhalte aus der [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) -Bibliothek verwenden, müssen Sie die Subdomäne einrichten, die zum Veröffentlichen dieses Inhalts verwendet wird.

Wählen Sie dazu aus der Liste der bereits an Adobe delegierten Subdomains aus. Weitere Informationen zum Delegieren von Subdomains an Adobe finden Sie in [diesem Abschnitt](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Die Konfiguration von Web-Subdomains ist in allen Umgebungen üblich. Daher gilt:
>
>* Zum Zugreifen auf und Bearbeiten von Web-Subdomains benötigen Sie die **[!UICONTROL Verwalten von Web-Subdomains]** -Berechtigung für die Produktions-Sandbox.
>
> * Änderungen an einer Web-Subdomain wirken sich auch auf die Produktions-Sandboxes aus.


Sie können mehrere Web-Subdomains erstellen, jedoch nur die **default** wird verwendet. Sie können die Standard-Web-Subdomäne ändern, es kann jedoch immer nur eine verwendet werden.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** Menü und wählen Sie **[!UICONTROL Webkonfiguration]** > **[!UICONTROL Web-Subdomains]**.

   ![](assets/web-access-subdomains.png)

1. Klicken Sie auf **[!UICONTROL Subdomain einrichten]**.

1. Wählen Sie aus der Liste eine delegierte Subdomain aus.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >Sie können keine Subdomain auswählen, die bereits als Web-Subdomain verwendet wird.

1. Das Präfix, das in Ihrer Web-URL angezeigt wird, wird automatisch hinzugefügt.

1. Um diese Subdomain als Standard festzulegen, wählen Sie die entsprechende Option aus.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Nur die **default** wird verwendet.

1. Klicken Sie auf **[!UICONTROL Absenden]**. Die Subdomäne erhält die **[!UICONTROL Erfolg]** Status. Es kann für Ihre Web-Erlebnisse verwendet werden.

1. Die **[!UICONTROL Standard]** neben der Subdomäne angezeigt wird, die derzeit als Standard verwendet wird. Um die Standard-Subdomain zu ändern, wählen Sie **[!UICONTROL Als Standard festlegen]** von **[!UICONTROL Mehr Aktionen]** neben der gewünschten Subdomain.

   >[!NOTE]
   >
   >Sie können die Standard-Web-Subdomäne ändern, es kann jedoch immer nur eine verwendet werden.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You can only delete a **[!UICONTROL Failed]** subdomain to clean up the list. To do so, select **[!UICONTROL Delete]** from the **[!UICONTROL More actions]** button next to the desired subdomain.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
