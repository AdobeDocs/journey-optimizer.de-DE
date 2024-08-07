---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit dem KI-Assistenten
description: Erfahren Sie, wie Sie auf den KI-Assistenten von Journey Optimizer zugreifen und mit ihm arbeiten können
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 930070843c2c1ce022beb5dc6e8a61c8d4f70365
workflow-type: ht
source-wordcount: '602'
ht-degree: 100%

---

# Erste Schritte mit dem KI-Assistenten {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="KI-Assistent"
>abstract="Nachdem der Versand erstellt und personalisiert wurde, kann der KI-Assistent verwendet werden, um die Inhalte zu verbessern. Diese Funktion vereinfacht den Prozess der Personalisierung und Inhaltsverbesserung, da der Inhalt durch eine Beschreibung dessen, was generieret werden soll, angepasst werden kann."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Hochladen von Marken-Assets"
>abstract="Über das Menü „Marken-Asset hochladen“ können Sie ein beliebiges Marken-Asset mit Inhalten hinzufügen, die dem KI-Assistenten zusätzlichen Kontext liefern, oder ein bereits hochgeladenes Asset auswählen. Diese Option stellt sicher, dass der KI-Assistent Zugriff auf alle erforderlichen Materialien hat, um seine Funktionalität und Relevanz zu verbessern."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe-Begriffe zu generativer KI"
>abstract="Der Zugriff auf diese Funktion unterliegt Ihrer Zustimmung zu den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. Überprüfen Sie alle Ausgaben dieser Funktion auf ihre Richtigkeit und stellen Sie sicher, dass sie für Ihren Anwendungsfall geeignet sind."
>additional-url="https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Benutzerrichtlinien für generative KI in Adobe"

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* Erste Schritte mit dem KI-Assistenten
* [Generierung von E-Mails mit dem KI-Assistenten](generative-email.md)
* [SMS-Generierung mit dem KI-Assistenten](generative-sms.md)
* [Generierung von Push-Benachrichtigungen mit dem KI-Assistenten](generative-push.md)
* [Inhaltsexperiment mit dem KI-Assistenten](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Der KI-Assistent in Adobe Journey Optimizer ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar.

Der KI-Assistent in Adobe Journey Optimizer, der von Azure OpenAI unterstützt wird, liefert proaktive Vorschläge zur Variation von Text- und Bildinhalten. Er ist für die Kanäle E-Mail, Push-Benachrichtigungen und SMS-Kanäle verfügbar. Diese neue Funktion bietet eine auf Eingabeaufforderungen basierende Text- und Bildgenerierung. Die Bildgenerierung wird mit Adobe Firefly gehandhabt.

Sie können den KI-Assistenten in Journey Optimizer verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Generieren Sie mehrere Varianten und erstellen Sie ein Experiment, um sie zu vergleichen. Mit dem Journey Optimizer-Inhaltsexperiment können Sie mehrere Nachrichtenabwandlungen definieren, um zu messen, welche bei Ihrer Zielgruppe am besten ankommt. Sie haben die Möglichkeit, Inhalt oder Betreff des Versands zu variieren. Die Zielgruppe der Nachricht wird nach dem Zufallsprinzip jeder Abwandlung zugewiesen, um zu bestimmen, welche Abwandlung in Bezug auf die angegebene Metrik am besten funktioniert. Weiterführende Informationen zum Inhaltsexperiment finden Sie in [diesem Abschnitt](../content-management/content-experiment.md).

## Leitlinien und Einschränkungen {#generative-guardrails}

Im Folgenden sind die allgemeinen Richtlinien zur Verwendung des KI-Assistenten in Journey Optimizer für die E-Mail-Generierung aufgeführt:

* Die Qualität des generierten Inhalts wird stark durch das von Ihnen definierte Marketing-Ziel bzw. den von Ihnen definierten Prompt beeinflusst. Verwenden Sie einen gut definierten Prompt, damit das GenAI-Modell diesen korrekt interpretieren kann. 
* Laden Sie Marken-Assets hoch, damit die Informationen über Markeninhalte exakt sind. Andernfalls basieren die Inhalte auf öffentlich verfügbaren Informationen. Die hochgeladenen Inhalte können die folgenden Formate aufweisen: PDF-, JPEG-, PNG- oder ZIP-Dateien (mit unterstützten Dateiformaten).
* Die maximale Größe für hochgeladene Marken-Assets beträgt 50 MB. Größere Dateien oder viele Bilder können funktionieren, aber die Verarbeitungszeit verlängert sich.
* Verwenden Sie eine in Adobe Campaign erstellte E-Mail-Vorlage, vorzugsweise [eine integrierte E-Mail-Vorlage](../email/use-email-templates.md), eine markenspezifische Vorlage oder eine benutzerdefinierte Vorlage, um Ihre E-Mail-Inhalte zu erstellen. Es wird eine E-Mail-Vorlage mit bis zu 8 bis 10 Bildern empfohlen.
* Vergewissern Sie sich, dass Sie problematische Ausgaben melden, indem Sie bei der Auswahl von Varianten die Symbole Daumen nach oben, Daumen nach unten oder Flagge verwenden.
* Ihre Verwendung des KI-Assistenten unterliegt den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. [Weitere Informationen](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Die folgenden Einschränkungen gelten für den KI-Assistenten in Journey Optimizer:

* Nur in englischer Sprache verfügbar.
* Nur für die folgenden Kanäle verfügbar: E-Mail, Push und SMS.
* GenAI-Inhalte sind möglicherweise nicht immer genau: Bitte teilen Sie uns Ihr Feedback mit, damit unsere Ingenieurinnen und Ingenieure die Modelle verfeinern können.
* Sie können mehrere Marken-Assets hochladen, jedoch nur eines für eine bestimmte Generierung nutzen.

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
</tr></table>
