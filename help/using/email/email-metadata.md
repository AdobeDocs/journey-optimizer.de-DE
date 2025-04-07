---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen von Metadaten zu Ihrem E-Mail-Inhalt
description: Erfahren Sie, wie Sie die Lesbarkeit und Zugänglichkeit Ihrer E-Mail-Inhalte mit Metadaten in Journey Optimizer verbessern können
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: Preheader, Editor, Zusammenfassung, E-Mail
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
source-git-commit: 50491d039f2baf8c30a6af0c1b59fe9041244ac7
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 24%

---

# Hinzufügen von Metadaten zu Ihrem E-Mail-Inhalt {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Hinzufügen eines Preheaders"
>abstract="Ein Preheader ist ein kurzer Zusammenfassungstext, der beim Anzeigen einer E-Mail über einen E-Mail-Client der Betreffzeile folgt. In vielen Fällen bietet er eine kurze Zusammenfassung der E-Mail und besteht normalerweise aus einem Satz."

Beim Entwerfen Ihrer E-Mails können Sie zur besseren Lesbarkeit und Barrierefreiheit zusätzliche Metaattribute für Ihre Inhalte definieren. Mit [!DNL Journey Optimizer] [E-Mail-Designer](get-started-email-design.md) können Sie die folgenden Elemente angeben:

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Preheader]**: Ein Preheader ist ein kurzer zusammenfassender Text, der unter der Betreffzeile zu sehen ist, wenn Sie eine E-Mail in Ihrem E-Mail-Programm öffnen. In vielen Fällen bietet er eine kurze Zusammenfassung der E-Mail und besteht normalerweise aus einem Satz.

  >[!NOTE]
  >
  >Preheader werden nicht von allen E-Mail-Clients unterstützt. Wird der Preheader nicht unterstützt, wird er nicht angezeigt.

* **[!UICONTROL Dokumenttitel]**: Dieses Feld, das dem `<title>`-Element entspricht, enthält beschreibende Informationen zu Ihrem E-Mail-Inhalt, die normalerweise als QuickInfo beim Zeigen mit der Maus angezeigt werden. Es kann Benutzenden mit Behinderungen helfen, indem es zusätzlichen Kontext bietet, und kann zu einem besseren Verständnis Ihrer Inhalte durch Suchmaschinen beitragen.

* **[!UICONTROL Dokumentsprache]**: Um die Barrierefreiheit zu gewährleisten, können Sie die Sprache angeben, die Bildschirmlesehilfen verwenden werden, um Text und Bilder in Sprache oder Braille zu konvertieren - für Menschen mit Sehbehinderung oder Lernbehinderung. Diese Einstellung entspricht dem `lang` im `<html>`.

Gehen Sie wie folgt vor, um diese Einstellungen zu konfigurieren.

1. Designer Fügen Sie in [E-Mail-](content-from-scratch.md)) mindestens eine **[!UICONTROL Strukturkomponente]** hinzu, um Ihre E-Mail zu entwerfen.

1. Klicken Sie **[!UICONTROL Textkörper]** entweder über den **[!UICONTROL Navigationsbaum]** links oder oben im rechten Bereich.

   ![](assets/email_body.png)

1. Geben Sie auf **[!UICONTROL Registerkarte]** Text in die Felder **[!UICONTROL Preheader]**, **[!UICONTROL Dokumenttitel]** und/oder **[!UICONTROL Dokumentsprache]** ein.

1. Sie können auch auf das Personalisierungssymbol neben jedem Feld klicken, um Ihren Inhalt anhand von Profilattributen, Zielgruppen, kontextuellen Attributen und mehr anzupassen. [Erfahren Sie mehr über Personalisierung](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.