---
title: Elementkatalog
description: Erfahren Sie, wie Sie mit dem Elementkatalog arbeiten.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PnRmHbBhPq33Fb723aBgYPmknwfETTRra3zBdmwf0O4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 460
ht-degree: 100%

---

# Konfigurieren des Elementkatalogs {#catalog}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Abrufen und Bearbeiten des Katalogschemas"
>abstract="Benutzerdefinierte Attribute sind spezifische Attribute, die auf Ihre Anforderungen zugeschnitten sind und die Sie einem Entscheidungselement zuweisen können. Sie werden im Katalogschema der Entscheidungselemente erstellt."

Bei der Entscheidungsfindung dienen Kataloge als zentrale Container für die Organisation von Entscheidungselementen. Jeder Katalog ist mit einem [!DNL Adobe Experience Platform]-Schema verknüpft, das alle Attribute umfasst, die einem Entscheidungselement zugeordnet werden können.

Zunächst werden alle erstellten Entscheidungselemente in einem einzigen Katalog „Angebote“ konsolidiert, auf den über das Menü **[!UICONTROL Kataloge]** zugegriffen werden kann.

![Elementkatalogliste mit dem Angebotskatalog](assets/catalogs-list.png)

## Leitlinien und Einschränkungen

Um eine optimale Leistung und Konsistenz sicherzustellen, werden bei der Entscheidungsfindung die folgenden Leitlinien und Einschränkungen durchgesetzt:

* **Unterstützte Datentypen**

  Derzeit unterstützt die Entscheidungsfindung ausschließlich die folgenden Datentypen: String, Integer, Boolean, Date, DateTime, Decisioning Asset und Object. Felder, die keinen dieser Datentypen besitzen, können beim Erstellen eines Entscheidungselements oder eines Katalogs nicht verwendet werden.

* **Benutzerdefinierte Attributbegrenzung**

  Jedes Entscheidungselement kann bis zu 100 benutzerdefinierte Attribute enthalten.

* **Verschachtelungsbeschränkungen**

  Es werden maximal vier Verschachtelungsebenen unterstützt. Bilder werden auf der letzten Ebene nicht unterstützt.

## Abrufen und Bearbeiten des Katalogschemas {#access-catalog-schema}

Gehen Sie folgendermaßen vor, um auf das Schema des Katalogs zuzugreifen, in dem die Attribute der Entscheidungselemente gespeichert werden:

1. Klicken Sie in der Elementliste auf die Schaltfläche **[!UICONTROL Schema bearbeiten]**, die sich neben der Schaltfläche **[!UICONTROL Element erstellen]** befindet.

1. Das Schema des Katalogs wird in einer neuen Registerkarte geöffnet, die der unten stehenden Struktur folgt:

   * Der **`_experience`**-Knoten enthält standardmäßige Entscheidungselementattribute wie Name, Start- und Enddatum sowie Beschreibung.
   * Der Knoten **`_<imsOrg>`** enthält Attribute für benutzerdefinierte Entscheidungselemente, wobei `<imsOrg>` durch den Namen Ihrer Organisation ersetzt wird (z. B. `_luma` für das Unternehmen Luma). Standardmäßig sind keine benutzerdefinierten Attribute konfiguriert. Es können jedoch beliebig viele hinzugefügt werden. Danach werden benutzerdefinierte Attribute auf dem Erstellungsbildschirm für Entscheidungselement neben den standardmäßigen Attributen angezeigt.

   ![Katalogschemastruktur mit Erlebnis- und Organisationsknoten](assets/catalogs-schema.png)

1. Um dem Schema ein benutzerdefiniertes Attribut hinzuzufügen, erweitern Sie den Knoten Ihrer Organisation (z. B. **`_luma`**) und klicken Sie auf die Schaltfläche „+“ am gewünschten Speicherort in der Struktur.

   ![Schaltfläche „Benutzerdefiniertes Attribut hinzufügen“ im Schema-Editor](assets/catalogs-add.png)

1. Füllen Sie die erforderlichen Felder für das hinzugefügte Attribut aus und klicken Sie auf **[!UICONTROL Anwenden]**.

   Der Wert, der in ein Attribut mit einem Entscheidungsfindungs-Asset-Attribut eingegeben wird, ist eine öffentliche URL. In den meisten Fällen würde dies auf ein Bild verweisen. Detaillierte Informationen zum Arbeiten mit [!DNL Adobe Experience Platform]-Schemata finden Sie in der [XDM-Systemdokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=de).

1. Sobald die gewünschten benutzerdefinierten Attribute hinzugefügt sind, speichern Sie das Schema. Das neue Feld ist jetzt im Bildschirm zur Erstellung von Entscheidungselementen im Abschnitt **[!UICONTROL Benutzerdefinierte Attribute]** verfügbar.

   Das folgende Beispiel zeigt einen Bildschirm zur Erstellung von Elementen mit benutzerdefinierten Attributen wie Objekten, die im Schema definiert sind.

   ![Bildschirm zur Erstellung von Entscheidungselementen mit dem Abschnitt „Benutzerdefinierte Attribute“](assets/custom-attributes.png)
