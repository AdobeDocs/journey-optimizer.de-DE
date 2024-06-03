---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Platform-Daten für die Personalisierung verwenden (Beta)
description: Erfahren Sie, wie Sie Adobe Experience Platform-Daten für die Personalisierung verwenden.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: Ausdruck, Editor
hidefromtoc: true
hide: true
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: d2bebc33b6afde51cef12049cfafc8217c377f9d
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 2%

---

# Adobe Experience Platform-Daten für die Personalisierung verwenden (Beta) {#aep-data}

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur als private Beta-Version verfügbar.
>
>Derzeit ist sie nur für die **E-Mail-Kanal** und zu Testzwecken in der Nicht-Produktions-Sandbox, die Sie der Adobe und den für die Beta-Version angeforderten Datensätzen bereitgestellt haben.

Mit Journey Optimizer können Sie Daten aus Adobe Experience Platform im Personalisierungs-Editor in [Personalisieren des Inhalts](../personalization/personalize.md). Gehen Sie wie folgt vor:

1. Öffnen Sie den Personalisierungs-Editor, der in jedem Kontext verfügbar ist und in dem Sie Personalisierungen wie beispielsweise Nachrichten definieren können. [Erfahren Sie, wie Sie mit dem Personalisierungseditor arbeiten.](../personalization/personalization-build-expressions.md)

1. Navigieren Sie zur Liste der Hilfsfunktionen und fügen Sie die **datasetLookup** Hilfsfunktion zum Codebereich hinzu.

   ![](assets/aep-data-helper.png)

1. Diese Funktion bietet eine vordefinierte Syntax, mit der Sie Felder aus Ihren Adobe Experience Platform-Datensätzen aufrufen können. Es gilt folgende Syntax:

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId** ist die ID des Datensatzes, mit dem Sie arbeiten,
   * **id** ist das Feld, das als primäre Identität im Datensatz verwendet wird;

     >[!NOTE]
     >
     >Der für dieses Feld eingegebene Wert kann entweder die Feld-ID (*profile.couponValue*), ein Feld, das in einem Journey-Ereignis (*context.Journey.events.event_ID.couponValue*) oder einem statischen Wert (*couponAbcd*). In jedem Fall verwendet das System den Wert und sucht in den Datensatz, um zu überprüfen, ob er mit einem Schlüssel übereinstimmt.

   * **result** ist ein beliebiger Name, den Sie bereitstellen müssen, um auf alle Feldwerte zu verweisen, die Sie aus dem Datensatz abrufen werden. Dieser Wert wird in Ihrem Code verwendet, um jedes Feld aufzurufen.

   +++ Wo kann ich eine Datensatz-ID abrufen?

   Datensatz-IDs können in der Adobe Experience Platform-Benutzeroberfläche abgerufen werden. Erfahren Sie im Abschnitt [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

   +++ Wie lässt sich ein primäres Identitätsfeld in einem Datensatz identifizieren?

   Das Feld, das als primäre Identität für einen bestimmten Datensatz definiert wurde, befindet sich im mit dem Datensatz verknüpften Schema. Erfahren Sie im Abschnitt [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity){target="_blank"}.

   ![](assets/aep-data-identity.png)

+++

1. Passen Sie die Syntax an Ihre Anforderungen an. In diesem Beispiel möchten wir Daten zu Passagierflügen abrufen. Es gilt folgende Syntax:

   ```
   {{entity.datasetId="1234567890abcdtId" id="profile.personalEmail.address" result="flight"}}
   ```

   * Wir arbeiten im Datensatz, dessen ID &quot;1234567890abcdtId&quot;lautet.
   * Das in diesem Datensatz als Primärschlüssel verwendete Feld ist die E-Mail-Adresse,
   * Wir möchten alle Feldwerte unter der Referenz &quot;Flug&quot;einbeziehen.

1. Nachdem die im Adobe Experience Platform-Datensatz aufzurufende Syntax konfiguriert wurde, können Sie angeben, welche Felder Sie abrufen möchten. Es gilt folgende Syntax:

   ```
   {{result.fieldId}}
   ```

   * **result** ist der Wert, den Sie dem **result** -Parameter in der **MultiEntity** Helper-Funktion. In diesem Beispiel &quot;flight&quot;.
   * **fieldID** ist die ID des Felds, das Sie abrufen möchten. Diese ID ist in der Adobe Experience Platform-Benutzeroberfläche beim Durchsuchen Ihres Datensatzes sichtbar. Erweitern Sie den folgenden Abschnitt, um ein Beispiel anzuzeigen:

     +++ Wo kann ich eine Feld-ID abrufen?

     Felder-IDs können bei der Vorschau eines Datensatzes in der Benutzeroberfläche von Adobe Experience Platform abgerufen werden. Erfahren Sie, wie Sie eine Vorschau von Datensätzen in der [Adobe Experience Platform-Dokumentation](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   In diesem Beispiel möchten wir Informationen bezüglich der Fluggastzeit und des Flugsteigs verwenden. Fügen Sie daher die beiden folgenden Zeilen hinzu:

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Nachdem Ihr Code fertig ist, können Sie Ihren Inhalt wie gewohnt abschließen und ihn mit dem **Inhalt simulieren** -Schaltfläche, um die Personalisierung zu überprüfen. [Erfahren Sie, wie Sie Inhalte in der Vorschau anzeigen und testen können.](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
