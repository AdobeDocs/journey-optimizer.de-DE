---
title: Erstellen und Verwalten von Genehmigungsrichtlinien
description: Erfahren Sie, wie Sie Genehmigungsrichtlinien erstellen und verwalten.
role: User
level: Beginner
feature: Approval
source-git-commit: 8fecd0d4812ba875dba1d47bc32ab08178a13f2c
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 93%

---


# Erstellen und Verwalten von Genehmigungsrichtlinien {#approval-policies}

>[!NOTE]
>
>Zum Erstellen von Genehmigungsrichtlinien benötigen Sie in Adobe Experience Platform über System- oder Produktadministratorberechtigungen. [Weitere Informationen](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home)

Genehmigungsrichtlinien ermöglichen es Admins, einen Validierungsprozess für Journeys und Kampagnen einzurichten. Dieses System legt spezifische Bedingungen fest, die bestimmen, ob eine Journey oder Kampagne genehmigt werden muss. Diese Richtlinien können unterschiedlich komplex sein, von der einfachen Anforderung, dass alle Kampagnen von bestimmten Benutzenden oder Teams überprüft werden müssen, bis hin zur Festlegung von Kriterien, die darauf basieren, wer die Kampagne erstellt hat.

## Erstellen von Genehmigungsrichtlinien {#create-policies}

1. Rufen Sie im Menü **[!UICONTROL Administration]** in Journey Optimizer **[!UICONTROL Berechtigungen]** und dann **[!UICONTROL Richtlinien]** auf.

   ![](assets/policy_create_1.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Genehmigungsrichtlinie]** auf **[!UICONTROL Erstellen]**, wählen Sie **[!UICONTROL Genehmigungsrichtlinie]** aus und klicken Sie auf **[!UICONTROL Bestätigen]**.

1. Geben Sie einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** für die Richtlinie ein.

1. Wählen Sie aus, ob die Richtlinie für **[!UICONTROL Journey]** oder **[!UICONTROL Kampagnen]** gelten soll.

   ![](assets/policy_create_2.png)

Sie können nun die Bedingungen verfeinern, um festzulegen, wer die Genehmigungsanfrage initiiert und wer sie validiert.

## Festlegen von Bedingungen für Genehmigungsrichtlinien {#conditions}

1. Greifen Sie auf Ihre **[!UICONTROL Genehmigungsrichtlinie]** zu.

1. Klicken Sie im Menü **[!UICONTROL Wenn]** auf **[!UICONTROL Bedingung hinzufügen]**, um festzulegen, welches Objekt oder welche Benutzerin bzw. welcher Benutzer eine Genehmigungsanfrage auslöst.

1. Wählen Sie die entsprechende **[!UICONTROL Kategorie]**, **[!UICONTROL Übereinstimmungsregel]** und **[!UICONTROL Optionen]** aus.

   Zum Beispiel „wenn Aktion mit Direktwerbung übereinstimmt“ oder „wenn Benutzername der anfragenden Person mit Max Mustermann übereinstimmt“.

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
    <td>Code-basiert</td>
    </tr>
    <tr>
    <td>Inhaltskarte</td>
    </tr>
    <tr>
    <td>Benutzername der anfragenden Person</td>
    <td>Name und E-Mail-Adresse der anfragenden Person</td>
    </tr>
    <tr>
    <td>Benutzergruppe der anfragenden Person</td>
    <td>Name der Benutzergruppe der anfragenden Personen</td>
    </tr>
    </table>


1. Um weitere Kriterien hinzuzufügen, klicken Sie auf **[!UICONTROL Bedingung hinzufügen]**, um zusätzliche Regeln zu definieren, und wählen Sie entweder **[!UICONTROL Und]** oder **[!UICONTROL Oder]** aus, um anzugeben, wie die Bedingungen miteinander verbunden sind.

1. Klicken Sie im Menü **[!UICONTROL Dann Genehmigungsanfrage senden an]** auf **[!UICONTROL Bedingung hinzufügen]**, um festzulegen, welche Benutzenden die Genehmigungsanfrage annehmen können.

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Kategorie]** aus, ob Sie eine Benutzergruppe oder einzelne Benutzende auswählen möchten.

1. Wählen Sie dann aus der Dropdown-Liste **[!UICONTROL Option]** die spezifische Benutzergruppe oder spezifische Benutzende aus.

   Die ausgewählte Benutzenden oder die ausgewählte Benutzergruppe sind für die Validierung der Genehmigungsanfrage verantwortlich.

   ![](assets/policy_condition_2.png)

1. Um weitere Kriterien hinzuzufügen, klicken Sie auf **[!UICONTROL Bedingung hinzufügen]**, um zusätzliche Regeln zu definieren, und wählen Sie entweder **[!UICONTROL Und]** oder **[!UICONTROL Oder]** aus, um anzugeben, wie die Bedingungen miteinander verbunden sind.

1. Sobald Ihre Richtlinie vollständig konfiguriert ist, klicken Sie auf **[!UICONTROL Speichern]**.

Sie können Ihre Genehmigungsrichtlinie jetzt aktivieren, um sie anzuwenden.

## Aktivieren und Verwalten von Genehmigungsrichtlinien {#activate-policies}

1. Greifen Sie auf Ihre **[!UICONTROL Genehmigungsrichtlinie]** zu.

1. Klicken Sie dann auf **[!UICONTROL Aktivieren]**, um die konfigurierten Bedingungen auf Ihre Umgebung anzuwenden.

   >[!NOTE]
   >
   >Einmal aktivierte Richtlinien können nicht mehr bearbeitet werden. Um Bedingungen zu ändern, deaktivieren Sie die Richtlinie zunächst.

   ![](assets/policy_activate_1.png)

1. Öffnen Sie im Menü **[!UICONTROL Richtlinie]** die erweiterten Optionen, um die Richtlinie nach Bedarf zu **[!UICONTROL Bearbeiten]**, zu **[!UICONTROL Deaktivieren]** oder zu **[!UICONTROL Duplizieren]**.

   ![](assets/policy_activate_2.png)

