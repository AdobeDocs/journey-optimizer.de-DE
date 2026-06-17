---
solution: Journey Optimizer
product: journey optimizer
title: KI-gestützte Markenkorrekturen
description: Erfahren Sie, wie Sie KI-gestützte Markenkorrekturen in Adobe Journey Optimizer konfigurieren und verwenden.
feature: Brand Validation
topic: Content Management
role: User
level: Intermediate
exl-id: dd4fde0e-86c8-4a57-86ba-202e3be2c41f
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 1%

---


# KI-gestützte Markenkorrekturen {#brand-corrections}

>[!AVAILABILITY]
>
>Diese Funktion ist für Adobe Journey Optimizer verfügbar und gilt für Push-, SMS- und Web-Inhaltskanäle.

## Überblick {#overview}

Wenn Inhalte während der Brand QA gekennzeichnet werden, kann Adobe Journey Optimizer mithilfe der generativen KI automatisch korrigierte oder verbesserte Textalternativen generieren. Anstatt die gekennzeichnete Kopie manuell neu zu schreiben, erhalten Sie Inline-Vorschläge, die Ihren Markenrichtlinien entsprechen und die Sie mit einem einzigen Klick überprüfen, in der Vorschau anzeigen und anwenden können.

Dadurch wird aus dem QA-Schritt der Marke ein blockierendes Überprüfungsfenster und ein **Fix-as-you-go-Erlebnis**, wodurch der Zeitaufwand für manuelle Korrekturen reduziert und die Inhaltserstellung kanalübergreifend beschleunigt wird.

Diese Funktion wurde für Inhalts-Marketing-Experten, Werbetexter und Kampagnenverantwortliche entwickelt, die die Markenkonformität in Kampagnen mit hohem Volumen und mehreren Kanälen aufrechterhalten müssen, ohne die Produktions-Workflows zu verlangsamen.

## Funktionsweise {#how-it-works}

Brand QA in Adobe Journey Optimizer bewertet Ihre Inhalte anhand der Markenrichtlinien Ihres Unternehmens, einschließlich des Tons, der Terminologie, der Messaging-Standards und der redaktionellen Regeln. Wenn ein Verstoß oder ein Qualitätsproblem erkannt wird, kennzeichnet das System das betroffene Inhaltselement und generiert, sofern unterstützt, automatisch einen empfohlenen Ersatz mit der Adobe Generative AI-Engine.

Der End-to-End-Fluss sieht wie folgt aus:

1. **QA-Prüfung** Marken): Wenn Sie eine Markenprüfung Ihres Inhalts durchführen (Push-Benachrichtigungs-Textkörper, SMS-Nachrichtentext oder Web-Inhaltsbaustein), bewertet das System jedes Element anhand der Regeln für aktive Marken.
2. **Erkennung von Verstößen** - Elemente, die ein oder mehrere Markenkriterien nicht erfüllen, werden mit einem Schweregrad-Indikator gekennzeichnet (z. B. „Kritisch“, „Warnung“ oder „Vorschlag„).
3. **KI-Vorschlagserstellung** - Für jedes gekennzeichnete Element generiert das System automatisch eine oder mehrere korrigierte Textalternativen. Die Vorschläge werden von der generativen KI-Engine von Adobe erstellt, die sowohl den Grund für die Verletzung als auch den Kontext der Richtlinien Ihrer Marke kennt.
4. **Inline-Vorschau** - Der vorgeschlagene Ersetzungstext wird inline direkt neben dem gekennzeichneten Original angezeigt. Sie können die Originalversion und die empfohlenen Versionen nebeneinander vergleichen, bevor Sie Änderungen vornehmen.
5. **Mit einem Klick anwenden** - Wenn der Vorschlag Ihren Anforderungen entspricht, wählen Sie **Anwenden** aus, um den markierten Text durch die KI-generierte Version zu ersetzen. Der Inhaltseditor wird sofort aktualisiert und das Marken-Flag wird gelöscht.
6. **Manuelle Außerkraftsetzung** - Sie sind nie an den KI-Vorschlag gebunden. Sie können den Vorschlag bearbeiten, bevor Sie ihn anwenden, ihn verwerfen und Ihre eigene Korrektur schreiben oder das Flag vollständig ignorieren, wenn der Kontext eine Ausnahme rechtfertigt.

>[!NOTE]
>
>KI-generierte Vorschläge sind nur Empfehlungen. Ihr Team behält die volle redaktionelle Kontrolle. Überprüfen Sie Vorschläge immer im Kontext Ihrer Kampagne, bevor Sie sie anwenden.

## Voraussetzungen {#prerequisites}

Bevor Sie KI-gestützte Markenkorrekturen einsetzen, stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind:

