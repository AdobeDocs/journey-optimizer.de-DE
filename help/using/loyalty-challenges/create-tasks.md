---
solution: Journey Optimizer
product: journey optimizer
title: Aufgaben für Herausforderungen im Zusammenhang mit der Treue erstellen
description: Erfahren Sie, wie Sie in Adobe Journey Optimizer Aufgaben für Herausforderungen im Zusammenhang mit dem Treueprogramm erstellen und konfigurieren.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 2%

---

# Aufgaben erstellen {#create-tasks}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md)
* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md)
* [Herausforderungen schaffen](create-challenges.md)
* **Aufgaben erstellen** ◀︎ **Sie sind hier**
* [API-Referenz für Herausforderungen im Treueprogramm](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **privaten Betaversion**. Ausführliche Informationen zum Veröffentlichungszyklus und zur Verfügbarkeitsphase finden Sie unter [Veröffentlichungszyklus für Journey Optimizer](../rn/releases.md).

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um bei einer Herausforderung im Rahmen des Treueprogramms Belohnungen zu erhalten. Sie können Aufgabentypen, Mengen und Produktanforderungen konfigurieren, um ansprechende und personalisierte Treueerlebnisse zu schaffen.

Jede Aufgabe stellt eine messbare Aktion dar, die zum Abschluss der Herausforderung beiträgt. Aufgaben sind wiederverwendbare Komponenten, die unabhängig erstellt und dann zu einer oder mehreren Herausforderungen hinzugefügt oder direkt in einer Herausforderung erstellt werden können.

## Erstellen einer Aufgabe {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="Erstellen einer Aufgabe"
>abstract="Wählen Sie eine Kundenaktivität (Kauf oder Ausgaben) aus und konfigurieren Sie dann aktivitätsspezifische Attribute: Mengen oder Beträge, geeignete Artikel und Ausschlüsse sowie optionale Limits wie Mindestausgaben oder maximale Transaktionen. Legen Sie im Bereich Eigenschaften den Aufgabennamen und die Beschreibung fest."

Sie können Aufgaben aus zwei Einstiegspunkten erstellen. Der Konfigurationsprozess ist unabhängig davon, wo Sie beginnen, identisch.

>[!BEGINTABS]

>[!TAB Aus dem Aufgabeninventar]

Wählen Sie die Registerkarte **[!UICONTROL Aufgaben]** und wählen Sie **[!UICONTROL Aufgabe erstellen]**. Aus dem Inventar erstellte Aufgaben werden gespeichert und stehen zur Wiederverwendung über mehrere Herausforderungen hinweg zur Verfügung.

![](assets/task-create-inventory.png)

>[!TAB Aus einer Herausforderung]

Öffnen Sie eine bestehende Challenge oder erstellen Sie eine neue. Wählen Sie **[!UICONTROL Aufgabe hinzufügen]** und klicken Sie auf die Schaltfläche **[!UICONTROL Neu]**. Auf diese Weise erstellte Aufgaben werden automatisch zu Ihrer Challenge hinzugefügt und auch im Aufgabeninventar gespeichert, um sie in anderen Challenges wiederzuverwenden.

![](assets/task-create-challenge.png)

>[!ENDTABS]

## Kundenaktivität auswählen {#choose-activity}

Wählen Sie den Aktivitätstyp aus, den Kunden ausführen müssen, um diese Aufgabe abzuschließen:

* **[!UICONTROL Kauf]**: Kunden müssen einen oder mehrere Artikel kaufen, um diese Aufgabe abzuschließen
* **[!UICONTROL Ausgaben]**: Kunden müssen einen bestimmten Betrag ausgeben, um diese Aufgabe abzuschließen

Um eine Aktivität auszuwählen, klicken Sie auf das Symbol **+** und wählen Sie die Kundenaktivität aus, die am besten zu Ihren Ergebniszielen passt. Jeder Aktivitätstyp verfügt über bestimmte konfigurierbare Attribute, um die Aufgabenanforderungen weiter zu definieren und zu gestalten.
![](assets/task-create-activity.png)

## Aufgabenattribute definieren {#define-attributes}

Konfigurieren Sie die Aufgabenattribute basierend auf dem ausgewählten Aktivitätstyp. Auf den folgenden Registerkarten finden Sie die verfügbaren Attribute für jeden Aktivitätstyp:

>[!BEGINTABS]

>[!TAB Kaufaktivität]

Verfügbare Attribute für **Kauf**-Aktivitäten:

* **[!UICONTROL Menge]**: Geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um diese Aufgabe abzuschließen.
* **[!UICONTROL Mögliche Artikel und Ausschlüsse]**: Definieren Sie Artikel oder Artikelgruppen, die für die Aufgabenfertigstellung angerechnet werden, und solche, die dies nicht tun. [Erfahren Sie mehr über geeignete Elemente und Ausschlüsse](#eligible-items-exclusions)
* **[!UICONTROL Mindestausgabewert-Betrag]**: Legen Sie eine Anforderung für den Mindestbezugsbetrag fest.
* **[!UICONTROL Maximale Anzahl von Transaktionen]**: Schränken Sie ein, wie viele Transaktionen zum Abschließen der Aufgabe verwendet werden können.

![](assets/task-create-purchase.png)

>[!TAB Ausgabenaktivität]

Verfügbare Attribute für **Ausgaben**-Aktivitäten:

* **[!UICONTROL Betrag]**: Geben Sie den Gesamtbetrag der Ausgaben ein, der erforderlich ist, um die Aufgabe abzuschließen.
* **[!UICONTROL Mögliche Artikel und Ausschlüsse]**: Definieren Sie Artikel oder Artikelgruppen, die für die Aufgabenfertigstellung angerechnet werden, und solche, die dies nicht tun. [Erfahren Sie mehr über geeignete Elemente und Ausschlüsse](#eligible-items-exclusions)
* **[!UICONTROL Maximale Anzahl von Transaktionen]**: Geben Sie an, wie viele Transaktionen die Ausgabenanforderung erfüllen dürfen. You can activate this attribute from the parameters icon.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Define eligible items and exclusions {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="Eligible items &amp; exclusions"
>abstract="For both **Purchase** and **Spend** activities, you can use the **[!UICONTROL Eligible items &amp; exclusions]** attribute to define which items and groups are eligible and which are excluded. This allows you to target specific products, categories, or locations to align with your challenge goals. For example, you can limit a spending task to specific product categories, or exclude gift cards or promotional items from counting toward task completion."

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

For both **Purchase** and **Spend** activities, you can use the **[!UICONTROL Eligible items &amp; exclusions]** attribute to define which items and groups are eligible and which are excluded. This allows you to target specific products, categories, or locations to align with your challenge goals.

For example, you can limit a spending task to specific product categories, or exclude gift cards or promotional items from counting toward task completion.

![](assets/tasks-create-eligible.png)

* To define eligible items, enter specific item IDs, categories, or destination IDs, separated by commas in the **[!UICONTROL Eligible task purchases are limited to the following]** field. If you leave this field empty, all purchases are eligible by default. You can also enter `*` to explicitly make all purchases eligible.

  Beispiel: `SKU001, SKU002, CategoryA`

* To exclude items from the task, enter specific item IDs, categories, or destination IDs in the **[!UICONTROL The following are excluded from this task]** field.

  Beispiel: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Define task properties {#define-task-properties}

In the task **[!UICONTROL Properties]** pane, configure the basic task information:

* **[!UICONTROL Task name]**: Enter a descriptive name for the task.
* **[!UICONTROL Task description]**: The description is automatically generated based on the configured activity and attributes. To enter a custom description, toggle off the automatic generation option and enter your description in the text field.

![](assets/tasks-create-properties.png)

After configuring all attributes and properties, select **[!UICONTROL Create]** to save the task. The task is saved to your Tasks inventory and, if created from within a challenge, is automatically added to that challenge.
