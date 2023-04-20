---
solution: Journey Optimizer
product: journey optimizer
title: Attributbasierte Zugriffssteuerung
description: Mit der attributbasierten Zugriffssteuerung (ABAC) können Sie Berechtigungen definieren, um den Datenzugriff für bestimmte Teams oder Benutzergruppen zu verwalten.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: ABAC, Attribut, Berechtigungen, Daten, Zugriff, vertraulich, Assets
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 100%

---

# Attributbasierte Zugriffssteuerung {#attribute-based-access}

>[!IMPORTANT]
>
>Die Verwendung der attributbasierten Zugriffssteuerung ist derzeit auf ausgewählte Kundinnen und Kunden beschränkt und wird in einer zukünftigen Version für alle Umgebungen bereitgestellt.

Mit der attributbasierten Zugriffssteuerung (ABAC) können Sie Berechtigungen definieren, um den Datenzugriff für bestimmte Teams oder Benutzergruppen zu verwalten. Sie dient dem Schutz sensibler digitaler Assets vor unbefugten Benutzenden und ermöglicht so einen weiteren Schutz personenbezogener Daten.

In Adobe Journey Optimizer können Sie mit ABAC Daten schützen und spezifischen Zugriff auf bestimmte Feldelemente gewähren, darunter Experience-Datenmodell (XDM)-Schemas, Profilattribute und Segmente.

Eine detailliertere Liste der bei ABAC verwendeten Begriffe finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=de).

In diesem Beispiel möchten wir dem Schemafeld **Staatsangehörigkeit** einen Titel hinzufügen, um nicht autorisierte Benutzer an der Verwendung zu hindern. Damit dies funktioniert, gehen Sie wie folgt vor:

1. Erstellen Sie eine neue **[!UICONTROL Rolle]** und weisen Sie ihr den entsprechenden **[!UICONTROL Titel]** zu, damit Benutzer auf das Schemafeld zugreifen und es verwenden können.

1. Weisen Sie dem Schemafeld **Staatsangehörigkeit** in Adobe Experience Platform einen **[!UICONTROL Titel]** zu.

1. Verwenden Sie das **[!UICONTROL Schemafeld]** in Adobe Journey Optimizer.

Beachten Sie, dass der Zugriff auf **[!UICONTROL Rollen]**, **[!UICONTROL Richtlinien]** und **[!UICONTROL Produkte]** auch über die attributbasierte Zugriffssteuerungs-API möglich ist. Weitere Informationen hierzu finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html?lang=de).

## Erstellen einer Rolle und Zuweisen von Titeln {#assign-role}

>[!IMPORTANT]
>
>Bevor Sie Berechtigungen für eine Rolle verwalten, müssen Sie zunächst eine Richtlinie erstellen. Weitere Informationen hierzu finden Sie in der [Dokumentation zu Adobe Experience Platform.](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=de).

**[!UICONTROL Rollen]** sind eine Gruppe von Benutzern, die innerhalb Ihrer Organisation dieselben Berechtigungen, Titel und Sandboxes verwenden. Jeder Benutzer, der einer **[!UICONTROL Rolle]** angehört, hat die Berechtigung für die Adobe-Programme und -Services, die im Produkt enthalten sind.
Sie können auch eigene **[!UICONTROL Rollen]** erstellen, wenn Sie den Zugriff Ihrer Benutzenden auf bestimmte Funktionen oder Objekte in der Benutzeroberfläche präziser definieren möchten.

Wir möchten ausgewählten Benutzern nun Zugriff auf das Feld **Staatsangehörigkeit** mit dem Titel „C2“ gewähren. Dazu müssen wir eine neue **[!UICONTROL Rolle]** mit einer bestimmten Benutzergruppe erstellen und ihr den Titel „C2“ zuweisen, sodass sie die **Staatsangehörigkeits**-Details in einer **[!UICONTROL Journey]** verwenden kann.

1. Wählen Sie aus dem [!DNL Permissions]-Produkt im Menü des linken Fensterbereichs die Option **[!UICONTROL Rolle]** und klicken Sie auf **[!UICONTROL Rolle erstellen]**. Beachten Sie, dass Sie auch **[!UICONTROL Titel]** zu integrierten Rollen hinzufügen können.

   ![](assets/role_1.png)

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

1. Wählen Sie den **[!UICONTROL Titel]** aus, den Sie Ihrer Rolle hinzufügen möchten, und klicken Sie auf **[!UICONTROL Speichern]**. In diesem Beispiel gewähren wir den Benutzern den Titel „C2“, damit sie Zugriff auf das zuvor eingeschränkte Feld des Schemas haben.

   ![](assets/role_4.png)

Die Benutzer in der **Eingeschränkten Rolle „Demografisch“** haben nun Zugriff auf die Objekte mit dem Titel „C2“.

## Zuweisen von Titeln zu einem Objekt in Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Die falsche Verwendung von Titeln kann den Zugang zu Personen unterbrechen und zu Richtlinienverstößen führen.

**[!UICONTROL Titel]** können verwendet werden, um bestimmte Funktionsbereiche mithilfe der attributbasierten Zugriffssteuerung zuzuweisen.
In diesem Beispiel möchten wir den Zugriff auf das Feld **Staatsangehörigkeit** einschränken. Auf dieses Feld können nur Benutzer mit dem entsprechenden **[!UICONTROL Titel]** in ihrer **[!UICONTROL Rolle]** zugreifen.

