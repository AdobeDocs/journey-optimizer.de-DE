---
title: 'Ändern von primären E-Mail-Adressen '
description: Erfahren Sie, wie Sie im Profil-Service bestimmen, welche E-Mail-Adresse verwendet werden soll.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 36%

---

# Ändern von primären E-Mail-Adressen {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definieren der zu verwendenden Adresse"
>abstract="Sie können auswählen, welche E-Mail-Adresse für den Versand priorisiert werden soll, wenn mehrere Adressen in der Datenbank verfügbar sind (persönlich, professionell usw.)."

Wenn Sie ein Profil als Ziel auswählen, stehen in der Datenbank möglicherweise mehrere E-Mail-Adressen zur Verfügung (private, berufliche E-Mail-Adresse usw.).

Mit [!DNL Journey Optimizer]können Sie festlegen, welche E-Mail-Adresse vom Profildienst verwendet werden soll und Prioritäten setzen, wenn mehrere Adressen verfügbar sind. Gehen Sie dazu wie folgt vor.

1. Zugriff auf  **[!UICONTROL Kanäle]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Ausführungsfelder]** Menü.

   ![](assets/primary-address-execution-fields.png)

1. Auf diesem Bildschirm wird das derzeit standardmäßig zur Bestimmung der E-Mail-Adressen der Profile verwendete Feld angezeigt. Klicken Sie auf **[!UICONTROL Bearbeiten]**, um die Einstellung zu ändern.

   ![](assets/primary-address.png)

1. Klicken Sie auf das aktuelle Feld oder auf das Bearbeitungssymbol, um ein neues Feld auszuwählen.

   ![](assets/primary-address-edit.png)

1. Die Liste der verfügbaren XDM-Felder vom Typ E-Mail wird angezeigt. Wählen Sie das zu verwendende Feld aus.

   ![](assets/primary-address-field.png)

1. Klicken **[!UICONTROL Speichern]** um Ihre Wahl zu bestätigen.

   ![](assets/primary-address-save.png)

   Das Ausführungsfeld wird aktualisiert und jetzt als primäre Adresse verwendet.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
