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
hidefromtoc: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 2
source-git-commit: 43d3593264ea6d33794914e1b1f9ea45c295c79e
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 2%

---


# Aufgaben erstellen {#create-tasks}

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Zugriff und Verwaltung von Herausforderungen und Aufgaben](access-loyalty-challenges.md) - Inventar-, Challenge- und Aufgabenverwaltung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* **Aufgaben erstellen** ◀︎ **Sie sind hier** - Herausforderung definieren

>[!ENDSHADEBOX]

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um bei einer Herausforderung im Rahmen des Treueprogramms Belohnungen zu erhalten. Sie können Aufgabentypen, Mengen und Produktanforderungen konfigurieren, um ansprechende und personalisierte Treueerlebnisse zu schaffen.

Jede Aufgabe stellt eine messbare Aktion dar, die zum Abschluss der Herausforderung beiträgt. Aufgaben sind wiederverwendbare Komponenten, die unabhängig erstellt und dann zu einer oder mehreren Herausforderungen hinzugefügt oder direkt in einer Herausforderung erstellt werden können.

## Erstellen einer Aufgabe {#create-task}

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
* **[!UICONTROL Maximale Anzahl von Transaktionen]**: Geben Sie an, wie viele Transaktionen die Ausgabenanforderung erfüllen dürfen. Sie können dieses Attribut über das Symbol Parameter aktivieren.

![](assets/task-create-spend.png)

>[!ENDTABS]

## Definieren der zulässigen Elemente und Ausschlüsse {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Sowohl für **Kauf** als auch für **Ausgaben** können Sie das Attribut **[!UICONTROL Mögliche Artikel und Ausschlüsse]** verwenden, um festzulegen, welche Artikel und Gruppen förderfähig und welche ausgeschlossen sind. Auf diese Weise können Sie bestimmte Produkte, Kategorien oder Standorte auswählen, um sie an Ihre Challenge-Ziele anzupassen.

Sie können beispielsweise eine Ausgabenaufgabe auf bestimmte Produktkategorien beschränken oder Geschenkgutscheine oder Werbeartikel von der Zählung für die Aufgabenerledigung ausschließen.

![](assets/tasks-create-eligible.png)

* Um geeignete Artikel zu definieren, geben Sie bestimmte Artikel-IDs, Kategorien oder Ziel-IDs ein, getrennt durch Kommas im Feld **[!UICONTROL Mögliche Aufgabenkäufe sind auf das folgende Feld beschränkt]**. Wenn Sie dieses Feld leer lassen, sind standardmäßig alle Käufe berechtigt. Sie können auch `*` eingeben, um alle Käufe explizit als geeignet festzulegen.

  Beispiel: `SKU001, SKU002, CategoryA`

* Um Elemente aus der Aufgabe auszuschließen, geben Sie bestimmte Element-IDs, Kategorien oder Ziel-IDs in das Feld **[!UICONTROL Folgendes ist von dieser Aufgabe ausgeschlossen]** ein.

  Beispiel: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## Aufgabeneigenschaften definieren {#define-task-properties}

Konfigurieren Sie im Bereich **[!UICONTROL Eigenschaften]** die grundlegenden Informationen zur Aufgabe:

* **[!UICONTROL Aufgabenname]**: Geben Sie einen beschreibenden Namen für die Aufgabe ein.
* **[!UICONTROL Aufgabenbeschreibung]**: Die Beschreibung wird automatisch auf der Grundlage der konfigurierten Aktivität und der Attribute generiert. Um eine benutzerdefinierte Beschreibung einzugeben, deaktivieren Sie die Option Automatische Generierung und geben Sie Ihre Beschreibung in das Textfeld ein.

![](assets/tasks-create-properties.png)

Klicken Sie nach dem Konfigurieren aller Attribute und Eigenschaften auf **[!UICONTROL Erstellen]**, um die Aufgabe zu speichern. Die Aufgabe wird in Ihrem Aufgabeninventar gespeichert und, wenn sie innerhalb einer Herausforderung erstellt wurde, automatisch zu dieser Herausforderung hinzugefügt.
