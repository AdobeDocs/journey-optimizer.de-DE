---
title: Anzeigen einer Vorschau und Testen der Inhalte
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 55%

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

## Über Vorschau und Test {#about}

Nachdem Ihr Inhalt definiert wurde, können Sie den Inhalt in der Vorschau anzeigen, bevor Sie die Nachricht senden. Dies ist ein entscheidender Schritt, um sicherzustellen, dass er präzise, aber auch frei von Fehlern ist, sowohl im Inhalt als auch in den Personalisierungseinstellungen.

Sie können auch Testsendungen Ihrer E-Mail-Nachrichten an bestimmte Empfänger oder Abonnenten senden, um sie zu testen und zu validieren, und deren Rendering in gängigen Desktop-, Mobile- und Web-basierten Clients überprüfen.

>[!CAUTION]
>
>Bei der Vorschau einer Nachricht oder beim Versand von Testsendungen werden nur Profil-Personalisierungsdaten angezeigt. Personalisierung, die auf Kontextdaten wie Ereignisinformationen basiert, kann nur im Kontext einer Journey getestet werden. In [diesem Anwendungsbeispiel](../personalization/personalization-use-case.md) erfahren Sie, wie Sie die Personalisierung testen können.

Alle diese Aktionen können mit der Schaltfläche **[!UICONTROL Inhalt simulieren]** durchgeführt werden, auf die Sie über den Bildschirm „Inhalt bearbeiten“ Ihrer Nachricht oder über die E-Mail- und Web-Designer für die E-Mail- bzw. Web-Kanäle zugreifen können.

![](../email/assets/email-preview-button.png)

Beachten Sie, dass die Berechtigung **[!DNL Manage Simulate Content]** im Produktprofil **[!DNL Content Library Manager]** enthalten sein muss. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager).

## Testen mit Testprofilen oder Beispieleingabedaten {#methods}

Sie können Ihre Inhalte wie folgt in der Vorschau anzeigen und testen:

* **Testprofile**

  Verwenden Sie Testprofile, um eine Vorschau Ihres Inhalts anzuzeigen, E-Mail-Testsendungen durchzuführen und das E-Mail-Rendering zu überprüfen. Wenn Sie personalisierte Felder hinzugefügt haben, können Sie anhand von Testprofildaten überprüfen, wie diese angezeigt werden.

  ➡️ [Testprofile auswählen](test-profiles.md)

  ➡️ [Vorschau Ihres Inhalts mit Testprofilen anzeigen](preview.md)

  ➡️ [E-Mail-Testsendungen senden](proofs.md)

  ➡️ [Prüfen des E-Mail-Renderings](rendering.md)

  ➡️ [Erfahren Sie in diesem Video, wie Sie Ihre E-Mail in der Vorschau anzeigen und einen Testversand durchführen können](#video-preview).

* **Beispieleingabedaten**

  Mit [!DNL Journey optimizer] können Sie verschiedene Varianten Ihres Inhalts testen, indem Sie ihn in der Vorschau anzeigen und mithilfe von Beispieleingabedaten, die aus einer CSV-/JSON-Datei hochgeladen oder manuell hinzugefügt wurden, Testsendungen durchführen.

  Alle Profilattribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.

  ➡️ [Erfahren Sie, wie Sie Ihren Inhalt mit Beispieleingabedaten testen können](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Diese Funktionen stehen derzeit nur allen Kunden als öffentliche Beta-Version für die Kanäle E-Mail, SMS und Push-Benachrichtigung zur Verfügung.

## Anleitungsvideo {#video-preview}

Erfahren Sie, wie Sie mit Testprofilen das E-Mail-Rendering über Postfächer hinweg testen, Ihre personalisierten E-Mails mit Testprofilen in der Vorschau ansehen und Testsendungen durchführen können.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
