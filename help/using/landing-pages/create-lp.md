---
solution: Journey Optimizer
product: journey optimizer
title: Landingpage erstellen
description: Erfahren Sie, wie Sie eine Landingpage in Journey Optimizer konfigurieren und veröffentlichen
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 61c90f39fa2bddb384e5581e3935c43d4691c355
workflow-type: tm+mt
source-wordcount: '1397'
ht-degree: 0%

---

# Landingpages erstellen und veröffentlichen {#create-lp}

## Auf Landingpages zugreifen {#access-landing-pages}

Um auf die Landingpage-Liste zuzugreifen, wählen Sie **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** über das Menü links.

![](assets/lp_access-list.png)

Die **[!UICONTROL Landing Pages]** Liste zeigt alle erstellten Elemente an. Sie können sie nach ihrem Status oder Änderungsdatum filtern.

![](assets/lp_access-list-filter.png)

In dieser Liste können Sie auf die [Landingpage-Live-Bericht](../reports/lp-report-live.md) oder [Landingpage Globaler Bericht](../reports/lp-report-global.md) für veröffentlichte Elemente.

Sie können eine Landingpage auch löschen, duplizieren und ihre Veröffentlichung rückgängig machen.

>[!CAUTION]
>
>Wenn Sie die Veröffentlichung einer Landingpage rückgängig machen, auf die in einer Nachricht verwiesen wird, wird der Link zur Landingpage beschädigt und eine Fehlerseite angezeigt.

