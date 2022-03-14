---
title: Profil aktualisieren
description: Erfahren Sie, wie Sie die Aktivität „Profil aktualisieren“ in einer Journey verwenden.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: ht
source-wordcount: '443'
ht-degree: 100%

---

# Profil aktualisieren {#update-profile}

Mit der Aktionsaktivität **[!UICONTROL Profil aktualisieren]** können Sie ein vorhandenes Adobe Experience Platform-Profil mit Informationen aus dem Ereignis, aus einer Datenquelle oder mit einem bestimmten Wert aktualisieren.

## Wichtige Hinweise

* Die Aktion **Profil aktualisieren** kann nur in Journeys verwendet werden, die mit einem Ereignis beginnen, das über einen Namespace verfügt.
* Die Aktion aktualisiert nur die vorhandenen Felder, sie erstellt keine neuen Profilfelder.
* Sie können die Aktion **Profil aktualisieren** nicht verwenden, um Erlebnisereignisse zu generieren, z. B. einen Kauf.
* Wie bei jeder anderen Aktion können Sie einen alternativen Pfad für den Fall eines Fehlers oder einer Zeitüberschreitung definieren und Sie können nicht zwei Aktionen parallel platzieren.
* Die an Platform gesendete Aktualisierungsanfrage erfolgt schnell, jedoch nicht sofort/innerhalb einer Sekunde. Es dauert normalerweise ein paar Sekunden, manchmal aber auch mehr, ohne dass dies garantiert werden kann. Wenn eine Aktion beispielsweise „Feld 1“ verwendet, das durch eine davor positionierte Profilaktualisierungsaktion aktualisiert wurde, sollte nicht davon ausgegangen werden, dass „Feld 1“ durch die Aktion aktualisiert wird.
* Die Aktivität **Profil aktualisieren** unterstützt keine XDM-Felder, die als Aufzählung definiert sind.

## Verwenden des Testmodus {#using-the-test-mode}

Im Testmodus wird die Aktualisierung des Profils nicht simuliert. Die Aktualisierung wird für das Testprofil durchgeführt.

Nur Testprofile können im Testmodus in eine Journey eintreten. Sie können entweder ein neues Testprofil erstellen oder ein vorhandenes Profil in ein Testprofil umwandeln. In Adobe Experience Platform können Sie Profilattribute über einen CSV-Dateiimport oder API-Aufruf aktualisieren. Eine einfachere Methode besteht darin, die Aktionsaktivität **Profil aktualisieren** zu verwenden und das boolesche Feld „Testprofil“ von „false“ in „true“ zu ändern.

Weitere Informationen dazu, wie Sie ein vorhandenes Profil in ein Testprofil umwandeln, finden Sie in diesem [Abschnitt](../building-journeys/creating-test-profiles.md#create-test-profiles-csv).

## Verwenden der Profilaktualisierung

1. Entwerfen Sie Ihre Journey, indem Sie mit einem Ereignis beginnen. Siehe diesen [Abschnitt](../building-journeys/journey.md).

1. Legen Sie im Abschnitt **Aktion** der Palette die Aktivität **Profil aktualisieren** auf der Arbeitsfläche ab.

   ![](assets/profileupdate0.png)

1. Wählen Sie ein Schema aus der Liste aus.

1. Klicken Sie auf **Feld**, um das Feld auszuwählen, das Sie aktualisieren möchten. Es kann nur ein Feld ausgewählt werden.

   ![](assets/profileupdate2.png)

1. Wählen Sie einen Datensatz aus der Liste aus.

   >[!NOTE]
   >
   >Die Aktion **Profil aktualisieren** aktualisiert die Profildaten in Echtzeit, sie aktualisiert jedoch keine Datensätze. Die Datensatzauswahl ist erforderlich, da das Profil ein Datensatz ist, der mit einem Datensatz verknüpft ist.

1. Klicken Sie auf das Feld **Wert**, um den gewünschten Wert zu definieren:

   * Mit dem einfachen Ausdruckseditor können Sie ein Feld aus einer Datenquelle oder aus dem eingehenden Ereignis auswählen.

      ![](assets/profileupdate4.png)

   * Wenn Sie einen bestimmten Wert definieren oder erweiterte Funktionen nutzen möchten, klicken Sie auf **Erweiterter Modus**.

      ![](assets/profileupdate3.png)

Die Aktivität **Profil aktualisieren** ist jetzt konfiguriert.

![](assets/profileupdate1.png)