- **Markenrichtlinien konfiguriert** - Für Ihr Unternehmen muss mindestens ein aktives Markenprofil in Adobe Journey Optimizer eingerichtet sein. Markenprofile definieren die Regeln, anhand derer Inhalte bewertet werden. Wenden Sie sich an Ihren Adobe-Administrator oder Brand Manager, um zu überprüfen, ob Markenprofile veröffentlicht und mit Ihren Sandboxes verknüpft werden.
- **Content AI-Funktionen aktiviert** - Für Ihre Organisation und Sandbox muss die KI-gestützte Inhaltsunterstützung aktiviert sein. Dies wird in Adobe Admin Console auf Produktprofilebene verwaltet. Wenn nach einem Brand Scan keine KI-Vorschläge angezeigt werden, sollten Sie sich von Ihrem Administrator vergewissern, dass die Berechtigung zur Generierung von KI-Inhalten aktiv ist.
- **Unterstützter Inhaltstyp** - Markenkorrekturen mit KI-Vorschlägen werden für die folgenden Inhaltstypen unterstützt: Push-Benachrichtigungs-Titel und -Textkörper, SMS-Nachrichtentext und Web-Inhaltsblöcke, die über die Journey Optimizer Web Designer bearbeitet werden. Rich-Media-Assets (Bilder, Videos) werden separat auf Markenkonformität geprüft und sind nicht für KI-Korrekturen auf Textebene verfügbar.
- **Bearbeitungsberechtigungen** - Sie müssen Bearbeitungszugriff auf die Journey, Kampagne oder Inhaltsvorlage haben, in der sich der gekennzeichnete Inhalt befindet.

## Konfigurieren {#configure}

Es ist keine zusätzliche Konfiguration erforderlich, um KI-gestützte Markenkorrekturen zu aktivieren, wenn Ihr Unternehmen bereits Brand QA verwendet. Die KI-Vorschlagsebene wird automatisch aktiviert, wenn Markenverletzungen in unterstützten Inhaltstypen erkannt werden.

So führen Sie eine Markenüberprüfung durch und greifen auf KI-Vorschläge zu:

1. Öffnen Sie eine Kampagne oder Journey in Adobe Journey Optimizer.
2. Navigieren Sie zum Inhaltsschritt für den entsprechenden Kanal (Push, SMS oder Web).
3. Wählen Sie **Markenausrichtung überprüfen** (oder öffnen Sie das Bedienfeld **Markenvalidierung** in der Symbolleiste des Inhaltseditors).
4. Warten Sie, bis die Überprüfung abgeschlossen ist. Markierte Elemente werden auf der Arbeitsfläche hervorgehoben und im Bedienfeld **Markenprobleme** auf der rechten Seite aufgeführt.
5. Erweitern Sie für jedes gekennzeichnete Element die Problemzeile, um den Grund der Verletzung und den KI-generierten Vorschlag anzuzeigen.
6. Verwenden Sie **Vorschau**, um den vorgeschlagenen Text anzuzeigen, der auf der Arbeitsfläche des Inhalts gerendert wird.
7. Wählen Sie **Vorschlag anwenden** aus, um den gekennzeichneten Text zu ersetzen, oder wählen Sie **Bearbeiten** aus, um den Vorschlag vor der Anwendung zu ändern.
8. Nachdem alle Probleme behoben oder quittiert wurden, führen Sie die Markenüberprüfung erneut durch, um die Einhaltung der Vorgaben zu bestätigen.

>[!NOTE]
>
>Durch die Anwendung eines Vorschlags wird der Live-Inhalt im Editor aktualisiert, die Kampagne wird jedoch nicht automatisch veröffentlicht oder aktiviert. Sie müssen die verbleibenden Schritte zur Kampagnenkonfiguration und -aktivierung wie gewohnt ausführen.

### Arbeiten mit mehreren Vorschlägen {#multiple-suggestions}

Bei einigen Verstößen kann die KI-Engine mehr als eine Alternative generieren. In diesen Fällen zeigt das Bedienfeld **Markenprobleme** eine nummerierte Liste von Optionen an. Verwenden Sie die Vorwärts- und Rückwärtspfeile, um durch Alternativen zu navigieren, bevor Sie die Option auswählen, die am besten zu Ihrer Absicht passt. Jede Alternative wird mit einem anderen stilistischen Ansatz generiert - zum Beispiel kann man Prägnanz priorisieren, während eine andere die Tonausrichtung betont.

### Massenkorrekturen {#bulk-corrections}

Wenn mehrere Elemente im selben Inhaltselement gekennzeichnet sind, können Sie Vorschläge einzeln anwenden oder die Aktion **Alle Vorschläge anwenden** oben im Bedienfeld **Markenprobleme** verwenden, um alle KI-generierten Ersetzungen in einem Schritt zu akzeptieren. Überprüfen Sie die Liste sorgfältig, bevor Sie die Massenanwendung verwenden, da diese Aktion alle markierten Texte gleichzeitig ersetzt.

>[!NOTE]
>
>Massenanwendung ist nur verfügbar, wenn allen gekennzeichneten Elementen ein KI-Vorschlag zugeordnet ist. Elemente ohne verfügbare Vorschläge (z. B. Image-Compliance-Flags) werden übersprungen und bleiben für die manuelle Überprüfung markiert.

## Verwandte Themen {#related-topics}

- [Übersicht über Markenrichtlinien](../content-management/brands.md)
- [Ausführen einer Markenüberprüfung für Ihren Inhalt](../content-management/brand-score.md)
- [KI-Assistent für die Inhaltsgenerierung](../content-management/gs-generative.md)
- [Erstellen einer Push-Benachrichtigung](create-push.md)
- [Erstellen einer SMS-Nachricht](../sms/create-sms.md)
- [Bearbeiten von Web-Inhalten mit Journey Optimizer](../web/edit-web-content.md)
