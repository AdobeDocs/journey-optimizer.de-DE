---
title: Profil aktualisieren
description: Erfahren Sie, wie Sie die Aktivität Update Profil in einer Journey verwenden
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Profil {#update-profile} aktualisieren

![](../assets/do-not-localize/badge.png)

Mit der Aktivität **[!UICONTROL Profil aktualisieren]** können Sie ein vorhandenes Adobe Experience Platform-Profil mit Informationen aktualisieren, die aus dem Ereignis, einer Datenquelle oder einem bestimmten Wert stammen.

## Wichtige Hinweise

* Die Aktion **Profil aktualisieren** kann nur in Journey verwendet werden, beginnend mit einem Ereignis mit einem Namensraum.
* Die Aktion aktualisiert nur die vorhandenen Felder, sie erstellt keine neuen Profil-Felder.
* Sie können die Aktion **Profil aktualisieren** nicht verwenden, um Erlebnis-Ereignis zu generieren, z. B. einen Kauf.
* Wie bei jeder anderen Aktion können Sie auch im Fehlerfall oder bei Zeitüberschreitung einen alternativen Pfad definieren und zwei Aktionen nicht parallel platzieren.
* Die an die Plattform gesendete Aktualisierungsanforderung erfolgt schnell, jedoch nicht sofort/innerhalb einer Sekunde. Es dauert normalerweise ein paar Sekunden, manchmal aber auch mehr ohne Garantie. Wenn eine Aktion beispielsweise &quot;field 1&quot;verwendet, die durch eine zuvor positionierte Aktualisierungsaktion aktualisiert wurde, sollten Sie nicht erwarten, dass &quot;field 1&quot;in der Profil-Aktion aktualisiert wird.
* Datenquellen haben eine Vorstellung von der Cachedauer auf Feldebene. Wenn Sie erwarten, dass Sie in einer Journey ein kürzlich aktualisiertes Profil-Feld nutzen, sollten Sie eine sehr kurze Cache-Dauer definieren.

## Verwenden des Testmodus {#using-the-test-mode}

Im Testmodus wird die Aktualisierung des Profils nicht simuliert. Die Aktualisierung wird am Test-Profil durchgeführt.

Nur Profil können im Testmodus in eine Journey wechseln. Sie können entweder ein neues Profil erstellen oder ein vorhandenes Profil in ein Test-Profil umwandeln. In Adobe Experience Platform können Sie Attribute von Profilen über einen CSV-Dateiimport- oder API-Aufruf aktualisieren. Eine einfachere Methode besteht darin, eine Aktivität für die Aktion **Profil aktualisieren** zu verwenden und das boolesche Testfeld des Profils von &quot;false&quot;in &quot;true&quot;zu ändern.

Weitere Informationen dazu, wie Sie ein vorhandenes Profil in ein Test-Profil umwandeln, finden Sie in diesem [Abschnitt](../building-journeys/creating-test-profiles.md#create-test-profiles-csv).

## Profil-Update verwenden

1. Entwerfen Sie Ihre Journey, indem Sie mit einem Ereignis beginnen. Siehe [Abschnitt](../building-journeys/journey.md).

1. Legen Sie im Bereich **Aktion** der Palette die Aktivität **Profil** aktualisieren auf der Arbeitsfläche ab.

   ![](../assets/profileupdate0.png)

1. Wählen Sie ein Schema aus der Liste.

1. Klicken Sie auf **Felder**, um das Feld auszuwählen, das Sie aktualisieren möchten. Es kann nur ein Feld ausgewählt werden.

   ![](../assets/profileupdate2.png)

1. Wählen Sie einen Datensatz aus der Liste aus. Die Datensatzauswahl bestimmt, wo der neue Profil gespeichert wird.

1. Klicken Sie auf das Feld **Wert**, um den gewünschten Wert zu definieren:

   * Mit dem einfachen Ausdruck-Editor können Sie ein Feld aus einer Datenquelle oder aus dem eingehenden Ereignis auswählen.

      ![](../assets/profileupdate4.png)

   * Wenn Sie einen bestimmten Wert definieren oder erweiterte Funktionen nutzen möchten, klicken Sie auf **Erweiterter Modus**.

      ![](../assets/profileupdate3.png)

Das Profil **Aktualisieren** ist jetzt konfiguriert.

![](../assets/profileupdate1.png)
