---
solution: Journey Optimizer
product: journey optimizer
title: Verwalten von Opt-out
description: Erfahren Sie, wie Sie Opt-out- und Datenschutzeinstellungen verwalten können
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f5390bbb3bab435b21ace4d1842de0048132bc8c
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 1%

---

# Implementieren der Zustimmung zum Opt-out für die Personalisierung {#cpes-opt-out}


## Ausdruckseditor

Ausdruckseditor beim Personalisieren von Bildern, Text und Betreffzeile ( Segment in Kampagnen) - Benutzeroberfläche und Headless

Der Personalisierungseditor selbst führt keine Einwilligungsüberprüfungen oder Durchsetzungsmaßnahmen durch, da er nicht an der Bereitstellung von Nachrichtenaktionen beteiligt ist. Der Personalisierungs-Editor hält sich an berechtigungsbasierte Zugriffssteuerungsbezeichnungen, die vom einheitlichen Profildienst bereitgestellt werden, um die Verwendung verschiedener Felder für die Personalisierung zu ermöglichen/zu verbieten. Der Nachrichtenvorschau- und Renderdienst maskiert identifizierte Felder mit sensiblen Informationen.

In AJO-Kampagnen kann die Durchsetzung der Zustimmungsrichtlinie an zwei Orten erfolgen. Kunden können Definitionen von Zustimmungsrichtlinien als Teil der Zielgruppe oder Segmenterstellung einbeziehen, um sicherzustellen, dass die für die Kampagne ausgewählte Zielgruppe bereits Profile herausgefiltert hat, die nicht den Zustimmungskriterien entsprechen. Zweitens führt der Message-Runtime-Dienst eine allgemeine Zustimmungsprüfung auf Kanalebene durch, um sicherzustellen, dass sich Profile für den Empfang von Marketing-Nachrichten über den jeweiligen Kanal angemeldet haben. Das AJO Campaign-Objekt selbst führt derzeit keine zusätzlichen Prüfungen zur Durchsetzung von Zustimmungsrichtlinien durch.

Schritte für AJO Campaign und Personalisierung zum manuellen Erzwingen der Zustimmung:

Der Opt-in-Status und die Personalisierungseinstellungen eines Benutzers sollten vor der Aktivierung in einer Journey Optimizer-Kampagne Teil der Zielgruppenregeln und -definitionen sein. Ein Marketing-Benutzer in Adobe Experience Platform kann seiner Zielgruppe eine Einverständnisprüfung hinzufügen, indem er eine neue Zielgruppenzusammensetzung erstellt oder mithilfe von Rule Builder ein neues Segment definiert.

Bei Verwendung von Audience Composer können Sie Ihre Zielgruppe mithilfe von Profilattributen aufteilen. Nachdem Sie die gewünschten Zustimmungsattribute ausgewählt haben, können Sie die resultierenden Zielgruppen zur Aktivierung in einer Kampagne speichern. Beachten Sie, dass bei der Erstellung einer Audience, die nicht die Zustimmung zur Personalisierung erteilt hat, und der anschließenden Auswahl dieser Audience zur Aktivierung in einer Kampagne weiterhin Personalisierungs-Tools verfügbar sind. Es liegt im Ermessen des Marketing-Benutzers zu verstehen, dass er keine Personalisierungs-Tools verwenden sollte, wenn er mit einer Zielgruppe arbeitet, die keine Personalisierung erhält.

Gehen Sie wie folgt vor, um eine aufgeteilte Zielgruppe in der Zielgruppenzusammensetzung zu erstellen:

1. Wählen Sie Ihre Startzielgruppe aus.

1. Klicken Sie auf das Pluszeichen, um eine aufgespaltete Zielgruppe zu erstellen.

1. Wählen Sie in den Aufspaltungseigenschaften als Typ &quot;Attributaufteilung&quot;.

1. Klicken Sie im Attributfeld auf das Stiftsymbol, um das Attributauswahlfenster aufzurufen.

1. Geben Sie in den Auswahlwert ein, um nach dem Personalisierungszustimmungsattribut zu suchen (beachten Sie, dass dies das Attribut path profile.consents.personalize.content.val sein wird).

1. Wählen Sie dieses Attribut aus.

1. Wählen Sie unter Pfad 1 einen Titel, der Ihnen bei der Definition der nicht personalisierten Zielgruppe hilft.

1. Wählen Sie den entsprechenden Wert aus dieser Liste aus: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=en#choice-values

   In diesem Fall verwenden wir ein &quot;n&quot;, um NEIN als Opt-out für die Personalisierung anzugeben

   Sie können einen separaten Pfad für andere Auswahlwerte erstellen oder verbleibende Pfade löschen und &quot;andere Profile&quot;aktivieren, die alle anderen Profile ohne Auswahlwert &quot;n&quot;enthalten würden.

1. Klicken Sie abschließend in das Feld, in dem &quot;Zielgruppe speichern&quot;steht. Daraufhin wird ein neues Eigenschaftenfenster geöffnet, in dem Sie auswählen können, welchen Namen Sie für die abgeleiteten Zielgruppen verwenden möchten.

1. Veröffentlichen Sie nach Abschluss die Komposition der Zielgruppe.

Wenn Sie den Segment Rule Builder zum Erstellen Ihrer Zielgruppe verwenden, können Sie in der Zielgruppendefinition Personalisierungs- und Zustimmungswertentscheidungen als Ausschlussparameter auswählen. Durch das Hinzufügen der Ausschlussparameter können Sie ein einzelnes Zielgruppensegment von Profilen erstellen, in denen Personen, die ihre Einwilligung nicht erteilt haben, herausgefiltert werden.

