---
title: Anzeigen einer Vorschau und Testen der Inhalte
description: Erfahren Sie, wie Sie Ihren Inhalt in der Vorschau darstellen und testen können.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 65%

---

# Vorschau und Test Ihres Inhalts {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Sobald der Inhalt definiert wurde, kann mithilfe von Testprofilen eine Vorschau davon angezeigt und überprüft werden, ob das Rendering je nach verwendetem Kanal korrekt ist."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Überprüfen des Inhalt-Renderings"
>abstract="Nachdem Ihr Inhalt definiert wurde, können Sie ihn in der Vorschau anzeigen und überprüfen, ob das Rendering entsprechend dem verwendeten Kanal korrekt ist."

Sobald der Inhalt der definiert wurde, können Sie ihn vor dem Senden der Nachricht in der Vorschau anzeigen. Dies ist ein entscheidender Schritt, um sicherzustellen, dass er präzise, aber auch frei von Fehlern ist, sowohl im Inhalt als auch in den Personalisierungseinstellungen.

Darüber hinaus können Sie auch Testsendungen Ihrer E-Mail-Nachrichten an bestimmte Empfängerinnen bzw. Empfänger oder Abonnentinnen bzw. Abonnenten zum Testen und Validieren senden sowie ihr Rendering in beliebten Desktop-, Mobile- und Web-basierten Clients überprüfen.

Alle diese Aktionen können mit der Schaltfläche **[!UICONTROL Inhalt simulieren]** durchgeführt werden, auf die Sie über den Bildschirm „Inhalt bearbeiten“ Ihrer Nachricht oder über die E-Mail- und Web-Designer für die E-Mail- bzw. Web-Kanäle zugreifen können.

![](../email/assets/email-preview-button.png)

## Testen mit Testprofildaten oder Beispieleingabedaten {#methods}

Journey Optimizer bietet zwei Erlebnisse zum Testen von Inhalten:

* **Testen von Inhalten mithilfe von Testprofildaten**

  Sie können Testprofile verwenden, um eine Vorschau Ihres Inhalts anzuzeigen, E-Mail-Testsendungen durchzuführen und das E-Mail-Rendering zu überprüfen. Wenn Sie personalisierte Felder hinzugefügt haben, können Sie mithilfe von Testprofildaten überprüfen, wie diese angezeigt werden. Weitere Informationen finden Sie in den folgenden Abschnitten:

  ➡️ [Testprofile auswählen](test-profiles.md)
➡️ [Vorschau mit Testprofilen](preview.md)
➡️ [E-Mail-Testsendungen durchführen](proofs.md)
➡️ [Überprüfen des E-Mail-Renderings](rendering.md)
➡️ [Vorschau und Testversand Ihrer E-Mail (Video)](#video-preview)

* **Testen von Inhaltsvarianten mit Beispieleingabedaten**

  [!DNL Journey optimizer] können Sie Testsendungen für verschiedene Varianten Ihres Inhalts mithilfe von Beispieleingabedaten, die aus einer CSV-/JSON-Datei hochgeladen oder manuell hinzugefügt wurden, in der Vorschau anzeigen und senden.

  Alle Profilattribute, die in Ihren Inhalten für die Personalisierung verwendet werden, werden automatisch vom System erkannt und können für Ihre Tests zur Erstellung mehrerer Varianten verwendet werden.

  ➡️ [Inhaltsvarianten simulieren](../test-approve/simulate-sample-input.md)

## Wichtige Informationen

* **Erforderliche**: Die **[!DNL Manage Simulate Content]** Berechtigung muss im **[!DNL Content Library Manager]**-Produktprofil enthalten sein. [Weitere Informationen](../administration/ootb-product-profiles.md#content-library-manager).

  Um Testsendungen durchführen zu können, benötigen Sie die Berechtigungen **Genehmigen und veröffentlichen** für die spezifische Ressource (Kampagne oder Journey), die mit der E-Mail verknüpft ist. Um Testsendungen in einer Journey durchzuführen, ist außerdem die Berechtigung **Journey veröffentlichen** erforderlich. [Erfahren Sie mehr über Berechtigungen](../administration/ootb-permissions.md).

* **Personalization mit Kontextdaten** - Bei der Vorschau einer Nachricht oder dem Versand von Testsendungen werden nur Profil-Personalisierungsdaten angezeigt. Personalisierung, die auf Kontextdaten wie Ereignisinformationen basiert, kann nur im Kontext einer Journey getestet werden. Weitere Informationen hierzu finden [ in diesem Anwendungsbeispiel](../personalization/personalization-use-case.md).

* **Vorschau von Inhalten mit mehreren bedingten Varianten** - Bei der Simulation oder dem Rendern von Korrekturabzügen für E-Mails mit mehreren bedingten Varianten kann Journey Optimizer mehr Verarbeitungszeit benötigen. Wenn Zeitüberschreitungen oder Fehlermeldungen auftreten, sollten Sie die Gesamtzahl der Varianten reduzieren oder die bedingten Regeln vereinfachen. Weitere Informationen zu bedingtem Inhalt finden Sie auf [dieser Seite](../personalization/dynamic-content.md).

## Anleitungsvideo {#video-preview}

Erfahren Sie, wie Sie mit Testprofilen das E-Mail-Rendering über Postfächer hinweg testen, personalisierten E-Mails mit Testprofilen in der Vorschau anzeigen und einen Testversand durchführen.

>[!VIDEO](https://video.tv.adobe.com/v/3430337?quality=12&captions=ger)
