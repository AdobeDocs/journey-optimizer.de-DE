---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie Adobe Experience Platform-Schemata in Adobe Journey Optimizer verwenden
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: Schemata, Plattform, Daten, Struktur
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erste Schritte mit Schemata {#schemas-gs}

[!DNL Adobe Journey Optimizer] stützt sich auf **Adobe Experience Platform** Schemata, um die Datenstruktur konsistent und wiederverwendbar zu beschreiben. Ein Schema bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legt fest, welche Daten in jeder Instanz dieses Objekts enthalten sein sollen (z. B. Name, Geburtsdatum usw.). Wenn Daten in Experience Platform aufgenommen werden, sind sie immer nach einem **XDM-Schema** strukturiert.

## Standard- und relationale Schemata

In Adobe Experience Platform gibt es zwei Arten von Schemata:

* **Standardschemata** sind hierarchische Schemata, die Klassen und Feldergruppen zur Erfassung von Datensatz- oder Zeitreihendaten verwenden.

  Ein Standardschema besteht aus:

   * Eine **Klasse** (die das Datenverhalten definiert: Datensatz oder Zeitreihe).
   * Eine oder mehrere **Feldergruppen** (die dem Schema bestimmte Felder hinzufügen).

  In Journey Optimizer werden Standardschemata normalerweise verwendet, um **Einzelpersonen und ihre**) darzustellen, **Zeitreiheninteraktionen** Klicks, Käufe oder Anmeldungen zu erfassen und **Echtzeit-Kundenprofil** für die Segmentierung und Personalisierung zu nutzen.

  ➡️ [Erfahren Sie in diesem Video, wie Sie ein Standardschema erstellen und konfigurieren](#video-schema) (Video)

* **Relationale Schemata** sind flache, nicht hierarchische Schemata, die keine Klassen oder Feldergruppen verwenden. Sie werden verwendet, um Datensatzdaten für relationale Entitäten zu erfassen, und werden hauptsächlich in [!DNL Journey Optimizer] (**Kampagnen** verwendet.

  Beispiele für relationale Entitäten:
   * Buchungen, Verträge oder Abonnements
   * Produkte oder Kataloge
   * Stores, Standorte oder Partner

  Mit relationalen Schemata können Sie eine Nachricht pro Entität senden (z. B. pro Buchung, pro Abonnement), Segmente basierend auf Entitätsattributen erstellen (z. B. Produktkategorie, Store-Standort) und die Adressierbarkeit verbessern, indem Sie alle mit einer Entität verknüpften Kontakte erreichen.

  Funktionsweise von relationalen Schemata:

   1. **Schemata manuell erstellen oder über DDL importieren**
   1. **Verknüpfungsschemata** zur Definition von Beziehungen zwischen Entitäten und Personen (z. B. mit Mitgliedern verknüpfte Treuetransaktionen, mit Marken verknüpfte Belohnungen).
   1. **Nehmen Sie Daten** aus unterstützten Quellen in Ihren Datensatz auf.

  ➡️ [Erfahren Sie, wie Sie relationale Schemata und Datensätze verwalten](../orchestrated/gs-schemas.md)
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
