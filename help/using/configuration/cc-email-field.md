---
solution: Journey Optimizer
product: journey optimizer
title: CC (Carbon Copy) bei der Konfiguration von E-Mail-Kanälen
description: Konfigurieren Sie sichtbare CC-Empfänger im Journey Optimizer-E-Mail-Kanal. Erfahren Sie, wie Sie das CC-Feld festlegen, wie es sich von BCC unterscheidet und welche Einschränkungen es gibt.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: CC, Kopie, E-Mail, Kanalkonfiguration, E-Mail-Kopfzeilen, BCC
badge: label="Eingeschränkte Verfügbarkeit" type="Informative"
source-git-commit: 5b804de873124b8ff53d55c943b3c95649dd9a7c
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 7%

---

# Hinzufügen eines CC-Felds zu E-Mails {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="Definieren einer CC-E-Mail-Adresse"
>abstract="Sie können ein sichtbares CC-Feld (Carbon Copy) zu E-Mails hinzufügen, die mit dieser Kanalkonfiguration gesendet werden. Geben Sie eine feste E-Mail-Adresse ein oder verwenden Sie eine Personalisierung (Profilattribut oder Kontextvariable). Beachten Sie, dass die CC-Nutzung auf das für Sie festgelegte Nachrichtenvolumen angerechnet wird."

>[!AVAILABILITY]
>
>Diese Funktion ist für alle Kunden mit eingeschränkter Verfügbarkeit verfügbar. Wenden Sie sich an den Adobe-Support, um Zugriff zu erhalten.

Sie können ein sichtbares CC-Feld (Carbon Copy) zu E-Mails hinzufügen, die von [!DNL Journey Optimizer] über Ihre Journey und Kampagnen gesendet werden. Diese optionale Funktion wird auf [Kanalkonfigurationsebene](channel-surfaces.md) zusammen mit den E-Mail-Kopfzeilenparametern und der BCC-E-Mail-Option konfiguriert.

>[!CAUTION]
>
>Die Nutzung der CC-Funktion wird auf die Anzahl der Nachrichten angerechnet, für die Sie lizenziert sind. Aktivieren Sie sie nur dort, wo Sie sichtbare CC-Empfänger benötigen. Prüfen Sie Ihren Vertrag auf das Lizenzvolumen.

