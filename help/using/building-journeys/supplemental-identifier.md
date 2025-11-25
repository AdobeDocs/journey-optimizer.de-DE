---
title: Verwenden zusätzlicher Kennungen in Journeys
description: Erfahren Sie, wie Sie zusätzliche Kennungen in Journeys verwenden.
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: ht
source-wordcount: '1424'
ht-degree: 100%

---

# Verwenden zusätzlicher Kennungen in Journeys {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Verwenden einer zusätzlichen Kennung"
>abstract="Die zusätzliche Kennung ist eine sekundäre Kennung, die zusätzlichen Kontext für die Ausführung einer Journey bereitstellt. Um sie zu definieren, das Feld auswählen, das als zusätzliche Kennung verwendet werden soll, und einen Namespace auswählen, der mit ihr verknüpft werden soll."

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="vertical-align: top; padding-right: 20px; border: none;">
      <p>Standardmäßig werden Journeys im Kontext einer <b>Profilkennung</b> ausgeführt. Das bedeutet, dass das Profil nicht erneut in eine andere Journey eintreten kann, solange es in einer bestimmten Journey aktiv ist. Um dies zu verhindern, können Sie mit Journey Optimizer zusätzlich zur Profilkennung eine <b>zusätzliche Kennung</b> in Ihren Ereignissen erfassen, z. B. eine Bestell-ID, Abonnement-ID oder Rezept-ID.  
      <p>In diesem Beispiel haben wir eine <b>Buchungs-ID</b> als zusätzliche Kennung hinzugefügt.</p>
      <p>Dadurch werden die Journeys im Kontext der Profilkennung ausgeführt, die der zusätzlichen Kennung zugeordnet ist (hier die Buchungs-ID). Für jede Iteration der zusätzlichen Kennung wird eine Instanz der Journey ausgeführt. Dadurch kann dieselbe Profilkennung mehrfach in Journeys eintreten, wenn sie unterschiedliche Buchungen vorgenommen haben.</p>
      <p>Darüber hinaus können Sie mit Journey Optimizer die Attribute der zusätzlichen Kennung (z. B. Buchungsnummer, Datum der Rezeptverlängerung, Produkttyp) für die Nachrichtenanpassung nutzen, um eine hochrelevante Kommunikation sicherzustellen. </p>
    </td>
    <td style="vertical-align: top; border: none; text-align: center; width: 40%;">
      <img src="assets/event-supplemental-id.png" alt="Beispiel für eine zusätzliche Kennung" style="max-width:100%;" />
    </td>
  </tr>
</table>

