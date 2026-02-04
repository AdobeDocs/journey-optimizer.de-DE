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
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 2%

---


# Aufgaben erstellen {#create-tasks}

>[!BEGINSHADEBOX]

**Dokumentation zu Herausforderungen im Zusammenhang mit der Treue:**

* [Erste Schritte mit Herausforderungen im Zusammenhang mit der Treue](get-started.md) - Übersicht, Workflow, Voraussetzungen
* [Herausforderungen im Zusammenhang mit Treue aufrufen und verwalten](access-loyalty-challenges.md) - Inventar-, Herausforderungen- und Aufgabenverwaltung
* [Herausforderungen erstellen](create-challenges.md) - Herausforderungen aufbauen und konfigurieren
* **Aufgaben erstellen** ◀︎ **Sie sind hier** - Herausforderung definieren

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Diese Funktion befindet sich derzeit in der **Private Beta**-Phase und ist in Ihrer Umgebung möglicherweise nicht verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

Aufgaben definieren die spezifischen Aktionen oder Meilensteine, die Kundinnen und Kunden abschließen müssen, um bei einer Herausforderung im Rahmen des Treueprogramms Belohnungen zu erhalten. Sie können Aufgabentypen, Mengen und Produktanforderungen konfigurieren, um ansprechende und personalisierte Treueerlebnisse zu schaffen.

Jede Aufgabe stellt eine messbare Aktion dar, die zum Abschluss der Herausforderung beiträgt. Aufgaben sind wiederverwendbare Komponenten, die unabhängig erstellt und dann zu einer oder mehreren Herausforderungen hinzugefügt oder direkt in einer Herausforderung erstellt werden können.

## Erstellen einer Aufgabe {#create-task}

Sie können Aufgaben aus zwei Einstiegspunkten erstellen. Der Konfigurationsprozess ist unabhängig davon, wo Sie beginnen, identisch.

>[!BEGINTABS]

>[!TAB Aus dem Aufgabeninventar]

Wählen Sie die Registerkarte **[!UICONTROL Aufgaben]** und wählen Sie **[!UICONTROL Aufgabe erstellen]**.

![](assets/task-create-inventory.png)

Aus dem Inventar erstellte Aufgaben werden gespeichert und stehen zur Wiederverwendung über mehrere Herausforderungen hinweg zur Verfügung.

>[!TAB Aus einer Herausforderung]

Öffnen Sie eine bestehende Challenge oder erstellen Sie eine neue. Wählen Sie **[!UICONTROL Aufgabe hinzufügen]** und klicken Sie auf die Schaltfläche **[!UICONTROL Neu]**.

![](assets/task-create-challenge.png)

Auf diese Weise erstellte Aufgaben werden automatisch zu Ihrer Challenge hinzugefügt und auch im Aufgabeninventar gespeichert, um sie in anderen Challenges wiederzuverwenden.

>[!ENDTABS]

## Kundenaktivität auswählen {#choose-activity}

Wählen Sie den Aktivitätstyp aus, den Kunden ausführen müssen, um diese Aufgabe abzuschließen:

* **[!UICONTROL Kauf]**: Kunden müssen einen oder mehrere Artikel kaufen, um diese Aufgabe abzuschließen
* **[!UICONTROL Ausgaben]**: Kunden müssen einen bestimmten Betrag ausgeben, um diese Aufgabe abzuschließen

Um einen Aktivitätstyp auszuwählen, klicken Sie auf das Symbol `+` und wählen Sie die Kundenaktivität aus, die am besten zu Ihren Ergebniszielen passt. Jeder Aktivitätstyp verfügt über bestimmte konfigurierbare Attribute, um die Aufgabenanforderungen weiter zu definieren und zu gestalten.

![](assets/task-create-activitiy.png)

## Attribute definieren {#define-attributes}

Konfigurieren Sie die Aufgabenattribute basierend auf Ihrem ausgewählten Aktivitätstyp:

>[!BEGINTABS]

>[!TAB Kaufaktivität]

![](assets/task-create-purchase.png)

Konfigurieren Sie die folgenden Attribute:

