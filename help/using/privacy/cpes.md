---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Opt-out
description: Erfahren Sie, wie Sie Opt-out- und Datenschutzeinstellungen verwalten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 97%

---

# Implementieren der Zustimmung zum Opt-out von der Personalisierung {#cpes-opt-out}


## Ausdruckseditor

Ausdrucks-Editor beim Personalisieren von Bildern, Text und Betreffzeile (Segment in Kampagnen) – Benutzeroberfläche und Headless

Der Personalisierungseditor selbst führt keine Einverständnisüberprüfung oder -durchsetzung durch, da er nicht am Versand von Nachrichtenaktionen beteiligt ist. Der Personalisierungs-Editor hält sich an berechtigungsbasierte Zugriffssteuerungsbezeichnungen, die vom einheitlichen Profildienst bereitgestellt werden, um die Verwendung verschiedener Felder für die Personalisierung zu ermöglichen bzw. zu verbieten. Der Vorschau- und Render-Dienst für Nachrichten maskiert identifizierte Felder mit sensiblen Informationen.

In AJO-Kampagnen kann die Durchsetzung der Zustimmungsrichtlinie an zwei Orten erfolgen. Kundinnen und Kunden können Definitionen von Zustimmungsrichtlinien als Teil der Zielgruppen- oder Segmenterstellung einbeziehen, um sicherzustellen, dass die für die Kampagne ausgewählte Zielgruppe bereits Profile herausgefiltert hat, die nicht den Zustimmungskriterien entsprechen. Zweitens führt der Nachricht-Runtime-Dienst eine allgemeine Einverständnisprüfung auf Kanalebene durch, um sicherzustellen, dass sich Profile per Opt-in auch wirklich dafür entschieden haben, Marketing-Kommunikationen über den spezifischen Kanal zu erhalten. Das AJO-Kampagnenobjekt selbst führt derzeit keine zusätzlichen Prüfungen zur Durchsetzung der Einverständnisrichtlinien durch.

AJO-Kampagnen- und Personalisierungsschritte zur manuellen Durchsetzung der Einverständnisses:

Der Opt-in-Status und die Personalisierungsvoreinstellungen einer Benutzerin bzw. eines Benutzers sollten vor der Aktivierung in einer Journey Optimizer-Kampagne Teil der Zielgruppenregeln und -definitionen sein. Personen, die Adobe Experience Platform zum Marketing nutzen, können ihrer Zielgruppe eine Einverständnisprüfung hinzufügen, indem eine neue Zielgruppenzusammensetzung erstellt oder mithilfe des Regel-Builders ein neues Segment definiert wird.

Bei Verwendung von Audience Composer können Sie Ihre Zielgruppe mithilfe von Profilattributen aufteilen. Nachdem Sie die gewünschten Einverständnisattribute ausgewählt haben, können Sie die resultierenden Zielgruppen zur Aktivierung in einer Kampagne speichern. Beachten Sie, dass bei der Erstellung einer Zielgruppe, die kein Einverständnis für Personalisierung erteilt hat, und der anschließenden Auswahl dieser Zielgruppe zur Aktivierung in einer Kampagne weiterhin Personalisierungs-Tools verfügbar sind. Die Marketing-Fachkraft trägt selbst die Verantwortung, keine Personalisierungs-Tools zu verwenden, wenn mit einer Zielgruppe gearbeitet wird, für die keine Personalisierung durchgeführt werden soll.

Gehen Sie wie folgt vor, um in der Zielgruppenkomposition eine aufgeteilte Zielgruppe zu erstellen:

1. Wählen Sie Ihre Start-Zielgruppe aus.

1. Klicken Sie auf das Pluszeichen, um eine aufgeteilte Zielgruppe zu erstellen.

1. Wählen Sie in den Aufteilungseigenschaften als Typ „Attributaufteilung“ aus.

1. Klicken Sie im Attributfeld auf das Stiftsymbol, um das Attributauswahlfenster aufzurufen.

1. Geben Sie in den Auswahlwert ein, um nach dem Einverständnisattribut für die Personalisierung zu suchen (beachten Sie, dass es sich um das Pfadattribut „profile.consents.personalize.content.val“ handelt).

1. Wählen Sie dieses Attribut aus.

1. Wählen Sie unter Pfad 1 einen Titel, der Ihnen bei der Definition der nicht personalisierten Zielgruppe hilft.

1. Wählen Sie den entsprechenden Wert aus dieser Liste aus: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values

   In diesem Fall verwenden wir ein „n“, um NEIN entsprechend dem Opt-out von der Personalisierung anzugeben

   Sie können einen separaten Pfad für andere Auswahlwerte erstellen oder verbleibende Pfade löschen und „andere Profile“ aktivieren, wodurch alle anderen Profile ohne den Auswahlwert „n“ eingeschlossen werden.

1. Klicken Sie abschließend in das Feld, in dem „Zielgruppe speichern“ steht. Daraufhin wird ein neues Eigenschaftenfenster geöffnet, in dem Sie auswählen können, welchen Namen Sie für die abgeleiteten Zielgruppen verwenden möchten.

1. Veröffentlichen Sie nach Abschluss die Zielgruppenkomposition.

Wenn Sie den Segment-Regel-Builder zum Erstellen Ihrer Zielgruppe verwenden, können Sie in der Zielgruppendefinition Auswahlwerte für Personalisierung und Einverständnis als Ausschlussparameter auswählen. Durch das Hinzufügen der Ausschlussparameter können Sie ein einzelnes Zielgruppensegment von Profilen erstellen, in denen die Personen, die ihr Einverständnis nicht erteilt haben, herausgefiltert werden.
