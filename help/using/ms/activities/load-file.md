---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Datei laden“
description: Erfahren Sie, wie Sie die Aktivität „Datei laden“ in einer mehrstufigen Kampagne verwenden
hide: true
hidefromtoc: true
exl-id: ae0dc980-2361-4c3b-a68e-ae0bb5dc0a26
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 88%

---

# Datei laden  {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile"
>title="Aktivität „Datei laden“"
>abstract="Die Aktivität **Datei laden** ist eine **Daten-Management**-Aktivität. Durch diese Aktivität kann mit Daten gearbeitet werden, die in einer externen Datei gespeichert sind. Es werden keine Profile und Daten zur Datenbank hinzugefügt, aber alle Felder in der Eingabedatei sind zur Personalisierung oder zur Aktualisierung von Profilen oder anderen Tabellen verfügbar. "

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition"
>title="Ausgehende Transition von der Zurückweisungsverwaltung"
>abstract="Ausgehende Transition von der Zurückweisungsverwaltung"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_outboundtransition_reject"
>title="Ausgehende Transition für Zurückweisungen der Zurückweisungsverwaltung"
>abstract="Ausgehende Transition für Zurückweisungen der Zurückweisungsverwaltung"


Die Aktivität **Datei laden** ist eine **Daten-Management**-Aktivität. Mit dieser Aktivität können Sie mit Profilen und Daten arbeiten, die in einer externen Datei gespeichert sind. Es werden keine Profile und Daten zur Datenbank hinzugefügt, aber alle Felder in der Eingabedatei sind zur Personalisierung oder zur Aktualisierung von Profilen oder anderen Tabellen verfügbar.

>[!NOTE]
>Unterstützte Dateiformate sind: Text (TXT) und kommagetrennte Werte (CSV). Sie können Dateien mit einer maximalen Größe von 50 MB laden.

Diese Aktivität kann mit einer [Abstimmungs](reconciliation.md)-Aktivität verwendet werden, um nicht identifizierte Daten mit vorhandenen Ressourcen zu verknüpfen. Zum Beispiel kann die Aktivität **Datei laden** vor dem Import nicht standardmäßiger Daten in die Datenbank vor einer **Abstimmungs**-Aktivität platziert werden.

## Konfigurieren der Aktivität „Datei laden“ {#load-configuration}

Die Konfiguration der Aktivität **Datei laden** erfolgt in zwei Schritten. Definieren Sie zunächst die Struktur, die die Importdatei aufweisen soll, indem Sie eine Beispieldatei hochladen. Geben Sie im Anschluss daran die Herkunft der Datei an, die die zu importierenden Daten enthält.  Führen Sie zur Konfiguration der Aktivität die folgenden Schritte aus:

![](../assets/workflow-load-file.png)

### Konfigurieren der Beispieldatei {#sample}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_samplefile"
>title="Beispieldatei"
>abstract="Legen Sie die erwartete Dateistruktur fest, indem Sie eine Beispieldatei hochladen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_formatting"
>title="Formatieren der Aktivität „Datei laden“"
>abstract="Geben Sie im Abschnitt **Formatierung** an, wie die externe Datei formatiert ist, damit die Daten korrekt importiert werden."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_valueremapping"
>title="Erneute Wertzuweisung für die Aktivität „Datei laden“"
>abstract="Verwenden Sie diese Option, um bestimmte Werte aus den geladenen Dateien neuen Werten zuzuordnen. Wenn die Spalte beispielsweise Werte vom Typ „True“/„False“ enthält, können Sie eine Zuordnung hinzufügen, um diese Werte automatisch durch die Zeichen „0“/„1“ zu ersetzen."

Führen Sie diese Schritte aus, um die Beispieldatei zu konfigurieren, mit der die erwartete Dateistruktur definiert wird:

1. Fügen Sie **mehrstufige Kampagne** Aktivität „Datei laden“ hinzu.

1. Wählen Sie die zu verwendende Beispieldatei aus, um die erwartete Dateistruktur zu definieren. Klicken Sie dazu im Abschnitt **[!UICONTROL Beispieldatei]** auf die Schaltfläche **Datei auswählen** und wählen Sie die zu verwendende lokale Datei aus.

