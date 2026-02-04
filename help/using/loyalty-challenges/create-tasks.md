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
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 2%

---


# Aufgaben erstellen {#create-tasks}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treueprogrammen](access-loyalty-challenges.md) - Inventar und Filterung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* **Aufgaben erstellen** ◀︎ **Sie sind hier** - Herausforderung definieren
* [Herausforderungen verwalten](manage-challenges.md) - Bearbeiten, Überwachen, Optimieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Überblick {#overview}

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um bei einer Herausforderung im Rahmen des Treueprogramms Belohnungen zu erhalten. Sie können Aufgabentypen, Mengen, Produktanforderungen und Belohnungswerte konfigurieren, um ansprechende und personalisierte Treueerlebnisse zu schaffen.

Jede Aufgabe stellt eine messbare Aktion dar, die zum Abschluss der Herausforderung beiträgt. Aufgaben sind wiederverwendbare Komponenten, die unabhängig erstellt und dann zu einer oder mehreren Herausforderungen hinzugefügt oder direkt in einer Herausforderung erstellt werden können.

### Funktionsweise von Aufgaben in verschiedenen Challenge-Typen {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

Je nach Challenge-Typ (Standard, Streak oder Sequential) führen Kunden Aufgaben unterschiedlich aus:

* **Standardherausforderungen**: Kunden führen eine beliebige Anzahl von Aufgaben in beliebiger Reihenfolge aus
* **Streak Challenges**: Kunden führen dieselbe Aufgabe mehrmals hintereinander aus
* **Sequenzielle Herausforderungen**: Kunden führen Aufgaben in einer definierten Reihenfolge aus

## Erstellen einer Aufgabe {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

Sie können Aufgaben aus zwei Einstiegspunkten erstellen. Der Konfigurationsprozess ist unabhängig davon, wo Sie beginnen, identisch.

+++Aus dem Aufgabeninventar

1. Navigieren Sie zu **[!UICONTROL Herausforderungen]** Treue“ in Journey Optimizer.

1. Wählen Sie die **[!UICONTROL Aufgaben]** aus.

1. Wählen Sie **[!UICONTROL Aufgabe erstellen]** aus.

Aus dem Inventar erstellte Aufgaben werden gespeichert und stehen zur Wiederverwendung über mehrere Herausforderungen hinweg zur Verfügung.

+++

+++Aus einer Herausforderung heraus

1. Öffnen Sie eine bestehende Challenge oder erstellen Sie eine neue.

1. Navigieren Sie zum Abschnitt **[!UICONTROL Aufgaben]** .

1. Wählen Sie **[!UICONTROL Aufgabe hinzufügen]** und dann **[!UICONTROL Neue Aufgabe erstellen]** aus.

Auf diese Weise erstellte Aufgaben werden automatisch zu Ihrer Challenge hinzugefügt und auch im Aufgabeninventar gespeichert, um sie in anderen Challenges wiederzuverwenden.

+++

### Aufgabeneigenschaften definieren {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

Konfigurieren der grundlegenden Aufgabeninformationen:

* **Aufgabenname**: Geben Sie einen beschreibenden Namen für die Aufgabe ein. Dieser Name ist für Sie und Ihr Team sichtbar, wird Kunden jedoch möglicherweise nicht angezeigt, je nach Design Ihrer Inhaltskarte.
* **Aufgabenbeschreibung**: (Optional) Fügen Sie Details zum Zweck oder zu den Anforderungen der Aufgabe hinzu.

### Kundenaktivität auswählen {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

Wählen Sie die Art der Kundenaktivität aus, die Kundinnen und Kunden durchführen müssen, um diese Aufgabe abzuschließen:

* **[!UICONTROL Kauf]**: Kunden müssen einen oder mehrere Artikel kaufen, um diese Aufgabe abzuschließen
* **[!UICONTROL Ausgaben]**: Kunden müssen einen bestimmten Betrag ausgeben, um diese Aufgabe abzuschließen

Wählen Sie die Kundenaktivität aus, die am besten zu Ihren Ergebniszielen passt. Jeder Aktivitätstyp verfügt über bestimmte konfigurierbare Attribute, um die Aufgabenanforderungen weiter zu definieren und zu gestalten.

### Attribute definieren {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

Konfigurieren Sie die Aufgabenattribute basierend auf Ihrem ausgewählten Aktivitätstyp:

+++Für Kaufaktivität

Konfigurieren Sie die folgenden Attribute:

* **Menge**: Geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um diese Aufgabe abzuschließen
* **Mögliche Artikel und Ausschlüsse**: Definieren Sie Artikel oder Artikelgruppen, die für die Aufgabenfertigstellung angerechnet werden, und solche, die dies nicht tun. Weitere Informationen zum [Definieren von zulässigen Elementen und Ausschlüssen](#eligible-items-exclusions)

**Optionale Attribute** (über das Symbol Parameter konfigurieren):

* **Mindestausgabewert-Betrag**: Legen Sie eine Anforderung für den Mindestbezugsbetrag fest
* **Maximale Anzahl an Transaktionen**: Schränken Sie ein, wie viele Transaktionen zum Abschließen der Aufgabe verwendet werden können

+++

+++Für Ausgabenaktivität

Konfigurieren Sie die folgenden Attribute:

* **Betrag**: Geben Sie den Gesamtausgabenbetrag ein, der zum Abschließen der Aufgabe erforderlich ist
* **Maximale Anzahl von Transaktionen**: Geben Sie an, wie viele Transaktionen die Ausgabenanforderung erfüllen dürfen. Sie können dieses Attribut über das Symbol Parameter deaktivieren, wenn Sie die Anzahl der Transaktionen nicht begrenzen möchten
* **Mögliche Elemente und Ausschlüsse**: (Optional) Definieren Sie Elemente oder Artikelgruppen, die für die Aufgabenfertigstellung zählen, und solche, die nicht zählen. Weitere Informationen zum [Definieren von zulässigen Elementen und Ausschlüssen](#eligible-items-exclusions)

+++

Wählen Sie nach dem Konfigurieren aller Attribute **[!UICONTROL Erstellen]** aus, um die Aufgabe zu speichern. Die Aufgabe wird in Ihrem Aufgabeninventar gespeichert und, wenn sie innerhalb einer Herausforderung erstellt wurde, automatisch zu dieser Herausforderung hinzugefügt.

## Definieren der zulässigen Elemente und Ausschlüsse {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Sowohl für Kauf- als auch für Ausgabenaktivitäten können Sie geeignete Artikel und Gruppen definieren sowie Artikel und Gruppen ausschließen. Auf diese Weise können Sie bestimmte Produkte, Kategorien oder Standorte auswählen, um sie an Ihre Challenge-Ziele anzupassen.

**Anwendungsfälle:**

* Aufgabe erstellen, die Kunden für den Kauf von Kaffeeartikeln belohnt, Clearance-Produkte jedoch ausschließt
* Ausgabenaufgabe auf bestimmte Produktkategorien beschränken
* Geschenkgutscheine oder Werbeartikel von der Zählung bis zum Abschluss der Aufgabe ausschließen

### Konfigurieren der zulässigen Elemente {#configure-eligible-items}

Um geeignete Artikel zu definieren, verwenden Sie den **[!UICONTROL Mögliche Aufgabenkäufe sind auf den folgenden Abschnitt]**:

* Geben Sie bestimmte Element-IDs, Kategorien oder Ziel-IDs ein, getrennt durch Kommas
* Beispiel: `SKU001, SKU002, CategoryA, StoreLocation123`
* **Tipp**: Geben Sie `*` ein, um alle Käufe als geeignet festzulegen (Standardverhalten, wenn leer gelassen)

### Konfigurieren von Ausschlüssen {#configure-exclusions}

Um Elemente aus der Aufgabe auszuschließen, verwenden Sie den Abschnitt **[!UICONTROL Folgende sind von dieser Aufgabe ausgeschlossen]**:

* Geben Sie bestimmte Element-IDs, Kategorien oder Ziel-IDs ein, die nicht für die Aufgabenfertigstellung gezählt werden sollen
* Beispiel: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* Häufige Ausschlüsse: Verkaufs- oder Clearance-Artikel, Geschenkgutscheine, Werbeartikel

>[!NOTE]
>
>Ausschlüsse haben Vorrang vor infrage kommenden Elementen. Wenn ein Element sowohl einem zulässigen Element als auch einem Ausschluss entspricht, wird es von der Aufgabe ausgeschlossen.

## Nächste Schritte {#next-steps}

Jetzt, da Sie wissen, wie Sie Aufgaben erstellen und konfigurieren:

* [Erstellen von Herausforderungen](create-challenges.md) - Erfahren Sie, wie Sie vollständige Herausforderungen erstellen und Belohnungen konfigurieren.
* [Herausforderungen verwalten](manage-challenges.md) - Erfahren Sie, wie Sie Herausforderungen bearbeiten, überwachen und optimieren können.
