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
TQID: https://experienceleague.adobe.com/zKV67LEfRVmEk9Fac-D45qdHLqbuVCS3rUt6Rt0HB7w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 771
ht-degree: 11%

---

# Verwenden von Entscheidungsrichtlinien in Nachrichten {#create-decision}

Nachdem Sie Ihrem Inhalt eine Entscheidungsrichtlinie hinzugefügt haben, können Sie Attribute aus zurückgegebenen Entscheidungselementen zur Personalisierung verwenden. Fügen Sie dazu zunächst den Entscheidungsrichtlinien-Code in Ihren Inhalt ein.

>[!CAUTION]
>
>Entscheidungsrichtlinien stehen allen Kundinnen und Kunden für die Kanäle **Code-basiertes Erlebnis**, **SMS**, **Push-Benachrichtigung** und **E** zur Verfügung.

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
   >Wenn Sie mehrere Entscheidungsrichtlinien in derselben E-Mail verwenden (z. B. eine für die Kopfzeile und eine für die Fußzeile), wird dasselbe Angebot für alle Platzierungen dedupliziert: es wird nicht zweimal gerendert. Die zweite Entscheidungsrichtlinie gibt keinen Inhalt zurück und zeigt eine Leerstelle an, es sei denn, Sie haben ein Fallback-Angebot konfiguriert. In diesem Fall wird stattdessen das Fallback angezeigt.

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
>Für Experience Decisioning mit Push-Benachrichtigungen ist eine bestimmte Version der Mobile SDK erforderlich. Bevor Sie diese Funktion implementieren, überprüfen Sie die [Versionshinweise](https://developer.adobe.com/client-sdks/home/release-notes){target="_blank"}, um die erforderliche Version zu identifizieren und sicherzustellen, dass Sie das Upgrade entsprechend durchgeführt haben. Sie können auch alle verfügbaren SDK-Versionen für Ihre Plattform in [diesem Abschnitt](https://developer.adobe.com/client-sdks/home/current-sdk-versions){target="_blank"} anzeigen.

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

Nachdem Sie Ihren Inhalt erstellt haben, sollten Sie ihn in der Vorschau anzeigen und testen, bevor Sie Ihren Journey oder Ihre Kampagne aktivieren. Entscheidungselemente werden basierend auf ausgewählten Profilen in der Simulationsoberfläche dargestellt. [Informationen zum Anzeigen von Inhalten in der Vorschau und Testen von Inhalten](../content-management/preview-test.md).

## Nächste Schritte {#final-steps}

Sobald Ihr Inhalt fertig ist, überprüfen und veröffentlichen Sie Ihre Kampagne oder Ihren Journey:

* [Veröffentlichen einer Journey](../building-journeys/publish-journey.md)
* [Überprüfen und Aktivieren einer Kampagne](../campaigns/review-activate-campaign.md)

Sobald Ihre Entwickelnden bei Code-basierten Erlebnissen einen API- oder SDK-Aufruf zum Abrufen von Inhalten für die in Ihrer Kanalkonfiguration definierte Oberfläche starten, werden die Änderungen auf Ihre Web-Seite oder App angewendet.

## Reporting-Dashboards verwenden

Um zu sehen, wie Ihre Entscheidungen funktionieren, können Sie vordefinierte Entscheidungsmetriken im Kampagnen- oder Journey-Bericht anzeigen oder benutzerdefinierte Customer Journey Analytics-Dashboards erstellen, um die Leistung zu messen und Erkenntnisse darüber zu erhalten, wie Ihre Entscheidungsrichtlinien und Angebote bereitgestellt und interagiert werden. [Erfahren Sie mehr über Decisioning-Reporting](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)
