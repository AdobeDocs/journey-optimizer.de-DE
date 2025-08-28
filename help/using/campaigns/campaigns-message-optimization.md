---
solution: Journey Optimizer
product: journey optimizer
title: Nachrichtenoptimierung
description: Nutzen Sie die Optimierung von Nachrichten, um personalisierte und optimierte Marketing-Journey und -Kampagnen zu erstellen.
role: User
level: Intermediate
keywords: Kampagnenoptimierung, Experimente, Targeting, A/B-Tests
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: a770cbc1736e7add7e25f2cc8210d81bd8b2e375
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 56%

---

# Optimierung in Kampagnen und Journey {#message-optimization}

Die Optimierung bietet Tools zur Bereitstellung personalisierter und optimierter Inhalte für Ihre Zielgruppe (<!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)--> maximale Interaktion und Erfolg, um hocheffektive Journey und Kampagnen <!--customized and --> erstellen).

Mit der Optimierung können Sie:

* [Targeting](#targeting)-Regeln nutzen
* [Inhaltsexperimente](#experimentation) ausführen
* [Erweiterte Kombinationen](#combination) aus Experimenten und Targeting in einer Kampagne nutzen

Sobald die Journey oder Kampagne live ist, werden die Profile anhand der definierten Kriterien bewertet. Anhand übereinstimmender Kriterien werden sie mit dem entsprechenden Erlebnis oder Inhalt aus der Journey/Kampagne bereitgestellt.

Der Unterschied zwischen Experimenten und Targeting lässt sich wie folgt umreißen:

* Experimente bestehen in einer zufälligen Aufteilung der Bereitstellung von Inhalten je nach Traffic-Zuordnung.
* Beim Targeting werden deterministische Techniken verwendet, um Inhalte anhand von Benutzerprofil, Zielgruppenzugehörigkeit oder kontextbasierten Regeln bereitzustellen.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

➡️ [Weitere Informationen zur Optimierung einer Kampagne finden Sie in diesem Video](#video)

## Verwenden von Targeting {#targeting}

Beim Targeting werden auf der Grundlage von Benutzerprofilattributen oder kontextuellen Attributen personalisierte Inhalte für bestimmte Zielgruppensegmente bereitgestellt.

Im Gegensatz zu Experimenten, bei denen es sich um eine zufällige Zuweisung des Inhalts einer Nachricht handelt, ist das Targeting in Bezug auf die Bereitstellung der Inhalte für die richtige Zielgruppe deterministisch.

Beim Targeting können spezifische Regeln definiert werden, die auf Folgendem basieren:

* **Benutzerprofilattribute** wie Standort (z. B. Geotargeting), Alter oder Präferenzen. In den USA wird Benutzenden beispielsweise eine „Golden Gate“-Promotion angeboten, in Frankreich hingegen eine „Eiffelturm“-Promotion.

* **Kontextdaten** wie Gerätetyp (z. B. Geräte-Targeting), Tageszeit oder Sitzungsdetails. Beispielsweise erhalten Desktop-Benutzende für den Desktop optimierte Inhalte, während mobile Benutzende für Mobilgeräte optimierte Inhalte erhalten.

* **Zielgruppen**, mit deren Hilfe Profile mit einer bestimmten Zielgruppenzugehörigkeit ein- oder ausgeschlossen werden können.

Gehen Sie wie folgt vor, um die Zielgruppenbestimmung einzurichten.

1. Erstellen Sie eine [Journey](../building-journeys/journey-gs.md#jo-build) oder eine [Kampagne](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Wenn Sie sich auf einer Journey befinden, fügen Sie eine Aktivität **[!UICONTROL Aktion]** hinzu, wählen Sie eine Kanalaktivität aus und wählen Sie **[!UICONTROL Aktion konfigurieren]**. [Weitere Informationen](../building-journeys/journey-action.md#add-action)

1. Wählen Sie auf der Registerkarte **[!UICONTROL Aktionen]** mindestens eine Aktion aus.

1. Wählen **[!UICONTROL Abschnitt]** Optimierung“ die Option **[!UICONTROL Zielgruppenbestimmungsregel erstellen]** aus.

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. Verwenden Sie den Regel-Builder, um Ihre Kriterien festzulegen. Definieren Sie beispielsweise eine Regel für in den USA ansässige Personen, eine Regel für in Frankreich ansässige Personen und eine Regel für in Indien ansässige Personen.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Wählen Sie nach Bedarf **[!UICONTROL Fallback-Inhalte aktivieren]** aus. Mit Fallback-Inhalten kann Ihre Zielgruppe Standardinhalte empfangen, wenn keine Targeting-Regeln qualifiziert sind.

   >[!NOTE]
   >
   >Falls Sie diese Option nicht auswählen, erhält jede Zielgruppe, die sich nicht für eine der oben definierten Targeting-Regeln qualifiziert, keine Inhalte.

1. Speichern Sie Ihre Einstellungen für die Targeting-Regel.

1. Zurück in der **[!UICONTROL Aktionen]** wählen Sie **[!UICONTROL Inhalt bearbeiten]**.

1. Gestalten Sie geeignete Inhalte für jede Gruppe, die durch die Einstellungen Ihrer Targeting-Regeln definiert wird.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   In diesem Beispiel erstellen wir einen bestimmten Inhalt für in den USA ansässige Personen, einen anderen Inhalt für in Frankreich ansässige Personen und einen dritten Inhalt für in Indien ansässige Personen.

1. [Aktivieren](review-activate-campaign.md) Sie Ihren Journey oder Ihre Kampagne.

Sobald die Journey/Kampagne live ist, werden Inhalte gesendet, die auf die einzelnen Zielgruppen zugeschnitten sind, sodass die Einwohner der USA eine bestimmte Nachricht erhalten, die Einwohner Frankreichs eine andere Nachricht und so weiter.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## Verwenden von Experimenten {#experimentation}

Mit Experimenten können Sie verschiedene Varianten von Inhalten testen, um anhand vordefinierter Erfolgsmetriken zu bestimmen, welche am besten funktioniert.

Gehen Sie wie folgt vor, um Experimente einzurichten.

Angenommen, Sie möchten die folgenden Werbenachrichten in einer Kampagne testen:

* **Abwandlung A**: „20 % Rabatt auf Ihren nächsten Kauf“
* **Abwandlung B**: „Kostenloser Versand bei Bestellungen über 50 €“
* **Abwandlung C**: „Erhalten Sie eine Geschenkkarte im Wert von 10 €“

Gehen Sie wie folgt vor, um ein Experiment einzurichten und zu bestimmen, welche Nachricht für die meisten Käufe sorgt.

1. Erstellen Sie eine [Journey](../building-journeys/journey-gs.md#jo-build) oder eine [Kampagne](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Wenn Sie sich auf einer Journey befinden, fügen Sie eine Aktivität **[!UICONTROL Aktion]** hinzu, wählen Sie eine Kanalaktivität aus und wählen Sie **[!UICONTROL Aktion konfigurieren]**. [Weitere Informationen](../building-journeys/journey-action.md#add-action)

1. Wählen Sie auf **[!UICONTROL Registerkarte]** Aktionen“ zwei eingehende Aktionen aus, beispielsweise [Code-basiertes Erlebnis](../code-based/get-started-code-based.md) und [In-App](../../rp_landing_pages/in-app-landing-page.md).

1. Wählen Sie **[!UICONTROL Abschnitt]** Optimierung“ **[!UICONTROL Experiment erstellen]** aus.

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Entwerfen und konfigurieren Sie Ihr Inhaltsexperiment nach Bedarf. [Weitere Informationen](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Sobald das Experiment definiert ist, gilt es für alle Aktionen, die in diese Kampagne oder über die Aktivität Journey **[!UICONTROL Action]** eingefügt wurden. Das bedeutet, dass dieselben Kundinnen und Kunden auf allen Oberflächen dieselben Angebote sehen.

   >[!NOTE]
   >
   >Sie können auch andere Aktionen auswählen: Das Experiment gilt für alle Aktionen, die der Kampagne oder der Journey-Aktion hinzugefügt werden.

1. [Aktivieren](review-activate-campaign.md) Sie Ihren Journey oder Ihre Kampagne.

Sobald die Journey/Kampagne live ist, werden den Benutzenden nach dem Zufallsprinzip die verschiedenen Inhaltsvarianten zugewiesen. [!DNL Journey Optimizer] verfolgt, welche Variante zu mehr Käufen führt, und stellt verwertbare Erkenntnisse zur Verfügung.

Verfolgen Sie den Erfolg Ihrer Kampagne mit den Berichten [Journey](../reports/journey-global-report-cja.md) und [Kampagne](../reports/campaign-global-report-cja-experimentation.md). <!--Link to Experimentation journey reportis missing-->

## Kombinieren von Targeting und Experimenten {#combination}

Journey Optimizer ermöglicht es Ihnen auch, Zielgruppenbestimmungen und Experimente innerhalb einer Journey oder Kampagne zu kombinieren, um komplexere Strategien zu erstellen.

Sie können das Targeting nutzen, um verschiedene Varianten einzurichten, und für jede Variante Experimente verwenden, um die jeweiligen Inhalte weiter zu optimieren. Dadurch wird sichergestellt, dass Experimente für jede Zielgruppenbestimmungsregel spezifisch sind und sich nicht über Varianten erstrecken.

Sie können beispielsweise eine „Promotion mit 50 % Rabatt“ gegenüber einer „Geschenkkarte im Wert von 50 Dollar“ für Kundschaft in den USA testen und für Kundschaft in Europa einen anderen Test durchführen, z. B. „kostenloser Versand bei Bestellungen über 50 €“ gegenüber „20 % Rabatt auf ihren nächsten Kauf“.

Gehen Sie wie folgt vor, um Zielgruppenbestimmungen und Experimente auf einer Journey oder in einer Kampagne zu kombinieren.

1. Erstellen Sie eine Journey oder eine Kampagne, in der bzw. der Sie mehrere Zielgruppenbestimmungsregeln definieren. [Weitere Informationen](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Erstellen Sie ein Experiment für die erste Targeting-Regel.

1. Entwerfen und konfigurieren Sie Ihr Inhaltsexperiment nach Bedarf. [Weitere Informationen](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Sobald das Experiment definiert ist, gilt es nur für die erste Targeting-Regel.

1. Zurück in der **[!UICONTROL Aktionen]** wählen Sie **[!UICONTROL Inhalt bearbeiten]**.

1. Für die Gruppe, die in Ihrer ersten Targeting-Regel definiert ist, können Sie für jede Variante Ihres Experiments einen bestimmten Inhalt definieren.

   Wenn Sie Ihrer Journey oder Kampagne mehr als eine eingehende Aktion hinzugefügt haben, gilt für jede Aktion dieselbe Kombination aus Zielgruppenbestimmung und Experiment. Sie müssen jedoch für jede Variante von jeder Aktion einen spezifischen Inhalt definieren.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Gehen Sie für die anderen Targeting-Regeln genauso vor und entwerfen Sie den entsprechenden Inhalt für die einzelnen Varianten.

1. Speichern Sie Ihre Änderungen und [ Sie ](review-activate-campaign.md) Journey oder Ihre Kampagne (aktivieren).

Sobald die Journey/Kampagne live ist, werden den Benutzerinnen und Benutzern aus jeder Zielgruppe nach dem Zufallsprinzip die verschiedenen Inhaltsvarianten zugewiesen, die für die Gruppe definiert wurden, der sie angehören.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

## Anleitungsvideo{#video}

Erfahren Sie, wie Sie die Nachrichtenoptimierung in durch eine Aktion oder durch API ausgelösten Kampagnen nutzen. Sie erfahren, wie Sie Teilzielgruppen ansprechen, Nachrichtenvarianten je nach Standort erstellen, Fallback-Inhalte aktivieren und mehrere Experimente innerhalb einer Kampagne durchführen. In diesem Tutorial wird auch beschrieben, wie Sie Multi-Channel-Kampagnen verwalten und dabei die Konsistenz der Nachrichten beibehalten können.

>[!VIDEO](https://video.tv.adobe.com/v/3470368?quality=12)