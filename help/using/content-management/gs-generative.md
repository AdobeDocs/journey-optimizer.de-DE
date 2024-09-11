---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit dem AI-Assistenten in Journey Optimizer - Content Accelerator
description: Erfahren Sie, wie Sie auf den AI-Assistenten in Journey Optimizer - Content Accelerator zugreifen und mit ihm arbeiten können
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 448568ff9ee96d4fa6dbaaa43ce2d45e38d6b920
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 43%

---

# Erste Schritte mit dem AI-Assistenten in Journey Optimizer - Content Accelerator {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="KI-Assistent in Journey Optimizer für Content Acceleration"
>abstract="Nachdem Sie Ihren Versand erstellt und personalisiert haben, können Sie den KI-Assistenten in Journey Optimizer für Inhaltsbeschleunigung verwenden, um Ihre Inhalte zu optimieren. Diese Funktion vereinfacht den Prozess der Personalisierung und Inhaltsverbesserung, da der Inhalt durch eine Beschreibung dessen, was generieret werden soll, angepasst werden kann."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Hochladen von Marken-Assets"
>abstract="Im Menü Marken-Asset hochladen können Sie beliebige Marken-Assets mit Inhalten hinzufügen, die zusätzlichen Kontext für den AI-Assistenten in Journey Optimizer zur Inhaltsbeschleunigung bieten können, oder ein zuvor hochgeladenes Asset auswählen. Diese Option stellt sicher, dass der KI-Assistent Zugriff auf alle erforderlichen Materialien hat, um seine Funktionalität und Relevanz zu verbessern."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe-Begriffe zu generativer KI"
>abstract="Der Zugriff auf diese Funktion unterliegt Ihrer Zustimmung zu den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. Überprüfen Sie alle Ausgaben dieser Funktion auf ihre Richtigkeit und stellen Sie sicher, dass sie für Ihren Anwendungsfall geeignet sind."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Benutzerrichtlinien für generative KI in Adobe"

>[!INFO]
>
>Machen Sie sich mit [unserer interaktiven Demo](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator) vertraut, die es Ihnen ermöglicht, die Funktionen selbst zu erforschen und deren Funktionen vollständig zu verstehen.


Der AI-Assistent in Adobe Journey Optimizer for Content Acceleration, der von Microsoft Azure OpenAI und Adobe Firefly unterstützt wird, bietet vorausschauende Vorschläge für Inhaltsvarianten für Text und Bilder. Er ist für die Kanäle E-Mail, Push-Benachrichtigungen und SMS-Kanäle verfügbar. Diese neue Funktion bietet eine auf Eingabeaufforderungen basierende Text- und Bildgenerierung. Die Bildgenerierung wird mit Adobe Firefly gehandhabt.

