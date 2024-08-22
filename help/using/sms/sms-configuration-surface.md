---
solution: Journey Optimizer
product: journey optimizer
title: SMS-Konfiguration konfigurieren
description: Erfahren Sie, wie Sie Ihre SMS-/MMS-Konfiguration so konfigurieren, dass Textnachrichten mit Journey Optimizer gesendet werden
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 51%

---

# SMS/MMS-Konfiguration erstellen {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Bestimmen der Nachrichtenkategorie"
>abstract="Wählen Sie den Typ der Textnachrichten mit dieser Konfiguration aus: Marketing für Werbenachrichten, für die die Zustimmung des Benutzers erforderlich ist, oder Transaktion für nicht kommerzielle Nachrichten, wie z. B. das Zurücksetzen des Kennworts."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=de#sms-opt-out-management" text="Abmeldung von Marketing-Textnachrichten"

Nachdem Ihr SMS-/MMS-Kanal konfiguriert wurde, müssen Sie eine Kanalkonfiguration erstellen, um SMS- und MMS-Nachrichten von **[!DNL Journey Optimizer]** senden zu können.

Gehen Sie wie folgt vor, um eine Kanalkonfiguration zu erstellen:

1. Navigieren Sie in der linken Leiste zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** und wählen Sie **[!UICONTROL Allgemeine Einstellungen]** > **[!UICONTROL Kanalkonfigurationen]** aus. Klicken Sie auf die Schaltfläche **[!UICONTROL Kanalkonfiguration erstellen]** .

   ![](assets/preset-create.png)

1. Geben Sie einen Namen und eine Beschreibung (optional) für die Konfiguration ein und wählen Sie dann den SMS-Kanal aus.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Namen müssen mit einem Buchstaben (A–Z) beginnen. Ein Name darf nur alphanumerische Zeichen enthalten. Sie können auch die Zeichen Unterstrich `_`, Punkt `.` und Bindestrich `-` verwenden.

1. Definieren Sie die **SMS-Einstellungen**.

   ![](assets/sms-surface-settings.png)

   Wählen Sie zunächst den mit der Konfiguration gesendeten **[!UICONTROL SMS-Typ]** aus: **[!UICONTROL Transactional]** oder **[!UICONTROL Marketing]**.

   * Wählen Sie **Marketing** für Werbetextnachrichten aus. Diese Nachrichten erfordern das Einverständnis der Benutzerin bzw. des Benutzers.
   * Wählen Sie **Transaktion** für nicht-kommerzielle Nachrichten, wie z. B. Bestellbestätigungen, Benachrichtigungen beim Zurücksetzen des Kennworts oder Versandinformationen.

   Bei der Erstellung einer SMS/MMS müssen Sie eine gültige Kanalkonfiguration auswählen, die der für Ihre Nachricht ausgewählten Kategorie entspricht.

   >[!CAUTION]
   >
   >**Transaktions**-Nachrichten können auch an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben. Diese Nachrichten können nur in bestimmten Kontexten gesendet werden.

1. Wählen Sie die **[!UICONTROL SMS-Konfiguration]** aus, die mit der Konfiguration verknüpft werden soll.

   Weiterführende Informationen zur Konfiguration Ihrer Umgebung für den Versand von SMS-Nachrichten finden Sie in [diesem Abschnitt](#create-api).

1. Geben Sie die **[!UICONTROL Absendernummer]** ein, die Sie für Ihre Sendungen verwenden möchten.

1. Wählen Sie Ihr **[!UICONTROL SMS-Ausführungsfeld]**, um das mit den Telefonnummern der Profile verbundene **[!UICONTROL Profilattribut]** auszuwählen.

1. Wenn Sie die URL-Verkürzungsfunktion in Ihren SMS-Nachrichten verwenden möchten, wählen Sie ein Element aus der **[!UICONTROL Subdomain]**-Liste aus.

   >[!NOTE]
   >
   >Um eine Subdomain auswählen zu können, müssen Sie zuvor mindestens eine SMS/MMS-Subdomain konfiguriert haben. [Weitere Informationen](sms-subdomains.md)

1. Nachdem alle Parameter konfiguriert wurden, klicken Sie zur Bestätigung auf **[!UICONTROL Senden]**. Sie können die Kanalkonfiguration auch als Entwurf speichern und die Konfiguration später fortsetzen.

   ![](assets/sms-submit-surface.png)

1. Nachdem die Kanalkonfiguration erstellt wurde, wird sie in der Liste mit dem Status **[!UICONTROL Verarbeitung]** angezeigt.

   >[!NOTE]
   >
   >In [diesem Abschnitt](#monitor-channel-surfaces) erfahren Sie mehr über die möglichen Fehlerursachen, wenn die Prüfungen nicht erfolgreich sind.

1. Sobald die Prüfungen erfolgreich sind, erhält die Kanalkonfiguration den Status **[!UICONTROL Aktiv]** . Sie kann nun zum Versand von Nachrichten verwendet werden.

   ![](assets/preset-active.png)

Sie können jetzt mit Journey Optimizer Textnachrichten senden.
