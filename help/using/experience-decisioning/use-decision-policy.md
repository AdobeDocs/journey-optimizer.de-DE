---
title: Verwenden von Entscheidungsrichtlinien in Nachrichten
description: Erfahren Sie, wie Sie Entscheidungsrichtlinien in Ihren Nachrichten verwenden.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
source-git-commit: 708c67796974e019417efbf086ab60d26dfca866
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 10%

---

# Verwenden von Entscheidungsrichtlinien in Nachrichten {#create-decision}

Nachdem Sie Ihrem Inhalt eine Entscheidungsrichtlinie hinzugefügt haben, können Sie Attribute aus zurückgegebenen Entscheidungselementen zur Personalisierung verwenden. Fügen Sie dazu zunächst den Entscheidungsrichtlinien-Code in Ihren Inhalt ein.

>[!CAUTION]
>
>Entscheidungsrichtlinien stehen allen Kunden für die Kanäle **Code-basiertes Erlebnis**, **SMS** und **Push-Benachrichtigung** zur Verfügung.
>
>Die Entscheidungsfindung für den **E-Mail**-Kanal ist nur in begrenzter Verfügbarkeit verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Weitere Informationen zu [Verfügbarkeitskennzeichnungen](../rn/releases.md#availability-labels).

## Einfügen des Entscheidungsrichtlinien-Codes {#insert}

>[!BEGINTABS]

>[!TAB Code-basiertes Erlebnis]

1. Bearbeiten Sie Ihr Code-basiertes Erlebnis und navigieren Sie zu **[!UICONTROL Entscheidungsrichtlinie]**.

2. Wählen **[!UICONTROL Richtlinie einfügen]**, um den Entscheidungsrichtlinien-Code hinzuzufügen.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>Wenn Ihre Entscheidungsrichtlinie für Code-basierte Erlebnisse Entscheidungselemente einschließlich Fragmenten enthält, können Sie diese Fragmente im Entscheidungsrichtlinien-Code nutzen. [Erfahren Sie, wie Sie Fragmente nutzen](fragments-decision-policies.md)

>[!TAB E-Mail]

1. Öffnen Sie den **Personalization** Editor und navigieren Sie zu **[!UICONTROL Entscheidungsrichtlinien]**.

2. Wählen Sie **[!UICONTROL Syntax einfügen]**, um den Code für Ihre Entscheidungsrichtlinie hinzuzufügen.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Wenn die Einfügeoption nicht angezeigt wird, ist möglicherweise bereits eine Entscheidungsrichtlinie für die übergeordnete Komponente konfiguriert.

3. Wenn der Komponente noch keine Platzierung zugewiesen wurde, wählen Sie eine aus der Liste aus und klicken Sie auf **[!UICONTROL Zuweisen]**.

   ![](assets/decision-policy-placement.png)

   >[!NOTE]
   >
   >Wenn Sie mehrere Entscheidungsrichtlinien in derselben E-Mail verwenden (z. B. eine für die Kopfzeile und eine für die Fußzeile), wird dasselbe Angebot für alle Platzierungen dedupliziert: Jeder Bereich erhält ein anderes Angebot. Um dasselbe Angebot in mehreren Bereichen anzuzeigen, verwenden Sie **[!UICONTROL Entscheidungsausgabe wiederverwenden]** wenn Sie eine Entscheidungsrichtlinie hinzufügen. [Erfahren Sie, wie Sie Entscheidungsrichtlinien erstellen](create-decision-policy.md).

>[!TAB SMS]

1. Öffnen Sie den **Personalization** Editor und navigieren Sie zu **[!UICONTROL Entscheidungsrichtlinien]**.

2. Wählen Sie **[!UICONTROL Syntax einfügen]**, um den Code für Ihre Entscheidungsrichtlinie hinzuzufügen.

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB Push-Benachrichtigung]

1. Öffnen Sie den **Personalization** Editor und navigieren Sie zu **[!UICONTROL Entscheidungsrichtlinien]**.

