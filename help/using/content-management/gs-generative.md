---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit dem KI-Assistenten in Journey Optimizer
description: Erfahren Sie, wie Sie auf den KI-Assistenten in Journey Optimizer zugreifen und damit arbeiten
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: ht
source-wordcount: '866'
ht-degree: 100%

---

# Erste Schritte mit dem KI-Assistenten {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="KI-Assistent in Journey Optimizer"
>abstract="Nachdem Sie den Versand erstellt und personalisiert haben, können Sie den KI-Assistenten in Journey Optimizer verwenden, um die Inhalte zu verbessern. Diese Funktion vereinfacht den Prozess der Personalisierung und Verbesserung der Inhalte, da diese durch eine Beschreibung dessen, was generiert werden soll, genauer angepasst werden können."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Hochladen von Marken-Assets"
>abstract="Mit dem Menü „Marken-Asset hochladen“ können Sie ein beliebiges Marken-Asset hinzufügen, das Inhalte enthält, die zusätzlichen Kontext für den KI-Assistenten in Journey Optimizer bieten. Die Auswahl eines zuvor hochgeladenen Assets ist ebenfalls möglich. Diese Option stellt sicher, dass der KI-Assistent Zugriff auf alle erforderlichen Materialien hat, wodurch seine Funktionalität und Relevanz verbessert werden."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Bedingungen der generativen KI in Adobe"
>abstract="Der Zugriff auf diese Funktion unterliegt der Zustimmung zu den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. Alle Ausgaben dieser Funktion auf ihre Richtigkeit überprüfen und sicherstellen, dass sie für den Anwendungsfall geeignet sind."
>additional-url="https://www.adobe.com/de/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Benutzerrichtlinien für generative KI in Adobe"

