---
solution: Journey Optimizer
product: journey optimizer
title: Testadressen
description: Erfahren Sie, wie Sie Seed-Listen in Journey Optimizer verwenden
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: Testliste, Testliste, Testadressen, Konfiguration
source-git-commit: 1276aa334a057de1a14b7772d07dd9e2ac4f614f
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 13%

---

# Testlisten verwenden {#seed-lists}

Testadressen in [!DNL Journey Optimizer] Sie können automatisch bestimmte Testadressen in Ihre Sendungen einbeziehen.

>[!CAUTION]
>
>Diese Funktion gilt derzeit nur für den E-Mail-Kanal.

Testadressen ermöglichen den Versand an Empfänger, die nicht den vorliegenden Zielgruppenkriterien entsprechen. Auf diese Weise können Empfänger, die außerhalb des Versandperimeters liegen, die Nachricht so wie jeder andere Empfänger innerhalb der Zielgruppe erhalten.

Testadressen sind weder echte Profile noch Testprofile, da sie keine Profildetails enthalten. Es handelt sich lediglich um Empfänger, die zu internen, im System gespeicherten Interessengruppen gehören. Wenn sie in einer bestimmten Kampagne oder Journey ausgewählt werden, werden sie zum Zeitpunkt der Ausführung des Versands einbezogen, d. h. sie erhalten zur Gewährleistung eine Kopie des Versands.

* Durch den Empfang von Sendungen zur gleichen Zeit und unter den gleichen Bedingungen wie Ihre Kunden können Sie mit Seed-Listen die gesendeten E-Mail-Kopien überwachen, um sicherzustellen, dass alle Anzeigeformate, Bilder und Links korrekt sind, und die tatsächlichen Nachrichten, die an Ihre Empfänger gesendet werden, verfolgen.

  Beispiel:

+++ Wenn Sie Marketing-Manager sind:

  Sie möchten, dass alle Teammitglieder Kopien der gesendeten Nachrichten gleichzeitig mit Ihren Kunden erhalten. Auf diese Weise kann Ihr Team sicherstellen, dass Nachrichten mit dem erwarteten Layout, aktiven URLs, korrektem Text und Bildern gesendet werden - alles wie geplant vor der Ausführung.

+++

+++ Wenn Sie Produkteigentümer sind:

  Sie müssen die tatsächlichen Nachrichten verfolgen, die an Kunden gesendet werden. Ihr Team und Ihre Führungsrolle können sich für einige Kampagnen interessieren und müssen auf Ad-hoc-Basis hinzugefügt werden, damit Sie zum Zeitpunkt des Versands Kopien von Nachrichten erhalten können.

+++

* Ein weiterer Grund für die Verwendung von Seed-Listen ist der Schutz Ihrer Mailingliste. Wenn Sie Testadressen in Ihre Mailing-Liste einfügen, können Sie feststellen, ob sie von einem Drittanbieter verwendet wird. Die Testadressen, die darin enthalten sind, erhalten die Sendungen an Ihre Mailing-Liste.

## Zugriff auf Testlisten {#access-seed-lists}

Um auf die bereits erstellten Testlisten zuzugreifen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** und wählen Sie **[!UICONTROL Testliste]**.