➡️ [Funktion im Video kennenlernen](#video)

## Leitlinien und Einschränkungen {#guardrails}

* **Unterstützte Journeys**: Zusätzliche Kennungen werden bei den Journeys **Ereignisgesteuert** und **Zielgruppe lesen** unterstützt. Sie werden **nicht unterstützt** bei Journeys zur Zielgruppenqualifizierung (d. h. bei Journeys, die mit einer Aktivität des Typs „Zielgruppenqualifizierung“ beginnen).

* **Beschränkungen gleichzeitiger Instanzen**: Profile können nicht über mehr als 10 gleichzeitige Journey-Instanzen verfügen.

* **Häufigkeitsregeln**: Jede Journey-Instanz, die über die Nutzung der zusätzlichen Kennung erstellt wurde, wird der Frequenzbegrenzung angerechnet, auch wenn ein einzelnes Ereignis zu mehreren Journey-Instanzen führt.

* **Datentyp und Schemastruktur**: Die zusätzliche Kennung muss vom Typ `string` sein. Dabei kann es sich um ein unabhängiges Zeichenfolgenattribut oder um ein Zeichenfolgenattribut in einem Array von Objekten handeln. Das unabhängige Zeichenfolgenattribut führt zu einer einzelnen Journey-Instanz, wohingegen das Zeichenfolgenattribut innerhalb eines Arrays von Objekten zu einer eindeutigen Journey-Instanz pro Iteration des Objekt-Arrays führt. Zeichenfolgen-Arrays und Zuordnungen werden nicht unterstützt.

* **Erneuter Eintritt in die Journey**

  Das Verhalten beim erneuten Eintritt in die Journey mit zusätzlichen Kennungen folgt der bestehenden Richtlinie für den erneuten Eintritt:

   * Wenn ein erneuter Eintritt in die Journey nicht möglich ist, kann dieselbe Kombination aus Profilkennung und zusätzlicher ID nicht erneut in die Journey eintreten.
   * Wenn ein erneuter Eintritt in die Journey möglich ist, kann dieselbe Kombination aus Profilkennung und zusätzlicher ID nach dem definierten Zeitfenster erneut eintreten.

* **Datennutzungskennzeichnung und -durchsetzung (Data Use Labeling and Enforcement, DULE)** – Für die zusätzliche ID werden keine DULE-Validierungsprüfungen durchgeführt. Dies bedeutet, dass dieses Attribut nicht berücksichtigt wird, wenn die Journey nach Verstößen gegen Data-Governance-Richtlinien sucht.

* **Konfiguration nachgelagerter Ereignisse**

  Wenn Sie ein weiteres Ereignis nachgelagert in der Journey verwenden, muss es dieselbe zusätzliche ID verwenden und denselben ID-Namespace haben.

* **Journeys vom Typ „Zielgruppe lesen“**

   * Die zusätzliche Kennung ist deaktiviert, wenn Sie ein Geschäftsereignis verwenden.
   * Die zusätzliche Kennung muss ein Feld aus dem Profil sein (d. h. kein Ereignis-/Kontextfeld).
   * Bei Journeys vom Typ „Zielgruppe lesen“, die zusätzliche Kennungen nutzen, ist die Leserate der Aktivität „Zielgruppe lesen“ für jede Journey-Instanz auf maximal 500 Profile pro Sekunde beschränkt.
   * Bei Verwendung von Journeys des Typs „Zielgruppe lesen“ mit zusätzlichen IDs werden nur Zielgruppen des einheitlichen Profildienstes unterstützt.

## Verhalten von Ausstiegskriterien mit zusätzlichen Kennungen {#exit-criteria}

Voraussetzung: Journey für zusätzliche Kennung aktiviert (über einziges Ereignis oder Aktivitäten des Typs „Zielgruppe lesen“)

In der folgenden Tabelle wird das Verhalten von Profilen in einer für eine zusätzliche Kennung aktivierten Journey erläutert, wenn Ausstiegskriterien konfiguriert sind:

| Konfiguration von Ausstiegskriterien | Verhalten, wenn Ausstiegskriterien erfüllt sind |
| ---------------------------- | ---------------------------------- |
| Basierend auf einem Ereignis ohne zusätzliche Kennung | Alle Instanzen des entsprechenden Profils in dieser Journey werden beendet. |
| Basierend auf einem Ereignis mit zusätzlicher Kennung <br/>*Hinweis: Der Namespace der zusätzlichen Kennung muss mit dem des ursprünglichen Knotens übereinstimmen.* | Es werden nur die Instanzen des übereinstimmenden Profils und der zusätzlichen Kennung beendet. |
| Basierend auf einer Zielgruppe | Alle Instanzen des entsprechenden Profils in dieser Journey werden beendet. |

## Hinzufügen einer zusätzlichen Kennung und Verwenden der Kennung in einer Journey {#add}

>[!BEGINTABS]

>[!TAB Durch Ereignis ausgelöste Journey]

Gehen Sie wie folgt vor, um eine zusätzliche Kennung in einer durch ein Ereignis ausgelösten Journey zu verwenden:

1. **Markieren des Attributs als Kennung im Ereignisschema**

   1. Greifen Sie auf das Ereignisschema zu, suchen Sie nach dem Attribut, das Sie als zusätzliche Kennung verwenden möchten (z. B. Buchungs-ID, Abonnement-ID), und markieren Sie es als ID. [Informationen zur Arbeit mit Schemata](../data/get-started-schemas.md)

   1. Markieren Sie die Kennung als **[!UICONTROL Identität]**.

      ![Schemakonfiguration mit Feldgruppe für zusätzliche Kennung](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Stellen Sie sicher, dass Sie das Attribut nicht als **Primäre Identität** markieren.

   1. Wählen Sie den Namespace aus, der mit der zusätzlichen ID verknüpft werden soll. Dies muss ein Namespace ohne Personenkennung sein.

      Nachdem Sie den nicht personenbezogenen Identity-Namespace auf ein Schema angewendet haben, müssen Sie ein neues Ereignis erstellen, um die zusätzliche Kennung verwenden zu können. Bestehende Entitäten können nicht aktualisiert werden, um die neue Kennung zu erkennen.

1. **Hinzufügen der zusätzlichen ID zum Ereignis**

   1. Erstellen oder bearbeiten Sie das gewünschte Ereignis. [Informationen zum Konfigurieren eines unitären Ereignisses](../event/about-creating.md)

   1. Aktivieren Sie im Bildschirm „Ereigniskonfiguration“ die Option **[!UICONTROL Zusätzliche Kennung verwenden]**.

      ![Ereigniskonfiguration mit Namespace-Auswahl für zusätzliche Kennung](assets/supplemental-ID-event.png)

   1. Verwenden Sie den Ausdruckseditor, um das Attribut auszuwählen, das Sie als zusätzliche ID markiert haben.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass Sie den Ausdruckseditor im **[!UICONTROL erweiterten Modus]** verwenden, um das Attribut auszuwählen.

   1. Nach Auswahl der zusätzlichen ID wird der zugehörige Namespace im Bildschirm „Ereigniskonfiguration“ als schreibgeschützt angezeigt.

1. **Hinzufügen des Ereignisses zur Journey**

   Ziehen Sie das konfigurierte Ereignis auf die Journey-Arbeitsfläche. Dadurch wird der Journey-Eintrag basierend auf der Profilkennung und der zusätzlichen ID ausgelöst.

   ![Journey mit zusätzlicher Kennung für Ereignisauslösung](assets/supplemental-ID-journey.png)

>[!TAB Journey vom Typ „Zielgruppe lesen“]

Gehen Sie wie folgt vor, um eine zusätzliche Kennung in einer Journey vom Typ „Zielgruppe lesen“ zu verwenden:

1. **Markieren des Attributs als Kennung im Vereinigungs-/Profilschema**

   1. Greifen Sie auf das Vereinigungs-/Profilschema zu, suchen Sie nach dem Attribut, das Sie als zusätzliche Kennung verwenden möchten (z. B. Buchungs-ID, Abonnement-ID), und markieren Sie es als ID. [Informationen zur Arbeit mit Schemata](../data/get-started-schemas.md)

   1. Markieren Sie die Kennung als **[!UICONTROL Identität]**.

      ![Profilschema mit konfiguriertem Feld für zusätzliche Kennung](assets/supplemental-ID-schema-profile.png)

      >[!IMPORTANT]
      >
      >Stellen Sie sicher, dass Sie das Attribut nicht als **Primäre Identität** markieren.

   1. Wählen Sie den Namespace aus, der mit der zusätzlichen ID verknüpft werden soll. Dies muss ein Namespace ohne Personenkennung sein.

      Nachdem Sie den nicht personenbezogenen Identity-Namespace auf ein Schema angewendet haben, müssen Sie eine neue Feldergruppe erstellen, um die zusätzliche Kennung verwenden zu können. Bestehende Entitäten können nicht aktualisiert werden, um die neue Kennung zu erkennen.

<!--1. **Add the supplemental ID field to the data source**

    1. Navigate to the **[!UICONTROL Configuration]** / **[!UICONTROL Data Sources]** menu, then locate the "ExperiencePlatformDataSource" data source.

        ![Data source configuration with supplemental identifier mapping](assets/supplemental-ID-data-source.png)

    1. Open the field selector then select the attribute you want to use as a supplemental identifier (e.g., booking ID, subscription ID).-->

1. **Hinzufügen und Konfigurieren einer Aktivität „Zielgruppe lesen“ in der Journey**

   1. Ziehen Sie eine Aktivität vom Typ **[!UICONTROL Zielgruppe lesen]** in Ihre Journey.

   1. Aktivieren Sie im Bereich der Aktivitätseigenschaften die Option **[!UICONTROL Zusätzliche Kennung verwenden]**.

      ![Aktivität „Zielgruppe lesen“ mit Konfiguration zusätzlicher Kennung](assets/supplemental-ID-read-audience.png)

   1. Verwenden Sie im Feld **[!UICONTROL Zusätzliche Kennung]** den Ausdruckseditor, um das Attribut auszuwählen, das Sie als zusätzliche Kennung markiert haben.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass Sie den Ausdruckseditor im **[!UICONTROL erweiterten Modus]** verwenden, um das Attribut auszuwählen.

   1. Nach Auswahl der zusätzlichen Kennung wird der zugehörige Namespace im Feld **[!UICONTROL Zusätzlicher Namespace]** als schreibgeschützt angezeigt.

>[!ENDTABS]

## Nutzen der Attribute der zusätzlichen Kennung

Verwenden Sie den Ausdruckseditor und den Personalisierungseditor, um auf Attribute der zusätzlichen Kennung für Personalisierung oder bedingte Logik zu verweisen. Auf Attribute kann über das Menü **[!UICONTROL Kontextuelle Attribute]** zugegriffen werden.

![Personalisierungseditor mit Feldern für zusätzliche Kennung für Inhalte](assets/supplemental-ID-perso.png)

Wenn Sie bei durch ein Ereignis ausgelöste Journeys mit Arrays arbeiten (z. B. mehrere Rezepte oder Richtlinien), verwenden Sie eine Formel, um bestimmte Elemente zu extrahieren.

+++ Siehe Beispiele

In einem Objekt-Array mit der zusätzlichen ID als `bookingNum` und einem Attribut auf derselben Ebene namens `bookingCountry` iteriert die Journey durch das Array-Objekt auf der Grundlage der bookingNum und erstellt für jedes Objekt eine Journey-Instanz.

* Der folgende Ausdruck in der Bedingungsaktivität iteriert durch das Objekt-Array und prüft, ob der Wert von `bookingCountry` gleich „FR“ ist:

  ```
  @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
  ```

* Der folgende Ausdruck im E-Mail-Personalisierungseditor iteriert durch das Objekt-Array, ruft das `bookingCountry` für die aktuelle Journey-Instanz ab und zeigt es im Inhalt an:

  ```
  {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
  
  {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
  
  {{/each}}
  ```

* Beispiel für das Ereignis, das zum Auslösen der Journey verwendet wird:

  ```
  "bookingList": [
        {
            "bookingInfo": {
                "bookingNum": "x1",
                      "bookingCountry": "US"
            }
        },
        {
            "bookingInfo": {
                "bookingNum": "x2",
                "bookingCountry": "FR"
            }
        }
    ]
  ```

+++

## Beispielhafte Anwendungsfälle

### **Benachrichtigungen zur Verlängerung von Policen**

* **Szenario**: Ein Versicherungsanbieter sendet Verlängerungserinnerungen für jede aktive Police einer Kundin oder eines Kunden.
* **Ausführung**:
   * Profil: „John“.
   * Zusätzliche IDs: `"AutoPolicy123", "HomePolicy456"`.
   * Die Journey wird für jede Police separat ausgeführt, mit personalisierten Verlängerungsterminen, Details zur Abdeckung und Premium-Informationen.

### **Abonnementverwaltung**

* **Szenario**: Ein Abonnementdienst sendet maßgeschneiderte Nachrichten für jedes Abonnement, wenn ein Ereignis für dieses Abonnement ausgelöst wird.
* **Ausführung**:
   * Profil: „Jane“.
   * Zusätzliche IDs: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Jedes Ereignis enthält eine Abonnement-ID und Details zu diesem Abonnement. Die Journey wird mit personalisierten Verlängerungsangeboten pro Abonnement für jedes Ereignis/Abonnement separat ausgeführt.

### **Produktempfehlungen**

* **Szenario**: Eine E-Commerce-Plattform sendet Empfehlungen, die auf bestimmten von einer Kundin bzw. einem Kunden gekauften Produkten basieren.
* **Ausführung**:
   * Profil: „Alex“.
   * Zusätzliche IDs: `"productID1234", "productID5678"`.
   * Die Journey wird mit personalisierten Upsell-Optionen für jedes Produkt separat ausgeführt.

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie eine zusätzliche Kennung in [!DNL Adobe Journey Optimizer] aktivieren und anwenden.

>[!VIDEO](https://video.tv.adobe.com/v/3464801?captions=ger&quality=12)
