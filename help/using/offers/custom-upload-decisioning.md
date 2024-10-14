---
title: Verwenden benutzerdefinierter Upload-Zielgruppen für Entscheidungen
description: Erfahren Sie, wie Sie benutzerdefinierte Upload-Zielgruppen für Entscheidungen nutzen können.
feature: Decision Management
role: User
level: Intermediate
source-git-commit: 1e46321de543196277613889c438dc6756e45652
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 1%

---


# Verwenden benutzerdefinierter Upload-Zielgruppen für Entscheidungen {#custom-upload-decisioning}

Mit Journey Optimizer können Sie Daten aus Zielgruppen nutzen, die mit benutzerdefiniertem Upload (CSV-Datei) in Adobe Experience Platform erstellt wurden, um Ihre Entscheidungsmanagement-Workflows zu unterstützen. Dies ist besonders nützlich, wenn die Daten nicht im Profil benötigt werden, aber dennoch für Entscheidungszwecke unerlässlich sind.

Daten aus benutzerdefinierten Upload-Zielgruppen können im Entscheidungsmanagement für Folgendes genutzt werden:

1. Eignungskriterien in Angeboten und Entscheidungen.
2. Personalisieren von Inhalten in Angebotsdarstellungen.

Weiterführende Informationen zu benutzerdefinierten Upload-Zielgruppen finden Sie in den folgenden Abschnitten:
* [Erste Schritte mit Zielgruppen und Journey Optimizer](../audience/about-audiences.md)
* [Importieren einer Zielgruppe in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## Wichtige Informationen {#must-read}

* Diese Funktion wird nur in **Entscheidungsverwaltung** unterstützt, nicht in Decisioning (ehemals &quot;Experience Decisioning&quot;).
* Sie ist ausschließlich über **Decisioning API (Hub)** -Anfragen verfügbar und wird nicht von der **Edge Decisioning API** oder der **Batch Decisioning** unterstützt.
 
## Verwenden einer benutzerdefinierten Upload-Zielgruppe als Berechtigungskriterien {#eligibilty}

Sie können eine benutzerdefinierte Upload-Zielgruppe als Eignungskriterien sowohl auf Angebots- als auch auf Entscheidungsebene verwenden. Nach dem Hinzufügen können diese Kriterien Angebote oder Kollektionen von Angeboten von der Eignung ausschließen. Hier finden Sie die verschiedenen Stellen, an denen Sie benutzerdefinierte Upload-Zielgruppen nutzen können, um die Eignung von Angeboten und Entscheidungen zu verfeinern:

* Erstellen Sie eine Entscheidungsregel mit einer benutzerdefinierten Upload-Zielgruppe:

   1. Rufen Sie beim Erstellen einer Regel die Registerkarte **Zielgruppen** auf und suchen Sie in der Liste nach Ihrer CSV-Zielgruppe. Ziehen Sie die Zielgruppe in die Arbeitsfläche der Regel.
   1. Verwenden Sie die Registerkarte **Attribute** und navigieren Sie zu den mit der ausgewählten Zielgruppe verknüpften Anreicherungsschemata, um auf alle Daten aus der CSV-Datei zuzugreifen und sie in Ihrer Regel zu verwenden. Auf diese Weise können Sie ein Feld aus der CSV-Datei verwenden, um Ihre Regel zu verfeinern. [Erfahren Sie, wie Sie eine Entscheidungsregel erstellen](../offers/offer-library/creating-decision-rules.md)
   1. Speichern Sie die Regel. Nach der Erstellung der Regel kann sie sowohl auf Angebots- als auch auf Entscheidungsebene verwendet werden, um ihre Eignung einzuschränken.

  ![](assets/csv-rule.png)

* Verwenden Sie benutzerdefinierte Upload-Zielgruppen als Angebotsbegrenzung. [Hinzufügen von Begrenzungen zu einem Angebot](../offers/offer-library/add-constraints.md)

  Beim Erstellen eines Angebots können Sie im Schritt **Einschränkungen hinzufügen** eine der folgenden Aktionen ausführen:

   * Verwenden Sie die benutzerdefinierte Upload-Zielgruppe, um die Eignung eines Angebots zu definieren.
   * Wenden Sie eine Regel an, die die benutzerdefinierte Upload-Zielgruppe nutzt.

  ![](assets/csv-offer.png)

* Verwenden Sie benutzerdefinierte Upload-Zielgruppen auf Entscheidungsebene.

  Beim Einrichten einer Entscheidung können Sie im Schritt **Entscheidungsbereich hinzufügen** benutzerdefinierte Upload-Zielgruppen als Bewertungskriterium für eine Angebotskollektion verwenden. [Erfahren Sie, wie Sie den Entscheidungsbereich definieren](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## Verwenden einer benutzerdefinierten Upload-Zielgruppe, um Angebotsdarstellungen zu personalisieren

Benutzerdefinierte Upload-Zielgruppen können auch verwendet werden, um den Inhalt von Angebotsdarstellungen zu personalisieren, indem auf Daten aus der CSV-Datei verwiesen wird. [Erfahren Sie, wie Sie einem Angebot Darstellungen hinzufügen](../offers/offer-library/add-representations.md)

Um die Attribute einer benutzerdefinierten Upload-Zielgruppe für die Personalisierung nutzen zu können, müssen Sie zunächst die benutzerdefinierte Zielgruppe als Einschränkung hinzufügen. Fügen Sie dazu beim Erstellen eines Angebots im Schritt **Einschränkungen hinzufügen** die Zielgruppe als Begrenzungen hinzu oder wählen Sie eine Regel aus, die die benutzerdefinierte Upload-Zielgruppe nutzt.

![](assets/csv-offer.png)

Nachdem die Zielgruppe als Einschränkung hinzugefügt wurde, können Sie ihre Attribute verwenden, um den Darstellungsinhalt zu personalisieren. Rufen Sie dazu die Registerkarte **Profilattribute** auf und suchen Sie nach der benutzerdefinierten Upload-Zielgruppe. Wählen Sie die relevanten Attribute aus der Audience aus, um den Angebotsinhalt zu personalisieren.

![](assets/csv-perso.png)
