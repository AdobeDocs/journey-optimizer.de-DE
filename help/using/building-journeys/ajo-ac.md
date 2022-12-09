---
solution: Journey Optimizer
product: journey optimizer
title: Nachricht mit Campaign v7/v8 senden
description: Erfahren Sie, wie Sie eine Nachricht mit Campaign v7/v8 senden.
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Anwendungsfall: Versand einer Nachricht mit Campaign v7/v8 {#campaign-classic-use-case}

In diesem Anwendungsbeispiel werden alle Schritte vorgestellt, die zum Senden einer E-Mail mithilfe der Integration mit Adobe Campaign Classic v7 und Adobe Campaign v8 erforderlich sind.

Zunächst wird in Campaign eine Transaktions-E-Mail-Vorlage erstellt. Anschließend erstellen wir in Journey Optimizer das Ereignis, die Aktion und entwerfen die Journey.

Weiterführende Informationen zur Campaign-Integration finden Sie auf diesen Seiten:

* [Erstellen einer Kampagnenaktion](../action/acc-action.md)
* [Verwenden der Aktion in einer Journey](../building-journeys/using-adobe-campaign-classic.md).

**Adobe Campaign**

Ihre Campaign-Instanz muss für diese Integration bereitgestellt werden. Die Funktion für Transaktionsnachrichten muss konfiguriert werden.

1. Melden Sie sich bei Ihrer Campaign-Kontrollinstanz an.

1. under **Administration** > **Plattform** > **Auflistungen**, wählen Sie die **Ereignistyp** (eventType)-Auflistung. Erstellen Sie einen neuen Ereignistyp (&quot;journey-event&quot;, in unserem Beispiel). Sie müssen den internen Namen des Ereignistyps beim späteren Schreiben der JSON-Datei verwenden.

   ![](assets/accintegration-uc-1.png)

1. Trennen Sie die Verbindung zur Instanz und verbinden Sie sie erneut, damit die Erstellung wirksam ist.

1. under **Message Center** > **Transaktionsnachrichten-Vorlagen** erstellen Sie eine neue E-Mail-Vorlage basierend auf dem zuvor erstellten Ereignistyp.

   ![](assets/accintegration-uc-2.png)

1. Entwerfen Sie Ihre Vorlage. In diesem Beispiel verwenden wir eine Personalisierung für den Vornamen und die Bestellnummer des Profils. Der Vorname befindet sich in der Adobe Experience Platform-Datenquelle und die Bestellnummer ist ein Feld aus unserem Journey Optimizer-Ereignis. Stellen Sie sicher, dass Sie die richtigen Feldnamen in Campaign verwenden.

   ![](assets/accintegration-uc-3.png)

1. Veröffentlichen Sie Ihre Transaktionsvorlage.

   ![](assets/accintegration-uc-4.png)

1. Jetzt müssen Sie die JSON-Payload schreiben, die der Vorlage entspricht.

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

* Geben Sie für den Kanal &quot;email&quot;ein.
* Verwenden Sie für eventType den internen Namen des zuvor erstellten Ereignistyps.
* Die E-Mail-Adresse ist eine Variable, sodass Sie einen beliebigen Titel eingeben können.
* Unter ctx sind die Personalisierungsfelder auch Variablen.

**Journey Optimizer**

1. Zunächst müssen Sie ein Ereignis erstellen. Stellen Sie sicher, dass Sie das Feld &quot;purchaseOrderNumber&quot;einschließen.

   ![](assets/accintegration-uc-5.png)

1. Anschließend müssen Sie in Journey Optimizer eine Aktion erstellen, die Ihrer Campaign-Vorlage entspricht. Im **Aktionstyp** Dropdown-Liste auswählen **Adobe Campaign Classic**.

   ![](assets/accintegration-uc-6.png)

1. Klicken Sie auf **Payload-Feld** und fügen Sie die zuvor erstellte JSON ein.

   ![](assets/accintegration-uc-7.png)

1. Ändern Sie für die E-Mail-Adresse und die beiden Personalisierungsfelder **Konstante** nach **Variable**.

   ![](assets/accintegration-uc-8.png)

1. Erstellen Sie jetzt eine neue Journey und beginnen Sie mit dem zuvor erstellten Ereignis.

   ![](assets/accintegration-uc-9.png)

1. Fügen Sie die Aktion hinzu und ordnen Sie jedes Feld dem richtigen Feld in Journey Optimizer zu.

   ![](assets/accintegration-uc-10.png)

1. Testen Sie Ihre Journey.

   ![](assets/accintegration-uc-11.png)

1. Sie können Ihre Journey jetzt veröffentlichen.
