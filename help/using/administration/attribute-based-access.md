---
solution: Journey Optimizer
product: journey optimizer
title: Attributbasierte Zugriffssteuerung
description: Mit der attributbasierten Zugriffssteuerung können Sie Berechtigungen definieren, um den Datenzugriff für bestimmte Teams oder Benutzergruppen zu verwalten.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: ABAC, Attribut, Berechtigungen, Daten, Zugriff, vertraulich, Assets
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 43%

---

# Attributbasierte Zugriffssteuerung {#attribute-based-access}

Mit der attributbasierten Zugriffssteuerungsfunktion können Sie Berechtigungen definieren, um den Datenzugriff für bestimmte Teams oder Benutzergruppen zu verwalten. Sie dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und bietet so einen weiteren Schutz personenbezogener Daten.

Verwenden Sie die attributbasierte Zuriffssteuerung in Adobe Journey Optimizer, um Daten zu schützen und spezifischen Zugriff auf bestimmte Feldelemente zu gewähren, darunter Experience-Datenmodell(XDM)-Schemata, Profilattribute und Zielgruppen.

Eine detailliertere Liste der bei der attributbasierten Zugriffssteuerung verwendeten Terminologie finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=de){target="_blank"}.

In diesem Beispiel wird dem Schemafeld **Staatsangehörigkeit“ ein Titel hinzugefügt** um nicht autorisierte Benutzer an der Verwendung zu hindern. Führen Sie die folgenden Schritte aus, damit dies funktioniert:

1. Erstellen Sie eine neue **[!UICONTROL Rolle]** und weisen Sie ihr den entsprechenden **[!UICONTROL Titel]** zu, damit Benutzer auf das Schemafeld zugreifen und es verwenden können.

1. Weisen Sie dem Schemafeld **Staatsangehörigkeit** in Adobe Experience Platform einen **[!UICONTROL Titel]** zu.

1. Verwenden Sie das **[!UICONTROL Schemafeld]** in Adobe Journey Optimizer.

Beachten Sie **[!UICONTROL dass]** Zugriff auf **[!UICONTROL Rollen]** und **[!UICONTROL Produkte]** auch über die attributbasierte Zugriffssteuerungs-API möglich ist. Weitere Informationen finden Sie in dieser [Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html?lang=de){target="_blank"}.

## Erstellen einer Rolle und Zuweisen von Titeln {#assign-role}

>[!IMPORTANT]
>
>>Bevor Sie Berechtigungen für eine Rolle verwalten, erstellen Sie eine Richtlinie. Weitere Informationen sind in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=de){target="_blank"} verfügbar.

**[!UICONTROL Rollen]** sind eine Gruppe von Benutzern, die innerhalb Ihrer Organisation dieselben Berechtigungen, Titel und Sandboxes verwenden. Jeder Benutzer, der einer **[!UICONTROL Rolle]** angehört, hat Anspruch auf die Adobe-Programme und -Services, die im Produkt enthalten sind. Sie können auch eigene &quot;**[!UICONTROL &quot; erstellen]** um den Zugriff von Benutzern auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche präziser festzulegen.

Um ausgewählten Benutzern Zugriff auf das Feld **Staatsangehörigkeit** mit der Bezeichnung C2 zu gewähren, erstellen Sie eine neue **[!UICONTROL Rolle]** mit einer bestimmten Benutzergruppe und gewähren Sie ihnen die Bezeichnung C2, sodass sie die **Staatsangehörigkeit** Details auf einer **[!UICONTROL Journey verwenden können]**.

1. Wählen Sie aus dem [!DNL Permissions]-Produkt im Menü des linken Fensterbereichs die Option **[!UICONTROL Rolle]** und klicken Sie auf **[!UICONTROL Rolle erstellen]**. Beachten Sie, dass Sie auch **[!UICONTROL Titel]** zu integrierten Rollen hinzufügen können.

   ![Erstellen Sie eine neue Rolle im Produkt „Berechtigungen“](assets/role_1.png)

1. Fügen Sie hier einen **[!UICONTROL Namen]** und eine **[!UICONTROL Beschreibung]** zu Ihrer neuen **[!UICONTROL Rolle]** hinzu, hier: Eingeschränkte Rolle „Demografisch“.

