---
title: Verwalten der Unterdrückungsliste
description: Erfahren Sie, wie Sie auf die Unterdrückungsliste in Journey Optimizer zugreifen und diese verwalten
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: ht
source-wordcount: '1049'
ht-degree: 100%

---

# Verwalten der Unterdrückungsliste {#manage-suppression-list}

Mit [!DNL Journey Optimizer] können Sie alle E-Mail-Adressen überwachen, die in einer Journey automatisch vom Versand ausgeschlossen sind, z. B.:

* ungültige Adressen (Hardbounces).
* Adressen, die durchgängig zu Softbounces führen und sich negativ auf Ihre E-Mail-Reputation auswirken können, wenn Sie sie weiterhin in Ihre Sendungen aufnehmen.
* Empfänger, die eine Spam-Beschwerde gegen eine Ihrer E-Mails einreichen.

Diese E-Mail-Adressen werden automatisch in der **Unterdrückungsliste** von Journey Optimizer erfasst. Weitere Informationen zum Konzept und zur Verwendung der Unterdrückungsliste finden Sie in [diesem Abschnitt](../reports/suppression-list.md).

## Zugriff auf die Unterdrückungsliste {#access-suppression-list}

Um auf die detaillierte Liste der ausgeschlossenen E-Mail-Adressen zuzugreifen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** und klicken Sie auf **[!UICONTROL Unterdrückungsliste]**.

