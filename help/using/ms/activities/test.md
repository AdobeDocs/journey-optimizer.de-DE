---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Testaktivität in Ihren koordinierten Kampagnen
description: Erfahren Sie, wie Sie die Test -Aktivität verwenden
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3d33d0bdbaf5b56a68d4ea708ce023c6aaae4811
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 60%

---

# Test {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Testaktivität"
>abstract="Die Aktivität **Test** ist eine Aktivität zur **Flusskontrolle**. Sie ermöglicht die Aktivierung von Transitionen auf der Basis der angegebenen Bedingungen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Bedingungen"
>abstract="Die Aktivität **Test** kann mehrere ausgehende Transitionen aufweisen. Während der orchestrierten Kampagnenausführung wird jede Bedingung sequenziell getestet, bis eine davon erfüllt ist. Wenn keine der Bedingungen erfüllt ist, fährt die orchestrierte Kampagne mit dem Pfad der **[!UICONTROL Standardbedingung]** fort. Wenn keine Standardbedingung aktiviert ist, stoppt die orchestrierte Kampagne an dieser Stelle."

Die Aktivität **Test** ist eine Aktivität zur **Flusskontrolle**. Sie ermöglicht die Aktivierung von Transitionen auf der Basis der angegebenen Bedingungen.

## Konfigurieren der Aktivität „Test“ {#test-configuration}

Führen Sie diese Schritte aus, um die Aktivität **Test** zu konfigurieren:

1. Fügen Sie **orchestrierten Kampagne** Aktivität „Test“ hinzu.

1. Standardmäßig stellt die Aktivität **[!UICONTROL Test]** einen einfachen booleschen Test dar. Wenn die in der Transition „True“ definierte Bedingung erfüllt ist, wird diese Transition aktiviert. Andernfalls wird die standardmäßige Transition „False“ aktiviert.

1. Um die einer Transition zugeordnete Bedingung zu konfigurieren, klicken Sie auf das Symbol **[!UICONTROL Personalisierungsdialog öffnen]**. Definieren Sie mithilfe des Ausdruckseditors die Regeln, die zum Aktivieren dieser Transition erforderlich sind. Sie können auch Ereignisvariablen, Bedingungen und Datums-/Uhrzeitfunktionen nutzen.

   Darüber hinaus können Sie das Feld **[!UICONTROL Titel]** ändern, um den Namen der Transition auf der koordinierten Kampagnen-Arbeitsfläche zu personalisieren.

   ![](../assets/workflow-test-default.png)

1. Sie können mehrere Ausgabe-Transitionen zu einer **[!UICONTROL Test]**-Aktivität hinzufügen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]** und konfigurieren Sie die Bezeichnung und die zugehörige Bedingung für jede Transition.
v
1. Während der orchestrierten Kampagnenausführung wird jede Bedingung sequenziell getestet, bis eine davon erfüllt ist. Wenn keine der Bedingungen erfüllt ist, werden die orchestrierten Kampagnen entlang des Pfads der **[!UICONTROL Standardbedingung“]**. Wenn keine Standardbedingung aktiviert ist, werden die Workflows an dieser Stelle beendet.

## Beispiel {#example}

In diesem Beispiel werden verschiedene Transitionen basierend auf der Anzahl an Profilen aktiviert, die von der Aktivität **[!UICONTROL Zielgruppe erstellen]** ausgewählt werden:

* Bei mehr als 10.000 ausgewählten Profilen wird eine E-Mail-Nachricht gesendet.
* Für 1.000 bis 10.000 Profile wird eine SMS gesendet.
* Wenn weniger als 1.000 Profile ausgewählt werden, werden sie an die Transition „Nicht kontaktieren“ weitergeleitet.

![](../assets/workflow-test-example.png)

Dazu wurde die Ereignisvariable `vars.recCount` in den Bedingungen „E-Mail“ und „SMS“ verwendet, um die Anzahl der ausgewählten Profile zu zählen und die entsprechende Transition zu aktivieren.

![](../assets/workflow-test-example-config.png)
