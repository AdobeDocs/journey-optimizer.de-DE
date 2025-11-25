---
solution: Journey Optimizer
product: journey optimizer
title: Suche nach Erlebnisereignissen in Journeys
description: Informationen zum Verwenden der Suche nach Erlebnisereignissen in Journeys
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '949'
ht-degree: 100%

---

# Suche nach einem Erlebnisereignis in Journeys {#ee-journeys}

>[!CAUTION]
>
>Seit dem 8. Juli 2025 wird in neuen Kundenorganisationen das Erstellen von Ausdrücken mit Erlebnisereignissen im in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Nachfolgend werden alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logiken mit Erlebnisereignissen beschrieben.
>
>Sie würden gerne mehr erfahren? [Lesen Sie die häufig gestellten Fragen](#faq-ee).

Auf dieser Seite werden gängige Muster und skalierbare Ansätze beschrieben, mit denen Sie die Erlebnisereignisse in Adobe Journey Optimizer optimal nutzen können. Diese Anwendungsfälle helfen Ihnen, häufige Herausforderungen zu lösen, wie z. B. das Verwalten von Opt-outs, das Steuern der Häufigkeit von Nachrichten, das Personalisieren von Inhalten basierend auf dem Benutzerverhalten und das Reagieren auf Echtzeitsignale.

Mithilfe dieser Strategien können Sie Verhaltensdaten in aussagekräftige Aktionen umwandeln, nämlich das Unterdrücken, Qualifizieren oder Ausschließen von Profilen basierend auf den von ihnen ausgelösten Ereignissen oder ihren enthaltenen Attributen. Unabhängig davon, ob Sie eine Logik für Kaufschwellen, Abbruch-Trigger oder die Handhabung von Bounces erstellen, bieten diese Beispiele praktische Anleitungen, die Sie an Ihre Anforderungen anpassen können.

Berücksichtigen Sie bei der Bewertung, welcher Ansatz am besten geeignet ist, die Latenzanforderungen Ihres Anwendungsfalls, um sicherzustellen, dass Ihre Journeys responsiv und effektiv bleiben.

## Unterdrückung von Opt-outs

Um Profile zu unterdrücken, die sich von Marketing-Nachrichten abgemeldet haben, verwenden Sie die integrierte Einverständnisverwaltung. Opt-out-Voreinstellungen werden automatisch in den Einverständnisfeldern des Profils erfasst. Sie können direkt in Journey-Bedingungen referenziert werden und werden von Journey Optimizer während des Nachrichtenversands automatisch durchgesetzt.

Weitere Informationen:

* [Einverständnisverwaltung](../privacy/opt-out.md)
* [Opt-out-Verwaltung für E-Mails](../email/email-opt-out.md)
* [Opt-out-Verwaltung für Textnachrichten](../sms/sms-opt-out.md)


## Unterdrückung bei Bounces

Um Profile auszuschließen, bei denen E-Mail-Bounces aufgetreten sind, nutzen Sie die automatische Unterdrückungsliste von Adobe Journey Optimizer für unzustellbare Adressen. Dieser integrierte Mechanismus stellt sicher, dass ungültige oder unerreichbare E-Mail-Adressen von zukünftigen Sendungen ausgeschlossen werden, ohne dass eine benutzerdefinierte Logik erforderlich ist.

Weitere Informationen:

* [Verwalten der Unterdrückungsliste](../configuration/manage-suppression-list.md)


## Generische Unterdrückung

Um Profile zu unterdrücken, die bestimmte Verhaltensweisen gezeigt haben, verwenden Sie Batch-Zielgruppen mit ereignisbasierter Logik zum Erfassen von Profilen, die die Unterdrückungskriterien erfüllen. Referenzieren Sie diese Zielgruppe in den Journey-Bedingungen.

Weitere Informationen:

* Adobe Experience Platform [Segment Builder – Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder – Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)


## Ausschluss nach Nachrichtenempfang

So verhindern Sie, dass Nachrichten an Profile gesendet werden, die kürzlich Nachrichten erhalten haben:

* Verwenden Sie Batch-Zielgruppen mit zeitbasierten Kriterien und referenzieren Sie sie in den Journey-Bedingungen.
* Wenden Sie Geschäftsregeln für Frequenzbegrenzung an, um tägliche oder wöchentliche Nachrichtenbeschränkungen zu erzwingen.


Weitere Informationen zum Verwenden von Zielgruppen:

* Adobe Experience Platform [Segment Builder – Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder – Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)


Siehe auch:

* [Frequenzbegrenzung nach Kanal und Kommunikationstyp](../conflict-prioritization/channel-capping.md)



## Nachrichtenspezifische Ein-/Ausschlüsse

Um Profile in Abhängigkeit davon ein- oder auszuschließen, ob sie eine bestimmte Nachricht erhalten haben, erstellen Sie Batch-Zielgruppen, die diese Logik enthalten, und referenzieren Sie sie in den Journey-Bedingungen.


Weitere Informationen:

* Adobe Experience Platform [Segment Builder – Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder – Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-a-segment)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)