Verwenden Sie den KI-Assistenten in Adobe Journey Optimizer for Content Acceleration, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Generieren Sie mehrere Varianten und erstellen Sie ein Experiment, um sie zu vergleichen. Mit dem Journey Optimizer-Inhaltsexperiment können Sie mehrere Nachrichtenabwandlungen definieren, um zu messen, welche bei Ihrer Zielgruppe am besten ankommt. Sie haben die Möglichkeit, Inhalt oder Betreff des Versands zu variieren. Die Zielgruppe der Nachricht wird nach dem Zufallsprinzip jeder Abwandlung zugewiesen, um zu bestimmen, welche Abwandlung in Bezug auf die angegebene Metrik am besten funktioniert. Weiterführende Informationen zum Inhaltsexperiment finden Sie in [diesem Abschnitt](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Bevor Sie mit der Verwendung dieser Funktion beginnen, lesen Sie die entsprechenden Informationen zu [Schutzmechanismen und Einschränkungen](#generative-guardrails).
>
>
>* Sie müssen einer [Benutzervereinbarung](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) zustimmen, bevor Sie den AI-Assistenten in Adobe Journey Optimizer für Inhaltsbeschleunigung verwenden können. Weitere Informationen erhalten Sie beim Adobe-Support.

## Zugriff auf den Inhaltsbeschleuniger des AI-Assistenten {#generative-access}

Um auf den AI-Assistenten in Adobe Journey Optimizer für die Inhaltsbeschleunigung zugreifen zu können, müssen Benutzer über die Berechtigung **Inhalt generieren** verfügen. [Weitere Informationen](../administration/permissions.md)

+++  Erfahren Sie, wie Sie Berechtigungen zur Inhaltserstellung zuweisen.

1. Gehen Sie im Produkt **Berechtigungen** zur Registerkarte **Rollen** und wählen Sie die gewünschte **Rolle** aus.

1. Klicken Sie auf **Bearbeiten** , um die Berechtigungen zu ändern.

1. Fügen Sie die Ressource **KI-Assistent** hinzu und wählen Sie dann aus dem Dropdown-Menü die Option **Inhalt erzeugen** aus.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Klicken Sie auf **Speichern** , um Änderungen anzuwenden.

   Alle Benutzer, die dieser Rolle bereits zugewiesen sind, erhalten ihre Berechtigungen automatisch aktualisiert.

1. Um diese Rolle neuen Benutzern zuzuweisen, navigieren Sie zur Registerkarte **Benutzer** im Dashboard **Rollen** und klicken Sie auf **Benutzer hinzufügen**.

1. Geben Sie den Namen und die E-Mail-Adresse des Benutzers ein oder wählen Sie aus der Liste aus und klicken Sie dann auf **Speichern**.

1. Wenn der Benutzer zuvor nicht erstellt wurde, lesen Sie die [Dokumentation für diese Version](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).

Der Benutzer erhält eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz.

+++

## Leitlinien und Einschränkungen {#generative-guardrails}

Die allgemeinen Richtlinien für die Verwendung des AI-Assistenten in Adobe Journey Optimizer for Content Acceleration zur E-Mail-Generierung sind unten aufgeführt:

* Die Qualität des generierten Inhalts wird stark durch das von Ihnen definierte Marketing-Ziel bzw. den von Ihnen definierten Prompt beeinflusst. Verwenden Sie einen gut definierten Prompt, damit das GenAI-Modell diesen korrekt interpretieren kann. 
* Laden Sie Marken-Assets hoch, damit die Informationen über Markeninhalte exakt sind. Andernfalls basieren die Inhalte auf öffentlich verfügbaren Informationen. Die hochgeladenen Inhalte können die folgenden Formate aufweisen: PDF-, JPEG-, PNG- oder ZIP-Dateien (mit unterstützten Dateiformaten).
* Die maximale Größe für hochgeladene Marken-Assets beträgt 50 MB. Größere Dateien oder viele Bilder können funktionieren, aber die Verarbeitungszeit verlängert sich.
* Verwenden Sie eine markenspezifische oder benutzerdefinierte Vorlage, um E-Mail-Inhalte mit dem AI-Assistenten in Adobe Journey Optimizer für die Inhaltsbeschleunigung zu erstellen. E-Mail-Vorlagen mit bis zu 8 bis 10 Bildern werden empfohlen.
* Vergewissern Sie sich, dass Sie problematische Ausgaben melden, indem Sie bei der Auswahl von Varianten die Symbole Daumen nach oben, Daumen nach unten oder Flagge verwenden.
* Ihre Verwendung des KI-Assistenten unterliegt den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. [Weitere Informationen](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Als Teil der Verpflichtung von Adobe zur Förderung der Transparenz bei der Verwendung generativer KI-Tools bei der Medienerstellung wendet Adobe Content credentials an, wenn Inhalte oder ein Projekt, das ein Firefly-generiertes Asset enthält, heruntergeladen oder exportiert werden. [Weitere Informationen](https://helpx.adobe.com/firefly/using/content-credentials.html)

Die folgenden Einschränkungen gelten für den AI-Assistenten in Adobe Journey Optimizer for Content Acceleration:

* Unterstützte Sprache ist nur Englisch. Nicht-englische Eingaben können zu inkonsistenten oder fehlerhaften Ergebnissen führen. Probleme, die sich aus nicht englischsprachigen Antworten ergeben, werden derzeit weder behoben noch verbessert.
* Nur für den E-Mail-, Push-, Web- und SMS-Kanal verfügbar.
* GenAI-Inhalte sind möglicherweise nicht immer genau: Bitte teilen Sie uns Ihr Feedback mit, damit unsere Ingenieurinnen und Ingenieure die Modelle verfeinern können.
* Sie können mehrere Marken-Assets hochladen, jedoch nur eines für eine bestimmte Generierung nutzen.


## Funktionen zur Inhaltserstellung für AI Assistant {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Generierung von E-Mails" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Generierung von E-Mails</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Generierung von SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Generierung von SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Generierung von Push-Benachrichtungen" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generierung von Push-Benachrichtigungen</strong></a>
</div>
<p></td>
<td>
<a href="generative-web.md">
<img alt="Webgenerierung" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Erstellung der Webseite</strong>
</div>
<p>
</td>
</tr></table>
