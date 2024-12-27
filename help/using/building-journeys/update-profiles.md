---
solution: Journey Optimizer
product: journey optimizer
title: Profil aktualisieren
description: Erfahren Sie, wie Sie die Aktivität „Profil aktualisieren“ in einer Journey verwenden.
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: Profil, Aktualisieren, Journey, Aktivität
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: dc226803d2df198bde9c525f82431161734f53f8
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 100%

---

# Profil aktualisieren {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Aktivität „Profil aktualisieren“"
>abstract="Mit der Aktionsaktivität „Profil aktualisieren“ können Sie ein vorhandenes Adobe Experience Platform-Profil mit Informationen aus dem Ereignis, aus einer Datenquelle oder mit einem bestimmten Wert aktualisieren."

Mit der Aktionsaktivität **[!UICONTROL Profil aktualisieren]** können Sie ein vorhandenes Adobe Experience Platform-Profil mit Informationen aus einem Ereignis, aus einer Datenquelle oder mit einem bestimmten Wert aktualisieren.

## Schlüsselkonzepte {#key-concepts}

* Die Aktion **Profil aktualisieren** kann nur in Journeys verwendet werden, die über einen Namespace verfügen.
* Die Aktion aktualisiert nur die vorhandenen Felder, sie erstellt keine neuen Profilfelder.
* Sie können die Aktion **Profil aktualisieren** nicht verwenden, um Erlebnisereignisse zu generieren, z. B. einen Kauf.
* Wie bei jeder anderen Aktion können Sie einen alternativen Pfad für den Fall eines Fehlers oder einer Zeitüberschreitung definieren, und Sie können nicht zwei Aktionen parallel platzieren.
* Die an Adobe Experience Platform gesendete Aktualisierungsanfrage erfolgt unmittelbar bzw. innerhalb einer Sekunde. Normalerweise dauert sie ein paar Sekunden, manchmal aber auch länger, ohne dass dies garantiert werden kann. Wenn eine Aktion beispielsweise „Feld 1“ verwendet, das durch die davor positionierte Aktion **Profil aktualisieren** aktualisiert wurde, sollte daher nicht davon ausgegangen werden, dass „Feld 1“ durch die Aktion aktualisiert wird.
* Die Aktivität **Profil aktualisieren** unterstützt keine XDM-Felder, die als Aufzählungen oder Vorschlagswerte definiert sind.
* Die Aktivität **[!UICONTROL Profil aktualisieren]** aktualisiert nur den [Profilspeicher](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=de#profile-data-store){target="_blank"}, nicht den Data Lake.

## Auswahl der Datensätze {#dataset-selection}

Die Aktivität **Profil aktualisieren** erfordert einen eigenen Datensatz, um Aktualisierungen zu speichern. Da diese Aktivität nur den Profilspeicher aktualisiert (nicht Data Lake), sollten alle Aktualisierungen in einem für Profile aktivierten Datensatz gespeichert werden, der speziell für Aktionen vom Typ **Profil aktualisieren** bestimmt ist. Wenn Sie einen Datensatz verwenden, der für die Batch- oder Streaming-Aufnahme verwendet wird, werden die Änderungen, die durch die Aktion **Profil aktualisieren** vorgenommen wurden, durch neu hinzugefügte Daten überschrieben.

Außerdem erfordert die Konfiguration der Aktivität **Profil aktualisieren** keinen Identity-Namespace. Stellen Sie daher sicher, dass der ausgewählte Datensatz denselben **Identity-Namespace** verwendet, den die Journey gestartet hat, da dieser Namespace für diese Aktualisierungen verwendet wird. Die Identitätszuordnung kann auch vom ausgewählten Datensatz verwendet werden. Wenn Sie keinen Datensatz mit dem richtigen Namespace auswählen oder einen, der eine Identitätszuordnung verwendet, schlägt die Aktivität „Profil aktualisieren“ fehl.

## Verwenden der Profilaktualisierung

1. Entwerfen Sie Ihre Journey, indem Sie mit einem Ereignis beginnen. Weitere Informationen finden Sie in diesem [Abschnitt](../building-journeys/journey.md).

1. Legen Sie im Abschnitt **Aktion** der Palette die Aktivität **Profil aktualisieren** auf der Arbeitsfläche ab.

   ![](assets/profileupdate0.png)

1. Wählen Sie ein Schema aus der Liste aus.

1. Klicken Sie auf **Feld**, um das Feld auszuwählen, das Sie aktualisieren möchten. Es kann nur ein Feld ausgewählt werden.

   ![](assets/profileupdate2.png)

1. Wählen Sie einen Datensatz aus der Liste aus.

   >[!NOTE]
   >
   >Die Aktion **Profil aktualisieren** aktualisiert die Profildaten in Echtzeit, sie aktualisiert jedoch keine Datensätze. Die Datensatzauswahl ist erforderlich, da das Profil ein Eintrag ist, der mit einem Datensatz verknüpft ist.

1. Klicken Sie auf das Feld **Wert**, um den gewünschten Wert zu definieren:

   * Mit dem einfachen Ausdruckseditor können Sie ein Feld aus einer Datenquelle oder aus dem eingehenden Ereignis auswählen.

     ![](assets/profileupdate4.png)

   * Wenn Sie einen bestimmten Wert definieren oder erweiterte Funktionen nutzen möchten, klicken Sie auf **Erweiterter Modus**.

     ![](assets/profileupdate3.png)

Die Aktivität **Profil aktualisieren** ist jetzt konfiguriert.

![](assets/profileupdate1.png)


## Verwenden des Testmodus {#using-the-test-mode}

Im Testmodus wird die Aktualisierung des Profils nicht simuliert. Die Aktualisierung wird für das Testprofil durchgeführt.

Nur Testprofile können im Testmodus in eine Journey eintreten. Sie können entweder ein neues Testprofil erstellen oder ein vorhandenes Profil in ein Testprofil umwandeln. In Adobe Experience Platform können Sie Profilattribute über einen CSV-Dateiimport oder API-Aufruf aktualisieren. Eine einfachere Methode besteht darin, die Aktionsaktivität **Profil aktualisieren** zu verwenden und das boolesche Feld „Testprofil“ von „false“ in „true“ zu ändern.

Weitere Informationen dazu, wie Sie ein vorhandenes Profil in ein Testprofil umwandeln, finden Sie in diesem [Abschnitt](../audience/creating-test-profiles.md#create-test-profiles-csv).
