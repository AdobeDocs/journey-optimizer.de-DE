---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden dynamischer Fragmente
description: Erfahren Sie, wie Sie mit der dynamischen Fragmentauflösung in Adobe Journey Optimizer Fragmente zur Laufzeit basierend auf Profilattributen, Datensatzsuchen oder Kontextdaten auswählen und einfügen können.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: dynamisch, Fragment, Ausdruck, Personalisierung, Laufzeit
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 3%

---

# Verwenden dynamischer Fragmente {#dynamic-fragments}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie mithilfe der dynamischen Fragmentauflösung in Adobe Journey Optimizer festlegen können, welches veröffentlichte Fragment zur Laufzeit in eine Nachricht eingefügt wird. Dies erfolgt auf der Grundlage von Profilattributen, Datensatzsuchen oder Kontextdaten, die zum Sendezeitpunkt übergeben werden.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] unterstützt **dynamische Fragmentauflösung** zur Laufzeit. Damit können Sie anhand von Profilattributen, Datensatzsuchen oder Kontextdaten, die zum Sendezeitpunkt übergeben werden, auswählen, welches veröffentlichte Fragment in eine Nachricht eingefügt wird. Dies ermöglicht hochgradig personalisierte Inhalte ohne Duplizierung der Kampagnen- oder Journey-Logik.

## Überblick {#overview}

**Statische Fragmente** werden zur Entwurfszeit in eine Nachricht eingebettet. Für jeden Empfänger wird dasselbe Fragment verwendet. **Dynamische Fragmente** lösen die Fragment-ID zur Laufzeit pro Empfänger auf. Das bedeutet, dass verschiedene Profile innerhalb derselben Kampagne oder Journey völlig unterschiedliche Inhaltsbausteine erhalten können.

Dynamische Fragment-IDs können aus drei Quellen stammen:

* Eine **Datensatzsuche** - z. B. ein nach Stil oder Produkt verschlüsselter Recommendations-Datensatz
* Ein **Profilattribut**, das in Adobe Experience Platform gespeichert ist
* **Kontextdaten** werden zum Sendezeitpunkt direkt in der API-Anfrage übergeben.

>[!NOTE]
>
>Die Verwendung der Hilfsfunktion `datasetLookup` in Ausdrucksfragmenten ist derzeit für eine begrenzte Anzahl von Kundinnen und Kunden verfügbar. Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support.

## Voraussetzungen {#prerequisites}

Stellen Sie vor der Verwendung dynamischer Fragmente Folgendes sicher:

* Sie verfügen über die erforderlichen Berechtigungen, um Fragmente in [!DNL Journey Optimizer] zu erstellen und zu veröffentlichen. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager)
* Das Fragment, auf das Sie verweisen möchten **ist &quot;**&quot; (Status: **Live**). Entwurfsfragmente können nicht zur Laufzeit aufgelöst werden.
* Wenn die Fragment-ID aus einem Datensatz aufgelöst wird, enthält das Datensatzschema ein Feld, in dem die Fragment-ID gespeichert wird, und der Datensatz wird [für die Suche aktiviert](../data/lookup-aep-data.md).
* Alle Profilattribute, auf die das dynamische Fragment selbst verweist, sind im Nachrichtenexportpfad enthalten oder zum Sendezeitpunkt im Profil verfügbar.

>[!CAUTION]
>
>Fragmentbezogene Validierungen werden im dynamischen Fragmentfluss übersprungen. Ungültige Fragment-IDs werden als Fehler bei der Laufzeitbereitstellung und nicht als Validierungsfehler im Vorfeld angezeigt. Überprüfen Sie vor der Aktivierung einer Kampagne immer, ob die referenzierten Fragment-IDs gültig und veröffentlicht sind.

## Schritt 1: Fragment erstellen und veröffentlichen {#create-fragment}

Bevor ein Fragment dynamisch referenziert werden kann, muss es in [!DNL Journey Optimizer] veröffentlicht werden.

1. Navigieren Sie in [!DNL Journey Optimizer] zu **[!UICONTROL Content-]** > **[!UICONTROL Fragmente]**.

1. Wählen Sie **[!UICONTROL Fragment erstellen]** aus und erstellen Sie den Inhalt. [Erfahren Sie, wie Sie Fragmente erstellen](create-fragments.md)

1. Wenn der Inhalt fertig ist, klicken Sie auf &quot;**[!UICONTROL &quot;]**. Die Veröffentlichung erfolgt asynchron und kann einige Sekunden dauern. Vergewissern Sie sich, dass der Fragmentstatus zu **Live** wechselt, bevor Sie fortfahren.

