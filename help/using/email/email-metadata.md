---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen von Metadaten zu E-Mail-Inhalten
description: Erfahren Sie, wie Sie die Lesbarkeit und Barrierefreiheit von E-Mail-Inhalten mit Metadaten in Journey Optimizer verbessern.
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: Preheader, Editor, Zusammenfassung, E-Mail
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
TQID: https://experienceleague.adobe.com/apen1-tlKZ3bnGV9X1RacDk1LXt7sJBQNfTQiaFAyYA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 91%

---

# Hinzufügen von Metadaten zu E-Mail-Inhalten {#email-metadata}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie E-Mail-Metadaten in der E-Mail-Designer festlegen, einschließlich Preheader, Dokumenttitel und Dokumentsprache, um die Lesbarkeit und Zugänglichkeit Ihrer E-Mail-Inhalte zu verbessern.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Definieren eines Preheaders"
>abstract="Ein Preheader ist ein kurzer Zusammenfassungstext, der beim Anzeigen einer E-Mail über einen E-Mail-Client der Betreffzeile folgt. In vielen Fällen bietet er eine kurze Zusammenfassung der E-Mail und besteht normalerweise aus einem Satz."

Beim Entwerfen Ihrer E-Mails können Sie zusätzliche Meta-Attribute für Ihre Inhalte definieren, um die Lesbarkeit und Barrierefreiheit zu verbessern. Mit dem [E-Mail-Designer](get-started-email-design.md) von [!DNL Journey Optimizer] können Sie die folgenden Elemente angeben:

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Preheader]**: Ein Preheader ist ein kurzer zusammenfassender Text, der auf die Betreffzeile folgt, wenn Sie eine E-Mail in Ihrem E-Mail-Client anzeigen. In vielen Fällen bietet er eine kurze Zusammenfassung der E-Mail und besteht normalerweise aus einem Satz.

  >[!NOTE]
  >
  >Preheader werden nicht von allen E-Mail-Clients unterstützt. Wird der Preheader nicht unterstützt, wird er nicht angezeigt.

* **[!UICONTROL Dokumententitel]**: Dieses Feld, das dem Element `<title>` entspricht, enthält beschreibende Informationen zum E-Mail-Inhalt, die normalerweise als QuickInfo angezeigt werden, wenn der Mauszeiger darüber bewegt wird. Es kann Benutzenden mit Beeinträchtigungen durch Bereitstellung von zusätzlichem Kontext helfen und zu einem besseren Verständnis Ihrer Inhalte durch Suchmaschinen beitragen.

* **[!UICONTROL Dokumentensprache]**: Um Barrierefreiheit sicherzustellen, können Sie die Sprache angeben, in der Bildschirmlesehilfen Text und Bilder für Menschen mit Seh- oder Lernbeeinträchtigungen in Sprache oder Blindenschrift konvertieren. Diese Einstellung entspricht dem Attribut `lang` im Element `<html>`.

Gehen Sie wie folgt vor, um diese Einstellungen zu konfigurieren.

1. Fügen Sie im [E-Mail-Designer](content-from-scratch.md) mindestens eine **[!UICONTROL Strukturkomponente]** hinzu, um mit der E-Mail-Gestaltung zu beginnen.

1. Klicken Sie entweder über dem **[!UICONTROL Navigationsbaum]** links oder oben im rechten Bereich auf **[!UICONTROL Hauptteil]**.

   ![](assets/email_body.png)

1. Geben Sie auf der Registerkarte **[!UICONTROL Einstellungen]** Text in die Felder **[!UICONTROL Preheader]**, **[!UICONTROL Dokumententitel]** und/oder **[!UICONTROL Dokumentensprache]** ein.

1. Sie können auch auf das Personalisierungssymbol neben jedem Feld klicken, um den Inhalt anhand von Profilattributen, Zielgruppen, Kontextattributen usw. anzupassen. [Weitere Informationen zur Personalisierung](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre Änderungen zu speichern.