---
solution: Journey Optimizer
product: journey optimizer
title: Eine Journey in eine andere Sandbox kopieren
description: Erfahren Sie, wie Sie eine Journey in eine andere Sandbox kopieren
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Eine Journey in eine andere Sandbox kopieren {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Eine Journey in eine andere Sandbox kopieren"
>abstract="Mit Journey Optimizer können Sie eine gesamte Journey von einer Sandbox in eine andere kopieren. Sie können beispielsweise eine Journey aus der Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren. Zusätzlich zur Journey selbst kopiert Journey Optimizer auch die meisten Objekte, von denen die Journey abhängig ist."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox-Details"
>abstract="Wählen Sie die Ziel-Sandbox aus, in die Sie die Journey kopieren möchten. Es sind nur Sandboxes innerhalb Ihrer IMS-Organisation verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Objektdetails"
>abstract="Dies ist die Journey, die Sie kopieren werden."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Abhängige Objekte"
>abstract="Dies ist die Liste der zugeordneten Objekte, die in der Journey verwendet werden. Diese Liste zeigt den Namen, den Objekttyp sowie die interne Journey Optimizer-ID an."

Mit Journey Optimizer können Sie eine gesamte Journey von einer Sandbox in eine andere kopieren. Sie können beispielsweise eine Journey aus Ihrer Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren. Zusätzlich zur Journey selbst kopiert Journey Optimizer auch die meisten Objekte, von denen die Journey abhängig ist: Segmente, Oberflächen (d. h. Vorgaben), Schemata, Ereignisse und Aktionen. Weiterführende Informationen zu kopierten Objekten finden Sie in diesem Abschnitt [Abschnitt](../building-journeys/copy-to-sandbox.md#limitations).

>[!CAUTION]
>
>Wir garantieren nicht, dass alle verknüpften Elemente in die Ziel-Sandbox kopiert werden. Es wird dringend empfohlen, eine gründliche Prüfung durchzuführen, bevor Sie die Journey veröffentlichen. Auf diese Weise können Sie potenzielle fehlende Objekte identifizieren.

Die kopierten Objekte in der Ziel-Sandbox sind eindeutig und es besteht kein Risiko, vorhandene Elemente zu überschreiben. Sowohl die Journey als auch alle Nachrichten innerhalb der Journey werden in den Entwurfsmodus versetzt. Auf diese Weise können Sie vor der Veröffentlichung in der Ziel-Sandbox eine gründliche Validierung durchführen. Der Kopiervorgang kopiert nur die Metadaten zur Journey und die Objekte in dieser Journey. Im Rahmen dieses Prozesses werden keine Profil- oder Datensatzdaten kopiert.

Gehen Sie wie folgt vor, um eine Journey in eine andere Sandbox zu kopieren:

1. Klicken Sie im Menüabschnitt JOURNEY MANAGEMENT auf **[!UICONTROL Journeys]**. Die Liste der Journeys wird angezeigt.

2. Suchen Sie nach der Journey, die Sie kopieren möchten, und klicken Sie auf die **Mehr Aktionen** Symbol (die drei Punkte neben dem Journey-Namen) und klicken Sie auf **In Sandbox kopieren**.

   ![](assets/copy-sandbox1.png)

   Die **In Sandbox kopieren** angezeigt.

   ![](assets/copy-sandbox2.png)

3. Wählen Sie die **Target-Sandbox** aus dem Dropdown-Feld. Es sind nur Sandboxes innerhalb Ihrer IMS-Organisation verfügbar.

4. Überprüfen Sie die **Abhängige Objekte** Abschnitt. Dies ist die Liste der zugeordneten Objekte, die in der Journey verwendet werden. Diese Liste zeigt den Namen, den Objekttyp sowie die interne Journey Optimizer-ID an.

5. Klicken Sie auf **Kopieren** -Schaltfläche oben rechts, um die Journey in die Ziel-Sandbox zu kopieren.

   ![](assets/copy-sandbox3.png)

   Der Kopiervorgang beginnt und der Fortschritt der einzelnen Objekte wird angezeigt. Der Kopiervorgang variiert je nach Komplexität der Journey und der Anzahl der Objekte, die kopiert werden müssen. Wenn ein Fehler auftritt, wird eine Meldung für das zugehörige Objekt angezeigt.

   ![](assets/copy-sandbox4.png)

6. Nachdem das Kopieren abgeschlossen ist, klicken Sie auf **Schließen**.

7. Greifen Sie auf Ihre Ziel-Sandbox zu und führen Sie eine gründliche Prüfung aller kopierten Objekte durch.

## Kopieren von Prozessen und Einschränkungen {#limitations}

Wir garantieren nicht, dass alle verknüpften Elemente in die Ziel-Sandbox kopiert werden. Es wird dringend empfohlen, eine gründliche Überprüfung durchzuführen. Ermitteln Sie alle potenziellen fehlenden Objekte und erstellen Sie sie manuell, bevor Sie die Journey veröffentlichen.

Die folgenden Objekte werden kopiert:

* Segment

   Ein Segment kann nur einmal von einer Sandbox in eine andere kopiert werden. Nachdem ein Segment kopiert wurde, kann es nicht mehr in der Ziel-Sandbox bearbeitet werden.

* Schema

   Die in dieser Journey verwendeten Schemata werden kopiert.

* Nachricht

   Die in der Journey verwendeten Kanalaktionsaktivitäten. Die für die Personalisierung in der Nachricht verwendeten Felder werden nicht auf Vollständigkeit überprüft. Inhaltsbausteine werden nicht kopiert.

* Informationen zur Journey - Arbeitsfläche

   Die Darstellung der Journey auf der Arbeitsfläche einschließlich der Objekte in der Journey wie Bedingungen, Aktionen, Ereignisse, gelesene Segmente usw. Die Sprungaktivität ist von der Kopie ausgeschlossen.

* Ereignis

   Die in der Journey verwendeten Ereignisse und Ereignisdetails werden kopiert.

* Aktion

   Die in der Journey verwendeten Aktionen und Aktionsdetails werden kopiert.

Oberflächen (d. h. Vorgaben) werden nicht kopiert. Das System wählt automatisch die nächstmögliche Übereinstimmung in der Ziel-Sandbox basierend auf Nachrichtentyp und Oberflächenname aus. Wenn keine Oberflächen in der Ziel-Sandbox gefunden werden, schlägt die Oberflächenkopie fehl. Dies bedeutet, dass die Nachrichtenkopie ebenfalls fehlschlägt, da für eine Nachricht eine Oberfläche zur Einrichtung verfügbar sein muss. In diesem Fall muss mindestens eine Fläche für den rechten Kanal der Nachricht erstellt werden, damit die Kopie funktioniert.

Bei Schemas, Zusammenführungsrichtlinien und Segmenten werden diese Objekte nur referenziert, wenn sie das zweite Mal versuchen, kopiert zu werden. Sie werden als bereits vorhandene Objekte behandelt und erneut kopiert. Dies bedeutet, dass diese Objekte nur einmal kopiert werden können.

Adobe Journey Optimizer kann innerhalb von fünf Minuten auf Schemas, Zusammenführungsrichtlinien und Segmente verweisen, ohne dass ein Fehler auf der Arbeitsfläche angezeigt wird. Warten Sie fünf Minuten. Diese Referenzen sind verfügbar.
