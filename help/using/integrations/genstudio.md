---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit GenStudio for Performance Marketing in Journey Optimizer
description: Informationen zur Arbeit mit GenStudio for Performance Marketing in Journey Optimizer
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: 73a347c104fe28799c264f9a8b6c3e5e12c8d892
workflow-type: ht
source-wordcount: '669'
ht-degree: 100%

---

# Arbeiten mit GenStudio for Performance Marketing {#ajo-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Verwenden einer mit GenStudio erstellten Vorlage"
>abstract="Dank der nahtlosen Integration mit Adobe GenStudio for Performance Marketing können Sie eine mit KI-Technologie von Adobe erweiterte GenStudio-Vorlage einfach importieren."

## Erste Schritte mit GenStudio {#gs-genstudio}

[Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"} ist eine generative KI-First-Anwendung, mit der Marketing-Teams ihre eigenen Anzeigen und E-Mails erstellen können, um wirkungsvolle, personalisierte Marketing-Kampagnen voranzubringen, die Ihren Markenstandards und Unternehmensrichtlinien entsprechen. Dank der KI-Technologie von Adobe bietet diese Anwendung eine umfassende Palette an Tools, die die komplexe Erstellung und Verwaltung von Inhalten vereinfachen, sodass sich Kreative darauf konzentrieren können, innovativ zu sein.

>[!AVAILABILITY]
>
>* Die GenStudio-Integration in [!DNL Adobe Journey Optimizer] ist derzeit nicht für die Verwendung mit den Add-ons **Healthcare Shield** oder **Privacy and Security Shield** verfügbar.
>
>* Diese Funktion steht nur für den E-Mail-Kanal zur Verfügung.

Um die Marketing-Effizienz zu steigern und Markenkonsistenz zu gewährleisten, können Sie [!DNL **GenStudio for Performance Marketing**]-Erlebnisse nahtlos mit [!DNL **Adobe Journey Optimizer**] integrieren. Nutzen Sie so die KI-gestützte Inhaltserstellung von [!DNL GenStudio] zusammen mit den erweiterten Orchestrierungsfunktionen von [!DNL Journey Optimizer].

![Importieren von GenStudio-Inhalten in Adobe Journey Optimizer](../rn/assets/do-not-localize/genstudio.gif)

>[!INFO]
>
>Weitere Informationen finden Sie in diesem [Überblick](https://business.adobe.com/de/products/genstudio-for-performance-marketing.html?lang=de#watch-overview){target="_blank"} und einer [Demo](https://business.adobe.com/de/products/genstudio-for-performance-marketing.html?lang=de#demo){target="_blank"} zu [!DNL Adobe GenStudio for Performance Marketing].

➡️ [Funktion im Video kennenlernen](#video)


<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->



<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](../content-management/gs-generative.md#generative-guardrails) for AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Verwenden der GenStudio-Funktionen in Journey Optimizer {#use-genstudio}

Durch die Integration von [!DNL GenStudio for Performance Marketing] und [!DNL Journey Optimizer] können Marketing-Fachleute in Ihrem Unternehmen besser im Team arbeiten, um Prozesse zu optimieren.

Eine technische Marketing-Fachkraft, die mit [!DNL Journey Optimizer] E-Mail-Kampagnen entwickelt und automatisiert, kann beispielsweise mit einer Performance-Marketing-Fachkraft zusammenarbeiten, die Inhalte mithilfe von [!DNL GenStudio] erstellt.

Mithilfe dieser Integration können beide zusammenarbeiten, um markenkonforme Inhalte von [!DNL GenStudio] einfach in [!DNL Journey Optimizer] zu integrieren und so ansprechende E-Mails zu versenden, die auf bestimmte Kundensegmente zugeschnitten sind und den Umsatz fördern.

### Exportieren einer HTML-Vorlage von Journey Optimizer nach GenStudio {#export-from-ajo-to-genstudio}

Zunächst können Sie eine [!DNL Journey Optimizer]-HTML-Vorlage mit den Richtlinien Ihrer Marke nach [!DNL GenStudio for Performance Marketing] exportieren. Führen Sie dazu folgende Schritte durch.

1. Greifen Sie in [!DNL Journey Optimizer] auf den Inhalt Ihrer E-Mail in einer Journey oder Kampagne zu. [Weitere Informationen](../email/get-started-email-design.md#key-steps)

1. Wählen Sie im E-Mail-Designer über die Schaltfläche **[!UICONTROL Mehr]** die Option **[!UICONTROL HTML exportieren]** aus.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Laden Sie diese exportierte HTML-Vorlage in [!DNL GenStudio for Performance Marketing] hoch. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Informationen zum Hochladen einer HTML-Vorlage in [!DNL GenStudio] finden Sie im entsprechenden Abschnitt des [Benutzerhandbuchs zu Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. Verwenden Sie in GenStudio diese Vorlage, um mehrere E-Mail-Varianten mit KI-Prompts zu erstellen und zu speichern.

   >[!NOTE]
   >
   >Wie Sie E-Mail-Erlebnisse erstellen, erfahren Sie im entsprechenden [Abschnitt](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"} des GenStudio-Benutzerhandbuchs.

### Nutzen von GenStudio-Erlebnissen in Journey Optimizer {#leverage-genstudio-experiences}

Gehen Sie wie folgt vor, um die [!DNL GenStudio]-E-Mail-Varianten zu nutzen, die Sie soeben durch deren Import in [!DNL Journey Optimizer] erstellt haben.

1. [Fügen Sie in [!DNL Journey Optimizer] eine E-Mail zu einer Kampagne hinzu](../email/create-email.md).

1. Gehen Sie im Bildschirm zur Kampagnenkonfiguration den Bildschirm [Inhalt bearbeiten](../email/create-email.md#define-email-content) durch und klicken Sie auf **[!UICONTROL E-Mail-Text bearbeiten]**, um den E-Mail-Designer zu öffnen. [Weitere Informationen](../email/get-started-email-design.md#key-steps)

1. Wählen Sie auf der Startseite des E-Mail-Designers die Option **[!UICONTROL HTML importieren]** aus und klicken Sie auf die Schaltfläche **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Durchsuchen Sie die GenStudio-Erlebnisse, um mit der Erstellung Ihrer Inhalte zu beginnen. Sie können die Erlebnisse nach verschiedenen Kriterien filtern, z. B. nach Produkten, Personas, Marken oder sogar Farben.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Wählen Sie ein Erlebnis aus und klicken Sie auf **[!UICONTROL Verwenden]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Wählen Sie den Ordner aus, in den das GenStudio-Erlebnis importiert werden soll.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. Der ausgewählte Inhalt wird im E-Mail-Designer angezeigt.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >GenStudio-Erlebnisse, die [anhand einer [!DNL Journey Optimizer] -Vorlage erstellt wurden](#export-from-ajo-to-genstudio), werden direkt in den E-Mail-Designer importiert. GenStudio-Erlebnisse, die ohne eine [!DNL Journey Optimizer]-Vorlage erstellt wurden, werden in den [Kompatibilitätsmodus](../email/existing-content.md) importiert.

   Verwenden Sie die [Tools zur Bearbeitung von E-Mail-Inhalten](../email/content-from-scratch.md) und [Personalisierungsfelder](../personalization/personalize.md), um Ihre E-Mail wie gewünscht zu bearbeiten. Speichern Sie Ihren Inhalt.

1. Gehen Sie zurück zur Übersichtsseite der Kampagne und klicken Sie auf **[!UICONTROL Experiment erstellen]**, um die Experimentierfunktion zu verwenden. [Erfahren Sie, wie Sie ein Inhaltsexperiment erstellen](../content-management/content-experiment.md).

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Erstellen Sie mehrere Abwandlungen und wiederholen Sie die obigen Schritte, um die anderen von Ihnen in [!DNL GenStudio] erstellten E-Mail-Erlebnisvarianten zu importieren und schnell nutzen zu können.

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Speichern Sie Ihre Änderungen und [aktivieren](../campaigns/review-activate-campaign.md) Sie die Kampagne. 

Verfolgen Sie nach dem Ausführen des Experiments mit dem [Experimentkampagnenbericht](../reports/campaign-global-report-cja-experimentation.md), wie Ihre Kampagnenabwandlungen funktionieren. Sie können dann die Ergebnisse Ihres Experiments auslegen. [Weitere Informationen](../content-management/get-started-experiment.md#interpret-results)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie eine E-Mail-Vorlage aus Journey Optimizer in GenStudio for Performance Marketing exportieren, markenkonforme E-Mails mit der Vorlage in GenStudio erstellen und diese dann nahtlos wieder in Journey Optimizer importieren.

>[!VIDEO](https://video.tv.adobe.com/v/3456038/?quality=12)