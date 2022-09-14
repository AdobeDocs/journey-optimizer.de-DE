---
title: Hinzufügen von Einschränkungen zu Angeboten
description: Erfahren Sie, wie Sie Bedingungen für ein anzuzeigendes Angebot definieren
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Hinzufügen von Einschränkungen zu Angeboten {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="Informationen zu Angebotseinschränkungen"
>abstract="Mit Einschränkungen können Sie angeben, wie das Angebot priorisiert und dem Benutzer im Vergleich zu anderen Angeboten angezeigt wird."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="Informationen zu Angebotseinschränkungen"
>abstract="Mit Einschränkungen können Sie angeben, wie das Angebot priorisiert und dem Benutzer im Vergleich zu anderen Angeboten angezeigt wird."

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="Informationen zur Angebotspriorität"
>abstract="In diesem Feld können Sie die Prioritätseinstellungen für das Angebot festlegen. Die Priorität ist eine Zahl, die verwendet wird, um Angebote, die alle Einschränkungen wie Berechtigung, Datum und Begrenzungen erfüllen, in eine Rangfolge zu bringen."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="Festlegen der Priorität"
>abstract="Mit der Priorität können Sie den Rang eines Angebots gegenüber anderen definieren, wenn der Benutzer für mehrere Angebote infrage kommt. Je höher die Priorität eines Angebots ist, desto höher ist seine Priorität gegenüber anderen Angeboten."

Mit Einschränkungen können Sie festlegen, unter welchen Bedingungen ein Angebot angezeigt werden soll.

1. Konfigurieren Sie die **[!UICONTROL Angebotseignung]**. [Weitere Informationen](#eligibility)

   ![](../assets/offer-eligibility.png)

1. Definieren Sie die **[!UICONTROL Priorität]** des Angebots gegenüber anderen, wenn der Benutzer für mehr als ein Angebot geeignet ist. Je höher die Priorität eines Angebots ist, desto höher ist seine Priorität gegenüber anderen Angeboten.

   ![](../assets/offer-priority.png)

1. Geben Sie die **[!UICONTROL Begrenzung]** des Angebots an, d. h. wie häufig das Angebot unterbreitet werden soll. [Weitere Informationen](#capping)

   ![](../assets/offer-capping.png)

1. Klicken Sie auf **[!UICONTROL Weiter]**, um alle definierten Einschränkungen zu bestätigen.

Angenommen, Sie legen die folgenden Einschränkungen fest:

![](../assets/offer-constraints-example.png)

* Das Angebot wird nur bei Benutzern berücksichtigt, die die Entscheidungsregel „Gold-Treuekunden“ erfüllen.
* Die Priorität des Angebots ist mit „50“ festgelegt, d. h. das Angebot wird vor Angeboten mit einer Priorität zwischen 1 und 49 und nach Angeboten mit einer Priorität von mindestens 51 unterbreitet.
* Das Angebot wird für alle Platzierungen nur einmal pro Benutzer angezeigt.

## Eignung {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="Definieren der Qualifikation"
>abstract="Standardmäßig kann jedem Profil das Angebot unterbreitet werden. Sie können jedoch Segmente oder Entscheidungsregeln verwenden, um das Angebot auf bestimmte Profile zu beschränken."

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="Informationen zur Eignung von Angeboten"
>abstract="In diesem Abschnitt können Sie mithilfe von Entscheidungsregeln bestimmen, welche Benutzer für das Angebot geeignet sind."
>additional-url="https://video.tv.adobe.com/v/329373?captions=ger" text="Demovideo ansehen"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="Gesamtprofilschätzung"
>abstract="Wenn Sie Segmente oder Entscheidungsregeln auswählen, können Sie Informationen zu den geschätzten qualifizierten Profilen sehen."

Im Abschnitt **[!UICONTROL Angebotseignung]** können Sie das Angebot auf bestimmte Profile beschränken, die Sie mithilfe von Segmenten oder Entscheidungsregeln definieren.

>[!NOTE]
>
>Weitere Informationen zur Verwendung von **Segmenten** versus **Entscheidungsregeln** finden Sie in [diesem Abschnitt](#segments-vs-decision-rules).

* Standardmäßig ist die Option **[!UICONTROL Alle Besucher]** aktiviert, d. h. das Angebot kann jedem Profil unterbreitet werden.

   ![](../assets/offer-eligibility-default.png)

* Sie können die Präsentation eines Angebots auch auf die Mitglieder eines oder mehrerer [Adobe Experience Platform-Segmente](../../segment/about-segments.md) beschränken.

   Aktivieren Sie dazu die Option **[!UICONTROL Besucher, die zu mindestens einem Segment passen]**, fügen Sie dann ein oder mehrere Segmente aus dem linken Bereich hinzu und kombinieren Sie sie mit den logischen Operatoren **[!UICONTROL Und]**/**[!UICONTROL Oder]**.

   ![](../assets/offer-eligibility-segment.png)

* Wenn Sie eine bestimmte [Entscheidungsregel](../offer-library/creating-decision-rules.md) mit dem Angebot verknüpfen möchten, wählen Sie **[!UICONTROL Nach definierter Entscheidungsregel]** aus und ziehen Sie die gewünschte Regel dann aus dem linken Bereich in den Bereich **[!UICONTROL Entscheidungsregel]**.

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >Ereignisbasierte Angebote werden derzeit in [!DNL Journey Optimizer] nicht unterstützt. Wenn Sie eine Entscheidungsregel basierend auf einem [Ereignis](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=de#events){target=&quot;_blank&quot;} erstellen, können Sie sie in einem Angebot nicht nutzen.

Wenn Sie Segmente oder Entscheidungsregeln auswählen, können Sie Informationen zu den geschätzten qualifizierten Profilen sehen. Klicken Sie auf **[!UICONTROL Aktualisieren]**, um diese Daten zu aktualisieren.

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>Profilschätzungen sind nicht verfügbar, wenn Regelparameter Daten enthalten, die nicht im Profil enthalten sind, z. B. Kontextdaten. Beispielsweise eine Eignungsregel, für die das aktuelle Wetter ≥ 80 Grad sein muss.

### Verwenden von Segmenten vs. Entscheidungsregeln {#segments-vs-decision-rules}

Um eine Einschränkung anzuwenden, können Sie die Auswahl von Angeboten auf ein oder mehrere **Adobe Experience Platform-Segmente** beschränken oder eine **Entscheidungsregel** verwenden. Diese beiden Lösungen werden in unterschiedlichen Fällen angewendet.

Grundsätzlich besteht ein Segment aus einer Liste von Profilen, während eine Entscheidungsregel eine Funktion ist, die während des Entscheidungsprozesses bei Bedarf für ein einzelnes Profil ausgeführt wird. Der Unterschied zwischen diesen beiden Anwendungen wird im Folgenden beschrieben.

* **Segmente**

   Segmente sind Adobe Experience Platform-Profile, die basierend auf Profilattributen und Erlebnisereignissen einer bestimmten Logik entsprechen. Doch beim Offer Decisioning-Prozess wird das Segment nicht neu berechnet, weshalb es zum Zeitpunkt der Angebotsunterbreitung möglicherweise nicht aktuell ist.

   Weitere Informationen zu Segmenten finden Sie in [diesem Abschnitt](../../segment/about-segments.md).

* **Entscheidungsregeln**

   Dagegen basiert eine Entscheidungsregel auf in Adobe Experience Platform verfügbaren Daten und bestimmt, wem ein Angebot angezeigt werden kann. Nachdem die Entscheidungsregel in einem Angebot oder einer Entscheidung für eine bestimmte Platzierung ausgewählt wurde, wird sie bei jedem Entscheidungsvorgang erneut ausgeführt. Dadurch wird jedem Profil immer ein aktuelles, optimales Angebot angezeigt.

   Weitere Informationen zu Entscheidungsregeln finden Sie in [diesem Abschnitt](creating-decision-rules.md).

## Begrenzung {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="Informationen zur Begrenzung von Angeboten"
>abstract="In diesem Feld können Sie angeben, wie oft das Angebot angezeigt werden kann."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="Verwenden der Begrenzung"
>abstract="Um zu vermeiden, dass Ihre Kunden und Kundinnen zu oft angesprochen werden, legen Sie mithilfe der Begrenzungen fest, wie oft ein Angebot maximal unterbreitet werden kann."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="Begrenzungsfrequenz festlegen"
>abstract="Sie können den Angebotsbegrenzungszähler auf täglicher, wöchentlicher oder monatlicher Basis zurücksetzen."

Mit Begrenzungen wird definiert, wie oft ein Angebot maximal angezeigt werden kann.

Durch die Begrenzung der Anzeige von Angeboten vermeiden Sie, dass Ihre Kunden überfordert werden, und können jeden Touchpoint mit dem besten Angebot optimieren.

Gehen Sie wie folgt vor, um Begrenzungen festzulegen.

1. Definieren Sie, wie oft das Angebot unterbreitet werden kann.

   ![](../assets/offer-capping-times.png)

   >[!NOTE]
   >
   >Der Wert muss eine Ganzzahl größer 0 sein.

1. Geben Sie an, ob die Begrenzung für alle Benutzer oder für ein bestimmtes Profil gelten soll:

   ![](../assets/offer-capping-total.png)

   * Wählen Sie **[!UICONTROL Insgesamt]** aus, um festzulegen, wie oft ein Angebot für die gesamte Ziel-Audience vorgeschlagen werden kann, d. h. für alle Benutzer.

      Wenn Sie z. B. ein Elektronikhändler sind, der einen Fernseher im Angebot hat, möchten Sie, dass das Angebot allen Profilen nur 200-mal angezeigt wird.

   * Wählen Sie **[!UICONTROL Pro Profil]** aus, um festzulegen, wie oft ein Angebot demselben Benutzer vorgeschlagen werden kann.

      Wenn Sie z. B. eine Bank mit dem Angebot einer Platin-Kreditkarte sind, soll dieses Angebot nicht öfter als fünfmal pro Profil angezeigt werden. Vermutlich nutzt ein Benutzer, der das Angebot fünfmal gesehen und nicht darauf reagiert hat, eher das nächste beste Angebot.
   <!--
    Set the **[!UICONTROL Frequency]** to define how often the capping count is reset. To do so, define the time period for the counting (daily, weekly or monthly) and enter the number of days/weeks/months of your choice.
    ![](../assets/offer-capping-frequency.png)
    >[!NOTE]
    >
    >The reset happens at 12am UTC, on the day that you defined or on the first day of the week/month when applicable. The week start day is Sunday.
    
    For example, if you want the capping count to be reset every 2 weeks, select **[!UICONTROL Weekly]** from the **[!UICONTROL Repeat]** drop-down list and type **2** in the other field. The reset will happen every other Sunday at 12pm UTC.
    -->

1. Wenn Sie mehrere [Darstellungen](add-representations.md) für Ihr Angebot haben, geben Sie an, ob Sie eine Begrenzung auf **[!UICONTROL alle Platzierungen]** oder **[!UICONTROL auf eine einzelne Platzierung]** anwenden möchten.

   ![](../assets/offer-capping-placement.png)

   * **[!UICONTROL Alle Platzierungen]**: Die Begrenzungswerte beziehen sich auf alle Entscheidungen in allen Platzierungen, die mit dem Angebot verbunden sind.

      Wenn beispielsweise ein Angebot eine **E-Mail**-Platzierung und eine **Web**-Platzierung hat und Sie die Begrenzung mit **2 pro Profil für alle Platzierungen** festlegen, kann jedes Profil unabhängig vom Platzierungs-Mix das Angebot insgesamt bis zu zweimal erhalten.

   * **[!UICONTROL Einzelne Platzierung]**: Die Begrenzungswerte beziehen sich auf jede einzelne Platzierung.

      Wenn beispielsweise ein Angebot eine **E-Mail**-Platzierung und eine **Web**-Platzierung hat und Sie die Begrenzung auf **2 pro Profil für jede Platzierung** festlegen, kann jedes Profil das Angebot bis zu zweimal für die E-Mail-Platzierung und zusätzlich zweimal für die Web-Platzierung erhalten.

1. Sobald das Angebot gespeichert und validiert wurde und die Anzahl der in diesem Feld angegebenen Male in Übereinstimmung mit den Kriterien und dem von Ihnen definierten Zeitraum angezeigt wurde, stoppt die Bereitstellung.

Die Häufigkeit, mit der ein Angebot vorgeschlagen wird, wird zum Zeitpunkt der E-Mail-Vorbereitung berechnet. Wenn Sie z. B. eine E-Mail mit mehreren Angeboten vorbereiten, wird diese Anzahl dem Begrenzungswert angerechnet, unabhängig davon, ob die E-Mail gesendet wird oder nicht.

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>Die Begrenzungszähler werden zurückgesetzt, wenn das Angebot abgelaufen ist, oder 2 Jahre nach dem Anfangsdatum des Angebots, je nachdem, was zuerst eintritt. In [diesem Abschnitt](creating-personalized-offers.md#create-offer) erfahren Sie, wie Sie das Datum eines Angebots definieren.

### Auswirkungen von Datumsänderungen auf die Begrenzung {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="Das Ändern von Datumsangaben kann sich auf die Begrenzung auswirken"
>abstract="Wenn auf ein Angebot eine Begrenzung angewendet wird, kann sich die Änderung des Anfangs- oder Enddatums auf das Angebot auswirken."

Sie müssen beim Ändern des Datums eines Angebots mit Vorsicht vorgehen, da dies Auswirkungen auf die Begrenzung haben kann, wenn die folgenden Voraussetzungen gegeben sind:

* Das Angebot wurde [genehmigt](#review).
* Auf das Angebot wurde eine [Begrenzung](#capping) angewendet.
* Die Begrenzung ist für einzelne Profile definiert.

>[!NOTE]
>
>In [diesem Abschnitt](creating-personalized-offers.md#create-offer) erfahren Sie, wie Sie das Datum eines Angebots definieren.

Wenn die Begrenzung für einzelne Profile festgelegt ist, wird für jedes Profil die Anzahl der Nachrichten erfasst. Wenn Sie das Anfangs- und Enddatum eines genehmigten Angebots ändern, kann sich der Begrenzungswert für einige Profile entsprechend den unten beschriebenen Szenarien auswirken.

![](../assets/offer-capping-change-date.png)

Im Folgenden finden Sie die möglichen Szenarien für **das Ändern des Anfangsdatums eines Angebots**:

| Szenario:<br>Wenn ... | Was geschieht:<br>dann ... | Mögliche Auswirkungen auf den Begrenzungswert |
|--- |--- |--- |
| ... das Anfangsdatum des Angebots vor Beginn des ursprünglichen Angebotsstartdatums geändert wird, | ... beginnt der Begrenzungswert am neuen Anfangsdatum. | Nein |
| ... das neue Anfangsdatum vor dem aktuellen Enddatum liegt, | ... wird die Begrenzung mit dem neuen Anfangsdatum fortgesetzt und der vorherige Begrenzungswert wird für jedes Profil übernommen. | Nein |
| ... das neue Anfangsdatum hinter dem aktuellen Enddatum liegt, | ... läuft die aktuelle Begrenzung ab und der neue Begrenzungswert beginnt für alle Profile am neuen Anfangsdatum wieder bei 0. | Ja |

Im Folgenden finden Sie mögliche Szenarien für **die Verlängerung des Enddatums eines Angebots**:

| Szenario:<br>Wenn ... | Was geschieht:<br>dann ... | Mögliche Auswirkungen auf den Begrenzungswert |
|--- |--- |--- |
| ... eine Entscheidungsanfrage vor dem ursprünglichen Enddatum eines Angebots erfolgt, | ... wird der Begrenzungswert aktualisiert und der vorherige Begrenzungswert wird für jedes Profil übernommen. | Nein |
| ... keine Entscheidungsanfrage vor dem ursprünglichen Enddatum erfolgt, | ... wird der Begrenzungswert am ursprünglichen Enddatum für jedes Profil zurückgesetzt. Der neue Begrenzungswert beginnt dann für alle neuen Entscheidungsanfragen, die nach dem ursprünglichen Enddatum erfolgen, wieder bei 0. | Ja |

**Beispiel**

Angenommen, Sie haben ein Angebot mit dem ursprünglichen Anfangsdatum **1. Januar**, das am **31. Januar** abläuft.

1. Den Profilen X, Y und Z wird das Angebot gezeigt.
1. Am **10. Januar** wird das Enddatum des Angebots in **15. Februar** geändert.
1. **Vom 11. bis zum 31. Januar** wird das Angebot nur Profil Z gezeigt.

   * Da eine Entscheidungsanfrage vor dem ursprünglichen Enddatum erfolgt ist, kann **für Profil Z** das Enddatum des Angebots auf **15. Februar** verlängert werden.
   * Da jedoch für **Profil X und Y** keine Aktivität vor dem ursprünglichen Enddatum stattfand, laufen ihre Zähler ab und ihre Begrenzungswerte werden am **31. Januar** auf 0 zurückgesetzt.

![](../assets/offer-capping-change-date-ex.png)
