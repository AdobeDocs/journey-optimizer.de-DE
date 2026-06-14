---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit IP-Aufwärmplänen
description: Informationen zur Implementierung eines IP-Aufwärmplans
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, Zustellbarkeit
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
TQID: https://experienceleague.adobe.com/xjJKrCXUmQY5sZu2w-B09agQh-tb4qkSXM0Vh2-TDnc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 93%

---

# Erste Schritte mit IP-Aufwärmplänen {#ip-warmup-gs}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie, wie IP-Aufwärmpläne Ihnen dabei helfen, das Versandvolumen schrittweise zu erhöhen, um die Reputation der Absender aufzubauen, und lernen Sie die wichtigsten Schritte zur Implementierung eines Pfades in Adobe Journey Optimizer kennen.

>[!ENDSHADEBOX]

Mit [!DNL Journey Optimizer] können Sie IP-Warmup-Workflows direkt von der Benutzeroberfläche aus auf standardisierte und effiziente Weise durchführen, die den Best Practices für optimale Zustellbarkeit folgt. Wenn E-Mails über eine neue Plattform versendet werden, sind ISPs normalerweise misstrauisch gegenüber den neuen IP-Adressen. Das plötzliche Versenden großer Mengen an E-Mails veranlasst ISPs oft dazu, sie als Spam zu qualifizieren.

Um eine Einordnung als Spam zu vermeiden, können Sie das Sendevolumen mithilfe der IP-Aufwärmplan-Funktion schrittweise erhöhen. Diese neue Option im Menü **[!UICONTROL Administration]** ermöglicht Ihnen die Automatisierung der Volume-Verwaltung und vereinfacht den Aufwärmvorgang, ohne dass komplexe Journey-Konfigurationen erforderlich sind.

>[!NOTE]
>
>Bevor Sie Ihren IP-Aufwärmplan implementieren, informieren Sie sich in diesem [Leitfaden zur IP-Aufwärm-Zustellbarkeit](ip-warmup-deliverability-guide.md) über die Grundlagen der Zustellbarkeit, die Reputationsbildung und Best Practices.

➡️ [Informationen zum Erstellen und Ausführen eines IP-Aufwärmplans finden Sie in diesem Video](#video)

>[!AVAILABILITY]
>
>Diese Funktion kann nur für Sandboxes vom Typ „Produktion“ aktiviert werden.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Die wichtigsten Schritte zur Implementierung eines IP-Aufwärmplans sind:

1. Zunächst müssen Sie eine oder mehrere Kampagnen mit aktivierter IP-Aufwärmoption erstellen. [Weitere Informationen](ip-warmup-campaign.md)

1. Erstellen Sie einen IP-Aufwärmplan in [!DNL Journey Optimizer] und laden Sie die Excel-Tabelle hoch, die mithilfe der Person, die Sie im Hinblick auf die Zustellbarkeit berät, erstellt wurde. [Weitere Informationen](ip-warmup-plan.md)

1. Wählen Sie für jede Phase Ihres Plans eine Kampagne aus und aktivieren Sie die entsprechenden Ausführungen. [Weitere Informationen](ip-warmup-execution.md)

## Anleitungsvideo {#video}

Erfahren Sie, wie Sie einen IP-Aufwärmplan erstellen und ausführen.

>[!VIDEO](https://video.tv.adobe.com/v/3453849/?captions=ger&learn=on)

>[!NOTE]
>
>Im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de) finden sich Informationen dazu, wie Ihre E-Mail-Reputation mit einer IP-Aufwärmung verbessert werden kann.

## Zusätzliche Ressourcen {#additional-resources}

In diesen hilfreichen Blog-Beiträgen erhalten Sie eine ausführlichere Anleitung zur IP-Aufwärmung:

* [Adobe Journey Optimizer Deliverability Guide: From Zero Reputation to Inbox Hero](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=de) – Umfassendes Handbuch zu den Grundlagen der Reputation, Aufwärmkalendern, Überwachung und Best Practices zur Fehlerbehebung.

* [Understanding how to set up the IP warmup](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949?profile.language=de) – Erfahren Sie mehr über die Grundlagen zum Einrichten von IP-Aufwärmplänen und Best Practices für eine erfolgreiche Implementierung.

* [Advanced features in IP warm-up plans](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958?profile.language=de) – Entdecken Sie erweiterte Funktionen und granulare Steuerelemente zur Optimierung Ihrer IP-Aufwärmstrategie.

* [IP warm-up troubleshooting](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952?profile.language=de) – Finden Sie Lösungen für häufige Probleme wie Zielgruppenverzögerungen und erfahren Sie mehr über intelligente Wiederholungsmechanismen.
