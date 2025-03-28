---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit der Integration von GenStudio in Journey Optimizer
description: Erfahren Sie, wie Sie in Journey Optimizer mit GenStudio arbeiten
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: e5edb719c4ff30385242700217c9c4c07ff28373
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 3%

---

# Erste Schritte mit der GenStudio-Integration {#gs-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Verwenden einer mit GenStudio erstellten Vorlage"
>abstract="Dank der nahtlosen Integration mit Adobe GenStudio for Performance Marketing können Sie eine GenStudio-Vorlage, die mit der Adobe-KI-Technologie erweitert wurde, einfach importieren."

>[!AVAILABILITY]
>
>Die GenStudio-Integration in [!DNL Adobe Journey Optimizer] ist derzeit nicht für die Verwendung mit den Add-on **Angeboten** Healthcare Shield oder **Privacy and Security Shield** verfügbar.
>
>Diese Funktion steht nur beim E-Mail-Kanal zur Verfügung.

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/de/products/genstudio-for-performance-marketing.html){target="_blank"} ist eine generative KI-First-Anwendung, mit der Marketing-Teams ihre eigenen Anzeigen und E-Mails erstellen können, um wirkungsvolle, personalisierte Marketing-Kampagnen zu fördern, die Ihren Markenstandards entsprechen und Ihren Unternehmensrichtlinien entsprechen. Durch die Nutzung der KI-Technologie von Adobe bietet diese eine umfassende Palette an Tools, die die komplexe Erstellung und Verwaltung von Inhalten vereinfachen, sodass sich Kreative auf Innovationen konzentrieren können.

