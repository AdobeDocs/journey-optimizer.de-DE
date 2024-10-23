---
solution: Journey Optimizer
product: journey optimizer
title: Testen von Inhalten mit Beispieleingabedaten
description: Erfahren Sie, wie Sie E-Mail-Inhalte in der Vorschau anzeigen und Testsendungen mit Beispiel-Eingabedaten versenden.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: ht
source-wordcount: '769'
ht-degree: 100%

---


# Testen von Inhalten mit Beispieleingabedaten {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulationen mit Beispieleingaben"
>abstract="Auf diesem Bildschirm können Sie verschiedene Varianten Ihrer E-Mail-Inhalte testen, indem Sie Werte für Personalisierungsfelder über eine CSV-Vorlage bereitstellen (CSV herunterladen) oder die Werte manuell eingeben."

>[!AVAILABILITY]
>
>Diese Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar.

Mit Journey Optimizer können Sie verschiedene Varianten Ihrer E-Mail-Inhalte testen, indem Sie eine Vorschau anzeigen und Testsendungen mit Beispiel-Eingabedaten senden, die aus einer CSV-Datei hochgeladen oder manuell hinzugefügt wurden. Alle Profilattribute, die in Ihrem Inhalt für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.

Um auf dieses Erlebnis zuzugreifen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalt simulieren]** und wählen Sie **[!UICONTROL Mit CSV (Beta) simulieren]** aus.

![](assets/simulate-sample.png)

Die wichtigsten Schritte zum Testen Ihrer Inhalte sind:

