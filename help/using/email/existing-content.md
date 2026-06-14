---
solution: Journey Optimizer
product: journey optimizer
title: Importieren von E-Mail-Inhalten
description: Erfahren Sie, wie Sie E-Mail-Inhalte importieren.
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: E-Mail, Import, Inhalt, HTML, ZIP, CSS
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
TQID: https://experienceleague.adobe.com/R0Csd9gbvY-iyW81G-clHoXozEBYWBfjb0y9PWq4zZA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 88%

---

# Importieren von E-Mail-Inhalten {#existing-content}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie vorhandene HTML-Inhalte importieren, entweder als HTML-Datei oder als ZIP-Ordner, und konvertieren Sie sie, damit Sie sie mit der E-Mail-Designer bearbeiten und personalisieren können.

>[!ENDSHADEBOX]

Mit [!DNL Journey Optimizer] können Sie vorhandenen HTML-Inhalt importieren, um Ihre E-Mails zu gestalten. Der Inhalt kann vorliegen als

* eine **HTML-Datei** mit integriertem Stylesheet;
* ein **komprimierter Ordner** (ZIP) mit HTML-Datei, Stylesheet (.css) und Bildern.

  >[!NOTE]
  >
  >Die Dateistruktur des komprimierten Ordners ist freigestellt. Verweise müssen jedoch relativ sein und mit der Baumstruktur des ZIP-Ordners übereinstimmen.


>[!TIP]
>
>Wenn Sie Bildentwürfe (JPEG oder PNG) anstelle von HTML-Dateien haben, können Sie den [Bild-zu-HTML-Converter](../content-management/image-to-html.md) verwenden, um diese automatisch mithilfe von KI in bearbeitbare HTML-E-Mail-Vorlagen zu konvertieren.

Gehen Sie wie folgt vor, um eine Datei mit HTML-Inhalt zu importieren:

1. Wählen Sie auf der Startseite des E-Mail-Designers die Option **[!UICONTROL HTML importieren]**.

   ![](assets/import-html_2.png)

1. Ziehen Sie die HTML- oder ZIP-Datei mit Ihrem HTML-Inhalt per Drag-and-Drop und klicken Sie auf **[!UICONTROL Importieren]**.

   ![](assets/html-imported_2.png)

1. Sobald der HTML-Inhalt hochgeladen wurde, befindet sich Ihr Inhalt im **[!UICONTROL Kompatibilitätsmodus]**.

   In diesem Modus können Sie nur Ihren Text personalisieren, Links hinzufügen oder Assets zu Ihrem Inhalt hinzufügen.

1. Um die Inhaltskomponenten des E-Mail-Designers nutzen zu können, gehen Sie zur Registerkarte **[!UICONTROL HTML-Konverter]** und klicken Sie auf **[!UICONTROL Konvertieren]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > Einen `<table>`-Tag als erste Ebene in einer HTML-Datei zu verwenden kann zum Verlust des Stils führen, einschließlich der Einstellungen für Hintergrund und Breite im Tag der obersten Ebene.

1. Jetzt können Sie Ihre importierte Datei nach Bedarf mit den Funktionen des E-Mail-Designers personalisieren. [Weitere Informationen](content-from-scratch.md)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie vorhandene HTML-Inhalte importieren, das Design anpassen, Mirrorseiten- und Abmelde-Links hinzufügen und Ihre Inhalte codieren können.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
