---
solution: Journey Optimizer
product: journey optimizer
title: Hinzufügen personalisierter Angebote
description: Erfahren Sie, wie Sie Ihren Nachrichten personalisierte Angebote hinzufügen
feature: Email Design, Offers
topic: Content Management
role: User
level: Intermediate
keywords: Angebote, Entscheidung, E-Mails, Personalisierung, Entscheidung
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
TQID: https://experienceleague.adobe.com/ajycOqX0Q6spKP8RgXmF-QLR95AYsCLLfIaKofpd95k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 623
ht-degree: 100%

---

# Hinzufügen personalisierter Angebote {#deliver-personalized-offers}

In [!DNL Journey Optimizer]-E-Mails können Sie Entscheidungen einfügen, die die Entscheidungs-Management-Engine nutzen, um das jeweils beste Angebot für Ihre Kundinnen und Kunden auszuwählen.

Sie können beispielsweise eine Entscheidung hinzufügen, die in Ihrer E-Mail ein besonderes Angebot mit Rabatten anzeigt, das je nach Treuestufe der Empfangenden variiert.

>[!IMPORTANT]
>
>Wenn Änderungen an einer Angebotsentscheidung vorgenommen werden, die in einer Journey-Nachricht verwendet wird, müssen Sie die Veröffentlichung der Journey aufheben und sie dann erneut veröffentlichen.  Dadurch wird sichergestellt, dass die Änderungen in die Journey aufgenommen werden und die Nachricht den neuesten Aktualisierungen entspricht.

* Weiterführende Informationen zur Erstellung und Verwaltung von Angeboten finden Sie in [diesem Abschnitt](../offers/get-started/starting-offer-decisioning.md).
* Ein **vollständiges Beispiel**, das zeigt, wie Angebote konfiguriert, in Entscheidungen verwendet und diese Entscheidungen in E-Mails eingesetzt werden, finden Sie in [diesem Abschnitt](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [In diesem Video erfahren Sie, wie Sie Angebote als Teil der Personalisierung hinzufügen](#video-offers)

## Einfügen einer Entscheidung in eine E-Mail {#insert-offers}

>[!CAUTION]
>
>Bevor Sie beginnen, müssen Sie [eine Angebotsentscheidung definieren](../offers/offer-activities/create-offer-activities.md).

Gehen Sie wie folgt vor, um eine Entscheidung in eine E-Mail-Nachricht einzufügen:

1. Erstellen Sie Ihre E-Mail und öffnen Sie dann E-Mail-Designer, um den Inhalt zu konfigurieren.

1. Fügen Sie die Inhaltskomponente **[!UICONTROL Angebotsentscheidung]** hinzu.

   ![](assets/deliver-offer-component.png)

   In [diesem Abschnitt](content-components.md) erfahren Sie, wie Sie Inhaltskomponenten verwenden.

1. Die Registerkarte **[!UICONTROL Angebotsentscheidung]** wird in der rechten Palette angezeigt. Klicken Sie auf **[!UICONTROL Angebotsentscheidung auswählen]**:

   1. Wählen Sie im sich öffnenden Fenster die Platzierung aus, die den anzuzeigenden Angeboten entspricht.

      [Platzierungen sind Container, mit denen Ihre Angebote präsentiert werden. ](../offers/offer-library/creating-placements.md) In diesem Beispiel verwenden wir die Platzierung „E-Mail-Top-Bild“. Diese Platzierung wurde in der Angebotsbibliothek erstellt, um Angebote des Typs Bild oben am Anfang von Nachrichten anzuzeigen.

   1. Entscheidungen, die mit der ausgewählten Platzierung übereinstimmen, werden angezeigt. Wählen Sie die in der Inhaltskomponente zu verwendende Entscheidung aus und klicken Sie dann auf **[!UICONTROL Hinzufügen]**.

      >[!NOTE]
      >
      >Beachten Sie, dass nur Entscheidungen, die mit der ausgewählten Platzierung kompatibel sind, in der Liste angezeigt werden. In diesem Beispiel stimmt nur eine Angebotsaktivität mit der Platzierung „E-Mail-Top-Bild“ überein.

      ![](assets/deliver-offer-placement.png)

Die Entscheidung wird nun der Komponente hinzugefügt. Nachdem Sie die Änderungen gespeichert haben, können Ihre Angebote den entsprechenden Profilen angezeigt werden, wenn die Nachricht als Teil einer Journey gesendet wird.

>[!NOTE]
>
>Wenn Sie ein Angebot, ein Fallback-Angebot, eine Angebotssammlung oder eine Angebotsentscheidung aktualisieren, auf die direkt oder indirekt in einer Nachricht verwiesen wird, werden die Aktualisierungen automatisch in der entsprechenden Nachricht angezeigt.

## Angebotsvorschau in einer E-Mail {#preview-offers-in-email}

Sie können die verschiedenen Angebote, die Teil der Entscheidung sind, die der E-Mail hinzugefügt wurde, in der Vorschau anzeigen, indem Sie den Abschnitt **[!UICONTROL Angebote]** oder die Pfeile für die Inhaltskomponenten verwenden.

![](assets/deliver-offer-preview.png)

Gehen Sie wie folgt vor, um die verschiedenen Angebote anzuzeigen, die Teil der Entscheidung bei einem Kundenprofil sind.

1. Wählen Sie die Testprofile aus, die für die Angebotsvorschau verwendet werden sollen:

   1. Klicken Sie auf die **[!UICONTROL Schaltfläche „Inhalt simulieren“]** und wählen Sie dann den Namespace, der zur Identifizierung von Testprofilen verwendet werden soll, aus dem **[!UICONTROL Identity-Namespace]**-Feld aus.

      >[!NOTE]
      >
      >In diesem Beispiel verwenden wir den Namespace **E-Mail**. Weitere Informationen zu den Identity-Namespaces der Adobe Experience Platform finden Sie [in diesem Abschnitt](../audience/get-started-identity.md).

   1. Geben Sie im Feld **[!UICONTROL Identitätswert]** den Wert ein, der das Testprofil identifiziert . Geben Sie in diesem Beispiel die E-Mail-Adresse eines Testprofils ein.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. Fügen Sie weitere Profile hinzu, damit Sie je nach den Profildaten verschiedene Varianten der Nachricht testen können.

      ![](assets/deliver-offer-test-profiles.png)

1. Klicken Sie auf **[!UICONTROL Vorschau]** zum Testen der Nachricht und zur Auswahl eines Testprofils. Das Angebot, das dem ausgewählten Profil (Frau) entspricht, wird angezeigt.

   ![](assets/deliver-offer-test-profile-female-preview.png)

   Wählen Sie für jede Nachrichtenvariante weitere Testprofile aus, um die Vorschau des E-Mail-Inhalts anzuzeigen. Im Nachrichteninhalt wird nun das Angebot angezeigt, das dem ausgewählten Testprofil (jetzt ein Mann) entspricht.

Weitere Informationen zu den detaillierten Schritten zur Überprüfung der Nachrichtenvorschau finden Sie in [diesem Abschnitt](#preview-your-messages).

## Anleitungsvideo{#video-offers}

Erfahren Sie, wie Sie in [!DNL Journey Optimizer] eine Entscheidungs-Management-Komponente zu Nachrichten hinzufügen.

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
