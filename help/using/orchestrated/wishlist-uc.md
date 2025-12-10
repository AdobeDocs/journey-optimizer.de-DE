---
solution: Journey Optimizer
product: journey optimizer
title: Wunschlisten-Artikelaktualisierungen senden
description: Wunschlisten-Artikelaktualisierungen senden
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# Wunschlisten-Artikelaktualisierungen senden {#wishist-uc}

>[!BEGINSHADEBOX]

In diesem Beispiel wird ein **Wunschliste**-Schema verwendet. Dasselbe Verfahren gilt jedoch für alle Entitäten mit einer Eins-zu-Viele-Beziehung zu **Empfängern** wie **Käufe**, **Abonnements** oder jedem benutzerdefinierten Schema, in dem jedem Empfänger mehrere Datensätze zugeordnet sein können.

**Für diesen Anwendungsfall erforderliche Schemata:**

* **Empfänger**: wird als Zielgruppendimension verwendet
* **WishlistItems**: mit Feldern: `creationDate`, `product`, `Wishlistid`
* **Produkt**: mit Feldern: `description`, `priceref`, `imageurl`
* **AbandonedCarts** (optional): mit Feld: `lastmodified`

➡️ [Erfahren Sie, wie Sie modellbasierte Schemata konfigurieren](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Diese koordinierte Kampagne konzentriert sich auf die erneute Interaktion mit Besuchern, indem sie an Produkte erinnert wird, die auf ihrer Wunschliste gespeichert wurden. Definieren Sie mithilfe der Kampagnenorchestrierung die Audience mit Bedingungen, die auf der Aktivität Wunschliste basieren, und helfen Sie damit, die Besucher zur Konvertierung zurückzubringen.

1. Erstellen Sie zunächst eine neue Kampagne, die speziell auf die Rückgewinnung von Wunschzetteln ausgerichtet ist. Auf diese Weise können Sie die Nachrichten auf Kunden konzentrieren, die ihre Kaufabsicht durch das Speichern von Artikeln gezeigt haben.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Füllen Sie Ihre **Kampagneneinstellungen** aus.

1. Fügen Sie eine Aktivität **[!UICONTROL Zielgruppe aufbauen]** hinzu, um die Kundengruppe zu identifizieren, die basierend auf dem Verhalten auf der Wunschliste angesprochen werden soll.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Legen Sie eine beschreibende **[!UICONTROL Bezeichnung]** für diese Zielgruppe fest und wählen Sie **[!UICONTROL Empfänger]** als **[!UICONTROL Zielgruppendimension]**. Klicken Sie dann **[!UICONTROL Fortfahren]**, um die Zielgruppe zu konfigurieren.

1. Klicken Sie **[!UICONTROL Bedingung hinzufügen]**, um Ihre Audience einzuschränken, indem Sie die folgende Bedingung erstellen:

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
ODER
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Diese Zielgruppe basiert auf Empfängern, die eine Wunschliste haben, Artikel mit Produktbildern enthalten oder innerhalb des definierten Zeitraums einen Warenkorb verlassen haben.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Berechnen]** um die Anzahl der von diesen Bedingungen betroffenen Profile anzuzeigen und **[!UICONTROL Ergebnisse anzeigen]** um Details für jede Bedingung zu überprüfen und zu bestätigen, dass die Zielgruppe Ihrem Zielsegment entspricht.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Fügen Sie eine Aktivität **[!UICONTROL Anreicherung]** hinzu, um die Kampagne mit **Wunschliste** und **Produktinformationen** zu personalisieren.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Anreicherungsdaten hinzufügen]**.

1. Zugriff auf `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Wählen Sie aus, wie die Daten erfasst werden (in diesem Fall **[!UICONTROL Daten erfassen]**, um Details zur Wunschliste für Ihre Audience zu erfassen.

1. Wählen Sie die Anzahl der abzurufenden Zeilen. Standardmäßig werden drei Elemente pro Wunschliste abgerufen. Dies kann jedoch je nach den Erfordernissen der Kampagne angepasst werden, um mehr oder weniger Produkte hervorzuheben.

1. Klicken Sie **[!UICONTROL Attribut hinzufügen]**, um die folgenden drei Attribute zu erstellen:

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Dadurch wird die Nachricht mit detaillierten Produktinformationen angereichert, um Konversionen zu fördern.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Fügen Sie eine E-Mail-Aktivität hinzu, um für jeden Kunden eine individuell personalisierte Nachricht zur erneuten Interaktion zu erstellen. Klicken Sie auf **[!UICONTROL Inhalt bearbeiten]**, um mit der Erstellung Ihres Inhalts zu beginnen.

   ➡️ [Weitere Informationen zur E-Mail-Personalisierung](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Nach Abschluss der E-Mail speichern und führen Sie die Kampagne im Entwurfsmodus aus, indem Sie in **[!UICONTROL orchestrierten Kampagne auf]** Starten“ klicken.

1. Nach dem Starten des Entwurfsmodus können Sie eine Vorschau der Zielgruppe mit Details auf der Wunschliste anzeigen.

   Um tiefere Einblicke zu erhalten, klicken Sie auf ein Ausgabeergebnis und wählen Sie **[!UICONTROL Vorschau der Ergebnisse]** aus.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Nachdem die Kampagne ausgeführt wurde, können wir unsere Berichte lesen, die uns einen robusten Satz von Daten und KPIs über die Leistung unserer Kampagne liefern.

➡️ [Weitere Informationen zum Reporting](../reports/campaign-global-report-cja.md)
