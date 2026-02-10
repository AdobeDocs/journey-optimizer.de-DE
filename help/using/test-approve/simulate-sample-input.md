---
solution: Journey Optimizer
product: journey optimizer
title: Simulieren von Inhaltsvarianten
description: Erfahren Sie, wie Sie mithilfe von Beispieleingabedaten aus einer CSV- oder JSON-Datei oder mit manuell hinzugefügten Beispieleingabedaten eine Vorschau der Inhalte anzeigen und den E-Mail-Testversand durchführen.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
exl-id: 8462c75e-4f4b-4c4f-8734-19efbbc70c7a
source-git-commit: 692b539f2c7623a14192558c3eba55d90c54f22d
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 89%

---

# Simulieren von Inhaltsvarianten {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulationen mit Beispieleingaben"
>abstract="Auf diesem Bildschirm können verschiedene Varianten der Inhalte getest werden, indem  Werte für Personalisierungsfelder über eine CSV- oder JSON-Vorlage bereitgestellt oder die Werte manuell eingegeben werden."

[!DNL Journey Optimizer] können Sie verschiedene Varianten Ihres Inhalts anhand von Beispieleingabedaten in der Vorschau anzeigen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden.

Alle Attribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden. Eine Variante bezieht sich auf eine Version des Inhalts mit unterschiedlichen Werten für die zugehörigen Attribute.

>[!NOTE]
>
>Varianten dienen nur zu Testzwecken für Ihre aktuellen Inhalte. Sie werden nicht in Adobe Experience Platform, sondern in Ihrer Benutzersitzung im Browser gespeichert, d. h., sie werden nicht angezeigt, wenn Sie sich abmelden oder von einem anderen Gerät aus arbeiten.

## Leitlinien und Einschränkungen {#limitations}

Bevor Sie mit dem Testen Ihrer Inhalte unter Verwendung von Beispiel-Eingabedaten beginnen, sollten Sie die folgenden Leitlinien und Voraussetzungen berücksichtigen.

* **Kanäle**: Eine Simulation von Inhaltsvarianten ist verfügbar für:

   * die Kanäle E-Mail, SMS und Push-Benachrichtigungen;
   * alle Inbound-Kanäle (Web, Code-basiertes Erlebnis, In-App, Inhaltskarten).

* **Unterstützte Funktionen**: Inhaltsvarianten können mit [!DNL Journey Optimizer]-Funktionen für mehrsprachige Inhalte und Inhaltsexperimente verwendet werden. Auf diese Weise können Sie Nachrichten in mehreren Sprachen testen und den Inhalt durch Experimentieren optimieren.

  Sie können auch Inhaltsvarianten nutzen, um Ihre Inhaltsvorlagen zu testen.

  >[!NOTE]
  >
  >Zurzeit sind Inbox-Rendering- und Spam-Berichte im aktuellen Erlebnis nicht verfügbar. Um diese Funktionen zu verwenden, wählen Sie in Ihrem Inhalt die Schaltfläche **[!UICONTROL Inhalt simulieren]** aus und greifen Sie auf die vorherige Benutzeroberfläche zu.

* **Attribute**: Sowohl Profil- als auch kontextuelle Attribute werden unterstützt.

* **Datentypen** - Bei der Eingabe von Daten für Varianten werden nur die folgenden Datentypen unterstützt: Zahl (Ganzzahl und Dezimalzahl), Zeichenfolge, Boolescher Wert und Datentyp. Bei allen anderen Datentypen wird eine Fehlermeldung angezeigt.

* **Variantenanzahl**: Sie können bis zu 30 Varianten entweder mithilfe einer Datei oder manuell hinzufügen, um Ihre Inhalte zu testen.

## Hinzufügen und Vorschau von Inhaltsvarianten

Um Varianten für Ihren Inhalt zu erstellen und in einer Vorschau anzuzeigen, klicken Sie auf die Schaltfläche **[!UICONTROL Inhalte simulieren]** und wählen Sie **[!UICONTROL Inhaltsvarianten simulieren]** aus.

![Option „Inhaltsvarianten simulieren“](assets/simulate-sample.png)

Die wichtigsten Schritte zum Testen Ihrer Inhalte sind:

1. **Varianten hinzufügen**: Fügen Sie bis zu 30 Varianten mit Beispieleingabedaten hinzu, entweder durch Hochladen einer Datei oder durch manuelles Hinzufügen von Daten. [Informationen zum Hinzufügen von Varianten](#profiles)
1. **Vorschau von Inhaltsvarianten**: Überprüfen Sie die Vorschau Ihres Inhalts mit den verschiedenen Varianten. [Informationen zur Vorschau von Inhalten](#preview)
1. **E-Mail-Testsendungen durchführen**: Senden Sie für E-Mail-Inhalte bis zu 10 Testsendungen an E-Mail-Adressen unter Verwendung der verschiedenen Varianten. [Informationen zum Durchführen eines Testversands](#proofs)

### Hinzufügen von Varianten {#profiles}

Beim Zugriff auf das Erlebnis mit den Inhaltsvarianten werden alle in Ihren Inhalten verwendeten Personalisierungsfelder automatisch erkannt und in einer Liste leerer Varianten angezeigt.

Wenn Ihre E-Mail beispielsweise die beiden Personalisierungsfelder „Stadt“ und „Guthaben an Programmpunkten“ enthält, werden diese in der Liste angezeigt. Zunächst werden keine Werte eingegeben und im Vorschaufenster wird kein personalisierter Inhalt angezeigt.

![Liste der Eingabevarianten](assets/simulate-custom-variants-list.png)

So bearbeiten Sie den Wert einer Variante:

1. Klicken Sie auf die Schaltfläche mit den Auslassungspunkten neben der Variante.
1. Wählen Sie **[!UICONTROL Bearbeiten]** aus, um benutzerdefinierte Werte für jedes Personalisierungsfeld anzugeben.
1. Der Vorschaubereich wird aktualisiert und zeigt an, wie Ihr Inhalt mit den eingegebenen Werten gerendert wird.

So fügen Sie eine neue Variante hinzu:

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Beispieleingabe erstellen]**.
1. Es wird eine neue leere Variante angezeigt, die alle erkannten Personalisierungsfelder enthält.
1. Bearbeiten Sie die neue Variante nach Bedarf.

![Beispiel-Eingabeschaltfläche erstellen](assets/simulate-custom-add.png)

Sie können auch eine Datei mit vordefinierten Varianten und Werten hochladen, um den Vorgang zu beschleunigen.

1. Klicken Sie auf **[!UICONTROL Beispiel herunterladen]**, um eine Dateivorlage herunterzuladen.
1. Wählen Sie ein Dateiformat aus: CSV, JSON oder JSONLINES.
1. Öffnen Sie die Vorlagendatei und geben Sie die gewünschten Werte für jedes Profilattribut ein. Die Vorlage enthält eine Spalte für jedes Profilattribut, das in Ihrem Inhalt zur Personalisierung verwendet wird.

   Beispiel für JSON-Syntax:

   ```
   {
   "profile": {
       "attributes": {
       "person": {
           "name": {
               "lastName": "Doe",
               "firstName": "John"
               }
           }
       }
   }
   }
   ```

1. Wenn Ihre Datei fertig ist, klicken Sie auf **[!UICONTROL Eingabedaten hochladen]**, um sie zu laden.
1. Nach dem Hochladen wird der Liste für jeden Eintrag in der Datei eine neue Variante hinzugefügt.

   ![Hochgeladene Beispiel-Eingabevarianten](assets/simulate-custom-variants.png)

Sobald Varianten hinzugefügt wurden, können Sie diese verwenden, um im rechten Bereich eine Vorschau Ihres Inhalts anzuzeigen und E-Mail-Testsendungen durchzuführen.

### Vorschau von Inhaltsvarianten {#preview}

Um eine Vorschau Ihrer Inhalte mit einer Variante anzuzeigen, wählen Sie die entsprechende Variante aus der Liste aus, um die Inhalte im Vorschaufenster mit den für diese Variante eingegebenen Informationen zu aktualisieren.

Im folgenden Beispiel haben wir zwei Varianten für die E-Mail-Betreffzeile hinzugefügt:

| Auswahl von Variante 1 | Auswahl von Variante 2 |
|----------|-------------|
| ![Auswahl Variante 1](assets/simulate-custom-boxes.png) | ![Auswahl Variante 2](assets/simulate-custom-boxes2.png) |

Für mehrsprachige Inhalte und Experimente steht eine Dropdown-Liste zur Verfügung, über die zwischen den verschiedenen Sprachvarianten oder Abwandlungen gewechselt werden kann.

![Sprach- oder Abwandlungsselektor](assets/simulate-custom-experiment.png)

Sie können eine Variante jederzeit entfernen, indem Sie oben rechts auf die Schaltfläche mit den Auslassungspunkten klicken und **[!UICONTROL Entfernen]** auswählen. Um Informationen für eine Variante zu bearbeiten, klicken Sie auf die Schaltfläche mit den drei Punkten und wählen **[!UICONTROL Bearbeiten]** aus.

### Durchführen von Testsendungen {#proofs}

Mit Journey Optimizer können Sie Testsendungen an E-Mail-Adressen durchführen und dabei die Identität einer oder mehrerer Varianten annehmen, die Sie im Simulationsbildschirm hinzugefügt haben. Gehen Sie dazu wie folgt vor:

1. Vergewissern Sie sich, dass Varianten zum Testen Ihrer Inhalte hinzugefügt wurden, und klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]**.

1. Geben Sie im Feld **[!UICONTROL Empfänger]** die E-Mail-Adresse ein, an die Sie den Testversand durchführen möchten, und klicken Sie dann auf **[!UICONTROL Hinzufügen]**. Wiederholen Sie den Vorgang, um den Testversand an zusätzliche E-Mail-Adressen zu senden. Sie können bis zu 10 Empfängerinnen und Empfänger für den Testversand hinzufügen.

1. Wählen Sie im unteren Bereich des Bildschirms die Variante aus, die Sie für den Testversand verwenden möchten. Sie können mehrere Varianten auswählen. In diesem Fall enthält die E-Mail so viele Testsendungen wie ausgewählte Varianten.

   Weitere Informationen zu einer Variante erhalten Sie über die Verknüpfung **[!UICONTROL Profilinformationen anzeigen]**. So können Sie die auf dem vorherigen Bildschirm eingegebenen Informationen für die verschiedenen Varianten anzeigen.

   ![Testversand-Empfänger und Variantenauswahl](assets/simulate-custom-proofs.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Testversand durchführen]**, um den Testversand zu beginnen.

1. Um den Testversand zu verfolgen, klicken Sie im Bildschirm „Inhalt simulieren“ auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]**.

![Liste der durchgeführten Testsendungen](assets/simulate-custom-sent-proofs.png)