Klicken Sie auf die drei Punkte neben einer Landingpage, um die gewünschte Aktion auszuwählen.

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>Eine [veröffentlicht](#publish-landing-page) Landingpage. Um sie zu löschen, müssen Sie zunächst die Veröffentlichung rückgängig machen.

## Landingpage erstellen {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="Landingpage definieren und konfigurieren"
>abstract="Um eine Landingpage zu erstellen, müssen Sie eine Vorgabe auswählen, dann die primäre Seite und die untergeordneten Seiten konfigurieren und Ihre Seite schließlich testen, bevor Sie sie veröffentlichen."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="Landingpage-Vorgaben erstellen"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html#publish-landing-page" text="Landingpage veröffentlichen"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="Zuweisen von Bezeichnungen zu Ihrer Landingpage"
>abstract="Zum Schutz sensibler digitaler Assets können Sie Berechtigungen definieren, mit denen Sie den Datenzugriff auf Ihre Landingpage mithilfe von Beschriftungen verwalten können."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html" text="Landingpage-Vorgaben erstellen"

Gehen Sie zur Erstellung einer Landingpage wie folgt vor:

1. Klicken Sie in der Landingpage-Liste auf **[!UICONTROL Create landing page]**.

   ![](assets/lp_create-lp.png)

1. Fügen Sie einen Titel hinzu. Sie können bei Bedarf eine Beschreibung hinzufügen.

   ![](assets/lp_create-lp-details.png)

1. Um der Landingpage benutzerdefinierte oder Core-Datennutzungsbezeichnungen zuzuweisen, wählen Sie **[!UICONTROL Manage access]**. [Weitere Informationen zur Zugriffskontrolle auf Objektebene (OLAC)](../administration/object-based-access.md)

   <!--You can add a tag. See AEP documentation?-->

1. Wählen Sie eine Vorgabe aus. Erfahren Sie, wie Sie Landingpage-Vorgaben erstellen in [diesem Abschnitt](../landing-pages/lp-presets.md#lp-create-preset).

   ![](assets/lp_create-lp-presets.png)

1. Klicken **[!UICONTROL Create]**.

1. Die primäre Seite und ihre Eigenschaften werden angezeigt. Erfahren Sie, wie Sie die Einstellungen der primären Seite konfigurieren [here](#configure-primary-page).

   ![](assets/lp_primary-page.png)

1. Klicken Sie auf das Symbol + , um eine Unterseite hinzuzufügen. Erfahren Sie, wie Sie die Einstellungen der Unterseite konfigurieren. [here](#configure-subpages).

   ![](assets/lp_add-subpage.png)

Nachdem Sie die [primäre Seite](#configure-primary-page)und die [Unterseiten](#configure-subpages) Wenn vorhanden, können Sie [test](#test-landing-page) und [publish](#publish-landing-page) Ihre Landingpage.

## Primärseite konfigurieren {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="Primäre Seiteneinstellungen definieren"
>abstract="Die primäre Seite wird den Benutzern sofort angezeigt, nachdem sie auf den Link zu Ihrer Landingpage geklickt haben, z. B. über eine E-Mail oder eine Website."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="Landingpage-Inhalt gestalten"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="Landingpage-URL definieren"
>abstract="Definieren Sie in diesem Abschnitt eine eindeutige Landingpage-URL. Für den ersten Teil der URL müssen Sie zuvor eine Landingpage-Subdomäne als Teil der von Ihnen ausgewählten Vorgabe eingerichtet haben."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html" text="Landingpage-Subdomains konfigurieren"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="Landingpage-Vorgaben erstellen"

Die primäre Seite ist die Seite, die den Benutzern sofort angezeigt wird, nachdem sie auf den Link zu Ihrer Landingpage geklickt haben, z. B. über eine E-Mail oder eine Website.

Gehen Sie wie folgt vor, um die Einstellungen der primären Seite zu definieren.

1. Sie können den Seitennamen ändern, also **[!UICONTROL Primary page]** Standardmäßig.

1. Bearbeiten Sie den Inhalt Ihrer Seite mit dem Content Designer. Erfahren Sie, wie Sie den Inhalt von Landingpages definieren [here](design-lp.md).

   ![](assets/lp_open-designer.png)

1. Definieren Sie Ihre Landingpage-URL. Für den ersten Teil der URL müssen Sie zuvor eine Landingpage-Subdomain als Teil der [preset](../landing-pages/lp-presets.md#lp-create-preset) ausgewählt haben. [Weitere Infos](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >Die Landingpage-URL muss eindeutig sein.

   ![](assets/lp_access-url.png)

   >[!NOTE]
   >
   >Sie können nicht auf Ihre Landingpage zugreifen, indem Sie diese URL einfach in einen Webbrowser kopieren, selbst wenn sie veröffentlicht wurde. Stattdessen können Sie sie mit der Vorschaufunktion testen, wie hier beschrieben: [diesem Abschnitt](#test-landing-page).

1. Wenn die Landingpage die bereits verfügbaren Formulardaten vorab ausfüllen soll, wählen Sie die **[!UICONTROL Pre-fill form fields with profile information]**.

   ![](assets/lp_prefill-form-fields.png)

   Wenn diese Option aktiviert ist und ein Profil sich bereits für eine An-/Abmeldung entschieden hat oder bereits einer Abonnementliste hinzugefügt wurde, werden seine Optionen bei der Anzeige der Landingpage angezeigt.

   Wenn sich beispielsweise ein Profil für den Empfang von Nachrichten zu künftigen Ereignissen entschieden hat, wird das entsprechende Kontrollkästchen bereits aktiviert, wenn diesem Profil die Landingpage das nächste Mal angezeigt wird.

   ![](assets/lp_prefill-form-ex.png)

1. Sie können ein Ablaufdatum für Ihre Seite festlegen. In diesem Fall müssen Sie eine Aktion nach Ablauf der Seite auswählen:

   * **[!UICONTROL Redirect URL]**: Geben Sie die URL der Seite ein, zu der Benutzer weitergeleitet werden, wenn die Seite abläuft.
   * **[!UICONTROL Custom page]**: [Konfigurieren einer Unterseite](#configure-subpages) und wählen Sie sie aus der angezeigten Dropdownliste aus.
   * **[!UICONTROL Browser error]**: Geben Sie den Fehlertext ein, der anstelle der Seite angezeigt wird.

   ![](assets/lp_expiry-date.png)

1. Im **[!UICONTROL Additional data]** definieren Sie einen oder mehrere Schlüssel und die zugehörigen Parameterwerte. Sie können diese Schlüssel im Inhalt Ihrer primären Seite und Unterseiten mit dem [Ausdruckseditor](../personalization/personalization-build-expressions.md). Weitere Informationen finden Sie unter [diesem Abschnitt](lp-content.md#use-form-component#use-additional-data).

   ![](assets/lp_create-lp-additional-data.png)

1. Wenn Sie bei der [Erstellen der primären Seite](design-lp.md), werden sie im **[!UICONTROL Subscription list]** Abschnitt.

   ![](assets/lp_subscription-list.png)

1. Über die Landingpage können Sie [Erstellen einer Journey](../building-journeys/journey-gs.md#jo-build) , der Benutzern beim Senden des Formulars eine Bestätigungsnachricht sendet. Erfahren Sie, wie Sie am Ende dieser [Anwendungsfall](lp-use-cases.md#subscription-to-a-service).

   ![](assets/lp_create-journey.png)

   Klicken **[!UICONTROL Create journey]** , die an die **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** Liste.

## Unterseiten konfigurieren {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="Unterseiteneinstellungen definieren"
>abstract="Sie können bis zu 2 Unterseiten hinzufügen. Sie können beispielsweise eine Dankeseite erstellen, die angezeigt wird, sobald Benutzer das Formular übermitteln, und Sie können eine Fehlerseite definieren, die aufgerufen wird, wenn ein Problem mit der Landingpage auftritt."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="Landingpage-Inhalt gestalten"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="Landingpage-URL definieren"
>abstract="Definieren Sie in diesem Abschnitt eine eindeutige Landingpage-URL. Für den ersten Teil der URL müssen Sie zuvor eine Landingpage-Subdomäne als Teil der von Ihnen ausgewählten Vorgabe eingerichtet haben."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html" text="Landingpage-Subdomains konfigurieren"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="Landingpage-Vorgaben erstellen"

Sie können bis zu 2 Unterseiten hinzufügen. Sie können beispielsweise eine Dankeseite erstellen, die angezeigt wird, sobald Benutzer das Formular übermitteln, und Sie können eine Fehlerseite definieren, die aufgerufen wird, wenn ein Problem mit der Landingpage auftritt.

Gehen Sie wie folgt vor, um die Einstellungen der Unterseite zu definieren.

1. Sie können den Seitennamen ändern, also **[!UICONTROL Subpage 1]** Standardmäßig.

1. Bearbeiten Sie den Inhalt Ihrer Seite mit dem Content Designer. Erfahren Sie, wie Sie den Inhalt von Landingpages definieren [here](design-lp.md).

   >[!NOTE]
   >
   >Sie können von jeder Unterseite derselben Landingpage aus einen Link zur primären Seite einfügen. Um beispielsweise Benutzer umzuleiten, die einen Fehler begangen haben und sich erneut anmelden möchten, können Sie einen Link von der Bestätigungs-Unterseite zur primären Anmeldeseite hinzufügen. Erfahren Sie, wie Sie Links in einfügen [diesem Abschnitt](../email/message-tracking.md#insert-links).

1. Definieren Sie Ihre Landingpage-URL. Für den ersten Teil der URL müssen Sie zuvor eine Subdomain für die Landingpage eingerichtet haben. [Weitere Infos](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >Die Landingpage-URL muss eindeutig sein.

![](assets/lp_subpage-settings.png)

## Landingpage testen {#test-landing-page}

Nachdem Sie die Einstellungen und den Inhalt Ihrer Landingpage definiert haben, können Sie sie mit Testprofilen in der Vorschau anzeigen. Wenn Sie [personalisierter Inhalt](../personalization/personalize.md)können Sie mithilfe von Testprofildaten überprüfen, wie dieser Inhalt auf der Landingpage dargestellt wird.

>[!CAUTION]
>
>Sie müssen über Testprofile verfügen, damit Sie eine Vorschau Ihrer Nachrichten anzeigen und Testsendungen durchführen können. Erfahren Sie, wie Sie [Testprofile erstellen](../segment/creating-test-profiles.md).

1. Klicken Sie in der Landingpage auf die Schaltfläche **[!UICONTROL Preview & test]** -Schaltfläche, um auf die Auswahl des Testprofils zuzugreifen.

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Preview]** -Schaltfläche kann auch über den Inhaltsdesigner aufgerufen werden.

1. Aus dem **[!UICONTROL Preview & test]** ein oder mehrere Testprofile aus.

   ![](assets/lp_test-profiles.png)

   Die Schritte zum Auswählen von Testprofilen sind mit denen beim Testen einer Nachricht identisch. Sie werden im Abschnitt [diesem Abschnitt](../email/preview.md#select-test-profiles).

1. Wählen Sie die **[!UICONTROL Preview]** Registerkarte und klicken Sie auf **[!UICONTROL Open preview]** , um Ihre Landingpage zu testen.

   ![](assets/lp_open-preview.png)

1. Die Vorschau Ihrer Landingpage wird in einem neuen Tab geöffnet. Personalisierte Elemente werden durch die ausgewählten Testprofildaten ersetzt.

   ![](assets/lp_preview.png)

1. Wählen Sie weitere Testprofile aus, um das Rendering für jede Variante Ihrer Landingpage in der Vorschau anzuzeigen.

## Warnungen überprüfen {#check-alerts}

Warnungen werden beim Erstellen Ihrer Landingpage angezeigt, wenn Sie wichtige Maßnahmen vor der Veröffentlichung treffen müssen.

Warnhinweise werden oben rechts im Bildschirm angezeigt, wie unten dargestellt:

![](assets/lp_alerts.png)

>[!NOTE]
>
>Wenn diese Schaltfläche nicht angezeigt wird, wurde kein Warnhinweis erkannt.

Es können zwei Arten von Warnhinweisen auftreten:

* **Warnungen** Siehe Empfehlungen und Best Practices. <!--For example, a message will display if -->

* **Fehler** verhindert, dass Sie die Landingpage veröffentlichen, solange sie nicht aufgelöst wurde. Beispielsweise erhalten Sie eine Warnung, wenn die URL der primären Seite fehlt.

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> Sie müssen alle **error** Warnhinweise vor der Veröffentlichung.

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you must resolve all **error** alerts.
-->

## Landingpage veröffentlichen {#publish-landing-page}

Sobald Ihre Landingpage fertig ist, können Sie sie veröffentlichen, um sie für die Verwendung in einer Nachricht verfügbar zu machen.

![](assets/lp_publish.png)

>[!CAUTION]
>
>Prüfen und lösen Sie Warnhinweise vor der Veröffentlichung. [Weitere Infos](#check-alerts)

Sobald Ihre Landingpage publiziert wurde, wird sie mit der **[!UICONTROL Published]** Status.

Sie ist jetzt live und kann in einer [!DNL Journey Optimizer] -Nachricht, die über eine [Journey](../building-journeys/journey.md).

>[!NOTE]
>
>Sie können die Auswirkungen Ihrer Landingpage mithilfe spezifischer Berichte überwachen. [Weitere Infos](../reports/lp-report-live.md)

