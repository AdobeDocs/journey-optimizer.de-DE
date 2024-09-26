---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer-Objekte zwischen Sandboxes kopieren
description: Erfahren Sie, wie Sie Journey, Inhaltsvorlagen und Fragmente zwischen Sandboxes kopieren.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: Sandbox, Journey, Kopieren, Umgebung
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 26%

---


# Kopieren von Journey Optimizer-Objekten in eine andere Sandbox {#copy-to-sandbox}

Sandbox Tooling ermöglicht Ihnen das Kopieren von Objekten wie Journey, Inhaltsvorlagen oder Fragmenten über mehrere Sandboxes hinweg, indem Sie Package-Export und -Import nutzen. Ein Paket kann aus einem oder mehreren Objekten bestehen. Alle Objekte, die in einem Paket enthalten sind, müssen aus derselben Sandbox stammen.

Auf dieser Seite wird der Anwendungsfall der Sandbox-Werkzeuge im Kontext von Journey Optimizer beschrieben. Weitere Informationen zur Funktion sind in der [Dokumentation zu Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=de) verfügbar.

>[!NOTE]
>
>Diese Funktion erfordert die folgenden Berechtigungen von der Funktion **Sandbox-Administration**: „Sandboxes verwalten“ (oder „Sandboxes anzeigen“) und „Pakete verwalten“. [Weitere Informationen](../administration/ootb-permissions.md)

Der Kopiervorgang erfolgt über den Export und Import eines Pakets zwischen der Quell- und der Ziel-Sandbox. Nachfolgend erfahren Sie, wie Sie eine Journey von einer Sandbox in eine andere kopieren:

1. Fügen Sie das Objekt hinzu, das als Paket in der Quell-Sandbox exportiert werden soll.
1. Exportieren Sie das Paket in die Ziel-Sandbox.

