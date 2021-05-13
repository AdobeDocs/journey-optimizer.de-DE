---
title: Konfiguration der Push-Benachrichtigung
description: Erfahren Sie, wie Sie Ihre Umgebung so konfigurieren, dass Push-Benachrichtigungen mit Journey Optimizer gesendet werden
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 1%

---

# Push-Benachrichtigungskonfiguration {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## Erste Schritte mit der Push-Konfiguration {#gs-push}

Bevor Sie mit dem Senden von Push-Benachrichtigungen mit [!DNL Journey Optimizer] beginnen, müssen Sie die Einstellungen in [!DNL Adobe Experience Platform] und [!DNL Adobe Experience Platform Launch] definieren.

## Adobe Experience Platform-Einstellungen {#platform-settings}

Gehen Sie wie folgt vor, um Ihre mobile App in [!DNL Adobe Experience Platform Launch] einzurichten:

1. [Rechte für Eigenschaft und Firma zuweisen](#push-rights)
1. [hinzufügen Sie die Push-Anmeldeinformationen Ihrer mobilen Anwendung in Platform launch](#push-credentials-launch).
1. [Erstellen Sie eine Edge-](#edge-configuration) Konfiguration, die von  **** Edgeextension verwendet wird, um benutzerdefinierte Daten von einem Mobilgerät an zu senden  [!DNL Adobe Experience Platform].
1. [Richten Sie eine Platform launch-Eigenschaft](#launch-property) ein.
1. [Veröffentlichen Sie die Eigenschaft](#publish-property).
1. [Konfigurieren Sie ProfileDataSource](#configure-profiledatasource).

### Schritt 1: Zuweisen von Eigenschaften- und Firmen-Rechten {#push-rights}

Bevor Sie eine Mobilanwendung erstellen, müssen Sie zunächst sicherstellen, dass Sie über die richtigen Benutzerberechtigungen verfügen oder diese zuweisen.

Weitere Informationen zur Benutzerverwaltung mit [!DNL Adobe Experience Platform Launch] finden Sie in der [Platform launch-Dokumentation](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions).

So weisen Sie Eigenschaften- und Firmen-Rechte zu:

1. Greifen Sie auf [!DNL Admin Console] zu.

1. Wählen Sie auf der Registerkarte **[!UICONTROL Produkte]** die Karte **[!UICONTROL Adobe Experience Platform Launch]** aus.

   ![](assets/push_product_1.png)

1. Wählen Sie ein vorhandenes **[!UICONTROL Profil]** oder erstellen Sie ein neues mit der Schaltfläche **[!UICONTROL Neues Profil]**. Weitere Informationen zum Erstellen eines neuen **[!UICONTROL neuen Profils]** finden Sie in der [Admin-Konsolendokumentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui).

1. Wählen Sie auf der Registerkarte **[!UICONTROL Berechtigungen]** **[!UICONTROL Eigenschaftsrechte]**.

   ![](assets/push_product_2.png)

1. Klicken Sie auf **[!UICONTROL Hinzufügen alle]**. Dadurch werden Ihrem Produkt-Profil die folgenden Rechte hinzugefügt:
   * **[!UICONTROL Genehmigen]**
   * **[!UICONTROL Entwickeln]**
   * **[!UICONTROL Umgebung verwalten]**
   * **[!UICONTROL Erweiterungen verwalten]**
   * **[!UICONTROL Veröffentlichen Sie]**

   ![](assets/push_product_3.png)

1. Wählen Sie dann **[!UICONTROL Firma rights]** im Menü links.

   ![](assets/push_product_4.png)

1. hinzufügen die folgenden Rechte:

   * **[!UICONTROL App-Konfigurationen verwalten]**
   * **[!UICONTROL Eigenschaften verwalten]**

   ![](assets/push_product_5.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

So weisen Sie Benutzern dieses **[!UICONTROL Produkt-Profil]** zu:

1. Wählen Sie in der Registerkarte [!DNL Admin Console] auf der Registerkarte **[!UICONTROL Produkte]** die Karte **[!UICONTROL Adobe Experience Platform Launch]**.

1. Wählen Sie Ihr zuvor konfiguriertes **[!UICONTROL Produkt-Profil]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Hinzufügen Benutzer]**.

   ![](assets/push_product_6.png)

1. Geben Sie den Namen oder die E-Mail-Adresse Ihres Benutzers ein und wählen Sie den Benutzer aus. Klicken Sie dann auf **[!UICONTROL Speichern]**.

   >[!NOTE]
   >
   >Wenn der Benutzer noch nicht in der Admin-Konsole erstellt wurde, lesen Sie die [Hinzufügen Benutzerdokumentation](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


Sie haben jetzt die richtigen Benutzerberechtigungen, um eine Mobilanwendung in [!DNL Adobe Experience Platform Launch] zu erstellen und zu konfigurieren.

### Schritt 2: hinzufügen Sie Ihre Push-Anmeldeinformationen für die Mobilanwendung in Platform launch {#push-credentials-launch}

>[!NOTE]
>
> Um Push-Anmeldeinformationen in [!DNL Adobe Experience Platform Launch] hinzuzufügen, sollte der Inhaber der mobilen App sie von APNs/FCM abrufen.

1. Vergewissern Sie sich, dass unter [!DNL Adobe Experience Platform Launch] **[!UICONTROL Clientseite]** im Dropdown-Menü ausgewählt ist.

1. Wählen Sie im linken Bereich die Registerkarte **[!UICONTROL App-Konfigurationen]** und klicken Sie auf **[!UICONTROL App-Konfiguration]**, um eine neue Konfiguration zu erstellen.

1. Geben Sie einen **[!UICONTROL Name]** für die Konfiguration ein.

1. Wählen Sie im Dropdownmenü **[!UICONTROL Messaging-Diensttyp]** den **[!UICONTROL Messaging-Diensttyp]** aus, der für diese Anmeldeinformationen verwendet werden soll. Hier haben wir **[!UICONTROL Apple Push Notification Service]** ausgewählt, da wir mit iOS arbeiten.

1. Geben Sie die mobile App **[!UICONTROL Bündel-ID]** in das Feld **[!UICONTROL App-ID (iOS-Bündel-ID)]** ein, wenn Sie den Apple-Push-Benachrichtigungsdienst verwenden, oder im Feld **[!UICONTROL App-ID (Android-Paketname)]**, wenn Sie Firebase Cloud Messaging verwenden.

   ![](assets/push_launch_app_configuration.png)

1. Ziehen Sie die .p8-Schlüsseldatei oder die .json-Datei mit privatem Schlüssel in das Feld **[!UICONTROL Push Credentials]**.

1. Geben Sie die **[!UICONTROL Key-ID]** und **[!UICONTROL Team-ID]** ein, wenn Sie den Apple-Push-Benachrichtigungsdienst verwenden.

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre App-Konfiguration zu erstellen.

### Schritt 3: Edge-Konfiguration erstellen {#edge-configuration}

**[!UICONTROL Die Edge-]** Konfiguration wird von  **** Edgeextension verwendet, um benutzerdefinierte Daten von einem Mobilgerät an zu senden  [!DNL Adobe Experience Platform].
Zum Konfigurieren von [!DNL Adobe Experience Platform] müssen Sie den Namen **[!UICONTROL Sandbox]** und den **[!UICONTROL Ereignis-Datensatz]** angeben.

1. Wählen Sie in [!DNL Adobe Experience Platform Launch] die Registerkarte **[!UICONTROL Edge Configurations]** und klicken Sie auf **[!UICONTROL Edge Configurations]**.

1. Wählen Sie **[!UICONTROL Neue Edge-Konfiguration]** aus, um eine neue **[!UICONTROL Edge-Konfiguration]** hinzuzufügen.
1. Geben Sie einen **[!UICONTROL Namen]** ein und klicken Sie auf **[!UICONTROL Speichern]**

1. Klicken Sie auf den Umschalter **[!UICONTROL Adobe Experience Platform]**, um ihn zu aktivieren.

1. Füllen Sie die Felder **[!UICONTROL Sandbox]**, **[!UICONTROL Ereignis-Datensatz]** und **[!UICONTROL Profil-Datensatz]** aus. Klicken Sie dann auf **[!UICONTROL Speichern]**.

   ![](assets/push-config-4.png)

### Schritt 4: Einrichten der Platform launch-Eigenschaft {#launch-property}

Durch das Einrichten einer [!DNL Adobe Experience Platform Launch]-Eigenschaft kann der Entwickler oder Vermarkter der mobilen App die Attribute der SDKs wie Sitzungszeitlimits, die [!DNL Adobe Experience Platform]-Sandbox, die als Ziel dienen sollen, und die **[!UICONTROL Adobe Experience Platform-Datensätze]**, die für das mobile SDK zum Senden von Daten an verwendet werden sollen, konfigurieren.

1. Vergewissern Sie sich, dass unter [!DNL Adobe Experience Platform Launch] **[!UICONTROL Clientseite]** im Dropdown-Menü ausgewählt ist.

1. Wählen Sie die Registerkarte **[!UICONTROL Eigenschaften]** und klicken Sie auf **[!UICONTROL Neue Eigenschaft]**.

   ![](assets/push-config-6.png)

1. Geben Sie eine **[!UICONTROL Name]** für Ihre neue Eigenschaft ein.

1. Wählen Sie **[!UICONTROL Mobil]** als **[!UICONTROL Plattform]**.

   ![](assets/push-config-7.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um Ihre neue Eigenschaft zu erstellen.

Damit die SDKs, die für die Push-Benachrichtigung benötigt werden, funktionieren, benötigen Sie die folgenden SDK-Erweiterungen für Android und iOS:

* **[!UICONTROL Mobile Core]**  (wird automatisch installiert)
* **[!UICONTROL Profil]**  (wird automatisch installiert)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optional, wird aber zum Debuggen der Implementierung für Mobilgeräte empfohlen.

Weitere Informationen zu [!DNL Adobe Experience Platform Launch] Erweiterungen finden Sie in der [Platform launch-Dokumentation](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).

So konfigurieren Sie die Adobe Experience Platform Edge Extension ]**, um benutzerdefinierte Daten von Mobilgeräten an [!DNL Adobe Experience Platform] zu senden.**[!UICONTROL 

1. Wählen Sie die zuvor erstellte Eigenschaft aus und klicken Sie auf die Registerkarte **[!UICONTROL Erweiterungen]**, um die Erweiterungen für diese Eigenschaft Ansicht.

   ![](assets/push-config-8.png)

1. Klicken Sie unter der Erweiterung **[!UICONTROL Adobe Experience Platform Edge]** auf ]**konfigurieren.**[!UICONTROL 

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Edge Configuration]** die **[!UICONTROL Edge Configuration]** aus, die Sie in den vorherigen Schritten erstellt haben. Weitere Informationen zu **[!UICONTROL Edge Configuration]** finden Sie in diesem [Abschnitt](#edge-configuration).

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Gehen Sie wie oben beschrieben vor, um die Erweiterung **[!UICONTROL Adobe Experience Platform Messaging]** so zu konfigurieren, dass Push-Profile und Push-Interaktionen an die richtigen Datensätze gesendet werden. Verwenden Sie **[!UICONTROL Sandbox]**, **[!UICONTROL Ereignis-Datensatz]** und **[!UICONTROL Profil-Datensatz]**, der im [Adobe Experience Platform-Setup](#edge-configuration) erstellt wurde.

### Schritt 5: Eigenschaft {#publish-property} veröffentlichen

Sie müssen die Eigenschaft jetzt veröffentlichen, um Ihre Konfiguration zu integrieren und sie in der mobilen App zu verwenden.
Informationen zum Veröffentlichen Ihrer Eigenschaft finden Sie in den Schritten unter [Adobe Experience Platform Mobile SDK-Dokumentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

### Schritt 6: ProfileDataSource {#configure-profiledatasource} konfigurieren

Um `ProfileDataSource` zu konfigurieren, verwenden Sie das `ProfileDCInletURL`-Setup von [!DNL Adobe Experience Platform] und fügen Sie Folgendes in der mobilen App hinzu:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->
