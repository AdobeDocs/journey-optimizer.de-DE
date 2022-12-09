---
title: Weberfahrungen erstellen
description: Erfahren Sie, wie Sie eine Webseite erstellen und ihren Inhalt in Journey Optimizer bearbeiten.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Weberfahrungen erstellen {#create-web}

>[!AVAILABILITY]
>
>Die Webkanalfunktion ist derzeit als Beta-Version verfügbar, über die nur Benutzer ausgewählt werden können.

[!DNL Journey Optimizer] ermöglicht es Ihnen, das Web-Erlebnis, das Sie Ihren Kunden über eingehende Web-Kampagnen bereitstellen, zu personalisieren.

>[!CAUTION]
>
>Derzeit in [!DNL Journey Optimizer] Sie können Web-Erlebnisse nur mit **Kampagnen**.

## Voraussetzungen {#prerequesites}

So können Sie auf Webseiten im [!DNL Journey Optimizer] Befolgen Sie die unten stehenden Voraussetzungen:

* Um Änderungen an Ihrer Website hinzuzufügen, müssen Sie die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;} auf Ihrer Website.

* So greifen Sie auf die [!DNL Journey Optimizer] Webdesigner müssen Sie die [Visual Editing Helper von Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=&quot;_blank&quot;} Browsererweiterung in Chrome. [Weitere Infos](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome ist derzeit der einzige Browser, der Authoring-Webseiten in unterstützt [!DNL Journey Optimizer].

Damit das Web-Erlebnis ordnungsgemäß bereitgestellt werden kann, müssen die folgenden Einstellungen definiert werden:

* Im [Adobe Experience Platform-Datenerfassung](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html){target=&quot;_blank&quot;} Stellen Sie sicher, dass Sie einen Datastream definiert haben, z. B. unter der **[!UICONTROL Adobe Experience Platform]** -Dienst haben Sie beide **[!UICONTROL Edge Segmentation]** und **[!UICONTROL Adobe Journey Optimizer]** Optionen aktiviert.

   Dadurch wird sichergestellt, dass die eingehenden Ereignisse von Journey Optimizer korrekt von Adobe Experience Platform Edge verarbeitet werden. [Weitere Infos](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target=&quot;_blank&quot;}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Adobe Journey Optimizer]** -Option kann nur aktiviert werden, wenn die **[!UICONTROL Edge Segmentation]** -Option bereits aktiviert ist.

* In [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}, stellen Sie sicher, dass Sie eine Zusammenführungsrichtlinie mit der **[!UICONTROL Active-On-Edge Merge Policy]** aktiviert ist. Wählen Sie dazu eine Richtlinie unter dem **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Menü &quot;Experience Platform&quot;. [Weitere Infos](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target=&quot;_blank&quot;}

   Diese Zusammenführungsrichtlinie wird von [!DNL Journey Optimizer] eingehende Kanäle, um eingehende Kampagnen korrekt zu aktivieren und zu veröffentlichen. [Weitere Infos](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target=&quot;_blank&quot;}

   ![](assets/web-aep-merge-policy.png)

## Webkampagne erstellen {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Weboberfläche definieren"
>abstract="Eine Weboberfläche kann mit einer einzelnen Seiten-URL oder mehreren Seiten übereinstimmen, sodass Sie Inhaltsänderungen auf einer oder mehreren Webseiten bereitstellen können."

Gehen Sie wie folgt vor, um mit der Erstellung Ihres Web-Erlebnisses durch eine Kampagne zu beginnen.

1. Erstellen Sie eine Kampagne. [Weitere Infos](../campaigns/create-campaign.md)

1. Wählen Sie die **[!UICONTROL Web]** Aktion.

   ![](assets/web-create-campaign.png)

1. Definieren Sie eine Weboberfläche.

   >[!NOTE]
   >
   >Eine Weboberfläche ist eine Webeigenschaft, die durch eine URL identifiziert wird, über die der Inhalt bereitgestellt wird. Sie kann mit einer einzelnen Seiten-URL oder mehreren Seiten übereinstimmen, sodass Sie Änderungen auf einer oder mehreren Webseiten bereitstellen können.

   Sie können entweder eine **[!UICONTROL Page URL]** , wenn Sie die Änderungen nur auf eine einzelne Seite anwenden möchten.

   ![](assets/web-campaign-surface.png)

1. Sie können auch eine **[!UICONTROL Pages matching rule]** , um mehrere URLs als Ziel auszuwählen, die derselben Regel entsprechen, z. B. wenn Sie die Änderungen auf ein Hero-Banner auf einer ganzen Website anwenden möchten oder ein oberstes Bild hinzufügen möchten, das auf allen Produktseiten einer Website angezeigt wird.

   Wählen Sie dazu **[!UICONTROL Pages matching rule]** und klicken Sie auf **[!UICONTROL Create rule]**.

   ![](assets/web-campaign-matching-rule.png)

1. Definieren Sie Ihre Kriterien für die **[!UICONTROL Domain]** und **[!UICONTROL Page]** -Felder.

   Wenn Sie beispielsweise Elemente bearbeiten möchten, die auf allen Damenproduktseiten Ihrer Luma-Website angezeigt werden, wählen Sie **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `luma` und **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Speichern Sie Ihre Änderungen. Die Regel wird im **[!UICONTROL Create campaign]** angezeigt.

   ![](assets/web-pages-matching-rule-example.png)

1. Nachdem Sie die Weboberfläche definiert haben, wählen Sie **[!UICONTROL Create]**. Jetzt können Sie die Eigenschaften und Einstellungen Ihrer Kampagne konfigurieren.

