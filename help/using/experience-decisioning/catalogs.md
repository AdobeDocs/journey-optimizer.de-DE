---
title: Elementkatalog
description: Erfahren Sie, wie Sie mit dem Elementkatalog arbeiten.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: 616e1dd9fbfd029f7209356d5c19cfff9d4b4f06
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 89%

---

# Elementkatalog {#catalog}

Bei der Entscheidungsfindung dienen Kataloge als zentrale Container für die Organisation von Entscheidungselementen. Jeder Katalog ist mit einem Adobe Experience Platform-Schema verknüpft, das alle Attribute umfasst, die einem Entscheidungselement zugeordnet werden können.

Zunächst werden alle erstellten Entscheidungselemente in einem einzigen Katalog „Angebote“ konsolidiert, auf den über das Menü **[!UICONTROL Kataloge]** zugegriffen werden kann.

![](assets/catalogs-list.png)

Gehen Sie folgendermaßen vor, um auf das Schema des Katalogs zuzugreifen, in dem die Attribute der Entscheidungselemente gespeichert werden:

1. Klicken Sie in der Elementliste auf die Schaltfläche **[!UICONTROL Schema bearbeiten]**, die sich neben der Schaltfläche **[!UICONTROL Element erstellen]** befindet.

1. Das Schema des Katalogs wird in einer neuen Registerkarte geöffnet, die der unten stehenden Struktur folgt:

   * Der **`_experience`**-Knoten enthält standardmäßige Entscheidungselementattribute wie Name, Start- und Enddatum sowie Beschreibung.
   * Der **`_<imsOrg>`**-Knoten enthält benutzerdefinierte Entscheidungselemente. Standardmäßig sind keine benutzerdefinierten Attribute konfiguriert. Es können jedoch beliebig viele hinzugefügt werden. Danach werden benutzerdefinierte Attribute auf dem Erstellungsbildschirm für Entscheidungselement neben den standardmäßigen Attributen angezeigt.

   ![](assets/catalogs-schema.png)

1. Um dem Schema ein benutzerdefiniertes Attribut hinzuzufügen, erweitern Sie den Knoten **`_<imsOrg>`** und klicken Sie auf die Schaltfläche „+“ am gewünschten Speicherort in der Struktur.

   ![](assets/catalogs-add.png)

1. Füllen Sie die erforderlichen Felder für das hinzugefügte Attribut aus und klicken Sie auf **[!UICONTROL Anwenden]**.

   >[!CAUTION]
   >
   >Derzeit unterstützt die Entscheidungsfindung ausschließlich die folgenden Datentypen: String, Integer, Boolean, Date, DateTime und Decisioning Asset. Felder, die nicht diese Datentypen besitzen, können beim Erstellen eines Entscheidungselements oder eines Katalogs nicht verwendet werden.

   Der Wert, der in ein Attribut mit einem Entscheidungs-Asset-Attribut eingegeben wird, ist eine öffentliche URL. In den meisten Fällen würde dies auf ein Bild hinweisen.

   Detaillierte Informationen zum Arbeiten mit Adobe Experience Platform-Schemata sind im Abschnitt [XDM-Systemdokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) zu finden.

1. Sobald die gewünschten benutzerdefinierten Attribute hinzugefügt sind, speichern Sie das Schema. Das neue Feld ist jetzt im Bildschirm zur Entscheidungselement-Erstellung im Abschnitt **[!UICONTROL Benutzerdefinierte Attribute]** verfügbar.

>[!NOTE]
>
>Ein Entscheidungselement kann maximal 100 benutzerdefinierte Attribute enthalten. [Weitere Informationen zu den Limits und Einschränkungen bei der Entscheidungsfindung](gs-experience-decisioning.md#guardrails)