1. Es wird eine Vorschau der Beispieldatei mit maximal 30 Zeilen angezeigt.

1. Geben Sie in der Dropdown-Liste **[!UICONTROL Dateityp]** an, ob die Datei getrennte Spalten oder Spalten mit fester Breite verwendet.

   ![](../assets/workflow-load-file-sample.png)

1. Für die Dateitypen mit getrennten Spalten verwenden Sie den Abschnitt **Spalten**, um die Eigenschaften der einzelnen Spalten zu konfigurieren.

   +++Verfügbare Optionen für Dateispalten

   * **[!UICONTROL Titel]**: Titel, der für die Spalte angezeigt wird.
   * **[!UICONTROL Datentyp]**: Die Art von Daten, die in der Spalte enthalten sind.
   * **[!UICONTROL Breite]** (Datentyp Zeichenfolge): Maximale Anzahl an Zeichen, die in der Spalte angezeigt werden sollen.
   * **[!UICONTROL Datentransformation]** (Datentyp Zeichenfolge): Wenden Sie die Transformation auf die in der Spalte enthaltenen Werte an.
   * **[!UICONTROL Umgang mit Leerzeichen]** (Datentyp Zeichenfolge): Geben Sie an, wie die in der Spalte enthaltenen Leerzeichen behandelt werden sollen.
   * **[!UICONTROL Trennzeichen]** (Datentypen für Datum, Uhrzeit, Ganzzahl und Zahl)*: Geben Sie die als Trennzeichen zu verwendenden Zeichen an.
   * **[!UICONTROL NULL zulassen]**: Geben Sie an, wie leere Werte in der Spalte verwaltet werden sollen.
   * **[!UICONTROL Fehlerverarbeitung]** (Zeichenfolgen-Datentyp): Legen Sie das Verhalten fest, wenn in einer der Zeilen Fehler auftreten.
   * **[!UICONTROL Neukodifizierung der Werte]**: Mit dieser Option können Sie bestimmte Werte neuen zuordnen. Wenn die Spalte beispielsweise Werte vom Typ „True“/„False“ enthält, können Sie eine Zuordnung hinzufügen, um diese Werte automatisch durch die Zeichen „0“/„1“ zu ersetzen.

+++

1. Geben Sie im Abschnitt **Formatierung** an, wie die externe Datei formatiert ist, damit die Daten korrekt importiert werden.

### Definieren der hochzuladenden Zieldatei {#target}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetfile"
>title="Zieldatei für die Aktivität „Datei laden“"
>abstract="Legen Sie im Abschnitt **[!UICONTROL Zieldatei]** fest, wie die auf den Server hochzuladende Datei abgerufen werden soll."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_nameofthefile"
>title="Name der Datei"
>abstract="Geben Sie den Namen der Datei an, die auf den Server hochgeladen werden soll. Klicken Sie auf das Symbol **[!UICONTROL Personalisierungsdialog öffnen]**, um mit dem Ausdruckseditor, einschließlich Ereignisvariablen, den Dateinamen zu ermitteln."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_targetdb"
>title="Zieldatenbank"
>abstract="Beim Zugreifen auf eine Aktivität **[!UICONTROL Datei laden]**, die bereits eingerichtet wurde, ist ein zusätzlicher Abschnitt **[!UICONTROL Zieldatenbank]** verfügbar, wenn Sie die Aktivität zum Hochladen der Datei in eine externe Datenbank konfiguriert haben."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_command"
>title="Befehl „Datei laden“"
>abstract="Das Zulassen beliebiger Befehle für die Vorverarbeitung ist ein Sicherheitsproblem. Deaktivieren Sie die Sicherheitsoption „XtkSecurity_Disable_Preproc“, um die Verwendung einer vordefinierten Liste von Befehlen zu erzwingen."

>[!CAUTION]
>
>Bevor Sie die Zieldatei laden, stellen Sie sicher, dass sie wie die Beispieldatei formatiert ist. Abweichungen im Dateiformat, in der Spaltenstruktur oder in der Anzahl der Spalten können zu Fehlern während der mehrstufigen Kampagnenausführung führen.

Gehen Sie wie folgt vor, um die hochzuladende Zieldatei zu definieren:

1. Legen Sie im Abschnitt **[!UICONTROL Zieldatei]** fest, welche Aktion beim Abrufen der auf den Server hochzuladenden Datei ausgeführt werden soll.

   * **[!UICONTROL Lokal gespeicherte Datei hochladen]**: Wählen Sie die von Ihrem Computer hochzuladende Datei aus.

   * **[!UICONTROL Wird durch die Transition angegeben]**: Laden Sie die in der eingehenden Transition angegebene Datei hoch, die aus einer vorherigen Aktivität wie **[!UICONTROL Dateiübertragung]** stammt.

   * **[!UICONTROL Datei vorab bearbeiten]**: Laden Sie die in der vorherigen Transition angegebene Datei hoch und wenden Sie einen Vorab-Bearbeitungsbefehl an, z. B. **[!UICONTROL Dekomprimierung]** oder **[!UICONTROL Entschlüsselung]**.

   * **[!UICONTROL Berechnet]**: Laden Sie die Datei hoch, deren Name im Feld **[!UICONTROL Dateiname]** angegeben ist. Klicken Sie auf das Symbol **[!UICONTROL Personalisierungsdialog öffnen]**, um mit dem Ausdruckseditor, einschließlich Ereignisvariablen, den Dateinamen zu ermitteln.

   ![](../assets/workflow-load-file-config.png)

   >[!NOTE]
   >
   >Wenn Sie auf eine **[!UICONTROL Datei laden]**-Aktivität zugreifen, die bereits eingerichtet wurde, wird ein zusätzlicher Abschnitt **[!UICONTROL Zieldatenbank]** angezeigt, wenn Sie die Aktivität zum Hochladen der Datei in eine externe Datenbank konfiguriert haben. Sie können damit angeben, ob die Datei auf den Campaign-Server oder in die externe Datenbank hochgeladen werden soll.

### Zusätzliche Optionen {#options}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_rejectmgt"
>title="Zurückweisungsverwaltung für die Aktivität „Datei laden“"
>abstract="Geben Sie im Abschnitt **Zurückweisungsverwaltung** an, wie sich die Aktivität bei einem Fehler verhalten soll. Sie können die maximal zulässige Anzahl von Fehlern festlegen und die Option zum **[!UICONTROL Beibehalten von Zurückweisungen in einer Datei]** aktivieren, um auf dem Server eine Datei mit den während des Imports aufgetretenen Fehlern herunterzuladen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_loadfile_delete"
>title="Löschen von Dateien nach dem Importieren"
>abstract="Schalten Sie die Option **Datei nach dem Import löschen** ein, um die Originaldatei nach dem Import vom Server zu löschen."


1. Legen Sie im Abschnitt **Zurückweisungsverwaltung** fest, wie sich die Aktivität bei einem Fehler verhalten soll:

   * Geben Sie im Feld **[!UICONTROL Erlaubte Fehleranzahl]** die maximale Anzahl der Fehler an, die bei der Verarbeitung der zu ladenden Datei zulässig sind. Wenn der Wert beispielsweise auf „20“ festgelegt ist, schlägt die mehrstufige Kampagnenausführung fehl, wenn beim Laden der Datei mehr als 20 Fehler auftreten.

   * Um die beim Laden der Datei aufgetretenen Fehler beizubehalten, aktivieren Sie die Option **[!UICONTROL Zurückweisungen in einer Datei speichern]** und geben Sie den gewünschten Namen für die Datei im Feld **[!UICONTROL Zurückweisungsdatei]** an.

     Nach der Aktivierung dieser Option wird nach der Aktivität eine zusätzliche ausgehende Transition mit dem Namen „Komplement“ hinzugefügt. Fehler, die während des Imports auftreten, werden in der angegebenen Datei auf dem Server gespeichert.

1. Um die hochgeladene Datei vom Server zu löschen, nachdem die mehrstufige Kampagne ausgeführt wurde, schalten Sie die Option **[!UICONTROL Datei nach Import löschen]** um.

   ![](../assets/workflow-load-file-options.png)

1. Klicken Sie auf **Bestätigen**, wenn die Einstellungen korrekt sind.

## Beispiel {#load-example}

Ein Beispiel für das Laden einer externen Datei mithilfe der Aktivität **Abstimmung**, ist in [diesem Abschnitt](reconciliation.md#reconciliation-example) verfügbar.
