---
solution: Journey Optimizer
product: journey optimizer
title: Suche nach Erlebnisereignissen in Journey
description: Erfahren Sie, wie Sie die Suche nach Erlebnisereignissen in Journey verwenden
source-git-commit: 190d7d5fd5cb93a6ddf3757e00f42a9714a1f722
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 6%

---


# Suche nach Erlebnisereignissen in Journey {#ee-journeys}

>[!CAUTION]
>
>Ab dem 8. Juli wird das Erstellen von Ausdrücken mit Erlebnisereignissen in neuen Kundenorganisationen in dem in Journey-Bedingungen verwendeten Ausdruckseditor nicht mehr unterstützt. Daher können Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) nicht zum Erstellen von Ausdrücken verwendet werden. Nachfolgend werden alternative Ansätze und Best Practices zum Erstellen von Ausdrücken/Logiken mit Erlebnisereignissen beschrieben.
>
>Benötigen Sie weitere Details? [Lesen Sie die häufig gestellten Fragen](#faq-ee).

Auf dieser Seite werden gängige Muster und skalierbare Ansätze beschrieben, mit denen Sie die Erlebnisereignisse in Adobe Journey Optimizer optimal nutzen können. Diese Anwendungsfälle helfen Ihnen, häufige Herausforderungen zu lösen, wie z. B. das Verwalten von Opt-outs, das Steuern der Häufigkeit von Nachrichten, das Personalisieren von Inhalten basierend auf dem Benutzerverhalten und das Reagieren auf Echtzeitsignale.

Mithilfe dieser Strategien können Sie Verhaltensdaten in aussagekräftige Aktionen umwandeln - Unterdrücken, Qualifizieren oder Ausschließen von Profilen basierend auf den von ihnen Trigger Ereignissen oder den Attributen, die sie enthalten. Unabhängig davon, ob Sie eine Logik für Kaufschwellen, Trigger bei Abbrüchen oder die Handhabung von Bounces erstellen, bieten diese Beispiele praktische Anleitungen, die Sie an Ihre Anforderungen anpassen können.

Berücksichtigen Sie bei der Bewertung, welcher Ansatz am besten geeignet ist, die Latenzanforderungen Ihres Anwendungsfalls, um sicherzustellen, dass Ihre Journey reaktionsfähig und effektiv bleiben.

## Unterdrückung des Opt-outs

Verwenden Sie die integrierte Einverständnisverwaltung, um Profile zu unterdrücken, die sich von Marketing-Nachrichten abgemeldet haben. Opt-out-Voreinstellungen werden automatisch in den Einverständnisfeldern des Profils erfasst; sie können direkt in Journey-Bedingungen referenziert werden und werden von Journey Optimizer während des Nachrichtenversands automatisch durchgesetzt.

Weitere Informationen:

* [Einverständnisverwaltung](../privacy/opt-out.md)
* [Opt-out-Verwaltung für E-Mails](../email/email-opt-out.md)
* [Opt-out-Verwaltung für Textnachrichten](../sms/sms-opt-out.md)


## Bounce-basierte Unterdrückung

Um Profile auszuschließen, bei denen E-Mail-Bounces aufgetreten sind, nutzen Sie die automatische Unterdrückungsliste von Adobe Journey Optimizer für unzustellbare Adressen. Dieser integrierte Mechanismus stellt sicher, dass ungültige oder nicht erreichbare E-Mails von zukünftigen Sendungen ausgeschlossen werden, ohne dass eine benutzerdefinierte Logik erforderlich ist.

Weitere Informationen:

* [Verwalten der Unterdrückungsliste](../configuration/manage-suppression-list.md)


## Generische Unterdrückung

Um Profile zu unterdrücken, die bestimmte Verhaltensweisen gezeigt haben, verwenden Sie Batch-Zielgruppen mit ereignisbasierter Logik, um Profile zu erfassen, die die Unterdrückungskriterien erfüllen. Referenzieren Sie diese Zielgruppe unter Journey-Bedingungen.

Weitere Informationen:

* Adobe Experience Platform [Segment Builder - Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder - Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)


## Ausschluss vom Nachrichtenempfang

So verhindern Sie, dass Nachrichten an Profile gesendet werden, die innerhalb eines kürzlichen Zeitfensters Nachrichten erhalten haben:

* Verwenden Sie Batch-Zielgruppen mit zeitbasierten Kriterien und referenzieren Sie sie in Journey-Bedingungen.
* Wenden Sie Häufigkeitsbegrenzungs-Geschäftsregeln an, um tägliche oder wöchentliche Nachrichtenbeschränkungen zu erzwingen.


Weitere Informationen zur Verwendung von Audiences:

* Adobe Experience Platform [Segment Builder - Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder - Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)


Siehe auch:

* [Frequenzbegrenzung nach Kanal und Kommunikationstyp](../conflict-prioritization/channel-capping.md)



## Nachrichtenspezifische Ein-/Ausschlüsse

Um Profile in Abhängigkeit davon, ob sie eine bestimmte Nachricht erhalten haben, ein- oder auszuschließen, erstellen Sie Batch-Zielgruppen, die diese Logik einkapseln und in Journey-Bedingungen auf sie verweisen.


Weitere Informationen:

* Adobe Experience Platform [Segment Builder - Ereignisse](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Segment Builder - Zeitbeschränkungen](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Verwenden von Zielgruppen in Bedingungen](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()-Funktion](../building-journeys/functions/functioninaudience.md)

## Personalisierung bei Warenkorbabbruch oder Navigation

So personalisieren Sie die Kommunikation basierend auf dem neuesten Warenkorb oder durchsuchen Ereignisse über mehrere Warenkorbtypen oder Produktansichten hinweg:

* Wenn Sie Zugriff auf [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/de/docs/experience-platform/query/data-distiller/overview){target="_blank"} haben, konfigurieren Sie automatisierte Abfragen, um die erforderlichen Daten aus dem Ereignis zu extrahieren, sie an den Anwendungsfall anzupassen und sie zur Aktivierung zurück in einen profilaktivierten Datensatz zu schreiben.
* Wenn die Verfallsdaten anhand des Profils mit Skalarattributen modelliert werden können, sollten Sie berechnete Attribute verwenden, um die neuesten Informationen zu erfassen und dann auf diese Attribute in der Journey zu verweisen, um die Kommunikation zu erstellen. [Weitere Informationen hierzu finden Sie in der Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/de/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}.


## Verhaltensbasierter Journey-Austritt

Um Profile von Journey zu entfernen, wenn sie ein bestimmtes Verhalten zeigen, verwenden Sie Ausstiegskriterien, um das Profil von der Journey zu beenden, wenn ein bestimmtes Ereignis eingeht oder das Profil für eine bestimmte Zielgruppe geeignet ist.

Weitere Informationen:

* [Festlegen der Journey-Eigenschaften - Beendigungskriterien](journey-properties.md#exit-criteria)

## Kaufbasierte Qualifizierung mit Wertschwellen

Um Journey anhand von Käufen Trigger und zu unterdrücken, wenn der Wert über oder unter einem Schwellenwert liegt, definieren Sie berechnete Attribute, um Käufe über einen bestimmten Zeitraum zu summieren. Erstellen Sie eine Zielgruppe, die Profile enthält, deren Ausgabenbetrag bestimmte Kriterien erfüllt.

Weitere Informationen:

* Adobe Experience Platform [Berechnete Attribute - Übersicht](https://experienceleague.adobe.com/de/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Häufig gestellte Fragen {#faq-ee}

Die Verwendung von Erlebnisereignissen in Journey-Ausdrücken/-Bedingungen wird nicht mehr unterstützt. Die Auswirkungen sind in den folgenden häufig gestellten Fragen aufgeführt:

+++Welche spezifischen Funktionen sind betroffen?

Dies hat nur Auswirkungen auf die Suche nach Erlebnisereignissen im Ausdruckseditor. Die folgenden Funktionen sind davon **nicht** und bleiben unverändert:

* Beobachten der mit einem bestimmten Profil verknüpften Erlebnisereignisse in der Profil-Benutzeroberfläche

* Verwenden von Erlebnisereignissen in berechneten Attributregeln und Zugreifen auf die berechneten Attribute in einer Journey

* Auslösen eines Journey mit einem unitären oder Geschäftsereignis

* Verwenden von Journey-Kontextdaten aus den Ereignissen, die den Trigger der Journey im Ausdruckseditor und im Personalisierungseditor bilden

* Überwachen eines Ereignisses innerhalb eines Journey

* Konfigurieren von Ereignissen zum Trigger einer Journey

* Erkennen von Endbenutzer-Reaktionsereignissen bei Marketing-Nachrichten (z. B. geöffnete E-Mails)

+++

+++Wird meine bestehende Adobe-Organisation von dieser Aktualisierung betroffen sein?

Ihre Adobe-Organisation wäre nur betroffen, wenn Sie die Suche nach Erlebnisereignissen nicht bereits verwendeten. Wenn Sie bereits Erlebnisereignisse in der [Experience Platform-Datenquelle](../datasource/adobe-experience-platform-data-source.md) verwenden, verfügt Ihre Adobe-Organisation weiterhin über Support für die Suche nach Erlebnisereignissen.

+++

+++Ich habe eine neue Adobe-Organisation. Wie kann ich meinen Anwendungsfall lösen, der Erlebnisereignisdaten erfordert?

Oben sind alternative Ansätze und Best Practices für Erlebnisereignisse verfügbar, um die gewünschten Anwendungsfälle zu erzielen.

+++

+++ Was ist, wenn alternative Ansätze für meinen Anwendungsfall nicht funktionieren?

Wenn Ihr Anwendungsfall nicht mit einem der oben aufgeführten alternativen Ansätze gelöst werden kann, wenden Sie sich bitte an Ihren Adobe-Support-Mitarbeiter.

+++