## Webkampagne konfigurieren {#configure-web-campaign}

1. Im **[!UICONTROL Properties]** können Sie den Kampagnennamen bearbeiten und bei Bedarf eine Beschreibung hinzufügen.

   ![](assets/web-campaign-properties.png)

1. Um der Webkampagne benutzerdefinierte oder zentrale Datennutzungsbezeichnungen zuzuweisen, wählen Sie die **[!UICONTROL Manage access]** -Schaltfläche am oberen Bildschirmrand. [Weitere Informationen zur Zugriffskontrolle auf Objektebene (OLAC)](../administration/object-based-access.md)

1. Sie können **[!UICONTROL Content experiment]** , um Inhaltsbehandlungen mit Teilen der Zielgruppe zu testen, um festzustellen, welche Behandlung im Vergleich zu einer bestimmten Metrik am besten abschneidet. [Weitere Infos](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >Die **Inhaltstest** ist derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrem Adobe-Support-Mitarbeiter.

1. Aus dem **[!UICONTROL Action]** im Tab der Kampagne, wählen Sie **[!UICONTROL Edit content]** , um mit der Erstellung Ihrer Web-Kampagne zu beginnen. [Weitere Infos](author-web.md)

   ![](assets/web-edit-content.png)

1. Aus dem **[!UICONTROL Audience]** festlegen, wer Ihre Web-Kampagne sehen kann. Standardmäßig ist die Webkampagne für alle Besucher sichtbar.

   ![](assets/web-campaign-audience.png)

   Sie können auch eine bestimmte Zielgruppe auswählen. Verwenden Sie die **[!UICONTROL Select audience]** -Schaltfläche, um die Liste der verfügbaren Adobe Experience Platform-Segmente anzuzeigen. [Weitere Informationen zu Segmenten](../segment/about-segments.md)

   >[!NOTE]
   >
   >Für API-gesteuerte Kampagnen muss die Zielgruppe über API-Aufruf festgelegt werden. [Weitere Infos](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. Im **[!UICONTROL Identity namespace]** wählen Sie den Namespace aus, der verwendet werden soll, um die Kontakte aus dem ausgewählten Segment zu identifizieren. [Weitere Informationen zu Namespaces](../event/about-creating.md#select-the-namespace)

1. Definieren Sie eine **[!UICONTROL Schedule]** für Ihre Web-Kampagne. [Weitere Infos](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   Standardmäßig startet sie bei manueller Aktivierung und endet, wenn sie manuell gestoppt wird. Sie können aber auch bestimmte Daten und Uhrzeiten definieren, damit Ihre Änderungen sichtbar sind.

   ![](assets/web-campaign-schedule-start.png)

## Aktivieren der Webkampagne {#activate-web-campaign}

Nachdem Sie Ihre [Webkampagneneinstellungen](#configure-web-campaign) und Sie haben Ihren Inhalt wie gewünscht mit dem [Webdesigner](author-web.md), können Sie Ihre Webkampagne überprüfen und aktivieren. Gehen Sie wie folgt vor:

>[!NOTE]
>
>Sie können vor der Aktivierung auch eine Vorschau des Webkampagneninhalts anzeigen. [Weitere Infos](author-web.md#test-web-campaign)

1. Wählen Sie in Ihrer Web-Kampagne **[!UICONTROL Review to activate]**.

   ![](assets/web-campaign-review.png)

1. Überprüfen und bearbeiten Sie bei Bedarf Inhalt, Eigenschaften, Oberfläche, Zielgruppe und Zeitplan.

1. Auswählen **[!UICONTROL Activate]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Nachdem Sie auf **[!UICONTROL Activate]** kann es bis zu 15 Minuten dauern, bis Webkampagnenänderungen live auf Ihrer Website verfügbar sind.

Ihre Webkampagne **[!UICONTROL Live]** -Status und ist nun für die ausgewählte Zielgruppe sichtbar. Jeder Empfänger Ihrer Kampagne kann die Änderungen sehen, die Sie Ihrer Website mithilfe der Variablen [!DNL Journey Optimizer] Webdesigner.

>[!NOTE]
>
>Wenn Sie einen Zeitplan für Ihre Webkampagne definiert haben, wird die Variable **[!UICONTROL Scheduled]** Status bis zum Erreichen des Anfangsdatums und der Startzeit.
>
>Wenn Sie eine Webkampagne aktivieren, die sich auf dieselben Seiten auswirkt wie eine andere bereits aktive Kampagne, werden alle Änderungen auf Ihre Webseiten angewendet.

Erfahren Sie mehr über das Aktivieren von Kampagnen in [diesem Abschnitt](../campaigns/review-activate-campaign.md).

## Eine Webkampagne stoppen {#stop-web-campaign}

Wenn eine Webkampagne live ist, können Sie sie stoppen, um zu verhindern, dass Ihre Änderungen für Ihre Zielgruppe sichtbar werden. Gehen Sie wie folgt vor:

1. Wählen Sie eine Live-Kampagne aus der Liste aus.

1. Wählen Sie im oberen Menü **[!UICONTROL Stop campaign]**.

   ![](assets/web-campaign-stop.png)

1. Die hinzugefügten Änderungen sind für die von Ihnen definierte Zielgruppe nicht mehr sichtbar.

>[!NOTE]
>
>Nachdem eine Webkampagne angehalten wurde, kann sie nicht mehr bearbeitet oder wieder aktiviert werden. Sie können sie nur duplizieren und die duplizierte Kampagne aktivieren.
