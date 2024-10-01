---
solution: Journey Optimizer
product: journey optimizer
title: Testen von Inhalten mit Beispieleingabedaten
description: Erfahren Sie, wie Sie mit Beispieleingabedaten eine Vorschau von E-Mail-Inhalten anzeigen und Testsendungen durchführen können.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 8%

---


# Testen von Inhalten mit Beispieleingabedaten {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulationen mit Beispieleingaben"
>abstract="Auf diesem Bildschirm können Sie verschiedene Varianten Ihrer E-Mail-Inhalte testen, indem Sie Werte für Personalisierungsfelder über eine CSV-Vorlage bereitstellen (CSV herunterladen) oder die Werte manuell eingeben."

>[!AVAILABILITY]
>
>Diese Funktionen sind derzeit nur ausgewählten Benutzern als Beta-Version verfügbar.

Mit Journey Optimizer können Sie verschiedene Varianten Ihres E-Mail-Inhalts testen, indem Sie eine Vorschau davon anzeigen und Testsendungen mithilfe von Beispieleingabedaten durchführen, die aus einer CSV-Datei hochgeladen oder manuell hinzugefügt wurden. Alle Profilattribute, die in Ihrem Inhalt für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests verwendet werden, um mehrere Varianten zu erstellen.

Um auf dieses Erlebnis zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** und wählen Sie **[!UICONTROL Mit CSV(Beta) simulieren]** aus.

![](assets/simulate-sample.png)

Die wichtigsten Schritte zum Testen Ihres Inhalts sind:

1. Fügen Sie bis zu 30 Varianten mit Beispieleingabedaten hinzu, entweder durch Hochladen einer CSV-Datei oder durch manuelles Hinzufügen von Daten. [Erfahren Sie, wie Sie Varianten hinzufügen](#profiles)
1. Überprüfen Sie die Vorschau Ihres Inhalts mit den verschiedenen Varianten. [Erfahren Sie, wie Sie eine Vorschau Ihres Inhalts anzeigen](#preview)
1. Senden Sie mit den verschiedenen Varianten bis zu 10 Testsendungen an E-Mail-Adressen. [Durchführen eines Testversands](#proofs)


## Leitlinien und Einschränkungen {#limitations}

Bevor Sie mit dem Testen Ihres Inhalts mit Beispieleingabedaten beginnen, sollten Sie die folgenden Limits und Voraussetzungen beachten.

* Derzeit ist der Test mit Beispieleingabedaten nur für den E-Mail-Kanal verfügbar. Auf das Erlebnis kann nicht über die Schaltfläche &quot;Inhalt simulieren&quot;in der E-Mail-Designer zugegriffen werden.
* Die folgenden Funktionen sind im aktuellen Erlebnis nicht verfügbar: Inbox Rendering, Spam-Berichte, mehrsprachige Inhalte und Inhaltsexperimente. Um diese Funktionen zu verwenden, wählen Sie in Ihrem Inhalt die Schaltfläche **[!UICONTROL Inhalt simulieren]** aus, um auf die vorherige Benutzeroberfläche zuzugreifen.
* Derzeit werden nur Profilattribute unterstützt. Wenn in Ihrem Inhalt für die Personalisierung kontextbezogene Attribute verwendet werden, können Sie Ihren Inhalt nicht mit diesen Attributen testen.
* Nur die folgenden Datentypen werden bei der Eingabe von Daten für Ihre Varianten unterstützt: Zahl (Ganzzahl und Dezimalzahl), Zeichenfolge, Boolescher Wert und Datentyp. Bei allen anderen Datentypen wird ein Fehler angezeigt.

## Varianten hinzufügen {#profiles}

Sie können bis zu 30 Varianten hinzufügen, um Ihren Inhalt zu testen, entweder mithilfe einer CSV-Datei oder manuell:

* Um Beispieleingabedaten aus einer CSV-Datei hochzuladen, klicken Sie auf den Link **[!UICONTROL CSV herunterladen]** , um eine CSV-Dateivorlage abzurufen. Diese Vorlagen enthalten eine Spalte für jedes Profilattribut, das in Ihrem Inhalt zur Personalisierung verwendet wird.

  Füllen Sie die CSV-Datei aus und klicken Sie dann auf **[!UICONTROL Eingabedaten hochladen]** , um sie zum Testen Ihres Inhalts zu laden.

* Um eine Variante manuell hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Beispieleingabe erstellen]** und füllen Sie die Beispieleingabe für die Variante aus. Für jedes Profilattribut, das in Ihrem Inhalt für die Personalisierung verwendet wird, wird ein Feld angezeigt.

  ![](assets/simulate-custom-add.png)

Nach Auswahl der Profile wird für jede Variante auf der linken Bildschirmseite ein Feld angezeigt. Sie können diese Profile verwenden, um Ihre Inhalte in der Vorschau anzuzeigen und Testsendungen durchzuführen.

>[!NOTE]
>
>Die hinzugefügten Varianten dienen nur als Testzwecke für Ihren aktuellen Inhalt. Die werden nicht in Adobe Experience Platform gespeichert, sondern in Ihrer Browser-Benutzersitzung, d. h. sie werden nicht angezeigt, wenn Sie sich abmelden oder von einem anderen Gerät aus arbeiten.

## Vorschau der Inhaltsvarianten {#preview}

Um eine Vorschau Ihres Inhalts mit einer der Varianten anzuzeigen, wählen Sie das entsprechende Feld aus, um die Inhaltsvorschau im rechten Bereich mit den für diese Variante eingegebenen Informationen zu aktualisieren.

Sie können eine Variante jederzeit mit der Suchschaltfläche oben rechts entfernen und **[!UICONTROL Entfernen]** auswählen. Um Informationen für eine Variante zu bearbeiten, klicken Sie auf die Suchschaltfläche und wählen Sie **[!UICONTROL Bearbeiten]** aus.

![](assets/simulate-custom-boxes.png)

## Durchführen eines Testversands {#proofs}

Mit Journey Optimizer können Sie Testsendungen an E-Mail-Adressen durchführen und dabei die Identität einer oder mehrerer Varianten annehmen, die Sie im Simulationsbildschirm hinzugefügt haben. Gehen Sie dazu wie folgt vor:

1. Vergewissern Sie sich, dass Varianten zum Testen Ihres Inhalts hinzugefügt wurden, und klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** .

1. Geben Sie im Feld **[!UICONTROL Empfänger]** die E-Mail-Adresse ein, an die Sie den Testversand durchführen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**. Wiederholen Sie den Vorgang, um den Testversand an zusätzliche E-Mail-Adressen zu senden. Sie können bis zu 10 Testversand-Empfänger hinzufügen.

1. Wählen Sie im unteren Bereich des Bildschirms die Variante aus, die Sie im Testversand verwenden möchten. Sie können mehrere Varianten auswählen. In diesem Fall enthält die E-Mail so viele Testsendungen wie ausgewählte Varianten.

   Wählen Sie für weitere Informationen zu einer Variante den Link **[!UICONTROL Profildetails anzeigen]** aus. Auf diese Weise können Sie die Informationen einsehen, die im vorherigen Bildschirm für die verschiedenen Varianten eingegeben wurden.

   ![](assets/simulate-custom-proofs.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]** , um mit dem Versand des Testversands zu beginnen.

1. Um den Testversand zu verfolgen, klicken Sie im Bildschirm zur Inhaltsimulation auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]** .

![](assets/simulate-custom-sent-proofs.png)