Weitere Informationen zu [!DNL GenStudio for Performance Marketing] finden Sie in der entsprechenden [Dokumentation](https://experienceleague.adobe.com/de/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"}.

>[!INFO]
>
>Weitere Informationen finden Sie in dieser [Übersicht](https://business.adobe.com/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"} und einer [Demo](https://business.adobe.com/products/genstudio-for-performance-marketing.html#demo){target="_blank"} von [!DNL Adobe GenStudio for Performance Marketing].

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

Um die Marketing-Effizienz zu steigern und die Markenkonsistenz zu wahren, können Sie [!DNL **GenStudio for Performance Marketing**]-Erlebnisse nahtlos mit [!DNL **Adobe Journey Optimizer**] integrieren. Auf diese Weise können Sie die KI-gestützte Inhaltserstellung von [!DNL GenStudio] zusammen mit den erweiterten Orchestrierungsfunktionen von [!DNL Journey Optimizer] nutzen.

<!--![](../rn/assets/do-not-localize/genstudio.gif)-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](gs-generative.md#generative-guardrails) for the AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Nutzen der GenStudio-Funktionen in Journey Optimizer {#use-genstudio}

Durch die Integration von [!DNL GenStudio for Performance Marketing] und [!DNL Journey Optimizer] können Marketing-Fachleute in Ihrem Unternehmen besser zusammenarbeiten, um Prozesse zu optimieren.

Ein technischer Marketing-Experte, der [!DNL Journey Optimizer] zum Entwickeln und Automatisieren von E-Mail-Kampagnen verwendet, kann beispielsweise mit einem Performance-Marketing-Experten zusammenarbeiten, der Inhalte mithilfe von [!DNL GenStudio] erstellt.

Mit dieser Integration können beide zusammenarbeiten, um markeninterne Inhalte von [!DNL GenStudio] einfach in [!DNL Journey Optimizer] zu integrieren und ansprechende E-Mails zu versenden, die auf bestimmte Kundensegmente zugeschnitten sind und den Umsatz steigern.

### Exportieren einer HTML-Vorlage von Journey Optimizer nach GenStudio {#export-from-ajo-to-genstudio}

Zunächst können Sie eine [!DNL Journey Optimizer] HTML-Vorlage mit den Richtlinien Ihrer Marke nach [!DNL GenStudio for Performance Marketing] exportieren. Führen Sie dazu folgende Schritte durch.

1. Greifen Sie [!DNL Journey Optimizer] auf den Inhalt Ihrer E-Mail in einer Journey oder Kampagne zu. [Weitere Informationen](../email/get-started-email-design.md#key-steps)

1. Wählen Sie in der E-Mail-Designer **[!UICONTROL HTML exportieren]** über die Schaltfläche **[!UICONTROL Mehr]** aus.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Laden Sie diese exportierte HTML-Vorlage in [!DNL GenStudio for Performance Marketing] hoch. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Im entsprechenden Abschnitt des [Adobe GenStudio for Performance Marketing-Benutzerhandbuchs erfahren Sie, wie Sie eine HTML-Vorlage in [!DNL GenStudio] hochladen](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. Verwenden Sie in GenStudio diese Vorlage, um mehrere E-Mail-Varianten mit KI-Eingabeaufforderungen zu erstellen und zu speichern.

   >[!NOTE]
   >
   >Wie Sie E-Mail-Erlebnisse erstellen, erfahren Sie im entsprechenden Abschnitt [ GenStudio](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"}.

### GenStudio-Erlebnisse in Journey Optimizer nutzen {#leverage-genstudio-experiences}

Gehen Sie wie folgt vor, um die [!DNL GenStudio] E-Mail-Varianten zu nutzen, die Sie soeben durch Importieren in [!DNL Journey Optimizer] erstellt haben.

1. Fügen Sie [!DNL Journey Optimizer] einer Kampagne [E-](../email/create-email.md) hinzu“.

1. Wechseln Sie im Konfigurationsbildschirm der Kampagne zum Bildschirm [Inhalt bearbeiten](../email/create-email.md#define-email-content) und klicken Sie auf **[!UICONTROL E-Mail-Textkörper bearbeiten]**, um die E-Mail-Designer zu öffnen. [Weitere Informationen](../email/get-started-email-design.md#key-steps)

1. Wählen Sie auf der Startseite von E-Mail-Designer **[!UICONTROL HTML importieren]** und klicken Sie auf die Schaltfläche **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Durchsuchen Sie die GenStudio-Erlebnisse, um mit der Erstellung Ihrer Inhalte zu beginnen. Sie können die Erlebnisse nach verschiedenen Kriterien filtern, z. B. nach Produkten, Rollen, Marken oder sogar Farben.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Wählen Sie ein Erlebnis aus und klicken Sie auf **[!UICONTROL Verwenden]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Wählen Sie den Ordner aus, in den Sie das GenStudio-Erlebnis importieren möchten.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. Der ausgewählte Inhalt wird in der E-Mail-Designer angezeigt.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >GenStudio-Erlebnisse [erstellt aus einer  [!DNL Journey Optimizer] -Vorlage](#export-from-ajo-to-genstudio) werden direkt in die E-Mail-Designer importiert. GenStudio-Erlebnisse, die ohne [!DNL Journey Optimizer] erstellt wurden, werden in den [Kompatibilitätsmodus“ ](../email/existing-content.md).

   Verwenden Sie die [Tools zur Bearbeitung von E](../email/content-from-scratch.md)Mail-Inhalten und [Personalisierungsfelder](../personalization/personalize.md), um Ihre E-Mail nach Bedarf zu bearbeiten. Speichern Sie Ihren Inhalt.

1. Gehen Sie zurück zur Übersichtsseite der Kampagne und klicken Sie auf **[!UICONTROL Experiment erstellen]**, um es zu verwenden. [Erfahren Sie, wie Sie ein Inhaltsexperiment erstellen](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Erstellen Sie mehrere Abwandlungen und wiederholen Sie die obigen Schritte, um die anderen E-Mail-Erlebnisvarianten, die Sie in [!DNL GenStudio] erstellt haben, zu importieren und schnell zu nutzen.

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Speichern Sie Ihre Änderungen und [ Sie ](../campaigns/review-activate-campaign.md) Kampagne.

Verfolgen Sie nach der Durchführung des Experiments mit dem [Experimentationskampagnenbericht](../reports/campaign-global-report-cja-experimentation.md), wie Ihre Kampagnenbehandlungen funktionieren. Anschließend können Sie die Ergebnisse Ihres Experiments interpretieren. [Weitere Informationen](../content-management/get-started-experiment.md#interpret-results)
