---
solution: Journey Optimizer
product: journey optimizer
title: Senden einer Nachricht mit Campaign v7/v8
description: Erfahren Sie, wie Sie mit Campaign v7/v8 eine Nachricht senden.
feature: Journeys, Integrations, Custom Actions, Use Cases
topic: Administration
role: Admin, Developer, User
level: Intermediate, Experienced
keywords: Journey, Nachricht, Kampagne, Integration
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/btOUMO8tgvwLD7kjVdgpj6I6QXRrj1iTD3P8AUrqJFM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 501
ht-degree: 80%

---

# Senden einer Nachricht mit Campaign v7/v8 {#campaign-v7-v8-use-case}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Erfahren Sie, wie Sie eine E-Mail von einer Journey mithilfe der Integration mit Adobe Campaign v7 und v8 senden, einschließlich der Erstellung der Transaktionsvorlage, des Ereignisses und der Aktion.

>[!ENDSHADEBOX]

In diesem Anwendungsbeispiel werden alle Schritte erläutert, die zum Senden einer E-Mail mithilfe der Integration mit [!DNL Adobe Campaign] v7 und [!DNL Adobe Campaign] v8 erforderlich sind.

>[!NOTE]
>
>Um diese Integration verwenden zu können, benötigen Sie Campaign v7/v8 Build 9125 oder höher.

Erstellen Sie zunächst eine Transaktions-E-Mail-Vorlage in Campaign. Erstellen Sie anschließend in Journey Optimizer das Ereignis, die Aktion und die Journey.

Weiterführende Informationen zur Campaign-Integration finden Sie auf diesen Seiten:

* [Erstellen einer Campaign-Aktion](../action/acc-action.md)
* [Verwenden der Aktion in einer Journey](../building-journeys/using-adobe-campaign-v7-v8.md).

**[!DNL Adobe Campaign]**

Die Campaign-Instanz muss für diese Integration bereitgestellt werden. Die Funktion für Transaktionsnachrichten muss konfiguriert sein.

1. Melden Sie sich bei Ihrer Campaign-Kontrollinstanz an.

1. Wählen Sie unter **Administration** > **Platform** > **Aufzählungen** die Aufzählung **Ereignistyp** (eventType) aus. Erstellen Sie einen neuen Ereignistyp (in unserem Beispiel „Journey-Ereignis“). Verwenden Sie später beim Schreiben der JSON-Datei den internen Name des Ereignistyps.

   ![Konfigurieren eines Ereignisses in [!DNL Adobe Journey Optimizer] mit Schema- und Feldauswahl](assets/accintegration-uc-1.png)

1. Trennen Sie die Verbindung zur Instanz und stellen Sie sie erneut her, damit die Erstellung wirksam wird.

1. Erstellen Sie unter **Message Center** > **Transaktionsnachrichten-Vorlagen** eine neue E-Mail-Vorlage basierend auf dem zuvor erstellten Ereignistyp.

   ![Ereigniskonfiguration mit Einstellungen für Namespace und Profilkennungen](assets/accintegration-uc-2.png)

1. Gestalten Sie Ihre Vorlage. In diesem Beispiel wird eine Personalisierung auf den Vornamen und die Bestellnummer des Profils angewendet. Der Vorname befindet sich in der [!DNL Adobe Experience Platform] Datenquelle und die Bestellnummer ist ein Feld aus dem Journey Optimizer-Ereignis. Stellen Sie sicher, dass Sie die richtigen Feldnamen in Campaign verwenden.

   ![Vorschau der Ereignis-Payload mit JSON-Struktur mit Profil- und Ereignisdaten](assets/accintegration-uc-3.png)

1. Veröffentlichen Sie Ihre Transaktionsnachrichtenvorlage.

   ![Schaltfläche „Ereigniskopie“ zum Kopieren der Payload-ID für die API-Integration](assets/accintegration-uc-4.png)

1. Die JSON-Payload muss entsprechend der Vorlage geschrieben werden.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Beim Kanal geben Sie „E-Mail“ ein.
* Verwenden Sie für eventType den internen Namen des zuvor erstellten Ereignistyps.
* Die E-Mail-Adresse ist eine Variable, sodass Sie ein beliebiges Label eingeben können.
* Unter ctx sind die Personalisierungsfelder auch Variablen.

**Journey Optimizer**

1. Erstellen Sie ein Ereignis. Schließen Sie das Feld „purchaseOrderNumber“ ein.

   ![Konfigurationsbildschirm für benutzerdefinierte Aktionen für die [!DNL Adobe Campaign] Classic-Integration](assets/accintegration-uc-5.png)

1. Erstellen Sie eine Aktion in Journey Optimizer, die der Kampagnenvorlage entspricht. Wählen **in der Dropdown** Liste „Aktionstyp“ **[!DNL Adobe Campaign]Classic**.

   ![Auswahl des Aktionstyps mit [!DNL Adobe Campaign] Option Classic](assets/accintegration-uc-6.png)

1. Klicken Sie auf das Feld **Payload** und fügen Sie die zuvor erstellte JSON-Datei ein.

   ![Dropdown-Liste zur Auswahl des Campaign-Kontos für die Integration von Aktionen](assets/accintegration-uc-7.png)

1. Ändern Sie für die E-Mail-Adresse und die beiden Personalisierungsfelder **Konstante** in **Variable**.

   ![Konfiguration der Aktions-Payload mit Feldzuordnung für die Campaign-Integration](assets/accintegration-uc-8.png)

1. Erstellen Sie nun eine neue Journey und beginnen Sie mit dem zuvor erstellten Ereignis.

   ![Journey-Arbeitsfläche mit konfiguriertem Ereignis und konfigurierter Campaign-Aktion](assets/accintegration-uc-9.png)

1. Fügen Sie die Aktion hinzu und ordnen Sie jedes Feld dem richtigen Feld in Journey Optimizer zu.

   ![Zuordnung von Aktionsparametern mit dem Ausdruckseditor für dynamische Werte](assets/accintegration-uc-10.png)

1. Testen Sie Ihre Journey.

   ![Vollständiger Journey-Fluss mit Ausführung von Ereignis-Trigger und Campaign-Aktion](assets/accintegration-uc-11.png)

1. Sie können Ihre Journey jetzt veröffentlichen.
