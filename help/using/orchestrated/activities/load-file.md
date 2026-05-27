---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Datei laden“
description: Erfahren Sie, wie Sie mit der Aktivität „Datei laden“ eine orchestrierte Kampagnenzielgruppe aus einer CSV- oder TXT-Datei ansprechen können, ohne die Datei in Adobe Experience Platform aufzunehmen
hide: true
exl-id: a7c3e891-4f2d-4b8e-9c1a-6e8f0d3b2a41
version: Campaign Orchestration
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: abac7d8c49e2dc7af9fde91b0e8305ce10a406ce
workflow-type: tm+mt
source-wordcount: 1511
ht-degree: 2%

---

# Datei laden {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_load_file"
>title="Aktivität „Datei laden“"
>abstract="Die Aktivität **Datei laden** ist eine Aktivität **Daten-Management** . Verwenden Sie diese Option, um mit Profilen und Daten zu arbeiten, die in einer externen Datei auf der orchestrierten Kampagnen-Arbeitsfläche gespeichert sind, und um die Kampagnen-Audience zu definieren. Dateidaten werden zur Ausführungszeit genutzt und nicht als Adobe Experience Platform-Datensatz beibehalten. Zeilen werden mithilfe einer Identitätsspalte und einer Zielgruppendimension mit vorhandenen Empfängern abgeglichen. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten."

Die Aktivität **[!UICONTROL Datei laden]** ist eine Aktivität **[!UICONTROL Daten-Management]** . Verwenden Sie diese Option, um mit Profilen und Daten zu arbeiten, die in einer externen Datei gespeichert sind. Es unterstützt **dateibasiertes Targeting** in orchestrierten Kampagnen, wenn Ihre Empfängerliste von einem externen System stammt (z. B. einem CRM-Export oder einer Partnerdatei) und Sie eine Kampagne ausführen möchten, ohne zuvor eine vollständige Adobe Experience Platform-Aufnahme-Pipeline zu erstellen.

>[!AVAILABILITY]
>
>Die **Datei laden**-Aktivität ist für **Reihe von** in „Eingeschränkte Verfügbarkeit“ verfügbar. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um Zugriff anzufordern. Informationen zu Verfügbarkeitsphasen finden Sie unter [Journey Optimizer-Versionszyklus](../../rn/releases.md).
>
>Die Aktivität ist derzeit nicht für die Verwendung mit **Healthcare Shield** oder **Privacy and Security Shield** verfügbar.

## Leitlinien und Einschränkungen {#limitations}

Die folgenden Einschränkungen gelten für die Aktivität Datei laden :

* Sie können bis zu 50 MB pro Datei hochladen.
* Es werden nur CSV- und TXT-Dateien mit flachen Strukturen unterstützt.
* Hochgeladene Daten werden bei der Kampagnenausführung verwendet und nicht als Adobe Experience Platform-Datensatz gespeichert.
* Jede Zeile muss mit einem vorhandenen Empfänger für die ausgewählte Zielgruppendimension übereinstimmen. Die Aktivität „Datei laden“ erstellt keine neuen Profile aus der Datei.

Einschränkungen für Kanal- und Arbeitsflächen-Aktivitäten finden Sie unter [Leitplanken und Einschränkungen](../guardrails.md#activities-limitations).

## Voraussetzungen {#prerequisites}

Vor der Konfiguration einer Aktivität **[!UICONTROL Datei laden]**:

1. Erstellen Sie die **[!UICONTROL Zielgruppendimension]** die Sie für die Abstimmung benötigen (z. B. Empfänger). [Erfahren Sie, wie Sie eine Zielgruppendimension erstellen](../target-dimension.md)

1. Stellen Sie sicher, dass die Identitätswerte in Ihrer Datei mit den vorhandenen Datensätzen für diese Dimension übereinstimmen. Zeilen aus der hochgeladenen Datei werden mit vorhandenen Empfängern abgestimmt. Die Aktivität erstellt keine neuen Profile aus der Datei.

## Konfigurieren der Aktivität „Datei laden“ {#load-file-configuration}

Konfigurieren Sie die Aktivität in zwei Teilen: Definieren Sie die erwartete Dateistruktur mit einer Beispieldatei und geben Sie dann die Datei an, die bei der Kampagnenausführung geladen werden soll, und wie die Zeilen mit Ihrer Zielgruppendimension abgestimmt werden.

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Datei laden]** zu konfigurieren:

1. Fügen Sie **[!UICONTROL orchestrierten Kampagnen]** Arbeitsfläche die Aktivität „Datei laden“ hinzu.

   ![](../assets/load-file.png)

1. Geben Sie einen **[!UICONTROL Titel]** für die Aktivität ein.

1. Wählen Sie im **[!UICONTROL Beispieldatei]** die lokale Datei aus, die die erwartete Struktur definiert.

   >[!NOTE]
   >
   > Die Beispieldatei wird nur zum Konfigurieren von Spalten und zur Formatierung verwendet. Die Daten werden nicht als Kampagnentität importiert. Das Format muss mit den Dateien übereinstimmen, die bei der Ausführung der Kampagne geladen werden.

1. Geben **[!UICONTROL in der Dropdown]** Liste Dateityp an, ob die Datei **Spalten mit Trennzeichen** oder **Spalten mit fester Breite** verwendet.

   ![](../assets/load-file-sample.png)

1. Erweitern Sie im Abschnitt **[!UICONTROL Spalten]** jede Spalte und konfigurieren Sie deren Eigenschaften.

   ![](../assets/load-file-sample-columns.png)

   Die folgenden Eigenschaften sind für jede Spalte verfügbar. Nachdem Sie einen **[!UICONTROL Datentyp]** ausgewählt haben, werden zusätzliche Optionen für diesen Typ angezeigt. Erweitern Sie die folgenden Abschnitte, um die vollständige Liste pro Datentyp anzuzeigen.

   * **[!UICONTROL Spalte ignorieren]** - Schließt die Spalte aus dem Import aus, wenn ausgewählt.
   * **[!UICONTROL label]** - Anzeigename für die Spalte (z. B. `email`).
   * **[!UICONTROL Interner Name]** - Systemname für die Spalte, abgeleitet aus der Dateikopfzeile (schreibgeschützt).
   * **[!UICONTROL Datentyp]** - Datentyp in der Spalte.
   * **[!UICONTROL NULL zulassen]** - Gibt an, wie leere Werte in der Spalte verwaltet werden:

      * **[!UICONTROL Adobe Campaign-Standard]** - Generiert einen Fehler nur für numerische Felder. Fügt andernfalls einen NULL-Wert ein.
      * **[!UICONTROL Leerer Wert zulässig]** - Autorisiert leere Werte. Der Wert NULL wird eingefügt.
      * **[!UICONTROL Immer befüllt]** - Generiert einen Fehler, wenn ein Wert leer ist.

   * **[!UICONTROL Fehlerverarbeitung]** - Definiert das Verhalten, wenn ein Fehler in der Spalte auftritt:

      * **[!UICONTROL Wert ignorieren]** - Der Wert wird ignoriert.
      * **[!UICONTROL Zeile ablehnen]** - Die gesamte Zeile wird nicht verarbeitet.
      * **[!UICONTROL Standardwert im Fehlerfall verwenden]** - Ersetzt den Wert, der den Fehler verursacht, durch einen Standardwert, der im Feld **[!UICONTROL Standardwert]** definiert ist.
      * **[!UICONTROL Standardwert verwenden, falls der Wert nicht neu zugeordnet wurde]** - Ersetzt den den Fehler verursachenden Wert durch einen Standardwert, der im Feld **[!UICONTROL Standardwert“]** ist, es sei denn, für den fehlerhaften Wert wurde eine Zuordnung definiert.
      * **[!UICONTROL Zeile ablehnen, wenn kein Neuzuordnungswert vorhanden ist]** - Die gesamte Zeile wird nicht verarbeitet, es sei denn, für den fehlerhaften Wert wurde eine Zuordnung definiert.

   * **[!UICONTROL Standardwert]** - Standardwert, der verwendet wird, wenn **[!UICONTROL Fehlerverarbeitung]** auf die Verwendung eines Standardwerts eingestellt ist.
   * **[!UICONTROL Wert-Neuzuordnung]** - Ordnen Sie bestimmte Werte neuen Werten zu. Klicken Sie **[!UICONTROL Zuordnung hinzufügen]**, um jede Zuordnung zu definieren (ersetzen Sie beispielsweise `True`/`False` durch `1`/`0`).

   +++Parameter der Zeichenfolgenspalten

   * **[!UICONTROL Breite]** - Maximale Zeichenanzahl.
   * **[!UICONTROL Datenumwandlung]** — Auf Zeichenfolgenwerte angewendete Groß-/Kleinschreibung (z. B. keine oder Groß-/Kleinschreibung).
   * **[!UICONTROL Leerraum-Management]** - Umgang mit führenden oder nachfolgenden Leerzeichen in Zeichenfolgenwerten.

   +++

   +++Parameter für Spalten mit Ganzzahlen und unverankerten Zahlen

   * **[!UICONTROL Format]** - Definiert, wie numerische Werte in der Datei gelesen werden:

      * **[!UICONTROL Sonstige]** - Definieren Sie **[!UICONTROL Tausendertrennzeichen]** und **[!UICONTROL Dezimaltrennzeichen]** im Abschnitt **[!UICONTROL Trennzeichen]**.
      * **[!UICONTROL 1.000.00]** - Komma als Tausendertrennzeichen und Punkt als Dezimaltrennzeichen.
      * **[!UICONTROL 1 000,00]** — Leerzeichen als Tausendertrennzeichen und Komma als Dezimaltrennzeichen.

   * **[!UICONTROL Trennzeichen]** (wenn **[!UICONTROL format]** den Wert **[!UICONTROL Other]** hat):

      * **[!UICONTROL Tausendertrennzeichen]** - Zeichen, das Tausende in numerischen Werten gruppiert (leer lassen, wenn es nicht verwendet wird).
      * **[!UICONTROL Dezimaltrennzeichen]** - Zeichen, das für den Dezimalteil numerischer Werte verwendet wird (z. B. `,` oder `.`).

   +++

   +++Parameter für Datumsspalten

   * **[!UICONTROL Datumsformat]** - Muster, das dem Aussehen von Datumsangaben in der Datei entspricht (z. B. `yyyy/mm/dd`).
   * **[!UICONTROL Trennzeichen]**:

      * **[!UICONTROL Jahr, Monat,]**: Zeichen zwischen den Komponenten für Jahr, Monat und Tag (z. B. `/`).

   +++

   +++Zeitspaltenparameter

   * **[!UICONTROL Zeitformat]** - Muster, das dem Aussehen der Zeiten in der Datei entspricht (z. B. `13:30` für 24-Stunden-Stunden und -Minuten).
   * **[!UICONTROL Trennzeichen]**:

      * **[!UICONTROL Stunde, Minute, Sekunde]** - Zeichen zwischen der Stunde, Minute und der zweiten Komponente (z. B. `:`).

   +++

   +++Parameter für Datums- und Uhrzeitspalten

   * **[!UICONTROL Datumsformat]** - Das Muster, das dem Aussehen des Datumsbereichs in der Datei entspricht.
   * **[!UICONTROL Zeitformat]** - Muster, das dem Aussehen des Zeitabschnitts in der Datei entspricht.
   * **[!UICONTROL Trennzeichen]** - Zeichen zwischen Datums- und Uhrzeitkomponenten, wie in der Benutzeroberfläche für Ihre Spalte dargestellt.

   +++

