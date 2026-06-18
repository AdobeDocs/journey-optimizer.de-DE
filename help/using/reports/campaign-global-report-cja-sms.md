---
solution: Journey Optimizer
product: journey optimizer
title: Kampagnenbericht
description: Informationen zum Verwenden von SMS-Daten aus dem Kampagnenbericht
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bd743a3b-0317-45d9-8e76-98d5cc258752
TQID: https://experienceleague.adobe.com/dFM14bh1Yil9GUsCk3mkcqz6QNH3fUWmQCNtj-FnWfA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f10f2b6cbad242efca31c84ce8adf5a615f57c1e
workflow-type: tm+mt
source-wordcount: 955
ht-degree: 65%

---

# SMS-Kampagnenbericht {#campaign-global-report-cja-sms}

>[!BEGINSHADEBOX]

**Auf dieser Seite** Sie, wie Sie den SMS-Kampagnenbericht in Adobe Journey Optimizer lesen, um die Versand- und Klick-Trends, den Versandstatus, getrackte Links, eingehende Nachrichten und Bounce-, Fehler- und Ausschlussgründe für Ihre SMS-Nachrichten zu analysieren.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Sie können auf Ihren SMS-Kampagnenbericht zugreifen, indem Sie in Ihrer Kampagne auf die Schaltfläche **[!UICONTROL Berichte]** klicken und dann **[!UICONTROL Bericht für gesamte Zeit anzeigen]** auswählen. [Weitere Informationen](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Versand- vs. Klick-Trend {#delivered-click-sms}

![](assets/cja-campaign-sms-delivered.png)

Der Graph **[!UICONTROL Versand- vs. Klick-Trend]** zeigt eine detaillierte Analyse der Interaktion Ihrer Profile mit Ihren E-Mails und bietet wertvolle Erkenntnisse zur Interaktion verschiedener Profile mit Ihrem Inhalt.

+++ Weitere Informationen zu den Metriken „Trend ‚Versandt vs. angeklickt‘“

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten im Verhältnis zur Gesamtzahl der SMS-Nachrichten.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren SMS-Nachrichten.

+++

## Versandstatus {#delivery-status-sms}

![](assets/cja-campaign-sms-status.png)

Die Tabelle **[!UICONTROL Versandstatus]** bietet eine detaillierte Übersicht über die Profilaktivitäten im Zusammenhang mit Ihren SMS-Kampagnen. Dazu gehören Metriken zu gesendeten SMS-Nachrichten, Klicks und andere relevante Interaktionsindikatoren, die einen umfassenden Überblick darüber bieten, wie Profile mit Ihrem SMS-Inhalt interagieren.

+++ Weitere Informationen zu den Metriken „Versandstatus“

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten SMS-Nachrichten im Verhältnis zur Gesamtzahl der SMS-Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler während des Sendevorgangs und der automatischen Rücksendung in Relation zur Gesamtzahl der gesendeten SMS-Nachrichten.

* **[!UICONTROL Fehler senden]**: Gesamtzahl der Fehler, die aufgetreten sind und den Versand an Profile verhindert haben.

* **[!UICONTROL Ausschlüsse senden]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden.

+++

## Kampagnen-Überblick {#campaign-global}

Die **[!UICONTROL Kampagnenübersicht]** dient als Dashboard für die SMS-Leistung in Ihrer Kampagne. Es fasst Zielgruppenprofile, Clickthrough-Metriken (einschließlich geschätzter Klicks, durch die nicht nur menschlicher Interaktions-Traffic ausgeschlossen ist) und Versandergebnisse wie Bounces, Versandfehler und Ausschlüsse zusammen.

+++ Weitere Informationen zu den Metriken „Kampagnenüberblick“

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre Nachrichten eignen.

* **[!UICONTROL Klickrate]**: Prozentsatz der Benutzenden, die mit der Nachricht interagiert haben.

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihrer Nachricht.

* **[!UICONTROL Einzelklicks]**: Anzahl der eindeutigen Profile, die auf mindestens einen Inhalt in der Nachricht für Mobilgeräte geklickt haben.

* **[!UICONTROL Geschätzte Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihrer Nachricht, mit Ausnahme des identifizierten Traffics von Bots und Nicht-Menschen-Interaktionen (NHI).

* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten E-Mails im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Bounces]**: Gesamtzahl der kumulierten Fehler während des Sendevorgangs und der automatischen Rücksendung im Verhältnis zur Gesamtzahl der gesendeten Nachrichten.

* **[!UICONTROL Fehler senden]**: Gesamtzahl der Fehler, die während des Sendevorgangs aufgetreten sind und den Versand an Profile verhindert haben.

* **[!UICONTROL Ausschlüsse senden]**: Anzahl der Profile, die durch Adobe Journey Optimizer ausgeschlossen wurden. [Erfahren Sie mehr darüber, wie Ausschlüsse gezählt werden](exclusion-list.md#exclusion-list).

+++

## Getrackte Labels {#track-label-sms}

Die **[!UICONTROL Verfolgte Kennzeichnungen]**-Tabelle bietet einen umfassenden Überblick über die Link-Kennzeichnungen in Ihren SMS-Nachrichten, wobei die Kennzeichnungen hervorgehoben werden, die den höchsten Besucher-Traffic generieren. Mit dieser Funktion können Sie die beliebtesten Links identifizieren und priorisieren.

+++ Weitere Informationen zu den Metriken „Labels für verfolgten Link“

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren SMS-Nachrichten.

* **[!UICONTROL Geschätzte Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihrer Nachricht, mit Ausnahme des identifizierten Traffics von Bots und Nicht-Menschen-Interaktionen (NHI).

* **[!UICONTROL Einzelklicks]**: Anzahl der eindeutigen Profile, die auf mindestens einen Inhalt in der Nachricht für Mobilgeräte geklickt haben.

+++

## Nachverfolgte Link-URLs {#track-link-url-sms}

Die Tabelle **[!UICONTROL Nachverfolgte Link-URLs]** bietet einen umfassenden Überblick über die URLs in Ihren SMS-Nachrichten, die den höchsten Besucher-Traffic anziehen. Auf diese Weise können Sie die beliebtesten Links identifizieren und priorisieren und Ihr Verständnis der Profilinteraktion mit bestimmten Inhalten in Ihren SMS-Nachrichten verbessern.

+++ Weitere Informationen zu den Metriken „Nachverfolgte Link-URLs“

* **[!UICONTROL Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihren SMS-Nachrichten.

* **[!UICONTROL Geschätzte Klicks]**: Anzahl der Klicks auf einen Inhalt in Ihrer Nachricht, mit Ausnahme des identifizierten Traffics von Bots und Nicht-Menschen-Interaktionen (NHI).

* **[!UICONTROL Einzelklicks]**: Anzahl der eindeutigen Profile, die auf mindestens einen Inhalt in der Nachricht für Mobilgeräte geklickt haben.

* **[!UICONTROL Anzeigen]**: Anzahl der Öffnungen der Nachricht.

* **[!UICONTROL Einzelanzeigen]**: Anzahl der Öffnungen der Nachricht, wobei mehrfache Interaktionen eines Profils nicht gezählt werden.

+++

## Eingehende SMS-Nachricht {#sms-inbound}

Die Tabelle **[!UICONTROL Eingehende SMS-Nachricht]** bietet einen umfassenden Überblick über die SMS-Nachrichten, die den meisten Besucher-Traffic angezogen haben. Diese Ressource bietet wertvolle Erkenntnisse zur Interaktionsdynamik von Zielgruppen.

+++ Weitere Informationen zu Metriken für eingehende SMS-Nachrichten

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre SMS-Nachrichten eignen.

+++

## SMS-Nachrichtentyp {#sms-message-type}

Die Tabelle **[!UICONTROL SMS-Nachrichtentyp]** bietet einen umfassenden Überblick darüber, welcher SMS-Nachrichtentyp den höchsten Besucher-Traffic angezogen hat. Diese Ressource bietet wertvolle Erkenntnisse zur Interaktionsdynamik von Zielgruppen.

+++ Weitere Informationen zu Metriken für den SMS-Nachrichtentyp

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre SMS-Nachrichten eignen.

+++

## SMS-Anbieter {#sms-providers}

Die Tabelle **[!UICONTROL SMS-Anbieter]** bietet einen umfassenden Überblick über die SMS-Anbieter, die den höchsten Besucher-Traffic erzielt haben. Diese Ressource bietet wertvolle Erkenntnisse zur Interaktionsdynamik von Zielgruppen.

+++ Weitere Informationen zu Metriken für SMS-Anbieter

* **[!UICONTROL Personen]**: Anzahl der Benutzerprofile, die sich als Zielgruppenprofile für Ihre SMS-Nachrichten eignen.

+++

## Bounce-Gründe {#bounce-reasons-sms}

Die Tabelle **[!UICONTROL Bounce-Gründe]** bietet einen umfassenden Überblick über Daten zu nicht zugestellten SMS-Nachrichten und liefert wertvolle Erkenntnisse zu den spezifischen Ursachen von nicht zugestellten SMS-Nachrichten.

## Fehlergründe {#error-reasons-sms}

Anhand der Tabelle **[!UICONTROL Fehlergründe]** können Sie die spezifischen Fehler identifizieren, die während des Sendevorgangs Ihrer SMS-Nachrichten aufgetreten sind. Dies ermöglicht eine gründliche Analyse aller aufgetretenen Probleme.

## Gründe für Ausschluss {#excluded-reasons-sms}

Die Tabelle **[!UICONTROL Gründe für Ausschluss]** zeigt visuell die verschiedenen Faktoren auf, die zum Ausschluss von Benutzerprofilen aus der Zielgruppe geführt haben, sodass diese keine SMS-Nachrichten von Ihnen erhalten konnten.

Auf [dieser Seite](exclusion-list.md) finden Sie eine umfassende Liste der Ausschlussgründe.
