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
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 1%

---

# Dynamische E-Mail-Subdomains konfigurieren {#surface-personalization}

Für mehr Flexibilität und Kontrolle über Ihre E-Mail-Einstellungen bei der Erstellung von E-Mail-Oberflächen, [!DNL Journey Optimizer] ermöglicht die Definition personalisierter Werte für Subdomains, Header und URL-Tracking-Parameter.

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

Gehen Sie wie folgt vor, um dynamische Subdomains zu definieren.

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

1. Legen Sie eine andere dynamische Subdomain wie gewünscht fest. Sie können bis zu 50 Elemente hinzufügen.

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. Wählen Sie die [IP-Pool](../configuration/ip-pools.md) mit der Oberfläche zu verknüpfen. [Weitere Informationen](email-settings.md#subdomains-and-ip-pools)

Nachdem Sie eine oder mehrere dynamische Subdomains zu einer Oberfläche hinzugefügt haben, werden die folgenden Elemente basierend auf der aufgelösten dynamischen Subdomain für diese Oberfläche aufgefüllt:

* Alle URLs (Ressourcen-URL, Mirrorseiten-URL und Tracking-URL)

* Die [Abmelde-URL](email-settings.md#list-unsubscribe)

* Die **Aus E-Mail** und **Fehler-Email** Suffixe

## Kopfzeile personalisieren (#personalize-header)

Sie können auch die Personalisierung für alle Header-Parameter verwenden, die auf einer Oberfläche definiert sind.

Wenn Sie beispielsweise über mehrere Marken verfügen, können Sie eine einzelne Oberfläche erstellen und für Ihre E-Mail-Header personalisierte Werte verwenden. Dadurch können Sie sicherstellen, dass alle von Ihren verschiedenen Marken gesendeten E-Mails mit den richtigen **Von** Namen und E-Mails. Wenn Ihre Empfänger die **Antwort** in der E-Mail-Client-Software, möchten Sie die **Antwort an** Namen und E-Mails entsprechen der richtigen Marke für den richtigen Benutzer.

Gehen Sie wie folgt vor, um personalisierte Variablen für die Parameter der Kopfzeile der Oberfläche zu verwenden.

1. Definieren Sie Ihre Header-Parameter wie gewohnt. [Weitere Informationen](email-settings.md#email-header)

1. Wählen Sie für jedes Feld das Symbol Bearbeiten aus.

   ![](assets/surface-email-personalize-header.png)

1. Die [Ausdruckseditor](../personalization/personalization-build-expressions.md) geöffnet. Definieren Sie Ihre Bedingung nach Bedarf und speichern Sie Ihre Änderungen.<!--In this example, set a condition such as -->

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

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
