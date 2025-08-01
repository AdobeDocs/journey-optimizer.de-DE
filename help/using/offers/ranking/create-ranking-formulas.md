---
title: Rangfolgenformeln
description: Erfahren Sie, wie Sie Formeln erstellen, um Angebote zu ordnen
badge: label="Legacy" type="Informative"
feature: Ranking, Decision Management
topic: Integrations
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: ht
source-wordcount: '596'
ht-degree: 100%

---

# Rangfolgenformeln {#create-ranking-formulas}

## Grundlagen zu Rangfolgeformeln {#about-ranking-formulas}

Mithilfe von **Rangfolgeformeln** können Sie festlegen, welches Angebot für eine bestimmte Platzierung zuerst angezeigt werden soll, anstatt die Prioritätswerte der Angebote zu berücksichtigen.

Rangfolgeformeln werden in der **PQL-Syntax** angegeben und können Profil-, Kontextdaten- und Angebotsattribute nutzen. Weiterführende Informationen zur Verwendung der PQL-Syntax finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/pql/overview).

Nachdem Sie eine Rangfolgenformel erstellt haben, können Sie sie einer Platzierung in einer Entscheidung zuweisen. Weitere Informationen dazu finden Sie unter [Konfigurieren der Auswahl von Angeboten in Entscheidungen](../offer-activities/configure-offer-selection.md).

## Erstellen einer Rangfolgeformel {#create-ranking-formula}

Gehen Sie wie folgt vor, um eine neue Rangfolgeformel zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Komponenten]** auf und wählen Sie dann die Registerkarte **[!UICONTROL Rangfolge]** aus. Die Registerkarte **[!UICONTROL Formeln]** ist standardmäßig ausgewählt. Es wird die Liste der zuvor erstellten Rangfolgen angezeigt.

   ![](../assets/rankings-list.png)

1. Klicken Sie auf **[!UICONTROL Rangfolge erstellen]**, um eine neue Rangfolgeformel zu erstellen.

   ![](../assets/ranking-create-formula.png)

1. Geben Sie den Namen und die Beschreibung der Formel sowie die Formel selbst an.

   In diesem Beispiel möchten wir die Priorität aller Angebote durch Hinzufügen des Attributs „heiß“ erhöhen, wenn das Wetter heiß ist. Zu diesem Zweck wurde **contextData.weather=hot** im Entscheidungsaufruf übergeben. [Weitere Informationen zum Arbeiten mit Kontextdaten](../context-data.md)

   ![](../assets/ranking-syntax.png)

   >[!IMPORTANT]
   >
   >Beim Erstellen einer Ranglistenformel wird ein Rückblick in einen vorherigen Zeitraum nicht unterstützt. So kann es beispielsweise sein, dass Sie als Bestandteil der Formel ein Erlebnisereignis angeben, das innerhalb des letzten Monats stattgefunden hat. Bei jedem Versuch, einen Rückblick-Zeitraum während der Formelerstellung einzubeziehen, wird beim Speichern ein Fehler ausgelöst.

1. Klicken Sie auf **[!UICONTROL Speichern]**. Ihre Rangfolgeformel wird erstellt. Sie können sie aus der Liste auswählen, um Details abzurufen und sie zu bearbeiten oder zu löschen.

   Sie kann jetzt in einer Entscheidung verwendet werden, um die geeigneten Angebote für eine Platzierung zu reihen (siehe [Auswahl der Angebote in Entscheidungen konfigurieren](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)

## Beispiele für Rangfolgeformeln {#ranking-formula-examples}

Sie können je nach Bedarf viele verschiedene Rangfolgeformeln erstellen. Im Folgenden finden Sie einige Beispiele.

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's audience membership

Boost the priority of offers based on whether the user is a member of a priority audience, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.get("prioritySegmentId")).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Verstärken von Angeboten mit bestimmten Angebotsattributen auf der Grundlage von Profilattributen

Wenn das Profil in der Stadt lebt, die dem Angebot entspricht, verdoppeln Sie die Priorität für alle Angebote in dieser Stadt.

