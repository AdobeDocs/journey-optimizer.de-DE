---
solution: Journey Optimizer
product: journey optimizer
title: Senden einer Nachricht an Abonnentinnen und Abonnenten
description: Hier erfahren Sie, wie Sie eine Journey erstellen, um eine Nachricht an die Abonnenten auf einer Liste zu senden.
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: Journey, Anwendungsfall, Nachricht, Abonnenten, Liste, Lesen
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sDhncesYlIjsj2zjB-QmjWqP--0KDyp-5x5-UGLSjRc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 92%

---

# Senden einer Nachricht an Abonnenten auf einer Liste {#send-a-message-to-the-subscribers-of-a-list}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine Journey erstellen, die eine Nachricht an die Abonnenten auf einer Liste mithilfe der Feldergruppe Einverständnis und Voreinstellungsdetails sendet.

>[!ENDSHADEBOX]

In diesem Anwendungsbeispiel soll eine Journey erstellt werden, um eine Nachricht an die Abonnenten auf einer Liste zu senden.

In diesem Beispiel wird die Feldergruppe **[!UICONTROL Einverständnis und Präferenzdetails]** aus [!DNL Adobe Experience Platform] verwendet. Um diese Feldergruppe zu finden, wählen Sie im Menü **[!UICONTROL Daten-Management]** die Option **[!UICONTROL Schemata]**. Geben Sie auf der Registerkarte **[!UICONTROL Feldergruppen]** im Suchfeld den Namen der Feldergruppe ein.

![Diese Feldergruppe enthält das Abonnement-Element &#x200B;](assets/consent-and-preference-details-field-group.png)

Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey, die mit der Aktivität **[!UICONTROL Lesen]** beginnt. Weitere Informationen finden Sie unter [Erstellen der ersten Journey](journey-gs.md).
1. Fügen Sie der Journey die Aktionsaktivität **[!UICONTROL E-Mail]** hinzu. Weitere Informationen zum [Arbeiten mit Kanalaktivitäten](journey-action.md).
1. Ersetzen Sie im Abschnitt **[!UICONTROL E-Mail-Parameter]** der Aktivitätseinstellungen der **[!UICONTROL E-Mail]** die standardmäßige E-Mail-Adresse (`PersonalEmail.adress`) durch die E-Mail-Adresse der Abonnenten auf der Liste:

   1. Klicken Sie auf das Symbol **[!UICONTROL Parameterüberschreibungen aktivieren]** rechts neben dem Feld **[!UICONTROL Adresse]** und klicken Sie auf das Symbol **[!UICONTROL Bearbeiten]**.

      ![Journey-Fluss mit „Zielgruppe lesen“ für das Targeting bei Abonnentenlisten](assets/message-to-subscribers-uc-1.png)

   1. Geben Sie im Ausdruckseditor den Ausdruck ein, um die E-Mail-Adressen der Abonnenten abzurufen. [Weitere Informationen](expression/expressionadvanced.md).

      Dieses Beispiel zeigt einen Ausdruck, der Verweise auf Zuordnungsfelder enthält:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In diesem Beispiel werden die folgenden Funktionen verwendet:

      | Funktion | Beschreibung | Beispiel |
      | --- | --- | --- |
      | `entry` | Verweist auf ein Zuordnungselement entsprechend dem ausgewählten Namespace | Verweis auf eine spezifische Abonnement-Liste |
      | `firstEntryKey` | Ruft den ersten Eintragsschlüssel einer Zuordnung ab | Abrufen der ersten E-Mail-Adresse der Abonnenten |

      In diesem Beispiel erhält die Abonnement-Liste den Namen `daily-email`. E-Mail-Adressen werden als Schlüssel in der Zuordnung `subscribers` definiert, die mit der Zuordnung der Abonnement-Liste verknüpft ist.

      Lesen Sie mehr über [Verweise auf Felder](expression/field-references.md) in Ausdrücken.

      ![E-Mail-Konfiguration mit personalisierten Inhalten für Abonnentinnen und Abonnenten](assets/message-to-subscribers-uc-2.png)

   1. Klicken Sie im Dialogfeld **[!UICONTROL Ausdruck hinzufügen]** auf **[!UICONTROL OK]**.

>[!CAUTION]
>
>Das Überschreiben von E-Mail-Adressen sollte nur für bestimmte Anwendungsfälle verwendet werden. Meistens müssen Sie die E-Mail-Adresse nicht ändern, da der Wert, der als die primäre Adresse in den **[!UICONTROL Ausführungsfeldern]** definiert ist, derjenige ist, der verwendet werden sollte. [Weitere Informationen](../configuration/primary-email-addresses.md)
