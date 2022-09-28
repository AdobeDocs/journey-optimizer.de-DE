---
title: Ändern von primären E-Mail-Adressen
description: Erfahren Sie, wie Sie im Profil-Service bestimmen, welche E-Mail-Adresse verwendet werden soll.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 100%

---

# Ändern von primären Adressen {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definieren der zu verwendenden Adresse"
>abstract="Wenn mehrere Adressen in der Datenbank vorhanden sind (privat, beruflich usw.), können Sie auswählen, welche Adresse für den Versand Vorrang haben soll."

Wenn ein Profil als Ziel ausgewählt wird, stehen in der Datenbank möglicherweise mehrere E-Mail-Adressen oder Telefonnummern zur Verfügung (berufliche E-Mail-Adresse, persönliche Telefonnummer usw.).

Mit [!DNL Journey Optimizer] kann über den Profil-Service bestimmt werden, welche E-Mail-Adresse oder Telefonnummer verwendet werden soll, und es können Prioritäten gesetzt werden, wenn mehrere Adressen verfügbar sind. Gehen Sie dazu wie folgt vor.

1. Öffnen Sie das Menü **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Ausführungsfelder]**.

   ![](assets/primary-address-execution-fields.png)

1. Die Felder, die derzeit standardmäßig zur Bestimmung der E-Mail-Adresse und Telefonnummer des Profils verwendet werden, werden auf diesem Bildschirm angezeigt. Auf **[!UICONTROL Bearbeiten]** klicken, um sie zu ändern.

   ![](assets/primary-address.png)

1. Auf das aktuelle Feld oder auf das Bearbeitungssymbol klicken, um ein neues Feld auszuwählen.

   ![](assets/primary-address-edit.png)

1. Die Liste der verfügbaren XDM-Felder vom Typ „E-Mail“ wird angezeigt. Wählen Sie das zu verwendende Feld aus.

   ![](assets/primary-address-select-field.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Auswahl zu speichern.

Das Ausführungsfeld wird aktualisiert und jetzt als primäre Adresse verwendet.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
