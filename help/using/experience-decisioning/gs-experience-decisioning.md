---
title: Erste Schritte mit Decisioning
description: Weitere Informationen zu Entscheidungsfindungen
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 75%

---

# Erste Schritte mit Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>Die Entscheidungsfindung ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.
>
>Für Kundinnen und Kunden, die die Zusatzangebote Adobe **Healthcare Shield** und **Privacy and Security Shield** erworben haben, ist die Funktion derzeit nicht verfügbar.

## Was ist Entscheidungsfindung {#about}

Decisioning vereinfacht die Personalisierung, indem es einen zentralisierten Katalog von Marketing-Angeboten anbietet, der als &quot;Entscheidungselemente&quot;bezeichnet wird, sowie eine ausgereifte Entscheidungs-Engine. Diese Engine nutzt Regeln und Ranking-Kriterien, um die relevantesten Entscheidungselemente für jeden Kontakt auszuwählen und darzustellen.

Diese Entscheidungselemente sind über den [neuen Code-basierten Erlebniskanal](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/code-based-experience/get-started-code-based), der jetzt in Journey Optimizer-Kampagnen verfügbar ist, nahtlos in eine breite Palette eingehender Oberflächen integriert. Entscheidungsrichtlinien sind nur zur Verwendung in code-basierten Erlebniskampagnen verfügbar.


## Wichtige Schritte bei der Entscheidung {#steps}

Die wichtigsten Schritte für die Arbeit mit Decisioning sind:

1. **Zuweisen entsprechender Berechtigungen**. Die Entscheidungsfindung ist nur für Benutzer verfügbar, die Zugriff auf eine Decisioning-bezogene **[!UICONTROL Rolle]** haben, z. B. Entscheidungsmanager. Wenn Sie nicht auf Decisioning zugreifen können, müssen Ihre Berechtigungen erweitert werden.

   +++Erfahren Sie, wie Sie die Rolle „Entscheidungsträger“ zuweisen

   1. Um Benutzenden eine Rolle im Produkt [!DNL Permissions] zuzuweisen, navigieren Sie zur Registerkarte **[!UICONTROL Rollen]** und wählen Sie „Entscheidungsträger“ aus.

      ![](assets/decision_permission_1.png)

   1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

      ![](assets/decision_permission_2.png)

   1. Geben Sie den Namen oder die E-Mail-Adresse der jeweiligen Person ein oder wählen Sie sie aus der Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

      Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie die [Dokumentation zum Hinzufügen von Benutzenden](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   Ihre Benutzenden sollten dann eine E-Mail mit einer Umleitung zu Ihrer Instanz erhalten.

+++

1. **Benutzerdefinierte Attribute konfigurieren**: Der Katalog der Elemente kann an spezifische Anforderungen angepasst werden, indem benutzerdefinierte Attribute im Schema des Katalogs eingerichtet werden.

1. **Entscheidungselemente erstellen**, um die Zielgruppe anzuzeigen.

1. **Mit Sammlungen organisieren**: Verwenden Sie Sammlungen, um Entscheidungselemente basierend auf attributbasierten Regeln zu kategorisieren. Sammlungen können in Auswahlstrategien integriert werden, um zu bestimmen, welche Sammlung von Entscheidungselementen berücksichtigt werden soll.

1. **Entscheidungsregeln erstellen**: Entscheidungsregeln werden in Entscheidungselementen und/oder Auswahlstrategien verwendet, um zu bestimmen, wem ein Entscheidungselement angezeigt werden kann.

1. **Rangfolgemethoden implementieren**: Erstellen Sie Rangfolgemethoden und wenden Sie diese innerhalb von Entscheidungsstrategien an, um die Prioritätsreihenfolge für die Auswahl von Entscheidungselementen festzulegen.

1. **Auswahlstrategien erstellen**: Erstellen Sie Auswahlstrategien, die Sammlungen, Entscheidungsregeln und Rangfolgemethoden nutzen, um die Entscheidungselemente zu identifizieren, die für die Anzeige in Profilen geeignet sind.

1. **Eine Entscheidungsrichtlinie in die Code-basierte Kampagne einbetten**: Entscheidungsrichtlinien kombinieren mehrere Auswahlstrategien, um die für die gewünschte Zielgruppe anzuzeigenden geeigneten Entscheidungselemente zu bestimmen.
