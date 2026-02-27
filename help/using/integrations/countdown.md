---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Verwenden von Dynamic Media mit Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 707bc4053ee05c275b562e35227e54836e91fa27
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 3%

---

# Countdown-Timer einfügen {#countdown}

Erstellen Sie eine Dringlichkeit und maximieren Sie Konversionen mit Dynamic Media-Countdown-Timern, die in Echtzeit aktualisiert werden, wenn Empfänger Ihre E-Mails öffnen. Diese Funktion ist ideal für Flash-Verkäufe, zeitlich begrenzte Angebote und zeitkritische Promotions.

Als Marketing-Experte für eine Einzelhandelsmarke führen Sie beispielsweise einen 48-Stunden-Flash-Verkauf durch. Verwenden Sie den Countdown-Timer in Ihren Werbe-E-Mails:

* Empfänger, die sofort öffnen, sehen „47 Stunden verbleibend“
* Empfänger, die 24 Stunden später öffnen, sehen „23 Stunden verbleibend“
* Empfänger, die nach Verkaufsende öffnen, sehen „Verkauf beendet“

Weitere Informationen zum Erstellen von Dynamic Media in Adobe Experience Manager finden Sie [diesem Dokument](assets/do-not-localize/countdown.pdf).


1. Erstellen Sie **[!DNL Adobe Experience Manager]** eine Dynamic Media-Vorlage und fügen Sie ihr eine Countdown-Timer-Komponente hinzu.

   ![](assets/timer-1.png)

1. Erstellen Sie **[!DNL Journey Optimizer]** eine neue Kampagne oder öffnen Sie eine bestehende und greifen Sie dann auf die E-Mail-Designer zu.

1. Ziehen Sie eine **[!UICONTROL HTML-Komponente]** per Drag-and-Drop in Ihren E-Mail-Inhalt.

1. Wählen Sie **[!UICONTROL Quellcode anzeigen]** aus, um die HTML direkt zu bearbeiten.

   ![](assets/timer-2.png)

1. Navigieren Sie im Menü **[!UICONTROL HTML bearbeiten]** zu **[!UICONTROL Assets]** und klicken Sie auf **[!UICONTROL Asset-Auswahl öffnen]**, um Ihre veröffentlichte Dynamic Media-Vorlage zu durchsuchen und auszuwählen.

   ![](assets/timer-3.png)

1. Konfigurieren **[!UICONTROL im Menü „Benutzerdefinierte]**&quot; alle anpassbaren URL-Parameter, die für Ihre Vorlage erforderlich sind.

   Klicken Sie **[!UICONTROL Speichern]** wenn Sie fertig sind.

   ![](assets/timer-4.png)

1. Wählen Sie das Asset in der E-Mail-Designer aus und rufen Sie dann das Menü **[!UICONTROL Stile]** auf.

   Konfigurieren Sie die folgenden Einstellungen:
   * **Bannertext**: Der mit dem Timer angezeigte Text
   * **Endzeit**: Datum und Uhrzeit, zu der der Countdown abläuft. Geben Sie die Uhrzeit nur in GMT (Greenwich Mean Time) ein. Das System akzeptiert keine anderen Zeitzonen.
   * **Fallback-Text**: Die Nachricht, die nach dem Ende des Timers angezeigt wird

   ![](assets/timer-5.png)

1. Klicken Sie **[!UICONTROL Vorschau]**, um den Timer mit Echtzeit-Countdown-Updates anzuzeigen und Ihre Konfiguration zu überprüfen.

Wenn Empfänger die E-Mail öffnen, sehen sie die genaue verbleibende Zeit für Ihren Flash-Verkauf. Wird die E-Mail zu einem späteren Zeitpunkt erneut geöffnet, wird der Countdown automatisch mit der aktuell verbleibenden Zeit aktualisiert. Nach dem Enddatum wird die Standardmeldung automatisch angezeigt.

