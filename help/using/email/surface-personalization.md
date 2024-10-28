---
solution: Journey Optimizer
product: journey optimizer
title: Personalisieren der Einstellungen der E-Mail-Konfiguration
description: Erfahren Sie, wie Sie personalisierte Werte für Ihre Einstellungen auf der Ebene der E-Mail-Kanalkonfiguration definieren.
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration, Subdomain
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 9b4ff0325d099252a5785aa13cfe0f1fe42acac6
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 68%

---

# Personalisieren der Einstellungen der E-Mail-Konfiguration {#surface-personalization}

Für mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen ermöglicht [!DNL Journey Optimizer] die Definition personalisierter Werte für Subdomains und Kopfzeilen<!--and URL tracking parameters--> beim Erstellen von E-Mail-Konfigurationen.

## Hinzufügen von dynamischen Subdomains {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalisierung nicht verfügbar"
>abstract="Diese Konfiguration wurde ohne Personalisierungsattribute erstellt. In der Dokumentation finden Sie Schritte, um dies zu beheben, falls eine Personalisierung erforderlich ist."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Aktivieren dynamischer Subdomains"
>abstract="Beim Erstellen einer E-Mail-Konfiguration können Sie dynamische Subdomains basierend auf Bedingungen einrichten, die Sie mit dem Personalisierungseditor definieren. Sie können bis zu 50 dynamische Subdomains hinzufügen."

Bei der Erstellung einer E-Mail-Konfiguration können Sie dynamische Subdomains basierend auf bestimmten Bedingungen einrichten.

Wenn beispielsweise rechtliche Einschränkungen gelten, die das Senden von Nachrichten von einer speziellen E-Mail-Adresse pro Land vorgeben, können Sie dynamische Subdomains verwenden. Auf diese Weise können Sie eine einzige Konfiguration mit mehreren Subdomains zum Senden erstellen, die verschiedenen Ländern entsprechen, anstatt für jedes Land mehrere Konfigurationen zu erstellen. Sie können dann Kunden und Kundinnen in verschiedenen, in einer Kampagne konsolidierten Ländern ansprechen.

Gehen Sie wie folgt vor, um dynamische Subdomains in einer E-Mail-Kanalkonfiguration zu definieren.

1. Richten Sie vor dem Erstellen einer Konfiguration nach Bedarf die Subdomains ein, die Sie für den E-Mail-Versand verwenden möchten. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

   Angenommen, Sie möchten verschiedene Subdomains für verschiedene Länder verwenden, indem Sie etwa eine Subdomain für die USA einrichten, eine für Großbritannien usw.

1. Erstellen Sie eine Kanalkonfiguration. [Weitere Informationen](../configuration/channel-surfaces.md)

1. Wählen Sie den Kanal **[!UICONTROL E-Mail]** aus.

1. Aktivieren Sie im Abschnitt **Subdomain** die Option **[!UICONTROL Dynamische Subdomain]**.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Klicken Sie auf das Bearbeitungssymbol neben dem ersten Feld **[!UICONTROL Bedingung]**.

