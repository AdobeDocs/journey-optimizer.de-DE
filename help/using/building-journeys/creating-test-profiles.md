---
title: Erstellen eines Testprofils
description: Erfahren Sie, wie Sie ein Testprofil erstellen
feature: Journeys
topic: Content-Management
role: User
level: Intermediate
source-git-commit: 8dfa7a7700e1bb452ea9cd5e7d0adb6df55de03b
workflow-type: tm+mt
source-wordcount: '1366'
ht-degree: 55%

---

# Erstellen von Testprofilen {#create-test-profiles}

Testprofile sind bei der Verwendung des Testmodus erforderlich. So erfahren Sie, wie Sie den [Testmodus](../building-journeys/testing-the-journey.md) in einer Journey verwenden und [Ihre Nachrichten in der Vorschau anzeigen und testen](../preview.md).

Die verfügbaren Methoden zum Erstellen von Testprofilen werden nachfolgend beschrieben:

* Sie können ein [vorhandenes Profil](#turning-profile-into-test) in ein Testprofil umwandeln

* Sie können ein Testprofil erstellen, indem Sie eine [CSV-Datei](#create-test-profiles-csv) hochladen oder [API-Aufrufe](#create-test-profiles-api) verwenden. Zusätzlich zu diesen beiden Methoden bietet Adobe Journey Optimizer einen speziellen [Anwendungsfall für das In-Produkt](#use-case-1), um die Erstellung von Testprofilen zu erleichtern.

* Sie können auch eine JSON-Datei in einen Datensatz hochladen. Weitere Informationen hierzu finden Sie in der [Dokumentation zur Datenerfassung](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=de#add-data-to-dataset).

Beachten Sie, dass das Erstellen eines Testprofils mit dem Erstellen regulärer Profile in Adobe Experience Platform vergleichbar ist. Weitere Informationen finden Sie in der [Dokumentation zu Echtzeit-Kundenprofilen](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de).

## Voraussetzungen    {#test-profile-prerequisites}

Um Profile erstellen zu können, müssen Sie zunächst ein Schema und einen Datensatz in Adobe [!DNL Journey Optimizer] erstellen.

Zuerst müssen Sie **ein Schema erstellen**. Führen Sie folgende Schritte aus:

1. Klicken Sie im Menüabschnitt DATA MANAGEMENT auf **[!UICONTROL Schemas]**.
   ![](../assets/test-profiles-0.png)
1. Klicken Sie oben rechts auf **[!UICONTROL Schema erstellen]** und wählen Sie dann einen Schematyp aus, z. B. **Einzelnes XDM-Profil**.
   ![](../assets/test-profiles-1.png)
1. Wählen Sie die entsprechenden Feldgruppen aus. Stellen Sie sicher, dass Sie die Feldgruppe **Profil-Testdetails** hinzufügen.
   ![](../assets/test-profiles-1-ter.png)
Klicken Sie abschließend auf **[!UICONTROL Feldgruppen hinzufügen]**: Die Liste der Feldgruppen wird im Bildschirm „Schemaübersicht“ angezeigt.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Klicken Sie auf den Namen des Schemas, um es zu ändern und seine Eigenschaften zu aktualisieren.
      >
      >
   * Klicken Sie im Abschnitt „Feldgruppen“ auf die Schaltfläche **[!UICONTROL Hinzufügen]**, um andere Feldgruppen auszuwählen, die dem Schema hinzugefügt werden sollen.


1. Klicken Sie in der Liste der Felder auf das Feld, das Sie als die primäre Identität definieren möchten.
   ![](../assets/test-profiles-3.png)
1. Aktivieren Sie im rechten Bereich **[!UICONTROL Feldeigenschaften]** die Optionen **[!UICONTROL Identität]** und **[!UICONTROL Primäre Identität]** und wählen Sie einen Namespace aus. Wenn die primäre Identität eine E-Mail-Adresse sein soll, wählen Sie den Namespace **[!UICONTROL E-Mail]**. Klicken Sie auf **[!UICONTROL Übernehmen]**.
   ![](../assets/test-profiles-4bis.png)
1. Wählen Sie das Schema aus und aktivieren Sie die Option **[!UICONTROL Profil]** im Bereich **[!UICONTROL Schemaeigenschaften]** .
   ![](../assets/test-profiles-5.png)
1. Klicken Sie auf **Speichern**.

>[!NOTE]
>
>Weitere Informationen zur Erstellung von Schemata finden Sie in der [XDM-Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=de#prerequisites).

Anschließend müssen Sie **den Datensatz erstellen**, in den die Profile importiert werden. Führen Sie folgende Schritte aus:

1. Gehen Sie zu **[!UICONTROL Datensätze]** und klicken Sie dann auf **[!UICONTROL Datensatz erstellen]**.
   ![](../assets/test-profiles-6.png)
1. Wählen Sie **[!UICONTROL Datensatz aus Schema erstellen]** aus.
   ![](../assets/test-profiles-7.png)
1. Wählen Sie das zuvor erstellte Schema aus und klicken Sie dann auf **[!UICONTROL Weiter]**.
   ![](../assets/test-profiles-8.png)
1. Wählen Sie einen Namen und klicken Sie dann auf **[!UICONTROL Beenden]**.
   ![](../assets/test-profiles-9.png)
1. Aktivieren Sie die Option **[!UICONTROL Profil]**.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> Weitere Informationen zur Erstellung von Datensätzen finden Sie in der [Dokumentation zum Katalogdienst](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=de#getting-started).

## Anwendungsfall für das Produkt{#use-case-1}

Auf der Adobe Journey Optimizer-Startseite können Sie die Anwendungsfälle für Testprofile im Produkt nutzen. Dieser Anwendungsfall erleichtert die Erstellung von Testprofilen, die vor der Veröffentlichung zum Testen von Journey verwendet werden.

![](../assets/use-cases-home.png)

Klicken Sie auf die Schaltfläche **[!UICONTROL Starten]** , um den Anwendungsfall zu starten.

Die folgenden Informationen werden benötigt:

1. **Identitäts-Namespace**: Der  [Identitäts-](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=de) Namespace, mit dem die Testprofile eindeutig identifiziert werden. Wenn beispielsweise E-Mail zur Identifizierung der Testprofile verwendet wird, sollte der Identitäts-Namespace **E-Mail** ausgewählt werden. Wenn die eindeutige Kennung die Telefonnummer ist, sollte der Identitäts-Namespace **Phone** ausgewählt werden.

2. **CSV-Datei**: Eine kommagetrennte Datei, die die Liste der zu erstellenden Testprofile enthält. Der Anwendungsfall erwartet ein vordefiniertes Format für die CSV-Datei, die die Liste der zu erstellenden Testprofile enthält. Jede Zeile in der Datei sollte die folgenden Felder in der richtigen Reihenfolge wie folgt enthalten:

   1. **Personen-ID**: Eindeutige Kennung des Testprofils. Die Werte dieses Felds sollten den ausgewählten Identitäts-Namespace widerspiegeln. (Wenn beispielsweise **Phone** für den Identitäts-Namespace ausgewählt ist, sollten die Werte dieses Felds Telefonnummern sein. Wenn **E-Mail** ausgewählt ist, sollten die Werte dieses Felds E-Mails sein.
   1. **E-Mail-Adresse**: E-Mail-Adresse des Testprofils. (Das Feld **Personen-ID** und das Feld **E-Mail-Adresse** können möglicherweise dieselben Werte enthalten, wenn **E-Mail** als Identitäts-Namespace ausgewählt ist.)
   1. **Vorname**: Vorname des Testprofils.
   1. **Nachname**: Nachname des Testprofils.
   1. **Ort**: Testprofilstadt des Wohnsitzes
   1. **Land**: Testprofil Land des Wohnsitzes
   1. **Geschlecht**: Testprofil-Geschlecht. Verfügbare Werte sind **male**, **female** und **non_specified**

Nachdem Sie den Identitäts-Namespace ausgewählt und die CSV-Datei basierend auf dem oben stehenden Format bereitgestellt haben, klicken Sie oben rechts auf die Schaltfläche **[!UICONTROL Ausführen]** . Der Anwendungsfall kann einige Minuten dauern. Sobald der Anwendungsfall die Verarbeitung und Erstellung der Testprofile abgeschlossen hat, wird eine Benachrichtigung gesendet, um den Benutzer zu benachrichtigen.

>[!NOTE]
>
>Testprofile können vorhandene Profile überschreiben. Bevor Sie den Anwendungsfall ausführen, stellen Sie sicher, dass die CSV-Datei nur Testprofile enthält und dass sie für die richtige Sandbox ausgeführt wird.

## Umwandeln eines Profils in ein Testprofil {#turning-profile-into-test}

So können Sie ein vorhandenes Profil in ein Testprofil umwandeln: Sie können Profilattribute auf dieselbe Weise aktualisieren wie bei der Erstellung eines Profils.

Eine einfache Möglichkeit besteht darin, die Aktionsaktivität **[!UICONTROL Profil]** in einer Journey zu verwenden und das boolesche Feld testProfile von false in true zu ändern.

Ihre Journey besteht aus einer **[!UICONTROL Segment lesen]** und einer **[!UICONTROL Profil-Update]** -Aktivität. Zunächst müssen Sie ein Segment erstellen, das auf die Profile zielt, die Sie in Testprofile umwandeln möchten.

>[!NOTE]
>
> Da Sie das Feld **testProfile** aktualisieren werden, müssen die ausgewählten Profile dieses Feld enthalten. Das zugehörige Schema muss über die Feldergruppe **Profiltestdetails** verfügen. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Gehen Sie oben rechts zu **Segmente** und dann zu **Segment erstellen**.
   ![](../assets/test-profiles-22.png)
1. Definieren Sie einen Namen für Ihr Segment und erstellen Sie das Segment: Wählen Sie die Felder und Werte aus, um die gewünschten Profile anzusprechen.
   ![](../assets/test-profiles-23.png)
1. Klicken Sie auf **Speichern** und prüfen Sie, ob die Profile korrekt durch das Segment angesprochen werden.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > Die Segmentberechnung kann einige Zeit in Anspruch nehmen. Weitere Informationen zu Segmenten finden Sie in [diesem Abschnitt](../segment/about-segments.md).

1. Erstellen Sie nun eine neue Journey und beginnen Sie mit einer Orchestrierungsaktivität **[!UICONTROL Segment lesen]** .
1. Wählen Sie das zuvor erstellte Segment und den Namespace aus, den Ihre Profile verwenden.
   ![](../assets/test-profiles-25.png)
1. Fügen Sie die Aktionsaktivität **[!UICONTROL Profil aktualisieren]** hinzu.
1. Wählen Sie das Schema, das Feld **testProfiles** und den Datensatz aus und legen Sie den Wert auf **true** fest. Klicken Sie dazu im Feld **[!UICONTROL WERT]** auf das **Stift**-Symbol rechts, wählen Sie **[!UICONTROL Erweiterter Modus]** aus und geben Sie **true** ein.
   ![](../assets/test-profiles-26.png)
1. Fügen Sie eine Aktivität des Typs **Ende** hinzu und klicken Sie auf **[!UICONTROL Veröffentlichen]**.
1. Überprüfen Sie im Abschnitt **[!UICONTROL Segmente]**, ob die Profile korrekt aktualisiert wurden.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Weitere Informationen zur Aktivität **[!UICONTROL Profil aktualisieren]** finden Sie in [diesem Abschnitt](../building-journeys/update-profiles.md).

## Erstellen eines Testprofils mithilfe einer CSV-Datei {#create-test-profiles-csv}

In Adobe Experience Platform können Sie Profile erstellen, indem Sie eine CSV-Datei, die die verschiedenen Profilfelder enthält, in Ihren Datensatz hochladen. Dies ist die einfachste Methode.

1. Erstellen Sie mit einer Tabellenkalkulations-Software eine einfache CSV-Datei.
1. Fügen Sie für jedes erforderliche Feld eine Spalte hinzu. Stellen Sie sicher, dass Sie das primäre Identitätsfeld („personID“ in unserem Beispiel oben) und das Feld „testProfile“ auf „true“ gesetzt hinzufügen.
   ![](../assets/test-profiles-11.png)
1. Fügen Sie pro Profil eine Zeile hinzu und geben Sie die Werte für die einzelnen Felder ein.
   ![](../assets/test-profiles-12.png)
1. Speichern Sie die Tabelle als CSV-Datei. Verwenden Sie als Trennzeichen Kommas.
1. Gehen Sie zu Adobe Experience Platform-**Workflows**.
   ![](../assets/test-profiles-14.png)
1. Wählen Sie **CSV einem XDM-Schema zuordnen** und klicken Sie dann auf **Starten**.
   ![](../assets/test-profiles-16.png)
1. Wählen Sie den Datensatz aus, in den Sie die Profile importieren möchten. Klicken Sie auf **Weiter**.
   ![](../assets/test-profiles-17.png)
1. Klicken Sie auf **Datei auswählen** und wählen Sie Ihre CSV-Datei aus. Klicken Sie nach dem Hochladen der Datei auf **Weiter**.
   ![](../assets/test-profiles-18.png)
1. Ordnen Sie die CSV-Quellfelder den Feldern des Schemas zu und klicken Sie dann auf **Beenden**.
   ![](../assets/test-profiles-19.png)
1. Der Datenimport beginnt. Der Status wechselt von **Verarbeitungsvorgang läuft** zu **Erfolg**. Klicken Sie oben rechts auf **Datensatz-Vorschau**.
   ![](../assets/test-profiles-20.png)
1. Vergewissern Sie sich, dass die Testprofile korrekt hinzugefügt wurden.
   ![](../assets/test-profiles-21.png)

Ihre Testprofile werden hinzugefügt und können jetzt beim Testen einer Journey verwendet werden. Weitere Informationen finden Sie in [diesem Abschnitt](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Weitere Informationen zu CSV-Importen finden Sie in der [Dokumentation zur Datenaufnahme](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=de#tutorials).

## Erstellen von Testprofilen mithilfe von API-Aufrufen {#create-test-profiles-api}

Sie können Testprofile auch über API-Aufrufe erstellen. Weiterführende Informationen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

Sie müssen ein Profilschema verwenden, das die Feldergruppe &quot;Profiltestdetails&quot;enthält. Das Flag testProfile ist Teil dieser Feldergruppe.
Achten Sie beim Erstellen eines Profils darauf, diesen Wert zu übergeben: testProfile = true.

Beachten Sie, dass Sie auch ein vorhandenes Profil aktualisieren können, um die Markierung „testProfile“ in „true“ zu ändern.

Hier sehen Sie ein Beispiel für einen API-Aufruf zum Erstellen eines Testprofils:

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```
