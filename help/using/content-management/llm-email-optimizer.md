---
title: Optimieren von E-Mail-Text für KI-Posteingänge
description: Verfeinern Sie die Nur-Text-Ebene von E-Mails in Journey Optimizer, damit KI-unterstützte Posteingangskunden Ihre Angebote und CTAs verwenden können, wenn sie E-Mails zusammenfassen oder Absichten extrahieren - in der E-Mail-Designer mit KI optimieren .
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Optimieren von E-Mail-Text für KI-Posteingänge {#email-text-optimizer}

[!DNL Adobe Journey Optimizer] verfügt über eine E-Mail-Kanal-Funktion, mit der Sie die [Textversion](../email/text-version-email.md) Ihrer Nachrichten strukturieren können, um die KI-gestützten Posteingangserlebnisse zu verbessern, z. B. [!DNL Apple Intelligence] und [!DNL Google Gemini] in [!DNL Gmail]. Auf diese Weise können E-Mails basierend auf Ihrem Inhalt präziser beantwortet und mit besseren Ergebnissen zusammengefasst werden.

>[!NOTE]
>
>Mit dieser Funktion wird nur Text geändert, nicht die HTML-Version Ihres E-Mail-Inhalts.

Mit diesem E-Mail-Textoptimierer können Sie sicherstellen, dass die Nur-Text-Version Ihres E-Mail-Inhalts für KI-unterstützte Posteingangserlebnisse erweitert wird, sodass die Informationen, die Sie den KI-Funktionen dieser E-Mail-Posteingangsanbieter bereitstellen, genau die sind, die Sie bereitstellen möchten.

## Funktionsweise {#how-it-works}

Zu den typischen Fragen, die Empfangende in KI-unterstützten Posteingängen stellen können, gehören *Worum geht es in dieser E-Mail?* oder *Was sind diese Angebote?*.

* Die Antworten dieser KI-Assistenten können eine kurze Zusammenfassung sein (z. B. dass die Nachricht werblich ist, frühzeitigen Zugriff auf VIP und einen Verkauf erwähnt und Links zu Produktkategorien enthält), aber sie lassen die Ziele aus, die dem Marketing-Experten wichtig waren, da die Assistenten aus dem tatsächlich angezeigten Text ableiten - nicht unbedingt die vollständige Story, die Sie beabsichtigt hatten.

* Außerdem können die Assistenten proaktiv nach Rabatten oder Coupons im Zusammenhang mit der Marke suchen und diese in die Antwort einfließen lassen, sodass der Benutzer nicht mehr nur das sieht, was Ihre Nachricht tatsächlich versprochen hat. Dieses Verhalten ist für Endbenutzende nützlich, beeinträchtigt aber die Kontrolle für Marketing-Fachleute, die Antworten benötigen, um die tatsächlichen Begriffe beim Versand zu verfolgen.

Um diese Probleme zu vermeiden, schreibt [!DNL Journey Optimizer] den Nur-Text-Code so um, dass Coupons, Rabattbereiche, Aktionsaufrufe und andere Prioritäten in klarer linearer Kopie im Voraus angezeigt werden. Ziel ist es, dass die KI des Posteingangs Zusammenfassungen und Fragen und Antworten in Ihren definierten Angeboten und Aktionen erstellt, anstatt sich auf einen dünnen Standardtextteil oder auf nicht verwandte Web-Ergebnisse zu stützen.

>[!IMPORTANT]
>
>Das genaue Verhalten der KI-Assistenten hängt vom Posteingangsanbieter und der Modellversion ab. Nachdem Ihre E-Mail zugestellt wurde, können Antworten und Zusammenfassungen, die von externen KI-Clients bereitgestellt werden, falsch, unvollständig oder mit Web-Ergebnissen vermischt sein.
>
>Die Funktion E-Mail-Text für KI-Posteingänge optimieren verbessert nur den in Journey Optimizer erstellten Klartext. Sie garantiert nicht, wie ein Drittanbieterassistent die Nachricht interpretiert oder anzeigt. Erfahren Sie mehr über [Einschränkungen und Risiken der Posteingangshilfe von Drittanbietern](#inbox-ai-risks).

## Empfohlene Anwendungsfälle {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **Dichte oder fragmentierter automatisch generierter Text** - Wenn der standardmäßige Nur-Text schwer zu scannen ist, kann die Optimierung eine klarere lineare Erzählung mit expliziten Angeboten und Links erzeugen.

* **Steuern des Posteingangs** - Wenn Sie von Empfängern erwarten, dass sie Assistenten fragen, *worum es bei der E-Mail geht* oder *was die Angebote sind*, reduziert eine starke Nur-Text-Version Teilzusammenfassungen und reduziert die Abhängigkeit von Web-ergänzten Antworten, die nicht an Ihre genehmigte Kopie gebunden sind.

## Für KI-Posteingangserlebnisse optimieren {#optimize-with-ai}

>[!IMPORTANT]
>
>Bevor Sie mit der Nutzung dieser Funktion beginnen, lesen Sie die entsprechenden [Risiken und Einschränkungen](#inbox-ai-risks).
>
>Um auf diese Funktion zugreifen zu können, müssen Sie einer Benutzervereinbarung zustimmen, die angezeigt wird, wenn Sie Generative AI in [!DNL Journey Optimizer] zum ersten Mal verwenden. Weitere Informationen finden Sie in den [Benutzerrichtlinien für die generative KI von Adobe Experience Cloud](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Gehen Sie wie folgt vor, um die Nur-Text-Version Ihrer E-Mail für KI-Posteingänge mit [!DNL Journey Optimizer] zu optimieren.

1. Öffnen Sie Ihre E-Mail in [E-Mail-Designer](../email/content-from-scratch.md) (über eine Kampagne, Journey oder Vorlage, je nach Workflow).

1. Wählen Sie das **[!UICONTROL Nur Text]**-Symbol aus, um die Textversion Ihrer E-Mail zu öffnen. [Weitere Informationen](../email/text-version-email.md)

   ![Wählen Sie das Symbol Nur Text aus, um die Textversion Ihrer E-Mail zu öffnen](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. Die Textversion Ihrer E-Mail wird angezeigt. Klicken Sie auf die **[!UICONTROL Für KI-Posteingang optimieren]**, um eine verbesserte Nur-Text-Version zu generieren, die wichtige Informationen für das KI-unterstützte Lesen und Zusammenfassen hervorhebt.

   ![Schaltfläche „Für KI-Posteingang optimieren“ in der Textansicht](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Beim Klicken auf die Schaltfläche **[!UICONTROL Für KI-]** optimieren **[!UICONTROL wird die Option]** Mit HTML synchronisieren“ automatisch deaktiviert. [Weitere Informationen](../email/text-version-email.md#plain-text-custom)

1. Wenn Sie in [!DNL Journey Optimizer] zum ersten Mal generative KI verwenden, werden Sie aufgefordert, der Benutzervereinbarung zuzustimmen. Weitere Informationen finden Sie in den [Benutzerrichtlinien für die generative KI von Adobe](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Dialogfeld für Benutzervereinbarungen für generative KI in Journey Optimizer](assets/text-optimizer-agreement.png){width=50%}

   Klicken Sie **[!UICONTROL Zustimmen]**, um fortzufahren.

1. Der generierte Text wird angezeigt. Überprüfen Sie die Änderungen, bearbeiten Sie sie bei Bedarf und speichern Sie dann Ihre E-Mail wie gewohnt.

   ![Generierter Text in der Textversionsansicht](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Der E-Mail-Textoptimierer aktualisiert nur den Textkörper. Das HTML-Design, das Layout oder die Bilder werden dadurch nicht geändert.

1. Sie können jederzeit wieder zur HTML-Version Ihrer E-Mail wechseln, indem Sie auf das Symbol **[!UICONTROL Zur Desktop-Ansicht wechseln]** klicken. Ihre Änderungen in der Textversion bleiben erhalten.

   >[!CAUTION]
   >
   >Wenn Sie die Option **[!UICONTROL Mit HTML synchronisieren]** erneut aktivieren, gehen Ihre Änderungen verloren und werden durch Textinhalte ersetzt, die von der HTML-Version generiert wurden.

## Risiken und Einschränkungen von Drittanbieter-Posteingang-KI {#inbox-ai-risks}

Mit der Funktion E-Mail-Text für KI-Posteingänge optimieren können Sie einfachen Text dafür vorbereiten, wie Postfachanbieter Ihre [!DNL Journey Optimizer]-Sendungen verarbeiten können. Sie kontrolliert nicht die Produkte dieser Anbieter. Nach dem Versand einer Nachricht werden alle KI-Funktionen in [!DNL Gmail], [!DNL Apple] Mail, [!DNL Outlook] oder anderen Clients nach ihren Bedingungen, Modellen und Richtlinien ausgeführt - nicht nach den Richtlinien von Adobe.

* **Unvorhersehbare Präsentation** - Zusammenfassungen, Benachrichtigungs-Blurbs und dialogorientierte Antworten können Angebote, Preise oder Datumsangaben weglassen, Inhalte mit nicht verwandten Web-Ergebnissen zusammenführen oder auf eine Weise umschreiben, die nicht mehr mit Ihrer genehmigten Kopie übereinstimmt. Das Verhalten ändert sich, wenn Anbieter Modelle oder Benutzeroberflächen ohne Vorankündigung aktualisieren.

* **Keine Gewähr für Parität mit HTML** - Empfängerinnen und Empfänger, die auf Vorschauen oder Hilfsantworten angewiesen sind, sehen möglicherweise nie Ihr vollständiges HTML-Design, Ihre Bilder oder Ihre rechtlichen Fußzeilen. Was sie glauben, dass die Nachricht „sagt“, kommt möglicherweise nur aus einem kurzen KI-generierten Auszug.

* **Datenschutz, Compliance und Datennutzung** - Die KI des Posteingangs kann Nachrichteninhalte in der Infrastruktur des Anbieters verarbeiten, wobei die Datenschutzrichtlinie, die Aufbewahrung und die regionalen Regeln dieses Anbieters zu beachten sind. Organisationen in regulierten Branchen sollten unabhängig davon, wie die E-Mail in [!DNL Journey Optimizer] verfasst wurde, bewerten, ob die Verwendung solcher Funktionen durch Empfänger ihre Verpflichtungen beeinträchtigt.

* **Marken- und rechtliche Offenlegung** - Falsche oder unvollständige KI-Zusammenfassungen können bei Kunden weiterhin Verwirrung oder Streitigkeiten über Werbeaktionen, Bedingungen oder die Sprache zum Opt-out hervorrufen. Der Optimierer verbessert die von Ihnen bereitgestellte Textebene. Er stellt nicht sicher, dass das Modell eines Drittanbieters sie getreu reproduziert.

* **[!UICONTROL Für KI-Posteingang optimieren]** in [!DNL Journey Optimizer] - Die Authoring-Zeit-Aktion in der E-Mail-Designer ist ein separates System von den Posteingangsassistenten für Endbenutzer. Generierten Text vor dem Versand immer überprüfen.

## Verwandte Themen {#related-topics}

* [Textversion einer E-Mail verwalten](../email/text-version-email.md)
* [Erste Schritte mit dem E-Mail-Design](../email/get-started-email-design.md)
* Allgemeine Informationen zu Adobe-Funktionen finden Sie unter [Erste Schritte mit dem KI-Assistenten zum Erstellen von Inhalten](gs-generative.md).
