---
solution: Journey Optimizer
product: journey optimizer
title: Entwerfen von E-Mails
description: Erfahren Sie, wie Sie E-Mails gestalten.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: E-Mail, Design, Stock, Assets
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 2762eb74ee4bd1c9dba4f8e542375ab7b4b25290
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 91%

---

# Erste Schritte mit dem E-Mail-Design {#get-started-content-design}

Um auf die E-Mail-Designer zuzugreifen und mit der Gestaltung Ihres E-Mail-Inhalts zu beginnen[ müssen Sie zunächst eine E-Mail ](create-email.md) einer Journey oder Kampagne erstellen.

Anschließend können Sie [!DNL Journey Optimizer]Funktionen zum **von E-Mails** verwenden, um vorhandene Inhalte zu importieren oder von Grund auf responsive E-Mails zu erstellen. [Weitere Informationen](content-from-scratch.md)

E-Mail-Designer bietet Ihnen außerdem folgende Möglichkeiten:

* Nutzen Sie die Möglichkeiten von **Adobe Experience Manager Assets Essentials**, um Ihre E-Mails zu gestalten und um Ihre eigene Asset-Datenbank zu erstellen und verwalten. [Weitere Informationen](../integrations/assets.md)

* Suchen Sie **Adobe Stock-Fotos**, um Ihre Inhalte zu erstellen und Ihr E-Mail-Design zu verbessern. [Weitere Informationen](../integrations/stock.md)

* Verbessern Sie das Kundenerlebnis, indem Sie personalisierte und dynamische Nachrichten auf der Basis ihrer Kundenprofil-Attribute erstellen. Weitere Informationen zu [Personalisierung](../personalization/personalize.md) und [dynamischen Inhalten](../personalization/get-started-dynamic-content.md).

