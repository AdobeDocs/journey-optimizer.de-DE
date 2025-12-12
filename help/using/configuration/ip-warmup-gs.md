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
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 57%

---

# Erste Schritte mit IP-Aufwärmplänen {#ip-warmup-gs}

Mit [!DNL Journey Optimizer] können Sie IP-Warmup-Workflows direkt von der Benutzeroberfläche aus auf standardisierte und effiziente Weise durchführen, die den Best Practices für optimale Zustellbarkeit folgt. Wenn E-Mails über eine neue Plattform versendet werden, sind ISPs normalerweise misstrauisch gegenüber den neuen IP-Adressen. Das plötzliche Versenden großer Mengen an E-Mails veranlasst ISPs oft dazu, sie als Spam zu qualifizieren.

Um eine Einordnung als Spam zu vermeiden, können Sie das Sendevolumen mithilfe der IP-Aufwärmplan-Funktion schrittweise erhöhen. Diese neue Option im Menü **[!UICONTROL Administration]** ermöglicht Ihnen die Automatisierung der Volume-Verwaltung und vereinfacht den Aufwärmvorgang, ohne dass komplexe Journey-Konfigurationen erforderlich sind.

>[!NOTE]
>
>Bevor Sie Ihren IP-Aufwärmplan implementieren, informieren Sie sich in diesem Leitfaden zur Zustellbarkeit von IP-[&#x200B; über die Grundlagen der Zustellbarkeit, die Reputationsbildung und Best Practices](ip-warmup-deliverability-guide.md).

➡️ [Erfahren Sie in diesem Video, wie Sie einen IP-Aufwärmplan erstellen und ausführen](#video)

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

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>Im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de) finden sich Informationen dazu, wie Ihre E-Mail-Reputation mit einer IP-Aufwärmung verbessert werden kann.

## Weitere Ressourcen {#additional-resources}

In diesen hilfreichen Blog-Beiträgen erhalten Sie eine ausführlichere Anleitung zur IP-Aufwärmung:

* [Handbuch zur Zustellbarkeit in Adobe Journey Optimizer: From Zero Reputation to Inbox Hero](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=de) - Umfassendes Handbuch zu den Grundlagen der Reputation, Aufwärmkalendern, Überwachung und Best Practices zur Fehlerbehebung.

* [Informationen zum Einrichten der IP-Aufwärmung](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949?profile.language=de) - Erfahren Sie mehr über die Grundlagen zum Einrichten von IP-Aufwärmplänen und Best Practices für eine erfolgreiche Implementierung.

* [Erweiterte Funktionen in IP-Aufwärmplänen](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958?profile.language=de) - Entdecken Sie erweiterte Funktionen und granulare Steuerelemente zur Optimierung Ihrer IP-Aufwärmstrategie.

* [Fehlerbehebung beim IP-Warm-up](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952?profile.language=de) - Finden Sie Lösungen für häufige Probleme wie Zielgruppenverzögerungen und erfahren Sie mehr über intelligente Wiederholungsmechanismen.
