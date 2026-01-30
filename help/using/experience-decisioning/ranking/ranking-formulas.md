---
title: Rangfolgenformeln
description: Erfahren Sie, wie Sie Formeln erstellen, um Angebote zu ordnen
feature: Ranking, Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 35d7488b-e7d8-402f-b337-28a0c869bff0
version: Journey Orchestration
source-git-commit: 21de0b9616c414db204a3eafebc6a8184028a1e1
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 95%

---

# Verwenden des KI-Formel-Builder {#create-ranking-formulas}

**Rangfolgeformeln** ermöglichen es Ihnen, Regeln zu definieren, die bestimmen, welches Angebot zuerst unterbreitet werden soll, anstatt die Prioritätswerte zu berücksichtigen.

Um diese Regeln zu erstellen, bietet der KI-Formel-Builder in **[!UICONTROL Adobe Journey Optimizer]** mehr Flexibilität und Kontrolle bei der Rangfolge von Angeboten. Anstatt sich nur auf eine statische Angebotspriorität zu verlassen, können Sie nun benutzerdefinierte Rangfolgenformeln definieren, die Werte von KI-Modellen, Angebotsprioritäten, Profilattribute, Angebotsattribute und kontextuelle Signale über eine geführte Benutzeroberfläche kombinieren.

Dieser Ansatz ermöglicht es Ihnen, die Angebotsrangfolge dynamisch auf der Grundlage einer beliebigen Kombination aus KI-gesteuerter Tendenz, geschäftlichem Nutzen und Echtzeit-Kontext anzupassen, was die Abstimmung der Entscheidungsfindung auf Marketing-Ziele und Kundenanforderungen erleichtert. Der KI-Formel-Builder unterstützt einfache oder erweiterte Formeln, je nachdem, wie viel Kontrolle Sie anwenden möchten.

Sobald eine Rangfolgenformel erstellt wurde, können Sie diese einer [Auswahlstrategie](../selection-strategies.md) zuweisen. Wenn mit dieser Auswahlstrategie mehrere Angebote für diese Platzierung infrage kommen, verwendet die Entscheidungs-Engine die ausgewählte Formel, um zu berechnen, welches Angebot zuerst bereitgestellt werden soll.

➡️ [Funktion im Video kennenlernen](#video)

## Erstellen einer Rangfolgenformel {#create-ranking-formula}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Erstellen von Ranglistenformeln"
>abstract="Mithilfe von Formeln kann festgelegt werden, welches Entscheidungselement zuerst angezeigt werden soll, anstatt die Prioritätswerte des Elements zu berücksichtigen. Sobald eine Rangfolgenformel erstellt wurde, können Sie diese einer Auswahlstrategie zuweisen."

Gehen Sie wie folgt vor, um eine Rangfolgenformel zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Strategie-Setup]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rangfolgenformeln]** aus. Es wird die Liste der zuvor erstellten Rangfolgen angezeigt.

   ![](../assets/ranking-formulas-list.png)

1. Klicken Sie auf **[!UICONTROL Formel erstellen]**.

1. Geben Sie den Namen der Formel an und fügen Sie bei Bedarf eine Beschreibung hinzu.

   ![](../assets/create-formula.png){width="80%"}