1. Der [Personalisierungseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Legen Sie in diesem Beispiel eine Bedingung wie „`Country` ist gleich `US`“ fest.

   ![](assets/surface-email-edit-condition.png)

1. Wählen Sie die Subdomain aus, die Sie mit dieser Bedingung verknüpfen möchten. [Weitere Informationen zu Subdomains](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Bestimmte Subdomains sind aufgrund einer ausstehenden [Feedback-Schleifen](../reports/deliverability.md#feedback-loops)-Registrierung derzeit nicht zur Auswahl verfügbar. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss können Sie aus allen verfügbaren Subdomains auswählen. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Alle Empfängerinnen und Empfänger in den USA erhalten Nachrichten, die die ausgewählte Subdomain für dieses Land verwenden. Das bedeutet, dass alle beteiligten URLs (z. B. Mirror-Seite, Tracking-URL oder Abmelde-Link) auf der Basis dieser Subdomain gefüllt werden.

1. Legen Sie andere dynamische Subdomains nach Bedarf fest. Sie können bis zu 50 Elemente hinzufügen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the configuration. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Definieren Sie alle anderen [E-Mail-Einstellungen](email-settings.md) und [übermitteln](../configuration/channel-surfaces.md#create-channel-surface) Sie Ihre Konfiguration.

Nachdem Sie eine oder mehrere dynamische Subdomains zu einer Konfiguration hinzugefügt haben, werden die folgenden Elemente basierend auf der aufgelösten dynamischen Subdomain für diese Konfiguration aufgefüllt:

* Alle URLs (Ressourcen-URL, Mirror-Seiten-URL und Tracking-URL)

* Die [Abmelde-URL](email-settings.md#list-unsubscribe)

* Die Suffixe **Von E-Mail** und **Fehler-E-Mail** 

>[!NOTE]
>
>Wenn Sie dynamische Subdomains einrichten und dann die Option **[!UICONTROL Dynamische Subdomain]** deaktivieren, werden alle dynamischen Werte entfernt. Wählen Sie eine Subdomain aus und übermitteln Sie die Konfiguration, damit die Änderungen wirksam werden.

## Personalisieren der Kopfzeile {#personalize-header}

Sie können die Personalisierung auch für alle Kopfzeilenparameter verwenden, die in einer Konfiguration definiert sind.

Wenn Sie beispielsweise über mehrere Marken verfügen, können Sie eine einzelne Konfiguration erstellen und für Ihre E-Mail-Kopfzeilen personalisierte Werte verwenden. Dadurch können Sie sicherstellen, dass alle von Ihren verschiedenen Marken gesendeten E-Mails jeweils mit den richtigen **Von**-Namen und -E-Mail-Adressen versehen werden. Wenn Ihre Empfängerinnen und Empfänger auf die Schaltfläche **Antworten** in der E-Mail-Client-Software klicken, sollten schließlich die Namen und E-Mail-Adressen für **Antwort an** der richtigen Marke für die richtige Person entsprechen.

Gehen Sie wie folgt vor, um personalisierte Variablen für die Kopfzeilenparameter der Konfiguration zu verwenden.

>[!NOTE]
>
>Sie können alle Felder für die **[!UICONTROL Kopfzeilenparameter]** außer dem Feld **[!UICONTROL Fehler beim E-Mail-Präfix]** personalisieren.


1. Definieren Sie Ihre Kopfzeilenparameter wie gewohnt. [Weitere Informationen](email-settings.md#email-header)

1. Wählen Sie für jedes Feld das Symbol „Bearbeiten“ aus.

   ![](assets/surface-email-personalize-header.png)

1. Der [Personalisierungseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Definieren Sie die gewünschte Bedingung und speichern Sie die Änderungen.

   <!--For example, set a condition such as each recipient receives an email from their own brand representative.-->

   >[!NOTE]
   >
   >Sie können nur **[!UICONTROL Profilattribute]** und **[!UICONTROL Hilfsfunktionen]** auswählen.

   Nehmen wir an, Sie möchten dynamische E-Mails verarbeiten, die im Auftrag eines Vertriebsmitarbeiters gesendet werden, wobei der Vertriebsmitarbeiter aus kontextbezogenen Ereignissen oder Kampagnen abgerufen wird. Zum Beispiel:

   * Wenn in einer [Journey](../building-journeys/journey-gs.md) ein Kaufereignis mit dem Vertriebsassistenten eines bestimmten Geschäfts verknüpft ist, kann der E-Mail-Header (Absendername, Absender-E-Mail, Antwort-Adresse) mit den Parametern des Vertriebsassistenten personalisiert werden, die aus den Ereignisattributen übernommen werden.

   * In einer [API-gesteuerten Kampagne](../campaigns/api-triggered-campaigns.md), die extern von einem Vertriebsmitarbeiter initiiert wird, kann die ausgelöste E-Mail im Namen des Vertriebsassistenten gesendet werden und die Kopfzeilenpersonalisierungswerte können aus den kontextbezogenen Kampagnenparametern entnommen werden.

1. Wiederholen Sie die obigen Schritte für jeden Parameter, den Sie personalisieren möchten.

>[!NOTE]
>
>Wenn Sie Ihrer Konfiguration eine oder mehrere dynamische Subdomains hinzugefügt haben, werden die Suffixe **Von-E-Mail** und **Fehler-E-Mail** basierend auf der aufgelösten [dynamischen Subdomain](#dynamic-subdomains) gefüllt.

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Anzeigen der Konfigurationsdetails {#view-surface-details}

Bei Verwendung einer Konfiguration mit personalisierten Einstellungen in einer Kampagne oder einer Journey können Sie die Konfigurationsdetails direkt innerhalb der Kampagne oder der Journey anzeigen. Führen Sie dazu folgende Schritte durch.

1. Erstellen Sie eine E-Mail-[Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Wählen Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** aus.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Konfigurationsdetails anzeigen]**.

   ![](assets/campaign-view-surface-details.png)

1. Das Fenster **[!UICONTROL Versandeinstellungen]** wird angezeigt. Sie können alle Konfigurationseinstellungen anzeigen, einschließlich der dynamischen Subdomains und der personalisierten Kopfzeilenparameter.

   >[!NOTE]
   >
   >Alle Informationen auf diesem Bildschirm sind schreibgeschützt.

1. Wählen Sie **[!UICONTROL Erweitern]** aus, um die Details der dynamischen Subdomains anzuzeigen.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)

## Überprüfen der Konfiguration {#check-configuration}

Bei Verwendung einer personalisierten Konfiguration in einer Kampagne oder einer Journey können Sie eine Vorschau Ihres E-Mail-Inhalts anzeigen, um nach potenziellen Fehlern mit den von Ihnen definierten dynamischen Einstellungen zu suchen. Führen Sie dazu folgende Schritte durch.

1. Klicken Sie im Bildschirm &quot;Inhalt bearbeiten&quot;Ihrer Nachricht oder in E-Mail-Designer auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** . [Weitere Informationen](../content-management/preview.md)

1. Wählen Sie ein [Testprofil](../content-management/test-profiles.md) aus.

1. Wenn ein Fehler angezeigt wird, klicken Sie auf die Schaltfläche **[!UICONTROL Konfigurationsdetails anzeigen]** .

   ![](assets/campaign-simulate-config-error.png)

1. Überprüfen Sie den Bildschirm **[!UICONTROL Versandeinstellungen]** auf die Fehlerdetails.

   ![](assets/campaign-simulate-config-details.png)

Mögliche Fehler sind:

* Die **Subdomain** wurde für das ausgewählte Testprofil nicht aufgelöst. Ihre Konfiguration verwendet beispielsweise mehrere Subdomains, die unterschiedlichen Ländern entsprechen, aber für das ausgewählte Profil ist kein Wert für das Attribut `Country` definiert oder das Attribut ist auf `France` festgelegt, dieser Wert ist jedoch keiner Subdomain in dieser Konfiguration zugeordnet.

* Dem ausgewählten Profil sind keine Werte für einen oder mehrere **Kopfzeilenparameter** zugeordnet.

Bei keinem dieser Fehler wird E-Mail an das ausgewählte Testprofil gesendet.

Um diesen Fehlertyp zu vermeiden, stellen Sie sicher, dass die von Ihnen definierten Header-Parameter personalisierte Attribute mit Werten für die meisten Ihrer Profile verwenden. Fehlende Werte können sich auf Ihre E-Mail-Zustellbarkeit auswirken.

>[!NOTE]
>
>Weiterführende Informationen zur Zustellbarkeit finden Sie in [diesem Abschnitt](../reports/deliverability.md) .
