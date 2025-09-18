---
solution: Journey Optimizer
product: journey optimizer
title: Erstellen und Verwenden von Formularen für Landingpages
description: Erfahren Sie, wie Sie Formulare für Ihre Landingpages in Journey Optimizer erstellen und verwenden
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: Landing, Landingpage, Erstellung, Seite, Formular
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 67283fe92282ce23c97c29fa2c0ad78132cc184a
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 4%

---

# Verwenden von Formularen in Ihren Landingpages {#lp-forms}

>[!AVAILABILITY]
>
>Diese Funktion ist nur eingeschränkt verfügbar. Wenden Sie sich an den Adobe-Support, um Zugang zu erhalten.

Um Profildaten mit Ihren [!DNL Journey Optimizer] Landingpages zu erfassen und Ihre [!DNL Experience Platform] Datensätze anzureichern, können Sie Formulare in Ihren Landingpages nutzen.

## Erstellen einer Formularvorgabe {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="Auswahl des zu verwendenden Endpunkts"
>abstract="Definieren Sie den Streaming-Endpunkt, an den Daten beim Senden des Formulars gesendet werden."
>additional-url="https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Erstellen einer HTTP-API-Streaming-Verbindung"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="Auswählen eines Datensatzes"
>abstract="Definieren Sie einen Datensatz, in dem die Formularantworten gespeichert und reflektiert werden. Sie können eingeben, um einen bestimmten Datensatz zu durchsuchen, oder ihn aus der Liste auswählen."

Bevor Sie ein Formular erstellen können, müssen Sie eine dedizierte Vorgabe erstellen, in der Sie den Verbindungsendpunkt auswählen, an den Formulardaten gesendet werden, und den Datensatz, in dem die im Formular erfassten Daten gespeichert werden.

Wenn Daten auf dem Streaming-Endpunkt landen, werden sie mit den Datensatzinformationen verknüpft. Mithilfe der generierten Quell-/Zielverbindungen und des Quellflusses werden die Daten dann in den Datensatz übertragen.

Beim Erstellen einer Voreinstellung:

* Sie können mehrere Vorgaben mit verschiedenen Kombinationen aus Datensätzen und Streaming-Verbindungen einrichten.
* Derselbe Datensatz oder dieselbe Streaming-Verbindung kann über mehrere Voreinstellungen hinweg wiederverwendet werden.
* Jede Streaming-Verbindung generiert automatisch Ressourcen wie:
   * **Source-Verbindung** - woher die Daten stammen.
   * **Zielverbindung** - wo die Daten gespeichert oder genutzt werden.
   * **Source-**: Die Pipeline, die Daten von der Quellverbindung in [!DNL Experience Platform] verschiebt, um Zuordnungen, Umwandlungen und Validierungen zu verarbeiten.

