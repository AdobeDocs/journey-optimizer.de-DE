---
title: Erstellen einer Landingpage
description: Erfahren Sie, wie Sie den Inhalt einer Landingpage in Journey Optimizer erstellen
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: c61b8d80-17e1-4fdd-a739-efcee032dc23
source-git-commit: 5e7db083affb7abcc33a76fa6fa7887f8fe73b06
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 100%

---

# Erstellen der Landingpage-Inhalte {#design-lp-content}

Um Inhalte für die [Primärseite](create-lp.md#configure-primary-page) oder [Unterseite](create-lp.md#configure-subpages) Ihrer Landingpage zu erstellen, bewegen Sie den Mauszeiger über die Primärseiteninhalte und klicken Sie auf **[!UICONTROL Designer öffnen]**. Sie können auch in der rechten Palette auf die entsprechende Schaltfläche klicken.

![](assets/lp_open-designer.png)

Dort haben Sie folgende Möglichkeiten:

* **Entwerfen Sie Ihre Landingpage von Grund auf** über die Benutzeroberfläche von Content Designer und nutzen Sie Bilder aus [Adobe Experience Manager Assets Essentials](../messages/assets-essentials.md). [In diesem Abschnitt](../messages/create-email-content.md) erfahren Sie, wie Sie Inhalte gestalten oder integrierte Vorlagen verwenden.

* **Codieren Sie oder fügen Sie rohen HTML-Code** direkt in Content Designer ein. Erfahren Sie [in diesem Abschnitt](../messages/existing-content.md#import-raw-html-code), wie Sie Ihren eigenen Inhalt kodieren.

* **Importieren Sie vorhandenen HTML-Inhalt** aus einer Datei oder einem .zip-Ordner. [In diesem Abschnitt](../messages/existing-content.md#import-html-content-from-file) erfahren Sie, wie Sie Inhalte importieren.

>[!NOTE]
>
>Content Designer für Landingpages ähnelt größtenteils Email Designer. Weitere Informationen finden Sie unter [Inhaltserstellung mit  [!DNL Journey Optimizer]](../messages/design-emails.md).

## Definieren von Landingpage-spezifischen Inhalten {#define-lp-specific-content}

Gehen Sie wie folgt vor, um bestimmte Inhalte zu definieren, mit denen Benutzer eine Auswahl auf Ihrer Landingpage treffen und übermitteln können.

1. Ziehen Sie die Landingpage-spezifische **[!UICONTROL Formular]**-Komponente aus der linken Palette in den Hauptarbeitsbereich.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Formular]**-Komponente kann auf einer Seite nur einmal verwendet werden.

1. Wählen Sie sie aus. Die Registerkarte **[!UICONTROL Formularinhalte]** wird in der rechten Palette angezeigt, damit Sie die verschiedenen Formularfelder bearbeiten können.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Sie können jederzeit zur Registerkarte **[!UICONTROL Formularstil]** wechseln, um die Stile Ihrer Inhalte in der Formularkomponente zu bearbeiten. [Weitere Informationen](#define-lp-styles)

1. Im Abschnitt **[!UICONTROL Kontrollkästchen 1]** können Sie den Titel bearbeiten, der diesem Kontrollkästchen entspricht.

1. Definieren Sie, ob dieses Kontrollkästchen Benutzern die An- oder Abmeldung ermöglichen soll: Erklären sie sich damit einverstanden, Nachrichten zu erhalten, oder möchten sie nicht mehr kontaktiert werden?

   ![](assets/lp_designer-form-update.png)

1. Wählen Sie aus den drei folgenden Optionen aus, was aktualisiert werden soll:

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Abonnement-Liste]**: Sie müssen die Abonnement-Liste auswählen, die aktualisiert wird, wenn das Profil dieses Kontrollkästchen aktiviert. Weitere Informationen finden Sie unter [Abonnement-Listen](subscription-list.md).

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Kanal (E-Mail)]**: Die An- oder Abmeldung gilt für den gesamten Kanal. Wenn beispielsweise ein Profil, das sich abgemeldet hat, zwei E-Mail-Adressen hat, werden beide Adressen aus Ihrer gesamten Kommunikation ausgeschlossen.

   * **[!UICONTROL E-Mail-Identität]**: Das Opt-in oder Opt-out gilt nur für die E-Mail-Adresse, die für den Zugriff auf die Landingpage verwendet wurde. Wenn beispielsweise ein Profil zwei E-Mail-Adressen hat, erhält nur diejenige E-Mail-Adresse, mit der es sich angemeldet hat, Nachrichten von Ihrer Marke.


1. Klicken Sie auf **[!UICONTROL Feld hinzufügen]** > **[!UICONTROL Kontrollkästchen]**, um ein weiteres Kontrollkästchen hinzuzufügen. Wiederholen Sie die obigen Schritte, um die Eigenschaften zu definieren.

   ![](assets/lp_designer-form-checkbox-2.png)

1. Nachdem Sie alle gewünschten Kontrollkästchen hinzugefügt haben, klicken Sie auf **[!UICONTROL Aktion]**, um den entsprechenden Abschnitt zu erweitern. Damit können Sie das Verhalten der Schaltfläche in der **[!UICONTROL Formular]**-Komponente definieren.

   ![](assets/lp_designer-form-call-to-action.png)

1. Definieren Sie, was beim Klicken auf die Schaltfläche passieren soll:

   * **[!UICONTROL Umleitungs-URL]**: Geben Sie die URL der Seite ein, zu der die Benutzer umgeleitet werden.
   * **[!UICONTROL Bestätigungstext]**: Geben Sie den Bestätigungstext ein, der angezeigt werden soll.
   * **[!UICONTROL Link zu einer Unterseite]**: Konfigurieren Sie eine [Unterseite](create-lp.md#configure-subpages) und wählen Sie sie aus der angezeigten Dropdown-Liste aus.

   ![](assets/lp_designer-form-confirmation-action.png)

1. Definieren Sie, was beim Klicken auf die Schaltfläche passieren soll, falls ein Fehler auftritt:

   * **[!UICONTROL Umleitungs-URL]**: Geben Sie die URL der Seite ein, zu der die Benutzer umgeleitet werden.
   * **[!UICONTROL Fehlertext]**: Geben Sie den Fehlertext ein, der angezeigt werden soll. Beim Definieren der [Formularstile](#define-lp-styles) können Sie sich eine Vorschau des Fehlertexts ansehen.

   * **[!UICONTROL Link zu einer Unterseite]**: Konfigurieren Sie eine [Unterseite](create-lp.md#configure-subpages) und wählen Sie sie aus der angezeigten Dropdown-Liste aus.

   ![](assets/lp_designer-form-error.png)

1. Wenn Sie beim Senden des Formulars zusätzliche Aktualisierungen vornehmen möchten, wählen Sie **[!UICONTROL Opt-in]** oder **[!UICONTROL Opt-out]** und definieren Sie, ob Sie eine Abonnement-Liste, den Kanal oder nur die verwendete E-Mail-Adresse aktualisieren möchten.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Speichern Sie die Inhalte und klicken Sie auf den Pfeil neben dem Seitennamen, um zurück zum Abschnitt [Landingpage-Eigenschaften](create-lp.md#configure-primary-page) zu gelangen.

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Definieren von Formularstilen für Landingpages {#define-lp-styles}

1. Um die Stile der Inhalte Ihrer Formularkomponente zu ändern, können Sie jederzeit zur Registerkarte **[!UICONTROL Formularstil]** wechseln.

   ![](assets/lp_designer-form-style.png)

1. Erweitern Sie den Abschnitt **[!UICONTROL Kontrollkästchen]**, um das Erscheinungsbild der Kontrollkästchen und des entsprechenden Texts zu definieren. Sie können beispielsweise die Schriftfamilie oder Schriftgröße sowie die Rahmenfarbe des Kontrollkästchens anpassen.

   ![](assets/lp_designer-form-style-checkboxes.png)

1. Erweitern Sie den Abschnitt **[!UICONTROL Schaltflächen]**, um das Erscheinungsbild der Schaltfläche im Komponentenformular zu ändern. Sie können beispielsweise einen Rahmen hinzufügen, die Beschriftungsfarbe beim Bewegen des Mauszeigers bearbeiten oder die Ausrichtung der Schaltfläche anpassen.

   ![](assets/lp_designer-form-style-buttons.png)

   Sie können einige Ihrer Einstellungen, z. B. die Farbe der Schaltflächenbeschriftung beim Bewegen des Mauszeigers, in der Vorschau anzeigen, indem Sie die Schaltfläche **[!UICONTROL Vorschau]** verwenden. Weitere Informationen zum Testen von Landingpages finden Sie [hier](create-lp.md#test-landing-page).

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. Erweitern Sie den Abschnitt **[!UICONTROL Formular-Layout]**, um die Layout-Einstellungen wie die Hintergrundfarbe, den Abstand oder den Rand zu bearbeiten.

   ![](assets/lp_designer-form-style-layout.png)

1. Erweitern Sie den Abschnitt **[!UICONTROL Formularfehler]**, um die Fehlermeldung anzupassen, die im Falle eines Problems angezeigt wird. Klicken Sie die entsprechende Option an, um den Fehlertext im Formular in der Vorschau anzuzeigen.

   ![](assets/lp_designer-form-error-preview.png)

