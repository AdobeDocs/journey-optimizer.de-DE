---
solution: Journey Optimizer
product: journey optimizer
title: CNIL-Anleitung zu E-Mail-Tracking-Pixeln
description: Erfahren Sie mehr über die aktualisierten CNIL-Anleitungen zu E-Mail-Tracking-Pixeln und den Adobe Journey Optimizer-Steuerelementen, die Ihre Compliance-Bemühungen unterstützen können.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, Tracking, Pixel, E-Mail, Einverständnis, Opt-out, Datenschutz
source-git-commit: 66b0ca498ae2b39575ed57118739234d1f54c887
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 1%

---


# Grundlegendes zur aktualisierten CNIL-Anleitung zu E-Mail-Tracking-Pixeln {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie mehr über die CNIL-Empfehlung vom April 2026 zu E-Mail-Tracking-Pixeln und lernen Sie die Adobe Journey Optimizer-Steuerelemente kennen, die Sie zur Einhaltung von Vorschriften verwenden können: Umschalter für die Öffnungs-Tracking, Tracking auf Link-Ebene, Einverständnisverwaltung, Opt-out-Mechanismen und Unterdrückung.

>[!ENDSHADEBOX]

>[!NOTE]
>
>Diese Seite dient nur zu Informationszwecken. Es ist keine Rechtsberatung und garantiert nicht, dass Sie das geltende Recht einhalten. Die unten beschriebenen Adobe Journey Optimizer-Produktfunktionen sind Bausteine, die eine konforme Implementierung unterstützen können, wenn sie entsprechend konfiguriert und betrieben werden. Jeder Kunde ist dafür verantwortlich, seine Verpflichtungen nach geltendem Recht zu bestimmen und zu erfüllen.

## Überblick {#overview}

Am 14. April 2026 veröffentlichte die *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL), Frankreichs Datenschutzbehörde, eine [Empfehlung zur Verwendung von Tracking-Pixeln in E-Mails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). In der Anleitung wird klargestellt, wann eine Zustimmung erforderlich ist, und die Bedeutung ordnungsgemäßer Zustimmungspraktiken für das E-Mail-Pixel-Tracking hervorgehoben. Diese Richtlinie könnte sich auf die Versandpraktiken von Entitäten auswirken, die E-Mails an Abonnenten mit Sitz in Frankreich versenden.

CNIL räumte Unternehmen ab dem Datum der Empfehlung einen Zeitraum von drei Monaten ein, um ihre E-Mail-Empfänger („Benutzer„) über das Vorhandensein der Tracking-Pixel, ihren Zweck und das Recht der Benutzer auf Opt-out zu informieren. Während dieser Übergangsphase wird von den Kunden erwartet, dass sie die Benutzer über das Pixel-Tracking informieren und ihnen bei Bedarf ein Opt-out anbieten. **CNIL wird voraussichtlich nach dem 14. Juli 2026 mit Durchsetzungsmaßnahmen beginnen.**

Während CNIL und andere Regulierungsbehörden die Anleitungen zum Tracking von Pixeln und damit zusammenhängenden Problemen erläutern, wird Adobe weiterhin Aktualisierungen überwachen und Kunden über die technischen Funktionen von Adobe-Produkten informieren, die E-Mail-Marketing, einschließlich Adobe Journey Optimizer, unterstützen.

Adobe Journey Optimizer bietet Steuerelemente, mit denen Kunden das Öffnungs-Tracking auf Versandebene verwalten können. Kunden sind dafür verantwortlich, ihre eigenen Compliance-Verpflichtungen gemäß den geltenden CNIL-Richtlinien und anderen Gesetzen zu bestimmen, aber diese Funktionen können die Bemühungen um die Einhaltung von Kundenrichtlinien unterstützen.

## Was ist ein E-Mail-Tracking-Pixel? {#tracking-pixel}