Beachten Sie, dass Sie **[!UICONTROL Titel]** auch zu **[!UICONTROL Schemas]**, **[!UICONTROL Datensätzen]** und **[!UICONTROL Segmenten]** hinzufügen können.

1. Erstellen Sie Ihr **[!UICONTROL Schema]**. Weitere Informationen hierzu finden Sie in [dieser Dokumentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=de).

   ![](assets/label_1.png)

1. Im neu erstellten **[!UICONTROL Schema]** fügen wir zunächst die Feldergruppe **[!UICONTROL Demografische Details]** hinzu, die das Feld **Staatsangehörigkeit** enthält.

   ![](assets/label_2.png)

1. Überprüfen Sie auf der Registerkarte **[!UICONTROL Titel]** den Namen des eingeschränkten Feldes, hier **Staatsangehörigkeit**. Wählen Sie dann im Menü des rechten Fensterbereichs die Option **[!UICONTROL Bearbeiten von Governance-Titeln]**.

   ![](assets/label_3.png)

1. Wählen Sie die entsprechenden **[!UICONTROL Titel]** aus. In diesem Fall können die C2-Daten nicht an einen Drittanbieter exportiert werden. Eine detaillierte Liste der verfügbaren Titel finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=de#contract-labels).

   ![](assets/label_4.png)

1. Personalisieren Sie Ihr Schema bei Bedarf weiter und aktivieren Sie es dann. Die detaillierten Schritte zum Aktivieren Ihres Schemas finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=de#profile).

Das Feld Ihres Schemas ist nun nur noch für Benutzer sichtbar, die Teil eines Rollensets mit dem Titel „C2“ sind, und kann nur von diesen verwendet werden.
Beachten Sie, dass der **[!UICONTROL Titel]** automatisch auf das Feld **Staatsangehörigkeit** in jedem erstellten Schema angewendet wird, wenn Sie Ihrem **[!UICONTROL Feldnamen]** einen **[!UICONTROL Titel]** zuweisen.

![](assets/label_5.png)

## Zugriff auf Objekte mit Titeln in Adobe Journey Optimizer {#attribute-access-ajo}

Nachdem wir den Namen unseres Feldes **Staatsangehörigkeit** in einem neuen Schema und unserer neuen Rolle angegeben haben, können wir nun die Auswirkungen dieser Einschränkung in Adobe Journey Optimizer sehen.
In unserem Beispiel erstellt ein erster Benutzer X mit Zugriff auf Objekte mit dem Titel „C2“ eine Journey mit einer Bedingung, die auf den eingeschränkten **[!UICONTROL Feldnamen]** abzielt. Ein zweiter Benutzer Y ohne Zugriff auf Objekte mit dem Titel „C2“ muss dann die Journey veröffentlichen.

1. In Adobe Journey Optimizer müssen Sie zunächst die **[!UICONTROL Datenquelle]** mit Ihrem neuen Schema konfigurieren.

   ![](assets/journey_1.png)

1. Fügen Sie eine neue **[!UICONTROL Feldergruppe]** Ihres neu erstellten **[!UICONTROL Schemas]** zur integrierten **[!UICONTROL Datenquelle]** hinzu. Sie können auch eine neue externe **[!UICONTROL Datenquelle]** und zugehörige **[!UICONTROL Feldergruppen]** erstellen.

   ![](assets/journey_2.png)

1. Nach Auswahl des zuvor erstellten **[!UICONTROL Schemas]** klicken Sie in der Kategorie **[!UICONTROL Felder]** auf **[!UICONTROL Bearbeiten]**.

   ![](assets/journey_3.png)

1. Wählen Sie den **[!UICONTROL Feldnamen]** aus, den Sie ansprechen möchten. Hier wählen wir das eingeschränkte Feld **Staatsangehörigkeit**.

   ![](assets/journey_4.png)

1. Erstellen Sie dann eine Journey, die Benutzern mit einer bestimmten Staatsangehörigkeit eine E-Mail sendet. Fügen Sie ein **[!UICONTROL Ereignis]** und dann eine **[!UICONTROL Bedingung]** hinzu.

   ![](assets/journey_5.png)

1. Wählen Sie das eingeschränkte Feld **Staatsangehörigkeit** aus, um mit der Erstellung Ihres Ausdrucks zu beginnen.

   ![](assets/journey_6.png)

1. Bearbeiten Sie Ihre **[!UICONTROL Bedingung]**, um eine bestimmte Population mit eingeschränktem Feld **Staatsangehörigkeit** anzusprechen.

   ![](assets/journey_7.png)

1. Personalisieren Sie Ihre Journey nach Bedarf. Hier fügen wir die Aktion **[!UICONTROL E-Mail]** hinzu.

   ![](assets/journey_8.png)

Wenn Benutzer Y ohne Zugriff auf Objekte mit dem Titel „C2“ auf diese Journey mit diesem eingeschränkten Feld zugreifen muss, geschieht Folgendes:

* Benutzer Y kann den eingeschränkten Feldnamen nicht verwenden, da er nicht sichtbar ist.

* Benutzer Y kann den Ausdruck mit dem eingeschränkten Feldnamen im erweiterten Modus nicht bearbeiten. Der folgende Fehler wird angezeigt `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* Benutzer Y kann den Ausdruck löschen.

* Benutzer Y kann die Journey nicht testen.

* Benutzer Y kann die Journey nicht veröffentlichen.
