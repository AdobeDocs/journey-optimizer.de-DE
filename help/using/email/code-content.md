---
solution: Journey Optimizer
product: journey optimizer
title: Codieren Ihres eigenen E-Mail-Inhalts
description: Erfahren Sie, wie Sie Ihren eigenen E-Mail-Inhalt codieren
feature: Email Design
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: Code, HTML, Editor
exl-id: 5fb79300-08c6-4c06-a77c-d0420aafca31
source-git-commit: 48b3ef3d2e041ea49d1b0c91cc72ea04237a5e33
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 50%

---

# Programmieren von eigenem Inhalt {#code-content}

Verwenden Sie den Modus **[!UICONTROL Eigenen Code schreiben]**, um Roh-HTML zu importieren und/oder Ihren E-Mail-Inhalt zu codieren. Diese Methode setzt HTML-Kenntnisse voraus.

➡️ [Funktion im Video kennenlernen](#video)

>[!CAUTION]
>
> Bilder von [Adobe Experience Manager Assets](../integrations/assets.md) können bei dieser Methode nicht referenziert werden. Die Bilder, auf die im HTML-Code verwiesen wird, müssen an einem öffentlichen Speicherort abrufbar sein.

1. Wählen Sie auf der Startseite des E-Mail-Designers die Option **[!UICONTROL Eigenen Code erstellen]**.

   ![](assets/code-your-own.png)

1. Geben Sie Ihren HTML-Roh-Code ein oder fügen Sie ihn ein.

1. Verwenden Sie den linken Bereich, um die Personalisierungsfunktionen von [!DNL Journey Optimizer] anzuwenden. [Weitere Informationen](../personalization/personalize.md)

   ![](assets/code-editor.png)

   >[!NOTE]
   >
   >Der Personalisierungseditor in der E-Mail-Designer weist im Vergleich zu Journey-Ausdrücken einige Funktionsbeschränkungen auf. [Erfahren Sie mehr über Funktionsbeschränkungen für Datum/Uhrzeit](#date-time-limitations)

1. Wenn Sie den E-Mail-Designer öffnen möchten, um Ihre E-Mail von einem neuen Design aus zu beginnen, wählen Sie **[!UICONTROL Design ändern]** aus dem Optionen-Menü aus.

   ![](assets/code-editor-change-design.png)

   >[!NOTE]
   >
   >Dadurch wird die ausgewählte Vorlage im E-Mail-Designer geöffnet. Dort können Sie entweder das Design Ihrer E-Mail abschließen oder mit der Option **[!UICONTROL Zum Code-Editor wechseln]** zurück zum Code-Editor gehen.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Vorschau]**, um den Nachrichtenentwurf und die Personalisierung mithilfe von Testprofilen zu überprüfen. [Weitere Informationen](../content-management/preview-test.md)

   ![](assets/code-editor-preview.png)

1. Wenn Ihr Code fertig ist, klicken Sie auf **[!UICONTROL Speichern]** und kehren Sie dann zurück zum Bildschirm „Nachrichtenerstellung“, um die Nachricht fertigzustellen.

   ![](assets/code-editor-save.png)

## Funktionseinschränkungen für Datum und Uhrzeit {#date-time-limitations}

Bei Verwendung der Personalisierung im E-Mail-Designer-Code-Editor ist die `now()` für dynamische Datumsberechnungen nicht verfügbar.

>[!IMPORTANT]
>
>Die `now()` Funktion wird **nicht unterstützt** in der Ausdruckssprache des E-Mail-Builders angezeigt. Obwohl `now()` in Journey-Bedingungen verfügbar ist, kann es nicht in E-Mail-Inhalten oder im Code-Editor verwendet werden.

**Verfügbare Alternativen:**

Verwenden Sie die folgenden Funktionen, um mit dem aktuellen Datum und der aktuellen Uhrzeit in der E-Mail-Personalisierung zu arbeiten:

* **`getCurrentZonedDateTime()`** - Gibt das aktuelle Datum und die aktuelle Uhrzeit mit Zeitzoneninformationen zurück. Dies ist die empfohlene Alternative zu `now()`.

  Beispiel: `{%= getCurrentZonedDateTime() %}` gibt `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]` zurück

* **`currentTimeInMillis()`** - Gibt die aktuelle Zeit in Epochenmillisekunden zurück.

  Beispiel: `{%= currentTimeInMillis() %}`

**Empfohlene Problemumgehungen:**

Wenn Sie in Ihrem E-Mail-Inhalt Datumsberechnungen durchführen müssen:

* **Datumsfelder vorberechnen** - Berechnen Sie die erforderlichen Datumswerte in Ihrer Datenpipeline oder in den Profilattributen, bevor Sie die E-Mail senden, und verweisen Sie dann in Ihrer Personalisierung auf diese vorberechneten Werte.

  Beispiel: `{%= profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate %}`

* **Funktionen zur Datumsbearbeitung verwenden** - Verwenden Sie [Datums-/](../personalization/functions/dates.md)-Funktionen wie `dayOfYear()` oder `diffInDays()` mit Datumswerten aus Profilattributen.

  Beispiel: `{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}`

* **Berechnete Attribute verwenden** - Erstellen Sie [berechnete Attribute](../audience/computed-attributes.md) die komplexe Datumsberechnungen durchführen und die Ergebnisse als Profilattribute verfügbar machen.

Weitere Informationen zu [Datums-/Uhrzeitfunktionen in der &#x200B;](../personalization/functions/dates.md)).
