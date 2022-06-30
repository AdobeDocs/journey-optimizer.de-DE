---
title: Journey in eine andere Sandbox kopieren
description: Erfahren Sie, wie Sie eine Journey in eine andere Sandbox kopieren
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f75ed263fd8226a6b5f55bbb50f4aae17cbfe9d4
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# Journey in eine andere Sandbox kopieren {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Journey in eine andere Sandbox kopieren"
>abstract="Mit Journey Optimizer können Sie eine ganze Journey von einer Sandbox in eine andere kopieren. Sie können beispielsweise eine Journey aus der Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren. Zusätzlich zur Journey kopiert Journey Optimizer auch die meisten Objekte, von denen die Journey abhängig ist."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox-Details"
>abstract="Wählen Sie die Ziel-Sandbox aus, in die Sie die Journey kopieren möchten. Es sind nur Sandboxes innerhalb Ihrer IMS-Organisation verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Objektdetails"
>abstract="Das ist die Journey, die Sie kopieren werden."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Abhängige Objekte"
>abstract="Dies ist die Liste der zugeordneten Objekte, die im Journey verwendet werden. In dieser Liste werden der Name, der Objekttyp und die interne Journey Optimizer ID angezeigt."

Mit Journey Optimizer können Sie eine ganze Journey von einer Sandbox in eine andere kopieren. Sie können beispielsweise eine Journey aus Ihrer Staging-Sandbox-Umgebung in Ihre Produktions-Sandbox kopieren. Zusätzlich zur Journey kopiert Journey Optimizer auch die meisten Objekte, von denen die Journey abhängig ist: Nachrichten, Segmente, Vorgaben, Schemas, Ereignisse und Aktionen. Siehe Abschnitt [Einschränkungen](../building-journeys/copy-to-sandbox.md#limitations)

>[!CAUTION]
>
>Wir garantieren nicht, dass alle verknüpften Elemente in die Ziel-Sandbox kopiert werden. Es wird dringend empfohlen, eine gründliche Prüfung durchzuführen, bevor Sie die Journey veröffentlichen. Auf diese Weise können Sie potenzielle fehlende Objekte identifizieren.

Die kopierten Objekte in der Ziel-Sandbox sind eindeutig und es besteht kein Risiko, vorhandene Elemente zu überschreiben. Sowohl die Journey als auch alle Nachrichten innerhalb der Journey werden im Entwurfsmodus übergeben. Auf diese Weise können Sie vor der Veröffentlichung in der Ziel-Sandbox eine gründliche Validierung durchführen. Der Kopiervorgang kopiert nur die Metadaten über die Journey und die Objekte in dieser Journey. Im Rahmen dieses Prozesses werden keine Profil- oder Datensatzdaten kopiert.

Gehen Sie wie folgt vor, um eine Journey in eine andere Sandbox zu kopieren:

1. Klicken Sie im Menü JOURNEY-MANAGEMENT auf **[!UICONTROL Journeys]**. Die Liste der Journeys wird angezeigt.

2. Suchen Sie nach der Journey, die Sie kopieren möchten, und klicken Sie auf die **Mehr Aktionen** (die drei Punkte neben dem Journey-Namen) und klicken Sie auf **In Sandbox kopieren**.

   ![](assets/copy-sandbox1.png)

   Die **In Sandbox kopieren** angezeigt.

   ![](assets/copy-sandbox2.png)

3. Wählen Sie die **Target-Sandbox** aus dem Dropdown-Feld. Es sind nur Sandboxes innerhalb Ihrer IMS-Organisation verfügbar.

4. Überprüfen Sie die **Abhängige Objekte** Abschnitt. Dies ist die Liste der zugeordneten Objekte, die im Journey verwendet werden. In dieser Liste werden der Name, der Objekttyp und die interne Journey Optimizer ID angezeigt.

5. Klicken Sie auf **Kopieren** -Schaltfläche oben rechts, um mit dem Kopieren der Journey in die Ziel-Sandbox zu beginnen.

   ![](assets/copy-sandbox3.png)

   Der Kopiervorgang beginnt und der Fortschritt der einzelnen Objekte wird angezeigt. Der Kopiervorgang hängt von der Komplexität der Journey ab und davon, wie viele Objekte kopiert werden müssen. Wenn ein Fehler auftritt, wird eine Meldung für das zugehörige Objekt angezeigt.

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

   Die in der Journey verwendeten physischen Nachrichten (E-Mail oder Push-Nachrichten). Die für die Personalisierung in der Nachricht verwendeten Felder werden nicht auf Vollständigkeit überprüft. Inhaltsbausteine werden nicht kopiert.

* Journey - Leinwanddetails

   Die Darstellung der Journey auf der Arbeitsfläche einschließlich der Objekte auf der Journey, wie Bedingungen, Aktionen, Ereignisse, Lesesegmente usw. Die Sprungaktivität ist von der Kopie ausgeschlossen.

* Event

   Die Ereignisse und Ereignisdetails, die auf der Journey verwendet werden, werden kopiert.

* Aktion

   Die im Journey verwendeten Aktionen und Aktionsdetails werden kopiert.

Vorgaben werden nicht kopiert. Das System wählt basierend auf dem Nachrichtentyp und dem Vorgabennamen automatisch die nächstmögliche Übereinstimmung für die Ziel-Sandbox aus. Wenn keine Vorgaben in der Ziel-Sandbox gefunden werden, schlägt die Vorgabenkopie fehl. Dies bedeutet, dass die Nachrichtenkopie ebenfalls fehlschlägt, da für eine Nachricht eine Vorgabe zur Einrichtung verfügbar sein muss. In diesem Fall muss mindestens eine Vorgabe für den rechten Kanal der Nachricht erstellt werden, damit die Kopie funktioniert.

Bei Schemas, Zusammenführungsrichtlinien und Segmenten werden diese Objekte nur referenziert, wenn sie das zweite Mal versuchen, kopiert zu werden. Sie werden als bereits vorhandene Objekte behandelt und erneut kopiert. Dies bedeutet, dass diese Objekte nur einmal kopiert werden können.

Es dauert fünf Minuten, bis Adobe Journey Optimizer auf Schemas, Zusammenführungsrichtlinien und Segmente verweisen kann, ohne dass auf der Arbeitsfläche ein Fehler angezeigt wird. Warten Sie fünf Minuten. Diese Referenzen sind verfügbar.