Ein E-Mail-Tracking-Pixel ist ein 1 x 1 transparentes Bild, das in die HTML einer E-Mail eingebettet ist. Wenn der E-Mail-Client des Empfängers dieses Bild lädt, pingt das Pixel einen Server an, der Daten wie Zeitstempel, Gerätetyp, E-Mail-Client und manchmal eine IP-Adresse als ungefähren Speicherort aufzeichnet. Dieses Protokoll wird dann an den Datensatz eines Empfängers gebunden, sodass Marketing-Experten sehen können, ob eine E-Mail geöffnet wird.

## Kunden-Support {#support}

Kunden, die Unterstützung bei der Implementierung der oben beschriebenen Änderungen benötigen, können mit ihrem bestehenden Adobe-Ökosystem interagieren. Wenden Sie sich bei technischen Fragen zu den Funktionen von Adobe, auf die verwiesen wird, an Ihren Customer Success Manager oder technischen Kundenbetreuer.

## Adobe Journey Optimizer-Funktionen im Zusammenhang mit dem E-Mail-Tracking {#ajo-functionality}

Adobe Journey Optimizer bietet mehrere native Steuerelemente, mit denen Kunden auf Elemente der CNIL-Anleitung eingehen können. In den folgenden Abschnitten werden die relevanten Produktfunktionen beschrieben.

### E-Mail-Typklassifizierung {#email-type}

In Adobe Journey Optimizer wird jede E-Mail-Kanalkonfiguration entweder als Marketing oder als Transaktion klassifiziert. Diese Klassifizierung bestimmt, ob vor dem Senden die Einwilligung des Abonnenten erforderlich ist.

* **Marketing-E** Mails: Werbenachrichten werden an angemeldete Abonnenten gesendet. Das Einverständnis des Benutzers ist erforderlich. Diese E-Mails berücksichtigen automatisch die Voreinstellungen für Unterdrückung und Opt-out.
* **Transaktions-E** Mails: Nicht-kommerzielle Kommunikation (z. B. Bestellbestätigungen, Zurücksetzen des Passworts). Diese können vorbehaltlich des geltenden Rechts an Profile gesendet werden, die sich von Marketing-Nachrichten abgemeldet haben.

