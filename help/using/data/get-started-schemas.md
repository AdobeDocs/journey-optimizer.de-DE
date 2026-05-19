---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Schemata
description: Erfahren Sie, wie Sie Adobe Experience Platform-Schemata in Adobe Journey Optimizer verwenden
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: Schemata, Plattform, Daten, Struktur
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 100%

---

# Erste Schritte mit Schemata {#schemas-gs}

[!DNL Adobe Journey Optimizer] nutzt **Adobe Experience Platform-Schemata** zur konsistenten und wiederverwendbaren Beschreibung der Struktur von Daten. Ein Schema bietet eine abstrakte Definition eines realen Objekts (z. B. einer Person) und legt dar, welche Daten in den einzelnen Instanzen dieses Objekts enthalten sein sollen (z. B. Vorname, Nachname, Geburtsdatum usw.). Wenn Daten in Experience Platform aufgenommen werden, werden sie nach einem **XDM-Schema** strukturiert.

## Standard- und relationale Schemata

In Adobe Experience Platform gibt es zwei Arten von Schemata:

* **Standardschemata** sind hierarchische Schemata, die Klassen und Feldergruppen verwenden, um Eintrags- oder Zeitreihendaten zu erfassen.

  Ein Standardschema besteht aus:

   * Einer **Klasse** (die das Datenverhalten definiert: Eintrag oder Zeitreihe).
   * Einer oder mehreren **Feldergruppen** (die dem Schema bestimmte Felder hinzufügen).

  In Journey Optimizer werden Standardschemata normalerweise verwendet, um **Einzelpersonen und ihre Attribute** darzustellen, **Zeitreiheninteraktionen** wie Klicks, Käufe oder Anmeldungen zu erfassen und das **Echtzeit-Kundenprofil** für die Segmentierung und Personalisierung zu nutzen.

  ➡️ [In diesem Video erfahren Sie, wie Sie ein Standardschema erstellen und konfigurieren](#video-schema) (Video)

* **Relationale Schemata** sind flache, nicht hierarchische Schemata, die keine Klassen oder Feldergruppen verwenden. Sie dienen dazu, Eintragsdaten für relationale Entitäten zu erfassen, und kommen hauptsächlich in [!DNL Journey Optimizer] **orchestrierten Kampagnen** zum Einsatz.

  Beispiele für relationale Entitäten:
   * Buchungen, Verträge oder Abonnements
   * Produkte oder Kataloge
   * Filialen, Standorte oder Partner

  Mit relationalen Schemata können Sie eine Nachricht pro Entität senden (z. B. pro Buchung, pro Abonnement), Segmente basierend auf Entitätsattributen erstellen (z. B. Produktkategorie, Filialstandort) und die Adressierbarkeit verbessern, indem Sie alle mit einer Entität verknüpften Kontakte ansprechen.

  Funktionsweise von relationalen Schemata:

   1. **Erstellen Sie Schemata manuell oder importieren Sie sie über DDL.**
   1. **Verknüpfen Sie Schemata**, um Beziehungen zwischen Entitäten und Personen zu definieren (z. B. mit Mitgliedern verknüpfte Treuetransaktionen, mit Marken verknüpfte Prämien).
   1. **Nehmen Sie Daten** aus unterstützten Quellen in Ihren Datensatz auf.

  ➡️ [Weiter Informationen zum Verwalten von relationalen Schemata und Datensätzen](../orchestrated/gs-schemas.md)
➡️ [Erste Schritte mit orchestrierten Kampagnen](../orchestrated/gs-schemas.md)

## Anleitungsvideo{#video-schema}

Erfahren Sie, wie Sie ein Standardschema erstellen, Feldergruppen hinzufügen sowie benutzerdefinierte Feldergruppen erstellen und konfigurieren.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Erste Schritte mit Daten-Management in Journey Optimizer](gs-data.md)
>* [Erstellen eines Schemas und eines Datensatzes und Aufnehmen von Daten zum Hinzufügen von Testprofilen in Journey Optimizer](../audience/creating-test-profiles.md)
>* [XDM-System – Übersicht](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=de){target="_blank"}
>* [Best Practices für die Datenmodellierung](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=de){target="_blank"}
>* [Erstellen eines Schemas mithilfe des Schema Registry-API](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=de){target="_blank"}
>* [Definieren einer Beziehung zwischen zwei Schemata mithilfe des Schema-Editors](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=de){target="_blank"}
