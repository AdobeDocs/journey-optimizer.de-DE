---
solution: Journey Optimizer
product: journey optimizer
title: Primäre E-Mail-Adressen ändern
description: Erfahren Sie, wie Sie bestimmen, welche E-Mail-Adresse vom Profildienst verwendet werden soll.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Primäradressen ändern {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definieren der zu verwendenden Adresse"
>abstract="Wenn mehrere E-Mail-Adressen oder Telefonnummern in der Datenbank verfügbar sind (persönlich, professionell usw.), können Sie wählen, welche für den Versand priorisiert werden soll."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definieren der zu verwendenden Adresse"
>abstract="Bearbeiten Sie die Felder, die zur Bestimmung der E-Mail-Adresse oder Telefonnummer des Profils verwendet werden, um den Versand zu priorisieren."

Wenn Sie ein Profil als Ziel auswählen, stehen in der Datenbank möglicherweise mehrere E-Mail-Adressen oder Telefonnummern zur Verfügung (professionelle E-Mail-Adresse, persönliche Telefonnummer usw.).

Mit [!DNL Journey Optimizer]können Sie festlegen, welche E-Mail-Adresse oder Telefonnummer vom Profildienst verwendet werden soll, und Prioritäten setzen, wenn mehrere Adressen verfügbar sind. Gehen Sie dazu wie folgt vor.

1. Zugriff auf  **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** Menü.

   ![](assets/primary-address-execution-fields.png)

1. Die Felder, die derzeit standardmäßig zur Bestimmung der E-Mail-Adresse und Telefonnummer des Profils verwendet werden, werden auf diesem Bildschirm angezeigt. Klicken **[!UICONTROL Edit]** , um sie zu ändern.

   ![](assets/primary-address.png)

1. Klicken Sie auf das aktuelle Feld Ihrer Wahl oder auf das Bearbeitungssymbol, um ein neues Feld auszuwählen.

   ![](assets/primary-address-edit.png)

1. Die Liste der verfügbaren XDM-Felder vom Typ E-Mail wird angezeigt. Wählen Sie das zu verwendende Feld aus.

   ![](assets/primary-address-select-field.png)

1. Klicken **[!UICONTROL Save]** um Ihre Wahl zu bestätigen.

Das Ausführungsfeld wird aktualisiert und jetzt als primäre Adresse verwendet.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