**Rangfolgeformel:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Verstärken von Angeboten, deren Enddatum in weniger als 24 Stunden liegt

**Rangfolgeformel:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Verstärken von Angeboten entsprechend der Neigung der Kunden, das angebotene Produkt zu kaufen

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

### Verstärken von Angeboten basierend auf Kontextdaten {#context-data}

Mit [!DNL Journey Optimizer] können Sie bestimmte Angebote basierend auf Kontextdaten verstärken, die beim Entscheidungsaufruf übergeben werden. Wenn beispielsweise `contextData.weather=hot` im Entscheidungsaufruf übergeben wird, muss die Priorität aller Angebote mit `attribute=hot` erhöht werden. Detaillierte Informationen zum Übergeben von Kontextdaten mithilfe der **Edge Decisioning**- und der **Decisioning**-API finden Sie [diesem Abschnitt](../context-data.md)

Beachten Sie, dass bei Verwendung der **Decisioning**-API die Kontextdaten zum Profilelement im Anfragehauptteil hinzugefügt werden wie im folgenden Beispiel.

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

Im Folgenden finden Sie Beispiele, die veranschaulichen, wie Kontextdaten in Rangfolgeformeln verwendet werden können, um die Priorität von Angeboten zu erhöhen. Erweitern Sie jeden Abschnitt, um Details zur Syntax der Rangfolgenformel zu erhalten.

>[!NOTE]
>
>Ersetzen Sie in den Beispielen für die Edge Decisioning-API `<OrgID>` durch Ihre Organisations-Mandanten-ID.

+++Erhöhen Sie die Angebotspriorität um 10, wenn der Kanal aus den Kontextdaten mit dem bevorzugten Kanal der Kundin bzw. des Kunden übereinstimmt

>[!BEGINTABS]

>[!TAB Decisioning-API]

`if (@{_xdm.context.additionalParameters;version=1}.channel.isNotNull() and @{_xdm.context.additionalParameters;version=1}.channel.equals(_abcMobile.preferredChannel), offer.rank.priority + 10, offer.rank.priority)`

>[!TAB Edge Decisioning-API]

`if (xEvent.<OrgID>.channel.isNotNull() and xEvent.<OrgID>.channel.equals(_abcMobile.preferredChannel), offer.rank.priority + 10, offer.rank.priority)`

>[!ENDTABS]

+++

+++Erhöhen Sie die Priorität aller Angebote mit „attribute=hot“, wenn „contextData.weather=hot“ im Aufruf übergeben wird.

>[!BEGINTABS]

>[!TAB Decisioning-API]

`if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull() and offer.characteristics.get("weather")=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)`

>[!TAB Edge Decisioning-API]

`if (xEvent.<OrgID>.weather.isNotNull() and offer.characteristics.get("weather")=xEvent.<OrgID>.weather, offer.rank.priority + 5, offer.rank.priority)`

>[!ENDTABS]

+++

+++Inhaltsherkunftsverstärkung

>[!BEGINTABS]

>[!TAB Decisioning-API]

`if (@{_xdm.context.additionalParameters;version=1}.contentorigin.isNotNull() and offer.characteristics.contentorigin=@{_xdm.context.additionalParameters;version=1}.contentorigin, offer.rank.priority * 100, offer.rank.priority)`

>[!TAB Edge Decisioning-API]

`if (xEvent.<OrgID>.contentorigin.isNotNull() and offer.characteristics.contentorigin=xEvent.<OrgID>.contentorigin, offer.rank.priority * 100, offer.rank.priority)`

>[!ENDTABS]

+++

+++Wetterverstärkung

>[!BEGINTABS]

>[!TAB Decisioning-API]

`if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull() and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority * offer.characteristics.scoringBoost, offer.rank.priority)`

>[!TAB Edge Decisioning-API]

`if (xEvent.<OrgID>.weather.isNotNull() and offer.characteristics.weather=xEvent.<OrgID>.weather, offer.rank.priority * offer.characteristics.scoringBoost, offer.rank.priority)`

>[!ENDTABS]

+++