>[!INFO]
>
>Nehmen Sie an unserer [Live-Funktionsvorstellung](https://experienceleague.adobe.com/de/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"} teil, um die Funktionen in der Praxis selbst zu erkunden und die vielfältigen Einsatzmöglichkeiten zu verstehen.


Der KI-Assistent in Adobe Journey Optimizer, der von Microsoft Azure OpenAI und Adobe Firefly unterstützt wird, liefert proaktiv Vorschläge zur Variation von Text- und Bildinhalten. Diese neue Funktion bietet eine **auf Prompts basierende Text- und Bildgenerierung**. Die Bildgenerierung wird von Adobe Firefly vewaltet.

Der KI-Assistent unterstützt die Generierung **in mehreren Sprachen**, sodass Sie unterschiedliche globale Zielgruppen erreichen und ansprechen können. Der KI-Assistent ist in den folgenden Sprachen verfügbar:

<table style="table-layout:fixed; margin-top: 0px; margin-bottom: 0px;">
  <tbody>
    <tr style="border: 0;background-color: #FFFFFF;">
      <td>
        <ul>
          <li>Französisch</li>
          <li>Spanisch</li>
          <li>Deutsch</li>
          <li>Italienisch</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Japanisch</li>
          <li>Schwedisch</li>
          <li>Niederländisch</li>
          <li>Norwegisch</li>
        </ul>
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

Sie können den KI-Assistenten in Adobe Journey Optimizer verwenden, um die Wirkung Ihrer Nachricht zu optimieren, indem Sie mit verschiedenen Haupttiteln und Bildern experimentieren. Generieren Sie mehrere Varianten und erstellen Sie ein Experiment, um sie zu vergleichen. Mit dem **Journey Optimizer-Inhaltsexperiment** können Sie mehrere Nachrichtenabwandlungen definieren, um zu messen, welche bei Ihrer Zielgruppe am besten ankommt. Sie haben die Möglichkeit, Inhalt oder Betreff des Versands zu variieren. Die Zielgruppe der Nachricht wird nach dem Zufallsprinzip jeder Abwandlung zugewiesen, um zu bestimmen, welche Abwandlung in Bezug auf die angegebene Metrik am besten funktioniert. Weiterführende Informationen zum Inhaltsexperiment finden Sie in [diesem Abschnitt](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Bevor Sie mit der Verwendung dieser Funktion beginnen, lesen Sie die entsprechenden Informationen zu [Schutzmechanismen und Einschränkungen](#generative-guardrails).
>
>
>* Sie müssen einer [Benutzervereinbarung](https://www.adobe.com/de/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} zustimmen, bevor Sie den KI-Assistenten in Adobe Journey Optimizer verwenden können. Weitere Informationen erhalten Sie beim Adobe-Support.

## Zugriff auf den KI-Assistenten {#generative-access}

Um auf den KI-Assistenten in Adobe Journey Optimizer zugreifen zu können, müssen Benutzende über die Berechtigung **Inhalt generieren** verfügen. [Weitere Informationen](../administration/permissions.md)

+++  Erfahren Sie, wie Sie Berechtigungen zur Inhaltserstellung zuweisen.

1. Gehen Sie im Produkt **Berechtigungen** zur Registerkarte **Rollen** und wählen Sie die gewünschte **Rolle** aus.

1. Klicken Sie auf **Bearbeiten**, um die Berechtigungen zu ändern.

1. Fügen Sie die Ressource **KI-Assistent** hinzu und wählen Sie dann aus dem Dropdown-Menü die Option **Inhalt generieren** aus.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Klicken Sie auf **Speichern**, um die Änderungen anzuwenden.

   Die Berechtigungen aller Benutzenden, die dieser Rolle bereits zugewiesen sind, werden automatisch aktualisiert.

1. Um diese Rolle neuen Benutzenden zuzuweisen, navigieren Sie im Dashboard **Rollen** zur Registerkarte **Benutzer** und klicken Sie auf **Benutzer hinzufügen**.

1. Geben Sie den Namen und die E-Mail-Adresse der Benutzerin oder des Benutzers ein oder wählen Sie aus der Liste aus und klicken Sie dann auf **Speichern**.

1. Wenn die Benutzerin bzw. der Benutzer vorher noch nicht erstellt wurde, lesen Sie [diese Dokumentation](https://experienceleague.adobe.com/de/docs/experience-platform/access-control/abac/permissions-ui/users).

Die Benutzerin oder der Benutzer erhält eine E-Mail mit Anweisungen zum Zugriff auf Ihre Instanz.

+++

## Leitlinien und Einschränkungen {#generative-guardrails}

Im Folgenden sind die allgemeinen Richtlinien zur Verwendung des KI-Assistenten in Adobe Journey Optimizer für die E-Mail-Generierung aufgeführt:

* Die Qualität des generierten Inhalts wird stark durch das von Ihnen definierte Marketing-Ziel bzw. den von Ihnen definierten Prompt beeinflusst. Verwenden Sie einen gut definierten Prompt, damit das GenAI-Modell diesen korrekt interpretieren kann. 
* Laden Sie Marken-Assets hoch, damit die Informationen über Markeninhalte exakt sind. Andernfalls basieren die Inhalte auf öffentlich verfügbaren Informationen. Die hochgeladenen Inhalte können die folgenden Formate aufweisen: PDF-, JPEG-, PNG- oder ZIP-Dateien (mit unterstützten Dateiformaten).
* Die maximale Größe für hochgeladene Marken-Assets beträgt 50 MB. Größere Dateien oder viele Bilder können funktionieren, aber die Verarbeitungszeit verlängert sich.
* Verwenden Sie eine markenspezifische oder benutzerdefinierte Vorlage, um E-Mail-Inhalte mit dem KI-Assistenten in Adobe Journey Optimizer zu erstellen. Es werden E-Mail-Vorlagen mit 8 bis 10 Bildern empfohlen.
* Vergewissern Sie sich, dass Sie problematische Ausgaben melden, indem Sie bei der Auswahl von Varianten die Symbole Daumen nach oben, Daumen nach unten oder Flagge verwenden.
* Die Verwendung des KI-Assistenten unterliegt den Benutzerrichtlinien für generative KI in Adobe Experience Cloud. [Weitere Informationen](https://www.adobe.com/de/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Im Zuge seiner Selbstverpflichtung zur Förderung von Transparenz bei der Nutzung generativer KI-Tools zur Medienerstellung wendet Adobe Content Credentials an, wenn Inhalte oder Projekte mit einem Firefly-generierten Asset heruntergeladen oder exportiert werden. [Weitere Informationen](https://helpx.adobe.com/de/firefly/using/content-credentials.html)

Die folgenden Einschränkungen gelten für den KI-Assistenten in Adobe Journey Optimizer:

* Der Assistent ist nur für den E-Mail-, Push- und SMS-Kanal verfügbar.
* GenAI-Inhalte sind möglicherweise nicht immer genau: Bitte teilen Sie uns Ihr Feedback mit, damit unsere Ingenieurinnen und Ingenieure die Modelle verfeinern können.
* Sie können mehrere Marken-Assets hochladen, jedoch nur eines für eine bestimmte Generierung nutzen.


## Funktionen des KI-Assistenten zur Inhaltserstellung {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-full-content.md">
<img alt="Generieren von vollständigen Inhalten" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-full-content.md"><strong>Generieren von vollständigen Inhalten</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-text.md">
<img alt="Textgenerierung" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div><a href="generative-text.md"><strong>Generieren von Text</strong>
</div>
<p>
</td>
<td>
<a href="generative-image.md">
<img alt="Bildgenerierung" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div>
<a href="generative-image.md"><strong>Generieren von Bildern</strong></a>
</div>
<p></td>
</tr></table>

## Weitere Ressourcen

* **[Generatives Experimentieren](generative-experimentation.md)** – Erfahren Sie, wie Sie KI-generierten Inhalt mit Experimenten kombinieren.
* **[Anwendungsfälle für den KI-Assistenten](generative-uc.md)** – Erfahren Sie durch Anwendungsfälle, wie Sie den KI-Assistenten verwenden
* **[Tutorials zum KI-Assistenten](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/ai-assistant){target="_blank"}** – Erkunden Sie die detaillierten Video-Tutorials mit Funktionen und Best Practices für den KI-Assistenten.
