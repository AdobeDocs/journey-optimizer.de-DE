---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Anreicherung“
description: Erfahren Sie, wie Sie die Aktivität „Anreicherung“ verwenden.
hide: true
hidefromtoc: true
exl-id: 8a0aeae8-f4f2-4f1d-9b89-28ce573fadfd
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '2049'
ht-degree: 83%

---

# Anreicherung {#enrichment}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment"
>title="Aktivität „Anreicherung“"
>abstract="Die Aktivität **Anreicherung** ermöglicht es Ihnen, die Zielgruppendaten um zusätzliche Informationen aus der Datenbank zu erweitern. Sie wird in einem Workflow häufig nach den Segmentierungsaktivitäten verwendet."


Die Aktivität der **Anreicherung** ist eine **Zielgruppenbestimmungs-Aktivität**. Sie ermöglicht Ihnen, die Zielgruppendaten um zusätzliche Informationen aus der Datenbank zu erweitern. Sie wird in einem Workflow häufig nach den Segmentierungsaktivitäten verwendet.

Anreicherungsdaten können verschiedene Ursprünge haben:

* **Aus derselben Arbeitstabelle** wie die Zielgruppe in Ihrer orchestrierten Kampagne:

  *Bestimmung einer Kundenzielgruppe und Hinzufügen des Felds „Geburtsdatum“ zur aktuellen Arbeitstabelle*

* **Aus einer anderen Arbeitstabelle**:

  *Zielgruppenbestimmung einer Kundengruppe und Hinzufügen der Felder „Betrag“ und „Produkttyp“ aus der „Kauf“-Tabelle*.

Nachdem die Anreicherungsdaten zur orchestrierten Kampagne hinzugefügt wurden, können sie in den Aktivitäten verwendet werden, die nach der Aktivität **Anreicherung** hinzugefügt wurden, um Kundinnen und Kunden basierend auf ihren Verhaltensweisen, Vorlieben und Anforderungen in verschiedene Gruppen zu unterteilen oder um personalisierte Marketing-Nachrichten und -Kampagnen zu erstellen, die Ihre Zielgruppe mit größerer Wahrscheinlichkeit ansprechen.

Sie können der orchestrierten Kampagnen-Arbeitstabelle beispielsweise Informationen zu Käufen von Kundinnen und Kunden hinzufügen und diese Daten verwenden, um E-Mails mit ihrem neuesten Kauf oder dem für diese Käufe ausgegebenen Betrag zu personalisieren.

## Hinzufügen einer Anreicherungsaktivität {#enrichment-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **Anreicherung** zu konfigurieren:

1. Fügen Sie Aktivitäten wie **Zielgruppe erstellen** und **Kombinieren** hinzu.
1. Fügen Sie eine Aktivität vom Typ **Anreicherung** hinzu.
1. Wenn in Ihrer orchestrierten Kampagne mehrere Transitionen konfiguriert wurden, können Sie im Feld **[!UICONTROL Primärer Satz]** definieren, welche Transition als Primärsatz zur Anreicherung mit Daten verwendet werden soll.

## Hinzufügen von Anreicherungsdaten {#enrichment-add}

>[!CONTEXTUALHELP]
>id="ajo_targetdata_personalization_enrichmentdata"
>title="Anreicherungsdaten"
>abstract="Auswahl der Daten, die zur Anreicherung der orchestrierten Kampagne verwendet werden sollen. Sie können zwei Arten von Anreicherungsdaten auswählen: ein einzelnes Anreicherungsattribut aus der Zieldimension oder eine Sammlungsrelation, bei der es sich um eine Verknüpfung mit einer 1:n-Kardinalität zwischen Tabellen handelt."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_data"
>title="Aktivität „Anreicherung“"
>abstract="Nachdem Anreicherungsdaten zur orchestrierten Kampagne hinzugefügt wurden, können sie in den Aktivitäten verwendet werden, die nach der Anreicherungsaktivität hinzugefügt wurden, um Kundinnen und Kunden basierend auf ihren Verhaltensweisen, Vorlieben und Anforderungen in verschiedene Gruppen zu unterteilen oder um personalisierte Marketing-Nachrichten und -Kampagnen zu erstellen, die Ihre Zielgruppe mit größerer Wahrscheinlichkeit ansprechen."

