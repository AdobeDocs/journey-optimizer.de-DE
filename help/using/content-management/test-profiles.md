---
title: Auswählen von Testprofilen
description: Erfahren Sie, wie Sie Testprofile auswählen, um Inhalte in der Vorschau anzuzeigen und zu testen.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: ht
source-wordcount: '274'
ht-degree: 100%

---

# Auswählen von Testprofilen {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Verwenden Sie Testprofile, um Ihre Inhalte zu überprüfen"
>abstract="Verwenden Sie Testprofile, um Ihre Inhalte in der Vorschau anzuzeigen und zu testen. Wenn Sie personalisierte Felder hinzugefügt haben, können Sie anhand von Testprofildaten überprüfen, wie diese angezeigt werden."

Vor der Vorschau oder dem Testen Ihres Inhalts müssen Sie zunächst Testprofile auswählen, bei denen es sich um zusätzliche Empfängerinnen und Empfänger handelt, die nicht den definierten Kriterien für die Zielgruppenbestimmung entsprechen. [Hier erfahren Sie, wie Sie Testprofile erstellen](../audience/creating-test-profiles.md)

>[!NOTE]
>
>Zusätzlich zu Testprofilen, können Sie mit [!DNL Journey optimizer] auch verschiedene Varianten Ihrer Inhalte testen, indem Sie sie in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Erfahren Sie, wie Sie Ihren Inhalt mit Beispieleingabedaten testen](../test-approve/simulate-sample-input.md)

Gehen Sie wie folgt vor, um Testprofile auszuwählen:

1. Klicken Sie auf dem Bildschirm „Inhalt bearbeiten“ Ihrer Nachricht oder im E-Mail-Designer auf die Schaltfläche **[!UICONTROL Inhalt simulieren]**.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testprofile verwalten]** und wählen Sie den Namespace aus, der zur Identifizierung von Testprofilen verwendet werden soll, indem Sie auf das Auswahlsymbol **[!UICONTROL Identity-Namespace]** klicken. [Weitere Informationen zu Identity-Namespaces von Adobe Experience Platform](../audience/get-started-identity.md).

   Im folgenden Beispiel verwenden wir den Namespace **E-Mail**.

   ![](../email/assets/previewselect-namespace.png)

1. Verwenden Sie das Suchfeld, um den Namespace zu finden, wählen Sie ihn aus und klicken Sie auf **[!UICONTROL Auswählen]**.

   ![](../email/assets/preview-email-namespace.png)

1. Geben Sie im Feld **[!UICONTROL Identitätswert]** den Wert (hier die E-Mail-Adresse) ein, um das Testprofil zu identifizieren, und klicken Sie auf **[!UICONTROL Profil hinzufügen]**.

   <!--![](assets/preview-identity-value.png)-->

1. Wenn Sie Ihrer Nachricht personalisierten Inhalt hinzugefügt haben, fügen Sie weitere Testprofile hinzu, damit Sie verschiedene Varianten der Nachricht anhand unterschiedlicher Profildaten testen können. Anschließend werden die hinzugefügten Profile unter den ausgewählten Feldern aufgelistet.

   ![](../email/assets/preview-profile-list.png)

   Basierend auf den Personalisierungselementen der Nachricht werden in dieser Liste Daten zu den einzelnen Testprofilen in den entsprechenden Spalten angezeigt.
