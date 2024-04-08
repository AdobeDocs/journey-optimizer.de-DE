---
solution: Journey Optimizer
product: journey optimizer
title: Dynamische E-Mail-Subdomains konfigurieren
description: Erfahren Sie, wie Sie dynamische Subdomains auf der Ebene der E-Mail-Kanal-Oberfläche konfigurieren
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: Einstellungen, E-Mail, Konfiguration, Subdomain
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 94d39089d94b4fe42eb3fb95603426012b104517
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 1%

---

# E-Mail-Oberflächeneinstellungen personalisieren {#surface-personalization}

Mehr Flexibilität und Kontrolle über E-Mail-Einstellungen [!DNL Journey Optimizer] Ermöglicht die Definition personalisierter Werte für Subdomains und Header<!--and URL tracking parameters--> beim Erstellen von E-Mail-Oberflächen.

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. <!--To join the beta program, contact Adobe Customer Care.-->

## Hinzufügen dynamischer Subdomains {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalisierung nicht verfügbar"
>abstract="Diese Oberfläche wurde ohne Personalisierungsattribute erstellt. Anweisungen zur Behebung, ob eine Personalisierung erforderlich ist, finden Sie in der Dokumentation."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Dynamische Subdomains aktivieren"
>abstract="Beim Erstellen einer E-Mail-Oberfläche können Sie dynamische Subdomains basierend auf Bedingungen einrichten, die Sie mit dem Ausdruckseditor definieren. Sie können bis zu 50 dynamische Subdomains hinzufügen."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Einige Subdomains sind möglicherweise nicht verfügbar"
>abstract="Bestimmte Subdomains sind derzeit aufgrund der ausstehenden Registrierung der Feedback-Schleife nicht zur Auswahl verfügbar. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss des Vorgangs können Sie aus allen verfügbaren Subdomains auswählen."

Beim Erstellen einer E-Mail-Oberfläche können Sie dynamische Subdomains auf der Grundlage bestimmter Bedingungen einrichten.

Wenn beispielsweise rechtliche Einschränkungen für den Versand von Nachrichten von einer bestimmten E-Mail-Adresse pro Land gelten, können dynamische Subdomains verwendet werden. Auf diese Weise können Sie eine einzelne Oberfläche mit mehreren Versand-Subdomains erstellen, die verschiedenen Ländern entsprechen, anstatt mehrere Oberflächen für jedes Land zu erstellen. Sie können dann Kunden in verschiedenen Ländern ansprechen, die in einer Kampagne zusammengefasst sind.

Gehen Sie wie folgt vor, um dynamische Subdomains in einer E-Mail-Kanaloberfläche zu definieren.

1. Bevor Sie eine Oberfläche erstellen, richten Sie die Subdomains ein, die Sie für den Versand von E-Mails je nach Anwendungsfall verwenden möchten. [Weitere Informationen](../configuration/about-subdomain-delegation.md)

   Angenommen, Sie möchten verschiedene Subdomains für verschiedene Länder verwenden: Richten Sie eine Subdomain ein, die speziell für die USA gilt, eine für Großbritannien usw.

1. Erstellen einer Kanaloberfläche. [Weitere Informationen](../configuration/channel-surfaces.md)

1. Wählen Sie die **[!UICONTROL E-Mail]** Kanal.

1. In der **Subdomain** Abschnitt, aktivieren Sie die **[!UICONTROL Dynamische Subdomain]** Option.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Klicken Sie auf das Symbol Bearbeiten neben dem ersten **[!UICONTROL Bedingung]** Feld.

