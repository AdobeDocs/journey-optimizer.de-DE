---
solution: Journey Optimizer
product: journey optimizer
title: Nachricht an Abonnenten senden
description: Erfahren Sie, wie Sie eine Journey erstellen, um eine Nachricht an die Abonnenten einer Liste zu senden.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Anwendungsfall: eine Nachricht an die Abonnenten einer Liste senden{#send-a-message-to-the-subscribers-of-a-list}

In diesem Anwendungsbeispiel wird eine Journey erstellt, um eine Nachricht an die Abonnenten einer Liste zu senden.

In diesem Beispiel wird die **[!UICONTROL Consent and Preference Details]** Feldergruppe aus [!DNL Adobe Experience Platform] verwendet. Um diese Feldergruppe zu finden, verwenden Sie die **[!UICONTROL Data Management]** Menü, wählen **[!UICONTROL Schemas]**. Im **[!UICONTROL Field groups]** den Namen der Feldergruppe im Suchfeld ein.

![Diese Feldergruppe enthält das Abonnement-Element](assets/consent-and-preference-details-field-group.png)

Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen einer Journey, die mit einer **[!UICONTROL Read]** Aktivität. [Mehr dazu](journey-gs.md).
1. Hinzufügen einer **[!UICONTROL Email]** Aktionsaktivität zur Journey. [Mehr dazu](journeys-message.md).
1. Im **[!UICONTROL Email parameters]** Abschnitt **[!UICONTROL Email]** Aktivitätseinstellungen ersetzen die standardmäßige E-Mail-Adresse (`PersonalEmail.adress`) mit der E-Mail-Adresse der Abonnenten der Liste:

   1. Klicken Sie auf **[!UICONTROL Enable parameter override]** rechts neben dem **[!UICONTROL Address]** und klicken Sie auf das **[!UICONTROL Edit]** Symbol.

      ![](assets/message-to-subscribers-uc-1.png)

   1. Geben Sie im Ausdruckseditor den Ausdruck ein, um die E-Mail-Adressen der Abonnenten abzurufen. [Mehr dazu](expression/expressionadvanced.md).

      Dieses Beispiel zeigt einen Ausdruck, der Verweise auf Zuordnungsfelder enthält:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In diesem Beispiel werden diese Funktionen verwendet:

      | Funktion | Beschreibung | Beispiel |
      | --- | --- | --- |
      | `entry` | Siehe Element Zuordnung entsprechend dem ausgewählten Namespace . | Spezifische Abonnementlisten |
      | `firstEntryKey` | Abrufen des ersten Eintragsschlüssels einer Zuordnung | Erste E-Mail-Adresse der Abonnenten abrufen |

      In diesem Beispiel erhält die Abonnementliste den Namen `daily-email`. E-Mail-Adressen werden als Schlüssel im `subscribers` -Karte, die mit der Abonnementlisten-Karte verknüpft ist.

      Mehr dazu [Verweise auf Felder](expression/field-references.md) in Ausdrücken.

      ![](assets/message-to-subscribers-uc-2.png)

   1. Im **[!UICONTROL Add an expression]** Dialogfeld, klicken Sie auf **[!UICONTROL Ok]**.
