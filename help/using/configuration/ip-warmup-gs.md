---
solution: Journey Optimizer
product: journey optimizer
title: Erste Schritte mit IP-Aufwärmeplänen
description: Erfahren Sie, wie Sie einen IP-Warmup-Plan implementieren
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, Pools, Gruppe, Subdomains, Zustellbarkeit
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 33%

---

# Erste Schritte mit IP-Aufwärmeplänen {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Inhalt dieses Dokumentationshandbuchs:

* **[Erste Schritte mit IP-Wärme](ip-warmup-gs.md)**
* [Erstellen von IP-Aufwärmekampagnen](ip-warmup-campaign.md)
* [Erstellen eines IP-Warmup-Plans](ip-warmup-plan.md)
* [IP-Warmup-Plan ausführen](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Die IP-Warmup-Funktion ist derzeit nur als Beta-Version für ausgewählte Benutzer verfügbar. Wenden Sie sich an die Kundenunterstützung von Adobe, um am Beta-Programm teilzunehmen.

Mit [!DNL Journey Optimizer]können Sie IP-Warmup-Workflows einfach direkt über die Benutzeroberfläche auf standardisierte und effiziente Weise durchführen, die den Best Practices für eine optimale Zustellbarkeit entspricht.

>[!CAUTION]
>
>Diese Funktion ist nur für den E-Mail-Kanal verfügbar.

Wenn E-Mails über eine neue Plattform versendet werden, sind ISPs normalerweise misstrauisch gegenüber den neuen IP-Adressen. Das plötzliche Versenden großer Mengen an E-Mails veranlasst ISPs oft dazu, sie als Spam zu qualifizieren.

Um zu vermeiden, als Spam gekennzeichnet zu werden, können Sie das gesendete Volumen mithilfe der Funktion IP-Warmup Plan schrittweise erhöhen. Eine neue Option im **[!UICONTROL Administration]** bietet Ihnen die Möglichkeit, die Arbeit reibungsloser zu gestalten, anstatt komplexe tägliche Journey zu erstellen. Dies gewährleistet eine reibungslose Anlaufphase, da die Gesamtrate ungültiger Adressen verringert wird.

>[!NOTE]
>
>Erfahren Sie mehr über die Verbesserung der Reputation Ihrer E-Mail mit IP-Warming im [Best Practices für die Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=de).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Die wichtigsten Schritte zur Implementierung eines IP-Warmup-Plans sind:

1. Zunächst müssen Sie eine oder mehrere Kampagnen mit aktivierter IP-Warmup-Option erstellen. [Weitere Informationen](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. Erstellen Sie einen IP-Warmup-Plan und laden Sie Ihren Plan hoch. [Weitere Informationen](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. Passen Sie jede Phase Ihres Plans an und aktivieren Sie die Läufe. [Weitere Informationen](ip-warmup-running.md)
