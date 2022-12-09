---
solution: Journey Optimizer
product: journey optimizer
title: Arbeiten mit der Arbeitsfläche für Kompositionen
description: Erfahren Sie, wie Sie mit der Arbeitsfläche für Kompositionen arbeiten.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# Arbeiten mit der Arbeitsfläche für Kompositionen {#composition-canvas}

Die Arbeitsfläche für Kompositionen ist eine visuelle Arbeitsfläche, mit der Sie Kompositionen erstellen können, indem Sie Zielgruppen und Aktivitäten nutzen (teilen, ausschließen...).

Die Schritte zum Konfigurieren einer Komposition auf der Arbeitsfläche der Komposition lauten wie folgt:

1. [Definieren der Anfangs-Audience(n)](#starting-audience)
1. [Eine oder mehrere Aktivitäten hinzufügen](#action-activities)
1. [Ergebnisse in einer neuen Zielgruppe speichern](#save)

## Wählen Sie die Startzielgruppe aus {#starting-audience}

Der erste Schritt zum Erstellen einer Komposition besteht darin, eine oder mehrere vorhandene Zielgruppen als Grundlage für Ihre Komposition auszuwählen.

1. Wählen Sie die **[!UICONTROL Audience]** -Aktivität und geben Sie einen Titel für die Aktivität an.

1. Wählen Sie die Zielgruppe aus:

   * Klicken Sie auf **[!UICONTROL Add audience]** Schaltfläche zur Auswahl einer oder mehrerer bestehender Zielgruppen,
   * Klicken Sie auf **[!UICONTROL Build rule]** Schaltfläche zum Erstellen einer neuen Segmentdefinition mithilfe der [Segmentierungsdienst](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-choose-audience.png)

1. Wenn mehrere Zielgruppen ausgewählt sind, legen Sie fest, wie die Profile dieser Zielgruppen zusammengeführt werden sollen:

* **[!UICONTROL Union]**: alle Profile der ausgewählten Zielgruppen einschließen,
* **[!UICONTROL Intersection]**: Profile einschließen, die für alle ausgewählten Zielgruppen gelten,
* **[!UICONTROL Exclude overlap]**: Profile einschließen, die nur zu einer der Zielgruppen gehören. Profile, die zu mehr als einer Zielgruppe gehören, werden nicht einbezogen.

In diesem Beispiel möchten wir alle Profile anvisieren, die zu den Gold- und Silber-Zielgruppen gehören.

![](assets/audiences-starting-audience.png)

Nach Auswahl der Zielgruppen wird die geschätzte Anzahl der Profile am unteren Ende der Aktivität angezeigt.

## Aktivitäten hinzufügen {#action-activities}

Fügen Sie Aktivitäten hinzu, nachdem Sie Ihre Startzielgruppe ausgewählt haben, um Ihre Auswahl zu verfeinern.

Klicken Sie dazu auf die Schaltfläche + im Kompositionspfad und wählen Sie dann die gewünschte Aktivität aus. Der rechte Bereich wird geöffnet, in dem Sie die Aktivität konfigurieren können.

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>Sie können beliebig viele **[!UICONTROL Audience]** und **[!UICONTROL Exclude]** Aktivitäten nach Bedarf in Ihrer Komposition. Es kann jedoch keine zusätzliche Aktivität hinzugefügt werden, nachdem **[!UICONTROL Rank]** und **[!UICONTROL Split]** Aktivitäten.

Sie können eine Aktivität jederzeit aus der Arbeitsfläche entfernen, indem Sie im rechten Bereich auf die Schaltfläche Löschen klicken. Alle Aktivitäten, die nach dieser Aktivität hinzugefügt wurden, werden ebenfalls aus der Arbeitsfläche entfernt.

Verfügbare Aktivitäten sind:

* [Zielgruppe](#audience): zusätzliche Profile einschließen, die zu einer oder mehreren vorhandenen Zielgruppen gehören,
* [Ausschließen](#exclude): Profile ausschließen, die zu einer existierenden Zielgruppe gehören, oder Profile ausschließen, die auf bestimmten Attributen basieren;
* [Rang](#rank): Profile nach einem bestimmten Attribut sortieren, die Anzahl der beizubehaltenden Profile angeben und sie in Ihre Komposition aufnehmen,
* [Aufspaltung](#split): unterteilen Ihre Komposition in mehrere Pfade basierend auf zufälligen Prozentsätzen oder Attributen.

### Zielgruppenaktivität {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Zielgruppenaktivität"
>abstract="Mit der Aktivität Zielgruppe können Sie zusätzliche Profile aus einer vorhandenen Zielgruppe in Ihre Komposition aufnehmen."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Zusammenführungstypen"
>abstract="Geben Sie an, wie die Profile der ausgewählten Zielgruppen zusammengeführt werden sollen."

Die **[!UICONTROL Audience]** ermöglicht es Ihnen, zusätzliche Profile, die zu einer vorhandenen Zielgruppe gehören, in Ihre Komposition aufzunehmen.

Die Konfiguration dieser Aktivität entspricht der des Starts [Zielgruppenaktivität](#starting-audience).

### Aktivität ausschließen {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Ausschlusstyp"
>abstract="Verwenden Sie den Typ Zielgruppe ausschließen , um Profile auszuschließen, die zu einer vorhandenen Zielgruppe gehören. Mit dem Attributtyp Ausschließen können Sie Profile anhand eines bestimmten Attributs ausschließen."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Aktivität ausschließen"
>abstract="Mit der Aktivität Ausschließen können Sie Profile aus Ihrer Komposition ausschließen, indem Sie eine vorhandene Zielgruppe auswählen oder eine Regel verwenden."

Die **[!UICONTROL Exclude]** -Aktivität können Sie Profile aus Ihrer Komposition ausschließen. Es stehen zwei Arten von Ausschlüssen zur Verfügung:

* **[!UICONTROL Exclude Audience]**: Schließen Sie Profile aus einer vorhandenen Zielgruppe aus.

   Klicken Sie auf **[!UICONTROL Add audience]** und wählen Sie die auszuschließende Audience aus.

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Exclude using attribute]**: Profile, die auf einem bestimmten Attribut basieren, ausschließen.

   Wählen Sie das zu suchende Attribut aus und geben Sie dann den auszuschließenden Wert an. In diesem Beispiel schließen wir Profile aus der Komposition aus, deren Wohnadresse in Japan liegt.

   ![](assets/audiences-exclude-attribute.png)

### Rangaktivität {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Rangaktivität"
>abstract="Mithilfe der Rang -Aktivität können Sie Profile nach einem bestimmten Attribut sortieren und in Ihre Komposition einfügen. Schließen Sie beispielsweise die 50 Profile mit der größten Anzahl an Treuepunkten ein."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Profilbegrenzung hinzufügen"
>abstract="Schalten Sie diese Option ein, um eine maximale Anzahl von Profilen anzugeben, die in die Komposition aufgenommen werden sollen."

Die **[!UICONTROL Rank]** ermöglicht es Ihnen, Profile nach einem bestimmten Attribut zu ordnen und in Ihre Komposition einzuschließen. Sie können beispielsweise die 50 Profile mit der größten Anzahl an Treuepunkten einbeziehen.

1. Wählen Sie das Attribut aus, das Sie nachschlagen möchten, und geben Sie eine Rangreihenfolge an (aufsteigend oder absteigend).

   >[!NOTE]
   >
   >Sie können Attribute mit den folgenden Datentypen auswählen: Ganzzahl, Zahlen, kurz <!--(other?)-->

1. Umschalten zwischen **[!UICONTROL Add profile limit]** und geben Sie eine maximale Anzahl von Profilen an, die in die Komposition aufgenommen werden sollen.

   ![](assets/audiences-rank.png)

### Aufspaltung {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Kontrollgruppe"
>abstract="Verwenden Sie Kontrollgruppen, um einen Teil der Profile zu isolieren. Auf diese Weise können Sie die Wirkung einer Marketing-Aktivität messen und einen Vergleich mit dem Verhalten der übrigen Population vornehmen."

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Aufspaltung"
>abstract="Die Aufspaltung ermöglicht es Ihnen, Ihre Komposition in mehrere Pfade zu unterteilen. Beim Veröffentlichen der Komposition wird für jeden Pfad eine Zielgruppe in Adobe Experience Platform gespeichert."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Aufspaltungstyp"
>abstract="Verwenden Sie den Aufspaltungstyp Prozent , um Profile nach dem Zufallsprinzip in mehrere Pfade zu unterteilen. Mit dem Aufspaltungstyp Attribut können Sie Profile anhand eines bestimmten Attributs aufteilen."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Andere Profile"
>abstract="Schalten Sie diese Option ein, um einen zusätzlichen Pfad mit den verbleibenden Profilen zu erstellen, die keiner der in den anderen Pfaden angegebenen Bedingungen entsprechen."

Die **[!UICONTROL Split]** ermöglicht es Ihnen, Ihre Komposition in mehrere Pfade zu unterteilen.

Durch diesen Vorgang wird automatisch ein **[!UICONTROL Save]** -Aktivität am Ende jedes Pfades. Beim Veröffentlichen der Komposition wird für jeden Pfad eine Zielgruppe in Adobe Experience Platform gespeichert.

Es stehen zwei Arten von Aufspaltungsvorgängen zur Verfügung:

* **[!UICONTROL Percent split]**: Profile nach dem Zufallsprinzip in zwei oder mehr Pfade aufgeteilt. Sie können beispielsweise die Profile in 2 verschiedene Pfade von jeweils 45 % aufteilen und einen zusätzlichen Pfad für die Kontrollgruppe hinzufügen.

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Attribute split]**: Profile anhand eines bestimmten Attributs aufteilen. In diesem Beispiel teilen wir Profile anhand ihrer Zimmereinstellungen auf.

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >Die **[!UICONTROL Other profiles]** -Option können Sie einen zusätzlichen Pfad mit den verbleibenden Profilen erstellen, die keiner der in den anderen Pfaden angegebenen Bedingungen entsprechen.

## Audiences speichern {#save}

Konfigurieren Sie die resultierenden Zielgruppen, die in Adobe Experience Platform gespeichert werden.

Wählen Sie dazu die **[!UICONTROL Save audience]** -Aktivität am Ende jedes Pfads und geben Sie dann den Namen der neuen Zielgruppe an, die erstellt werden soll.

![](assets/audiences-publish.png)

Sobald Ihre Komposition fertig ist, können Sie sie veröffentlichen. [Erfahren Sie, wie Sie Kompositionen erstellen](create-compositions.md)

Weitere Informationen:

* [Erste Schritte mit der Komposition von Zielgruppen](get-started-audience-orchestration.md)
* [Erstellen von Komposition-Workflows](create-compositions.md)
* [Zielgruppen aufrufen und verwalten](access-audiences.md)
