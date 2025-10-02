---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden von Adobe Experience Platform-Daten in Journey
description: Erfahren Sie, wie Sie mit der Aktivität „Datensatzsuche“ in Adobe Journey Optimizer Kunden-Journey mit externen Daten aus Adobe Experience Platform anreichern können.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
version: Journey Orchestration
exl-id: b6f54a79-b9e7-4b3a-9a6f-72d5282c01d3
source-git-commit: 189a5e1c31946e05ef88161f0b5d678b95dd2064
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 22%

---

# Verwenden von [!DNL Adobe Experience Platform] in Journey {#datalookup}

>[!CONTEXTUALHELP]
>id="ajo_journey_dataset_lookup"
>title="Aktivität „Datensatzsuche“"
>abstract="Die Aktivität **[!UICONTROL Datensatzsuche]** ermöglicht während der Laufzeit das dynamische Abrufen von Daten aus Adobe Experience Platform-Eintragsdatensätzen. Mit dieser Funktion können Sie auf Daten zugreifen, die sich möglicherweise nicht in der Profil- oder Ereignis-Payload befinden. So können Sie sicherstellen, dass Ihre Kundeninteraktionen sowohl relevant als auch zeitlich passend sind."

Die Aktivität **[!UICONTROL Datensatzsuche]** ermöglicht während der Laufzeit das dynamische Abrufen von Daten aus Adobe Experience Platform-Eintragsdatensätzen. Mit dieser Funktion können Sie auf Daten zugreifen, die sich möglicherweise nicht in der Profil- oder Ereignis-Payload befinden. So können Sie sicherstellen, dass Ihre Kundeninteraktionen sowohl relevant als auch zeitlich passend sind.

Die wichtigsten Vorteile:

* **Echtzeit-Personalisierung**: Personalisieren Sie Kundenerlebnisse mit angereicherten Daten.
* **Dynamische Entscheidungsfindung**: Verwenden Sie externe Daten, um Journey-Logik und -Aktionen zu steuern.
* **Verbesserter Datenzugriff**: Abrufen von Produktmetadaten, Preistabellen oder relationalen Daten, die mit bestimmten Schlüsseln verknüpft sind.

>[!AVAILABILITY]
>
>Diese Aktivität ist nur für ausgewählte Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

## Wichtige Informationen {#must-read}

### Datensatzaktivierung

Der Datensatz muss für die Suche in Adobe Experience Platform aktiviert sein. Detaillierte Informationen finden Sie in diesem Abschnitt: [Verwenden von Adobe Experience Platform-](../data/lookup-aep-data.md).

### Beschränkungen und Einschränkungen

* Es können maximal 10 Datensatzsuchaktivitäten pro Journey verwendet werden.
* Es können maximal 20 Felder ausgewählt werden.
* Maximal 500 Schlüssel im Suchschlüssel-Array.
* Die Größe der angereicherten Daten ist auf 10 KB beschränkt.

### Weitere Überlegungen zur Leistung

Die folgenden Empfehlungen geben Hinweise, wie Sie Verzögerungen bei der Zustellbarkeit vermeiden können:

| Überlegung | Empfohlenes Limit | Beschreibung |
| ------- | ------- | ------- |
| Attribute pro Suche | Bis zu 20 | Anzahl der pro Eintrag in einer einzigen Suchaktivität abgerufenen Datenfelder. |
| Suchaktivitäten | Bis zu 5 pro Journey | Jede Journey kann bis zu 5 verschiedene Suchaktivitäten enthalten. Bei jeder Suche kann ein anderer Datensatz ausgewählt werden. |

## Konfigurieren der Datensatz-Suchaktivität {#configure}

Gehen Sie wie **[!UICONTROL vor, um die Aktivität]** Datensatzsuche“ zu konfigurieren:

1. Erweitern Sie die Kategorie **[!UICONTROL Orchestrierung]** und legen Sie eine Aktivität **[!UICONTROL Datensatzsuche]** auf Ihrer Arbeitsfläche ab.

   ![](assets/aep-data-activity.png)

1. Fügen Sie ein Label und eine Beschreibung hinzu.

