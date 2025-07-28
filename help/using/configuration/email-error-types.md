---
solution: Journey Optimizer
product: journey optimizer
title: E-Mail-Fehlertypen
description: Rufen Sie die Liste aller möglichen E-Mail-Fehler beim Versand mit Journey Optimizer auf.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: weitere Zustellversuche, Bounce, Soft, Ignoriert, Hard, Optimizer, Fehler
hide: true
hidefromtoc: true
source-git-commit: 1e36871c2c975c81d018fabb3cff51d11c98962e
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 19%

---


# E-Mail-Fehlertypen

Mögliche Ursachen für einen fehlgeschlagenen Versand sind mehrere. In der folgenden Tabelle sind alle Fehler, die beim Senden von E-Mail-Sendungen mit [!DNL Journey Optimizer] auftreten können, zusammen mit ihrer Beschreibung und dem Fehlertyp aufgeführt.

Diese Fehler finden Sie im [AJO-Nachrichten-Feedback-Ereignisdatensatz](../data/datasets-query-examples.md#message-feedback-event-dataset) der die Versandlogs der Nachrichten enthält, einschließlich Informationen über den gesamten Nachrichtenversand von [!DNL Journey Optimizer] und Feedback-Datensätze von den E-Mail-ISPs zu Bounces.

| Bezeichnung des Fehlers | Fehlertyp | Technischer Wert | Beschreibung |
| --- | --- | --- | --- |
| **Unbestimmt** | Ignoriert | 1 | Die vom ISP empfangene SMTP-Bounce-Nachricht kann nicht klassifiziert werden. |
| **Ungültiger Empfänger** | Hardbounce | 10 | Die Empfängeradresse ist ungültig. |
| **Empfänger abgelehnt** | Hardbounce | 15 | Der ISP des Empfängers hat die Nachricht abgelehnt, und der ISP kann den Absender blockieren, wenn der Empfänger nicht unterdrückt wird. |
| **Soft-Bounce** | Softbounce | 20 | Bei der Nachricht ist ein vorübergehender Fehler aufgetreten. Dies kann bei zukünftigen weiteren Zustellversuchen erfolgreich sein. |
| **DNS-Fehler** | Softbounce | 21 | Beim Nachrichtenversand ist ein temporärer DNS-Fehler aufgetreten. Dies kann bei zukünftigen weiteren Zustellversuchen erfolgreich sein. |
| **Postfach voll** | Softbounce | 22 | Bei der Nachricht ist ein vorübergehender Versandfehler aufgetreten, da das Postfach des Empfängers voll war. |
| **Zu groß** | Ignoriert | 23 | Bei der Nachricht ist ein temporärer Versandfehler aufgetreten, da die Nachrichtengröße das Limit des Empfängers überschritten hat. |
| **Zeitüberschreitung** | Ignoriert | 24 | Der Nachrichtenversand ist entweder fehlgeschlagen, weil die Nachrichtengültigkeit abgelaufen ist, oder es hat zu lange gedauert, bis er an den ISP gesendet wurde. |
| **Administratorfehler** | Admin | 25 | Der Versand ist aufgrund einer Richtlinienkonfiguration in der E-Mail-Versandinfrastruktur fehlgeschlagen. |
| **Generischer Bounce: NO RCPT** | Ignoriert | 30 | Die Nachricht konnte nicht zugestellt werden, da der Empfänger nicht identifiziert wurde. |
| **Generischer Bounce** | Ignoriert | 40 | Bei der Nachricht ist aus unbestimmten Gründen ein vorübergehender Versand fehlgeschlagen. |
| **E-Mail-Block** | Ignoriert | 50 | Beim Versand ist ein vorübergehender Fehler aufgetreten, da der ISP hohe Volumen- oder Ratenbeschränkungen hatte. |
| **Spam-Block** | Ignoriert | 51 | Beim Versand ist ein vorübergehender Fehler aufgetreten, da der ISP die Domains oder IPs des Absenders als bekannte Spam-Quelle betrachtete. |
| **Spam-Inhalt** | Ignoriert | 52 | Beim Versand ist ein vorübergehender Fehler aufgetreten, da der ISP den E-Mail-Inhalt als Spam klassifiziert hat. |
| **Weiterleitung verweigert** | Softbounce | 54 | Die Nachricht konnte nicht akzeptiert werden, da die Ziel-Domain nicht auf der Zulassungsliste für das Weiterleiten steht. |
| **Automatische Antwort** | Ignoriert | 60 | Diese Nachrichten werden vom [!DNL Journey Optimizer] beim Empfang verworfen, es sei denn, die Weiterleitung ist aktiviert. |
| **Übertragungsfehler** | Ignoriert | 70 | Der Versand wird mit einer eingeschränkten Rate erneut versucht oder kann im Falle einer Aussetzung verschoben werden. |
| **Challenge-Response** | Softbounce | 100 | Der Versand kann dauerhaft fehlschlagen, da [!DNL Journey Optimizer] keinen Challenge-Response-Authentifizierungsmechanismus unterstützt. |
