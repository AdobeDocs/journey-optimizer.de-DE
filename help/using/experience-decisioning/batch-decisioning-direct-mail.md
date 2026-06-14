---
title: Batch-Entscheidung in Briefpost
description: Verwenden Sie Experience Decisioning, um Briefpost-Extraktionsdateien zu personalisieren oder Entscheidungsdaten zur Verwendung in nachgelagerten Systemen zu exportieren
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: Batch-Entscheidung, Briefpost, Entscheidung
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%

---


# Batch-Entscheidung in Briefpost {#batch-decisioning-direct-mail}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Verwenden Sie Batch Decisioning im Briefpostkanal, um die Extraktionsdatei jedes Empfängers mit den besten Entscheidungselementen zu personalisieren oder Profil- und Entscheidungsdaten in nachgelagerte Systeme zu exportieren.

>[!ENDSHADEBOX]

Bei der Batch-Entscheidung wählt Decisioning die besten Entscheidungselemente für jedes Profil aus und nimmt diese Ergebnisse in die Briefpost-Extraktionsdatei auf. Sie können mehrere Elemente pro Profil zurückgeben, indem Sie **[!UICONTROL Anzahl der Elemente]** beim Konfigurieren der Entscheidungsrichtlinie festlegen. Die exportierte Datei kann für die Personalisierung von Briefpost oder für Batch-Anwendungsfälle verwendet werden, bei denen Sie Profile und Entscheidungsattribute in ein anderes System exportieren.

Batch-Entscheidungen in Briefpost unterstützen zwei Hauptanwendungsfälle:

* **Briefpost mit Entscheidungsfindung** - Personalisieren Sie die physische Post pro Empfänger. Wählen Sie beispielsweise das beste Bild oder Angebot für jedes Profil mithilfe von Eignungsregeln und Rangfolgen (Priorität oder Formeln) aus. Die Extraktionsdatei enthält Profildaten plus Attribute aus den ausgewählten Entscheidungselementen (z. B. Angebotsbild-URL) für Ihren Briefpostanbieter.
* **Batch-Export für nachgelagerte Systeme** - Exportprofile und ihre Entscheidungsergebnisse (z. B. Angebots-IDs, Attribute) zur Verwendung in einem anderen System. Sie führen Batch Decisioning aus und exportieren die Datei auf Ihren Server. Nachgelagerte Tools (z. B. ein E-Mail-Dienstanbieter) nutzen diese Daten für eigene Kampagnen oder Prozesse.

>[!NOTE]
>
>Diese Seite konzentriert sich auf die entscheidungsspezifischen Aspekte der Verwendung von Batch Decisioning mit Briefpost. Umfassende Informationen zum Einrichten und Verwenden des Briefpostkanals - einschließlich Dateirouting, Kanalkonfiguration und Einrichtung der Extraktionsdatei - finden Sie unter [Erste Schritte mit Briefpost](../direct-mail/get-started-direct-mail.md) und [Erstellen einer Briefpostnachricht](../direct-mail/create-direct-mail.md).

## Workflow-Übersicht {#workflow}

1. **Erstellen einer Briefpostkampagne oder Journey**: Erstellen Sie eine Journey oder Kampagne, wählen Sie die Aktion **[!UICONTROL Briefpost]** aus, wählen Sie eine Briefpostkonfiguration aus und definieren Sie die Audience.

   ➡️ [Erfahren Sie, wie Sie eine Briefpostnachricht erstellen](../direct-mail/create-direct-mail.md)