1. Beachten Sie die **Fragment-ID** in der Detailansicht des Fragments oder in der Fragments-API-Antwort. Sie werden in der Nachricht auf diese ID verweisen.

>[!NOTE]
>
>Sie können alle veröffentlichten Fragment-IDs programmgesteuert über die `GET /fragments`-API abrufen. Weitere Informationen finden Sie in der Dokumentation zu den [Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}APIs .

## Schritt 2: Verfassen Sie die Nachricht mit einem dynamischen Fragmentverweis {#author-message}

Fügen Sie im Personalisierungseditor den Platzhalter für dynamische Fragmente mit der folgenden Syntax ein:

```handlebars
{{fragment id=dynamic_fragment_id}}
```

Die Kennung `dynamic_fragment_id` ist ein Variablenname. Der Wert muss aufgelöst werden, bevor die Fragmentsuche erfolgt. Sie können sie mithilfe eines Datensatzsuchausdrucks, eines Profilattributs oder Kontextdaten auflösen.

### Auflösen über eine Datensatzsuche {#resolve-from-dataset}

Wenn die Fragment-ID in einem AEP-Datensatz gespeichert ist (z. B. in einer Zuordnungstabelle zwischen Stil und Fragment), verwenden Sie die `datasetLookup` Hilfsfunktion, um sie aufzulösen:

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

In diesem Beispiel enthält der Datensatz Zeilen, die durch einen Stilwert (z. B. `style1`) verschlüsselt wurden. Für ein bestimmtes Profil ruft die Suche den entsprechenden Wert der `fragmentId` Spalte ab und weist ihn `dynamic_fragment_id` zu, die dann zum Auflösen des Fragments verwendet wird.

>[!NOTE]
>
>Die Verwendung der Hilfsfunktion `datasetLookup` in Ausdrucksfragmenten ist derzeit für eine begrenzte Anzahl von Kundinnen und Kunden verfügbar. Um Zugriff zu erhalten, wenden Sie sich an den Adobe-Support. Weitere Informationen zur Datensatzsuche in der Personalisierung finden Sie unter [Verwenden von Adobe Experience Platform-Daten](../data/lookup-aep-data.md).

### Aus Kontextdaten auflösen {#resolve-from-context}

Wenn die Fragment-ID zum Zeitpunkt des Versands als Teil des API-Anfragekontexts angegeben wird, verweisen Sie mithilfe des `context`-Namespace darauf:

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

Der `context.audiencePayload` ist das erforderliche Präfix für alle Attribute, die aus einer CSV-Zielgruppendatei stammen oder über den API-Anfragekontext übergeben werden. Der Spaltenname aus der CSV-Datei (z. B. `fragmentId`) folgt dem Präfix .

### Aus einem Profilattribut auflösen {#resolve-from-profile}

Wenn die Fragment-ID in Adobe Experience Platform als Profilattribut gespeichert ist, verweisen Sie direkt darauf:

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## Schritt 3: Konfigurieren Sie Ihren Datensatz für den Suchansatz {#configure-dataset}

Wenn Sie den Ansatz der Datensatzsuche verwenden, aktualisieren Sie Ihr Datensatzschema und Ihre Daten, um die Fragment-ID zu übernehmen.

1. Fügen Sie in Ihren Recommendations- oder Zuordnungsdatensätzen eine Spalte (z. B. `fragmentId`) hinzu, in der die veröffentlichte AJO-Fragment-ID für jede Zeile gespeichert ist.

1. Füllen Sie für jeden Stil bzw. jede Variante (z. B. `style1`, `style2`) die Spalte `fragmentId` mit der entsprechenden Fragment-ID aus.

1. Stellen Sie sicher, dass der Datensatz in Adobe Experience Platform aufgenommen und [für die Suche aktiviert](../data/lookup-aep-data.md) wird.

1. Vergewissern Sie sich, dass alle Profilattribute, auf die im dynamischen Fragment verwiesen wird, in der Nachricht oder in einem statischen Fragment erfasst werden, um ein leeres Rendering zur Exportzeit zu verhindern.

**Beispiel für eine Datensatzstruktur:**

| Spalte | Beispielwert |
|---|---|
| Stil | style1 |
| fragmentId | &lt;fragment-id-1> |
| Stil | style2 |
| fragmentId | &lt;fragment-id-2> |

## Schritt 4: Kontextdaten zum Sendezeitpunkt übergeben {#pass-context-data}

Wenn Sie die Fragment-ID aus Kontextdaten auflösen (z. B. aus einer CSV-Zielgruppenempfehlungsdatei), übergeben Sie die Fragment-ID in der API-Anfrage unter dem erforderlichen Kontextpräfix.