➡️ [Funktion im Video kennenlernen](#video)

## Wichtige Schritte zum Erstellen von E-Mail-Inhalten {#key-steps}

Nachdem Sie eine E-Mail erstellt haben, können Sie mit der Gestaltung Ihres E-Mail-Inhalts beginnen.

1. Verwenden Sie im Konfigurationsbildschirm der Journey oder der Kampagne den Bildschirm **[!UICONTROL Inhalt bearbeiten]**, um auf den E-Mail-Designer zuzugreifen. [Weitere Informationen](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. Wählen Sie zum Gestalten Ihrer E-Mail auf der Startseite des E-Mail-Designers unter den folgenden Optionen:

   * **Entwerfen Sie Ihre E-Mail von Grund auf** über die Benutzeroberfläche des E-Mail-Designers und nutzen Sie Bilder aus [Adobe Experience Manager Assets](../integrations/assets.md). In [diesem Abschnitt](content-from-scratch.md) erfahren Sie, wie Sie E-Mail-Inhalte gestalten.

   * **Codieren oder fügen Sie unbearbeitetes HTML** direkt in den E-Mail-Designer ein. In [diesem Abschnitt](code-content.md) erfahren Sie, wie Sie Ihren Inhalt codieren.

     >[!NOTE]
     >
     >In einer Kampagne können Sie auch die Schaltfläche **[!UICONTROL Code Editor]** im Bildschirm **[!UICONTROL Inhalt bearbeiten]** auswählen. [Weitere Informationen](create-email.md#define-email-content)

   * **Importieren Sie vorhandenen HTML-Inhalt** aus einer Datei oder einem .zip-Ordner. In [diesem Abschnitt](existing-content.md) erfahren Sie, wie Sie E-Mail-Inhalte importieren.

   * **Konvertieren von Bild-Designs in HTML-Vorlagen** mithilfe des KI-gestützten Bild-zu-HTML-Converters. In [diesem Abschnitt](image-to-html.md) erfahren Sie, wie Sie statische Bilder in bearbeitbare E-Mail-Vorlagen transformieren.

   * Wählen Sie aus einer Liste integrierter oder benutzerdefinierter Vorlagen einen **existierenden Inhalt** aus. In [diesem Abschnitt](../email/use-email-templates.md) erfahren Sie, wie Sie mit E-Mail-Vorlagen arbeiten.

   ![](assets/email_designer_create_options.png)

1. Sobald Ihr E-Mail-Inhalt definiert und personalisiert wurde, können Sie Ihren Inhalt zur Validierung oder zur späteren Verwendung exportieren. Klicken Sie auf **[!UICONTROL HTML exportieren]**, um eine ZIP-Datei auf Ihrem Computer zu speichern, die Ihre HTML und Ihre Assets enthält.

   ![](assets/email_designer_export.png)

## Best Practices für das E-Mail-Design {#best-practices}

Beim Senden von E-Mails ist es wichtig zu beachten, dass die Empfängerinnen und Empfänger sie weiterleiten könnten, was manchmal zu Problemen mit dem Rendering der E-Mail führen kann. Dies gilt insbesondere bei der Verwendung von CSS-Klassen, die vom E-Mail-Anbieter, der für die Weiterleitung verwendet wird, möglicherweise nicht unterstützt werden, z. B. wenn Sie die CSS-Klasse „is-desktop-hidden“ verwenden, um ein Bild auf Mobilgeräten auszublenden.

Um diese Rendering-Probleme zu minimieren, empfehlen wir, Ihre E-Mail-Design-Struktur so einfach wie möglich zu halten. Versuchen Sie, ein einzelnes Design zu verwenden, das sowohl für Desktop- als auch für Mobilgeräte gut funktioniert, und vermeiden Sie die Verwendung komplexer CSS-Klassen oder anderer Design-Elemente, die möglicherweise nicht von allen E-Mail-Clients vollständig unterstützt werden. Mithilfe dieser Best Practices können Sie sicherstellen, dass Ihre E-Mails konsistent korrekt gerendert werden, unabhängig davon, wie sie von Empfangenden angezeigt oder weitergeleitet werden.

Best Practices für die Gestaltung von E-Mails finden Sie in der unten stehenden Tabelle:

| Empfohlen | Mit Vorsicht zu verwenden | Nicht empfohlen |
|-|-|-|
| <ul><li><b>Statische, tabellenbasierte Layouts</b> für die Struktur</li> <li><b>HTML-Tabellen und verschachtelte Tabellen</b> für ein konsistentes Layout</li> <li><b>Vorlagenbreiten</b> zwischen 600 px und 800 px </li> <li><b>Einfaches Inline-CSS</b> für die Formatierung </li> <li><b>Web-sichere Schriftarten</b> für universelle Kompatibilität</li> | <ul><li><b>Hintergrundbilder</b> werden auf bestimmten E-Mail-Plattformen möglicherweise nicht angezeigt.</li><li><b>Benutzerdefinierte Web-Schriftarten</b> werden nicht universell unterstützt.</li><li><b>Breites Layout</b> wird auf kleineren Bildschirmen möglicherweise schlecht angezeigt.</li><li><b>Imagemaps</b> bieten eingeschränkte Funktionalität.</li><li><b>Eingebettetes CSS</b> wird manchmal während des E-Mail-Versands entfernt.</li> | <ul><li><b>JavaScript</b> wird in E-Mail-Umgebungen im Allgemeinen nicht unterstützt.</li> <li> <b>`<iframe>`</b>-Tags sind auf den meisten Plattformen blockiert. </li> <li><b>Flash</b> ist veraltet und wird nicht mehr unterstützt.</li> <li><b>Eingebettetes Audio</b> kann oft nicht abgespielt werden.</li> <li><b>Eingebettetes Video</b> ist mit vielen E-Mail-Plattformen nicht kompatibel.</li> <li> <b>Formulare</b> funktionieren in E-Mails nicht.</li> <li> `<div>`-Ebenen können zu Problemen beim Rendern führen.</li> |

>[!NOTE]
>
>Die [EU-Richtlinie zur Barrierefreiheit](https://eur-lex.europa.eu/legal-content/DE/TXT/?uri=CELEX:32019L0882){target="_blank"} legt fest, dass alle digitalen Kommunikationen zugänglich sein sollten. Zusätzlich zu den in diesem Abschnitt aufgeführten Best Practices zum Entwerfen von E-Mails sollten Sie auch die auf [dieser Seite](accessible-content.md) aufgeführten Richtlinien zum Erstellen barrierefreier Inhalte mit dem E-Mail-Designer befolgen.

## Anleitungsvideos {#video}

Erfahren Sie, wie Sie mit dem Nachrichteneditor E-Mail-Inhalte erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)

Erfahren Sie, wie Sie Inhaltsexperimente für A/B-Tests konfigurieren und E-Mail-Inhalte ausprobieren können, um Ihre Geschäftsziele bestmöglich zu erreichen.

>[!VIDEO](https://video.tv.adobe.com/v/3419893)
