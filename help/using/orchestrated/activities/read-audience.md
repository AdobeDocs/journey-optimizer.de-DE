---
solution: Journey Optimizer
product: journey optimizer
title: Verwenden der Aktivität „Zielgruppe lesen“
description: Erfahren Sie, wie Sie die Aktivität „Zielgruppe lesen“ in einer koordinierten Kampagne verwenden
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 16%

---


# Lesen der Zielgruppe {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Aktivität „Zielgruppe erstellen“"
>abstract="Mit der Aktivität **Zielgruppe erstellen** können Sie die Zielgruppe auswählen, die in die orchestrierte Kampagne eintritt. Bei dieser Zielgruppe kann es sich um eine bestehende Adobe Experience Platform-Zielgruppe oder um eine aus einer CSV-Datei abgerufene Zielgruppe handeln. Beim Senden von Nachrichten im Rahmen einer orchestrierten Kampagne wird die Nachrichtenzielgruppe nicht in der Kanalaktivität, sondern in der Aktivität **Zielgruppe lesen** oder in der Aktivität **Zielgruppe erstellen** definiert."

Mit **[!UICONTROL Aktivität „Zielgruppe lesen]** können Sie eine vorhandene Zielgruppe abrufen - zuvor gespeichert oder importiert - und sie in einer orchestrierten Kampagne wiederverwenden. Diese Aktivität ist besonders nützlich, um einen vordefinierten Satz von Profilen anzusprechen, ohne dass ein neuer Segmentierungsprozess ausgeführt werden muss.

Nachdem die Zielgruppe geladen wurde, können Sie sie optional einschränken, indem Sie ein Feld für eine eindeutige Identität auswählen und die Zielgruppe mit zusätzlichen Profilattributen für Targeting-, Personalisierungs- oder Berichtszwecke anreichern.

## Konfigurieren der Aktivität „Zielgruppe lesen“ {#read-audience-configuration}

Führen Sie die folgenden Schritte aus, um die Aktivität **[!UICONTROL Zielgruppe lesen]** zu konfigurieren:

1. Bevor Sie die Aktivität **[!UICONTROL Zielgruppe lesen]** hinzufügen, wählen Sie in **[!UICONTROL Kampagneneinstellungen]** Zusammenführungsrichtlinie“ aus.

   ![](../assets/read-audience-6.png)

1. Fügen Sie Ihrer **[!UICONTROL Kampagne]** Aktivität „Zielgruppe lesen“ hinzu.

   ![](../assets/read-audience-1.png)

1. Geben Sie **[!UICONTROL Aktivität einen]** Titel“ ein. Dieser Titel dient als Name Ihrer Zielgruppe.

1. Klicken Sie ![Ordnersuchsymbol](../assets/do-not-localize/folder-search.svg), um die Audience auszuwählen, die Sie für Ihre orchestrierte Kampagne ansprechen möchten.

   ![](../assets/read-audience-2.png)

1. Wählen Sie eine **[!UICONTROL Entität&#x200B;]** Ihrer Zielgruppendimension aus. Diese Einstellung definiert die Zielentität und das Attribut, das zur Abstimmung der Zielgruppe mit der Zielgruppendimension verwendet wird.

   ➡️ [Führen Sie die auf dieser Seite beschriebenen Schritte aus, um Ihre Zielgruppendimension für Campaign zu erstellen](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Wählen Sie [!UICONTROL Attribut hinzufügen] aus, um Ihre ausgewählte Zielgruppe mit zusätzlichen Daten anzureichern. In diesem Schritt können Sie der Zielgruppe Profilattribute hinzufügen, was zu einer Liste von Empfängern führt, die mit diesen Attributen erweitert wurden.

1. Wählen Sie **[!UICONTROL Attribute]** aus, die Sie Ihrer Audience hinzufügen möchten. Die Attributauswahl zeigt Felder aus dem **Vereinigungsprofilschema**:

   * Bei CSV-basierten Zielgruppen umfasst dies sowohl **Profil**-Attribute als auch benutzerdefinierte Attribute auf Zielgruppenebene. Diese Attribute befinden sich unter dem folgenden Schemapfad:

     `<audienceid> > _ajobatchjourneystage > audienceEnrichment > CustomerAudienceUpload > <audienceid>`

   * Für standardmäßige AEP-Zielgruppen sind nur **Profil**-Attribute verfügbar, da sie keine eingebetteten zielgruppenspezifischen Felder enthalten.

   >[!NOTE]
   >
   > Einige Attribute werden zwar möglicherweise in der Auswahl angezeigt, ihre Verfügbarkeit zur Laufzeit hängt jedoch davon ab, ob die Zielgruppendaten erfolgreich mit dem **Adobe Experience Platform-Profil abgestimmt und zusammengeführt**.

   ![](../assets/read-audience-4.png)

Nachdem eine Zielgruppe erstellt wurde, ist sie schreibgeschützt verfügbar und kann nicht mehr bearbeitet werden. Sie kann nur verwendet werden, nachdem der Erstellungsprozess vollständig abgeschlossen ist.

## Beispiel

Im folgenden Beispiel wird die Aktivität **[!UICONTROL Zielgruppe lesen]** verwendet, um eine zuvor erstellte und gespeicherte Zielgruppe von Profilen abzurufen, die sich für den Newsletter angemeldet haben. Die Zielgruppe wird dann mit dem Attribut **Treuemitgliedschaft** angereichert, um die Zielgruppenbestimmung für Benutzende zu ermöglichen, die registrierte Mitglieder des Treueprogramms sind.

![](../assets/read-audience-5.png)
