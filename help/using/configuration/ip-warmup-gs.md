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
hide: true
hidefromtoc: true
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: ht
source-wordcount: '275'
ht-degree: 100%

---

# Erste Schritte mit IP-Aufwärmplänen {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* **[Erste Schritte beim IP-Aufwärmen](ip-warmup-gs.md)**
* [Erstellen von IP-Aufwärmkampagnen](ip-warmup-campaign.md)
* [Erstellen eines IP-Aufwärmplans](ip-warmup-plan.md)
* [Ausführen des IP-Aufwärmplans](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Die IP-Aufwärmfunktion ist derzeit nur als Beta-Version für ausgewählte Benutzerinnen und Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Mit [!DNL Journey Optimizer] können Sie IP-Warmup-Workflows direkt von der Benutzeroberfläche aus auf standardisierte und effiziente Weise durchführen, die den Best Practices für optimale Zustellbarkeit folgt.

>[!CAUTION]
>
>Diese Funktion ist nur für den E-Mail-Kanal verfügbar.

Wenn E-Mails über eine neue Plattform versendet werden, sind ISPs normalerweise misstrauisch gegenüber den neuen IP-Adressen. Das plötzliche Versenden großer Mengen an E-Mails veranlasst ISPs oft dazu, sie als Spam zu qualifizieren.

Um eine Einordnung als Spam zu vermeiden, können Sie das Sendevolumen mithilfe der IP-Aufwärmplan-Funktion schrittweise erhöhen. Mit dieser neuen Option im Menü **[!UICONTROL Administration]** können Sie dies einfach und konsolidiert tun, anstatt komplexe tägliche Journeys zu erstellen.

>[!NOTE]
>
>Im [Handbuch zu Best Practices bei der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de) finden sich Informationen dazu, wie die E-Mail-Reputation mit einer IP-Aufwärmung verbessert werden kann.

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
