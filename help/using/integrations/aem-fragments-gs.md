---
solution: Journey Optimizer
product: journey optimizer
title: AEM-Inhaltsfragmente
description: Erfahren Sie, wie Sie auf AEM-Inhaltsfragmente zugreifen und diese verwalten
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 12%

---

# Erste Schritte mit Adobe Experience Manager-Inhaltsfragmenten {#aem-fragments}

Durch die Integration von Adobe Experience Manager as a Cloud Service mit Adobe Journey Optimizer können Sie jetzt Ihre AEM-Inhaltsfragmente nahtlos in Journey Optimizer in Ihre Inhalte integrieren. Diese optimierte Verbindung vereinfacht den Zugriff auf und die Nutzung von AEM-Inhalten und ermöglicht die Erstellung personalisierter und dynamischer Kampagnen und Journeys.

Weitere Informationen zu AEM-Inhaltsfragmenten finden Sie unter [Arbeiten mit Inhaltsfragmenten](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Dokumentation zu Experience Manager.

## Bevor Sie beginnen {#start}

>[!AVAILABILITY]
>
>Für Kundinnen und Kunden im Gesundheitswesen wird die Integration nur bei einer Lizenzierung der Add-on-Angebote Journey Optimizer Healthcare Shield und Adobe Experience Manager Enhanced Security aktiviert.

### Einschränkungen {#limitations}

Beachten Sie die folgenden Einschränkungen beim Arbeiten mit Adobe Experience Manager-Inhaltsfragmenten in Journey Optimizer:

* **Inhaltsfragmenttypen**: Einfache Inhaltsfragmente und verschachtelte Inhaltsfragmente werden unterstützt. Varianten von Inhaltsfragmenten werden derzeit nicht unterstützt.

* **Mehrsprachige Inhalte**: Es wird nur der manuelle Fluss unterstützt. Jede Sprachvariante muss unabhängig in Adobe Experience Manager erstellt, getaggt, veröffentlicht und manuell in Journey Optimizer ausgewählt werden. Es gibt keinen automatischen Sprachauflösungs- oder Ausweichmechanismus.

* **Repository-Zugriff**: Journey Optimizer lässt sich ausschließlich in die Adobe Experience Manager-Veröffentlichungsebene integrieren, auf der Inhaltsfragmente über einen öffentlichen, nicht authentifizierten Endpunkt verfügbar sind. Während Autoren-Repositorys möglicherweise im Repository-Selektor angezeigt werden, können in Journey Optimizer nur Inhaltsfragmente verwendet werden, die auf der Veröffentlichungsebene veröffentlicht wurden.

* **Inhaltsfragmentstatus**: Journey Optimizer zeigt Inhaltsfragmente mit dem Status **Veröffentlicht** und **Geändert** an. In allen Fällen wird nur die zuletzt veröffentlichte Version verwendet. Wenn ein Fragment nach der Veröffentlichung geändert wird, werden diese Änderungen erst dann in Journey Optimizer übernommen, wenn das Inhaltsfragment erneut in Adobe Experience Manager veröffentlicht wurde. Es gibt keine automatische Versionsabstimmung zwischen Adobe Experience Manager und Journey Optimizer.

* **Personalization**: Es werden nur Profilattribute, kontextuelle Attribute, statische Zeichenfolgen und vordeklarierte Variablen unterstützt. Abgeleitete oder berechnete Attribute werden nicht unterstützt.

* **Aktualisierungen und Versionierung**: Inhaltsfragmentaktualisierungen müssen von Adobe Experience Manager manuell erneut veröffentlicht werden. Es gibt keine automatische Versionsabstimmung zwischen Adobe Experience Manager und Journey Optimizer. Wenn ein Inhaltsfragment in Adobe Experience Manager veröffentlicht wird, erhält Journey Optimizer ein Ereignis und Aktualisierungen auf der Journey Optimizer-Seite. Bei Erfolg ist das Update nach 5 Minuten für unitäre Journey und im nächsten Batch für Batch-Anwendungsfälle verfügbar.

* **Caching und Proofing**: Inhaltsfragmente werden in Echtzeit aus der Adobe Experience Manager-Veröffentlichungsebene abgerufen. Es gibt keine Zwischenspeicherung vor dem Rendern oder der Momentaufnahme. Testsendungen für Kampagnen und Journey spiegeln immer die zuletzt veröffentlichte Version des Inhaltsfragments wider. Verlaufsversionen können nicht für das Proofing gesperrt werden.

* **Benutzerzugriff**: Es wird empfohlen, die Anzahl der Benutzer mit Zugriff auf die Veröffentlichung von Inhaltsfragmenten zu begrenzen, um das Risiko versehentlicher Fehler zu reduzieren.


### Lebenszyklus von Inhaltsfragmenten

![](assets/do-not-localize/AEM_CF.png)

Inhaltsfragmente folgen verschiedenen Lebenszyklusphasen, je nachdem, in welcher Adobe Experience Manager-Ebene sie vorhanden sind. [Weitere Informationen finden Sie in der Dokumentation zu Adobe Experience Manager](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Inhalte werden auf der **Autorenebene“ erstellt und verwaltet** wo Fragmente Status wie Neu, Entwurf, Veröffentlicht, Geändert oder Veröffentlichung rückgängig gemacht haben können. Diese Status gelten nur für die **Autorenebene** und unterstützen die Inhaltserstellung und -überprüfung.

Wenn ein Inhaltsfragment veröffentlicht wird, wird eine Kopie auf der **Veröffentlichungsebene** erstellt und über einen öffentlichen, nicht authentifizierten Endpunkt verfügbar gemacht. Journey Optimizer kann ausschließlich mit dieser **Veröffentlichungsebene“ integriert**.

Infolgedessen werden in Journey Optimizer nur veröffentlichte oder geänderte Inhaltsfragmente angezeigt und es wird immer die neueste veröffentlichte Version verwendet. Änderungen, die nach der Veröffentlichung vorgenommen werden, werden erst dann in Journey Optimizer übernommen, wenn das Inhaltsfragment erneut veröffentlicht wurde.


## Fehlerbehebung {#troubleshooting}

Wenn beim Arbeiten mit Adobe Experience Manager-Inhaltsfragmenten in Journey Optimizer Probleme auftreten, lesen Sie die folgenden häufigen Probleme und Lösungen:

| Problem | Ursache | Lösung |
|-|-|-|
| **Tag nicht gefunden** oder **Inhaltsfragment nicht in Selektor sichtbar** | Adobe Experience Manager-Tag-Syntax stimmt nicht mit dem erforderlichen `ajo-enabled:{OrgId}/{SandboxName}` überein | Überprüfen Sie, ob die Tag-ID die richtige **Organisations-ID** und **Sandbox-Name** verwendet. Stellen Sie sicher, dass keine Leerzeichen oder falschen Trennzeichen vorhanden sind. Veröffentlichen Sie das Inhaltsfragment nach der Korrektur des Tags erneut. |
| **Inhaltsfragment wird nicht in der Liste angezeigt** | Inhaltsfragment befindet sich im Entwurfsstatus oder ist nicht genehmigt | In der Journey Optimizer-Auswahl werden nur genehmigte und veröffentlichte Inhaltsfragmente angezeigt. Veröffentlichen Sie das Inhaltsfragment in Adobe Experience Manager und stellen Sie sicher, dass es den Status Genehmigt hat. |
| **Undefinierter Variablenfehler** | Personalization-Platzhalter nicht im Fragment-Helper-Tag deklariert | Fügen Sie alle erforderlichen Parameter zum Fragment-Helper-Tag hinzu. Jeder im Inhaltsfragment verwendete Platzhalter muss explizit mit seiner Zuordnung deklariert werden. |
| **Korrekturabzug zeigt unerwartete Inhalte an** | Der Korrekturabzug verwendet die neueste veröffentlichte Version von Adobe Experience Manager | Korrekturabzüge spiegeln immer die neueste Veröffentlichung des Inhaltsfragments in Adobe Experience Manager wider. Wenn Sie die letzten Änderungen in Adobe Experience Manager vorgenommen haben, veröffentlichen Sie das Fragment erneut und aktualisieren Sie den Korrekturabzug. |
| **Fehler: Zugriff verweigert (CPES)** | Benutzerrolle ist nicht berechtigt, auf bestimmte Attribute zuzugreifen | Wenden Sie sich an Ihren Systemadministrator, um sicherzustellen, dass Ihre Rolle über die entsprechenden Berechtigungen für das Profil oder die kontextuellen Attribute verfügt, die bei der Personalisierung verwendet werden. |
| **Fragment zeigt leere oder fehlende Inhalte an** | Fehlende erforderliche Personalisierungsparameter oder Fallback-Werte | Stellen Sie sicher, dass alle erforderlichen Parameter bereitgestellt werden, und erwägen Sie, Fallback-Werte für optionale Attribute hinzuzufügen. |

Wenn das Problem weiterhin besteht, wenden Sie sich mit Details zu Ihrer Inhaltsfragment-ID, der Kampagnen- oder Journey-ID und allen angezeigten Fehlermeldungen an den Adobe-Support.
