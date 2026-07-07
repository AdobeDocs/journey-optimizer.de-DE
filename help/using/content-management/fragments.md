---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit Fragmenten
description: Erfahren Sie, wie Sie mit Inhaltsfragmenten arbeiten, um Inhalte in Journey Optimizer-Kampagnen und -Journeys wiederzuverwenden
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
TQID: https://experienceleague.adobe.com/2XVXr3MjYnD-7o0C2ARXQ8j3sJOFfJfvjfCEZdkV50I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebbid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 8c3b899a9e1f4fbe5f951798337870f66beb1523
workflow-type: tm+mt
source-wordcount: 439
ht-degree: 78%

---

# Erste Schritte mit Fragmenten {#fragments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erste Schritte mit visuellen und Ausdrucksinhaltsfragmenten in Adobe Journey Optimizer, wiederverwendbare Komponenten, die Sie einmal erstellen und auf mehrere E-Mails in mehreren Kampagnen und Journey verweisen können.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Definieren Ihrer eigenen Fragmente"
>abstract="Erstellen und verwalten Sie eigenständige Fragmente, um Ihre Inhalte über mehrere Journeys und Kampagnen hinweg wiederzuverwenden."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Erstellen von Fragmenten"

Ein Fragment ist eine wiederverwendbare Komponente, die in einer oder mehreren E-Mails in Kampagnen und Journeys von [!DNL Journey Optimizer] referenziert werden kann. Mit dieser Funktion können Sie mehrere benutzerdefinierte Inhaltsbausteine vorab erstellen, mit denen Marketing-Fachleute E-Mail-Inhalte schnell in einem verbesserten Design-Prozess zusammenstellen können.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [In diesen Videos erfahren Sie, wie Sie Fragmente verwalten, erstellen und verwenden.](#video-fragments)

So nutzen Sie Fragmente am besten:

* **Erstellen eigener Fragmente**: Erstellen Sie visuelle Fragmente oder Ausdrucksfragmente, indem Sie sie von Grund auf neu erstellen oder Inhalte als Fragment speichern. [Erfahren Sie, wie Sie ein Fragment erstellen](create-fragments.md). Darüber hinaus können Sie Inhaltsfragmente mit der **Inhalts-REST API** von Journey Optimizer verwalten. Weiterführende Informationen finden Sie in der [Dokumentation zu Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}.
* **Wiederverwenden eigener Fragmente:** Diese können beliebig oft in Ihren Inhalten verwendet werden. Siehe [Hinzufügen visueller Fragmente](../email/use-visual-fragments.md) und [Nutzen von Ausdrucksfragmenten](../personalization/use-expression-fragments.md)
* **Dynamische Fragmente verwenden** Lösen Sie auf der Grundlage von Profilattributen, Datensatzsuchen oder Kontextdaten auf, welches Fragment zur Laufzeit pro Empfänger eingefügt werden soll. [Erfahren Sie, wie Sie dynamische Fragmente verwenden](dynamic-fragments.md)


>[!NOTE]
>
>Die **[!UICONTROL Fragmente]** die auf dieser Seite beschrieben werden, sind wiederverwendbare **Inhalts** Komponenten. Sie unterscheiden sich von:
>
>* **[Journey-Fragmente](../building-journeys/journey-fragments.md)** - wiederverwendbare Sets von Journey-Knoten, die in Journey eingefügt wurden.
>* **[AEM-Inhaltsfragmente](../integrations/aem-fragments.md)** - Inhalte, die in Adobe Experience Manager verfasst und in [!DNL Journey Optimizer] verwendet werden.


## Bevor Sie beginnen {#fragment-prerequisites}

Zum Erstellen, Bearbeiten, Archivieren und Veröffentlichen von Fragmenten benötigen Sie die Berechtigungen **[!DNL Manage library items]** und **[Fragment veröffentlichen]**, die im Produktprofil des **[!DNL Content Library Manager]** enthalten sind. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)

In dieser Version gelten folgende Einschränkungen:

* **Visuelle Fragmente** sind nur für den E-Mail-Kanal verfügbar.
* **Ausdrucksfragmente** sind nicht für den In-App-Kanal verfügbar.

Weitere Leitlinien für Fragmente finden Sie in [diesem Abschnitt](../start/guardrails.md#fragments-guardrails).

## Visuelle Fragmente und Ausdrucksfragmente {#visual-expression}

Es stehen zwei Arten von Fragmenten zur Verfügung:

* **Visuelle Fragmente** sind vordefinierte visuelle Bausteine, die Sie über mehrere E-Mail-Sendungen hinweg mithilfe des [E-Mail-Designers](../email/get-started-email-design.md) oder in [Inhaltsvorlagen](../email/use-email-templates.md) wiederverwenden können.
* **Ausdrucksfragmente** sind vordefinierte Ausdrücke, die über einen dedizierten Eintrag im [Personalisierungseditor](../personalization/personalization-build-expressions.md) verfügbar sind.

Alle Fragmente sind links über das Menü **[!UICONTROL Content-Management]** > **[!UICONTROL Fragmente]** zugänglich. [Informationen zum Verwalten von Fragmenten](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Anleitungsvideo {#video-fragments}

Informationen zum Verwalten, Erstellen und Verwenden von **visuellen Fragmenten** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Informationen zum Verwalten, Erstellen und Verwenden von **Ausdrucksfragmenten** in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
