---
solution: Journey Optimizer
product: journey optimizer
title: Steigern der Versandaktivität
description: Hier erfahren Sie, wie Sie Ihre Versandaktivität steigern können.
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: Zustellbarkeit, Journey, Anwendungsfall, E-Mail, Reputation
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 82%

---

# Anwendungsfall: Steigern der Versandaktivität{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie Sie mit der Aktivität „Optimieren“ und einer Profilbegrenzung eine Journey erstellen, die Ihre E-Mail-Sendungen schrittweise beschleunigt, sodass Sie eine neue IP-Adresse aufwärmen und Ihre Reputation als Absender aufbauen können.

>[!ENDSHADEBOX]

Wenn Sie kürzlich Ihren E-Mail-Dienstleister, Ihre IP-Adresse, Ihre E-Mail-Domain oder Ihre Subdomain gewechselt haben, müssen Sie erst Ihre Reputation als Absender aufbauen. Andernfalls könnten Ihre Sendungen blockiert oder in den Spam-Ordner des Postfachs der Empfänger verschoben werden. Im [Handbuch zu Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de){target="_blank"} finden sich Informationen dazu, wie die E-Mail-Reputation mit IP-Warming verbessert werden kann.

Um die Reputation Ihrer IP-Adresse zu verbessern, können Sie die Anzahl Ihrer Sendungen schrittweise erhöhen. Mehr dazu erfahren Sie unter [Zustellbarkeit in Journey Optimizer optimieren](../reports/deliverability.md).

In diesem Anwendungsbeispiel wird eine Journey erstellt, um die Versandaktivität Ihrer E-Mails zu steigern. Gehen Sie wie folgt vor, um diese Journey zu konfigurieren:

1. Erstellen Sie eine Journey. [Weitere Informationen](journey-gs.md).

1. Fügen Sie **[!UICONTROL Journey]** Aktivität „Optimieren“ hinzu. [Weitere Informationen](optimize.md).

1. Legen Sie in den Einstellungen für die Aktivität **[!UICONTROL Bedingung]** die maximale Empfängeranzahl für Ihren Versand fest:

   1. Wählen Sie in **[!UICONTROL Aktivitätseinstellungen]** Optimieren) die Methode **[!UICONTROL Bedingungen]** und setzen Sie das Feld **[!UICONTROL Typ]** auf **[!UICONTROL Profilbegrenzung]**. [Weitere Informationen](conditions.md#profile_cap).

   1. Legen Sie das Feld **[!UICONTROL Limit]** auf die maximale Anzahl an Empfängern für diesen Versand fest.

   ![Konfiguration der Profilbegrenzungsbedingung zur Steuerung des Versandvolumens](assets/profile-cap-condition.png)

   Sie können dieses Limit schrittweise auf die Gesamtzahl Ihrer Abonnenten erhöhen.

1. Fügen Sie im nominalen Pfad nach der Aktivität **[!UICONTROL Bedingung]** die Aktionsaktivität **[!UICONTROL E-Mail]** hinzu.

   ![Konfiguration von E-Mail-Nachrichten in einer gesteigerten Versand-Journey](assets/ramp-up-deliveries-message.png)

   Wenn die Journey ausgeführt wird, wird die Nachricht bis zu der von Ihnen angegebenen Höchstzahl an Profilen an die eingehenden Profile gesendet. Wenn dieses Limit erreicht ist, nehmen die eingehenden Profile den alternativen Pfad.

1. Vervollständigen Sie die Journey mit den Aktivitäten Ihrer Wahl.

Nach dem Aufwärmen Ihrer IP können Sie diese Bedingung entfernen.