Fügen Sie bei Verwendung der Kampagnen-Proofing-API die Fragment-ID in das `context` ein:

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

Das Präfix `context.audiencePayload` ist erforderlich. Attribute, die unter diesem Schlüssel verschachtelt sind, werden beim Ausführen der Live-Kampagne direkt den Spalten in der CSV-Zielgruppendatei zugeordnet.

## Schritt 5: Testen und Validieren {#proof-validate}

Bevor Sie die Kampagne aktivieren, verwenden Sie die Proofing-API von Campaign , um zu überprüfen, ob das dynamische Fragment korrekt aufgelöst wird und ob die gerenderte E-Mail-Ausgabe wie erwartet aussieht.

1. Erstellen Sie einen Trigger für einen Korrekturabzugsauftrag mithilfe des `POST /campaigns/{id}/proofs`-Endpunkts. Übergeben Sie in der Testversand-Anfrage unter `context.audiencePayload.fragmentId` die Fragment-ID, die Sie testen möchten.

1. Fragen Sie den Status des Korrekturabzugsvorgangs mit dem `GET /campaigns/{id}/proofs/{proofId}`-Endpunkt ab, bis der Status `Submitted` oder `Failed` ist.

1. Überprüfen Sie die zugestellte E-Mail, um sicherzustellen, dass der richtige Fragmentinhalt gerendert wird.

1. Wenn der Fragmentinhalt fehlt oder falsch ist, stellen Sie sicher, dass die Fragment-ID gültig ist, das Fragment veröffentlicht wird und alle erforderlichen Profilattribute vorhanden sind.

Weitere Informationen zur Campaign-API finden Sie in der Dokumentation zu [Journey Optimizer-APIs](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}.

## Leitlinien und Einschränkungen {#guardrails}

>[!CAUTION]
>
>OLAC (Object-Level Access Control) wird für Fragmente im dynamischen Fragmentmodell nicht erzwungen. Stellen Sie sicher, dass Ihre Zugriffskontrollanforderungen auf Kampagnen- und Zielgruppenebene berücksichtigt werden.

Die folgenden Einschränkungen gelten für die Verwendung dynamischer Fragmente:

* **Profilattributabdeckung zur Exportzeit**: Das Fragment wird zur Laufzeit pro Profil ausgewählt. Die für das dynamische Fragment erforderlichen Profilattribute sind nicht im Voraus bekannt. Wenn das dynamische Fragment auf ein Profilattribut angewiesen ist, das nicht in der ursprünglichen Nachricht oder in einem statischen Fragment vorhanden war, auf das in der Nachricht verwiesen wird, kann dieses Feld im Exportpfad leer gerendert werden.

* **Keine vorherige Fragmentvalidierung**: Fragmentbezogene Validierungen werden in diesem Fluss übersprungen. Falsche oder nicht veröffentlichte Fragment-IDs werden in der Benutzeroberfläche als Laufzeitbereitstellungsfehler anstatt als Validierungsfehler angezeigt.

* **Schemaänderung erforderlich für den Datensatzansatz**: Für die Verwendung des Pfads „Lookup-by-ID“ muss das Datensatzschema aktualisiert werden, um die Fragment-ID zu speichern und zu übergeben. Außerdem müssen die erforderlichen Sanitärinstallationen vorhanden sein, um diese in die Nachrichten-Pipeline einzuspeisen.

* **Attributerfassung für den Export**: Stellen Sie sicher, dass alle im dynamischen Fragment verwendeten Attribute in der Nachricht oder in statischen Fragmenten erfasst werden, um ein leeres Rendering im Exportpfad zu verhindern.

Weitere Leitlinien für Fragmente finden Sie in [diesem Abschnitt](../start/guardrails.md#fragments-guardrails).

## Umgang mit Fehlern {#error-handling}

Wenn ein dynamisches Fragment zur Laufzeit nicht aufgelöst werden kann, wird ein Ausschlussereignis für das betroffene Profil generiert. Derzeit werden alle Fehler beim Rendern von Fragmenten als ein einziger allgemeiner Fehlertyp kategorisiert.

So debuggen Sie Fehler bei der Fragmentauflösung:

1. Prüfen Sie die Versandberichte der Kampagne auf Ausschlussereignisse.
1. Überprüfen Sie, ob die zur Laufzeit übergebene Fragment-ID mit einem veröffentlichten Fragment übereinstimmt.
1. Vergewissern Sie sich, dass alle für das Fragment erforderlichen Profilattribute zum Sendezeitpunkt im Profil vorhanden sind.
1. Verwenden Sie die [Proofing-API](#proof-validate) um bestimmte Fragment-IDs zu testen, bevor Sie die Kampagne aktivieren.
