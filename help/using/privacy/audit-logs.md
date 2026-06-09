---
solution: Journey Optimizer
product: journey optimizer
title: Audit-Aktionen für Journey Optimizer-Ressourcen
description: Erfahren Sie, wie Sie Aktionen verfolgen, die für Journey Optimizer-Ressourcen durchgeführt wurden.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 06565328f42ff79943f774df55d8e41118b40815
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 97%

---

# Audit-Aktionen für Journey Optimizer-Ressourcen {#track-changes}

## Über Auditprotokolle {#audit-logs}

>[!IMPORTANT]
>
>Zum Anzeigen und Exportieren des Auditprotokolls benötigen Sie die Genehmigung **[!DNL View User Activity Log]**. [Weitere Informationen](../administration/ootb-product-profiles.md)

Mit Journey Optimizer können Sie die von den Nutzern im System durchgeführten Aktionen für verschiedene Services und Funktionen wie Journeys, Nachrichten, Landingpages usw. ermitteln.

So können Sie die Sichtbarkeit der im System durchgeführten Aktivitäten erhöhen, Probleme beheben und Ihr Unternehmen bei der Einhaltung von Vorschriften und Unternehmensrichtlinien zur Datenverwaltung unterstützen.

Jede Aktion wird mit Metadaten in „Auditprotokollen“ aufgezeichnet, die in Adobe Experience Platform zugänglich sind. Weiterführende Informationen zu Auditprotokollen, einschließlich ihrer Anzeige und Verwaltung in der Benutzeroberfläche oder API, finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=de).

![](assets/audit-logs.png)

## Von Auditprotokollen erfasste Ereignistypen {#events}

In der folgenden Tabelle sind die Aktionen aufgeführt, für die Journey Optimizer-Ressourcen in Auditprotokollen aufgezeichnet werden. Die vollständige Liste der in den Auditprotokollen erfassten Aktionen finden Sie in der [Dokumentation zu Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=de#category).

>[!NOTE]
>
>Auditprotokolle zum **Entscheidungs-Management** sind nur in der CSV-Datei sichtbar, die mit der Schaltfläche **[!UICONTROL Protokoll herunterladen]** heruntergeladen werden kann.

| Ressource | Aktion |
|-----------|------------------|
| AJO-Kampagne | Erstellen/Löschen/Aktualisieren/Aktivieren/Stoppen |
| Allgemeine Einstellungen für den AJO-Kanal | Erstellen/Löschen/Aktualisieren |
| AJO-IP-Pool | Erstellen/Löschen/Aktualisieren |
| AJO-Landingpage | Erstellen/Löschen/Aktualisieren/Veröffentlichen/Veröffentlichung aufheben |
| AJO-Landingpage-HTML-Vorlage | Erstellen/Löschen/Aktualisieren |
| AJO-Landingpage-Voreinstellung | Erstellen/Löschen/Aktualisieren |
| AJO-Landingpage-Subdomain | Erstellen/Löschen/Aktualisieren |
| AJO-Nachrichtenvoreinstellung | Erstellen/Löschen/Aktualisieren |
| AJO-PTR-Eintrag | Erstellen/Löschen/Aktualisieren |
| AJO-Vorlage für gespeicherte Ausdrücke | Erstellen/Löschen/Aktualisieren |
| Anmeldedaten der AJO-SMS-API | Erstellen/Löschen/Aktualisieren |
| AJO-Subdomain | Erstellen/Löschen/Aktualisieren |
| AJO-Unterdrückungsliste | Erstellen/Löschen/Herunterladen der CSV |
| Feldergruppe | Erstellen/Löschen/Aktualisieren |
| Journey | Erstellen/Löschen/Aktualisieren/Stoppen/Veröffentlichen |
| Benutzerdefinierte Aktion in Journey | Erstellen/Löschen/Aktualisieren |
| Journey-Datenquelle | Erstellen/Löschen/Aktualisieren |
| Journey-Ereignis | Erstellen/Löschen/Aktualisieren |
| Journey-Fragment | Erstellen/Löschen/Aktualisieren/Aktivieren/Archivieren |
| Häufigkeitsregeln für Nachrichten | Erstellen/Löschen/Aktualisieren |
| Rangfolgestrategie | Erstellen/Löschen/Aktualisieren |