1. Fügen Sie bis zu 30 Varianten mit Beispiel-Eingabedaten hinzu, entweder durch Hochladen einer CSV-Datei oder durch manuelles Hinzufügen von Daten. [Erfahren Sie, wie Sie Varianten hinzufügen](#profiles)
1. Überprüfen Sie die Vorschau Ihres Inhalts mit den verschiedenen Varianten. [Erfahren Sie, wie Sie eine Vorschau Ihrer Inhalte anzeigen können](#preview)
1. Senden Sie bis zu 10 Testsendungen an E-Mail-Adressen unter Verwendung der verschiedenen Varianten. [Durchführen eines Testversands](#proofs)


## Leitlinien und Einschränkungen {#limitations}

Bevor Sie mit dem Testen Ihrer Inhalte unter Verwendung von Beispiel-Eingabedaten beginnen, sollten Sie die folgenden Leitlinien und Voraussetzungen berücksichtigen.

* Derzeit ist das Testen unter Verwendung von Beispiel-Eingabedaten nur für den E-Mail-Kanal verfügbar. Das Erlebnis kann nicht über die Schaltfläche „Inhalt simulieren“ im E-Mail-Designer aufgerufen werden.
* Die folgenden Funktionen sind im aktuellen Erlebnis nicht verfügbar: Inbox-Rendering, Spam-Berichte, mehrsprachige Inhalte und Inhaltsexperimente. Um diese Funktionen zu verwenden, wählen Sie in Ihrem Inhalt die Schaltfläche **[!UICONTROL Inhalt simulieren]** aus, um auf die vorherige Benutzeroberfläche zuzugreifen.
* Derzeit werden nur Profilattribute unterstützt. Wenn in Ihren Inhalten kontextbezogene Attribute zur Personalisierung verwendet werden, können Sie Ihre Inhalte nicht mit diesen Attributen testen.
* Bei der Dateneingabe für Ihre Varianten werden nur die folgenden Datentypen unterstützt: Zahl (Ganzzahl und Dezimalzahl), Zeichenkette, boolescher Wert und Datum. Bei allen anderen Datentypen wird eine Fehlermeldung angezeigt.

## Hinzufügen von Varianten {#profiles}

Sie können bis zu 30 Varianten hinzufügen, um Ihre Inhalte zu testen, entweder mithilfe einer CSV-Datei oder manuell:

* Um Beispiel-Eingabedaten aus einer CSV-Datei hochzuladen, klicken Sie auf die Verknüpfung ]**CSV herunterladen**[!UICONTROL , um eine CSV-Dateivorlage abzurufen. Diese Vorlagen enthalten eine Spalte für jedes Profilattribut, das in Ihrem Inhalt zur Personalisierung verwendet wird.

  Füllen Sie die CSV-Datei aus und klicken Sie dann auf **[!UICONTROL Eingabedaten hochladen]**, um sie zum Testen Ihres Inhalts zu laden.

* Um eine Variante manuell hinzuzufügen, klicken Sie auf die Schaltfläche **[!UICONTROL Beispieleingabe erstellen]** und geben Sie die Beispiel-Eingabedaten für die Variante ein. Für jedes Profilattribut, das in Ihren personalisierten Inhalten verwendet wird, wird ein Feld angezeigt.

  ![](assets/simulate-custom-add.png)

Nach Auswahl der Profile wird für jede Variante auf der linken Bildschirmseite ein Feld angezeigt. Sie können diese Profile verwenden, um Ihre Inhalte in der Vorschau anzuzeigen und Testsendungen durchzuführen.

>[!NOTE]
>
>Die hinzugefügten Varianten dienen nur zu Testzwecken für Ihre aktuellen Inhalte. Sie werden nicht in Adobe Experience Platform, sondern in Ihrer Benutzersitzung im Browser gespeichert, d. h. sie werden nicht angezeigt, wenn Sie sich abmelden oder von einem anderen Gerät aus arbeiten.

## Vorschau Ihrer Inhaltsvarianten {#preview}

Für eine Vorschau Ihrer Inhalte mit einer der Varianten wählen Sie das entsprechende Kästchen zur Aktualisierung der Inhaltsvorschau im rechten Bereich mit den für diese Variante eingegebenen Informationen aus.

Sie können eine Variante jederzeit entfernen, indem Sie auf die Schaltfläche mit den drei Punkten in der oberen rechten Ecke klicken und **[!UICONTROL Entfernen]** auswählen. Um Informationen für eine Variante zu bearbeiten, klicken Sie auf die Schaltfläche mit den drei Punkten und wählen **[!UICONTROL Bearbeiten]** aus.

![](assets/simulate-custom-boxes.png)

## Durchführen eines Testversands {#proofs}

Mit Journey Optimizer können Sie Testsendungen an E-Mail-Adressen durchführen und dabei die Identität einer oder mehrerer Varianten annehmen, die Sie im Simulationsbildschirm hinzugefügt haben. Gehen Sie dazu wie folgt vor:

1. Vergewissern Sie sich, dass Varianten zum Testen Ihrer Inhalte hinzugefügt wurden, und klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]**.

1. Geben Sie im Feld **[!UICONTROL Empfänger]** die E-Mail-Adresse ein, an die Sie den Testversand durchführen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**. Wiederholen Sie den Vorgang, um den Testversand an zusätzliche E-Mail-Adressen zu senden. Sie können bis zu 10 Empfängerinnen und Empfänger für den Testversand hinzufügen.

1. Wählen Sie im unteren Bereich des Bildschirms die Variante aus, die Sie für den Testversand verwenden möchten. Sie können mehrere Varianten auswählen. In diesem Fall enthält die E-Mail so viele Testsendungen wie ausgewählte Varianten.

   Weitere Informationen zu einer Variante erhalten Sie über die Verknüpfung **[!UICONTROL Profilinformationen anzeigen]**. So können Sie die auf dem vorherigen Bildschirm eingegebenen Informationen für die verschiedenen Varianten anzeigen.

   ![](assets/simulate-custom-proofs.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]**, um den Testversand zu beginnen.

1. Um den Testversand zu verfolgen, klicken Sie im Bildschirm „Inhalt simulieren“ auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]**.

![](assets/simulate-custom-sent-proofs.png)
