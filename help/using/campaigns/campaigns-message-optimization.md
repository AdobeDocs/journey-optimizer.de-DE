---
solution: Journey Optimizer
product: journey optimizer
title: Optimierung von Nachrichten
description: Nutzen Sie die Optimierung von Nachrichten, um personalisierte und optimierte Marketing-Kampagnen zu erstellen.
role: User
level: Intermediate
keywords: Kampagnenoptimierung, Experimentieren, Targeting, A/B-Tests
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 4d7ad2c3ed71801298f1afe31d0e29d7bb1d5c7f
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 5%

---

# Optimierung in Kampagnen {#message-optimization}

Die Optimierung bietet Tools zur Bereitstellung personalisierter und optimierter Inhalte für die Zielgruppen Ihrer Kampagnen (<!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)--> maximale Interaktion und maximalen Erfolg, um hocheffektive <!--customized and --> zu erstellen).

Mit der Optimierung können Sie:

* Nutzen [Targeting](#targeting)-Regeln
* Ausführen [Inhaltsexperimenten](#experimentation)
* Verwenden [erweiterter Kombinationen](#combination) von Experimentieren und Targeting in einer einzigen Kampagne

Sobald die Kampagne live ist, werden die Profile anhand der definierten Kriterien bewertet, und basierend auf den passenden Kriterien wird ihnen das entsprechende Erlebnis oder der entsprechende Inhalt aus der Kampagne bereitgestellt.

Der Unterschied zwischen Experimenten und Zielgruppenbestimmung lässt sich wie folgt umreißen:

* Experimentieren besteht in einer zufälligen Aufteilung der Bereitstellung von Inhalten basierend auf der Traffic-Zuordnung&#x200B;.
* Beim Targeting werden deterministische Techniken verwendet, um Inhalte basierend auf Benutzerprofil, Zielgruppenzugehörigkeit oder kontextbasierten Regeln bereitzustellen.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Verwenden von Targeting {#targeting}

Beim Targeting werden auf der Grundlage von Benutzerprofilattributen oder kontextuellen Attributen personalisierte Inhalte für bestimmte Zielgruppensegmente bereitgestellt.

Im Gegensatz zu Experimenten, bei denen es sich um eine zufällige Zuweisung des Inhalts einer Nachricht handelt, ist die Zielgruppenbestimmung in Bezug auf die Bereitstellung des Inhalts für die richtige Zielgruppe deterministisch.

Beim Targeting können spezifische Regeln definiert werden, die auf Folgendem basieren:

* **Benutzerprofilattribute** wie Speicherort (z. B. Geotargeting), Alter oder Voreinstellungen. In den USA wird beispielsweise eine „Golden Gate“-Promotion angeboten, in Frankreich hingegen eine „Eiffelturm“-Promotion.

* **Kontextdaten** wie Gerätetyp (z. B. Geräte-Targeting), Tageszeit oder Sitzungsdetails. Desktop-Benutzer erhalten beispielsweise Desktop-optimierte Inhalte, während mobile Benutzer Mobile-optimierte Inhalte erhalten.

* **Zielgruppen** mit denen Profile mit einer bestimmten Zielgruppenzugehörigkeit ein- oder ausgeschlossen werden können.

Gehen Sie wie folgt vor, um die Zielgruppenbestimmung in einer Kampagne einzurichten.

1. Erstellen einer Kampagne. [Weitere Informationen](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Wählen Sie auf **[!UICONTROL Registerkarte]** Aktionen“ mindestens eine Aktion aus.

1. Wählen Sie im **[!UICONTROL Nachrichtenoptimierung]** die Option **[!UICONTROL Targeting]**.

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. Verwenden Sie den Regel-Builder, um Ihre Kriterien zu definieren. Definieren Sie beispielsweise eine Regel für in den USA ansässige Personen, eine Regel für in Frankreich ansässige Personen und eine Regel für in Indien ansässige Personen.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Wählen Sie **[!UICONTROL Fallback-Inhalt aktivieren]** nach Bedarf aus. Mit Fallback-Inhalten kann Ihre Zielgruppe Standardinhalte empfangen, wenn keine Targeting-Regeln qualifiziert sind. Wenn Sie diese Option nicht auswählen, erhält jede Zielgruppe, die sich nicht für eine der oben definierten Zielgruppenbestimmungsregeln qualifiziert, keine Inhalte.

1. Speichern Sie Ihre Einstellungen für die Zielgruppenregel.

1. Zurück in der **[!UICONTROL (Aktionen]** wählen Sie **[!UICONTROL Inhalt bearbeiten]**.

1. Entwerfen Sie geeignete Inhalte für jede Gruppe, die durch die Einstellungen Ihrer Zielgruppenbestimmungsregeln definiert wird.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   In diesem Beispiel erstellen wir einen bestimmten Inhalt für US-Bürger, einen anderen Inhalt für in Frankreich ansässige Personen und einen anderen Inhalt für in Indien ansässige Personen.

1. [Aktivieren](review-activate-campaign.md) Ihrer Kampagne.

Sobald die Kampagne live ist, werden Inhalte gesendet, die auf die einzelnen Zielgruppen zugeschnitten sind, sodass die US-Bürger eine bestimmte Nachricht erhalten, die Bewohner Frankreichs eine andere Nachricht und so weiter.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## Experimentieren verwenden {#experimentation}

Mit Experimenten können Sie mehrere Versionen von Inhalten testen, um anhand vordefinierter Erfolgsmetriken zu bestimmen, welche am besten funktioniert.

Gehen Sie wie folgt vor, um das Experimentieren in einer Kampagne einzurichten.

Angenommen, Sie möchten die folgenden Werbenachrichten in einer Kampagne testen:

* **Abwandlung A**: „20 % Rabatt auf Ihren nächsten Kauf“
* **Abwandlung B**: „Kostenloser Versand bei Bestellungen über 50 $&quot;
* **Behandlung C**: „Erhalten Sie Ihre 10-Dollar-Geschenkkarte“

Gehen Sie wie folgt vor, um ein Experiment einzurichten und zu bestimmen, welche Nachricht die meisten Käufe antreibt.

1. Erstellen einer Kampagne. [Weitere Informationen](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Wählen Sie auf **[!UICONTROL Registerkarte]** mindestens zwei eingehende Aktionen aus, z. B. [Code-basiertes Erlebnis](../code-based/get-started-code-based.md) und [In-App](../../rp_landing_pages/in-app-landing-page.md).

1. Wählen Sie **[!UICONTROL Abschnitt]** Nachrichtenoptimierung“ **[!UICONTROL Experimentieren]** aus.

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Entwerfen und konfigurieren Sie Ihr Inhaltsexperiment nach Bedarf. [Weitere Informationen](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Sobald das Experiment definiert ist, gilt es für alle in diese Kampagne eingefügten Aktionen, d. h. dieselben Kundinnen und Kunden sehen auf allen Oberflächen dieselben Angebote.

   >[!NOTE]
   >
   >Sie können auch andere Aktionen auswählen: Das Experiment gilt für alle Aktionen, die der Kampagne hinzugefügt werden.

1. [Aktivieren](review-activate-campaign.md) Ihrer Kampagne.

Sobald die Kampagne live ist, werden den Benutzern nach dem Zufallsprinzip die verschiedenen Inhaltsvarianten zugewiesen. [!DNL Journey Optimizer] verfolgt, welche Varianz zu mehr Käufen führt, und bietet umsetzbare Einblicke.

Verfolgen Sie den Erfolg Ihrer Kampagne mit dem [Experimentierkampagnenbericht](../reports/campaign-global-report-cja-experimentation.md).

## Kombinieren von Targeting und Experimentieren {#combination}

Journey Optimizer ermöglicht es Ihnen auch, Zielgruppenbestimmungen und Experimente innerhalb einer Kampagne zu kombinieren, um komplexere Strategien zu erstellen.

Sie können Targeting verwenden, um mehrere Varianten zu erstellen, und für jede Variante Experimente verwenden, um jeden Inhalt weiter zu optimieren. Dadurch wird sichergestellt, dass die Experimente für jede Zielgruppenbestimmungsregel spezifisch sind und sich nicht über Varianten innerhalb der Kampagne erstrecken.

Sie können beispielsweise eine „50 % Rabatt auf eine Promotion“ gegenüber einer „50 $ Geschenkkarte“ für Kunden in den USA testen und einen anderen Test für Kunden in Europa durchführen, z. B. „kostenloser Versand bei Bestellungen über 50 €&quot; gegenüber „20 % Rabatt auf ihren nächsten Kauf“.

Gehen Sie wie folgt vor, um Zielgruppenbestimmungen und Experimente in einer Kampagne zu kombinieren.

1. Erstellen Sie eine Kampagne, in der Sie mehrere Zielgruppenbestimmungsregeln definieren. [Weitere Informationen](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Erstellen Sie ein Experiment für die erste Zielgruppenbestimmungsregel.

1. Entwerfen und konfigurieren Sie Ihr Inhaltsexperiment nach Bedarf. [Weitere Informationen](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Sobald das Experiment definiert ist, gilt es nur für die erste Zielgruppenbestimmungsregel.

1. Zurück in der **[!UICONTROL (Aktionen]** wählen Sie **[!UICONTROL Inhalt bearbeiten]**.

1. Für die Gruppe, die in Ihrer ersten Zielgruppenbestimmungsregel definiert ist, können Sie für jede Variante Ihres Experiments einen bestimmten Inhalt definieren.

   Wenn Sie Ihrer Kampagne mehr als eine eingehende Aktion hinzugefügt haben, gilt für jede Aktion dieselbe Kombination aus Zielgruppenbestimmung und Experiment. Sie müssen jedoch für jede Variante jeder Aktion einen spezifischen Inhalt definieren.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Gehen Sie für die anderen Targeting-Regeln ähnlich vor und entwerfen Sie den entsprechenden Inhalt für jede Variante.

1. Speichern Sie Ihre Änderungen und [ Sie ](review-activate-campaign.md) Kampagne.

Sobald die Kampagne live ist, werden den Benutzern der einzelnen Zielgruppen nach dem Zufallsprinzip die verschiedenen Inhaltsvarianten zugewiesen, die für die Gruppe definiert wurden, der sie angehören.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->
