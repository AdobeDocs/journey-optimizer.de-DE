---
title: Erste Schritte mit Experience Decisioning
description: Weitere Informationen zu Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: f71795c99157ce43f5250aaf10eb0b97f235b454
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 83%

---

# Erste Schritte mit Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX „Was Sie in diesem Dokumentationshandbuch finden“]

* **[Erste Schritte mit Experience Decisioning](gs-experience-decisioning.md)**
* Verwalten Ihrer Entscheidungselemente: [Konfigurieren des Elementkatalogs](catalogs.md) – [Erstellen von Entscheidungselementen](items.md) – [Verwalten von Elementsammlungen](collections.md)
* Konfigurieren der Elementauswahl: [Erstellen von Entscheidungsregeln](rules.md) – [Erstellen von Ranking-Methoden](ranking.md)
* [Erstellen von Auswahlstrategien](selection-strategies.md)
* [Erstellen von Entscheidungsrichtlinien](create-decision.md)

>[!ENDSHADEBOX]

## Was ist Experience Decisioning? {#about}

>[!AVAILABILITY]
>
>Die Experience Decisioning-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.
>
>Entscheidungsrichtlinien sind nur zur Verwendung in Code-basierten Erlebniskampagnen verfügbar.

Experience Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten, die als „Entscheidungselemente“ bezeichnet werden und eine ausgereifte Entscheidungs-Engine anbietet. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den neuen Code-basierten Erlebniskanal, der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert.

## Wichtige Schritte bei Experience Decisioning {#steps}

Die wichtigsten Schritte für die Arbeit mit Experience Decisioning sind:

1. **Zuweisen ordnungsgemäßer Berechtigungen**. Entscheidungen stehen nur Benutzern mit Zugriff auf Experience Decisioning-bezogene **[!UICONTROL Rolle]** z. B. Entscheidungsträger. Wenn Sie nicht auf Entscheidungen zugreifen können, müssen Ihre Berechtigungen erweitert werden.

   +++ Erfahren Sie, wie Sie die Rolle &quot;Entscheidungsmanager&quot;zuweisen

   1. So weisen Sie Benutzern eine Rolle im [!DNL Permissions] Produkt, navigieren Sie zur **[!UICONTROL Rollen]** Registerkarte und wählen Sie Entscheidungsmanager aus.

      ![](assets/decision_permission_1.png)

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

      ![](assets/decision_permission_2.png)

   1. Geben Sie den Namen oder die E-Mail-Adresse der jeweiligen Person ein oder wählen Sie sie aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn der Benutzer zuvor nicht erstellt wurde, lesen Sie den Abschnitt [Benutzerhandbuch hinzufügen](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

+++

1. **Benutzerdefinierte Attribute konfigurieren**: Der Katalog der Entscheidungselemente kann an spezifische Anforderungen angepasst werden, indem benutzerdefinierte Attribute im Schema des Katalogs eingerichtet werden.

1. **Entscheidungselemente erstellen**, um die Zielgruppe anzuzeigen.

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

1. **Eine Entscheidungsrichtlinie in die Code-basierte Kampagne einbetten**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden geeigneten Entscheidungselemente zu bestimmen.
