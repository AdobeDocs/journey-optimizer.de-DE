---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Verwenden benutzerdefinierter Upload-Zielgruppen zur Entscheidungsfindung
description: Erfahren Sie, wie Sie benutzerdefinierte Upload-Zielgruppen zur Entscheidungsfindung nutzen.
badge: label="Vorgängerversion" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: bd950410-691b-49d8-8851-8c6c448c00fd
version: Journey Orchestration
source-git-commit: 8dcac6e63f6a38874b3aff4996fc317e3606cb9b
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 97%

---

# Verwenden benutzerdefinierter Upload-Zielgruppen zur Entscheidungsfindung {#custom-upload-decisioning}

>[!TIP]
>
>Die neue Entscheidungsfindungsfunktion in [!DNL Adobe Journey Optimizer] ist jetzt über den Code-basierten Erlebniskanal und den E-Mail-Kanal verfügbar. [Weitere Informationen](../experience-decisioning/gs-experience-decisioning.md)

Mit [!DNL Journey Optimizer] können Sie Daten aus Zielgruppen nutzen, die mit benutzerdefiniertem Upload (CSV-Datei) in [!DNL Adobe Experience Platform] erstellt wurden. Diese Daten unterstützen Ihre Entscheidungs-Management-Workflows. Dies ist besonders nützlich, wenn die Daten nicht im Profil benötigt werden, aber dennoch für Entscheidungszwecke unerlässlich sind.

Daten aus benutzerdefinierten Upload-Zielgruppen können beim Entscheidungs-Management für Folgendes genutzt werden:

1. Eignungskriterien in Angeboten und Entscheidungen
2. Personalisieren von Inhalten in Angebotsdarstellungen

Weiterführende Informationen zu benutzerdefinierten Upload-Zielgruppen finden Sie in den folgenden Abschnitten:

* [Erste Schritte mit Zielgruppen und Journey Optimizer](../audience/about-audiences.md)
* [Importieren einer Zielgruppe in Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## Wichtige Informationen {#must-read}

* **Nur Entscheidungs-Management**: Diese Funktion wird nur beim Entscheidungs-Management unterstützt, nicht bei der Entscheidungsfindung (zuvor „Erlebnis-Entscheidung“).
* **Nur Decisioning-API (Hub)**: Sie ist ausschließlich über Anfragen der Decisioning-API (Hub) verfügbar und wird nicht von der Edge Decisioning-API oder der Batch-Entscheidungsfindung unterstützt.
* **Erforderliches API-Flag für Anreicherungsdaten**: Wenn Sie eine benutzerdefinierte Upload-Zielgruppe (CSV) verwenden und Anreicherungsdaten in der Antwort auf die Angebotsentscheidung abrufen möchten, müssen Sie `"xdm:enrichedAudience": true` in die Payload Ihrer API-Anfrage aufnehmen. Ohne dieses Flag werden Anreicherungsattribute aus der über CSV hochgeladenen Zielgruppe nicht zurückgegeben. [Weitere Informationen zur Decisioning-API](api-reference/offer-delivery-api/decisioning-api.md)

## Verwenden einer benutzerdefinierten Upload-Zielgruppe als Eignungskriterium {#eligibilty}

Sie können eine benutzerdefinierte Upload-Zielgruppe als Eignungskriterium sowohl auf Angebots- als auch auf Entscheidungsebene verwenden. Nach dem Hinzufügen können Angebote oder Sammlungen von Angeboten anhand dieses Kriteriums von der Eignung ausgeschlossen werden. Hier erfahren Sie, wo Sie benutzerdefinierte Upload-Zielgruppen nutzen können, um die Eignung von Angeboten und Entscheidungen einzuschränken:

* Erstellen Sie eine Entscheidungsregel mithilfe einer benutzerdefinierten Upload-Zielgruppe:

   1. Rufen Sie beim Erstellen einer Regel die Registerkarte **Zielgruppen** auf und suchen Sie in der Liste nach Ihrer CSV-Zielgruppe. Ziehen Sie die Zielgruppe in die Arbeitsfläche der Regel.
   1. Verwenden Sie die Registerkarte **Attribute** und navigieren Sie zu Anreicherungsschemata, die mit der ausgewählten Zielgruppe verknüpft sind. Auf diese Weise können Sie auf alle Daten aus der CSV-Datei zugreifen und sie in Ihrer Regel verwenden. [Erfahren Sie, wie Sie eine Entscheidungsregel erstellen können](../offers/offer-library/creating-decision-rules.md).
   1. Speichern Sie die Regel. Nach der Erstellung der Regel kann sie sowohl auf Angebots- als auch auf Entscheidungsebene verwendet werden, um die Eignung einzuschränken.

  ![CSV-Zielgruppe auf der Arbeitsfläche für Entscheidungsregeln](assets/csv-rule.png)

* Verwenden Sie benutzerdefinierte Upload-Zielgruppen als Angebotseinschränkung. [Hinzufügen von Begrenzungen zu einem Angebot](../offers/offer-library/add-constraints.md)

  Beim Erstellen eines Angebots können Sie im Schritt **Einschränkungen hinzufügen** eine der folgenden Aktionen ausführen:

   * Verwenden Sie die benutzerdefinierte Upload-Zielgruppe, um die Eignung eines Angebots zu definieren.
   * Wenden Sie eine Regel an, die die benutzerdefinierte Upload-Zielgruppe nutzt.

  ![Einschränkungsoptionen für benutzerdefinierte Upload-Zielgruppen](assets/csv-offer.png)

* Verwenden Sie benutzerdefinierte Upload-Zielgruppen auf Entscheidungsebene.

  Beim Einrichten einer Entscheidung können Sie im Schritt **Entscheidungsumfang hinzufügen** benutzerdefinierte Upload-Zielgruppen als Bewertungskriterium für eine Sammlung von Angeboten verwenden. [Erfahren Sie, wie Sie Entscheidungsumfänge definieren](../offers/offer-activities/create-offer-activities.md#add-decision-scopes).

  ![Benutzerdefinierte Upload-Zielgruppe auf Entscheidungsebene](assets/csv-decision.png)

## Personalisieren von Angebotsdarstellungen mit einer benutzerdefinierten Upload-Zielgruppe

Benutzerdefinierte Upload-Zielgruppen können ebenfalls verwendet werden, um den Inhalt von Angebotsdarstellungen zu personalisieren, indem auf Daten aus der CSV-Datei verwiesen wird. [Erfahren Sie, wie Sie Darstellungen zu einem Angebot hinzufügen](../offers/offer-library/add-representations.md).

Um die Attribute einer benutzerdefinierten Upload-Zielgruppe zur Personalisierung zu nutzen, müssen Sie zunächst die benutzerdefinierte Zielgruppe als Einschränkung hinzufügen. Fügen Sie hierzu beim Erstellen eines Angebots im Schritt **Einschränkungen hinzufügen** die Zielgruppe als Einschränkung hinzu oder wählen Sie eine Regel aus, die die benutzerdefinierte Upload-Zielgruppe nutzt.

![Einschränkungsoptionen für benutzerdefinierte Upload-Zielgruppen](assets/csv-offer.png)

Nachdem die Zielgruppe als Einschränkung hinzugefügt wurde, können Sie ihre Attribute verwenden, um den Darstellungsinhalt zu personalisieren. Rufen Sie hierzu die Registerkarte **Profilattribute** auf und suchen Sie nach der benutzerdefinierten Upload-Zielgruppe. Wählen Sie die relevanten Attribute aus der Zielgruppe aus, um den Angebotsinhalt zu personalisieren.

Im Entscheidungs-Management werden bei der Personalisierung von Inhalten nur bestimmte Funktionen unterstützt - siehe [Unterstützte Funktionen im Ausdruckseditor](personalization-editor-supported-functions.md).

![Benutzeroberfläche zur Personalisierung von Profilattributen](assets/csv-perso.png)