>[!NOTE]
>
> Um auf Formularvorgaben zuzugreifen und sie zu bearbeiten, benötigen Sie die Berechtigung **[!UICONTROL Formularvorgaben verwalten]** für die Produktions-Sandbox. Weitere Informationen zu Berechtigungen finden Sie [ (diesem Abschnitt](../administration/high-low-permissions.md#administration-permissions).<!--TBC-->

1. Um auf das Inventar **[!UICONTROL Formularvorgaben]** zuzugreifen, wählen Sie **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** >**[!UICONTROL Formulareinstellungen]** aus dem linken Menü aus.

1. Klicken Sie **[!UICONTROL Formularvorgabe erstellen]**.

1. Aktualisieren Sie den Namen, um ihn leichter abzurufen, und fügen Sie bei Bedarf eine Beschreibung hinzu.

   ![](assets/lp_create-form-preset.png){width=80%}

1. Wählen Sie die **[!UICONTROL Streaming-Verbindung]** aus, die für dieses Formular verwendet werden soll. Dies ist der Streaming-Endpunkt, an den Daten beim Senden des Formulars gesendet werden.

   >[!NOTE]
   >
   >Weitere Informationen zum Erstellen einer Streaming-Quellverbindung finden Sie in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}.

1. Wählen Sie einen **[!UICONTROL Datensatz]** aus, um ihn mit dem Formular zu verknüpfen. Hier werden die Formularantworten gespeichert und dargestellt. Sie können eingeben, um einen bestimmten Datensatz zu durchsuchen, oder ihn aus der Liste auswählen.

   >[!NOTE]
   >
   >Derzeit stehen nur [!DNL Adobe Experience Platform] Datensätze zur Auswahl. Es kann jeweils nur ein Datensatz ausgewählt werden.

1. Klicken Sie auf **[!UICONTROL Veröffentlichen]**. Ihre Voreinstellung kann jetzt in einem Formular verwendet werden.

## Zugriff und Verwaltung von Formularen {#access-forms}

Um auf die Formularliste zuzugreifen, wählen Sie **[!UICONTROL Content]** Management > **[!UICONTROL Forms]** aus dem linken Menü aus.

Alle vorhandenen Formulare werden angezeigt. Sie können Formulare nach Status, Erstellungs- oder Änderungsdatum filtern.

## Erstellen und Entwerfen eines Formulars {#create-form}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_preset"
>title="Voreinstellung auswählen"
>abstract="Wählen Sie eine vordefinierte Vorgabe aus, die die zu verwendende Verbindung und einen vordefinierten Datensatz für Ihr Formular enthält."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/content-management/landing-pages/lp-forms#create-form-preset" text="Erstellen einer Formularvorgabe"

Gehen Sie wie folgt vor, um ein Formular zu erstellen.

1. Klicken Sie in der Liste **&#x200B;**&#x200B;Forms **[!UICONTROL auf „Formular erstellen]**.

1. Einen Namen hinzufügen. Sie können bei Bedarf eine Beschreibung hinzufügen.

   ![](assets/lp_create-form.png)

1. Wählen Sie eine **[!UICONTROL Vorgabe]** aus, die die zu verwendende Verbindung und einen vordefinierten Datensatz für Ihr Formular enthält. [Erfahren Sie, wie Sie eine Formularvorgabe erstellen](#create-form-preset)

1. Klicken Sie auf **[!UICONTROL Erstellen]**.

   <!--![](assets/lp_create-form-filled.png){width=50%}-->

1. Der Formular-Designer wird geöffnet. Fügen Sie [Komponenten](../email/content-components.md#add-content-components) hinzu, um Ihren Formularinhalt zu erstellen. Sie können Komponenten [Text](../email/content-components.md#text) und Komponenten **[!UICONTROL Feld]** verwenden.

1. Mit der **[!UICONTROL Feld]**-Komponente können Sie Attribute basierend auf dem ausgewählten Datensatzschema auswählen.

   >[!NOTE]
   >
   >Um die erfassten Daten einem Profil zuzuordnen, wählen Sie ein Profilidentitätsfeld aus. Um die Identitätsfelder in der Attributliste zu identifizieren, suchen Sie nach den Feldern, die als &quot;**[!UICONTROL &quot;]** sind<!--Explain-->

   Sie können beispielsweise die E-Mail-Adresse und die Personen-ID festlegen. Wenn Benutzer diese Felder ausfüllen, werden die eingegebenen Informationen im ausgewählten Datensatz gespeichert.

   ![](assets/lp_create-form-fields.png)

1. Sie können jedes **[!UICONTROL Felddetails“]** Anweisungen, einen Standardwert, eine Validierungsmeldung, maximale Länge usw. angeben.

   ![](assets/lp_create-form-field-details.png)

1. Sie können das Layout, die Formatierung und die Abmessungen des Formulars nach Bedarf mithilfe des Bereichs **[!UICONTROL Stile]** anpassen. [Erfahren Sie mehr über das Styling](../email/get-started-email-style.md)

1. Klicken Sie **[!UICONTROL Speichern und schließen]**.

1. Konfigurieren Sie die Dankesseite. [Weitere Informationen](#thank-you-page)

1. **[!UICONTROL Veröffentlichen]** des Formulars, um es für die Auswahl auf Landingpages verfügbar zu machen.

### Konfigurieren der Dankesseite {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="Dankeseite"
>abstract="Konfigurieren Sie, was passiert, wenn jemand das Formular ausfüllt oder weiterleitet."

Konfigurieren Sie **[!UICONTROL Abschnitt „Dankeseite]**, was passiert, wenn ein Benutzer das Formular ausfüllt.

![](assets/lp_create-form-thank-you.png){width=70%}

Richten Sie eine der folgenden Aktionen ein:

* **[!UICONTROL Auf Seite bleiben]** - Mit dieser Option bleibt der Besucher auf derselben Seite, wenn das Formular gesendet wurde.
* **[!UICONTROL Landingpage]** - Wählen Sie eine veröffentlichte [Landingpage](create-lp.md) aus, zu der der Benutzer nach dem Absenden des Formulars weitergeleitet wird.
* **[!UICONTROL Externe URL]** - Geben Sie die vollständige URL ein, die als Folgeseite verwendet werden soll. Nachdem der Benutzer das Formular gesendet hat, wird er an die angegebene URL weitergeleitet.
* **[!UICONTROL Bedingte Umleitung]** - Richten Sie Regeln ein, um verschiedene Folgeaktionen basierend auf den Formularantworten dynamisch anzuzeigen.

  Sie können für jede spezifische Zielgruppe eine Regel definieren. Sie können beispielsweise eine bestimmte Landingpage für US-Bürger, eine andere Seite für Personen mit Wohnsitz in Kanada usw. anzeigen. Richten Sie abschließend eine Standardaktion für Benutzer ein, die nicht unter eine von Ihnen definierte Regel fallen.

  >[!NOTE]
  >
  >Die in einer Regel definierten Bedingungen werden sequenziell gelesen.

  ![](assets/lp_create-form-thank-you-conditional.png){width=40%}

## Verwenden des Formulars in einer Landingpage {#leverage-form-in-lp}

Sie können dieses Formular jetzt in eine Landingpage einbetten, um Daten zu erfassen, die den im Formular definierten Attributen entsprechen, und sie im ausgewählten Datensatz zu speichern. Gehen Sie wie folgt vor.

1. Erstellen Sie eine Landingpage. [Weitere Informationen](create-lp.md#create-landing-page)

1. Wählen Sie **[!UICONTROL Landingpage-Typ]** Datenerfassung“ aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   ![](assets/lp_create-lp-data-capture.png){width=65%}

1. Konfigurieren Sie die Primärseite. [Weitere Informationen](create-lp.md#configure-primary-page)

1. Öffnen Sie den [Landingpage-Designer](design-lp.md).

1. Ziehen Sie per Drag-and **[!UICONTROL Drop eine]** Strukturkomponente“ in Ihren Inhalt. Ziehen Sie eine **[!UICONTROL Formular]**-Komponente in diese Struktur.

   >[!NOTE]
   >
   >Auf einer Landingpage können nur veröffentlichte Formulare ausgewählt werden.

1. Wählen Sie im **[!UICONTROL Einbettungsformular]** das erstellte Formular aus.

   ![](assets/lp_embed-form.png)

   >[!NOTE]
   >
   >Sie können das ausgewählte Formular mithilfe der Schaltfläche **[!UICONTROL Formular bearbeiten]** aktualisieren. Das Formular wird auf einer neuen Registerkarte geöffnet. Die Schritte zum Bearbeiten des Formularinhalts sind dieselben wie in [diesem Abschnitt](#create-form) beschrieben.

1. Konfigurieren Sie **[!UICONTROL Abschnitt]** Folgenachrichtentyp), was passiert, wenn ein Benutzer das Formular ausfüllt:

   * Wählen Sie **[!UICONTROL Formular definiert]** aus, um die Aktion auszuwählen, die im eingebetteten Formular definiert wurde. [Weitere Informationen](#thank-you-page)

   * Sie können auch eine veröffentlichte [Landingpage) auswählen](create-lp.md) zu der der Benutzer nach dem Absenden des Formulars weitergeleitet wird.

   * Oder definieren Sie eine **[!UICONTROL externe URL]** als Folgeseite, auf die Benutzer beim Senden des Formulars weitergeleitet werden.

1. Speichern und testen Sie Ihre Landingpage. [Weitere Informationen](create-lp.md#test-landing-page)

Sobald Ihre Landingpage [veröffentlicht) ](create-lp.md#publish-landing-page) auf einer Journey verwendet wurde und Benutzer das Formular ausfüllen, werden die eingegebenen Informationen in den ausgewählten Datensatz aufgenommen.

>[!NOTE]
>
>Wenn Sie die Veröffentlichung eines Formulars aufheben, das in einer Landingpage verwendet wird, bearbeiten Sie dieses Formular und veröffentlichen Sie es erneut. Für die Landingpage wird immer die neueste veröffentlichte Version des Formulars verwendet.
