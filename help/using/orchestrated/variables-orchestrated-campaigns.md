---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Variablen in koordinierten Kampagnen
description: Erfahren Sie, wie Sie Ereignisvariablen in orchestrierten Kampagnen verwenden, um Bedingungen und Zielgruppenbestimmungsregeln zu erstellen.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
feature_v2: 
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 1%

---


# Verwenden von Variablen in koordinierten Kampagnen {#variables-oc}

## Festlegen von Variablen {#set}

In einer orchestrierten Kampagne können Sie mit Variablen arbeiten, d. h. mit Werten, die das Targeting, **[!UICONTROL Test]** Bedingungen und andere Arbeitsflächen-Logiken steuern. Diese Werte können aus zwei Orten stammen:

* **Ein Signal** - Wenn der Kampagnenkalender **[!UICONTROL durch ein Signal ausgelöst]** können Sie Parameter übergeben, wenn Sie die Kampagne auslösen. Diese Parameter werden als Variablen in der ausgelösten orchestrierten Kampagne für diese Ausführung verfügbar. [Erfahren Sie, wie Sie einen Trigger für eine orchestrierte Kampagne mithilfe eines Signals erstellen](trigger-orchestrated-campaign.md)

* **Globale Variablen** - Sie können Name-Wert-Paare direkt in der Kampagne über das Menü **[!UICONTROL Variablen bearbeiten]** definieren, ohne dass eine API oder ein Signal erforderlich ist. [Erfahren Sie, wie Sie globale Variablen in orchestrierten Kampagnen definieren](global-variables.md)

>[!NOTE]
>
>Derzeit unterstützen Variablen nur **Text**-Werte.
>
>Variablen steuern **Arbeitsflächen-Logik** (Regeln, Bedingungen) und können nicht für die Personalisierung von Nachrichten verwendet werden.

## Verwenden von Variablen auf der Arbeitsfläche {#use}

Variablen sind an den folgenden Stellen auf der Arbeitsfläche verfügbar:

* **Regel-Builder** - Öffnen Sie den Ausdruckseditor für eine Regel und verwenden Sie die Auswahl **Ereignisvariablen**, um eine Variable auszuwählen und ihren Verweis in Ihren Ausdruck einzufügen. [Erfahren Sie, wie Sie Ausdrücke bearbeiten](edit-expressions.md)

  Im folgenden Beispiel wurde eine Variable mit dem Namen `brand` übergeben, und die Regel verwendet sie als Filterbedingung.

  ![Rule Builder-Bedingung unter Verwendung einer Markenvariablen aus Ereignisvariablen](assets/variables-rule.png){zoomable="yes"}

* **[!UICONTROL Test] Aktivität** - Wenn Sie eine Bedingung definieren, werden in **[!UICONTROL Dropdown-Liste Bedingungstyp]** alle Variablen im Gültigkeitsbereich zusammen mit **[!UICONTROL Populationsanzahl]** aufgelistet. Wählen Sie eine Variable aus, um sie als Grundlage für eine Testverzweigung zu verwenden. [Erfahren Sie, wie Sie die Aktivität **[!UICONTROL Test]** konfigurieren](activities/test.md)

  Im folgenden Beispiel wird die Variable `channel` verwendet, um den Fluss je nach seinem Wert zu verschiedenen Transitionen zu leiten.

  ![Dropdown-Liste „Bedingungstyp der Testaktivität“ mit der Kanalvariablen](assets/variables-test.png){zoomable="yes"}