1. Geben **[!UICONTROL im Abschnitt]** an, wie die Datei strukturiert ist, damit Zeilen und Spalten bei der Kampagnenausführung korrekt gelesen werden. Die Zieldatei muss dieselbe Formatierung wie die Beispieldatei verwenden.

   ![](../assets/load-file-sample-formatting.png)

   * **[!UICONTROL Erste Zeile als Spaltenüberschrift verwenden]** - Wenn diese Option aktiviert ist, wird die erste Zeile der Datei als Spaltenname behandelt. Diese Option ist normalerweise aktiviert, wenn Sie das Beispiel aus einer Datei konfigurieren, die eine Kopfzeile enthält.
   * **[!UICONTROL Zeilennummer als Kennung verwenden]** - Wenn diese Option aktiviert ist, wird jede Zeile durch ihre Zeilennummer in der Datei identifiziert.
   * **[!UICONTROL Datensätze erstrecken sich über mehrere Zeilen]** - Wenn diese Option aktiviert ist, kann ein einzelner Datensatz mehrere Zeilen in der Datei umfassen (z. B. wenn Felder Zeilenumbrüche enthalten).
   * **[!UICONTROL Zu ignorierende Zeilen]** - Anzahl der Zeilen, die am Anfang der Datei übersprungen werden sollen, bevor Daten gelesen werden (z. B. Kommentar- oder Metadatenzeilen).
   * **[!UICONTROL Zeitzone]** - Zeitzone, die beim Importieren von Datums- und Zeitwerten angewendet wird.
   * **[!UICONTROL Codierung]** - Zeichencodierung der Datei. Wählen Sie die Kodierung aus, die Ihrer Quelldatei entspricht.
   * **[!UICONTROL Zeichenfolgen-Trennzeichen]** - Zum Einschließen von Zeichenfolgenwerten in die Datei verwendetes Zeichen.
   * **[!UICONTROL Spaltentrennzeichen]** - Zeichen, das Spalten in einer durch Trennzeichen getrennten Datei trennt.

