---
solution: Journey Optimizer
product: journey optimizer
title: Überlegungen zu Adobe Experience Manager-Inhaltsfragmenten und Fehlerbehebung
description: Überlegungen und häufige Probleme für AEM-Inhaltsfragmente in Journey Optimizer.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Überlegungen und Fehlerbehebung {#aem-fragments-limitations}

## Wichtige Aspekte {#considerations}

Beachten Sie Folgendes bei der Verwendung von Inhaltsfragmenten aus [!DNL Adobe Experience Manager] in [!DNL Journey Optimizer]:

* **Inhaltsfragmenttypen**
   * Einfache Inhaltsfragmente, verschachtelte Inhaltsfragmente und **Varianten von Inhaltsfragmenten** werden unterstützt. Wählen Sie die Variante aus, wenn Sie das Fragment in [!DNL Journey Optimizer] einfügen. Wenn Sie keine Variante auswählen, wird die Variante **Main** (der primäre Inhalt des Fragments in [!DNL Adobe Experience Manager]) verwendet.

* **Mehrsprachige Inhalte**
   * Jede Variante muss in [!DNL Adobe Experience Manager] erstellt, getaggt und veröffentlicht werden. Wählen Sie in [!DNL Journey Optimizer] die Fragmentvariante aus, die jeder Nachrichtensprache oder jedem Gebietsschema entspricht.
   * Es gibt keine automatische Sprachauflösung oder Fallback zwischen Varianten.

* **Repository-Zugriff**
   * [!DNL Journey Optimizer] lässt sich nur mit der [!DNL Adobe Experience Manager] **Veröffentlichungsebene** integrieren (Sites, Inhaltsfragmente). Inhaltsfragmente sind über einen öffentlichen, nicht authentifizierten Endpunkt verfügbar.
   * Autoren-Repositorys werden möglicherweise im Repository-Selektor angezeigt, aber in **können nur in** Publish[!DNL Journey Optimizer] veröffentlichte Fragmente verwendet werden.

* **Inhaltsfragmentstatus**
   * Fragmente können den Status **[!UICONTROL Veröffentlicht]** oder **[!UICONTROL Geändert]** aufweisen. [!DNL Journey Optimizer] wird immer die **zuletzt veröffentlichte Version** verwendet.
   * Nach der Veröffentlichung vorgenommene Änderungen werden erst dann in [!DNL Journey Optimizer] übernommen, wenn das Fragment erneut in [!DNL Adobe Experience Manager] veröffentlicht wurde. Es gibt keine automatische Versionsabstimmung zwischen den beiden Produkten.

* **Personalisierung**
   * Unterstützt: Profilattribute, kontextuelle Attribute, statische Zeichenfolgen und vordeklarierte Variablen.
   * Nicht unterstützt: abgeleitete oder berechnete Attribute.

* **Aktualisierungen und Versionierung**
   * Für Aktualisierungen ist eine manuelle Neuveröffentlichung durch [!DNL Adobe Experience Manager] erforderlich. Es gibt keine automatische Versionsabstimmung.
   * Wenn ein Inhaltsfragment in [!DNL Adobe Experience Manager] veröffentlicht oder erneut veröffentlicht wird, aktualisiert [!DNL Journey Optimizer] dieses Fragment und aktualisiert **alle Varianten dieses Fragments, auf die verwiesen wird** in aktiven Kampagnen oder Journey.
   * Die [!DNL Adobe Experience Manager] [Veröffentlichungsaktion](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) kann verzögert werden. Nach Abschluss des Vorgangs erhält [!DNL Journey Optimizer] ein Ereignis und aktualisiert den Inhalt.
   * Nach einer erfolgreichen Aktualisierung sind Änderungen normalerweise innerhalb von etwa **5 Minuten** für unitäre Journey und im **nächsten Batch** für Batch-Anwendungsfälle verfügbar.

* **Caching und Proofing**
   * Wenn ein Fragment zum ersten Mal zu einer Kampagne oder einem Journey hinzugefügt wird, speichert [!DNL Journey Optimizer] es im Zwischenspeicher. Wenn Sie ein Fragment auswählen, das bereits an anderer Stelle über **[!UICONTROL Open AEM CF selector]** verwendet wurde, wird es aus dem [!DNL Journey Optimizer]-Cache geladen.
   * Nachdem Sie ein geändertes Fragment in [!DNL Adobe Experience Manager] erneut veröffentlicht haben, überwacht [!DNL Journey Optimizer] das Ereignis und aktualisiert den Cache.
   * Korrekturabzüge spiegeln immer die **zuletzt veröffentlichte** Version wider. Für das Proofing kann keine historische Version gesperrt werden.

## Fehlerbehebung {#troubleshooting}

Wenn beim Arbeiten mit Adobe Experience Manager-Inhaltsfragmenten in Journey Optimizer Probleme auftreten, lesen Sie die folgenden häufigen Probleme und Lösungen:

| Problem | Ursache | Lösung |
|-|-|-|
| **Tag nicht gefunden** oder **Inhaltsfragment nicht in Selektor sichtbar** | Adobe Experience Manager-Tag-Syntax stimmt nicht mit dem erforderlichen `ajo-enabled:{OrgId}/{SandboxName}` überein | Überprüfen Sie, ob die Tag-ID die richtige **Organisations-ID** und **Sandbox-Name** verwendet. Stellen Sie sicher, dass keine Leerzeichen oder falschen Trennzeichen vorhanden sind. Veröffentlichen Sie das Inhaltsfragment nach der Korrektur des Tags erneut. |
| **Inhaltsfragment wird nicht in der Liste angezeigt** | Inhaltsfragment befindet sich im Entwurfsstatus oder ist nicht veröffentlicht | In der Journey Optimizer-Auswahl werden nur genehmigte und veröffentlichte Inhaltsfragmente angezeigt. Veröffentlichen Sie das Inhaltsfragment in Adobe Experience Manager und stellen Sie sicher, dass es den Status Veröffentlicht hat. |
| **Undefinierter Variablenfehler** | Personalization-Platzhalter nicht im Fragment-Helper-Tag deklariert | Fügen Sie alle erforderlichen Parameter zum Fragment-Helper-Tag hinzu. Jeder im Inhaltsfragment verwendete Platzhalter muss explizit mit seiner Zuordnung deklariert werden. |
| **Korrekturabzug zeigt unerwartete Inhalte an** | Der Korrekturabzug verwendet die neueste veröffentlichte Version von Adobe Experience Manager | Korrekturabzüge spiegeln immer die neueste Veröffentlichung des Inhaltsfragments in Adobe Experience Manager wider. Wenn Sie die letzten Änderungen in Adobe Experience Manager vorgenommen haben, veröffentlichen Sie das Fragment erneut und aktualisieren Sie den Korrekturabzug. |
| **Fehler: Zugriff verweigert (CPES)** | Benutzerrolle ist nicht berechtigt, auf bestimmte Attribute zuzugreifen | Wenden Sie sich an Ihren Systemadministrator, um sicherzustellen, dass Ihre Rolle über die entsprechenden Berechtigungen für das Profil oder die kontextuellen Attribute verfügt, die bei der Personalisierung verwendet werden. |
| **Fragment zeigt leere oder fehlende Inhalte an** | Fehlende erforderliche Personalisierungsparameter oder Fallback-Werte | Stellen Sie sicher, dass alle erforderlichen Parameter bereitgestellt werden, und erwägen Sie, Fallback-Werte für optionale Attribute hinzuzufügen. |
| **Bild wird nicht gerendert oder scheint beschädigt zu sein** | Bild-URL im Inhaltsfragment ist ein relativer Pfad oder vom Kanal nicht erreichbar | Verwenden Sie **absolute** URLs (`https://...`) für Bildfelder. Relative Pfade von Adobe Experience Manager werden nicht unterstützt. Bestätigen Sie die URL in einem Browser oder in der Nachrichtenvorschau. |
| **Experience League AEM-Link gibt 404 zurück** | Veraltetes Lesezeichen, Vorschau-Build oder unveröffentlichte AEM-Hilfeseite | Öffnen Sie [&#x200B; Thema „Inhaltsfragmente mit Adobe Journey Optimizer](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} in der Live Experience Manager-Dokumentation und navigieren Sie zum Inhaltsverzeichnis auf der Seite, oder suchen Sie nach dem Abschnittsnamen (z. B. **Dispatcher-Konfiguration**). |

Wenn das Problem weiterhin besteht, wenden Sie sich mit Details zu Ihrer Inhaltsfragment-ID, der Kampagnen- oder Journey-ID und allen angezeigten Fehlermeldungen an den Adobe-Support.
