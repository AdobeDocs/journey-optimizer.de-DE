---
solution: Journey Optimizer
product: journey optimizer
title: Benachrichtigen von Benutzenden über Produktverfügbarkeit
description: Benachrichtigen von Benutzenden über Produktverfügbarkeit
feature: Use Cases
version: Campaign Orchestration
exl-id: a3b5ff92-fe26-41ad-ad12-b346025e9e0f
TQID: https://experienceleague.adobe.com/OOuzKAv-SCDhIxYSdrrQhtBI8jM4VevcpNj2z0pLUuQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: d2249f211bab8b5416b2d3e036181ccc9a629305
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 100%

---

# Benachrichtigen von Benutzenden über Produktverfügbarkeit {#product-availability-uc}

>[!BEGINSHADEBOX]

Dieser Anwendungsfall zeigt den mehrstufigen Versand: Für jedes Wunschlistenelement wird eine eigene E-Mail generiert, indem die mit dem einzelnen Element gespeicherte E-Mail-Adresse verwendet wird und nicht die mit dem Empfängereintrag gespeicherte. Dadurch können Kundinnen und Kunden für jedes Produkt auf ihrer Wunschliste separate Benachrichtigungen erhalten, auch wenn sie für verschiedene Artikel unterschiedliche E-Mail-Adressen verwenden.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Erstellen Sie eine Benachrichtigung zu Aktualisierungen des Bestands, um Kundinnen und Kunden zu informieren, wenn Artikel von ihrer Wunschliste wieder verfügbar sind. Diese Nachricht hilft dabei, interessierte Kundinnen und Kunden zurückzugewinnen, und ermutigt sie, ihren Kauf abzuschließen, während der Bestand wieder aufgefüllt wird.

1. Richten Sie zunächst eine neue Kampagne ein, die speziell auf die Rückgewinnung basierend auf Wunschlisten ausgerichtet ist. Dadurch wird sichergestellt, dass sich Ihre Werbebotschaft auf Kundschaft konzentriert, die bereits ihre Kaufabsicht gezeigt hat, indem sie Produkte auf ihrer Wunschliste gespeichert hat.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Geben Sie Ihre **[!UICONTROL Kampagneneinstellungen]** wie den Kampagnennamen, die Beschreibung, das Start- und Enddatum und relevante Tags ein.

1. Fügen Sie die Aktivität **[!UICONTROL Zielgruppe erstellen]** mit „Wunschliste“ als **[!UICONTROL Zielgruppendimension]** hinzu.

   ![](assets/notify-1.png){zoomable="yes"}

1. Fügen Sie Ihre Bedingung hinzu, um nur Wunschlisten einzuschließen, die in den letzten 36 Monaten erstellt wurden.

   ![](assets/notify-2.png){zoomable="yes"}

1. Fügen Sie eine Aktivität des Typs **[!UICONTROL Dimensionsänderung]** hinzu, um von Wunschlisten zurück zum entsprechenden Kundensatz für das Targeting zu wechseln.

   ![](assets/notify-3.png){zoomable="yes"}

1. Nach dem Starten des Entwurfsmodus können Sie eine Vorschau der Zielgruppe mit Details zur Wunschliste anzeigen. Um detaillierter Erkenntnisse zu erhalten, klicken Sie auf ein Ausgabeergebnis und wählen Sie **[!UICONTROL Vorschau der Ergebnisse]** aus.

   Hier zeigen die Daten sowohl Empfangende als auch deren Wunschlistenelemente an. Einige Kundinnen und Kunden verfügen über mehrere Wunschlistenelemente und erhalten durch mehrstufigen Versand für jeden Artikel eine separate E-Mail. In einigen Fällen verwenden Kundinnen und Kunden unterschiedliche E-Mail-Adressen für separate Anfragen zur Verfügbarkeit von Produkten.

   ![](assets/notify-4.png){zoomable="yes"}

1. Um für jedes Element eine separate E-Mail senden zu können, stellen Sie sicher, dass für [Ihre E-Mail-Konfiguration](../orchestrated/target-dimension.md) `Recipients - email` als **[!UICONTROL Profilzieldimension]** und `Wishlistitems` als **[!UICONTROL Sekundäre Dimension]** festgelegt ist.

   Wählen Sie dann im Menü **[!UICONTROL Ausführungsadresse]** die Option `wishlist.email` als **[!UICONTROL Sekundäre Dimension]** aus. Für jeden Artikel auf der Wunschliste wird eine separate E-Mail ausgelöst, wobei die in den Wunschlistendaten gespeicherte E-Mail-Adresse als sekundäre Dimension verwendet wird.

   ![](assets/notify-5.png){zoomable="yes"}

1. Fügen Sie eine **[!UICONTROL E-Mail]**-Aktivität hinzu, um eine Produktverfügbarkeitsnachricht zu erstellen. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**, um mit der Inhaltserstellung zu beginnen.

   ➡️ [Weitere Informationen zu E-Mail-Personalisierung](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Sobald Ihre Kampagne getestet wurde und bereit ist, klicken Sie auf **[!UICONTROL Veröffentlichen]**, um sie live zu schalten.

Mit dieser orchestrierten Kampagne erhält die Kundin bzw. der Kunde eine separate E-Mail für jedes Wunschlistenelement. Jede Nachricht wird an die spezifische E-Mail-Adresse gesendet, die mit dieser Wunschliste verknüpft ist, wobei der personalisierte Inhalt aus den Details dieses bestimmten Wunschlistenelements abgerufen wird.