## Personalisierung bei Verlassen des Warenkorbs oder der Seite

So personalisieren Sie die Nachrichten basierend auf den letzten Ereignissen im Zusammenhang mit dem Warenkorb oder der Seitennavigation über mehrere Warenkorbtypen oder Produktansichten hinweg:

* Wenn Sie über Zugriff auf [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/de/docs/experience-platform/query/data-distiller/overview){target="_blank"} verfügen, konfigurieren Sie automatisierte Abfragen, um die erforderlichen Daten aus dem Ereignis zu extrahieren, sie an den Anwendungsfall anzupassen und sie zur Aktivierung zurück in einen für das Profil aktivierten Datensatz zu schreiben.
* Wenn die Daten zum Abbruchverhalten anhand des Profils mit Skalarattributen modelliert werden können, sollten Sie berechnete Attribute verwenden, um die neuesten Informationen zu erfassen, und diese Attribute dann in der Journey referenzieren, um Nachrichten zu erstellen. [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}.


## Verhaltensbasierter Journey-Ausstieg

Um Profile aufgrund eines bestimmten Verhaltens aus einer Journey zu entfernen, verwenden Sie Ausstiegskriterien, die Profile bei Empfang eines bestimmten Ereignisses oder bei Qualifizierung des Profils für eine bestimmte Zielgruppe aus der Journey ausschließen.

Weitere Informationen:

* [Festlegen der Journey-Eigenschaften – Ausstiegskriterien](journey-properties.md#exit-criteria)

## Kaufbasierte Qualifizierung mit Wertschwellen

Um Journeys basierend auf Käufen auszulösen und zu unterdrücken, wenn der Wert über oder unter einem Schwellenwert liegt, definieren Sie berechnete Attribute, um Käufe über einen bestimmten Zeitraum zu addieren. Erstellen Sie eine Zielgruppe, die Profile enthält, deren Ausgabenbetrag bestimmte Kriterien erfüllt.

Weitere Informationen:

* Adobe Experience Platform [Berechnete Attribute – Überblick](https://experienceleague.adobe.com/de/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Häufig gestellte Fragen {#faq-ee}

Im Folgenden finden Sie häufig gestellte Fragen zum Suchen nach Erlebnisereignissen in Journeys.

Sie würden gerne mehr erfahren? Verwenden Sie die Feedback-Optionen unten auf dieser Seite, um Ihre Frage zu stellen, oder vernetzen Sie sich mit der [Adobe Journey Optimizer-Community](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=de){target="_blank"}.

+++Welche spezifischen Funktionen sind betroffen? 

Nur die Suche nach Erlebnisereignissen im Ausdruckseditor ist betroffen. Die folgenden Funktionen sind **nicht** betroffen und funktionieren weiterhin unverändert:

* Beobachten der mit einem bestimmten Profil verknüpften Erlebnisereignisse in der Profil-Benutzeroberfläche

* Verwenden von Erlebnisereignissen in Regeln für berechnete Attribute und Zugreifen auf die berechneten Attribute in einer Journey

* Auslösen einer Journey mit einem unitären Ereignis oder einem Geschäftsereignis

* Verwenden von Journey-Kontextdaten aus den Ereignissen, die die Journey im Ausdruckseditor und im Personalisierungseditor auslösen

* Überwachen eines Ereignisses innerhalb einer Journey

* Konfigurieren von Ereignissen, um eine Journey auszulösen

* Erkennen von Reaktionsereignissen von Endbenutzenden auf Marketing-Nachrichten (z. B. geöffnete E-Mails)

+++

+++Ist meine bestehende Adobe-Organisation von dieser Aktualisierung betroffen? 

Ihre Adobe-Organisation ist nur betroffen, wenn Sie die Suche nach Erlebnisereignissen noch nicht verwenden. Wenn Sie bereits Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) verwenden, verfügt Ihre Adobe-Organisation weiterhin über Support für die Suche nach Erlebnisereignissen.

+++

+++Ich habe eine neue Adobe-Organisation. Wie kann ich meinen Anwendungsfall lösen, der Erlebnisereignisdaten erfordert? 

Alternative Ansätze und Best Practices für Erlebnisereignisse sind oben verfügbar. Mit diesen können Sie gewünschte Anwendungsfälle erreichen.

+++

+++ Was mache ich, wenn alternative Ansätze für meinen Anwendungsfall nicht funktionieren?

Wenn Ihr Anwendungsfall nicht mit einem der oben aufgeführten alternativen Ansätze gelöst werden kann, wenden Sie sich bitte an den Adobe-Support.

+++