1. Im Abschnitt **[!UICONTROL Target-Datei]** wählen Sie aus, wie die Datei bereitgestellt wird - z. B. **[!UICONTROL Datei vom lokalen Computer hochladen]** um sie in dieser Version manuell hochzuladen.

1. Wählen Sie die hochzuladende CSV- oder TXT-Datei aus.

   >[!CAUTION]
   >
   > Stellen Sie sicher, dass die Zieldatei demselben Format, derselben Spaltenstruktur und derselben Spaltenanzahl folgt wie die Beispieldatei. Abweichungen können bei der Ausführung zu Fehlern führen.

1. Wählen Sie die Identitätsspalte in der Datei aus - das Feld, das verwendet wird, um jede Zeile mit einem vorhandenen Empfänger abzugleichen (z. B. E-Mail-Adresse oder Kunden-ID).

1. Wählen Sie die **[!UICONTROL Zielgruppendimension]** für die Abstimmung aus.

1. Wenn die Konfiguration abgeschlossen ist, sollten Sie ein Beispiel für zugeordnete Zeilen in der Vorschau anzeigen, falls die Benutzeroberfläche dies anbietet, und dann bestätigen.

1. Definieren Sie **[!UICONTROL Abschnitt]** Zurückweisungsverwaltung“, wie sich die Aktivität verhält, wenn bei der Dateiverarbeitung Fehler auftreten:

   * **[!UICONTROL Anzahl der zulässigen Fehler]** — Maximal zulässige Anzahl von Fehlern, bevor die Aktivität fehlschlägt.
   * **[!UICONTROL Zurückweisungen in einer Datei beibehalten]** - Wenn diese Option aktiviert ist, werden Zeilen, die nicht geladen werden konnten, nach der Ausführung zur Überprüfung in eine Zurückweisungsdatei auf dem Server geschrieben.

1. Verbindet die ausgehende Transition mit nachgelagerten Aktivitäten.

Zeilen, die nicht mit einem vorhandenen Empfänger abgestimmt werden können, werden aus der Zielgruppe ausgeschlossen. Ausgeschlossene Zeilen werden im Ausführungsprotokoll der Kampagne aufgezeichnet. Die Kampagne schlägt nicht allein deshalb fehl, weil einige Zeilen nicht übereingestimmt haben.

## Verwenden der Audience-Datei in Sendungen {#downstream}

Nachdem **[!UICONTROL Datei laden]** die Zielgruppe aufgelöst hat, können Sie standardmäßige orchestrierte Kampagnenaktivitäten verwenden:

* **[Kanalaktivitäten](channels.md)** - E-Mail, SMS, Push-Benachrichtigung oder Briefpost.

* **[Anreicherung](enrichment.md)** oder **[Abstimmung](reconciliation.md)** - Arbeitstabellendaten bei Bedarf weiter verfeinern oder verknüpfen.

[Informationen zum Orchestrieren von Kampagnenaktivitäten](../orchestrate-activities.md)

## Ausführung und Reporting {#execution}

Wenn die Kampagne ausgeführt wird:

* Die Datei wird zur **Ausführungszeit** verarbeitet.

* Akzeptierte Zeilen aus der Zielgruppe, die an nachgelagerte Aktivitäten übergeben werden.

* Zurückgewiesene oder nicht abgestimmte Zeilen werden ausgeschlossen; Zählungen und Gründe erscheinen im **Ausführungsprotokoll** (z. B. Gesamtanzahl der geladenen Zeilen, akzeptierte Zeilen, zurückgewiesene Zeilen).

Die Zielgruppenauflösung wird innerhalb von etwa **60 Sekunden** einer **100.000 Zeilen umfassenden** CSV unter der standardmäßigen orchestrierten Kampagneninfrastruktur abgeschlossen.

## Verwandte Inhalte {#related}

* [Erstellen einer Zielgruppendimension](../target-dimension.md)
* [Aktivität „Zielgruppe erstellen“](build-audience.md)
* [Aktivität des Typs „Zielgruppe lesen“](read-audience.md)
* [Aktivität „Abstimmung“](reconciliation.md)
* [Leitlinien und Einschränkungen](../guardrails.md)