1. Klicken Sie optional auf **[!UICONTROL KI-Modell auswählen]**, um das Modell festzulegen, das als Referenz zur Erstellung der Rangfolgenformel verwendet wird. 

   >[!NOTE]
   >
   >[Personalisierte Optimierungsmodelle](personalized-optimization-model.md), die kontinuierliche Metriken verwenden, werden vom KI-Formel-Builder nicht unterstützt.

   Jedes Mal, wenn Sie bei der Definition Ihrer unten stehenden Formel auf eine Modellbewertung verweisen, wird das von Ihnen ausgewählte KI-Modell verwendet.

   >[!CAUTION]
   >
   >Wenn Sie ein KI-Modell verwenden, das in eine Rangfolgenformel integriert ist, werden Daten nicht im Bericht [Konversionsrate für Holdout und modellgesteuerten Traffic](../../reports/campaign-global-report-cja-code.md#conversion-rate) angezeigt.

1. Definieren Sie die Bedingungen, die den Rangfolgewert für die übereinstimmenden Entscheidungselemente bestimmen. Sie haben folgende Möglichkeiten:

   * Füllen Sie den Abschnitt **[!UICONTROL Kriterien]** über die [Benutzeroberfläche](#ranking-select-criteria) aus,
   * oder wechseln Sie zum [Code-Editor](#ranking-code-editor).

   >[!NOTE]
   >
   >Die Verschachtelungstiefe in einer Rangfolgenformel ist auf 30  Ebenen beschränkt. Diese wird durch Zählen der schließenden Klammern `)` in der PQL-Zeichenfolge gemessen. Eine Regelzeichenfolge kann für UTF-8-kodierte Zeichen bis zu 8 KB groß sein. Dies entspricht 8.000 ASCII-Zeichen (jeweils 1 Byte) oder 2.000 bis 4.000 Nicht-ASCII-Zeichen (jeweils 2 bis 4 Byte). [Weitere Informationen zu den Leitlinien und Einschränkungen für die Entscheidungsfindung](../decisioning-guardrails.md#ranking-formulas)

1. Sie können auch Daten aus Adobe Experience Platform verwenden, um die Rangfolgenlogik dynamisch anzupassen und so reale Bedingungen widerzuspiegeln. Dies ist besonders nützlich bei Attributen, die sich häufig ändern, z. B. Produktverfügbarkeit oder Echtzeitpreise.

   Diese Funktion steht derzeit allen Kundinnen und Kunden als öffentliche Beta-Version zur Verfügung. Wenden Sie sich an Ihren Kontakt in der Kundenbetreuung, wenn Sie Zugriff wünschen. [Informationen zum Verwenden von Adobe Experience Platform-Daten für die Entscheidungsfindung](../aep-data-exd.md)

<!--## Select an ELS dataset {#els-dataset}

Journey Optimizer allows you to leverage data from Adobe Experience Platform. [Learn more](../data/aep-data-perso.md)

To leverage data from an AEP dataset, follow the steps below.

1. From the **[!UICONTROL ELS settings]** section, select an ELS dataset from the list.

1. Select a decision attribute.

    >[!NOTE]
    >
    >This action is mandatory.

![](../assets/formula-els-settings.png){width="80%"-->

## Definieren von Kriterien mithilfe des Formel-Builders {#ranking-select-criteria}

Mit einer intuitiven Benutzeroberfläche können Sie durch die Anpassung von KI-Bewertungen (Tendenz), Angebotswert (Priorität), kontextuellen Hebeln und externen Profiltendenzen die Entscheidungsfindung einzeln oder in Kombination verfeinern, um jede Interaktion zu optimieren. <!--Whether you are maximizing revenue, promoting strategic offers, or balancing business goals with real-time context, the formula builder gives you total control in defining ranking strategies.-->

Gehen Sie wie folgt vor, um Kriterien direkt über die Benutzeroberfläche zu definieren.

<!--![](../assets/ranking-formula-criteria.png){width="80%"}-->

1. Geben Sie im Abschnitt **[!UICONTROL Kriterium 1]** die Entscheidungselemente an, auf die Sie einen Rangfolgenwert anwenden möchten, indem Sie Folgendes durchführen:
   * Wählen Sie ein [Entscheidungselement-Attribut](../items.md#attributes)
   * Logischen Operator auswählen
   * Übereinstimmende Bedingung hinzufügen - Sie können entweder einen Wert eingeben oder ein Profilattribut oder [Kontextdaten“ &#x200B;](../context-data.md)

   ![](../assets/ranking-formula-criterion-1.png){width="70%"}

1. Optional können Sie zusätzliche Elemente angeben, um die übereinstimmenden Bedingungen zu verfeinern, damit Ihre Kriterien erfüllt sind.

   ![](../assets/ranking-formula-addtional-conditions.png){width="80%"}

   Sie haben beispielsweise Kriterium 1 so definiert: „Das benutzerdefinierte Attribut *Wetter* *ist gleich* der Bedingung *Warm*“. Darüber hinaus können Sie eine weitere Bedingung hinzufügen, z. B. wenn die erste Bedingung erfüllt ist und wenn die Temperatur zum Zeitpunkt der Anfrage 23 Grad überschreitet, dann ist Kriterium 1 wahr.<!--Add a screenshot with the example-->

1. Erstellen Sie einen Ausdruck, der den Entscheidungselementen, die die oben definierte Bedingung erfüllen, einen Rangfolgenwert zuweist. Sie können eine der folgenden Optionen referenzieren:

   * die Punktzahl, die aus dem KI-Modell hervorgegangen ist, das Sie optional im Abschnitt **[!UICONTROL Details]** [oben](#create-ranking-formula) ausgewählt haben;
   * die Priorität des Entscheidungselements, die ein Wert ist, der beim [Erstellen eines Entscheidungselements](../items.md#attributes) manuell zugewiesen wird; <!--If a profile qualifies for multiple decision items, a higher priority grants the item precedence over others.-->
   * alle Attribute, die im Profil live sein könnten, z. B. jede extern abgeleitete Tendenzbewertung;
   * ein statischer Wert, den Sie in einem freien Format zuweisen können;
   * jede Kombination der oben genannten Optionen

   ![](../assets/ranking-formula-expression.png){width="70%"}

   >[!NOTE]
   >
   >Klicken Sie auf das Symbol neben dem Feld, um vordefinierte Variablen hinzuzufügen.

1. Klicken Sie auf **[!UICONTROL Kriterium hinzufügen]**, um ein oder mehrere Kriterien beliebig oft hinzuzufügen. Es gilt folgende Logik:
   * Wenn das erste Kriterium für ein bestimmtes Entscheidungselement zutrifft, hat es Vorrang vor den nächsten Kriterien.
   * Wenn dies nicht der Fall ist, wechselt die Entscheidungs-Engine zum zweiten Kriterium usw.

1. Im letzten Feld können Sie einen Ausdruck erstellen, der allen Entscheidungselementen zugewiesen wird, die die oben genannten Kriterien nicht erfüllen.

   ![](../assets/ranking-formula-criteria-not-met.png){width="70%"}

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um Ihre Rangfolgenformel fertigzustellen. Sie können sie jetzt aus der Liste auswählen, um ihre Details anzuzeigen und sie zu bearbeiten oder zu löschen. Sie kann in einer [Auswahlstrategie](../selection-strategies.md) verwendet werden, um die geeigneten Entscheidungselemente in einer Rangfolge zu ordnen.

### Beispiel für Rangfolgenformeln

Siehe das Beispiel unten:

![](../assets/ranking-formula-example.png){width="80%"}

Wenn die Region des Entscheidungselements (benutzerdefiniertes Attribut) gleich dem geografischen Label des Profils (Profilattribut) ist, wird der hier ausgedrückte Rangfolgenwert (eine Kombination aus der Priorität des Entscheidungselements, dem Wert des KI-Modells und einem statischen Wert) auf alle Entscheidungselemente angewendet, die diese Bedingung erfüllen.

## Verwenden des Code-Editors {#ranking-code-editor}

Um Rangfolgenformeln in der **PQL-Syntax** auszudrücken, wechseln Sie mithilfe der entsprechenden Schaltfläche oben rechts auf dem Bildschirm zum Code-Editor. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie in der [entsprechenden Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=de).

>[!CAUTION]
>
>Diese Aktion verhindert ein Zurückkehren zur Standard-Builder-Ansicht für diese Formel.

Anschließend können Sie Profilattribute, [Kontextdaten](../context-data.md) und [Entscheidungselement-Attribute](../items.md#attributes) nutzen.

Sie möchten zum Beispiel die Priorität aller Angebote durch Hinzufügen des Attributs „heiß“ erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben. <!--[Learn how to work with context data](context-data.md)-->

![](../assets/ranking-formula-code-editor.png){width="80%"}

>[!IMPORTANT]
>
>Beim Erstellen einer Rangfolgenformel wird ein Rückblick auf einen früheren Zeitraum nicht unterstützt, z. B. das Hinzufügen eines Erlebnisereignisses, das innerhalb des letzten Monats stattgefunden hat, als Komponente der Formel. Bei jedem Versuch, einen Rückblick-Zeitraum während der Formelerstellung einzubeziehen, wird beim Speichern ein Fehler ausgelöst.

Um Attribute im Zusammenhang mit Ihren Entscheidungselementen in Formeln zu nutzen, stellen Sie sicher, dass Sie die korrekte Syntax im Code Ihrer Rangfolgenformel befolgen. Erweitern Sie jeden Abschnitt, um weitere Informationen zu erhalten:

+++Verwenden von Standardattributen von Entscheidungselementen

![](../assets/formula-attribute.png)

+++

+++Verwenden benutzerdefinierter Attribute von Entscheidungselementen

![](../assets/formula-attribute-custom.png)

+++

### Beispiele für Rangfolgenformel-PQLs {#ranking-formula-examples}

Sie können je nach Bedarf viele verschiedene Rangfolgeformeln erstellen. Im Folgenden finden Sie einige Beispiele.

+++Verstärken von Angeboten mit bestimmten Angebotsattributen auf der Grundlage von Profilattributen

Wenn das Profil in der Stadt lebt, die dem Angebot entspricht, verdoppeln Sie die Priorität für alle Angebote in dieser Stadt.

**Rangfolgeformel:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

+++

+++Verstärken von Angeboten, deren Enddatum in weniger als 24 Stunden liegt

**Rangfolgeformel:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

+++

+++Verstärken von Angeboten entsprechend der Neigung der Kunden, das angebotene Produkt zu kaufen

Sie können die Punktzahl für ein Angebot basierend auf einem Tendenzwert für den Kunden erhöhen.

In diesem Beispiel lautet der Instanzmandant *_salesvelocity* und das Profilschema enthält einen Bereich von Werten, die in einem Array gespeichert sind:

![](../assets/ranking-example-schema.png)

In diesem Fall für ein Profil wie:

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

+++

+++Verstärken von Angeboten basierend auf der Postleitzahl und dem Jahreseinkommen eines Profils

In diesem Beispiel versucht das System immer zuerst, ein Angebot anzuzeigen, das mit der Postleitzahl übereinstimmt. Wenn keine Übereinstimmung gefunden wird, wird ein allgemeines Angebot verwendet und die Anzeige von Angeboten für andere Postleitzahlen wird vermieden.

```pql
if( offer._luma.offerDetails.zipCode = _luma.zipCode,luma.annualIncome / 1000 + 10000, if( not offer.luma.offerDetails.zipCode,_luma.annualIncome / 1000, -9999) )
```

Was die Formel bewirkt:

* Wenn das Angebot dieselbe Postleitzahl wie die Benutzerin bzw. der Benutzer hat, weisen Sie ihm eine sehr hohe Punktzahl zu, damit es zuerst ausgewählt wird.
* Wenn das Angebot überhaupt keine Postleitzahl hat (es handelt sich um ein allgemeines Angebot), geben Sie ihm eine normale Punktzahl, die auf dem Einkommen der Benutzerin bzw. des Benutzers basiert.
* Wenn das Angebot eine andere Postleitzahl hat als die Benutzerin bzw. der Benutzer, geben Sie ihm eine sehr niedrige Punktzahl, damit es nicht ausgewählt wird.

+++

+++Verstärken von Angeboten basierend auf Kontextdaten

Mit [!DNL Journey Optimizer] können Sie bestimmte Angebote basierend auf Kontextdaten verstärken, die beim Entscheidungsaufruf übergeben werden. Wenn beispielsweise `contextData.weather=hot` übergeben wird, muss die Priorität aller Angebote mit `attribute=hot` erhöht werden.

>[!NOTE]
>
>Weiterführende Informationen zum Übergeben von Kontextdaten<!-- using the **Edge Decisioning** and **Decisioning** APIs--> finden Sie in [diesem Abschnitt](../context-data.md).

Beachten Sie, dass bei Verwendung des **Decisioning**-API die Kontextdaten zum Profilelement im Anfragehauptteil hinzugefügt werden wie im folgenden Beispiel:

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
    
}],
```

+++

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie mit dem KI-Formel-Builder in Adobe Journey Optimizer Strategien für die benutzerdefinierte Rangfolge von Angeboten erstellen.

>[!VIDEO](https://video.tv.adobe.com/v/3464446/?learn=on&enablevpops)
