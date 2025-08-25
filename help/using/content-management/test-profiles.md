---
title: Auswählen von Testprofilen
description: Erfahren Sie, wie Sie Testprofile auswählen, um Inhalte in der Vorschau anzuzeigen und zu testen.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 95a6d032808bc735a27a98dcb61efefa93cf5047
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 100%

---

# Auswählen von Testprofilen {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Verwenden Sie Testprofile, um Ihre Inhalte zu überprüfen"
>abstract="Verwenden Sie Testprofile, um Ihre Inhalte in der Vorschau anzuzeigen und zu testen. Wenn Sie personalisierte Felder hinzugefügt haben, können Sie anhand von Testprofildaten überprüfen, wie diese angezeigt werden."

Testprofile sind zusätzliche Empfangende, die nicht den definierten Targeting-Kriterien entsprechen. [Informationen zum Erstellen von Testprofilen](../audience/creating-test-profiles.md)

Bevor Sie Testprofile zum Testen Ihres Inhalts verwenden, müssen Sie sie zunächst auswählen. Gehen Sie dazu wie folgt vor:

1. Klicken Sie im Bildschirm „Inhalt bearbeiten“ oder im E-Mail-Designer auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** und wählen Sie **[!UICONTROL Inhalt simulieren]** aus.

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

>[!NOTE]
>
>Zusätzlich zu Testprofilen, können Sie mit [!DNL Journey optimizer] auch verschiedene Varianten Ihrer Inhalte testen, indem Sie sie in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Informationen zum Simulieren von Inhaltsvarianten](../test-approve/simulate-sample-input.md)
