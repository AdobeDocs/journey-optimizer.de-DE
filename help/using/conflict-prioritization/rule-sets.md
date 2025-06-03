---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit Regelsätzen
description: Erfahren Sie, wie Sie Regelsätze erstellen und anwenden können
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: Nachricht, Häufigkeit, Regeln, Druck
exl-id: 07f5f0b4-417e-408e-8d9e-86615c8a3fbf
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 58%

---

# Arbeiten mit Regelsätzen {#rule-sets}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_rule_sets"
>title="Regelsätze"
>abstract="Verwenden Sie Regelsätze, um die Frequenzbegrenzung auf verschiedene Arten von Marketing-Kommunikationen anzuwenden. Sie können auch Regelsätze erstellen, um einen Teil der Zielgruppe anhand von Regeln zur Frequenzbegrenzung von Journeys auszuschließen."

## Erste Schritte mit Regelsätzen {#gs}

### Was sind Regelsätze? {#what}

Mit Regelsätzen können Sie **mehrere Regeln zu Regelsätzen gruppieren** und auf die gewünschten Journey und Kampagnen anwenden. Dies bietet eine verbesserte Granularität, um zu begrenzen, wie oft und wie viele Journey ein Kunde innerhalb eines bestimmten Zeitraums eingeben kann, oder zu steuern, wie oft Benutzer eine Nachricht je nach Kommunikationstyp erhalten.

Sie können zwei Arten von Regelsätzen erstellen:

* **Kanal** Regelsätze wenden Begrenzungsregeln auf Kommunikationskanäle an. Senden Sie beispielsweise nicht mehr als eine E-Mail- oder SMS-Nachricht pro Tag.
* **Journey** Regelsätze wenden Begrenzungsregeln für Eintritte und Gleichzeitigkeit auf eine Journey an. Lassen Sie Profile beispielsweise nicht in mehrere Journeys gleichzeitig eintreten.

➡️ [Funktion im Video kennenlernen](#video).

### Berechtigungen {#permissions-frequency-rules}

Um mit Geschäftsregeln arbeiten zu können, benötigen Sie die folgenden Berechtigungen:

* **[!UICONTROL Häufigkeitsregeln anzeigen]**: Zugreifen auf und Anzeigen von Geschäftsregeln.
* **[!UICONTROL Häufigkeitsregeln verwalten]**: Erstellen, Bearbeiten oder Löschen von Geschäftsregeln.

Weiterführende Informationen zu Berechtigungen finden Sie in [diesem Abschnitt](../administration/high-low-permissions.md).

### Globale und benutzerdefinierte Regelsätze {#global-custom}

Wenn Sie zum ersten Mal über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Geschäftsregeln]** auf Regelsätze zugreifen, wird ein Standardregelsatz vorab erstellt und aktiviert: der **globale Standardregelsatz**.

Dieser Regelsatz enthält globale Regeln, mit denen Sie steuern können, wie oft Benutzer Nachrichten über einen oder mehrere Kanäle erhalten. Alle in diesem Regelsatz definierten Regeln gelten für alle ausgewählten Kanäle, unabhängig davon, ob Nachrichten von einer Journey oder einer Kampagne gesendet werden.

