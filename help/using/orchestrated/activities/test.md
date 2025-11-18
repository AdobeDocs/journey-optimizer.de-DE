---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Test“ in Ihren orchestrierten Kampagnen
description: Informationen zur Verwendung der Aktivität „Test“
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: 341a4dac0ae1c124559ebf552af5b3e7a35519e7
workflow-type: ht
source-wordcount: '375'
ht-degree: 100%

---


# Test {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Testaktivität"
>abstract="Die Aktivität **Test** ist eine Aktivität zur **Flusskontrolle**. Sie ermöglicht die Aktivierung von Transitionen auf der Basis der angegebenen Bedingungen."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Bedingungen"
>abstract="Die Aktivität **Test** kann mehrere ausgehende Transitionen aufweisen. Während der Ausführung der orchestrierten Kampagne wird jede Bedingung nacheinander getestet, bis eine der Bedingungen erfüllt ist. Wenn keine der Bedingungen erfüllt ist, wird die orchestrierte Kampagne entlang des Pfads der **[!UICONTROL Standardbedingung]** fortgesetzt. Wenn keine Standardbedingung aktiviert ist, wird die orchestrierte Kampagne an dieser Stelle gestoppt."

Die Aktivität **[!UICONTROL Test]** ist eine Aktivität zur **[!UICONTROL Flusskontrolle]**. Sie ermöglicht die Aktivierung von Transitionen auf der Basis der angegebenen Bedingungen.

## Konfigurieren der Aktivität „Test“ {#test-configuration}

Führen Sie diese Schritte aus, um die Aktivität **[!UICONTROL Test]** zu konfigurieren:

1. Fügen Sie Ihrer orchestrierten Kampagne eine Aktivität des Typs **[!UICONTROL Test]** hinzu.

1. Standardmäßig stellt die Aktivität **[!UICONTROL Test]** einen einfachen booleschen Test dar. Wenn die in der Transition „True“ definierte Bedingung erfüllt ist, wird diese Transition aktiviert. Andernfalls wird die standardmäßige Transition „False“ aktiviert.

1. Um die einer Transition zugeordnete Bedingung zu konfigurieren, klicken Sie auf das Symbol **[!UICONTROL Personalisierungsdialog öffnen]**. Definieren Sie mithilfe des Ausdruckseditors die Regeln, die zum Aktivieren dieser Transition erforderlich sind. Sie können auch Ereignisvariablen, Bedingungen und Datums-/Uhrzeitfunktionen nutzen.

   Darüber hinaus können Sie das Feld **[!UICONTROL Label]** ändern, um den Namen der Transition auf der Arbeitsfläche der orchestrierten Kampagne zu personalisieren.

   ![](../assets/workflow-test-default.png)

1. Sie können mehrere Ausgabe-Transitionen zu einer **[!UICONTROL Test]**-Aktivität hinzufügen. Klicken Sie dazu auf die Schaltfläche **[!UICONTROL Bedingung hinzufügen]** und konfigurieren Sie das Label und die zugehörige Bedingung für jede Transition.
v
1. Während der Ausführung der orchestrierten Kampagne wird jede Bedingung nacheinander getestet, bis eine der Bedingungen erfüllt ist. Wenn keine der Bedingungen erfüllt wird, wird die orchestrierte Kampagne auf dem Pfad der **[!UICONTROL Standardbedingung]** fortgesetzt. Wenn keine Standardbedingung aktiviert ist, wird die Kampagne an dieser Stelle gestoppt.

## Beispiel {#example}

In diesem Beispiel werden verschiedene Transitionen basierend auf der Anzahl an Profilen aktiviert, die von der Aktivität **[!UICONTROL Zielgruppe erstellen]** ausgewählt werden:

* Bei mehr als 10.000 ausgewählten Profilen wird eine E-Mail-Nachricht gesendet.
* Für 1.000 bis 10.000 Profile wird eine SMS gesendet.
* Wenn weniger als 1.000 Profile ausgewählt werden, werden sie an die Transition „Nicht kontaktieren“ weitergeleitet.

![](../assets/workflow-test-example.png)

Dazu wurde die Ereignisvariable `vars.recCount` in den Bedingungen „E-Mail“ und „SMS“ verwendet, um die Anzahl der ausgewählten Profile zu zählen und die entsprechende Transition zu aktivieren.

![](../assets/workflow-test-example-config.png)