Darüber hinaus können Sie Sandbox-Objekte mithilfe der **Objektkopierdienst-REST-API** von Journey Optimizer verwalten. [Erfahren Sie, wie Sie mit der Objektkopierdienst-REST-API arbeiten](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## Exportierte Objekte und Best Practices {#objects}

Journey Optimizer ermöglicht den Export von Journey, Inhaltsvorlagen und Fragmenten in eine andere Sandbox. Die folgenden Abschnitte enthalten Informationen und Best Practices für die einzelnen Objekttypen.

### Allgemeine Best Practices {#global}

* Beim Kopieren eines Objekts werden alle Abhängigkeiten (z. B. verschachtelte Fragmente, Journey-Zielgruppen oder Aktionen) im übergeordneten Objekt korrekt aktualisiert, sodass eine ordnungsgemäße Zuordnung in der Ziel-Sandbox gewährleistet ist.

* Wenn ein exportiertes Objekt eine Profilpersonalisierung enthält, stellen Sie sicher, dass das entsprechende Schema in der Ziel-Sandbox vorhanden ist, um Personalisierungsprobleme zu vermeiden.

### Journeys {#journeys}

* Beim Exportieren einer Journey kopiert Journey Optimizer neben der Journey selbst auch die meisten Objekte, von denen die Journey abhängig ist: Zielgruppen, Schemata, Ereignisse und Aktionen. Weiterführende Informationen zu kopierten Objekten finden Sie in diesem [Abschnitt](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=de#abobe-journey-optimizer-objects).

* Wir garantieren nicht, dass alle verknüpften Elemente in die Ziel-Sandbox kopiert werden. Es wird dringend empfohlen, eine gründliche Prüfung durchzuführen, z. B. bevor Sie eine Journey veröffentlichen. Auf diese Weise können Sie potenzielle fehlende Objekte identifizieren.

* Die kopierten Objekte in der Ziel-Sandbox sind eindeutig, sodass kein Risiko besteht, vorhandene Elemente zu überschreiben. Sowohl die Journey als auch alle Nachrichten innerhalb der Journey werden im Entwurfsmodus übergeben. Auf diese Weise können Sie vor der Veröffentlichung in der Ziel-Sandbox eine gründliche Validierung durchführen.

* Der Kopiervorgang kopiert nur die Metadaten über die Journey und die Objekte in dieser Journey. Im Rahmen dieses Prozesses werden keine Profil- oder Datensatzdaten kopiert.

### Inhaltsvorlagen {#content-templates}

* Beim Exportieren einer Inhaltsvorlage werden auch alle verschachtelten Fragmente kopiert.

* Das Exportieren von Inhaltsvorlagen kann manchmal zu einer Duplizierung von Fragmenten führen. Wenn beispielsweise zwei Vorlagen dasselbe Fragment verwenden und in separate Pakete kopiert werden, müssen beide Vorlagen dasselbe Fragment in der Ziel-Sandbox wiederverwenden. Um Duplikate zu vermeiden, wählen Sie während des Importvorgangs die Option &quot;Vorhandene verwenden&quot;. [Erfahren Sie, wie Sie ein Paket importieren](#import)

* Um Duplikate zu vermeiden, wird empfohlen, Inhaltsvorlagen in ein einzelnes Package zu exportieren. Dadurch wird sichergestellt, dass das System Deduplizierungen effizient verwaltet.

### Fragmente {#fragments}

* Fragmente können über mehrere Status verfügen, z. B. Live, Entwurf und Live mit Entwurf. Beim Exportieren eines Fragments wird der aktuelle Entwurfsstatus in die Ziel-Sandbox kopiert.

* Beim Exportieren eines Fragments werden auch alle verschachtelten Fragmente kopiert.

## Objekte als Paket hinzufügen{#export}

Um Objekte in eine andere Sandbox zu kopieren, müssen Sie sie zunächst als Paket in die Quell-Sandbox hinzufügen. Führen Sie folgende Schritte aus:

1. Navigieren Sie zum Inventar, in dem das erste Objekt, das Sie kopieren möchten, gespeichert ist, z. B. die Liste Journey . Klicken Sie auf das Symbol &quot;**Mehr Aktionen**&quot;(die drei Punkte neben dem Objektnamen) und klicken Sie auf &quot;**Zu Paket hinzufügen**&quot;.

   ![](assets/journey-sandbox1.png)

1. Wählen Sie im Fenster **Zu Paket hinzufügen** aus, ob Sie das Objekt einem vorhandenen Paket hinzufügen oder ein neues Paket erstellen möchten:

   ![](assets/journey-sandbox2.png)

   * **Vorhandenes Paket**: Wählen Sie das Paket aus dem Dropdown-Menü aus.
   * **Neues Paket erstellen**: Geben Sie den Paketnamen ein. Sie können auch eine Beschreibung hinzufügen.

1. Wiederholen Sie diese Schritte, um alle Objekte hinzuzufügen, die Sie mit Ihrem Package exportieren möchten.

>[!NOTE]
>
>Für Journey-Exporte kopiert Journey Optimizer neben der Journey selbst auch die meisten Objekte, von denen die Journey abhängig ist: Zielgruppen, Schemata, Ereignisse und Aktionen. Weiterführende Informationen zum Exportieren von Journey finden Sie in [diesem Abschnitt](../building-journeys/copy-to-sandbox.md).

## Publish des zu exportierenden Packages {#publish}

Nachdem Ihr Paket für den Export bereit ist, führen Sie die folgenden Schritte aus, um es zu veröffentlichen:

1. Navigieren Sie zum Menü **[!UICONTROL Administration]** > **[!UICONTROL Sandboxes]** und wählen Sie die Registerkarte **Pakete** aus.

1. Öffnen Sie das Paket, das Sie exportieren möchten, wählen Sie die Objekte aus, die Sie exportieren möchten, und klicken Sie auf **Publish**.

   In diesem Beispiel möchten wir eine Journey, eine Inhaltsvorlage und ein Fragment exportieren.

   ![](assets/journey-sandbox4.png)

1. So verfolgen Sie den Status der Veröffentlichung des Pakets auf der Registerkarte **[!UICONTROL Aufträge]** . Weitere Informationen zu einem Auftrag erhalten Sie, wenn Sie ihn in der Liste auswählen und auf die Schaltfläche **[!UICONTROL Importdetails anzeigen]** klicken.

   ![](assets/journey-sandbox9.png)

## Importieren des Pakets in die Ziel-Sandbox {#import}

Nachdem das Paket veröffentlicht wurde, müssen Sie es in die Ziel-Sandbox importieren. Führen Sie folgende Schritte aus:

1. Navigieren Sie zum Menü **[!UICONTROL Sandboxes]** und wählen Sie die Registerkarte **[!UICONTROL Durchsuchen]** aus.

1. Suchen Sie nach der Sandbox, in die Sie das Paket importieren möchten, und klicken Sie dann neben dem Namen auf das Symbol + .

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Es sind nur Sandboxes innerhalb Ihrer Organisation verfügbar.

1. Überprüfen Sie im Feld **Ziel-Sandbox** , ob die richtigen Ziel-Sandboxes ausgewählt sind, und wählen Sie das zu importierende Paket aus der Dropdownliste **[!UICONTROL Paketname]** aus. Klicken Sie auf **Weiter**.

   ![](assets/journey-sandbox6.png)

1. Überprüfen Sie die Paketobjekte und Abhängigkeiten. Dies ist die Liste der Objekte, die zum Package hinzugefügt wurden, zusammen mit anderen Objekten, von denen Journey abhängig sind, wie Zielgruppen, Schemata, Ereignisse oder Aktionen.

   Für jedes Objekt können Sie entweder ein neues erstellen oder ein vorhandenes Objekt in der Ziel-Sandbox verwenden. Auf diese Weise können Sie beispielsweise Fragmentduplizierung vermeiden, die beim Import von Inhaltsvorlagen mit gängigen Fragmenten auftreten kann.

   ![](assets/journey-sandbox7.png)

1. Klicken Sie oben rechts auf die Schaltfläche **Beenden** , um mit dem Kopieren des Pakets in die Ziel-Sandbox zu beginnen. Der Kopiervorgang variiert je nach Komplexität der Objekte und der Anzahl der zu kopierenden Objekte.

1. Klicken Sie auf den Importvorgang, um das Kopierergebnis zu überprüfen:

   * Klicken Sie auf die Schaltfläche **Importierte Objekte anzeigen** , um die einzelnen kopierten Objekte anzuzeigen.
   * Klicken Sie auf die Schaltfläche **Importdetails anzeigen** , um die Importergebnisse für jedes Objekt zu überprüfen.

   ![](assets/journey-sandbox8.png)

1. Greifen Sie auf Ihre Ziel-Sandbox zu und führen Sie eine gründliche Prüfung aller kopierten Objekte durch.