Zusätzlich zu diesem Regelsatz „Globaler Standardregelsatz“ können Sie &quot;**&quot; erstellen** die Sie auf jede Journey oder Kampagne anwenden können, um bestimmte Begrenzungsregeln anzuwenden. [Erfahren Sie, wie Sie benutzerdefinierte Regelsätze erstellen](#create)

![](assets/rule-sets-default.png)

## Regelsätze erstellen und aktivieren {#Create}

>[!CONTEXTUALHELP]
>id="ajo_rule_set_domain"
>title="Domain des Regelsatzes"
>abstract="Beim Erstellen eines Regelsatzes müssen Sie angeben, ob die Regeln im Regelsatz Begrenzungsregeln erzwingen, die für Kommunikationskanäle oder Journeys spezifisch sind."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Häufigkeitsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie „Marketing“ verfügbar."

<!--NOT USED?
[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="Set the capping for your rule"
>abstract="Specify the maximum number of messages sent to a customer profile within the chosen time frame. The frequency cap will be based on the selected calendar period and will be reset at the beginning of the corresponding time frame."-->

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Wählen Sie die Kategorie der Nachrichtenregel aus"
>abstract="Bei Aktivierung und Anwendung auf eine Nachricht werden alle Häufigkeitsregeln, die der ausgewählten Kategorie entsprechen, automatisch auf diese Nachricht angewendet. Derzeit ist nur die Kategorie „Marketing“ verfügbar."

>[!CONTEXTUALHELP]
>id="ajo_rule_set_rule_capping"
>title="Regelbegrenzung"
>abstract="Legen Sie die Begrenzung für Ihre Regel fest.  Abhängig von der Domain des Regelsatzes und der Auswahl im Feld Regeltyp kann dieses Feld die maximale Anzahl von Nachrichten definieren, die an ein Profil gesendet werden können, oder die maximale Anzahl von Journey, in die das Profil gleichzeitig eintreten oder registriert sein kann."

Gehen Sie wie folgt vor, um einen Regelsatz zu erstellen:

>[!NOTE]
>
>Sie können bis zu 3 lokale Regelsätze der Kanal-Domain und bis zu 5 lokale Regelsätze der Journey-Domain erstellen.

1. Rufen Sie die Liste **[!UICONTROL Regelsätze]** auf und klicken Sie dann auf **[!UICONTROL Regelsatz erstellen]**.

   ![](assets/rule-sets-create-button.png)

1. Legen Sie einen eindeutigen Namen für den Regelsatz fest und fügen Sie eine Beschreibung hinzu.

1. Wählen Sie die Domain des Regelsatzes aus und klicken Sie auf **[!UICONTROL Speichern]**.

   * **Kanal** Domäne: Wenden Sie Begrenzungsregeln für Kommunikationskanäle an.
   * **Journey**-Domain: Wenden Sie Begrenzungsregeln für Einträge und gleichzeitige Zugriffe auf eine Journey an.

   ![](assets/rule-sets-create.png)

1. Definieren Sie die Regeln, die Sie diesem Regelsatz hinzufügen möchten. Rufen Sie dazu den Regelsatz auf und klicken Sie auf **[!UICONTROL Regel hinzufügen]**.

1. Konfigurieren Sie die Regelparameter entsprechend Ihren Anforderungen. Die für die Regel verfügbaren Parameter hängen von der bei ihrer Erstellung ausgewählten Regelsatz-Domain ab.

   Detaillierte Informationen zum Konfigurieren von Journey- und Kanalbegrenzungsregeln finden Sie in den folgenden Abschnitten:

   * [Journey-Begrenzung](../conflict-prioritization/journey-capping.md)
   * [Frequenzlimitierung nach Kanal und Kommunikationstyp](../conflict-prioritization/channel-capping.md)

1. Klicken Sie auf **[!UICONTROL Speichern]**, um die Erstellung der Regel zu bestätigen. Ihre Nachricht wird dem Regelsatz mit dem Status **[!UICONTROL Entwurf]** hinzugefügt.

   ![](assets/rule-set-rule-created.png)

1. Wiederholen Sie die obigen Schritte, um dem Regelsatz so viele Regeln wie nötig hinzuzufügen.

1. Wenn eine Regel erstellt wird, verfügt sie über den Status **[!UICONTROL Entwurf]** und wirkt sich noch auf keine Nachricht aus. Um sie zu aktivieren, klicken Sie auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben der Regel und wählen Sie **[!UICONTROL Aktivieren]**.

   ![](assets/rule-set-activate-rule.png)

1. Aktivieren Sie den Regelsatz, um ihn auf Ihre Journey und Nachrichten anwenden zu können.

   ![](assets/rule-set-activate-set.png)

   >[!NOTE]
   >
   >Es kann bis zu 20 Minuten dauern, bis eine Regel oder ein Regelsatz vollständig aktiviert ist. Sie müssen keine Nachrichten ändern oder Journeys erneut veröffentlichen, damit eine Regel wirksam wird.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

1. Sie können einen Regelsatz auf eine Nachricht oder eine Journey anwenden, je nachdem, welche Domain Sie beim Erstellen des Regelsatzes ausgewählt haben.

   Detaillierte Informationen über die Anwendung von Regelsätzen finden Sie in den folgenden Abschnitten:

   * [Anwenden eines Regelsatzes auf eine Journey](../conflict-prioritization/journey-capping.md#apply-capping)
   * [Anwenden von Begrenzungsregeln auf eine Nachricht](../conflict-prioritization/channel-capping.md#apply)

## Zugriff auf und Verwaltung von Regelsätzen {#access-rule-sets}

Alle erstellten Regelsätze werden im Menü **[!UICONTROL Administration]** > **[!UICONTROL Geschäftsregeln (Beta)]** angezeigt. Sie werden nach dem Datum der letzten Änderung sortiert.

![](assets/rule-sets-list.png)

Klicken Sie auf den Namen eines Regelsatzes, um dessen Inhalt anzuzeigen und zu bearbeiten. Alle Regeln, die in diesem Regelsatz enthalten sind, werden aufgelistet. Im Kontextmenü oben rechts können Sie den Namen und die Beschreibung des Regelsatzes bearbeiten, aktivieren und löschen.

![](assets/rule-set-example.png)

Für jede Regel im Regelsatz können Sie mit der Schaltfläche **[!UICONTROL Mehr Aktionen]** die Regel bearbeiten, aktivieren und löschen.

![](assets/rule-set-example-rules.png)

Um eine Regel oder einen Regelsatz zu deaktivieren, klicken Sie auf die Schaltfläche **[!UICONTROL Weitere Aktionen]** neben dem gewünschten Element und wählen Sie **[!UICONTROL Deaktivieren]**.

![](assets/rule-set-inactive-rule.png)

Der Status ändert sich in **[!UICONTROL Inaktiv]** und die Regel wird nicht mehr auf zukünftige Nachrichtenausführungen angewendet. Alle aktuell ausgeführten Nachrichten sind davon nicht betroffen.

>[!NOTE]
>
>Das Deaktivieren eines Regelsatzes wirkt sich weder auf die Zählung für einzelne Profile aus, noch wird die Zählung zurückgesetzt.

## Anleitungsvideo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435531?quality=12)
