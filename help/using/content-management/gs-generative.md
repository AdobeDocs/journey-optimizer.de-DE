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
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 38%

---

# Erste Schritte mit dem KI-Assistenten {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="KI-Assistent"
>abstract="Nachdem Sie Ihren Versand erstellt und personalisiert haben, können Sie den KI-Assistenten verwenden, um Ihren Inhalt zu verbessern. Diese Funktion vereinfacht den Prozess der Personalisierung und Inhaltsverbesserung, indem Sie den Inhalt durch eine Beschreibung dessen, was Sie generieren möchten, anpassen können."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Kontext mit dem AI-Assistenten definieren"
>abstract="Um den ausgewählten Inhalt als Eingabe für die Inhaltserstellung zu verwenden, aktivieren Sie die **Originalinhalt verwenden** umschalten. Sie können Ihre Marken-Assets auch hochladen, um sie als Quelle zu verwenden. Wenn Sie den ausgewählten Inhalt nicht verwenden, ist das Hochladen und Auswählen von Marken-Assets obligatorisch."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe Generische KI-Begriffe"
>abstract="Der Zugriff auf diese Funktion unterliegt Ihrer Zustimmung zu den Adobe Experience Cloud Generative AI-Benutzerrichtlinien. Eingabeaufforderungen, Kontextdaten, zusätzliche Informationen oder andere Eingaben, die Sie für diese Funktion bereitstellen, müssen an einen bestimmten Kontext gebunden sein, der Ihre Branding-Materialien, Website-Inhalte, Daten, Schemata für solche Daten, Vorlagen oder andere vertrauenswürdige Dokumente umfassen kann und keine personenbezogenen Daten enthalten darf (personenbezogene Daten umfassen alles, was mit einer bestimmten Person verknüpft werden kann). Sie sollten alle Ausgaben dieser Funktion auf ihre Richtigkeit hin überprüfen und sicherstellen, dass sie für Ihren Anwendungsfall geeignet sind"
>additional-url="https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe Generative AI-Benutzerrichtlinien"

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

Der KI-Assistent in Adobe Journey Optimizer liefert proaktiv Vorschläge zur Variation von Text- und Bildinhalten. Er ist für die Kanäle E-Mail, Push-Benachrichtigungen und SMS-Kanäle verfügbar. Diese neue Funktion bietet eine auf Eingabeaufforderungen basierende Text- und Bildgenerierung. Die Bildgenerierung wird mit Adobe Firefly gehandhabt.

Sie können den KI-Assistenten in Journey Optimizer verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Generieren Sie mehrere Varianten und erstellen Sie ein Experiment, um sie zu vergleichen. Mit dem Journey Optimizer-Inhaltsexperiment können Sie mehrere Nachrichtenabwandlungen definieren, um zu messen, welche bei Ihrer Zielgruppe am besten ankommt. Sie haben die Möglichkeit, Inhalt oder Betreff des Versands zu variieren. Die Zielgruppe der Nachricht wird nach dem Zufallsprinzip jeder Abwandlung zugewiesen, um zu bestimmen, welche Abwandlung in Bezug auf die angegebene Metrik am besten funktioniert. Weiterführende Informationen zum Inhaltsexperiment finden Sie in [diesem Abschnitt](../campaigns/content-experiment.md).

## Leitlinien und Einschränkungen {#generative-guardrails}

Im Folgenden sind die allgemeinen Richtlinien zur Verwendung des KI-Assistenten in Journey Optimizer für die E-Mail-Generierung aufgeführt:

* Die Qualität des generierten Inhalts wird stark durch das von Ihnen definierte Marketingziel/die von Ihnen definierte Aufforderung beeinflusst. Verwenden Sie eine gut definierte Eingabeaufforderung für die korrekte Interpretation des GenAI-Modells. 
* Laden Sie Marken-Assets hoch, um genaue Informationen über Markeninhalte zu erhalten. Andernfalls basieren Inhalte auf öffentlich verfügbaren Informationen. Der hochgeladene Inhalt kann die folgenden Formate aufweisen: PDF-, JPEG-, PNG- oder ZIP-Dateien (mit unterstützten Dateiformaten).
* Die maximale Größe für hochgeladene Marken-Assets beträgt 50 MB. Größere Dateien oder viele Bilder können funktionieren, aber die Verarbeitungszeit wird verlängert.
* Verwenden Sie eine von Adobe Campaign erstellte E-Mail-Vorlage, vorzugsweise [integrierte E-Mail-Vorlagen](../email/use-email-templates.md), einer markenspezifischen Vorlage oder einer benutzerdefinierten Vorlage, um Ihren E-Mail-Inhalt zu erstellen. Eine E-Mail-Vorlage mit bis zu 8 bis 10 Bildern wird empfohlen.
* Achten Sie bei der Auswahl von Varianten darauf, alle problematischen Ausgaben mithilfe des Daumen-Up-, Daumen-Down- oder Flag-Symbols zu melden.
* Ihre Verwendung des KI-Assistenten unterliegt den Allgemeinen KI-Benutzerhandbüchern von Adobe Experience Cloud. [Weitere Informationen](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Die folgenden Einschränkungen gelten für den KI-Assistenten in Journey Optimizer:

* Unterstützte Sprache ist nur Englisch.
* Nur für die Kanäle E-Mail, Push und SMS verfügbar.
* GenAI-Inhalte sind möglicherweise nicht immer genau: Teilen Sie bitte Ihr Feedback mit, damit unsere Ingenieure die Modelle verfeinern können.
* Sie können mehrere Marken-Assets hochladen, jedoch nur eines für eine bestimmte Generation nutzen.

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