1. Wählen Sie Ihre **[!UICONTROL Sandbox]** aus der Dropdown-Liste.

   ![](assets/role_2.png)

1. Klicken Sie im Menü **[!UICONTROL Ressourcen]** auf **[!UICONTROL Adobe Experience Platform]**, um die verschiedenen Funktionen zu öffnen. Hier wählen wir **[!UICONTROL Journeys]** aus.

   ![](assets/role_3.png)

1. Wählen Sie aus der Dropdown-Liste die **[!UICONTROL Berechtigungen]** aus, die mit der ausgewählten Funktion verknüpft sind, z. B. **[!UICONTROL Anzeigen von Journeys]** oder **[!UICONTROL Veröffentlichen von Journeys]**.

   ![](assets/role_6.png)

1. Nach dem Speichern der neu erstellten **[!UICONTROL Rolle]** klicken Sie auf **[!UICONTROL Eigenschaften]**, um den Zugriff auf Ihre Rolle weiter zu konfigurieren.

   ![](assets/role_7.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Benutzer]** auf **[!UICONTROL Benutzer hinzufügen]**.

   ![](assets/role_8.png)

1. Klicken Sie auf der Registerkarte **[!UICONTROL Titel]** auf **[!UICONTROL Titel hinzufügen]**.

   ![](assets/role_9.png)

1. Wählen Sie den **[!UICONTROL Titel]** aus, den Sie Ihrer Rolle hinzufügen möchten, und klicken Sie auf **[!UICONTROL Speichern]**. Gewähren Sie in diesem Beispiel Benutzern den Titel „C2“ für den Zugriff auf das zuvor eingeschränkte Schemafeld.

   ![Speichern Sie die Titelkonfiguration](assets/role_4.png)

Die Benutzer in der Rolle **Eingeschränkte Rolle** Demografisch) haben jetzt Zugriff auf die Objekte mit dem Titel „C2“.

## Zuweisen von Titeln zu einem Objekt in Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Durch die falsche Verwendung von Kennzeichnungen kann der Zugriff für Personen- und Trigger-Richtlinienverletzungen unterbrochen werden.

**[!UICONTROL Kennzeichnungen]** können verwendet werden, um bestimmte Funktionsbereiche mithilfe der attributbasierten Zugriffssteuerung zuzuweisen. In diesem Beispiel ist der Zugriff auf das Feld **Staatsangehörigkeit** eingeschränkt. Auf dieses Feld können nur Benutzer zugreifen, denen die entsprechende **[!UICONTROL Bezeichnung]** zugewiesen **[!UICONTROL Rolle]**.

Beachten Sie, dass Sie **[!UICONTROL Titel]** auch zu **[!UICONTROL Schemata]**, **[!UICONTROL Datensätzen]** und **[!UICONTROL Zielgruppen]** hinzufügen können.

1. Erstellen Sie Ihr **[!UICONTROL Schema]**. Weitere Informationen finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de){target="_blank"}.

   ![](assets/label_1.png)

1. Im neu erstellten **[!UICONTROL Schema]** fügen wir zunächst die Feldergruppe **[!UICONTROL Demografische Details]** hinzu, die das Feld **Staatsangehörigkeit** enthält.

   ![](assets/label_2.png)

1. Überprüfen Sie auf der Registerkarte **[!UICONTROL Titel]** den Namen des eingeschränkten Feldes, hier **Staatsangehörigkeit**. Wählen Sie dann im Menü des rechten Fensterbereichs die Option **[!UICONTROL Bearbeiten von Governance-Titeln]**.

   ![Bearbeiten von Governance-Kennzeichnungen für das Feld](assets/label_3.png)

1. Wählen Sie die entsprechenden **[!UICONTROL Titel]** aus. In diesem Fall können die C2-Daten nicht an einen Drittanbieter exportiert werden. Eine detaillierte Liste der verfügbaren Titel finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de#contract-labels){target="_blank"}.

   ![](assets/label_4.png)

