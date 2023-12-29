---
title: Elementkatalog
description: Weitere Informationen dazu, wie Sie mit dem Elementkatalog arbeiten
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 100%

---

# Elementkatalog {#catalog}

>[!BEGINSHADEBOX „Was Sie in diesem Dokumentationshandbuch finden“]

* [Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)
* Verwalten Ihrer Entscheidungselemente: **[Konfigurieren des Elementkatalogs](catalogs.md)** – [Erstellen von Entscheidungselementen](items.md) – [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: [Erstellen von Entscheidungsregeln](rules.md) – [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

In Experience Decisioning dienen Kataloge als zentrale Container für die Organisation von Entscheidungselementen. Jeder Katalog ist mit einem Adobe Experience Platform-Schema verknüpft, das alle Attribute umfasst, die einem Entscheidungselement zugeordnet werden können.

Zunächst werden alle erstellten Entscheidungselemente in einem einzigen „Angebote“-Katalog konsolidiert, auf den über das Menü **[!UICONTROL Elemente]** zugegriffen werden kann.

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
   >Derzeit unterstützt Experience Decisioning ausschließlich die unten aufgeführten Datentypen. Felder, die nicht zu diesen Datentypen gehören, können beim Erstellen eines Entscheidungselements nicht verwendet werden.
   >* Zeichenfolge
   >* Boolesch
   >* Zahl

   Detaillierte Informationen zum Arbeiten mit Adobe Experience Platform-Schemata sind im Abschnitt [XDM-Systemdokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de) zu finden.

1. Sobald die gewünschten benutzerdefinierten Attribute hinzugefügt sind, speichern Sie das Schema. Das neue Feld ist jetzt im Erstellungsbildschirm zur Entscheidung für Elemente im Abschnitt **[!UICONTROL Benutzerdefinierte Attribute]** verfügbar.