1. **Entscheidungsrichtlinie hinzufügen**:

   1. Klicken Sie **[!UICONTROL Inhalt bearbeiten]**, um die Extraktionsdatei zu konfigurieren.
   1. Fügen Sie der Extraktionsdatei eine Spalte hinzu und öffnen Sie den Personalisierungseditor mithilfe des ![](assets/do-no-localize/editor-icon.svg).

      ![](assets/decision-policy-dm-add.png)

   1. Navigieren Sie zum **[!UICONTROL Decisioning]**-Menü, um eine Entscheidungsrichtlinie zu erstellen. Legen Sie in der Richtlinienkonfiguration **[!UICONTROL Anzahl von Elementen]** fest, wenn Sie mehr als ein Entscheidungselement pro Profil benötigen, konfigurieren Sie die Auswahlstrategie und das optionale Fallback.

      ![](assets/decision-policy-dm-create.png)

   ➡️ [Erfahren Sie, wie Sie eine Entscheidungsrichtlinie in Briefpost hinzufügen und konfigurieren](create-decision-policy.md#add)

1. **Briefpostdatei mit Entscheidungsattributen personalisieren**: Für Spalten, die das Entscheidungsergebnis enthalten sollen, öffnen Sie den Personalization-Editor, navigieren Sie zu **[!UICONTROL Entscheidungsrichtlinien]** und wählen Sie **[!UICONTROL Richtlinie einfügen]** aus, um den Code für Ihre Entscheidungsrichtlinie hinzuzufügen.

   Verwenden Sie die zurückgegebenen Entscheidungselementattribute, damit die ausgewählten Angebotsinformationen in der Extraktionsdatei für jedes Profil enthalten sind. Wenn mehrere Elemente zurückgegeben werden, ordnen Sie mithilfe der Policy `#each`-Schleife Attribute aus jedem Element in Ihren Spalten zu.

   ➡️ [Erfahren Sie, wie Sie Entscheidungsrichtlinien in Nachrichten verwenden - Registerkarte „Briefpost“](use-decision-policy.md)

1. Verwenden Sie **[!UICONTROL Inhalt simulieren]** mit einem Testprofil, um die exportierte Zeile in der Vorschau anzuzeigen (einschließlich des Entscheidungswerts).

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [Erfahren Sie, wie Sie Ihre Inhalte in der Vorschau anzeigen und testen können](../content-management/preview-test.md)

1. Aktivieren Sie die Kampagne oder veröffentlichen Sie die Journey, um die Datei zu generieren und zu exportieren (CSV oder Text mit Trennzeichen).

   ➡️ [Erfahren Sie, wie Sie eine Kampagne überprüfen und aktivieren](../campaigns/review-activate-campaign.md) | [Erfahren Sie, wie Sie eine Journey veröffentlichen](../building-journeys/publish-journey.md)

## Beispiel für Briefpost + Entscheidungsfindung {#example-direct-mail}

Beispiel: Ein Fitness-retailer sendet jedem Kunden eine personalisierte Postkarte mit einem von zehn möglichen Bildern. Sie verwenden Decisioning, um das beste Bild pro Profil auszuwählen.

1. Erstellen Sie 10 Entscheidungselemente (ein pro Bild) mit jeweils Eignungsregeln (z. B. Alter, Geschlecht).
2. Fügen Sie sie einer Sammlung hinzu und erstellen Sie eine Auswahlstrategie mit einer Rangfolgenmethode (z. B. manuelle Priorität oder Formel).
3. Aktivieren Sie in einer Briefpostkampagne oder auf einer Journey die Entscheidungsfindung und fügen Sie eine Entscheidungsrichtlinie hinzu, die diese Auswahlstrategie verwendet.
4. Fügen Sie der Extraktionsdatei eine Spalte hinzu, deren Daten das Entscheidungsattribut sind, das das ausgewählte Bild enthält (z. B. Angebotsbild-URL). Andere Spalten können Vollständiger Name, Adresse, Bundesland, Postleitzahl usw. sein.
5. Wenn die Kampagne ausgeführt wird, erhält jedes Profil eine Zeile im Export mit dem für dieses Profil ausgewählten Bild. Der Briefpostanbieter verwendet diese Datei für die Erstellung der physischen Post.

Sie können **[!UICONTROL Inhalt simulieren]** mit einem Testprofil verwenden, um das Entscheidungsergebnis (z. B. das Bild) anzuzeigen, das für dieses Profil exportiert werden würde.

## Anwendungsfall für Batch-Export (Middleware) {#example-batch-export}

Einige Kunden verwenden Batch Decisioning, um Profile und ihre Entscheidungsergebnisse zur Verwendung in anderen Systemen (z. B. einem CRM- oder E-Mail-Dienstleister) zu exportieren. Der Fluss ist:

1. Konfigurieren Sie Briefpost (Datei-Routing + Kanalkonfiguration) wie oben beschrieben.
2. Erstellen Sie eine Briefpostkampagne oder Journey und fügen Sie eine Entscheidungsrichtlinie hinzu.
3. Fügen Sie Spalten für Profilfelder und für die Entscheidungselementattribute hinzu, die Sie für den Export benötigen.
4. Aktivieren Sie die Kampagne. Die Datei wird auf Ihren Server exportiert (z. B. Amazon S3 oder SFTP).
5. Ihr nachgelagertes System ruft die Datei ab und verwendet die Profil- und Entscheidungsdaten für eigene Kampagnen oder Prozesse.

Dies unterstützt Anwendungsfälle für Batch-Entscheidungen über den Briefpost-Kanal mit Experience Decisioning.

## Verwandte Dokumentation {#related}

* [Erstellen einer Briefpostnachricht](../direct-mail/create-direct-mail.md) - Konfigurieren der Extraktionsdatei und Aktivieren der Entscheidung
* [Entscheidungsrichtlinien erstellen](create-decision-policy.md#add) - Fügen Sie auf der Registerkarte „Briefpost“ eine Entscheidungsrichtlinie hinzu.
* [Konfiguration von Briefpost](../direct-mail/direct-mail-configuration.md) - Datei-Routing und Kanalkonfiguration
* [Erste Schritte mit Decisioning](gs-experience-decisioning.md) - Konzepte und Schutzmechanismen