1. Personalisieren Sie Ihr Schema bei Bedarf weiter und aktivieren Sie es dann. Ausführliche Anweisungen zum Aktivieren Ihres Schemas finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=de#profile){target="_blank"}.

Das Feld Ihres Schemas ist jetzt nur noch für Benutzer sichtbar und verwendbar, die Teil eines Rollensatzes mit der Kennzeichnung C2 sind. Wenn Sie Ihrem **[!UICONTROL Feldnamen]** ein **[!UICONTROL Label]** zuweisen, wird **[!UICONTROL Label]** automatisch auf das Feld **Staatsangehörigkeit** in jedem erstellten Schema angewendet.

![](assets/label_5.png)

## Zugriff auf Objekte mit Titeln in Adobe Journey Optimizer {#attribute-access-ajo}

Nachdem der Feldname **Staatsangehörigkeit** in einem neuen Schema und einer neuen Rolle angegeben wurde, kann die Auswirkung dieser Einschränkung in Adobe Journey Optimizer beobachtet werden. In diesem Beispiel:

* Benutzer X, der Zugriff auf Objekte mit dem Titel „C2“ hat, erstellt eine Journey mit einer Bedingung, die auf den eingeschränkten **[!UICONTROL Feldname“]**.
* Benutzer Y versucht ohne Zugriff auf Objekte mit dem Titel „C2“, die Journey zu veröffentlichen.


1. Konfigurieren Sie in Adobe Journey Optimizer die **[!UICONTROL Datenquelle]** mit Ihrem neuen Schema.

   ![Konfigurieren der Datenquelle](assets/journey_1.png)

1. Fügen Sie eine neue **[!UICONTROL Feldergruppe]** Ihres neu erstellten **[!UICONTROL Schemas]** zur integrierten **[!UICONTROL Datenquelle]** hinzu. Sie können auch eine neue externe **[!UICONTROL Datenquelle]** und zugehörige **[!UICONTROL Feldergruppen]** erstellen.

   ![Hinzufügen einer Feldergruppe zur Datenquelle](assets/journey_2.png)

1. Nach Auswahl des zuvor erstellten **[!UICONTROL Schemas]** klicken Sie in der Kategorie **[!UICONTROL Felder]** auf **[!UICONTROL Bearbeiten]**.

   ![](assets/journey_3.png)

1. Wählen Sie den **[!UICONTROL Feldnamen]** aus, den Sie ansprechen möchten. Hier wählen wir das eingeschränkte Feld **Staatsangehörigkeit**.

   ![](assets/journey_4.png)

1. Erstellen Sie eine Journey, die eine E-Mail an Benutzende mit einer bestimmten Staatsangehörigkeit sendet. Fügen Sie ein **[!UICONTROL Ereignis]** und eine **[!UICONTROL Bedingung]** hinzu.

   ![](assets/journey_5.png)

1. Wählen Sie das eingeschränkte Feld **Staatsangehörigkeit** aus, um mit der Erstellung Ihres Ausdrucks zu beginnen.

   ![](assets/journey_6.png)

1. Bearbeiten Sie Ihre **[!UICONTROL Bedingung]**, um eine bestimmte Population mit eingeschränktem Feld **Staatsangehörigkeit** anzusprechen.

   ![](assets/journey_7.png)

1. Personalisieren Sie Ihre Journey nach Bedarf. Hier fügen wir die Aktion **[!UICONTROL E-Mail]** hinzu.

   ![Hinzufügen einer E-Mail-Aktion zur Journey](assets/journey_8.png)

Wenn Benutzer Y ohne Zugriff auf Objekte mit dem Titel „C2“ auf diese Journey mit dem eingeschränkten Feld zugreifen muss:

* Benutzer Y kann den eingeschränkten Feldnamen nicht verwenden, da er nicht sichtbar ist.
* Benutzer Y kann den Ausdruck mit dem eingeschränkten Feldnamen im erweiterten Modus nicht bearbeiten. Der folgende Fehler wird angezeigt: `The expression is invalid. Field is no longer available or you do not have enough permission to see it`.
* Benutzer Y kann den Ausdruck löschen.
* Benutzer Y kann die Journey nicht testen.
* Benutzer Y kann die Journey nicht veröffentlichen.