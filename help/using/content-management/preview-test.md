---
title: Anzeigen einer Vorschau und Testen der Inhalte
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: a5eacd7a746b2f17804062b23aee3146db0434c9
workflow-type: ht
source-wordcount: '438'
ht-degree: 100%

---

# Anzeigen einer Vorschau und Testen der Inhalte {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Sobald der Inhalt definiert wurde, kann mithilfe von Testprofilen eine Vorschau davon angezeigt und überprüft werden, ob das Rendering je nach verwendetem Kanal korrekt ist."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Nachdem Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

## Informationen zu Vorschau und Test {#about}

Sobald der Inhalt der definiert wurde, können Sie ihn vor dem Senden der Nachricht in der Vorschau anzeigen. Dies ist ein entscheidender Schritt, um sicherzustellen, dass er präzise, aber auch frei von Fehlern ist, sowohl im Inhalt als auch in den Personalisierungseinstellungen.

Darüber hinaus können Sie auch Testsendungen Ihrer E-Mail-Nachrichten an bestimmte Empfängerinnen bzw. Empfänger oder Abonnentinnen bzw. Abonnenten zum Testen und Validieren senden sowie ihr Rendering in beliebten Desktop-, Mobile- und Web-basierten Clients überprüfen.

>[!CAUTION]
>
>Bei der Vorschau einer Nachricht oder beim Versand von Testsendungen werden nur Profil-Personalisierungsdaten angezeigt. Personalisierung, die auf Kontextdaten wie Ereignisinformationen basiert, kann nur im Kontext einer Journey getestet werden. In [diesem Anwendungsbeispiel](../personalization/personalization-use-case.md) erfahren Sie, wie Sie die Personalisierung testen können.

Alle diese Aktionen können mit der Schaltfläche **[!UICONTROL Inhalt simulieren]** durchgeführt werden, auf die Sie über den Bildschirm „Inhalt bearbeiten“ Ihrer Nachricht oder über die E-Mail- und Web-Designer für die E-Mail- bzw. Web-Kanäle zugreifen können.

![](../email/assets/email-preview-button.png)

Beachten Sie, dass über die Berechtigung „**[!DNL Manage Simulate Content]**“ im Produktprofil „**[!DNL Content Library Manager]**“ verfügen müssen. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager).

## Testen mit Testprofilen oder Beispieleingabedaten {#methods}

Sie können Ihre Inhalte wie folgt in der Vorschau anzeigen und testen:

* **Testprofile**

  Verwenden Sie Testprofile, um eine Vorschau Ihres Inhalts anzuzeigen, einen E-Mail-Testversand durchzuführen und das E-Mail-Rendering zu überprüfen. Wenn Sie personalisierte Felder hinzugefügt haben, können Sie anhand von Testprofildaten überprüfen, wie diese angezeigt werden. Weitere Informationen finden Sie in den folgenden Abschnitten:

  ➡️ [Auswählen von Testprofilen](test-profiles.md)

  ➡️ [Vorschau des Inhalts mithilfe von Testprofilen](preview.md)

  ➡️ [Senden von E-Mail-Testsendungen](proofs.md)

  ➡️ [Überprüfen von E-Mail-Rendering](rendering.md)

  ➡️ [Vorschau und Durchführen eines Testversands einer E-Mail (Video)](#video-preview)

* **Beispieleingabedaten**

  Mit [!DNL Journey optimizer] können Sie verschiedene Varianten Ihrer Inhalte testen, indem Sie sie in der Vorschau anzeigen und einen Testversand mit Beispieleingabedaten durchführen, die aus einer CSV- oder JSON-Datei hochgeladen oder manuell hinzugefügt wurden.

  Alle Profilattribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.

  ➡️ [Erfahren Sie, wie Sie Ihren Inhalt mit Beispieleingabedaten testen](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Diese Funktionen stehen derzeit allen Kundinnen und Kunden als öffentliche Beta-Version nur für die Kanäle für E-Mail, SMS und Push-Benachrichtigungen zur Verfügung.

## Anleitungsvideo {#video-preview}

Erfahren Sie, wie Sie mit Testprofilen das E-Mail-Rendering über Postfächer hinweg testen, personalisierten E-Mails mit Testprofilen in der Vorschau anzeigen und einen Testversand durchführen.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
