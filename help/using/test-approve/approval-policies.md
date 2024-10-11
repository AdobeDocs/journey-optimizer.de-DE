---
title: Erstellen und Verwalten von Validierungsrichtlinien
description: Erfahren Sie, wie Sie Genehmigungsrichtlinien erstellen und verwalten.
role: User
level: Beginner
feature: Approval
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: cd46b3346e284958e6f3f9fa641b548f68672000
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 5%

---


# Erstellen und Verwalten von Validierungsrichtlinien {#approval-policies}

>[!AVAILABILITY]
>
> Genehmigungsrichtlinien sind derzeit nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Um Zugang zu erhalten, wenden Sie sich an den Adobe-Support.

Genehmigungsrichtlinien ermöglichen es Administratoren, einen Validierungsprozess für Journey und Kampagnen einzurichten. In diesem System werden spezifische Bedingungen beschrieben, die bestimmen, ob eine Journey oder Kampagne genehmigt werden muss. Diese Richtlinien können sich hinsichtlich der Komplexität unterscheiden, von der bloßen Anforderung, dass alle Kampagnen von einem bestimmten Benutzer oder Team überprüft werden müssen, bis hin zur Festlegung von Kriterien, anhand derer die Kampagne erstellt wurde.

## Validierungsrichtlinien erstellen {#create-policies}

1. Rufen Sie im Menü **[!UICONTROL Administration]** in Journey Optimizer **[!UICONTROL Berechtigungen]** und dann **[!UICONTROL Richtlinien]** auf.

   ![](assets/policy_create_1.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Validierungsrichtlinie]** auf **[!UICONTROL Erstellen]** , wählen Sie **[!UICONTROL Validierungsrichtlinie]** und klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Geben Sie einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** für die Richtlinie ein.

1. Wählen Sie aus, ob die Richtlinie für **[!UICONTROL Journey]** oder **[!UICONTROL Kampagnen]** gilt.

   ![](assets/policy_create_2.png)

Jetzt können Sie die Bedingungen verfeinern, um festzulegen, wer die Genehmigungsanfrage starten und wer sie validieren soll.

## Bedingungen für Validierungsrichtlinien festlegen {#conditions}

1. Greifen Sie auf Ihre **[!UICONTROL Validierungsrichtlinie]** zu.

1. Klicken Sie unter dem Menü **[!UICONTROL If]** auf **[!UICONTROL Bedingung hinzufügen]** , um festzulegen, welches Objekt oder welcher Benutzer eine Genehmigungsanfrage Trigger.

1. Wählen Sie die entsprechende **[!UICONTROL Kategorie]**, **[!UICONTROL Übereinstimmungsregel]** und **[!UICONTROL Optionen]** aus.

   Beispiel: &quot;Wenn die Aktion mit einer Briefpost übereinstimmt&quot;oder &quot;Wenn der Anforderer-Benutzername mit John Doe übereinstimmt&quot;.

   ![](assets/policy_condition_1.png)

+++ Weitere Informationen zu verfügbaren Kategorien und Optionen
   <table>
    <tr>
      <th>Kategorie</th>
      <th>Option</th>
    </tr>
    <tr>
      <td rowspan="3">Kampagnentyp</td>
      <td>Geplant (Marketing)</td>
    </tr>
    <tr>
    <td>API-ausgelöst (Marketing)</td>
    </tr>
    <tr>
    <td>API-ausgelöst (Transaktion)</td>
    </tr>
    <tr>
    <td rowspan="8">Aktion</td>
    <td>In-App</td>
    </tr>
    <tr>
    <td>Push-Benachrichtigung</td>
   </tr>
    <tr>
    <td>SMS</td>
    </tr>
    <tr>
    <td>E-Mail</td>
    </tr>
    <tr>
    <td>Direkt-Mail</td>
    </tr>
    <tr>
    <td>Web</td>
    </tr>
    <tr>
    <td>Codebasiert</td>
    </tr>
    <tr>
    <td>Inhaltskarte</td>
    </tr>
    <tr>
    <td>Anforderer-Benutzername</td>
    <td>Name und E-Mail-Adresse des designierten Anforderers</td>
    </tr>
    <tr>
    <td>Anforderer-Benutzergruppe</td>
    <td>Name der Benutzergruppe der entworfenen Anforderer</td>
    </tr>
    </table>


1. Um weitere Kriterien hinzuzufügen, klicken Sie auf **[!UICONTROL Bedingung hinzufügen]** , um zusätzliche Regeln zu definieren, und wählen Sie entweder **[!UICONTROL And]** oder **[!UICONTROL Or]** aus, um festzulegen, wie die Bedingungen verbunden werden.

1. Klicken Sie unter **[!UICONTROL Dann, senden Sie eine Genehmigungsanfrage an das Menü]**, auf **[!UICONTROL Bedingung hinzufügen]** , um festzulegen, welcher Benutzer die Genehmigungsanforderung annehmen kann.

1. Wählen Sie aus der Dropdownliste **[!UICONTROL Kategorie]** aus, ob Sie eine Benutzergruppe oder einen einzelnen Benutzer auswählen möchten.

1. Wählen Sie dann aus der Dropdownliste **[!UICONTROL Option]** die spezifische Benutzergruppe oder den jeweiligen Benutzer aus.

   Der ausgewählte Benutzer oder die ausgewählte Benutzergruppe ist für die Validierung der Genehmigungsanforderung verantwortlich.

   ![](assets/policy_condition_2.png)

1. Um weitere Kriterien hinzuzufügen, klicken Sie auf **[!UICONTROL Bedingung hinzufügen]** , um zusätzliche Regeln zu definieren, und wählen Sie entweder **[!UICONTROL And]** oder **[!UICONTROL Or]** aus, um festzulegen, wie die Bedingungen verbunden werden.

1. Sobald Ihre Richtlinie vollständig konfiguriert ist, klicken Sie auf **[!UICONTROL Speichern]**.

Jetzt können Sie Ihre Validierungsrichtlinie aktivieren, um sie anzuwenden.

## Validierungsrichtlinien aktivieren und verwalten {#activate-policies}

1. Greifen Sie auf Ihre **[!UICONTROL Validierungsrichtlinie]** zu.

1. Klicken Sie dann auf **[!UICONTROL Aktivieren]** , um die konfigurierten Bedingungen auf Ihre Umgebung anzuwenden.

   >[!NOTE]
   >
   >Nach der Aktivierung können Richtlinien nicht mehr bearbeitet werden. Um Bedingungen zu ändern, deaktivieren Sie zuerst die Richtlinie.

   ![](assets/policy_activate_1.png)

1. Öffnen Sie im Menü **[!UICONTROL Richtlinie]** die erweiterten Optionen nach Bedarf zu **[!UICONTROL Bearbeiten]**, **[!UICONTROL Deaktivieren]** oder **[!UICONTROL Duplizieren]** .

   ![](assets/policy_activate_2.png)

