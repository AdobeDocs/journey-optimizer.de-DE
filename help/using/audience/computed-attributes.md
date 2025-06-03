---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit berechneten Attributen
description: Erfahren Sie, wie Sie mit berechneten Attributen arbeiten.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: d87f33c80cc85b1d1a87150687f6d7c9a268a016
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 44%

---

# Arbeiten mit berechneten Attributen {#computed-attributes}

Berechnete Attribute fassen die einzelnen Verhaltensereignisse in berechneten Profilattributen zusammen, die in Adobe Experience Platform verfügbar sind. Diese Attribute basieren auf profilaktivierten Erlebnisereignis-Datensätzen, die in Adobe Experience Platform aufgenommen werden und als aggregierte Datenpunkte dienen, die in Kundenprofilen gespeichert werden.

Jedes berechnete Attribut ist ein Profilattribut, das Sie für die Segmentierung, Personalisierung und Aktivierung in Journeys und Kampagnen nutzen können. Diese Vereinfachung verbessert die Fähigkeit, Ihren Kundinnen und Kunden zeitnahe und aussagekräftige, personalisierte Erlebnisse bereitzustellen.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Um auf berechnete Attribute zuzugreifen, benötigen Sie die entsprechenden Berechtigungen (**Berechnete Attribute anzeigen** und **Berechnete Attribute verwalten**).

## Erstellen von berechneten Attributen {#manage}

Um berechnete Attribute zu erstellen, gehen Sie zur Registerkarte **[!UICONTROL Berechnete Attribute]** im Menü **[!UICONTROL Profile]** auf der linken Seite.

Auf diesem Bildschirm können Sie berechnete Attribute erstellen, indem Sie Regeln erstellen, die Ereignisattribute und Aggregatfunktionen zusammen mit einem bestimmten Lookback-Zeitraum kombinieren. Sie können beispielsweise die Summe der Käufe der letzten drei Monate berechnen, den zuletzt angezeigten Artikel eines Profils ermitteln, das in der letzten Woche keinen Kauf getätigt hat, oder die von jedem Profil gesammelten Belohnungspunkte addieren.

![](assets/computed-attributes.png)

Sobald Ihre Regel fertig ist, veröffentlichen Sie das berechnete Attribut, um es in anderen nachgelagerten Diensten, einschließlich Journey Optimizer, verfügbar zu machen.

Ausführliche Informationen zum Erstellen und Verwalten berechneter Attribute finden Sie in der [Dokumentation zu berechneten Attributen](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=de)

## Hinzufügen von berechneten Attributen zur Adobe Experience Platform-Datenquelle {#source}

Um berechnete Attribute in Journey Optimizer zu nutzen, fügen Sie sie zur Datenquelle Journey Optimizer **Experience Platform** hinzu.

Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ruft Profildaten und Erlebnisereignisdaten vom Echtzeit-Kundenprofil-Service ab.

Gehen Sie wie folgt vor, um berechnete Attribute zur Datenquelle hinzuzufügen:

1. Navigieren Sie zum **[!UICONTROL Menü]** Konfigurationen“ und klicken Sie dann auf die Karte **[!UICONTROL Datenquellen]**.

1. Wählen Sie die **[!UICONTROL Experience Platform]**-Datenquelle aus.

   ![](assets/computed-attributes-add.png)

1. Fügen Sie die Feldergruppe **[!UICONTROL Vom System berechnete Attribute]** hinzu, die alle erstellten berechneten Attribute enthält.

   ![](assets/computed-attributes-fieldgroup.png)

Berechnete Attribute stehen jetzt zur Verwendung in Journey Optimizer zur Verfügung. [Erfahren Sie, wie Sie berechnete Attribute in Journey Optimizer verwenden](#use)

Detaillierte Informationen zum Hinzufügen von Feldergruppen zur Adobe Experience Platform-Datenquelle finden Sie in [diesem Abschnitt](../datasource/adobe-experience-platform-data-source.md).

## Verwenden von berechneten Attributen in Journey Optimizer {#use}

>[!NOTE]
>
>Stellen Sie vor dem Start sicher, dass Sie Ihre berechneten Attribute zur Adobe Experience Platform-Datenquelle hinzugefügt haben. [Mehr dazu erfahren Sie in diesem Abschnitt](#source).

Berechnete Attribute bieten in Journey Optimizer vielseitige Funktionen. Sie können sie für verschiedene Zwecke verwenden, z. B. für die Personalisierung des Nachrichteninhalts, die Erstellung neuer Zielgruppen oder die Aufteilung der Journey auf der Grundlage eines bestimmten berechneten Attributs. Teilen Sie beispielsweise einen Pfad zu einer Journey auf der Basis der Gesamtkäufe eines Profils in den letzten drei Wochen auf, indem Sie ein einziges berechnetes Attribut zu einer Bedingungsaktivität hinzufügen. Sie können eine E-Mail auch personalisieren, indem Sie für jedes Profil das zuletzt angezeigte Element anzeigen.

Da es sich bei berechneten Attributen um Profilattributfelder handelt, die für Ihr Profilvereinigungsschema erstellt wurden, greifen Sie über den Personalisierungseditor innerhalb der Feldergruppe **SystemComputedAttributes** darauf zu. Fügen Sie von dort aus berechnete Attribute zu Ihren Ausdrücken hinzu und behandeln Sie sie wie jedes andere Profilattribut, um die gewünschten Vorgänge auszuführen.

![](assets/computed-attributes-ajo.png)
