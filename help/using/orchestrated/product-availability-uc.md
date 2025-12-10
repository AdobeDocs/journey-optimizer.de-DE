---
solution: Journey Optimizer
product: journey optimizer
title: Benutzer über Produktverfügbarkeit benachrichtigen
description: Benutzer über Produktverfügbarkeit benachrichtigen
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# Benutzer über Produktverfügbarkeit benachrichtigen {#product-availability-uc}

>[!BEGINSHADEBOX]

Dieser Anwendungsfall zeigt den mehrstufigen Versand: Für jedes Wunschlistenelement wird eine eigene E-Mail generiert, indem die E-Mail-Adresse verwendet wird, die mit dem einzelnen Element und nicht mit dem Empfängerdatensatz gespeichert ist. Dadurch können Kunden für jedes Produkt auf ihrer Wunschliste separate Benachrichtigungen erhalten, auch wenn sie für verschiedene Artikel unterschiedliche E-Mail-Adressen verwenden.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Gestalten Sie eine Benachrichtigung „Auf Lager“, um Kunden zu informieren, wenn Artikel von ihrer Wunschliste wieder verfügbar sind. Diese Nachricht hilft, interessierte Kundinnen und Kunden erneut zu gewinnen, und ermutigt sie, ihren Kauf abzuschließen, während der Bestand wieder aufgefüllt wird.

1. Richten Sie zunächst eine neue Kampagne ein, die speziell auf die Rückgewinnung von Wunschzetteln ausgerichtet ist. Dadurch wird sichergestellt, dass sich Ihre Werbebotschaft auf Kunden konzentriert, die bereits ihre Kaufabsicht gezeigt haben, indem sie Produkte auf ihrer Wunschliste speichern.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Geben Sie Ihre **[!UICONTROL Kampagneneinstellungen]** wie den Kampagnennamen, die Beschreibung, das Start- und Enddatum und relevante Tags ein.

1. Fügen Sie **[!UICONTROL Aktivität „Zielgruppe aufbauen]** mit Wunschliste als **[!UICONTROL Zielgruppendimension]** hinzu.

   ![](assets/notify-1.png){zoomable="yes"}

1. Fügen Sie Ihre Bedingung hinzu, um nur Wunschlisten einzuschließen, die in den letzten 36 Monaten erstellt wurden.

   ![](assets/notify-2.png){zoomable="yes"}

1. Fügen Sie eine Aktivität **[!UICONTROL Dimensionsänderung]** hinzu, um von Wunschlisten zurück zum entsprechenden Kundenset für die Zielgruppenbestimmung zu wechseln.

   ![](assets/notify-3.png){zoomable="yes"}

1. Nach dem Starten des Entwurfsmodus können Sie eine Vorschau der Zielgruppe mit Details auf der Wunschliste anzeigen. Um tiefere Einblicke zu erhalten, klicken Sie auf ein Ausgabeergebnis und wählen Sie **[!UICONTROL Vorschau der Ergebnisse]** aus.

   Hier zeigen die Daten sowohl Empfänger als auch deren Wunschlistenelemente an. Einige Kunden verfügen über mehrere Wunschlistenelemente und erhalten durch mehrstufigen Versand für jeden Artikel eine separate E-Mail. In einigen Fällen verwenden Kundinnen und Kunden unterschiedliche E-Mail-Adressen für separate Anfragen zum Back-in-Stock.

   ![](assets/notify-4.png){zoomable="yes"}

1. Um für jedes Element eine separate E-Mail senden zu können, stellen Sie sicher, dass [Ihre E-Mail](../orchestrated/target-dimension.md)-Konfiguration mit `Recipients - email` als **[!UICONTROL Profilziel-Dimension)]** und `Wishlistitems` als **[!UICONTROL Sekundäre Dimension festgelegt]**.

   Wählen Sie dann im Menü **[!UICONTROL Ausführungsadresse]** die Option `wishlist.email` als **[!UICONTROL Sekundäre Dimension]**. Für jeden Artikel auf der Wunschliste wird eine separate E-Mail Trigger, wobei die in den Wunschlistendaten gespeicherte E-Mail-Adresse als sekundäre Dimension verwendet wird.

   ![](assets/notify-5.png){zoomable="yes"}

1. Fügen Sie eine **[!UICONTROL E-Mail]**-Aktivität hinzu, um eine Produktverfügbarkeitsnachricht zu erstellen. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**, um mit der Erstellung Ihres Inhalts zu beginnen.

   ➡️ [Weitere Informationen zur E-Mail-Personalisierung](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Sobald Ihre Kampagne getestet wurde und bereit ist, klicken Sie auf **[!UICONTROL Veröffentlichen]**, um sie live zu schalten.

Mit dieser orchestrierten Kampagne erhält der Kunde eine separate E-Mail für jedes seiner Wunschlistenelemente. Jede Nachricht wird an die spezifische E-Mail-Adresse gesendet, die mit dieser Wunschliste verknüpft ist, wobei der personalisierte Inhalt aus den Details dieses bestimmten Wunschlistenelements abgerufen wird.