Wie [BCC](archiving-support.md#bcc-email) soll das Feld CC eine Kopie der E-Mail an eine zusätzliche Adresse senden. Sie unterscheidet sich jedoch von BCC wie folgt:

* Die CC-E-Mail-Adresse ist für den primären Empfänger sichtbar, sodass dieser sehen kann, wer kopiert wurde, und weiß, an wen er sich zwecks Nachbereitung wenden soll.
* Im Gegensatz zu BCC unterstützt das CC-E-Mail-Feld die Personalisierung, die es Ihnen ermöglicht, eine Kanalkonfiguration für viele Szenarien zu verwenden und die Kopie an die richtige Person pro Empfänger zu senden (z. B. ihren Beziehungs-Manager). Bei von einer API ausgelösten Kampagnen können Sie damit die Adresse kopieren, die für ein bestimmtes Ereignis oder eine bestimmte Transaktion relevant ist.

>[!NOTE]
>
>Wenn Sie Kopien aufbewahren müssen, bei denen die Adresse für die Archivierung oder Compliance für den Empfänger nicht sichtbar sein darf, verwenden Sie [BCC](archiving-support.md#bcc-email) anstelle von CC.

## CC-E-Mail aktivieren {#enable-cc}

Um die Option **[!UICONTROL CC-E]** zu aktivieren, konfigurieren Sie das Feld CC in der Konfiguration [E-Mail-Kanals](../email/email-settings.md).

![](assets/email-config-cc.png)

Sie können eine beliebige externe Adresse im korrekten Format angeben, mit Ausnahme einer E-Mail-Adresse, die in der Adobe zugewiesenen Subdomain definiert ist. Wenn Sie zum Beispiel die Subdomain *marketing.luma.com* an Adobe delegiert haben, ist jede Adresse des Typs *abc@marketing.luma.com* verboten.

>[!CAUTION]
>
>Sie können nur eine E-Mail-Adresse definieren. Stellen Sie sicher, dass die CC-Adresse über genügend Aufnahmekapazität verfügt, um alle E-Mails zu speichern, die mit der aktuellen Kanalkonfiguration gesendet werden.
>
>Weitere Empfehlungen finden Sie in [diesem Abschnitt](#cc-recommendations-limitations).

Das **[!UICONTROL CC email]**-Feld akzeptiert drei Werttypen:

* Ein **hartcodierter Wert** der eine feste E-Mail-Adresse sein kann.

* Ein **Profilattribut**, z. B. die im Profil verfügbare E-Mail-Adresse von Relationship Manager.

* Ein **kontextuelles Attribut** - dieser Wert kann **nur in API-ausgelösten Kampagnen verwendet werden**. Sie wird aus der API-Payload abgerufen, die die mit dem CC-Adresswert `context.channel.email.ccvalues` Kontextvariable enthalten muss.

  >[!WARNING]
  >
  >Wenn CC mithilfe einer **Kontextvariablen“ festgelegt**, wird dies nur in **API-ausgelösten Kampagnen** unterstützt. Wenn Sie diese Kanalkonfiguration auf einer Journey oder in einer Aktionskampagne verwenden, wird die E-Mail nur an den primären Empfänger gesendet, keine Kopie an die CC-Adresse.

Jeder [Anhang](../email/pdf-attachments.md) der Nachricht wird sowohl an den primären Empfänger als auch an die CC-Adresse gesendet.

Wenn der CC-Wert zum Zeitpunkt des Versands ungültig ist oder fehlt (z. B. eine leere Kontextvariable), wird die CC-Kopie übersprungen; der primäre Empfänger erhält weiterhin die E-Mail.

Wenn für das CC-Feld mehrere Werte vorhanden sind (z. B. bei Verwendung eines Profilattributs oder Ausdrucks, das bzw. der in mehrere Adressen aufgelöst wird), wird nur der erste Wert für den Versand der E-Mail verwendet.

## CC-E-Mail in vorhandenen Kanalkonfigurationen bearbeiten {#cc-edit}

Wenn Sie [E-Mail-Konfiguration bearbeiten](channel-surfaces.md#edit-channel-surface) und das CC-Feld hinzufügen oder ändern, können Sie nur Folgendes verwenden:

* eine **hartcodierte** CC-E-Mail-Adresse oder
* Eine **Kontextvariable** (für API-ausgelöste Verwendung).

>[!CAUTION]
>
>Beim Bearbeiten einer vorhandenen E-Mail-Kanal-Konfiguration können Sie keine neuen [Profilattribute](../personalization/personalization-build-expressions.md#sources) zum Feld **[!UICONTROL CC-E-Mail]** hinzufügen. Sie müssen eine [neue Kanalkonfiguration“ &#x200B;](channel-surfaces.md#create-channel-surface).

## Empfehlungen und Einschränkungen {#cc-recommendations-limitations}

* **Berechtigung:** CC-Nutzung wird auf das für Sie berechtigte Nachrichtenvolumen angerechnet. Verwenden Sie CC nur, wenn Sie sichtbare CC-Empfänger benötigen. Prüfen Sie Ihren Vertrag auf das Lizenzvolumen.

* **Datenschutz und Compliance:** Um die Einhaltung der Datenschutzbestimmungen sicherzustellen, müssen CC-E-Mails von einem System verarbeitet werden, das in der Lage ist, personenbezogene Daten (PII, Personally Identifiable Information) bei Bedarf sicher zu speichern. Da Nachrichten vertrauliche oder private Daten wie personenbezogene Daten enthalten können, müssen Sie sicherstellen, dass die CC-Adresse korrekt ist und der Zugriff auf Nachrichten gesichert ist.

* **Posteingangsverwaltung:** Ihr Posteingang, der für CC verwendet wird, sollte in Bezug auf Speicherplatz und Versand ordnungsgemäß verwaltet werden. Wenn der Posteingang Bounces zurückgibt, werden einige E-Mails möglicherweise nicht empfangen.

* **Versandzeitpunkt:** Nachrichten können vor den Zielgruppenempfängerinnen und -empfängern an die CC-E-Mail-Adresse gesendet werden. CC-Nachrichten können auch dann gesendet werden, wenn es bei den ursprünglichen Nachrichten zu einem „Bounce[&#x200B; gekommen &#x200B;](../reports/suppression-list.md#delivery-failures).

* **Reporting:** Öffnungen, Klicks und andere Interaktionen von CC-Empfängern sind in E-Mail-Reporting-Metriken enthalten. Öffnungen oder Klicks von CC-Empfängern führen daher zu falschen Berechnungen in [Berichten](../reports/report-gs-cja.md).

* **Spam:** Nachrichten im CC-Posteingang nicht als Spam kennzeichnen, da sich dies auf alle anderen an diese Adresse gesendeten E-Mails auswirken wird.

* **Zustellbarkeit:** Sie CC entsprechend Ihren Versandpraktiken und Empfängererwartungen. Übermäßige Nutzung von CC kann sich auf die Zustellbarkeit auswirken. Befolgen Sie [Best Practices für die Zustellbarkeit](../reports/deliverability.md) und Ihre Vertragsbedingungen.

>[!CAUTION]
>
>Klicken Sie nicht auf den Abmelde-Link in den an die CC-Adresse gesendeten E-Mails, da dadurch der **-Empfänger** E-Mail sofort abgemeldet wird.