1. Die [Ausdruckseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Legen Sie in diesem Beispiel eine Bedingung wie fest. `Country` ist gleich `US`.

   ![](assets/surface-email-edit-condition.png)

1. Subdomain auswählen, die mit dieser Bedingung verknüpft werden soll. [Weitere Informationen zu Subdomains](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Bestimmte Subdomains stehen derzeit aufgrund ausstehender Anfragen nicht zur Auswahl [Rückkopplungsschleife](../reports/deliverability.md#feedback-loops) Registrierung. Dieser Vorgang kann bis zu 10 Werktage dauern. Nach Abschluss des Vorgangs können Sie aus allen verfügbaren Subdomains auswählen. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Alle Empfänger in den USA erhalten Nachrichten unter Verwendung der ausgewählten Subdomain für dieses Land, was bedeutet, dass alle beteiligten URLs (wie Mirrorseite, Tracking-URL oder Abmelde-Link) basierend auf dieser Subdomain ausgefüllt werden.

1. Legen Sie andere dynamische Subdomains nach Bedarf fest. Sie können bis zu 50 Elemente hinzufügen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Alle anderen definieren [E-Mail-Einstellungen](email-settings.md) und [einreichen](../configuration/channel-surfaces.md#create-channel-surface) Ihre Oberfläche.

Nachdem Sie eine oder mehrere dynamische Subdomains zu einer Oberfläche hinzugefügt haben, werden die folgenden Elemente basierend auf der aufgelösten dynamischen Subdomain für diese Oberfläche ausgefüllt:

* Alle URLs (Ressourcen-URL, Mirrorseiten-URL und Tracking-URL)

* Die [Abmelde-URL](email-settings.md#list-unsubscribe)

* Die **Von E-Mail** und **Fehler-E-Mail** Suffixe

>[!NOTE]
>
>Beim Einrichten dynamischer Subdomains und anschließendem Deaktivieren von **[!UICONTROL Dynamische Subdomain]** alle dynamischen Werte entfernt werden. Wählen Sie eine Subdomain aus und senden Sie die Oberfläche, damit die Änderungen wirksam werden.

## Personalisieren der Kopfzeile {#personalize-header}

Sie können auch eine Personalisierung für alle in einer Oberfläche definierten Kopfzeilenparameter verwenden.

Wenn Sie beispielsweise über mehrere Marken verfügen, können Sie eine einzelne Oberfläche erstellen und personalisierte Werte für Ihre E-Mail-Kopfzeilen verwenden. Auf diese Weise können Sie sicherstellen, dass alle von Ihren verschiedenen Marken gesendeten E-Mails mit den richtigen **Von** Namen und E-Mails. Ähnlich verhält es sich, wenn Ihre Empfänger die **Antwort** in ihrer E-Mail-Client-Software verwenden, möchten Sie die **Antwort an** Namen und E-Mails entsprechen der richtigen Marke für den richtigen Benutzer.

Gehen Sie wie folgt vor, um personalisierte Variablen für die Kopfzeilenparameter Ihrer Oberfläche zu verwenden.

>[!NOTE]
>
>Sie können alle personalisieren **[!UICONTROL Header-Parameter]** Felder mit Ausnahme des **[!UICONTROL E-Mail-Präfix für Fehler]** Feld.


1. Definieren Sie Ihre Header-Parameter wie gewohnt. [Weitere Informationen](email-settings.md#email-header)

1. Wählen Sie für jedes Feld das Symbol Bearbeiten aus.

   ![](assets/surface-email-personalize-header.png)

1. Die [Ausdruckseditor](../personalization/personalization-build-expressions.md) wird geöffnet. Definieren Sie Ihre Bedingung wie gewünscht und speichern Sie Ihre Änderungen.

   Legen Sie beispielsweise eine Bedingung fest, nach der jeder Empfänger eine E-Mail von seinem eigenen Markenvertreter erhält.

   >[!NOTE]
   >
   >Sie können nur auswählen **[!UICONTROL Profilattribute]** und **[!UICONTROL Helper-Funktionen]**.

1. Wiederholen Sie die obigen Schritte für jeden Parameter, dem Sie eine Personalisierung hinzufügen möchten.

>[!NOTE]
>
>Wenn Sie eine oder mehrere dynamische Subdomains zu Ihrer Oberfläche hinzugefügt haben, gilt Folgendes: **Von E-Mail** und **Fehler-E-Mail** Suffixe werden basierend auf dem aufgelösten -Objekt gefüllt [Dynamische Subdomain](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Oberflächendetails anzeigen {#view-surface-details}

Bei Verwendung einer Oberfläche mit personalisierten Einstellungen in einer Kampagne oder einer Oberfläche können Sie die Details der Oberfläche direkt in der Kampagne oder in der Oberfläche anzeigen. Führen Sie dazu folgende Schritte durch.

1. E-Mail erstellen [Wahlkampf](../campaigns/create-campaign.md) oder [Journey](../building-journeys/journey-gs.md).

1. Wählen Sie die **[!UICONTROL Inhalt bearbeiten]** Schaltfläche.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Oberflächendetails anzeigen]** Schaltfläche.

   ![](assets/campaign-view-surface-details.png)

1. Die **[!UICONTROL Versandeinstellungen]** Das Fenster wird angezeigt. Sie können alle Oberflächeneinstellungen anzeigen, einschließlich der dynamischen Subdomains und personalisierten Kopfzeilenparameter.

   >[!NOTE]
   >
   >Alle Informationen auf diesem Bildschirm sind schreibgeschützt.

1. Auswählen **[!UICONTROL Expand]** , um die Details der dynamischen Subdomains anzuzeigen.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