* **[!UICONTROL Menge]**: Geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um diese Aufgabe abzuschließen
* **[!UICONTROL Mögliche Artikel und Ausschlüsse]**: Definieren Sie Artikel oder Artikelgruppen, die für die Aufgabenfertigstellung angerechnet werden, und solche, die dies nicht tun. Weitere Informationen zum [Definieren von zulässigen Elementen und Ausschlüssen](#eligible-items-exclusions)

**Optionale Attribute** (aktiviert über das Symbol „Parameter„):

* **[!UICONTROL Mindestausgabewert-Betrag]**: Legen Sie eine Anforderung für den Mindestbezugsbetrag fest
* **[!UICONTROL Maximale Anzahl an Transaktionen]**: Schränken Sie ein, wie viele Transaktionen zum Abschließen der Aufgabe verwendet werden können

>[!TAB Ausgabenaktivität]

![](assets/task-create-spend.png)

Konfigurieren Sie die folgenden Attribute:

* **[!UICONTROL Betrag]**: Geben Sie den Gesamtbetrag der Ausgaben ein, der erforderlich ist, um die Aufgabe abzuschließen.
* **[!UICONTROL Maximale Anzahl von Transaktionen]**: Geben Sie an, wie viele Transaktionen die Ausgabenanforderung erfüllen dürfen. Sie können dieses Attribut über das Symbol Parameter deaktivieren, wenn Sie die Anzahl der Transaktionen nicht begrenzen möchten.
* **[!UICONTROL Mögliche Elemente und Ausschlüsse]**: (Optional) Definieren Sie Elemente oder Artikelgruppen, die für die Aufgabenfertigstellung zählen, und solche, die nicht zählen. Weitere Informationen zum [Definieren von zulässigen Elementen und Ausschlüssen](#eligible-items-exclusions)

>[!ENDTABS]

## Definieren der zulässigen Elemente und Ausschlüsse {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

Sowohl für **Kauf** als auch für **Ausgaben** können Sie das Attribut **[!UICONTROL Mögliche Artikel und Ausschlüsse]** verwenden, um festzulegen, welche Artikel und Gruppen förderfähig und welche ausgeschlossen sind. Auf diese Weise können Sie bestimmte Produkte, Kategorien oder Standorte auswählen, um sie an Ihre Challenge-Ziele anzupassen.

Anwendungsfälle sind: das Beschränken einer Ausgabenaufgabe auf bestimmte Produktkategorien oder das Ausschließen von Geschenkgutscheinen oder Werbeartikeln von der Zählung bis zum Abschluss einer Aufgabe.

![](assets/tasks-create-eligible.png)

* Um geeignete Artikel zu definieren, verwenden Sie den **[!UICONTROL Mögliche Aufgabenkäufe sind auf den folgenden Abschnitt]**. Geben Sie bestimmte Element-IDs, Kategorien oder Ziel-IDs ein, getrennt durch Kommas.

  Beispiel: `SKU001, SKU002, CategoryA`

  Geben Sie `*` ein, um alle Käufe als geeignet festzulegen (Standardverhalten, wenn leer gelassen).

* Um Elemente aus der Aufgabe auszuschließen, verwenden Sie den Abschnitt **[!UICONTROL Folgende sind von dieser Aufgabe ausgeschlossen]**. Geben Sie bestimmte Element-IDs, Kategorien oder Ziel-IDs ein, die nicht für die Aufgabenfertigstellung gezählt werden sollen.

  Beispiel: `CLEARANCE01, GIFTCARD, SALE_CATEGORY`

  >[!NOTE]
  >
  >Ausschlüsse haben Vorrang vor infrage kommenden Elementen. Wenn ein Element sowohl einem zulässigen Element als auch einem Ausschluss entspricht, wird es von der Aufgabe ausgeschlossen.

## Aufgabeneigenschaften definieren {#define-task-properties}

Konfigurieren Sie im Bereich **[!UICONTROL Eigenschaften]** die grundlegenden Informationen zur Aufgabe:

* **[!UICONTROL Aufgabenname]**: Geben Sie einen beschreibenden Namen für die Aufgabe ein. Dieser Name ist für Sie und Ihr Team sichtbar, wird Kunden jedoch möglicherweise nicht angezeigt, je nach Design Ihrer Inhaltskarte.
* **[!UICONTROL Aufgabenbeschreibung]**: Die Beschreibung wird automatisch basierend auf dem Aktivitätstyp und den Attributen generiert, die Sie für die Aufgabe konfigurieren. Sie können die automatische Generierung deaktivieren und bei Bedarf eine benutzerdefinierte Beschreibung eingeben.

![](assets/tasks-create-properties.png)

Klicken Sie nach dem Konfigurieren aller Attribute und Eigenschaften auf **[!UICONTROL Erstellen]**, um die Aufgabe zu speichern. Die Aufgabe wird in Ihrem Aufgabeninventar gespeichert und, wenn sie innerhalb einer Herausforderung erstellt wurde, automatisch zu dieser Herausforderung hinzugefügt.
