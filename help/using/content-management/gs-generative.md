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
source-git-commit: 98ce21578d30ac50665561438715d19d1723f4a7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 89%

---

# Erste Schritte mit dem KI-Assistenten {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="Erstellen des E-Mail-Inhalts"
>abstract="Der KI-Assistent von Adobe Journey Optimizer bietet proaktiv Inhaltsvariantenvorschläge für Text und Bilder. Er ist für die Kanäle E-Mail, Push, SMS und Web verfügbar. Diese neue Funktion bietet eine auf Eingabeaufforderungen basierende Text- und Bildgenerierung."

>[!BEGINSHADEBOX]

**Inhaltsverzeichnis**

* **[Erste Schritte mit dem KI-Assistenten](gs-generative.md)**
* [Generierung von E-Mails mit dem KI-Assistenten](generative-email.md)
* [Generierung von SMS mit dem KI-Assistenten](generative-sms.md)
* [Push-Generierung mit dem AI-Assistenten](generative-push.md)
* [Inhaltsexperiment mit dem KI-Assistenten](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Der KI-Assistent von Adobe Journey Optimizer ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Der KI-Assistent von Adobe Journey Optimizer bietet proaktiv Inhaltsvariantenvorschläge für Text und Bilder. Sie ist für die Kanäle E-Mail, Push und SMS verfügbar. Diese neue Funktion bietet eine auf Eingabeaufforderungen basierende Text- und Bildgenerierung. Die Bildgenerierung wird mit Adobe Firefly gehandhabt.

Sie können den KI-Assistenten in Journey Optimizer verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Generieren Sie mehrere Varianten und erstellen Sie ein Experiment, um sie zu vergleichen. Mit dem Journey Optimizer-Inhaltsexperiment können Sie mehrere Nachrichtenabwandlungen definieren, um zu messen, welche bei Ihrer Zielgruppe am besten ankommt. Sie haben die Möglichkeit, Inhalt oder Betreff des Versands zu variieren. Die Zielgruppe der Nachricht wird nach dem Zufallsprinzip jeder Abwandlung zugewiesen, um zu bestimmen, welche Abwandlung in Bezug auf die angegebene Metrik am besten funktioniert. Weiterführende Informationen zum Inhaltsexperiment finden Sie in [diesem Abschnitt](../campaigns/content-experiment.md).

## Leitlinien und Einschränkungen {#generative-guardrails}

Die allgemeinen Richtlinien für die Verwendung des AI-Assistenten in Journey Optimizer zur E-Mail-Generierung sind unten aufgeführt:

* Die Qualität des generierten Inhalts wird stark durch das von Ihnen definierte Marketing-Ziel bzw. die von Ihnen definierte Eingabeaufforderung beeinflusst. Verwenden Sie eine gut definierte Eingabeaufforderung, damit das generative KI-Modell korrekt implementiert wird. 
* Laden Sie Marken-Assets hoch, um genaue Informationen zu Markeninhalten zu haben. Andernfalls basieren Inhalte auf öffentlich verfügbaren Informationen. Der hochgeladene Inhalt kann folgende Formate haben: PDF-, JPEG-, PNG- oder ZIP-Dateien (mit unterstützten Dateiformaten).
* Die maximale Größe für hochgeladene Marken-Assets beträgt 50 MB. Größere Dateien oder viele Bilder können funktionieren, aber die Verarbeitungszeit verlängert sich.
* Verwenden Sie eine von Adobe Campaign erstellte E-Mail-Vorlage oder vorzugsweise eine der [integrierten E-Mail-Vorlagen](../email/use-email-templates.md), eine markenspezifische oder benutzerdefinierte Vorlage, um Ihren E-Mail-Inhalt zu erstellen. Es wird eine E-Mail-Vorlage mit 8 bis 10 Bildern empfohlen.
* Denken Sie daran, problematische Ausgaben zu melden, indem Sie bei der Auswahl von Varianten die Symbole mit dem Daumen nach oben, dem Daumen nach unten oder andere Kennzeichnungssymbole verwenden.
* Ihre Nutzung des KI-Assistenten unterliegt den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. [Weitere Informationen](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Die folgenden Einschränkungen gelten für den AI-Assistenten in Journey Optimizer:

* Unterstützte Sprache ist nur Englisch.
* Nur für den E-Mail-, Push- und SMS-Kanal verfügbar.
* Generative KI-Inhalte sind möglicherweise nicht immer genau: Teilen Sie uns bitte ggf. Ihr Feedback mit, damit unsere Ingenieurinnen und Ingenieure die Modelle präzisieren können.
* Sie können mehrere Marken-Assets hochladen, jedoch für eine bestimmte Generierung nur eines verwenden.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Generierung von E-Mails" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>E-Mail-Erzeugung</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Generierung von SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>SMS-Generierung</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Generierung von Push-Benachrichtungen" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Generieren von Push-Benachrichtigungen</strong></a>
</div>
<p></td>
</tr></table>
