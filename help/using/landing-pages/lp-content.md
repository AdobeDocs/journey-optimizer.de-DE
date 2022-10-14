---
title: Definieren von Landingpage-spezifischen Inhalten
description: Erfahren Sie, wie Sie Landingpage-spezifische Inhalte in Journey Optimizer erstellen.
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: ad04aeddac78a6910258d924148fceca8fd7b6d9
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 100%

---

# Definieren von Landingpage-spezifischen Inhalten {#lp-content}

Um spezifische Inhalte zu definieren, die es den Nutzern ermöglichen, ihre Auswahl auf Ihrer Landingpage zu treffen und abzusenden, verwenden Sie die Komponente **[!UICONTROL Formular]**. Gehen Sie dazu wie folgt vor.

>[!NOTE]
>
>Sie können auch eine Clickthrough-Landingpage ohne **[!UICONTROL Formular]**-Komponente erstellen. In diesem Fall wird die Landingpage Benutzern angezeigt, sie müssen jedoch kein Formular absenden. Dies kann nützlich sein, wenn Sie nur eine Landingpage präsentieren möchten, ohne eine Aktion, wie beispielsweise ein Opt-in oder Opt-out, von Ihren Empfängern zu verlangen, oder wenn Sie Informationen bereitstellen möchten, die keine Benutzereingabe erfordern.

## Verwenden der Formularkomponente {#use-form-component}

1. Ziehen Sie die Landingpage-spezifische **[!UICONTROL Formular]**-Komponente aus der linken Palette in den Hauptarbeitsbereich.

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Formular]**-Komponente kann auf einer Seite nur einmal verwendet werden.

1. Wählen Sie sie aus. Die Registerkarte **[!UICONTROL Formularinhalt]** wird in der rechten Palette angezeigt, damit Sie die verschiedenen Felder des Formulars bearbeiten können.

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Sie können jederzeit zur Registerkarte **[!UICONTROL Formularstil]** wechseln, um die Stile Ihrer Inhalte in der Formularkomponente zu bearbeiten. [Weitere Informationen](#define-lp-styles)

1. Im Abschnitt **[!UICONTROL Kontrollkästchen 1]** können Sie den Titel bearbeiten, der diesem Kontrollkästchen entspricht.

1. Definieren Sie, ob dieses Kontrollkästchen Benutzern die An- oder Abmeldung ermöglichen soll: Erklären sie sich damit einverstanden, Nachrichten zu erhalten, oder möchten sie nicht mehr kontaktiert werden?

   ![](assets/lp_designer-form-update.png)

   Wählen Sie unter den drei folgenden Optionen eine aus:

   * **[!UICONTROL Opt-out, wenn aktiviert]**: Benutzer müssen das Kontrollkästchen markieren, um ihre Zustimmung zu erteilen (Opt-in).
   * **[!UICONTROL Opt-out, wenn markiert]**: Benutzer müssen das Kontrollkästchen markieren, um ihre Zustimmung zu entfernen (Opt-out).
   * **[!UICONTROL Opt-in, wenn aktiviert, Opt-out, wenn deaktiviert]**: Mit dieser Option können Sie ein einziges Kontrollkästchen für das Opt-in/Opt-out einfügen. Benutzer müssen das Kontrollkästchen aktivieren, um ihr Einverständnis zu erteilen (Opt-in), und es deaktivieren, um ihr Einverständnis zurückzuziehen (Opt-out).

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

1. Wenn Sie beim Senden des Formulars zusätzliche Aktualisierungen vornehmen möchten, wählen Sie **[!UICONTROL Opt-in]** oder **[!UICONTROL Opt-out]** und definieren Sie, ob Sie eine Abonnementliste, den Kanal oder nur die verwendete E-Mail-Adresse aktualisieren möchten.

   ![](assets/lp_designer-form-additionnal-update.png)

1. Speichern Sie die Inhalte und klicken Sie auf den Pfeil neben dem Seitennamen, um zurück zum Abschnitt [Landingpage-Eigenschaften](create-lp.md#configure-primary-page) zu gelangen.

   ![](assets/lp_designer-form-save.png)

## Definieren von Formularstilen für Landingpages {#lp-form-styles}

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

## Verwenden des primären Seitenkontexts {#use-primary-page-context}

Sie können kontextbezogene Daten verwenden, die von einer anderen Seite innerhalb derselben Landingpage stammen.

Wenn Sie zum Beispiel ein Kontrollkästchen<!-- or the submission of the page--> mit einer [Abonnementliste](subscription-list.md) auf der primären Landingpage verknüpfen, können Sie diese Abonnementliste auf der Unterseite „Vielen Dank“ verwenden.

Angenommen, Sie verknüpfen zwei Kontrollkästchen auf Ihrer primären Seite mit zwei verschiedenen Abonnementlisten. Wenn ein Benutzer eine dieser Listen abonniert, möchten Sie beim Absenden des Formulars eine bestimmte Nachricht anzeigen, je nachdem, welches Kästchen die Person ausgewählt hat.

Gehen Sie dazu wie folgt vor:

1. Verknüpfen Sie auf der primären Seite jedes Kontrollkästchen mit der entsprechenden Abonnementliste. [Weitere Informationen](#use-form-component).

   ![](assets/lp_designer-form-luma-newsletter.png)

1. Platzieren Sie den Mauszeiger auf der Unterseite an der Stelle, an der Sie den Text einfügen möchten, und wählen Sie in der kontextbezogenen Symbolleiste **[!UICONTROL Personalisierung hinzufügen]**.

   ![](assets/lp_designer-form-subpage-perso.png)

1. Im Fenster **[!UICONTROL Personalisierung bearbeiten]** wählen Sie **[!UICONTROL Kontextuelle Attribute]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Primärer Seitenkontext]** > **[!UICONTROL Abonnement]**.

1. Alle Abonnementlisten, die Sie auf der primären Seite ausgewählt haben, werden aufgelistet. Wählen Sie über das Symbol „+“ die entsprechenden Elemente aus.

   ![](assets/lp_designer-form-add-subscription.png)

1. Fügen Sie die entsprechenden Bedingungen über die Hilfsfunktionen des Ausdruckseditors hinzu. [Weitere Informationen](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >Wenn der Ausdruck ein Sonderzeichen wie einen Bindestrich enthält, müssen Sie den Text einschließlich des Bindestrichs mit Escape-Zeichen versehen.

1. Speichern Sie Ihre Änderungen.

![](assets/lp_designer-form-preview-checked-box.png)

Wenn Benutzende jetzt eines der Kontrollkästchen aktivieren, wird beim Absenden des Formulars die dem ausgewählten Kontrollkästchen entsprechende Meldung angezeigt.

![](assets/lp_designer-form-thankyou-preview.png)

>[!NOTE]
>
>Wenn Benutzende die beiden Kontrollkästchen aktivieren, werden beide Texte angezeigt.

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [Expression editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->