>[!CAUTION]
>
>Die Berechtigungen zum Anzeigen, Exportieren und Verwalten der Unterdrückungsliste sind auf [Journey-Administratoren](../administration/ootb-product-profiles.md#journey-administrator) beschränkt. Weitere Informationen zur Verwaltung der Zugriffsberechtigungen für [!DNL Journey Optimizer]-Benutzer finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).

![](assets/suppression-list-access.png)

Es stehen Filter zur Verfügung, mit denen Sie die Liste durchsuchen können.

![](assets/suppression-list-filters.png)

Sie können nach **[!UICONTROL Unterdrückungskategorie]**, **[!UICONTROL Adresstyp]** oder **[!UICONTROL Grund]** filtern. Wählen Sie für jedes Kriterium die von Ihnen gewünschten Optionen aus. Nach der Auswahl können Sie einzelne oder alle Filter löschen, die über der Liste angezeigt werden.

![](assets/suppression-list-filtering-example.png)

Wenn Sie versehentlich manuell eine E-Mail-Adresse oder eine Domain hinzugefügt haben, können Sie mit dem Button **[!UICONTROL Löschen]** diesen Eintrag entfernen.

>[!CAUTION]
>
>Verwenden Sie den Button **[!UICONTROL Löschen]** niemals, um unterdrückte E-Mail-Adressen oder Domains zu entfernen.

![](assets/suppression-list-delete.png)

Wenn Sie eine E-Mail-Adresse oder Domain aus der Unterdrückungsliste löschen, wird der Versand an diese Adresse oder Domain wieder aufgenommen. Dies kann sich erheblich auf Ihre Zustellbarkeit und IP-Reputation auswirken und letztendlich dazu führen, dass Ihre IP-Adresse oder Versand-Domain blockiert wird. In [diesem Abschnitt](../reports/suppression-list.md) erfahren Sie mehr darüber, wie wichtig es ist, eine Unterdrückungsliste korrekt zu verwalten.

>[!NOTE]
>
>Gehen Sie beim Löschen von E-Mail-Adressen oder Domains mit besonderer Sorgfalt vor. Wenden Sie sich im Zweifel an einen Zustellbarkeitsexperten.

In der Ansicht **[!UICONTROL Unterdrückungsliste]** können Sie auch Unterdrückungsregeln bearbeiten. [Weitere Informationen](retries.md)

Um die Unterdrückungsliste als CSV-Datei zu exportieren, klicken Sie auf den Button **[!UICONTROL CSV herunterladen]**.

![](assets/suppression-list-download-csv.png)

## Unterdrückungskategorien und -gründe {#suppression-categories-and-reasons}

Wenn eine Nachricht nicht an eine E-Mail-Adresse gesendet werden kann, bestimmt [!DNL Journey Optimizer], warum der Versand fehlgeschlagen ist, und ordnet ihr eine **[!UICONTROL Unterdrückungskategorie]** zu.

Die Unterdrückungskategorien lauten wie folgt:

* **Hard**: Die E-Mail-Adresse wird sofort an die Unterdrückungsliste gesendet.

   >[!NOTE]
   >
   >Wenn der Fehler das Ergebnis einer Spam-Beschwerde ist, fällt er auch in die Kategorie **Hard**. Die E-Mail-Adresse des Empfängers, der die Beschwerde eingereicht hat, wird sofort an die Unterdrückungsliste gesendet.

* **Soft**: Bei Softbounces wird eine Adresse an die Unterdrückungsliste gesendet, sobald der Fehlerzähler den Schwellenwert erreicht hat. [Erfahren Sie mehr über weitere Zustellversuche](retries.md)

* **Manuell**: Sie können der Unterdrückungsliste auch manuell eine E-Mail-Adresse oder eine Domain hinzufügen. [Weitere Informationen](#add-addresses-and-domains)

>[!NOTE]
>
>Weitere Informationen zu Softbounces und Hardbounces finden Sie im Abschnitt [Typen von fehlgeschlagenen Sendungen](../reports/suppression-list.md#delivery-failures).

Für jede aufgelistete E-Mail-Adresse können Sie auch den **[!UICONTROL Typ]** (E-Mail oder Domain), den **[!UICONTROL Grund]**, der zum Ausschluss führte, die Person, die die E-Mail-Adresse zur Unterdrückungsliste hinzufügte, und das Datum mit Uhrzeit, zu dem die Adresse der Unterdrückungsliste hinzugefügt wurde, überprüfen.

![](assets/suppression-list.png)

Mögliche Ursachen für fehlgeschlagene Sendungen sind:

| Grund | Beschreibung | Unterdrückungskategorie |
| --- | --- | --- |
| **[!UICONTROL Ungültiger Empfänger]** | Der Empfänger ist ungültig oder existiert nicht. | Hard |
| **[!UICONTROL Soft-Bounce]** | Die Nachricht führte aus einem anderen Grund als den in dieser Tabelle aufgeführten Soft-Fehlern zu einem Softbounce, z. B. beim Senden über der von einem ISP empfohlenen zulässigen Rate. | Soft |
| **[!UICONTROL DNS-Fehler]** | Die Nachricht führte aufgrund eines DNS-Fehlers zu einem Bounce. | Soft |
| **[!UICONTROL Postfach voll]** | Die Nachricht führte zu einem Bounce, weil das Postfach des Empfängers voll ist und keine weiteren Nachrichten akzeptieren kann. | Soft |
| **[!UICONTROL Weiterleitung verweigert]** | Die Nachricht wurde vom Empfänger blockiert, da eine Weiterleitung nicht zulässig ist. | Soft |
| **[!UICONTROL Challenge-Response]**  | Die Nachricht ist ein Challenge-Response-Test. | Soft |
| **[!UICONTROL Spam-Beschwerde]** | Die Nachricht wurde blockiert, da sie vom Empfänger als Spam gekennzeichnet wurde. | Hard |

>[!NOTE]
>
>Abgemeldete Benutzer erhalten keine E-Mails von [!DNL Journey Optimizer], daher können ihre E-Mail-Adressen nicht an die Unterdrückungsliste gesendet werden. Ihre Entscheidung wird auf der Ebene von Experience Platform gehandhabt. [Weitere Informationen zum Opt-out](../messages/consent.md)

## Adressen und Domains manuell hinzufügen {#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="Hinzufügen von E-Mails/Domains zur Unterdrückungsliste"
>abstract="Sie können die Unterdrückungsliste von Journey Optimizer manuell füllen, um bestimmte E-Mail-Adressen und/oder Domains vom Versand auszuschließen."

Wenn eine Nachricht nicht an eine E-Mail-Adresse gesendet werden kann, wird diese Adresse basierend auf der definierten Unterdrückungsregel oder der Anzahl der Bounces automatisch auf die Unterdrückungsliste gesetzt.

Sie können die [!DNL Journey Optimizer]-Unterdrückungsliste jedoch auch manuell füllen, um bestimmte E-Mail-Adressen und/oder Domains von Ihrem Versand auszuschließen.

Sie können E-Mail-Adressen oder Domains [einzeln](#add-one-address-or-domain) oder [im Bulk-Modus](#upload-csv-file) über einen CSV-Datei-Upload hinzufügen.

Klicken Sie dazu auf den Button **[!UICONTROL E-Mail oder Domain hinzufügen]** und folgen Sie dann einer der folgenden Methoden.

![](assets/suppression-list-add-email.png)

### Eine einzelne Adresse oder Domain hinzufügen {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="Hinzufügen eines Elements zur Unterdrückungsliste"
>abstract="Sie können E-Mail-Adressen und/oder Domains einzeln zur Unterdrückungsliste hinzufügen."

1. Wählen Sie die Option **[!UICONTROL Einzeln]** aus.

   ![](assets/suppression-list-add-email-address.png)

1. Wählen Sie den Adresstyp aus: **[!UICONTROL E-Mail-Adresse]** oder **[!UICONTROL Domain-Adresse]**.

1. Geben Sie die E-Mail-Adresse oder Domain ein, die Sie vom Versand ausschließen möchten.

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass Sie eine gültige E-Mail-Adresse (z. B. abc@company) oder Domain (z. B. abc.company.com) eingeben.

1. Geben Sie bei Bedarf einen Grund an.

1. Klicken Sie auf **[!UICONTROL Senden]**.

### CSV-Datei hochladen {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="Hochladen von CSV-Dateien, um Elemente zur Unterdrückungsliste hinzuzufügen"
>abstract="Sie können eine CSV-Datei mit den E-Mail-Adressen/Domains, die Sie ausschließen möchten, in die Unterdrückungsliste hochladen."

1. Wählen Sie die Option **[!UICONTROL CSV hochladen]** aus.

   ![](assets/suppression-list-upload-csv.png)

1. Laden Sie die zu verwendende CSV-Vorlage herunter, die die folgenden Spalten und das folgende Format enthält:

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```

   Sie können diese Vorlage auch von der Hauptansicht **[!UICONTROL Unterdrückungsliste]** herunterladen.

   >[!CAUTION]
   >
   >Ändern Sie nicht die Namen der Spalten in der CSV-Vorlage.
   >
   >Die Dateigröße darf 1 MB nicht überschreiten.

1. Füllen Sie die CSV-Vorlage mit den E-Mail-Adressen und/oder Domains aus, die Sie der Unterdrückungsliste hinzufügen möchten.

1. Ziehen Sie danach die CSV-Datei per Drag-and-Drop in den entsprechenden Bereich und klicken Sie auf **[!UICONTROL Datei hochladen]**.

   ![](assets/suppression-list-upload-file-button.png)

1. Klicken Sie auf **[!UICONTROL Senden]**.

### Status der letzten Uploads überprüfen {#recent-uploads}

Sie können die Liste der zuletzt hochgeladenen CSV-Dateien überprüfen.

Klicken Sie dazu in der Ansicht **[!UICONTROL Unterdrückungsliste]** auf den Button **[!UICONTROL Letzte Uploads]**.

![](assets/suppression-list-recent-uploads-button.png)

Es werden die neuesten von Ihnen übermittelten Uploads und deren Status angezeigt.

Wenn ein Fehlerbericht mit einer Datei verknüpft ist, können Sie ihn herunterladen, um die aufgetretenen Fehler zu überprüfen.

![](assets/suppression-list-recent-uploads-error.png)

Nachstehend finden Sie ein Beispiel für die Art der Einträge, die Sie im Fehlerbericht finden:

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```
