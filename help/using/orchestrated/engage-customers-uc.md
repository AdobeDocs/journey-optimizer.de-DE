---
solution: Journey Optimizer
product: journey optimizer
title: Kundeninteraktion durch Durchsuchen der Aktivität
description: Kundeninteraktion durch Durchsuchen der Aktivität
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# Kundeninteraktion durch Durchsuchen der Aktivität {#engage-customers-uc}

>[!BEGINSHADEBOX]

Beachten Sie, dass dieser Anwendungsfall mit einer Zielgruppe beginnt, die bereits in Experience Platform vorhanden ist, insbesondere einer Zielgruppe mit Webverhalten in Echtzeit, die Browser-Aktivitäten erfasst, während sie auftritt. [Weitere Informationen finden Sie in Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Für diesen Anwendungsfall erforderliche Schemata:**

* **Empfänger**: wird als Zielgruppendimension verwendet, mit Feldern: `email`, `churnprop`
* **Wunschliste**: mit Feldern: `description`, `priceref`, `imageurl`

➡️ [Erfahren Sie, wie Sie modellbasierte Schemata konfigurieren](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Diese Kampagne richtet sich an Kunden, die die Kategorie Übungsgeräte durchsucht haben. Die Zielgruppe wird dedupliziert und nach Abwanderungsrisiko segmentiert, d. h. wie wahrscheinlich es ist, dass jemand aufhört, Kontakte zu knüpfen oder Einkäufe zu tätigen.

Kunden mit hohem Risiko werden in einer separaten neuen Zielgruppe zusammengefasst, die später für eine bestimmte Kommunikation verwendet wird, während Kunden mit niedrigem und mittlerem Risiko eine mehrstufige Journey mit personalisierten E-Mails und Folgemaßnahmen durchlaufen.

1. Richten Sie zunächst eine neue Kampagne ein, die speziell auf **Wishlist-Rückgewinnung“**. Dadurch wird sichergestellt, dass sich Ihre Werbebotschaft auf Kunden konzentriert, die bereits ihre Kaufabsicht gezeigt haben, indem sie Produkte auf ihrer Wunschliste speichern.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Geben Sie Ihre **[!UICONTROL Kampagneneinstellungen]** wie Kampagnenname, Beschreibung, Start- und Enddatum sowie relevante Tags ein.

1. Fügen Sie die Aktivität **[!UICONTROL Zielgruppe lesen]** hinzu, um eine vordefinierte Zielgruppe aus Adobe Experience Platform auszuwählen, d. h. Kunden, die die Kategorie Übungsgeräte auf Ihrer Website durchsucht haben.

   Die Empfänger werden mit ihren E-Mail-Adressen identifiziert, die aus dem Feld **[!UICONTROL Entität]** ausgewählt wurden.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Fügen Sie eine Aktivität **[!UICONTROL Deduplizierung]** hinzu, um doppelte E-Mail-Adressen aus Ihrer Audience zu entfernen, sodass jeder Kunde nur eine Nachricht erhält.

1. Klicken Sie auf **[!UICONTROL Attribut hinzufügen]** und wählen Sie E-Mail als Attribut für die Deduplizierung aus.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Als Nächstes fügen Sie eine **[!UICONTROL Aufspaltung]**-Aktivität hinzu, um Kundinnen und Kunden nach ihrer Abwanderungswahrscheinlichkeit zu segmentieren, sodass Sie personalisierte Erlebnisse bereitstellen können, die auf jede Kundengruppe zugeschnitten sind.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Segment hinzufügen]**, um drei Gruppen zu erstellen:

   * Geringes Risiko

   * Medium-Risiko

   * Hohes Risiko

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Klicken Sie **[!UICONTROL Filter erstellen]**, um die Abwanderungswahrscheinlichkeit für jede Gruppe zu definieren.

   Verwenden Sie den **Bedingungseditor** um die spezifischen Werte festzulegen, die das Abwanderungsrisiko jedes Kunden bestimmen.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Jedes Segment wird anders gehandhabt:

   * [Geringes/mittleres Risiko](#low-medium-risk)
   * [Hohes Risiko](#high-risk)

1. Sobald Ihre Kampagne getestet wurde und bereit ist, klicken Sie auf **[!UICONTROL Veröffentlichen]**, um sie live zu schalten.

Nachdem die Kampagne ausgeführt wurde, können Sie das Reporting-Dashboard erkunden, um Leistungsmetriken und wichtige Erkenntnisse zu überprüfen.

➡️ [Weitere Informationen zum Reporting](../reports/campaign-global-report-cja.md)

## Segmente mit hohem Risiko {#high-risk}

Erstellen Sie für Kunden, bei denen ein hohes Abwanderungsrisiko besteht, ein dediziertes Zielgruppensegment. Diese Zielgruppe wird später für eine separate, zielgerichtete Kommunikation verwendet.

1. Fügen Sie eine **[!UICONTROL Zielgruppe speichern]** hinzu.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Fügen Sie **[!UICONTROL Zielgruppe einen]** hinzu und wählen Sie das Feld **[!UICONTROL Profilzuordnung]** hier **recipients-email**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Diese Zielgruppe wird dann in Experience Cloud gespeichert, wo sie später für eine bestimmte Zielkampagne verwendet werden kann.

## Segmente mit niedrigem/mittlerem Risiko {#low-medium-risk}

Richten Sie für Kunden mit niedrigem und mittlerem Abwanderungsrisiko eine mehrstufige Kampagne ein, die darauf abzielt, die Interaktion zu stärken:

1. Kombinieren Sie niedrige und Medium-Risiken mit einer **[!UICONTROL Union]**-Aktivität.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Fügen Sie eine Aktivität **[!UICONTROL Anreicherung]** hinzu, um die Kampagne mit Wunschliste und Produktinformationen zu personalisieren.

1. Klicken Sie **[!UICONTROL Attribut hinzufügen]**, um die folgenden drei Attribute zu erstellen:

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Dadurch wird die Nachricht mit detaillierten Informationen zur Wunschliste angereichert.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Erstellen Sie eine neue Audience für das Retargeting basierend auf der Interaktion mit E-Mails.

   Hier erstellen wir eine Zielgruppe basierend auf E-Mail-Klickereignissen, um alle Personen erneut anzusprechen, die mit einer zuvor gesendeten E-Mail interagiert haben, und genauer gesagt, auf einen Link in dieser Nachricht geklickt haben.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Teilen Sie die Interaktion gleichmäßig auf, um eine Folgenachricht über SMS oder Push-Benachrichtigungen zu senden und so Konversionen zu fördern.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Erstellen Sie den Nachrichteninhalt für jeden Kanal einschließlich Profilattributen, wie z. B. den Namen des Empfängers, zusammen mit Anreicherungsdaten wie Wunschlistenelementen, um jede Nachricht zu personalisieren.

   ![](assets/uc-interest-13.png){zoomable="yes"}
