---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit berechneten Attributen
description: Erfahren Sie, wie Sie mit berechneten Attributen arbeiten.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 520
ht-degree: 100%

---

# Arbeiten mit berechneten Attributen {#computed-attributes}

Berechnete Attribute ermöglichen das Zusammenfassen einzelner Verhaltensereignisse in berechnete Profilattribute, die in Adobe Experience Platform verfügbar sind. Diese Attribute basieren auf profilaktivierten Erlebnisereignis-Datensätzen, die in Adobe Experience Platform aufgenommen werden und als aggregierte Datenpunkte dienen, die in Kundenprofilen gespeichert werden.

Jedes berechnete Attribut ist ein Profilattribut, das Sie für die Segmentierung, Personalisierung und Aktivierung in Journeys und Kampagnen nutzen können. Diese Vereinfachung verbessert die Fähigkeit, Ihren Kundinnen und Kunden zeitnahe und aussagekräftige, personalisierte Erlebnisse bereitzustellen.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Für den Zugriff auf berechnete Attribute werden die entsprechenden Berechtigungen benötigt (**Berechnete Attribute anzeigen** und **Berechnete Attribute verwalten**).

## Erstellen von berechneten Attributen {#manage}

Navigieren Sie zum Erstellen berechneter Attribute zur Registerkarte **[!UICONTROL Berechnete Attribute]** im Menü **[!UICONTROL Profile]** auf der linken Seite.

Auf diesem Bildschirm können Sie berechnete Attribute erstellen, indem Sie Regeln erstellen, die Ereignisattribute und Aggregatfunktionen zusammen mit einem bestimmten Lookback-Zeitraum kombinieren. Sie können beispielsweise die Summe der Käufe der letzten drei Monate berechnen, den zuletzt angezeigten Artikel eines Profils ermitteln, das in der letzten Woche keinen Kauf getätigt hat, oder die von jedem Profil gesammelten Belohnungspunkte addieren.

![](assets/computed-attributes.png)

Sobald Ihre Regel fertig ist, veröffentlichen Sie das berechnete Attribut, um es in anderen nachgelagerten Diensten, einschließlich Journey Optimizer, verfügbar zu machen.

Die [Dokumentation zu berechneten Attributen](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=de) enthält detaillierte Informationen zum Erstellen und Verwalten berechneter Attribute.

## Hinzufügen von berechneten Attributen zur Adobe Experience Platform-Datenquelle {#source}

Um berechnete Attribute in Journey Optimizer zu nutzen, fügen Sie sie zur **Experience Platform**-Datenquelle von Journey Optimizer hinzu.

Die Adobe Experience Platform-Datenquelle definiert die Verbindung zum Echtzeit-Kundenprofil von Adobe. Diese Datenquelle ruft Profil- und Erlebnisereignisdaten vom Echtzeit-Kundenprofil-Dienst ab.

Gehen Sie wie folgt vor, um berechnete Attribute zur Datenquelle hinzuzufügen:

1. Navigieren Sie zum Menü **[!UICONTROL Konfigurationen]** auf der linken Seite und klicken Sie dann auf die Karte **[!UICONTROL Datenquellen]**.

1. Wählen Sie die **[!UICONTROL Experience Platform]**-Datenquelle aus.

   ![](assets/computed-attributes-add.png)

1. Fügen Sie die Feldergruppe **[!UICONTROL Vom System berechnete Attribute]** hinzu, die alle erstellten berechneten Attribute enthält.

   ![](assets/computed-attributes-fieldgroup.png)

Berechnete Attribute stehen jetzt zur Verwendung in Journey Optimizer zur Verfügung. [Erfahren Sie, wie Sie berechnete Attribute in Journey Optimizer verwenden](#use)

[Dieser Abschnitt](../datasource/adobe-experience-platform-data-source.md) enthält detaillierte Informationen zum Hinzufügen von Feldergruppen zur Adobe Experience Platform-Datenquelle.

## Verwenden von berechneten Attributen in Journey Optimizer {#use}

>[!NOTE]
>
>Stellen Sie vor Beginn sicher, dass die berechneten Attribute zur Adobe Experience Platform-Datenquelle hinzugefügt wurden. [Mehr dazu erfahren Sie in diesem Abschnitt](#source).

Berechnete Attribute bieten in Journey Optimizer eine Vielzahl von Funktionen. Sie können für verschiedene Zwecke verwendet werden, z. B. zum Personalisieren von Nachrichteninhalten, Erstellen neuer Zielgruppen oder Aufteilen von Journeys basierend auf einem spezifischen berechneten Attribut. Beispielsweise kann ein Journey-Pfad anhand der Gesamteinkäufe eines Profils in den letzten drei Wochen aufgeteilt werden, indem in einer Bedingungsaktivität ein einziges berechnetes Attribut hinzufügt wird. Sie können eine E-Mail auch personalisieren, indem Sie für jedes Profil das zuletzt angezeigte Element anzeigen.

Da berechnete Attribute Profilattributfelder sind, die im Profilvereinigungsschema erstellt wurden, kann über den Personalisierungseditor in der Feldergruppe **Vom System berechnete Attribute** auf sie zugegriffen werden. Von dort aus können berechnete Attribute zu Ausdrücken hinzugefügt und wie jedes andere Profilattribut behandelt werden, um die gewünschten Vorgänge auszuführen.

![](assets/computed-attributes-ajo.png)
