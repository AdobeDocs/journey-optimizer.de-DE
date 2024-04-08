---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische E-Mail-Subdomains konfigurieren
description: Erfahren Sie, wie Sie dynamische Subdomains auf der Ebene des E-Mail-Kanals konfigurieren.
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration, Subdomain
hide: true
hidefromtoc: true
badge: label="Beta"
source-git-commit: e63823dc2f901b870f11b0478e682e2af61b5b98
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 1%

---

# E-Mail-Oberflächeneinstellungen personalisieren {#surface-personalization}

Für mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen [!DNL Journey Optimizer] ermöglicht die Definition personalisierter Werte für Subdomains und Header<!--and URL tracking parameters--> beim Erstellen von E-Mail-Oberflächen.

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit als Beta-Version verfügbar, um nur Benutzer auszuwählen. <!--To join the beta program, contact Adobe Customer Care.-->

## Dynamische Subdomains hinzufügen {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalisierung nicht verfügbar"
>abstract="Diese Oberfläche wurde ohne Personalisierungsattribute erstellt. In der Dokumentation finden Sie Schritte, um zu beheben, ob eine Personalisierung erforderlich ist."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Dynamische Subdomains aktivieren"
>abstract="Beim Erstellen einer E-Mail-Oberfläche können Sie dynamische Subdomains basierend auf Bedingungen einrichten, die Sie mit dem Ausdruckseditor definieren. Sie können bis zu 50 dynamische Subdomains hinzufügen."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Einige Subdomains sind möglicherweise nicht verfügbar"
>abstract="Bestimmte Subdomains sind aufgrund der Registrierung einer ausstehenden Feedback-Schleife derzeit nicht zur Auswahl verfügbar. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss können Sie aus allen verfügbaren Subdomains auswählen."

Bei der Erstellung einer E-Mail-Oberfläche können Sie dynamische Subdomains basierend auf bestimmten Bedingungen einrichten.

Wenn Sie beispielsweise über rechtliche Einschränkungen zum Senden von Nachrichten von einer speziellen E-Mail-Adresse pro Land verfügen, können Sie dynamische Subdomains verwenden. Auf diese Weise können Sie eine einzige Oberfläche mit mehreren Versandsubdomains erstellen, die verschiedenen Ländern entsprechen, anstatt für jedes Land mehrere Oberflächen zu erstellen. Sie können dann Kunden in verschiedenen, in einer Kampagne konsolidierten Ländern ansprechen.

Gehen Sie wie folgt vor, um dynamische Subdomains in einer E-Mail-Kanal-Oberfläche zu definieren.

1. Richten Sie vor dem Erstellen einer Oberfläche die Subdomains ein, die Sie für den E-Mail-Versand verwenden möchten. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

   Angenommen, Sie möchten verschiedene Subdomains für verschiedene Länder verwenden: Einrichten einer Subdomain für die USA, einer für Großbritannien usw.

1. Erstellen einer Kanaloberfläche. [Weitere Informationen](../configuration/channel-surfaces.md)

1. Wählen Sie die **[!UICONTROL Email]** -Kanal.

1. Im **Subdomain** aktivieren Sie die **[!UICONTROL Dynamische Subdomain]** -Option.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Klicken Sie auf das Bearbeitungssymbol neben dem ersten **[!UICONTROL Bedingung]** -Feld.

1. Die [Ausdruckseditor](../personalization/personalization-build-expressions.md) geöffnet. Legen Sie in diesem Beispiel eine Bedingung wie `Country` gleich `US`.

   ![](assets/surface-email-edit-condition.png)

