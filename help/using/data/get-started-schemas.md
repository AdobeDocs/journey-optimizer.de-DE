---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie Adobe Experience Platform-Schemata in Adobe Journey Optimizer verwenden
feature: Data Model, Datasets, Data Management
role: Engineer, Admin
level: Experienced
keywords: Schemata, Plattform, Daten, Struktur
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 100%

---

# Erste Schritte mit Schemata {#schemas-gs}

[!DNL Adobe Journey Optimizer] nutzt **Adobe Experience Platform-Schemata** zur konsistenten und wiederverwendbaren Beschreibung der Struktur von Daten. Ein Schema bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legt dar, welche Daten in den einzelnen Instanzen dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtsdatum usw.). Wenn Daten in Experience Platform aufgenommen werden, werden sie nach einem **XDM-Schema** strukturiert.

## Standard- und modellbasierte Schemata

In Adobe Experience Platform gibt es zwei Arten von Schemata:

* **Standardschemata** sind hierarchische Schemata, die Klassen und Feldergruppen verwenden, um Eintrags- oder Zeitreihendaten zu erfassen.

  Ein Standardschema besteht aus:

   * Einer **Klasse** (die das Datenverhalten definiert: Eintrag oder Zeitreihe).
   * Einer oder mehreren **Feldergruppen** (die dem Schema bestimmte Felder hinzufügen).

  In Journey Optimizer werden Standardschemata normalerweise verwendet, um **Einzelpersonen und ihre Attribute** darzustellen, **Zeitreiheninteraktionen** wie Klicks, Käufe oder Anmeldungen zu erfassen und das **Echtzeit-Kundenprofil** für die Segmentierung und Personalisierung zu nutzen.

  ➡️ [In diesem Video erfahren Sie, wie Sie ein Standardschema erstellen und konfigurieren](#video-schema) (Video)

* **Modellbasierte Schemata** sind flache, nicht hierarchische Schemata, die keine Klassen oder Feldergruppen verwenden. Sie dienen dazu, Eintragsdaten für relationale Entitäten zu erfassen, und kommen hauptsächlich in [!DNL Journey Optimizer] **orchestrierten Kampagnen** zum Einsatz.

  Beispiele für relationale Entitäten:
   * Buchungen, Verträge oder Abonnements
   * Produkte oder Kataloge
   * Filialen, Standorte oder Partner

  Mit modellbasierten Schemata können Sie eine Nachricht pro Entität senden (z. B. pro Buchung, pro Abonnement), Segmente basierend auf Entitätsattributen erstellen (z. B. Produktkategorie, Filialstandort) und die Adressierbarkeit verbessern, indem Sie alle mit einer Entität verknüpften Kontakte ansprechen.

  Funktionsweise von modellbasierten Schemata:

   1. **Erstellen Sie Schemata manuell oder importieren Sie sie über DDL.**
   1. **Verknüpfen Sie Schemata**, um Beziehungen zwischen Entitäten und Personen zu definieren (z. B. mit Mitgliedern verknüpfte Treuetransaktionen, mit Marken verknüpfte Prämien).
   1. **Nehmen Sie Daten** aus unterstützten Quellen in Ihren Datensatz auf.

  ➡️ [Informationen zum Verwalten von modellbasierten Schemata und Datensätzen](../orchestrated/gs-schemas.md)
➡️ [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-schemas.md)

## Anleitungsvideo{#video-schema}

Erfahren Sie, wie Sie ein Standardschema erstellen, Feldergruppen hinzufügen sowie benutzerdefinierte Feldergruppen erstellen und konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Erstellen eines Schemas und eines Datensatzes und Aufnehmen von Daten zum Hinzufügen von Testprofilen in Journey Optimizer](../audience/creating-test-profiles.md)
>* [XDM-System – Übersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}
>* [Best Practices für die Datenmodellierung](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=de){target="_blank"}
>* [Erstellen eines Schemas mithilfe des Schema Registry-API](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=de){target="_blank"}
>* [Definieren einer Beziehung zwischen zwei Schemata mithilfe des Schema-Editors](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=de){target="_blank"}