1. Klicken Sie auf **Anreicherungsdaten hinzufügen** und wählen Sie das Attribut zur Datenanreicherung aus.

   Sie können zwei Arten von Anreicherungsdaten auswählen: ein einzelnes Anreicherungsattribut aus der Zielgruppendimension oder eine Sammlungsrelation. Jeder dieser Typen wird in den Beispielen unten detailliert beschrieben:
   * [Einzelnes Anreicherungsattribut](#single-attribute)
   * [Sammlungsrelation](#collection-link)

   >[!NOTE]
   >
   >Sie können im Bildschirm „Attributauswahl“ über die Schaltfläche **Ausdruck bearbeiten** erweiterte Ausdrücke zur Attributauswahl erstellen. 

   ![](../assets/workflow-enrichment1.png)

## Erstellen von Verknüpfungen zwischen Tabellen {#create-links}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_simplejoin"
>title="Verknüpfungsdefinition"
>abstract="Erstellen Sie eine Verknüpfung zwischen den Arbeitstabellendaten und Adobe Journey Optimizer. Wenn Sie beispielsweise Daten aus einer Datei laden, die die Kundennummer, das Land und die E-Mail-Adresse der Empfängerinnen und Empfänger enthält, müssen Sie eine Verknüpfung mit der Ländertabelle erstellen, um die entsprechende Information im Empfängerprofil zu aktualisieren."

Im **[!UICONTROL Link-Definition]** können Sie eine Verknüpfung zwischen den Arbeitstabellendaten und Adobe Journey Optimizer erstellen. Wenn Sie beispielsweise Daten aus einer Datei laden, die die Kundennummer, das Land und die E-Mail-Adresse der Empfängerinnen und Empfänger enthält, müssen Sie eine Verknüpfung mit der Ländertabelle erstellen, um die entsprechende Information im Empfängerprofil zu aktualisieren.

Es stehen verschiedene Relationstypen zur Verfügung:

* **[!UICONTROL Einfache Relation mit Kardinalität 1]**: Jeder Eintrag aus der Hauptmenge kann genau einem Eintrag aus den verknüpften Daten zugeordnet werden.
* **[!UICONTROL Einfache Relation mit Kardinalität 0 oder 1]**: Jeder Eintrag der Hauptmenge kann 0 oder maximal 1 Eintrag der verknüpften Menge zugeordnet werden.
* **[!UICONTROL Sammlungsrelation mit Kardinalität N]**: Jeder Eintrag aus der Hauptmenge kann 0, 1 oder mehr (N) Einträgen der verknüpften Daten zugeordnet werden.

Gehen Sie wie folgt vor, um eine Relation zu erzeugen:

1. Klicken Sie im Abschnitt **[!UICONTROL Relationsdefinition]** auf die Schaltfläche **[!UICONTROL Relation hinzufügen]** .

   ![](../assets/workflow-enrichment-link.png)

1. Wählen Sie in der Dropdown-Liste **Relationstyp** den Relationstyp aus, den Sie erzeugen möchten.

1. Bestimmen Sie die Zielgruppe, die Sie mit der Hauptmenge verknüpfen möchten:

   * Um eine vorhandene Tabelle in der Datenbank zu verknüpfen, wählen Sie **[!UICONTROL Datenbankschema]** aus und wählen Sie dann aus dem Feld **[!UICONTROL Zielschema]** die gewünschte Tabelle aus.
   * Um eine Relation mit Daten aus der eingehenden Transition herzustellen, wählen Sie **Temporäres Schema** und dann die Transition aus, deren Daten Sie verwenden möchten.

1. Definieren Sie die Abstimmkriterien, um die Daten der Hauptmenge mit dem verknüpften Schema abzustimmen. Es gibt zwei Arten von Joins:

   * **Einfacher Join**: Wählen Sie ein bestimmtes Attribut aus, um die Daten aus den beiden Schemata abzugleichen. Klicken Sie auf **Join hinzufügen** und wählen Sie die Attribute **Quelle** und **Ziel** aus, die als Abstimmkriterien verwendet werden.
   * **Erweiterter Join**: Erstellen Sie einen Join mit erweiterten Bedingungen. Klicken Sie auf **Join hinzufügen** und klicken Sie auf die Schaltfläche **Bedingung erstellen**, um den Abfrage-Modeler zu öffnen.

Ein Workflow-Beispiel mit Relationen ist im Abschnitt [Beispiele](#link-example) verfügbar.

## Datenabstimmung {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_reconciliation"
>title="Abstimmung"
>abstract="Die **Anreicherungsaktivität** kann verwendet werden, um Daten aus dem Journey Optimizer-Schema mit Daten aus einem anderen Schema oder mit Daten aus einem temporären Schema abzustimmen, z. B. mit Daten, die mithilfe der Aktivität „Datei laden“ hochgeladen wurden. Diese Art von Verknüpfung definiert eine Abstimmung zu einem eindeutigen Eintrag. Journey Optimizer erstellt einen Link zu einer Zieltabelle, indem ein Fremdschlüssel eingefügt wird, der eine Referenz zum eindeutigen Eintrag enthält."

Die **Abstimmungsaktivität** kann verwendet werden, um Daten aus dem Campaign-Datenbankschema mit Daten aus einem anderen Schema oder mit Daten aus einem temporären Schema abzustimmen, z. B. mit Daten, die mithilfe der Aktivität „Datei laden“ hochgeladen wurden. Diese Art von Verknüpfung definiert eine Abstimmung zu einem eindeutigen Eintrag. Journey Optimizer erstellt einen Link zu einer Zieltabelle, indem ein Fremdschlüssel eingefügt wird, der eine Referenz zum eindeutigen Eintrag enthält.

Mit dieser Option können Sie zum Beispiel das Land eines Profils, das in einer hochgeladenen Datei angegeben ist, mit einem der Länder abstimmen, die in der dedizierten Tabelle der Campaign-Datenbank verfügbar sind.

Führen Sie die Schritte zum Konfigurieren einer **Anreicherungsaktivität** mit einem Abstimm-Link durch:

1. Klicken Sie im Abschnitt **Abstimmung** auf die Schaltfläche **Link hinzufügen**.
1. Identifizieren Sie die Daten, mit denen Sie einen Abstimm-Link erstellen möchten.

   * Um einen Abstimm-Link mit Daten aus der Campaign-Datenbank zu erstellen, wählen Sie **Datenbankschema** und dann das Schema aus, in dem die Zielgruppe gespeichert ist.
   * Um einen Abstimmlink mit den Daten aus der eingehenden Transition zu erstellen, wählen Sie **Temporäres Schema** und wählen Sie die orchestrierte Kampagnentransition, in der die Zieldaten gespeichert werden.

1. Die Felder **Titel** und **Name** werden basierend auf dem ausgewählten Zielschema automatisch ausgefüllt. Ihre Werte können an dieser Stelle geändert werden.

1. Legen Sie im Abschnitt **Abstimmbedingungen** fest, wie Daten aus den Quell- und Zieltabellen abgestimmt werden sollen:

   * **Einfacher Join**: Stimmen Sie ein bestimmtes Feld aus der Quelltabelle mit einem anderen Feld in der Zieltabelle ab. Klicken Sie dazu auf die Schaltfläche **Join hinzufügen** und geben Sie die Felder **Quelle** und **Ziel** an, die für die Abstimmung verwendet werden sollen.

     >[!NOTE]
     >
     >Sie können eine oder mehrere Bedingungen für **Einfacher Join** verwenden. In diesem Fall müssen alle Bedingungen überprüft werden, damit die Daten miteinander verknüpft werden können.

   * **Erweiterter Join**: Konfigurieren Sie die Abstimmbedingungen mithilfe des Abfrage-Modelers.  Klicken Sie dazu auf die Schaltfläche **Bedingung erstellen** und definieren Sie dann Ihre Abstimmbedingungen, indem Sie Ihre eigene Regel mithilfe von UND- und ODER-Operationen erstellen.

Das folgende Beispiel zeigt eine orchestrierte Kampagne, die so konfiguriert wurde, dass eine Verknüpfung zwischen der Journey Optimizer-Profiltabelle und einer temporären Tabelle hergestellt wird, die die Aktivität **Datei laden** generiert. In diesem Beispiel werden mit der Aktivität **Anreicherung** beide Tabellen mithilfe der E-Mail-Adresse als Abstimmkriterium abgestimmt.

![](../assets/enrichment-reconciliation.png)

## Hinzufügen von Angeboten  {#add-offers}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_enrichment_offer_proposition"
>title="Angebotsvorschlag"
>abstract="Die Aktivität „Anreicherung“ ermöglicht das Hinzufügen von Angeboten für jedes Profil."

Mit der Aktivität **[!UICONTROL Anreicherung]** können Sie jedem Profil Angebote hinzufügen.

Gehen Sie wie folgt vor, um die Aktivität **[!UICONTROL Anreicherung]** mit einem Angebot zu konfigurieren:

1. Klicken Sie in der Aktivität **[!UICONTROL Anreicherung]** im Bereich **[!UICONTROL Angebotsvorschlag]** auf die Schaltfläche **[!UICONTROL Angebot hinzufügen]**.

   ![](../assets/enrichment-addoffer.png)

1. Sie haben zwei Möglichkeiten zur Angebotsauswahl:

   * **[!UICONTROL Nach dem besten Angebot in einer Kategorie suchen]**: Beim Aktivieren dieser Option geben Sie die verschiedenen Parameter der Abfrage des Angebotsmoduls an (Platzierung, Kategorie oder Themen, Kontaktdatum, Anzahl der beizubehaltenden Angebote). Das Modul berechnet die besten hinzuzufügenden Angebote, die diesen Parametern entsprechen. Wir empfehlen, entweder das Feld „Kategorie“ oder das Feld „Thema“ vollständig auszufüllen, und nicht beide gleichzeitig.

     ![](../assets/enrichment-bestoffer.png)

   * **[!UICONTROL Vordefiniertes Angebot]**: Beim Aktivieren dieser Option können Sie ohne Abfrage des Angebotsmoduls direkt das einzufügende Angebot konfigurieren (Platzierung, Kontaktdatum).

     ![](../assets/enrichment-predefinedoffer.png)

1. Klicken Sie nach Auswahl des Angebots auf die Schaltfläche **[!UICONTROL Bestätigen]**.

Sie können das Angebot jetzt in der Versandaktivität verwenden.

### Verwenden der Angebote aus der Anreicherungsaktivität

Wenn Sie in einer orchestrierten Kampagne die Angebote verwenden möchten, die Sie aus einer Anreicherungsaktivität in Ihrem Versand erhalten, führen Sie die folgenden Schritte aus:

1. Öffnen Sie die Versandaktivität und navigieren Sie zur Inhaltsbearbeitung. Klicken Sie auf die Schaltfläche **[!UICONTROL Angebotseinstellungen]** und wählen Sie in der Dropdown-Liste die Ihrem Angebot entsprechende **[!UICONTROL Platzierung]** aus.
Wenn Sie nur Angebote aus der Anreicherungsaktivität anzeigen möchten, setzen Sie die Anzahl der **[!UICONTROL Vorschläge]** auf 0 und speichern Sie die Änderungen.

   ![](../assets/offers-settings.png)

1. Wenn Sie im E-Mail-Designer eine Personalisierung mit Angeboten hinzufügen, klicken Sie auf das Symbol **[!UICONTROL Vorschläge]**. Dadurch werden die Angebote angezeigt, die Sie aus der Aktivität **[!UICONTROL Anreicherung]** erhalten. Öffnen Sie das Angebot, das Sie auswählen möchten, indem Sie darauf klicken.

   ![](../assets/offers-propositions.png)

   Navigieren Sie zu **[!UICONTROL Rendering-Funktionen]** und wählen Sie je nach Bedarf **[!UICONTROL HTML-Rendering]** oder **[!UICONTROL Text-Rendering]** aus.

   ![](../assets/offers-rendering.png)

>[!NOTE]
>
>Wenn Sie sich in der Aktivität **[!UICONTROL Anreicherung]** unter der Option **[!UICONTROL Anzahl der beizubehaltenden Angebote]** für mehr als ein Angebot entscheiden, werden alle Angebote angezeigt, wenn Sie auf das Symbol **[!UICONTROL Vorschläge]** klicken.

## Beispiele {#example}

### Einzelnes Anreicherungsattribut {#single-attribute}

Hier fügen wir nur ein einziges Anreicherungsattribut hinzu, z. B. das Geburtsdatum. Führen Sie folgende Schritte aus:

1. Klicken Sie in das Feld **Attribut**.
1. Wählen Sie ein einfaches Feld aus der Zielgruppendimension aus, in unserem Beispiel das Geburtsdatum.
1. Klicken Sie auf **Bestätigen**.

![](../assets/workflow-enrichment2.png)

### Sammlungsrelation {#collection-link}

In diesem komplexeren Anwendungsfall wählen wir eine Sammlungsrelation aus, die eine Verknüpfung mit einer Kardinalität von 1:n zwischen Tabellen darstellt. Rufen wir die drei neuesten Käufe ab, die weniger als 100 € betragen. Dazu müssen Sie Folgendes definieren:

* ein Anreicherungsattribut: das Feld **Preis**
* die Anzahl der abzurufenden Zeilen: 3
* einen Filter: Elemente herausfiltern, die über 100 € liegen
* eine Sortierung: absteigende Sortierung nach dem Feld **Bestelldatum**.

#### Fügen Sie das Attribut hinzu. {#add-attribute}

Hier wählen Sie die Sammlungsrelation aus, um sie als Anreicherungsdaten zu verwenden.

1. Klicken Sie in das Feld **Attribut**.
1. Klicken Sie auf **Erweiterte Attribute anzeigen**.
1. Wählen Sie das Feld **Preis** aus der Tabelle **Käufe**.

<!-- ![](../assets/workflow-enrichment3.png) -->

#### Definieren Sie die Sammlungseinstellungen.{#collection-settings}

Definieren Sie dann, wie die Daten erfasst werden und wie viele Einträge abgerufen werden sollen.

1. Wählen Sie **Daten erfassen** in der Dropdown-Liste **Auswählen, wie die Daten erfasst werden**.
1. Geben Sie „3“ in das Feld **Abzurufende Zeilen (zu erstellende Spalten)** ein.

![](../assets/workflow-enrichment4bis.png)

Wenn Sie beispielsweise die durchschnittliche Anzahl der Käufe für eine Person abrufen möchten, wählen Sie stattdessen **Aggregierte Daten** und wählen Sie **Durchschnitt** in der Dropdown-Liste **Aggregatfunktion**.

Verwenden Sie die Felder **Label** und **Alias** Ihres Attributs, um es verständlicher zu machen, wie unten dargestellt.

![](../assets/workflow-enrichment5bis.png)

#### Definieren von Filtern{#collection-filters}

Hier definieren wir den Maximalwert für das Anreicherungsattribut. Wir filtern Elemente heraus, die mehr als 100 € betragen.
1. Klicken Sie auf **Filter erstellen**.
1. Fügen Sie die beiden folgenden Filter hinzu: **Preis** vorhanden UND **Preis** ist kleiner als 100. Der erste filtert NULL-Werte, da sie als größter Wert erscheinen würden.
1. Klicken Sie auf **Bestätigen**.

![](../assets/workflow-enrichment6bis.png)

#### Definieren der Sortierung{#collection-sorting}

Jetzt müssen wir eine Sortierung anwenden, um die drei **letzten** Käufe abzurufen.

1. Aktivieren Sie die Option **Sortierung aktivieren**.
1. Klicken Sie in das Feld **Attribut**.
1. Wählen Sie das Feld **Bestelldatum**.
1. Klicken Sie auf **Bestätigen**.
1. Wählen Sie **Absteigend** aus der Dropdown-Liste **Sortieren**.

![](../assets/workflow-enrichment7bis.png)

### Anreicherung mit in Relation stehenden Daten {#link-example}

Das folgende Beispiel zeigt eine orchestrierte Kampagne, die so konfiguriert wurde, dass eine Verknüpfung zwischen zwei Transitionen hergestellt wird. Die ersten Transitionen enthalten eine Aktivität zur **Abfrage** von Profildaten einer Zielgruppe, während die zweite Transition Kaufdaten enthält, die in einer Datei gespeichert sind, welche über die Aktivität „Datei laden“ geladen wurde.

![](../assets/enrichment-uc-link.png)

* Die erste **Anreicherungsaktivität** verknüpft den primären Satz (Daten aus der **Abfrageaktivität**) mit dem Schema aus der Aktivität **Datei laden**. Dadurch können wir jedes Profil, das zur Zielgruppe der Abfrage gehört, mit den entsprechenden Kaufdaten abgleichen.

  ![](../assets/enrichment-uc-link-purchases.png)

* Eine zweite Aktivität **Anreicherung** wird hinzugefügt, um Daten aus der orchestrierten Kampagnentabelle mit den Kaufdaten aus der Aktivität **Datei laden** anzureichern. Auf diese Weise können wir diese Daten in weiteren Aktivitäten verwenden, um beispielsweise die an die Kundinnen und Kunden gesendeten Nachrichten mit Informationen zum Kauf zu personalisieren.

  ![](../assets/enrichment-uc-link-data.png)