1. Wählen Sie die Subdomain aus, die Sie mit dieser Bedingung verknüpfen möchten. [Weitere Informationen zu Subdomains](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Bestimmte Subdomains stehen aufgrund von ausstehenden [Feedback Loop](../reports/deliverability.md#feedback-loops) registrieren. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss können Sie aus allen verfügbaren Subdomains auswählen. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Alle Empfänger in den USA erhalten Nachrichten, die die ausgewählte Subdomain für dieses Land verwenden. Das bedeutet, dass alle beteiligten URLs (z. B. Mirrorseite, Tracking-URL oder Abmelde-Link) auf der Basis dieser Subdomain gefüllt werden.

1. Legen Sie andere dynamische Subdomains nach Bedarf fest. Sie können bis zu 50 Elemente hinzufügen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

<!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Alle anderen definieren [E-Mail-Einstellungen](email-settings.md) und [submit](../configuration/channel-surfaces.md#create-channel-surface) Ihre Oberfläche.

Nachdem Sie eine oder mehrere dynamische Subdomains zu einer Oberfläche hinzugefügt haben, werden die folgenden Elemente basierend auf der aufgelösten dynamischen Subdomain für diese Oberfläche aufgefüllt:

* Alle URLs (Ressourcen-URL, Mirrorseiten-URL und Tracking-URL)

* Die [Abmelde-URL](email-settings.md#list-unsubscribe)

* Die **Aus E-Mail** und **Fehler-Email** Suffixe

>[!NOTE]
>
>Wenn Sie dynamische Subdomains einrichten, deaktivieren Sie die **[!UICONTROL Dynamische Subdomain]** -Option, werden alle dynamischen Werte entfernt. Wählen Sie eine Subdomain aus und senden Sie die Oberfläche, damit die Änderungen wirksam werden.

## Kopfzeile personalisieren {#personalize-header}

Sie können auch die Personalisierung für alle Header-Parameter verwenden, die auf einer Oberfläche definiert sind.

Wenn Sie beispielsweise über mehrere Marken verfügen, können Sie eine einzelne Oberfläche erstellen und für Ihre E-Mail-Header personalisierte Werte verwenden. Dadurch können Sie sicherstellen, dass alle von Ihren verschiedenen Marken gesendeten E-Mails mit den richtigen **Von** Namen und E-Mails. Wenn Ihre Empfänger die **Antwort** in der E-Mail-Client-Software, möchten Sie die **Antwort an** Namen und E-Mails entsprechen der richtigen Marke für den richtigen Benutzer.

Gehen Sie wie folgt vor, um personalisierte Variablen für die Parameter der Kopfzeile der Oberfläche zu verwenden.

>[!NOTE]
>
>Sie können alle **[!UICONTROL Kopfzeilenparameter]** -Felder außer **[!UICONTROL Fehler-E-Mail-Präfix]** -Feld.


1. Definieren Sie Ihre Header-Parameter wie gewohnt. [Weitere Informationen](email-settings.md#email-header)

1. Wählen Sie für jedes Feld das Symbol Bearbeiten aus.

   ![](assets/surface-email-personalize-header.png)

1. Die [Ausdruckseditor](../personalization/personalization-build-expressions.md) geöffnet. Definieren Sie Ihre Bedingung nach Bedarf und speichern Sie Ihre Änderungen.

   Legen Sie beispielsweise eine Bedingung fest, dass jeder Empfänger eine E-Mail von seinem eigenen Markenvertreter erhält.

   >[!NOTE]
   >
   >Sie können nur **[!UICONTROL Profilattribute]** und **[!UICONTROL Helper-Funktionen]**.

1. Wiederholen Sie die obigen Schritte für jeden Parameter, dem Sie Personalisierung hinzufügen möchten.

>[!NOTE]
>
>Wenn Sie Ihrer Oberfläche eine oder mehrere dynamische Subdomains hinzugefügt haben, wird die **Aus E-Mail** und **Fehler-Email** -Suffixe werden basierend auf den aufgelösten [dynamische Subdomain](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Anzeigen von Oberflächendetails {#view-surface-details}

Wenn Sie eine Oberfläche mit personalisierten Einstellungen in einer Kampagne oder einer Oberfläche verwenden, können Sie die Oberflächendetails direkt innerhalb der Kampagne oder Oberfläche anzeigen. Führen Sie dazu folgende Schritte durch.

1. E-Mail erstellen [Kampagne](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Wählen Sie die **[!UICONTROL Inhalt bearbeiten]** Schaltfläche.

1. Klicken Sie auf **[!UICONTROL Anzeigen von Oberflächendetails]** Schaltfläche.

   ![](assets/campaign-view-surface-details.png)

1. Die **[!UICONTROL Versandeinstellungen]** angezeigt. Sie können alle Oberflächeneinstellungen anzeigen, einschließlich der dynamischen Subdomains und der personalisierten Kopfzeilenparameter.

   >[!NOTE]
   >
   >Alle Informationen auf diesem Bildschirm sind schreibgeschützt.

1. Auswählen **[!UICONTROL Erweitern]** , um die Details der dynamischen Subdomains anzuzeigen.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)

