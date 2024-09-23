---
solution: Journey Optimizer
product: journey optimizer
title: Testen Sie Ihren Inhalt mit benutzerdefinierten Profilen.
description: Erfahren Sie, wie Sie mithilfe benutzerdefinierter Profile eine Vorschau Ihres Inhalts anzeigen und Testsendungen durchführen können.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 2%

---


# Testen Sie Ihren Inhalt mit benutzerdefinierten Profilen. {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulieren mit benutzerdefinierten Profilen"
>abstract="In diesem Bildschirm können Sie eine Vorschau Ihres Inhalts anzeigen und Testsendungen durchführen, während Sie benutzerdefinierte Profile imitieren, die Sie aus einer CSV-Datei hochladen oder manuell direkt über diesen Bildschirm hinzufügen können."

>[!AVAILABILITY]
>
>Diese Funktionen sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar.
>
>Inbox Rendering- und Spam-Berichte sind im aktuellen Erlebnis nicht verfügbar. Um diese Funktionen zu verwenden, wählen Sie in Ihrem Inhalt die Schaltfläche **[!UICONTROL Inhalt simulieren]** aus, um auf die alte Benutzeroberfläche zuzugreifen.

Mit Journey Optimizer können Sie Ihre Inhalte mithilfe von benutzerdefinierten Profilen in der Vorschau anzeigen und testen, die Sie aus einer CSV-Datei hochladen oder bei der Inhaltsimulation manuell hinzufügen können.

Um auf dieses Erlebnis zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** und wählen Sie **[!UICONTROL Mit CSV(Beta) simulieren]** aus.

In diesem Bildschirm können Sie Profile auswählen, die für die Vorschau Ihres Inhalts und den Versand von Testsendungen verwendet werden sollen. Alle Attribute, die in Ihrem Inhalt für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests verwendet werden.

Die wichtigsten Schritte zum Testen Ihres Inhalts sind:

1. Fügen Sie benutzerdefinierte Profile hinzu, indem Sie entweder eine CSV-Datei hochladen oder manuell einzeln hinzufügen. [Erfahren Sie, wie Sie benutzerdefinierte Profile hinzufügen](#profiles)
1. Überprüfen Sie die Vorschau Ihres Inhalts mit den hinzugefügten Profilen. [Erfahren Sie, wie Sie eine Vorschau Ihres Inhalts anzeigen](#preview)
1. Senden Sie bis zu 10 Testsendungen an die E-Mail-Adressen, während Sie die gewünschten benutzerdefinierten Profile imitieren. [Durchführen eines Testversands](#proofs)


## Hinzufügen benutzerdefinierter Profile {#profiles}

Sie können benutzerdefinierte Profile hinzufügen, um Ihren Inhalt entweder mithilfe einer CSV-Datei oder manuell zu testen:

* Um Profile aus einer CSV-Datei hochzuladen, klicken Sie auf den Link **[!UICONTROL Vorlage herunterladen]** , um eine CSV-Dateivorlage abzurufen. Diese Vorlagen enthalten eine Spalte für jedes Personalisierungsattribut, das in Ihrem Inhalt verwendet wird.

  Füllen Sie die CSV-Datei aus und klicken Sie dann auf die Schaltfläche **[!UICONTROL Beispielprofile hochladen]** , um sie zum Testen Ihres Inhalts zu laden.

* Um ein Profil manuell hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Beispielprofil erstellen]** und geben Sie die Informationen für das Profil ein. Für jedes in Ihrem Inhalt verwendete Personalisierungsattribut wird ein Feld angezeigt.

  ![](assets/simulate-custom-add.png)

Nach Auswahl der Profile wird für jedes Profil auf der linken Bildschirmseite ein Feld angezeigt. Sie können diese Profile verwenden, um Ihre Inhalte in der Vorschau anzuzeigen und Testsendungen durchzuführen.

## Vorschau Ihres Inhalts mit benutzerdefinierten Profilen {#preview}

Um eine Vorschau Ihres Inhalts mit einem der Profile anzuzeigen, wählen Sie das entsprechende Feld aus, um die Inhaltsvorschau im rechten Bereich mit den für dieses Profil eingegebenen Informationen zu aktualisieren.

Sie können ein Feld jederzeit mit der Suchschaltfläche oben rechts entfernen und **[!UICONTROL Entfernen]** auswählen. Um Informationen für ein Profil zu bearbeiten, klicken Sie auf die Suchschaltfläche und wählen Sie **[!UICONTROL Bearbeiten]** aus.

![](assets/simulate-custom-boxes.png)

## Durchführen eines Testversands {#proofs}

Mit Journey Optimizer können Sie Testsendungen an E-Mail-Adressen senden, während Sie die Identität eines oder mehrerer benutzerdefinierter Profile annehmen, die Sie im Simulationsbildschirm hinzugefügt haben. Gehen Sie dazu wie folgt vor:

1. Vergewissern Sie sich, dass benutzerdefinierte Profile hinzugefügt wurden, um Ihren Inhalt zu testen, und klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** .

1. Geben Sie im Feld **[!UICONTROL Empfänger]** die E-Mail-Adresse ein, an die Sie den Testversand durchführen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**. Wiederholen Sie den Vorgang, um den Testversand an zusätzliche E-Mail-Adressen zu senden. Sie können bis zu 10 Testversand-Empfänger hinzufügen.

1. Wählen Sie im unteren Bereich des Bildschirms die benutzerdefinierten Profile aus, die Sie im Testversand stellvertretend agieren möchten. Sie können mehrere Profile auswählen. In diesem Fall enthält die E-Mail so viele Testsendungen wie ausgewählte Profile.

   ![](assets/simulate-custom-proofs.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** , um mit dem Versand des Testversands zu beginnen.

Sie können den Versand jederzeit verfolgen, indem Sie im Bildschirm &quot;Inhalt simulieren&quot;auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]** klicken.

![](assets/simulate-custom-sent-proofs.png)
