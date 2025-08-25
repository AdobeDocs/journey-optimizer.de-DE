---
solution: Journey Optimizer
product: journey optimizer
title: E-Mail-Fehlertypen
description: Rufen Sie die Liste aller möglichen E-Mail-Fehler beim Versand mit Journey Optimizer auf.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: weitere Zustellversuche, Bounce, soft, ignoriert, hard, Optimizer, Fehler
hide: true
hidefromtoc: true
exl-id: a8908b11-2288-4d53-897c-3f99cb5ceab4
source-git-commit: 0cb73489981659c3f231b9def40e0e483ed3aef8
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 100%

---

# E-Mail-Fehlertypen {#email-error-types}

Es gibt viele mögliche Ursachen für einen fehlgeschlagenen Versand. In der folgenden Tabelle sind alle Fehler, die beim Senden von E-Mail-Sendungen mit [!DNL Journey Optimizer] auftreten können, zusammen mit ihrer Beschreibung und dem Fehlertyp aufgeführt.

Diese Fehler finden Sie im [AJO-Nachrichten-Feedback-Ereignisdatensatz](../data/datasets-query-examples.md#message-feedback-event-dataset) der die Versand-Logs der Nachrichten enthält, einschließlich der Informationen über den gesamten Nachrichtenversand von [!DNL Journey Optimizer] und der Feedback-Einträge der E-Mail-ISPs zu Bounces.

| Bezeichnung des Fehlers | Fehlertyp | Technischer Wert | Beschreibung |
| --- | --- | --- | --- |
| **Unbestimmt** | Ignoriert | 1 | Die vom ISP empfangene SMTP-Bounce-Nachricht kann nicht klassifiziert werden. |
| **Ungültige Empfängerin bzw. ungültiger Empfänger** | Hardbounce | 10 | Die Adresse der Empfängerin bzw. des Empfängers ist ungültig. |
| **Empfängerin bzw. Empfänger abgelehnt** | Hardbounce | 15 | Der ISP der Empfängerin bzw. des Empfängers hat die Nachricht abgelehnt, und der ISP kann die Absenderin bzw. den Absender blockieren, wenn die Empfängerin bzw. der Empfänger nicht unterdrückt wird. |
| **Softbounce** | Softbounce | 20 | Bei der Nachricht ist ein vorübergehender Fehler aufgetreten. Der Versand kann bei zukünftigen weiteren Zustellversuchen erfolgreich sein. |
| **DNS-Fehler** | Softbounce | 21 | Beim Nachrichtenversand ist ein temporärer DNS-Fehler aufgetreten. Der Versand kann bei zukünftigen weiteren Zustellversuchen erfolgreich sein. |
| **Postfach voll** | Softbounce | 22 | Bei der Nachricht ist ein vorübergehender Versandfehler aufgetreten, da das Postfach der Empfängerin bzw. des Empfängers voll war. |
| **Zu groß** | Ignoriert | 23 | Bei der Nachricht ist ein temporärer Versandfehler aufgetreten, da die Nachrichtengröße das Limit der Empfängerin bzw. des Empfängers überschritten hat. |
| **Timeout** | Ignoriert | 24 | Der Nachrichtenversand ist entweder fehlgeschlagen, weil die Nachrichtengültigkeit abgelaufen ist, oder weil der Versand an den ISP zu lange gedauert hat. |
| **Admin-Fehler** | Admin | 25 | Der Versand ist aufgrund einer bestimmten Richtlinienkonfiguration in der E-Mail-Versandinfrastruktur fehlgeschlagen. |
| **Generischer Bounce: KEIN EMPFÄNGER** | Ignoriert | 30 | Die Nachricht konnte nicht zugestellt werden, da die Empfängerin bzw. der Empfänger nicht identifiziert wurde. |
| **Generischer Bounce** | Ignoriert | 40 | Bei der Nachricht ist aus unbestimmten Gründen ein vorübergehender Versandfehler aufgetreten. |
| **Mail-Sperre** | Ignoriert | 50 | Beim Versand ist ein vorübergehender Fehler aufgrund hoher Volumen- oder Ratenbeschränkungen des ISPs aufgetreten. |
| **Spam-Sperre** | Ignoriert | 51 | Beim Versand ist ein vorübergehender Fehler aufgetreten, da der ISP die Domains oder IPs der Absenderin bzw. des Absenders als bekannte Spam-Quelle betrachtete. |
| **Spam-Inhalt** | Ignoriert | 52 | Beim Versand ist ein vorübergehender Fehler aufgetreten, da der ISP den E-Mail-Inhalt als Spam klassifiziert hat. |
| **Weiterleitung verweigert** | Softbounce | 54 | Die Nachricht konnte nicht akzeptiert werden, da die Ziel-Domain nicht auf der Zulassungsliste zum Weiterleiten steht. |
| **Automatische Antwort** | Ignoriert | 60 | Diese Nachrichten werden von [!DNL Journey Optimizer] beim Empfang verworfen, es sei denn, die Weiterleitung ist aktiviert. |
| **Vorübergehender Fehler** | Ignoriert | 70 | Der Versand wird mit einer eingeschränkten Rate erneut versucht oder kann im Falle einer Aussetzung verschoben werden. |
| **Challenge-Response** | Softbounce | 100 | Der Versand kann dauerhaft fehlschlagen, da [!DNL Journey Optimizer] keinen Challenge-Response-Authentifizierungsmechanismus unterstützt. |
