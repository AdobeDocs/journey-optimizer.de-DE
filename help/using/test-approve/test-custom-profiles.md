---
solution: Journey Optimizer
product: journey optimizer
title: Testen des Inhalts mit Beispielprofilen
description: Erfahren Sie, wie Sie mit Beispielprofilen eine Vorschau von E-Mail-Inhalten anzeigen und Testsendungen durchführen können.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Testen des Inhalts mit Beispielprofilen {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulieren mit Beispielprofilen"
>abstract="In diesem Bildschirm können Sie eine Vorschau des E-Mail-Inhalts anzeigen und Testsendungen durchführen, während Sie die Identität von Beispielprofilen annehmen, die Sie aus einer CSV-Datei hochladen oder manuell direkt über diesen Bildschirm hinzufügen können."


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>Diese Funktionen sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar.

Mit Journey Optimizer können Sie E-Mail-Inhalte mithilfe von Beispielprofilen in der Vorschau anzeigen und testen, die Sie aus einer CSV-Datei hochladen oder bei der Inhaltsimulation manuell hinzufügen können. Mit dieser Funktion können Sie Beispielprofile auswählen, mit denen Sie eine Vorschau Ihres Inhalts anzeigen und Testsendungen durchführen können. Alle Profilattribute, die in Ihrem Inhalt für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests verwendet werden.

Um auf dieses Erlebnis zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** und wählen Sie **[!UICONTROL Mit CSV(Beta) simulieren]** aus.

![](assets/simulate-sample.png)


Die wichtigsten Schritte zum Testen Ihres Inhalts sind:

1. Fügen Sie bis zu 30 Beispielprofile hinzu, indem Sie entweder eine CSV-Datei hochladen oder manuell einzeln hinzufügen. [Erfahren Sie, wie Sie Beispielprofile hinzufügen](#profiles)
1. Überprüfen Sie die Vorschau Ihres Inhalts mit den hinzugefügten Profilen. [Erfahren Sie, wie Sie eine Vorschau Ihres Inhalts anzeigen](#preview)
1. Senden Sie bis zu 10 Testsendungen an die E-Mail-Adressen, während Sie die gewünschten Beispielprofile imitieren. [Durchführen eines Testversands](#proofs)


## Leitlinien und Einschränkungen {#limitations}

Bevor Sie mit dem Testen Ihres Inhalts mit Beispielprofilen beginnen, sollten Sie die folgenden Limits und Voraussetzungen beachten.

* Derzeit ist das Testen mit Beispielprofilen nur innerhalb von Kampagnen und für den E-Mail-Kanal verfügbar.
* Die folgenden Funktionen sind im aktuellen Erlebnis nicht verfügbar: Inbox Rendering, Spam-Berichte, mehrsprachige Inhalte und Inhaltsexperimente. Um diese Funktionen zu verwenden, wählen Sie in Ihrem Inhalt die Schaltfläche **[!UICONTROL Inhalt simulieren]** aus, um auf die vorherige Benutzeroberfläche zuzugreifen.
* Derzeit werden nur Profilattribute unterstützt. Wenn in Ihrem Inhalt für die Personalisierung kontextbezogene Attribute verwendet werden, können Sie Ihren Inhalt nicht mit diesen Attributen testen.
* Nur die folgenden Datentypen werden bei der Eingabe von Daten für Ihre Beispielprofile unterstützt: Zahl (Ganzzahl und Dezimalzahl), Zeichenfolge, boolescher Wert und Datentyp. Bei allen anderen Datentypen wird ein Fehler angezeigt.

## Beispielprofile hinzufügen {#profiles}

Sie können bis zu 30 Beispielprofile hinzufügen, um Ihren Inhalt entweder mithilfe einer CSV-Datei oder manuell zu testen:

* Um Profile aus einer CSV-Datei hochzuladen, klicken Sie auf den Link **[!UICONTROL Vorlage herunterladen]** , um eine CSV-Dateivorlage abzurufen. Diese Vorlagen enthalten eine Spalte für jedes Profilattribut, das in Ihrem Inhalt zur Personalisierung verwendet wird.

  Füllen Sie die CSV-Datei aus und klicken Sie dann auf die Schaltfläche **[!UICONTROL Beispielprofile hochladen]** , um sie zum Testen Ihres Inhalts zu laden.

* Um ein Profil manuell hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Beispielprofil erstellen]** und geben Sie die Informationen für das Profil ein. Für jedes Profilattribut, das in Ihrem Inhalt für die Personalisierung verwendet wird, wird ein Feld angezeigt.

  ![](assets/simulate-custom-add.png)

Nach Auswahl der Profile wird für jedes Profil auf der linken Bildschirmseite ein Feld angezeigt. Sie können diese Profile verwenden, um Ihre Inhalte in der Vorschau anzuzeigen und Testsendungen durchzuführen.

>[!NOTE]
>
>Die hinzugefügten Beispielprofile dienen nur als Testzwecke für Ihren aktuellen Inhalt. Die werden nicht in Adobe Experience Platform gespeichert, sondern in Ihrer Browser-Benutzersitzung, d. h. sie werden nicht angezeigt, wenn Sie sich abmelden oder von einem anderen Gerät aus arbeiten.

## Vorschau des Inhalts mit Beispielprofilen {#preview}

Um eine Vorschau Ihres Inhalts mit einem der Profile anzuzeigen, wählen Sie das entsprechende Feld aus, um die Inhaltsvorschau im rechten Bereich mit den für dieses Profil eingegebenen Informationen zu aktualisieren.

Sie können ein Feld jederzeit mit der Suchschaltfläche oben rechts entfernen und **[!UICONTROL Entfernen]** auswählen. Um Informationen für ein Profil zu bearbeiten, klicken Sie auf die Suchschaltfläche und wählen Sie **[!UICONTROL Bearbeiten]** aus.

![](assets/simulate-custom-boxes.png)

## Durchführen eines Testversands {#proofs}

Mit Journey Optimizer können Sie Testsendungen an E-Mail-Adressen senden, während Sie die Identität eines oder mehrerer Beispielprofile annehmen, die Sie im Simulationsbildschirm hinzugefügt haben. Gehen Sie dazu wie folgt vor:

1. Vergewissern Sie sich, dass Beispielprofile hinzugefügt wurden, um Ihren Inhalt zu testen, und klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** .

1. Geben Sie im Feld **[!UICONTROL Empfänger]** die E-Mail-Adresse ein, an die Sie den Testversand durchführen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**. Wiederholen Sie den Vorgang, um den Testversand an zusätzliche E-Mail-Adressen zu senden. Sie können bis zu 10 Testversand-Empfänger hinzufügen.

1. Wählen Sie im unteren Bereich des Bildschirms die Beispielprofile aus, die Sie im Testversand stellvertretend agieren möchten. Sie können mehrere Profile auswählen. In diesem Fall enthält die E-Mail so viele Testsendungen wie ausgewählte Profile.

   Wählen Sie für weitere Informationen zu einem Profil den Link **[!UICONTROL Profildetails anzeigen]** aus. Auf diese Weise können Sie die im vorherigen Bildschirm eingegebenen Informationen zu den verschiedenen Profilattributen anzeigen.

   ![](assets/simulate-custom-proofs.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** , um mit dem Versand des Testversands zu beginnen.

Sie können den Versand jederzeit verfolgen, indem Sie im Bildschirm &quot;Inhalt simulieren&quot;auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]** klicken.

![](assets/simulate-custom-sent-proofs.png)
