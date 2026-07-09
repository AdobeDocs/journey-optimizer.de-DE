---
title: Erste Schritte mit In-App-Nachrichten
description: Erfahren Sie, wie Sie In-App-Benachrichtigungen mit Journey Optimizer senden.
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: In-App, Nachricht, Erstellung, Starten
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: cc5c44e2-54a1-4927-b794-442cd87d8f74
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 601
ht-degree: 44%

---

# Erste Schritte mit dem In-App-Kanal {#gs-in-app}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Unternehmen Sie die ersten Schritte mit dem In-App-Nachrichtenkanal in Adobe Journey Optimizer, um App-Benutzende mit Benachrichtigungen anzusprechen, die Funktionen, Angebote und Onboarding bewerben.

>[!ENDSHADEBOX]

In-App-Nachrichten sind Benachrichtigungen, die an Benutzerinnen und Benutzer in Ihrer App gesendet werden können und sie zu bestimmten Punkten von Interesse führen. Diese Benachrichtigungen können für verschiedene Zwecke verwendet werden, z. B. zur Förderung neuer Funktionen, zur Präsentation von Sonderangeboten oder zur Erleichterung des Onboardings von Benutzenden. Mithilfe von In-App-Nachrichten können Sie effektiv mit Ihrer Zielgruppe interagieren und diese auf wichtige Aspekte Ihrer Anwendung lenken.

Verwenden Sie Journey Optimizer, um In-App-Benachrichtigungen zu erstellen und Erlebnisoptionen zu konfigurieren, einschließlich des Nachrichten-Layouts und der Anzeige-, Text- und Schaltflächenoptionen.

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="Validierung" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>Konfigurieren des In-App-Kanals</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="Lead" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>Erstellen einer In-App-Nachricht</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="Gelegentlich" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>Gestalten Ihrer In-App-Inhalte</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="Validierung" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>Aufrufen von In-App-Berichten</strong></a>
</div>
<p>
</td>
</tr></table>

## Anwendungsszenarien

In-App-Nachrichten funktionieren am besten, wenn Sie Benutzer anleiten oder beeinflussen möchten, während sie bereits mit Ihrer App interagieren, und nutzen Sie diesen Moment der aktiven Aufmerksamkeit.

| Vorteil | Warum | Beispielhafte Anwendungsfälle |
| --- | --- | --- |
| Hohe Benutzerinteraktion | Erreicht Benutzer, während sie aktiv an einer App-Sitzung teilnehmen | Funktionsankündigungen, Onboarding-Tipps |
| Kontextuell relevante Trigger | Kann basierend auf dem In-App-Verhalten oder dem Ort ausgelöst werden | Hervorheben einer Funktion direkt nachdem ein Benutzer einen entsprechenden Bildschirm besucht hat |
| Versand in Echtzeit | Keine Abhängigkeit von Push-Token oder externen Versanddiensten | Zeitkritische Eingabeaufforderungen, die während der aktuellen Sitzung angezeigt werden |
| Keine Abhängigkeit von externen Kanälen | Funktioniert vollständig innerhalb der App, unabhängig vom Opt-in-Status für andere Kanäle | Benutzer erreichen, die sich gegen Push-Benachrichtigungen entschieden haben |
| Besseres Konversionspotenzial | Wird zu einem Zeitpunkt mit aktiver Aufmerksamkeit durchgeführt, wodurch die Reaktionsraten steigen | Upsell- oder Crosssell-Angebote, Umfrageaufforderungen |
| Anpassung und Segmentierung | Layout, Text und Schaltflächen können auf bestimmte Zielgruppen zugeschnitten werden | Personalisierte Onboarding-Abläufe für verschiedene Benutzersegmente |
| Unaufdringliches Design | Kann so gestaltet werden, dass es das Benutzererlebnis ergänzt und nicht unterbricht | Banner oder Modale, die an der Benutzeroberfläche der App ausgerichtet sind |

## Verwendung

In-App-Nachrichten hängen von einer aktiven Sitzung ab und sind daher nicht für jedes Szenario geeignet. Betrachten Sie in den folgenden Situationen einen anderen Kanal:

* Der Benutzer verwendet die App nicht aktiv, da die Nachricht nie angezeigt wird
* Die Nachricht ist ein kritisches oder zeitkritisches Problem, bei dem Benutzende außerhalb der App erreicht werden müssen, z. B. ein Ausfall oder eine Sicherheitswarnung
* Die Kommunikation ist gesetzlich vorgeschrieben oder erfordert eine Lesebestätigung, die In-App-Nachrichten nicht bereitstellen können
* Das Ziel ist die Reaktivierung des Kontos oder eine Win-back-Kampagne für inaktive Benutzer, die die App wahrscheinlich nicht öffnen werden
* Bei der Nachricht handelt es sich um eine Transaktionsaktualisierung mit hohem Volumen, z. B. eine Bestellbestätigung, die sich besser für E-Mail oder SMS eignet
* Überbeanspruchung kann zu Bannerblindheit führen, wodurch Benutzer anfangen, Nachrichten zu ignorieren, die zu oft angezeigt werden
* Benutzer sind möglicherweise offline oder ohne App-Konnektivität, wenn die Nachricht zugestellt werden soll



## Zusätzliche Ressourcen

* **[Erstellen von In-App-Nachrichten](create-in-app.md)** – Erfahren Sie, wie Sie In-App-Nachrichten für Apps erstellen und konfigurieren.
* **[Konfigurieren des In-App-Kanals](inapp-configuration.md)** – Richten Sie Ihren In-App-Nachrichtenkanal mit den richtigen App-Konfigurationen ein.
* **[Entwerfen von In-App-Inhalten](design-in-app.md)** – Passen Sie Layouts, Stile, Schaltflächen und interaktive Elemente von In-App-Nachrichten an.
* **[In-App für Web](create-in-app-web.md)** – Erfahren Sie, wie Sie In-App-Nachrichten für Web-Anwendungen erstellen und versenden.
* **[Tutorials zum In-App-Kanal](https://experienceleague.adobe.com/de/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}** – Erkunden Sie die detaillierten Video-Tutorials zu In-App-Messaging-Funktionen und Best Practices.

