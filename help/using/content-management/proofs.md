---
title: Senden von E-Mail-Testsendungen
description: Erfahren Sie, wie Sie E-Mail-Testsendungen versenden.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 83da97926138c867ea2dacca6e5cf5e40c926eda
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 83%

---

# Senden von E-Mail-Testsendungen {#send-proofs}

>[!PREREQUISITES]
>
>Um Testsendungen durchführen zu können, müssen Benutzende über Berechtigungen **Genehmigen und veröffentlichen** für die spezifische Ressource, Kampagne oder Journey verfügen, die mit der E-Mail verknüpft ist. [Weitere Informationen zu Berechtigungen](../administration/ootb-permissions.md)

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die wichtigste Zielgruppe gesendet wird. Die Empfänger des Testversands sind für die Überprüfung der Nachricht verantwortlich: Darstellung, Inhalt, Personalisierungseinstellungen, Konfiguration.

Beachten Sie, dass Sie mit [!DNL Journey optimizer] auch verschiedene Varianten Ihres Inhalts testen können, indem Sie ihn in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV-/JSON-Datei hochgeladen oder manuell hinzugefügt wurden. [Erfahren Sie, wie Sie Ihren Inhalt mit Beispieleingabedaten testen](../test-approve/simulate-sample-input.md)

Gehen Sie wie folgt vor, um einen E-Mail-Testversand nach der Auswahl von [Testprofilen](test-profiles.md) durchzuführen:

1. Klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testversand durchführen]**.

   ![](../email/assets/send-proof-button.png)

1. Geben Sie im Fenster **[!UICONTROL Testversand starten]** die E-Mail-Adresse Ihres Empfängers ein und klicken Sie auf **[!UICONTROL Hinzufügen]**, um den Testversand an sich selbst oder Mitglieder Ihrer Organisation zu senden.

   Beachten Sie, dass Sie bis zu zehn Empfänger für Ihren Testversand hinzufügen können.

   ![](../email/assets/send-proof-add.png)

1. Wählen Sie die **Testprofile** aus, die zur Personalisierung des Nachrichteninhalts verwendet werden.

   Die Anzahl der Testversandnachrichten, die jede Person erhält, entspricht der Anzahl der ausgewählten Testprofile. Wenn Sie beispielsweise fünf Empfänger-E-Mails hinzugefügt und zehn Testprofile ausgewählt haben, senden Sie fünfzig Testversandnachrichten, von denen jeder Empfänger zehn erhält.

1. Bei Bedarf können Sie der Betreffzeile des Testversands ein Präfix hinzufügen. Nur alphanumerische Zeichen und Sonderzeichen, wie etwa . - _ ( ) [ ], sind als Präfix für die Betreffzeile zulässig.

1. Klicken Sie auf **[!UICONTROL Testversand durchführen]**.

   ![](../email/assets/send-proof-select.png)

1. Um den Status zu prüfen, klicken Sie im Bildschirm **[!UICONTROL Simulieren]** auf die Schaltfläche **[!UICONTROL Testsendungen anzeigen]**.

   ![](../email/assets/send-proof-view.png)

Es wird empfohlen, nach jeder Änderung am Nachrichteninhalt Testsendungen durchzuführen.

>[!NOTE]
>
>Bei Testsendungen ist der Link zur Mirrorseite nicht aktiv. Er wird erst in den endgültigen Nachrichten aktiviert.