2. Wählen Sie **[!UICONTROL Syntax einfügen]**, um den Code für Ihre Entscheidungsrichtlinie hinzuzufügen.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>Für Experience Decisioning mit Push-Benachrichtigungen ist eine bestimmte Version der Mobile SDK erforderlich. Bevor Sie diese Funktion implementieren, überprüfen Sie die [Versionshinweise](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}, um die erforderliche Version zu identifizieren und sicherzustellen, dass Sie das Upgrade entsprechend durchgeführt haben. Sie können auch alle verfügbaren SDK-Versionen für Ihre Plattform in [diesem Abschnitt](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"} anzeigen.

>[!ENDTABS]

Der Entscheidungsrichtlinien-Code wird hinzugefügt. Sie können jetzt Attribute aus den zurückgegebenen Entscheidungselementen verwenden, um Ihren Inhalt zu personalisieren.

>[!NOTE]
>
>Wiederholen Sie diese Sequenz für Code-basierte Erlebnis- und E-Mail-Kanäle einmal pro Entscheidungselement, das Sie zurückgeben möchten. Wenn Sie beispielsweise beim Erstellen der Entscheidung zwei Elemente zurückgeben [, wiederholen ](create-decision-policy.md) die Sequenz zweimal. Bei SMS- und Push-Kanälen kann nur ein Entscheidungselement zurückgegeben werden.

## Mit Entscheidungselementattributen personalisieren {#attributes}

Nachdem Sie den Code für eine Entscheidungsrichtlinie zu Ihrem Inhalt hinzugefügt haben, werden alle Attribute aus den zurückgegebenen Entscheidungselementen für die Personalisierung verfügbar. [Erfahren Sie, wie Sie mit Personalisierung ](../personalization/personalize.md).

Attribute werden im „Angebote“ ([) ](catalogs.md). Sie werden im Personalisierungseditor in den folgenden Ordnern angezeigt:
* **Benutzerdefinierte Attribute**: `_\<imsOrg\>` Ordner
* **Standardattribute**: `_experience` Ordner

Entscheidungselementattribute und kontextuelle Attribute werden in [!DNL Journey Optimizer] Fragmenten nicht standardmäßig unterstützt. Sie können jedoch stattdessen globale Variablen verwenden, wie unten beschrieben.

![](assets/decision-code-based-decision-attributes.png)

Um ein Attribut hinzuzufügen, klicken Sie auf das **`+`** neben dem Attribut. Sie können beliebig viele Attribute hinzufügen. Sie können auch andere Personalisierungsattribute wie Profildaten einbeziehen.

* Umschließen **bei**- und **Code-basierten**-Kanälen die Attribute in der `#each` Schleife mithilfe von eckigen Klammern `[ ]` und fügen Sie ein Komma vor dem schließenden `/each`-Tag hinzu.

  +++Siehe Beispiel

  ![](assets/decision-code-based-wrap-code.png)

  +++

* Stellen Sie bei **SMS**- und **Push**-Kanälen sicher, dass Sie Attribute nach dem Syntaxcode für die Entscheidungsrichtlinie einfügen. Diese Syntax sollte immer in Zeile 1 beibehalten werden.

  +++Siehe Beispiel

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >Wenn Sie ein Bild-Asset-Attribut in SMS- oder Push-Inhalt einfügen (z. B. in den Titel oder Hauptteil), wird der Attributwert als URL angezeigt. Das Bild selbst wird in diesen Feldern nicht gerendert.

* Um die Entscheidungselement-Nachverfolgung zu aktivieren, fügen Sie das `trackingToken` Attribut hinzu: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Vorschau und Test Ihres Inhalts

Nachdem Sie Ihren Inhalt erstellt haben, sollten Sie ihn in der Vorschau anzeigen und testen, bevor Sie Ihren Journey oder Ihre Kampagne aktivieren. Entscheidungselemente werden basierend auf ausgewählten Profilen in der Simulationsoberfläche dargestellt. [Erfahren Sie, wie Sie Inhalte in der Vorschau anzeigen und testen können](../content-management/preview-test.md).

## Nächste Schritte {#final-steps}

Sobald Ihr Inhalt fertig ist, überprüfen und veröffentlichen Sie Ihre Kampagne oder Ihren Journey:

* [Veröffentlichen einer Journey](../building-journeys/publish-journey.md)
* [Überprüfen und Aktivieren einer Kampagne](../campaigns/review-activate-campaign.md)

Sobald Ihre Entwickelnden bei Code-basierten Erlebnissen einen API- oder SDK-Aufruf zum Abrufen von Inhalten für die in Ihrer Kanalkonfiguration definierte Oberfläche starten, werden die Änderungen auf Ihre Web-Seite oder App angewendet.

>[!NOTE]
>
>Sie können derzeit keine entscheidungsbasierten Inhalte für ([-basierte Erlebnisse](../code-based/create-code-based.md) Kampagnen oder Journey simulieren. Eine Problemumgehung ist verfügbar [hier](../code-based/code-based-decisioning-implementations.md).

## Reporting-Dashboards verwenden

Um zu sehen, wie Ihre Entscheidungen funktionieren, können Sie vordefinierte Entscheidungsmetriken im Kampagnen- oder Journey-Bericht anzeigen oder benutzerdefinierte Customer Journey Analytics-Dashboards erstellen, um die Leistung zu messen und Erkenntnisse darüber zu erhalten, wie Ihre Entscheidungsrichtlinien und Angebote bereitgestellt und interagiert werden. [Erfahren Sie mehr über Decisioning-Reporting](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