Der E-Mail-Typ wird auf der Ebene [Kanalkonfiguration](../email/email-settings.md#email-type) festgelegt. Beim Verfassen einer E-Mail auf einer Journey oder in einer Kampagne müssen die Autoren eine Kanalkonfiguration auswählen, deren E-Mail-Typ der Art der Kommunikation entspricht. Diese Klassifizierung informiert darüber, welche Einverständnisprüfungen vor dem Versand durchgeführt werden.

### Tracking-Steuerung öffnen {#open-tracking}

Adobe Journey Optimizer ermöglicht es Marketing-Experten, das Öffnungs-Tracking (d. h. das 1 x 1 Pixel) auf der Ebene der einzelnen Nachrichten zu steuern. Beim Erstellen einer E-Mail auf einer Journey oder in einer Kampagne stehen im Bedienfeld Nachrichteneigenschaften zwei Tracking-Optionen zur Verfügung:

* **[!UICONTROL Geöffnete E-Mails]**: Steuert, ob das Öffnungs-Tracking-Pixel in der E-Mail enthalten ist. Standardmäßig ist diese Option aktiviert.
* **[!UICONTROL Klick in E-Mail]**: Steuert, ob Link-Klicks verfolgt werden. Diese Option ist auch standardmäßig aktiviert.

Um das Öffnungs-Tracking für eine bestimmte E-Mail zu deaktivieren, deaktivieren Sie die Option **[!UICONTROL E-Mail-Öffnungen]** beim Erstellen Ihrer Nachricht. Wenn diese Option deaktiviert ist, verhindert sie, dass offene Tracking-Daten für diesen Versand erfasst werden. Für Organisationen, die Nachrichten an französische Abonnenten senden, überprüfen Sie vor dem Erzwingungsdatum die Einstellungen für das Öffnungs-Tracking für alle aktiven Journey und Kampagnen.

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[Erfahren Sie, wie Sie Ihre Nachrichten verfolgen können](../email/message-tracking.md)

### Tracking-Verwaltung auf Link-Ebene {#link-tracking}

Über den Umschalter für das Öffnungs-Tracking pro Nachricht hinaus bietet Adobe Journey Optimizers E-Mail-Designer eine granulare Kontrolle darüber, welche URLs verfolgt werden. Über das Bedienfeld **[!UICONTROL Links]** in der E-Mail-Designer können Autoren alle verfolgten URLs in einer Nachricht anzeigen und den Tracking-Modus für jeden Link einzeln festlegen.

Zu den verfügbaren Tracking-Modi für jeden Link gehören:

* **Verfolgt**: Aktiviert das Tracking dieser URL.
* **Opt-out**: Legt diese URL als Opt-out- oder Abmelde-URL fest.
* **Mirrorseite**: Legt diese URL als Mirrorseiten-Link fest.
* **Nie**: Das Tracking wird für diese URL unabhängig von den Einstellungen auf Nachrichtenebene nie aktiviert.

Das Festlegen spezifischer Links auf **Never** kann sicherstellen, dass bestimmte URLs nicht verfolgt werden, selbst wenn das Tracking auf Nachrichtenebene aktiviert ist.

[Erfahren Sie, wie Sie das Tracking in E-Mail Designer verwalten](../email/message-tracking.md#manage-tracking)

### Einverständniserfassung und -verwaltung {#consent-management}

Adobe Journey Optimizer verwaltet das Einverständnis über das Adobe Experience Platform (AEP) [Einverständnis- und Voreinstellungsschema](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=de){target="_blank"}. Einverständnisvoreinstellungen werden auf Profilebene gespeichert und beim Journey und bei der Kampagnenausführung automatisch durchgesetzt.

Zu den wichtigsten Einverständnisattributen, die für das E-Mail-Tracking relevant sind, gehören:

* **`consents.marketing.email.val`**: Das Feld für das primäre E-Mail-Marketing-Einverständnis. Der Wert `y` bedeutet Opt-in, `n` bedeutet Opt-out. Ein leerer Wert wird standardmäßig als Einverständnis behandelt (dieser Standardwert kann beim Onboarding geändert werden).

### Opt-out- und Ausstiegsmechanismen {#opt-out}

Adobe Journey Optimizer bietet Abonnentinnen und Abonnenten mehrere Mechanismen zum Opt-out von Nachrichten und zum Verwalten ihrer Voreinstellungen, die alle die Einverständnisattribute des Profils in Adobe Experience Platform aktualisieren.

**Abo mit einem Klick kündigen (E-Mail-Kopfzeile)**

Wenn die Option **[!UICONTROL Enable list-unsubscribe]** in der Konfiguration des E-Mail-Kanals aktiviert ist, werden eine 1-Klick-Abmelde-URL und eine Mailto-Adresse automatisch zum E-Mail-Header hinzugefügt. Empfänger können sich direkt von ihrem E-Mail-Client abmelden, ohne in den Textkörper der E-Mail zu klicken. Diese Option ist bei neuen Kanalkonfigurationen standardmäßig aktiviert.

[Erfahren Sie, wie Sie Listen-Abmeldungen konfigurieren](../email/list-unsubscribe.md)

**Opt-out mit einem Klick (E-Mail-Textkörper)**

Autoren können mit der E-Mail-Designer einen 1-Klick-Opt-out-Link direkt in den E-Mail-Inhalt einfügen. Wenn ein Empfänger auf diesen Link klickt, wird seine Voreinstellung sofort aktualisiert. Das Opt-out kann wie folgt behandelt werden:

* **Kanalebene**: Schließt das Profil aus allen künftigen E-Mail-Nachrichten über den Kanal aus.
* **Identitätsstufe**: Schließt die spezifische E-Mail-Adresse ab, die nur in der aktuellen Nachricht verwendet wird.

[Erfahren Sie, wie Sie einen Link zum Abmelden mit einem Klick hinzufügen.](../email/email-opt-out.md#one-click-opt-out)

**Präferenzzentrum über Landingpages**

Die native Landingpage-Funktion von Adobe Journey Optimizer ermöglicht Unternehmen den Aufbau von Präferenzzentren, in denen Abonnentinnen und Abonnenten ihre Kommunikations- und Tracking-Voreinstellungen verwalten können. Wenn ein Abonnent ein Formular eines Präferenzzentrums sendet, werden seine Auswahlmöglichkeiten in die AEP-Profilattribute in der Feldergruppe Einverständnis und Voreinstellungen zurückgeschrieben.

Bei CNIL-Compliance-Szenarien kann eine Landingpage des Präferenzzentrums über die E-Mail-Fußzeile verknüpft werden (im Gegensatz zum Abmelde-Link), sodass Empfängerinnen und Empfänger ihre Tracking-Voreinstellungen unabhängig von ihrem Abonnementstatus verwalten können.

[Erfahren Sie, wie Sie die Voreinstellungen Ihrer Kunden verwalten](../action/preference-center.md)

### Verarbeitung und Durchsetzung von Einverständnissen {#consent-enforcement}

Wenn sich ein Empfänger über einen der oben genannten Mechanismen abmeldet, geschieht Folgendes:

* Das Einverständnisattribut (`consents.marketing.email.val`) des Profils wird in Adobe Experience Platform auf `n` aktualisiert.
* Das Profil wird sofort von zukünftigen Marketing-E-Mail-Sendungen in Journey und Kampagnen ausgeschlossen.
* Die Opt-out-Informationen werden im Einverständnisdienst-Datensatz von AEP gespeichert.
* Journey Optimizer führt vor jedem Versand eine Einverständnisprüfung auf Kanalebene durch, um sicherzustellen, dass abgemeldete Profile keine Marketing-Nachrichten erhalten.

[Weitere Informationen zur Opt-out-Verwaltung](opt-out.md)

### Einverständniserklärungen {#consent-policies}

Unternehmen können in Adobe Journey Optimizer Einverständnisrichtlinien erstellen und durchsetzen, um sicherzustellen, dass nur Profile, die bestimmte Einverständniskriterien erfüllen, Nachrichten erhalten. Einverständnisrichtlinien können über Marketing-Aktionen mit Kanalkonfigurationen verknüpft werden.

[Erfahren Sie, wie Sie mit Einverständnisrichtlinien arbeiten](../action/consent.md)

### Unterdrückungsliste und erneute Anfrage {#suppression}

Adobe Journey Optimizer verwaltet automatisch eine Unterdrückungsliste mit E-Mail-Adressen, die zu Hardbounces, Softbounces oder Spam-Beschwerden führen. Profile auf der Unterdrückungsliste sind von zukünftigen Marketing-Sendungen ausgeschlossen.

Die Journey Optimizer-Unterdrückungs-REST-API bietet zusätzliche programmgesteuerte Kontrolle über ausgehende Nachrichten, sodass Unternehmen das Unterdrückungs- und Steuerungsverhalten über die API verwalten können.

[Informationen zum Verwalten der Unterdrückungsliste](../configuration/manage-suppression-list.md)

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### Berichterstellung {#reporting}

Die E-Mail-Berichte von Adobe Journey Optimizer bieten Öffnungs- und Klickmetriken über [Live-Berichte](../reports/live-report.md) und [Customer Journey Analytics-Berichte](../reports/report-gs-cja.md). Wenn **[!UICONTROL Geöffnete E-Mails]** das Tracking für eine Nachricht deaktiviert ist, werden für diesen Versand keine offenen Daten erfasst. Die Berichte spiegeln nur Klicks und andere Interaktionssignale wider.

