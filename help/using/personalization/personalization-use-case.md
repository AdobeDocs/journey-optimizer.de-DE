---
title: Anwendungsfall Personalisierung&colon; Bestellstatus-Benachrichtigung
description: Erfahren Sie, wie Sie eine Nachricht mit Profil-, Angebotsentscheidungs- und Kontextinformationen personalisieren..
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 89%

---

# Personalisierung – Anwendungsfall: Benachrichtigung über den Bestellstatus {#personalization-use-case}

In diesem Anwendungsfall erfahren Sie, wie Sie mehrere Personalisierungsarten in einer einzigen Push-Benachrichtigung verwenden. Es werden drei Arten der Personalisierung verwendet:

* **Profil**: Personalisierung von Nachrichten basierend auf einem Profilfeld
* **Angebotsentscheidung**: Personalisierung basierend auf Offer-Decisioning-Variablen
* **Kontext**: Personalisierung basierend auf Kontextdaten aus der Journey

Das Ziel dieses Beispiels ist es, jedes Mal, wenn eine Kundenbestellung aktualisiert wird, ein Ereignis an [!DNL Journey Optimizer] zu senden. Anschließend wird eine Push-Benachrichtigung mit Informationen zur Bestellung und einem personalisierten Angebot an den Kunden gesendet.

Für diesen Anwendungsfall müssen die folgenden Voraussetzungen gegeben sein:

* Konfigurieren eines Bestellereignisses mit Bestellnummer, Status und Artikelnamen. Siehe diesen [Abschnitt](../event/about-events.md).
* Informationen zum Erstellen einer Entscheidung finden Sie in diesem [Abschnitt](../offers/offer-activities/create-offer-activities.md).

## Schritt 1 – Journey erstellen {#create-journey}

1. Klicken Sie auf das Menü **[!UICONTROL Journey]** und erstellen Sie eine neue Journey.

   ![](assets/perso-uc4.png)

1. Fügen Sie Ihr Eintrittsereignis und ein **Push** Aktionsaktivität.

   ![](assets/perso-uc5.png)

1. Konfigurieren und gestalten Sie Ihre Push-Benachrichtigung. Siehe diesen [Abschnitt](../messages/get-started-content.md).

## Schritt 2 – Personalisierung in Profil hinzufügen {#add-perso}

1. Im **Push** Aktivität, klicken Sie auf **Inhalt bearbeiten**.

1. Klicken Sie auf das Feld **Titel**.

   ![](assets/perso-uc2.png)

1. Geben Sie den Betreff ein und fügen Sie eine Personalisierung aus dem Profil hinzu. Verwenden Sie die Suchleiste, um das Feld „Vorname“ des Profils zu finden. Setzen Sie den Cursor im Betrefftext an die Stelle, an der Sie das Personalisierungsfeld einfügen möchten, und klicken Sie auf das Symbol **+**. Klicken Sie auf **Speichern**.

   ![](assets/perso-uc3.png)

## Schritt 3 – Personalisierung für Kontextdaten hinzufügen  {#add-perso-contextual-data}

1. Im **Push** Aktivität, klicken Sie auf **Inhalt bearbeiten** und klicken Sie auf **Titel** -Feld.

   ![](assets/perso-uc9.png)

1. Wählen Sie das Menü **Kontextattribute**. Kontextattribute sind nur verfügbar, wenn eine Journey Kontextdaten an die Nachricht übergeben hat. Klicken Sie auf **Journey Orchestration**. Die folgenden Kontextinformationen werden angezeigt:

   * **Veranstaltungen**: Diese Kategorie enthält alle Felder aus den Ereignissen, die vor der Aktivität Kanalaktion in der Journey platziert wurden.
   * **Journey-Eigenschaften**: die technischen Felder, die sich auf die Journey für ein bestimmtes Profil beziehen, z. B. die Fahrt-ID oder die aufgetretenen spezifischen Fehler. Weitere Informationen finden Sie in der [Dokumentation zu Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Erweitern Sie das Element **Ereignis** und suchen Sie das Feld für die Bestellnummer, das sich auf Ihr Ereignis bezieht. Sie können auch das Suchfeld verwenden. Klicken Sie auf das Symbol **+**, um das Personalisierungsfeld in den Betrefftext einzufügen. Klicken Sie auf **Speichern**.

   ![](assets/perso-uc11.png)

1. Klicken Sie nun auf das Feld **Textkörper**.

   ![](assets/perso-uc12.png)

1. Geben Sie die Nachricht ein und fügen Sie vom Menü **[!UICONTROL Kontextuelle Attribute]** den Bestellartikelnamen und den Bestellstatus ein.

   ![](assets/perso-uc13.png)

1. Wählen Sie aus dem linken Menü **Angebotsentscheidungen**, um eine Offer-Decisioning-Variable einzufügen. Wählen Sie die Platzierung aus und klicken Sie neben der Entscheidung auf das Symbol **+**, um sie dem Textkörper hinzuzufügen.

   ![](assets/perso-uc14.png)

1. Klicken Sie auf „Validieren“, um sicherzustellen, dass keine Fehler auftreten, und klicken Sie auf **Speichern**.

   ![](assets/perso-uc15.png)

## Schritt 4 – Journey testen und veröffentlichen  {#test-publish}

1. Klicken Sie auf die Schaltfläche **Test** und dann auf **Ereignis auslösen**.

   ![](assets/perso-uc17.png)

1. Geben Sie die verschiedenen Werte zum Bestehen des Tests ein. Der Testmodus funktioniert nur mit Testprofilen. Die Profilkennung muss mit einem Testprofil übereinstimmen. Klicken Sie auf **Senden**.

   ![](assets/perso-uc18.png)

   Die Push-Benachrichtigung wird gesendet und auf dem Handy des Testprofils angezeigt.

   ![](assets/perso-uc19.png)

1. Vergewissern Sie sich, dass kein Fehler vorliegt, und veröffentlichen Sie die Journey.
