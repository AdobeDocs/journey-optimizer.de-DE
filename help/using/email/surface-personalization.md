---
solution: Journey Optimizer
product: journey optimizer
title: E-Mail-Konfigurationseinstellungen personalisieren
description: Erfahren Sie, wie Sie auf der Konfigurationsebene des E-Mail-Kanals personalisierte Werte für Ihre Einstellungen definieren
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration, Subdomain
badge: label="Eingeschränkte Verfügbarkeit"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 59%

---

# E-Mail-Konfigurationseinstellungen personalisieren {#surface-personalization}

Für mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen können Sie mit [!DNL Journey Optimizer] personalisierte Werte für Subdomains und Header<!--and URL tracking parameters--> definieren, wenn Sie E-Mail-Konfigurationen erstellen.

>[!AVAILABILITY]
>
>Die Personalisierung der E-Mail-Konfiguration ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

## Hinzufügen von dynamischen Subdomains {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalisierung nicht verfügbar"
>abstract="Diese Konfiguration wurde ohne Personalisierungsattribute erstellt. In der Dokumentation finden Sie Schritte, um dies zu beheben, falls eine Personalisierung erforderlich ist."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Aktivieren dynamischer Subdomains"
>abstract="Bei der Erstellung einer E-Mail-Konfiguration können Sie dynamische Subdomains basierend auf Bedingungen einrichten, die Sie mithilfe des Personalisierungs-Editors definieren. Sie können bis zu 50 dynamische Subdomains hinzufügen."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Einige Subdomains sind möglicherweise nicht verfügbar"
>abstract="Bestimmte Subdomains sind aufgrund einer ausstehenden Feedback-Schleifen-Registrierung derzeit nicht zur Auswahl verfügbar. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss können Sie aus allen verfügbaren Subdomains auswählen."
>additional-url="https://experienceleague.adobe.com/de/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Erste Schritte mit der Delegierung von Subdomains"

Bei der Erstellung einer E-Mail-Konfiguration können Sie dynamische Subdomains basierend auf bestimmten Bedingungen einrichten.

Wenn beispielsweise rechtliche Einschränkungen gelten, die das Senden von Nachrichten von einer speziellen E-Mail-Adresse pro Land vorgeben, können Sie dynamische Subdomains verwenden. Auf diese Weise können Sie eine einzelne Konfiguration mit mehreren Versandsubdomains erstellen, die verschiedenen Ländern entsprechen, anstatt für jedes Land mehrere Konfigurationen zu erstellen. Sie können dann Kunden und Kundinnen in verschiedenen, in einer Kampagne konsolidierten Ländern ansprechen.

Gehen Sie wie folgt vor, um in einer E-Mail-Kanalkonfiguration dynamische Subdomains zu definieren.

1. Richten Sie vor der Erstellung einer Konfiguration die Subdomains ein, die Sie zum Senden von E-Mails verwenden möchten, entsprechend Ihrem Anwendungsfall. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

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

1. Definieren Sie alle anderen [E-Mail-Einstellungen](email-settings.md) und [Senden](../configuration/channel-surfaces.md#create-channel-surface) Ihrer Konfiguration.

Nachdem Sie einer Konfiguration eine oder mehrere dynamische Subdomains hinzugefügt haben, werden die folgenden Elemente basierend auf der aufgelösten dynamischen Subdomain für diese Konfiguration aufgefüllt:

* Alle URLs (Ressourcen-URL, Mirror-Seiten-URL und Tracking-URL)

* Die [Abmelde-URL](email-settings.md#list-unsubscribe)

* Die Suffixe **Von E-Mail** und **Fehler-E-Mail** 

>[!NOTE]
>
>Wenn Sie dynamische Subdomains einrichten und dann die Option **[!UICONTROL Dynamische Subdomain]** deaktivieren, werden alle dynamischen Werte entfernt. Wählen Sie eine Subdomain aus und senden Sie die Konfiguration, damit die Änderungen wirksam werden.

## Personalisieren der Kopfzeile {#personalize-header}

Sie können auch die Personalisierung für alle in einer Konfiguration definierten Kopfzeilenparameter verwenden.

Wenn Sie beispielsweise über mehrere Marken verfügen, können Sie eine einzelne Konfiguration erstellen und personalisierte Werte für Ihre E-Mail-Header verwenden. Dadurch können Sie sicherstellen, dass alle von Ihren verschiedenen Marken gesendeten E-Mails jeweils mit den richtigen **Von**-Namen und -E-Mail-Adressen versehen werden. Wenn Ihre Empfängerinnen und Empfänger auf die Schaltfläche **Antworten** in der E-Mail-Client-Software klicken, sollten schließlich die Namen und E-Mail-Adressen für **Antwort an** der richtigen Marke für die richtige Person entsprechen.

Gehen Sie wie folgt vor, um personalisierte Variablen für Ihre Konfigurationsheader-Parameter zu verwenden.

>[!NOTE]
>
>Sie können alle Felder für die **[!UICONTROL Kopfzeilenparameter]** außer dem Feld **[!UICONTROL Fehler beim E-Mail-Präfix]** personalisieren.


1. Definieren Sie Ihre Kopfzeilenparameter wie gewohnt. [Weitere Informationen](email-settings.md#email-header)

1. Wählen Sie für jedes Feld das Symbol „Bearbeiten“ aus.

   ![](assets/surface-email-personalize-header.png)

1. Der [Personalisierungseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Definieren Sie Ihre Bedingung nach Bedarf und speichern Sie Ihre Änderungen.

   Legen Sie beispielsweise eine Bedingung fest, dass jede Empfängerin und jeder Empfänger eine E-Mail von der Person erhält, die die jeweilige Marke repräsentiert.

   >[!NOTE]
   >
   >Sie können nur **[!UICONTROL Profilattribute]** und **[!UICONTROL Hilfsfunktionen]** auswählen.

1. Wiederholen Sie die obigen Schritte für jeden Parameter, den Sie personalisieren möchten.

>[!NOTE]
>
>Wenn Sie Ihrer Konfiguration eine oder mehrere dynamische Subdomains hinzugefügt haben, werden die Suffixe &quot;**Von E-Mail**&quot;und &quot;**Fehler-E-Mail**&quot;auf der Grundlage der aufgelösten &quot;[dynamischen Subdomain](#dynamic-subdomains)&quot;gefüllt.

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Konfigurationsdetails anzeigen {#view-surface-details}

Bei der Verwendung einer Konfiguration mit personalisierten Einstellungen in einer Kampagne oder Konfiguration können Sie die Konfigurationsdetails direkt in der Kampagne oder Konfiguration anzeigen. Führen Sie dazu folgende Schritte durch.

1. Erstellen Sie eine E-Mail-[Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Wählen Sie die Schaltfläche **[!UICONTROL Inhalt bearbeiten]** aus.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Konfigurationsdetails anzeigen]** .

   ![](assets/campaign-view-surface-details.png)

1. Das Fenster **[!UICONTROL Versandeinstellungen]** wird angezeigt. Sie können alle Konfigurationseinstellungen anzeigen, einschließlich der dynamischen Subdomains und der personalisierten Kopfzeilenparameter.

   >[!NOTE]
   >
   >Alle Informationen auf diesem Bildschirm sind schreibgeschützt.

1. Wählen Sie **[!UICONTROL Erweitern]** aus, um die Details der dynamischen Subdomains anzuzeigen.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
