---
solution: Journey Optimizer
product: journey optimizer
title: Web-Subdomains konfigurieren
description: Erfahren Sie, wie Sie mit Journey Optimizer Web-Subdomains einrichten.
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: Web, Subdomains, Konfiguration
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 6%

---

# Web-Subdomains konfigurieren {#web-subdomains}

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
>title="Festlegen einer Standard-Subdomäne"
>abstract="Sie können mehrere Web-Subdomains erstellen, es wird jedoch nur die Standard-Subdomain verwendet. Sie können die Standard-Web-Subdomäne ändern, es kann jedoch immer nur eine verwendet werden."

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

1. Um diese Subdomain als Standard festzulegen, wählen Sie die entsprechende Option aus.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Nur die **default** wird verwendet. Sie können die Standard-Web-Subdomäne ändern, es kann jedoch immer nur eine verwendet werden.

1. Klicken Sie auf **[!UICONTROL Absenden]**. Die Subdomäne erhält die **[!UICONTROL Erfolg]** Status. Es kann für Ihre Web-Erlebnisse verwendet werden.

1. Die **[!UICONTROL Standard]** neben der Subdomäne angezeigt wird, die derzeit als Standard verwendet wird. Um die Standard-Subdomain zu ändern, wählen Sie **[!UICONTROL Als Standard festlegen]** von **[!UICONTROL Mehr Aktionen]** neben der gewünschten Subdomain.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.-->

1. Sie können eine **[!UICONTROL Fehlgeschlagen]** Subdomäne , um die Liste zu bereinigen. Wählen Sie dazu **[!UICONTROL Löschen]** von **[!UICONTROL Mehr Aktionen]** neben der gewünschten Subdomain.

<!--You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->