>[!CAUTION]
>
>Die Berechtigungen zum Anzeigen, Exportieren und Verwalten der Seed-Listen sind auf [Journey-Administratoren](../administration/ootb-product-profiles.md#journey-administrator). Weitere Informationen zur Verwaltung der Zugriffsberechtigungen für [!DNL Journey Optimizer]-Benutzende finden Sie in [diesem Abschnitt](../administration/permissions-overview.md).

![](assets/seed-list-access.png)

Sie können Seed-Listen nach Namen durchsuchen und/oder nach dem Benutzer filtern, der die Liste erstellt hat, oder nach dem Erstellungsdatum. Nach der Auswahl können Sie den oben in der Liste angezeigten Filter löschen.

![](assets/seed-list-filtering.png)

Verwenden Sie den Button **[!UICONTROL Löschen]**, um einen Eintrag dauerhaft zu entfernen.

>[!CAUTION]
>
>Es ist nicht möglich, eine in einer aktiven [Kampagne](../campaigns/review-activate-campaign.md) oder [Journey](../building-journeys/publishing-the-journey.md). Sie müssen die Kampagne/Journey deaktivieren oder sie bearbeiten, um eine andere Oberfläche zu verwenden, für die die Testliste nicht ausgewählt wurde. [Erfahren Sie mehr über die Verwendung von Testadressen](#use-seed-list)

Sie können auf den Namen einer Testliste klicken, um sie zu bearbeiten. <!--Use the **[!UICONTROL Edit]** button to edit a seed list.-->

## Testliste erstellen {#create-seed-list}

>[!CONTEXTUALHELP]
>id="ajo_seed_list_details"
>title="Testadressen definieren"
>abstract="Füllen Sie die Details der Testliste aus, um automatisch bestimmte Testadressen in Ihre Sendungen einzuschließen. Diese Adressen werden zum Zeitpunkt der Ausführung des Versands hinzugefügt und erhalten aus Sicherheitsgründen eine exakte Kopie des Versands."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=de" text="Was sind Seed-Listen?"

>[!CONTEXTUALHELP]
>id="ajo_seed_addresses"
>title="Zu verwendende Testadressen angeben"
>abstract="Fügen Sie die Testadressen hinzu, die automatisch in Ihre Sendungen eingeschlossen werden. Sie können entweder eine CSV-Datei importieren oder manuell E-Mail-Adressen eingeben."

Gehen Sie wie folgt vor, um eine Testliste zu erstellen.

1. Zugriff auf **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail-Konfiguration]** > **[!UICONTROL Testliste]** Menü.

1. Wählen Sie die **[!UICONTROL Testliste erstellen]** Schaltfläche.

   ![](assets/seed-list-create-button.png)

1. Füllen Sie die Details aus. Fügen Sie zunächst einen Namen hinzu.

   ![](assets/seed-list-details.png)

   >[!NOTE]
   >
   >Namen müssen mit einem Buchstaben (A-Z) beginnen und nur alphanumerische Zeichen oder Sonderzeichen ( _, ., -) enthalten.

1. Wählen Sie den Kanal aus. Derzeit ist nur der E-Mail-Kanal verfügbar.

1. Wählen Sie ein Testprofil aus. Da Testadressen keine Profildetails enthalten, werden mit diesem Testprofil nur die Personalisierungsdaten in der an die Testadressen gesendeten Nachricht angezeigt.

   >[!NOTE]
   >
   >Es kann jeweils nur ein Testprofil ausgewählt werden.

1. Fügen Sie die Testadressen hinzu, an die Sie Ihre Sendungen senden möchten. Sie können entweder eine CSV-Datei importieren oder manuell E-Mail-Adressen eingeben.

   ![](assets/seed-list-email-addresses.png)

   >[!NOTE]
   >
   >Sie können beide Optionen kombinieren, die Gesamtzahl der Adressen in einer Testliste darf jedoch 50 nicht überschreiten.

1. Klicks **[!UICONTROL Erstellen]** zur Bestätigung. Die neu erstellte Seed-Liste wird im [Testlistenbildschirm](#access-seed-lists).

## Testadressen in Kampagnen oder Journey verwenden {#use-seed-list}

Nachdem Sie Ihre Testliste erstellt haben, können Sie sie in jeder Kampagne oder Journey verwenden, um die entsprechenden Testadressen in Ihre Sendungen aufzunehmen. Gehen Sie dazu wie folgt vor.

>[!CAUTION]
>
>Nachrichten, die an Testadressen gesendet werden, sind nicht in Berichten enthalten.

1. Erstellen Sie eine Oberfläche und wählen Sie die **[!UICONTROL Email]** -Kanal. [Weitere Informationen](../email/email-settings.md)

1. Wählen Sie die von Ihnen ausgewählte Seed-Liste im [entsprechenden Abschnitt](../email/email-settings.md#seed-list).

   >[!NOTE]
   >
   >Es kann jeweils nur eine Testliste ausgewählt werden.

   ![](assets/seed-list-surface.png)

1. Senden Sie die Oberfläche.

1. Erstellen Sie eine [Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Wählen Sie die **[!UICONTROL Email]** und wählen Sie die [Oberfläche](channel-surfaces.md) , einschließlich der für Sie relevanten Testliste.

   ![](assets/seed-list-campaign-email.png)

1. Aktivieren Ihrer [Kampagne](../campaigns/review-activate-campaign.md) oder veröffentlichen Sie Ihre [Journey](../building-journeys/publishing-the-journey.md).

Jedes Mal, wenn eine E-Mail-Nachricht über diese Kampagne oder Journey an Ihre Kunden gesendet wird, erhalten die E-Mail-Adressen auf der ausgewählten Testliste diese unter den gleichen Bedingungen, zur gleichen Zeit und mit demselben Inhalt wie die Zielgruppenempfänger.

>[!NOTE]
>
>Bei Journey wird der E-Mail-Versand nur bei der ersten Journey-Ausführung an die Testadressen gesendet.