1. Wählen **[!UICONTROL im Feld]** den Datensatz mit den benötigten Attributen aus.

   >[!NOTE]
   >
   >Wenn der gesuchte Datensatz nicht in der Liste angezeigt wird, stellen Sie sicher, dass Sie ihn für die Suche aktiviert haben. Weitere Informationen finden Sie im Abschnitt [Muss gelesen werden](#must-read) .

1. Wählen Sie die spezifischen Felder aus, die Sie aus dem Datensatz abrufen möchten.

   * Sie können nur Blattknoten (Felder auf der untersten Ebene des Schemas) auswählen. Das Feld muss ein primitiver Wert sein (Zeichenfolge, Zahl, boolescher Wert, Datum usw.).

   * Listen (Arrays) und Zuordnungen (Schlüssel-Wert-Objekte) können nicht ausgewählt werden.

   +++Beispiel

   ![](assets/aep-data-leaf-primitive.png)

   +++

1. Wählen **[!UICONTROL im Feld]** einen Verbindungsschlüssel aus, der sowohl in den Attributen des Entscheidungselements als auch im Datensatz vorhanden ist. Dieser Schlüssel wird vom System zum Suchen im ausgewählten Datensatz verwendet.

   * Bei Schlüsseln kann es sich um Ausdrücke handeln, die aus dem Journey-Kontext abgeleitet werden, z. B. SKUs, E-Mail-IDs oder andere Kennungen. Beispiel: `@profile.email` oder `list(@event{purchase_event.products.sku})`.

   * Nur **Zeichenfolgen** oder **Zeichenfolgen-Listen** werden unterstützt.

   +++Beispiel

   ![](assets/aep-data-strings.png)

   +++

## Verwenden von angereicherten Daten auf der Journey

Die von der Aktivität **[!UICONTROL Datensatzsuche]** abgerufenen Daten werden im Journey-Kontext als Array von Objekten gespeichert. Sie ist im Journey-Ausdruckseditor und im Personalisierungseditor verfügbar und ermöglicht so bedingte Logik und personalisiertes Messaging auf der Grundlage angereicherter Daten.

* **Journey-Ausdruckseditor**:

  Rufen Sie den **[!UICONTROL Erweiterter Modus]**-Editor auf und verwenden Sie die Syntax `@datasetLookup{MyDatasetLookUpActivity1.entities}` . [Erfahren Sie, wie Sie mit dem erweiterten Ausdruckseditor arbeiten](../building-journeys/expression/expressionadvanced.md)

* **Personalization-Editor**:

  Verwenden Sie die Syntax: `{{context.journey.datasetLookup.1482319411.entities}}`.

>[!NOTE]
>
>Angereicherte Daten sind vorübergehend und nur während der Laufzeit des Journey sowie bei der Personalisierung ausgehender Aktivitäten (E-Mail, Push, SMS usw.) verfügbar

## Beispiele für Anwendungsfälle

+++Produktkategoriebasierte Filterung

**Szenario**:Send ein Gutschein für Benutzer, die mehr als 40 USD für Haushaltsprodukte ausgeben.

**Journey-Fluss**:

1. **Kaufereignis**: Erfassen Sie SKUs aus dem Warenkorb des Benutzers.

1. **Datensatz-Suchaktivität**:
* Datensatz: `products-dataset` (SKU als Primärschlüssel).
* Lookup keys: `list(@event{purchase_event.products.sku})`.
* Zurückzugebende Felder: `["SKU", "category", "price"]`.

1. **Bedingungsaktivität**:

   * Filtern Sie SKUs, bei denen die Kategorie „Haushalt“ lautet.

     ```
     @event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookupActivity1.entities.all(currentDatasetLookupField.category == ‘household’).sku} ) )} 
     ```

   OR

   * Aggregieren Sie die Gesamtausgaben für Haushaltsprodukte und vergleichen Sie sie mit dem Schwellenwert von 40 Dollar.

     ```
     sum(@event{purchase_event.products.all( in(currentEventField.sku, @datasetlookup{MyDatasetLookUpActivity1.entities.all(currentDatasetLookupField.category == ‘household’).sku} ) )}.price}, ',', true ) > 40
     ```

1. **Personalization-Editor**:

   Verwenden Sie die angereicherten Daten, um den E-Mail-Inhalt zu personalisieren:

   ```
   {% let householdTotal = 0 %}
   {{#each journey.datasetlookup.3709000.entities as |product|}}
   {%#if get(product, "category") = "household"%}
   {% let householdTotal = householdTotal + product.price %}{%/if%}
   {{/each}}
   "Hi, thanks for spending " + {%= householdTotal %} + " on household products. Here is your reward!"
   ```

+++

+++Personalization mit externen Treuedaten

**Szenario**: Ermitteln Sie, welches E-Mail-Konto für ein Profil den Treuestatus „Platin“ hat. In diesem Szenario ist das Treuekonto mit einer E-Mail-ID verknüpft und Treuedaten sind im Standardprofil-Suchspeicher nicht verfügbar.

**Journey-Fluss**:

1. **Profilereignis-Trigger**: Erfassen Sie E-Mail-IDs aus dem Profil- oder Ereigniskontext.

1. **Aktivität „Datensatzsuche“**:
   * Datensatz: `loyalty-member-dataset` (E-Mail als Primärschlüssel).
   * Lookup keys: `@profile.email`.
   * Zurückzugebende Felder: `["email", "loyaltyTier"]`.

1. **Bedingungsaktivität**:

   Verzweigen Sie die Journey nach der Treuestufe:

   ```
   @datasetLookup{MyDatasetLookUpActivity1.entity.loyaltyMember.loyaltyTier} == 'Platinum'
   ```

1. **Personalization-Editor**:

   Verwenden Sie die angereicherten Treuestanddaten, um die ausgehende Kommunikation zu personalisieren:

   ```
   {{context.journey.datasetLookup.1482319411.entity.loyaltyMember.loyaltyTier}}
   ```
